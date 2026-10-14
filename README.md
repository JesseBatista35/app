S=bt-client-secret-siifx-api-aplicacao-des
oc get secret $S -o jsonpath='{.metadata.creationTimestamp}{"  "}{.metadata.resourceVersion}{"\n"}'
oc get secret $S -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d; echo
oc get secret $S -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d | wc -c
oc get secret $S -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d | grep -E '\$\(|#\{|__' && echo ">>> PLACEHOLDER NAO SUBSTITUIDO"
