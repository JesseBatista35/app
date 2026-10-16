   oc set env dc/sihdg-jboss8-tqs SEC_URL_SERV_AUTH=https://login.tqs.caixa/auth -n sihdg-tqs
   oc get pods -n sihdg-tqs | grep jboss8      # aguarde o novo pod 1/1 Running
   curl -sk https://sihdg-jboss8-tqs.apps.nprd.caixa/sihdg-api/api/seguranca/configuracao-seguranca; echo

      oc rsh <pod-novo> grep SEC_URL_SERV_AUTH /opt/server/standalone/configuration/standalone.xml
