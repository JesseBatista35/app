-sh-4.2$ oc get route -n sispi-des | grep med-gestao
sispi-med-gestao-des                             sispi-med-gestao-des.apps.pixnprd4.caixa                                       sispi-med-gestao-des                             web       edge/Redirect   None
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get route sispi-med-gestao-des -n sispi-des -o yaml | grep -A4 -E '^  to:|port:|tls:'
        f:port:
          .: {}
          f:targetPort: {}
        f:tls:
          .: {}
          f:termination: {}
        f:to:
          f:kind: {}
--
        f:tls:
          f:insecureEdgeTerminationPolicy: {}
    manager: Mozilla
    operation: Update
    time: 2026-10-26T20:03:53Z
--
  port:
    targetPort: web
  tls:
    insecureEdgeTerminationPolicy: Redirect
    termination: edge
  to:
    kind: Service
    name: sispi-med-gestao-des
    weight: 100
  wildcardPolicy: None
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc port-forward pod/sispi-med-gestao-des-22-ckdkt 18080:8080 -n sispi-des &
[1] 41353
-sh-4.2$ Forwarding from 127.0.0.1:18080 -> 8080
Forwarding from [::1]:18080 -> 8080
^C
-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -s localhost:18080/q/health/ready | jq .
Handling connection for 18080
{
  "status": "UP",
  "checks": []
}
-sh-4.2$ oc get route sispi-med-gestao-des -n sispi-des -o jsonpath='{.status.ingress[*].conditions}'; echo
[map[type:Admitted status:True lastTransitionTime:2026-10-22T19:22:25Z]]
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get peerauthentication -n sispi-des
No resources found.
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get route sispi-med-auditoria-des -n sispi-des -o yaml | grep -A4 -E '^  to:|port:|tls:'
        f:port:
          .: {}
          f:targetPort: {}
        f:tls:
          .: {}
          f:insecureEdgeTerminationPolicy: {}
          f:termination: {}
        f:to:
--
  port:
    targetPort: web
  tls:
    insecureEdgeTerminationPolicy: Redirect
    termination: edge
  to:
    kind: Service
    name: sispi-med-auditoria-des
    weight: 100
  wildcardPolicy: None
-sh-4.2$



C:\Users\p585600>curl -skI https://sispi-med-gestao-des.apps.pixnprd4.caixa/q/health/ready
HTTP/1.0 503 Service Unavailable
pragma: no-cache
cache-control: private, max-age=0, no-cache, no-store
content-type: text/html


C:\Users\p585600>curl -skI http://sispi-med-gestao-des.apps.pixnprd4.caixa/q/health/ready

C:\Users\p585600>


