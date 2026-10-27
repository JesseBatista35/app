oc get dc sispi-qrcode-api-validador-des -n sispi-des -o jsonpath='{.status.latestVersion}{"\n"}'
# se ainda for 309: oc rollout latest dc/sispi-qrcode-api-validador-des -n sispi-des
oc get pods -n sispi-des -l deploymentconfig=sispi-qrcode-api-validador-des -w

POD=<pod novo>
oc exec $POD -n sispi-des -c sispi-qrcode-api-validador-des -- kill -3 1
oc logs $POD -n sispi-des -c sispi-qrcode-api-validador-des | grep -A 40 '"main"'

oc exec $POD -n sispi-des -c istio-proxy -- bash -c 'timeout 5 bash -c "</dev/tcp/10.116.101.16/1521" && echo ORACLE_OK || echo ORACLE_FALHA'
oc exec $POD -n sispi-des -c istio-proxy -- bash -c 'timeout 5 bash -c "</dev/tcp/cnpexdadvm01-scan4.extra.caixa.gov.br/1521" && echo SPX_OK || echo SPX_FALHA'
