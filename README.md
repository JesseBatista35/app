
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods -n sihdg-tqs | grep jboss8
sihdg-jboss8-tqs-44-deploy      0/1       Completed   0          71m
sihdg-jboss8-tqs-45-deploy      0/1       Completed   0          3m20s
sihdg-jboss8-tqs-45-lcc2c       1/1       Running     0          3m17s
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc rsh sihdg-jboss8-tqs-45-lcc2c grep SEC_URL_SERV_AUTH /opt/server/standalone/configuration/standalone.xml
command terminated with exit code 1
-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -sk https://sihdg-jboss8-tqs.apps.nprd.caixa/sihdg-api/api/seguranca/configuracao-seguranca; echo
{"realm":"intranet","idCliente":"cli-web-hdg","urlServidorAutorizacao":"https://login.des.caixa/auth","tempoVidaToken":300,"tempoMaximoIdle":-1,"versaoApi":"3.22.0.3"}
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc rsh sihdg-jboss8-tqs-45-lcc2c grep SEC_URL_SERV_AUTH /opt/server/standalone/configuration/standalone.xml
command terminated with exit code 1
-sh-4.2$ oc get pods
NAME                            READY     STATUS      RESTARTS   AGE
sihdg-angular18-tqs-27-deploy   0/1       Completed   0          72m
sihdg-angular18-tqs-28-deploy   0/1       Completed   0          55m
sihdg-angular18-tqs-28-xw6jj    2/2       Running     0          55m
sihdg-backend-tqs-142-deploy    0/1       Completed   0          87d
sihdg-backend-tqs-143-deploy    0/1       Completed   0          41d
sihdg-backend-tqs-143-wltb8     1/1       Running     0          41d
sihdg-frontend-tqs-78-deploy    0/1       Completed   0          235d
sihdg-frontend-tqs-79-deploy    0/1       Completed   0          150d
sihdg-frontend-tqs-79-lb6fz     2/2       Running     0          150d
sihdg-jboss8-tqs-44-deploy      0/1       Completed   0          72m
sihdg-jboss8-tqs-45-deploy      0/1       Completed   0          4m9s
sihdg-jboss8-tqs-45-lcc2c       1/1       Running     0          4m6s
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
