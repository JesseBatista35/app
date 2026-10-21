
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pod sigsj-alvara-des-702-m5bvt -o jsonpath='{.spec.containers[*].image}{"\n"}'
default-route-openshift-image-registry.apps.produtos4.caixa/build-images-ads/sigsj-alvara:20261021.1323-3.0.9.101-SNAPSHOT
-sh-4.2$ oc get rc | grep sigsj-alvara-des-
sigsj-alvara-des-701                      0         0         0         19h
sigsj-alvara-des-702                      1         1         1         27m
-sh-4.2$ oc get rc sigsj-alvara-des-693 -o jsonpath='{.spec.template.spec.containers[*].image}{"\n"}'
Error from server (NotFound): replicationcontrollers "sigsj-alvara-des-693" not found
-sh-4.2$ oc get rc sigsj-alvara-des-701 -o jsonpath='{.spec.template.spec.containers[*].image}{"\n"}'
default-route-openshift-image-registry.apps.produtos4.caixa/build-images-ads/sigsj-alvara:20261015.1632-3.0.2.1-SNAPSHOT
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs sigsj-alvara-des-702-m5bvt | head -40          # procurar "started in X.XXXs"
exec java -Dquarkus.http.host=0.0.0.0 -Dquarkus.http.port=8080 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Djavax.net.ssl.trustStore=/deployments/caixa-truststore-acteste-nprd-sigsj-20260707.jks -Dotel.exporter.otlp.endpoint=https://otel-collector-nprd.cemot.cloud.caixa -Dhttps.proxyHost=proxydes.caixa -Dhttps.proxyPort=80 -Dhttp.nonProxyHosts=*.caixa|*.caixa.gov.br|apim-parceiros-sandbox.azure-api.net -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/quarkus-run.jar
LogManager error of type GENERIC_FAILURE: Unable to find named filter 'controle-logging'
__  ____  __  _____   ___  __ ____  ______
 --/ __ \/ / / / _ | / _ \/ //_/ / / / __/
 -/ /_/ / /_/ / __ |/ , _/ ,< / /_/ /\ \
--\___\_\____/_/ |_/_/|_/_/|_|\____/___/
13:45:32 WARN  [id=] VertxTracer delegate not set. Will not submit this trace. SpanKind: RPC; Request: io.vertx.core.http.impl.HttpRequestHead@76cc57d6; Operation:GET.
13:45:32 WARN  [id=] VertxTracer delegate not set. Will not submit this trace. Response: io.vertx.core.http.impl.HttpResponseHead@22f1eaa4; Failure: null.
13:45:32 WARN  [id=] VertxTracer delegate not set. Will not submit this trace. SpanKind: RPC; Request: io.vertx.core.http.impl.HttpRequestHead@34d5d071; Operation:GET.
13:45:32 WARN  [id=] VertxTracer delegate not set. Will not submit this trace. Response: io.vertx.core.http.impl.HttpResponseHead@67aa313a; Failure: null.
13:45:32 WARN  [id=] VertxTracer delegate not set. Will not submit this trace. SpanKind: RPC; Request: io.vertx.core.http.impl.HttpRequestHead@6dbd464b; Operation:GET.
13:45:32 WARN  [id=] VertxTracer delegate not set. Will not submit this trace. Response: io.vertx.core.http.impl.HttpResponseHead@8692437; Failure: null.
13:45:32 WARN  [id=] VertxTracer delegate not set. Will not submit this trace. SpanKind: RPC; Request: io.vertx.core.http.impl.HttpRequestHead@7e444859; Operation:GET.
13:45:32 WARN  [id=] VertxTracer delegate not set. Will not submit this trace. Response: io.vertx.core.http.impl.HttpResponseHead@ed8fea5; Failure: null.
13:45:32 WARN  [id=] VertxTracer delegate not set. Will not submit this trace. SpanKind: RPC; Request: io.vertx.core.http.impl.HttpRequestHead@21177b2f; Operation:GET.
13:45:32 WARN  [id=] VertxTracer delegate not set. Will not submit this trace. Response: io.vertx.core.http.impl.HttpResponseHead@5208eb0a; Failure: null.
13:45:33 WARN  [id=] Log level ALL for category 'io.opentelemetry.sdk' set below minimum logging level DEBUG, promoting it to DEBUG. Set the build time configuration property 'quarkus.log.category."io.opentelemetry.sdk".min-level' to 'ALL' to avoid this warning
LogManager error of type WRITE_FAILURE: The delayed handler's queue was overrun and log record(s) were lost (Did you forget to configure logging?):
         - io.opentelemetry.exporter.internal.http.HttpExporterBuilder: [FINE]
         - io.opentelemetry.instrumentation.api.internal.EmbeddedInstrumentationProperties: [FINE]
         - io.opentelemetry.sdk.autoconfigure.AutoConfiguredOpenTelemetrySdkBuilder: [FINE]
         - io.opentelemetry.sdk.internal.JavaVersionSpecific: [FINE]

