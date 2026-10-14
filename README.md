IMG=$(oc get dc siifx-api-aplicacao-des -o jsonpath='{.spec.template.spec.initContainers[?(@.name=="secrets-agent-sidecar")].image}')
S=bt-client-secret-siifx-api-aplicacao-des
CID=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d)
CSEC=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d)
oc run bt-test --rm -it --restart=Never --image="$IMG" --env="CID=$CID" --env="CSEC=$CSEC" --command -- sh
unset CID CSEC

BT=https://sicsn.caixa/BeyondTrust/api/public/v3
TOKEN=$(curl -sk -m 30 -X POST "$BT/Auth/connect/token" -d "grant_type=client_credentials&client_id=$CID&client_secret=$CSEC" | sed -E 's/.*"access_token":"([^"]+)".*/\1/')
curl -sk -m 30 -c /tmp/bt -X POST -d '' "$BT/Auth/SignAppIn" -H "Authorization: Bearer $TOKEN" -o /dev/null -w "SignAppIn HTTP %{http_code}\n"
for t in sifxds01_oracle cli-ser-ifx_sso_intra siifx_api SIFXDS04_DATAGRID apikey_siifx_intranet; do
  echo "== $t"; curl -sk -m 60 -b /tmp/bt -H "Authorization: Bearer $TOKEN" -o /dev/null \
    -w "HTTP %{http_code} em %{time_total}s\n" "$BT/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/&title=$t"
done
exit
