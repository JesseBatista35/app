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
SIICO-rj-api
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
SIICO

SIICO-rj-api
Predefined variables
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
OKD-PRODUTOS (8)
Credenciais para o Cluster OKD4 de PRODUTOS
Scopes: Release
CI_NAME
7366CLU-OKD4-PRODUTOS
OKD_API_PRODUTOS
api.produtos4.caixa:6443
OKD_REGISTRY_PRODUTOS
default-route-openshift-image-registry.apps.produtos4.caixa
OKD_TOKEN_PRODUTOS
********
OKD_URL_SUFFIX_PRODUTOS
api.produtos4.caixa:6443
OKD_USER_SERVICE_PRODUTOS
ads-sa
TOKEN_CRQ
********
URL_CRQ
https://infradevops-novoportal-backend-prd.apps.produtos4.caixa/api.php?acao=devopsCaixacriarMudancaPadrao
SonarQube Variables (1)
Variáveis com dados do SonarQube
Scopes: Release
SONAR_URL
http://sonar.produtos.caixa
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
TERRAFORM-ESTEIRA-COMMON (6)
WO0000079295714 - add variável INFRAFACIL
Scopes: Release
INFRAFACIL
infradevops-novoportal-backend-prd.apps.produtos4.caixa
TERRAFORM_ESX_PASSWORD
********
TERRAFORM_ESX_USERNAME
s736660
TF_HTTPS_NO_PROXY
10.122.144.168,10.122.144.195,10.122.144.130,10.221.144.17,*.caixa,*.intra.caixa.gov.br,cadsvgerap030-1.intra.caixa.gov.br,cadsvgerap027-1.intra.caixa.gov.br,cadsvgerap028-1.intra.caixa.gov.br,cert-api.access.redhat.com,cadsvgerap107-1.intra.caixa.gov.br
TF_HTTPS_PROXY
http://proxynuvem.caixa:80
arm_access_key
********
ANSIBLE_JBOSS_VM_VERSION_3 (11)
WO0000072264656 - Config Portal Infrafácil NO_PROXY cadsvgerap027-1.intra.caixa.gov.br, 10.122.144.168
Scopes: Release
ANSIBLE_CONFIG
$(HOME_ADS_AGENT)/$(DIR_ANSIBLE)/ansible.cfg
ANSIBLE_INVENTORY_ANY_UNPARSED_IS_FAILED
True
ANSIBLE_VAULT
********
DIR_ANSIBLE
esteira-jboss-vm-v2
HOME_ADS_AGENT
$(System.DefaultWorkingDirectory)
NO_PROXY
10.122.144.168,10.122.144.195,10.122.144.130,10.221.144.17,devops.caixa,cadsvgerap004-1.intra.caixa.gov.br,cadsvgerap028-1.intra.caixa.gov.br,infradevops-novoportal-backend-prd.apps.produtos4.caixa,infradevops-ads-api-prd.apps.produtos4.caixa,infradevops-db-api-prd.apps.produtos4.caixa,cadsvgerap027-1.intra.caixa.gov.br
REPO_ESTEIRA_JBOSS_VM
https://devops.caixa/projetos/Infraestrutura/_git/esteira-jboss-vm-v2
REPO_ESTEIRA_JBOSS_VM_BRANCH
master
REPO_ESTEIRA_TERRAFORM
https://devops.caixa/projetos/Infraestrutura/_git/esteira-vm-release-terraform
REPO_ESTEIRA_TERRAFORM_BRANCH
main
TOKEN_INFRAFACIL_MUDANCA
********
sample-java-des (13)
WO0000081293906 - SISME
Scopes: Release
JVM_HEAP_MAX
4096m
JVM_HEAP_MIN
4096m
JVM_METASPACE_MAX
512m
JVM_METASPACE_MIN
512M
PASSWORD_TRUSTSTORE
changeit
PATH_DESTINO
/sample
PATH_NFS
/ifs/CADSVISISD4/SERVIDORES/CESTI/SAMPLE_DES
SERVER_NFS
nfsctcnprd.ctc.caixa
SIZE_VOLUME
50Gi
SSO_URL_INTERNET
https://login.des.caixa.gov.br
SSO_URL_INTRANET
https://login.des.caixa
TESTE_TRUST
caixa-truststore-acteste-nprd.jks
VERSAO
$(Build.BuildNumber)
TERRAFORM-ESTEIRA-NPRD (17)
Variáveis do terraform para automação de ambientes
Scopes: EC DES,EC TQS,EC HMP
TERRAFORM_CLUSTER
CTC_NPRDXF2488HV7_NPRD
TERRAFORM_DATACENTER
NPRD
TERRAFORM_DATASTORE
CTCHWNPRDC011_0259
TERRAFORM_ESX_NETWORK
tn-NPRD+NPRD_AUTO_DES_BSB-ap+VL3676-ep+10.116.192.0
TERRAFORM_ESX_NETWORK_BCK
tn-NPRD|NPRD_BKP-ap|VL3697-ep
TERRAFORM_ESX_NETWORK_BCK_1
tn-BACKUP|BACKUP-NPRD-ap|BACKUP-NPRD-ep
TERRAFORM_ESX_PASSWORD
********
TERRAFORM_ESX_USERNAME
s736660
TERRAFORM_ESX_VCENTER_SERVER
10.122.144.195
TERRAFORM_NET_ADAPTER_TYPE
vmxnet3
TERRAFORM_VM_DNS
["10.116.193.77", "10.116.193.78"]
TERRAFORM_VM_DOMAIN
agil.nprd.caixa.gov.br
TERRAFORM_VM_IPNETMASK
19
TERRAFORM_VM_IPNETMASK_BCK
19
TERRAFORM_VM_IPNETMASK_BCK_1
16
TERRAFORM_VSPHERE_FOLDER
/vm
TERRAFORM_VSPHERE_POOL
/Resources/RP_TERRAFORM_NPRD
SIICO-RJ_API-DES (20)
Grupo de variáveis de SIICO-RJ_API-DES