13:45:33 INFO  [id=] Conectado e consumindo a fila SIGSJ.REQ.EXECUCAO_LEVANTAMENTO
13:45:34 INFO  [id=] SIGSJ-alvara 3.0.9.101 on JVM (powered by Quarkus 3.16.1) started in 4.612s. Listening on: http://0.0.0.0:8080
13:45:34 INFO  [id=] Profile prod activated.
13:45:34 INFO  [id=] Installed features: [agroal, cache, cdi, config-yaml, cxf, cxf-rt-transports-http-hc5, hibernate-orm, hibernate-orm-panache, hibernate-validator, jdbc-db2, messaging, messaging-amqp, narayana-jta, oidc, oidc-client, opentelemetry, rest, rest-client, rest-client-jackson, rest-jackson, scheduler, security, smallrye-context-propagation, smallrye-fault-tolerance, smallrye-health, smallrye-jwt, smallrye-openapi, vertx]
13:45:34 INFO  [id=]
SER > API [GET] https://apim-parceiros-sandbox.azure-api.net/deposito-judicial/cnj/api/v1/usuarios/healthcheck/perfis
null
13:45:34 INFO  [id=] Exportacao de eventos customizados habilitada pelo OpenTelemetry global; scope=sigsj-alvara
13:45:34 INFO  [id=] Evento OTEL: Alvará em AC - Tribunal: TJCE, Tipo: creditoEmConta, Esfera: estadual
13:45:34 INFO  [id=] Evento OTEL: Alvará em AC - Tribunal: TJCE, Tipo: desconhecido, Esfera: estadual
13:45:34 INFO  [id=] Evento OTEL: Alvará em AC - Tribunal: TJCE, Tipo: creditoEmConta, Esfera: estadual
13:45:34 INFO  [id=] Evento OTEL: Alvará em AC - Tribunal: TJCE, Tipo: creditoEmConta, Esfera: estadual
13:45:34 INFO  [id=] Snapshot da metrica alvaras_ac atualizado: 4 alvaras em AC
13:45:34 INFO  [id=] Monitoramento de alvaras AC concluido: 4/4 custom events emitidos
13:45:34 INFO  [id=]
API > SER [GET] https://apim-parceiros-sandbox.azure-api.net/deposito-judicial/cnj/api/v1/usuarios/healthcheck/perfis : 400
{
-sh-4.2$ oc get dc sigsj-alvara-des -o yaml | grep -B2 -A12 -E 'readinessProbe|livenessProbe|timeoutSeconds'
                    f:name: {}
                    f:value: {}
                f:livenessProbe:
                  .: {}
                  f:failureThreshold: {}
                  f:httpGet:
                    .: {}
                    f:path: {}
                    f:port: {}
                    f:scheme: {}
                  f:initialDelaySeconds: {}
                  f:periodSeconds: {}
                  f:successThreshold: {}
                  f:timeoutSeconds: {}
                f:readinessProbe:
                  .: {}
                  f:failureThreshold: {}
                  f:httpGet:
                    .: {}
                    f:path: {}
                    f:port: {}
                    f:scheme: {}
                  f:initialDelaySeconds: {}
                  f:periodSeconds: {}
                  f:successThreshold: {}
                  f:timeoutSeconds: {}
                f:resources:
                  f:limits:
                    f:cpu: {}
                    f:memory: {}
                  f:requests:
                    f:cpu: {}
                    f:memory: {}
            f:hostAliases:
              .: {}
              k:{"ip":"172.28.144.217"}:
                .: {}
                f:ip: {}
--
            f:maxSurge: {}
            f:maxUnavailable: {}
            f:timeoutSeconds: {}
            f:updatePeriodSeconds: {}
          f:type: {}
        f:template:
          .: {}
          f:metadata:
            .: {}
            f:annotations:
              .: {}
              f:openshift.io/generated-by: {}
            f:creationTimestamp: {}
            f:labels:
              .: {}
--
      maxSurge: 25%
      maxUnavailable: 25%
      timeoutSeconds: 600
      updatePeriodSeconds: 1
    type: Rolling
  template:
    metadata:
      annotations:
        openshift.io/generated-by: OpenShiftNewApp
      creationTimestamp: null
      labels:
        CGC_DES: "7266"
        CGC_OPS: "7259"
        UNIDADE: BR
        app: sigsj-alvara-des
--
        image: default-route-openshift-image-registry.apps.produtos4.caixa/build-images-ads/sigsj-alvara:20261021.1323-3.0.9.101-SNAPSHOT
        imagePullPolicy: Always
        livenessProbe:
          failureThreshold: 3
          httpGet:
            path: /q/health/live
            port: 8080
            scheme: HTTP
          initialDelaySeconds: 180
          periodSeconds: 10
          successThreshold: 1
          timeoutSeconds: 30
        name: sigsj-alvara-des
        ports:
        - containerPort: 8080
          protocol: TCP
        readinessProbe:
          failureThreshold: 3
          httpGet:
            path: /q/health/ready
            port: 8080
            scheme: HTTP
          initialDelaySeconds: 180
          periodSeconds: 10
          successThreshold: 1
          timeoutSeconds: 30
        resources:
          limits:
            cpu: "2"
            memory: 2Gi
          requests:
            cpu: 200m
            memory: 256Mi
        terminationMessagePath: /dev/termination-log
        terminationMessagePolicy: File
        volumeMounts:
        - mountPath: /deployments/caixa-truststore-azure.jks
          name: caixa-truststore-azure
-sh-4.2$
-sh-4.2$ oc get events --sort-by=.metadata.creationTimestamp | grep -i alvara
2h          6d           283       sigsj-alvara-sandbox-des-147-tjscn.18dea0bbdc69511d               Pod                     spec.containers{sigsj-alvara-sandbox-des}                  Warning   Unhealthy           kubelet, ceadecldlx044.nprd.caixa   Readiness probe failed: HTTP probe failed with statuscode: 503
27m         27m          1         sigsj-alvara-des.18e09936ea2f325c                                 DeploymentConfig                                                                   Normal    DeploymentCreated   deploymentconfig-controller         Created new replication controller "sigsj-alvara-des-702" for version 702
<unknown>   <unknown>    0         sigsj-alvara-des-702-deploy.18e09936ef8219d4                      Pod                                                                                Normal    Scheduled                                               Successfully assigned sigsj-des/sigsj-alvara-des-702-deploy to ceadecldlx058.nprd.caixa
27m         27m          1         sigsj-alvara-des-702-deploy.18e0993766558923                      Pod                     spec.containers{deployment}                                Normal    Pulled              kubelet, ceadecldlx058.nprd.caixa   Container image "quay.io/openshift/okd-content@sha256:0c49a1e144b537b9c69339d504287fe5c6974ffe69a3212345a5608c06db8a18" already present on machine
27m         27m          1         sigsj-alvara-des-702-deploy.18e09937642d6cf6                      Pod                                                                                Normal    AddedInterface      multus                              Add eth0 [25.0.45.242/23] from openshift-sdn
27m         27m          1         sigsj-alvara-des-702-deploy.18e09937721e5ed8                      Pod                     spec.containers{deployment}                                Normal    Created             kubelet, ceadecldlx058.nprd.caixa   Created container deployment
27m         27m          1         sigsj-alvara-des-702-deploy.18e09937737fbf3c                      Pod                     spec.containers{deployment}                                Normal    Started             kubelet, ceadecldlx058.nprd.caixa   Started container deployment
<unknown>   <unknown>    0         sigsj-alvara-des-702-m5bvt.18e09937bf8b33ef                       Pod                                                                                Normal    Scheduled                                               Successfully assigned sigsj-des/sigsj-alvara-des-702-m5bvt to ceadecldlx037.nprd.caixa
27m         27m          1         sigsj-alvara-des-702.18e09937be2f2b57                             ReplicationController                                                              Normal    SuccessfulCreate    replication-controller              Created pod: sigsj-alvara-des-702-m5bvt
27m         27m          1         sigsj-alvara-des-702-m5bvt.18e099382374a6d2                       Pod                                                                                Normal    AddedInterface      multus                              Add eth0 [25.1.16.194/23] from openshift-sdn
27m         27m          1         sigsj-alvara-des-702-m5bvt.18e0993830f9543c                       Pod                     spec.initContainers{secrets-agent-sidecar}                 Normal    Created             kubelet, ceadecldlx037.nprd.caixa   Created container secrets-agent-sidecar
27m         27m          1         sigsj-alvara-des-702-m5bvt.18e0993826668c5e                       Pod                     spec.initContainers{secrets-agent-sidecar}                 Normal    Pulled              kubelet, ceadecldlx037.nprd.caixa   Container image "default-route-openshift-image-registry.apps.produtos4.caixa/openshift/secrets-agent:v23.3.2" already present on machine
27m         27m          1         sigsj-alvara-des-702-m5bvt.18e09938328ebf52                       Pod                     spec.initContainers{secrets-agent-sidecar}                 Normal    Started             kubelet, ceadecldlx037.nprd.caixa   Started container secrets-agent-sidecar
27m         27m          1         sigsj-alvara-des-702-m5bvt.18e0993919e0a45e                       Pod                     spec.initContainers{secrets-check}                         Normal    Pulled              kubelet, ceadecldlx037.nprd.caixa   Container image "default-route-openshift-image-registry.apps.produtos4.caixa/openshift/ubi:9.3-1552" already present on machine
27m         27m          1         sigsj-alvara-des-702-m5bvt.18e0993928a3ba5b                       Pod                     spec.initContainers{secrets-check}                         Normal    Created             kubelet, ceadecldlx037.nprd.caixa   Created container secrets-check
27m         27m          1         sigsj-alvara-des-702-m5bvt.18e099392a5a0ff1                       Pod                     spec.initContainers{secrets-check}                         Normal    Started             kubelet, ceadecldlx037.nprd.caixa   Started container secrets-check
27m         27m          1         sigsj-alvara-des-702-m5bvt.18e0993955d0bd40                       Pod                     spec.containers{sigsj-alvara-des}                          Normal    Pulling             kubelet, ceadecldlx037.nprd.caixa   Pulling image "default-route-openshift-image-registry.apps.produtos4.caixa/build-images-ads/sigsj-alvara:20261021.1323-3.0.9.101-SNAPSHOT"
27m         27m          1         sigsj-alvara-des-702-m5bvt.18e0993ac3f3b346                       Pod                     spec.containers{sigsj-alvara-des}                          Normal    Started             kubelet, ceadecldlx037.nprd.caixa   Started container sigsj-alvara-des
27m         27m          1         sigsj-alvara-des-702-m5bvt.18e0993ab073afcc                       Pod                     spec.containers{sigsj-alvara-des}                          Normal    Pulled              kubelet, ceadecldlx037.nprd.caixa   Successfully pulled image "default-route-openshift-image-registry.apps.produtos4.caixa/build-images-ads/sigsj-alvara:20261021.1323-3.0.9.101-SNAPSHOT" in 5.815564237s (5.815575932s including waiting)
27m         27m          1         sigsj-alvara-des-702-m5bvt.18e0993ac23a5ed0                       Pod                     spec.containers{sigsj-alvara-des}                          Normal    Created             kubelet, ceadecldlx037.nprd.caixa   Created container sigsj-alvara-des
24m         24m          1         sigsj-alvara-des-701.18e09966a435f240                             ReplicationController                                                              Normal    SuccessfulDelete    replication-controller              Deleted pod: sigsj-alvara-des-701-2cspd
23m         24m          2         sigsj-alvara-des-701-2cspd.18e09966a49bfd88                       Pod                     spec.containers{sigsj-alvara-des}                          Normal    Killing             kubelet, ceadecldlx086.nprd.caixa   Stopping container sigsj-alvara-des
-sh-4.2$
