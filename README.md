Favor, verificar e ajustar Repositório -sispi-med-gestao. O pod da aplicação não está acessível, quando tentam acessar, retornar esse erro, 503. REQ semelhante: REQ000146856086.


A aplicação está no ar, são gerados logs de inicialização, porém está inacessível conforme é possível verificar pelo link informado no resumo da release https://sispi-med-gestao-des.apps.pixnprd4.caixa/




2026-10-26T19:38:47.6344951Z ##[section]Starting: Logs da Aplicação
2026-10-26T19:38:47.6348531Z ==============================================================================
2026-10-26T19:38:47.6348662Z Task         : Bash
2026-10-26T19:38:47.6348703Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-26T19:38:47.6348774Z Version      : 3.227.0
2026-10-26T19:38:47.6348817Z Author       : Microsoft Corporation
2026-10-26T19:38:47.6348865Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-26T19:38:47.6348953Z ==============================================================================
2026-10-26T19:38:47.7870321Z Generating script.
2026-10-26T19:38:47.7882643Z ========================== Starting Command Output ===========================
2026-10-26T19:38:47.7889949Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/3e90d229-c763-4cf5-b3c3-c73206fb00ca.sh
2026-10-26T19:38:47.7947629Z + shopt -s expand_aliases
2026-10-26T19:38:47.7948861Z + [[ -n ocp_nprd ]]
2026-10-26T19:38:47.7949027Z + [[ ocp_nprd =~ ocp ]]
2026-10-26T19:38:47.7949522Z + app=sispi-med-gestao-des
2026-10-26T19:38:47.7949734Z + arquivo=/usr/local/bin/oc-v4.13
2026-10-26T19:38:47.7949899Z + '[' -e /usr/local/bin/oc-v4.13 ']'
2026-10-26T19:38:47.7950015Z + oc version
2026-10-26T19:38:47.8607205Z Client Version: v4.2.0-alpha.0-1394-g45460a5
2026-10-26T19:38:47.8607522Z Server Version: 4.15.59
2026-10-26T19:38:47.8607728Z Kubernetes Version: v1.28.15+d227d65
2026-10-26T19:38:47.8658151Z ++ tac
2026-10-26T19:38:47.8658754Z ++ oc get pod -l name=sispi-med-gestao-des -n sispi-des -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-10-26T19:38:47.8659512Z ++ grep -v '^$'
2026-10-26T19:38:47.8659720Z ++ head -n1
2026-10-26T19:38:48.0037235Z + last_pod=sispi-med-gestao-des-21-k7cws
2026-10-26T19:38:48.0037554Z + echo 'Logs do POD: sispi-med-gestao-des-21-k7cws'
2026-10-26T19:38:48.0037781Z + oc logs sispi-med-gestao-des-21-k7cws -c sispi-med-gestao-des -n sispi-des
2026-10-26T19:38:48.0037990Z Logs do POD: sispi-med-gestao-des-21-k7cws
2026-10-26T19:38:48.1015825Z exec java -Dquarkus.http.host=0.0.0.0 -Dquarkus.http.port=8080 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Djavax.net.ssl.trustStore=/deployments/caixa-truststore-acteste-nprd.jks -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/quarkus-run.jar
2026-10-26T19:38:48.1016200Z __  ____  __  _____   ___  __ ____  ______ 
2026-10-26T19:38:48.1016722Z  --/ __ \/ / / / _ | / _ \/ //_/ / / / __/ 
2026-10-26T19:38:48.1016872Z  -/ /_/ / /_/ / __ |/ , _/ ,< / /_/ /\ \   
2026-10-26T19:38:48.1017019Z --\___\_\____/_/ |_/_/|_/_/|_|\____/___/   
2026-10-26T19:38:48.1017413Z 16:38:16 WARN  [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.config] (main) [SISPI][MED][GESTAO] Unrecognized configuration key "quarkus.http.cors" was provided; it will be ignored; verify that the dependency extension for this configuration is set or that you did not make a typo
2026-10-26T19:38:48.1017937Z 16:38:16 WARN  [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.config] (main) [SISPI][MED][GESTAO] Unrecognized configuration key "quarkus.log.console.charset" was provided; it will be ignored; verify that the dependency extension for this configuration is set or that you did not make a typo
2026-10-26T19:38:48.1018477Z 16:38:16 WARN  [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.config] (main) [SISPI][MED][GESTAO] Unrecognized configuration key "quarkus.http.encoding.default-charset" was provided; it will be ignored; verify that the dependency extension for this configuration is set or that you did not make a typo
2026-10-26T19:38:48.1018992Z 16:38:16 WARN  [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.config] (main) [SISPI][MED][GESTAO] Unrecognized configuration key "quarkus.http.encoding.force" was provided; it will be ignored; verify that the dependency extension for this configuration is set or that you did not make a typo
2026-10-26T19:38:48.1019749Z 16:38:16 WARN  [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.config] (main) [SISPI][MED][GESTAO] Unrecognized configuration key "quarkus.resteasy-reactive.json.default-charset" was provided; it will be ignored; verify that the dependency extension for this configuration is set or that you did not make a typo
2026-10-26T19:38:48.1020504Z 16:38:16 WARN  [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.config] (main) [SISPI][MED][GESTAO] Unrecognized configuration key "quarkus.http.encoding.enabled" was provided; it will be ignored; verify that the dependency extension for this configuration is set or that you did not make a typo
2026-10-26T19:38:48.1020945Z 16:38:17 WARN  [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.tl.ru.CertificateRecorder] (main) [SISPI][MED][GESTAO] TLS certificate validation disabled via trust-all configuration - name: <default>
2026-10-26T19:38:48.1021404Z 16:38:17 WARN  [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.tl.ru.CertificateRecorder] (main) [SISPI][MED][GESTAO] This configuration is INSECURE and must not be used in production
2026-10-26T19:38:48.1021866Z 16:38:18 INFO  [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.quarkus] (main) [SISPI][MED][GESTAO] sispi-med-gestao 1.0.0-SNAPSHOT on JVM (powered by Quarkus 3.40.1) started in 4.149s. Listening on: http://0.0.0.0:8080
2026-10-26T19:38:48.1022206Z 16:38:18 INFO  [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.quarkus] (main) [SISPI][MED][GESTAO] Profile prod activated. 
2026-10-26T19:38:48.1022809Z 16:38:18 INFO  [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.quarkus] (main) [SISPI][MED][GESTAO] Installed features: [agroal, cache, cdi, correlation-id, hibernate-orm, hibernate-validator, jdbc-oracle, narayana-jta, problem-details, rest, rest-client, rest-client-jackson, rest-jackson, scheduler, servlet, smallrye-context-propagation, smallrye-fault-tolerance, smallrye-health, smallrye-openapi, swagger-ui, token-service, validacao-token, vertx]
2026-10-26T19:38:48.1170776Z ##[section]Finishing: Logs da Aplicação


