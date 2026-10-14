Skip to main content
Azure DevOps
projetos
/
Caixa
/
Pipelines
/
Releases
/
SIIFX-caixinhas-api-aplicacao
/
SIIFX-caixinhas-api-aplicacao-20261014.1305-1.0.13.00010-SNAPSHOT(1)
Search


Caixa

Overview

Boards

Repos

Pipelines
Pipelines
Environments
Releases
Library
Task groups
Deployment groups
Portal Infra

Test Plans

Artifacts
Project settings
SIIFX-caixinhas-api-aplicacao

SIIFX-caixinhas-api-aplicacao-20261014.1305-1.0.13.00010-SNAPSHOT(1)


EC DES

Succeeded


Pipeline

Tasks

Variables

Logs

Tests
Agent job
Started: 14/10/2026, 13:13:15
Pool:
Release-Linux-OKD4
·
Agent: azp-ads-agent-release-5cd876f98-2xqqd

1m 30s

Initialize job
·
succeeded
<1s

Pre-job: Download secure file
·
succeeded
1s

Download Artifacts
·
succeeded
1 warning
<1s

Exportando as variáveis do arquivo Trust Store
·
succeeded
<1s

Recuperando nome do repositório
·
succeeded
1s

Convertendo Minúsculo e Definindo nome do Projeto/Repositório
·
succeeded
<1s

Git clone https://devops.caixa/projetos/Infraestrutura/_git/esteira-logs
·
succeeded
<1s

Cria Streams Graylog
·
succeeded
3s

Recupera VEC
·
succeeded
<1s

VEC - Aferição
·
succeeded
1 warning
<1s

Login OpenShift
·
succeeded
<1s

Exportando Variáveis de Ambiente "_ENV."
·
succeeded
<1s

Criando novo Projeto
·
succeeded
<1s

Adicionando ISTIO_INJECTION
·
skipped


Criando nova APP
·
succeeded
<1s

Atualizando Variáveis de Ambiente
·
succeeded
2s

Criando Rota Customizada
·
succeeded
<1s

Aplicando Service Mesh
·
skipped


Git clone https://devops.caixa/projetos/Infraestrutura/_git/esteira-beyondtrust-check
·
succeeded
<1s

Create BT Secret
·
succeeded
<1s

Create BT Shared Volume
·
succeeded
<1s

Create BT Sidecar
·
succeeded
<1s

Create Secret Check Script
·
succeeded
<1s

Create Secret Check
·
succeeded
<1s

Create BT App Mount Volume
·
succeeded
<1s

Exporta Variáveis de Ambiente "_SECRET."
·
succeeded
<1s

Alterando valores placeholder no exec_secret.sh
·
succeeded
<1s

Criando Secrets
·
succeeded
<1s

Vinculando Secrets
·
succeeded
<1s

Adicionando Multiplas Secrets
·
succeeded
<1s

Executando Tag na Imagem do ambiente de build OKD3, OKD4 e OCP
·
succeeded
20s

Concedendo Acesso OKD
·
succeeded
<1s

Verificando IP de Saída
·
succeeded
<1s

Configurando IP de Saída - deployment
·
skipped


Configurando IP de Saída - deploymentconfig
·
succeeded
<1s

Cadastrando no Portal IIF
·
succeeded
<1s

Verificando Status do Deployment
·
succeeded
46s

Logs da Aplicação
·
succeeded
<1s

Resumo da Release
·
succeeded
<1s

Coletando dados da imagem
·
succeeded
3s

Atualizando versão no PortalIF
·
succeeded
<1s

Realizando Logout OKD
·
succeeded
<1s

Finalize Job
·
succeeded
<1s
Row 7. Clickable

Showing 6 filtered items.

Get started and run this pipeline for the first time!

19 pipelines found

Select a release pipeline to view its releases

16 pipelines found

Select a release pipeline to view its releases

5 pipelines found

Select a release pipeline to view its releases

2 pipelines found

Row 2

Row 2

Showing filters 1 through 2

Row 2



o caixihas que tava dano o meoso esrro usa a mesma libary passou

