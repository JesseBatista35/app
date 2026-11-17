Passo a passo no 471 (10.116.97.59)

1. Backup do domain.xml (no bash do 471)

bash
JH=$(ps -ef | grep -o 'jboss.home.dir=[^ ]*' | head -1 | cut -d= -f2); echo $JH
cp -p $JH/domain/configuration/domain.xml /tmp/domain.xml.bkp_ccr_$(date +%Y%m%d_%H%M)
ls -l /tmp/domain.xml.bkp_ccr_*

Se o cp falhar porque o arquivo não existe, siga mesmo assim. O snapshot do passo 2 cobre o backup.

2. Entrar no CLI, tirar o snapshot e salvar a configuração atual

$JH/bin/jboss-cli.sh --connect --controller=10.116.97.59:9990

Já dentro do CLI:

:take-snapshot
/profile=full-ha-sifec-intranet/subsystem=keycloak/secure-deployment=ccr-api.war:read-resource(recursive=true)

Copie a saída do read-resource e guarde. É o seu rollback. Ela deve mostrar realm => "internet", resource => "cli-ser-fec_api" e bearer-only => true.

3. Remover

/profile=full-ha-sifec-intranet/subsystem=keycloak/secure-deployment=ccr-api.war:remove

4. Redeploy do CCR (sem precisar reiniciar o SIFEC inteiro)

/server-group=sifec-intranet/deployment=SIFEC-CCR:redeploy

Me manda a saída dos passos 2, 3 e 4 antes de seguir.

5. Validar

O Matheus testa o /v8/contratos/simular com token intranet e com token internet.
No 473, acompanhe o mesmo server.log em que você viu o ORA-25156:
bash
grep -aiE "keycloak|ccr-api|401|403" <mesmo arquivo do ORA-25156> | tail -30

Se ainda der 401 depois do redeploy, o servidor ficou com o adapter em memória. Nesse caso é preciso reiniciar o server-group. Isso derruba todo o SIFEC por alguns minutos, então só fazemos combinando antes na sala.

Rollback, se precisar (no CLI do 471):

/profile=full-ha-sifec-intranet/subsystem=keycloak/secure-deployment=ccr-api.war:add(realm=internet,resource=cli-ser-fec_api,bearer-only=true)
/server-group=sifec-intranet/deployment=SIFEC-CCR:redeploy
Mensagem corrigida para registrar na sala (depois de aplicar)

Decisão: CCR-API (JBoss 7.4, DES), validação de token Keycloak

Contexto: no 7.4, o subsystem Keycloak tinha um secure-deployment para o ccr-api.war no realm internet. Com isso, o container validava o token antes da aplicação, mesmo sem login-config no web.xml, e recusava com 401 os consumidores que usam token do realm intranet. No 6.4 essa validação pelo container não acontecia: é a própria aplicação que trata o token dos dois realms.

Decisão (alinhada com Alessandro, Paulo e Gustavo): em DES, remover o secure-deployment do ccr-api.war, igualando ao 6.4.

Ações realizadas: backup do domain.xml e snapshot do domain, configuração original guardada para rollback, remoção do secure-deployment e redeploy do SIFEC-CCR.

Pendências:

Teste com token intranet e internet (Matheus).
Confirmação, pelo responsável do CCR, de que a aplicação valida o token, já que em DES o container deixou de validar.
Nos ambientes seguintes e em produção, prever a segregação intranet/internet, o que vale também para os demais pacotes SIFEC que atendem internet.
O ORA-25156 (dialeto Oracle) segue com o dev, separado do 401.

Antes de aplicar, vale avisar na sala que vai haver o redeploy do CCR, porque o CCR fica indisponível por alguns segundos.
