
-sh-4.2$
-sh-4.2$ POD=sispi-qrcode-api-validador-des-297-6jjtp
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs $POD -n sispi-des -c sispi-qrcode-api-validador-des --previous | tail -300
exec java -Dquarkus.http.host=0.0.0.0 -Dquarkus.http.port=8080 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Djavax.net.ssl.trustStore=/deployments/caixa-truststore-cedesbr_azurepush_atualizado.jks -javaagent:/opt/apm_agent/elastic-apm-agent.jar -Delastic.apm.config_file=/opt/apm_agent/elasticapm.properties -Delastic.apm.service_name=sispi -Delastic.apm.environment=des -Delastic.apm.application_packages=br.gov.caixa -Delastic.apm.server_urls=http://apm-server-devops.apps.produtos4.caixa -Delastic.apm.global_labels=deployment=sispi-qrcode-api-validador -XX:+UseParallelGC -XX:GCTimeRatio=4 -XX:AdaptiveSizePolicyWeight=90 -XX:MinHeapFreeRatio=20 -XX:MaxHeapFreeRatio=40 -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/quarkus-run.jar
Picked up JAVA_TOOL_OPTIONS: -Dfile.encoding=UTF8 -javaagent:/otel-auto-instrumentation-java-sispi-qrcode-api-validador-des/javaagent.jar
[otel.javaagent 2026-10-27 11:53:58:228 -0300] [main] INFO io.opentelemetry.javaagent.tooling.VersionLogger - opentelemetry-javaagent - version: 2.12.0
WARNING: sun.reflect.Reflection.getCallerClass is not supported. This will impact performance.
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pod $POD -n sispi-des -o jsonpath='{.status.containerStatuses[?(@.name=="sispi-qrcode-api-validador-des")].lastState}{"\n"}'
map[terminated:map[exitCode:137 reason:Error startedAt:2026-10-27T14:53:48Z finishedAt:2026-10-27T14:56:11Z containerID:cri-o://92ea98901d42bd3bb06b550b45bbe7d37b27dc39a18bd998d22957c6369f3658]]
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec $POD -n sispi-des -c sispi-qrcode-api-validador-des -- ls -l /deployments/
total 108228
drwxr-xr-x. 2 1001 root        50 Oct 20 16:40 app
-rw-r--r--. 1 root root     39055 Oct 27 11:53 caixa-truststore-acteste-nprd.jks
-rw-r--r--. 1 root root     17158 Oct 27 11:53 caixa-truststore-azurepush_2023.jks
-rw-r--r--. 1 root root       249 Oct 27 11:53 customhosts5
drwxr-xr-x. 4 1001 root        30 Oct 20 16:40 lib
drwxr-xr-x. 2 1001 root        99 Oct 20 16:40 quarkus
-rw-r--r--. 1 1001 root     14950 Oct 20 16:40 quarkus-app-dependencies.txt
-rw-r--r--. 1 1001 root       599 Oct 20 16:40 quarkus-run.jar
-r-xr-----. 1 1001 root     20219 Oct 27 11:56 run-java.sh
-rw-r--r--. 1 root root      8454 Oct 27 11:53 sispi-des-keystore.jks
-rw-r--r--. 1 1001 root 110706105 Oct 20 16:40 sispi-qrcode-api-validador-20261020-1640-0-0-1-SNAPSHOT.zip
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec $POD -n sispi-des -c istio-proxy -- curl -s -w '\n%{http_code}\n' localhost:8080/q/health

000
command terminated with exit code 7
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs sispi-qrcode-api-validador-des-309-deploy -n sispi-des
--> Scaling up sispi-qrcode-api-validador-des-309 from 0 to 1, scaling down sispi-qrcode-api-validador-des-297 from 1 to 0 (keep 1 pods available, don't exceed 2 pods)
    Scaling sispi-qrcode-api-validador-des-309 up to 1
error: timed out waiting for any update progress to be made
-sh-4.2$
