1s
Run caixagithub/DevSecOps-Actions/.github/integrations/argocd/logs@main
  with:
    ARGOCD_SERVER: https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io
    ARGOCD_APP: caixagithub/silce-gestao-operacional
    AMBIENTE: DES
    IMAGE_TAG: 39603505605
    HEALTH_CHECK_WAS_SUCCESSFUL: false
  env:
    APIM_VERSIONAPI: 
    APIM_displaynameAPI: 
    APIM_PATH: 
    APIM_SWAGGERPATH: 
    APIM_TAGSAPI: 
    APIM_POLICIESALLOPERATIONSPATH: 
    AZ_INSTALL_STATUS: ms_repo_ok
    AZ_VERSION: latest
    INSTALL_PREREQUISITES: true
    AZ_LATEST_VERSION: 2.91.0
    environment: des
    repository_suffix: infranprd
    REPO: silce-gestao-operacional
    JOB_ID: 166063
    ARGOCD_AUTH_TOKEN: ***
Formate ARGO REPOSITORY
0s
Run echo "REPO_NAME=$(echo 'caixagithub/silce-gestao-operacional' | cut -d'/' -f2)" >> $GITHUB_ENV
    echo "REPO_NAME=$(echo 'caixagithub/silce-gestao-operacional' | cut -d'/' -f2)" >> $GITHUB_ENV
    echo "INPUT_IMAGE_TAG: '39603505605'"
    echo "AMBIENTE_LOWER=$(echo 'DES' | tr '[:upper:]' '[:lower:]')" >> $GITHUB_ENV
    shell: /usr/bin/bash --noprofile --norc -e -o pipefail {0}
    env:
      APIM_VERSIONAPI: 
      APIM_displaynameAPI: 
      APIM_PATH: 
      APIM_SWAGGERPATH: 
      APIM_TAGSAPI: 
      APIM_POLICIESALLOPERATIONSPATH: 
      AZ_INSTALL_STATUS: ms_repo_ok
      AZ_VERSION: latest
      INSTALL_PREREQUISITES: true
      AZ_LATEST_VERSION: 2.91.0
      environment: des
      repository_suffix: infranprd
      REPO: silce-gestao-operacional
      JOB_ID: 166063
      ARGOCD_AUTH_TOKEN: ***
  INPUT_IMAGE_TAG: '39603505605'
