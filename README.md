
-sh-4.2$
-sh-4.2$ os rsh sihdg-jboss8-tqs-46-h6zlf
-sh: os: comando não encontrado
-sh-4.2$ oc rsh sihdg-jboss8-tqs-46-h6zlf env | grep SEC_URL_SERV_AUTH
SEC_URL_SERV_AUTH=https://login.tqs.caixa/auth
-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -sk https://sihdg-jboss8-tqs.apps.nprd.caixa/sihdg-api/api/seguranca/configuracao-seguranca; echo
{"realm":"intranet","idCliente":"cli-web-hdg","urlServidorAutorizacao":"https://login.tqs.caixa/auth","tempoVidaToken":300,"tempoMaximoIdle":-1,"versaoApi":"3.22.0.3"}
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
