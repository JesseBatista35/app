2026-10-26T12:51:06.3423050Z ##[section]Starting: Correção Artefato Final SIIFX-CAIXINHAS-BATCH
2026-10-26T12:51:06.3426481Z ==============================================================================
2026-10-26T12:51:06.3426565Z Task         : Bash
2026-10-26T12:51:06.3426610Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-26T12:51:06.3426687Z Version      : 3.227.0
2026-10-26T12:51:06.3426732Z Author       : Microsoft Corporation
2026-10-26T12:51:06.3426792Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-26T12:51:06.3426865Z ==============================================================================
2026-10-26T12:51:06.4715997Z Generating script.
2026-10-26T12:51:06.4726564Z ========================== Starting Command Output ===========================
2026-10-26T12:51:06.4733774Z [command]/bin/bash /opt/ads-agent/_work/_temp/6d0de740-6175-4e37-b4db-ced31f18f049.sh
2026-10-26T12:51:06.5943903Z Versão: 0.0.10-SNAPSHOT
2026-10-26T12:51:06.6127700Z Artefato: http://binario.caixa:8081/repository/snapshots/br/gov/caixa/siifx/caixinhas/siifx-caixinhas-batch/0.0.10-SNAPSHOT/siifx-caixinhas-batch-0.0.10-20261023.110358-1.jar
2026-10-26T12:51:06.6174162Z   % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
2026-10-26T12:51:06.6174434Z                                  Dload  Upload   Total   Spent    Left  Speed
2026-10-26T12:51:06.6174496Z 
2026-10-26T12:51:06.8451825Z   0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
2026-10-26T12:51:06.8452265Z 100 29.1M  100 29.1M    0     0   127M      0 --:--:-- --:--:-- --:--:--  128M
2026-10-26T12:51:06.8478278Z total 29888
2026-10-26T12:51:06.8478698Z -rw-r--r-- 1 sadscp01 sadscp01    60819 Out 26 09:51 core-starter-1.0-20261023.110255-31.jar
2026-10-26T12:51:06.8479158Z -rw-r--r-- 1 sadscp01 sadscp01 30543335 Out 26 09:51 siifx-caixinhas-batch-0.0.10-20261023.110358-1.jar
2026-10-26T12:51:06.8533076Z ##[section]Finishing: Correção Artefato Final SIIFX-CAIXINHAS-BATCH