Coletando logs dos pods
0s
Run RESOURCE_TREE_URL="https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io/api/v1/applications/silce-gestao-operacional-des/resource-tree?appNamespace=openshift-gitops"
    RESOURCE_TREE_URL="https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io/api/v1/applications/silce-gestao-operacional-des/resource-tree?appNamespace=openshift-gitops"
    echo "Fazendo requisição para: ${RESOURCE_TREE_URL}"
    
    RESOURCE_TREE_JSON=$(curl -s -H "Authorization: ***" "${RESOURCE_TREE_URL}")
    if [ $? -ne 0 ]; then
      echo "Erro ao fazer requisição para o resource-tree"
      exit 1
    fi
    
    echo "Resource-tree obtido com sucesso"
    
    echo "Filtrando pods e encontrando o mais recente..."
    
    LATEST_POD=$(echo "$RESOURCE_TREE_JSON" | jq -r '
      .nodes // [] |
      map(select(.kind == "Pod" and .createdAt != null)) |
      sort_by(.createdAt) |
      last |
      .name // empty
    ')
    
    if [ -z "$LATEST_POD" ]; then
      echo "Nenhum pod encontrado ou JSON não contém dados esperados"
      exit 0
    fi
    
    echo "Pod mais recente encontrado: ${LATEST_POD}"
    
    LOGS_URL="https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io/api/v1/applications/silce-gestao-operacional-des/logs?appNamespace=openshift-gitops&container=silce-gestao-operacional-des&namespace=silce-gestao-operacional&follow=false&podName=${LATEST_POD}&tailLines=1000&sinceSeconds=0"
    echo "URL dos logs: ${LOGS_URL}"
    
    LOGS_RESPONSE=$(curl -s -H "Authorization: ***" "${LOGS_URL}")
    
    if [ $? -ne 0 ]; then
      echo "Erro ao obter logs do pod"
      exit 1
    fi
    
    echo "Logs obtidos com sucesso"
    echo "Logs do pod ${LATEST_POD}:"
    echo "================================================"
    
    echo "Exibindo os Logs:"
    echo "$LOGS_RESPONSE" | jq -r '.result.content'
    
    echo "================================================"
    echo "Script executado com sucesso!"
    echo "Pod utilizado: ${LATEST_POD}"
    
    if [ "false" = "false" ]; then
      echo "Falha na sincronização"
      exit 1
    fi
    shell: /usr/bin/bash --noprofile --norc -e -o pipefail {0}
    env:
      APIM_VERSIONAPI: 
      APIM_displaynameAPI: 
      APIM_PATH: 
      APIM_SWAGGERPATH: 
      APIM_TAGSAPI: 
      APIM_POLICIESALLOPERATIONSPATH: 
      AZ_INSTALL_STATUS: ms_repo_ok
      AZ_VERSION: latest
      INSTALL_PREREQUISITES: true
      AZ_LATEST_VERSION: 2.91.0
      environment: des
      repository_suffix: infranprd
      REPO: silce-gestao-operacional
      JOB_ID: 166063
      ARGOCD_AUTH_TOKEN: ***
      REPO_NAME: silce-gestao-operacional
      AMBIENTE_LOWER: des
  Fazendo requisição para: https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io/api/v1/applications/silce-gestao-operacional-des/resource-tree?appNamespace=openshift-gitops
  Resource-tree obtido com sucesso
  Filtrando pods e encontrando o mais recente...
  Pod mais recente encontrado: silce-gestao-operacional-des-b9bdbf96c-8f864
  URL dos logs: https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io/api/v1/applications/silce-gestao-operacional-des/logs?appNamespace=openshift-gitops&container=silce-gestao-operacional-des&namespace=silce-gestao-operacional&follow=false&podName=silce-gestao-operacional-des-b9bdbf96c-8f864&tailLines=1000&sinceSeconds=0
  Logs obtidos com sucesso
  Logs do pod silce-gestao-operacional-des-b9bdbf96c-8f864:
  ================================================
  Exibindo os Logs:
  I1021 13:06:24.844258       1 version.go:31] "version info" version="" commit="1e11cd2" buildDate="2024-10-04T10:20:06Z" component="vaultenv"
  I1021 13:06:24.844367       1 main.go:184] "azure key vault env injector initializing"
  I1021 13:06:24.844585       1 main.go:253] "found original container command" cmd="/usr/bin/java" args=["java","-jar","/opt/deploy/quarkus-run.jar"]
  I1021 13:06:24.844642       1 authentication.go:110] "checking if current auth service credentials are stale" url="http://akv2k8s-envinjector.akv2k8s.svc:80/auth/silce-gestao-operacional/silce-gestao-operacional-des-b9bdbf96c-8f864?secret=akv2k8s-silce-gestao-operacional-des"
  I1021 13:06:25.004514       1 authentication.go:123] "auth service credentials ok" url="http://akv2k8s-envinjector.akv2k8s.svc:80/auth/silce-gestao-operacional/silce-gestao-operacional-des-b9bdbf96c-8f864?secret=akv2k8s-silce-gestao-operacional-des"
  I1021 13:06:25.005529       1 authentication.go:159] "requesting azure key vault oauth token" url="https://akv2k8s-envinjector.akv2k8s.svc:9443/auth/silce-gestao-operacional/silce-gestao-operacional-des-b9bdbf96c-8f864"
  I1021 13:06:25.038798       1 authentication.go:179] "successfully received oauth token"
  I1021 13:06:25.238902       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="silce-gestao-operacional/akvs-env-gestao-datasource-password" env="DATABASE_PASSWORD"
  I1021 13:06:25.301509       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="silce-gestao-operacional/akvs-env-servicebus-password" env="SERVICE_BUS_PASSWORD"
  I1021 13:06:25.374130       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="silce-gestao-operacional/akvs-env-mkp-apikey" env="MKP_APIKEY"
  I1021 13:06:25.436258       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="silce-gestao-operacional/akvs-env-compra-datasource-password" env="QUARKUS_DATASOURCE__COMPRA__PASSWORD"
  I1021 13:06:25.436288       1 main.go:343] "starting process with secrets in env vars" cmd="/usr/bin/java" args=["java","-jar","/opt/deploy/quarkus-run.jar"]
  __  ____  __  _____   ___  __ ____  ______
   --/ __ \/ / / / _ | / _ \/ //_/ / / / __/
   -/ /_/ / /_/ / __ |/ , _/ ,< / /_/ /\ \
  --\___\_\____/_/ |_/_/|_/_/|_|\____/___/
  2026-10-21 10:06:32,860 WARN  [io.qua.config] (main) The "quarkus.hibernate-orm.database.generation" config property is deprecated and should not be used anymore.
  2026-10-21 10:06:35,470 WARN  [io.qua.ope.run.tra.int.ver.OpenTelemetryVertxTracingFactory$VertxDelegator] (vert.x-eventloop-thread-0) VertxTracer delegate not set. Will not submit this trace. SpanKind: RPC; Request: io.vertx.core.http.impl.HttpRequestHead@7995f69b; Operation:GET.
  2026-10-21 10:06:35,512 WARN  [io.qua.ope.run.tra.int.ver.OpenTelemetryVertxTracingFactory$VertxDelegator] (vert.x-eventloop-thread-0) VertxTracer delegate not set. Will not submit this trace. Response: io.vertx.core.http.impl.HttpResponseHead@d37ed65; Failure: null.
  2026-10-21 10:06:35,805 WARN  [io.qua.ope.run.tra.int.ver.OpenTelemetryVertxTracingFactory$VertxDelegator] (vert.x-eventloop-thread-0) VertxTracer delegate not set. Will not submit this trace. SpanKind: RPC; Request: io.vertx.core.http.impl.HttpRequestHead@6f5a9cc7; Operation:GET.
  2026-10-21 10:06:35,856 WARN  [io.qua.ope.run.tra.int.ver.OpenTelemetryVertxTracingFactory$VertxDelegator] (vert.x-eventloop-thread-0) VertxTracer delegate not set. Will not submit this trace. Response: io.vertx.core.http.impl.HttpResponseHead@179219ba; Failure: null.
  2026-10-21 10:06:35,861 WARN  [io.qua.ope.run.tra.int.ver.OpenTelemetryVertxTracingFactory$VertxDelegator] (vert.x-eventloop-thread-0) VertxTracer delegate not set. Will not submit this trace. SpanKind: RPC; Request: io.vertx.core.http.impl.HttpRequestHead@596d451d; Operation:GET.
  2026-10-21 10:06:35,953 WARN  [io.qua.ope.run.tra.int.ver.OpenTelemetryVertxTracingFactory$VertxDelegator] (vert.x-eventloop-thread-0) VertxTracer delegate not set. Will not submit this trace. Response: io.vertx.core.http.impl.HttpResponseHead@83e1720; Failure: null.
  2026-10-21 10:06:36,155 WARN  [io.qua.ope.run.tra.int.ver.OpenTelemetryVertxTracingFactory$VertxDelegator] (vert.x-eventloop-thread-0) VertxTracer delegate not set. Will not submit this trace. SpanKind: RPC; Request: io.vertx.core.http.impl.HttpRequestHead@1cfedafc; Operation:GET.
  2026-10-21 10:06:36,298 WARN  [io.qua.ope.run.tra.int.ver.OpenTelemetryVertxTracingFactory$VertxDelegator] (vert.x-eventloop-thread-0) VertxTracer delegate not set. Will not submit this trace. Response: io.vertx.core.http.impl.HttpResponseHead@4beb1a50; Failure: null.
  2026-10-21 10:06:36,300 WARN  [io.qua.ope.run.tra.int.ver.OpenTelemetryVertxTracingFactory$VertxDelegator] (vert.x-eventloop-thread-0) VertxTracer delegate not set. Will not submit this trace. SpanKind: RPC; Request: io.vertx.core.http.impl.HttpRequestHead@15917c68; Operation:GET.
  2026-10-21 10:06:36,424 WARN  [io.qua.ope.run.tra.int.ver.OpenTelemetryVertxTracingFactory$VertxDelegator] (vert.x-eventloop-thread-0) VertxTracer delegate not set. Will not submit this trace. Response: io.vertx.core.http.impl.HttpResponseHead@6ab8b9db; Failure: null.
  2026-10-21 10:06:36,756 INFO  [io.qua.hib.orm.run.JPAConfig] (main) Hibernate ORM persistence unit 'compra' was deactivated through configuration properties
  2026-10-21 10:06:39,684 WARN  [io.qua.run.log.LoggingSetupRecorder] (main) Log level TRACE for category 'org.hibernate.type.descriptor.sql.BasicBinder' set below minimum logging level DEBUG, promoting it to DEBUG. Set the build time configuration property 'quarkus.log.category."org.hibernate.type.descriptor.sql.BasicBinder".min-level' to 'TRACE' to avoid this warning
  2026-10-21 10:06:39,882 WARN  [io.sma.rea.mes.jms] (main) Please add one of the additional mapping modules (-jsonb or -jackson) to be able to (de)serialize JSON messages.
  2026-10-21 10:06:43,155 INFO  [io.quarkus] (main) silce-gestao 1.0.0-SNAPSHOT on JVM (powered by Quarkus 3.28.5) started in 17.662s. Listening on: http://0.0.0.0:8080
  2026-10-21 10:06:43,156 INFO  [io.quarkus] (main) Profile prod activated.
  2026-10-21 10:06:43,156 INFO  [io.quarkus] (main) Installed features: [agroal, cache, cdi, hibernate-orm, hibernate-orm-panache, hibernate-orm-rest-data-panache, hibernate-validator, jdbc-h2, jdbc-mssql, messaging, narayana-jta, oidc, oidc-client, opentelemetry, rest, rest-client, rest-client-jackson, rest-client-oidc-filter, rest-jackson, rest-links, security, smallrye-context-propagation, smallrye-health, smallrye-jwt, smallrye-openapi, vertx]
  
  ================================================
  Script executado com sucesso!
  Pod utilizado: silce-gestao-operacional-des-b9bdbf96c-8f864
  Falha na sincronização
  Error: Process completed with exit code 1.


  <img width="1896" height="915" alt="image" src="https://github.com/user-attachments/assets/46a0c5b7-cd65-406b-af4d-b3f6b1c63728" />
