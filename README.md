# acompanhar os pods subindo
oc get pods -w | grep siifx-api-aplicacao

# assim que o pod novo aparecer, acompanhar o agente em tempo real
POD=$(oc get pod -l name=siifx-api-aplicacao-des --sort-by=.metadata.creationTimestamp -o name | tail -1); echo $POD
oc logs -f $POD -c secrets-agent-sidecar