2026-10-26T19:38:48.1189806Z ##[section]Starting: Resumo da Release
2026-10-26T19:38:48.1192960Z ==============================================================================
2026-10-26T19:38:48.1193044Z Task         : Bash
2026-10-26T19:38:48.1193086Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-26T19:38:48.1193158Z Version      : 3.227.0
2026-10-26T19:38:48.1193290Z Author       : Microsoft Corporation
2026-10-26T19:38:48.1193340Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-26T19:38:48.1193412Z ==============================================================================
2026-10-26T19:38:48.2697058Z Generating script.
2026-10-26T19:38:48.2711252Z ========================== Starting Command Output ===========================
2026-10-26T19:38:48.2719157Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/6dcce650-2a05-414c-99f0-fcacad6a897f.sh
2026-10-26T19:38:48.2787404Z URL do Projeto no OKD: api.pixnprd4.caixa:6443/console/project/sispi-des/overview
2026-10-26T19:38:48.2795669Z /opt/ads-agent/_work/_temp/6dcce650-2a05-414c-99f0-fcacad6a897f.sh: line 92: CONTEXTO_JBOSS: command not found
2026-10-26T19:38:48.3629109Z APP Publicada na URL: https://sispi-med-gestao-des.apps.pixnprd4.caixa
2026-10-26T19:38:48.3737583Z ##[section]Finishing: Resumo da Release


<img width="1895" height="963" alt="image" src="https://github.com/user-attachments/assets/6730c591-f2f7-47f5-a185-26617c85ed06" />




