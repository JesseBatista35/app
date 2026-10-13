Solicita-se verificação da montagem do compartilhamento NFS no ambiente de esteira DevOps do sistema SIMCN - BackEnd (DES), no servidor ceadecldlx022.nprd.caixa (10.116.208.42), validando o acesso ao servidor NFS nfsctcnprd.ctc.caixa, export ifs/CADSVISISD4/SERVIDORES/CEPTIBR/UP_SIMCN/, e ao diretório upload/des/simcn.


Solicito a verificação de montagem do NFS em ambiente de estiera DevOps
hostname:ceadecldlx022.nprd.caixa
IP:10.116.208.42
Compartilhamento NFS
Servidor NFS: nfsctcnprd.ctc.caixa
Export: ifs/CADSVISISD4/SERVIDORES/CEPTIBR/UP_SIMCN/
upload/des/simcn

Ip foia lterado, esse é o IP, 25.128.181.35, link dos PODs do SIMCN - DES 
https://console-openshift-console.apps.nprd.caixa/k8s/ns/simcn-des/pods


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
SIMCN-BACKEND-HMP (19)
Grupo de variáveis de SIMCN-BACKEND-HMP
Scopes: EC HMP
OKD-4-APL (12)
Scopes: EC PRD
SIMCN-BACKEND-PRD (19)
Grupo de variáveis de SIMCN-BACKEND-PRD
Scopes: EC PRD
Variable 'NFS_MOUNT_POINT_VM' is already defined

Variable 'NFS_MOUNT_POINT_VM' is already defined

Variable 'NFS_ENDPOINT_ISILON ' is already defined

Variable 'NFS_ENDPOINT_ISILON' is already defined

Variable 'NFS_MOUNT_POINT_ISILON' is already defined

Variable 'NFS_MOUNT_POINT_ISILON' is already defined

293 pipelines found

Select a release pipeline to view its releases

3 pipelines found

Expanded

Collapsed

Row 2

Row 2

Showing filters 1 through 2


