O write e o reload falharam só porque ficaram sem o --controller: o management escuta no IP da VM, não no localhost. Repita os dois com ele:

bash
CLI="$JB/bin/jboss-cli.sh -c --controller=10.116.193.253:9990"

$CLI '/subsystem=modcluster/mod-cluster-config=configuration:write-attribute(name=node-timeout,value=600)'
$CLI ':reload'

O write deve responder "outcome" => "success" com "process-state" => "reload-required". O reload derruba a aplicação por alguns segundos.

Depois, confirme:

bash
sleep 30
$CLI '/subsystem=modcluster/mod-cluster-config=configuration:read-attribute(name=node-timeout)'
grep -n 'node-timeout' $CFG
$CLI ':read-attribute(name=server-state)'

O esperado é result => 600, a linha node-timeout="600" no XML e server-state => running.

Com isso, peça ao usuário para repetir a exportação. No 137, acompanhe:

bash
tail -f /logs/apache2/sigec-csc/sigec-csc.esteiras.tqs.caixa-access.log | grep exportarbase

Se aparecer status 200 com o último campo acima de 120000000, a correção está confirmada. Esse mesmo número mostra quanto a exportação realmente demora, e serve para a conversa com o dev sobre a query.