2026-10-26T12:51:34.9998553Z ##[section]Starting: Deploy Pacote
2026-10-26T12:51:35.0002697Z ==============================================================================
2026-10-26T12:51:35.0002784Z Task         : Bash
2026-10-26T12:51:35.0002852Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-26T12:51:35.0002932Z Version      : 3.227.0
2026-10-26T12:51:35.0002977Z Author       : Microsoft Corporation
2026-10-26T12:51:35.0003046Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-26T12:51:35.0003121Z ==============================================================================
2026-10-26T12:51:35.1515623Z Generating script.
2026-10-26T12:51:35.1529790Z ========================== Starting Command Output ===========================
2026-10-26T12:51:35.1539088Z [command]/bin/bash /opt/ads-agent/_work/_temp/04ee6942-9468-4dd5-bedd-e2150ac9c3f7.sh
2026-10-26T12:51:35.1646052Z /opt/ads-agent/_work/_temp/04ee6942-9468-4dd5-bedd-e2150ac9c3f7.sh: line 2: quantidade_vm: comando não encontrado
2026-10-26T12:51:35.1673043Z ansible-playbook /opt/ads-agent/_work/r19346/a/esteira-jboss-vm-v2/site.yml --tags batch --skip-tags vm,monitoracao,autenticacao,git_conf,tsm,controlm -e sistema_ambiente=des -e sistema_nome=siifx-caixinhas-batch -e default_working_directory_tfs=/opt/ads-agent/_work/r19346/a -e build_repository_name_tfs=SIIFX-caixinhas-batch -e quantidade_vm= -e url_deploy=http://binario.caixa:8081/repository/snapshots/br/gov/caixa/siifx/caixinhas/siifx-caixinhas-batch/0.0.10-SNAPSHOT/siifx-caixinhas-batch-0.0.10-20261023.110358-1.jar -e package_path=/opt/ads-agent/_work/r19346/a/binario/siifx-caixinhas-batch-0.0.10-20261023.110358-1.jar -e site=ctc_nprd -e batch_deploy=true
2026-10-26T12:51:35.1678447Z /opt/ads-agent/_work/_temp/04ee6942-9468-4dd5-bedd-e2150ac9c3f7.sh: line 5: quantidade_vm: comando não encontrado
2026-10-26T12:51:37.6358651Z 
2026-10-26T12:51:37.6359439Z PLAY [local] *******************************************************************
2026-10-26T12:51:37.6716748Z 
2026-10-26T12:51:37.6717498Z PLAY [Configurando o DNS] ******************************************************
2026-10-26T12:51:37.8867347Z 
2026-10-26T12:51:37.8868207Z PLAY [local] *******************************************************************
2026-10-26T12:51:37.8906623Z 
2026-10-26T12:51:37.8907466Z PLAY [Verificando serviços] ****************************************************
2026-10-26T12:51:37.9003433Z 
2026-10-26T12:51:37.9003919Z PLAY [Configuração LDAP] *******************************************************
2026-10-26T12:51:37.9040523Z [WARNING]: Found variable using reserved name: when
2026-10-26T12:51:37.9046559Z 
2026-10-26T12:51:37.9046807Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:37.9158797Z 
2026-10-26T12:51:37.9159711Z PLAY [Stack Jboss] *************************************************************
2026-10-26T12:51:37.9418811Z Monday 26 October 2026  09:51:37 -0300 (0:00:00.372)       0:00:00.372 ******** 
2026-10-26T12:51:38.5114819Z 
2026-10-26T12:51:38.5116050Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-10-26T12:51:38.5116344Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:51:38.5116647Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-26T12:51:38.5117046Z caddeapllx2695.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-26T12:51:38.5117369Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-26T12:51:38.5117649Z releases. A future Ansible release will default to using the discovered 
2026-10-26T12:51:38.5117946Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-26T12:51:38.5118256Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-26T12:51:38.5118548Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-26T12:51:38.5118821Z setting deprecation_warnings=False in ansible.cfg.
2026-10-26T12:51:38.5142784Z 
2026-10-26T12:51:38.5143981Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:38.5208675Z 
2026-10-26T12:51:38.5209225Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:38.5253129Z 
2026-10-26T12:51:38.5253588Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:38.5286969Z 
2026-10-26T12:51:38.5287717Z PLAY [Copiando deployments adicionais] *****************************************
2026-10-26T12:51:38.5315414Z 
2026-10-26T12:51:38.5315851Z PLAY [Copiando modules adicionais] *********************************************
2026-10-26T12:51:38.5347629Z 
2026-10-26T12:51:38.5348149Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:38.5384335Z 
2026-10-26T12:51:38.5385023Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:38.5418529Z 
2026-10-26T12:51:38.5419105Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:38.5461432Z 
2026-10-26T12:51:38.5462166Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:38.5489097Z 
2026-10-26T12:51:38.5489710Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:38.5516352Z 
2026-10-26T12:51:38.5516742Z PLAY [local] *******************************************************************
2026-10-26T12:51:38.5545740Z [WARNING]: Could not match supplied host pattern, ignoring: instance_restart
2026-10-26T12:51:38.5547877Z 
2026-10-26T12:51:38.5548512Z PLAY [instance_restart] ********************************************************
2026-10-26T12:51:38.5548711Z skipping: no hosts matched
2026-10-26T12:51:38.5550819Z [WARNING]: Could not match supplied host pattern, ignoring: machine_reboot
2026-10-26T12:51:38.5557514Z 
2026-10-26T12:51:38.5557966Z PLAY [machine_reboot] **********************************************************
2026-10-26T12:51:38.5558242Z skipping: no hosts matched
2026-10-26T12:51:38.5564276Z 
2026-10-26T12:51:38.5564501Z PLAY [local] *******************************************************************
2026-10-26T12:51:38.5592495Z [WARNING]: Could not match supplied host pattern, ignoring: instance_stop
2026-10-26T12:51:38.5594327Z 
2026-10-26T12:51:38.5594681Z PLAY [instance_stop] ***********************************************************
2026-10-26T12:51:38.5594910Z skipping: no hosts matched
2026-10-26T12:51:38.5598216Z 
2026-10-26T12:51:38.5598590Z PLAY [machine_reboot] **********************************************************
2026-10-26T12:51:38.5598871Z skipping: no hosts matched
2026-10-26T12:51:38.5609267Z 
2026-10-26T12:51:38.5609663Z PLAY [local] *******************************************************************
2026-10-26T12:51:38.5637058Z [WARNING]: Could not match supplied host pattern, ignoring: escopo_execucao
2026-10-26T12:51:38.5641752Z 
2026-10-26T12:51:38.5641993Z PLAY [Executar o Start do Sirot Connector no escopo definido] ******************
2026-10-26T12:51:38.5642245Z skipping: no hosts matched
2026-10-26T12:51:38.5649055Z 
2026-10-26T12:51:38.5649248Z PLAY [local] *******************************************************************
2026-10-26T12:51:38.5680529Z 
2026-10-26T12:51:38.5681149Z PLAY [Executar o Stop do Sirot Connector] **************************************
2026-10-26T12:51:38.5681367Z skipping: no hosts matched
2026-10-26T12:51:38.5687561Z 
2026-10-26T12:51:38.5688096Z PLAY [Configura TSM] ***********************************************************
2026-10-26T12:51:38.5721246Z 
2026-10-26T12:51:38.5751308Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:38.5751503Z 
2026-10-26T12:51:38.5752158Z PLAY [Configura Control-M] *****************************************************
2026-10-26T12:51:38.5788853Z 
2026-10-26T12:51:38.5789363Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:38.5831218Z 
2026-10-26T12:51:38.5831723Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:38.5874061Z 
2026-10-26T12:51:38.5874668Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:38.5913222Z Monday 26 October 2026  09:51:38 -0300 (0:00:00.649)       0:00:01.021 ******** 
2026-10-26T12:51:41.6878370Z 
2026-10-26T12:51:41.6879253Z TASK [Gathering Facts] *********************************************************
2026-10-26T12:51:41.6879476Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:51:41.7344779Z Monday 26 October 2026  09:51:41 -0300 (0:00:03.142)       0:00:04.164 ******** 
2026-10-26T12:51:41.7853138Z 
2026-10-26T12:51:41.7854733Z TASK [Gerando lista de secure files] *******************************************
2026-10-26T12:51:41.7855516Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:51:41.7878130Z 
2026-10-26T12:51:41.7879105Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:41.8176996Z Monday 26 October 2026  09:51:41 -0300 (0:00:00.083)       0:00:04.247 ******** 
2026-10-26T12:51:42.4655455Z 
2026-10-26T12:51:42.4657224Z TASK [Gathering Facts] *********************************************************
2026-10-26T12:51:42.4658022Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:51:42.4981332Z Monday 26 October 2026  09:51:42 -0300 (0:00:00.680)       0:00:04.928 ******** 
2026-10-26T12:51:43.0367038Z 
2026-10-26T12:51:43.0368102Z TASK [Cria Diretórios em /opt/batch/] ******************************************
2026-10-26T12:51:43.0368455Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => (item=/opt/batch)
2026-10-26T12:51:43.2605879Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => (item=/opt/batch/config)
2026-10-26T12:51:43.4741959Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => (item=/opt/batch/deploy)
2026-10-26T12:51:43.6877699Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => (item=/opt/batch/securefiles)
2026-10-26T12:51:43.7211770Z Monday 26 October 2026  09:51:43 -0300 (0:00:01.223)       0:00:06.151 ******** 
2026-10-26T12:51:43.7952499Z Monday 26 October 2026  09:51:43 -0300 (0:00:00.073)       0:00:06.225 ******** 
2026-10-26T12:51:43.8751104Z included: /opt/ads-agent/_work/r19346/a/esteira-jboss-vm-v2/roles/batch/tasks/batch_deploy.yml for caddeapllx2695.agil.nprd.caixa.gov.br
2026-10-26T12:51:43.9016483Z Monday 26 October 2026  09:51:43 -0300 (0:00:00.106)       0:00:06.331 ******** 
2026-10-26T12:51:43.9607795Z 
2026-10-26T12:51:43.9608935Z TASK [Cria variáveis] **********************************************************
2026-10-26T12:51:43.9609400Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:51:43.9884064Z Monday 26 October 2026  09:51:43 -0300 (0:00:00.086)       0:00:06.418 ******** 
2026-10-26T12:51:44.4645347Z 
2026-10-26T12:51:44.4646171Z TASK [Get path of deploy] ******************************************************
2026-10-26T12:51:44.4646915Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br] => (item=http://binario.caixa:8081/repository/snapshots/br/gov/caixa/siifx/caixinhas/siifx-caixinhas-batch/0.0.10-SNAPSHOT/siifx-caixinhas-batch-0.0.10-20261023.110358-1.jar)
2026-10-26T12:51:44.4931872Z Monday 26 October 2026  09:51:44 -0300 (0:00:00.504)       0:00:06.923 ******** 
2026-10-26T12:51:44.5556377Z 
2026-10-26T12:51:44.5557022Z TASK [set package_urls] ********************************************************
2026-10-26T12:51:44.5557345Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:51:44.5947328Z Monday 26 October 2026  09:51:44 -0300 (0:00:00.101)       0:00:07.024 ******** 
2026-10-26T12:51:45.1624503Z 
2026-10-26T12:51:45.1625246Z TASK [Verifica o se package existe] ********************************************
2026-10-26T12:51:45.1625810Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r19346/a/binario/siifx-caixinhas-batch-0.0.10-20261023.110358-1.jar)
2026-10-26T12:51:45.1926993Z Monday 26 October 2026  09:51:45 -0300 (0:00:00.598)       0:00:07.622 ******** 
2026-10-26T12:51:47.2310539Z 
2026-10-26T12:51:47.2311536Z TASK [Deploy do Pacote] ********************************************************
2026-10-26T12:51:47.2312476Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r19346/a/binario/siifx-caixinhas-batch-0.0.10-20261023.110358-1.jar)
2026-10-26T12:51:47.2661291Z Monday 26 October 2026  09:51:47 -0300 (0:00:02.073)       0:00:09.696 ******** 
2026-10-26T12:51:47.5288843Z 
2026-10-26T12:51:47.5289867Z TASK [Verifica se o arquivo /producao//configuration/custom-deploy.sh existe] ***
2026-10-26T12:51:47.5290156Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:51:47.5679657Z Monday 26 October 2026  09:51:47 -0300 (0:00:00.301)       0:00:09.998 ******** 
2026-10-26T12:51:47.6410295Z Monday 26 October 2026  09:51:47 -0300 (0:00:00.072)       0:00:10.071 ******** 
2026-10-26T12:51:47.7137187Z Monday 26 October 2026  09:51:47 -0300 (0:00:00.072)       0:00:10.143 ******** 
2026-10-26T12:51:47.7873319Z included: /opt/ads-agent/_work/r19346/a/esteira-jboss-vm-v2/roles/batch/tasks/batch_logs.yml for caddeapllx2695.agil.nprd.caixa.gov.br
2026-10-26T12:51:47.8165611Z Monday 26 October 2026  09:51:47 -0300 (0:00:00.102)       0:00:10.246 ******** 
2026-10-26T12:51:48.2983918Z 
2026-10-26T12:51:48.2985245Z TASK [Criacao diretorio /logs/batch] *******************************************
2026-10-26T12:51:48.2985974Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:51:48.3025311Z 
2026-10-26T12:51:48.3026655Z PLAY [localhost] ***************************************************************
2026-10-26T12:51:48.3067254Z 
2026-10-26T12:51:48.3067786Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:48.3117070Z 
2026-10-26T12:51:48.3117718Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:48.3160382Z 
2026-10-26T12:51:48.3161177Z PLAY [jboss] *******************************************************************
2026-10-26T12:51:48.3200994Z 
2026-10-26T12:51:48.3201652Z PLAY RECAP *********************************************************************
2026-10-26T12:51:48.3202107Z caddeapllx2695.agil.nprd.caixa.gov.br : ok=14   changed=2    unreachable=0    failed=0    skipped=3    rescued=0    ignored=0   
2026-10-26T12:51:48.3202229Z 
2026-10-26T12:51:48.3202913Z Monday 26 October 2026  09:51:48 -0300 (0:00:00.504)       0:00:10.750 ******** 
2026-10-26T12:51:48.3203150Z =============================================================================== 
2026-10-26T12:51:48.3203969Z Gathering Facts --------------------------------------------------------- 3.14s
2026-10-26T12:51:48.3204316Z Deploy do Pacote -------------------------------------------------------- 2.07s
2026-10-26T12:51:48.3204624Z Cria Diretórios em /opt/batch/ ------------------------------------------ 1.22s
2026-10-26T12:51:48.3204965Z Gathering Facts --------------------------------------------------------- 0.68s
2026-10-26T12:51:48.3205254Z Verifica ser o Jboss já foi instalado ----------------------------------- 0.65s
2026-10-26T12:51:48.3206292Z Verifica o se package existe -------------------------------------------- 0.60s
2026-10-26T12:51:48.3206955Z Get path of deploy ------------------------------------------------------ 0.50s
2026-10-26T12:51:48.3207402Z Criacao diretorio /logs/batch ------------------------------------------- 0.50s
2026-10-26T12:51:48.3207812Z Verifica se o arquivo /producao//configuration/custom-deploy.sh existe --- 0.30s
2026-10-26T12:51:48.3208517Z include_tasks ----------------------------------------------------------- 0.11s
2026-10-26T12:51:48.3208874Z include_tasks ----------------------------------------------------------- 0.10s
2026-10-26T12:51:48.3209269Z set package_urls -------------------------------------------------------- 0.10s
2026-10-26T12:51:48.3209689Z Cria variáveis ---------------------------------------------------------- 0.09s
2026-10-26T12:51:48.3210154Z Gerando lista de secure files ------------------------------------------- 0.08s
2026-10-26T12:51:48.3210903Z include_tasks ----------------------------------------------------------- 0.07s
2026-10-26T12:51:48.3211301Z Executa shell customizada ----------------------------------------------- 0.07s
2026-10-26T12:51:48.3211692Z include_tasks ----------------------------------------------------------- 0.07s
2026-10-26T12:51:48.3212044Z Playbook run took 0 days, 0 hours, 0 minutes, 10 seconds
2026-10-26T12:51:48.4522744Z ##[section]Finishing: Deploy Pacote



2026-10-26T12:51:58.6734161Z ##[section]Starting: Configura Control-M
2026-10-26T12:51:58.6740251Z ==============================================================================
2026-10-26T12:51:58.6740342Z Task         : Bash
2026-10-26T12:51:58.6740388Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-26T12:51:58.6740469Z Version      : 3.227.0
2026-10-26T12:51:58.6740517Z Author       : Microsoft Corporation
2026-10-26T12:51:58.6740592Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-26T12:51:58.6740670Z ==============================================================================
2026-10-26T12:51:58.8354286Z Generating script.
2026-10-26T12:51:58.8367548Z ========================== Starting Command Output ===========================
2026-10-26T12:51:58.8375790Z [command]/bin/bash /opt/ads-agent/_work/_temp/91e28dbc-d70c-45a8-8dc4-4eb16e88efa9.sh
2026-10-26T12:52:01.3583263Z 
2026-10-26T12:52:01.3584434Z PLAY [local] *******************************************************************
2026-10-26T12:52:01.3916442Z 
2026-10-26T12:52:01.3917118Z PLAY [Configurando o DNS] ******************************************************
2026-10-26T12:52:01.6585368Z 
2026-10-26T12:52:01.6586160Z PLAY [local] *******************************************************************
2026-10-26T12:52:01.6624565Z 
2026-10-26T12:52:01.6625464Z PLAY [Verificando serviços] ****************************************************
2026-10-26T12:52:01.6727554Z 
2026-10-26T12:52:01.6728754Z PLAY [Configuração LDAP] *******************************************************
2026-10-26T12:52:01.6768734Z [WARNING]: Found variable using reserved name: when
2026-10-26T12:52:01.6772231Z 
2026-10-26T12:52:01.6772951Z PLAY [jboss] *******************************************************************
2026-10-26T12:52:01.6877698Z 
2026-10-26T12:52:01.6878945Z PLAY [Stack Jboss] *************************************************************
2026-10-26T12:52:01.6910713Z 
2026-10-26T12:52:01.6911668Z PLAY [jboss] *******************************************************************
2026-10-26T12:52:01.6956328Z 
2026-10-26T12:52:01.6956811Z PLAY [jboss] *******************************************************************
2026-10-26T12:52:01.7259085Z Monday 26 October 2026  09:52:01 -0300 (0:00:00.437)       0:00:00.437 ******** 
2026-10-26T12:52:02.4746566Z 
2026-10-26T12:52:02.4747292Z TASK [Verifica se o arquivo nfs_config.json existe] ****************************
2026-10-26T12:52:02.4747542Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:02.4782485Z Monday 26 October 2026  09:52:02 -0300 (0:00:00.752)       0:00:01.190 ******** 
2026-10-26T12:52:02.5411929Z included: /opt/ads-agent/_work/r19346/a/esteira-jboss-vm-v2/roles/nfs/tasks/get_nfs.yml for caddeapllx2695.agil.nprd.caixa.gov.br
2026-10-26T12:52:02.5473157Z Monday 26 October 2026  09:52:02 -0300 (0:00:00.069)       0:00:01.259 ******** 
2026-10-26T12:52:02.6117812Z 
2026-10-26T12:52:02.6118981Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-26T12:52:02.6119314Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:02.6182851Z Monday 26 October 2026  09:52:02 -0300 (0:00:00.070)       0:00:01.330 ******** 
2026-10-26T12:52:03.2476958Z 
2026-10-26T12:52:03.2478064Z TASK [nfs : Coletar variáveis de ambiente] *************************************
2026-10-26T12:52:03.2478323Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:03.2522796Z Monday 26 October 2026  09:52:03 -0300 (0:00:00.634)       0:00:01.964 ******** 
2026-10-26T12:52:03.3143237Z 
2026-10-26T12:52:03.3144090Z TASK [nfs : Exibir resultado em JSON] ******************************************
2026-10-26T12:52:03.3145171Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-26T12:52:03.3145762Z     "nfs_vars_json": {
2026-10-26T12:52:03.3145942Z         "changed": false, 
2026-10-26T12:52:03.3146350Z         "cmd": "cat /opt/ads-agent/_work/r19346/a/nfs_config.json", 
2026-10-26T12:52:03.3146579Z         "delta": "0:00:00.045986", 
2026-10-26T12:52:03.3147149Z         "end": "2026-10-26 09:52:03.223957", 
2026-10-26T12:52:03.3147290Z         "failed": false, 
2026-10-26T12:52:03.3147414Z         "rc": 0, 
2026-10-26T12:52:03.3147592Z         "start": "2026-10-26 09:52:03.177971", 
2026-10-26T12:52:03.3147732Z         "stderr": "", 
2026-10-26T12:52:03.3147853Z         "stderr_lines": [], 
2026-10-26T12:52:03.3148296Z         "stdout": "[{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH\",\"NFS_MOUNT_POINT_ISILON\": \"/SIIFX\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX\",\"NFS_MOUNT_POINT_ISILON_2\": \"/SIIFX_B2B\"}]", 
2026-10-26T12:52:03.3148571Z         "stdout_lines": [
2026-10-26T12:52:03.3148997Z             "[{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH\",\"NFS_MOUNT_POINT_ISILON\": \"/SIIFX\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX\",\"NFS_MOUNT_POINT_ISILON_2\": \"/SIIFX_B2B\"}]"
2026-10-26T12:52:03.3149231Z         ]
2026-10-26T12:52:03.3149333Z     }
2026-10-26T12:52:03.3149422Z }
2026-10-26T12:52:03.3191184Z Monday 26 October 2026  09:52:03 -0300 (0:00:00.066)       0:00:02.031 ******** 
2026-10-26T12:52:03.3875227Z 
2026-10-26T12:52:03.3876332Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-26T12:52:03.3876528Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:03.3933364Z Monday 26 October 2026  09:52:03 -0300 (0:00:00.074)       0:00:02.105 ******** 
2026-10-26T12:52:07.6719483Z 
2026-10-26T12:52:07.6720137Z TASK [nfs : execute montagem script] *******************************************
2026-10-26T12:52:07.6720322Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:07.6765206Z Monday 26 October 2026  09:52:07 -0300 (0:00:04.283)       0:00:06.388 ******** 
2026-10-26T12:52:07.7447007Z 
2026-10-26T12:52:07.7447720Z TASK [nfs : ansible.builtin.debug] *********************************************
2026-10-26T12:52:07.7450795Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-26T12:52:07.7451054Z     "changed": false, 
2026-10-26T12:52:07.7451243Z     "msg": {
2026-10-26T12:52:07.7451449Z         "changed": true, 
2026-10-26T12:52:07.7451634Z         "cmd": [
2026-10-26T12:52:07.7451811Z             "python", 
2026-10-26T12:52:07.7452583Z             "/opt/ads-agent/_work/r19346/a/esteira-jboss-vm-v2/roles/nfs/files/nfs.py", 
2026-10-26T12:52:07.7452826Z             "montagem", 
2026-10-26T12:52:07.7453079Z             "siifx-caixinhas-batch", 
2026-10-26T12:52:07.7453282Z             "des", 
2026-10-26T12:52:07.7453436Z             "ctc_nprd", 
2026-10-26T12:52:07.7453720Z             "/opt/ads-agent/_work/r19346/a/esteira-jboss-vm-v2", 
2026-10-26T12:52:07.7453924Z             "C&t@d02", 
2026-10-26T12:52:07.7454240Z             "***", 
2026-10-26T12:52:07.7454417Z             "s736651@corp.caixa.gov.br", 
2026-10-26T12:52:07.7454617Z             "***", 
2026-10-26T12:52:07.7455227Z             "[{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH\",\"NFS_MOUNT_POINT_ISILON\": \"/SIIFX\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX\",\"NFS_MOUNT_POINT_ISILON_2\": \"/SIIFX_B2B\"}]"
2026-10-26T12:52:07.7455653Z         ], 
2026-10-26T12:52:07.7455863Z         "delta": "0:00:03.823143", 
2026-10-26T12:52:07.7456129Z         "end": "2026-10-26 09:52:07.644811", 
2026-10-26T12:52:07.7456333Z         "failed": false, 
2026-10-26T12:52:07.7456499Z         "rc": 0, 
2026-10-26T12:52:07.7457329Z         "start": "2026-10-26 09:52:03.821668", 
2026-10-26T12:52:07.7457531Z         "stderr": "", 
2026-10-26T12:52:07.7457717Z         "stderr_lines": [], 
2026-10-26T12:52:07.7460023Z         "stdout": "[{u'NFS_MOUNT_POINT_ISILON': u'/SIIFX', u'NFS_ENDPOINT_ISILON': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH'}, {u'NFS_MOUNT_POINT_ISILON_2': u'/SIIFX_B2B', u'NFS_ENDPOINT_ISILON_2': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX'}]\nNome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           \n------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH /SIIFX                              ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/SIIFX\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH /SIIFX                              ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX /SIIFX_B2B                          ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/SIIFX_B2B\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX /SIIFX_B2B                          ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-26T12:52:07.7461424Z         "stdout_lines": [
2026-10-26T12:52:07.7462059Z             "[{u'NFS_MOUNT_POINT_ISILON': u'/SIIFX', u'NFS_ENDPOINT_ISILON': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH'}, {u'NFS_MOUNT_POINT_ISILON_2': u'/SIIFX_B2B', u'NFS_ENDPOINT_ISILON_2': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX'}]", 
2026-10-26T12:52:07.7462653Z             "Nome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           ", 
2026-10-26T12:52:07.7463186Z             "------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------", 
2026-10-26T12:52:07.7463752Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH /SIIFX                              ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-26T12:52:07.7464052Z             "nfs_path=/SIIFX", 
2026-10-26T12:52:07.7464345Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH", 
2026-10-26T12:52:07.7464847Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH /SIIFX                              ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-26T12:52:07.7465215Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX /SIIFX_B2B                          ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-26T12:52:07.7465500Z             "nfs_path=/SIIFX_B2B", 
2026-10-26T12:52:07.7465716Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX", 
2026-10-26T12:52:07.7466260Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX /SIIFX_B2B                          ISILON                              nfsctcnprd.ctc.caixa                des                                "
2026-10-26T12:52:07.7466487Z         ]
2026-10-26T12:52:07.7466792Z     }
2026-10-26T12:52:07.7466929Z }
2026-10-26T12:52:07.7492185Z Monday 26 October 2026  09:52:07 -0300 (0:00:00.072)       0:00:06.461 ******** 
2026-10-26T12:52:08.1322234Z 
2026-10-26T12:52:08.1323106Z TASK [nfs : execute clean json] ************************************************
2026-10-26T12:52:08.1323649Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-26T12:52:08.1329492Z caddeapllx2695.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-26T12:52:08.1329835Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-26T12:52:08.1330116Z releases. A future Ansible release will default to using the discovered 
2026-10-26T12:52:08.1330398Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-26T12:52:08.1330585Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-26T12:52:08.1330836Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-26T12:52:08.1331067Z setting deprecation_warnings=False in ansible.cfg.
2026-10-26T12:52:08.1331269Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:08.1365645Z Monday 26 October 2026  09:52:08 -0300 (0:00:00.387)       0:00:06.849 ******** 
2026-10-26T12:52:08.2079028Z 
2026-10-26T12:52:08.2079862Z TASK [nfs : result_new_string_json] ********************************************
2026-10-26T12:52:08.2080743Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-26T12:52:08.2080948Z     "msg": {
2026-10-26T12:52:08.2081079Z         "ansible_facts": {
2026-10-26T12:52:08.2081230Z             "discovered_interpreter_python": "/usr/bin/python"
2026-10-26T12:52:08.2081415Z         }, 
2026-10-26T12:52:08.2081581Z         "changed": true, 
2026-10-26T12:52:08.2082591Z         "cmd": "echo '[{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH\",\"NFS_MOUNT_POINT_ISILON\": \"/SIIFX\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX\",\"NFS_MOUNT_POINT_ISILON_2\": \"/SIIFX_B2B\"}]' | sed 's/NFS_ENDPOINT_ISILON[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_ISILON[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_HUAWEI[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_HUAWEI[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_VM[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_VM[^\"]*/NFS_MOUNT_POINT/g'", 
2026-10-26T12:52:08.2083158Z         "delta": "0:00:00.003742", 
2026-10-26T12:52:08.2083287Z         "deprecations": [
2026-10-26T12:52:08.2083401Z             {
2026-10-26T12:52:08.2083963Z                 "msg": "Distribution rhel 9.3 on host caddeapllx2695.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, but is using /usr/bin/python for backward compatibility with prior Ansible releases. A future Ansible release will default to using the discovered platform python for this host. See https://docs.ansible.com/ansible/2.9/reference_appendices/interpreter_discovery.html for more information", 
2026-10-26T12:52:08.2084276Z                 "version": "2.12"
2026-10-26T12:52:08.2084377Z             }
2026-10-26T12:52:08.2084482Z         ], 
2026-10-26T12:52:08.2084693Z         "end": "2026-10-26 09:52:08.109837", 
2026-10-26T12:52:08.2084830Z         "failed": false, 
2026-10-26T12:52:08.2084943Z         "rc": 0, 
2026-10-26T12:52:08.2085119Z         "start": "2026-10-26 09:52:08.106095", 
2026-10-26T12:52:08.2085250Z         "stderr": "", 
2026-10-26T12:52:08.2085370Z         "stderr_lines": [], 
2026-10-26T12:52:08.2085777Z         "stdout": "[{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH\",\"NFS_MOUNT_POINT\": \"/SIIFX\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX\",\"NFS_MOUNT_POINT\": \"/SIIFX_B2B\"}]", 
2026-10-26T12:52:08.2086414Z         "stdout_lines": [
2026-10-26T12:52:08.2086820Z             "[{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH\",\"NFS_MOUNT_POINT\": \"/SIIFX\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX\",\"NFS_MOUNT_POINT\": \"/SIIFX_B2B\"}]"
2026-10-26T12:52:08.2087174Z         ]
2026-10-26T12:52:08.2087276Z     }
2026-10-26T12:52:08.2087384Z }
2026-10-26T12:52:08.2119694Z Monday 26 October 2026  09:52:08 -0300 (0:00:00.075)       0:00:06.924 ******** 
2026-10-26T12:52:08.2801936Z 
2026-10-26T12:52:08.2802792Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-26T12:52:08.2802986Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:08.2839969Z Monday 26 October 2026  09:52:08 -0300 (0:00:00.072)       0:00:06.996 ******** 
2026-10-26T12:52:08.3487050Z 
2026-10-26T12:52:08.3487718Z TASK [nfs : result_new_json] ***************************************************
2026-10-26T12:52:08.3487930Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-26T12:52:08.3488068Z     "msg": [
2026-10-26T12:52:08.3488185Z         {
2026-10-26T12:52:08.3488598Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH", 
2026-10-26T12:52:08.3488785Z             "NFS_MOUNT_POINT": "/SIIFX"
2026-10-26T12:52:08.3488963Z         }, 
2026-10-26T12:52:08.3489075Z         {
2026-10-26T12:52:08.3489231Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX", 
2026-10-26T12:52:08.3489385Z             "NFS_MOUNT_POINT": "/SIIFX_B2B"
2026-10-26T12:52:08.3489501Z         }
2026-10-26T12:52:08.3489606Z     ]
2026-10-26T12:52:08.3489706Z }
2026-10-26T12:52:08.3527831Z Monday 26 October 2026  09:52:08 -0300 (0:00:00.068)       0:00:07.065 ******** 
2026-10-26T12:52:08.4282613Z included: /opt/ads-agent/_work/r19346/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2695.agil.nprd.caixa.gov.br
2026-10-26T12:52:08.4375694Z included: /opt/ads-agent/_work/r19346/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2695.agil.nprd.caixa.gov.br
2026-10-26T12:52:08.4442029Z Monday 26 October 2026  09:52:08 -0300 (0:00:00.091)       0:00:07.156 ******** 
2026-10-26T12:52:08.5069528Z 
2026-10-26T12:52:08.5070393Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-26T12:52:08.5070664Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:08.5110201Z Monday 26 October 2026  09:52:08 -0300 (0:00:00.066)       0:00:07.223 ******** 
2026-10-26T12:52:08.5740454Z 
2026-10-26T12:52:08.5741128Z TASK [nfs : debug] *************************************************************
2026-10-26T12:52:08.5741375Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-26T12:52:08.5741521Z     "msg": {
2026-10-26T12:52:08.5742106Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH", 
2026-10-26T12:52:08.5742526Z         "NFS_MOUNT_POINT": "/SIIFX"
2026-10-26T12:52:08.5742713Z     }
2026-10-26T12:52:08.5742843Z }
2026-10-26T12:52:08.5782707Z Monday 26 October 2026  09:52:08 -0300 (0:00:00.067)       0:00:07.290 ******** 
2026-10-26T12:52:08.6398827Z 
2026-10-26T12:52:08.6399558Z TASK [nfs : debug] *************************************************************
2026-10-26T12:52:08.6401529Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-26T12:52:08.6401685Z     "msg": "/SIIFX"
2026-10-26T12:52:08.6401877Z }
2026-10-26T12:52:08.6437316Z Monday 26 October 2026  09:52:08 -0300 (0:00:00.065)       0:00:07.356 ******** 
2026-10-26T12:52:08.7057064Z 
2026-10-26T12:52:08.7057689Z TASK [nfs : debug] *************************************************************
2026-10-26T12:52:08.7057941Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-26T12:52:08.7058380Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH"
2026-10-26T12:52:08.7059006Z }
2026-10-26T12:52:08.7117556Z Monday 26 October 2026  09:52:08 -0300 (0:00:00.067)       0:00:07.424 ******** 
2026-10-26T12:52:08.7778558Z 
2026-10-26T12:52:08.7779630Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-26T12:52:08.7779926Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-26T12:52:08.7780679Z     "changed": false, 
2026-10-26T12:52:08.7780856Z     "msg": "All assertions passed"
2026-10-26T12:52:08.7781025Z }
2026-10-26T12:52:08.7836840Z Monday 26 October 2026  09:52:08 -0300 (0:00:00.071)       0:00:07.495 ******** 
2026-10-26T12:52:12.3151726Z 
2026-10-26T12:52:12.3153252Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-26T12:52:12.3153485Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:12.3201230Z Monday 26 October 2026  09:52:12 -0300 (0:00:03.536)       0:00:11.032 ******** 
2026-10-26T12:52:13.1701462Z 
2026-10-26T12:52:13.1702536Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-26T12:52:13.1702842Z [WARNING]: Consider using the yum, dnf or zypper module rather than running
2026-10-26T12:52:13.1703420Z 'rpm'.  If you need to use command because yum, dnf or zypper is insufficient
2026-10-26T12:52:13.1703770Z you can add 'warn: false' to this command task or set 'command_warnings=False'
2026-10-26T12:52:13.1704052Z in ansible.cfg to get rid of this message.
2026-10-26T12:52:13.1708107Z fatal: [caddeapllx2695.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.584406", "end": "2026-10-26 09:52:13.150666", "msg": "non-zero return code", "rc": 1, "start": "2026-10-26 09:52:12.566260", "stderr": "aviso: /var/tmp/rpm-tmp.5PevHr: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.5PevHr: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-26T12:52:13.1709302Z ...ignoring
2026-10-26T12:52:13.1749585Z Monday 26 October 2026  09:52:13 -0300 (0:00:00.855)       0:00:11.887 ******** 
2026-10-26T12:52:13.9658445Z 
2026-10-26T12:52:13.9659152Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-26T12:52:13.9663564Z fatal: [caddeapllx2695.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.521177", "end": "2026-10-26 09:52:13.944708", "msg": "non-zero return code", "rc": 1, "start": "2026-10-26 09:52:13.423531", "stderr": "aviso: /var/tmp/rpm-tmp.qd8DuK: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.qd8DuK: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-26T12:52:13.9664766Z ...ignoring
2026-10-26T12:52:13.9709684Z Monday 26 October 2026  09:52:13 -0300 (0:00:00.795)       0:00:12.683 ******** 
2026-10-26T12:52:14.4690988Z 
2026-10-26T12:52:14.4691950Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-26T12:52:14.4692727Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:14.4743208Z Monday 26 October 2026  09:52:14 -0300 (0:00:00.503)       0:00:13.186 ******** 
2026-10-26T12:52:14.7459890Z 
2026-10-26T12:52:14.7460948Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-26T12:52:14.7461250Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:14.7508715Z Monday 26 October 2026  09:52:14 -0300 (0:00:00.276)       0:00:13.463 ******** 
2026-10-26T12:52:15.7562509Z 
2026-10-26T12:52:15.7563245Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-26T12:52:15.7563458Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:15.7631962Z Monday 26 October 2026  09:52:15 -0300 (0:00:01.012)       0:00:14.475 ******** 
2026-10-26T12:52:16.0372496Z 
2026-10-26T12:52:16.0373136Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-26T12:52:16.0373416Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:16.0414380Z Monday 26 October 2026  09:52:16 -0300 (0:00:00.278)       0:00:14.753 ******** 
2026-10-26T12:52:26.4991167Z 
2026-10-26T12:52:26.4991975Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-26T12:52:26.4992254Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:26.5044562Z Monday 26 October 2026  09:52:26 -0300 (0:00:10.462)       0:00:25.216 ******** 
2026-10-26T12:52:26.9847932Z 
2026-10-26T12:52:26.9848718Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-26T12:52:26.9849003Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:26.9894223Z Monday 26 October 2026  09:52:26 -0300 (0:00:00.484)       0:00:25.701 ******** 
2026-10-26T12:52:27.0511991Z Monday 26 October 2026  09:52:27 -0300 (0:00:00.061)       0:00:25.763 ******** 
2026-10-26T12:52:27.1143633Z 
2026-10-26T12:52:27.1144587Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-26T12:52:27.1144845Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:27.1192036Z Monday 26 October 2026  09:52:27 -0300 (0:00:00.068)       0:00:25.831 ******** 
2026-10-26T12:52:27.1826723Z 
2026-10-26T12:52:27.1827515Z TASK [nfs : debug] *************************************************************
2026-10-26T12:52:27.1827718Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-26T12:52:27.1827853Z     "msg": {
2026-10-26T12:52:27.1828011Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX", 
2026-10-26T12:52:27.1828203Z         "NFS_MOUNT_POINT": "/SIIFX_B2B"
2026-10-26T12:52:27.1828318Z     }
2026-10-26T12:52:27.1828492Z }
2026-10-26T12:52:27.1885095Z Monday 26 October 2026  09:52:27 -0300 (0:00:00.069)       0:00:25.900 ******** 
2026-10-26T12:52:27.2485157Z 
2026-10-26T12:52:27.2485841Z TASK [nfs : debug] *************************************************************
2026-10-26T12:52:27.2486063Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-26T12:52:27.2486187Z     "msg": "/SIIFX_B2B"
2026-10-26T12:52:27.2486301Z }
2026-10-26T12:52:27.2523266Z Monday 26 October 2026  09:52:27 -0300 (0:00:00.064)       0:00:25.964 ******** 
2026-10-26T12:52:27.3156266Z 
2026-10-26T12:52:27.3156944Z TASK [nfs : debug] *************************************************************
2026-10-26T12:52:27.3157133Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-26T12:52:27.3157300Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX"
2026-10-26T12:52:27.3157861Z }
2026-10-26T12:52:27.3199417Z Monday 26 October 2026  09:52:27 -0300 (0:00:00.067)       0:00:26.032 ******** 
2026-10-26T12:52:27.3849237Z 
2026-10-26T12:52:27.3850225Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-26T12:52:27.3850542Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-26T12:52:27.3850773Z     "changed": false, 
2026-10-26T12:52:27.3851548Z     "msg": "All assertions passed"
2026-10-26T12:52:27.3851981Z }
2026-10-26T12:52:27.3890962Z Monday 26 October 2026  09:52:27 -0300 (0:00:00.069)       0:00:26.101 ******** 
2026-10-26T12:52:30.0220770Z 
2026-10-26T12:52:30.0221605Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-26T12:52:30.0221903Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:30.0265304Z Monday 26 October 2026  09:52:30 -0300 (0:00:02.637)       0:00:28.738 ******** 
2026-10-26T12:52:30.8949999Z 
2026-10-26T12:52:30.8950727Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-26T12:52:30.8957469Z fatal: [caddeapllx2695.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.594033", "end": "2026-10-26 09:52:30.874961", "msg": "non-zero return code", "rc": 1, "start": "2026-10-26 09:52:30.280928", "stderr": "aviso: /var/tmp/rpm-tmp.a0f5w4: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.a0f5w4: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-26T12:52:30.8958191Z ...ignoring
2026-10-26T12:52:30.9010642Z Monday 26 October 2026  09:52:30 -0300 (0:00:00.874)       0:00:29.613 ******** 
2026-10-26T12:52:31.6929274Z 
2026-10-26T12:52:31.6930251Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-26T12:52:31.6934940Z fatal: [caddeapllx2695.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.535849", "end": "2026-10-26 09:52:31.674268", "msg": "non-zero return code", "rc": 1, "start": "2026-10-26 09:52:31.138419", "stderr": "aviso: /var/tmp/rpm-tmp.rHAWuu: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.rHAWuu: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-26T12:52:31.6935597Z ...ignoring
2026-10-26T12:52:31.6970925Z Monday 26 October 2026  09:52:31 -0300 (0:00:00.796)       0:00:30.409 ******** 
2026-10-26T12:52:31.9404726Z 
2026-10-26T12:52:31.9405677Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-26T12:52:31.9405926Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:31.9439820Z Monday 26 October 2026  09:52:31 -0300 (0:00:00.246)       0:00:30.656 ******** 
2026-10-26T12:52:32.1948518Z 
2026-10-26T12:52:32.1949053Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-26T12:52:32.1949693Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:32.1983765Z Monday 26 October 2026  09:52:32 -0300 (0:00:00.254)       0:00:30.910 ******** 
2026-10-26T12:52:32.8365090Z 
2026-10-26T12:52:32.8365695Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-26T12:52:32.8365866Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:32.8410361Z Monday 26 October 2026  09:52:32 -0300 (0:00:00.642)       0:00:31.553 ******** 
2026-10-26T12:52:33.0972904Z 
2026-10-26T12:52:33.0974101Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-26T12:52:33.0974277Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:33.1006365Z Monday 26 October 2026  09:52:33 -0300 (0:00:00.259)       0:00:31.813 ******** 
2026-10-26T12:52:43.5039051Z 
2026-10-26T12:52:43.5039745Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-26T12:52:43.5039921Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:43.5075523Z Monday 26 October 2026  09:52:43 -0300 (0:00:10.406)       0:00:42.220 ******** 
2026-10-26T12:52:43.7698748Z 
2026-10-26T12:52:43.7699246Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-26T12:52:43.7699402Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:43.7735190Z Monday 26 October 2026  09:52:43 -0300 (0:00:00.265)       0:00:42.486 ******** 
2026-10-26T12:52:43.8154948Z 
2026-10-26T12:52:43.8155178Z PLAY [jboss] *******************************************************************
2026-10-26T12:52:43.8183984Z 
2026-10-26T12:52:43.8184163Z PLAY [Copiando deployments adicionais] *****************************************
2026-10-26T12:52:43.8213518Z 
2026-10-26T12:52:43.8213673Z PLAY [Copiando modules adicionais] *********************************************
2026-10-26T12:52:43.8240415Z 
2026-10-26T12:52:43.8240580Z PLAY [jboss] *******************************************************************
2026-10-26T12:52:43.8281374Z 
2026-10-26T12:52:43.8281536Z PLAY [jboss] *******************************************************************
2026-10-26T12:52:43.8318650Z 
2026-10-26T12:52:43.8318875Z PLAY [jboss] *******************************************************************
2026-10-26T12:52:43.8356997Z 
2026-10-26T12:52:43.8357233Z PLAY [jboss] *******************************************************************
2026-10-26T12:52:43.8383379Z 
2026-10-26T12:52:43.8383716Z PLAY [jboss] *******************************************************************
2026-10-26T12:52:43.8407948Z 
2026-10-26T12:52:43.8408176Z PLAY [local] *******************************************************************
2026-10-26T12:52:43.8434273Z [WARNING]: Could not match supplied host pattern, ignoring: instance_restart
2026-10-26T12:52:43.8437517Z 
2026-10-26T12:52:43.8437743Z PLAY [instance_restart] ********************************************************
2026-10-26T12:52:43.8437896Z skipping: no hosts matched
2026-10-26T12:52:43.8440549Z [WARNING]: Could not match supplied host pattern, ignoring: machine_reboot
2026-10-26T12:52:43.8443569Z 
2026-10-26T12:52:43.8443804Z PLAY [machine_reboot] **********************************************************
2026-10-26T12:52:43.8443957Z skipping: no hosts matched
2026-10-26T12:52:43.8449910Z 
2026-10-26T12:52:43.8450541Z PLAY [local] *******************************************************************
2026-10-26T12:52:43.8475403Z [WARNING]: Could not match supplied host pattern, ignoring: instance_stop
2026-10-26T12:52:43.8478444Z 
2026-10-26T12:52:43.8478589Z PLAY [instance_stop] ***********************************************************
2026-10-26T12:52:43.8478950Z skipping: no hosts matched
2026-10-26T12:52:43.8481890Z 
2026-10-26T12:52:43.8482528Z PLAY [machine_reboot] **********************************************************
2026-10-26T12:52:43.8482679Z skipping: no hosts matched
2026-10-26T12:52:43.8488015Z 
2026-10-26T12:52:43.8488247Z PLAY [local] *******************************************************************
2026-10-26T12:52:43.8513940Z [WARNING]: Could not match supplied host pattern, ignoring: escopo_execucao
2026-10-26T12:52:43.8517225Z 
2026-10-26T12:52:43.8517483Z PLAY [Executar o Start do Sirot Connector no escopo definido] ******************
2026-10-26T12:52:43.8517842Z skipping: no hosts matched
2026-10-26T12:52:43.8523517Z 
2026-10-26T12:52:43.8523960Z PLAY [local] *******************************************************************
2026-10-26T12:52:43.8546154Z 
2026-10-26T12:52:43.8546402Z PLAY [Executar o Stop do Sirot Connector] **************************************
2026-10-26T12:52:43.8546553Z skipping: no hosts matched
2026-10-26T12:52:43.8556154Z 
2026-10-26T12:52:43.8556390Z PLAY [Configura TSM] ***********************************************************
2026-10-26T12:52:43.8583300Z 
2026-10-26T12:52:43.8583548Z PLAY [jboss] *******************************************************************
2026-10-26T12:52:43.8622793Z Monday 26 October 2026  09:52:43 -0300 (0:00:00.088)       0:00:42.574 ******** 
2026-10-26T12:52:43.9167658Z 
2026-10-26T12:52:43.9168177Z TASK [Cria variável build_repository_name] *************************************
2026-10-26T12:52:43.9168553Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:43.9196392Z Monday 26 October 2026  09:52:43 -0300 (0:00:00.057)       0:00:42.632 ******** 
2026-10-26T12:52:43.9740567Z 
2026-10-26T12:52:43.9742671Z TASK [Buscando diretorio de config] ********************************************
2026-10-26T12:52:43.9742887Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:43.9841238Z Monday 26 October 2026  09:52:43 -0300 (0:00:00.064)       0:00:42.696 ******** 
2026-10-26T12:52:44.4107448Z 
2026-10-26T12:52:44.4108547Z TASK [Verifica se o arquivo {{ item }}/etc/hosts-{{ sistema_ambiente }} existe] ***
2026-10-26T12:52:44.4108914Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r19346/a/_SIIFX-caixinhas-batch-config)
2026-10-26T12:52:44.6862819Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r19346/a/_SIIFX-caixinhas-batch-config/so)
2026-10-26T12:52:44.6903193Z Monday 26 October 2026  09:52:44 -0300 (0:00:00.706)       0:00:43.402 ******** 
2026-10-26T12:52:45.1180198Z 
2026-10-26T12:52:45.1180695Z TASK [Altera arquivo /etc/hosts] ***********************************************
2026-10-26T12:52:45.1182422Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r19346/a/_SIIFX-caixinhas-batch-config', u'stat': {u'charset': u'us-ascii', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1793019066.1068223, u'block_size': 4096, u'inode': 469786965, u'isgid': False, u'size': 30, u'wgrp': False, u'executable': False, u'isuid': False, u'readable': True, u'isreg': True, u'version': u'18446744073071157209', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'text/plain', u'blocks': 8, u'xoth': False, u'islnk': False, u'nlink': 1, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r19346/a/_SIIFX-caixinhas-batch-config/etc/hosts-des', u'xusr': False, u'atime': 1793019087.0196528, u'isdir': False, u'ctime': 1793019066.1078224, u'isblk': False, u'checksum': u'4a057994371ed4eef904eb2508abb8c246f35ff5', u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0644', u'xgrp': False, u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r19346/a/_SIIFX-caixinhas-batch-config/etc/hosts-des', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-26T12:52:45.1258805Z 
2026-10-26T12:52:45.1259048Z PLAY [Configura Control-M] *****************************************************
2026-10-26T12:52:45.1310874Z Monday 26 October 2026  09:52:45 -0300 (0:00:00.440)       0:00:43.843 ******** 
2026-10-26T12:52:45.7620649Z 
2026-10-26T12:52:45.7621194Z TASK [Gathering Facts] *********************************************************
2026-10-26T12:52:45.7621667Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:45.7813644Z Monday 26 October 2026  09:52:45 -0300 (0:00:00.650)       0:00:44.493 ******** 
2026-10-26T12:52:46.0290416Z 
2026-10-26T12:52:46.0291082Z TASK [stat] ********************************************************************
2026-10-26T12:52:46.0291512Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:46.0438775Z Monday 26 October 2026  09:52:46 -0300 (0:00:00.262)       0:00:44.756 ******** 
2026-10-26T12:52:46.1019634Z 
2026-10-26T12:52:46.1019961Z TASK [assert] ******************************************************************
2026-10-26T12:52:46.1020569Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-26T12:52:46.1020707Z     "changed": false, 
2026-10-26T12:52:46.1020924Z     "msg": "All assertions passed"
2026-10-26T12:52:46.1021042Z }
2026-10-26T12:52:46.1177404Z Monday 26 October 2026  09:52:46 -0300 (0:00:00.073)       0:00:44.830 ******** 
2026-10-26T12:52:46.1889220Z 
2026-10-26T12:52:46.1889767Z TASK [control_m : Cria variável ansible] ***************************************
2026-10-26T12:52:46.1889971Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:46.2037503Z Monday 26 October 2026  09:52:46 -0300 (0:00:00.085)       0:00:44.916 ******** 
2026-10-26T12:52:47.0037736Z 
2026-10-26T12:52:47.0038589Z TASK [control_m : Copiando arquivo de certificado] *****************************
2026-10-26T12:52:47.0038802Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:47.0200439Z Monday 26 October 2026  09:52:47 -0300 (0:00:00.816)       0:00:45.732 ******** 
2026-10-26T12:52:47.2716751Z 
2026-10-26T12:52:47.2717470Z TASK [control_m : Executando add-user.sh] **************************************
2026-10-26T12:52:47.2717663Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:47.2864072Z Monday 26 October 2026  09:52:47 -0300 (0:00:00.266)       0:00:45.999 ******** 
2026-10-26T12:52:47.6941355Z 
2026-10-26T12:52:47.6942534Z TASK [control_m : Removendo add-user.sh] ***************************************
2026-10-26T12:52:47.6942788Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:47.7091157Z Monday 26 October 2026  09:52:47 -0300 (0:00:00.422)       0:00:46.421 ******** 
2026-10-26T12:52:47.9603057Z 
2026-10-26T12:52:47.9603483Z TASK [control_m : Criacao diretorio /producao/carga] ***************************
2026-10-26T12:52:47.9604037Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:47.9751500Z Monday 26 October 2026  09:52:47 -0300 (0:00:00.265)       0:00:46.687 ******** 
2026-10-26T12:52:48.2260310Z 
2026-10-26T12:52:48.2260793Z TASK [control_m : Criacao diretorio /producao/suporte] *************************
2026-10-26T12:52:48.2260989Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:48.2409559Z Monday 26 October 2026  09:52:48 -0300 (0:00:00.265)       0:00:46.953 ******** 
2026-10-26T12:52:48.8052991Z 
2026-10-26T12:52:48.8053509Z TASK [control_m : Garante bash_profile] ****************************************
2026-10-26T12:52:48.8053703Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:48.8199628Z Monday 26 October 2026  09:52:48 -0300 (0:00:00.578)       0:00:47.532 ******** 
2026-10-26T12:52:49.0702287Z 
2026-10-26T12:52:49.0703028Z TASK [control_m : Cria Diretório de Scripts] ***********************************
2026-10-26T12:52:49.0703204Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:49.0853379Z Monday 26 October 2026  09:52:49 -0300 (0:00:00.265)       0:00:47.797 ******** 
2026-10-26T12:52:50.5436453Z 
2026-10-26T12:52:50.5436976Z TASK [control_m : Copia Scripts] ***********************************************
2026-10-26T12:52:50.5437444Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:50.5598559Z Monday 26 October 2026  09:52:50 -0300 (0:00:01.474)       0:00:49.272 ******** 
2026-10-26T12:52:50.8097624Z 
2026-10-26T12:52:50.8098062Z TASK [control_m : Verifica se o arquivo /producao//configuration/custom.sh existe] ***
2026-10-26T12:52:50.8098233Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:50.8249968Z Monday 26 October 2026  09:52:50 -0300 (0:00:00.265)       0:00:49.537 ******** 
2026-10-26T12:52:51.0755566Z 
2026-10-26T12:52:51.0755951Z TASK [control_m : Executa shell customizada] ***********************************
2026-10-26T12:52:51.0756125Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:51.0901980Z Monday 26 October 2026  09:52:51 -0300 (0:00:00.265)       0:00:49.802 ******** 
2026-10-26T12:52:51.7194249Z 
2026-10-26T12:52:51.7197613Z TASK [control_m : Configuração Control-M] **************************************
2026-10-26T12:52:51.7203337Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:52:51.7346576Z Monday 26 October 2026  09:52:51 -0300 (0:00:00.644)       0:00:50.447 ******** 
2026-10-26T12:53:16.8047406Z 
2026-10-26T12:53:16.8047918Z TASK [control_m : Restart ControlM] ********************************************
2026-10-26T12:53:16.8050067Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-26T12:53:16.8086553Z 
2026-10-26T12:53:16.8086890Z PLAY [jboss] *******************************************************************
2026-10-26T12:53:16.8131743Z 
2026-10-26T12:53:16.8131911Z PLAY [jboss] *******************************************************************
2026-10-26T12:53:16.8174820Z 
2026-10-26T12:53:16.8175098Z PLAY [jboss] *******************************************************************
2026-10-26T12:53:16.8201587Z 
2026-10-26T12:53:16.8201761Z PLAY [jboss] *******************************************************************
2026-10-26T12:53:16.8234448Z 
2026-10-26T12:53:16.8234666Z PLAY [localhost] ***************************************************************
2026-10-26T12:53:16.8258695Z 
2026-10-26T12:53:16.8258890Z PLAY [jboss] *******************************************************************
2026-10-26T12:53:16.8302685Z 
2026-10-26T12:53:16.8303099Z PLAY [jboss] *******************************************************************
2026-10-26T12:53:16.8343746Z 
2026-10-26T12:53:16.8344044Z PLAY [jboss] *******************************************************************
2026-10-26T12:53:16.8381412Z 
2026-10-26T12:53:16.8381565Z PLAY RECAP *********************************************************************
2026-10-26T12:53:16.8381853Z caddeapllx2695.agil.nprd.caixa.gov.br : ok=62   changed=20   unreachable=0    failed=0    skipped=2    rescued=0    ignored=4   
2026-10-26T12:53:16.8381959Z 
2026-10-26T12:53:16.8383858Z Monday 26 October 2026  09:53:16 -0300 (0:00:25.103)       0:01:15.550 ******** 
2026-10-26T12:53:16.8384054Z =============================================================================== 
2026-10-26T12:53:16.8388389Z control_m : Restart ControlM ------------------------------------------- 25.10s
2026-10-26T12:53:16.8389102Z nfs : Networker | Restart networker ------------------------------------ 10.46s
2026-10-26T12:53:16.8418697Z nfs : Networker | Restart networker ------------------------------------ 10.41s
2026-10-26T12:53:16.8419026Z nfs : execute montagem script ------------------------------------------- 4.28s
2026-10-26T12:53:16.8419300Z nfs : Instalando o NFS Client ------------------------------------------- 3.54s
2026-10-26T12:53:16.8419534Z nfs : Instalando o NFS Client ------------------------------------------- 2.64s
2026-10-26T12:53:16.8419767Z control_m : Copia Scripts ----------------------------------------------- 1.47s
2026-10-26T12:53:16.8420000Z nfs : Networker | Start networker --------------------------------------- 1.01s
2026-10-26T12:53:16.8420229Z nfs : Install networker lgtoclnt_url ------------------------------------ 0.87s
2026-10-26T12:53:16.8420458Z nfs : Install networker lgtoclnt_url ------------------------------------ 0.86s
2026-10-26T12:53:16.8420925Z control_m : Copiando arquivo de certificado ----------------------------- 0.82s
2026-10-26T12:53:16.8421151Z nfs : Install networker lgtonmda_url ------------------------------------ 0.80s
2026-10-26T12:53:16.8421372Z nfs : Install networker lgtonmda_url ------------------------------------ 0.80s
2026-10-26T12:53:16.8421712Z Verifica se o arquivo nfs_config.json existe ---------------------------- 0.75s
2026-10-26T12:53:16.8421943Z Verifica se o arquivo {{ item }}/etc/hosts-{{ sistema_ambiente }} existe --- 0.71s
2026-10-26T12:53:16.8422167Z Gathering Facts --------------------------------------------------------- 0.65s
2026-10-26T12:53:16.8422515Z control_m : Configuração Control-M -------------------------------------- 0.64s
2026-10-26T12:53:16.8422751Z nfs : Networker | Start networker --------------------------------------- 0.64s
2026-10-26T12:53:16.8422989Z nfs : Coletar variáveis de ambiente ------------------------------------- 0.63s
2026-10-26T12:53:16.8423223Z control_m : Garante bash_profile ---------------------------------------- 0.58s
2026-10-26T12:53:16.8423379Z Playbook run took 0 days, 0 hours, 1 minutes, 15 seconds
2026-10-26T12:53:16.9144393Z ##[section]Finishing: Configura Control-M




rodei a release passou


