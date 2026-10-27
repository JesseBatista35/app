-sh-4.2$  oc get pod -n sispi-des -l name=sispi-med-gestao-des --show-labels
NAME                            READY     STATUS    RESTARTS   AGE       LABELS
sispi-med-gestao-des-22-ckdkt   2/2       Running   0          21h       CGC_DES=7390,CGC_OPS=7259,app=sispi-med-gestao-des,deployment=sispi-med-gestao-des-22,deploymentconfig=sispi-med-gestao-des,maistra-version=2.5.12,maistra.io/expose-route=true,name=sispi-med-gestao-des,security.istio.io/tlsMode=istio,service.istio.io/canonical-name=sispi-med-gestao-des,service.istio.io/canonical-revision=latest
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods -n sispi-des -L maistra.io/expose-route | grep -v Completed
NAME                                                      READY     STATUS             RESTARTS         AGE       EXPOSE-ROUTE
sispi-agendar-pix-internos-des-8-tgzh4                    2/2       Running            0                60d
sispi-agrupador-frontend-des-149-hckpn                    3/3       Running            2 (4d1h ago)     4d1h
sispi-api-consulta-chave-parceiros-des-76-jq4rs           2/2       Running            811 (146m ago)   72d
sispi-api-consulta-situacao-transacao-des-57-gwqq8        2/2       Running            0                90d
sispi-api-dados-pix-interno-des-5-dkzcl                   2/2       Running            79 (13d ago)     112d
sispi-api-extrato-pix-des-243-6bvgt                       2/2       Running            0                3d12h
sispi-api-fabrica-ids-des-37-9h57s                        2/2       Running            0                107m
sispi-api-fabrica-ids-des-37-cv5d8                        2/2       Running            0                68d
sispi-api-fabrica-ids-des-37-dwxgk                        2/2       Running            0                112m
sispi-api-fabrica-ids-des-37-hz845                        2/2       Running            0                102m
sispi-api-fabrica-ids-des-37-kpb8f                        2/2       Running            0                115m
sispi-api-fabrica-ids-des-37-pgtnz                        2/2       Running            0                104m
sispi-api-fabrica-ids-des-37-phkfc                        2/2       Running            0                135m
sispi-api-fabrica-ids-des-37-q2dtc                        2/2       Running            0                121m
sispi-api-fabrica-ids-des-37-q552h                        2/2       Running            0                112m
sispi-api-fabrica-ids-des-37-qbzbk                        2/2       Running            0                104m
sispi-api-fabrica-ids-des-37-sjr6x                        2/2       Running            0                4d16h
sispi-api-fabrica-ids-des-37-v4fmj                        2/2       Running            0                107m
sispi-api-fabrica-ids-des-37-zllkm                        2/2       Running            0                102m
sispi-api-feriados-des-3-zwxxv                            2/2       Running            9 (25d ago)      129d
sispi-api-gestao-documento-des-10-f45nr                   2/2       Running            0                3h2m
sispi-api-notificacao-des-487-kfsfk                       2/2       Running            14 (68m ago)     25h
sispi-api-open-finance-des-39-tfn6g                       2/2       Running            0                18d
sispi-api-participantes-pix-des-53-b2d75                  2/2       Running            0                25d
sispi-api-pix-envio-interno-des-143-r7ndx                 2/2       Running            17 (4d ago)      53d
sispi-api-proxy-sso-des-86-bwfn9                          2/2       Running            0                129d
sispi-api-rco-des-139-wfrmm                               2/2       Running            0                24d
sispi-api-tarifacao-des-52-pk9gl                          2/2       Running            0                7d3h
sispi-api-valida-pix-des-42-7dqzq                         2/2       Running            0                129d
sispi-atendimento-bff-des-117-66lvb                       2/2       Running            0                7d1h
sispi-atendimento-bff-des-117-pw7np                       2/2       Running            0                7d1h
sispi-atendimento-bff-des-117-t859s                       2/2       Running            0                7d1h
sispi-atendimento-bff-des-117-wpdlb                       2/2       Running            0                7d1h
sispi-atendimento-frontend-des-141-m8sjt                  3/3       Running            2 (22h ago)      22h
sispi-backend-antifraude-des-90-trj2k                     2/2       Running            0                4d3h
sispi-backend-batch-contabil-des-500-g7ptd                2/2       Running            6 (33h ago)      34d
sispi-backend-batch-dimp-des-35-gpjvs                     2/2       Running            0                91d
sispi-backend-batch-efinanceira-des-66-z6c87              2/2       Running            0                129d
sispi-backend-recebimento-des-395-h4rnk                   2/2       Running            0                4d2h
sispi-backend-recebimento-secundario-des-454-8gxnb        2/2       Running            0                4d1h
sispi-backend-retorno-des-498-nqcc2                       2/2       Running            0                24h
sispi-backend-retorno-secundario-des-351-xvkh4            2/2       Running            0                4d2h
sispi-batch-busca-pendencia-des-118-5cwr9                 2/2       Running            669 (151m ago)   5d1h
sispi-batch-extrato-relatorio-des-83-wcdwt                2/2       Running            0                17d
sispi-batch-qrcode-certificados-des-47-khc4p              2/2       Running            2 (62d ago)      129d
sispi-batch-relatorio-operacional-des-36-r4fsj            2/2       Running            0                91d
sispi-batch-resolve-pendencia-des-107-t8qwb               2/2       Running            1 (33h ago)      5d1h
sispi-batch-tratamento-bloqueio-antifraude-des-12-7d7qc   2/2       Running            0                129d
sispi-container-backend-des-1036-gscmg                    2/2       Running            3 (3d18h ago)    3d18h
sispi-container-dict-des-879-b7k2z                        2/2       Running            0                122m
sispi-container-frontend-des-635-g2cs7                    3/3       Running            2 (2d15h ago)    2d15h
sispi-dict-api-des-31-h2z9b                               2/2       Running            0                123m
sispi-dict-api-med-des-160-fktrr                          2/2       Running            0                3d20h
sispi-dict-balde-chaves-des-33-kf8j5                      2/2       Running            0                7d22h
sispi-dict-batch-polling-des-737-7tmcm                    1/2       CrashLoopBackOff   19 (3m40s ago)   70m
sispi-dict-consulta-chaves-des-38-r8ftd                   2/2       Running            0                4h7m
sispi-dict-consulta-estatisticas-des-59-f2h4x             2/2       Running            0                4d
sispi-dict-gestao-chaves-des-55-95pmc                     2/2       Running            0                52d
sispi-dict-lista-restrita-des-76-d85td                    2/2       Running            383 (147m ago)   3d21h
sispi-dict-polling-des-115-gmcmr                          2/2       Running            0                3d20h
sispi-dict-processar-antifraude-des-23-szpwt              2/2       Running            0                4h9m
sispi-dict-validacao-posse-des-10-pkg72                   2/2       Running            0                3d22h
sispi-dict-verifica-chaves-batch-des-38-g5t6l             2/2       Running            0                126d
sispi-dict-verifica-chaves-des-75-v95cx                   2/2       Running            0                69d
sispi-disparador-eventos-des-1-cc5pl                      2/2       Running            0                21d
sispi-envio-notif-intra-bacen-des-126-2d7xg               2/2       Running            15 (24h ago)     26d
sispi-med-auditoria-des-30-x5zjs                          2/2       Running            0                82d
sispi-med-gestao-des-22-ckdkt                             2/2       Running            0                21h       true
sispi-parametrizacoes-pix-des-43-j9kzn                    2/2       Running            0                129d
sispi-pix-api-onboarding-des-93-6krnb                     2/2       Running            2 (35d ago)      129d
sispi-pix-gestao-des-642-p9pb7                            2/2       Running            0                69m
sispi-pix-gestao-dict-des-305-72r7g                       2/2       Running            0                24h
sispi-pix-med-des-394-bpttm                               2/2       Running            12 (3h27m ago)   3d19h
sispi-pocrosa-orchestrator-des-25-k47mf                   2/2       Running            2 (5d16h ago)    20d
sispi-processar-ans-iga-des-71-5k6qc                      2/2       Running            2 (24h ago)      4d21h
sispi-processar-fila-secundario-des-44-4lbxh              1/2       Running            2 (7d13h ago)    129d
sispi-processar-health-check-des-37-fgf7f                 2/2       Running            39 (3d4h ago)    129d
sispi-processar-health-check-des-37-zqt6z                 2/2       Running            23 (4d3h ago)    126d
sispi-processar-mensagem-contabil-des-112-tnxf5           2/2       Running            0                3d22h
sispi-processar-notif-intra-bacen-des-88-pffwm            2/2       Running            9 (24h ago)      26d
sispi-processar-pix-automatico-des-269-2ddzs              2/2       Running            1 (33h ago)      4d3h
sispi-processar-pix-externo-des-58-tc5vx                  2/2       Running            1 (24h ago)      28h
sispi-processar-pix-internos-des-621-g987m                2/2       Running            0                25m
sispi-processar-pix-internos-primario-des-243-deploy      0/1       Error              0                168m
sispi-processar-pix-internos-primario-des-244-fqvjs       2/2       Running            0                125m
sispi-processar-recebimento-pix-auto-des-59-ftmjp         2/2       Running            70 (24h ago)     129d
sispi-processar-resolve-pendencia-des-247-n6ssg           2/2       Running            0                5d1h
sispi-processar-solicitacao-historico-des-139-gmn4r       2/2       Running            0                4d3h
sispi-processar-solicitacao-notificacao-des-160-6ndpn     2/2       Running            75 (146m ago)    7h16m
sispi-processar-solicitacao-push-des-69-ccqt7             2/2       Running            0                20d
sispi-processar-tempo-envio-intra-bacen-des-19-9sblj      2/2       Running            1 (101d ago)     129d
sispi-processar-tratamento-padrao-siatr-des-166-mq5mk     2/2       Running            0                97d
sispi-qrcode-api-consultas-des-453-qd9c7                  2/2       Running            1 (16h ago)      6d5h
sispi-qrcode-api-credenciamento-des-443-cmq9r             2/2       Running            0                13d
sispi-qrcode-api-dinamico-des-384-4vhh9                   2/2       Running            13 (4d ago)      6d4h
sispi-qrcode-api-dinamico-lote-des-178-s72gc              2/2       Running            8 (21m ago)      5d2h
sispi-qrcode-api-estatico-des-74-w5jqt                    2/2       Running            0                129d
sispi-qrcode-api-externo-des-215-wkc56                    2/2       Running            2 (2d4h ago)     55d
sispi-qrcode-api-prelocation-des-111-csgf6                2/2       Running            0                129d
sispi-qrcode-api-validador-des-312-mthvm                  2/2       Running            0                153m
sispi-qrcode-api-webhook-des-93-dpk5n                     2/2       Running            608 (47m ago)    98d
sispi-qrcode-clientid-exclusivo-des-10-mwlln              2/2       Running            0                83d
sispi-qrcode-envia-notificacao-des-17-q77xt               2/2       Running            0                83d
sispi-qrcode-frontend-des-305-r4tmj                       3/3       Running            2 (3h45m ago)    3h45m
sispi-qualidade-roteador-des-33-xjc4f                     2/2       Running            0                129d
sispi-reenvio-notificacao-des-74-gbf89                    1/2       Running            0                129d
sispi-resolve-pendencia-notif-intra-bacen-des-68-5ftll    2/2       Running            0                91d
-sh-4.2$
-sh-4.2$
-sh-4.2$


