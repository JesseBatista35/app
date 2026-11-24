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
SIGEC-CSC
/
SIGEC-CSC-1012
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
SIGEC-CSC

SIGEC-CSC-1012


EC TQS

Partially succeeded


Pipeline

Tasks

Variables

Logs

Tests
Agent job
Started: 19/11/2026, 13:42:36
Pool:
Release-Linux
·
Agent: cadsvaprlx068.intra.caixa.gov.br

2m 40s

Initialize job
·
succeeded
<1s

Pre-job: Download secure file
·
succeeded
<1s

Download Artifacts
·
succeeded
1 warning
<1s

Exportando as variáveis do arquivo Trust Store
·
succeeded
<1s

Valida Variáveis Obrigatórias
·
succeeded
<1s

Recuperando URL Pacote Nexus
·
succeeded
<1s

Recupera Pacote
·
succeeded
<1s

Recuperando nome do repositório
·
succeeded
<1s

Convertendo Minúsculo e Definindo nome do Projeto/Repositório
·
succeeded
<1s

Corrigindo Codificação Arquivos dos2unix
·
succeeded

<1s

Alterando Valores placeholders nos arquivos de config
·
succeeded
<1s

Git clone https://devops.caixa/projetos/Infraestrutura/_git/esteira-logs
·
succeeded
<1s

Cria Streams Graylog
·
succeeded
2s

Criando as VMs
·
succeeded
35s

Configurando DNS
·
succeeded
7s

Permissionamento LDAP
·
succeeded
2s

Configurando JBoss
·
succeeded
11s

Configurando Stack de Monitoração
·
1 error
12s
Bash exited with code '2'.

Configurando Logrotate
·
succeeded
2s

Configurando o Apache
·
succeeded
9s

Deploy Config no JBOSS
·
succeeded
20s

Deploy Pacote no JBOSS
·
succeeded
24s

Check Deployments [JBOSS]
·
succeeded
24s

Atualizando versão no PortalIF
·
succeeded
<1s

Resumo da release
·
succeeded
<1s

Finalize Job
·
succeeded
<1s
Row 2

No pipelines match your search

Select a release pipeline to view its releases

16 pipelines found

Row 6

Row 2

29 pipelines found

Select a release pipeline to view its releases

18 pipelines found

Select a release pipeline to view its releases

7 pipelines found

Select a release pipeline to view its releases

4 pipelines found

Row 4

Row 5

Row 2

Row 2

Row 2

Row 2

Row 2