2026-10-13T19:38:09.7490592Z ##[debug]Evaluating condition for step: 'Resumo da Release'
2026-10-13T19:38:09.7491085Z ##[debug]Evaluating: succeeded()
2026-10-13T19:38:09.7491254Z ##[debug]Evaluating succeeded:
2026-10-13T19:38:09.7491561Z ##[debug]=> True
2026-10-13T19:38:09.7491742Z ##[debug]Result: True
2026-10-13T19:38:09.7491940Z ##[section]Starting: Resumo da Release
2026-10-13T19:38:09.7495191Z ==============================================================================
2026-10-13T19:38:09.7495299Z Task         : Bash
2026-10-13T19:38:09.7495342Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-13T19:38:09.7495404Z Version      : 3.227.0
2026-10-13T19:38:09.7495481Z Author       : Microsoft Corporation
2026-10-13T19:38:09.7495533Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-13T19:38:09.7495602Z ==============================================================================
2026-10-13T19:38:09.7709596Z ##[debug]Agent environment resources - Disk: / Available 69589.00 MB out of 122356.00 MB, Unable to get memory info, exception: "free" utility is unavailable. Exception: An error occurred trying to start process 'free' with working directory '/opt/ads-agent/bin'. No such file or directory, CPU: Usage 6.89%
2026-10-13T19:38:09.8137365Z ##[debug]Using node path: /opt/ads-agent/externals/node16/bin/node
2026-10-13T19:38:09.8814944Z ##[debug]agent.TempDirectory=/opt/ads-agent/_work/_temp
2026-10-13T19:38:09.8822810Z ##[debug]loading inputs and endpoints
2026-10-13T19:38:09.8830204Z ##[debug]loading INPUT_TARGETTYPE
2026-10-13T19:38:09.8837423Z ##[debug]loading INPUT_FILEPATH
2026-10-13T19:38:09.8838563Z ##[debug]loading INPUT_SCRIPT
2026-10-13T19:38:09.8839181Z ##[debug]loading INPUT_WORKINGDIRECTORY
2026-10-13T19:38:09.8839878Z ##[debug]loading INPUT_FAILONSTDERR
2026-10-13T19:38:09.8840602Z ##[debug]loading ENDPOINT_AUTH_SYSTEMVSSCONNECTION
2026-10-13T19:38:09.8841235Z ##[debug]loading ENDPOINT_AUTH_SCHEME_SYSTEMVSSCONNECTION
2026-10-13T19:38:09.8843184Z ##[debug]loading ENDPOINT_AUTH_PARAMETER_SYSTEMVSSCONNECTION_ACCESSTOKEN
2026-10-13T19:38:09.8848154Z ##[debug]loading SECRET_AZPAT
2026-10-13T19:38:09.8849604Z ##[debug]loading SECRET_PW_ISILON
2026-10-13T19:38:09.8851088Z ##[debug]loading SECRET_FORTIFY_APITOKEN
2026-10-13T19:38:09.8852873Z ##[debug]loading SECRET_PW_ALOCAIP
2026-10-13T19:38:09.8854508Z ##[debug]loading SECRET_ALOCAIP_SENHA
2026-10-13T19:38:09.8855771Z ##[debug]loading SECRET_OKD_TOKEN_REGISTRY
2026-10-13T19:38:09.8856376Z ##[debug]loading SECRET_BT_SECRETS_PATH
2026-10-13T19:38:09.8857041Z ##[debug]loading SECRET_TOKEN_CRQ
2026-10-13T19:38:09.8857666Z ##[debug]loading SECRET_DATASOURCE_ORACLE_PASSWORD
2026-10-13T19:38:09.8858232Z ##[debug]loading SECRET_GRAYLOG_PASSWORD
2026-10-13T19:38:09.8858844Z ##[debug]loading SECRET_PASSWORD_CGC
2026-10-13T19:38:09.8859428Z ##[debug]loading SECRET_FORTIFY_PASS
2026-10-13T19:38:09.8860672Z ##[debug]loading SECRET_OKD_TOKEN_KAFKA
2026-10-13T19:38:09.8861192Z ##[debug]loading SECRET_OKD_4_TOKEN
2026-10-13T19:38:09.8861765Z ##[debug]loaded 22
2026-10-13T19:38:09.8866100Z ##[debug]Agent.ProxyUrl=undefined
2026-10-13T19:38:09.8866955Z ##[debug]Agent.CAInfo=undefined
2026-10-13T19:38:09.8867269Z ##[debug]Agent.ClientCert=undefined
2026-10-13T19:38:09.8867590Z ##[debug]Agent.SkipCertValidation=True
2026-10-13T19:38:09.8880959Z ##[debug]check path : /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-13T19:38:09.8882892Z ##[debug]adding resource file: /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-13T19:38:09.8883209Z ##[debug]system.culture=en-US
2026-10-13T19:38:09.8890935Z ##[debug]failOnStderr=false
2026-10-13T19:38:09.8892511Z ##[debug]workingDirectory=/opt/ads-agent/_work/r118/a
2026-10-13T19:38:09.8892818Z ##[debug]check path : /opt/ads-agent/_work/r118/a
2026-10-13T19:38:09.8893302Z ##[debug]targetType=inline
2026-10-13T19:38:09.8893547Z ##[debug]bashEnvValue=undefined
2026-10-13T19:38:09.8895281Z ##[debug]script=#!/bin/bash

shopt -s extglob

CLUSTER="${AMBIENTE}_${SITE}"

case "${CLUSTER,,}" in
  # OKD 3
  +(des|tqs|hmp)_?(ctc_nprd))
	_okd_url="$(OKD_API)"
	;;
	
  prd_?(ctc_npcn))
    _okd_url="$(OKD_API_APL)"
    ;;

  prd_dtc_npcn)
	_okd_url="$(OKD_API_PRD_DTC)"
  ;;
  
  prd_ctc_canais)
	_okd_url="$(OKD_API_PRD_CANAIS_CTC)"
  ;;
  
  prd_dtc_canais)
	_okd_url="$(OKD_API_PRD_CANAIS_DTC)"
  ;;
  		
  # OKD 4
  +(des|tqs|hmp)_okd4_nprd)
	_okd_url="api.nprd.caixa:6443"
    ;;
	
  prd_okd4_prd)
	_okd_url="$(OKD_4_API_APL)"
    ;;

  # OCP
  +(des|tqs|hmp)_ocp_nprd)
	_okd_url="$(OCP_API)"
    ;;
	
  prd_ocp_prd)
	_okd_url="$(OCP_API_PRD)"
    ;;

  # OPENSHIFT-LOTERIAS-NPRD
  +(des|tqs|hmp)_openshift_nprd_loterias)
  _okd_url="$(OPENSHIFT_LOTERIAS_API_NPRD)"
    ;;

  # OPENSHIFT-LOTERIAS-PRD
  prd_openshift_prd_loterias)
	_okd_url="$(OPENSHIFT_LOTERIAS_API_PRD)"
    ;;

  # OCP LOTERIAS-PRD
  prd_ocp_loterias)
	_okd_url="$(OCP_LOTERIAS_API_PRD)"
    ;;

  # IBMCLOUD
  *_ibmcloud)
    echo "IBMCLOUD $AMBIENTE"
	_okd_url="$(OCP_API_IBMCLOUD)"
	;;
  *)
	echo "Não encontrei o registry para logar"
    exit 1 ;;
