2026-10-13T14:50:22.5424224Z ##[section]Starting: Verificando Status do Deployment
2026-10-13T14:50:22.5427275Z ==============================================================================
2026-10-13T14:50:22.5427363Z Task         : Bash
2026-10-13T14:50:22.5427406Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-13T14:50:22.5427469Z Version      : 3.227.0
2026-10-13T14:50:22.5427522Z Author       : Microsoft Corporation
2026-10-13T14:50:22.5427572Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-13T14:50:22.5427644Z ==============================================================================
2026-10-13T14:50:22.6645819Z Generating script.
2026-10-13T14:50:22.6656148Z ========================== Starting Command Output ===========================
2026-10-13T14:50:22.6663340Z [command]/bin/bash /opt/ads-agent/_work/_temp/51f39114-68fa-4e8a-b8e1-b64e618d20b9.sh
2026-10-13T14:50:22.9014925Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-13T14:50:23.3648589Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-13T14:50:23.4428606Z Waiting for rollout to finish: 1 old replicas are pending termination...
2026-10-13T14:56:30.0518718Z ##[error]The task has timed out.
2026-10-13T14:56:30.0520043Z ##[section]Finishing: Verificando Status do Deployment



2026-10-13T14:56:30.0540160Z ##[section]Starting: Logs da Aplicação
2026-10-13T14:56:30.0543365Z ==============================================================================
2026-10-13T14:56:30.0543451Z Task         : Bash
2026-10-13T14:56:30.0543493Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-13T14:56:30.0543577Z Version      : 3.227.0
2026-10-13T14:56:30.0543620Z Author       : Microsoft Corporation
2026-10-13T14:56:30.0543669Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-13T14:56:30.0543749Z ==============================================================================
2026-10-13T14:56:30.1703473Z Generating script.
2026-10-13T14:56:30.1714013Z ========================== Starting Command Output ===========================
2026-10-13T14:56:30.1721277Z [command]/bin/bash /opt/ads-agent/_work/_temp/27d53ccb-0b3c-41bd-9d52-9ddf2bfc27d8.sh
2026-10-13T14:56:30.1772749Z + shopt -s expand_aliases
2026-10-13T14:56:30.1772948Z + [[ -n okd4_nprd ]]
2026-10-13T14:56:30.1773121Z + [[ okd4_nprd =~ ocp ]]
2026-10-13T14:56:30.1774084Z + [[ -n okd4_nprd ]]
2026-10-13T14:56:30.1774245Z + [[ okd4_nprd =~ (okd4|openshift) ]]
2026-10-13T14:56:30.1774354Z + app=sinfs-tqs
2026-10-13T14:56:30.1774461Z + oc version
2026-10-13T14:56:30.3292983Z oc v3.11.0+0cbc58b
2026-10-13T14:56:30.3293562Z kubernetes v1.11.0+d4cacc0
2026-10-13T14:56:30.3293869Z features: Basic-Auth GSSAPI Kerberos SPNEGO
2026-10-13T14:56:30.3391408Z 
2026-10-13T14:56:30.3392179Z Server https://api.nprd.caixa:6443
2026-10-13T14:56:30.3392592Z kubernetes v1.25.0-2824+27e744f55d2e99-dirty
2026-10-13T14:56:30.3422896Z ++ oc get pod -l name=sinfs-tqs -n sinfs-tqs -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-10-13T14:56:30.3423069Z ++ tac
2026-10-13T14:56:30.3424147Z ++ grep -v '^$'
2026-10-13T14:56:30.3424624Z ++ head -n1
2026-10-13T14:56:30.6460156Z + last_pod=sinfs-tqs-14-4r89q
2026-10-13T14:56:30.6460422Z + echo 'Logs do POD: sinfs-tqs-14-4r89q'
2026-10-13T14:56:30.6460634Z + oc logs sinfs-tqs-14-4r89q -c sinfs-tqs -n sinfs-tqs
2026-10-13T14:56:30.6460798Z Logs do POD: sinfs-tqs-14-4r89q
2026-10-13T14:56:31.0026427Z Error from server (BadRequest): container "sinfs-tqs" in pod "sinfs-tqs-14-4r89q" is waiting to start: PodInitializing
2026-10-13T14:56:31.0097928Z ##[error]Bash exited with code '1'.
2026-10-13T14:56:31.0110457Z ##[section]Finishing: Logs da Aplicação



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
DB2_URL
jdbc:db2://10.216.80.110:448/RJKDB2DSD0:currentSchema=DESNFS;
EXT
jks
JCICSDIRECT
10.216.80.110
JCICSDIRECT-VAULT
${JCICSDIRECT}
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
SISGR_WS_AUTH
https://webservice.acessoseguro.sso.des.intra.corerj.caixa
SSO_SENHA
********
SSO_SENHA_VAULT
${SSO_SENHA}
SSO_URL
https://login.des.caixa/auth
TGNFSNFDV_SENHA
${TGNFSNFDV_SENHA}
TGNFSNFDV_USER
SNFSDR01
TGSGRS142_SENHA
********
TGSGRS142_SENHA_VAULT
${TGSGRS142_SENHA}
TGSGRS142_USER
JDIRSGRD
TGSGRS143_SENHA
********
TGSGRS143_SENHA_VAULT
${TGSGRS143_SENHA}
TGSGRS143_USER
JDIRSGRD
TGSGRS144_SENHA
${tgnfsnfdv_senha}
TGSGRS144_SENHA_VAULT
********
TGSGRS144_USER
JDIRSGRD
TRUSTSTORE_SENHA
********
TRUSTSTORE_VALUE
/opt/jboss/standalone/configuration/cacerts_sinfs_intra_des_2026.jks
URL_PROXY
proxydes.caixa
_ENV.APPLICATIONINSIGHTS_CONNECTION_STRING
"InstrumentationKey=8148a712-eee7-4c41-95ef-5153b19d0497;IngestionEndpoint=https://southcentralus-3.in.applicationinsights.azure.com/;LiveEndpoint=https://southcentralus.livediagnostics.monitor.azure.com/;ApplicationId=8c7e524c-9be9-44ee-894c-6d034d92a7f5"
_ENV.APPLICATIONINSIGHTS_INSTRUMENTATION_LOGGING_LEVELGGING_LEVEL
INFO
_ENV.APPLICATIONINSIGHTS_ROLE_NAME
SINFS-des
_ENV.APPLICATIONINSIGHTS_SAMPLING_PERCENTAGE
100
_ENV.APPLICATIONINSIGHTS_SELF_DIAGNOSTICS_LEVEL
INFO
xDB2_SENHA
xDB2_USER
SNFSDR01
OKD-4-NPRD (12)
Credenciais para o Cluster OKD4 de NPRD (DES/TQS/HMP)
Scopes: OKD4 EC DES,OKD4 EC TQS,OKD4 EC HMP
OKD-REGISTRY-CENTRALIZADO (7)
Credenciais para o Registry Centralizado - Produtos 4 (OKD)
Scopes: OKD4 EC DES,OKD4 EC TQS,OKD4 EC HMP,OKD4 EC PRD
SINFS-BT-VAULT-DES (1)
WO0000080991099
Scopes: OKD4 EC DES
SINFS-BT-VAULT-SECRET-DES (2)
WO0000080991099
Scopes: OKD4 EC DES
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
SINFS-BT-VAULT-SECRET-TQS (2)
WO0000081007679
Scopes: OKD4 EC TQS
SINFS-prd (24)
Scopes: OKD4 EC PRD
OKD-4-APL (12)
Scopes: OKD4 EC PRD
|Manage variable groups
Select a release pipeline to view its releases

3 pipelines found

Expanded

Row 2

Collapsed

Showing 16 deployments

Showing 16 deployments

Showing 16 deployments

Row 2

EC TQSDeploy release

Expanded

Row 3

Collapsed

Row 2

2 pipelines found

Select a release pipeline to view its releases

2 pipelines found

Row 3

Row 2

Showing filters 1 through 2


