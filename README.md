
-sh-4.2$
-sh-4.2$
-sh-4.2$ POD=$(oc get pod -l name=siifx-api-aplicacao-des --sort-by=.metadata.creationTimestamp -o name | tail -1); echo $POD
Error from server (Forbidden): pods is forbidden: User "p585600@corp.caixa.gov.br" cannot list resource "pods" in API group "" in the namespace "siifx-des"

-sh-4.2$ oc logs -f $POD -c secrets-agent-sidecar | grep -E 'secret path|ERROR|number of files|Timeout'
error: expected 'logs (POD | TYPE/NAME) [CONTAINER_NAME]'.
POD or TYPE/NAME is a required argument for the logs command
See 'oc logs -h' for help and examples.
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$   for s in bt-client-secret-siifx-api-aplicacao-des bt-client-secret-siifx-caixinhas-api-aplicacao-des; do
>     echo -n "$s: "; oc get secret $s -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d; echo
>   done
bt-client-secret-siifx-api-aplicacao-des: Error from server (Forbidden): secrets "bt-client-secret-siifx-api-aplicacao-des" is forbidden: User "p585600@corp.caixa.gov.br" cannot get resource "secrets" in API group "" in the namespace "siifx-des"

bt-client-secret-siifx-caixinhas-api-aplicacao-des: Error from server (Forbidden): secrets "bt-client-secret-siifx-caixinhas-api-aplicacao-des" is forbidden: User "p585600@corp.caixa.gov.br" cannot get resource "secrets" in API group "" in the namespace "siifx-des"

-sh-4.2$
