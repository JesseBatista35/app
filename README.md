
-sh-4.2$ NS=sigec-tqs
-sh-4.2$
-sh-4.2$
-sh-4.2$ POD=sigec-csc-frontend-tqs-83-rvzvp
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pod $POD -n $NS -o jsonpath='{.spec.containers[*].name}'; echo
sigec-csc-frontend-tqs sigec-csc-frontend-tqs-exporter
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs -n $NS $POD -c sigec-csc-frontend-tqs --since=168h | grep -E '" 504 |upstream' | tail -20
[24/Nov/2026:10:27:30 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526850.357 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:27:30 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526850.357 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:27:40 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526860.358 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:27:40 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526860.358 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:27:50 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526870.358 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:27:50 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526870.358 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:28:00 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526880.358 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:28:00 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526880.358 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:28:10 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526890.358 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:28:10 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526890.359 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:28:20 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526900.358 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:28:20 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526900.358 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:28:30 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526910.358 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:28:30 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526910.358 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:28:40 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526920.358 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:28:40 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526920.358 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:28:50 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526930.358 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:28:50 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526930.358 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:29:00 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526940.359 request_time 0.000 200 3469 - kube-probe/1.25 -
[24/Nov/2026:10:29:00 -0300] 25.1.8.1 - - - _ to: -: GET / HTTP/1.1 upstream_response_time - msec 1795526940.359 request_time 0.000 200 3469 - kube-probe/1.25 -
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc rsh -n $NS -c sigec-csc-frontend-tqs $POD sh -c 'getent hosts sigec-csc.esteiras.tqs.caixa; curl -skI https://sigec-csc.esteiras.tqs.caixa/csc-api/ | head -15'
10.116.180.23   sigec-csc.esteiras.tqs.caixa
HTTP/1.1 200 OK
Date: Tue, 24 Nov 2026 13:29:10 GMT
Server: JBoss-EAP/7
Accept-Language: pt-BR,pt;q=0.9,en-US;q=0.8,en;q=0.7
X-Powered-By: Undertow/1
Accept-Encoding: gzip, deflate
Access-Control-Allow-Headers: *
Access-Control-Expose-Headers: X-Total-Count
Accept-Ranges: bytes
Access-Control-Allow-Origin: *
Last-Modified: Thu, 29 Oct 2026 12:41:18 GMT
Access-Control-Allow-Credentials: true
Content-Type: text/html; charset=UTF-8
Content-Length: 1468
Access-Control-Allow-Methods: GET, HEAD, OPTIONS, POST, DELETE, PUT
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
