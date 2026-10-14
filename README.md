
-sh-4.2$
-sh-4.2$
-sh-4.2$ POD=$(oc get pod -l name=siifx-api-aplicacao-des --sort-by=.metadata.creationTimestamp -o name | tail -1); echo $POD
pod/siifx-api-aplicacao-des-2905-27xhf
-sh-4.2$ oc logs -f $POD -c secrets-agent-sidecar | grep -E 'secret path|ERROR|number of files|Timeout'
2026-10-14 16:35:50,637 INFO (50fb3c38-c7ed-11f1-a383-0a58190120f2) **************** secret path: SIIFX_DES/apikey_siifx_intranet *****************
2026-10-14 16:37:52,033 ERROR (50fb3c38-c7ed-11f1-a383-0a58190120f2) General error with secrets_safe.SecretsSafe: HTTPSConnectionPool(host='sicsn.caixa', port=443): Max retries exceeded with url: /BeyondTrust/api/public/v3/secrets-safe/secrets?path=SIIFX_DES&separator=%2F&version=3.1&title=apikey_siifx_intranet (Caused by ReadTimeoutError("HTTPSConnectionPool(host='sicsn.caixa', port=443): Read timed out. (read timeout=30)"))
2026-10-14 16:37:52,033 INFO (50fb3c38-c7ed-11f1-a383-0a58190120f2) Creating files with the secrets as content, number of files 0
                "message": "Creating files with the secrets as content, number of files 0",
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$   for s in bt-client-secret-siifx-api-aplicacao-des bt-client-secret-siifx-caixinhas-api-aplicacao-des; do
>     echo -n "$s: "; oc get secret $s -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d; echo
>   done
bt-client-secret-siifx-api-aplicacao-des: 7bee4ea6-f78e-4291-ac59-330aa1f9da82
bt-client-secret-siifx-caixinhas-api-aplicacao-des: 7bee4ea6-f78e-4291-ac59-330aa1f9da82
-sh-4.2$ for d in siifx-api-aplicacao-des siifx-caixinhas-api-aplicacao-des; do
>   echo "== $d"; oc get dc $d -o jsonpath='{.spec.template.spec.initContainers[?(@.name=="secrets-agent-sidecar")].env[?(@.name=="SECRETS_LIST")].value}'; echo
> done
== siifx-api-aplicacao-des
SIIFX_DES/apikey_siifx_intranet,SIIFX_DES/sifxds01_oracle,SIIFX_DES/cli-ser-ifx_sso_intra,SIIFX_DES/siifx_api,SIIFX_DES/SIFXDS04_DATAGRID
== siifx-caixinhas-api-aplicacao-des
SIIFX_TGE/apikey_siifx_intranet,SIIFX_TGE/sifxgs01_oracle,SIIFX_TGE/cli-ser-ifx_sso_intra
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs siifx-caixinhas-api-aplicacao-des-72-rkr7s -c secrets-agent-sidecar | grep -E 'secret path|ERROR|number of files'
2026-10-14 16:14:00,811 INFO (443fda10-c7ea-11f1-a15a-0a5819022063) **************** secret path: SIIFX_DES/apikey_siifx_intranet *****************
2026-10-14 16:14:00,924 INFO (443fda10-c7ea-11f1-a15a-0a5819022063) **************** secret path: SIIFX_DES/sifxds01_oracle *****************
2026-10-14 16:14:00,997 INFO (443fda10-c7ea-11f1-a15a-0a5819022063) **************** secret path: SIIFX_DES/cli-ser-ifx_sso_intra *****************
2026-10-14 16:14:01,084 INFO (443fda10-c7ea-11f1-a15a-0a5819022063) **************** secret path: SIIFX_DES/siifx_api *****************
2026-10-14 16:14:01,161 INFO (443fda10-c7ea-11f1-a15a-0a5819022063) **************** secret path: SIIFX_DES/SIFXDS04_DATAGRID *****************
2026-10-14 16:14:01,233 INFO (443fda10-c7ea-11f1-a15a-0a5819022063) Creating files with the secrets as content, number of files 10
                "message": "Creating files with the secrets as content, number of files 10",
-sh-4.2$
