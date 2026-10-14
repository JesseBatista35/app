# quando a secret foi alterada por último
oc get secret $S -o jsonpath='{range .metadata.managedFields[*]}{.manager}{"  "}{.time}{"\n"}{end}'

# testar o token com o valor atual
BT=https://sicsn.caixa/BeyondTrust/api/public/v3
CID=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d)
CSEC=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d)
curl -sk -m 30 -X POST "$BT/Auth/connect/token" \
  -d "grant_type=client_credentials&client_id=$CID&client_secret=$CSEC" \
  -w "\ntoken HTTP %{http_code}\n" | grep -v access_token; unset CID CSEC
