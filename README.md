oc get pods -n sihdg-tqs | grep jboss8
oc rsh <pod-jboss8-novo> grep SEC_URL_SERV_AUTH /opt/server/standalone/configuration/standalone.xml
curl -sk https://sihdg-jboss8-tqs.apps.nprd.caixa/sihdg-api/api/seguranca/configuracao-seguranca; echo
