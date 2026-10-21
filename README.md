2026-10-21T19:35:25.9314898Z ##[section]Starting: Check Deployments [JBOSS]
2026-10-21T19:35:25.9317939Z ==============================================================================
2026-10-21T19:35:25.9318020Z Task         : Bash
2026-10-21T19:35:25.9318070Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-21T19:35:25.9318130Z Version      : 3.227.0
2026-10-21T19:35:25.9318172Z Author       : Microsoft Corporation
2026-10-21T19:35:25.9318228Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-21T19:35:25.9318297Z ==============================================================================
2026-10-21T19:35:26.0528491Z Generating script.
2026-10-21T19:35:26.0536791Z Script contents:
2026-10-21T19:35:26.0537380Z ansible-playbook /opt/ads-agent/_work/r19326/a/esteira-jboss-vm-v2/site.yml --tags check_deployments -e sistema_ambiente=des -e sistema_nome=sigsj-boleto -e site=ctc_nprd
2026-10-21T19:35:26.0539957Z ========================== Starting Command Output ===========================
2026-10-21T19:35:26.0564546Z [command]/bin/bash /opt/ads-agent/_work/_temp/d5cf2ce4-465c-4d04-8951-2f97a367ec94.sh
2026-10-21T19:35:28.2383560Z 
2026-10-21T19:35:28.2384017Z PLAY [local] *******************************************************************
2026-10-21T19:35:28.2674194Z 
2026-10-21T19:35:28.2674857Z PLAY [Configurando o DNS] ******************************************************
2026-10-21T19:35:28.4637197Z 
2026-10-21T19:35:28.4660509Z PLAY [local] *******************************************************************
2026-10-21T19:35:28.4671692Z 
2026-10-21T19:35:28.4672439Z PLAY [Verificando serviços] ****************************************************
2026-10-21T19:35:28.4752753Z 
2026-10-21T19:35:28.4753264Z PLAY [Configuração LDAP] *******************************************************
2026-10-21T19:35:28.4786247Z [WARNING]: Found variable using reserved name: when
2026-10-21T19:35:28.4791724Z 
2026-10-21T19:35:28.4791868Z PLAY [jboss] *******************************************************************
2026-10-21T19:35:28.4879124Z 
2026-10-21T19:35:28.4879407Z PLAY [Stack Jboss] *************************************************************
2026-10-21T19:35:28.5122213Z Wednesday 21 October 2026  16:35:28 -0300 (0:00:00.334)       0:00:00.334 ***** 
2026-10-21T19:35:29.0217215Z 
2026-10-21T19:35:29.0217951Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-10-21T19:35:29.0220856Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-21T19:35:29.0221274Z caddeapllx2557.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-21T19:35:29.0221442Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-21T19:35:29.0221595Z releases. A future Ansible release will default to using the discovered 
2026-10-21T19:35:29.0221753Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-21T19:35:29.0221910Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-21T19:35:29.0222092Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-21T19:35:29.0225127Z setting deprecation_warnings=False in ansible.cfg.
2026-10-21T19:35:29.0225303Z ok: [caddeapllx2557.agil.nprd.caixa.gov.br]
2026-10-21T19:35:29.0244016Z 
2026-10-21T19:35:29.0244202Z PLAY [jboss] *******************************************************************
2026-10-21T19:35:29.0287292Z 
2026-10-21T19:35:29.0287444Z PLAY [jboss] *******************************************************************
2026-10-21T19:35:29.0327667Z 
2026-10-21T19:35:29.0327973Z PLAY [jboss] *******************************************************************
2026-10-21T19:35:29.0351412Z 
2026-10-21T19:35:29.0351617Z PLAY [Copiando deployments adicionais] *****************************************
2026-10-21T19:35:29.0379673Z 
2026-10-21T19:35:29.0379841Z PLAY [Copiando modules adicionais] *********************************************
2026-10-21T19:35:29.0407017Z 
2026-10-21T19:35:29.0407349Z PLAY [jboss] *******************************************************************
2026-10-21T19:35:29.0440619Z 
2026-10-21T19:35:29.0440793Z PLAY [jboss] *******************************************************************
2026-10-21T19:35:29.0470729Z 
2026-10-21T19:35:29.0471084Z PLAY [jboss] *******************************************************************
2026-10-21T19:35:29.0517941Z Wednesday 21 October 2026  16:35:29 -0300 (0:00:00.539)       0:00:00.873 ***** 
2026-10-21T19:38:49.6335541Z 
2026-10-21T19:38:49.6336195Z TASK [Wait for Jboss Management port] ******************************************
2026-10-21T19:38:49.6336436Z fatal: [caddeapllx2557.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "elapsed": 200, "msg": "Timeout when waiting for 10.116.201.25:9990"}
2026-10-21T19:38:49.6367522Z Wednesday 21 October 2026  16:38:49 -0300 (0:03:20.584)       0:03:21.458 ***** 
2026-10-21T19:38:56.3853448Z 
2026-10-21T19:38:56.3853963Z TASK [systemd] *****************************************************************
2026-10-21T19:38:56.3854147Z changed: [caddeapllx2557.agil.nprd.caixa.gov.br]
2026-10-21T19:38:56.3891044Z Wednesday 21 October 2026  16:38:56 -0300 (0:00:06.752)       0:03:28.211 ***** 
2026-10-21T19:42:16.8479893Z 
2026-10-21T19:42:16.8483343Z TASK [Wait for Jboss Management port] ******************************************
2026-10-21T19:42:16.8483611Z fatal: [caddeapllx2557.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "elapsed": 200, "msg": "Timeout when waiting for 10.116.201.25:9990"}
2026-10-21T19:42:16.8490032Z 
2026-10-21T19:42:16.8490182Z PLAY RECAP *********************************************************************
2026-10-21T19:42:16.8492545Z caddeapllx2557.agil.nprd.caixa.gov.br : ok=2    changed=1    unreachable=0    failed=1    skipped=0    rescued=1    ignored=0   
2026-10-21T19:42:16.8492770Z 
2026-10-21T19:42:16.8493654Z Wednesday 21 October 2026  16:42:16 -0300 (0:03:20.460)       0:06:48.671 ***** 
2026-10-21T19:42:16.8493879Z =============================================================================== 
2026-10-21T19:42:16.8494189Z Wait for Jboss Management port ---------------------------------------- 200.58s
2026-10-21T19:42:16.8494422Z Wait for Jboss Management port ---------------------------------------- 200.46s
2026-10-21T19:42:16.8496830Z systemd ----------------------------------------------------------------- 6.75s
2026-10-21T19:42:16.8497232Z Verifica ser o Jboss já foi instalado ----------------------------------- 0.54s
2026-10-21T19:42:16.8497761Z Playbook run took 0 days, 0 hours, 6 minutes, 48 seconds
2026-10-21T19:42:16.9160643Z ##[error]Bash exited with code '2'.
2026-10-21T19:42:16.9193632Z ##[section]Finishing: Check Deployments [JBOSS]
