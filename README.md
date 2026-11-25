2026-11-25T13:39:39.4122142Z ##[section]Starting: Definir size como executado
2026-11-25T13:39:39.4125666Z ==============================================================================
2026-11-25T13:39:39.4125759Z Task         : Bash
2026-11-25T13:39:39.4125802Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-11-25T13:39:39.4125876Z Version      : 3.227.0
2026-11-25T13:39:39.4125918Z Author       : Microsoft Corporation
2026-11-25T13:39:39.4125979Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-11-25T13:39:39.4126052Z ==============================================================================
2026-11-25T13:39:40.2031242Z Generating script.
2026-11-25T13:39:40.2048541Z ========================== Starting Command Output ===========================
2026-11-25T13:39:40.2057795Z [command]/bin/bash /opt/ads-agent/_work/_temp/64a0310d-bb8e-4178-96bd-45d3be705d1d.sh
2026-11-25T13:39:40.2124030Z ++ echo _SIGSJ-internet
2026-11-25T13:39:40.2125613Z ++ sed s/_//
2026-11-25T13:39:40.2134011Z + REPO=SIGSJ-internet
2026-11-25T13:39:40.2136085Z + ansible-playbook /opt/ads-agent/_work/r6259/a/esteira-jboss-vm-v2/site.yml --tags size_executado -e sistema_ambiente=des -e sistema_nome=sigsj-internet -e site=ctc_nprd -e quantidade_vm=1 -e centralizadora_operacoes=7259 -e centralizadora_desenvolvimento=7390 -e default_working_directory_tfs=/opt/ads-agent/_work/r6259/a -e build_repository_name_tfs=SIGSJ-internet
2026-11-25T13:39:42.5092819Z 
2026-11-25T13:39:42.5093378Z PLAY [local] *******************************************************************
2026-11-25T13:39:42.5405404Z 
2026-11-25T13:39:42.5405910Z PLAY [Configurando o DNS] ******************************************************
2026-11-25T13:39:42.7373841Z 
2026-11-25T13:39:42.7374382Z PLAY [local] *******************************************************************
2026-11-25T13:39:42.7405738Z 
2026-11-25T13:39:42.7406197Z PLAY [Verificando serviços] ****************************************************
2026-11-25T13:39:42.7495125Z 
2026-11-25T13:39:42.7495628Z PLAY [Configuração LDAP] *******************************************************
2026-11-25T13:39:42.7537183Z [WARNING]: Found variable using reserved name: when
2026-11-25T13:39:42.7542494Z 
2026-11-25T13:39:42.7542645Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:42.7904216Z 
2026-11-25T13:39:42.7904644Z PLAY [Stack Jboss] *************************************************************
2026-11-25T13:39:42.8139577Z Wednesday 25 November 2026  10:39:42 -0300 (0:00:00.368)       0:00:00.368 **** 
2026-11-25T13:39:47.0060824Z [WARNING]: Unhandled error in Python interpreter discovery for host
2026-11-25T13:39:47.0061250Z caddeapllx2854.agil.nprd.caixa.gov.br: Invalid/incorrect username/password.
2026-11-25T13:39:47.0061521Z Skipping remaining 3 retries to prevent account lockout: Warning: Permanently
2026-11-25T13:39:47.0062086Z added '10.116.202.45' (ECDSA) to the list of known hosts.  Permission denied,
2026-11-25T13:39:47.0062222Z please try again.
2026-11-25T13:39:49.0581157Z 
2026-11-25T13:39:49.0581917Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-11-25T13:39:49.0582609Z fatal: [caddeapllx2854.agil.nprd.caixa.gov.br]: UNREACHABLE! => {"changed": false, "msg": "Invalid/incorrect username/password. Skipping remaining 3 retries to prevent account lockout: Warning: Permanently added '10.116.202.45' (ECDSA) to the list of known hosts.\r\nPermission denied, please try again.", "unreachable": true}
2026-11-25T13:39:49.0586704Z 
2026-11-25T13:39:49.0586943Z PLAY RECAP *********************************************************************
2026-11-25T13:39:49.0587135Z caddeapllx2854.agil.nprd.caixa.gov.br : ok=0    changed=0    unreachable=1    failed=0    skipped=0    rescued=0    ignored=0   
2026-11-25T13:39:49.0587220Z 
2026-11-25T13:39:49.0588772Z Wednesday 25 November 2026  10:39:49 -0300 (0:00:06.245)       0:00:06.613 **** 
2026-11-25T13:39:49.0589053Z =============================================================================== 
2026-11-25T13:39:49.0589605Z Verifica ser o Jboss já foi instalado ----------------------------------- 6.25s
2026-11-25T13:39:49.0589761Z Playbook run took 0 days, 0 hours, 0 minutes, 6 seconds
2026-11-25T13:39:49.1216959Z ##[error]Bash exited with code '4'.
2026-11-25T13:39:49.1246068Z ##[warning]RetryHelper encountered task failure, will retry (attempt #: 1 out of 5) after 1000 ms
2026-11-25T13:39:50.2049621Z Generating script.
2026-11-25T13:39:50.2064905Z ========================== Starting Command Output ===========================
2026-11-25T13:39:50.2074007Z [command]/bin/bash /opt/ads-agent/_work/_temp/7eeca065-f269-4551-96d7-671faf30e801.sh
2026-11-25T13:39:50.2127224Z ++ echo _SIGSJ-internet
2026-11-25T13:39:50.2127375Z ++ sed s/_//
2026-11-25T13:39:50.2136698Z + REPO=SIGSJ-internet
2026-11-25T13:39:50.2137271Z + ansible-playbook /opt/ads-agent/_work/r6259/a/esteira-jboss-vm-v2/site.yml --tags size_executado -e sistema_ambiente=des -e sistema_nome=sigsj-internet -e site=ctc_nprd -e quantidade_vm=1 -e centralizadora_operacoes=7259 -e centralizadora_desenvolvimento=7390 -e default_working_directory_tfs=/opt/ads-agent/_work/r6259/a -e build_repository_name_tfs=SIGSJ-internet
2026-11-25T13:39:52.5284723Z 
2026-11-25T13:39:52.5285268Z PLAY [local] *******************************************************************
2026-11-25T13:39:52.5588201Z 
2026-11-25T13:39:52.5588702Z PLAY [Configurando o DNS] ******************************************************
2026-11-25T13:39:52.7528137Z 
2026-11-25T13:39:52.7528774Z PLAY [local] *******************************************************************
2026-11-25T13:39:52.7558599Z 
2026-11-25T13:39:52.7559078Z PLAY [Verificando serviços] ****************************************************
2026-11-25T13:39:52.7645316Z 
2026-11-25T13:39:52.7645982Z PLAY [Configuração LDAP] *******************************************************
2026-11-25T13:39:52.7684865Z [WARNING]: Found variable using reserved name: when
2026-11-25T13:39:52.7689638Z 
2026-11-25T13:39:52.7690210Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:52.8060632Z 
2026-11-25T13:39:52.8061179Z PLAY [Stack Jboss] *************************************************************
2026-11-25T13:39:52.8289434Z Wednesday 25 November 2026  10:39:52 -0300 (0:00:00.362)       0:00:00.362 **** 
2026-11-25T13:39:57.0364532Z [WARNING]: Unhandled error in Python interpreter discovery for host
2026-11-25T13:39:57.0365501Z caddeapllx2854.agil.nprd.caixa.gov.br: Invalid/incorrect username/password.
2026-11-25T13:39:57.0365722Z Skipping remaining 3 retries to prevent account lockout: Warning: Permanently
2026-11-25T13:39:57.0366130Z added '10.116.202.45' (ECDSA) to the list of known hosts.  Permission denied,
2026-11-25T13:39:57.0366319Z please try again.
2026-11-25T13:39:57.7178593Z 
2026-11-25T13:39:57.7179489Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-11-25T13:39:57.7179740Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:39:57.7179993Z [WARNING]: Platform unknown on host caddeapllx2854.agil.nprd.caixa.gov.br is
2026-11-25T13:39:57.7180209Z using the discovered Python interpreter at /usr/bin/python, but future
2026-11-25T13:39:57.7180443Z installation of another Python interpreter could change this. See https://docs.
2026-11-25T13:39:57.7180611Z ansible.com/ansible/2.9/reference_appendices/interpreter_discovery.html for
2026-11-25T13:39:57.7180758Z more information.
2026-11-25T13:39:57.7212707Z 
2026-11-25T13:39:57.7213037Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:57.7260983Z 
2026-11-25T13:39:57.7261476Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:57.7305334Z 
2026-11-25T13:39:57.7305917Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:57.7328957Z 
2026-11-25T13:39:57.7329612Z PLAY [Copiando deployments adicionais] *****************************************
2026-11-25T13:39:57.7355163Z 
2026-11-25T13:39:57.7355507Z PLAY [Copiando modules adicionais] *********************************************
2026-11-25T13:39:57.7379523Z 
2026-11-25T13:39:57.7380214Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:57.7415508Z 
2026-11-25T13:39:57.7415768Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:57.7443650Z 
2026-11-25T13:39:57.7443986Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:57.7474856Z 
2026-11-25T13:39:57.7475408Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:57.7501447Z 
2026-11-25T13:39:57.7501798Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:57.7525923Z 
2026-11-25T13:39:57.7526246Z PLAY [local] *******************************************************************
2026-11-25T13:39:57.7552395Z [WARNING]: Could not match supplied host pattern, ignoring: instance_restart
2026-11-25T13:39:57.7554474Z 
2026-11-25T13:39:57.7554783Z PLAY [instance_restart] ********************************************************
2026-11-25T13:39:57.7555164Z skipping: no hosts matched
2026-11-25T13:39:57.7557623Z [WARNING]: Could not match supplied host pattern, ignoring: machine_reboot
2026-11-25T13:39:57.7560509Z 
2026-11-25T13:39:57.7560880Z PLAY [machine_reboot] **********************************************************
2026-11-25T13:39:57.7561091Z skipping: no hosts matched
2026-11-25T13:39:57.7566911Z 
2026-11-25T13:39:57.7567117Z PLAY [local] *******************************************************************
2026-11-25T13:39:57.7591726Z [WARNING]: Could not match supplied host pattern, ignoring: instance_stop
2026-11-25T13:39:57.7594781Z 
2026-11-25T13:39:57.7595122Z PLAY [instance_stop] ***********************************************************
2026-11-25T13:39:57.7595311Z skipping: no hosts matched
2026-11-25T13:39:57.7598166Z 
2026-11-25T13:39:57.7598380Z PLAY [machine_reboot] **********************************************************
2026-11-25T13:39:57.7598524Z skipping: no hosts matched
2026-11-25T13:39:57.7604422Z 
2026-11-25T13:39:57.7604689Z PLAY [local] *******************************************************************
2026-11-25T13:39:57.7635076Z [WARNING]: Could not match supplied host pattern, ignoring: escopo_execucao
2026-11-25T13:39:57.7637458Z 
2026-11-25T13:39:57.7637945Z PLAY [Executar o Start do Sirot Connector no escopo definido] ******************
2026-11-25T13:39:57.7638092Z skipping: no hosts matched
2026-11-25T13:39:57.7643710Z 
2026-11-25T13:39:57.7643857Z PLAY [local] *******************************************************************
2026-11-25T13:39:57.7665229Z 
2026-11-25T13:39:57.7665450Z PLAY [Executar o Stop do Sirot Connector] **************************************
2026-11-25T13:39:57.7665939Z skipping: no hosts matched
2026-11-25T13:39:57.7674127Z 
2026-11-25T13:39:57.7674827Z PLAY [Configura TSM] ***********************************************************
2026-11-25T13:39:57.7698840Z 
2026-11-25T13:39:57.7699152Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:57.7725206Z 
2026-11-25T13:39:57.7725674Z PLAY [Configura Control-M] *****************************************************
2026-11-25T13:39:57.7758249Z 
2026-11-25T13:39:57.7758767Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:57.7798061Z 
2026-11-25T13:39:57.7798272Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:57.7841905Z 
2026-11-25T13:39:57.7842665Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:57.7882521Z 
2026-11-25T13:39:57.7882911Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:57.7905854Z 
2026-11-25T13:39:57.7906218Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:57.7935349Z 
2026-11-25T13:39:57.7935932Z PLAY [localhost] ***************************************************************
2026-11-25T13:39:57.7967899Z Wednesday 25 November 2026  10:39:57 -0300 (0:00:04.968)       0:00:05.330 **** 
2026-11-25T13:39:57.8477145Z included: /opt/ads-agent/_work/r6259/a/esteira-jboss-vm-v2/roles/vm/tasks/size/executed.yml for 127.0.0.1
2026-11-25T13:39:57.8506083Z Wednesday 25 November 2026  10:39:57 -0300 (0:00:00.053)       0:00:05.384 **** 
2026-11-25T13:39:57.8914464Z included: /opt/ads-agent/_work/r6259/a/esteira-jboss-vm-v2/roles/vm/tasks/size/approved.yml for 127.0.0.1
2026-11-25T13:39:57.8948680Z Wednesday 25 November 2026  10:39:57 -0300 (0:00:00.044)       0:00:05.428 **** 
2026-11-25T13:39:58.5306613Z 
2026-11-25T13:39:58.5307076Z TASK [Consultar API] ***********************************************************
2026-11-25T13:39:58.5307806Z ok: [127.0.0.1]
2026-11-25T13:39:58.5336913Z Wednesday 25 November 2026  10:39:58 -0300 (0:00:00.638)       0:00:06.067 **** 
2026-11-25T13:39:58.5774904Z 
2026-11-25T13:39:58.5775551Z TASK [Parse JSON] **************************************************************
2026-11-25T13:39:58.5775766Z ok: [127.0.0.1]
2026-11-25T13:39:58.5799790Z Wednesday 25 November 2026  10:39:58 -0300 (0:00:00.046)       0:00:06.113 **** 
2026-11-25T13:39:58.6244931Z Wednesday 25 November 2026  10:39:58 -0300 (0:00:00.044)       0:00:06.158 **** 
2026-11-25T13:39:58.6691363Z 
2026-11-25T13:39:58.6691927Z PLAY [jboss] *******************************************************************
2026-11-25T13:39:58.6759664Z Wednesday 25 November 2026  10:39:58 -0300 (0:00:00.051)       0:00:06.209 **** 
2026-11-25T13:39:59.7378571Z 
2026-11-25T13:39:59.7379153Z TASK [Gathering Facts] *********************************************************
2026-11-25T13:39:59.7379315Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:39:59.7585670Z Wednesday 25 November 2026  10:39:59 -0300 (0:00:01.082)       0:00:07.292 **** 
2026-11-25T13:40:00.5673765Z 
2026-11-25T13:40:00.5674281Z TASK [relogio : Copy chrony.conf] **********************************************
2026-11-25T13:40:00.5674480Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:00.5798974Z Wednesday 25 November 2026  10:40:00 -0300 (0:00:00.821)       0:00:08.113 **** 
2026-11-25T13:40:01.0608695Z 
2026-11-25T13:40:01.0609254Z TASK [relogio : Refresh chronyd] ***********************************************
2026-11-25T13:40:01.0609766Z changed: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:01.0733181Z Wednesday 25 November 2026  10:40:01 -0300 (0:00:00.493)       0:00:08.607 **** 
2026-11-25T13:40:05.3890267Z 
2026-11-25T13:40:05.3890920Z TASK [tunning : Install tuned] *************************************************
2026-11-25T13:40:05.3891168Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:05.4014989Z Wednesday 25 November 2026  10:40:05 -0300 (0:00:04.328)       0:00:12.935 **** 
2026-11-25T13:40:05.9933338Z 
2026-11-25T13:40:05.9934047Z TASK [tunning : Remover o arquivo (/etc/sysctl.d/30-nproc-nofile.conf) se ele existir] ***
2026-11-25T13:40:05.9934260Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:06.0071108Z Wednesday 25 November 2026  10:40:06 -0300 (0:00:00.605)       0:00:13.540 **** 
2026-11-25T13:40:06.2737862Z 
2026-11-25T13:40:06.2738638Z TASK [tunning : Remover o arquivo (/etc/security/limits.d/20-nproc.conf) se ele existir] ***
2026-11-25T13:40:06.2738872Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:06.2859170Z Wednesday 25 November 2026  10:40:06 -0300 (0:00:00.278)       0:00:13.819 **** 
2026-11-25T13:40:06.9044830Z 
2026-11-25T13:40:06.9045573Z TASK [tunning : Copy 90-rhel-sysctl.conf] **************************************
2026-11-25T13:40:06.9045729Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:06.9166319Z Wednesday 25 November 2026  10:40:06 -0300 (0:00:00.630)       0:00:14.450 **** 
2026-11-25T13:40:07.5191888Z 
2026-11-25T13:40:07.5192742Z TASK [tunning : Copy 30-nproc-nofile.conf] *************************************
2026-11-25T13:40:07.5193244Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:07.5317112Z Wednesday 25 November 2026  10:40:07 -0300 (0:00:00.615)       0:00:15.065 **** 
2026-11-25T13:40:07.9569183Z 
2026-11-25T13:40:07.9569724Z TASK [tunning : Add tcp_keepalive_time to sysctl.conf] *************************
2026-11-25T13:40:07.9569887Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:07.9709409Z Wednesday 25 November 2026  10:40:07 -0300 (0:00:00.439)       0:00:15.504 **** 
2026-11-25T13:40:08.2427667Z 
2026-11-25T13:40:08.2429121Z TASK [tunning : Refresh sysctl.conf] *******************************************
2026-11-25T13:40:08.2429407Z changed: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:08.2555082Z Wednesday 25 November 2026  10:40:08 -0300 (0:00:00.284)       0:00:15.789 **** 
2026-11-25T13:40:09.8016702Z 
2026-11-25T13:40:09.8017241Z TASK [tunning : Change tuned profile] ******************************************
2026-11-25T13:40:09.8017427Z changed: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:09.8160940Z Wednesday 25 November 2026  10:40:09 -0300 (0:00:01.560)       0:00:17.349 **** 
2026-11-25T13:40:14.7013104Z 
2026-11-25T13:40:14.7013788Z TASK [qualys : Instalação do Qualys] *******************************************
2026-11-25T13:40:14.7014006Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:14.7138040Z Wednesday 25 November 2026  10:40:14 -0300 (0:00:04.897)       0:00:22.247 **** 
2026-11-25T13:40:15.1734870Z 
2026-11-25T13:40:15.1735564Z TASK [Create directory /logs/qualys] *******************************************
2026-11-25T13:40:15.1735831Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:15.1870073Z Wednesday 25 November 2026  10:40:15 -0300 (0:00:00.473)       0:00:22.720 **** 
2026-11-25T13:40:15.4471815Z 
2026-11-25T13:40:15.4472535Z TASK [qualys : Configura Agent Qualys] *****************************************
2026-11-25T13:40:15.4472835Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:15.4600828Z Wednesday 25 November 2026  10:40:15 -0300 (0:00:00.273)       0:00:22.993 **** 
2026-11-25T13:40:16.0883608Z 
2026-11-25T13:40:16.0884545Z TASK [Criar arquivo de proxy do qualys] ****************************************
2026-11-25T13:40:16.0885306Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:16.1005955Z Wednesday 25 November 2026  10:40:16 -0300 (0:00:00.640)       0:00:23.634 **** 
2026-11-25T13:40:16.8147335Z 
2026-11-25T13:40:16.8148456Z TASK [Start qualys] ************************************************************
2026-11-25T13:40:16.8148701Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:16.8317691Z Wednesday 25 November 2026  10:40:16 -0300 (0:00:00.731)       0:00:24.365 **** 
2026-11-25T13:40:19.9616000Z 
2026-11-25T13:40:19.9616540Z TASK [qualys : Coletar facts dos servicos] *************************************
2026-11-25T13:40:19.9616704Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:20.0015573Z Wednesday 25 November 2026  10:40:19 -0300 (0:00:03.169)       0:00:27.535 **** 
2026-11-25T13:40:20.0702896Z 
2026-11-25T13:40:20.0703465Z TASK [qualys : Validar servico do Qualys em execucao] **************************
2026-11-25T13:40:20.0703949Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br] => {
2026-11-25T13:40:20.0704081Z     "changed": false, 
2026-11-25T13:40:20.0704392Z     "msg": "Servico qualys-cloud-agent esta em execucao."
2026-11-25T13:40:20.0704527Z }
2026-11-25T13:40:20.0965599Z Wednesday 25 November 2026  10:40:20 -0300 (0:00:00.095)       0:00:27.630 **** 
2026-11-25T13:40:20.4050601Z 
2026-11-25T13:40:20.4051080Z TASK [qualys : Coletar status detalhado do Qualys para log] ********************
2026-11-25T13:40:20.4051283Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:40:20.4313820Z Wednesday 25 November 2026  10:40:20 -0300 (0:00:00.334)       0:00:27.965 **** 
2026-11-25T13:40:20.4858362Z 
2026-11-25T13:40:20.4858874Z TASK [qualys : Exibir status detalhado do Qualys] ******************************
2026-11-25T13:40:20.4859384Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br] => {
2026-11-25T13:40:20.4859517Z     "status_output.stdout_lines": [
2026-11-25T13:40:20.4859898Z         "● qualys-cloud-agent.service - Qualys cloud agent daemon", 
2026-11-25T13:40:20.4860158Z         "     Loaded: loaded (/usr/lib/systemd/system/qualys-cloud-agent.service; enabled; preset: disabled)", 
2026-11-25T13:40:20.4860453Z         "     Active: active (running) since Thu 2026-11-12 16:20:59 -03; 1 week 5 days ago", 
2026-11-25T13:40:20.4860661Z         "   Main PID: 1088001 (qualys-cloud-ag)", 
2026-11-25T13:40:20.4860791Z         "      Tasks: 45 (limit: 23075)", 
2026-11-25T13:40:20.4860892Z         "     Memory: 172.9M", 
2026-11-25T13:40:20.4861004Z         "        CPU: 51min 43.236s", 
2026-11-25T13:40:20.4861189Z         "     CGroup: /system.slice/qualys-cloud-agent.service", 
2026-11-25T13:40:20.4861406Z         "             ├─1088001 /usr/local/qualys/cloud-agent/bin/qualys-cloud-agent", 
2026-11-25T13:40:20.4863018Z         "             ├─1088919 /usr/local/qualys/cloud-agent/mux/bin/qualys-mux", 
2026-11-25T13:40:20.4863508Z         "             ├─1088947 /usr/local/qualys/cloud-agent/mux/bpf/bin/qualys-bpf --grpc.config_timeout=120 --grpc.super_agent_uds_socket_path=/var/run/qualys/cloud-agent/sock/mux-server.sock --grpc.config_wait=true --grpc.uds_socket_path=/var/run/qualys/cloud-agent/sock/bpf-agent.sock", 
2026-11-25T13:40:20.4863890Z         "             └─1089097 /usr/local/qualys/cloud-agent/bin/qualys-cep", 
2026-11-25T13:40:20.4864012Z         "", 
2026-11-25T13:40:20.4864286Z         "nov 25 08:36:13 caddeapllx2854.agil.nprd.caixa.gov.br su[2349230]: pam_unix(su-l:session): session closed for user root", 
2026-11-25T13:40:20.4864564Z         "nov 25 09:44:04 caddeapllx2854.agil.nprd.caixa.gov.br su[2361696]: (to root) root on none", 
2026-11-25T13:40:20.4864878Z         "nov 25 09:44:05 caddeapllx2854.agil.nprd.caixa.gov.br su[2361696]: pam_unix(su-l:session): session opened for user root(uid=0) by (uid=0)", 
2026-11-25T13:40:20.4865201Z         "nov 25 09:44:05 caddeapllx2854.agil.nprd.caixa.gov.br su[2361696]: pam_unix(su-l:session): session closed for user root", 
2026-11-25T13:40:20.4865401Z         "nov 25 09:44:05 caddeapllx2854.agil.nprd.caixa.gov.br su[2361803]: (to root) root on none", 
2026-11-25T13:40:20.4865712Z         "nov 25 09:44:05 caddeapllx2854.agil.nprd.caixa.gov.br su[2361803]: pam_unix(su-l:session): session opened for user root(uid=0) by (uid=0)", 
2026-11-25T13:40:20.4866206Z         "nov 25 09:44:05 caddeapllx2854.agil.nprd.caixa.gov.br su[2361803]: pam_unix(su-l:session): session closed for user root", 
2026-11-25T13:40:20.4866398Z         "nov 25 09:44:11 caddeapllx2854.agil.nprd.caixa.gov.br su[2363171]: (to root) root on none", 
2026-11-25T13:40:20.4866691Z         "nov 25 09:44:11 caddeapllx2854.agil.nprd.caixa.gov.br su[2363171]: pam_unix(su-l:session): session opened for user root(uid=0) by (uid=0)", 
2026-11-25T13:40:20.4866992Z         "nov 25 09:44:11 caddeapllx2854.agil.nprd.caixa.gov.br su[2363171]: pam_unix(su-l:session): session closed for user root"
2026-11-25T13:40:20.4867147Z     ]
2026-11-25T13:40:20.4867236Z }
2026-11-25T13:40:20.4885599Z 
2026-11-25T13:40:20.4885779Z PLAY [jboss] *******************************************************************
2026-11-25T13:40:20.4939807Z 
2026-11-25T13:40:20.4940133Z PLAY [jboss] *******************************************************************
2026-11-25T13:40:20.4980696Z 
2026-11-25T13:40:20.4980987Z PLAY RECAP *********************************************************************
2026-11-25T13:40:20.4981284Z 127.0.0.1                  : ok=4    changed=0    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0   
2026-11-25T13:40:20.4981589Z caddeapllx2854.agil.nprd.caixa.gov.br : ok=21   changed=3    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
2026-11-25T13:40:20.4981733Z 
2026-11-25T13:40:20.4982468Z Wednesday 25 November 2026  10:40:20 -0300 (0:00:00.067)       0:00:28.032 **** 
2026-11-25T13:40:20.4982945Z =============================================================================== 
2026-11-25T13:40:20.4983704Z Verifica ser o Jboss já foi instalado ----------------------------------- 4.97s
2026-11-25T13:40:20.4984102Z qualys : Instalação do Qualys ------------------------------------------- 4.90s
2026-11-25T13:40:20.4984330Z tunning : Install tuned ------------------------------------------------- 4.33s
2026-11-25T13:40:20.4984559Z qualys : Coletar facts dos servicos ------------------------------------- 3.17s
2026-11-25T13:40:20.4984902Z tunning : Change tuned profile ------------------------------------------ 1.56s
2026-11-25T13:40:20.4985244Z Gathering Facts --------------------------------------------------------- 1.08s
2026-11-25T13:40:20.4985596Z relogio : Copy chrony.conf ---------------------------------------------- 0.82s
2026-11-25T13:40:20.4985942Z Start qualys ------------------------------------------------------------ 0.73s
2026-11-25T13:40:20.4986279Z Criar arquivo de proxy do qualys ---------------------------------------- 0.64s
2026-11-25T13:40:20.4986598Z Consultar API ----------------------------------------------------------- 0.64s
2026-11-25T13:40:20.4986890Z tunning : Copy 90-rhel-sysctl.conf -------------------------------------- 0.63s
2026-11-25T13:40:20.4987104Z tunning : Copy 30-nproc-nofile.conf ------------------------------------- 0.62s
2026-11-25T13:40:20.4987332Z tunning : Remover o arquivo (/etc/sysctl.d/30-nproc-nofile.conf) se ele existir --- 0.61s
2026-11-25T13:40:20.4987553Z relogio : Refresh chronyd ----------------------------------------------- 0.49s
2026-11-25T13:40:20.4987761Z Create directory /logs/qualys ------------------------------------------- 0.47s
2026-11-25T13:40:20.4987976Z tunning : Add tcp_keepalive_time to sysctl.conf ------------------------- 0.44s
2026-11-25T13:40:20.4988198Z qualys : Coletar status detalhado do Qualys para log -------------------- 0.33s
2026-11-25T13:40:20.4988417Z tunning : Refresh sysctl.conf ------------------------------------------- 0.28s
2026-11-25T13:40:20.4988647Z tunning : Remover o arquivo (/etc/security/limits.d/20-nproc.conf) se ele existir --- 0.28s
2026-11-25T13:40:20.4988858Z qualys : Configura Agent Qualys ----------------------------------------- 0.27s
2026-11-25T13:40:20.4989003Z Playbook run took 0 days, 0 hours, 0 minutes, 27 seconds
2026-11-25T13:40:20.5668475Z ##[section]Finishing: Definir size como executado



