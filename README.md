sh-4.2$
-sh-4.2$ oc get networkpolicy -n sispi-des
NAME                          POD-SELECTOR                   AGE
istio-expose-route-pix-mesh   maistra.io/expose-route=true   2y139d
istio-mesh-pix-mesh           <none>                         2y139d
user-workload-access          <none>                         2y190d
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get networkpolicy -n sispi-des -o yaml | grep -B2 -A8 expose-route
    annotations:
      kubectl.kubernetes.io/last-applied-configuration: |
        {"apiVersion":"networking.k8s.io/v1","kind":"NetworkPolicy","metadata":{"annotations":{"maistra.io/mesh-generation":"2.5.2-1-1"},"labels":{"app":"istio","app.kubernetes.io/component":"mesh-config","app.kubernetes.io/instance":"istio-system","app.kubernetes.io/managed-by":"maistra-istio-operator","app.kubernetes.io/name":"mesh-config","app.kubernetes.io/part-of":"istio","app.kubernetes.io/version":"2.5.2-1-1","maistra-version":"2.5.2","maistra.io/owner":"istio-system","maistra.io/owner-name":"pix-mesh","release":"istio"},"name":"istio-expose-route-pix-mesh","namespace":"istio-system","ownerReferences":[{"apiVersion":"maistra.io/v2","blockOwnerDeletion":true,"controller":true,"kind":"ServiceMeshControlPlane","name":"pix-mesh","uid":"3e333fb0-8aa9-4011-a97b-1f1905f0d759"}]},"spec":{"ingress":[{"from":[{"namespaceSelector":{"matchLabels":{"network.openshift.io/policy-group":"ingress"}}}]}],"podSelector":{"matchLabels":{"maistra.io/expose-route":"true"}}}}
      maistra.io/mesh-generation: 2.5.2-1-1
    creationTimestamp: 2024-06-10T13:49:17Z
    generation: 1
    labels:
      app: istio
      app.kubernetes.io/component: mesh-config
      app.kubernetes.io/instance: istio-system
      app.kubernetes.io/managed-by: maistra-istio-operator
--
      operation: Update
      time: 2024-06-10T13:49:17Z
    name: istio-expose-route-pix-mesh
    namespace: sispi-des
    resourceVersion: "227197682"
    uid: c55533c4-8105-490e-96c7-9033c632a75d
  spec:
    ingress:
    - from:
      - namespaceSelector:
          matchLabels:
--
    podSelector:
      matchLabels:
        maistra.io/expose-route: "true"
    policyTypes:
    - Ingress
- apiVersion: networking.k8s.io/v1
  kind: NetworkPolicy
  metadata:
    annotations:
      kubectl.kubernetes.io/last-applied-configuration: |
        {"apiVersion":"networking.k8s.io/v1","kind":"NetworkPolicy","metadata":{"annotations":{"maistra.io/mesh-generation":"2.5.2-1-1"},"labels":{"app":"istio","app.kubernetes.io/component":"mesh-config","app.kubernetes.io/instance":"istio-system","app.kubernetes.io/managed-by":"maistra-istio-operator","app.kubernetes.io/name":"mesh-config","app.kubernetes.io/part-of":"istio","app.kubernetes.io/version":"2.5.2-1-1","maistra-version":"2.5.2","maistra.io/owner":"istio-system","maistra.io/owner-name":"pix-mesh","release":"istio"},"name":"istio-mesh-pix-mesh","namespace":"istio-system","ownerReferences":[{"apiVersion":"maistra.io/v2","blockOwnerDeletion":true,"controller":true,"kind":"ServiceMeshControlPlane","name":"pix-mesh","uid":"3e333fb0-8aa9-4011-a97b-1f1905f0d759"}]},"spec":{"ingress":[{"from":[{"namespaceSelector":{"matchLabels":{"maistra.io/member-of":"istio-system"}}}]}]}}
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pod -n sispi-des -l name=sispi-med-auditoria-des --show-labels
NAME                               READY     STATUS    RESTARTS   AGE       LABELS
sispi-med-auditoria-des-30-x5zjs   2/2       Running   0          82d       CGC_DES=7390,CGC_OPS=7259,app=sispi-med-auditoria-des,deployment=sispi-med-auditoria-des-30,deploymentconfig=sispi-med-auditoria-des,maistra-version=2.5.12,name=sispi-med-auditoria-des,security.istio.io/tlsMode=istio,service.istio.io/canonical-name=sispi-med-auditoria-des,service.istio.io/canonical-revision=latest
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pod sispi-med-gestao-des-22-ckdkt -n sispi-des --show-labels
NAME                            READY     STATUS    RESTARTS   AGE       LABELS
sispi-med-gestao-des-22-ckdkt   2/2       Running   0          21h       CGC_DES=7390,CGC_OPS=7259,app=sispi-med-gestao-des,deployment=sispi-med-gestao-des-22,deploymentconfig=sispi-med-gestao-des,maistra-version=2.5.12,name=sispi-med-gestao-des,security.istio.io/tlsMode=istio,service.istio.io/canonical-name=sispi-med-gestao-des,service.istio.io/canonical-revision=latest
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc label pod sispi-med-gestao-des-22-ckdkt -n sispi-des maistra.io/expose-route=true
pod/sispi-med-gestao-des-22-ckdkt labeled
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc patch dc sispi-med-gestao-des -n sispi-des --type merge \
>   -p '{"spec":{"template":{"metadata":{"labels":{"maistra.io/expose-route":"true"}}}}}'
deploymentconfig.apps.openshift.io/sispi-med-gestao-des patched
-sh-4.2$




C:\Users\p585600>curl -skI http://sispi-med-gestao-des.apps.pixnprd4.caixa/q/health/ready

C:\Users\p585600>curl -skI https://sispi-med-auditoria-des.apps.pixnprd4.caixa/q/health/ready
HTTP/1.0 503 Service Unavailable
pragma: no-cache
cache-control: private, max-age=0, no-cache, no-store
content-type: text/html


C:\Users\p585600>curl -skI https://sispi-med-gestao-des.apps.pixnprd4.caixa/q/health/ready
HTTP/1.1 200 OK
content-type: application/json; charset=UTF-8
cache-control: no-store
set-cookie: 9ecd4910eee7bb9b6bbe052d24350293=c404f983a68be13250e4f64c92c71f49; path=/; HttpOnly; Secure; SameSite=None


C:\Users\p585600>
