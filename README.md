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
SIPPG-proposta-pf
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
All pipelines

SIPPG

SIPPG-proposta-pf
Predefined variables
Filter by keywords
Scope


AMBIENTE
des
AMBIENTE
tqs
AMBIENTE
prd
AMBIENTE_BUILD
build-images-ads
CGC_UNIDADE_DES
7390
CGC_UNIDADE_OPS
7259
fortify_disable
false
PASSWORD_TRUSTSTORE
changeit
SISTEMAAMBIENTE
des
SISTEMAAMBIENTE
tqs
SISTEMAAMBIENTE
prd
SISTEMANOME
sippg-proposta-pf
SITE
okd4_nprd
SITE
okd4_prd
TemplateRelease_OKD
openshift/quarkus-caixa-release
UNIDADE
BR
Row 2. Clickable

Row 2. Clickable

Row 2. Clickable

Collapsed

Expanded

Select a release pipeline to view its releases

19 pipelines found

Select a release pipeline to view its releases

16 pipelines found

Select a release pipeline to view its releases

2 pipelines found

Row 3

Row 2

Showing filters 1 through 2

Row 2

1 pipelines found

Row 2

Row 2

Showing filters 1 through 2

Showing filters 1 through 2




2026-10-23T19:41:21.4441504Z ##[section]Starting: Atualizando Variáveis de Ambiente
2026-10-23T19:41:21.4444546Z ==============================================================================
2026-10-23T19:41:21.4444727Z Task         : Bash
2026-10-23T19:41:21.4444779Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-23T19:41:21.4444841Z Version      : 3.227.0
2026-10-23T19:41:21.4444883Z Author       : Microsoft Corporation
2026-10-23T19:41:21.4444941Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-23T19:41:21.4445012Z ==============================================================================
2026-10-23T19:41:21.5720898Z Generating script.
2026-10-23T19:41:21.5732024Z ========================== Starting Command Output ===========================
2026-10-23T19:41:21.5739404Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/0391dbe0-f330-4da4-8799-9836fe32e568.sh
2026-10-23T19:41:21.5932725Z Nova APP: false
2026-10-23T19:41:21.7443297Z /opt/ads-agent/_work/_temp/0391dbe0-f330-4da4-8799-9836fe32e568.sh: line 23: syntax error in conditional expression
2026-10-23T19:41:21.7481278Z ##[error]Bash exited with code '2'.
2026-10-23T19:41:21.7496776Z ##[section]Finishing: Atualizando Variáveis de Ambiente



Skip to main content
projetos
/
Caixa
/
Pipelines
/
Releases
/
SIPPG-proposta-pf
Search








All pipelines

SIPPG

