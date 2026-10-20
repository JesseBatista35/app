2026-10-20T20:47:26.6541062Z ##[section]Starting: Configurando Stack de Monitoração
2026-10-20T20:47:26.6544073Z ==============================================================================
2026-10-20T20:47:26.6544154Z Task         : Bash
2026-10-20T20:47:26.6544199Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-20T20:47:26.6544274Z Version      : 3.227.0
2026-10-20T20:47:26.6544321Z Author       : Microsoft Corporation
2026-10-20T20:47:26.6544375Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-20T20:47:26.6544472Z ==============================================================================
2026-10-20T20:47:27.6577582Z Generating script.
2026-10-20T20:47:27.6587787Z ========================== Starting Command Output ===========================
2026-10-20T20:47:27.6595156Z [command]/bin/bash /opt/ads-agent/_work/_temp/e7e49ea6-9a7f-44d0-a9d8-bbaa100f9884.sh
2026-10-20T20:47:27.6648854Z ++ echo _SIGSJ-intranet
2026-10-20T20:47:27.6648980Z ++ sed s/_//
2026-10-20T20:47:27.6659292Z + REPO=SIGSJ-intranet
2026-10-20T20:47:27.6661786Z ++ quantidade_vm
2026-10-20T20:47:27.6664073Z /opt/ads-agent/_work/_temp/e7e49ea6-9a7f-44d0-a9d8-bbaa100f9884.sh: line 3: quantidade_vm: comando não encontrado
2026-10-20T20:47:27.6665420Z + ansible-playbook /opt/ads-agent/_work/r18036/a/esteira-jboss-vm-v2/site.yml --tags monitoracao --skip-tags jboss -e sistema_ambiente=des -e quantidade_vm= -e sistema_nome=sigsj-intranet -e default_working_directory_tfs=/opt/ads-agent/_work/r18036/a -e build_repository_name_tfs=SIGSJ-intranet -e centralizadora_desenvolvimento=7390 -e centralizadora_operacoes=7259 -e fields_site=BR -e site=ctc_nprd
2026-10-20T20:47:29.7151763Z 
2026-10-20T20:47:29.7152287Z PLAY [local] *******************************************************************
2026-10-20T20:47:29.7422407Z 
2026-10-20T20:47:29.7423022Z PLAY [Configurando o DNS] ******************************************************
2026-10-20T20:47:29.9151810Z 
2026-10-20T20:47:29.9152323Z PLAY [local] *******************************************************************
2026-10-20T20:47:29.9374146Z Tuesday 20 October 2026  17:47:29 -0300 (0:00:00.281)       0:00:00.281 ******* 
2026-10-20T20:47:30.6664034Z 
2026-10-20T20:47:30.6664653Z TASK [Loga OKD] ****************************************************************
2026-10-20T20:47:30.6665773Z changed: [127.0.0.1]
2026-10-20T20:47:30.6685967Z Tuesday 20 October 2026  17:47:30 -0300 (0:00:00.731)       0:00:01.012 ******* 
2026-10-20T20:47:31.9315679Z 
2026-10-20T20:47:31.9316407Z TASK [Cria ConfigMap Prometheus] ***********************************************
2026-10-20T20:47:31.9316567Z changed: [127.0.0.1]
2026-10-20T20:47:31.9338251Z Tuesday 20 October 2026  17:47:31 -0300 (0:00:01.265)       0:00:02.277 ******* 
2026-10-20T20:47:32.3984629Z 
2026-10-20T20:47:32.3985533Z TASK [Logout OKD] **************************************************************
2026-10-20T20:47:32.3985876Z changed: [127.0.0.1]
2026-10-20T20:47:32.4008760Z 
2026-10-20T20:47:32.4009507Z PLAY [Verificando serviços] ****************************************************
2026-10-20T20:47:32.4110360Z Tuesday 20 October 2026  17:47:32 -0300 (0:00:00.477)       0:00:02.755 ******* 
2026-10-20T20:47:33.3404501Z 
2026-10-20T20:47:33.3405243Z TASK [Gathering Facts] *********************************************************
2026-10-20T20:47:33.3409190Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-20T20:47:33.3409662Z caddeapllx955.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-20T20:47:33.3409908Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-20T20:47:33.3410072Z releases. A future Ansible release will default to using the discovered 
2026-10-20T20:47:33.3410288Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-20T20:47:33.3410561Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-20T20:47:33.3410783Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-20T20:47:33.3411294Z setting deprecation_warnings=False in ansible.cfg.
2026-10-20T20:47:33.3411511Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:33.3577220Z Tuesday 20 October 2026  17:47:33 -0300 (0:00:00.946)       0:00:03.701 ******* 
2026-10-20T20:47:33.7415499Z 
2026-10-20T20:47:33.7416385Z TASK [Verifiando o jxm_exporter esta instalado] ********************************
2026-10-20T20:47:33.7416634Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:33.7536820Z Tuesday 20 October 2026  17:47:33 -0300 (0:00:00.395)       0:00:04.097 ******* 
2026-10-20T20:47:33.8034162Z Tuesday 20 October 2026  17:47:33 -0300 (0:00:00.049)       0:00:04.147 ******* 
2026-10-20T20:47:33.8538493Z Tuesday 20 October 2026  17:47:33 -0300 (0:00:00.050)       0:00:04.197 ******* 
2026-10-20T20:47:33.9040668Z Tuesday 20 October 2026  17:47:33 -0300 (0:00:00.050)       0:00:04.248 ******* 
2026-10-20T20:47:34.2859740Z 
2026-10-20T20:47:34.2860247Z TASK [Criando o grupo do "node_exporter"] **************************************
2026-10-20T20:47:34.2860433Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:34.3001663Z Tuesday 20 October 2026  17:47:34 -0300 (0:00:00.396)       0:00:04.644 ******* 
2026-10-20T20:47:34.8088261Z 
2026-10-20T20:47:34.8088610Z TASK [Criando o usuario "node_exporter" vinculado ao grupo "node_exporter"] ****
2026-10-20T20:47:34.8088770Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:34.8207818Z Tuesday 20 October 2026  17:47:34 -0300 (0:00:00.520)       0:00:05.164 ******* 
2026-10-20T20:47:35.2056554Z 
2026-10-20T20:47:35.2057274Z TASK [Criar diretório node_exporter] *******************************************
2026-10-20T20:47:35.2057453Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:35.2175175Z Tuesday 20 October 2026  17:47:35 -0300 (0:00:00.396)       0:00:05.561 ******* 
2026-10-20T20:47:35.8490636Z 
2026-10-20T20:47:35.8491100Z TASK [node_exporter : Copia o Node Exporter para o servidor] *******************
2026-10-20T20:47:35.8491296Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:35.8615701Z Tuesday 20 October 2026  17:47:35 -0300 (0:00:00.644)       0:00:06.205 ******* 
2026-10-20T20:47:36.3768096Z 
2026-10-20T20:47:36.3768778Z TASK [node_exporter : Criando o service do Node Exporter] **********************
2026-10-20T20:47:36.3769313Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:36.3892230Z Tuesday 20 October 2026  17:47:36 -0300 (0:00:00.527)       0:00:06.733 ******* 
2026-10-20T20:47:36.4478480Z 
2026-10-20T20:47:36.4478928Z TASK [filebeat : Set variables] ************************************************
2026-10-20T20:47:36.4479075Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:36.4595976Z Tuesday 20 October 2026  17:47:36 -0300 (0:00:00.070)       0:00:06.803 ******* 
2026-10-20T20:47:37.0348852Z 
2026-10-20T20:47:37.0349632Z TASK [Download RPM filebeat] ***************************************************
2026-10-20T20:47:37.0349799Z changed: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:37.0481683Z Tuesday 20 October 2026  17:47:37 -0300 (0:00:00.588)       0:00:07.392 ******* 
2026-10-20T20:47:40.4265183Z 
2026-10-20T20:47:40.4265751Z TASK [Instalando o filebeat versao 7.17.12] ************************************
2026-10-20T20:47:40.4265931Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:40.4386245Z Tuesday 20 October 2026  17:47:40 -0300 (0:00:03.390)       0:00:10.782 ******* 
2026-10-20T20:47:40.7096705Z 
2026-10-20T20:47:40.7097218Z TASK [Delete RPM filebeat] *****************************************************
2026-10-20T20:47:40.7097407Z changed: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:40.7218618Z Tuesday 20 October 2026  17:47:40 -0300 (0:00:00.283)       0:00:11.065 ******* 
2026-10-20T20:47:41.2755803Z 
2026-10-20T20:47:41.2756346Z TASK [Template a file to /etc/filebeat/filebeat.yml] ***************************
2026-10-20T20:47:41.2756522Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:41.2890605Z Tuesday 20 October 2026  17:47:41 -0300 (0:00:00.567)       0:00:11.633 ******* 
2026-10-20T20:47:41.5209677Z 
2026-10-20T20:47:41.5210197Z TASK [Create directory /var/log/filebeat_apache] *******************************
2026-10-20T20:47:41.5210370Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:41.5381818Z Tuesday 20 October 2026  17:47:41 -0300 (0:00:00.249)       0:00:11.882 ******* 
2026-10-20T20:47:42.0594292Z 
2026-10-20T20:47:42.0594799Z TASK [Template a file to /usr/lib/systemd/system/filebeat_apache.service] ******
2026-10-20T20:47:42.0595152Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:42.0723728Z Tuesday 20 October 2026  17:47:42 -0300 (0:00:00.534)       0:00:12.416 ******* 
2026-10-20T20:47:42.6113211Z 
2026-10-20T20:47:42.6113720Z TASK [Template a file to /etc/filebeat/filebeat_apache.yml] ********************
2026-10-20T20:47:42.6113895Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:42.6236171Z Tuesday 20 October 2026  17:47:42 -0300 (0:00:00.551)       0:00:12.967 ******* 
2026-10-20T20:47:42.8556048Z 
2026-10-20T20:47:42.8556983Z TASK [Create directory /var/log/filebeat_monit] ********************************
2026-10-20T20:47:42.8557197Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:42.8679554Z Tuesday 20 October 2026  17:47:42 -0300 (0:00:00.244)       0:00:13.212 ******* 
2026-10-20T20:47:43.3875670Z 
2026-10-20T20:47:43.3876597Z TASK [Template a file to /usr/lib/systemd/system/filebeat_monit.service] *******
2026-10-20T20:47:43.3876841Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:43.3997213Z Tuesday 20 October 2026  17:47:43 -0300 (0:00:00.531)       0:00:13.743 ******* 
2026-10-20T20:47:43.9258162Z 
2026-10-20T20:47:43.9259090Z TASK [Template a file to /etc/filebeat/filebeat_monit.yml] *********************
2026-10-20T20:47:43.9259389Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:43.9384594Z Tuesday 20 October 2026  17:47:43 -0300 (0:00:00.538)       0:00:14.282 ******* 
2026-10-20T20:47:47.4358275Z 
2026-10-20T20:47:47.4358831Z TASK [Install metricbeat] ******************************************************
2026-10-20T20:47:47.4359026Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:47.4470396Z Tuesday 20 October 2026  17:47:47 -0300 (0:00:03.508)       0:00:17.791 ******* 
2026-10-20T20:47:48.0775522Z 
2026-10-20T20:47:48.0776037Z TASK [Metricbeat | Start metricbeat] *******************************************
2026-10-20T20:47:48.0776199Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:48.0908049Z Tuesday 20 October 2026  17:47:48 -0300 (0:00:00.643)       0:00:18.434 ******* 
2026-10-20T20:47:48.3372590Z 
2026-10-20T20:47:48.3373102Z TASK [Verificando APM Agent] ***************************************************
2026-10-20T20:47:48.3373257Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:48.3497225Z Tuesday 20 October 2026  17:47:48 -0300 (0:00:00.258)       0:00:18.693 ******* 
2026-10-20T20:47:48.4002744Z Tuesday 20 October 2026  17:47:48 -0300 (0:00:00.050)       0:00:18.744 ******* 
2026-10-20T20:47:48.4496785Z Tuesday 20 October 2026  17:47:48 -0300 (0:00:00.049)       0:00:18.793 ******* 
2026-10-20T20:47:48.4990511Z Tuesday 20 October 2026  17:47:48 -0300 (0:00:00.049)       0:00:18.843 ******* 
2026-10-20T20:47:48.5481267Z Tuesday 20 October 2026  17:47:48 -0300 (0:00:00.049)       0:00:18.892 ******* 
2026-10-20T20:47:51.4212910Z 
2026-10-20T20:47:51.4214037Z TASK [zabbix : Instalar psql e libs - RHEL 8/9] ********************************
2026-10-20T20:47:51.4214407Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:51.4340987Z Tuesday 20 October 2026  17:47:51 -0300 (0:00:02.886)       0:00:21.778 ******* 
2026-10-20T20:47:51.6651780Z 
2026-10-20T20:47:51.6652287Z TASK [zabbix : Validar psql instalado] *****************************************
2026-10-20T20:47:51.6652456Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:51.6772195Z Tuesday 20 October 2026  17:47:51 -0300 (0:00:00.242)       0:00:22.021 ******* 
2026-10-20T20:47:51.9132574Z 
2026-10-20T20:47:51.9133531Z TASK [Verifica se existe servico zabbix-agent] *********************************
2026-10-20T20:47:51.9133732Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:51.9257677Z Tuesday 20 October 2026  17:47:51 -0300 (0:00:00.248)       0:00:22.269 ******* 
2026-10-20T20:47:51.9771169Z Tuesday 20 October 2026  17:47:51 -0300 (0:00:00.051)       0:00:22.321 ******* 
2026-10-20T20:47:52.0292683Z Tuesday 20 October 2026  17:47:52 -0300 (0:00:00.052)       0:00:22.373 ******* 
2026-10-20T20:47:55.2964292Z 
2026-10-20T20:47:55.2965207Z TASK [Install zabbix agent2 - Red Hat 9] ***************************************
2026-10-20T20:47:55.2965392Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:55.3093721Z Tuesday 20 October 2026  17:47:55 -0300 (0:00:03.280)       0:00:25.653 ******* 
2026-10-20T20:47:55.8048632Z 
2026-10-20T20:47:55.8049301Z TASK [zabbix : Backup da configuração atual] ***********************************
2026-10-20T20:47:55.8049472Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:55.8172145Z Tuesday 20 October 2026  17:47:55 -0300 (0:00:00.507)       0:00:26.161 ******* 
2026-10-20T20:47:56.3497729Z 
2026-10-20T20:47:56.3498251Z TASK [Template a file to /etc/zabbix/zabbix_agent2.conf] ***********************
2026-10-20T20:47:56.3498420Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:56.3621011Z Tuesday 20 October 2026  17:47:56 -0300 (0:00:00.544)       0:00:26.706 ******* 
2026-10-20T20:47:56.6936196Z 
2026-10-20T20:47:56.6936714Z TASK [Garantindo que o zabbix_agent2 esta startado] ****************************
2026-10-20T20:47:56.6936903Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:56.7074365Z Tuesday 20 October 2026  17:47:56 -0300 (0:00:00.345)       0:00:27.051 ******* 
2026-10-20T20:47:56.7566539Z Tuesday 20 October 2026  17:47:56 -0300 (0:00:00.049)       0:00:27.100 ******* 
2026-10-20T20:47:56.8139912Z 
2026-10-20T20:47:56.8140856Z TASK [zabbix : Gera o nome do grupo e templates quando o ambiente não é PRD] ***
2026-10-20T20:47:56.8141052Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:56.8259939Z Tuesday 20 October 2026  17:47:56 -0300 (0:00:00.069)       0:00:27.170 ******* 
2026-10-20T20:47:57.0589581Z 
2026-10-20T20:47:57.0590519Z TASK [zabbix : Verificar usuário] **********************************************
2026-10-20T20:47:57.0590731Z changed: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T20:47:57.0733301Z Tuesday 20 October 2026  17:47:57 -0300 (0:00:00.247)       0:00:27.417 ******* 
2026-10-20T20:47:57.6811666Z 
2026-10-20T20:47:57.6812181Z TASK [zabbix : hostgroup get to Zabbix Az CEMOT] *******************************
2026-10-20T20:47:57.6814040Z fatal: [caddeapllx955.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "connection": "close", "content": "", "content_length": "0", "date": "Tue, 20 Oct 2026 20:47:57 GMT", "elapsed": 0, "msg": "Status code was 404 and not [200, 202]: HTTP Error 404: Not Found", "redirected": false, "server": "istio-envoy", "status": 404, "url": "https://monitoracao.az.cloud.caixa/zabbixapi/api_jsonrpc.php"}
2026-10-20T20:47:57.6827875Z 
2026-10-20T20:47:57.6828025Z PLAY RECAP *********************************************************************
2026-10-20T20:47:57.6828203Z 127.0.0.1                  : ok=3    changed=3    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
2026-10-20T20:47:57.6828393Z caddeapllx955.agil.nprd.caixa.gov.br : ok=30   changed=3    unreachable=0    failed=1    skipped=10   rescued=0    ignored=0   
2026-10-20T20:47:57.6829431Z 
2026-10-20T20:47:57.6829689Z Tuesday 20 October 2026  17:47:57 -0300 (0:00:00.609)       0:00:28.027 ******* 
2026-10-20T20:47:57.6829870Z =============================================================================== 
2026-10-20T20:47:57.6832190Z Install metricbeat ------------------------------------------------------ 3.51s
2026-10-20T20:47:57.6832422Z Instalando o filebeat versao 7.17.12 ------------------------------------ 3.39s
2026-10-20T20:47:57.6832653Z Install zabbix agent2 - Red Hat 9 --------------------------------------- 3.28s
2026-10-20T20:47:57.6833072Z zabbix : Instalar psql e libs - RHEL 8/9 -------------------------------- 2.89s
2026-10-20T20:47:57.6833287Z Cria ConfigMap Prometheus ----------------------------------------------- 1.27s
2026-10-20T20:47:57.6833509Z Gathering Facts --------------------------------------------------------- 0.95s
2026-10-20T20:47:57.6833741Z Loga OKD ---------------------------------------------------------------- 0.73s
2026-10-20T20:47:57.6833960Z node_exporter : Copia o Node Exporter para o servidor ------------------- 0.64s
2026-10-20T20:47:57.6834189Z Metricbeat | Start metricbeat ------------------------------------------- 0.64s
2026-10-20T20:47:57.6834409Z zabbix : hostgroup get to Zabbix Az CEMOT ------------------------------- 0.61s
2026-10-20T20:47:57.6834631Z Download RPM filebeat --------------------------------------------------- 0.59s
2026-10-20T20:47:57.6834853Z Template a file to /etc/filebeat/filebeat.yml --------------------------- 0.57s
2026-10-20T20:47:57.6835154Z Template a file to /etc/filebeat/filebeat_apache.yml -------------------- 0.55s
2026-10-20T20:47:57.6835370Z Template a file to /etc/zabbix/zabbix_agent2.conf ----------------------- 0.54s
2026-10-20T20:47:57.6835592Z Template a file to /etc/filebeat/filebeat_monit.yml --------------------- 0.54s
2026-10-20T20:47:57.6835820Z Template a file to /usr/lib/systemd/system/filebeat_apache.service ------ 0.53s
2026-10-20T20:47:57.6836037Z Template a file to /usr/lib/systemd/system/filebeat_monit.service ------- 0.53s
2026-10-20T20:47:57.6836265Z node_exporter : Criando o service do Node Exporter ---------------------- 0.53s
2026-10-20T20:47:57.6836483Z Criando o usuario "node_exporter" vinculado ao grupo "node_exporter" ---- 0.52s
2026-10-20T20:47:57.6836715Z zabbix : Backup da configuração atual ----------------------------------- 0.51s
2026-10-20T20:47:57.6836868Z Playbook run took 0 days, 0 hours, 0 minutes, 27 seconds
2026-10-20T20:47:57.7401515Z ##[error]Bash exited with code '2'.
2026-10-20T20:47:57.7432022Z ##[section]Finishing: Configurando Stack de Monitoração





