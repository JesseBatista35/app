
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
-sh-4.2$ S=bt-client-secret-siifx-api-aplicacao-des
-sh-4.2$ BT=https://sicsn.caixa/BeyondTrust/api/public/v3
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get secret $S -o jsonpath='{range .metadata.managedFields[*]}{.manager                                                                                                                    }{"  "}{.time}{"\n"}{end}'
oc  2026-06-19T20:04:34Z
kubectl-patch  2026-10-14T14:12:18Z
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ CID=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d)
-sh-4.2$ CSEC=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -                                                                                                                    d)
-sh-4.2$ curl -sk -m 30 -X POST "$BT/Auth/connect/token" \
>   -d "grant_type=client_credentials&client_id=$CID&client_secret=$CSEC" \
>   -o /dev/null -w "token HTTP %{http_code}\n"; unset CID CSEC
token HTTP 200
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ POD=$(oc get pod -l name=siifx-api-aplicacao-des --sort-by=.metadata.crea                                                                                                                    tionTimestamp -o name | tail -1); echo $POD
pod/siifx-api-aplicacao-des-2901-l8s7n
-sh-4.2$ oc logs -f $POD -c secrets-agent-sidecar | grep -E 'secret path|ERROR|num                                                                                                                    ber of files|Timeout'
2026-10-14 14:13:22,603 INFO (69f98b90-c7d9-11f1-ae73-0a581901259c) **************                                                                                                                    ** secret path: SIIFX_DES/apikey_siifx_intranet *****************

