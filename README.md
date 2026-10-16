# A) Ver o que o endpoint devolve (a resposta deve trazer a URL do SSO)
curl -sk https://sihdg-jboss8-tqs.apps.nprd.caixa/sihdg-api/api/seguranca/configuracao-seguranca
#   (ou abra essa URL direto no navegador; se der erro, veja a aba Console do F12: CORS? cert? 503?)

# B) Entrar no backend CERTO
oc rsh sihdg-jboss8-tqs-44-6jtfq
grep -rn -iE "login\.(des|tqs)" $JBOSS_HOME/standalone/configuration/ 2>/dev/null
grep -rn -iE "login\.(des|tqs)" /opt /deployments 2>/dev/null | grep -v "\.jar:" | head
env | grep -iE "login|sso|auth|keycloak|oidc"
ps -ef | grep -o "\-c [^ ]*\|--server-config=[^ ]*"   # qual standalone está em uso

# C) Log do jboss8 (subiu ok? erro no endpoint?)
oc logs sihdg-jboss8-tqs-44-6jtfq | grep -iE "error|exception|login\.|started in" | tail -30



command terminated with exit code 1
-sh-4.2$ curl -sk https://sihdg-jboss8-tqs.apps.nprd.caixa/sihdg-api/api/seguranca/configuracao-seguranca
{"realm":"intranet","idCliente":"cli-web-hdg","urlServidorAutorizacao":"https://login.des.caixa/auth","tempoVidaToken":300,"tempoMaximoIdle":-1,"versaoApi":"3.22.0.1"}-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc rsh sihdg-jboss8-tqs-44-6jtfq
sh-5.1$
sh-5.1$
sh-5.1$ grep -rn -iE "login\.(des|tqs)" $JBOSS_HOME/standalone/configuration/ 2>/dev/null
grep -rn -iE "login\.(des|tqs)" /opt /deployments 2>/dev/null | grep -v "\.jar:" | head
env | grep -iE "login|sso|auth|keycloak|oidc"
ps -ef | grep -o "\-c [^ ]*\|--server-config=[^ ]*"   # qual standalone está em uso
/opt/server/standalone/configuration/standalone.xml:337:                <auth-server-url>https://login.tqs.caixa/auth</auth-server-url>
/opt/server/standalone/configuration/standalone_xml_history/standalone.initial.xml:337:                <auth-server-url>https://login.tqs.caixa/auth</auth-server-url>
/opt/server/standalone/configuration/standalone_xml_history/standalone.last.xml:337:                <auth-server-url>https://login.tqs.caixa/auth</auth-server-url>
/opt/server/standalone/configuration/standalone_xml_history/standalone.boot.xml:337:                <auth-server-url>https://login.tqs.caixa/auth</auth-server-url>
/opt/server/standalone/configuration/standalone.xml:337:                <auth-server-url>https://login.tqs.caixa/auth</auth-server-url>
/opt/server/standalone/configuration/standalone_xml_history/standalone.initial.xml:337:                <auth-server-url>https://login.tqs.caixa/auth</auth-server-url>
/opt/server/standalone/configuration/standalone_xml_history/standalone.last.xml:337:                <auth-server-url>https://login.tqs.caixa/auth</auth-server-url>
/opt/server/standalone/configuration/standalone_xml_history/standalone.boot.xml:337:                <auth-server-url>https://login.tqs.caixa/auth</auth-server-url>
SSO_DEFAULT_PROVIDER_NAME=rh-sso
sh: ps: command not found
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$ oc logs sihdg-jboss8-tqs-44-6jtfq | grep -iE "error|exception|login\.|started in" | tail -30
sh: oc: command not found
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
