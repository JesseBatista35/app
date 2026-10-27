
-sh-4.2$ oc get route --all-namespaces | grep med-gestao
istio-system                         sispi-med-gestao-des                                                        sispi-med-gestao-des.apps.pixnprd4.caixa                                              istio-ingressgateway                              http2             edge/Allow             None
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -skI https://sispi-med-gestao-des.apps.pixnprd4.caixa/q/health/ready
HTTP/1.1 200 OK
content-type: application/json; charset=UTF-8
cache-control: no-store
x-envoy-upstream-service-time: 7
date: Tue, 27 Oct 2026 18:00:29 GMT
server: istio-envoy
transfer-encoding: chunked
set-cookie: 91f40973d3a0ebf783797fd3a472707d=ad951987fc9b916eb4c7eaea60d59003; path=/; HttpOnly

-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -sk  https://sispi-med-gestao-des.apps.pixnprd4.caixa/
<html><head><title>Error</title></head><body>Forbidden</body></html>-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$



