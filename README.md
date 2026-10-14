
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ POD=$(oc get pod -l name=siifx-api-aplicacao-des --sort-by=.metadata.creationTimestamp -o name | tail -1)
-sh-4.2$ oc logs $POD -c secrets-agent-sidecar | grep -m1 -oE '\([0-9a-f-]{36}\)'
(02e7bd44-c7ef-11f1-9d89-0a5819011a70)
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