deu esse erro mais essa aks ta marcado como continun and error 

,mais enfim deuce rto passou

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
SIGSJ-intranet
/
SIGSJ-intranet-21
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
SIGSJ-intranet

SIGSJ-intranet-21


EC DES

Partially succeeded


Pipeline

Tasks

Variables

Logs

Tests
Agent job
Started: 20/10/2026, 17:44:55
Pool:
Release-Linux
·
Agent: cadsvaprlx070.intra.caixa.gov.br

5m 19s

Initialize job
·
succeeded
1s

Pre-job: Download secure file
·
succeeded
<1s

Download Artifacts
·
succeeded
1 warning
2s

Exportando as variáveis do arquivo Trust Store
·
succeeded
<1s

Recupera VEC
·
succeeded
2s

VEC - Aferição
·
succeeded
1 warning
<1s

Exportar variáveis NFS
·
succeeded
<1s

Exportar variáveis Infrafácil
·
succeeded
1s

Alocando o IP (AlocaIP e Infradevops)
·
succeeded
41s

Exporta as variáveis para o Terraform
·
succeeded
<1s

Replace tokens in **/*.tfvars.json **/*.tf
·
succeeded
<1s

Remove caracteres
·
succeeded
<1s

Install Terraform 1.3.5
·
succeeded
<1s

