2026-11-25T13:45:01.1880768Z ##[section]Starting: Check Deployments [JBOSS]
2026-11-25T13:45:01.1883815Z ==============================================================================
2026-11-25T13:45:01.1883900Z Task         : Bash
2026-11-25T13:45:01.1883940Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-11-25T13:45:01.1883998Z Version      : 3.227.0
2026-11-25T13:45:01.1884048Z Author       : Microsoft Corporation
2026-11-25T13:45:01.1884094Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-11-25T13:45:01.1884170Z ==============================================================================
2026-11-25T13:45:02.0391450Z Generating script.
2026-11-25T13:45:02.0400278Z Script contents:
2026-11-25T13:45:02.0400692Z ansible-playbook /opt/ads-agent/_work/r12572/a/esteira-jboss-vm-v2/site.yml --tags check_deployments -e sistema_ambiente=des -e sistema_nome=sigsj-boleto -e site=ctc_nprd
2026-11-25T13:45:02.0403466Z ========================== Starting Command Output ===========================
2026-11-25T13:45:02.0411423Z [command]/bin/bash /opt/ads-agent/_work/_temp/a90fd537-0128-4453-b6f9-ecb94b4484a6.sh
2026-11-25T13:45:04.5003997Z 
2026-11-25T13:45:04.5004585Z PLAY [local] *******************************************************************
2026-11-25T13:45:04.5314130Z 
2026-11-25T13:45:04.5314589Z PLAY [Configurando o DNS] ******************************************************
2026-11-25T13:45:04.7366388Z 
2026-11-25T13:45:04.7366996Z PLAY [local] *******************************************************************
2026-11-25T13:45:04.7405303Z 
2026-11-25T13:45:04.7405901Z PLAY [Verificando serviços] ****************************************************
2026-11-25T13:45:04.7500782Z 
2026-11-25T13:45:04.7501430Z PLAY [Configuração LDAP] *******************************************************
2026-11-25T13:45:04.7545354Z [WARNING]: Found variable using reserved name: when
2026-11-25T13:45:04.7549714Z 
2026-11-25T13:45:04.7549977Z PLAY [jboss] *******************************************************************
2026-11-25T13:45:04.8005122Z 
2026-11-25T13:45:04.8006193Z PLAY [Stack Jboss] *************************************************************
2026-11-25T13:45:04.8271596Z Wednesday 25 November 2026  10:45:04 -0300 (0:00:00.392)       0:00:00.392 **** 
2026-11-25T13:45:05.3671317Z 
2026-11-25T13:45:05.3672277Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-11-25T13:45:05.3673972Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-11-25T13:45:05.3674482Z caddeapllx2557.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-11-25T13:45:05.3674653Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-11-25T13:45:05.3674824Z releases. A future Ansible release will default to using the discovered 
2026-11-25T13:45:05.3674973Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-11-25T13:45:05.3675145Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-11-25T13:45:05.3675368Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-11-25T13:45:05.3675506Z setting deprecation_warnings=False in ansible.cfg.
2026-11-25T13:45:05.3676512Z ok: [caddeapllx2557.agil.nprd.caixa.gov.br]
2026-11-25T13:45:05.3707661Z 
2026-11-25T13:45:05.3708485Z PLAY [jboss] *******************************************************************
2026-11-25T13:45:05.3760505Z 
2026-11-25T13:45:05.3760985Z PLAY [jboss] *******************************************************************
2026-11-25T13:45:05.3806117Z 
2026-11-25T13:45:05.3806574Z PLAY [jboss] *******************************************************************
2026-11-25T13:45:05.3833521Z 
2026-11-25T13:45:05.3834371Z PLAY [Copiando deployments adicionais] *****************************************
2026-11-25T13:45:05.3862541Z 
2026-11-25T13:45:05.3863065Z PLAY [Copiando modules adicionais] *********************************************
2026-11-25T13:45:05.3891498Z 
2026-11-25T13:45:05.3892310Z PLAY [jboss] *******************************************************************
2026-11-25T13:45:05.3931423Z 
2026-11-25T13:45:05.3931806Z PLAY [jboss] *******************************************************************
2026-11-25T13:45:05.3967083Z 
2026-11-25T13:45:05.3967810Z PLAY [jboss] *******************************************************************
2026-11-25T13:45:05.4014449Z Wednesday 25 November 2026  10:45:05 -0300 (0:00:00.574)       0:00:00.967 **** 
2026-11-25T13:48:26.0752615Z 
2026-11-25T13:48:26.0753323Z TASK [Wait for Jboss Management port] ******************************************
2026-11-25T13:48:26.0755567Z fatal: [caddeapllx2557.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "elapsed": 200, "msg": "Timeout when waiting for 10.116.201.25:9990"}
2026-11-25T13:48:26.0791586Z Wednesday 25 November 2026  10:48:26 -0300 (0:03:20.677)       0:03:21.644 **** 
2026-11-25T13:48:32.8843712Z 
2026-11-25T13:48:32.8844170Z TASK [systemd] *****************************************************************
2026-11-25T13:48:32.8846102Z changed: [caddeapllx2557.agil.nprd.caixa.gov.br]
2026-11-25T13:48:32.8881600Z Wednesday 25 November 2026  10:48:32 -0300 (0:00:06.809)       0:03:28.453 **** 
2026-11-25T13:51:53.4026390Z 
2026-11-25T13:51:53.4027100Z TASK [Wait for Jboss Management port] ******************************************
2026-11-25T13:51:53.4028933Z fatal: [caddeapllx2557.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "elapsed": 200, "msg": "Timeout when waiting for 10.116.201.25:9990"}
2026-11-25T13:51:53.4029203Z 
2026-11-25T13:51:53.4029403Z PLAY RECAP *********************************************************************
2026-11-25T13:51:53.4029927Z caddeapllx2557.agil.nprd.caixa.gov.br : ok=2    changed=1    unreachable=0    failed=1    skipped=0    rescued=1    ignored=0   
2026-11-25T13:51:53.4030044Z 
2026-11-25T13:51:53.4030607Z Wednesday 25 November 2026  10:51:53 -0300 (0:03:20.514)       0:06:48.968 **** 
2026-11-25T13:51:53.4030900Z =============================================================================== 
2026-11-25T13:51:53.4031686Z Wait for Jboss Management port ---------------------------------------- 200.68s
2026-11-25T13:51:53.4031909Z Wait for Jboss Management port ---------------------------------------- 200.51s
2026-11-25T13:51:53.4032249Z systemd ----------------------------------------------------------------- 6.81s
2026-11-25T13:51:53.4032477Z Verifica ser o Jboss já foi instalado ----------------------------------- 0.57s
2026-11-25T13:51:53.4032626Z Playbook run took 0 days, 0 hours, 6 minutes, 48 seconds
2026-11-25T13:51:53.4810142Z ##[error]Bash exited with code '2'.
2026-11-25T13:51:53.4822850Z ##[section]Finishing: Check Deployments [JBOSS]
