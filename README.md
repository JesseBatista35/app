2026-11-25T15:00:12.0212348Z ##[section]Starting: Check Deployments [JBOSS]
2026-11-25T15:00:12.0216239Z ==============================================================================
2026-11-25T15:00:12.0216350Z Task         : Bash
2026-11-25T15:00:12.0216392Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-11-25T15:00:12.0216452Z Version      : 3.227.0
2026-11-25T15:00:12.0216505Z Author       : Microsoft Corporation
2026-11-25T15:00:12.0216669Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-11-25T15:00:12.0216740Z ==============================================================================
2026-11-25T15:00:12.1450522Z Generating script.
2026-11-25T15:00:12.1459951Z Script contents:
2026-11-25T15:00:12.1460566Z ansible-playbook /opt/ads-agent/_work/r19593/a/esteira-jboss-vm-v2/site.yml --tags check_deployments -e sistema_ambiente=des -e sistema_nome=sigec-portabilidade-online -e site=ctc_nprd
2026-11-25T15:00:12.1463444Z ========================== Starting Command Output ===========================
2026-11-25T15:00:12.1470732Z [command]/bin/bash /opt/ads-agent/_work/_temp/3ca2a2b4-a18d-4c4c-863e-863f0a4f4d3b.sh
2026-11-25T15:00:14.5601767Z 
2026-11-25T15:00:14.5602719Z PLAY [local] *******************************************************************
2026-11-25T15:00:14.5903909Z 
2026-11-25T15:00:14.5904563Z PLAY [Configurando o DNS] ******************************************************
2026-11-25T15:00:14.8520721Z 
2026-11-25T15:00:14.8521260Z PLAY [local] *******************************************************************
2026-11-25T15:00:14.8556951Z 
2026-11-25T15:00:14.8557547Z PLAY [Verificando serviços] ****************************************************
2026-11-25T15:00:14.8659906Z 
2026-11-25T15:00:14.8660621Z PLAY [Configuração LDAP] *******************************************************
2026-11-25T15:00:14.8709372Z [WARNING]: Found variable using reserved name: when
2026-11-25T15:00:14.8713443Z 
2026-11-25T15:00:14.8713729Z PLAY [jboss] *******************************************************************
2026-11-25T15:00:14.9117810Z 
2026-11-25T15:00:14.9118621Z PLAY [Stack Jboss] *************************************************************
2026-11-25T15:00:14.9360247Z Wednesday 25 November 2026  12:00:14 -0300 (0:00:00.439)       0:00:00.439 **** 
2026-11-25T15:00:15.6651761Z 
2026-11-25T15:00:15.6652462Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-11-25T15:00:15.6652814Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-11-25T15:00:15.6653040Z caddeapllx2871.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-11-25T15:00:15.6653329Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-11-25T15:00:15.6653474Z releases. A future Ansible release will default to using the discovered 
2026-11-25T15:00:15.6653642Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-11-25T15:00:15.6653801Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-11-25T15:00:15.6653971Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-11-25T15:00:15.6654115Z setting deprecation_warnings=False in ansible.cfg.
2026-11-25T15:00:15.6656916Z ok: [caddeapllx2871.agil.nprd.caixa.gov.br]
2026-11-25T15:00:15.6685065Z 
2026-11-25T15:00:15.6685376Z PLAY [jboss] *******************************************************************
2026-11-25T15:00:15.6743270Z 
2026-11-25T15:00:15.6743539Z PLAY [jboss] *******************************************************************
2026-11-25T15:00:15.6792085Z 
2026-11-25T15:00:15.6792557Z PLAY [jboss] *******************************************************************
2026-11-25T15:00:15.6821415Z 
2026-11-25T15:00:15.6821764Z PLAY [Copiando deployments adicionais] *****************************************
2026-11-25T15:00:15.6847990Z 
2026-11-25T15:00:15.6848189Z PLAY [Copiando modules adicionais] *********************************************
2026-11-25T15:00:15.6874032Z 
2026-11-25T15:00:15.6874757Z PLAY [jboss] *******************************************************************
2026-11-25T15:00:15.6911751Z 
2026-11-25T15:00:15.6912118Z PLAY [jboss] *******************************************************************
2026-11-25T15:00:15.6944437Z 
2026-11-25T15:00:15.6944778Z PLAY [jboss] *******************************************************************
2026-11-25T15:00:15.6990758Z Wednesday 25 November 2026  12:00:15 -0300 (0:00:00.763)       0:00:01.203 **** 
2026-11-25T15:03:36.2836520Z 
2026-11-25T15:03:36.2837070Z TASK [Wait for Jboss Management port] ******************************************
2026-11-25T15:03:36.2837302Z fatal: [caddeapllx2871.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "elapsed": 200, "msg": "Timeout when waiting for 10.116.202.61:9990"}
2026-11-25T15:03:36.2869450Z Wednesday 25 November 2026  12:03:36 -0300 (0:03:20.587)       0:03:21.790 **** 
2026-11-25T15:03:43.1009555Z 
2026-11-25T15:03:43.1010260Z TASK [systemd] *****************************************************************
2026-11-25T15:03:43.1010502Z changed: [caddeapllx2871.agil.nprd.caixa.gov.br]
2026-11-25T15:03:43.1048252Z Wednesday 25 November 2026  12:03:43 -0300 (0:00:06.817)       0:03:28.608 **** 
2026-11-25T15:07:03.6933323Z 
2026-11-25T15:07:03.6935948Z TASK [Wait for Jboss Management port] ******************************************
2026-11-25T15:07:03.6936232Z fatal: [caddeapllx2871.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "elapsed": 200, "msg": "Timeout when waiting for 10.116.202.61:9990"}
2026-11-25T15:07:03.6947851Z 
2026-11-25T15:07:03.6948252Z PLAY RECAP *********************************************************************
2026-11-25T15:07:03.6948437Z caddeapllx2871.agil.nprd.caixa.gov.br : ok=2    changed=1    unreachable=0    failed=1    skipped=0    rescued=1    ignored=0   
2026-11-25T15:07:03.6951172Z 
2026-11-25T15:07:03.6952017Z Wednesday 25 November 2026  12:07:03 -0300 (0:03:20.590)       0:06:49.198 **** 
2026-11-25T15:07:03.6952242Z =============================================================================== 
2026-11-25T15:07:03.6952489Z Wait for Jboss Management port ---------------------------------------- 200.59s
2026-11-25T15:07:03.6953977Z Wait for Jboss Management port ---------------------------------------- 200.59s
2026-11-25T15:07:03.6954229Z systemd ----------------------------------------------------------------- 6.82s
2026-11-25T15:07:03.6954462Z Verifica ser o Jboss já foi instalado ----------------------------------- 0.76s
2026-11-25T15:07:03.6954611Z Playbook run took 0 days, 0 hours, 6 minutes, 49 seconds
2026-11-25T15:07:03.7626612Z ##[error]Bash exited with code '2'.
2026-11-25T15:07:03.7656115Z ##[section]Finishing: Check Deployments [JBOSS]
