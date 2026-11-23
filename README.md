Por favor, verificar e ajustar

Repositório: SIMPI-batch-log-auditoria

Erro para gerar a release

Erro  no passo: Cadastrar Servidor no Satellite

Link da release:
https://devops.caixa/projetos/Caixa/_releaseProgress?_a=release-pipeline-progress&releaseId=559336

Impacto: STRY00174869 



2026-11-20T14:21:20.8797003Z ##[section]Starting: Cadastrar Servidor no Satellite
2026-11-20T14:21:20.8800340Z ==============================================================================
2026-11-20T14:21:20.8800419Z Task         : Bash
2026-11-20T14:21:20.8800475Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-11-20T14:21:20.8800541Z Version      : 3.227.0
2026-11-20T14:21:20.8800594Z Author       : Microsoft Corporation
2026-11-20T14:21:20.8800646Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-11-20T14:21:20.8800720Z ==============================================================================
2026-11-20T14:21:21.0157507Z Generating script.
2026-11-20T14:21:21.0168681Z ========================== Starting Command Output ===========================
2026-11-20T14:21:21.0176096Z [command]/bin/bash /opt/ads-agent/_work/_temp/63ed7bae-7ed0-4421-90fc-0264bf7d0d65.sh
2026-11-20T14:21:21.0235456Z ++ echo _SIMPI-batch-log-auditoria
2026-11-20T14:21:21.0236948Z ++ sed s/_//
2026-11-20T14:21:21.0248969Z + REPO=SIMPI-batch-log-auditoria
2026-11-20T14:21:21.0257211Z ++ tf_var_quant
2026-11-20T14:21:21.0257507Z /opt/ads-agent/_work/_temp/63ed7bae-7ed0-4421-90fc-0264bf7d0d65.sh: line 4: tf_var_quant: comando não encontrado
2026-11-20T14:21:21.0258219Z + ansible-playbook /opt/ads-agent/_work/r19600/a/esteira-jboss-vm-v2/site.yml --tags satellite -e sistema_ambiente=des -e sistema_nome=simpi-batch-log-auditoria -e site=ctc_nprd -e quantidade_vm= -e centralizadora_operacoes=7259 -e centralizadora_desenvolvimento=5088 -e default_working_directory_tfs=/opt/ads-agent/_work/r19600/a -e build_repository_name_tfs=SIMPI-batch-log-auditoria
2026-11-20T14:21:23.3178446Z 
2026-11-20T14:21:23.3178986Z PLAY [local] *******************************************************************
2026-11-20T14:21:23.3473301Z 
2026-11-20T14:21:23.3473724Z PLAY [Configurando o DNS] ******************************************************
2026-11-20T14:21:23.5387816Z 
2026-11-20T14:21:23.5388738Z PLAY [local] *******************************************************************
2026-11-20T14:21:23.5424044Z 
2026-11-20T14:21:23.5424446Z PLAY [Verificando serviços] ****************************************************
2026-11-20T14:21:23.5519175Z 
2026-11-20T14:21:23.5519510Z PLAY [Configuração LDAP] *******************************************************
2026-11-20T14:21:23.5564392Z [WARNING]: Found variable using reserved name: when
2026-11-20T14:21:23.5570229Z 
2026-11-20T14:21:23.5570407Z PLAY [jboss] *******************************************************************
2026-11-20T14:21:23.5940206Z 
2026-11-20T14:21:23.5940729Z PLAY [Stack Jboss] *************************************************************
2026-11-20T14:21:23.6178103Z Friday 20 November 2026  11:21:23 -0300 (0:00:00.360)       0:00:00.360 ******* 
2026-11-20T14:21:24.0705523Z 
2026-11-20T14:21:24.0706257Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-11-20T14:21:24.0706908Z ok: [caddeapllx1668.agil.nprd.caixa.gov.br]
2026-11-20T14:21:24.0731170Z 
2026-11-20T14:21:24.0731652Z PLAY [jboss] *******************************************************************
2026-11-20T14:21:24.0783001Z 
2026-11-20T14:21:24.0783306Z PLAY [jboss] *******************************************************************
2026-11-20T14:21:24.0835161Z 
2026-11-20T14:21:24.0836240Z PLAY [jboss] *******************************************************************
2026-11-20T14:21:24.0867065Z 
2026-11-20T14:21:24.0867592Z PLAY [Copiando deployments adicionais] *****************************************
2026-11-20T14:21:24.0893387Z 
2026-11-20T14:21:24.0893677Z PLAY [Copiando modules adicionais] *********************************************
2026-11-20T14:21:24.0922766Z 
2026-11-20T14:21:24.0923534Z PLAY [jboss] *******************************************************************
2026-11-20T14:21:24.0959497Z 
2026-11-20T14:21:24.0960117Z PLAY [jboss] *******************************************************************
2026-11-20T14:21:24.1001072Z 
2026-11-20T14:21:24.1001752Z PLAY [jboss] *******************************************************************
2026-11-20T14:21:24.1046893Z 
2026-11-20T14:21:24.1047350Z PLAY [jboss] *******************************************************************
2026-11-20T14:21:24.1074628Z 
2026-11-20T14:21:24.1074906Z PLAY [jboss] *******************************************************************
2026-11-20T14:21:24.1107289Z 
2026-11-20T14:21:24.1107541Z PLAY [local] *******************************************************************
2026-11-20T14:21:24.1135637Z [WARNING]: Could not match supplied host pattern, ignoring: instance_restart
2026-11-20T14:21:24.1138426Z 
2026-11-20T14:21:24.1139081Z PLAY [instance_restart] ********************************************************
2026-11-20T14:21:24.1139279Z skipping: no hosts matched
2026-11-20T14:21:24.1144694Z [WARNING]: Could not match supplied host pattern, ignoring: machine_reboot
2026-11-20T14:21:24.1147760Z 
2026-11-20T14:21:24.1147958Z PLAY [machine_reboot] **********************************************************
2026-11-20T14:21:24.1148747Z skipping: no hosts matched
2026-11-20T14:21:24.1157519Z 
2026-11-20T14:21:24.1157677Z PLAY [local] *******************************************************************
2026-11-20T14:21:24.1182316Z [WARNING]: Could not match supplied host pattern, ignoring: instance_stop
2026-11-20T14:21:24.1185320Z 
2026-11-20T14:21:24.1185710Z PLAY [instance_stop] ***********************************************************
2026-11-20T14:21:24.1185955Z skipping: no hosts matched
2026-11-20T14:21:24.1188478Z 
2026-11-20T14:21:24.1188789Z PLAY [machine_reboot] **********************************************************
2026-11-20T14:21:24.1188951Z skipping: no hosts matched
2026-11-20T14:21:24.1196939Z 
2026-11-20T14:21:24.1197147Z PLAY [local] *******************************************************************
2026-11-20T14:21:24.1221288Z [WARNING]: Could not match supplied host pattern, ignoring: escopo_execucao
2026-11-20T14:21:24.1224211Z 
2026-11-20T14:21:24.1224474Z PLAY [Executar o Start do Sirot Connector no escopo definido] ******************
2026-11-20T14:21:24.1224638Z skipping: no hosts matched
2026-11-20T14:21:24.1230047Z 
2026-11-20T14:21:24.1230204Z PLAY [local] *******************************************************************
2026-11-20T14:21:24.1255204Z 
2026-11-20T14:21:24.1255439Z PLAY [Executar o Stop do Sirot Connector] **************************************
2026-11-20T14:21:24.1255591Z skipping: no hosts matched
2026-11-20T14:21:24.1262188Z 
2026-11-20T14:21:24.1262409Z PLAY [Configura TSM] ***********************************************************
2026-11-20T14:21:24.1287937Z 
2026-11-20T14:21:24.1288089Z PLAY [jboss] *******************************************************************
2026-11-20T14:21:24.1316313Z 
2026-11-20T14:21:24.1316924Z PLAY [Configura Control-M] *****************************************************
2026-11-20T14:21:24.1352852Z 
2026-11-20T14:21:24.1353049Z PLAY [jboss] *******************************************************************
2026-11-20T14:21:24.1409274Z Friday 20 November 2026  11:21:24 -0300 (0:00:00.523)       0:00:00.883 ******* 
2026-11-20T14:21:25.2158805Z 
2026-11-20T14:21:25.2159308Z TASK [Gathering Facts] *********************************************************
2026-11-20T14:21:25.2159582Z ok: [caddeapllx1668.agil.nprd.caixa.gov.br]
2026-11-20T14:21:25.2517471Z Friday 20 November 2026  11:21:25 -0300 (0:00:01.110)       0:00:01.993 ******* 
2026-11-20T14:21:26.1312935Z 
2026-11-20T14:21:26.1313976Z TASK [satellite : Executar comando subscription-manager status] ****************
2026-11-20T14:21:26.1314297Z changed: [caddeapllx1668.agil.nprd.caixa.gov.br]
2026-11-20T14:21:26.1569940Z Friday 20 November 2026  11:21:26 -0300 (0:00:00.905)       0:00:02.899 ******* 
2026-11-20T14:21:26.2144545Z 
2026-11-20T14:21:26.2146262Z TASK [satellite : set_fact] ****************************************************
2026-11-20T14:21:26.2147040Z ok: [caddeapllx1668.agil.nprd.caixa.gov.br]
2026-11-20T14:21:26.2296049Z Friday 20 November 2026  11:21:26 -0300 (0:00:00.072)       0:00:02.971 ******* 
2026-11-20T14:21:26.2900053Z 
2026-11-20T14:21:26.2900612Z TASK [satellite : Extrair valor do status] *************************************
2026-11-20T14:21:26.2900795Z ok: [caddeapllx1668.agil.nprd.caixa.gov.br]
2026-11-20T14:21:26.3056055Z Friday 20 November 2026  11:21:26 -0300 (0:00:00.076)       0:00:03.047 ******* 
2026-11-20T14:21:26.3658557Z 
2026-11-20T14:21:26.3659104Z TASK [satellite : Exibir o valor do status] ************************************
2026-11-20T14:21:26.3660415Z ok: [caddeapllx1668.agil.nprd.caixa.gov.br] => {
2026-11-20T14:21:26.3660549Z     "msg": [
2026-11-20T14:21:26.3661362Z         "É preciso registrar: False", 
2026-11-20T14:21:26.3661526Z         "", 
2026-11-20T14:21:26.3661626Z         {
2026-11-20T14:21:26.3661726Z             "changed": true, 
2026-11-20T14:21:26.3661920Z             "cmd": "subscription-manager identity", 
2026-11-20T14:21:26.3662094Z             "delta": "0:00:00.482893", 
2026-11-20T14:21:26.3662320Z             "end": "2026-11-20 11:21:26.114661", 
2026-11-20T14:21:26.3662459Z             "failed": false, 
2026-11-20T14:21:26.3662567Z             "rc": 0, 
2026-11-20T14:21:26.3662741Z             "start": "2026-11-20 11:21:25.631768", 
2026-11-20T14:21:26.3662855Z             "stderr": "", 
2026-11-20T14:21:26.3662965Z             "stderr_lines": [], 
2026-11-20T14:21:26.3663381Z             "stdout": "identidade do sistema: d2b94552-8357-4a64-9f1b-3e8542f1c988\nnome: caddeapllx1668\nnome da org: CEF\norg ID: CEF\nnome do ambiente: PRD/CV-RHEL-7", 
2026-11-20T14:21:26.3663571Z             "stdout_lines": [
2026-11-20T14:21:26.3663777Z                 "identidade do sistema: d2b94552-8357-4a64-9f1b-3e8542f1c988", 
2026-11-20T14:21:26.3663920Z                 "nome: caddeapllx1668", 
2026-11-20T14:21:26.3664037Z                 "nome da org: CEF", 
2026-11-20T14:21:26.3664151Z                 "org ID: CEF", 
2026-11-20T14:21:26.3665865Z                 "nome do ambiente: PRD/CV-RHEL-7"
2026-11-20T14:21:26.3666042Z             ]
2026-11-20T14:21:26.3666153Z         }
2026-11-20T14:21:26.3666251Z     ]
2026-11-20T14:21:26.3666344Z }
2026-11-20T14:21:26.3823765Z Friday 20 November 2026  11:21:26 -0300 (0:00:00.076)       0:00:03.124 ******* 
2026-11-20T14:21:26.4351032Z Friday 20 November 2026  11:21:26 -0300 (0:00:00.052)       0:00:03.177 ******* 
2026-11-20T14:21:26.4877035Z Friday 20 November 2026  11:21:26 -0300 (0:00:00.052)       0:00:03.229 ******* 
2026-11-20T14:21:29.4958367Z 
2026-11-20T14:21:29.4959126Z TASK [satellite : Execute subscription-manager repos Zabbix] *******************
2026-11-20T14:21:29.4960041Z fatal: [caddeapllx1668.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": "subscription-manager repos --enable=CEF_Zabbix_Zabbix_6_REDHAT_7", "delta": "0:00:02.736893", "end": "2026-11-20 11:21:29.481671", "msg": "non-zero return code", "rc": 1, "start": "2026-11-20 11:21:26.744778", "stderr": "", "stderr_lines": [], "stdout": "Erro: 'CEF_Zabbix_Zabbix_6_REDHAT_7' não corresponde a um ID de repositório válido. Use \"subscription-manager repos --list\" para ver os repositórios válidos.", "stdout_lines": ["Erro: 'CEF_Zabbix_Zabbix_6_REDHAT_7' não corresponde a um ID de repositório válido. Use \"subscription-manager repos --list\" para ver os repositórios válidos."]}
2026-11-20T14:21:29.4966639Z 
2026-11-20T14:21:29.4967017Z PLAY RECAP *********************************************************************
2026-11-20T14:21:29.4967215Z caddeapllx1668.agil.nprd.caixa.gov.br : ok=6    changed=1    unreachable=0    failed=1    skipped=2    rescued=0    ignored=0   
2026-11-20T14:21:29.4967321Z 
2026-11-20T14:21:29.4967999Z Friday 20 November 2026  11:21:29 -0300 (0:00:03.009)       0:00:06.239 ******* 
2026-11-20T14:21:29.4968265Z =============================================================================== 
2026-11-20T14:21:29.4969059Z satellite : Execute subscription-manager repos Zabbix ------------------- 3.01s
2026-11-20T14:21:29.4969459Z Gathering Facts --------------------------------------------------------- 1.11s
2026-11-20T14:21:29.4970053Z satellite : Executar comando subscription-manager status ---------------- 0.91s
2026-11-20T14:21:29.4970366Z Verifica ser o Jboss já foi instalado ----------------------------------- 0.52s
2026-11-20T14:21:29.4970602Z satellite : Exibir o valor do status ------------------------------------ 0.08s
2026-11-20T14:21:29.4970833Z satellite : Extrair valor do status ------------------------------------- 0.08s
2026-11-20T14:21:29.4971135Z satellite : set_fact ---------------------------------------------------- 0.07s
2026-11-20T14:21:29.4971367Z satellite : Download RegistraSatellite-v5.sh ---------------------------- 0.05s
2026-11-20T14:21:29.4971592Z satellite : Execute RegistraSatellite-v5.sh ----------------------------- 0.05s
2026-11-20T14:21:29.4971749Z Playbook run took 0 days, 0 hours, 0 minutes, 6 seconds
2026-11-20T14:21:29.5644276Z ##[error]Bash exited with code '2'.
2026-11-20T14:21:29.5663761Z ##[section]Finishing: Cadastrar Servidor no Satellite




