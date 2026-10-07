CONVERSA FIADA 
 DEPLOY DE HOJE AS 10:02

 TA FALHANDO
 
2026-10-07T13:01:50.2040331Z ##[section]Starting: Configurando Stack de Monitoração
2026-10-07T13:01:50.2043319Z ==============================================================================
2026-10-07T13:01:50.2043407Z Task         : Bash
2026-10-07T13:01:50.2043449Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-07T13:01:50.2043523Z Version      : 3.227.0
2026-10-07T13:01:50.2043564Z Author       : Microsoft Corporation
2026-10-07T13:01:50.2043613Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-07T13:01:50.2043681Z ==============================================================================
2026-10-07T13:01:51.2296433Z Generating script.
2026-10-07T13:01:51.2311364Z ========================== Starting Command Output ===========================
2026-10-07T13:01:51.2326035Z [command]/bin/bash /opt/ads-agent/_work/_temp/1e494c79-af2d-4c75-9b3a-069808906394.sh
2026-10-07T13:01:51.2364353Z ++ echo _SIPQV
2026-10-07T13:01:51.2366842Z ++ sed s/_//
2026-10-07T13:01:51.2376168Z + REPO=SIPQV
2026-10-07T13:01:51.2383899Z ++ site
2026-10-07T13:01:51.2384252Z /opt/ads-agent/_work/_temp/1e494c79-af2d-4c75-9b3a-069808906394.sh: line 3: site: comando não encontrado
2026-10-07T13:01:51.2389618Z + ansible-playbook /opt/ads-agent/esteira-jboss-vm/site.yml --tags monitoracao --skip-tags jboss -e sistema_ambiente=des -e quantidade_vm=1 -e sistema_nome=sipqv -e default_working_directory_tfs=/opt/ads-agent/_work/r15852/a -e build_repository_name_tfs=SIPQV -e centralizadora_desenvolvimento=7390 -e centralizadora_operacoes=7259 -e fields_site=BR -e site=
2026-10-07T13:01:53.2012154Z 
2026-10-07T13:01:53.2012959Z PLAY [local] *******************************************************************
2026-10-07T13:01:53.2530970Z 
2026-10-07T13:01:53.2531659Z PLAY [Configurando o DNS] ******************************************************
2026-10-07T13:01:53.4071185Z 
2026-10-07T13:01:53.4071972Z PLAY [local] *******************************************************************
2026-10-07T13:01:53.4100359Z 
2026-10-07T13:01:53.4100897Z PLAY [Verificando serviços] ****************************************************
2026-10-07T13:01:53.4208378Z Wednesday 07 October 2026  10:01:53 -0300 (0:00:00.277)       0:00:00.277 ***** 
2026-10-07T13:01:55.2031212Z 
2026-10-07T13:01:55.2061414Z TASK [Gathering Facts] *********************************************************
2026-10-07T13:01:55.2061635Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:01:55.2205504Z Wednesday 07 October 2026  10:01:55 -0300 (0:00:01.799)       0:00:02.077 ***** 
2026-10-07T13:01:55.6574301Z 
2026-10-07T13:01:55.6574626Z TASK [Verifiando o jxm_exporter esta instalado] ********************************
2026-10-07T13:01:55.6574783Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:01:55.6706498Z Wednesday 07 October 2026  10:01:55 -0300 (0:00:00.450)       0:00:02.527 ***** 
2026-10-07T13:01:55.7263136Z Wednesday 07 October 2026  10:01:55 -0300 (0:00:00.055)       0:00:02.583 ***** 
2026-10-07T13:01:55.7808480Z Wednesday 07 October 2026  10:01:55 -0300 (0:00:00.054)       0:00:02.637 ***** 
2026-10-07T13:01:55.8371362Z Wednesday 07 October 2026  10:01:55 -0300 (0:00:00.056)       0:00:02.693 ***** 
2026-10-07T13:01:56.2682283Z 
2026-10-07T13:01:56.2682816Z TASK [Criando o grupo do "node_exporter"] **************************************
2026-10-07T13:01:56.2682970Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:01:56.2828399Z Wednesday 07 October 2026  10:01:56 -0300 (0:00:00.445)       0:00:03.139 ***** 
2026-10-07T13:01:56.7912628Z 
2026-10-07T13:01:56.7913485Z TASK [Criando o usuario "node_exporter" vinculado ao grupo "node_exporter"] ****
2026-10-07T13:01:56.7913729Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:01:56.8047238Z Wednesday 07 October 2026  10:01:56 -0300 (0:00:00.521)       0:00:03.661 ***** 
2026-10-07T13:01:57.4981016Z 
2026-10-07T13:01:57.4981939Z TASK [node_exporter : Copia o Apache Exporter para o servidor] *****************
2026-10-07T13:01:57.4982386Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:01:57.5119629Z Wednesday 07 October 2026  10:01:57 -0300 (0:00:00.707)       0:00:04.368 ***** 
2026-10-07T13:01:58.2847483Z 
2026-10-07T13:01:58.2848019Z TASK [node_exporter : Criando o service do Node Exporter] **********************
2026-10-07T13:01:58.2848182Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:01:58.2984977Z Wednesday 07 October 2026  10:01:58 -0300 (0:00:00.786)       0:00:05.155 ***** 
2026-10-07T13:01:58.8129457Z 
2026-10-07T13:01:58.8129999Z TASK [Download RPM filebeat] ***************************************************
2026-10-07T13:01:58.8130162Z changed: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:01:58.8281658Z Wednesday 07 October 2026  10:01:58 -0300 (0:00:00.529)       0:00:05.685 ***** 
2026-10-07T13:01:59.5962983Z 
2026-10-07T13:01:59.5963509Z TASK [Instalando o filebeat versao 7.2.1] **************************************
2026-10-07T13:01:59.5963666Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:01:59.6095847Z Wednesday 07 October 2026  10:01:59 -0300 (0:00:00.781)       0:00:06.466 ***** 
2026-10-07T13:01:59.8845563Z 
2026-10-07T13:01:59.8846065Z TASK [Delete RPM filebeat] *****************************************************
2026-10-07T13:01:59.8846234Z changed: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:01:59.8982860Z Wednesday 07 October 2026  10:01:59 -0300 (0:00:00.288)       0:00:06.755 ***** 
2026-10-07T13:02:00.5005439Z 
2026-10-07T13:02:00.5006228Z TASK [Template a file to /etc/filebeat/filebeat.yml] ***************************
2026-10-07T13:02:00.5006865Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:02:00.5128355Z Wednesday 07 October 2026  10:02:00 -0300 (0:00:00.614)       0:00:07.369 ***** 
2026-10-07T13:02:00.7876980Z 
2026-10-07T13:02:00.7877807Z TASK [Verificando APM Agent] ***************************************************
2026-10-07T13:02:00.7878005Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:02:00.8013520Z Wednesday 07 October 2026  10:02:00 -0300 (0:00:00.288)       0:00:07.658 ***** 
2026-10-07T13:02:00.8575579Z Wednesday 07 October 2026  10:02:00 -0300 (0:00:00.056)       0:00:07.714 ***** 
2026-10-07T13:02:00.9143141Z Wednesday 07 October 2026  10:02:00 -0300 (0:00:00.056)       0:00:07.771 ***** 
2026-10-07T13:02:00.9683921Z Wednesday 07 October 2026  10:02:00 -0300 (0:00:00.054)       0:00:07.825 ***** 
2026-10-07T13:02:01.0222113Z Wednesday 07 October 2026  10:02:01 -0300 (0:00:00.053)       0:00:07.878 ***** 
2026-10-07T13:02:01.0780257Z Wednesday 07 October 2026  10:02:01 -0300 (0:00:00.056)       0:00:07.934 ***** 
2026-10-07T13:02:01.5120838Z 
2026-10-07T13:02:01.5121953Z TASK [Verifica se existe servico zabbix-agent] *********************************
2026-10-07T13:02:01.5122543Z fatal: [caddeapllx984.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["systemctl", "is-active", "zabbix-agent"], "delta": "0:00:00.005012", "end": "2026-10-07 10:02:01.494944", "msg": "non-zero return code", "rc": 3, "start": "2026-10-07 10:02:01.489932", "stderr": "", "stderr_lines": [], "stdout": "unknown", "stdout_lines": ["unknown"]}
2026-10-07T13:02:01.5122831Z ...ignoring
2026-10-07T13:02:01.5259912Z Wednesday 07 October 2026  10:02:01 -0300 (0:00:00.448)       0:00:08.382 ***** 
2026-10-07T13:02:01.5807533Z Wednesday 07 October 2026  10:02:01 -0300 (0:00:00.054)       0:00:08.437 ***** 
2026-10-07T13:02:02.8822705Z 
2026-10-07T13:02:02.8823403Z TASK [zabbix : Install libpcre2-8 - Red Hat 7] *********************************
2026-10-07T13:02:02.8827325Z fatal: [caddeapllx984.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "changes": {"installed": ["/root/.ansible/tmp/ansible-moduletmp-1791378122.06-nE73xb/libpcre2-8-0-10.39-150400.2.3.x86_64sEQujk.rpm"]}, "msg": "\nThis system is not registered with RHN Classic or Red Hat Satellite.\nYou can use rhn_register to register.\nRed Hat Satellite or RHN Classic support will be disabled.\n\n\nTransaction check error:\n  file /usr/lib64/libpcre2-8.so.0 from install of libpcre2-8-0-10.39-150400.2.3.x86_64 conflicts with file from package pcre2-10.23-2.el7.x86_64\n\nError Summary\n-------------\n\n", "rc": 1, "results": ["Loaded plugins: product-id, rhnplugin, search-disabled-repos, subscription-\n              : manager\nExamining /root/.ansible/tmp/ansible-moduletmp-1791378122.06-nE73xb/libpcre2-8-0-10.39-150400.2.3.x86_64sEQujk.rpm: libpcre2-8-0-10.39-150400.2.3.x86_64\nMarking /root/.ansible/tmp/ansible-moduletmp-1791378122.06-nE73xb/libpcre2-8-0-10.39-150400.2.3.x86_64sEQujk.rpm to be installed\nResolving Dependencies\n--> Running transaction check\n---> Package libpcre2-8-0.x86_64 0:10.39-150400.2.3 will be installed\n--> Finished Dependency Resolution\n\nDependencies Resolved\n\n================================================================================\n Package\n      Arch   Version          Repository                                   Size\n================================================================================\nInstalling:\n libpcre2-8-0\n      x86_64 10.39-150400.2.3 /libpcre2-8-0-10.39-150400.2.3.x86_64sEQujk 910 k\n\nTransaction Summary\n================================================================================\nInstall  1 Package\n\nTotal size: 910 k\nInstalled size: 910 k\nDownloading packages:\nRunning transaction check\nRunning transaction test\n"]}
2026-10-07T13:02:02.8829015Z ...ignoring
2026-10-07T13:02:02.8958417Z Wednesday 07 October 2026  10:02:02 -0300 (0:00:01.315)       0:00:09.752 ***** 
2026-10-07T13:02:03.5175712Z 
2026-10-07T13:02:03.5176239Z TASK [Install zabbix agent2] ***************************************************
2026-10-07T13:02:03.5176683Z ok: [caddeapllx984.agil.nprd.caixa.gov.br] => (item=http://10.122.154.12/deploy/zabbix-agent2-plugin-mongodb-6.0.23-release1.el7.x86_64.rpm)
2026-10-07T13:02:04.1283540Z ok: [caddeapllx984.agil.nprd.caixa.gov.br] => (item=http://10.122.154.12/deploy/zabbix-agent2-plugin-postgresql-6.0.23-release1.el7.x86_64.rpm)
2026-10-07T13:02:04.7263240Z ok: [caddeapllx984.agil.nprd.caixa.gov.br] => (item=http://10.122.154.12/deploy/zabbix-agent2-6.0.23-release1.el7.x86_64.rpm)
2026-10-07T13:02:04.7422513Z Wednesday 07 October 2026  10:02:04 -0300 (0:00:01.846)       0:00:11.598 ***** 
2026-10-07T13:02:05.3604156Z 
2026-10-07T13:02:05.3604687Z TASK [Template a file to /etc/zabbix_zabbix_agente.d/monit_agent2.conf] ********
2026-10-07T13:02:05.3604836Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:02:05.3732080Z Wednesday 07 October 2026  10:02:05 -0300 (0:00:00.630)       0:00:12.230 ***** 
2026-10-07T13:02:06.0140830Z 
2026-10-07T13:02:06.0141722Z TASK [Garantindo que o zabbix_agent2 esta startado] ****************************
2026-10-07T13:02:06.0141948Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:02:06.0285210Z Wednesday 07 October 2026  10:02:06 -0300 (0:00:00.655)       0:00:12.885 ***** 
2026-10-07T13:02:06.0824681Z Wednesday 07 October 2026  10:02:06 -0300 (0:00:00.053)       0:00:12.939 ***** 
2026-10-07T13:02:06.1422032Z 
2026-10-07T13:02:06.1422575Z TASK [zabbix : Gera o nome do grupo e templates quando o ambiente não é PRD] ***
2026-10-07T13:02:06.1422820Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:02:06.1587068Z Wednesday 07 October 2026  10:02:06 -0300 (0:00:00.076)       0:00:13.015 ***** 
2026-10-07T13:02:07.0966837Z 
2026-10-07T13:02:07.0967286Z TASK [zabbix : hostgroup create to Zabbix Az CEMOT] ****************************
2026-10-07T13:02:07.0967478Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:02:07.1132965Z Wednesday 07 October 2026  10:02:07 -0300 (0:00:00.954)       0:00:13.970 ***** 
2026-10-07T13:02:07.8272042Z 
2026-10-07T13:02:07.8272488Z TASK [zabbix : template get to Zabbix Az CEMOT] ********************************
2026-10-07T13:02:07.8272644Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:02:07.8436094Z Wednesday 07 October 2026  10:02:07 -0300 (0:00:00.730)       0:00:14.700 ***** 
2026-10-07T13:02:08.5321890Z 
2026-10-07T13:02:08.5322385Z TASK [zabbix : hostgroup get to Zabbix Az CEMOT] *******************************
2026-10-07T13:02:08.5322742Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:02:08.5489347Z Wednesday 07 October 2026  10:02:08 -0300 (0:00:00.705)       0:00:15.405 ***** 
2026-10-07T13:02:09.2343993Z 
2026-10-07T13:02:09.2344749Z TASK [zabbix : proxy get to Zabbix Az CEMOT] ***********************************
2026-10-07T13:02:09.2345446Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:02:09.2506657Z Wednesday 07 October 2026  10:02:09 -0300 (0:00:00.701)       0:00:16.107 ***** 
2026-10-07T13:02:09.9491894Z 
2026-10-07T13:02:09.9492383Z TASK [zabbix : host create to Zabbix Az CEMOT] *********************************
2026-10-07T13:02:09.9492543Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:02:09.9634702Z Wednesday 07 October 2026  10:02:09 -0300 (0:00:00.712)       0:00:16.820 ***** 
2026-10-07T13:02:10.0178246Z Wednesday 07 October 2026  10:02:10 -0300 (0:00:00.054)       0:00:16.874 ***** 
2026-10-07T13:02:10.0772352Z 
2026-10-07T13:02:10.0773093Z TASK [zabbix : Gera o nome do grupo e define os templates quando o ambiente NPRD] ***
2026-10-07T13:02:10.0773487Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:02:10.0902594Z Wednesday 07 October 2026  10:02:10 -0300 (0:00:00.072)       0:00:16.947 ***** 
2026-10-07T13:02:10.1478040Z 
2026-10-07T13:02:10.1478830Z TASK [zabbix : Gera os nomes de grupos e dados para tratamento dos consolidados.] ***
2026-10-07T13:02:10.1479054Z ok: [caddeapllx984.agil.nprd.caixa.gov.br]
2026-10-07T13:02:10.1640239Z Wednesday 07 October 2026  10:02:10 -0300 (0:00:00.073)       0:00:17.020 ***** 
2026-10-07T13:02:10.2342483Z /opt/ads-agent/ansible/lib/python2.7/site-packages/psycopg2/__init__.py:144: UserWarning: The psycopg2 wheel package will be renamed from release 2.8; in order to keep installing from binary please use "pip install psycopg2-binary" instead. For details see: <http://initd.org/psycopg/docs/install.html#binary-install-from-pypi>.
2026-10-07T13:02:10.2343080Z   """)
2026-10-07T13:02:12.9316481Z 
2026-10-07T13:02:12.9322955Z TASK [zabbix : Consultar os dados do sistema.] *********************************
2026-10-07T13:02:12.9324340Z fatal: [caddeapllx984.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "msg": "unable to connect to database: FATAL:  password authentication failed for user \"monitdbadm\"\nFATAL:  no pg_hba.conf entry for host \"10.122.155.67\", user \"monitdbadm\", database \"monitordb001\", no encryption\n"}
2026-10-07T13:02:12.9330169Z 
2026-10-07T13:02:12.9330455Z PLAY RECAP *********************************************************************
2026-10-07T13:02:12.9331042Z caddeapllx984.agil.nprd.caixa.gov.br : ok=24   changed=3    unreachable=0    failed=1    skipped=11   rescued=0    ignored=2   
2026-10-07T13:02:12.9331132Z 
2026-10-07T13:02:12.9332374Z Wednesday 07 October 2026  10:02:12 -0300 (0:00:02.769)       0:00:19.790 ***** 
2026-10-07T13:02:12.9332554Z =============================================================================== 
2026-10-07T13:02:12.9336265Z zabbix : Consultar os dados do sistema. --------------------------------- 2.77s
2026-10-07T13:02:12.9336506Z Install zabbix agent2 --------------------------------------------------- 1.85s
2026-10-07T13:02:12.9336742Z Gathering Facts --------------------------------------------------------- 1.80s
2026-10-07T13:02:12.9336961Z zabbix : Install libpcre2-8 - Red Hat 7 --------------------------------- 1.32s
2026-10-07T13:02:12.9339054Z zabbix : hostgroup create to Zabbix Az CEMOT ---------------------------- 0.95s
2026-10-07T13:02:12.9339412Z node_exporter : Criando o service do Node Exporter ---------------------- 0.79s
2026-10-07T13:02:12.9339640Z Instalando o filebeat versao 7.2.1 -------------------------------------- 0.78s
2026-10-07T13:02:12.9339853Z zabbix : template get to Zabbix Az CEMOT -------------------------------- 0.73s
2026-10-07T13:02:12.9340068Z zabbix : host create to Zabbix Az CEMOT --------------------------------- 0.71s
2026-10-07T13:02:12.9340284Z node_exporter : Copia o Apache Exporter para o servidor ----------------- 0.71s
2026-10-07T13:02:12.9340694Z zabbix : hostgroup get to Zabbix Az CEMOT ------------------------------- 0.71s
2026-10-07T13:02:12.9340999Z zabbix : proxy get to Zabbix Az CEMOT ----------------------------------- 0.70s
2026-10-07T13:02:12.9341221Z Garantindo que o zabbix_agent2 esta startado ---------------------------- 0.66s
2026-10-07T13:02:12.9341437Z Template a file to /etc/zabbix_zabbix_agente.d/monit_agent2.conf -------- 0.63s
2026-10-07T13:02:12.9341657Z Template a file to /etc/filebeat/filebeat.yml --------------------------- 0.61s
2026-10-07T13:02:12.9341878Z Download RPM filebeat --------------------------------------------------- 0.53s
2026-10-07T13:02:12.9342100Z Criando o usuario "node_exporter" vinculado ao grupo "node_exporter" ---- 0.52s
2026-10-07T13:02:12.9342344Z Verifiando o jxm_exporter esta instalado -------------------------------- 0.45s
2026-10-07T13:02:12.9342564Z Verifica se existe servico zabbix-agent --------------------------------- 0.45s
2026-10-07T13:02:12.9342780Z Criando o grupo do "node_exporter" -------------------------------------- 0.45s
2026-10-07T13:02:12.9342925Z Playbook run took 0 days, 0 hours, 0 minutes, 19 seconds
2026-10-07T13:02:13.0005217Z ##[error]Bash exited with code '2'.
2026-10-07T13:02:13.0013846Z ##[section]Finishing: Configurando Stack de Monitoração