2026-10-14T16:14:42.0272460Z ##[section]Starting: Logs da Aplicação
2026-10-14T16:14:42.0275414Z ==============================================================================
2026-10-14T16:14:42.0275488Z Task         : Bash
2026-10-14T16:14:42.0275538Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-14T16:14:42.0275602Z Version      : 3.227.0
2026-10-14T16:14:42.0275645Z Author       : Microsoft Corporation
2026-10-14T16:14:42.0275704Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-14T16:14:42.0275776Z ==============================================================================
2026-10-14T16:14:42.2159826Z Generating script.
2026-10-14T16:14:42.2172412Z ========================== Starting Command Output ===========================
2026-10-14T16:14:42.2179120Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/7230d081-f7b1-4798-904b-734ad45b0ce6.sh
2026-10-14T16:14:42.2229141Z + shopt -s expand_aliases
2026-10-14T16:14:42.2229302Z + [[ -n okd4_nprd ]]
2026-10-14T16:14:42.2229468Z + [[ okd4_nprd =~ ocp ]]
2026-10-14T16:14:42.2229667Z + [[ -n okd4_nprd ]]
2026-10-14T16:14:42.2229780Z + [[ okd4_nprd =~ (okd4|openshift) ]]
2026-10-14T16:14:42.2229951Z + app=siifx-caixinhas-api-aplicacao-des
2026-10-14T16:14:42.2230065Z + oc version
2026-10-14T16:14:42.2885083Z Client Version: v4.2.0-alpha.0-1394-g45460a5
2026-10-14T16:14:42.2885343Z Server Version: 4.12.0-0.okd-2023-04-16-041331
2026-10-14T16:14:42.2885543Z Kubernetes Version: v1.25.0-2824+27e744f55d2e99-dirty
2026-10-14T16:14:42.2919041Z ++ oc get pod -l name=siifx-caixinhas-api-aplicacao-des -n siifx-des -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-10-14T16:14:42.2919352Z ++ tac
2026-10-14T16:14:42.2921190Z ++ grep -v '^$'
2026-10-14T16:14:42.2921301Z ++ head -n1
2026-10-14T16:14:42.3750518Z + last_pod=siifx-caixinhas-api-aplicacao-des-72-rkr7s
2026-10-14T16:14:42.3750805Z + echo 'Logs do POD: siifx-caixinhas-api-aplicacao-des-72-rkr7s'
2026-10-14T16:14:42.3751063Z + oc logs siifx-caixinhas-api-aplicacao-des-72-rkr7s -c siifx-caixinhas-api-aplicacao-des -n siifx-des
2026-10-14T16:14:42.3751306Z Logs do POD: siifx-caixinhas-api-aplicacao-des-72-rkr7s
2026-10-14T16:14:42.4578392Z exec java -Dquarkus.http.host=0.0.0.0 -Dquarkus.http.port=8080 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Djavax.net.ssl.trustStore=/deployments/caixa-truststore-acteste-nprd.jks -javaagent:/deployments/lib/main/com.microsoft.azure.applicationinsights-agent-3.7.1.jar -Dhttps.proxyHost=proxydes.caixa -Dhttps.proxyPort=80 -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/quarkus-run.jar
2026-10-14T16:14:42.4579259Z OpenJDK 64-Bit Server VM warning: Sharing is only supported for boot loader classes because bootstrap classpath has been appended
2026-10-14T16:14:42.4579879Z 2026-10-14 13:14:10.124-03:00 WARN  i.o.s.a.ResourceConfiguration - Found reference to io.opentelemetry.sdk.autoconfigure.internal.EnvironmentResourceProvider in otel.java.enabled.resource.providers. Please update to io.opentelemetry.sdk.autoconfigure.EnvironmentResourceProvider. Support for the old provider name will be removed after 1.49.0.
2026-10-14T16:14:42.4580344Z 2026-10-14 13:14:12.796-03:00 INFO  c.m.applicationinsights.agent - Application Insights Java Agent 3.7.1 started successfully (PID 8, JVM running for 5.947 s)
2026-10-14T16:14:42.4580686Z 2026-10-14 13:14:12.797-03:00 INFO  c.m.applicationinsights.agent - Java version: 21.0.1, vendor: Oracle Corporation, home: /usr/java/jdk-21.0.1
2026-10-14T16:14:42.4580871Z __  ____  __  _____   ___  __ ____  ______ 
2026-10-14T16:14:42.4581031Z  --/ __ \/ / / / _ | / _ \/ //_/ / / / __/ 
2026-10-14T16:14:42.4581180Z  -/ /_/ / /_/ / __ |/ , _/ ,< / /_/ /\ \   
2026-10-14T16:14:42.4581336Z --\___\_\____/_/ |_/_/|_/_/|_|\____/___/   
2026-10-14T16:14:42.4581582Z 2026-10-14 13:14:18 [] INFO  io.mi.co.in.pu.PushMeterRegistry - publishing metrics for AzureMonitorMeterRegistry every 1m
2026-10-14T16:14:42.4581976Z 2026-10-14 13:14:19 [] WARN  io.qu.config - Unrecognized configuration key "quarkus.smallrye-openapi.generate" was provided; it will be ignored; verify that the dependency extension for this configuration is set or that you did not make a typo
2026-10-14T16:14:42.4582481Z 2026-10-14 13:14:23 [] WARN  or.hi.or.jdbc - HHH100123: Low default JDBC fetch size: 10 (consider setting 'hibernate.jdbc.fetch_size')
2026-10-14T16:14:42.4582833Z 2026-10-14 13:14:25 [] INFO  io.quarkus - caixinhas 1.0.13.00010 on JVM (powered by Quarkus 3.33.2.1) started in 13.000s. Listening on: http://0.0.0.0:8080
2026-10-14T16:14:42.4583091Z 2026-10-14 13:14:25 [] INFO  io.quarkus - Profile prod activated. 
2026-10-14T16:14:42.4583616Z 2026-10-14 13:14:25 [] INFO  io.quarkus - Installed features: [agroal, cache, cdi, hibernate-orm, hibernate-orm-panache, hibernate-validator, jdbc-h2, jdbc-oracle, micrometer, narayana-jta, oidc, oidc-client, rest, rest-client, rest-client-jackson, rest-client-oidc-filter, rest-jackson, security, smallrye-context-propagation, smallrye-fault-tolerance, smallrye-health, smallrye-openapi, swagger-ui, vertx]
2026-10-14T16:14:42.4667295Z ##[section]Finishing: Logs da Aplicação






