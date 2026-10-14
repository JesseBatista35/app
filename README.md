
-sh-4.2$
-sh-4.2$ S=bt-client-secret-siifx-api-aplicacao-des
-sh-4.2$ oc get secret $S -o jsonpath='{.metadata.creationTimestamp}{"  "}{.metadata.resourceVersion}{"\n"}'
2025-07-30T22:17:52Z  2260597766
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get secret $S -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d; echo
639dc38f-1006-4e3f-abab-836500019823
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get secret $S -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d | wc -c
44
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get secret $S -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d | grep -E '\$\(|#\{|__' && echo ">>> PLACEHOLDER NAO SUBSTITUIDO"
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