Terraform init
·
succeeded
9s

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
17s

Definir size como executado
·
succeeded
13s

Cadastrar Servidor no Satellite
·
succeeded
9s

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

Recuperando nome do repositório
·
succeeded
2s

Convertendo Minúsculo e Definindo nome do Projeto/Repositório
·
succeeded
1s

Corrigindo Codificação Arquivos dos2unix
·
succeeded
<1s

Alterando Valores placeholders nos arquivos de config
·
succeeded
<1s

Valida XML JBOSS
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
3s

Permissionamento LDAP
·
succeeded
19s

Configurando JBoss
·
succeeded
5s

Configurando Stack de Monitoração
·
1 error
31s
Bash exited with code '2'.

Configurando Logrotate
·
succeeded
8s

Configurando o Apache
·
succeeded
19s

Deploy Secure Files [JBOSS]
·
succeeded
5s

Deploy Config no JBOSS
·
succeeded
37s

Deploy Pacote no JBOSS
·
succeeded
8s

Check Deployments [JBOSS]
·
succeeded
6s

Atualizando versão no PortalIF
·
succeeded
1s

Resumo da release
·
succeeded
49s

Finalize Job
·
succeeded
<1s
6 pipelines found

Select a release pipeline to view its releases

6 pipelines found

Showing 11 deployments

Showing 11 deployments

Showing 11 deployments

Row 2

Row 2

Showing 11 deployments

Row 2

Showing filters 1 through 2

Showing filters 1 through 2

Expanded

Row 3

Collapsed

Showing 11 deployments

Row 3

Row 2

Row 2

Row 2



me jada com o resumo do que foi feito e avisa que agora vamos para o boleto 
