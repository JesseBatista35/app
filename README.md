2026-10-28T13:26:08.6485606Z ##[section]Starting: Verificando Status do Deployment
2026-10-28T13:26:08.6488513Z ==============================================================================
2026-10-28T13:26:08.6488599Z Task         : Bash
2026-10-28T13:26:08.6488637Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-28T13:26:08.6488698Z Version      : 3.227.0
2026-10-28T13:26:08.6488757Z Author       : Microsoft Corporation
2026-10-28T13:26:08.6488804Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-28T13:26:08.6488870Z ==============================================================================
2026-10-28T13:26:09.4991161Z Generating script.
2026-10-28T13:26:09.5001254Z ========================== Starting Command Output ===========================
2026-10-28T13:26:09.5008537Z [command]/bin/bash /opt/ads-agent/_work/_temp/65faeca1-ade4-4f2a-b347-109ec8bb3b84.sh
2026-10-28T13:26:09.7154867Z Waiting for rollout to finish: 1 old replicas are pending termination...
2026-10-28T13:32:16.1586552Z ##[error]The task has timed out.
2026-10-28T13:32:16.1587372Z ##[section]Finishing: Verificando Status do Deployment


2026-10-28T13:32:16.1606319Z ##[section]Starting: Logs da Aplicação
2026-10-28T13:32:16.1609473Z ==============================================================================
2026-10-28T13:32:16.1609548Z Task         : Bash
2026-10-28T13:32:16.1609676Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-28T13:32:16.1609736Z Version      : 3.227.0
2026-10-28T13:32:16.1609777Z Author       : Microsoft Corporation
2026-10-28T13:32:16.1609833Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-28T13:32:16.1609902Z ==============================================================================
2026-10-28T13:32:17.0269659Z Generating script.
2026-10-28T13:32:17.0279735Z ========================== Starting Command Output ===========================
2026-10-28T13:32:17.0286890Z [command]/bin/bash /opt/ads-agent/_work/_temp/5d7d581c-f04c-4e75-82c0-9b51d4f75111.sh
2026-10-28T13:32:17.0333456Z + shopt -s expand_aliases
2026-10-28T13:32:17.0333725Z + [[ -n okd4_nprd ]]
2026-10-28T13:32:17.0333902Z + [[ okd4_nprd =~ ocp ]]
2026-10-28T13:32:17.0334083Z + [[ -n okd4_nprd ]]
2026-10-28T13:32:17.0334222Z + [[ okd4_nprd =~ (okd4|openshift) ]]
2026-10-28T13:32:17.0334371Z + app=sigsj-frontend-rc-des
2026-10-28T13:32:17.0334820Z + oc version
2026-10-28T13:32:17.1741270Z oc v3.11.0+0cbc58b
2026-10-28T13:32:17.1741961Z kubernetes v1.11.0+d4cacc0
2026-10-28T13:32:17.1742353Z features: Basic-Auth GSSAPI Kerberos SPNEGO
2026-10-28T13:32:17.1840829Z 
2026-10-28T13:32:17.1841489Z Server https://api.nprd.caixa:6443
2026-10-28T13:32:17.1841959Z kubernetes v1.25.0-2824+27e744f55d2e99-dirty
2026-10-28T13:32:17.1873454Z ++ oc get pod -l name=sigsj-frontend-rc-des -n sigsj-des -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-10-28T13:32:17.1874035Z ++ tac
2026-10-28T13:32:17.1875100Z ++ grep -v '^$'
2026-10-28T13:32:17.1875336Z ++ head -n1
2026-10-28T13:32:18.0757614Z + last_pod=sigsj-frontend-rc-des-28-fxnxf
2026-10-28T13:32:18.0757988Z + echo 'Logs do POD: sigsj-frontend-rc-des-28-fxnxf'
2026-10-28T13:32:18.0758643Z + oc logs sigsj-frontend-rc-des-28-fxnxf -c sigsj-frontend-rc-des -n sigsj-des
2026-10-28T13:32:18.0758881Z Logs do POD: sigsj-frontend-rc-des-28-fxnxf
2026-10-28T13:32:18.4151135Z sed: can't read /opt/app-root/src/main*.js: No such file or directory
2026-10-28T13:32:18.4235404Z ##[section]Finishing: Logs da Aplicação



