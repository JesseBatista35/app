POD=$(oc get pod -l name=siifx-api-aplicacao-des --sort-by=.metadata.creationTimestamp -o name | tail -1)
oc logs $POD -c secrets-agent-sidecar | grep -m1 -oE '\([0-9a-f-]{36}\)'