esac

if [[ -n "$SITE" && "$SITE" =~ (okd4|ocp|openshift) ]];
then
  app="simcn-backend-des"
else
  app="simcn-backend-des-esteiras"
fi


echo "URL do Projeto no OKD: $_okd_url/console/project/simcn-des/overview"

if [[ -n $(ISTIO_INJECTION) ]]; then
  if [[ $(ISTIO_INJECTION) == "enabled" ]]; then
    namespace='istio-system'
  else
    namespace=simcn-des
  fi
else
  namespace=simcn-des
fi

if [[ -n $(CONTEXTO_JBOSS) ]] ; then
   oc get route -l app="$app" -n $namespace -o jsonpath='{range .items[*].spec}{"APP Publicada na URL: https://"}{.host}'$(CONTEXTO_JBOSS)'{"\n"}{end}'
else
   oc get route -l app="$app" -n $namespace -o jsonpath='{range .items[*].spec}{"APP Publicada na URL: https://"}{.host}{"\n"}{end}'
fi
2026-10-13T19:38:09.8905198Z Generating script.
2026-10-13T19:38:09.8907248Z ##[debug]which 'bash'
2026-10-13T19:38:09.8912779Z ##[debug]found: '/usr/bin/bash'
2026-10-13T19:38:09.8913357Z ##[debug]Agent.Version=3.236.1
2026-10-13T19:38:09.8914170Z ##[debug]agent.tempDirectory=/opt/ads-agent/_work/_temp
2026-10-13T19:38:09.8914779Z ##[debug]check path : /opt/ads-agent/_work/_temp
2026-10-13T19:38:09.8917651Z ========================== Starting Command Output ===========================
2026-10-13T19:38:09.8918992Z ##[debug]which '/usr/bin/bash'
2026-10-13T19:38:09.8920287Z ##[debug]found: '/usr/bin/bash'
2026-10-13T19:38:09.8921044Z ##[debug]/usr/bin/bash arg: /opt/ads-agent/_work/_temp/48e67ff1-a85b-416a-8a16-54479266dff2.sh
2026-10-13T19:38:09.8924019Z ##[debug]exec tool: /usr/bin/bash
2026-10-13T19:38:09.8924601Z ##[debug]arguments:
2026-10-13T19:38:09.8925094Z ##[debug]   /opt/ads-agent/_work/_temp/48e67ff1-a85b-416a-8a16-54479266dff2.sh
2026-10-13T19:38:09.8927503Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/48e67ff1-a85b-416a-8a16-54479266dff2.sh
2026-10-13T19:38:09.8984115Z URL do Projeto no OKD: api.nprd.caixa:6443/console/project/simcn-des/overview
2026-10-13T19:38:09.8988931Z /opt/ads-agent/_work/_temp/48e67ff1-a85b-416a-8a16-54479266dff2.sh: line 82: ISTIO_INJECTION: command not found
2026-10-13T19:38:09.8992442Z /opt/ads-agent/_work/_temp/48e67ff1-a85b-416a-8a16-54479266dff2.sh: line 92: CONTEXTO_JBOSS: command not found
2026-10-13T19:38:09.9649298Z APP Publicada na URL: https://simcn-backend-des.apps.nprd.caixa
2026-10-13T19:38:09.9693361Z ##[debug]Exit code 0 received from tool '/usr/bin/bash'
2026-10-13T19:38:09.9696479Z ##[debug]STDIO streams have closed for tool '/usr/bin/bash'
2026-10-13T19:38:09.9701533Z ##[debug]task result: Succeeded
2026-10-13T19:38:09.9702775Z ##[debug]Processed: ##vso[task.complete result=Succeeded;done=true;]
2026-10-13T19:38:09.9738183Z ##[section]Finishing: Resumo da Release