2026-11-25T13:43:30.0675262Z ##[section]Starting: Check Deployments [JBOSS]
2026-11-25T13:43:30.0678630Z ==============================================================================
2026-11-25T13:43:30.0678719Z Task         : Bash
2026-11-25T13:43:30.0678777Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-11-25T13:43:30.0678880Z Version      : 3.227.0
2026-11-25T13:43:30.0678947Z Author       : Microsoft Corporation
2026-11-25T13:43:30.0679027Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-11-25T13:43:30.0679154Z ==============================================================================
2026-11-25T13:43:30.9366804Z Generating script.
2026-11-25T13:43:30.9375089Z Script contents:
2026-11-25T13:43:30.9375717Z ansible-playbook /opt/ads-agent/_work/r6259/a/esteira-jboss-vm-v2/site.yml --tags check_deployments -e sistema_ambiente=des -e sistema_nome=sigsj-internet -e site=ctc_nprd
2026-11-25T13:43:30.9378814Z ========================== Starting Command Output ===========================
2026-11-25T13:43:30.9386233Z [command]/bin/bash /opt/ads-agent/_work/_temp/9fe84868-9cb3-42c7-ba7b-8ee5c0934e8c.sh
2026-11-25T13:43:33.1525926Z 
2026-11-25T13:43:33.1526822Z PLAY [local] *******************************************************************
2026-11-25T13:43:33.1826460Z 
2026-11-25T13:43:33.1826964Z PLAY [Configurando o DNS] ******************************************************
2026-11-25T13:43:33.3821808Z 
2026-11-25T13:43:33.3822434Z PLAY [local] *******************************************************************
2026-11-25T13:43:33.3855796Z 
2026-11-25T13:43:33.3856384Z PLAY [Verificando serviços] ****************************************************
2026-11-25T13:43:33.3953064Z 
2026-11-25T13:43:33.3953732Z PLAY [Configuração LDAP] *******************************************************
2026-11-25T13:43:33.3996425Z [WARNING]: Found variable using reserved name: when
2026-11-25T13:43:33.4001510Z 
2026-11-25T13:43:33.4001819Z PLAY [jboss] *******************************************************************
2026-11-25T13:43:33.4369942Z 
2026-11-25T13:43:33.4370480Z PLAY [Stack Jboss] *************************************************************
2026-11-25T13:43:33.4594679Z Wednesday 25 November 2026  10:43:33 -0300 (0:00:00.367)       0:00:00.367 **** 
2026-11-25T13:43:33.9492576Z 
2026-11-25T13:43:33.9493415Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-11-25T13:43:33.9493678Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-11-25T13:43:33.9494025Z caddeapllx2854.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-11-25T13:43:33.9494272Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-11-25T13:43:33.9494508Z releases. A future Ansible release will default to using the discovered 
2026-11-25T13:43:33.9494705Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-11-25T13:43:33.9494918Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-11-25T13:43:33.9495180Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-11-25T13:43:33.9495399Z setting deprecation_warnings=False in ansible.cfg.
2026-11-25T13:43:33.9495621Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:43:33.9522148Z 
2026-11-25T13:43:33.9522595Z PLAY [jboss] *******************************************************************
2026-11-25T13:43:33.9573479Z 
2026-11-25T13:43:33.9573972Z PLAY [jboss] *******************************************************************
2026-11-25T13:43:33.9619013Z 
2026-11-25T13:43:33.9619624Z PLAY [jboss] *******************************************************************
2026-11-25T13:43:33.9643396Z 
2026-11-25T13:43:33.9644606Z PLAY [Copiando deployments adicionais] *****************************************
2026-11-25T13:43:33.9670911Z 
2026-11-25T13:43:33.9671351Z PLAY [Copiando modules adicionais] *********************************************
2026-11-25T13:43:33.9704011Z 
2026-11-25T13:43:33.9704390Z PLAY [jboss] *******************************************************************
2026-11-25T13:43:33.9745921Z 
2026-11-25T13:43:33.9746259Z PLAY [jboss] *******************************************************************
2026-11-25T13:43:33.9783200Z 
2026-11-25T13:43:33.9783477Z PLAY [jboss] *******************************************************************
2026-11-25T13:43:33.9823530Z Wednesday 25 November 2026  10:43:33 -0300 (0:00:00.523)       0:00:00.890 **** 
2026-11-25T13:46:54.6406291Z 
2026-11-25T13:46:54.6407147Z TASK [Wait for Jboss Management port] ******************************************
2026-11-25T13:46:54.6409508Z fatal: [caddeapllx2854.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "elapsed": 200, "msg": "Timeout when waiting for 10.116.202.45:9990"}
2026-11-25T13:46:54.6447463Z Wednesday 25 November 2026  10:46:54 -0300 (0:03:20.662)       0:03:21.553 **** 
2026-11-25T13:47:01.4486226Z 
2026-11-25T13:47:01.4486925Z TASK [systemd] *****************************************************************
2026-11-25T13:47:01.4487296Z changed: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-25T13:47:01.4525093Z Wednesday 25 November 2026  10:47:01 -0300 (0:00:06.807)       0:03:28.360 **** 
2026-11-25T13:50:22.0183630Z 
2026-11-25T13:50:22.0184340Z TASK [Wait for Jboss Management port] ******************************************
2026-11-25T13:50:22.0185409Z fatal: [caddeapllx2854.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "elapsed": 200, "msg": "Timeout when waiting for 10.116.202.45:9990"}
2026-11-25T13:50:22.0193227Z 
2026-11-25T13:50:22.0193585Z PLAY RECAP *********************************************************************
2026-11-25T13:50:22.0193799Z caddeapllx2854.agil.nprd.caixa.gov.br : ok=2    changed=1    unreachable=0    failed=1    skipped=0    rescued=1    ignored=0   
2026-11-25T13:50:22.0193899Z 
2026-11-25T13:50:22.0194893Z Wednesday 25 November 2026  10:50:22 -0300 (0:03:20.567)       0:06:48.928 **** 
2026-11-25T13:50:22.0195301Z =============================================================================== 
2026-11-25T13:50:22.0197018Z Wait for Jboss Management port ---------------------------------------- 200.66s
2026-11-25T13:50:22.0198520Z Wait for Jboss Management port ---------------------------------------- 200.57s
2026-11-25T13:50:22.0200589Z systemd ----------------------------------------------------------------- 6.81s
2026-11-25T13:50:22.0200995Z Verifica ser o Jboss já foi instalado ----------------------------------- 0.52s
2026-11-25T13:50:22.0201240Z Playbook run took 0 days, 0 hours, 6 minutes, 48 seconds
2026-11-25T13:50:22.0886238Z ##[error]Bash exited with code '2'.
2026-11-25T13:50:22.0908611Z ##[section]Finishing: Check Deployments [JBOSS]
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
SIGSJ-internet
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
SIGSJ

