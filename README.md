
Using project "default".
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs sispi-qrcode-api-validador-des-297-fs9kn -n sispi-des --previous
Error from server (BadRequest): a container name must be specified for pod sispi-qrcode-api-validador-des-297-fs9kn, choose one of: [secrets-agent-sidecar secrets-check dynatrace-operator opentelemetry-auto-instrumentation-java sispi-qrcode-api-validador-des istio-proxy]
-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -s -w '\n%{http_code}\n' localhost:8080/q/health

000
-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -s -w '\n%{http_code}\n' localhost:8080/q/health/live

000
-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -s -w '\n%{http_code}\n' localhost:8080/q/health/ready

000
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc rollout history dc/sispi-qrcode-api-validador-des -n sispi-des
deploymentconfigs "sispi-qrcode-api-validador-des"
REVISION        STATUS          CAUSE
296             Complete        manual change
297             Complete        manual change
298             Failed          cancelled by the user
299             Failed          cancelled by the user
300             Failed          manual change
301             Failed          manual change
302             Failed          manual change
303             Failed          manual change
304             Failed          manual change
305             Failed          manual change
306             Failed          manual change
307             Failed          manual change
308             Failed          manual change
309             Failed          manual change

-sh-4.2$
-sh-4.2$
-sh-4.2$  oc rollout history dc/sispi-qrcode-api-validador-des -n sispi-des --revision=297
deploymentconfigs "sispi-qrcode-api-validador-des" with revision #297
Pod Template:
  Labels:       CGC_DES=7390
        CGC_OPS=7261
        app=sispi-qrcode-api-validador-des
        deployment=sispi-qrcode-api-validador-des-297
        deploymentconfig=sispi-qrcode-api-validador-des
        name=sispi-qrcode-api-validador-des
  Annotations:  instrumentation.opentelemetry.io/inject-java=true
        openshift.io/deployment-config.latest-version=297
        openshift.io/deployment-config.name=sispi-qrcode-api-validador-des
        openshift.io/deployment.name=sispi-qrcode-api-validador-des-297
        openshift.io/generated-by=OpenShiftNewApp
        sidecar.istio.io/inject=true
  Init Containers:
   secrets-agent-sidecar:
    Image:      default-route-openshift-image-registry.apps.produtos4.caixa/openshift/secrets-agent:v23.3.2
    Port:       <none>
    Host Port:  <none>
    Limits:
      memory:   400Mi
    Environment:
      SECRETS_PATH:     /usr/src/app/secrets_files
      BT_API_URL:       https://sicsn.caixa/BeyondTrust/api/public/v3
      CLIENT_ID:        <set to the key 'BT_CLIENT_ID' in secret 'bt-client-secret-sispi-qrcode-api-validador-des'>     Optional: false
      CLIENT_SECRET:    <set to the key 'BT_CLIENT_SECRET' in secret 'bt-client-secret-sispi-qrcode-api-validador-des'> Optional: false
      BT_API_VERSION:   3.1
      SECRETS_LIST:     SISPI_DES/SSPIBD04_ORACLE,SISPI_DES/SSPIBD03_ORACLE,SISPI_DES/SISPI_PROXY,SISPI_DES/SISPX/SSPXBD01_ORACLE_DG,SISPI_DES/SISPI_SECRET_INTRANET
      BT_VERIFY_CA:     False
    Mounts:
      /usr/src/app/secrets_files from secrets (rw)
   secrets-check:
    Image:      default-route-openshift-image-registry.apps.produtos4.caixa/openshift/ubi:9.3-1552
    Port:       <none>
    Host Port:  <none>
    Command:
      /bin/bash
      /script/bt-check.sh
    Environment:
      SECRETS_PATH:     /usr/src/app/secrets_files
      SECRETS_LIST:     SISPI_DES/SSPIBD04_ORACLE,SISPI_DES/SSPIBD03_ORACLE,SISPI_DES/SISPI_PROXY,SISPI_DES/SISPX/SSPXBD01_ORACLE_DG,SISPI_DES/SISPI_SECRET_INTRANET
    Mounts:
      /script from script-bt-volume (rw)
      /usr/src/app/secrets_files from secrets (rw)
  Containers:
   sispi-qrcode-api-validador-des:
    Image:      default-route-openshift-image-registry.apps.produtos4.caixa/build-images-ads/sispi-qrcode-api-validador:20261020.1640-0.0.1-SNAPSHOT
    Port:       8080/TCP
    Host Port:  0/TCP
    Limits:
      cpu:      1
      memory:   1Gi
    Requests:
      cpu:      30m
      memory:   1Gi
    Liveness:   http-get http://:8080/q/health/live delay=90s timeout=5s period=10s #success=1 #failure=3
    Readiness:  http-get http://:8080/q/health/ready delay=90s timeout=5s period=10s #success=1 #failure=3
    Environment:
      TZ:       America/Sao_Paulo
      CACHE_CERTIFICADOS_REFRESH_TIME_SEG:      1200s
      CACHE_CHAVESASSINATURA_REFRESH_TIME_SEG:  1200s
      DATASOURCE_SPX_PASSWORD:  ${SSPXBD01_ORACLE_DG}
      DATASOURCE_SPX_URL:       jdbc:oracle:thin:@cnpexdadvm01-scan4.extra.caixa.gov.br:1521/CDBD08NGPDB017
      DATASOURCE_SPX_USERNAME:  SSPXBD01
      JAVA_OPTIONS_APPEND:      -Djavax.net.ssl.trustStore=/deployments/caixa-truststore-cedesbr_azurepush_atualizado.jks
      JAVA_OPTS_MONITORING:     -javaagent:/opt/apm_agent/elastic-apm-agent.jar -Delastic.apm.config_file=/opt/apm_agent/elasticapm.properties -Delastic.apm.service_name=sispi -Delastic.apm.environment=des -Delastic.apm.application_packages=br.gov.caixa -Delastic.apm.server_urls=http://apm-server-devops.apps.produtos4.caixa -Delastic.apm.global_labels=deployment=sispi-qrcode-api-validador
      JAVA_TOOL_OPTIONS:        -Dfile.encoding=UTF8
      PIX_DICT_URL:     https://sispi-container-dict-des.apps.pixnprd4.caixa/
      PIX_SUPORTE_PROXY_BYPASS_FOR:     .caixa;.sispl-des;.sispl-tqs;.svc;sispi-qrcode-api-externo;sispx-pix-automatico-externo-api
      PIX_SUPORTE_PROXY_HOST:   proxydes.caixa
      PIX_SUPORTE_PROXY_PORTA:  80
      PIX_SUPORTE_PROXY_SENHA:  ${SISPI_PROXY}
      PIX_SUPORTE_PROXY_USUARIO:        s739019
      QUARKUS_DATASOURCE_DATAGUARD_JDBC_URL:    jdbc:oracle:thin:@(DESCRIPTION=(LOAD_BALANCE=off)(ADDRESS=(PROTOCOL=TCP)(HOST=10.116.101.16)(PORT=1521))(CONNECT_DATA=(SERVICE_NAME=CDBD08NGPDB017)(SERVER=DEDICATED)))
      QUARKUS_DATASOURCE_DATAGUARD_PASSWORD:    ${SSPIBD04_ORACLE}
      QUARKUS_DATASOURCE_DATAGUARD_USERNAME:    SSPIBD04
      QUARKUS_DATASOURCE_JDBC_URL:      jdbc:oracle:thin:@(DESCRIPTION=(LOAD_BALANCE=off)(ADDRESS=(PROTOCOL=TCP)(HOST=10.116.101.16)(PORT=1521))(CONNECT_DATA=(SERVICE_NAME=CDBD08NGPDB017)(SERVER=DEDICATED)))
      QUARKUS_DATASOURCE_PASSWORD:      ${SSPIBD03_ORACLE}
      QUARKUS_DATASOURCE_USERNAME:      SSPIBD03
      SISPI_CERTIFICADOS_CACHE_RESET:   0 */10 * ? * * *
      SISPI_CLIENT_ID_SPI:      cli-ser-spi
      SISPI_LOGIN_CAIXA_INTRANET_SECRET:        ${SISPI_SECRET_INTRANET}
      SISPI_PIX_URL_QRCODE:     pix-qrcode-h.caixa.gov.br
      SISPI_QRCODE_CACHE_RELOAD:        0 0/1 * ? * * *
      SISPI_QRCODE_CERTIFICADOS_CACHE_EVERY:    10m
      SISPI_QRCODE_CERTIFICADOS_CACHE_MAX_SIZE: 10000
      SISPI_QRCODE_DICT_CACHE_MAX_SIZE: 10000
      SISPI_QRCODE_DICT_CACHE_TTL_SECONDS:      300
      SISPI_QRCODE_JKU_CACHE_EVERY:     5m
      SISPI_QRCODE_JKU_CACHE_MAX_SIZE:  10000
      SISPI_QRCODE_JKU_CACHE_TTL_MINUTES:       5
      SISPI_QRCODE_QDT_RETRY:   3
      SISPI_QRCODE_TEMPO_DELAY: 5
      SISPI_QRCODE_URL_EXTERNA: pix-qrcode-h.caixa.gov.br
      SISPI_QRCODE_URL_INTERNA: sispi-qrcode-api-externo-des:8080
      SISPI_QRCODE_VALIDACAO_TIMEOUT:   5000
      SISPX_QRCODE_URL_INTERNA: sispx-pix-automatico-externo-api-des.sispx-des:8080
      SMALLRYE_CONFIG_SOURCE_FILE_LOCATIONS:    <set to the key 'SMALLRYE_CONFIG_SOURCE_FILE_LOCATIONS' in secret 'sispi-qrcode-api-validador-des'>     Optional: false
    Mounts:
      /deployments/caixa-truststore-acteste-nprd.jks from caixa-truststore-acteste-nprd (rw)
      /deployments/caixa-truststore-azurepush_2023.jks from caixa-truststore-azurepush-2023 (rw)
      /deployments/customhosts5 from customhosts5 (rw)
      /deployments/sispi-des-keystore.jks from sispi-des-keystore (rw)
      /usr/src/app/secrets_files from secrets (rw)
  Volumes:
   sispi-des-keystore:
    Type:       Secret (a volume populated by a Secret)
    SecretName: sispi-des-keystore
    Optional:   false
   secrets:
    Type:       EmptyDir (a temporary directory that shares a pod's lifetime)
    Medium:     Memory
   script-bt-volume:
    Type:       ConfigMap (a volume populated by a ConfigMap)
    Name:       sispi-qrcode-api-validador-des-script-bt-check
    Optional:   false
   customhosts5:
    Type:       Secret (a volume populated by a Secret)
    SecretName: customhosts5
    Optional:   false
   caixa-truststore-azurepush-2023:
    Type:       Secret (a volume populated by a Secret)
    SecretName: caixa-truststore-azurepush-2023
    Optional:   false
   caixa-truststore-acteste-nprd:
    Type:       Secret (a volume populated by a Secret)
    SecretName: caixa-truststore-acteste-nprd
    Optional:   false

-sh-4.2$
