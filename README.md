4.2$
-sh-4.2$
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
-sh-4.2$ oc get secret $S -o jsonpath='{range .metadata.managedFields[*]}{.manager}{"  "}{.time}{"\n"}{end}'
oc  2026-06-19T20:04:34Z
kubectl-patch  2026-10-14T14:02:21Z
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ BT=https://sicsn.caixa/BeyondTrust/api/public/v3
-sh-4.2$ CID=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d)
-sh-4.2$
-sh-4.2$
-sh-4.2$ CSEC=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d)
-sh-4.2$ curl -sk -m 30 -X POST "$BT/Auth/connect/token" \
>   -d "grant_type=client_credentials&client_id=$CID&client_secret=$CSEC" \
>   -w "\ntoken HTTP %{http_code}\n" | grep -v access_token; unset CID CSEC
{"error":"invalid_client"}
token HTTP 400
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get secret $S -o jsonpath='{range .metadata.managedFields[*]}{.manager}{"  "}{.time}{"\n"}{end}'
oc  2026-06-19T20:04:34Z
kubectl-patch  2026-10-14T14:02:21Z
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get netnamespace siifx-des -o jsonpath='{.egressIPs}{"\n"}'
[10.116.220.69]
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get egressip -o wide 2>/dev/null | grep -i siifx
-sh-4.2$ POD=$(oc get pod -l name=siifx-api-aplicacao-des --sort-by=.metadata.creationTimestamp -o name | tail -1)
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get $POD -o jsonpath='{.spec.nodeName}{"  "}{.status.hostIP}{"\n"}'
ceadecldlx029.nprd.caixa  10.116.208.49
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