SIGSJ-internet
Predefined variables
Usuario-Azure-DevOps (12)
Scopes: Release
OKD-PRODUTOS (8)
Credenciais para o Cluster OKD4 de PRODUTOS
Scopes: Release
SonarQube Variables (1)
Variáveis com dados do SonarQube
Scopes: Release
MONITORACAO_LOGS (4)
REQ000143540550 - Conforme autorizado na req por FLAVIO ALMEIDA GAGLIARDI, removido as variáveis JAVA_OPTS_MONITORING e URL_APM_SERVER, por entrar em conflitos com releases que utilizam o Application Insights
Scopes: Release
TERRAFORM-ESTEIRA-COMMON (6)
WO0000079295714 - add variável INFRAFACIL
Scopes: Release
ANSIBLE_JBOSS_VM_VERSION_3 (11)
WO0000072264656 - Config Portal Infrafácil NO_PROXY cadsvgerap027-1.intra.caixa.gov.br, 10.122.144.168
Scopes: Release
TERRAFORM-ESTEIRA-NPRD (17)
Variáveis do terraform para automação de ambientes
Scopes: EC DES,EC TQS,EC HMP
SIGSJ-INTERNET-DES (16)
Grupo de variáveis de SIGSJ-INTERNET-DES

Scopes: EC DES
JKS_FILE
caixa-truststore-acteste-nprd.jks
JVM_HEAP_MAX
2048m
JVM_HEAP_MIN
1024m
JVM_METASPACE_MAX
512m
JVM_METASPACE_MIN
96m
JVM_PROXY_HOST
proxydes.caixa
PASSWORD_TRUSTSTORE
changeit
SIGSJ04_CONNECTION_STRING
jdbc:oracle:thin:@CNPEXDADVM01CLU08.EXTRA.CAIXA.GOV.BR:1521/orad01bc
SIGSJ04_PASSWORD
********
SIGSJ04_USER
SGSJSD01
SIGSJ_AMBIENTE
DES
SIGSJ_B2B_CLOTE_BASE
http://10.116.89.232:5033
SIGSJ_B2B_INTERNET_BASE
https://sigsj.b2b.des.caixa.gov.br
SIGSJ_CONVIVENCIA_URL
https://sigsj-convivencia-des.apps.nprd.caixa/convivencia/v1
SIGSJ_SIMTR_URL
http://simtr-api-intranet-des.apps.nprd.caixa/
URL_APM_SERVER
http://apm-server-devops.apps.produtos4.caixa
SIGSJ-INTERNET-TQS (11)
Grupo de variáveis de SIGSJ-INTERNET-TQS
Scopes: EC TQS
SIGSJ-INTERNET-HMP (1)
Grupo de variáveis de SIGSJ-INTERNET-HMP
Scopes: EC HMP
TERRAFORM-ESTEIRA-PRD-CTC-NPCN (17)
Variáveis do terraform para automação de ambientes TERRAFORM_VSPHERE_POOL - RP_ESTEIRAS_AGEIS_NPCN_CTC_V7 13/03/2025
Scopes: EC PRD CTC
SIGSJ-INTERNET-PRD (1)
Grupo de variáveis de SIGSJ-INTERNET-PRD
Scopes: EC PRD CTC,EC PRD DTC
TERRAFORM-ESTEIRA-PRD-DTC-PCN (15)
Variáveis do terraform para automação de ambientes
Scopes: EC PRD DTC
|Manage variable groups
Row 2

Row 2

Showing filters 1 through 2

Row 2

Row 2

72 pipelines found

Select a release pipeline to view its releases

64 pipelines found

Select a release pipeline to view its releases

6 pipelines found

Row 3

Row 2

Showing filters 1 through 2