SIPPG-proposta-pf
Predefined variables
SonarQube Variables (1)
Variáveis com dados do SonarQube
Scopes: Release
SONAR_URL
http://sonar.produtos.caixa
Usuario-Azure-DevOps (12)
Scopes: Release
AZPAT
********
AZUSER
s736639
BT_API_URL
https://sicsn.caixa/BeyondTrust/api/public/v3
BT_SECRETS_PATH
********
FORTIFY_API
https://novocodigoseguro.caixa/ssc/api/v1
FORTIFY_APITOKEN
********
FORTIFY_PASS
********
FORTIFY_USER
admin
OKD_KAFKA
api.kafka-nprd.caixa:6443
OKD_TOKEN_KAFKA
********
TOKEN_CRQ
********
URL_CRQ
https://infradevops-novoportal-backend-prd.apps.produtos4.caixa/api.php?acao=devopsCaixacriarMudancaPadrao
MONITORACAO_LOGS (4)
REQ000143540550 - Conforme autorizado na req por FLAVIO ALMEIDA GAGLIARDI, removido as variáveis JAVA_OPTS_MONITORING e URL_APM_SERVER, por entrar em conflitos com releases que utilizam o Application Insights
Scopes: Release
DIR_LOGS
/opt/ads-agent/esteira-logs
GRAYLOG_PASSWORD
********
GRAYLOG_USERNAME
API_CLIENT
REPOSITORY_LOGS
https://devops.caixa/projetos/Infraestrutura/_git/esteira-logs
EGRESS_IP_OKD (81)
WO0000072264656 - Config Portal Infrafácil NO_PROXY
Scopes: Release
ALOCAIP_AMBIENTE
Aplicacao
ALOCAIP_AMBIENTE_OCP
Aplicacao
ALOCAIP_AMBIENTE_OCP_LOTERIAS_PRD
Cloud
ALOCAIP_AMBIENTE_OCP_PRD
Cloud
ALOCAIP_AMBIENTE_OKD4
Aplicacao
ALOCAIP_AMBIENTE_OKD4_PRD_CTC
Cloud
ALOCAIP_AMBIENTE_OPENSHIFT_LOTERIAS_NPRD
Desenvolvimento
ALOCAIP_AMBIENTE_OPENSHIFT_LOTERIAS_PRD
Cloud
ALOCAIP_AMBIENTE_PRD_CANAIS
Cloud
ALOCAIP_AMBIENTE_PRD_DTC
Cloud
ALOCAIP_CATEGORIA
Linux
ALOCAIP_CATEGORIA_OKD4_PRD_CTC
Linux
ALOCAIP_FIM_RANGE_OCP
10.116.223.250
ALOCAIP_FIM_RANGE_OCP_LOTERIAS_PRD
10.190.64.200
ALOCAIP_FIM_RANGE_OCP_PRD
10.118.121.250
ALOCAIP_FIM_RANGE_OKD4
10.116.215.250
ALOCAIP_FIM_RANGE_OKD4_PRD_CTC
10.121.103.250
ALOCAIP_FIM_RANGE_OPENSHIFT_LOTERIAS_NPRD
10.190.160.254
ALOCAIP_FIM_RANGE_OPENSHIFT_LOTERIAS_PRD
10.190.255.253
ALOCAIP_FIM_RANGE_PRD_CANAIS_CTC
10.118.97.255
ALOCAIP_FIM_RANGE_PRD_CANAIS_CTC_OB
10.118.97.254
ALOCAIP_FIM_RANGE_PRD_CANAIS_DTC
10.220.225.255
ALOCAIP_FIM_RANGE_PRD_DTC
10.221.101.250
ALOCAIP_ID
"C&t@d02"
ALOCAIP_INICIO_RANGE_OCP
10.116.223.1
ALOCAIP_INICIO_RANGE_OCP_LOTERIAS_PRD
10.190.64.161
ALOCAIP_INICIO_RANGE_OCP_PRD
10.118.121.1
ALOCAIP_INICIO_RANGE_OKD4
10.116.209.0
ALOCAIP_INICIO_RANGE_OKD4_PRD_CTC
10.121.101.1
ALOCAIP_INICIO_RANGE_OPENSHIFT_LOTERIAS_NPRD
10.190.160.201
ALOCAIP_INICIO_RANGE_OPENSHIFT_LOTERIAS_PRD
10.190.255.245
ALOCAIP_INICIO_RANGE_PRD_CANAIS_CTC
10.118.96.100
ALOCAIP_INICIO_RANGE_PRD_CANAIS_CTC_OB
10.118.97.100
ALOCAIP_INICIO_RANGE_PRD_CANAIS_DTC
10.220.224.100
ALOCAIP_INICIO_RANGE_PRD_DTC
10.221.100.100
ALOCAIP_RED_NUM
3022
ALOCAIP_RED_NUM_OCP
4995
ALOCAIP_RED_NUM_OCP_LOTERIAS_PRD
13616
ALOCAIP_RED_NUM_OCP_PRD
6053
ALOCAIP_RED_NUM_OKD4
4995
ALOCAIP_RED_NUM_OKD4_PRD_CTC
4996
ALOCAIP_RED_NUM_OPENSHIFT_LOTERIAS_NPRD
14583
ALOCAIP_RED_NUM_OPENSHIFT_LOTERIAS_PRD
14582
ALOCAIP_RED_NUM_PRD
4104
ALOCAIP_RED_NUM_PRD_CANAIS_CTC
6053
ALOCAIP_RED_NUM_PRD_CANAIS_DTC
6055
ALOCAIP_RED_NUM_PRD_DTC
5199
ALOCAIP_SENHA
********
ALOCAIP_SITE
CTC
ALOCAIP_SITE_DTC
DTC
ALOCAIP_SITE_OCP
CTC
ALOCAIP_SITE_OCP_LOTERIAS_PRD
CTC
ALOCAIP_SITE_OCP_PRD
CTC
ALOCAIP_SITE_OKD4
CTC
ALOCAIP_SITE_OKD4_PRD_CTC
CTC
ALOCAIP_SITE_OPENSHIFT_LOTERIAS_NPRD
CTC
ALOCAIP_SITE_OPENSHIFT_LOTERIAS_PRD
CTC
ALOCAIP_UNIDADE
CEPTIBR
ALOCAIP_UNIDADE_OCP
CEPTI
ALOCAIP_UNIDADE_OCP_LOTERIAS_PRD
CETAD
ALOCAIP_UNIDADE_OCP_PRD
CETAD
ALOCAIP_UNIDADE_OKD4
CEPTI
ALOCAIP_UNIDADE_OKD4_PRD_CTC
CETAD
ALOCAIP_UNIDADE_OPENSHIFT_LOTERIAS_NPRD
CETAD
ALOCAIP_UNIDADE_OPENSHIFT_LOTERIAS_PRD
CETAD
ALOCAIP_UNIDADE_PRD_CANAIS
CETAD
ALOCAIP_UNIDADE_PRD_DTC
CETAD
ALOCAIP_VERTICAL
Desenvolvimento
ALOCAIP_VERTICAL_OCP
Desenvolvimento
ALOCAIP_VERTICAL_OCP_LOTERIAS_PRD
Cloud
ALOCAIP_VERTICAL_OCP_PRD
IBC
ALOCAIP_VERTICAL_OKD4
Desenvolvimento
ALOCAIP_VERTICAL_OKD4_PRD_CTC
Vertical_Nao_PCN
ALOCAIP_VERTICAL_OPENSHIFT_LOTERIAS_NPRD
Cloud
ALOCAIP_VERTICAL_OPENSHIFT_LOTERIAS_PRD
Cloud
ALOCAIP_VERTICAL_PRD_CANAIS
IBC
ALOCAIP_VERTICAL_PRD_DTC
Vertical Nao PCN
APIALOCAIP
https://api.alocaip.telecom.caixa
PASSWORD_CGC
********
PORTALIF
https://infradevops-novoportal-backend-prd.apps.produtos4.caixa
USER_CGC
USR_CETADPOR1
OKD-REGISTRY-CENTRALIZADO (7)
Credenciais para o Registry Centralizado - Produtos 4 (OKD)
Scopes: Release
KIND_DEPLOY
deploymentconfig
OKD_API_REGISTRY
api.produtos4.caixa:6443
OKD_REGISTRY
default-route-openshift-image-registry.apps.produtos4.caixa
OKD_TOKEN_REGISTRY
********
OKD_USER_SERVICE_REGISTRY
ads-sa
ProjetoBuild
build-images-ads
TIMEOUT_DEPLOY
300
OKD-4-NPRD (12)
Credenciais para o Cluster OKD4 de NPRD (DES/TQS/HMP)
Scopes: EC DES,EC TQS
CI_NAME
7366CLU-OKD4-NPRD
KIND_DEPLOY
deploymentconfig
OKD_4_API
api.nprd.caixa:6443
OKD_4_REGISTRY
default-route-openshift-image-registry.apps.nprd.caixa
OKD_4_TOKEN
********
OKD_4_URL_SUFFIX
apps.nprd.caixa
OKD_4_USER_SERVICE
ads-sa
OKD_URL_SUFFIX
apps.nprd.caixa
OKD_USER_SERVICE
ads-sa
TIMEOUT_DEPLOY
600
TOKEN_CRQ
********
URL_CRQ
https://infradevops-novoportal-backend-prd.apps.produtos4.caixa/api.php?acao=devopsCaixacriarMudancaPadrao
SIPPG-PROPOSTA-PF-DES (51)
Grupo de variáveis de SIPPG-PROPOSTA-PF-DES
Scopes: EC DES
VAULT_LOCATION
/usr/src/app/secrets_files/SIPPG_DES/
_ENV.API_CPP_URL
https://apitest.cpp.app.br/cpp-api-test
_ENV.API_INTRANET_API_KEY
'${SIPPG_BT_APIKEY}'
_ENV.API_INTRANET_URL
https://api.des.caixa:8443
_ENV.API_SIPPG_REMUNERACAO_URL
https://sippg-remuneracao-des.apps.nprd.caixa/cartoes/cartao-pre-pago/remuneracao
_ENV.API_SIPPG_URL
https://sippg-api-des.apps.nprd.caixa/sippg-api/cartaoprepago
_ENV.APPLICATIONINSIGHTS_CONNECTION_STRING
"InstrumentationKey=589c8f57-f18b-412c-ba31-79db9a5182d2;IngestionEndpoint=https://brazilsouth-1.in.applicationinsights.azure.com/;LiveEndpoint=https://brazilsouth.livediagnostics.monitor.azure.com/;ApplicationId=e49df5bc-89ba-414d-b99f-fdae3487af63"
_ENV.APPLICATIONINSIGHTS_INSTRUMENTATION_LOGGING_LEVEL
INFO
_ENV.APPLICATIONINSIGHTS_PROXY
http://proxydes.caixa:80
_ENV.APPLICATIONINSIGHTS_ROLE_NAME
SIPPG-PROPOSTA-PF-DES
_ENV.APPLICATIONINSIGHTS_SAMPLING_PERCENTAGE
100
_ENV.APPLICATIONINSIGHTS_SELF_DIAGNOSTICS_LEVEL
INFO
_ENV.CACHE_CPP_ANTIFRAUDE
true
_ENV.CACHE_CPP_ANTIFRAUDE_AFTER_WRITE
86400S
_ENV.CACHE_CPP_PLANOS
true
_ENV.CACHE_CPP_PLANOS_AFTER_WRITE
86400S
_ENV.CACHE_SICLI_PF_EXPIRE_AFTER_WRITE
86400S
_ENV.CPP_APIKEY
'${SIPPG_BT_APIKEY_CPP}'
_ENV.CPP_APIKEY_HEADER
Ocp-Apim-Subscription-Key
_ENV.CPP_KEY_STORE_FILE
/deployments/sippg_tqs_caixa_gov_br_serpro.p12
_ENV.CPP_KEY_STORE_PW
'${SIPPG_KEYSTORE_CPP}'
_ENV.CPP_TRUST_STORE_FILE
/deployments/caixa-truststore-acteste-nprd.jks
_ENV.CPP_TRUST_STORE_PW
'${SIPPG_TRUSTSTORE_CPP}'
_ENV.CRYPT_CARTAO_PASSWORD
'${SIPPG_CRYPT_PASSWORD}'
_ENV.EMAIL_ORIGEM
cesob275@caixa.gov.br
_ENV.EMAIL_SMTP_PORT
25
_ENV.EMAIL_SMTP_SERVER
smtptest.correiolivre.caixa
_ENV.EMAIL_USER
S739002
_ENV.EMAIL_USER_PASS
'${S739002_SMTP}'
_ENV.FEATURE_FLAG_SIPCS_VIRTUAL_ENABLE
true
_ENV.FTP_PROXY
http://proxydes.caixa:80
_ENV.HTTPS_PROXY
http://proxydes.caixa:80
_ENV.HTTP_PROXY
http://proxydes.caixa:80
_ENV.JAVA_OPTIONS_APPEND
"-Djavax.net.ssl.trustStore=/deployments/caixa-truststore-acteste-nprd.jks -javaagent:/deployments/lib/main/com.microsoft.azure.applicationinsights-agent-3.7.8.jar"
_ENV.NO_PROXY
localhost,127.0.0.1,*.caixa
_ENV.PROXY_CAIXA_PORT
80
_ENV.PROXY_CAIXA_PROTOCOL
http
_ENV.PROXY_CAIXA_URL
proxydes.caixa
_ENV.QUARKUS_DATASOURCE_JDBC_URL
jdbc:oracle:thin:@oracle-nprd-1000.caixa:1521/prim_D01NGSRV
_ENV.QUARKUS_DATASOURCE_PASSWORD
'${SPPGBD01_ORACLE}'
_ENV.QUARKUS_DATASOURCE_USERNAME
SPPGBD01
_ENV.QUARKUS_HTTP_SSL_CERTIFICATE_KEY-STORE-PASSWORD
'${SIPPG_KEYSTORE_CPP}'
_ENV.SIPPG_AMBIENTE
DES
_ENV.SSO_CLIENT_SECRET_PPG
'${CLISERPPG_SSO_INTRA}'
_ENV.SSO_CLIENT_SERVICE_PPG
cli-ser-ppg
_ENV.SSO_INTERNET_PUBLICKEY
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAxz8PNmiUW5J1669pWY0APB4flqqDnghAv/QV5DIHyXE39fj9u1DPXbgfDUhUfK0i/B0CHJukbI44Rgo/vuhCMImTnLjS49XuTH6GI4lU/CtdzE/qACMO/GUky73m0Uszo2Bh1wNV+fvw/mMQVAGKj6/qXjSB9npRZKydoXnwGPIepcrqF6KkMJIFtZ+0w35J9SYwgLNezUbAJgs9dq3yMj4ussSfxMFcUC9UKziJJSg0UQfl0fOQGMsrsnUbS2GgXeDqdskbZq9/wfL0ikU2pWf0hKjX+PXtqZI0SVWurVyydc0efbTE7qIlrwF8lWZ8NZ8zcV2oVk7TjoIktZ4zBwIDAQAB
_ENV.SSO_INTERNET_SERVER
https://logindes.caixa.gov.br/auth/realms/internet
_ENV.SSO_INTRANET_PUBLICKEY
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAzcYY/UbvrEldbQRd4TgLeP9bS8YnaL67MZUsfozWRyocBF3S0L7UEbkPaPoCoBnhoRv8VJHp0grqe3mqEmkMuDlt20Vx6q04ADDyS0c8xaU+Ot+g1Pgwjze944ATUjZogEMko6jvqqUGTt/Nt64yCCIaMaTB119vOBExQim7vPHNe/o7hLxh6VBYINxFA/esxjz8j28/uJWIiK0Gvt07Yx7ycn2DJlQHjnH2GzCSUL87AAYmjyYxW2JZaPLLvRlpcHIWrlr9GNtLiq0++xfJ0jFYxQWs1jxhlfXdqr8NE5vfA/RRRjRFnWzFOhIsOnIHPO9eEwwYzCZSoW2zXkFDYwIDAQAB
_ENV.SSO_INTRANET_SERVER
https://login.des.caixa/auth/realms/intranet
_ENV.quarkus.http.ssl.certificate.key-store-file
/deployments/sippg_tqs_caixa_gov_br_serpro.p12
_SECRET.SMALLRYE.CONFIG.SOURCE.FILE.LOCATIONS
#{VAULT_LOCATION}#
SIPPG-PROPOSTA-PF-BT-VAULT-DES (1)
Scopes: EC DES
BT_SECRETS_LIST
SIPPG_DES/CLISERPPG_SSO_INTRA,SIPPG_DES/SIPPG_BT_APIKEY,SIPPG_DES/SPPGBD01_ORACLE,SIPPG_DES/S739002_SMTP,SIPPG_DES/SIPPG_CRYPT_PASSWORD,SIPPG_DES/SIPPG_BT_APIKEY_CPP,SIPPG_DES/SIPPG_KEYSTORE_CPP,SIPPG_DES/SIPPG_TRUSTSTORE_CPP
SIPPG-BT-VAULT-SECRET-DES (2)
Scopes: EC DES
BT_CLIENT_ID
74e729f6-acce-4764-a75f-bcc5f0cfa42b
BT_CLIENT_SECRET
********
SIPPG-PROPOSTA-PF-TQS (52)
Grupo de variáveis de SIPPG-PROPOSTA-PF-TQS
Scopes: EC TQS
VAULT_LOCATION
/usr/src/app/secrets_files/SIPPG_TQS/
_ENV.API_CPP_URL
https://apitest.cpp.app.br/cpp-api-test
_ENV.API_INTRANET_API_KEY
'${SIPPG_BT_APIKEY}'
_ENV.API_INTRANET_URL
https://api.des.caixa:8443
_ENV.API_SIPPG_REMUNERACAO_URL
https://sippg-remuneracao-tqs.apps.nprd.caixa/cartoes/cartao-pre-pago/remuneracao
_ENV.API_SIPPG_URL
https://sippg-api-tqs.apps.nprd.caixa/sippg-api/cartaoprepago
_ENV.APPLICATIONINSIGHTS_CONNECTION_STRING
"InstrumentationKey=589c8f57-f18b-412c-ba31-79db9a5182d2;IngestionEndpoint=https://brazilsouth-1.in.applicationinsights.azure.com/;LiveEndpoint=https://brazilsouth.livediagnostics.monitor.azure.com/;ApplicationId=e49df5bc-89ba-414d-b99f-fdae3487af63"
_ENV.APPLICATIONINSIGHTS_INSTRUMENTATION_LOGGING_LEVEL
INFO
_ENV.APPLICATIONINSIGHTS_PROXY
http://proxydes.caixa:80
_ENV.APPLICATIONINSIGHTS_ROLE_NAME
SIPPG-PROPOSTA-PF-TQS
_ENV.APPLICATIONINSIGHTS_SAMPLING_PERCENTAGE
100
_ENV.APPLICATIONINSIGHTS_SELF_DIAGNOSTICS_LEVEL
INFO
_ENV.CACHE_CPP_ANTIFRAUDE
true
_ENV.CACHE_CPP_ANTIFRAUDE_AFTER_WRITE
86400S
_ENV.CACHE_CPP_PLANOS
true
_ENV.CACHE_CPP_PLANOS_AFTER_WRITE
86400S
_ENV.CACHE_SICLI_PF_EXPIRE_AFTER_WRITE
86400S
_ENV.CPP_APIKEY
'${SIPPG_BT_APIKEY_CPP}'
_ENV.CPP_APIKEY_HEADER
Ocp-Apim-Subscription-Key
_ENV.CPP_KEY_STORE_FILE
/deployments/sippg_tqs_caixa_gov_br_serpro.p12
_ENV.CPP_KEY_STORE_PW
'${SIPPG_KEYSTORE_CPP}'
_ENV.CPP_TRUST_STORE_FILE
/deployments/caixa-truststore-acteste-nprd.jks
_ENV.CPP_TRUST_STORE_PW
'${SIPPG_TRUSTSTORE_CPP}'
_ENV.CRYPT_CARTAO_PASSWORD
'${SIPPG_CRYPT_PASSWORD}'
_ENV.EMAIL_ORIGEM
cesob275@caixa.gov.br
_ENV.EMAIL_SMTP_PORT
25
_ENV.EMAIL_SMTP_SERVER
smtptest.correiolivre.caixa
_ENV.EMAIL_USER
S739002
_ENV.EMAIL_USER_PASS
''${S739002_SMTP}'
_ENV.FEATURE_FLAG_EMAIL_TAGPF_ENABLE
true
_ENV.FEATURE_FLAG_SIPCS_VIRTUAL_ENABLE
true
_ENV.FTP_PROXY
http://proxydes.caixa:80
_ENV.HTTPS_PROXY
http://proxydes.caixa:80
_ENV.HTTP_PROXY
http://proxydes.caixa:80
_ENV.JAVA_OPTIONS_APPEND
"-Djavax.net.ssl.trustStore=/deployments/caixa-truststore-acteste-nprd.jks"
_ENV.NO_PROXY
localhost,127.0.0.1,*.caixa
_ENV.PROXY_CAIXA_PORT
80
_ENV.PROXY_CAIXA_PROTOCOL
http
_ENV.PROXY_CAIXA_URL
proxydes.caixa
_ENV.QUARKUS_DATASOURCE_JDBC_URL
jdbc:oracle:thin:@cnpexdadvm01-scan5.extra.caixa.gov.br:1521/prim_T01NGSRV
_ENV.QUARKUS_DATASOURCE_PASSWORD
'${SPPGBT01_ORACLE}'
_ENV.QUARKUS_DATASOURCE_USERNAME
SPPGBT01
_ENV.QUARKUS_HTTP_SSL_CERTIFICATE_KEY-STORE-PASSWORD
'${SIPPG_KEYSTORE_CPP}'
_ENV.SIPPG_AMBIENTE
TQS
_ENV.SSO_CLIENT_SECRET_PPG
'${CLISERPPG_SSO_INTRA}'
_ENV.SSO_CLIENT_SERVICE_PPG
cli-ser-ppg
_ENV.SSO_INTERNET_PUBLICKEY
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAxz8PNmiUW5J1669pWY0APB4flqqDnghAv/QV5DIHyXE39fj9u1DPXbgfDUhUfK0i/B0CHJukbI44Rgo/vuhCMImTnLjS49XuTH6GI4lU/CtdzE/qACMO/GUky73m0Uszo2Bh1wNV+fvw/mMQVAGKj6/qXjSB9npRZKydoXnwGPIepcrqF6KkMJIFtZ+0w35J9SYwgLNezUbAJgs9dq3yMj4ussSfxMFcUC9UKziJJSg0UQfl0fOQGMsrsnUbS2GgXeDqdskbZq9/wfL0ikU2pWf0hKjX+PXtqZI0SVWurVyydc0efbTE7qIlrwF8lWZ8NZ8zcV2oVk7TjoIktZ4zBwIDAQAB
_ENV.SSO_INTERNET_SERVER
https://logindes.caixa.gov.br/auth/realms/internet
_ENV.SSO_INTRANET_PUBLICKEY
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAzcYY/UbvrEldbQRd4TgLeP9bS8YnaL67MZUsfozWRyocBF3S0L7UEbkPaPoCoBnhoRv8VJHp0grqe3mqEmkMuDlt20Vx6q04ADDyS0c8xaU+Ot+g1Pgwjze944ATUjZogEMko6jvqqUGTt/Nt64yCCIaMaTB119vOBExQim7vPHNe/o7hLxh6VBYINxFA/esxjz8j28/uJWIiK0Gvt07Yx7ycn2DJlQHjnH2GzCSUL87AAYmjyYxW2JZaPLLvRlpcHIWrlr9GNtLiq0++xfJ0jFYxQWs1jxhlfXdqr8NE5vfA/RRRjRFnWzFOhIsOnIHPO9eEwwYzCZSoW2zXkFDYwIDAQAB
_ENV.SSO_INTRANET_SERVER
https://login.des.caixa/auth/realms/intranet
_ENV.quarkus.http.ssl.certificate.key-store-file
/deployments/sippg_tqs_caixa_gov_br_serpro.p12
_SECRET.SMALLRYE.CONFIG.SOURCE.FILE.LOCATIONS
#{VAULT_LOCATION}#
SIPPG-PROPOSTA-PF-BT-VAULT-TQS (1)
Scopes: EC TQS
BT_SECRETS_LIST
SIPPG_TQS/CLISERPPG_SSO_INTRA,SIPPG_TQS/SIPPG_BT_APIKEY,SIPPG_TQS/SPPGBT01_ORACLE,SIPPG_TQS/S739002_SMTP,SIPPG_TQS/SIPPG_CRYPT_PASSWORD,SIPPG_TQS/SIPPG_BT_APIKEY_CPP,SIPPG_TQS/SIPPG_KEYSTORE_CPP,SIPPG_TQS/SIPPG_TRUSTSTORE_CPP
SIPPG-BT-VAULT-SECRET-TQS (2)
Scopes: EC TQS
BT_CLIENT_ID
cc7e9007-eb8f-4bef-86b7-231c04cd31b9
BT_CLIENT_SECRET
********
OKD-4-APL (12)
Scopes: EC PRD
CI_NAME
7366CLU-OKD-APL
CLIENT_ID
cli-web-ceh-sdceh
KIND_DEPLOY
deploymentconfig
OKD_4_API_APL
https://api.apl4.caixa:6443
OKD_4_TOKEN_APL
********
OKD_4_URL_SUFFIX_APL
apps.apl4.caixa
OKD_4_USER_SERVICE_APL
ads-sa
OKD_URL_SUFFIX_APL
apps.apl4.caixa
OKD_USER_SERVICE
ads-sa
TIMEOUT_DEPLOY
900
TOKEN_CRQ
********
URL_CRQ
https://infradevops-novoportal-backend-prd.apps.produtos4.caixa/api.php?acao=devopsCaixacriarMudancaPadrao
SIPPG-PROPOSTA-PF-PRD (49)
Grupo de variáveis de SIPPG-PROPOSTA-PF-PRD