2026-11-19T16:44:26.3352524Z ##[section]Starting: Deploy Pacote no JBOSS
2026-11-19T16:44:26.3355988Z ==============================================================================
2026-11-19T16:44:26.3356075Z Task         : Bash
2026-11-19T16:44:26.3356117Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-11-19T16:44:26.3356179Z Version      : 3.227.0
2026-11-19T16:44:26.3356230Z Author       : Microsoft Corporation
2026-11-19T16:44:26.3356278Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-11-19T16:44:26.3356346Z ==============================================================================
2026-11-19T16:44:26.4539083Z Generating script.
2026-11-19T16:44:26.4547106Z Script contents:
2026-11-19T16:44:26.4548420Z ansible-playbook /opt/ads-agent/esteira-jboss-vm/site.yml --tags deploy -e sistema_ambiente=tqs -e quantidade_vm=1 -e url_deploy="`echo "http://binario.caixa:8081/repository/releases/br/gov/caixa/sigec/csc-ear/0.0.112.2/csc-ear-0.0.112.2.ear" | tr -d "\'"`" -e package_path=/opt/ads-agent/_work/r19377/a/binario/`basename http://binario.caixa:8081/repository/releases/br/gov/caixa/sigec/csc-ear/0.0.112.2/csc-ear-0.0.112.2.ear` -e package_hash=$(HASH_BUILD) -e http_context_default=csc-api -e site=$(site)
2026-11-19T16:44:26.4550595Z ========================== Starting Command Output ===========================
2026-11-19T16:44:26.4557839Z [command]/bin/bash /opt/ads-agent/_work/_temp/f1fb9044-37e4-458c-8e17-37ca22de0532.sh
2026-11-19T16:44:26.4642726Z /opt/ads-agent/_work/_temp/f1fb9044-37e4-458c-8e17-37ca22de0532.sh: line 1: HASH_BUILD: comando não encontrado
2026-11-19T16:44:26.4645976Z /opt/ads-agent/_work/_temp/f1fb9044-37e4-458c-8e17-37ca22de0532.sh: line 1: site: comando não encontrado
2026-11-19T16:44:28.6099097Z 
2026-11-19T16:44:28.6099592Z PLAY [local] *******************************************************************
2026-11-19T16:44:28.6664666Z 
2026-11-19T16:44:28.6665142Z PLAY [Configurando o DNS] ******************************************************
2026-11-19T16:44:28.8649208Z 
2026-11-19T16:44:28.8649606Z PLAY [local] *******************************************************************
2026-11-19T16:44:28.8677791Z 
2026-11-19T16:44:28.8678175Z PLAY [local] *******************************************************************
2026-11-19T16:44:28.8708923Z 
2026-11-19T16:44:28.8709358Z PLAY [Verificando serviços] ****************************************************
2026-11-19T16:44:28.8796784Z 
2026-11-19T16:44:28.8797442Z PLAY [Configuração LDAP] *******************************************************
2026-11-19T16:44:28.8860613Z 
2026-11-19T16:44:28.8861181Z PLAY [apache_tqs] **************************************************************
2026-11-19T16:44:28.8896300Z 
2026-11-19T16:44:28.8896691Z PLAY [jboss] *******************************************************************
2026-11-19T16:44:28.8923446Z 
2026-11-19T16:44:28.8923894Z PLAY [Instalando stack Jboss] **************************************************
2026-11-19T16:44:28.9051562Z Thursday 19 November 2026  13:44:28 -0300 (0:00:00.355)       0:00:00.355 ***** 
2026-11-19T16:44:29.5196695Z 
2026-11-19T16:44:29.5197728Z TASK [Verificando o java versão esta instalado: 1.8.0_221] *********************
2026-11-19T16:44:29.5198359Z ok: [caddeapllx765.agil.nprd.caixa.gov.br]
2026-11-19T16:44:29.5237332Z Thursday 19 November 2026  13:44:29 -0300 (0:00:00.618)       0:00:00.973 ***** 
2026-11-19T16:44:29.9949807Z 
2026-11-19T16:44:29.9950506Z TASK [Verificando a versão do Java] ********************************************
2026-11-19T16:44:29.9950663Z changed: [caddeapllx765.agil.nprd.caixa.gov.br]
2026-11-19T16:44:29.9990240Z Thursday 19 November 2026  13:44:29 -0300 (0:00:00.475)       0:00:01.449 ***** 
2026-11-19T16:44:30.0529533Z Thursday 19 November 2026  13:44:30 -0300 (0:00:00.053)       0:00:01.502 ***** 
2026-11-19T16:44:30.4274253Z 
2026-11-19T16:44:30.4274959Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-11-19T16:44:30.4275123Z ok: [caddeapllx765.agil.nprd.caixa.gov.br]
2026-11-19T16:44:30.4316212Z Thursday 19 November 2026  13:44:30 -0300 (0:00:00.378)       0:00:01.881 ***** 
2026-11-19T16:44:30.4921802Z 
2026-11-19T16:44:30.4922422Z TASK [Setando a versão do Jboss] ***********************************************
2026-11-19T16:44:30.4922627Z ok: [caddeapllx765.agil.nprd.caixa.gov.br]
2026-11-19T16:44:30.4960101Z Thursday 19 November 2026  13:44:30 -0300 (0:00:00.064)       0:00:01.945 ***** 
2026-11-19T16:44:30.5402790Z Thursday 19 November 2026  13:44:30 -0300 (0:00:00.044)       0:00:01.990 ***** 
2026-11-19T16:44:30.5839375Z Thursday 19 November 2026  13:44:30 -0300 (0:00:00.043)       0:00:02.033 ***** 
2026-11-19T16:44:30.6275944Z Thursday 19 November 2026  13:44:30 -0300 (0:00:00.043)       0:00:02.077 ***** 
2026-11-19T16:44:30.6716340Z Thursday 19 November 2026  13:44:30 -0300 (0:00:00.043)       0:00:02.121 ***** 
2026-11-19T16:44:30.7169388Z Thursday 19 November 2026  13:44:30 -0300 (0:00:00.045)       0:00:02.166 ***** 
2026-11-19T16:44:30.7624430Z Thursday 19 November 2026  13:44:30 -0300 (0:00:00.045)       0:00:02.212 ***** 
2026-11-19T16:44:30.8080230Z Thursday 19 November 2026  13:44:30 -0300 (0:00:00.045)       0:00:02.257 ***** 
2026-11-19T16:44:30.8504046Z 
2026-11-19T16:44:30.8504579Z PLAY [jboss] *******************************************************************
2026-11-19T16:44:30.8530083Z 
2026-11-19T16:44:30.8530618Z PLAY [jboss] *******************************************************************
2026-11-19T16:44:30.8564718Z 
2026-11-19T16:44:30.8565082Z PLAY [jboss] *******************************************************************
2026-11-19T16:44:30.8611512Z Thursday 19 November 2026  13:44:30 -0300 (0:00:00.053)       0:00:02.311 ***** 
2026-11-19T16:44:32.7822865Z 
2026-11-19T16:44:32.7823530Z TASK [Gathering Facts] *********************************************************
2026-11-19T16:44:32.7823706Z ok: [caddeapllx765.agil.nprd.caixa.gov.br]
2026-11-19T16:44:32.8000897Z Thursday 19 November 2026  13:44:32 -0300 (0:00:01.938)       0:00:04.249 ***** 
2026-11-19T16:44:32.8632121Z 
2026-11-19T16:44:32.8633035Z TASK [Setando a versão do Jboss] ***********************************************
2026-11-19T16:44:32.8633291Z ok: [caddeapllx765.agil.nprd.caixa.gov.br]
2026-11-19T16:44:32.8756041Z Thursday 19 November 2026  13:44:32 -0300 (0:00:00.075)       0:00:04.325 ***** 
2026-11-19T16:44:33.5371104Z 
2026-11-19T16:44:33.5371563Z TASK [Garante que o Jboss esteja startado] *************************************
2026-11-19T16:44:33.5371729Z ok: [caddeapllx765.agil.nprd.caixa.gov.br]
2026-11-19T16:44:33.5530938Z Thursday 19 November 2026  13:44:33 -0300 (0:00:00.677)       0:00:05.003 ***** 
2026-11-19T16:44:34.0526576Z 
2026-11-19T16:44:34.0527027Z TASK [Verifica o se package existe] ********************************************
2026-11-19T16:44:34.0527184Z ok: [caddeapllx765.agil.nprd.caixa.gov.br]
2026-11-19T16:44:34.0675152Z Thursday 19 November 2026  13:44:34 -0300 (0:00:00.514)       0:00:05.517 ***** 
2026-11-19T16:44:38.4725073Z 
2026-11-19T16:44:38.4725673Z TASK [Deploy do pacote Local] **************************************************
2026-11-19T16:44:38.4725847Z changed: [caddeapllx765.agil.nprd.caixa.gov.br]
2026-11-19T16:44:38.4735108Z Thursday 19 November 2026  13:44:38 -0300 (0:00:04.406)       0:00:09.923 ***** 
2026-11-19T16:44:51.1261945Z 
2026-11-19T16:44:51.1262945Z RUNNING HANDLER [Restart Jboss] ************************************************
2026-11-19T16:44:51.1263295Z changed: [caddeapllx765.agil.nprd.caixa.gov.br]
2026-11-19T16:44:51.1286808Z 
2026-11-19T16:44:51.1286949Z PLAY [local] *******************************************************************
2026-11-19T16:44:51.1315122Z 
2026-11-19T16:44:51.1315265Z PLAY [jboss] *******************************************************************
2026-11-19T16:44:51.1343897Z 
2026-11-19T16:44:51.1344083Z PLAY [jboss] *******************************************************************
2026-11-19T16:44:51.1375323Z 
2026-11-19T16:44:51.1375526Z PLAY [Copiando deployments adicionais] *****************************************
2026-11-19T16:44:51.1403819Z 
2026-11-19T16:44:51.1403993Z PLAY [Copiando modules adicionais] *********************************************
2026-11-19T16:44:51.1435862Z 
2026-11-19T16:44:51.1436297Z PLAY [local] *******************************************************************
2026-11-19T16:44:51.1464391Z [WARNING]: Could not match supplied host pattern, ignoring: instance_restart
2026-11-19T16:44:51.1467792Z 
2026-11-19T16:44:51.1468168Z PLAY [instance_restart] ********************************************************
2026-11-19T16:44:51.1468415Z skipping: no hosts matched
2026-11-19T16:44:51.1472970Z [WARNING]: Could not match supplied host pattern, ignoring: machine_reboot
2026-11-19T16:44:51.1475971Z 
2026-11-19T16:44:51.1476125Z PLAY [machine_reboot] **********************************************************
2026-11-19T16:44:51.1476531Z skipping: no hosts matched
2026-11-19T16:44:51.1482468Z 
2026-11-19T16:44:51.1482803Z PLAY [local] *******************************************************************
2026-11-19T16:44:51.1507177Z [WARNING]: Could not match supplied host pattern, ignoring: instance_stop
2026-11-19T16:44:51.1510616Z 
2026-11-19T16:44:51.1511075Z PLAY [instance_stop] ***********************************************************
2026-11-19T16:44:51.1511244Z skipping: no hosts matched
2026-11-19T16:44:51.1516963Z 
2026-11-19T16:44:51.1517121Z PLAY [machine_reboot] **********************************************************
2026-11-19T16:44:51.1517328Z skipping: no hosts matched
2026-11-19T16:44:51.1522969Z 
2026-11-19T16:44:51.1523243Z PLAY [Configura TSM] ***********************************************************
2026-11-19T16:44:51.1551061Z 
2026-11-19T16:44:51.1551570Z PLAY [Configura Control-M] *****************************************************
2026-11-19T16:44:51.1576003Z 
2026-11-19T16:44:51.1576188Z PLAY RECAP *********************************************************************
2026-11-19T16:44:51.1576634Z caddeapllx765.agil.nprd.caixa.gov.br : ok=10   changed=3    unreachable=0    failed=0    skipped=9    rescued=0    ignored=0   
2026-11-19T16:44:51.1576765Z 
2026-11-19T16:44:51.1577664Z Thursday 19 November 2026  13:44:51 -0300 (0:00:12.684)       0:00:22.607 ***** 
2026-11-19T16:44:51.1577840Z =============================================================================== 
2026-11-19T16:44:51.1580939Z Restart Jboss ---------------------------------------------------------- 12.68s
2026-11-19T16:44:51.1581319Z Deploy do pacote Local -------------------------------------------------- 4.41s
2026-11-19T16:44:51.1581527Z Gathering Facts --------------------------------------------------------- 1.94s
2026-11-19T16:44:51.1581764Z Garante que o Jboss esteja startado ------------------------------------- 0.68s
2026-11-19T16:44:51.1581999Z Verificando o java versão esta instalado: 1.8.0_221 --------------------- 0.62s
2026-11-19T16:44:51.1582214Z Verifica o se package existe -------------------------------------------- 0.51s
2026-11-19T16:44:51.1582427Z Verificando a versão do Java -------------------------------------------- 0.48s
2026-11-19T16:44:51.1582644Z Verifica ser o Jboss já foi instalado ----------------------------------- 0.38s
2026-11-19T16:44:51.1588343Z Setando a versão do Jboss ----------------------------------------------- 0.08s
2026-11-19T16:44:51.1588696Z Setando a versão do Jboss ----------------------------------------------- 0.06s
2026-11-19T16:44:51.1588979Z java : include ---------------------------------------------------------- 0.05s
2026-11-19T16:44:51.1589196Z jboss : Copy template script -------------------------------------------- 0.05s
2026-11-19T16:44:51.1589431Z jboss : Domain | Set service name --------------------------------------- 0.05s
2026-11-19T16:44:51.1589641Z jboss : Standalone | Set service name ----------------------------------- 0.05s
2026-11-19T16:44:51.1589851Z jboss : Update domain.xml to use LDAP ----------------------------------- 0.05s
2026-11-19T16:44:51.1590055Z Determine variable jboss_domain_instance DC ----------------------------- 0.04s
2026-11-19T16:44:51.1590490Z jboss : Set file config to use domain.xml subsystem management ---------- 0.04s
2026-11-19T16:44:51.1590706Z Determine variable jboss_domain_instance standalone --------------------- 0.04s
2026-11-19T16:44:51.1590921Z Determine variable jboss_domain_instance HC ----------------------------- 0.04s
2026-11-19T16:44:51.1591058Z Playbook run took 0 days, 0 hours, 0 minutes, 22 seconds
2026-11-19T16:44:51.2239265Z ##[section]Finishing: Deploy Pacote no JBOSS



The authenticity of host '10.116.193.253 (10.116.193.253)' can't be established.
ED25519 key fingerprint is SHA256:KO10dr3WhBOs9ag9MpNZh2LtGRR7P9KoXXpaIqma8eg.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:32: 10.116.194.28
    ~/.ssh/known_hosts:50: 10.116.194.157
    ~/.ssh/known_hosts:59: 10.116.198.41
    ~/.ssh/known_hosts:72: 10.116.194.156
    ~/.ssh/known_hosts:133: 10.116.193.244
    ~/.ssh/known_hosts:185: 10.116.195.93
    ~/.ssh/known_hosts:222: 10.116.200.45
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '10.116.193.253' (ED25519) to the list of known hosts.
p585600@10.116.193.253's password:
Permission denied, please try again.
p585600@10.116.193.253's password:
Creating home directory for p585600.
Last failed login: Tue Nov 24 10:34:49 -03 2026 from 10.122.150.31 on ssh:notty
There was 1 failed login attempt since the last successful login.
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
