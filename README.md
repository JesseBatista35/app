2026-10-07T17:23:09.7973231Z ##[section]Starting: Configurando Stack de Monitoração
2026-10-07T17:23:09.7976568Z ==============================================================================
2026-10-07T17:23:09.7976662Z Task         : Bash
2026-10-07T17:23:09.7976801Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-07T17:23:09.7976860Z Version      : 3.227.0
2026-10-07T17:23:09.7976911Z Author       : Microsoft Corporation
2026-10-07T17:23:09.7976959Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-07T17:23:09.7977025Z ==============================================================================
2026-10-07T17:23:10.6577297Z Generating script.
2026-10-07T17:23:10.6588281Z ========================== Starting Command Output ===========================
2026-10-07T17:23:10.6600606Z [command]/bin/bash /opt/ads-agent/_work/_temp/5ca703d6-301a-4519-a651-2f869433f8f7.sh
2026-10-07T17:23:10.6646219Z ++ echo _SIGPD-backend
2026-10-07T17:23:10.6646638Z ++ sed s/_//
2026-10-07T17:23:10.6657922Z + REPO=SIGPD-backend
2026-10-07T17:23:10.6660763Z ++ site
2026-10-07T17:23:10.6663400Z /opt/ads-agent/_work/_temp/5ca703d6-301a-4519-a651-2f869433f8f7.sh: line 3: site: comando não encontrado
2026-10-07T17:23:10.6665011Z + ansible-playbook /opt/ads-agent/esteira-jboss-vm/site.yml --tags monitoracao --skip-tags jboss -e sistema_ambiente=tqs -e quantidade_vm=1 -e sistema_nome=sigpd-backend -e default_working_directory_tfs=/opt/ads-agent/_work/r2298/a -e build_repository_name_tfs=SIGPD-backend -e centralizadora_desenvolvimento=7390 -e centralizadora_operacoes=7259 -e fields_site=BR -e site=
2026-10-07T17:23:12.6733824Z 
2026-10-07T17:23:12.6734385Z PLAY [local] *******************************************************************
2026-10-07T17:23:12.7270157Z 
2026-10-07T17:23:12.7270658Z PLAY [Configurando o DNS] ******************************************************
2026-10-07T17:23:12.8829012Z 
2026-10-07T17:23:12.8829586Z PLAY [local] *******************************************************************
2026-10-07T17:23:12.8854746Z 
2026-10-07T17:23:12.8855072Z PLAY [local] *******************************************************************
2026-10-07T17:23:12.8884513Z 
2026-10-07T17:23:12.8885165Z PLAY [Verificando serviços] ****************************************************
2026-10-07T17:23:12.8992272Z Wednesday 07 October 2026  14:23:12 -0300 (0:00:00.287)       0:00:00.287 ***** 
2026-10-07T17:23:14.8143129Z 
2026-10-07T17:23:14.8143898Z TASK [Gathering Facts] *********************************************************
2026-10-07T17:23:14.8144687Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:14.8322049Z Wednesday 07 October 2026  14:23:14 -0300 (0:00:01.932)       0:00:02.220 ***** 
2026-10-07T17:23:15.2422621Z 
2026-10-07T17:23:15.2423201Z TASK [Verifiando o jxm_exporter esta instalado] ********************************
2026-10-07T17:23:15.2423369Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:15.2575631Z Wednesday 07 October 2026  14:23:15 -0300 (0:00:00.425)       0:00:02.645 ***** 
2026-10-07T17:23:15.3144348Z Wednesday 07 October 2026  14:23:15 -0300 (0:00:00.056)       0:00:02.702 ***** 
2026-10-07T17:23:15.3719468Z Wednesday 07 October 2026  14:23:15 -0300 (0:00:00.057)       0:00:02.760 ***** 
2026-10-07T17:23:15.4300942Z Wednesday 07 October 2026  14:23:15 -0300 (0:00:00.058)       0:00:02.818 ***** 
2026-10-07T17:23:15.8591958Z 
2026-10-07T17:23:15.8592733Z TASK [Criando o grupo do "node_exporter"] **************************************
2026-10-07T17:23:15.8593120Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:15.8759140Z Wednesday 07 October 2026  14:23:15 -0300 (0:00:00.445)       0:00:03.264 ***** 
2026-10-07T17:23:16.4906502Z 
2026-10-07T17:23:16.4907203Z TASK [Criando o usuario "node_exporter" vinculado ao grupo "node_exporter"] ****
2026-10-07T17:23:16.4907466Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:16.5064294Z Wednesday 07 October 2026  14:23:16 -0300 (0:00:00.630)       0:00:03.894 ***** 
2026-10-07T17:23:17.2385226Z 
2026-10-07T17:23:17.2386423Z TASK [node_exporter : Copia o Apache Exporter para o servidor] *****************
2026-10-07T17:23:17.2387023Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:17.2505910Z Wednesday 07 October 2026  14:23:17 -0300 (0:00:00.744)       0:00:04.638 ***** 
2026-10-07T17:23:18.0525576Z 
2026-10-07T17:23:18.0526183Z TASK [node_exporter : Criando o service do Node Exporter] **********************
2026-10-07T17:23:18.0526873Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:18.0663156Z Wednesday 07 October 2026  14:23:18 -0300 (0:00:00.815)       0:00:05.454 ***** 
2026-10-07T17:23:18.6264362Z 
2026-10-07T17:23:18.6264909Z TASK [Download RPM filebeat] ***************************************************
2026-10-07T17:23:18.6265071Z changed: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:18.6422628Z Wednesday 07 October 2026  14:23:18 -0300 (0:00:00.575)       0:00:06.030 ***** 
2026-10-07T17:23:19.4277932Z 
2026-10-07T17:23:19.4279012Z TASK [Instalando o filebeat versao 7.2.1] **************************************
2026-10-07T17:23:19.4279799Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:19.4420870Z Wednesday 07 October 2026  14:23:19 -0300 (0:00:00.799)       0:00:06.830 ***** 
2026-10-07T17:23:19.7436192Z 
2026-10-07T17:23:19.7437323Z TASK [Delete RPM filebeat] *****************************************************
2026-10-07T17:23:19.7437732Z changed: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:19.7589199Z Wednesday 07 October 2026  14:23:19 -0300 (0:00:00.316)       0:00:07.147 ***** 
2026-10-07T17:23:20.3985268Z 
2026-10-07T17:23:20.3985825Z TASK [Template a file to /etc/filebeat/filebeat.yml] ***************************
2026-10-07T17:23:20.3985987Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:20.4127306Z Wednesday 07 October 2026  14:23:20 -0300 (0:00:00.653)       0:00:07.800 ***** 
2026-10-07T17:23:20.7288956Z 
2026-10-07T17:23:20.7289542Z TASK [Verificando APM Agent] ***************************************************
2026-10-07T17:23:20.7289718Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:20.7421445Z Wednesday 07 October 2026  14:23:20 -0300 (0:00:00.329)       0:00:08.130 ***** 
2026-10-07T17:23:20.7976612Z Wednesday 07 October 2026  14:23:20 -0300 (0:00:00.055)       0:00:08.185 ***** 
2026-10-07T17:23:20.8579990Z Wednesday 07 October 2026  14:23:20 -0300 (0:00:00.060)       0:00:08.246 ***** 
2026-10-07T17:23:20.9149747Z Wednesday 07 October 2026  14:23:20 -0300 (0:00:00.056)       0:00:08.303 ***** 
2026-10-07T17:23:20.9709200Z Wednesday 07 October 2026  14:23:20 -0300 (0:00:00.055)       0:00:08.359 ***** 
2026-10-07T17:23:21.0269092Z Wednesday 07 October 2026  14:23:21 -0300 (0:00:00.055)       0:00:08.415 ***** 
2026-10-07T17:23:21.4746053Z 
2026-10-07T17:23:21.4747218Z TASK [Verifica se existe servico zabbix-agent] *********************************
2026-10-07T17:23:21.4747891Z fatal: [caddeapllx930.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["systemctl", "is-active", "zabbix-agent"], "delta": "0:00:00.005140", "end": "2026-10-07 14:23:21.460034", "msg": "non-zero return code", "rc": 3, "start": "2026-10-07 14:23:21.454894", "stderr": "", "stderr_lines": [], "stdout": "unknown", "stdout_lines": ["unknown"]}
2026-10-07T17:23:21.4748259Z ...ignoring
2026-10-07T17:23:21.4887883Z Wednesday 07 October 2026  14:23:21 -0300 (0:00:00.461)       0:00:08.877 ***** 
2026-10-07T17:23:21.5456577Z Wednesday 07 October 2026  14:23:21 -0300 (0:00:00.056)       0:00:08.933 ***** 
2026-10-07T17:23:22.8028242Z 
2026-10-07T17:23:22.8029380Z TASK [zabbix : Install libpcre2-8 - Red Hat 7] *********************************
2026-10-07T17:23:22.8033631Z fatal: [caddeapllx930.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "changes": {"installed": ["/root/.ansible/tmp/ansible-moduletmp-1791393802.01-B6Za4v/libpcre2-8-0-10.39-150400.2.3.x86_64jhaVcI.rpm"]}, "msg": "This system is not registered with RHN Classic or Red Hat Satellite.\nYou can use rhn_register to register.\nRed Hat Satellite or RHN Classic support will be disabled.\n\n\nTransaction check error:\n  file /usr/lib64/libpcre2-8.so.0 from install of libpcre2-8-0-10.39-150400.2.3.x86_64 conflicts with file from package pcre2-10.23-2.el7.x86_64\n\nError Summary\n-------------\n\n", "rc": 1, "results": ["Loaded plugins: product-id, rhnplugin, search-disabled-repos, subscription-\n              : manager\nThis system is not registered with an entitlement server. You can use subscription-manager to register.\nExamining /root/.ansible/tmp/ansible-moduletmp-1791393802.01-B6Za4v/libpcre2-8-0-10.39-150400.2.3.x86_64jhaVcI.rpm: libpcre2-8-0-10.39-150400.2.3.x86_64\nMarking /root/.ansible/tmp/ansible-moduletmp-1791393802.01-B6Za4v/libpcre2-8-0-10.39-150400.2.3.x86_64jhaVcI.rpm to be installed\nResolving Dependencies\n--> Running transaction check\n---> Package libpcre2-8-0.x86_64 0:10.39-150400.2.3 will be installed\n--> Finished Dependency Resolution\n\nDependencies Resolved\n\n================================================================================\n Package\n      Arch   Version          Repository                                   Size\n================================================================================\nInstalling:\n libpcre2-8-0\n      x86_64 10.39-150400.2.3 /libpcre2-8-0-10.39-150400.2.3.x86_64jhaVcI 910 k\n\nTransaction Summary\n================================================================================\nInstall  1 Package\n\nTotal size: 910 k\nInstalled size: 910 k\nDownloading packages:\nRunning transaction check\nRunning transaction test\n"]}
2026-10-07T17:23:22.8035419Z ...ignoring
2026-10-07T17:23:22.8162026Z Wednesday 07 October 2026  14:23:22 -0300 (0:00:01.270)       0:00:10.204 ***** 
2026-10-07T17:23:23.4550638Z 
2026-10-07T17:23:23.4551996Z TASK [Install zabbix agent2] ***************************************************
2026-10-07T17:23:23.4552718Z ok: [caddeapllx930.agil.nprd.caixa.gov.br] => (item=http://10.122.154.12/deploy/zabbix-agent2-plugin-mongodb-6.0.23-release1.el7.x86_64.rpm)
2026-10-07T17:23:23.9955548Z ok: [caddeapllx930.agil.nprd.caixa.gov.br] => (item=http://10.122.154.12/deploy/zabbix-agent2-plugin-postgresql-6.0.23-release1.el7.x86_64.rpm)
2026-10-07T17:23:24.5648089Z ok: [caddeapllx930.agil.nprd.caixa.gov.br] => (item=http://10.122.154.12/deploy/zabbix-agent2-6.0.23-release1.el7.x86_64.rpm)
2026-10-07T17:23:24.5796107Z Wednesday 07 October 2026  14:23:24 -0300 (0:00:01.763)       0:00:11.967 ***** 
2026-10-07T17:23:25.2112893Z 
2026-10-07T17:23:25.2113392Z TASK [Template a file to /etc/zabbix_zabbix_agente.d/monit_agent2.conf] ********
2026-10-07T17:23:25.2113605Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:25.2261053Z Wednesday 07 October 2026  14:23:25 -0300 (0:00:00.646)       0:00:12.614 ***** 
2026-10-07T17:23:25.8682989Z 
2026-10-07T17:23:25.8684005Z TASK [Garantindo que o zabbix_agent2 esta startado] ****************************
2026-10-07T17:23:25.8684240Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:25.8829853Z Wednesday 07 October 2026  14:23:25 -0300 (0:00:00.656)       0:00:13.271 ***** 
2026-10-07T17:23:25.9399658Z Wednesday 07 October 2026  14:23:25 -0300 (0:00:00.056)       0:00:13.328 ***** 
2026-10-07T17:23:26.0055864Z 
2026-10-07T17:23:26.0057206Z TASK [zabbix : Gera o nome do grupo e templates quando o ambiente não é PRD] ***
2026-10-07T17:23:26.0057519Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:26.0225086Z Wednesday 07 October 2026  14:23:26 -0300 (0:00:00.082)       0:00:13.410 ***** 
2026-10-07T17:23:27.0428088Z 
2026-10-07T17:23:27.0428579Z TASK [zabbix : hostgroup create to Zabbix Az CEMOT] ****************************
2026-10-07T17:23:27.0428791Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:27.0603031Z Wednesday 07 October 2026  14:23:27 -0300 (0:00:01.037)       0:00:14.448 ***** 
2026-10-07T17:23:27.8380508Z 
2026-10-07T17:23:27.8381195Z TASK [zabbix : template get to Zabbix Az CEMOT] ********************************
2026-10-07T17:23:27.8381470Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:27.8567441Z Wednesday 07 October 2026  14:23:27 -0300 (0:00:00.796)       0:00:15.244 ***** 
2026-10-07T17:23:28.6018410Z 
2026-10-07T17:23:28.6018964Z TASK [zabbix : hostgroup get to Zabbix Az CEMOT] *******************************
2026-10-07T17:23:28.6019412Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:28.6167946Z Wednesday 07 October 2026  14:23:28 -0300 (0:00:00.759)       0:00:16.004 ***** 
2026-10-07T17:23:29.1721917Z 
2026-10-07T17:23:29.1722465Z TASK [zabbix : proxy get to Zabbix Az CEMOT] ***********************************
2026-10-07T17:23:29.1722634Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:29.1888888Z Wednesday 07 October 2026  14:23:29 -0300 (0:00:00.572)       0:00:16.577 ***** 
2026-10-07T17:23:29.8718874Z 
2026-10-07T17:23:29.8719973Z TASK [zabbix : host create to Zabbix Az CEMOT] *********************************
2026-10-07T17:23:29.8720263Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:29.8878392Z Wednesday 07 October 2026  14:23:29 -0300 (0:00:00.698)       0:00:17.275 ***** 
2026-10-07T17:23:29.9513973Z Wednesday 07 October 2026  14:23:29 -0300 (0:00:00.063)       0:00:17.339 ***** 
2026-10-07T17:23:30.0162972Z 
2026-10-07T17:23:30.0163927Z TASK [zabbix : Gera o nome do grupo e define os templates quando o ambiente NPRD] ***
2026-10-07T17:23:30.0164334Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:30.0306647Z Wednesday 07 October 2026  14:23:30 -0300 (0:00:00.079)       0:00:17.418 ***** 
2026-10-07T17:23:30.0912603Z 
2026-10-07T17:23:30.0914353Z TASK [zabbix : Gera os nomes de grupos e dados para tratamento dos consolidados.] ***
2026-10-07T17:23:30.0914687Z ok: [caddeapllx930.agil.nprd.caixa.gov.br]
2026-10-07T17:23:30.1076352Z Wednesday 07 October 2026  14:23:30 -0300 (0:00:00.077)       0:00:17.495 ***** 
2026-10-07T17:23:30.1712276Z /opt/ads-agent/ansible/lib/python2.7/site-packages/psycopg2/__init__.py:144: UserWarning: The psycopg2 wheel package will be renamed from release 2.8; in order to keep installing from binary please use "pip install psycopg2-binary" instead. For details see: <http://initd.org/psycopg/docs/install.html#binary-install-from-pypi>.
2026-10-07T17:23:30.1712791Z   """)
2026-10-07T17:23:33.0010231Z 
2026-10-07T17:23:33.0011016Z TASK [zabbix : Consultar os dados do sistema.] *********************************
2026-10-07T17:23:33.0011298Z fatal: [caddeapllx930.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "msg": "unable to connect to database: FATAL:  password authentication failed for user \"monitdbadm\"\nFATAL:  no pg_hba.conf entry for host \"10.122.156.88\", user \"monitdbadm\", database \"monitordb001\", no encryption\n"}
2026-10-07T17:23:33.0014306Z 
2026-10-07T17:23:33.0014960Z PLAY RECAP *********************************************************************
2026-10-07T17:23:33.0015419Z caddeapllx930.agil.nprd.caixa.gov.br : ok=24   changed=3    unreachable=0    failed=1    skipped=11   rescued=0    ignored=2   
2026-10-07T17:23:33.0015640Z 
2026-10-07T17:23:33.0016154Z Wednesday 07 October 2026  14:23:33 -0300 (0:00:02.894)       0:00:20.390 ***** 
2026-10-07T17:23:33.0016346Z =============================================================================== 
2026-10-07T17:23:33.0018140Z zabbix : Consultar os dados do sistema. --------------------------------- 2.89s
2026-10-07T17:23:33.0018642Z Gathering Facts --------------------------------------------------------- 1.93s
2026-10-07T17:23:33.0020011Z Install zabbix agent2 --------------------------------------------------- 1.76s
2026-10-07T17:23:33.0020823Z zabbix : Install libpcre2-8 - Red Hat 7 --------------------------------- 1.27s
2026-10-07T17:23:33.0021530Z zabbix : hostgroup create to Zabbix Az CEMOT ---------------------------- 1.04s
2026-10-07T17:23:33.0021893Z node_exporter : Criando o service do Node Exporter ---------------------- 0.82s
2026-10-07T17:23:33.0022114Z Instalando o filebeat versao 7.2.1 -------------------------------------- 0.80s
2026-10-07T17:23:33.0022354Z zabbix : template get to Zabbix Az CEMOT -------------------------------- 0.80s
2026-10-07T17:23:33.0022883Z zabbix : hostgroup get to Zabbix Az CEMOT ------------------------------- 0.76s
2026-10-07T17:23:33.0023150Z node_exporter : Copia o Apache Exporter para o servidor ----------------- 0.74s
2026-10-07T17:23:33.0023440Z zabbix : host create to Zabbix Az CEMOT --------------------------------- 0.70s
2026-10-07T17:23:33.0023652Z Garantindo que o zabbix_agent2 esta startado ---------------------------- 0.66s
2026-10-07T17:23:33.0023880Z Template a file to /etc/filebeat/filebeat.yml --------------------------- 0.65s
2026-10-07T17:23:33.0024101Z Template a file to /etc/zabbix_zabbix_agente.d/monit_agent2.conf -------- 0.65s
2026-10-07T17:23:33.0024321Z Criando o usuario "node_exporter" vinculado ao grupo "node_exporter" ---- 0.63s
2026-10-07T17:23:33.0024528Z Download RPM filebeat --------------------------------------------------- 0.58s
2026-10-07T17:23:33.0024742Z zabbix : proxy get to Zabbix Az CEMOT ----------------------------------- 0.57s
2026-10-07T17:23:33.0024943Z Verifica se existe servico zabbix-agent --------------------------------- 0.46s
2026-10-07T17:23:33.0025154Z Criando o grupo do "node_exporter" -------------------------------------- 0.45s
2026-10-07T17:23:33.0025363Z Verifiando o jxm_exporter esta instalado -------------------------------- 0.43s
2026-10-07T17:23:33.0025511Z Playbook run took 0 days, 0 hours, 0 minutes, 20 seconds
2026-10-07T17:23:33.0865836Z ##[error]Bash exited with code '2'.
2026-10-07T17:23:33.0868721Z ##[section]Finishing: Configurando Stack de Monitoração



essa aqui colocamos essa nota

Durante a etapa "Configurando Stack de Monitoração" da esteira esteira-jboss-vm, a consulta à base PostgreSQL falha na autenticação.
 
Origem: cadsvaprlx072 (10.122.155.67), agente Azure DevOps
Destino: 10.244.74.86:5432 / database monitordb001 / usuário monitdbadm
 
Validações realizadas:
 
Conectividade OK (nc/telnet na porta 5432).
Teste direto do agente com a senha configurada na esteira (conexão com SSL): FATAL: password authentication failed for user "monitdbadm".
 
A conexão com SSL é aceita pelo pg_hba.conf e rejeitada na senha. A mensagem "no pg_hba.conf entry ... no encryption" do log é apenas o fallback do cliente sem SSL, e não é a causa.
 
Solicitação: verificar se a senha do usuário monitdbadm foi alterada ou expirou (VALID UNTIL) e informar a credencial vigente, para atualização na esteira.


Histórico de Informações de Trabalho da Ordem de Trabalho
ID da Ordem de Trabalho	 WO0000081808304
Criado em	 06/10/2026 13:57:58
Criado por	 P656511
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezados, favor encerrar a demanda conforme propria nota da CEPRO
ID da Ordem de Trabalho	 WO0000081808304
Criado em	 06/10/2026 11:03:00
Criado por	 P565574
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezados,


Para solicitação de acesso específica para um usuário, a "Solicitação FICUS" deve ser aberta com informações necessárias para atendimento, caso precisem apenas de informação para verificação, por favor abrir na categoria de "informações de perfil de um usuário".


Atenciosamente,

P565574 – Plataforma Intermediária

HITSS/CEPRO20 - Gestão de Identidade e acesso
ID da Ordem de Trabalho	 WO0000081808304
Criado em	 06/10/2026 10:44:04
Criado por	 F710695
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezados,

Estamos com demandas da PI3 represadas por conta desta release.

Essa FICUS seria de responsabilidade de quem, logo que é uma demanda interna de esteiras.

Seria uma TE191 para esta esteira específica?

Preciso entender como podemos agilizar este atendimento.

Grato,

F710695
ID da Ordem de Trabalho	 WO0000081808304
Criado em	 06/10/2026 09:14:18
Criado por	 P768728
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezados,

Por não termos atuação nesse atendimento não podemos concluir a demanda na nossa fila.

Atte.

Esteira Devops NPRD
ID da Ordem de Trabalho	 WO0000081808304
Criado em	 05/10/2026 23:53:22
Criado por	 P779823
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezados,

Favor abrir uma Ficus para ajuste de perfil.

Informando o Real acesso HOST> PORTA > DATABASE .

Atenciosamente,
P779823 -  Plataforma Intermediária
HITSS/CEPRO20 - Gestão de Identidade e acesso


ID da Ordem de Trabalho	 WO0000081808304
Criado em	 05/10/2026 22:23:37
Criado por	 P972797
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 À CESTI

    Fiz a tentativa de conectar via SSH no host e não é possível, ele deve ser um postgres no Azure.

    Refiz o teste de liberação de firewall e o servidor cadsvaprlx072 (10.122.155.67) tem acesso ao IP  10.244.74.86 na porta 5432.

    Não consegui encontrar o nome do host de IP mas ele deve estar no Azure tal como está o servidor apontado pelo FQDN db-monit-prd.postgres.database.azure.com --> c6cdf8f79b7d.privatelink.postgres.database.azure.com (10.244.74.88) (exemplo)

     A mensagem de erro original, conforme observado em nota anterior, indica problemas de "Password".

     Neste caso sugiro encaminhar esta solicitação para a equipe de segurança que administra/armazena normalmente as senhas dos usuários.

Att.
   Jeandre Bernadelli Guerra
   DBA Suporte - CTIS

  
ID da Ordem de Trabalho	 WO0000081808304
Criado em	 05/10/2026 16:59:32
Criado por	 P796413
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 em investigação.
ID da Ordem de Trabalho	 WO0000081808304
Criado em	 05/10/2026 16:30:28
Criado por	 P686198
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 À EQUIPE DE BANCO DE DADOS
Prezados,

Durante a etapa "Configurando Stack de Monitoração" da esteira esteira-jboss-vm, a consulta à base PostgreSQL falha na autenticação.

Origem: cadsvaprlx072 (10.122.155.67), agente Azure DevOps
Destino: 10.244.74.86:5432 / database monitordb001 / usuário monitdbadm

Validações realizadas:

Conectividade OK (nc/telnet na porta 5432).
Teste direto do agente com a senha configurada na esteira (conexão com SSL): FATAL: password authentication failed for user "monitdbadm".

A conexão com SSL é aceita pelo pg_hba.conf e rejeitada na senha. A mensagem "no pg_hba.conf entry ... no encryption" do log é apenas o fallback do cliente sem SSL, e não é a causa.

Solicitação: verificar se a senha do usuário monitdbadm foi alterada ou expirou (VALID UNTIL) e informar a credencial vigente, para atualização na esteira.

Atenciosamente,

Rainier Barbosa dos Santos Viana

Analista
CTIS / CESTI Esteira DEVOPS DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081808304
Criado em	 05/10/2026 15:01:36
Criado por	 P507043
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezado(a),



Informamos que sua solicitação PRIORIZADA foi recebida .  



Nosso SLA para atendimento é de até 8h úteis, analisaremos a solicitação para nos certificarmos que o atendimento está dentro do escopo de atuação da nossa equipe.



Caso seja identificado que o atendimento não corresponde ao nosso escopo, a solicitação será redirecionada à equipe responsável.



Novas informações e atualizações serão registradas diretamente nesta WO.



Atte.



Esteira DEVOPS DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081808304
Criado em	 05/10/2026 14:42:27
Criado por	 P779479
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Demanda inicial sem viés de falha, erro, degradação ou
esgotamento de infraestrutura, serviço, máquina, armazenamento,
rotina ou situação que não esteja na iminência de tornar-se
incidente. Previsto atendimento em até 24 horas.

[CENTRAL-SID]
ID da Ordem de Trabalho	 WO0000081808304
Criado em	 05/10/2026 13:55:34
Criado por	 P768728
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezado(a),

Informamos que sua solicitação foi recebida.

Nosso SLA para atendimento é de até 24h úteis, analisaremos a solicitação para nos certificarmos que o atendimento está dentro do escopo de atuação da nossa equipe.

Caso seja identificado que o atendimento não corresponde ao nosso escopo, a solicitação será redirecionada à equipe responsável.

Novas informações e atualizações serão registradas diretamente nesta WO.

Atte.

Esteira Devops DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081808304
Criado em	 05/10/2026 13:48:36
Criado por	 Remedy Application Service
Origem de Comunicação	 E-mail
Exibir Acesso	 Interno
Notas	 Este ticket foi criado a partir do sistema de solicitação de serviço.
Impresso por P585600 em Quarta-feira, 07/10/2026 14:24:59