Scopes: EC PRD
APIKEY_CPP_CYPT
********
API_INTRANET_API_KEY
********
CPP_APIKEY
********
CPP_KEY_STORE_PW
********
CPP_TRUST_STORE_PW
********
CRYPT_CARTAO_PASSWORD
********
EMAIL_USER_PASS
********
QUARKUS_DATASOURCE_PASSWORD
********
SSO_CLIENT_SECRET_PPG
********
_ENV.APIKEY_CPP_CYPT_HEADER
x-api-key
_ENV.API_CPP_URL
https://api.cpp.app.br/cpp-api-prod
_ENV.API_INTRANET_URL
https://api.caixa:8443
_ENV.API_SIPPG_REMUNERACAO_URL
https://sippg-remuneracao-prd.apps.apl4.caixa/cartoes/cartao-pre-pago/remuneracao
_ENV.API_SIPPG_URL
https://sippg-api-prd.apps.apl4.caixa/sippg-api/cartaoprepago
_ENV.APPLICATIONINSIGHTS_CONNECTION_STRING
"InstrumentationKey=cd2fcf83-1b92-4fbf-adb8-d4b3f46a5c52;IngestionEndpoint=https://southcentralus-3.in.applicationinsights.azure.com/;LiveEndpoint=https://southcentralus.livediagnostics.monitor.azure.com/;ApplicationId=50693336-5296-4ab3-8b3e-497373d8ce5f"
_ENV.APPLICATIONINSIGHTS_INSTRUMENTATION_LOGGING_LEVEL
INFO
_ENV.APPLICATIONINSIGHTS_PROXY
http://proxynuvem.caixa:80
_ENV.APPLICATIONINSIGHTS_ROLE_NAME
SIPPG-PROPOSTA-PF-PRD
_ENV.APPLICATIONINSIGHTS_SAMPLING_PERCENTAGE
100
_ENV.APPLICATIONINSIGHTS_SELF_DIAGNOSTICS_LEVEL
INFO
_ENV.CPP_APIKEY_HEADER
Ocp-Apim-Subscription-Key
_ENV.CPP_CYPT
https://cyptgw.fleetcor.com.br
_ENV.CPP_KEY_STORE_FILE
/deployments/sippg_caixa_gov_br_2025.p12
_ENV.CPP_TRUST_STORE_FILE
/deployments/sippg-truststore_prd_v6.jks
_ENV.EMAIL_ORIGEM
prepagos@aplicacao.caixa.gov.br
_ENV.EMAIL_SMTP_PORT
25
_ENV.EMAIL_SMTP_SERVER
correioexternoapl.caixa
_ENV.EMAIL_USER
cartoescaixa@aplicacao.caixa.gov.br
_ENV.FEATURE_FLAG_SIPCS_VIRTUAL_ENABLE
true
_ENV.JAVA_OPTIONS_APPEND
"-Djavax.net.ssl.trustStore=/deployments/sippg-truststore_prd_v7.jks -javaagent:/deployments/lib/main/com.microsoft.azure.applicationinsights-agent-3.7.8.jar"
_ENV.PROXY_CAIXA_PORT
80
_ENV.PROXY_CAIXA_PROTOCOL
http
_ENV.PROXY_CAIXA_URL
proxyprd.caixa
_ENV.QUARKUS_DATASOURCE_JDBC_URL
jdbc:oracle:thin:@cadecrk03cl01scan.intra.caixa.gov.br:1521/CDBP07NGPDB002
_ENV.QUARKUS_DATASOURCE_USERNAME
SPPGPB01
_ENV.SSO_CLIENT_SERVICE_PPG
cli-ser-ppg
_ENV.SSO_INTRANET_PUBLICKEY
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA0KLpORcQdKU59iMD7KlHXIF6bNYERSRBkGpY5YSLBzbIZLNkRps/8B06QgK+Q+eRE4ufaEOGc78mfGz6z0w5UxH2k7II3NVzGcjsb9qz7ooa3fJAgkrQaHQlt6UsOtFvUQeoQ0BOaBgdguhCZ9NPhP4uqKXa8ERFuP9g7Gns5d2livChAbjOwDAGLUUuuQnqL2xpG5wGMF/ZRu160PMO1/q7/VAVW5TipixIQ8FDY8FvBgS27qOeX0nKmx47Qs7zwnv9TafuiBZ7Nt7Ko+UYtrjMnmneJHPOec+vwaaO7ahyhh8j2eqsnNjO5StYLiPytvhr43Dei1vbwe22jNJvNQIDAQAB
_ENV.SSO_INTRANET_SERVER
https://login.prd.caixa/auth/realms/intranet
_ENV.quarkus.http.ssl.certificate.key-store-file
/deployments/sippg_caixa_gov_br_2025.p12
_SECRET.APIKEY_CPP_CYPT
#{APIKEY_CPP_CYPT}#
_SECRET.API_INTRANET_API_KEY
#{API_INTRANET_API_KEY}#
_SECRET.CPP_APIKEY
#{CPP_APIKEY}#
_SECRET.CPP_KEY_STORE_PW
#{CPP_KEY_STORE_PW}#
_SECRET.CPP_TRUST_STORE_PW
#{CPP_TRUST_STORE_PW}#
_SECRET.CRYPT_CARTAO_PASSWORD
#{CRYPT_CARTAO_PASSWORD}#
_SECRET.EMAIL_USER_PASS
#{EMAIL_USER_PASS}#
_SECRET.QUARKUS_DATASOURCE_PASSWORD
#{QUARKUS_DATASOURCE_PASSWORD}#
_SECRET.QUARKUS_HTTP_SSL_CERTIFICATE_KEY-STORE-PASSWORD
#{CPP_KEY_STORE_PW}#
_SECRET.SSO_CLIENT_SECRET_PPG
#{SSO_CLIENT_SECRET_PPG}#
|Manage variable groups
Row 2. Clickable

Row 2. Clickable

Collapsed

Expanded

19 pipelines found

Select a release pipeline to view its releases

16 pipelines found

Select a release pipeline to view its releases

2 pipelines found

Row 3

Row 2

Showing filters 1 through 2

Row 2

1 pipelines found

Row 2

Row 2

Showing filters 1 through 2

Showing filters 1 through 2

Row 2

Showing filters 1 through 2


