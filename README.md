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
SIHDG-angular18
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
SIHDG

SIHDG-angular18
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
SIHDG-ANGULAR18-DES (7)
Grupo de variáveis de SIHDG-ANGULAR18-DES
Scopes: EC DES
HTTP_SERVICE_API
https://sihdg-jboss8-des.apps.nprd.caixa
INIT
Criado via api
_ENV.AMBIENTE
"Desenvolvimento"
_ENV.API
://sihdg-jboss8-des.apps.nprd.caixa:
_ENV.JAVA_OPTIONS_APPEND
"-Djavax.net.ssl.trustStore=/deployments/ac_caixav4.jks"
_ENV.URL_SSO
https://login.des.caixa/auth
_ENV.VERSION
$(Build.BuildNumber)
SIHDG-ANGULAR18-TQS (7)
Grupo de variáveis de SIHDG-ANGULAR18-TQS

Scopes: EC TQS
HTTP_SERVICE_API
https://sihdg-jboss8-tqs.apps.nprd.caixa
INIT
Criado via api
_ENV.AMBIENTE
"TQS"
_ENV.API
://sihdg-jboss8-tqs.apps.nprd.caixa:
_ENV.JAVA_OPTIONS_APPEND
"-Djavax.net.ssl.trustStore=/deployments/ac_caixav4.jks"
_ENV.URL_SSO
https://login.tqs.caixa/auth
_ENV.VERSION
$(Build.BuildNumber)
SIHDG-ANGULAR18-HMP (1)
Grupo de variáveis de SIHDG-ANGULAR18-HMP
Scopes: EC HMP
SIHDG-ANGULAR18-PRD (1)
Grupo de variáveis de SIHDG-ANGULAR18-PRD
Scopes: EC PRD
|Manage variable groups
Row 2

EC TQSDeploy release

15 pipelines found

Select a release pipeline to view its releases

5 pipelines found

Row 2

Showing filters 1 through 2




<img width="1842" height="890" alt="image" src="https://github.com/user-attachments/assets/1f3168d8-dc43-4a46-8f2b-d37247156136" />


o certificado ta auqi mais na ta ajustatrr no javaapend
<img width="1635" height="858" alt="image" src="https://github.com/user-attachments/assets/3f7ed1f6-fcf3-4a8e-ade2-8adbfb559810" />


ocjop uq e e so ajsutar a task que vai dar vcerto né

e no sihadg-jboss8 qual variavel colocar para a relesae ja deixar tudo certo la



Skip to main content
Azure DevOps
projetos
/
Caixa
/
Pipelines
/
Library
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

Library

SIHDG-JBOSS8-TQS

Variable group
Properties
Variable group name
SIHDG-JBOSS8-TQS
Description



Variables
_ENV.JAVA_OPTS_APPEND
"-Djavax.net.ssl.trustStore=/opt/server/standalone/configuration/caixa-truststore-acteste-nprd.jks -Djava.security.properties=/opt/server/bin/java.security.override -Djava.security.disableSystemPropertiesFile=true"
DATASOURCE_CONNECTION_URL
jdbc:sqlserver://10.116.29.201:31153;DatabaseName=HDGDB001;encrypt=true;trustServerCertificate=true
DATASOURCE_PASSWORD
********
DATASOURCE_USER_NAME
SHDGTB01
JKS_FILE
caixa-truststore-acteste-nprd.jks
JVM_HEAP_MAX
2048m
JVM_HEAP_MIN
1024m
JVM_METASPACE_MAX
512m
JVM_METASPACE_MIN
256m
NFS_PATH
/fs_sihdg_tqs
NFS_SERVER
hypernprd12.ad.caixa
NFS_STORAGE_SIZE_VOLUME
20Gi
PASSWORD_TRUSTSTORE
changeit
PATH_DESTINO
/sihdg_tqs
PATH_DESTINO_PWC
/sihdg_powercenter
PATH_NFS
/fs_sihdg_tqs
PATH_NFS_PWC
/fs_sihdg_powercenter
SERVER_NFS
hypernprd12.ad.caixa
SERVER_NFS_PWC
hypernprd12.ad.caixa
SIHDG-classificacao.informacao
#INTERNO.CONFIDENCIAL
SIHDG-DB_INTERNO
true
SIHDG-derivativo.avaliacao.remetente
GEGAP
SIHDG-mail.avaliacao.derivativo
GEOMI@MAIL.CAIXA
SIHDG-mail.endereco
gitecbr05@caixa.gov.br
SIHDG-mail.ordem.alteracao
GEOMI@MAIL.CAIXA
SIHDG-mail.ordem.cancelamento
GEOMI@MAIL.CAIXA
SIHDG-mail.ordem.execucao
GEANF@MAIL.CAIXA
SIHDG-mail.ordem.insercao
GEOMI@MAIL.CAIXA
SIHDG-mail.ordem.invalidacao
GEANF@MAIL.CAIXA
SIHDG-mail.registro.efetividade
GEANF@MAIL.CAIXA,GEMOC@MAIL.CAIXA
SIHDG-mail.smtp.host
smtptest.correiolivre.caixa
SIHDG-mail.smtp.port
25
SIHDG-ordem.alteracao.remetente
GEGAP
SIHDG-ordem.cancelamento.remetente
GEGAP
SIHDG-ordem.execucao.remetente
GETES
SIHDG-ordem.insercao.remetente
GEGAP
SIHDG-ordem.invalidacao.remetente
GESEN
SIHDG-path.arquivo.sinaf
/sihdg_tqs/Arquivos_SINAF/
SIHDG-SEC_TEMPO_VIDA_TOKEN
5
SIHDG-SEC_URL_SERV_AUTH
https://login.tqs.caixa/auth
SIZE_VOLUME
20Gi
SIZE_VOLUME_PWC
50Gi
SSO_REALM
intranet
SSO_REQUIRED
none
SSO_RESOURCE
cli-web-hdg
SSO_URL
https://login.tqs.caixa/auth
Variable ' SIHDG-SEC_URL_SERV_AUTH' is already defined

Variable 'SIHDG-SEC_URL_SERV_AUTH' is already defined