Predefined variables
Filter by keywords
Release (+1)


AMBIENTE
des
AMBIENTE_BUILD
build-images-ads
CGC_UNIDADE_DES
7390
CGC_UNIDADE_OPS
7259
SISTEMAAMBIENTE
des
SISTEMANOME
sigsj-frontend-rc
SITE
okd4_nprd
TemplateRelease_OKD
openshift/angular-caixa-release
UNIDADE
BR

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
SIGSJ-frontend-rc
/
SIGSJ-frontend-1.0.00.1-SNAPSHOT(1)
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
SIGSJ-frontend-rc

SIGSJ-frontend-1.0.00.1-SNAPSHOT(1)


EC DES

Failed


Pipeline

Tasks

Variables

Logs

Tests
Predefined variables
Usuario-Azure-DevOps (12)
Scopes: Release
SonarQube Variables (1)
Variáveis com dados do SonarQube
Scopes: Release
EGRESS_IP_OKD (81)
WO0000072264656 - Config Portal Infrafácil NO_PROXY
Scopes: Release
MONITORACAO_LOGS (4)
REQ000143540550 - Conforme autorizado na req por FLAVIO ALMEIDA GAGLIARDI, removido as variáveis JAVA_OPTS_MONITORING e URL_APM_SERVER, por entrar em conflitos com releases que utilizam o Application Insights
Scopes: Release
OKD-4-NPRD (12)
Credenciais para o Cluster OKD4 de NPRD (DES/TQS/HMP)
Scopes: Release
OKD-4-APL (12)
Scopes: Release
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
SIGSJ-frontend-rc-des (10)
WO0000081228179
Scopes: EC DES
HTTP_SERVICE_API
https://sigsj-backend-publico-rc-des.apps.nprd.caixa/
_ENV.API_BASE_PATH
https://sigsj-backend-publico-rc-des.apps.nprd.caixa/
_ENV.APPLICATIONINSIGHTS_CONNECTION_STRING
"InstrumentationKey=f6b9b060-c8fc-4702-a924-a3632ca25bb1;IngestionEndpoint=https://brazilsouth-1.in.applicationinsights.azure.com/;LiveEndpoint=https://brazilsouth.livediagnostics.monitor.azure.com/;ApplicationId=3ba7c0c0-1c00-4692-8f9a-61a48d60d078"
_ENV.APPLICATIONINSIGHTS_ROLE_NAME
SIGSJ-FRONTEND-DES
_ENV.CNPJ_ALFA
true
_ENV.CSP_CONNECT_SRC
https://sigsj-backend-publico-rc-des.apps.nprd.caixa/
_ENV.FISERV_PAGAMENTO_URL
https://hml.azulzinhapay.fiserv.com/CNJ/pagaid
_ENV.HTTP_BACKEND_API
https://sigsj-backend-publico-rc-des.apps.nprd.caixa/
_ENV.SIPNC_CACHE_TIMEOUT
300000
_ENV.SSO_URL
https://login.des.caixa/auth/realms/intranet
SIGSJ-frontend-tqs (9)
Scopes: EC TQS
SIGSJ-frontend-hmp (4)
Scopes: EC HMP
SIGSJ-frontend-prd (8)
Scopes: EC PRD
Row 2. Clickable

Row 2. Clickable

Row 3. Clickable

Row 2. Clickable

Row 2. Clickable

Row 2. Clickable

Select a release pipeline to view its releases

5 pipelines found

Row 2

Row 2

68 pipelines found

Select a release pipeline to view its releases

60 pipelines found

Select a release pipeline to view its releases

9 pipelines found

Select a release pipeline to view its releases

9 pipelines found

Row 8

Row 2

Showing filters 1 through 2


