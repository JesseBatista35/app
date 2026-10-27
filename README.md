-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get dc sispi-qrcode-api-validador-des -n sispi-des -o jsonpath='{.status.latestVersion}{"\n"}'
311
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods -n sispi-des -l deploymentconfig=sispi-qrcode-api-validador-des -w
NAME                                       READY     STATUS    RESTARTS   AGE
sispi-qrcode-api-validador-des-297-6jjtp   1/2       Running   4          9m
sispi-qrcode-api-validador-des-311-9wrn4   1/2       Running   0          1m
^C-sh-4.2$ POD=sispi-qrcode-api-validador-des-311-9wrn4
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec $POD -n sispi-des -c sispi-qrcode-api-validador-des -- kill -3 1
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs $POD -n sispi-des -c sispi-qrcode-api-validador-des | grep -A 40 '"main"'
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec $POD -n sispi-des -c istio-proxy -- bash -c 'timeout 5 bash -c "</dev/tcp/10.116.101.16/1521" && echo ORACLE_OK || echo ORACLE_FALHA'
ORACLE_OK
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec $POD -n sispi-des -c istio-proxy -- bash -c 'timeout 5 bash -c "</dev/tcp/cnpexdadvm01-scan4.extra.caixa.gov.br/1521" && echo SPX_OK || echo SPX_FALHA'
SPX_OK
-sh-4.2$
-sh-4.2$
-sh-4.2$
