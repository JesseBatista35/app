POD=$(oc get pod -l name=siifx-api-aplicacao-des --sort-by=.metadata.creationTimestamp -o name | tail -1); echo $POD
oc logs -f $POD -c secrets-agent-sidecar | grep -E 'secret path|ERROR|number of files|Timeout'

  for s in bt-client-secret-siifx-api-aplicacao-des bt-client-secret-siifx-caixinhas-api-aplicacao-des; do
    echo -n "$s: "; oc get secret $s -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d; echo
  done
