Erro ao tentar gerar release na pipeline do backend:


+ oc start-build sisko-backend --from-dir=/opt/ads-agent/_work/12227/a --follow --wait=true -n build-images-ads -v=5
I1027 10:03:33.347937   90724 repository.go:424] Executing git show -s HEAD --format=%H%n%an%n%ae%n%cn%n%ce%n%B
I1027 10:03:33.349986   90724 repository.go:484] Error executing command: exit status 128
Uploading directory "/opt/ads-agent/_work/12227/a" as binary input for the build ...
I1027 10:03:33.350078   90724 tar.go:217] Adding "/opt/ads-agent/_work/12227/a" to tar ...
I1027 10:03:33.350355   90724 tar.go:312] Adding to tar: /opt/ads-agent/_work/12227/a/jboss-deployments as jboss-deployments
I1027 10:03:33.350843   90724 tar.go:312] Adding to tar: /opt/ads-agent/_work/12227/a/sisko-backend.ear as sisko-backend.ear
............
Uploading finished
I1027 10:04:33.383789   90724 helpers.go:219] Connection error: Post https://api.produtos4.caixa:6443/apis/build.openshift.io/v1/namespaces/build-images-ads/buildconfigs/sisko-backend/instantiatebinary?name=sisko-backend&namespace=build-images-ads: unexpected EOF
F1027 10:04:33.383806   90724 helpers.go:119] Unable to connect to the server: unexpected EOF
##[error]Bash exited with code '255'.
##[warning]RetryHelper encountered task failure, will retry (attempt #: 1 out of 1) after 1000 ms
Generating script.
========================== Starting Command Output ===========================
/bin/bash /opt/ads-agent/_work/_temp/53995bd8-321a-4bd7-92af-3af19a96d76a.sh
+ echo okd4_nprd
+ egrep -q '^(okd4|ocp)'
+ buildconfig=sisko-backend
+ DOTNET_ASSEMBLY=
/opt/ads-agent/_work/_temp/53995bd8-321a-4bd7-92af-3af19a96d76a.sh: line 12:  -4: expressão de substring < 0
+ cd /opt/ads-agent/_work/12227/a
+ FILES=(`find -maxdepth 1 -name "*.runtimeconfig*.json"`)
++ find -maxdepth 1 -name '*.runtimeconfig*.json'


<img width="1760" height="740" alt="image" src="https://github.com/user-attachments/assets/84e9f95d-bd96-401b-bca3-fcb14c2e76b0" />


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
SISKO-backend
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
SISKO

SISKO-backend
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
OKD-NPRD (7)
Credenciais para o Cluster OKD de NPRD2 (DES/TQS/HMP)
Scopes: EC DES,EC TQS,EC HMP,EC PRD
KIND_DEPLOY
deploymentconfig
OKD_API
https://cloudnprd2.caixa
OKD_REGISTRY
docker-registry-default.nprd2.caixa
OKD_TOKEN
********
OKD_URL_SUFFIX
nprd2.caixa
OKD_USER_SERVICE
ads-sa
TIMEOUT_DEPLOY
600
SISKO-BACKEND-DES (30)
Scopes: EC DES,OKD4 EC DES
SISKO-BACKEND-TQS (21)
Scopes: EC TQS,OKD4 EC TQS
OKD-APL (7)
Credenciais para o Cluster OKD de Produção (PRD).
Scopes: EC PRD
SISKO-BACKEND-PRD (30)
Scopes: EC PRD,OKD4 EC PRD
OKD-4-NPRD (12)
Credenciais para o Cluster OKD4 de NPRD (DES/TQS/HMP)
Scopes: OKD4 EC DES,OKD4 EC TQS,OKD4 EC HMP
OKD-REGISTRY-CENTRALIZADO (7)
Credenciais para o Registry Centralizado - Produtos 4 (OKD)
Scopes: OKD4 EC DES,OKD4 EC TQS,OKD4 EC HMP,OKD4 EC PRD
OKD-4-APL (12)
Scopes: OKD4 EC PRD
|Manage variable groups
Collapsed

5 pipelines found

Row 3

Row 5

Row 3

Row 2

Row 3

Row 2

Showing filters 1 through 2

Expanded

Collapsed

2 pipelines found

Row 2

Showing filters 1 through 2

Showing filters 1 through 2

<img width="1847" height="906" alt="image" src="https://github.com/user-attachments/assets/549462a7-d39e-4def-b3d5-e4f8abdef15d" />


pelo que vi ele tentou exeucatl a relese na esteira antiga que ainda tava com okd3. a relesae que ele deve excultar e a backend-okd4.

me ajuda a fechar o chamando.

