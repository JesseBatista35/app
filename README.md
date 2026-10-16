oc logs sihdg-jboss8-tqs-45-lcc2c | grep -i "SEC_URL_SERV_AUTH"


oc set env dc/sihdg-jboss8-tqs SEC_URL_SERV_AUTH=https://login.tqs.caixa/auth -n sihdg-tqs
# isso gera um novo pod; aguarde ficar 1/1 Running
oc get pods -n sihdg-tqs | grep jboss8
curl -sk https://sihdg-jboss8-tqs.apps.nprd.caixa/sihdg-api/api/seguranca/configuracao-seguranca; echo
