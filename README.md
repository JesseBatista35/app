BT=https://sicsn.caixa/BeyondTrust/api/public/v3
S=bt-client-secret-siifx-api-aplicacao-des
CID=$(oc get secret $S -n siifx-des -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d)
CSEC=$(oc get secret $S -n siifx-des -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d)

# 1. token OAuth
TOKEN=$(curl -sk -m 30 -X POST "$BT/Auth/connect/token" \
  -d "grant_type=client_credentials&client_id=$CID&client_secret=$CSEC" \
  | sed -E 's/.*"access_token":"([^"]+)".*/\1/'); echo "token: ${TOKEN:0:15}..."

# 2. sign in
curl -sk -m 30 -c /tmp/bt -X POST "$BT/Auth/SignAppIn" -H "Authorization: Bearer $TOKEN"; echo

# 3. cada segredo, com tempo (retorna metadados, não o valor)
for t in apikey_siifx_intranet sifxds01_oracle cli-ser-ifx_sso_intra siifx_api SIFXDS04_DATAGRID; do
  echo "== $t"
  curl -sk -m 60 -b /tmp/bt -H "Authorization: Bearer $TOKEN" \
    -o /dev/null -w "HTTP %{http_code} em %{time_total}s\n" \
    "$BT/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/&title=$t"
done

# 4. pasta inteira
curl -sk -m 60 -b /tmp/bt -H "Authorization: Bearer $TOKEN" \
  -w "\nHTTP %{http_code} em %{time_total}s\n" \
  "$BT/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/"

# 5. sign out e limpeza
curl -sk -b /tmp/bt -X POST "$BT/Auth/Signout" -H "Authorization: Bearer $TOKEN"; rm -f /tmp/bt; unset CID CSEC TOKEN
