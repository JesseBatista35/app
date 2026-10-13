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
SIEXC-web-aplicacao-des

Variable group
Properties
Variable group name
SIEXC-web-aplicacao-des
Description



Variables
DB_HOST
10.116.92.41
DB_HOST_ORA
jdbc:oracle:thin:@cnpexdadvm01-scan4.extra.caixa.gov.br:1521/ORAD71NG
DB_NAME
excdb002
DB_PASS
${VAULT::SIEXC-web-aplicacao-des::DB_PASS::1}
DB_PASS_ORA
${VAULT::SIEXC-web-aplicacao-des::DB_PASS_ORA::1}
DB_PORT
5104
DB_USER
${VAULT::SIEXC-web-aplicacao-des::DB_USER::1}
DB_USER_ORA
${VAULT::SIEXC-web-aplicacao-des::DB_USER_ORA::1}
JVM_HEAP_MAX
2548m
JVM_HEAP_MIN
1024m
JVM_METASPACE_MAX
1024m
JVM_METASPACE_MIN
256m
MQ_CONNECTION_FACTORY_POOL_CHANNEL
BRD1.SVRCONN
MQ_CONNECTION_FACTORY_POOL_HOSTNAME
10.192.228.145
MQ_CONNECTION_FACTORY_POOL_PORT
1414
MQ_CONNECTION_FACTORY_POOL_QUEUE_MANAGER
BRD1
MQ_CONNECTION_FACTORY_POOL_USERNAME
SEXCS01D
MQ_NSGD_CHANNEL
SIEXC.SRVCONN
MQ_NSGD_HOSTNAME
10.192.224.63
MQ_NSGD_PASSWORD
undefined
MQ_NSGD_PORT
1420
MQ_NSGD_QUEUE_MANAGER
QSQA
MQ_NSGD_USERNAME
SEXCMQQ1
MQ_SICLI_CHANNEL
SIEXC.SVRCONN
MQ_SICLI_HOSTNAME
10.192.224.66
MQ_SICLI_PORT
1420
MQ_SICLI_QUEUE_MANAGER
QSDA
MQ_SICLI_USERNAME
SEXCS01D
MQ_SIINT_CHANNEL
SIEXC.SVRCONN
MQ_SIINT_HOSTNAME
10.192.224.66
MQ_SIINT_PORT
1420
MQ_SIINT_QUEUE_MANAGER
QSDA
MQ_SIINT_RESPOSTA_CHANNEL
SIEXC.SVRCONN
MQ_SIINT_RESPOSTA_HOSTNAME
10.192.224.66
MQ_SIINT_RESPOSTA_PORT
1420
MQ_SIINT_RESPOSTA_QUEUE_MANAGER
QSDA
MQ_SIINT_RESPOSTA_USERNAME
SEXCS01D
MQ_SIINT_USERNAME
SEXCS01D
MQ_SIRIC_CHANNEL
SIEXC.SVRCONN
MQ_SIRIC_HOSTNAME
10.192.224.66
MQ_SIRIC_PORT
1420
MQ_SIRIC_QUEUE_MANAGER
QSDA
MQ_SIRIC_USERNAME
SEXCS01D
NFS_ENDPOINT_ISILON
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
NFS_ENDPOINT_ISILON_2
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF
NFS_ENDPOINT_ISILON_3
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC
NFS_ENDPOINT_ISILON_4
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
NFS_ENDPOINT_ISILON_5
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
NFS_ENDPOINT_ISILON_6
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
NFS_ENDPOINT_ISILON_7
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
NFS_ENDPOINT_ISILON_8
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
NFS_ENDPOINT_ISILON_9
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC
NFS_ENDPOINT_VM
192.168.227.59:/export/sicql_bovespa
NFS_ENDPOINT_VM_2
192.168.227.59:/export/sicql_bovespa
NFS_ENDPOINT_VM_3
192.168.227.59:/export/sicql_bovespa
NFS_ENDPOINT_VM_4
192.168.227.59:/export/sicql_bovespa
NFS_ENDPOINT_VM_5
192.168.227.59:/export/sicql_bovespa
NFS_MOUNT_POINT_ISILON
/siexc_incoming
NFS_MOUNT_POINT_ISILON_2
/integracoes/SIISF
NFS_MOUNT_POINT_ISILON_3
/SIAPC
NFS_MOUNT_POINT_ISILON_4
/SIGPL
NFS_MOUNT_POINT_ISILON_5
/legado
NFS_MOUNT_POINT_ISILON_6
/eFinanceira_ctc/siexc
NFS_MOUNT_POINT_ISILON_7
/eFinanceira/siexc/entrada
NFS_MOUNT_POINT_ISILON_8
/suporte
NFS_MOUNT_POINT_ISILON_9
/siexc
NFS_MOUNT_POINT_VM
/SIEXC_SWIFT
NFS_MOUNT_POINT_VM_2
/SIEXC
NFS_MOUNT_POINT_VM_3
/producao/SWIFT
NFS_MOUNT_POINT_VM_4
/producao
NFS_MOUNT_POINT_VM_5
/SIEXC_SWIFT
SISTEMA_AMBIENTE
des
URL_GESTOR
https://siexc-web-aplicacao.esteiras.des.caixa/swifter-webapp
USER_ID
${VAULT::SIEXC-web-aplicacao-des::USER-ID::1}
USER_SECRET
${VAULT::SIEXC-web-aplicacao-des::SECRET::1}



