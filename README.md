**
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ BT=https://sicsn.caixa/BeyondTrust/api/public/v3
-sh-4.2$ S=bt-client-secret-siifx-api-aplicacao-des
-sh-4.2$ CID=$(oc get secret $S -n siifx-des -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d)
-sh-4.2$ CSEC=$(oc get secret $S -n siifx-des -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d)
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ TOKEN=$(curl -sk -m 30 -X POST "$BT/Auth/connect/token" \
>   -d "grant_type=client_credentials&client_id=$CID&client_secret=$CSEC" \
>   | sed -E 's/.*"access_token":"([^"]+)".*/\1/'); echo "token: ${TOKEN:0:15}..."
token: eyJhbGciOiJSUzI...
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -sk -m 30 -c /tmp/bt -X POST -d '' "$BT/Auth/SignAppIn" \
>   -H "Authorization: Bearer $TOKEN" -w "\nSignAppIn HTTP %{http_code}\n"
"Failed to authenticate due to one or more authentication rules."
SignAppIn HTTP 401
-sh-4.2$
-sh-4.2$
-sh-4.2$ for t in apikey_siifx_intranet sifxds01_oracle cli-ser-ifx_sso_intra siifx_api SIFXDS04_DATAGRID; do
>   echo "== $t"
>   curl -sk -m 60 -b /tmp/bt -H "Authorization: Bearer $TOKEN" \
>     -o /dev/null -w "HTTP %{http_code} em %{time_total}s\n" \
>     "$BT/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/&title=$t"
> done
== apikey_siifx_intranet
HTTP 401 em 0,141s
== sifxds01_oracle
HTTP 401 em 0,110s
== cli-ser-ifx_sso_intra
HTTP 401 em 0,104s
== siifx_api
HTTP 401 em 0,105s
== SIFXDS04_DATAGRID
HTTP 401 em 0,105s
-sh-4.2$