Creating home directory for p585600.
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ sudo subscription-manager clean

Presumimos que você recebeu as instruções de sempre do administrador
de sistema local. Basicamente, resume-se a estas três coisas:

    #1) Respeite a privacidade dos outros.
    #2) Pense antes de digitar.
    #3) Com grandes poderes vêm grandes responsabilidades.

[sudo] senha para p585600:
Todos os dados removidos
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$


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
SIMPI-batch-log-auditoria
/
SIMPI-batch-log-auditoria-0.0.1-SNAPSHOT(12)
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
SIMPI-batch-log-auditoria

SIMPI-batch-log-auditoria-0.0.1-SNAPSHOT(12)
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
Agent job
Started: 23/11/2026, 10:09:19
Pool:
Release-Linux
·
Agent: cadsvaprlx212.intra.caixa.gov.br

4m 4s

Initialize job
·
succeeded
<1s

Download Artifacts
·
succeeded
2 warnings
3s

Recupera VEC
·
succeeded
1s

VEC - Aferição
·
succeeded
1 warning

<1s

Exportar variáveis NFS
·
succeeded
1s

Exportar variáveis Infrafácil
·
succeeded
1s

Alocando o IP (AlocaIP e Infradevops)
·
succeeded
22s

Exporta as variáveis para o Terraform
·
succeeded
<1s

