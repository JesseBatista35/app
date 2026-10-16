****# 1) a variável está no DC?
oc set env dc/sihdg-jboss8-tqs --list -n sihdg-tqs | grep SEC_URL_SERV_AUTH

# se não aparecer, aplica:
oc set env dc/sihdg-jboss8-tqs SEC_URL_SERV_AUTH=https://login.tqs.caixa/auth -n sihdg-tqs

# 2) forçar novo deploy
oc rollout latest dc/sihdg-jboss8-tqs -n sihdg-tqs

# 3) acompanhar
oc rollout status dc/sihdg-jboss8-tqs -n sihdg-tqs
oc get pods -n sihdg-tqs | grep jboss8


oc rsh <pod-46> env | grep SEC_URL_SERV_AUTH
curl -sk https://sihdg-jboss8-tqs.apps.nprd.caixa/sihdg-api/api/seguranca/configuracao-seguranca; echo
