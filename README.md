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
