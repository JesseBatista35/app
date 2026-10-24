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
SICOW-conres-okd
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
sicow

SICOW-conres-okd
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
OKD-4-NPRD (12)
Credenciais para o Cluster OKD4 de NPRD (DES/TQS/HMP)
Scopes: EC DES,EC TQS,EC HMP
SICOW-CONRES-OKD-DES (54)
Grupo de variáveis de SICOW-CONRES-OKD-DES

Scopes: EC DES
JKS_FILE
caixa-truststore-acteste-nprd-sicow.jks
JVM_HEAP_MAX
1024m
JVM_HEAP_MIN
1024m
JVM_METASPACE_MAX
512m
JVM_METASPACE_MIN
96m
JVM_PROXY_HOST
proxydes.caixa
JVM_PROXY_PORT
80
MAIL_EXPRESSO_HOST
smtptest.correiolivre.caixa
MAIL_EXPRESSO_PORT
25
PASTA_NFS
/sicow
PATH_DESTINO
/sicow
PATH_NFS
/ifs/CADSVISISD4/SERVIDORES/CESTI/SICOW
SERVER_NFS
nfsctcnprd.ctc.caixa
SICOWCONRES_WAR
https://sicow-conres-okd-des.apps.nprd.caixa/sicow-conres
SICOWIMP_WAR
https://sicow-imp-okd-des.apps.nprd.caixa/sicow-imp-okd
SICOWLG_WAR
https://sicow-lg-okd-des.apps.nprd.caixa/sicowlg
SICOWMTE_WAR
https://sicow-mte-okd-des.apps.nprd.caixa/sicow-mte-okd
SICOWNIA_WAR
https://sicow-nia-okd-des.apps.nprd.caixa/sicow-nia-okd
SICOWPENHOR_WAR
https://sicow-penhor-okd-des.apps.nprd.caixa/sicowpenhor
SICOWPORTALURL
https://sicow-portal-okd-des.apps.nprd.caixa/sicow-portal-okd/pages/home.cef
SICOWSEG_WAR
https://sicow-seg-okd-des.apps.nprd.caixa/sicowseg
SICOW_DS
jdbc:postgresql://10.116.92.41:5116/cowdb001?autoReconnect=true
SICOW_DS_MAX_POLL_SIZE
10
SICOW_DS_MIN_POLL_SIZE
5
SICOW_DS_PASSWORD
${VAULT::SICOW::SCOWDB01::1}
SICOW_DS_USER
scowdb01
SICOW_SICLI_WS_APIKEY
l7415d496745d74a079735c47ef0f3b4be
SICOW_SICLI_WS_SISTEMA
SICOW
SICOW_SICLI_WS_TOKEN_CLIENT_ID
cli-ser-cow
SICOW_SICLI_WS_TOKEN_CLIENT_SECRET
57670b90-1378-49b7-94c9-c3d3c7d545bf
SICOW_SICLI_WS_TOKEN_GRANT_TYPE
client_credentials
SICOW_SICLI_WS_TOKEN_URL
https://login.des.caixa/auth/realms/intranet/protocol/openid-connect/token
SICOW_SICLI_WS_URL
https://api.des.caixa:8443/cadastro/v1/clientes
SICOW_SIISO_WS_API_KEY
l7415d496745d74a079735c47ef0f3b4be
SICOW_SIISO_WS_CLIENT_URL
https://api.des.caixa:8443/cadastro-receita/v4/pessoas-fisicas
SICOW_SIISO_WS_TOKEN_CLIENT_GRANT_TYPE
client_credentials
SICOW_SIISO_WS_TOKEN_CLIENT_ID
cli-ser-cow
SICOW_SIISO_WS_TOKEN_CLIENT_SECRET
57670b90-1378-49b7-94c9-c3d3c7d545bf
SICOW_SIISO_WS_TOKEN_URL
https://login.des.caixa/auth/realms/intranet/protocol/openid-connect/token
SIICO_DS
jdbc:postgresql://sctdedadlx0026.df.caixa:51491/posprd01?autoReconnect=true
SIICO_DS_MAX_POLL_SIZE
25
SIICO_DS_MIN_POLL_SIZE
5
SIICO_DS_PASSWORD
${VAULT::SICOW::SCOWDB01::1}
SIICO_DS_USER
scowdb01
SIUSR_END_POINT
http://hmp.autentica.proinfo.caixa/siusr-service/SiusrService/SiusrWS
SIZE_VOLUME
50Gi
URL_PROXY
proxydes.caixa
USER_TIMEZONE
America/Buenos_Aires
VAULT_ITERATION_COUNT
44
VAULT_KEYSTORE_ALIAS
SecurityKey
VAULT_KEYSTORE_FILE
vault-sicow-des.keystore
VAULT_KEYSTORE_PASSWORD
MASK-lHQotGsUSmQ5YQRzdtNLD361rwn0c0oJ
VAULT_SALT
87654321
_ENV.APPLICATIONINSIGHTS_ROLE_NAME
SICOW-CONRES-OKD-DES
ADAPTER_VARIABLES - SIACM Cartões (7)
Variáveis disponíveis para todas os projetos do tipo ADAPTER.
Scopes: EC DES
SICOW-APPLICATIONINSIGHTS-DES (5)
Grupo de variáveis de APPLICATIONINSIGHTS-DES
Scopes: EC DES
SICOW-BT-VAULT-SECRET-DES (3)
WO0000081288532
Scopes: EC DES
BT_CLIENT_ID
BT_CLIENT_SECRET
SCOWDB01
********
SICOW-CONRES-OKD-TQS (1)
Grupo de variáveis de SICOW-CONRES-OKD-TQS
Scopes: EC TQS
SICOW-PORTAL-OKD-TQS (268)
Grupo de variáveis de SICOW-PORTAL-OKD-TQS
Scopes: EC TQS
SICOW-CONRES-OKD-HMP (1)
Grupo de variáveis de SICOW-CONRES-OKD-HMP
Scopes: EC HMP
OKD-4-APL (12)
Scopes: EC PRD
SICOW-CONRES-OKD-PRD (1)
Grupo de variáveis de SICOW-CONRES-OKD-PRD
Scopes: EC PRD
|Manage variable groups
52 pipelines found