Scopes: EC DES
AMBIENTE
des
APPLICATIONINSIGHTS_CONNECTION_STRING
InstrumentationKey=1db83fd9-8b2f-4a25-89d8-8cf25fa9321a;IngestionEndpoint=https://brazilsouth-1.in.applicationinsights.azure.com/;LiveEndpoint=https://brazilsouth.livediagnostics.monitor.azure.com/
APPLICATIONINSIGHTS_INSTRUMENTATION_LOGGING_LEVEL
INFO
APPLICATIONINSIGHTS_PROXY
http://proxydes.caixa:80
APPLICATIONINSIGHTS_ROLE_NAME
SIICO-RJAPI-DES
APPLICATIONINSIGHTS_SAMPLING_PERCENTAGE
10
APPLICATIONINSIGHTS_SELF_DIAGNOSTICS_LEVEL
INFO
DB2_CONNECTION_URL
jdbc:db2://10.216.80.110:448/RJKDB2DSD0
DB2_PASSWORD
${VAULT::SICODR01::SIICO::1}
DB2_USER
SICODR01
LOG_LEVEL
ERROR
URL_PROXY
proxydes.caixa
VALIDA_TOKEN
https://login.des.caixa/auth/realms/intranet/protocol/openid-connect/certs
VALIDA_TOKEN_INTERNET
https://logindes.caixa.gov.br/auth/realms/internet/protocol/openid-connect/certs
VAULT_ITERATION_COUNT
44
VAULT_KEYSTORE_ALIAS
SecurityKey
VAULT_KEYSTORE_PASSWORD
********
VAULT_NAME
vaultcaixa
VAULT_SALT
87654321
http_context_default
cadastro
SIICO-RJ_API-TQS (20)
Grupo de variáveis de SIICO-RJ_API-TQS
Scopes: EC TQS
SIICO-RJ_API-HMP (15)
Grupo de variáveis de SIICO-RJ_API-HMP
Scopes: EC HMP
TERRAFORM-ESTEIRA-PRD-CTC-NPCN (17)
Variáveis do terraform para automação de ambientes TERRAFORM_VSPHERE_POOL - RP_ESTEIRAS_AGEIS_NPCN_CTC_V7 13/03/2025
Scopes: EC PRD CTC
SIICO-RJ_API-PRD (17)
TAS000047101774
Scopes: EC PRD CTC,EC PRD DTC
TERRAFORM-ESTEIRA-PRD-DTC-PCN (15)
Variáveis do terraform para automação de ambientes
Scopes: EC PRD DTC
|Manage variable groups
Row 2

Row 2

Row 2

Row 2

Row 4

Row 2

Select a release pipeline to view its releases

12 pipelines found

Row 5

Showing filters 1 through 2

Row 3

Showing filters 1 through 2

No pipelines match your search

Select a release pipeline to view its releases

80 pipelines found

Select a release pipeline to view its releases

3 pipelines found

Row 4

Row 2

Showing filters 1 through 2

