
-sh-4.2$
-sh-4.2$ oc logs sinfs-des-80-zlj8m -n sinfs-des -c secrets-agent-sidecar | grep -E "secret path|UserName|number of files|ERROR"
2026-10-13 14:44:57,086 INFO (a8a75b08-c714-11f1-9c11-0a58190313f6) **************** secret path: SINFS_DES/JCICSDIRECT *****************
2026-10-13 14:44:57,205 INFO (a8a75b08-c714-11f1-9c11-0a58190313f6) **************** secret path: SINFS_DES/SSO_SENHA *****************
2026-10-13 14:44:57,285 INFO (a8a75b08-c714-11f1-9c11-0a58190313f6) **************** secret path: SINFS_DES/TGNFSNFDV_SENHA *****************
2026-10-13 14:44:57,368 INFO (a8a75b08-c714-11f1-9c11-0a58190313f6) **************** secret path: SINFS_DES/TGSGRS142_SENHA *****************
2026-10-13 14:44:57,448 INFO (a8a75b08-c714-11f1-9c11-0a58190313f6) **************** secret path: SINFS_DES/TGSGRS143_SENHA *****************
2026-10-13 14:44:57,530 INFO (a8a75b08-c714-11f1-9c11-0a58190313f6) **************** secret path: SINFS_DES/TGSGRS144_SENHA *****************
2026-10-13 14:44:57,610 INFO (a8a75b08-c714-11f1-9c11-0a58190313f6) Creating files with the secrets as content, number of files 12
            "UserName": "clientid_SNFSDR01",
                "message": "Creating files with the secrets as content, number of files 12",
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get dc/sinfs-des -n sinfs-des -o jsonpath='{range .spec.template.spec.initContainers[0].env[*]}{.name}{" -> "}{.valueFrom}{"\n"}{end}'
SECRETS_PATH ->
BT_API_URL ->
CLIENT_ID -> map[secretKeyRef:map[name:bt-client-secret-sinfs-des key:BT_CLIENT_ID]]
CLIENT_SECRET -> map[secretKeyRef:map[name:bt-client-secret-sinfs-des key:BT_CLIENT_SECRET]]
BT_API_VERSION ->
SECRETS_LIST ->
BT_VERIFY_CA ->
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get dc/sinfs-des -n sinfs-des -o jsonpath='{.spec.template.spec.initContainers[0].envFrom}{"\n"}'

-sh-4.2$
-sh-4.2$
-sh-4.2$
