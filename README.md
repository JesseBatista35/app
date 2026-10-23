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
SIIFX-caixinhas-batch
/
SIIFX-caixinhas-batch-37
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
SIIFX-caixinhas-batch

SIIFX-caixinhas-batch-37
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
Compartilhamentos (4)
Scopes: Release
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
sample-java-des (13)
WO0000081293906 - SISME
Scopes: EC DES,EC TQS
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
SIIFX-CAIXINHAS-BATCH-DES (37)
Grupo de variáveis de SIIFX-CAIXINHAS-BATCH-DES
Scopes: EC DES
BATCH_HOME
/opt/batch/deploy
BATCH_LOG_DIR
/logs/caixinhas
BATCH_PROFILE
des
DB_ALIAS
alias_sifxds01
DB_IDLE
3
DB_PASS
********
DB_POOL_MAX
32
DB_POOL_MIN
8
DB_SCHEMA
IFX
DB_URL
jdbc:oracle:thin:@(DESCRIPTION=(ADDRESS_LIST=(ADDRESS=(PROTOCOL=TCP)(HOST=cnpexdadvm01-scan8.extra.caixa.gov.br)(PORT=1521)))(CONNECT_DATA=(SERVICE_NAME=orad01bc)))
DB_USER
SIFXDS01
JAVA_OPTIONS_APPEND
-Djavax.net.ssl.trustStore=/opt/batch/securefiles/caixa-truststore-acteste-nprd.jks -Djavax.net.ssl.trustStorePassword=changeit
JVM_HEAP_MAX
2048m
JVM_HEAP_MIN
1024m
JVM_METASPACE_MAX
512m
JVM_METASPACE_MIN
256m
KEYSTORE
/opt/jboss/standalone/configuration/dskeystore_des_siifx.jceks
LOG_LEVEL
INFO
NFS_ENDPOINT_ISILON
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH
NFS_ENDPOINT_ISILON_2
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX
NFS_MOUNT_POINT_ISILON
/SIIFX
NFS_MOUNT_POINT_ISILON_2
/SIIFX_B2B
NSGD_DESFAZ_CREDITO
https://api.des.caixa:8443/conta-deposito/lancamentos-financeiros/v1/desfazimento/credito
NSGD_DESFAZ_DEBITO
https://api.des.caixa:8443/conta-deposito/lancamentos-financeiros/v1/desfazimento/debito
NSGD_KEY
********
ORA_DRIVE
oracle.jdbc.driver.OracleDriver
PARALLEL
8
SERVER_LOG_LEVEL
INFO
SIIFX_DATAGRID_HOST
caddeapllx2221.agil.nprd.caixa.gov.br
SIIFX_DATAGRID_PASS
********
SIIFX_DATAGRID_PORT
11222
SIIFX_DATAGRID_USER
sifxds04
TASK_CORE_POOL_SIZE
16
TASK_MAX_POOL_SIZE
32
TASK_QUEUE_CAPACITY
32
TOKEN_HOST
https://login.des.caixa/auth/realms/intranet/protocol/openid-connect/token
TOKEN_KEY
********
SIIFX-CAIXINHAS-BATCH-TQS (33)
Grupo de variáveis de SIIFX-CAIXINHAS-BATCH-TQS
Scopes: EC TQS
DB_ALIAS
alias_sifxst01
DB_IDLE
3
DB_PASS
********
DB_POOL_MAX
32
DB_POOL_MIN
8
DB_URL
jdbc:oracle:thin:@(DESCRIPTION=(ADDRESS_LIST=(ADDRESS=(PROTOCOL=TCP)(HOST=cnpexdadvm01-scan11.extra.caixa.gov.br)(PORT=1521)))(CONNECT_DATA=(SERVICE_NAME=orat01bc)))
DB_USER
SIFXTS01
JAVA_OPTIONS_APPEND
-Djavax.net.ssl.trustStore=/opt/batch/securefiles/caixa-truststore-acteste-nprd.jks -Djavax.net.ssl.trustStorePassword=changeit
JVM_HEAP_MAX
2048m
JVM_HEAP_MIN
1024m
JVM_METASPACE_MAX
512m
JVM_METASPACE_MIN
256m
KEYSTORE
/opt/jboss/standalone/configuration/dskeystore_tqs_siifx.jceks
LOG_LEVEL
DEBUG
NFS_ENDPOINT_ISILON
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH
NFS_ENDPOINT_ISILON_2
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX
NFS_MOUNT_POINT_ISILON
/SIIFX
NFS_MOUNT_POINT_ISILON_2
/SIIFX_B2B
NSGD_DESFAZ_CREDITO
https://api.des.caixa:8443/conta-deposito/lancamentos-financeiros/v1/desfazimento/credito
NSGD_DESFAZ_DEBITO
https://api.des.caixa:8443/conta-deposito/lancamentos-financeiros/v1/desfazimento/debito
NSGD_KEY
********
ORA_DRIVE
oracle.jdbc.driver.OracleDriver
PARALLEL
8
SERVER_LOG_LEVEL
INFO
SIIFX_DATAGRID_HOST
caddeapllx2221.agil.nprd.caixa.gov.br
SIIFX_DATAGRID_PASS
********
SIIFX_DATAGRID_PORT
11222
SIIFX_DATAGRID_USER
sifxds04
TASK_CORE_POOL_SIZE
8
TASK_MAX_POOL_SIZE
16
TASK_QUEUE_CAPACITY
16
TOKEN_HOST
https://login.des.caixa/auth/realms/intranet/protocol/openid-connect/token
TOKEN_KEY
********
sample-java-hmp (13)
WO0000081430821
Scopes: EC HMP
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
/ifs/CADSVISISD4/SERVIDORES/CESTI/SAMPLE_HMP
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
SIIFX-CAIXINHAS-BATCH-HMP (1)
Grupo de variáveis de SIIFX-CAIXINHAS-BATCH-HMP
Scopes: EC HMP
INIT
Criado via api
TERRAFORM-ESTEIRA-PRD-CTC-NPCN (17)
Variáveis do terraform para automação de ambientes TERRAFORM_VSPHERE_POOL - RP_ESTEIRAS_AGEIS_NPCN_CTC_V7 13/03/2025
Scopes: EC PRD CTC
TERRAFORM_CLUSTER
CTC_PRDXF2488HV7_NPCN
TERRAFORM_DATACENTER
DC_NPCN_CTC
TERRAFORM_DATASTORE
CTCHW3005_00034
TERRAFORM_ESX_NETWORK
tn-NPCN-CTC|APLICACAO|VL1187-ep
TERRAFORM_ESX_NETWORK_BCK
tn-BACKUP|BACKUP-CTC-ap|VL0020-ep
TERRAFORM_ESX_NETWORK_BCK_1
tn-BACKUP|BACKUP-PROD-ap|BACKUP-PROD-ep
TERRAFORM_ESX_PASSWORD
********
TERRAFORM_ESX_USERNAME
s736660
TERRAFORM_ESX_VCENTER_SERVER
cadsvgerap027-1.intra.caixa.gov.br
TERRAFORM_NET_ADAPTER_TYPE
vmxnet3
TERRAFORM_VM_DNS
["10.121.128.203", "10.121.128.204"]
TERRAFORM_VM_DOMAIN
agil.caixa.gov.br
TERRAFORM_VM_IPNETMASK
19
TERRAFORM_VM_IPNETMASK_BCK
20
TERRAFORM_VM_IPNETMASK_BCK_1
21
TERRAFORM_VSPHERE_FOLDER
/vm
TERRAFORM_VSPHERE_POOL
/Resources/RP_ESTEIRAS_AGEIS_NPCN_CTC_V7
sample-java-prd (10)
Scopes: EC PRD CTC,EC PRD DTC
JVM_HEAP_MAX
6144m
JVM_HEAP_MIN
4096m
JVM_METASPACE_MAX
512m
JVM_METASPACE_MIN
256m
MAX_POOL_EJB
100
PASSWORD_TRUSTSTORE
********
SSO_URL_INTERNET
https://login.caixa.gov.br
SSO_URL_INTRANET
https://login.prd.caixa
VERSAO
$(Build.BuildNumber)
_ENV.FOO
covid
SIIFX-CAIXINHAS-BATCH-PRD (1)
Grupo de variáveis de SIIFX-CAIXINHAS-BATCH-PRD
Scopes: EC PRD CTC,EC PRD DTC
INIT
Criado via api
TERRAFORM-ESTEIRA-PRD-DTC-PCN (15)
Variáveis do terraform para automação de ambientes
Scopes: EC PRD DTC
TERRAFORM_CLUSTER
DTC_PRDHW2488HV5_CANAIS
TERRAFORM_DATACENTER
DTC
TERRAFORM_DATASTORE
DTCHW3008_0000
TERRAFORM_ESX_NETWORK
tn-PCN-DTC|INTERNET-ap|VL2162-ep
TERRAFORM_ESX_NETWORK_BCK
PortGroup_Backup_10.223.32.0_VLAN62_Private
TERRAFORM_ESX_PASSWORD
********
TERRAFORM_ESX_USERNAME
s736660
TERRAFORM_ESX_VCENTER_SERVER
10.221.144.17
TERRAFORM_NET_ADAPTER_TYPE
vmxnet3
TERRAFORM_VM_DNS
["10.222.144.12", "10.222.144.13"]
TERRAFORM_VM_DOMAIN
agil.caixa.gov.br
TERRAFORM_VM_IPNETMASK
23
TERRAFORM_VM_IPNETMASK_BCK
20
TERRAFORM_VSPHERE_FOLDER
/vm/
TERRAFORM_VSPHERE_POOL
/Resources/RP_ESTEIRAS_CANAIS_DTC
Collapsed

Row 5. Clickable

Row 2. Clickable

Row 2. Clickable

Showing 31 filtered items.

Showing 25 filtered items.

Row 2. Clickable

Row 2. Clickable

Collapsed

Expanded

212 pipelines found

Select a release pipeline to view its releases

19 pipelines found

Select a release pipeline to view its releases

16 pipelines found

Select a release pipeline to view its releases

2 pipelines found

Row 3

Row 2

Showing filters 1 through 2

