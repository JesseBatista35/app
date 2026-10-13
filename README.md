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
SINFS-okd4
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
SINFS

SINFS-okd4
Predefined variables
SonarQube Variables (1)
Variáveis com dados do SonarQube
Scopes: Release
Usuario-Azure-DevOps (12)
Scopes: Release
EGRESS_IP_OKD (81)
WO0000072264656 - Config Portal Infrafácil NO_PROXY
Scopes: Release
MONITORACAO_LOGS (4)
REQ000143540550 - Conforme autorizado na req por FLAVIO ALMEIDA GAGLIARDI, removido as variáveis JAVA_OPTS_MONITORING e URL_APM_SERVER, por entrar em conflitos com releases que utilizam o Application Insights
Scopes: Release
SINFS-des (34)
Scopes: OKD4 EC DES
OKD-4-NPRD (12)
Credenciais para o Cluster OKD4 de NPRD (DES/TQS/HMP)
Scopes: OKD4 EC DES,OKD4 EC TQS,OKD4 EC HMP
OKD-REGISTRY-CENTRALIZADO (7)
Credenciais para o Registry Centralizado - Produtos 4 (OKD)
Scopes: OKD4 EC DES,OKD4 EC TQS,OKD4 EC HMP,OKD4 EC PRD
SINFS-BT-VAULT-DES (1)
WO0000080991099
Scopes: OKD4 EC DES
BT_SECRETS_LIST
SINFS_DES/JCICSDIRECT,SINFS_DES/SSO_SENHA,SINFS_DES/TGNFSNFDV_SENHA,SINFS_DES/TGSGRS142_SENHA,SINFS_DES/TGSGRS143_SENHA,SINFS_DES/TGSGRS144_SENHA
SINFS-BT-VAULT-SECRET-DES (2)
WO0000080991099
Scopes: OKD4 EC DES
BT_CLIENT_ID
3d9ed850-192e-4709-82e4-ff4a2e53268d
BT_CLIENT_SECRET
********
SINFS-tqs (30)
Scopes: OKD4 EC TQS
DB2_SENHA
********
DB2_URL
jdbc:db2://10.216.80.111:446/RJKDB2DSDH:currentSchema=TQSNFS;
DB2_USER
SNFSTR01
EXT
jks
JCICSDIRECT
10.216.80.111
JCONNECTOR
/tmp/sinfs_jconnector.properties
JVM_HEAP_MAX
2048m
JVM_HEAP_MIN
1024m
JVM_METASPACE_MAX
512m
JVM_METASPACE_MIN
256m
KEYCLOAK_SSL_REQUIRED
ALL
SISGR_WS_AUTH
https://webservice.acessoseguro.sso.tqs.intra.corerj.caixa
SSO_SENHA
********
SSO_URL
https://login.tqs.caixa/auth
TGNFSNFDV_SENHA
********
TGNFSNFDV_USER
SNFSTR01
TGSGRS142_SENHA
********
TGSGRS142_USER
JDIRSGRQ
TGSGRS143_SENHA
********
TGSGRS143_USER
JDIRSGRQ
TGSGRS144_SENHA
********
TGSGRS144_USER
JDIRSGRQ
TRUSTSTORE_SENHA
changeit
TRUSTSTORE_VALUE
/opt/jboss/standalone/configuration/cacerts_sinfs_intra_tqs2
URL_PROXY
proxydes.caixa
_ENV.APPLICATIONINSIGHTS_CONNECTION_STRING
"InstrumentationKey=8148a712-eee7-4c41-95ef-5153b19d0497;IngestionEndpoint=https://southcentralus-3.in.applicationinsights.azure.com/;LiveEndpoint=https://southcentralus.livediagnostics.monitor.azure.com/;ApplicationId=8c7e524c-9be9-44ee-894c-6d034d92a7f5"
_ENV.APPLICATIONINSIGHTS_INSTRUMENTATION_LOGGING_LEVEL
INFO
_ENV.APPLICATIONINSIGHTS_ROLE_NAME
SINFS-tqs
_ENV.APPLICATIONINSIGHTS_SAMPLING_PERCENTAGE
100
_ENV.APPLICATIONINSIGHTS_SELF_DIAGNOSTICS_LEVEL
INFO
SINFS-BT-VAULT-TQS (1)
WO0000081007679
Scopes: OKD4 EC TQS
BT_SECRETS_LIST
SINFS_TQS/JCICSDIRECT,SINFS_TQS/SSO_SENHA,SINFS_TQS/TGNFSNFDV_SENHA
SINFS-BT-VAULT-SECRET-TQS (2)
WO0000081007679

Scopes: OKD4 EC TQS
BT_CLIENT_ID
4c3c08e8-336e-4fa1-9919-e5f9f730f865
BT_CLIENT_SECRET
********
SINFS-prd (24)
Scopes: OKD4 EC PRD
OKD-4-APL (12)
Scopes: OKD4 EC PRD
|Manage variable groups
OKD4 EC TQSDeploy release

Showing filters 1 through 2

Showing filters 1 through 2

Showing 26 deployments

OKD4 EC TQSDeploy release

Showing 26 deployments

OKD4 EC TQSDeploy release

Collapsed

Expanded

Row 3

Collapsed

Row 2

Showing filters 1 through 2

Row 2

OKD4 EC TQSDeploy release

Expanded

Row 3

Collapsed

Row 2

Showing filters 1 through 2



novo pod

P
sinfs-tqs-17-4ddnk
Init:CrashLoopBackOff

ERRO: Nao foram encontrados arquivos com segredos no diretorio '/usr/src/app/secrets_files'.
