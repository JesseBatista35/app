
-sh-4.2$ oc get pod sihdg-jboss8-tqs-37-6llp9 -n sihdg-tqs
NAME                        READY     STATUS    RESTARTS     AGE
sihdg-jboss8-tqs-37-6llp9   0/1       Running   4 (9s ago)   8m10s
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get events -n sihdg-tqs --field-selector involvedObject.name=sihdg-jboss8-tqs-37-6llp9 | tail
8m8s        Normal    Pulled           pod/sihdg-jboss8-tqs-37-6llp9   Successfully pulled image "default-route-openshift-image-registry.apps.produtos4.caixa/build-images-ads/sihdg-jboss8:3.18.0.1" in 6.153239157s (6.153252227s including waiting)
6m16s       Normal    Created          pod/sihdg-jboss8-tqs-37-6llp9   Created container sihdg-jboss8-tqs
6m16s       Normal    Started          pod/sihdg-jboss8-tqs-37-6llp9   Started container sihdg-jboss8-tqs
5m32s       Warning   Unhealthy        pod/sihdg-jboss8-tqs-37-6llp9   Readiness probe failed: Get "http://25.3.44.25:8080/sihdg-api/health/ready": context deadline exceeded (Client.Timeout exceeded while awaiting headers)
6m47s       Warning   Unhealthy        pod/sihdg-jboss8-tqs-37-6llp9   Liveness probe failed: HTTP probe failed with statuscode: 404
3m7s        Warning   Unhealthy        pod/sihdg-jboss8-tqs-37-6llp9   Readiness probe failed: HTTP probe failed with statuscode: 404
6m47s       Normal    Killing          pod/sihdg-jboss8-tqs-37-6llp9   Container sihdg-jboss8-tqs failed liveness probe, will be restarted
6m17s       Warning   Unhealthy        pod/sihdg-jboss8-tqs-37-6llp9   Readiness probe failed: HTTP probe failed with statuscode: 503
6m16s       Normal    Pulled           pod/sihdg-jboss8-tqs-37-6llp9   Successfully pulled image "default-route-openshift-image-registry.apps.produtos4.caixa/build-images-ads/sihdg-jboss8:3.18.0.1" in 80.118901ms (80.127844ms including waiting)
6m16s       Warning   Unhealthy        pod/sihdg-jboss8-tqs-37-6llp9   Readiness probe failed: Get "http://25.3.44.25:8080/sihdg-api/health/ready": dial tcp 25.3.44.25:8080: connect: connection refused
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc rsh -n sihdg-des -c sihdg-jboss8-des sihdg-jboss8-des-116-mq4ct curl -s -o /dev/null -w "%{http_code}\n" http://localhost:8080/sihdg-api/health/ready
200
-sh-4.2$


a sandatra ta falndo isso Poderia habilitar o atributo <healthcheck> para vermos se isso resolve o problema ou não

mais acho que ela esta perdida tambem igual ao fabio