2026-10-13T20:58:38.0248426Z ##[debug]Evaluating condition for step: 'Deploy Config no JBOSS'
2026-10-13T20:58:38.0248839Z ##[debug]Evaluating: succeeded()
2026-10-13T20:58:38.0248991Z ##[debug]Evaluating succeeded:
2026-10-13T20:58:38.0249266Z ##[debug]=> True
2026-10-13T20:58:38.0249450Z ##[debug]Result: True
2026-10-13T20:58:38.0249626Z ##[section]Starting: Deploy Config no JBOSS
2026-10-13T20:58:38.0252567Z ==============================================================================
2026-10-13T20:58:38.0252644Z Task         : Bash
2026-10-13T20:58:38.0252684Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-13T20:58:38.0252754Z Version      : 3.227.0
2026-10-13T20:58:38.0252796Z Author       : Microsoft Corporation
2026-10-13T20:58:38.0252845Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-13T20:58:38.0252924Z ==============================================================================
2026-10-13T20:58:38.8869254Z ##[debug]Using node path: /opt/ads-agent/externals/node16/bin/node
2026-10-13T20:58:38.9529225Z ##[debug]agent.TempDirectory=/opt/ads-agent/_work/_temp
2026-10-13T20:58:38.9536785Z ##[debug]loading inputs and endpoints
2026-10-13T20:58:38.9540497Z ##[debug]loading INPUT_TARGETTYPE
2026-10-13T20:58:38.9547920Z ##[debug]loading INPUT_FILEPATH
2026-10-13T20:58:38.9548946Z ##[debug]loading INPUT_SCRIPT
2026-10-13T20:58:38.9549791Z ##[debug]loading INPUT_WORKINGDIRECTORY
2026-10-13T20:58:38.9550315Z ##[debug]loading INPUT_FAILONSTDERR
2026-10-13T20:58:38.9551826Z ##[debug]loading ENDPOINT_AUTH_SYSTEMVSSCONNECTION
2026-10-13T20:58:38.9552665Z ##[debug]loading ENDPOINT_AUTH_SCHEME_SYSTEMVSSCONNECTION
2026-10-13T20:58:38.9554003Z ##[debug]loading ENDPOINT_AUTH_PARAMETER_SYSTEMVSSCONNECTION_ACCESSTOKEN
2026-10-13T20:58:38.9559882Z ##[debug]loading SECRET_BT_SECRETS_PATH
2026-10-13T20:58:38.9561590Z ##[debug]loading SECRET_TERRAFORM_ESX_PASSWORD
2026-10-13T20:58:38.9563142Z ##[debug]loading SECRET_PW_ALOCAIP
2026-10-13T20:58:38.9564691Z ##[debug]loading SECRET_OKD_TOKEN_PRODUTOS
2026-10-13T20:58:38.9567105Z ##[debug]loading SECRET_PW_ISILON
2026-10-13T20:58:38.9568865Z ##[debug]loading SECRET_TOKEN_CRQ
2026-10-13T20:58:38.9569713Z ##[debug]loading SECRET_ARM_ACCESS_KEY
2026-10-13T20:58:38.9570403Z ##[debug]loading SECRET_FORTIFY_PASS
2026-10-13T20:58:38.9570914Z ##[debug]loading SECRET_TOKEN_INFRAFACIL_MUDANCA
2026-10-13T20:58:38.9571446Z ##[debug]loading SECRET_AZPAT
2026-10-13T20:58:38.9572042Z ##[debug]loading SECRET_OKD_TOKEN_KAFKA
2026-10-13T20:58:38.9573383Z ##[debug]loading SECRET_FORTIFY_APITOKEN
2026-10-13T20:58:38.9574261Z ##[debug]loading SECRET_ANSIBLE_VAULT
2026-10-13T20:58:38.9574778Z ##[debug]loading SECRET_GRAYLOG_PASSWORD
2026-10-13T20:58:38.9576173Z ##[debug]loaded 22
2026-10-13T20:58:38.9581159Z ##[debug]Agent.ProxyUrl=undefined
2026-10-13T20:58:38.9581593Z ##[debug]Agent.CAInfo=undefined
2026-10-13T20:58:38.9581814Z ##[debug]Agent.ClientCert=undefined
2026-10-13T20:58:38.9582039Z ##[debug]Agent.SkipCertValidation=True
2026-10-13T20:58:38.9596651Z ##[debug]check path : /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-13T20:58:38.9599520Z ##[debug]adding resource file: /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-13T20:58:38.9599798Z ##[debug]system.culture=en-US
2026-10-13T20:58:38.9609328Z ##[debug]failOnStderr=false
2026-10-13T20:58:38.9610377Z ##[debug]workingDirectory=/opt/ads-agent/_work/r17882/a
2026-10-13T20:58:38.9610691Z ##[debug]check path : /opt/ads-agent/_work/r17882/a
2026-10-13T20:58:38.9611052Z ##[debug]targetType=inline
2026-10-13T20:58:38.9611908Z ##[debug]bashEnvValue=undefined
2026-10-13T20:58:38.9612901Z ##[debug]script=REPO=$(echo _SIEXC-web-aplicacao | sed 's/_//')
ansible-playbook /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/site.yml --tags git_conf -e sistema_ambiente=des -e sistema_nome=siexc-web-aplicacao -e default_working_directory_tfs=/opt/ads-agent/_work/r17882/a -e build_repository_name_tfs=$REPO -e quantidade_vm=$(quantidade_vm) -e package_path=/opt/ads-agent/_work/r17882/a/binario/`basename http://binario.caixa:8081/repository/thirdparty/br/com/caixa/siexc/siexc-web-aplicacao/1.1.14/siexc-web-aplicacao-1.1.14.ear` -e use_wmq=$(USE_WMQ) -e jks_file=/opt/ads-agent/_work/_temp/caixa-truststore-acteste-nprd.jks -e site=ctc_nprd -e url_deploy="`echo "http://binario.caixa:8081/repository/thirdparty/br/com/caixa/siexc/siexc-web-aplicacao/1.1.14/siexc-web-aplicacao-1.1.14.ear" | tr -d "\'"`"
2026-10-13T20:58:38.9621344Z Generating script.
2026-10-13T20:58:38.9623230Z ##[debug]which 'bash'
2026-10-13T20:58:38.9629072Z ##[debug]found: '/bin/bash'
2026-10-13T20:58:38.9629542Z ##[debug]Agent.Version=3.225.2
2026-10-13T20:58:38.9629775Z ##[debug]agent.tempDirectory=/opt/ads-agent/_work/_temp
2026-10-13T20:58:38.9630017Z ##[debug]check path : /opt/ads-agent/_work/_temp
2026-10-13T20:58:38.9632128Z ========================== Starting Command Output ===========================
2026-10-13T20:58:38.9633227Z ##[debug]which '/bin/bash'
2026-10-13T20:58:38.9634038Z ##[debug]found: '/bin/bash'
2026-10-13T20:58:38.9634653Z ##[debug]/bin/bash arg: /opt/ads-agent/_work/_temp/25e38d2c-8d04-42e2-8c7e-32a034380028.sh
2026-10-13T20:58:38.9637095Z ##[debug]exec tool: /bin/bash
2026-10-13T20:58:38.9637322Z ##[debug]arguments:
2026-10-13T20:58:38.9637562Z ##[debug]   /opt/ads-agent/_work/_temp/25e38d2c-8d04-42e2-8c7e-32a034380028.sh
2026-10-13T20:58:38.9639243Z [command]/bin/bash /opt/ads-agent/_work/_temp/25e38d2c-8d04-42e2-8c7e-32a034380028.sh
2026-10-13T20:58:38.9712178Z /opt/ads-agent/_work/_temp/25e38d2c-8d04-42e2-8c7e-32a034380028.sh: line 2: quantidade_vm: comando não encontrado
2026-10-13T20:58:38.9722560Z /opt/ads-agent/_work/_temp/25e38d2c-8d04-42e2-8c7e-32a034380028.sh: line 2: USE_WMQ: comando não encontrado
2026-10-13T20:58:41.0565712Z 
2026-10-13T20:58:41.0566276Z PLAY [local] *******************************************************************
2026-10-13T20:58:41.0846128Z 
2026-10-13T20:58:41.0846538Z PLAY [Configurando o DNS] ******************************************************
2026-10-13T20:58:41.2634354Z 
2026-10-13T20:58:41.2634851Z PLAY [local] *******************************************************************
2026-10-13T20:58:41.2669034Z 
2026-10-13T20:58:41.2669650Z PLAY [Verificando serviços] ****************************************************
2026-10-13T20:58:41.2748379Z 
2026-10-13T20:58:41.2748695Z PLAY [Configuração LDAP] *******************************************************
2026-10-13T20:58:41.2780580Z [WARNING]: Found variable using reserved name: when
2026-10-13T20:58:41.2785727Z 
2026-10-13T20:58:41.2785953Z PLAY [jboss] *******************************************************************
2026-10-13T20:58:41.2868654Z 
2026-10-13T20:58:41.2869179Z PLAY [Stack Jboss] *************************************************************
2026-10-13T20:58:41.3090302Z Tuesday 13 October 2026  17:58:41 -0300 (0:00:00.312)       0:00:00.312 ******* 
2026-10-13T20:58:41.7962538Z 
2026-10-13T20:58:41.7963600Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-10-13T20:58:41.7964161Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-13T20:58:41.7964703Z caddeapllx2193.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-13T20:58:41.7965151Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-13T20:58:41.7966238Z releases. A future Ansible release will default to using the discovered 
2026-10-13T20:58:41.7966559Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-13T20:58:41.7966729Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-13T20:58:41.7966899Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-13T20:58:41.7967035Z setting deprecation_warnings=False in ansible.cfg.
2026-10-13T20:58:41.7967168Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:58:41.7987426Z 
2026-10-13T20:58:41.7987689Z PLAY [jboss] *******************************************************************
2026-10-13T20:58:41.8051496Z Tuesday 13 October 2026  17:58:41 -0300 (0:00:00.496)       0:00:00.808 ******* 
2026-10-13T20:58:42.1143435Z 
2026-10-13T20:58:42.1144143Z TASK [Verifica se o arquivo nfs_config.json existe] ****************************
2026-10-13T20:58:42.1144500Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:58:42.1166669Z Tuesday 13 October 2026  17:58:42 -0300 (0:00:00.311)       0:00:01.119 ******* 
2026-10-13T20:58:42.1622339Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/tasks/get_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T20:58:42.1658715Z Tuesday 13 October 2026  17:58:42 -0300 (0:00:00.049)       0:00:01.169 ******* 
2026-10-13T20:58:42.2216125Z 
2026-10-13T20:58:42.2216681Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-13T20:58:42.2216836Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:58:42.2253938Z Tuesday 13 October 2026  17:58:42 -0300 (0:00:00.059)       0:00:01.228 ******* 
2026-10-13T20:58:42.6236157Z 
2026-10-13T20:58:42.6237069Z TASK [nfs : Coletar variáveis de ambiente] *************************************
2026-10-13T20:58:42.6237436Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:58:42.6264311Z Tuesday 13 October 2026  17:58:42 -0300 (0:00:00.401)       0:00:01.629 ******* 
2026-10-13T20:58:42.6818478Z 
2026-10-13T20:58:42.6819514Z TASK [nfs : Exibir resultado em JSON] ******************************************
2026-10-13T20:58:42.6822164Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:58:42.6822307Z     "nfs_vars_json": {
2026-10-13T20:58:42.6822421Z         "changed": false, 
2026-10-13T20:58:42.6822710Z         "cmd": "cat /opt/ads-agent/_work/r17882/a/nfs_config.json", 
2026-10-13T20:58:42.6822906Z         "delta": "0:00:00.003256", 
2026-10-13T20:58:42.6823087Z         "end": "2026-10-13 17:58:42.608918", 
2026-10-13T20:58:42.6823204Z         "failed": false, 
2026-10-13T20:58:42.6823306Z         "rc": 0, 
2026-10-13T20:58:42.6823505Z         "start": "2026-10-13 17:58:42.605662", 
2026-10-13T20:58:42.6823622Z         "stderr": "", 
2026-10-13T20:58:42.6823720Z         "stderr_lines": [], 
2026-10-13T20:58:42.6824637Z         "stdout": "[{\"NFS_ENDPOINT_VM\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM\": \"/SIEXC_SWIFT\"},{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON\": \"/siexc_incoming\"},{\"NFS_ENDPOINT_ISILON_3\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC\",\"NFS_MOUNT_POINT_ISILON_3\": \"/SIAPC\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF\",\"NFS_MOUNT_POINT_ISILON_2\": \"/integracoes/SIISF\"},{\"NFS_ENDPOINT_ISILON_5\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_5\": \"/legado\"},{\"NFS_ENDPOINT_ISILON_4\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_4\": \"/SIGPL\"},{\"NFS_ENDPOINT_ISILON_7\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_7\": \"/eFinanceira/siexc/entrada\"},{\"NFS_ENDPOINT_ISILON_6\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_6\": \"/eFinanceira_ctc/siexc\"},{\"NFS_ENDPOINT_VM_2\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_2\": \"/SIEXC\"},{\"NFS_ENDPOINT_ISILON_9\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_9\": \"/siexc\"},{\"NFS_ENDPOINT_VM_3\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_3\": \"/producao/SWIFT\"},{\"NFS_ENDPOINT_ISILON_8\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_8\": \"/suporte\"},{\"NFS_ENDPOINT_VM_4\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_4\": \"/producao\"},{\"NFS_ENDPOINT_VM_5\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_5\": \"/SIEXC_SWIFT\"}]", 
2026-10-13T20:58:42.6825922Z         "stdout_lines": [
2026-10-13T20:58:42.6826803Z             "[{\"NFS_ENDPOINT_VM\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM\": \"/SIEXC_SWIFT\"},{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON\": \"/siexc_incoming\"},{\"NFS_ENDPOINT_ISILON_3\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC\",\"NFS_MOUNT_POINT_ISILON_3\": \"/SIAPC\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF\",\"NFS_MOUNT_POINT_ISILON_2\": \"/integracoes/SIISF\"},{\"NFS_ENDPOINT_ISILON_5\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_5\": \"/legado\"},{\"NFS_ENDPOINT_ISILON_4\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_4\": \"/SIGPL\"},{\"NFS_ENDPOINT_ISILON_7\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_7\": \"/eFinanceira/siexc/entrada\"},{\"NFS_ENDPOINT_ISILON_6\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_6\": \"/eFinanceira_ctc/siexc\"},{\"NFS_ENDPOINT_VM_2\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_2\": \"/SIEXC\"},{\"NFS_ENDPOINT_ISILON_9\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_9\": \"/siexc\"},{\"NFS_ENDPOINT_VM_3\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_3\": \"/producao/SWIFT\"},{\"NFS_ENDPOINT_ISILON_8\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_8\": \"/suporte\"},{\"NFS_ENDPOINT_VM_4\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_4\": \"/producao\"},{\"NFS_ENDPOINT_VM_5\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_5\": \"/SIEXC_SWIFT\"}]"
2026-10-13T20:58:42.6827650Z         ]
2026-10-13T20:58:42.6827738Z     }
2026-10-13T20:58:42.6827816Z }
2026-10-13T20:58:42.6847548Z Tuesday 13 October 2026  17:58:42 -0300 (0:00:00.058)       0:00:01.687 ******* 
2026-10-13T20:58:42.7410777Z 
2026-10-13T20:58:42.7411723Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-13T20:58:42.7411965Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:58:42.7451379Z Tuesday 13 October 2026  17:58:42 -0300 (0:00:00.060)       0:00:01.748 ******* 
2026-10-13T20:59:14.7464241Z 
2026-10-13T20:59:14.7465162Z TASK [nfs : execute montagem script] *******************************************
2026-10-13T20:59:14.7465422Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:14.7506592Z Tuesday 13 October 2026  17:59:14 -0300 (0:00:32.005)       0:00:33.753 ******* 
2026-10-13T20:59:14.8380354Z 
2026-10-13T20:59:14.8380790Z TASK [nfs : ansible.builtin.debug] *********************************************
2026-10-13T20:59:14.8391760Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:59:14.8391909Z     "changed": false, 
2026-10-13T20:59:14.8392261Z     "msg": {
2026-10-13T20:59:14.8395335Z         "changed": true, 
2026-10-13T20:59:14.8395764Z         "cmd": [
2026-10-13T20:59:14.8395869Z             "python", 
2026-10-13T20:59:14.8396214Z             "/opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/files/nfs.py", 
2026-10-13T20:59:14.8396353Z             "montagem", 
2026-10-13T20:59:14.8396510Z             "siexc-web-aplicacao", 
2026-10-13T20:59:14.8396605Z             "des", 
2026-10-13T20:59:14.8396700Z             "ctc_nprd", 
2026-10-13T20:59:14.8396875Z             "/opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2", 
2026-10-13T20:59:14.8397056Z             "C&t@d02", 
2026-10-13T20:59:14.8397229Z             "***", 
2026-10-13T20:59:14.8397339Z             "s736651@corp.caixa.gov.br", 
2026-10-13T20:59:14.8397454Z             "***", 
2026-10-13T20:59:14.8398351Z             "[{\"NFS_ENDPOINT_VM\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM\": \"/SIEXC_SWIFT\"},{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON\": \"/siexc_incoming\"},{\"NFS_ENDPOINT_ISILON_3\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC\",\"NFS_MOUNT_POINT_ISILON_3\": \"/SIAPC\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF\",\"NFS_MOUNT_POINT_ISILON_2\": \"/integracoes/SIISF\"},{\"NFS_ENDPOINT_ISILON_5\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_5\": \"/legado\"},{\"NFS_ENDPOINT_ISILON_4\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_4\": \"/SIGPL\"},{\"NFS_ENDPOINT_ISILON_7\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_7\": \"/eFinanceira/siexc/entrada\"},{\"NFS_ENDPOINT_ISILON_6\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_6\": \"/eFinanceira_ctc/siexc\"},{\"NFS_ENDPOINT_VM_2\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_2\": \"/SIEXC\"},{\"NFS_ENDPOINT_ISILON_9\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_9\": \"/siexc\"},{\"NFS_ENDPOINT_VM_3\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_3\": \"/producao/SWIFT\"},{\"NFS_ENDPOINT_ISILON_8\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_8\": \"/suporte\"},{\"NFS_ENDPOINT_VM_4\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_4\": \"/producao\"},{\"NFS_ENDPOINT_VM_5\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_5\": \"/SIEXC_SWIFT\"}]"
2026-10-13T20:59:14.8399386Z         ], 
2026-10-13T20:59:14.8399522Z         "delta": "0:00:31.694124", 
2026-10-13T20:59:14.8399694Z         "end": "2026-10-13 17:59:14.729999", 
2026-10-13T20:59:14.8399815Z         "failed": false, 
2026-10-13T20:59:14.8399917Z         "rc": 0, 
2026-10-13T20:59:14.8400082Z         "start": "2026-10-13 17:58:43.035875", 
2026-10-13T20:59:14.8400207Z         "stderr": "", 
2026-10-13T20:59:14.8400306Z         "stderr_lines": [], 
2026-10-13T20:59:14.8408196Z         "stdout": "[{u'NFS_MOUNT_POINT_VM': u'/SIEXC_SWIFT', u'NFS_ENDPOINT_VM': u'192.168.227.59:/export/sicql_bovespa'}, {u'NFS_MOUNT_POINT_ISILON': u'/siexc_incoming', u'NFS_ENDPOINT_ISILON': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC'}, {u'NFS_MOUNT_POINT_ISILON_3': u'/SIAPC', u'NFS_ENDPOINT_ISILON_3': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC'}, {u'NFS_MOUNT_POINT_ISILON_2': u'/integracoes/SIISF', u'NFS_ENDPOINT_ISILON_2': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF'}, {u'NFS_ENDPOINT_ISILON_5': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_5': u'/legado'}, {u'NFS_ENDPOINT_ISILON_4': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_4': u'/SIGPL'}, {u'NFS_ENDPOINT_ISILON_7': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_7': u'/eFinanceira/siexc/entrada'}, {u'NFS_ENDPOINT_ISILON_6': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_6': u'/eFinanceira_ctc/siexc'}, {u'NFS_ENDPOINT_VM_2': u'192.168.227.59:/export/sicql_bovespa', u'NFS_MOUNT_POINT_VM_2': u'/SIEXC'}, {u'NFS_ENDPOINT_ISILON_9': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_9': u'/siexc'}, {u'NFS_ENDPOINT_VM_3': u'192.168.227.59:/export/sicql_bovespa', u'NFS_MOUNT_POINT_VM_3': u'/producao/SWIFT'}, {u'NFS_MOUNT_POINT_ISILON_8': u'/suporte', u'NFS_ENDPOINT_ISILON_8': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC'}, {u'NFS_MOUNT_POINT_VM_4': u'/producao', u'NFS_ENDPOINT_VM_4': u'192.168.227.59:/export/sicql_bovespa'}, {u'NFS_MOUNT_POINT_VM_5': u'/SIEXC_SWIFT', u'NFS_ENDPOINT_VM_5': u'192.168.227.59:/export/sicql_bovespa'}]\nNome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           \n------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /integracoes/SIISF                  ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/integracoes/SIISF\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /integracoes/SIISF                  ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF /SIGPL                              ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/SIGPL\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF /SIGPL                              ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC /legado                             ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/legado\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC /legado                             ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /SIEXC_SWIFT                        ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/SIEXC_SWIFT\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /SIEXC_SWIFT                        ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao                           ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/producao\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao                           ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao/SWIFT                     ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/producao/SWIFT\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao/SWIFT                     ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /SIEXC                              ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/SIEXC\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /SIEXC                              ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira_ctc/siexc              ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/eFinanceira_ctc/siexc\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira_ctc/siexc              ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira/siexc/entrada          ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/eFinanceira/siexc/entrada\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira/siexc/entrada          ISILON                              nfsctcnprd.ctc.caixa                des                                \n192.168.227.59                      /export/sicql_bovespa               /siexc_incoming                     VM                                  192.168.227.59                      des                                \nnfs_path=/siexc_incoming\nnfs_src=192.168.227.59:/export/sicql_bovespa\n192.168.227.59                      /export/sicql_bovespa               /siexc_incoming                     VM                                  192.168.227.59                      des                                \n192.168.227.59                      /export/sicql_bovespa               /SIEXC_SWIFT                        VM                                  192.168.227.59                      des                                \nnfs_path=/SIEXC_SWIFT\nnfs_src=192.168.227.59:/export/sicql_bovespa\n192.168.227.59                      /export/sicql_bovespa               /SIEXC_SWIFT                        VM                                  192.168.227.59                      des                                \n192.168.227.59                      /export/sicql_bovespa               /SIAPC                              VM                                  192.168.227.59                      des                                \nnfs_path=/SIAPC\nnfs_src=192.168.227.59:/export/sicql_bovespa\n192.168.227.59                      /export/sicql_bovespa               /SIAPC                              VM                                  192.168.227.59                      des                                \n192.168.227.59                      /export/sicql_bovespa               /siexc                              VM                                  192.168.227.59                      des                                \nnfs_path=/siexc\nnfs_src=192.168.227.59:/export/sicql_bovespa\n192.168.227.59                      /export/sicql_bovespa               /siexc                              VM                                  192.168.227.59                      des                                \n192.168.227.59                      /export/sicql_bovespa               /suporte                            VM                                  192.168.227.59                      des                                \nnfs_path=/suporte\nnfs_src=192.168.227.59:/export/sicql_bovespa\n192.168.227.59                      /export/sicql_bovespa               /suporte                            VM                                  192.168.227.59                      des                                ", 
2026-10-13T20:59:14.8411542Z         "stdout_lines": [
2026-10-13T20:59:14.8413374Z             "[{u'NFS_MOUNT_POINT_VM': u'/SIEXC_SWIFT', u'NFS_ENDPOINT_VM': u'192.168.227.59:/export/sicql_bovespa'}, {u'NFS_MOUNT_POINT_ISILON': u'/siexc_incoming', u'NFS_ENDPOINT_ISILON': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC'}, {u'NFS_MOUNT_POINT_ISILON_3': u'/SIAPC', u'NFS_ENDPOINT_ISILON_3': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC'}, {u'NFS_MOUNT_POINT_ISILON_2': u'/integracoes/SIISF', u'NFS_ENDPOINT_ISILON_2': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF'}, {u'NFS_ENDPOINT_ISILON_5': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_5': u'/legado'}, {u'NFS_ENDPOINT_ISILON_4': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_4': u'/SIGPL'}, {u'NFS_ENDPOINT_ISILON_7': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_7': u'/eFinanceira/siexc/entrada'}, {u'NFS_ENDPOINT_ISILON_6': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_6': u'/eFinanceira_ctc/siexc'}, {u'NFS_ENDPOINT_VM_2': u'192.168.227.59:/export/sicql_bovespa', u'NFS_MOUNT_POINT_VM_2': u'/SIEXC'}, {u'NFS_ENDPOINT_ISILON_9': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_9': u'/siexc'}, {u'NFS_ENDPOINT_VM_3': u'192.168.227.59:/export/sicql_bovespa', u'NFS_MOUNT_POINT_VM_3': u'/producao/SWIFT'}, {u'NFS_MOUNT_POINT_ISILON_8': u'/suporte', u'NFS_ENDPOINT_ISILON_8': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC'}, {u'NFS_MOUNT_POINT_VM_4': u'/producao', u'NFS_ENDPOINT_VM_4': u'192.168.227.59:/export/sicql_bovespa'}, {u'NFS_MOUNT_POINT_VM_5': u'/SIEXC_SWIFT', u'NFS_ENDPOINT_VM_5': u'192.168.227.59:/export/sicql_bovespa'}]", 
2026-10-13T20:59:14.8414328Z             "Nome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           ", 
2026-10-13T20:59:14.8414685Z             "------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------", 
2026-10-13T20:59:14.8414924Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /integracoes/SIISF                  ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8415156Z             "nfs_path=/integracoes/SIISF", 
2026-10-13T20:59:14.8415294Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T20:59:14.8415479Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /integracoes/SIISF                  ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8415718Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF /SIGPL                              ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8415865Z             "nfs_path=/SIGPL", 
2026-10-13T20:59:14.8415997Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF", 
2026-10-13T20:59:14.8416212Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF /SIGPL                              ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8416401Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC /legado                             ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8416553Z             "nfs_path=/legado", 
2026-10-13T20:59:14.8416680Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC", 
2026-10-13T20:59:14.8416851Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC /legado                             ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8417083Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /SIEXC_SWIFT                        ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8417238Z             "nfs_path=/SIEXC_SWIFT", 
2026-10-13T20:59:14.8417361Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T20:59:14.8417536Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /SIEXC_SWIFT                        ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8417729Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao                           ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8417874Z             "nfs_path=/producao", 
2026-10-13T20:59:14.8418010Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T20:59:14.8418202Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao                           ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8418575Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao/SWIFT                     ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8418725Z             "nfs_path=/producao/SWIFT", 
2026-10-13T20:59:14.8418857Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T20:59:14.8419030Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao/SWIFT                     ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8419225Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /SIEXC                              ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8419363Z             "nfs_path=/SIEXC", 
2026-10-13T20:59:14.8419491Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T20:59:14.8419645Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /SIEXC                              ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8419830Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira_ctc/siexc              ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8420019Z             "nfs_path=/eFinanceira_ctc/siexc", 
2026-10-13T20:59:14.8420153Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T20:59:14.8420328Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira_ctc/siexc              ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8420528Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira/siexc/entrada          ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8420686Z             "nfs_path=/eFinanceira/siexc/entrada", 
2026-10-13T20:59:14.8420824Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T20:59:14.8421000Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira/siexc/entrada          ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T20:59:14.8421320Z             "192.168.227.59                      /export/sicql_bovespa               /siexc_incoming                     VM                                  192.168.227.59                      des                                ", 
2026-10-13T20:59:14.8421468Z             "nfs_path=/siexc_incoming", 
2026-10-13T20:59:14.8421595Z             "nfs_src=192.168.227.59:/export/sicql_bovespa", 
2026-10-13T20:59:14.8421749Z             "192.168.227.59                      /export/sicql_bovespa               /siexc_incoming                     VM                                  192.168.227.59                      des                                ", 
2026-10-13T20:59:14.8421916Z             "192.168.227.59                      /export/sicql_bovespa               /SIEXC_SWIFT                        VM                                  192.168.227.59                      des                                ", 
2026-10-13T20:59:14.8422063Z             "nfs_path=/SIEXC_SWIFT", 
2026-10-13T20:59:14.8422173Z             "nfs_src=192.168.227.59:/export/sicql_bovespa", 
2026-10-13T20:59:14.8422326Z             "192.168.227.59                      /export/sicql_bovespa               /SIEXC_SWIFT                        VM                                  192.168.227.59                      des                                ", 
2026-10-13T20:59:14.8422491Z             "192.168.227.59                      /export/sicql_bovespa               /SIAPC                              VM                                  192.168.227.59                      des                                ", 
2026-10-13T20:59:14.8422623Z             "nfs_path=/SIAPC", 
2026-10-13T20:59:14.8422742Z             "nfs_src=192.168.227.59:/export/sicql_bovespa", 
2026-10-13T20:59:14.8422894Z             "192.168.227.59                      /export/sicql_bovespa               /SIAPC                              VM                                  192.168.227.59                      des                                ", 
2026-10-13T20:59:14.8423055Z             "192.168.227.59                      /export/sicql_bovespa               /siexc                              VM                                  192.168.227.59                      des                                ", 
2026-10-13T20:59:14.8423187Z             "nfs_path=/siexc", 
2026-10-13T20:59:14.8423306Z             "nfs_src=192.168.227.59:/export/sicql_bovespa", 
2026-10-13T20:59:14.8423454Z             "192.168.227.59                      /export/sicql_bovespa               /siexc                              VM                                  192.168.227.59                      des                                ", 
2026-10-13T20:59:14.8423614Z             "192.168.227.59                      /export/sicql_bovespa               /suporte                            VM                                  192.168.227.59                      des                                ", 
2026-10-13T20:59:14.8423779Z             "nfs_path=/suporte", 
2026-10-13T20:59:14.8423901Z             "nfs_src=192.168.227.59:/export/sicql_bovespa", 
2026-10-13T20:59:14.8424036Z             "192.168.227.59                      /export/sicql_bovespa               /suporte                            VM                                  192.168.227.59                      des                                "
2026-10-13T20:59:14.8424156Z         ]
2026-10-13T20:59:14.8424245Z     }
2026-10-13T20:59:14.8424332Z }
2026-10-13T20:59:14.8430100Z Tuesday 13 October 2026  17:59:14 -0300 (0:00:00.092)       0:00:33.846 ******* 
2026-10-13T20:59:15.1453691Z 
2026-10-13T20:59:15.1454207Z TASK [nfs : execute clean json] ************************************************
2026-10-13T20:59:15.1454377Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:15.1478743Z Tuesday 13 October 2026  17:59:15 -0300 (0:00:00.304)       0:00:34.151 ******* 
2026-10-13T20:59:15.2044450Z 
2026-10-13T20:59:15.2044970Z TASK [nfs : result_new_string_json] ********************************************
2026-10-13T20:59:15.2048489Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:59:15.2048727Z     "msg": {
2026-10-13T20:59:15.2048888Z         "changed": true, 
2026-10-13T20:59:15.2050999Z         "cmd": "echo '[{\"NFS_ENDPOINT_VM\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM\": \"/SIEXC_SWIFT\"},{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON\": \"/siexc_incoming\"},{\"NFS_ENDPOINT_ISILON_3\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC\",\"NFS_MOUNT_POINT_ISILON_3\": \"/SIAPC\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF\",\"NFS_MOUNT_POINT_ISILON_2\": \"/integracoes/SIISF\"},{\"NFS_ENDPOINT_ISILON_5\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_5\": \"/legado\"},{\"NFS_ENDPOINT_ISILON_4\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_4\": \"/SIGPL\"},{\"NFS_ENDPOINT_ISILON_7\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_7\": \"/eFinanceira/siexc/entrada\"},{\"NFS_ENDPOINT_ISILON_6\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_6\": \"/eFinanceira_ctc/siexc\"},{\"NFS_ENDPOINT_VM_2\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_2\": \"/SIEXC\"},{\"NFS_ENDPOINT_ISILON_9\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_9\": \"/siexc\"},{\"NFS_ENDPOINT_VM_3\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_3\": \"/producao/SWIFT\"},{\"NFS_ENDPOINT_ISILON_8\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_8\": \"/suporte\"},{\"NFS_ENDPOINT_VM_4\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_4\": \"/producao\"},{\"NFS_ENDPOINT_VM_5\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_5\": \"/SIEXC_SWIFT\"}]' | sed 's/NFS_ENDPOINT_ISILON[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_ISILON[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_HUAWEI[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_HUAWEI[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_VM[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_VM[^\"]*/NFS_MOUNT_POINT/g'", 
2026-10-13T20:59:15.2052284Z         "delta": "0:00:00.003696", 
2026-10-13T20:59:15.2052468Z         "end": "2026-10-13 17:59:15.131131", 
2026-10-13T20:59:15.2052592Z         "failed": false, 
2026-10-13T20:59:15.2052683Z         "rc": 0, 
2026-10-13T20:59:15.2052844Z         "start": "2026-10-13 17:59:15.127435", 
2026-10-13T20:59:15.2052960Z         "stderr": "", 
2026-10-13T20:59:15.2053063Z         "stderr_lines": [], 
2026-10-13T20:59:15.2053848Z         "stdout": "[{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/SIEXC_SWIFT\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/siexc_incoming\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC\",\"NFS_MOUNT_POINT\": \"/SIAPC\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF\",\"NFS_MOUNT_POINT\": \"/integracoes/SIISF\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/legado\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/SIGPL\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/eFinanceira/siexc/entrada\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/eFinanceira_ctc/siexc\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/SIEXC\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/siexc\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/producao/SWIFT\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/suporte\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/producao\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/SIEXC_SWIFT\"}]", 
2026-10-13T20:59:15.2054950Z         "stdout_lines": [
2026-10-13T20:59:15.2055864Z             "[{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/SIEXC_SWIFT\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/siexc_incoming\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC\",\"NFS_MOUNT_POINT\": \"/SIAPC\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF\",\"NFS_MOUNT_POINT\": \"/integracoes/SIISF\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/legado\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/SIGPL\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/eFinanceira/siexc/entrada\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/eFinanceira_ctc/siexc\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/SIEXC\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/siexc\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/producao/SWIFT\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/suporte\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/producao\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/SIEXC_SWIFT\"}]"
2026-10-13T20:59:15.2056623Z         ]
2026-10-13T20:59:15.2056715Z     }
2026-10-13T20:59:15.2056801Z }
2026-10-13T20:59:15.2073830Z Tuesday 13 October 2026  17:59:15 -0300 (0:00:00.059)       0:00:34.210 ******* 
2026-10-13T20:59:15.2648221Z 
2026-10-13T20:59:15.2648695Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T20:59:15.2648870Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:15.2673549Z Tuesday 13 October 2026  17:59:15 -0300 (0:00:00.059)       0:00:34.270 ******* 
2026-10-13T20:59:15.3235750Z 
2026-10-13T20:59:15.3236209Z TASK [nfs : result_new_json] ***************************************************
2026-10-13T20:59:15.3237988Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:59:15.3238175Z     "msg": [
2026-10-13T20:59:15.3238316Z         {
2026-10-13T20:59:15.3238809Z             "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T20:59:15.3239009Z             "NFS_MOUNT_POINT": "/SIEXC_SWIFT"
2026-10-13T20:59:15.3239149Z         }, 
2026-10-13T20:59:15.3239277Z         {
2026-10-13T20:59:15.3239487Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T20:59:15.3239636Z             "NFS_MOUNT_POINT": "/siexc_incoming"
2026-10-13T20:59:15.3239737Z         }, 
2026-10-13T20:59:15.3239826Z         {
2026-10-13T20:59:15.3239949Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC", 
2026-10-13T20:59:15.3240084Z             "NFS_MOUNT_POINT": "/SIAPC"
2026-10-13T20:59:15.3240171Z         }, 
2026-10-13T20:59:15.3240254Z         {
2026-10-13T20:59:15.3240379Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF", 
2026-10-13T20:59:15.3240529Z             "NFS_MOUNT_POINT": "/integracoes/SIISF"
2026-10-13T20:59:15.3240715Z         }, 
2026-10-13T20:59:15.3240798Z         {
2026-10-13T20:59:15.3240914Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T20:59:15.3241109Z             "NFS_MOUNT_POINT": "/legado"
2026-10-13T20:59:15.3241252Z         }, 
2026-10-13T20:59:15.3241376Z         {
2026-10-13T20:59:15.3241560Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T20:59:15.3241739Z             "NFS_MOUNT_POINT": "/SIGPL"
2026-10-13T20:59:15.3241923Z         }, 
2026-10-13T20:59:15.3242015Z         {
2026-10-13T20:59:15.3242137Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T20:59:15.3242276Z             "NFS_MOUNT_POINT": "/eFinanceira/siexc/entrada"
2026-10-13T20:59:15.3242383Z         }, 
2026-10-13T20:59:15.3242469Z         {
2026-10-13T20:59:15.3242590Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T20:59:15.3242738Z             "NFS_MOUNT_POINT": "/eFinanceira_ctc/siexc"
2026-10-13T20:59:15.3242834Z         }, 
2026-10-13T20:59:15.3242973Z         {
2026-10-13T20:59:15.3243090Z             "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T20:59:15.3243215Z             "NFS_MOUNT_POINT": "/SIEXC"
2026-10-13T20:59:15.3243313Z         }, 
2026-10-13T20:59:15.3243397Z         {
2026-10-13T20:59:15.3243511Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T20:59:15.3243644Z             "NFS_MOUNT_POINT": "/siexc"
2026-10-13T20:59:15.3243738Z         }, 
2026-10-13T20:59:15.3243819Z         {
2026-10-13T20:59:15.3243936Z             "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T20:59:15.3244061Z             "NFS_MOUNT_POINT": "/producao/SWIFT"
2026-10-13T20:59:15.3244161Z         }, 
2026-10-13T20:59:15.3244244Z         {
2026-10-13T20:59:15.3244354Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T20:59:15.3244488Z             "NFS_MOUNT_POINT": "/suporte"
2026-10-13T20:59:15.3244587Z         }, 
2026-10-13T20:59:15.3244668Z         {
2026-10-13T20:59:15.3244778Z             "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T20:59:15.3244901Z             "NFS_MOUNT_POINT": "/producao"
2026-10-13T20:59:15.3245102Z         }, 
2026-10-13T20:59:15.3245202Z         {
2026-10-13T20:59:15.3245314Z             "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T20:59:15.3245437Z             "NFS_MOUNT_POINT": "/SIEXC_SWIFT"
2026-10-13T20:59:15.3245534Z         }
2026-10-13T20:59:15.3245620Z     ]
2026-10-13T20:59:15.3245705Z }
2026-10-13T20:59:15.3264569Z Tuesday 13 October 2026  17:59:15 -0300 (0:00:00.059)       0:00:34.329 ******* 
2026-10-13T20:59:15.4410675Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T20:59:15.4489441Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T20:59:15.4562763Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T20:59:15.4634452Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T20:59:15.4705541Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T20:59:15.4778081Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T20:59:15.4852880Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T20:59:15.4929980Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T20:59:15.5001049Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T20:59:15.5080348Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T20:59:15.5154846Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T20:59:15.5228865Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T20:59:15.5300847Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T20:59:15.5376320Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T20:59:15.5432002Z Tuesday 13 October 2026  17:59:15 -0300 (0:00:00.216)       0:00:34.546 ******* 
2026-10-13T20:59:15.5967758Z 
2026-10-13T20:59:15.5968554Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T20:59:15.5968794Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:15.5992498Z Tuesday 13 October 2026  17:59:15 -0300 (0:00:00.056)       0:00:34.602 ******* 
2026-10-13T20:59:15.6513899Z 
2026-10-13T20:59:15.6514332Z TASK [nfs : debug] *************************************************************
2026-10-13T20:59:15.6514506Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:59:15.6514628Z     "msg": {
2026-10-13T20:59:15.6514751Z         "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T20:59:15.6514886Z         "NFS_MOUNT_POINT": "/SIEXC_SWIFT"
2026-10-13T20:59:15.6515081Z     }
2026-10-13T20:59:15.6515172Z }
2026-10-13T20:59:15.6540262Z Tuesday 13 October 2026  17:59:15 -0300 (0:00:00.054)       0:00:34.657 ******* 
2026-10-13T20:59:15.7073174Z 
2026-10-13T20:59:15.7074168Z TASK [nfs : debug] *************************************************************
2026-10-13T20:59:15.7074940Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:59:15.7075301Z     "msg": "/SIEXC_SWIFT"
2026-10-13T20:59:15.7075408Z }
2026-10-13T20:59:15.7097370Z Tuesday 13 October 2026  17:59:15 -0300 (0:00:00.055)       0:00:34.712 ******* 
2026-10-13T20:59:15.7615772Z 
2026-10-13T20:59:15.7616106Z TASK [nfs : debug] *************************************************************
2026-10-13T20:59:15.7616276Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:59:15.7616417Z     "msg": "192.168.227.59:/export/sicql_bovespa"
2026-10-13T20:59:15.7616524Z }
2026-10-13T20:59:15.7643155Z Tuesday 13 October 2026  17:59:15 -0300 (0:00:00.054)       0:00:34.767 ******* 
2026-10-13T20:59:15.8200226Z 
2026-10-13T20:59:15.8200709Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T20:59:15.8201166Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:59:15.8201303Z     "changed": false, 
2026-10-13T20:59:15.8201423Z     "msg": "All assertions passed"
2026-10-13T20:59:15.8201513Z }
2026-10-13T20:59:15.8227404Z Tuesday 13 October 2026  17:59:15 -0300 (0:00:00.058)       0:00:34.825 ******* 
2026-10-13T20:59:19.1081117Z 
2026-10-13T20:59:19.1081664Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T20:59:19.1081833Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:19.1109857Z Tuesday 13 October 2026  17:59:19 -0300 (0:00:03.288)       0:00:38.114 ******* 
2026-10-13T20:59:22.2355905Z 
2026-10-13T20:59:22.2356407Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T20:59:22.2356596Z [WARNING]: Consider using the yum, dnf or zypper module rather than running
2026-10-13T20:59:22.2356944Z 'rpm'.  If you need to use command because yum, dnf or zypper is insufficient
2026-10-13T20:59:22.2357488Z you can add 'warn: false' to this command task or set 'command_warnings=False'
2026-10-13T20:59:22.2392919Z in ansible.cfg to get rid of this message.
2026-10-13T20:59:22.2393258Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:22.2393621Z Tuesday 13 October 2026  17:59:22 -0300 (0:00:03.127)       0:00:41.241 ******* 
2026-10-13T20:59:25.5471155Z 
2026-10-13T20:59:25.5471652Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T20:59:25.5471863Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:25.5504892Z Tuesday 13 October 2026  17:59:25 -0300 (0:00:03.311)       0:00:44.553 ******* 
2026-10-13T20:59:25.9473622Z 
2026-10-13T20:59:25.9474310Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T20:59:25.9474478Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:25.9503858Z Tuesday 13 October 2026  17:59:25 -0300 (0:00:00.399)       0:00:44.953 ******* 
2026-10-13T20:59:26.2005179Z 
2026-10-13T20:59:26.2006101Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T20:59:26.2006309Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:26.2034049Z Tuesday 13 October 2026  17:59:26 -0300 (0:00:00.253)       0:00:45.206 ******* 
2026-10-13T20:59:27.3165976Z 
2026-10-13T20:59:27.3166478Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T20:59:27.3166647Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:27.3203618Z Tuesday 13 October 2026  17:59:27 -0300 (0:00:01.116)       0:00:46.323 ******* 
2026-10-13T20:59:27.5826798Z 
2026-10-13T20:59:27.5827292Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T20:59:27.5827455Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:27.5853328Z Tuesday 13 October 2026  17:59:27 -0300 (0:00:00.264)       0:00:46.588 ******* 
2026-10-13T20:59:37.9936514Z 
2026-10-13T20:59:37.9937166Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T20:59:37.9937340Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:37.9964533Z Tuesday 13 October 2026  17:59:37 -0300 (0:00:10.411)       0:00:56.999 ******* 
2026-10-13T20:59:38.7095990Z 
2026-10-13T20:59:38.7096515Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T20:59:38.7096688Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:38.7123458Z Tuesday 13 October 2026  17:59:38 -0300 (0:00:00.715)       0:00:57.715 ******* 
2026-10-13T20:59:38.7525352Z Tuesday 13 October 2026  17:59:38 -0300 (0:00:00.040)       0:00:57.755 ******* 
2026-10-13T20:59:38.8045178Z 
2026-10-13T20:59:38.8046312Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T20:59:38.8046477Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:38.8069112Z Tuesday 13 October 2026  17:59:38 -0300 (0:00:00.054)       0:00:57.810 ******* 
2026-10-13T20:59:38.8596558Z 
2026-10-13T20:59:38.8597575Z TASK [nfs : debug] *************************************************************
2026-10-13T20:59:38.8597796Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:59:38.8597914Z     "msg": {
2026-10-13T20:59:38.8598049Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T20:59:38.8598196Z         "NFS_MOUNT_POINT": "/siexc_incoming"
2026-10-13T20:59:38.8600047Z     }
2026-10-13T20:59:38.8600182Z }
2026-10-13T20:59:38.8621311Z Tuesday 13 October 2026  17:59:38 -0300 (0:00:00.055)       0:00:57.865 ******* 
2026-10-13T20:59:38.9137284Z 
2026-10-13T20:59:38.9137673Z TASK [nfs : debug] *************************************************************
2026-10-13T20:59:38.9137839Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:59:38.9137970Z     "msg": "/siexc_incoming"
2026-10-13T20:59:38.9138076Z }
2026-10-13T20:59:38.9161069Z Tuesday 13 October 2026  17:59:38 -0300 (0:00:00.053)       0:00:57.919 ******* 
2026-10-13T20:59:38.9680189Z 
2026-10-13T20:59:38.9680642Z TASK [nfs : debug] *************************************************************
2026-10-13T20:59:38.9680813Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:59:38.9680965Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC"
2026-10-13T20:59:38.9681086Z }
2026-10-13T20:59:38.9704743Z Tuesday 13 October 2026  17:59:38 -0300 (0:00:00.054)       0:00:57.973 ******* 
2026-10-13T20:59:39.0246397Z 
2026-10-13T20:59:39.0246852Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T20:59:39.0247020Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:59:39.0247134Z     "changed": false, 
2026-10-13T20:59:39.0247252Z     "msg": "All assertions passed"
2026-10-13T20:59:39.0247349Z }
2026-10-13T20:59:39.0270538Z Tuesday 13 October 2026  17:59:39 -0300 (0:00:00.056)       0:00:58.030 ******* 
2026-10-13T20:59:41.6929586Z 
2026-10-13T20:59:41.6930127Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T20:59:41.6930296Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:41.6955982Z Tuesday 13 October 2026  17:59:41 -0300 (0:00:02.668)       0:01:00.698 ******* 
2026-10-13T20:59:42.8949195Z 
2026-10-13T20:59:42.8949695Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T20:59:42.8954083Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.921917", "end": "2026-10-13 17:59:42.880561", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 17:59:41.958644", "stderr": "aviso: /var/tmp/rpm-tmp.3OsBPQ: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.3OsBPQ: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T20:59:42.8954868Z ...ignoring
2026-10-13T20:59:42.8981137Z Tuesday 13 October 2026  17:59:42 -0300 (0:00:01.202)       0:01:01.901 ******* 
2026-10-13T20:59:43.8555395Z 
2026-10-13T20:59:43.8555918Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T20:59:43.8557278Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.712114", "end": "2026-10-13 17:59:43.839788", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 17:59:43.127674", "stderr": "aviso: /var/tmp/rpm-tmp.ASksxV: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.ASksxV: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T20:59:43.8558216Z ...ignoring
2026-10-13T20:59:43.8579849Z Tuesday 13 October 2026  17:59:43 -0300 (0:00:00.959)       0:01:02.861 ******* 
2026-10-13T20:59:44.1060588Z 
2026-10-13T20:59:44.1061250Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T20:59:44.1061447Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:44.1093220Z Tuesday 13 October 2026  17:59:44 -0300 (0:00:00.251)       0:01:03.112 ******* 
2026-10-13T20:59:44.3515835Z 
2026-10-13T20:59:44.3516425Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T20:59:44.3516684Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:44.3544672Z Tuesday 13 October 2026  17:59:44 -0300 (0:00:00.245)       0:01:03.357 ******* 
2026-10-13T20:59:44.9733687Z 
2026-10-13T20:59:44.9734220Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T20:59:44.9734382Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:44.9773116Z Tuesday 13 October 2026  17:59:44 -0300 (0:00:00.622)       0:01:03.980 ******* 
2026-10-13T20:59:45.2357905Z 
2026-10-13T20:59:45.2358417Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T20:59:45.2358587Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:45.2384792Z Tuesday 13 October 2026  17:59:45 -0300 (0:00:00.261)       0:01:04.241 ******* 
2026-10-13T20:59:55.6430477Z 
2026-10-13T20:59:55.6430971Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T20:59:55.6431130Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:55.6456967Z Tuesday 13 October 2026  17:59:55 -0300 (0:00:10.407)       0:01:14.648 ******* 
2026-10-13T20:59:55.9608485Z 
2026-10-13T20:59:55.9608998Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T20:59:55.9609166Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:55.9634913Z Tuesday 13 October 2026  17:59:55 -0300 (0:00:00.317)       0:01:14.966 ******* 
2026-10-13T20:59:56.0045761Z Tuesday 13 October 2026  17:59:56 -0300 (0:00:00.041)       0:01:15.007 ******* 
2026-10-13T20:59:56.0579877Z 
2026-10-13T20:59:56.0580580Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T20:59:56.0580789Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:56.0603103Z Tuesday 13 October 2026  17:59:56 -0300 (0:00:00.055)       0:01:15.063 ******* 
2026-10-13T20:59:56.1122182Z 
2026-10-13T20:59:56.1122610Z TASK [nfs : debug] *************************************************************
2026-10-13T20:59:56.1123639Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:59:56.1123773Z     "msg": {
2026-10-13T20:59:56.1123894Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC", 
2026-10-13T20:59:56.1124038Z         "NFS_MOUNT_POINT": "/SIAPC"
2026-10-13T20:59:56.1124137Z     }
2026-10-13T20:59:56.1124500Z }
2026-10-13T20:59:56.1147296Z Tuesday 13 October 2026  17:59:56 -0300 (0:00:00.054)       0:01:15.117 ******* 
2026-10-13T20:59:56.1668193Z 
2026-10-13T20:59:56.1668786Z TASK [nfs : debug] *************************************************************
2026-10-13T20:59:56.1669018Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:59:56.1669145Z     "msg": "/SIAPC"
2026-10-13T20:59:56.1669240Z }
2026-10-13T20:59:56.1691341Z Tuesday 13 October 2026  17:59:56 -0300 (0:00:00.054)       0:01:15.172 ******* 
2026-10-13T20:59:56.2206450Z 
2026-10-13T20:59:56.2206938Z TASK [nfs : debug] *************************************************************
2026-10-13T20:59:56.2207453Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:59:56.2207655Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC"
2026-10-13T20:59:56.2207768Z }
2026-10-13T20:59:56.2230547Z Tuesday 13 October 2026  17:59:56 -0300 (0:00:00.053)       0:01:15.226 ******* 
2026-10-13T20:59:56.2779743Z 
2026-10-13T20:59:56.2780487Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T20:59:56.2780638Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T20:59:56.2780763Z     "changed": false, 
2026-10-13T20:59:56.2780877Z     "msg": "All assertions passed"
2026-10-13T20:59:56.2780980Z }
2026-10-13T20:59:56.2801965Z Tuesday 13 October 2026  17:59:56 -0300 (0:00:00.057)       0:01:15.283 ******* 
2026-10-13T20:59:58.8924474Z 
2026-10-13T20:59:58.8924977Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T20:59:58.8925260Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T20:59:58.8953538Z Tuesday 13 October 2026  17:59:58 -0300 (0:00:02.615)       0:01:17.898 ******* 
2026-10-13T20:59:59.8365789Z 
2026-10-13T20:59:59.8366290Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T20:59:59.8370579Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.678377", "end": "2026-10-13 17:59:59.821764", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 17:59:59.143387", "stderr": "aviso: /var/tmp/rpm-tmp.NUBeoe: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.NUBeoe: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T20:59:59.8371211Z ...ignoring
2026-10-13T20:59:59.8398103Z Tuesday 13 October 2026  17:59:59 -0300 (0:00:00.944)       0:01:18.842 ******* 
2026-10-13T21:00:01.1524284Z 
2026-10-13T21:00:01.1525229Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T21:00:01.1528934Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:01.063016", "end": "2026-10-13 18:00:01.137876", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:00:00.074860", "stderr": "aviso: /var/tmp/rpm-tmp.dcG3Go: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.dcG3Go: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:00:01.1529838Z ...ignoring
2026-10-13T21:00:01.1559151Z Tuesday 13 October 2026  18:00:01 -0300 (0:00:01.316)       0:01:20.159 ******* 
2026-10-13T21:00:01.4036415Z 
2026-10-13T21:00:01.4037123Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T21:00:01.4037292Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:01.4066851Z Tuesday 13 October 2026  18:00:01 -0300 (0:00:00.250)       0:01:20.409 ******* 
2026-10-13T21:00:01.6544012Z 
2026-10-13T21:00:01.6544493Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T21:00:01.6544661Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:01.6570265Z Tuesday 13 October 2026  18:00:01 -0300 (0:00:00.250)       0:01:20.660 ******* 
2026-10-13T21:00:02.2917886Z 
2026-10-13T21:00:02.2918406Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T21:00:02.2918564Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:02.2955604Z Tuesday 13 October 2026  18:00:02 -0300 (0:00:00.638)       0:01:21.298 ******* 
2026-10-13T21:00:02.5585136Z 
2026-10-13T21:00:02.5585652Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T21:00:02.5585808Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:02.5611287Z Tuesday 13 October 2026  18:00:02 -0300 (0:00:00.265)       0:01:21.564 ******* 
2026-10-13T21:00:13.0192140Z 
2026-10-13T21:00:13.0192668Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T21:00:13.0192835Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:13.0217774Z Tuesday 13 October 2026  18:00:13 -0300 (0:00:10.460)       0:01:32.024 ******* 
2026-10-13T21:00:13.3538327Z 
2026-10-13T21:00:13.3538818Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T21:00:13.3538993Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:13.3565412Z Tuesday 13 October 2026  18:00:13 -0300 (0:00:00.334)       0:01:32.359 ******* 
2026-10-13T21:00:13.3973581Z Tuesday 13 October 2026  18:00:13 -0300 (0:00:00.040)       0:01:32.400 ******* 
2026-10-13T21:00:13.4522837Z 
2026-10-13T21:00:13.4523025Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T21:00:13.4523322Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:13.4547213Z Tuesday 13 October 2026  18:00:13 -0300 (0:00:00.057)       0:01:32.457 ******* 
2026-10-13T21:00:13.5102586Z 
2026-10-13T21:00:13.5102887Z TASK [nfs : debug] *************************************************************
2026-10-13T21:00:13.5103299Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:00:13.5103416Z     "msg": {
2026-10-13T21:00:13.5103544Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF", 
2026-10-13T21:00:13.5103691Z         "NFS_MOUNT_POINT": "/integracoes/SIISF"
2026-10-13T21:00:13.5103798Z     }
2026-10-13T21:00:13.5103889Z }
2026-10-13T21:00:13.5141229Z Tuesday 13 October 2026  18:00:13 -0300 (0:00:00.059)       0:01:32.517 ******* 
2026-10-13T21:00:13.5685584Z 
2026-10-13T21:00:13.5686037Z TASK [nfs : debug] *************************************************************
2026-10-13T21:00:13.5686197Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:00:13.5686327Z     "msg": "/integracoes/SIISF"
2026-10-13T21:00:13.5686428Z }
2026-10-13T21:00:13.5713869Z Tuesday 13 October 2026  18:00:13 -0300 (0:00:00.057)       0:01:32.574 ******* 
2026-10-13T21:00:13.6261384Z 
2026-10-13T21:00:13.6262045Z TASK [nfs : debug] *************************************************************
2026-10-13T21:00:13.6262289Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:00:13.6262478Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF"
2026-10-13T21:00:13.6262599Z }
2026-10-13T21:00:13.6289263Z Tuesday 13 October 2026  18:00:13 -0300 (0:00:00.057)       0:01:32.632 ******* 
2026-10-13T21:00:13.6870788Z 
2026-10-13T21:00:13.6871573Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T21:00:13.6871983Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:00:13.6872545Z     "changed": false, 
2026-10-13T21:00:13.6872743Z     "msg": "All assertions passed"
2026-10-13T21:00:13.6872850Z }
2026-10-13T21:00:13.6895287Z Tuesday 13 October 2026  18:00:13 -0300 (0:00:00.060)       0:01:32.692 ******* 
2026-10-13T21:00:16.2937741Z 
2026-10-13T21:00:16.2938783Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T21:00:16.2939090Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:16.2964504Z Tuesday 13 October 2026  18:00:16 -0300 (0:00:02.606)       0:01:35.299 ******* 
2026-10-13T21:00:17.3867693Z 
2026-10-13T21:00:17.3868248Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T21:00:17.3872383Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.852795", "end": "2026-10-13 18:00:17.368828", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:00:16.516033", "stderr": "aviso: /var/tmp/rpm-tmp.LfOh7B: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.LfOh7B: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:00:17.3873038Z ...ignoring
2026-10-13T21:00:17.3898733Z Tuesday 13 October 2026  18:00:17 -0300 (0:00:01.093)       0:01:36.393 ******* 
2026-10-13T21:00:18.6864133Z 
2026-10-13T21:00:18.6864828Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T21:00:18.6870797Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:01.037970", "end": "2026-10-13 18:00:18.669362", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:00:17.631392", "stderr": "aviso: /var/tmp/rpm-tmp.7bzh7F: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.7bzh7F: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:00:18.6871881Z ...ignoring
2026-10-13T21:00:18.6898683Z Tuesday 13 October 2026  18:00:18 -0300 (0:00:01.299)       0:01:37.693 ******* 
2026-10-13T21:00:18.9416109Z 
2026-10-13T21:00:18.9416797Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T21:00:18.9416966Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:18.9442315Z Tuesday 13 October 2026  18:00:18 -0300 (0:00:00.254)       0:01:37.947 ******* 
2026-10-13T21:00:19.1872117Z 
2026-10-13T21:00:19.1873046Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T21:00:19.1873286Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:19.1899897Z Tuesday 13 October 2026  18:00:19 -0300 (0:00:00.245)       0:01:38.193 ******* 
2026-10-13T21:00:19.8259387Z 
2026-10-13T21:00:19.8259888Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T21:00:19.8260067Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:19.8297695Z Tuesday 13 October 2026  18:00:19 -0300 (0:00:00.639)       0:01:38.832 ******* 
2026-10-13T21:00:20.0831987Z 
2026-10-13T21:00:20.0832488Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T21:00:20.0832659Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:20.0858948Z Tuesday 13 October 2026  18:00:20 -0300 (0:00:00.256)       0:01:39.089 ******* 
2026-10-13T21:00:30.5248390Z 
2026-10-13T21:00:30.5248884Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T21:00:30.5249652Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:30.5271594Z Tuesday 13 October 2026  18:00:30 -0300 (0:00:10.441)       0:01:49.530 ******* 
2026-10-13T21:00:34.3497157Z 
2026-10-13T21:00:34.3497670Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T21:00:34.3497837Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:34.3526177Z Tuesday 13 October 2026  18:00:34 -0300 (0:00:03.825)       0:01:53.355 ******* 
2026-10-13T21:00:34.3934839Z Tuesday 13 October 2026  18:00:34 -0300 (0:00:00.040)       0:01:53.396 ******* 
2026-10-13T21:00:34.4462141Z 
2026-10-13T21:00:34.4462868Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T21:00:34.4463091Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:34.4485463Z Tuesday 13 October 2026  18:00:34 -0300 (0:00:00.055)       0:01:53.451 ******* 
2026-10-13T21:00:34.5020618Z 
2026-10-13T21:00:34.5021049Z TASK [nfs : debug] *************************************************************
2026-10-13T21:00:34.5021213Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:00:34.5021328Z     "msg": {
2026-10-13T21:00:34.5021461Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T21:00:34.5021605Z         "NFS_MOUNT_POINT": "/legado"
2026-10-13T21:00:34.5021757Z     }
2026-10-13T21:00:34.5021882Z }
2026-10-13T21:00:34.5045207Z Tuesday 13 October 2026  18:00:34 -0300 (0:00:00.055)       0:01:53.507 ******* 
2026-10-13T21:00:34.5559006Z 
2026-10-13T21:00:34.5559279Z TASK [nfs : debug] *************************************************************
2026-10-13T21:00:34.5560252Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:00:34.5560390Z     "msg": "/legado"
2026-10-13T21:00:34.5560487Z }
2026-10-13T21:00:34.5583989Z Tuesday 13 October 2026  18:00:34 -0300 (0:00:00.053)       0:01:53.561 ******* 
2026-10-13T21:00:34.6112618Z 
2026-10-13T21:00:34.6113279Z TASK [nfs : debug] *************************************************************
2026-10-13T21:00:34.6113500Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:00:34.6113653Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC"
2026-10-13T21:00:34.6113778Z }
2026-10-13T21:00:34.6136423Z Tuesday 13 October 2026  18:00:34 -0300 (0:00:00.055)       0:01:53.616 ******* 
2026-10-13T21:00:34.6678188Z 
2026-10-13T21:00:34.6678811Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T21:00:34.6679770Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:00:34.6679911Z     "changed": false, 
2026-10-13T21:00:34.6680036Z     "msg": "All assertions passed"
2026-10-13T21:00:34.6680139Z }
2026-10-13T21:00:34.6704367Z Tuesday 13 October 2026  18:00:34 -0300 (0:00:00.056)       0:01:53.673 ******* 
2026-10-13T21:00:37.3103531Z 
2026-10-13T21:00:37.3104029Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T21:00:37.3104187Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:37.3130693Z Tuesday 13 October 2026  18:00:37 -0300 (0:00:02.642)       0:01:56.316 ******* 
2026-10-13T21:00:38.9709789Z 
2026-10-13T21:00:38.9710301Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T21:00:38.9713963Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:01.413127", "end": "2026-10-13 18:00:38.950523", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:00:37.537396", "stderr": "aviso: /var/tmp/rpm-tmp.dqVFMI: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.dqVFMI: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:00:38.9715166Z ...ignoring
2026-10-13T21:00:38.9739893Z Tuesday 13 October 2026  18:00:38 -0300 (0:00:01.660)       0:01:57.977 ******* 
2026-10-13T21:00:40.2081092Z 
2026-10-13T21:00:40.2081608Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T21:00:40.2085602Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.962902", "end": "2026-10-13 18:00:40.191950", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:00:39.229048", "stderr": "aviso: /var/tmp/rpm-tmp.PRTG77: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.PRTG77: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:00:40.2086234Z ...ignoring
2026-10-13T21:00:40.2113542Z Tuesday 13 October 2026  18:00:40 -0300 (0:00:01.237)       0:01:59.214 ******* 
2026-10-13T21:00:40.4700373Z 
2026-10-13T21:00:40.4701082Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T21:00:40.4701246Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:40.4730803Z Tuesday 13 October 2026  18:00:40 -0300 (0:00:00.261)       0:01:59.476 ******* 
2026-10-13T21:00:40.7321517Z 
2026-10-13T21:00:40.7322021Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T21:00:40.7322172Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:40.7348692Z Tuesday 13 October 2026  18:00:40 -0300 (0:00:00.261)       0:01:59.737 ******* 
2026-10-13T21:00:41.4042266Z 
2026-10-13T21:00:41.4042788Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T21:00:41.4042958Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:41.4080892Z Tuesday 13 October 2026  18:00:41 -0300 (0:00:00.673)       0:02:00.411 ******* 
2026-10-13T21:00:41.6636495Z 
2026-10-13T21:00:41.6636976Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T21:00:41.6637144Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:41.6662144Z Tuesday 13 October 2026  18:00:41 -0300 (0:00:00.258)       0:02:00.669 ******* 
2026-10-13T21:00:52.0990353Z 
2026-10-13T21:00:52.0991155Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T21:00:52.0991304Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:52.1017397Z Tuesday 13 October 2026  18:00:52 -0300 (0:00:10.435)       0:02:11.104 ******* 
2026-10-13T21:00:52.4155814Z 
2026-10-13T21:00:52.4156314Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T21:00:52.4156483Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:52.4181947Z Tuesday 13 October 2026  18:00:52 -0300 (0:00:00.316)       0:02:11.421 ******* 
2026-10-13T21:00:52.4583918Z Tuesday 13 October 2026  18:00:52 -0300 (0:00:00.040)       0:02:11.461 ******* 
2026-10-13T21:00:52.5112109Z 
2026-10-13T21:00:52.5112552Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T21:00:52.5112720Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:52.5136081Z Tuesday 13 October 2026  18:00:52 -0300 (0:00:00.055)       0:02:11.516 ******* 
2026-10-13T21:00:52.5677864Z 
2026-10-13T21:00:52.5678298Z TASK [nfs : debug] *************************************************************
2026-10-13T21:00:52.5678460Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:00:52.5678583Z     "msg": {
2026-10-13T21:00:52.5678842Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T21:00:52.5678988Z         "NFS_MOUNT_POINT": "/SIGPL"
2026-10-13T21:00:52.5679088Z     }
2026-10-13T21:00:52.5679165Z }
2026-10-13T21:00:52.5700249Z Tuesday 13 October 2026  18:00:52 -0300 (0:00:00.056)       0:02:11.573 ******* 
2026-10-13T21:00:52.6227680Z 
2026-10-13T21:00:52.6227943Z TASK [nfs : debug] *************************************************************
2026-10-13T21:00:52.6230247Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:00:52.6230382Z     "msg": "/SIGPL"
2026-10-13T21:00:52.6230478Z }
2026-10-13T21:00:52.6253968Z Tuesday 13 October 2026  18:00:52 -0300 (0:00:00.055)       0:02:11.628 ******* 
2026-10-13T21:00:52.6769059Z 
2026-10-13T21:00:52.6769561Z TASK [nfs : debug] *************************************************************
2026-10-13T21:00:52.6769961Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:00:52.6770121Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC"
2026-10-13T21:00:52.6770248Z }
2026-10-13T21:00:52.6793985Z Tuesday 13 October 2026  18:00:52 -0300 (0:00:00.053)       0:02:11.682 ******* 
2026-10-13T21:00:52.7333421Z 
2026-10-13T21:00:52.7333885Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T21:00:52.7334067Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:00:52.7334190Z     "changed": false, 
2026-10-13T21:00:52.7334305Z     "msg": "All assertions passed"
2026-10-13T21:00:52.7334404Z }
2026-10-13T21:00:52.7357843Z Tuesday 13 October 2026  18:00:52 -0300 (0:00:00.056)       0:02:11.738 ******* 
2026-10-13T21:00:55.3928661Z 
2026-10-13T21:00:55.3929663Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T21:00:55.3929921Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:55.3949388Z Tuesday 13 October 2026  18:00:55 -0300 (0:00:02.659)       0:02:14.398 ******* 
2026-10-13T21:00:56.8901878Z 
2026-10-13T21:00:56.8902472Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T21:00:56.8906729Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:01.249076", "end": "2026-10-13 18:00:56.874813", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:00:55.625737", "stderr": "aviso: /var/tmp/rpm-tmp.C0ZyRh: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.C0ZyRh: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:00:56.8907658Z ...ignoring
2026-10-13T21:00:56.8936716Z Tuesday 13 October 2026  18:00:56 -0300 (0:00:01.498)       0:02:15.896 ******* 
2026-10-13T21:00:59.2435172Z 
2026-10-13T21:00:59.2435684Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T21:00:59.2439872Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:02.108058", "end": "2026-10-13 18:00:59.228077", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:00:57.120019", "stderr": "aviso: /var/tmp/rpm-tmp.tzy3aQ: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.tzy3aQ: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:00:59.2440520Z ...ignoring
2026-10-13T21:00:59.2467643Z Tuesday 13 October 2026  18:00:59 -0300 (0:00:02.353)       0:02:18.249 ******* 
2026-10-13T21:00:59.5036239Z 
2026-10-13T21:00:59.5037356Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T21:00:59.5037597Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:59.5064775Z Tuesday 13 October 2026  18:00:59 -0300 (0:00:00.259)       0:02:18.509 ******* 
2026-10-13T21:00:59.7500229Z 
2026-10-13T21:00:59.7500696Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T21:00:59.7500866Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:00:59.7527105Z Tuesday 13 October 2026  18:00:59 -0300 (0:00:00.246)       0:02:18.755 ******* 
2026-10-13T21:01:00.3769793Z 
2026-10-13T21:01:00.3770281Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T21:01:00.3770725Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:00.3807948Z Tuesday 13 October 2026  18:01:00 -0300 (0:00:00.628)       0:02:19.383 ******* 
2026-10-13T21:01:00.6407257Z 
2026-10-13T21:01:00.6407562Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T21:01:00.6407720Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:00.6434897Z Tuesday 13 October 2026  18:01:00 -0300 (0:00:00.262)       0:02:19.646 ******* 
2026-10-13T21:01:11.0592040Z 
2026-10-13T21:01:11.0592805Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T21:01:11.0593139Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:11.0619896Z Tuesday 13 October 2026  18:01:11 -0300 (0:00:10.418)       0:02:30.065 ******* 
2026-10-13T21:01:11.3910373Z 
2026-10-13T21:01:11.3910947Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T21:01:11.3911197Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:11.3937611Z Tuesday 13 October 2026  18:01:11 -0300 (0:00:00.331)       0:02:30.396 ******* 
2026-10-13T21:01:11.4350331Z Tuesday 13 October 2026  18:01:11 -0300 (0:00:00.041)       0:02:30.437 ******* 
2026-10-13T21:01:11.4878575Z 
2026-10-13T21:01:11.4879219Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T21:01:11.4879616Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:11.4901274Z Tuesday 13 October 2026  18:01:11 -0300 (0:00:00.055)       0:02:30.493 ******* 
2026-10-13T21:01:11.5435662Z 
2026-10-13T21:01:11.5436489Z TASK [nfs : debug] *************************************************************
2026-10-13T21:01:11.5436725Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:01:11.5436850Z     "msg": {
2026-10-13T21:01:11.5437228Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T21:01:11.5437392Z         "NFS_MOUNT_POINT": "/eFinanceira/siexc/entrada"
2026-10-13T21:01:11.5437527Z     }
2026-10-13T21:01:11.5437609Z }
2026-10-13T21:01:11.5460039Z Tuesday 13 October 2026  18:01:11 -0300 (0:00:00.055)       0:02:30.549 ******* 
2026-10-13T21:01:11.5982797Z 
2026-10-13T21:01:11.5983247Z TASK [nfs : debug] *************************************************************
2026-10-13T21:01:11.5983394Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:01:11.5983542Z     "msg": "/eFinanceira/siexc/entrada"
2026-10-13T21:01:11.5983650Z }
2026-10-13T21:01:11.6007325Z Tuesday 13 October 2026  18:01:11 -0300 (0:00:00.054)       0:02:30.603 ******* 
2026-10-13T21:01:11.6537805Z 
2026-10-13T21:01:11.6538387Z TASK [nfs : debug] *************************************************************
2026-10-13T21:01:11.6538582Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:01:11.6538723Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC"
2026-10-13T21:01:11.6538854Z }
2026-10-13T21:01:11.6561779Z Tuesday 13 October 2026  18:01:11 -0300 (0:00:00.055)       0:02:30.659 ******* 
2026-10-13T21:01:11.7111809Z 
2026-10-13T21:01:11.7112245Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T21:01:11.7112452Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:01:11.7112580Z     "changed": false, 
2026-10-13T21:01:11.7112693Z     "msg": "All assertions passed"
2026-10-13T21:01:11.7112791Z }
2026-10-13T21:01:11.7137399Z Tuesday 13 October 2026  18:01:11 -0300 (0:00:00.057)       0:02:30.716 ******* 
2026-10-13T21:01:14.5711849Z 
2026-10-13T21:01:14.5712357Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T21:01:14.5712513Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:14.5739016Z Tuesday 13 October 2026  18:01:14 -0300 (0:00:02.860)       0:02:33.577 ******* 
2026-10-13T21:01:16.1698072Z 
2026-10-13T21:01:16.1698595Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T21:01:16.1704676Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:01.336157", "end": "2026-10-13 18:01:16.150187", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:01:14.814030", "stderr": "aviso: /var/tmp/rpm-tmp.VHYGX6: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.VHYGX6: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:01:16.1705779Z ...ignoring
2026-10-13T21:01:16.1731468Z Tuesday 13 October 2026  18:01:16 -0300 (0:00:01.599)       0:02:35.176 ******* 
2026-10-13T21:01:18.0621084Z 
2026-10-13T21:01:18.0621594Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T21:01:18.0626649Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:01.512295", "end": "2026-10-13 18:01:18.039665", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:01:16.527370", "stderr": "aviso: /var/tmp/rpm-tmp.cVUCBc: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.cVUCBc: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:01:18.0627362Z ...ignoring
2026-10-13T21:01:18.0656152Z Tuesday 13 October 2026  18:01:18 -0300 (0:00:01.892)       0:02:37.068 ******* 
2026-10-13T21:01:18.3266710Z 
2026-10-13T21:01:18.3267376Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T21:01:18.3267606Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:18.3295509Z Tuesday 13 October 2026  18:01:18 -0300 (0:00:00.263)       0:02:37.332 ******* 
2026-10-13T21:01:18.5855941Z 
2026-10-13T21:01:18.5856445Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T21:01:18.5856609Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:18.5882983Z Tuesday 13 October 2026  18:01:18 -0300 (0:00:00.258)       0:02:37.591 ******* 
2026-10-13T21:01:19.2446750Z 
2026-10-13T21:01:19.2447266Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T21:01:19.2447435Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:19.2486129Z Tuesday 13 October 2026  18:01:19 -0300 (0:00:00.660)       0:02:38.251 ******* 
2026-10-13T21:01:19.5143273Z 
2026-10-13T21:01:19.5144178Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T21:01:19.5144374Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:19.5170543Z Tuesday 13 October 2026  18:01:19 -0300 (0:00:00.268)       0:02:38.520 ******* 
2026-10-13T21:01:29.9436483Z 
2026-10-13T21:01:29.9437013Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T21:01:29.9437179Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:29.9456731Z Tuesday 13 October 2026  18:01:29 -0300 (0:00:10.428)       0:02:48.948 ******* 
2026-10-13T21:01:30.2627591Z 
2026-10-13T21:01:30.2628110Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T21:01:30.2628271Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:30.2653986Z Tuesday 13 October 2026  18:01:30 -0300 (0:00:00.319)       0:02:49.268 ******* 
2026-10-13T21:01:30.3056262Z Tuesday 13 October 2026  18:01:30 -0300 (0:00:00.040)       0:02:49.308 ******* 
2026-10-13T21:01:30.3587709Z 
2026-10-13T21:01:30.3588186Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T21:01:30.3588345Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:30.3612192Z Tuesday 13 October 2026  18:01:30 -0300 (0:00:00.055)       0:02:49.364 ******* 
2026-10-13T21:01:30.4150656Z 
2026-10-13T21:01:30.4151132Z TASK [nfs : debug] *************************************************************
2026-10-13T21:01:30.4151316Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:01:30.4151434Z     "msg": {
2026-10-13T21:01:30.4151559Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T21:01:30.4151711Z         "NFS_MOUNT_POINT": "/eFinanceira_ctc/siexc"
2026-10-13T21:01:30.4151820Z     }
2026-10-13T21:01:30.4151914Z }
2026-10-13T21:01:30.4174958Z Tuesday 13 October 2026  18:01:30 -0300 (0:00:00.056)       0:02:49.420 ******* 
2026-10-13T21:01:30.4693611Z 
2026-10-13T21:01:30.4694047Z TASK [nfs : debug] *************************************************************
2026-10-13T21:01:30.4694228Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:01:30.4694364Z     "msg": "/eFinanceira_ctc/siexc"
2026-10-13T21:01:30.4694464Z }
2026-10-13T21:01:30.4718553Z Tuesday 13 October 2026  18:01:30 -0300 (0:00:00.054)       0:02:49.474 ******* 
2026-10-13T21:01:30.5247545Z 
2026-10-13T21:01:30.5247958Z TASK [nfs : debug] *************************************************************
2026-10-13T21:01:30.5248323Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:01:30.5248478Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC"
2026-10-13T21:01:30.5248874Z }
2026-10-13T21:01:30.5273565Z Tuesday 13 October 2026  18:01:30 -0300 (0:00:00.055)       0:02:49.530 ******* 
2026-10-13T21:01:30.5827827Z 
2026-10-13T21:01:30.5828450Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T21:01:30.5828998Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:01:30.5829194Z     "changed": false, 
2026-10-13T21:01:30.5829404Z     "msg": "All assertions passed"
2026-10-13T21:01:30.5829512Z }
2026-10-13T21:01:30.5851736Z Tuesday 13 October 2026  18:01:30 -0300 (0:00:00.057)       0:02:49.588 ******* 
2026-10-13T21:01:34.9324983Z 
2026-10-13T21:01:34.9325704Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T21:01:34.9325852Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:34.9353346Z Tuesday 13 October 2026  18:01:34 -0300 (0:00:04.350)       0:02:53.938 ******* 
2026-10-13T21:01:35.9390154Z 
2026-10-13T21:01:35.9390676Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T21:01:35.9394522Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.763346", "end": "2026-10-13 18:01:35.923799", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:01:35.160453", "stderr": "aviso: /var/tmp/rpm-tmp.LOXsQ9: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.LOXsQ9: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:01:35.9395598Z ...ignoring
2026-10-13T21:01:35.9421501Z Tuesday 13 October 2026  18:01:35 -0300 (0:00:01.006)       0:02:54.945 ******* 
2026-10-13T21:01:37.0414567Z 
2026-10-13T21:01:37.0415579Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T21:01:37.0419403Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.852813", "end": "2026-10-13 18:01:37.026355", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:01:36.173542", "stderr": "aviso: /var/tmp/rpm-tmp.96fqHE: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.96fqHE: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:01:37.0420292Z ...ignoring
2026-10-13T21:01:37.0447561Z Tuesday 13 October 2026  18:01:37 -0300 (0:00:01.102)       0:02:56.047 ******* 
2026-10-13T21:01:37.2881301Z 
2026-10-13T21:01:37.2882169Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T21:01:37.2882435Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:37.2911885Z Tuesday 13 October 2026  18:01:37 -0300 (0:00:00.246)       0:02:56.294 ******* 
2026-10-13T21:01:37.5373830Z 
2026-10-13T21:01:37.5374630Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T21:01:37.5374894Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:37.5402951Z Tuesday 13 October 2026  18:01:37 -0300 (0:00:00.249)       0:02:56.543 ******* 
2026-10-13T21:01:38.1782114Z 
2026-10-13T21:01:38.1782637Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T21:01:38.1782867Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:38.1821745Z Tuesday 13 October 2026  18:01:38 -0300 (0:00:00.641)       0:02:57.185 ******* 
2026-10-13T21:01:38.4398801Z 
2026-10-13T21:01:38.4399331Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T21:01:38.4399489Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:38.4428511Z Tuesday 13 October 2026  18:01:38 -0300 (0:00:00.260)       0:02:57.445 ******* 
2026-10-13T21:01:48.8604280Z 
2026-10-13T21:01:48.8605336Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T21:01:48.8605556Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:48.8633138Z Tuesday 13 October 2026  18:01:48 -0300 (0:00:10.420)       0:03:07.866 ******* 
2026-10-13T21:01:49.1672264Z 
2026-10-13T21:01:49.1673524Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T21:01:49.1674052Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:49.1700078Z Tuesday 13 October 2026  18:01:49 -0300 (0:00:00.306)       0:03:08.173 ******* 
2026-10-13T21:01:49.2139987Z Tuesday 13 October 2026  18:01:49 -0300 (0:00:00.043)       0:03:08.216 ******* 
2026-10-13T21:01:49.2690893Z 
2026-10-13T21:01:49.2691415Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T21:01:49.2691565Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:49.2714423Z Tuesday 13 October 2026  18:01:49 -0300 (0:00:00.057)       0:03:08.274 ******* 
2026-10-13T21:01:49.3246989Z 
2026-10-13T21:01:49.3247492Z TASK [nfs : debug] *************************************************************
2026-10-13T21:01:49.3247663Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:01:49.3247769Z     "msg": {
2026-10-13T21:01:49.3247893Z         "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T21:01:49.3248029Z         "NFS_MOUNT_POINT": "/SIEXC"
2026-10-13T21:01:49.3248424Z     }
2026-10-13T21:01:49.3248514Z }
2026-10-13T21:01:49.3273624Z Tuesday 13 October 2026  18:01:49 -0300 (0:00:00.055)       0:03:08.330 ******* 
2026-10-13T21:01:49.4069581Z 
2026-10-13T21:01:49.4070101Z TASK [nfs : debug] *************************************************************
2026-10-13T21:01:49.4070265Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:01:49.4070393Z     "msg": "/SIEXC"
2026-10-13T21:01:49.4070487Z }
2026-10-13T21:01:49.4096759Z Tuesday 13 October 2026  18:01:49 -0300 (0:00:00.082)       0:03:08.412 ******* 
2026-10-13T21:01:49.4693194Z 
2026-10-13T21:01:49.4694044Z TASK [nfs : debug] *************************************************************
2026-10-13T21:01:49.4694560Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:01:49.4694766Z     "msg": "192.168.227.59:/export/sicql_bovespa"
2026-10-13T21:01:49.4694928Z }
2026-10-13T21:01:49.4719509Z Tuesday 13 October 2026  18:01:49 -0300 (0:00:00.062)       0:03:08.475 ******* 
2026-10-13T21:01:49.5395136Z 
2026-10-13T21:01:49.5395616Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T21:01:49.5395893Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:01:49.5396164Z     "changed": false, 
2026-10-13T21:01:49.5396275Z     "msg": "All assertions passed"
2026-10-13T21:01:49.5396375Z }
2026-10-13T21:01:49.5421305Z Tuesday 13 October 2026  18:01:49 -0300 (0:00:00.070)       0:03:08.545 ******* 
2026-10-13T21:01:52.1376523Z 
2026-10-13T21:01:52.1377043Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T21:01:52.1377204Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:52.1403360Z Tuesday 13 October 2026  18:01:52 -0300 (0:00:02.598)       0:03:11.143 ******* 
2026-10-13T21:01:53.7283344Z 
2026-10-13T21:01:53.7283867Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T21:01:53.7289383Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:01.335061", "end": "2026-10-13 18:01:53.712773", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:01:52.377712", "stderr": "aviso: /var/tmp/rpm-tmp.z7iy16: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.z7iy16: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:01:53.7290264Z ...ignoring
2026-10-13T21:01:53.7315553Z Tuesday 13 October 2026  18:01:53 -0300 (0:00:01.591)       0:03:12.734 ******* 
2026-10-13T21:01:54.8867815Z 
2026-10-13T21:01:54.8868717Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T21:01:54.8872442Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.919839", "end": "2026-10-13 18:01:54.871879", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:01:53.952040", "stderr": "aviso: /var/tmp/rpm-tmp.0WcSjd: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.0WcSjd: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:01:54.8873319Z ...ignoring
2026-10-13T21:01:54.8902820Z Tuesday 13 October 2026  18:01:54 -0300 (0:00:01.158)       0:03:13.893 ******* 
2026-10-13T21:01:55.1414149Z 
2026-10-13T21:01:55.1414805Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T21:01:55.1415168Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:55.1442477Z Tuesday 13 October 2026  18:01:55 -0300 (0:00:00.254)       0:03:14.147 ******* 
2026-10-13T21:01:55.3817621Z 
2026-10-13T21:01:55.3818130Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T21:01:55.3818282Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:55.3844436Z Tuesday 13 October 2026  18:01:55 -0300 (0:00:00.240)       0:03:14.387 ******* 
2026-10-13T21:01:56.0040913Z 
2026-10-13T21:01:56.0041423Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T21:01:56.0041596Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:56.0079301Z Tuesday 13 October 2026  18:01:56 -0300 (0:00:00.623)       0:03:15.011 ******* 
2026-10-13T21:01:56.2731526Z 
2026-10-13T21:01:56.2732000Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T21:01:56.2732207Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:01:56.2761170Z Tuesday 13 October 2026  18:01:56 -0300 (0:00:00.268)       0:03:15.279 ******* 
2026-10-13T21:02:06.6926981Z 
2026-10-13T21:02:06.6927600Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T21:02:06.6927807Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:06.6956132Z Tuesday 13 October 2026  18:02:06 -0300 (0:00:10.419)       0:03:25.698 ******* 
2026-10-13T21:02:06.9900652Z 
2026-10-13T21:02:06.9901191Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T21:02:06.9901469Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:06.9928234Z Tuesday 13 October 2026  18:02:06 -0300 (0:00:00.297)       0:03:25.995 ******* 
2026-10-13T21:02:07.0339619Z Tuesday 13 October 2026  18:02:07 -0300 (0:00:00.040)       0:03:26.036 ******* 
2026-10-13T21:02:07.0893043Z 
2026-10-13T21:02:07.0893393Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T21:02:07.0893716Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:07.0918112Z Tuesday 13 October 2026  18:02:07 -0300 (0:00:00.058)       0:03:26.094 ******* 
2026-10-13T21:02:07.1458968Z 
2026-10-13T21:02:07.1459340Z TASK [nfs : debug] *************************************************************
2026-10-13T21:02:07.1460085Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:07.1460295Z     "msg": {
2026-10-13T21:02:07.1460430Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T21:02:07.1460574Z         "NFS_MOUNT_POINT": "/siexc"
2026-10-13T21:02:07.1460673Z     }
2026-10-13T21:02:07.1460761Z }
2026-10-13T21:02:07.1487956Z Tuesday 13 October 2026  18:02:07 -0300 (0:00:00.057)       0:03:26.151 ******* 
2026-10-13T21:02:07.2012484Z 
2026-10-13T21:02:07.2013082Z TASK [nfs : debug] *************************************************************
2026-10-13T21:02:07.2013298Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:07.2013481Z     "msg": "/siexc"
2026-10-13T21:02:07.2014510Z }
2026-10-13T21:02:07.2038668Z Tuesday 13 October 2026  18:02:07 -0300 (0:00:00.055)       0:03:26.207 ******* 
2026-10-13T21:02:07.2573350Z 
2026-10-13T21:02:07.2575279Z TASK [nfs : debug] *************************************************************
2026-10-13T21:02:07.2577156Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:07.2578469Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC"
2026-10-13T21:02:07.2579666Z }
2026-10-13T21:02:07.2599661Z Tuesday 13 October 2026  18:02:07 -0300 (0:00:00.056)       0:03:26.263 ******* 
2026-10-13T21:02:07.3155275Z 
2026-10-13T21:02:07.3156001Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T21:02:07.3156393Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:07.3156640Z     "changed": false, 
2026-10-13T21:02:07.3157052Z     "msg": "All assertions passed"
2026-10-13T21:02:07.3157210Z }
2026-10-13T21:02:07.3184734Z Tuesday 13 October 2026  18:02:07 -0300 (0:00:00.058)       0:03:26.321 ******* 
2026-10-13T21:02:09.8982928Z 
2026-10-13T21:02:09.8983807Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T21:02:09.8984110Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:09.9012929Z Tuesday 13 October 2026  18:02:09 -0300 (0:00:02.582)       0:03:28.904 ******* 
2026-10-13T21:02:11.8343002Z 
2026-10-13T21:02:11.8343534Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T21:02:11.8350888Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:01.691917", "end": "2026-10-13 18:02:11.818306", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:02:10.126389", "stderr": "aviso: /var/tmp/rpm-tmp.NUjOue: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.NUjOue: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:02:11.8351881Z ...ignoring
2026-10-13T21:02:11.8375174Z Tuesday 13 October 2026  18:02:11 -0300 (0:00:01.936)       0:03:30.840 ******* 
2026-10-13T21:02:12.9378819Z 
2026-10-13T21:02:12.9379614Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T21:02:12.9383938Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.862901", "end": "2026-10-13 18:02:12.922711", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:02:12.059810", "stderr": "aviso: /var/tmp/rpm-tmp.BqEheR: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.BqEheR: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:02:12.9384955Z ...ignoring
2026-10-13T21:02:12.9413365Z Tuesday 13 October 2026  18:02:12 -0300 (0:00:01.103)       0:03:31.944 ******* 
2026-10-13T21:02:13.1899789Z 
2026-10-13T21:02:13.1900770Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T21:02:13.1901096Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:13.1929061Z Tuesday 13 October 2026  18:02:13 -0300 (0:00:00.251)       0:03:32.196 ******* 
2026-10-13T21:02:13.4302244Z 
2026-10-13T21:02:13.4302992Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T21:02:13.4303299Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:13.4329531Z Tuesday 13 October 2026  18:02:13 -0300 (0:00:00.240)       0:03:32.436 ******* 
2026-10-13T21:02:14.0443096Z 
2026-10-13T21:02:14.0443809Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T21:02:14.0444092Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:14.0481978Z Tuesday 13 October 2026  18:02:14 -0300 (0:00:00.615)       0:03:33.051 ******* 
2026-10-13T21:02:14.3008383Z 
2026-10-13T21:02:14.3008897Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T21:02:14.3009066Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:14.3036232Z Tuesday 13 October 2026  18:02:14 -0300 (0:00:00.255)       0:03:33.306 ******* 
2026-10-13T21:02:24.7003952Z 
2026-10-13T21:02:24.7004462Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T21:02:24.7004626Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:24.7030788Z Tuesday 13 October 2026  18:02:24 -0300 (0:00:10.399)       0:03:43.706 ******* 
2026-10-13T21:02:25.0185819Z 
2026-10-13T21:02:25.0186340Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T21:02:25.0186503Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:25.0215267Z Tuesday 13 October 2026  18:02:25 -0300 (0:00:00.318)       0:03:44.024 ******* 
2026-10-13T21:02:25.0620651Z Tuesday 13 October 2026  18:02:25 -0300 (0:00:00.040)       0:03:44.064 ******* 
2026-10-13T21:02:25.1166881Z 
2026-10-13T21:02:25.1167408Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T21:02:25.1167592Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:25.1189335Z Tuesday 13 October 2026  18:02:25 -0300 (0:00:00.057)       0:03:44.122 ******* 
2026-10-13T21:02:25.1721393Z 
2026-10-13T21:02:25.1721827Z TASK [nfs : debug] *************************************************************
2026-10-13T21:02:25.1721993Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:25.1722112Z     "msg": {
2026-10-13T21:02:25.1722238Z         "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T21:02:25.1722373Z         "NFS_MOUNT_POINT": "/producao/SWIFT"
2026-10-13T21:02:25.1722475Z     }
2026-10-13T21:02:25.1722859Z }
2026-10-13T21:02:25.1746995Z Tuesday 13 October 2026  18:02:25 -0300 (0:00:00.055)       0:03:44.177 ******* 
2026-10-13T21:02:25.2291507Z 
2026-10-13T21:02:25.2291975Z TASK [nfs : debug] *************************************************************
2026-10-13T21:02:25.2292136Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:25.2293692Z     "msg": "/producao/SWIFT"
2026-10-13T21:02:25.2293824Z }
2026-10-13T21:02:25.2316537Z Tuesday 13 October 2026  18:02:25 -0300 (0:00:00.056)       0:03:44.234 ******* 
2026-10-13T21:02:25.2836311Z 
2026-10-13T21:02:25.2836769Z TASK [nfs : debug] *************************************************************
2026-10-13T21:02:25.2836927Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:25.2837067Z     "msg": "192.168.227.59:/export/sicql_bovespa"
2026-10-13T21:02:25.2837175Z }
2026-10-13T21:02:25.2861141Z Tuesday 13 October 2026  18:02:25 -0300 (0:00:00.054)       0:03:44.289 ******* 
2026-10-13T21:02:25.3437411Z 
2026-10-13T21:02:25.3438168Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T21:02:25.3438338Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:25.3438459Z     "changed": false, 
2026-10-13T21:02:25.3438571Z     "msg": "All assertions passed"
2026-10-13T21:02:25.3438668Z }
2026-10-13T21:02:25.3461535Z Tuesday 13 October 2026  18:02:25 -0300 (0:00:00.060)       0:03:44.349 ******* 
2026-10-13T21:02:27.9180377Z 
2026-10-13T21:02:27.9181088Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T21:02:27.9181423Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:27.9209040Z Tuesday 13 October 2026  18:02:27 -0300 (0:00:02.574)       0:03:46.924 ******* 
2026-10-13T21:02:28.8217841Z 
2026-10-13T21:02:28.8218551Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T21:02:28.8225638Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.661301", "end": "2026-10-13 18:02:28.806003", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:02:28.144702", "stderr": "aviso: /var/tmp/rpm-tmp.8YF01x: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.8YF01x: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:02:28.8226411Z ...ignoring
2026-10-13T21:02:28.8254860Z Tuesday 13 October 2026  18:02:28 -0300 (0:00:00.904)       0:03:47.828 ******* 
2026-10-13T21:02:29.7016886Z 
2026-10-13T21:02:29.7017396Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T21:02:29.7020846Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.635000", "end": "2026-10-13 18:02:29.686307", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:02:29.051307", "stderr": "aviso: /var/tmp/rpm-tmp.0zDHpM: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.0zDHpM: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:02:29.7021720Z ...ignoring
2026-10-13T21:02:29.7051388Z Tuesday 13 October 2026  18:02:29 -0300 (0:00:00.879)       0:03:48.708 ******* 
2026-10-13T21:02:29.9514063Z 
2026-10-13T21:02:29.9514644Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T21:02:29.9514810Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:29.9542647Z Tuesday 13 October 2026  18:02:29 -0300 (0:00:00.249)       0:03:48.957 ******* 
2026-10-13T21:02:30.1992442Z 
2026-10-13T21:02:30.1992893Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T21:02:30.1993053Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:30.2020774Z Tuesday 13 October 2026  18:02:30 -0300 (0:00:00.247)       0:03:49.205 ******* 
2026-10-13T21:02:30.8333402Z 
2026-10-13T21:02:30.8333971Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T21:02:30.8334263Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:30.8371628Z Tuesday 13 October 2026  18:02:30 -0300 (0:00:00.635)       0:03:49.840 ******* 
2026-10-13T21:02:31.0929238Z 
2026-10-13T21:02:31.0929745Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T21:02:31.0929909Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:31.0955416Z Tuesday 13 October 2026  18:02:31 -0300 (0:00:00.258)       0:03:50.098 ******* 
2026-10-13T21:02:41.5112107Z 
2026-10-13T21:02:41.5112716Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T21:02:41.5112938Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:41.5138027Z Tuesday 13 October 2026  18:02:41 -0300 (0:00:10.418)       0:04:00.516 ******* 
2026-10-13T21:02:41.8015135Z 
2026-10-13T21:02:41.8015608Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T21:02:41.8015821Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:41.8042517Z Tuesday 13 October 2026  18:02:41 -0300 (0:00:00.290)       0:04:00.807 ******* 
2026-10-13T21:02:41.8459228Z Tuesday 13 October 2026  18:02:41 -0300 (0:00:00.041)       0:04:00.848 ******* 
2026-10-13T21:02:41.9010006Z 
2026-10-13T21:02:41.9010408Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T21:02:41.9010574Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:41.9037354Z Tuesday 13 October 2026  18:02:41 -0300 (0:00:00.057)       0:04:00.906 ******* 
2026-10-13T21:02:41.9569735Z 
2026-10-13T21:02:41.9570265Z TASK [nfs : debug] *************************************************************
2026-10-13T21:02:41.9570480Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:41.9570588Z     "msg": {
2026-10-13T21:02:41.9570725Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T21:02:41.9570865Z         "NFS_MOUNT_POINT": "/suporte"
2026-10-13T21:02:41.9570963Z     }
2026-10-13T21:02:41.9571051Z }
2026-10-13T21:02:41.9595656Z Tuesday 13 October 2026  18:02:41 -0300 (0:00:00.055)       0:04:00.962 ******* 
2026-10-13T21:02:42.0140827Z 
2026-10-13T21:02:42.0141312Z TASK [nfs : debug] *************************************************************
2026-10-13T21:02:42.0141506Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:42.0141630Z     "msg": "/suporte"
2026-10-13T21:02:42.0141727Z }
2026-10-13T21:02:42.0166823Z Tuesday 13 October 2026  18:02:42 -0300 (0:00:00.057)       0:04:01.019 ******* 
2026-10-13T21:02:42.0712523Z 
2026-10-13T21:02:42.0713036Z TASK [nfs : debug] *************************************************************
2026-10-13T21:02:42.0713198Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:42.0713359Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC"
2026-10-13T21:02:42.0713482Z }
2026-10-13T21:02:42.0737841Z Tuesday 13 October 2026  18:02:42 -0300 (0:00:00.057)       0:04:01.076 ******* 
2026-10-13T21:02:42.1310054Z 
2026-10-13T21:02:42.1310701Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T21:02:42.1310947Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:42.1311148Z     "changed": false, 
2026-10-13T21:02:42.1311319Z     "msg": "All assertions passed"
2026-10-13T21:02:42.1311450Z }
2026-10-13T21:02:42.1334464Z Tuesday 13 October 2026  18:02:42 -0300 (0:00:00.059)       0:04:01.136 ******* 
2026-10-13T21:02:44.7467627Z 
2026-10-13T21:02:44.7468088Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T21:02:44.7468583Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:44.7493478Z Tuesday 13 October 2026  18:02:44 -0300 (0:00:02.615)       0:04:03.752 ******* 
2026-10-13T21:02:45.7842575Z 
2026-10-13T21:02:45.7843102Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T21:02:45.7847140Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.789059", "end": "2026-10-13 18:02:45.769485", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:02:44.980426", "stderr": "aviso: /var/tmp/rpm-tmp.OmGue6: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.OmGue6: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:02:45.7847738Z ...ignoring
2026-10-13T21:02:45.7875250Z Tuesday 13 October 2026  18:02:45 -0300 (0:00:01.038)       0:04:04.790 ******* 
2026-10-13T21:02:46.7092585Z 
2026-10-13T21:02:46.7093109Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T21:02:46.7097631Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.668134", "end": "2026-10-13 18:02:46.693155", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:02:46.025021", "stderr": "aviso: /var/tmp/rpm-tmp.q2gMy5: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.q2gMy5: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:02:46.7098544Z ...ignoring
2026-10-13T21:02:46.7133238Z Tuesday 13 October 2026  18:02:46 -0300 (0:00:00.925)       0:04:05.716 ******* 
2026-10-13T21:02:46.9569446Z 
2026-10-13T21:02:46.9570005Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T21:02:46.9570169Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:46.9596107Z Tuesday 13 October 2026  18:02:46 -0300 (0:00:00.246)       0:04:05.962 ******* 
2026-10-13T21:02:47.2111483Z 
2026-10-13T21:02:47.2112025Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T21:02:47.2112209Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:47.2140394Z Tuesday 13 October 2026  18:02:47 -0300 (0:00:00.254)       0:04:06.217 ******* 
2026-10-13T21:02:47.8317243Z 
2026-10-13T21:02:47.8317933Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T21:02:47.8318263Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:47.8382780Z Tuesday 13 October 2026  18:02:47 -0300 (0:00:00.624)       0:04:06.841 ******* 
2026-10-13T21:02:48.1050171Z 
2026-10-13T21:02:48.1050815Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T21:02:48.1051179Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:48.1077287Z Tuesday 13 October 2026  18:02:48 -0300 (0:00:00.269)       0:04:07.110 ******* 
2026-10-13T21:02:58.5056934Z 
2026-10-13T21:02:58.5057444Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T21:02:58.5057611Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:58.5081655Z Tuesday 13 October 2026  18:02:58 -0300 (0:00:10.400)       0:04:17.511 ******* 
2026-10-13T21:02:58.8918548Z 
2026-10-13T21:02:58.8919064Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T21:02:58.8919226Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:58.8945462Z Tuesday 13 October 2026  18:02:58 -0300 (0:00:00.386)       0:04:17.897 ******* 
2026-10-13T21:02:58.9362326Z Tuesday 13 October 2026  18:02:58 -0300 (0:00:00.041)       0:04:17.939 ******* 
2026-10-13T21:02:58.9946426Z 
2026-10-13T21:02:58.9946871Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T21:02:58.9947033Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:02:58.9969369Z Tuesday 13 October 2026  18:02:58 -0300 (0:00:00.060)       0:04:18.000 ******* 
2026-10-13T21:02:59.0514967Z 
2026-10-13T21:02:59.0515764Z TASK [nfs : debug] *************************************************************
2026-10-13T21:02:59.0515968Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:59.0516087Z     "msg": {
2026-10-13T21:02:59.0516210Z         "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T21:02:59.0516472Z         "NFS_MOUNT_POINT": "/producao"
2026-10-13T21:02:59.0516581Z     }
2026-10-13T21:02:59.0516668Z }
2026-10-13T21:02:59.0543611Z Tuesday 13 October 2026  18:02:59 -0300 (0:00:00.057)       0:04:18.057 ******* 
2026-10-13T21:02:59.1089552Z 
2026-10-13T21:02:59.1090103Z TASK [nfs : debug] *************************************************************
2026-10-13T21:02:59.1090275Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:59.1090736Z     "msg": "/producao"
2026-10-13T21:02:59.1090882Z }
2026-10-13T21:02:59.1117197Z Tuesday 13 October 2026  18:02:59 -0300 (0:00:00.057)       0:04:18.114 ******* 
2026-10-13T21:02:59.1684662Z 
2026-10-13T21:02:59.1685649Z TASK [nfs : debug] *************************************************************
2026-10-13T21:02:59.1686002Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:59.1686381Z     "msg": "192.168.227.59:/export/sicql_bovespa"
2026-10-13T21:02:59.1686545Z }
2026-10-13T21:02:59.1710472Z Tuesday 13 October 2026  18:02:59 -0300 (0:00:00.059)       0:04:18.174 ******* 
2026-10-13T21:02:59.2288317Z 
2026-10-13T21:02:59.2288822Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T21:02:59.2289285Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:02:59.2289417Z     "changed": false, 
2026-10-13T21:02:59.2289531Z     "msg": "All assertions passed"
2026-10-13T21:02:59.2289631Z }
2026-10-13T21:02:59.2314341Z Tuesday 13 October 2026  18:02:59 -0300 (0:00:00.060)       0:04:18.234 ******* 
2026-10-13T21:03:01.8440898Z 
2026-10-13T21:03:01.8441391Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T21:03:01.8441549Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:01.8468059Z Tuesday 13 October 2026  18:03:01 -0300 (0:00:02.615)       0:04:20.849 ******* 
2026-10-13T21:03:03.4435645Z 
2026-10-13T21:03:03.4436180Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T21:03:03.4440223Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:01.347807", "end": "2026-10-13 18:03:03.428298", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:03:02.080491", "stderr": "aviso: /var/tmp/rpm-tmp.4cMh05: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.4cMh05: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:03:03.4441132Z ...ignoring
2026-10-13T21:03:03.4467457Z Tuesday 13 October 2026  18:03:03 -0300 (0:00:01.599)       0:04:22.449 ******* 
2026-10-13T21:03:04.4181451Z 
2026-10-13T21:03:04.4181967Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T21:03:04.4186301Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.708469", "end": "2026-10-13 18:03:04.402698", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:03:03.694229", "stderr": "aviso: /var/tmp/rpm-tmp.tSIrl3: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.tSIrl3: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:03:04.4186935Z ...ignoring
2026-10-13T21:03:04.4217056Z Tuesday 13 October 2026  18:03:04 -0300 (0:00:00.974)       0:04:23.424 ******* 
2026-10-13T21:03:04.6661942Z 
2026-10-13T21:03:04.6663039Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T21:03:04.6663265Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:04.6694084Z Tuesday 13 October 2026  18:03:04 -0300 (0:00:00.247)       0:04:23.672 ******* 
2026-10-13T21:03:04.9190196Z 
2026-10-13T21:03:04.9190723Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T21:03:04.9191199Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:04.9219627Z Tuesday 13 October 2026  18:03:04 -0300 (0:00:00.252)       0:04:23.925 ******* 
2026-10-13T21:03:05.5473321Z 
2026-10-13T21:03:05.5473841Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T21:03:05.5473988Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:05.5513404Z Tuesday 13 October 2026  18:03:05 -0300 (0:00:00.629)       0:04:24.554 ******* 
2026-10-13T21:03:05.8131602Z 
2026-10-13T21:03:05.8132374Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T21:03:05.8132617Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:05.8158222Z Tuesday 13 October 2026  18:03:05 -0300 (0:00:00.264)       0:04:24.818 ******* 
2026-10-13T21:03:16.2108830Z 
2026-10-13T21:03:16.2109353Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T21:03:16.2109801Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:16.2134878Z Tuesday 13 October 2026  18:03:16 -0300 (0:00:10.397)       0:04:35.216 ******* 
2026-10-13T21:03:16.5037025Z 
2026-10-13T21:03:16.5037687Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T21:03:16.5037955Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:16.5065961Z Tuesday 13 October 2026  18:03:16 -0300 (0:00:00.293)       0:04:35.509 ******* 
2026-10-13T21:03:16.5505691Z Tuesday 13 October 2026  18:03:16 -0300 (0:00:00.043)       0:04:35.553 ******* 
2026-10-13T21:03:16.6046191Z 
2026-10-13T21:03:16.6046793Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T21:03:16.6047016Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:16.6073640Z Tuesday 13 October 2026  18:03:16 -0300 (0:00:00.056)       0:04:35.610 ******* 
2026-10-13T21:03:16.6622922Z 
2026-10-13T21:03:16.6623462Z TASK [nfs : debug] *************************************************************
2026-10-13T21:03:16.6623639Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:03:16.6623757Z     "msg": {
2026-10-13T21:03:16.6623867Z         "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T21:03:16.6624001Z         "NFS_MOUNT_POINT": "/SIEXC_SWIFT"
2026-10-13T21:03:16.6624105Z     }
2026-10-13T21:03:16.6627161Z }
2026-10-13T21:03:16.6648369Z Tuesday 13 October 2026  18:03:16 -0300 (0:00:00.057)       0:04:35.667 ******* 
2026-10-13T21:03:16.7183009Z 
2026-10-13T21:03:16.7183439Z TASK [nfs : debug] *************************************************************
2026-10-13T21:03:16.7183909Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:03:16.7184060Z     "msg": "/SIEXC_SWIFT"
2026-10-13T21:03:16.7184157Z }
2026-10-13T21:03:16.7208567Z Tuesday 13 October 2026  18:03:16 -0300 (0:00:00.055)       0:04:35.723 ******* 
2026-10-13T21:03:16.7754929Z 
2026-10-13T21:03:16.7755411Z TASK [nfs : debug] *************************************************************
2026-10-13T21:03:16.7756269Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:03:16.7756738Z     "msg": "192.168.227.59:/export/sicql_bovespa"
2026-10-13T21:03:16.7756917Z }
2026-10-13T21:03:16.7780341Z Tuesday 13 October 2026  18:03:16 -0300 (0:00:00.057)       0:04:35.781 ******* 
2026-10-13T21:03:16.8351864Z 
2026-10-13T21:03:16.8352371Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T21:03:16.8352553Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T21:03:16.8352678Z     "changed": false, 
2026-10-13T21:03:16.8352790Z     "msg": "All assertions passed"
2026-10-13T21:03:16.8352894Z }
2026-10-13T21:03:16.8376574Z Tuesday 13 October 2026  18:03:16 -0300 (0:00:00.059)       0:04:35.840 ******* 
2026-10-13T21:03:19.4758178Z 
2026-10-13T21:03:19.4758681Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T21:03:19.4759135Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:19.4786343Z Tuesday 13 October 2026  18:03:19 -0300 (0:00:02.640)       0:04:38.481 ******* 
2026-10-13T21:03:20.4562070Z 
2026-10-13T21:03:20.4562583Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T21:03:20.4566981Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.731235", "end": "2026-10-13 18:03:20.441326", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:03:19.710091", "stderr": "aviso: /var/tmp/rpm-tmp.tq1sfb: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.tq1sfb: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:03:20.4567872Z ...ignoring
2026-10-13T21:03:20.4594173Z Tuesday 13 October 2026  18:03:20 -0300 (0:00:00.980)       0:04:39.462 ******* 
2026-10-13T21:03:21.5077048Z 
2026-10-13T21:03:21.5077704Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T21:03:21.5081519Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.790691", "end": "2026-10-13 18:03:21.491747", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 18:03:20.701056", "stderr": "aviso: /var/tmp/rpm-tmp.7AQ4Wx: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.7AQ4Wx: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T21:03:21.5082153Z ...ignoring
2026-10-13T21:03:21.5110691Z Tuesday 13 October 2026  18:03:21 -0300 (0:00:01.051)       0:04:40.514 ******* 
2026-10-13T21:03:21.7632637Z 
2026-10-13T21:03:21.7633677Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T21:03:21.7633895Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:21.7660588Z Tuesday 13 October 2026  18:03:21 -0300 (0:00:00.254)       0:04:40.769 ******* 
2026-10-13T21:03:22.0211036Z 
2026-10-13T21:03:22.0211733Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T21:03:22.0211936Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:22.0238037Z Tuesday 13 October 2026  18:03:22 -0300 (0:00:00.257)       0:04:41.026 ******* 
2026-10-13T21:03:22.6507962Z 
2026-10-13T21:03:22.6508459Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T21:03:22.6508747Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:22.6545542Z Tuesday 13 October 2026  18:03:22 -0300 (0:00:00.630)       0:04:41.657 ******* 
2026-10-13T21:03:22.9163923Z 
2026-10-13T21:03:22.9164431Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T21:03:22.9165676Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:22.9193409Z Tuesday 13 October 2026  18:03:22 -0300 (0:00:00.264)       0:04:41.922 ******* 
2026-10-13T21:03:33.3277732Z 
2026-10-13T21:03:33.3278242Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T21:03:33.3278405Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:33.3308171Z Tuesday 13 October 2026  18:03:33 -0300 (0:00:10.411)       0:04:52.333 ******* 
2026-10-13T21:03:33.6073242Z 
2026-10-13T21:03:33.6073743Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T21:03:33.6073910Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:33.6106303Z Tuesday 13 October 2026  18:03:33 -0300 (0:00:00.279)       0:04:52.613 ******* 
2026-10-13T21:03:33.6536992Z 
2026-10-13T21:03:33.6537254Z PLAY [jboss] *******************************************************************
2026-10-13T21:03:33.6579552Z 
2026-10-13T21:03:33.6579941Z PLAY [jboss] *******************************************************************
2026-10-13T21:03:33.6612923Z Tuesday 13 October 2026  18:03:33 -0300 (0:00:00.050)       0:04:52.664 ******* 
2026-10-13T21:03:34.2886437Z 
2026-10-13T21:03:34.2886965Z TASK [Gathering Facts] *********************************************************
2026-10-13T21:03:34.2887130Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:34.3094385Z Tuesday 13 October 2026  18:03:34 -0300 (0:00:00.648)       0:04:53.312 ******* 
2026-10-13T21:03:35.6775651Z 
2026-10-13T21:03:35.6776293Z TASK [Gerando fatos de servicos] ***********************************************
2026-10-13T21:03:35.6776535Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:35.7118845Z Tuesday 13 October 2026  18:03:35 -0300 (0:00:01.402)       0:04:54.714 ******* 
2026-10-13T21:03:35.7709321Z 
2026-10-13T21:03:35.7710031Z TASK [Gerando lista de units jboss] ********************************************
2026-10-13T21:03:35.7710260Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:35.7988985Z Tuesday 13 October 2026  18:03:35 -0300 (0:00:00.086)       0:04:54.801 ******* 
2026-10-13T21:03:35.8660274Z Tuesday 13 October 2026  18:03:35 -0300 (0:00:00.067)       0:04:54.869 ******* 
2026-10-13T21:03:35.8762375Z 
2026-10-13T21:03:35.8762619Z PLAY [Copiando deployments adicionais] *****************************************
2026-10-13T21:03:35.9066033Z Tuesday 13 October 2026  18:03:35 -0300 (0:00:00.040)       0:04:54.909 ******* 
2026-10-13T21:03:35.9607633Z 
2026-10-13T21:03:35.9608531Z TASK [Cria variável build_repository_name] *************************************
2026-10-13T21:03:35.9608755Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:35.9884329Z Tuesday 13 October 2026  18:03:35 -0300 (0:00:00.081)       0:04:54.991 ******* 
2026-10-13T21:03:36.0421987Z 
2026-10-13T21:03:36.0422490Z TASK [Buscando diretorio de config] ********************************************
2026-10-13T21:03:36.0422805Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:36.0699923Z Tuesday 13 October 2026  18:03:36 -0300 (0:00:00.081)       0:04:55.072 ******* 
2026-10-13T21:03:36.1224107Z 
2026-10-13T21:03:36.1224676Z TASK [Buscando diretorio de config] ********************************************
2026-10-13T21:03:36.1224947Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:36.1570343Z Tuesday 13 October 2026  18:03:36 -0300 (0:00:00.087)       0:04:55.160 ******* 
2026-10-13T21:03:36.6463706Z 
2026-10-13T21:03:36.6464220Z TASK [Create a symbolic link] **************************************************
2026-10-13T21:03:36.6464638Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config)
2026-10-13T21:03:36.9252639Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T21:03:36.9581750Z Tuesday 13 October 2026  18:03:36 -0300 (0:00:00.800)       0:04:55.960 ******* 
2026-10-13T21:03:37.2792961Z 
2026-10-13T21:03:37.2793597Z TASK [Verifica se o arquivo  existe] *******************************************
2026-10-13T21:03:37.2794063Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config)
2026-10-13T21:03:37.5460272Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T21:03:37.5753701Z Tuesday 13 October 2026  18:03:37 -0300 (0:00:00.617)       0:04:56.578 ******* 
2026-10-13T21:03:37.6678728Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/jboss/tasks/stack_deployments_custom_block.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T21:03:37.6975954Z Tuesday 13 October 2026  18:03:37 -0300 (0:00:00.122)       0:04:56.700 ******* 
2026-10-13T21:03:38.1391401Z 
2026-10-13T21:03:38.1392190Z TASK [Lendo artefatos do arquivo CSV] ******************************************
2026-10-13T21:03:38.1392455Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:38.1708846Z Tuesday 13 October 2026  18:03:38 -0300 (0:00:00.473)       0:04:57.173 ******* 
2026-10-13T21:03:38.1786674Z [WARNING]: The loop variable 'item' is already in use. You should set the
2026-10-13T21:03:38.1786909Z `loop_var` value in the `loop_control` option for the task to something else to
2026-10-13T21:03:38.1787061Z avoid variable collisions and unexpected behavior.
2026-10-13T21:03:38.2157947Z 
2026-10-13T21:03:38.2158373Z TASK [Mostra artefatos] ********************************************************
2026-10-13T21:03:38.2158882Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'7.0.1.12', u'group_id': u'com.ibm.wmq', u'extension': u'rar', u'artifact_id': u'wmq.jmsra'}) => {
2026-10-13T21:03:38.2159114Z     "msg": "Artefato: wmq.jmsra - versao 7.0.1.12"
2026-10-13T21:03:38.2159228Z }
2026-10-13T21:03:38.2450977Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'0.0.2', u'group_id': u'br.com.treesolution', u'extension': u'war', u'artifact_id': u'exc_web'}) => {
2026-10-13T21:03:38.2451259Z     "msg": "Artefato: exc_web - versao 0.0.2"
2026-10-13T21:03:38.2451370Z }
2026-10-13T21:03:38.2783775Z Tuesday 13 October 2026  18:03:38 -0300 (0:00:00.107)       0:04:57.281 ******* 
2026-10-13T21:03:38.8954525Z 
2026-10-13T21:03:38.8955346Z TASK [maven_artifact] **********************************************************
2026-10-13T21:03:38.8955955Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'7.0.1.12', u'group_id': u'com.ibm.wmq', u'extension': u'rar', u'artifact_id': u'wmq.jmsra'})
2026-10-13T21:03:39.2601661Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'0.0.2', u'group_id': u'br.com.treesolution', u'extension': u'war', u'artifact_id': u'exc_web'})
2026-10-13T21:03:39.3127847Z Tuesday 13 October 2026  18:03:39 -0300 (0:00:01.034)       0:04:58.315 ******* 
2026-10-13T21:03:40.8647026Z 
2026-10-13T21:03:40.8647872Z TASK [Copiando artefatos para o(s) servidor(es) Jboss] *************************
2026-10-13T21:03:40.8648083Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:40.8933373Z Tuesday 13 October 2026  18:03:40 -0300 (0:00:01.580)       0:04:59.896 ******* 
2026-10-13T21:03:40.9336907Z 
2026-10-13T21:03:40.9337645Z PLAY [Copiando modules adicionais] *********************************************
2026-10-13T21:03:40.9633972Z Tuesday 13 October 2026  18:03:40 -0300 (0:00:00.070)       0:04:59.966 ******* 
2026-10-13T21:03:41.0175117Z 
2026-10-13T21:03:41.0175738Z TASK [Cria variável build_repository_name] *************************************
2026-10-13T21:03:41.0175910Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:41.0450657Z Tuesday 13 October 2026  18:03:41 -0300 (0:00:00.081)       0:05:00.048 ******* 
2026-10-13T21:03:41.0990580Z 
2026-10-13T21:03:41.0990925Z TASK [Buscando diretorio de config] ********************************************
2026-10-13T21:03:41.0991307Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:41.1275145Z Tuesday 13 October 2026  18:03:41 -0300 (0:00:00.082)       0:05:00.130 ******* 
2026-10-13T21:03:41.1804055Z 
2026-10-13T21:03:41.1804527Z TASK [Buscando diretorio de config] ********************************************
2026-10-13T21:03:41.1804693Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:41.2121782Z Tuesday 13 October 2026  18:03:41 -0300 (0:00:00.084)       0:05:00.215 ******* 
2026-10-13T21:03:41.5229351Z 
2026-10-13T21:03:41.5229864Z TASK [Create a directory] ******************************************************
2026-10-13T21:03:41.5230280Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config)
2026-10-13T21:03:41.7920159Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T21:03:41.8248368Z Tuesday 13 October 2026  18:03:41 -0300 (0:00:00.612)       0:05:00.827 ******* 
2026-10-13T21:03:42.1264810Z 
2026-10-13T21:03:42.1265467Z TASK [Verifica se o arquivo  existe] *******************************************
2026-10-13T21:03:42.1265947Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config)
2026-10-13T21:03:42.3935131Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T21:03:42.4314171Z Tuesday 13 October 2026  18:03:42 -0300 (0:00:00.606)       0:05:01.434 ******* 
2026-10-13T21:03:42.5269005Z included: /opt/ads-agent/_work/r17882/a/esteira-jboss-vm-v2/roles/jboss/tasks/stack_modules_custom_block.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T21:03:42.5581182Z Tuesday 13 October 2026  18:03:42 -0300 (0:00:00.126)       0:05:01.561 ******* 
2026-10-13T21:03:42.9033692Z 
2026-10-13T21:03:42.9034139Z TASK [Lendo artefatos do arquivo CSV] ******************************************
2026-10-13T21:03:42.9034362Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:42.9371529Z Tuesday 13 October 2026  18:03:42 -0300 (0:00:00.379)       0:05:01.940 ******* 
2026-10-13T21:03:42.9472632Z [WARNING]: The loop variable 'item' is already in use. You should set the
2026-10-13T21:03:42.9472829Z `loop_var` value in the `loop_control` option for the task to something else to
2026-10-13T21:03:42.9472987Z avoid variable collisions and unexpected behavior.
2026-10-13T21:03:42.9855964Z 
2026-10-13T21:03:42.9856322Z TASK [Mostra lista de artefatos] ***********************************************
2026-10-13T21:03:42.9856730Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.6.redhat-6', u'group_id': u'commons-pool', u'extension': u'xml', u'artifact_id': u'commons-pool'}) => {
2026-10-13T21:03:42.9856983Z     "msg": "Artefato: commons-pool - versao 1.6.redhat-6"
2026-10-13T21:03:42.9857181Z }
2026-10-13T21:03:43.0172036Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.6.redhat-6', u'group_id': u'commons-pool', u'extension': u'jar', u'artifact_id': u'commons-pool'}) => {
2026-10-13T21:03:43.0172401Z     "msg": "Artefato: commons-pool - versao 1.6.redhat-6"
2026-10-13T21:03:43.0172521Z }
2026-10-13T21:03:43.0482550Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'42.7.7', u'group_id': u'org.postgres', u'extension': u'jar', u'artifact_id': u'postgresql'}) => {
2026-10-13T21:03:43.0482849Z     "msg": "Artefato: postgresql - versao 42.7.7"
2026-10-13T21:03:43.0482963Z }
2026-10-13T21:03:43.0777810Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'19.3.0.0', u'group_id': u'com.oracle.ojdbc', u'extension': u'jar', u'artifact_id': u'ojdbc8'}) => {
2026-10-13T21:03:43.0778126Z     "msg": "Artefato: ojdbc8 - versao 19.3.0.0"
2026-10-13T21:03:43.0778227Z }
2026-10-13T21:03:43.1075619Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.1', u'group_id': u'org.apache.commons.jexl', u'extension': u'jar', u'artifact_id': u'commons-jexl'}) => {
2026-10-13T21:03:43.1076186Z     "msg": "Artefato: commons-jexl - versao 1.1"
2026-10-13T21:03:43.1076300Z }
2026-10-13T21:03:43.1378998Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.2.5', u'group_id': u'net.sourceforge', u'extension': u'jar', u'artifact_id': u'jtds'}) => {
2026-10-13T21:03:43.1379286Z     "msg": "Artefato: jtds - versao 1.2.5"
2026-10-13T21:03:43.1379409Z }
2026-10-13T21:03:43.1679632Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.3.1', u'group_id': u'net.sourceforge', u'extension': u'jar', u'artifact_id': u'jtds'}) => {
2026-10-13T21:03:43.1680031Z     "msg": "Artefato: jtds - versao 1.3.1"
2026-10-13T21:03:43.1680172Z }
2026-10-13T21:03:43.1983969Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.0.0', u'group_id': u'br.com.treebpm', u'extension': u'jar', u'artifact_id': u'treebpm'}) => {
2026-10-13T21:03:43.1984354Z     "msg": "Artefato: treebpm - versao 1.0.0"
2026-10-13T21:03:43.1984775Z }
2026-10-13T21:03:43.2277583Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.0.0', u'group_id': u'br.com.concepting.framework', u'extension': u'jar', u'artifact_id': u'concepting-framework'}) => {
2026-10-13T21:03:43.2277898Z     "msg": "Artefato: concepting-framework - versao 3.0.0"
2026-10-13T21:03:43.2278020Z }
2026-10-13T21:03:43.2594277Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'2.2', u'group_id': u'cglib', u'extension': u'jar', u'artifact_id': u'cglib-nodep'}) => {
2026-10-13T21:03:43.2594566Z     "msg": "Artefato: cglib-nodep - versao 2.2"
2026-10-13T21:03:43.2594720Z }
2026-10-13T21:03:43.2899369Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.4.1', u'group_id': u'javax.mail', u'extension': u'jar', u'artifact_id': u'mail'}) => {
2026-10-13T21:03:43.2899682Z     "msg": "Artefato: mail - versao 1.4.1"
2026-10-13T21:03:43.2899793Z }
2026-10-13T21:03:43.3196178Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.10.1', u'group_id': u'org.apache.poi', u'extension': u'jar', u'artifact_id': u'poi'}) => {
2026-10-13T21:03:43.3196487Z     "msg": "Artefato: poi - versao 3.10.1"
2026-10-13T21:03:43.3196596Z }
2026-10-13T21:03:43.3501728Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.10.1', u'group_id': u'org.apache.poi', u'extension': u'jar', u'artifact_id': u'poi-ooxml'}) => {
2026-10-13T21:03:43.3501994Z     "msg": "Artefato: poi-ooxml - versao 3.10.1"
2026-10-13T21:03:43.3502091Z }
2026-10-13T21:03:43.3797368Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.10.1', u'group_id': u'org.apache.poi', u'extension': u'jar', u'artifact_id': u'poi-ooxml-schemas'}) => {
2026-10-13T21:03:43.3797650Z     "msg": "Artefato: poi-ooxml-schemas - versao 3.10.1"
2026-10-13T21:03:43.3797765Z }
2026-10-13T21:03:43.4104093Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'2.6.0', u'group_id': u'org.apache.xmlbeans', u'extension': u'jar', u'artifact_id': u'xmlbeans'}) => {
2026-10-13T21:03:43.4104390Z     "msg": "Artefato: xmlbeans - versao 2.6.0"
2026-10-13T21:03:43.4104498Z }
2026-10-13T21:03:43.4428080Z Tuesday 13 October 2026  18:03:43 -0300 (0:00:00.505)       0:05:02.445 ******* 
2026-10-13T21:03:43.7962193Z 
2026-10-13T21:03:43.7962898Z TASK [Listar arquivos no diretório baixados anteriormente] *********************
2026-10-13T21:03:43.7963069Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:43.8288497Z Tuesday 13 October 2026  18:03:43 -0300 (0:00:00.386)       0:05:02.831 ******* 
2026-10-13T21:03:43.8686322Z [WARNING]: conditional statements should not include jinja2 templating
2026-10-13T21:03:43.8686694Z delimiters such as {{ }} or {% %}. Found: '{{ inner_item.artifact_id }}-{{
2026-10-13T21:03:43.8686915Z inner_item.version }}.{{ inner_item.extension|default('jar',true) }}' not in
2026-10-13T21:03:43.8687133Z files_found.files | map(attribute='path') | map('basename') | list
2026-10-13T21:03:44.2167973Z 
2026-10-13T21:03:44.2168368Z TASK [maven_artifact] **********************************************************
2026-10-13T21:03:44.2169062Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.6.redhat-6', u'group_id': u'commons-pool', u'extension': u'xml', u'artifact_id': u'commons-pool'})
2026-10-13T21:03:45.2640469Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.6.redhat-6', u'group_id': u'commons-pool', u'extension': u'jar', u'artifact_id': u'commons-pool'})
2026-10-13T21:03:45.6547556Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'42.7.7', u'group_id': u'org.postgres', u'extension': u'jar', u'artifact_id': u'postgresql'})
2026-10-13T21:03:46.0316049Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'19.3.0.0', u'group_id': u'com.oracle.ojdbc', u'extension': u'jar', u'artifact_id': u'ojdbc8'})
2026-10-13T21:03:46.3951133Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.1', u'group_id': u'org.apache.commons.jexl', u'extension': u'jar', u'artifact_id': u'commons-jexl'})
2026-10-13T21:03:49.7998659Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.2.5', u'group_id': u'net.sourceforge', u'extension': u'jar', u'artifact_id': u'jtds'})
2026-10-13T21:03:50.1663631Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.3.1', u'group_id': u'net.sourceforge', u'extension': u'jar', u'artifact_id': u'jtds'})
2026-10-13T21:03:50.5206495Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.0.0', u'group_id': u'br.com.treebpm', u'extension': u'jar', u'artifact_id': u'treebpm'})
2026-10-13T21:03:50.8792385Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.0.0', u'group_id': u'br.com.concepting.framework', u'extension': u'jar', u'artifact_id': u'concepting-framework'})
2026-10-13T21:03:51.2431296Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'2.2', u'group_id': u'cglib', u'extension': u'jar', u'artifact_id': u'cglib-nodep'})
2026-10-13T21:03:51.6189776Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.4.1', u'group_id': u'javax.mail', u'extension': u'jar', u'artifact_id': u'mail'})
2026-10-13T21:03:52.0007884Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.10.1', u'group_id': u'org.apache.poi', u'extension': u'jar', u'artifact_id': u'poi'})
2026-10-13T21:03:52.3787187Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.10.1', u'group_id': u'org.apache.poi', u'extension': u'jar', u'artifact_id': u'poi-ooxml'})
2026-10-13T21:03:52.7982711Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.10.1', u'group_id': u'org.apache.poi', u'extension': u'jar', u'artifact_id': u'poi-ooxml-schemas'})
2026-10-13T21:03:53.1640431Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'2.6.0', u'group_id': u'org.apache.xmlbeans', u'extension': u'jar', u'artifact_id': u'xmlbeans'})
2026-10-13T21:03:53.2053188Z Tuesday 13 October 2026  18:03:53 -0300 (0:00:09.376)       0:05:12.208 ******* 
2026-10-13T21:03:53.5198695Z 
2026-10-13T21:03:53.5199566Z TASK [Verifica se o arquivo jboss-modules-custom tem conteudo] *****************
2026-10-13T21:03:53.5199875Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:03:53.5489420Z Tuesday 13 October 2026  18:03:53 -0300 (0:00:00.343)       0:05:12.551 ******* 
2026-10-13T21:04:01.2470101Z 
2026-10-13T21:04:01.2470637Z TASK [Copiando artefatos (Modules) para o(s) servidor(es) Jboss] ***************
2026-10-13T21:04:01.2470800Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:04:01.2774419Z Tuesday 13 October 2026  18:04:01 -0300 (0:00:07.728)       0:05:20.280 ******* 
2026-10-13T21:04:01.9368357Z 
2026-10-13T21:04:01.9369305Z TASK [Copiando artefato (jboss-custom.cli) para o(s) servidor(es) Jboss] *******
2026-10-13T21:04:01.9369612Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:04:01.9673411Z Tuesday 13 October 2026  18:04:01 -0300 (0:00:00.689)       0:05:20.970 ******* 
2026-10-13T21:04:09.2309933Z 
2026-10-13T21:04:09.2310753Z TASK [Executando o jboss-custom.cli] *******************************************
2026-10-13T21:04:09.2310966Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:04:09.2591951Z Tuesday 13 October 2026  18:04:09 -0300 (0:00:07.292)       0:05:28.262 ******* 
2026-10-13T21:04:11.2100884Z 
2026-10-13T21:04:11.2101403Z TASK [Encontrar todos os arquivos module.xml] **********************************
2026-10-13T21:04:11.2101564Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:04:11.5845391Z Tuesday 13 October 2026  18:04:11 -0300 (0:00:02.325)       0:05:30.587 ******* 
2026-10-13T21:04:12.9545706Z 
2026-10-13T21:04:12.9546683Z TASK [Filtrar arquivos dentro da pasta system na raiz] *************************
2026-10-13T21:04:12.9547263Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:04:13.2101038Z Tuesday 13 October 2026  18:04:13 -0300 (0:00:01.625)       0:05:32.212 ******* 
2026-10-13T21:04:13.5944567Z 
2026-10-13T21:04:13.5945884Z TASK [Filtrar arquivos fora da pasta system na raiz] ***************************
2026-10-13T21:04:13.5946182Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:04:13.6235356Z Tuesday 13 October 2026  18:04:13 -0300 (0:00:00.413)       0:05:32.626 ******* 
2026-10-13T21:04:13.6655636Z Tuesday 13 October 2026  18:04:13 -0300 (0:00:00.041)       0:05:32.668 ******* 
2026-10-13T21:04:13.7237161Z 
2026-10-13T21:04:13.7237657Z PLAY [jboss] *******************************************************************
2026-10-13T21:04:13.7540775Z Tuesday 13 October 2026  18:04:13 -0300 (0:00:00.088)       0:05:32.756 ******* 
2026-10-13T21:04:13.8144350Z 
2026-10-13T21:04:13.8145656Z TASK [Setando a versão do Jboss] ***********************************************
2026-10-13T21:04:13.8145876Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:04:13.8429967Z Tuesday 13 October 2026  18:04:13 -0300 (0:00:00.088)       0:05:32.845 ******* 
2026-10-13T21:04:13.9005225Z 
2026-10-13T21:04:13.9006402Z TASK [Cria variável build_repository_name_tfs] *********************************
2026-10-13T21:04:13.9006669Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:04:13.9307890Z Tuesday 13 October 2026  18:04:13 -0300 (0:00:00.087)       0:05:32.933 ******* 
2026-10-13T21:04:13.9856996Z 
2026-10-13T21:04:13.9857462Z TASK [Buscando diretorio de config] ********************************************
2026-10-13T21:04:13.9857637Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:04:14.0146578Z Tuesday 13 October 2026  18:04:14 -0300 (0:00:00.083)       0:05:33.017 ******* 
2026-10-13T21:04:14.5800487Z 
2026-10-13T21:04:14.5801389Z TASK [Copy common_start.sh] ****************************************************
2026-10-13T21:04:14.5801684Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:04:14.6090882Z Tuesday 13 October 2026  18:04:14 -0300 (0:00:00.594)       0:05:33.611 ******* 
2026-10-13T21:04:15.2368560Z 
2026-10-13T21:04:15.2369484Z TASK [Copy template script] ****************************************************
2026-10-13T21:04:15.2369719Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:04:15.2650033Z Tuesday 13 October 2026  18:04:15 -0300 (0:00:00.655)       0:05:34.267 ******* 
2026-10-13T21:04:15.8898353Z 
2026-10-13T21:04:15.8898981Z TASK [JBoss systemd wrapper for sysvinit script mode domain] *******************
2026-10-13T21:04:15.8899244Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:04:15.9181422Z Tuesday 13 October 2026  18:04:15 -0300 (0:00:00.653)       0:05:34.921 ******* 
2026-10-13T21:04:16.6653661Z 
2026-10-13T21:04:16.6654287Z TASK [Realiza copia do arquivo de Trust Store] *********************************
2026-10-13T21:04:16.6654459Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:04:16.6941079Z Tuesday 13 October 2026  18:04:16 -0300 (0:00:00.775)       0:05:35.696 ******* 
2026-10-13T21:04:16.7649244Z Tuesday 13 October 2026  18:04:16 -0300 (0:00:00.070)       0:05:35.767 ******* 
2026-10-13T21:04:16.8489638Z Tuesday 13 October 2026  18:04:16 -0300 (0:00:00.084)       0:05:35.851 ******* 
2026-10-13T21:04:17.1693766Z 
2026-10-13T21:04:17.1694276Z TASK [Check directory configuration exists] ************************************
2026-10-13T21:04:17.1694687Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config)
2026-10-13T21:04:17.4274055Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T21:04:17.4573031Z Tuesday 13 October 2026  18:04:17 -0300 (0:00:00.608)       0:05:36.460 ******* 
2026-10-13T21:04:50.5591160Z 
2026-10-13T21:04:50.5593192Z TASK [Copiando arquivos para jboss.server.config.dir] **************************
2026-10-13T21:04:50.5594807Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config', u'stat': {u'charset': u'binary', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1791924959.1024294, u'block_size': 4096, u'inode': 171973428, u'isgid': False, u'size': 102, u'wgrp': False, u'executable': True, u'isuid': False, u'readable': True, u'isreg': False, u'version': u'806874357', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'inode/directory', u'blocks': 0, u'xoth': True, u'islnk': False, u'nlink': 5, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/configuration', u'xusr': True, u'atime': 1791924963.035372, u'isdir': True, u'ctime': 1791924959.1024294, u'isblk': False, u'xgrp': True, u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0755', u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/configuration', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-13T21:04:50.5975364Z Tuesday 13 October 2026  18:04:50 -0300 (0:00:33.140)       0:06:09.600 ******* 
2026-10-13T21:04:50.8958830Z 
2026-10-13T21:04:50.8959681Z TASK [Get standalone-full-ha.xml status] ***************************************
2026-10-13T21:04:50.8959968Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config)
2026-10-13T21:04:51.1622579Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T21:04:51.1933549Z Tuesday 13 October 2026  18:04:51 -0300 (0:00:00.595)       0:06:10.196 ******* 
2026-10-13T21:04:51.8497420Z 
2026-10-13T21:04:51.8498066Z TASK [Copiando arquivo standalone-full-ha.xml] *********************************
2026-10-13T21:04:51.8501623Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/jboss', u'stat': {u'charset': u'us-ascii', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1791924963.0643716, u'block_size': 4096, u'inode': 230692010, u'isgid': False, u'size': 53658, u'wgrp': False, u'executable': False, u'isuid': False, u'readable': True, u'isreg': True, u'version': u'2141205865', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'application/xml', u'blocks': 112, u'xoth': False, u'islnk': False, u'nlink': 1, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/jboss/standalone-full-ha.xml', u'xusr': False, u'atime': 1791924963.987358, u'isdir': False, u'ctime': 1791924963.0643716, u'isblk': False, u'checksum': u'068865c141f587f59187503ef73ad9fe4fe8fb3e', u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0644', u'xgrp': False, u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/jboss/standalone-full-ha.xml', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-13T21:04:51.8873595Z Tuesday 13 October 2026  18:04:51 -0300 (0:00:00.694)       0:06:10.890 ******* 
2026-10-13T21:04:52.1846307Z 
2026-10-13T21:04:52.1847253Z TASK [Get standalone-ha.xml status] ********************************************
2026-10-13T21:04:52.1847757Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config)
2026-10-13T21:04:52.4373228Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T21:04:52.4670226Z Tuesday 13 October 2026  18:04:52 -0300 (0:00:00.579)       0:06:11.470 ******* 
2026-10-13T21:04:52.5475488Z Tuesday 13 October 2026  18:04:52 -0300 (0:00:00.079)       0:06:11.549 ******* 
2026-10-13T21:04:52.8427735Z 
2026-10-13T21:04:52.8428202Z TASK [Get standalone.xml status] ***********************************************
2026-10-13T21:04:52.8428737Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config)
2026-10-13T21:04:53.0960533Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T21:04:53.1279627Z Tuesday 13 October 2026  18:04:53 -0300 (0:00:00.580)       0:06:12.130 ******* 
2026-10-13T21:04:53.2097992Z Tuesday 13 October 2026  18:04:53 -0300 (0:00:00.081)       0:06:12.212 ******* 
2026-10-13T21:04:53.5087937Z 
2026-10-13T21:04:53.5088459Z TASK [Get standalone.conf status] **********************************************
2026-10-13T21:04:53.5088861Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config)
2026-10-13T21:04:53.7752497Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T21:04:53.8047786Z Tuesday 13 October 2026  18:04:53 -0300 (0:00:00.595)       0:06:12.807 ******* 
2026-10-13T21:04:54.4506258Z 
2026-10-13T21:04:54.4506725Z TASK [Copiando arquivo standalone.conf] ****************************************
2026-10-13T21:04:54.4508392Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/jboss', u'stat': {u'charset': u'us-ascii', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1791924963.0723715, u'block_size': 4096, u'inode': 230692011, u'isgid': False, u'size': 4820, u'wgrp': False, u'executable': False, u'isuid': False, u'readable': True, u'isreg': True, u'version': u'516679102', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'text/plain', u'blocks': 16, u'xoth': False, u'islnk': False, u'nlink': 1, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/jboss/standalone.conf', u'xusr': False, u'atime': 1791924963.0713716, u'isdir': False, u'ctime': 1791924963.0723715, u'isblk': False, u'checksum': u'c8ab4145a3767cb7fbb7957a7732cf1973517f8e', u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0644', u'xgrp': False, u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/jboss/standalone.conf', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-13T21:04:54.4818459Z Tuesday 13 October 2026  18:04:54 -0300 (0:00:00.676)       0:06:13.484 ******* 
2026-10-13T21:04:54.8165823Z 
2026-10-13T21:04:54.8166340Z TASK [Restart Zabbix] **********************************************************
2026-10-13T21:04:54.8167046Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "msg": "Could not find the requested service zabbix-agent: host"}
2026-10-13T21:04:54.8167209Z ...ignoring
2026-10-13T21:04:54.8452035Z Tuesday 13 October 2026  18:04:54 -0300 (0:00:00.363)       0:06:13.848 ******* 
2026-10-13T21:04:54.9120344Z Tuesday 13 October 2026  18:04:54 -0300 (0:00:00.066)       0:06:13.914 ******* 
2026-10-13T21:04:54.9446540Z [WARNING]: conditional statements should not include jinja2 templating
2026-10-13T21:04:54.9446890Z delimiters such as {{ }} or {% %}. Found: {{ lookup('env','HSM') |
2026-10-13T21:04:54.9447065Z default('false', true) | bool }}
2026-10-13T21:04:54.9529250Z Tuesday 13 October 2026  18:04:54 -0300 (0:00:00.040)       0:06:13.955 ******* 
2026-10-13T21:05:01.7337313Z 
2026-10-13T21:05:01.7337844Z RUNNING HANDLER [Restart Jboss] ************************************************
2026-10-13T21:05:01.7338012Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:05:01.7377666Z 
2026-10-13T21:05:01.7379952Z PLAY [jboss] *******************************************************************
2026-10-13T21:05:01.7419254Z 
2026-10-13T21:05:01.7419536Z PLAY [jboss] *******************************************************************
2026-10-13T21:05:01.7448769Z 
2026-10-13T21:05:01.7448971Z PLAY [jboss] *******************************************************************
2026-10-13T21:05:01.7741611Z Tuesday 13 October 2026  18:05:01 -0300 (0:00:06.821)       0:06:20.777 ******* 
2026-10-13T21:05:01.8472451Z 
2026-10-13T21:05:01.8473169Z TASK [Cria variável build_repository_name] *************************************
2026-10-13T21:05:01.8473334Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:05:01.8763294Z Tuesday 13 October 2026  18:05:01 -0300 (0:00:00.101)       0:06:20.879 ******* 
2026-10-13T21:05:01.9323731Z 
2026-10-13T21:05:01.9324226Z TASK [Buscando diretorio de config] ********************************************
2026-10-13T21:05:01.9324384Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:05:02.0221936Z Tuesday 13 October 2026  18:05:02 -0300 (0:00:00.145)       0:06:21.025 ******* 
2026-10-13T21:05:02.3555231Z 
2026-10-13T21:05:02.3555966Z TASK [Verifica se o arquivo {{ item }}/etc/hosts-{{ sistema_ambiente }} existe] ***
2026-10-13T21:05:02.3556252Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config)
2026-10-13T21:05:02.6198465Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r17882/a/_SIEXC-web-aplicacao-config/so)
2026-10-13T21:05:02.6510407Z Tuesday 13 October 2026  18:05:02 -0300 (0:00:00.628)       0:06:21.653 ******* 
2026-10-13T21:05:02.7042644Z 
2026-10-13T21:05:02.7043388Z PLAY [jboss] *******************************************************************
2026-10-13T21:05:02.7353965Z Tuesday 13 October 2026  18:05:02 -0300 (0:00:00.084)       0:06:21.738 ******* 
2026-10-13T21:05:03.1601026Z 
2026-10-13T21:05:03.1602216Z TASK [Verifica se o arquivo /opt/jboss-eap/standalone/configuration/custom.sh existe] ***
2026-10-13T21:05:03.1602488Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:05:03.1891506Z Tuesday 13 October 2026  18:05:03 -0300 (0:00:00.453)       0:06:22.192 ******* 
2026-10-13T21:05:10.3499047Z 
2026-10-13T21:05:10.3499566Z TASK [Executa shell customizada (jboss_home)] **********************************
2026-10-13T21:05:10.3499731Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:05:10.3823321Z Tuesday 13 October 2026  18:05:10 -0300 (0:00:07.193)       0:06:29.385 ******* 
2026-10-13T21:05:10.7155811Z 
2026-10-13T21:05:10.7156313Z TASK [Verifica se o arquivo /opt/batch/config/configuration/custom.sh existe] ***
2026-10-13T21:05:10.7156485Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T21:05:10.7451131Z Tuesday 13 October 2026  18:05:10 -0300 (0:00:00.362)       0:06:29.748 ******* 
2026-10-13T21:05:10.7863370Z 
2026-10-13T21:05:10.7864288Z PLAY [local] *******************************************************************
2026-10-13T21:05:10.7889808Z [WARNING]: Could not match supplied host pattern, ignoring: instance_restart
2026-10-13T21:05:10.7890261Z 
2026-10-13T21:05:10.7890401Z PLAY [instance_restart] ********************************************************
2026-10-13T21:05:10.7890549Z skipping: no hosts matched
2026-10-13T21:05:10.7893414Z [WARNING]: Could not match supplied host pattern, ignoring: machine_reboot
2026-10-13T21:05:10.7896477Z 
2026-10-13T21:05:10.7896608Z PLAY [machine_reboot] **********************************************************
2026-10-13T21:05:10.7896749Z skipping: no hosts matched
2026-10-13T21:05:10.7916888Z 
2026-10-13T21:05:10.7917209Z PLAY [local] *******************************************************************
2026-10-13T21:05:10.7939169Z [WARNING]: Could not match supplied host pattern, ignoring: instance_stop
2026-10-13T21:05:10.7941712Z 
2026-10-13T21:05:10.7941979Z PLAY [instance_stop] ***********************************************************
2026-10-13T21:05:10.7942142Z skipping: no hosts matched
2026-10-13T21:05:10.7945131Z 
2026-10-13T21:05:10.7945351Z PLAY [machine_reboot] **********************************************************
2026-10-13T21:05:10.7945496Z skipping: no hosts matched
2026-10-13T21:05:10.7953422Z 
2026-10-13T21:05:10.7953567Z PLAY [local] *******************************************************************
2026-10-13T21:05:10.7975419Z [WARNING]: Could not match supplied host pattern, ignoring: escopo_execucao
2026-10-13T21:05:10.7978146Z 
2026-10-13T21:05:10.7978379Z PLAY [Executar o Start do Sirot Connector no escopo definido] ******************
2026-10-13T21:05:10.7978529Z skipping: no hosts matched
2026-10-13T21:05:10.7984421Z 
2026-10-13T21:05:10.7984645Z PLAY [local] *******************************************************************
2026-10-13T21:05:10.8008610Z 
2026-10-13T21:05:10.8008836Z PLAY [Executar o Stop do Sirot Connector] **************************************
2026-10-13T21:05:10.8008974Z skipping: no hosts matched
2026-10-13T21:05:10.8015624Z 
2026-10-13T21:05:10.8015993Z PLAY [Configura TSM] ***********************************************************
2026-10-13T21:05:10.8041156Z 
2026-10-13T21:05:10.8041396Z PLAY [jboss] *******************************************************************
2026-10-13T21:05:10.8068009Z 
2026-10-13T21:05:10.8068455Z PLAY [Configura Control-M] *****************************************************
2026-10-13T21:05:10.8102150Z 
2026-10-13T21:05:10.8102393Z PLAY [jboss] *******************************************************************
2026-10-13T21:05:10.8143218Z 
2026-10-13T21:05:10.8143528Z PLAY [jboss] *******************************************************************
2026-10-13T21:05:10.8184538Z 
2026-10-13T21:05:10.8184740Z PLAY [jboss] *******************************************************************
2026-10-13T21:05:10.8207904Z 
2026-10-13T21:05:10.8208124Z PLAY [jboss] *******************************************************************
2026-10-13T21:05:10.8237255Z 
2026-10-13T21:05:10.8237510Z PLAY [localhost] ***************************************************************
2026-10-13T21:05:10.8260961Z 
2026-10-13T21:05:10.8261167Z PLAY [jboss] *******************************************************************
2026-10-13T21:05:10.8303059Z 
2026-10-13T21:05:10.8303304Z PLAY [jboss] *******************************************************************
2026-10-13T21:05:10.8341372Z 
2026-10-13T21:05:10.8341521Z PLAY [jboss] *******************************************************************
2026-10-13T21:05:10.8378487Z 
2026-10-13T21:05:10.8378888Z PLAY RECAP *********************************************************************
2026-10-13T21:05:10.8379097Z caddeapllx2193.agil.nprd.caixa.gov.br : ok=276  changed=116  unreachable=0    failed=0    skipped=27   rescued=0    ignored=27  
2026-10-13T21:05:10.8379188Z 
2026-10-13T21:05:10.8380854Z Tuesday 13 October 2026  18:05:10 -0300 (0:00:00.092)       0:06:29.841 ******* 
2026-10-13T21:05:10.8381077Z =============================================================================== 
2026-10-13T21:05:10.8386450Z Copiando arquivos para jboss.server.config.dir ------------------------- 33.14s
2026-10-13T21:05:10.8386686Z nfs : execute montagem script ------------------------------------------ 32.01s
2026-10-13T21:05:10.8386903Z nfs : Networker | Restart networker ------------------------------------ 10.46s
2026-10-13T21:05:10.8387127Z nfs : Networker | Restart networker ------------------------------------ 10.44s
2026-10-13T21:05:10.8387358Z nfs : Networker | Restart networker ------------------------------------ 10.44s
2026-10-13T21:05:10.8387571Z nfs : Networker | Restart networker ------------------------------------ 10.43s
2026-10-13T21:05:10.8387787Z nfs : Networker | Restart networker ------------------------------------ 10.42s
2026-10-13T21:05:10.8388000Z nfs : Networker | Restart networker ------------------------------------ 10.42s
2026-10-13T21:05:10.8388210Z nfs : Networker | Restart networker ------------------------------------ 10.42s
2026-10-13T21:05:10.8388420Z nfs : Networker | Restart networker ------------------------------------ 10.42s
2026-10-13T21:05:10.8388707Z nfs : Networker | Restart networker ------------------------------------ 10.41s
2026-10-13T21:05:10.8389228Z nfs : Networker | Restart networker ------------------------------------ 10.41s
2026-10-13T21:05:10.8389448Z nfs : Networker | Restart networker ------------------------------------ 10.41s
2026-10-13T21:05:10.8389667Z nfs : Networker | Restart networker ------------------------------------ 10.40s
2026-10-13T21:05:10.8389880Z nfs : Networker | Restart networker ------------------------------------ 10.40s
2026-10-13T21:05:10.8390090Z nfs : Networker | Restart networker ------------------------------------ 10.40s
2026-10-13T21:05:10.8390306Z maven_artifact ---------------------------------------------------------- 9.38s
2026-10-13T21:05:10.8390528Z Copiando artefatos (Modules) para o(s) servidor(es) Jboss --------------- 7.73s
2026-10-13T21:05:10.8390744Z Executando o jboss-custom.cli ------------------------------------------- 7.29s
2026-10-13T21:05:10.8390964Z Executa shell customizada (jboss_home) ---------------------------------- 7.19s
2026-10-13T21:05:10.8391102Z Playbook run took 0 days, 0 hours, 6 minutes, 29 seconds
2026-10-13T21:05:10.9052658Z ##[debug]Exit code 0 received from tool '/bin/bash'
2026-10-13T21:05:10.9054208Z ##[debug]STDIO streams have closed for tool '/bin/bash'
2026-10-13T21:05:10.9064290Z ##[debug]task result: Succeeded
2026-10-13T21:05:10.9067069Z ##[debug]Processed: ##vso[task.complete result=Succeeded;done=true;]
2026-10-13T21:05:10.9094049Z ##[section]Finishing: Deploy Config no JBOSS

