
-sh-4.2$ POD=$(oc get pod -l name=siifx-api-aplicacao-des --sort-by=.metadata.creationTimestamp -o name | tail -1); echo $POD
pod/siifx-api-aplicacao-des-2899-9xk6r
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs $POD -c secrets-agent-sidecar | grep -E 'secret path|ERROR|UserName|sign_app'
2026-10-14 13:50:29,505 INFO (3792b7b0-c7d6-11f1-b7e6-0a5819011f6d) Calling sign_app_in endpoint: https://sicsn.caixa/BeyondTrust/api/public/v3
2026-10-14 13:50:29,546 INFO (3792b7b0-c7d6-11f1-b7e6-0a5819011f6d) **************** secret path: SIIFX_DES/apikey_siifx_intranet *****************
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get dc siifx-api-aplicacao-des -o jsonpath='{range .spec.template.spec.initContainers[?(@.name=="secrets-agent-sidecar")].env[*]}{.name}={.value}{.valueFrom}{"\n"}{end}'
SECRETS_PATH=/usr/src/app/secrets_files
BT_API_URL=https://sicsn.caixa/BeyondTrust/api/public/v3
CLIENT_ID=map[secretKeyRef:map[key:BT_CLIENT_ID name:bt-client-secret-siifx-api-aplicacao-des]]
CLIENT_SECRET=map[secretKeyRef:map[name:bt-client-secret-siifx-api-aplicacao-des key:BT_CLIENT_SECRET]]
BT_API_VERSION=3.1
SECRETS_LIST=SIIFX_DES/apikey_siifx_intranet,SIIFX_DES/sifxds01_oracle,SIIFX_DES/cli-ser-ifx_sso_intra,SIIFX_DES/siifx_api,SIIFX_DES/SIFXDS04_DATAGRID
BT_VERIFY_CA=False
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get dc siifx-caixinhas-api-aplicacao-des -o jsonpath='{range .spec.template.spec.initContainers[?(@.name=="secrets-agent-sidecar")].env[*]}{.name}={.value}{.valueFrom}{"\n"}{end}'
SECRETS_PATH=/usr/src/app/secrets_files
BT_API_URL=https://sicsn.caixa/BeyondTrust/api/public/v3
CLIENT_ID=map[secretKeyRef:map[name:bt-client-secret-siifx-caixinhas-api-aplicacao-des key:BT_CLIENT_ID]]
CLIENT_SECRET=map[secretKeyRef:map[key:BT_CLIENT_SECRET name:bt-client-secret-siifx-caixinhas-api-aplicacao-des]]
BT_API_VERSION=3.1
SECRETS_LIST=SIIFX_DES/apikey_siifx_intranet,SIIFX_DES/sifxds01_oracle,SIIFX_DES/cli-ser-ifx_sso_intra,SIIFX_DES/siifx_api,SIIFX_DES/SIFXDS04_DATAGRID
BT_VERIFY_CA=False
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs $POD -c secrets-agent-sidecar --previous | grep -E 'secret path|ERROR|UserName|sign_app'
Error from server (BadRequest): previous terminated container "secrets-agent-sidecar" in pod "siifx-api-aplicacao-des-2899-9xk6r" not found
-sh-4.2$
