A release SIGSJ-alvara-20261020.1646-3.0.12.1-SNAPSHOT(1) falhou.

Gostaria de entender a razão para a falha, que não parece registrada em nenhuma das etapas da subida.

https://devops.caixa/projetos/Caixa/_releaseProgress?_a=release-pipeline-progress&releaseId=543669

Agradeço desde já!


O ERRO

2026-10-20T19:52:30.4133144Z ##[section]Starting: Verificando Status do Deployment
2026-10-20T19:52:30.4136769Z ==============================================================================
2026-10-20T19:52:30.4136861Z Task         : Bash
2026-10-20T19:52:30.4136902Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-20T19:52:30.4136962Z Version      : 3.227.0
2026-10-20T19:52:30.4137018Z Author       : Microsoft Corporation
2026-10-20T19:52:30.4137066Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-20T19:52:30.4137134Z ==============================================================================
2026-10-20T19:52:31.1021840Z Generating script.
2026-10-20T19:52:31.1033208Z ========================== Starting Command Output ===========================
2026-10-20T19:52:31.1040893Z [command]/bin/bash /opt/ads-agent/_work/_temp/b2f73ea9-446f-4dc9-88f3-1156a5ee65ce.sh
2026-10-20T19:52:31.2135313Z Waiting for rollout to finish: 1 old replicas are pending termination...
2026-10-20T19:58:37.9240879Z ##[error]The task has timed out.
2026-10-20T19:58:37.9241866Z ##[section]Finishing: Verificando Status do Deployment


2026-10-20T19:58:37.9267129Z ##[section]Starting: Logs da Aplicação
2026-10-20T19:58:37.9270943Z ==============================================================================
2026-10-20T19:58:37.9271046Z Task         : Bash
2026-10-20T19:58:37.9271091Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-20T19:58:37.9271153Z Version      : 3.227.0
2026-10-20T19:58:37.9271216Z Author       : Microsoft Corporation
2026-10-20T19:58:37.9271304Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-20T19:58:37.9271394Z ==============================================================================
2026-10-20T19:58:39.0389282Z Generating script.
2026-10-20T19:58:39.0400421Z ========================== Starting Command Output ===========================
2026-10-20T19:58:39.0408062Z [command]/bin/bash /opt/ads-agent/_work/_temp/394e06af-7396-44fa-895e-374e0e1eb2d6.sh
2026-10-20T19:58:39.0468206Z + shopt -s expand_aliases
2026-10-20T19:58:39.0469473Z + [[ -n okd4_nprd ]]
2026-10-20T19:58:39.0469730Z + [[ okd4_nprd =~ ocp ]]
2026-10-20T19:58:39.0469905Z + [[ -n okd4_nprd ]]
2026-10-20T19:58:39.0470065Z + [[ okd4_nprd =~ (okd4|openshift) ]]
2026-10-20T19:58:39.0472618Z + app=sigsj-alvara-des
2026-10-20T19:58:39.0473033Z + oc version
2026-10-20T19:58:39.1335517Z Client Version: v4.2.0-alpha.0-1650-g31aa3e8
2026-10-20T19:58:39.1335734Z Kustomize Version: v4.5.7
2026-10-20T19:58:39.1335914Z Server Version: 4.12.0-0.okd-2023-04-16-041331
2026-10-20T19:58:39.1336415Z Kubernetes Version: v1.25.0-2824+27e744f55d2e99-dirty
2026-10-20T19:58:39.1364367Z ++ oc get pod -l name=sigsj-alvara-des -n sigsj-des -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-10-20T19:58:39.1367408Z ++ tac
2026-10-20T19:58:39.1367697Z ++ grep -v '^$'
2026-10-20T19:58:39.1367805Z ++ head -n1
2026-10-20T19:58:39.2435017Z + last_pod=sigsj-alvara-des-693-gnfhp
2026-10-20T19:58:39.2435439Z + echo 'Logs do POD: sigsj-alvara-des-693-gnfhp'
2026-10-20T19:58:39.2435746Z + oc logs sigsj-alvara-des-693-gnfhp -c sigsj-alvara-des -n sigsj-des
2026-10-20T19:58:39.2436051Z Logs do POD: sigsj-alvara-des-693-gnfhp
2026-10-20T19:58:39.3515092Z exec java -Dquarkus.http.host=0.0.0.0 -Dquarkus.http.port=8080 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Djavax.net.ssl.trustStore=/deployments/caixa-truststore-acteste-nprd-sigsj-20260707.jks -Dotel.exporter.otlp.endpoint=https://otel-collector-nprd.cemot.cloud.caixa -Dhttps.proxyHost=proxydes.caixa -Dhttps.proxyPort=80 -Dhttp.nonProxyHosts=*.caixa|*.caixa.gov.br|apim-parceiros-sandbox.azure-api.net -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/quarkus-run.jar
2026-10-20T19:58:39.3597887Z ##[section]Finishing: Logs da Aplicação
