C:\Users\p585600>curl -skI https://sispi-med-gestao-des.apps.pixnprd4.caixa/q/health/ready
HTTP/1.1 200 OK
content-type: application/json; charset=UTF-8
cache-control: no-store
x-envoy-upstream-service-time: 7
date: Tue, 27 Oct 2026 17:50:22 GMT
server: istio-envoy
transfer-encoding: chunked
set-cookie: 91f40973d3a0ebf783797fd3a472707d=56198feb3697441baa49b6b86b0a3637; path=/; HttpOnly


C:\Users\p585600>curl -skI https://sispi-med-auditoria-des.apps.pixnprd4.caixa/q/health/ready
HTTP/1.1 200 OK
content-type: application/json; charset=UTF-8
cache-control: no-store
x-envoy-upstream-service-time: 10
date: Tue, 27 Oct 2026 17:50:30 GMT
server: istio-envoy
transfer-encoding: chunked
set-cookie: e078b9f0dc9f58180f1fa9fe434ae7fa=5f89b29ea9e110b8c3867c7af9dedabe; path=/; HttpOnly


C:\Users\p585600>




-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get route sispi-med-gestao-des -n sispi-des -o yaml > route-med-gestao-sispi-des.bkp.yaml
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get route sispi-med-auditoria-des -n sispi-des -o yaml > route-med-auditoria-sispi-des.bkp.yaml
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc delete route sispi-med-gestao-des -n sispi-des
route.route.openshift.io "sispi-med-gestao-des" deleted
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc delete route sispi-med-auditoria-des -n sispi-des
route.route.openshift.io "sispi-med-auditoria-des" deleted
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get route sispi-med-gestao-des -n istio-system -o jsonpath='{.status.ingress[*].conditions}'; echo
[map[status:True lastTransitionTime:2026-10-27T17:49:53Z type:Admitted]]
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get route sispi-med-auditoria-des -n istio-system -o jsonpath='{.status.ingress[*].conditions}'; echo
[map[type:Admitted status:True lastTransitionTime:2026-10-27T17:50:01Z]]
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
