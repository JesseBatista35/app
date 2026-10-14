S=bt-client-secret-siifx-api-aplicacao-des
BT=https://sicsn.caixa/BeyondTrust/api/public/v3

# 1. confirmar que a release já aplicou (o horário do kubectl-patch tem que mudar)
oc get secret $S -o jsonpath='{range .metadata.managedFields[*]}{.manager}{"  "}{.time}{"\n"}{end}'

# 2. testar o token com o valor que está lá agora
CID=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d)
CSEC=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d)
curl -sk -m 30 -X POST "$BT/Auth/connect/token" \
  -d "grant_type=client_credentials&client_id=$CID&client_secret=$CSEC" \
  -o /dev/null -w "token HTTP %{http_code}\n"; unset CID CSEC

# 3. acompanhar o agente no pod novo
POD=$(oc get pod -l name=siifx-api-aplicacao-des --sort-by=.metadata.creationTimestamp -o name | tail -1); echo $POD
oc logs -f $POD -c secrets-agent-sidecar | grep -E 'secret path|ERROR|number of files|Timeout'
