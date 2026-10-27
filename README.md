<img width="1588" height="835" alt="image" src="https://github.com/user-attachments/assets/8bce0f6c-6979-4729-b481-e4401df7911b" />


tem outra pessoam mechendo na aplicação rodam um novo deploy


sispi-qrcode-api-validador-des-312-mthvm
Running


3 lines
exec java -Dquarkus.http.host=0.0.0.0 -Dquarkus.http.port=8080 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Djavax.net.ssl.trustStore=/deployments/caixa-truststore-cedesbr_azurepush_atualizado.jks -javaagent:/opt/apm_agent/elastic-apm-agent.jar -Delastic.apm.config_file=/opt/apm_agent/elasticapm.properties -Delastic.apm.service_name=sispi -Delastic.apm.environment=des -Delastic.apm.application_packages=br.gov.caixa -Delastic.apm.server_urls=http://apm-server-devops.apps.produtos4.caixa -Delastic.apm.global_labels=deployment=sispi-qrcode-api-validador -XX:+UseParallelGC -XX:GCTimeRatio=4 -XX:AdaptiveSizePolicyWeight=90 -XX:MinHeapFreeRatio=20 -XX:MaxHeapFreeRatio=40 -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/quarkus-run.jar
Picked up JAVA_TOOL_OPTIONS: -Dfile.encoding=UTF8
WARNING: sun.reflect.Reflection.getCallerClass is not supported. This will impact performance.


