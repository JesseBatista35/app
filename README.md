bash
JB=/opt/jboss/jboss-eap
CFG=$JB/standalone/configuration/standalone-full-ha.xml
cp -p $CFG $CFG.bkp.$(date +%Y%m%d%H%M)

# ler o valor atual (deve vir undefined)
$JB/bin/jboss-cli.sh -c '/subsystem=modcluster/mod-cluster-config=configuration:read-attribute(name=node-timeout)'

Se der erro de conexão, repita acrescentando --controller=10.116.193.253:9990 logo depois do -c. Se a leitura funcionar:

bash
$JB/bin/jboss-cli.sh -c '/subsystem=modcluster/mod-cluster-config=configuration:write-attribute(name=node-timeout,value=600)'
$JB/bin/jboss-cli.sh -c ':reload'

O :reload deixa a aplicação fora do ar por alguns segundos em TQS. Escolha um momento sem teste em andamento.

Validar
bash
# na 765: confirmar que gravou no XML
grep -n 'node-timeout' $CFG

# no 137: o nó deve reaparecer no mod_cluster-manager
curl -s http://10.116.223.233/mod_cluster-manager | grep -iE 'node|timeout' | head -20

Depois, peça ao usuário para repetir a exportação. No 137, acompanhe o access log: o tempo (último campo) deve passar de 120000000 sem 504.

bash
tail -f /logs/apache2/sigec-csc/sigec-csc.esteiras.tqs.caixa-access.log | grep exportarbase

Atenção à persistência: a task "Configurando JBoss" da esteira pode regerar o standalone-full-ha.xml na próxima release e apagar o node-timeout. Depois que o teste passar, vale ver no template do esteira-jboss-vm se dá para parametrizar esse valor.
