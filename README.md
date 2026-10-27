2026-10-27T14:09:08.3629054Z ##[section]Starting: Verificando Status do Deployment
2026-10-27T14:09:08.3632439Z ==============================================================================
2026-10-27T14:09:08.3632529Z Task         : Bash
2026-10-27T14:09:08.3632576Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-27T14:09:08.3632638Z Version      : 3.227.0
2026-10-27T14:09:08.3632690Z Author       : Microsoft Corporation
2026-10-27T14:09:08.3632836Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-27T14:09:08.3632922Z ==============================================================================
2026-10-27T14:09:08.4771841Z Generating script.
2026-10-27T14:09:08.4782087Z ========================== Starting Command Output ===========================
2026-10-27T14:09:08.4789315Z [command]/bin/bash /opt/ads-agent/_work/_temp/3e6c229e-6674-4fc9-9ed5-60914bff5fc8.sh
2026-10-27T14:09:08.7244960Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-27T14:09:10.3622292Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-27T14:09:10.5589312Z Waiting for rollout to finish: 1 old replicas are pending termination...
2026-10-27T14:14:08.7248491Z E1027 11:14:08.724172   44290 streamwatcher.go:109] Unable to decode an event from the watch stream: net/http: request canceled (Client.Timeout exceeded while reading body)
2026-10-27T14:14:08.7250418Z error: watch closed before Until timeout
2026-10-27T14:14:08.7284325Z A aplicação não foi iniciada com sucesso!
2026-10-27T14:14:08.7285447Z Os logs da aplicação estão disponíveis na próxima task: Logs da Aplicação
2026-10-27T14:14:08.7328192Z ##[error]Bash exited with code '1'.
2026-10-27T14:14:08.7337066Z ##[section]Finishing: Verificando Status do Deployment


2026-10-27T14:09:08.3629054Z ##[section]Starting: Verificando Status do Deployment
2026-10-27T14:09:08.3632439Z ==============================================================================
2026-10-27T14:09:08.3632529Z Task         : Bash
2026-10-27T14:09:08.3632576Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-27T14:09:08.3632638Z Version      : 3.227.0
2026-10-27T14:09:08.3632690Z Author       : Microsoft Corporation
2026-10-27T14:09:08.3632836Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-27T14:09:08.3632922Z ==============================================================================
2026-10-27T14:09:08.4771841Z Generating script.
2026-10-27T14:09:08.4782087Z ========================== Starting Command Output ===========================
2026-10-27T14:09:08.4789315Z [command]/bin/bash /opt/ads-agent/_work/_temp/3e6c229e-6674-4fc9-9ed5-60914bff5fc8.sh
2026-10-27T14:09:08.7244960Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-27T14:09:10.3622292Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-27T14:09:10.5589312Z Waiting for rollout to finish: 1 old replicas are pending termination...
2026-10-27T14:14:08.7248491Z E1027 11:14:08.724172   44290 streamwatcher.go:109] Unable to decode an event from the watch stream: net/http: request canceled (Client.Timeout exceeded while reading body)
2026-10-27T14:14:08.7250418Z error: watch closed before Until timeout
2026-10-27T14:14:08.7284325Z A aplicação não foi iniciada com sucesso!
2026-10-27T14:14:08.7285447Z Os logs da aplicação estão disponíveis na próxima task: Logs da Aplicação
2026-10-27T14:14:08.7328192Z ##[error]Bash exited with code '1'.
2026-10-27T14:14:08.7337066Z ##[section]Finishing: Verificando Status do Deployment



exec java -Dquarkus.http.host=0.0.0.0 -Dquarkus.http.port=8080 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Djavax.net.ssl.trustStore=/deployments/caixa-truststore-cedesbr_azurepush_atualizado.jks -javaagent:/opt/apm_agent/elastic-apm-agent.jar -Delastic.apm.config_file=/opt/apm_agent/elasticapm.properties -Delastic.apm.service_name=sispi -Delastic.apm.environment=des -Delastic.apm.application_packages=br.gov.caixa -Delastic.apm.server_urls=http://apm-server-devops.apps.produtos4.caixa -Delastic.apm.global_labels=deployment=sispi-qrcode-api-validador -XX:+UseParallelGC -XX:GCTimeRatio=4 -XX:AdaptiveSizePolicyWeight=90 -XX:MinHeapFreeRatio=20 -XX:MaxHeapFreeRatio=40 -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/quarkus-run.jar
Picked up JAVA_TOOL_OPTIONS: -Dfile.encoding=UTF8 -javaagent:/otel-auto-instrumentation-java-sispi-qrcode-api-validador-des/javaagent.jar
[otel.javaagent 2026-10-27 11:48:10:721 -0300] [main] INFO io.opentelemetry.javaagent.tooling.VersionLogger - opentelemetry-javaagent - version: 2.12.0

<img width="1633" height="792" alt="image" src="https://github.com/user-attachments/assets/9789acfa-5d62-4019-9471-f13db2108f85" />