Select a release pipeline to view its releases

5 pipelines found

Row 5

Showing filters 1 through 2




feito. sobre o ajuste no repositroi vamos cirar a branch Cesti-teste e faze ro ajuste beleza?





Skip to main content
Azure DevOps
projetos
/
Caixa
/
Repos
/
Files
/

SICOW-conres-okd
Search


Caixa

Overview

Boards

Repos
Files
Commits
Pushes
Branches
Tags
Pull requests

Pipelines

Test Plans

Artifacts
Project settings
SICOW-conres-okd

src
main
java
br
resources
META-INF
messages.properties
webapp

META-INF
pages
resources
templates
WEB-INF
access_denied.xhtml
error.xhtml
expired_session.xhtml
index.html
login.xhtml
login2.xhtml
login3.xhtml
loginSicowConres.xhtml
page_not_found.xhtml
test
.gitignore
cli-offline.sh

develop

/
Type to find a file or folder...
Files
Set up build

Clone

Contents
History

src
14 de out.
f6d68fcc
Application Insights c161288
.gitignore
8 de set.
9af12541
Versão c161288
cli-offline.sh
13 de mar.
a12799e5
Added cli-offline.sh Higor Antonio Delsoto
jboss-deployments
14 de out.
f6d68fcc
Application Insights c161288
jboss-modules
16 de out.
3ba393b5
Updated jboss-modules Evandro Alves de Souza
pom.xml
14 de out.
f6d68fcc
Application Insights c161288
README.md
19 de mar. de 2024
45559b40
Added README.md Rafael Augusto Soares
Introduction
TODO: Give a short introduction of your project. Let this section explain the objectives or the motivation behind this project.

Getting Started
TODO: Guide users through getting your code up and running on their own system. In this section you can talk about:

Installation process
Software dependencies
Latest releases
API references
Build and Test
TODO: Describe and show how to build your code and run the tests.

Contribute
TODO: Explain how other users and developers can contribute to make your code better.

If you want to learn more about creating good readme files then refer the following guidelines . You can also seek inspiration from the below readme files:

ASP.NET Core 
Visual Studio Code 
Chakra Core 