Replace tokens in **/*.tfvars.json **/*.tf
·
succeeded
1s

Remove caracteres
·
succeeded
<1s

Install Terraform 1.3.5
·
succeeded
3s

Terraform init
·
succeeded
8s

Terraform validate
·
succeeded
1s

Terraform workspace
·
succeeded
1s

Terraform destroy
·
succeeded
<1s

Terraform apply
·
succeeded
18s

Definir size como executado
·
succeeded
17s

Cadastrar Servidor no Satellite
·
succeeded
50s

Valida Variáveis Obrigatórias
·
succeeded
<1s

Recuperando URL Pacote Nexus
·
succeeded
2s

Recupera Pacote
·
succeeded
1s

Convertendo Minúsculo e Definindo nome do Projeto/Repositório
·
succeeded
<1s

Corrigindo Codificação Arquivos dos2unix
·
succeeded
1s

Alterando Valores placeholders nos arquivos de config
·
succeeded
<1s

Git clone https://devops.caixa/projetos/Infraestrutura/_git/esteira-logs
·
succeeded
1s

Cria Streams Graylog
·
succeeded
4s

Configura Control-M
·
succeeded
43s

Arquivos de Configuração
·
succeeded
29s

Deploy Pacote
·
succeeded
11s

Secure Files
·
succeeded
8s

Finalize Job
·
succeeded
<1s
Row 2

Showing 26 deployments

Row 2

Showing 26 deployments

Row 3

Row 2


