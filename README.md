sh-4.2$
-sh-4.2$ IMG=$(oc get dc siifx-api-aplicacao-des -o jsonpath='{.spec.template.spec.initContainers[?(@.name=="secrets-agent-sidecar")].image}')
-sh-4.2$ S=bt-client-secret-siifx-api-aplicacao-des
-sh-4.2$
-sh-4.2$
-sh-4.2$ CID=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d)
-sh-4.2$
-sh-4.2$
-sh-4.2$ CSEC=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d)
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc run bt-test --rm -it --restart=Never --image="$IMG" --env="CID=$CID" --env="CSEC=$CSEC" --command -- sh
If you don't see a command prompt, try pressing enter.
/usr/src/app #
/usr/src/app # unset CID CSEC
/usr/src/app #
/usr/src/app #
/usr/src/app # ^C

/usr/src/app # BT=https://sicsn.caixa/BeyondTrust/api/public/v3
/usr/src/app # TOKEN=$(curl -sk -m 30 -X POST "$BT/Auth/connect/token" -d "grant_type=client_credentials&client_id=$CID&client_secret=$CSEC" | sed -E 's/.*"access_token":"([^"]+)".*/\1/')
sh: curl: not found
/usr/src/app # curl -sk -m 30 -c /tmp/bt -X POST -d '' "$BT/Auth/SignAppIn" -H "Authorization: Bearer $TOKEN" -o /dev/null -w "SignAppIn HTTP %{http_code}\n"
sh: curl: not found
/usr/src/app # for t in sifxds01_oracle cli-ser-ifx_sso_intra siifx_api SIFXDS04_DATAGRID apikey_siifx_intranet; do
>   echo "== $t"; curl -sk -m 60 -b /tmp/bt -H "Authorization: Bearer $TOKEN" -o /dev/null \
>     -w "HTTP %{http_code} em %{time_total}s\n" "$BT/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/&title=$t"
> done
== sifxds01_oracle
sh: curl: not found
== cli-ser-ifx_sso_intra
sh: curl: not found
== siifx_api
sh: curl: not found
== SIFXDS04_DATAGRID
sh: curl: not found
== apikey_siifx_intranet
sh: curl: not found
/usr/src/app #
/usr/src/app #
/usr/src/app #
/usr/src/app # exit
pod "bt-test" deleted
pod siifx-des/bt-test terminated (Error)
-sh-4.2$ ^C
-sh-4.2$ BT=https://sicsn.caixa/BeyondTrust/api/public/v3
-sh-4.2$ TOKEN=$(curl -sk -m 30 -X POST "$BT/Auth/connect/token" -d "grant_type=client_credentials&client_id=$CID&client_secret=$CSEC" | sed -E 's/.*"access_token":"([^"]+)".*/\1/')
-sh-4.2$ curl -sk -m 30 -c /tmp/bt -X POST -d '' "$BT/Auth/SignAppIn" -H "Authorization: Bearer $TOKEN" -o /dev/null -w "SignAppIn HTTP %{http_code}\n"
SignAppIn HTTP 401
-sh-4.2$ for t in sifxds01_oracle cli-ser-ifx_sso_intra siifx_api SIFXDS04_DATAGRID apikey_siifx_intranet; do
>   echo "== $t"; curl -sk -m 60 -b /tmp/bt -H "Authorization: Bearer $TOKEN" -o /dev/null \
>     -w "HTTP %{http_code} em %{time_total}s\n" "$BT/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/&title=$t"
> done
== sifxds01_oracle
HTTP 401 em 0,114s
== cli-ser-ifx_sso_intra
HTTP 401 em 0,106s
== siifx_api
HTTP 401 em 0,105s
== SIFXDS04_DATAGRID
HTTP 401 em 0,103s
== apikey_siifx_intranet
HTTP 401 em 0,102s
-sh-4.2$