Skip to main content
projetos
/
Caixa
/
Pipelines
/
Releases
/
SISPI-med-gestao
Search








All pipelines

SISPI

SISPI-med-gestao
Predefined variables
Filter by keywords
Scope


AMBIENTE
des
AMBIENTE
tqs
AMBIENTE
hmp
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
hmp
SISTEMAAMBIENTE
prd
SISTEMANOME
sispiI-med-gestao
SITE
ocp_nprd
SITE
ocp_prd
TemplateRelease_OKD
openshift/quarkus-caixa-release
UNIDADE
BR
URL_APM_SERVER
http://apm-server-devops.apps.produtos4.caixa
Row 2

Row 2

Row 2

Row 10

Row 2

Row 2

Row 2

No pipelines match your search

Select a release pipeline to view its releases

No pipelines match your search

Select a release pipeline to view its releases

271 pipelines found

Select a release pipeline to view its releases

151 pipelines found

Select a release pipeline to view its releases

4 pipelines found

Row 3

Row 2

Row 2

Showing filters 1 through 2

Cannot edit in read-only editor


Skip to main content
projetos
/
Caixa
/
Pipelines
/
Releases
/
SISPI-med-gestao
Search








All pipelines

SISPI

SISPI-med-gestao
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
OCP-NPRD (8)
Credenciais para o Cluster OCP de NPRD (DES/TQS/HMP)
Scopes: EC DES,EC TQS,EC HMP
ISTIO_INJECTION
enabled
KIND_DEPLOY
deploymentconfig
OCP_API
api.pixnprd4.caixa:6443
OCP_REGISTRY
default-route-openshift-image-registry.apps.pixnprd4.caixa
OCP_TOKEN
********
OCP_URL_SUFFIX
apps.pixnprd4.caixa
OCP_USER_SERVICE
ads
TIMEOUT_DEPLOY
300
SISPI-MED-GESTAO-DES (17)
Grupo de variáveis de SISPI-MED-GESTAO
Scopes: EC DES
VAULT_LOCATION
/usr/src/app/secrets_files/SISPI_DES
_ENV.JAVA_OPTIONS_APPEND
"-Djavax.net.ssl.trustStore=/deployments/caixa-truststore-acteste-nprd.jks"
_ENV.PIX_FRAMEWORK_TOKEN_CLIENT_ID
cli-ser-spi
_ENV.PIX_FRAMEWORK_TOKEN_SECRET_ID
'${sispi_secret_intranet}'
_ENV.PIX_FRAMEWORK_TOKEN_URL
https://login.des.caixa/auth/realms/intranet/protocol/openid-connect/token
_ENV.PIX_FRAMEWORK_VALIDACAO_TOKEN_SSO_EMISSOR
"https://login.des.caixa/auth/realms/intranet"
_ENV.PIX_FRAMEWORK_VALIDACAO_TOKEN_SSO_URL
"https://sispi-api-proxy-sso-des.apps.pixnprd4.caixa/auth/realms/intranet;https://login.des.caixa/auth/realms/intranet"
_ENV.PIX_FRAMEWORK_VALIDACAO_TOKEN_VALIDACAO_GLOBAL
true
_ENV.QUARKUS_DATASOURCE_JDBC_URL
"jdbc:oracle:thin:@cnpexdadvm01-scan4.extra.caixa.gov.br:1521/CDBD08NGPDB017"
_ENV.QUARKUS_DATASOURCE_PASSWORD
'${sspibd03_oracle}'
_ENV.QUARKUS_DATASOURCE_USERNAME
SSPIBD03
_ENV.SIMPI_MED_URL
https://simpi-med-des.apps.pixnprd4.caixa
_ENV.SISPI_API_KEY
'${sispi_api_key}'
_ENV.SISPI_LOGIN_CAIXA_INTRANET_SECRET
'${sispi_secret_intranet}'
_ENV.SISPI_LOGIN_CAIXA_INTRANET_URL
"https://login.des.caixa/auth/realms/intranet"
_ENV.SISPI_LOGIN_PROXY_INTRANET_URL
https://sispi-api-proxy-sso-des.apps.pixnprd4.caixa/auth/realms/intranet
_SECRET.SMALLRYE.CONFIG.SOURCE.FILE.LOCATIONS
#{VAULT_LOCATION}#
SISPI-MED-GESTAO-BT-VAULT-DES (1)
Scopes: EC DES
SISPI-BT-VAULT-SECRET-DES (2)
Scopes: EC DES
SISPI-MED-GESTAO-TQS (1)
Grupo de variáveis de SISPI-MED-GESTAO
Scopes: EC TQS
SISPI-MED-GESTAO-HMP (1)
Grupo de variáveis de SISPI-MED-GESTAO
Scopes: EC HMP
OCP-PRD (16)
Credenciais para o Cluster OCP de PRD
Scopes: EC PRD
SISPI-MED-GESTAO-PRD (1)
Grupo de variáveis de SISPI-MED-GESTAO
Scopes: EC PRD
|Manage variable groups
Row 2

Row 2

Row 2

Row 10

Row 2

Row 2

Row 2

No pipelines match your search

Select a release pipeline to view its releases

No pipelines match your search

Select a release pipeline to view its releases

271 pipelines found

Select a release pipeline to view its releases

151 pipelines found

Select a release pipeline to view its releases

4 pipelines found

Row 3

Row 2

Row 2

Showing filters 1 through 2

Cannot edit in read-only editor
