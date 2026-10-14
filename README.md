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
SIMCN-backend
/
SIMCN-backend-2.110.9.2-SNAPSHOT(36)
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
SIMCN-backend

SIMCN-backend-2.110.9.2-SNAPSHOT(36)
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
MUDANCA_GSC (3)
WO0000079495945
Scopes: Release
ADAPTER_VARIABLES (9)
Variáveis disponíveis para todas os projetos do tipo ADAPTER.
Scopes: Release
OKD-REGISTRY-CENTRALIZADO (7)
Credenciais para o Registry Centralizado - Produtos 4 (OKD)
Scopes: Release
Compartilhamentos (4)
Scopes: Release
ID_ALOCAIP
C&t@d02
PW_ALOCAIP
********
PW_ISILON
********
USR_ISILON
s736651@corp.caixa.gov.br
OKD-4-NPRD (12)
Credenciais para o Cluster OKD4 de NPRD (DES/TQS/HMP)
Scopes: EC DES,EC TQS,EC HMP
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
SIMCN-BACKEND-DES (19)
Grupo de variáveis de SIMCN-BACKEND-DES
Scopes: EC DES
DATASOURCE_ORACLE_CONNECTION_URL
jdbc:oracle:thin:@oracle-nprd-1000.caixa:1521/prim_D01NGSRV
DATASOURCE_ORACLE_MAX_POOL_SIZE
50
DATASOURCE_ORACLE_MIN_POOL_SIZE
1
DATASOURCE_ORACLE_PASSWORD
********
DATASOURCE_ORACLE_USER_NAME
SMCNDB01
JVM_HEAP_MAX
2048m
JVM_HEAP_MIN
1024m
JVM_METASPACE_MAX
512m
JVM_METASPACE_MIN
96m
JVM_PASSWORD_TRUSTSTORE
changeit
PATH_DESTINO
/simcn
PATH_NFS
ifs/CADSVISISD4/SERVIDORES/CEPTIBR/UP_SIMCN/
SERVER_NFS
nfsctcnprd.ctc.caixa
SIZE_VOLUME
50Gi
STORAGE_PATH
/upload/des/simcn/conciliacao
TRUSTSTORE_FILE
/opt/jboss/standalone/configuration/caixa-truststore-acteste-nprd.jks
sso.client.id
cli-web-mcn
sso.realm
intranet
sso.url
https://login.des.caixa/auth
SIMCN-BACKEND-TQS (19)
Grupo de variáveis de SIMCN-BACKEND-TQS
Scopes: EC TQS
DATASOURCE_ORACLE_CONNECTION_URL
jdbc:oracle:thin:@cnpexdadvm02clu05.extra.caixa.gov.br:1521/ORAT01NG
DATASOURCE_ORACLE_MAX_POOL_SIZE
50
DATASOURCE_ORACLE_MIN_POOL_SIZE
1
DATASOURCE_ORACLE_PASSWORD
********
DATASOURCE_ORACLE_USER_NAME
********
JVM_HEAP_MAX
2048m
JVM_HEAP_MIN
1024m
JVM_METASPACE_MAX
512m
JVM_METASPACE_MIN
96m
JVM_PASSWORD_TRUSTSTORE
changeit
PATH_DESTINO
/simcn
PATH_NFS
/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/UP_SIMCN
SERVER_NFS
nfsctcnprd.ctc.caixa
SIZE_VOLUME
50Gi
STORAGE_PATH
/upload/des/simcn
TRUSTSTORE_FILE
/opt/jboss/standalone/configuration/caixa-truststore-acteste-nprd.jks
sso.client.id
cli-web-mcn
sso.realm
intranet
sso.url
https://login.des.caixa/auth
SIMCN-BACKEND-HMP (19)
Grupo de variáveis de SIMCN-BACKEND-HMP
Scopes: EC HMP
OKD-4-APL (12)
Scopes: EC PRD
SIMCN-BACKEND-PRD (19)
Grupo de variáveis de SIMCN-BACKEND-PRD
Scopes: EC PRD
71 pipelines found

Select a release pipeline to view its releases

2 pipelines found

Showing 25 deployments

EC DESDeploy release

Expanded

Row 3

Collapsed

Row 2

Expanded

Collapsed

8 pipelines found

Select a release pipeline to view its releases

3 pipelines found

Row 2

Row 2

Row 2

Row 2

Showing filters 1 through 2

