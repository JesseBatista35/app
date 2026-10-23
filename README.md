2026-10-23T15:05:53.2913457Z ##[section]Starting: Configura Control-M
2026-10-23T15:05:53.2916962Z ==============================================================================
2026-10-23T15:05:53.2917049Z Task         : Bash
2026-10-23T15:05:53.2917101Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-23T15:05:53.2917177Z Version      : 3.227.0
2026-10-23T15:05:53.2917225Z Author       : Microsoft Corporation
2026-10-23T15:05:53.2917299Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-23T15:05:53.2917376Z ==============================================================================
2026-10-23T15:05:53.4237581Z Generating script.
2026-10-23T15:05:53.4248400Z ========================== Starting Command Output ===========================
2026-10-23T15:05:53.4255577Z [command]/bin/bash /opt/ads-agent/_work/_temp/8c4667c9-96df-44c3-bbec-57715e854302.sh
2026-10-23T15:05:55.6459954Z 
2026-10-23T15:05:55.6460516Z PLAY [local] *******************************************************************
2026-10-23T15:05:55.6758478Z 
2026-10-23T15:05:55.6758974Z PLAY [Configurando o DNS] ******************************************************
2026-10-23T15:05:55.8650563Z 
2026-10-23T15:05:55.8651372Z PLAY [local] *******************************************************************
2026-10-23T15:05:55.8687375Z 
2026-10-23T15:05:55.8688237Z PLAY [Verificando serviços] ****************************************************
2026-10-23T15:05:55.8779319Z 
2026-10-23T15:05:55.8780300Z PLAY [Configuração LDAP] *******************************************************
2026-10-23T15:05:55.8813984Z [WARNING]: Found variable using reserved name: when
2026-10-23T15:05:55.8819042Z 
2026-10-23T15:05:55.8819494Z PLAY [jboss] *******************************************************************
2026-10-23T15:05:55.8909387Z 
2026-10-23T15:05:55.8909708Z PLAY [Stack Jboss] *************************************************************
2026-10-23T15:05:55.8939311Z 
2026-10-23T15:05:55.8939548Z PLAY [jboss] *******************************************************************
2026-10-23T15:05:55.8982307Z 
2026-10-23T15:05:55.8982570Z PLAY [jboss] *******************************************************************
2026-10-23T15:05:55.9264382Z Friday 23 October 2026  12:05:55 -0300 (0:00:00.341)       0:00:00.341 ******** 
2026-10-23T15:05:56.4283439Z 
2026-10-23T15:05:56.4284570Z TASK [Verifica se o arquivo nfs_config.json existe] ****************************
2026-10-23T15:05:56.4284814Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:05:56.4314148Z Friday 23 October 2026  12:05:56 -0300 (0:00:00.505)       0:00:00.846 ******** 
2026-10-23T15:05:56.4806539Z included: /opt/ads-agent/_work/r19403/a/esteira-jboss-vm-v2/roles/nfs/tasks/get_nfs.yml for caddeapllx2695.agil.nprd.caixa.gov.br
2026-10-23T15:05:56.4852418Z Friday 23 October 2026  12:05:56 -0300 (0:00:00.053)       0:00:00.900 ******** 
2026-10-23T15:05:56.5455393Z 
2026-10-23T15:05:56.5456677Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-23T15:05:56.5456922Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:05:56.5511252Z Friday 23 October 2026  12:05:56 -0300 (0:00:00.065)       0:00:00.966 ******** 
2026-10-23T15:05:57.0205653Z 
2026-10-23T15:05:57.0206400Z TASK [nfs : Coletar variáveis de ambiente] *************************************
2026-10-23T15:05:57.0206578Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:05:57.0241464Z Friday 23 October 2026  12:05:57 -0300 (0:00:00.472)       0:00:01.439 ******** 
2026-10-23T15:05:57.0819260Z 
2026-10-23T15:05:57.0820166Z TASK [nfs : Exibir resultado em JSON] ******************************************
2026-10-23T15:05:57.0822061Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-23T15:05:57.0822202Z     "nfs_vars_json": {
2026-10-23T15:05:57.0822642Z         "changed": false, 
2026-10-23T15:05:57.0823087Z         "cmd": "cat /opt/ads-agent/_work/r19403/a/nfs_config.json", 
2026-10-23T15:05:57.0823259Z         "delta": "0:00:00.006268", 
2026-10-23T15:05:57.0823824Z         "end": "2026-10-23 12:05:57.004287", 
2026-10-23T15:05:57.0823960Z         "failed": false, 
2026-10-23T15:05:57.0824074Z         "rc": 0, 
2026-10-23T15:05:57.0824259Z         "start": "2026-10-23 12:05:56.998019", 
2026-10-23T15:05:57.0824389Z         "stderr": "", 
2026-10-23T15:05:57.0824508Z         "stderr_lines": [], 
2026-10-23T15:05:57.0824949Z         "stdout": "[{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH\",\"NFS_MOUNT_POINT_ISILON\": \"/SIIFX\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX\",\"NFS_MOUNT_POINT_ISILON_2\": \"/SIIFX_B2B\"}]", 
2026-10-23T15:05:57.0825339Z         "stdout_lines": [
2026-10-23T15:05:57.0825778Z             "[{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH\",\"NFS_MOUNT_POINT_ISILON\": \"/SIIFX\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX\",\"NFS_MOUNT_POINT_ISILON_2\": \"/SIIFX_B2B\"}]"
2026-10-23T15:05:57.0826004Z         ]
2026-10-23T15:05:57.0826102Z     }
2026-10-23T15:05:57.0826490Z }
2026-10-23T15:05:57.0855359Z Friday 23 October 2026  12:05:57 -0300 (0:00:00.061)       0:00:01.500 ******** 
2026-10-23T15:05:57.1460771Z 
2026-10-23T15:05:57.1461627Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-23T15:05:57.1461862Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:05:57.1511880Z Friday 23 October 2026  12:05:57 -0300 (0:00:00.065)       0:00:01.566 ******** 
2026-10-23T15:06:01.1658272Z 
2026-10-23T15:06:01.1658847Z TASK [nfs : execute montagem script] *******************************************
2026-10-23T15:06:01.1659029Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:01.1693069Z Friday 23 October 2026  12:06:01 -0300 (0:00:04.018)       0:00:05.584 ******** 
2026-10-23T15:06:01.2340281Z 
2026-10-23T15:06:01.2340838Z TASK [nfs : ansible.builtin.debug] *********************************************
2026-10-23T15:06:01.2342440Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-23T15:06:01.2342584Z     "changed": false, 
2026-10-23T15:06:01.2343125Z     "msg": {
2026-10-23T15:06:01.2343316Z         "changed": true, 
2026-10-23T15:06:01.2343435Z         "cmd": [
2026-10-23T15:06:01.2343550Z             "python", 
2026-10-23T15:06:01.2343928Z             "/opt/ads-agent/_work/r19403/a/esteira-jboss-vm-v2/roles/nfs/files/nfs.py", 
2026-10-23T15:06:01.2344102Z             "montagem", 
2026-10-23T15:06:01.2344264Z             "siifx-caixinhas-batch", 
2026-10-23T15:06:01.2344387Z             "des", 
2026-10-23T15:06:01.2344493Z             "ctc_nprd", 
2026-10-23T15:06:01.2344675Z             "/opt/ads-agent/_work/r19403/a/esteira-jboss-vm-v2", 
2026-10-23T15:06:01.2344807Z             "C&t@d02", 
2026-10-23T15:06:01.2344991Z             "***", 
2026-10-23T15:06:01.2345109Z             "s736651@corp.caixa.gov.br", 
2026-10-23T15:06:01.2345377Z             "***", 
2026-10-23T15:06:01.2345826Z             "[{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH\",\"NFS_MOUNT_POINT_ISILON\": \"/SIIFX\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX\",\"NFS_MOUNT_POINT_ISILON_2\": \"/SIIFX_B2B\"}]"
2026-10-23T15:06:01.2346158Z         ], 
2026-10-23T15:06:01.2346284Z         "delta": "0:00:03.654086", 
2026-10-23T15:06:01.2346808Z         "end": "2026-10-23 12:06:01.147141", 
2026-10-23T15:06:01.2346944Z         "failed": false, 
2026-10-23T15:06:01.2347054Z         "rc": 0, 
2026-10-23T15:06:01.2347226Z         "start": "2026-10-23 12:05:57.493055", 
2026-10-23T15:06:01.2347357Z         "stderr": "", 
2026-10-23T15:06:01.2347486Z         "stderr_lines": [], 
2026-10-23T15:06:01.2349169Z         "stdout": "[{u'NFS_MOUNT_POINT_ISILON': u'/SIIFX', u'NFS_ENDPOINT_ISILON': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH'}, {u'NFS_MOUNT_POINT_ISILON_2': u'/SIIFX_B2B', u'NFS_ENDPOINT_ISILON_2': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX'}]\nNome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           \n------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH /SIIFX                              ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/SIIFX\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH /SIIFX                              ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX /SIIFX_B2B                          ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/SIIFX_B2B\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX /SIIFX_B2B                          ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-23T15:06:01.2350004Z         "stdout_lines": [
2026-10-23T15:06:01.2350429Z             "[{u'NFS_MOUNT_POINT_ISILON': u'/SIIFX', u'NFS_ENDPOINT_ISILON': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH'}, {u'NFS_MOUNT_POINT_ISILON_2': u'/SIIFX_B2B', u'NFS_ENDPOINT_ISILON_2': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX'}]", 
2026-10-23T15:06:01.2350697Z             "Nome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           ", 
2026-10-23T15:06:01.2351054Z             "------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------", 
2026-10-23T15:06:01.2351453Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH /SIIFX                              ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-23T15:06:01.2351615Z             "nfs_path=/SIIFX", 
2026-10-23T15:06:01.2351837Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH", 
2026-10-23T15:06:01.2352179Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH /SIIFX                              ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-23T15:06:01.2352399Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX /SIIFX_B2B                          ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-23T15:06:01.2352623Z             "nfs_path=/SIIFX_B2B", 
2026-10-23T15:06:01.2352774Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX", 
2026-10-23T15:06:01.2352969Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX /SIIFX_B2B                          ISILON                              nfsctcnprd.ctc.caixa                des                                "
2026-10-23T15:06:01.2353119Z         ]
2026-10-23T15:06:01.2353263Z     }
2026-10-23T15:06:01.2353361Z }
2026-10-23T15:06:01.2375443Z Friday 23 October 2026  12:06:01 -0300 (0:00:00.068)       0:00:05.652 ******** 
2026-10-23T15:06:01.5900355Z 
2026-10-23T15:06:01.5902989Z TASK [nfs : execute clean json] ************************************************
2026-10-23T15:06:01.5903236Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-23T15:06:01.5903619Z caddeapllx2695.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-23T15:06:01.5903818Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-23T15:06:01.5903993Z releases. A future Ansible release will default to using the discovered 
2026-10-23T15:06:01.5904170Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-23T15:06:01.5904353Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-23T15:06:01.5904520Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-23T15:06:01.5904689Z setting deprecation_warnings=False in ansible.cfg.
2026-10-23T15:06:01.5904839Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:01.5935259Z Friday 23 October 2026  12:06:01 -0300 (0:00:00.355)       0:00:06.008 ******** 
2026-10-23T15:06:01.6552512Z 
2026-10-23T15:06:01.6553017Z TASK [nfs : result_new_string_json] ********************************************
2026-10-23T15:06:01.6555357Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-23T15:06:01.6555520Z     "msg": {
2026-10-23T15:06:01.6556051Z         "ansible_facts": {
2026-10-23T15:06:01.6556249Z             "discovered_interpreter_python": "/usr/bin/python"
2026-10-23T15:06:01.6556378Z         }, 
2026-10-23T15:06:01.6556492Z         "changed": true, 
2026-10-23T15:06:01.6557304Z         "cmd": "echo '[{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH\",\"NFS_MOUNT_POINT_ISILON\": \"/SIIFX\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX\",\"NFS_MOUNT_POINT_ISILON_2\": \"/SIIFX_B2B\"}]' | sed 's/NFS_ENDPOINT_ISILON[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_ISILON[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_HUAWEI[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_HUAWEI[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_VM[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_VM[^\"]*/NFS_MOUNT_POINT/g'", 
2026-10-23T15:06:01.6557746Z         "delta": "0:00:00.004165", 
2026-10-23T15:06:01.6557878Z         "deprecations": [
2026-10-23T15:06:01.6557986Z             {
2026-10-23T15:06:01.6558549Z                 "msg": "Distribution rhel 9.3 on host caddeapllx2695.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, but is using /usr/bin/python for backward compatibility with prior Ansible releases. A future Ansible release will default to using the discovered platform python for this host. See https://docs.ansible.com/ansible/2.9/reference_appendices/interpreter_discovery.html for more information", 
2026-10-23T15:06:01.6558835Z                 "version": "2.12"
2026-10-23T15:06:01.6558945Z             }
2026-10-23T15:06:01.6559040Z         ], 
2026-10-23T15:06:01.6559212Z         "end": "2026-10-23 12:06:01.571769", 
2026-10-23T15:06:01.6559385Z         "failed": false, 
2026-10-23T15:06:01.6559495Z         "rc": 0, 
2026-10-23T15:06:01.6559669Z         "start": "2026-10-23 12:06:01.567604", 
2026-10-23T15:06:01.6559794Z         "stderr": "", 
2026-10-23T15:06:01.6559906Z         "stderr_lines": [], 
2026-10-23T15:06:01.6560633Z         "stdout": "[{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH\",\"NFS_MOUNT_POINT\": \"/SIIFX\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX\",\"NFS_MOUNT_POINT\": \"/SIIFX_B2B\"}]", 
2026-10-23T15:06:01.6562212Z         "stdout_lines": [
2026-10-23T15:06:01.6562739Z             "[{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH\",\"NFS_MOUNT_POINT\": \"/SIIFX\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX\",\"NFS_MOUNT_POINT\": \"/SIIFX_B2B\"}]"
2026-10-23T15:06:01.6563228Z         ]
2026-10-23T15:06:01.6563327Z     }
2026-10-23T15:06:01.6563426Z }
2026-10-23T15:06:01.6588528Z Friday 23 October 2026  12:06:01 -0300 (0:00:00.065)       0:00:06.074 ******** 
2026-10-23T15:06:01.7203990Z 
2026-10-23T15:06:01.7204571Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-23T15:06:01.7204768Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:01.7234574Z Friday 23 October 2026  12:06:01 -0300 (0:00:00.064)       0:00:06.138 ******** 
2026-10-23T15:06:01.7841894Z 
2026-10-23T15:06:01.7842358Z TASK [nfs : result_new_json] ***************************************************
2026-10-23T15:06:01.7843116Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-23T15:06:01.7843253Z     "msg": [
2026-10-23T15:06:01.7843362Z         {
2026-10-23T15:06:01.7844143Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH", 
2026-10-23T15:06:01.7844410Z             "NFS_MOUNT_POINT": "/SIIFX"
2026-10-23T15:06:01.7844524Z         }, 
2026-10-23T15:06:01.7844628Z         {
2026-10-23T15:06:01.7844772Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX", 
2026-10-23T15:06:01.7844928Z             "NFS_MOUNT_POINT": "/SIIFX_B2B"
2026-10-23T15:06:01.7845037Z         }
2026-10-23T15:06:01.7845141Z     ]
2026-10-23T15:06:01.7845325Z }
2026-10-23T15:06:01.7876682Z Friday 23 October 2026  12:06:01 -0300 (0:00:00.064)       0:00:06.202 ******** 
2026-10-23T15:06:01.8558109Z included: /opt/ads-agent/_work/r19403/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2695.agil.nprd.caixa.gov.br
2026-10-23T15:06:01.8636414Z included: /opt/ads-agent/_work/r19403/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2695.agil.nprd.caixa.gov.br
2026-10-23T15:06:01.8695173Z Friday 23 October 2026  12:06:01 -0300 (0:00:00.081)       0:00:06.284 ******** 
2026-10-23T15:06:01.9280080Z 
2026-10-23T15:06:01.9281123Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-23T15:06:01.9281397Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:01.9311885Z Friday 23 October 2026  12:06:01 -0300 (0:00:00.061)       0:00:06.346 ******** 
2026-10-23T15:06:01.9885662Z 
2026-10-23T15:06:01.9886675Z TASK [nfs : debug] *************************************************************
2026-10-23T15:06:01.9888075Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-23T15:06:01.9888342Z     "msg": {
2026-10-23T15:06:01.9888836Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH", 
2026-10-23T15:06:01.9889098Z         "NFS_MOUNT_POINT": "/SIIFX"
2026-10-23T15:06:01.9889278Z     }
2026-10-23T15:06:01.9889436Z }
2026-10-23T15:06:01.9920339Z Friday 23 October 2026  12:06:01 -0300 (0:00:00.060)       0:00:06.407 ******** 
2026-10-23T15:06:02.0495435Z 
2026-10-23T15:06:02.0495994Z TASK [nfs : debug] *************************************************************
2026-10-23T15:06:02.0496178Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-23T15:06:02.0496312Z     "msg": "/SIIFX"
2026-10-23T15:06:02.0496415Z }
2026-10-23T15:06:02.0529687Z Friday 23 October 2026  12:06:02 -0300 (0:00:00.060)       0:00:06.468 ******** 
2026-10-23T15:06:02.1095547Z 
2026-10-23T15:06:02.1096098Z TASK [nfs : debug] *************************************************************
2026-10-23T15:06:02.1096611Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-23T15:06:02.1097001Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIIFX-BATCH"
2026-10-23T15:06:02.1097141Z }
2026-10-23T15:06:02.1129977Z Friday 23 October 2026  12:06:02 -0300 (0:00:00.060)       0:00:06.528 ******** 
2026-10-23T15:06:02.1728073Z 
2026-10-23T15:06:02.1728638Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-23T15:06:02.1728823Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-23T15:06:02.1729341Z     "changed": false, 
2026-10-23T15:06:02.1729469Z     "msg": "All assertions passed"
2026-10-23T15:06:02.1729569Z }
2026-10-23T15:06:02.1764335Z Friday 23 October 2026  12:06:02 -0300 (0:00:00.063)       0:00:06.591 ******** 
2026-10-23T15:06:05.6958992Z 
2026-10-23T15:06:05.6959577Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-23T15:06:05.6959782Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:05.7005855Z Friday 23 October 2026  12:06:05 -0300 (0:00:03.524)       0:00:10.115 ******** 
2026-10-23T15:06:06.4847332Z 
2026-10-23T15:06:06.4847894Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-23T15:06:06.4848209Z [WARNING]: Consider using the yum, dnf or zypper module rather than running
2026-10-23T15:06:06.4848595Z 'rpm'.  If you need to use command because yum, dnf or zypper is insufficient
2026-10-23T15:06:06.4848835Z you can add 'warn: false' to this command task or set 'command_warnings=False'
2026-10-23T15:06:06.4849013Z in ansible.cfg to get rid of this message.
2026-10-23T15:06:06.4854336Z fatal: [caddeapllx2695.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.532080", "end": "2026-10-23 12:06:06.467691", "msg": "non-zero return code", "rc": 1, "start": "2026-10-23 12:06:05.935611", "stderr": "aviso: /var/tmp/rpm-tmp.IskY6q: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.IskY6q: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-23T15:06:06.4855068Z ...ignoring
2026-10-23T15:06:06.4888417Z Friday 23 October 2026  12:06:06 -0300 (0:00:00.788)       0:00:10.904 ******** 
2026-10-23T15:06:07.2434603Z 
2026-10-23T15:06:07.2435165Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-23T15:06:07.2440208Z fatal: [caddeapllx2695.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.506688", "end": "2026-10-23 12:06:07.226344", "msg": "non-zero return code", "rc": 1, "start": "2026-10-23 12:06:06.719656", "stderr": "aviso: /var/tmp/rpm-tmp.Ot0p3e: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.Ot0p3e: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-23T15:06:07.2441662Z ...ignoring
2026-10-23T15:06:07.2476831Z Friday 23 October 2026  12:06:07 -0300 (0:00:00.758)       0:00:11.662 ******** 
2026-10-23T15:06:07.6772207Z 
2026-10-23T15:06:07.6773374Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-23T15:06:07.6773993Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:07.6808666Z Friday 23 October 2026  12:06:07 -0300 (0:00:00.433)       0:00:12.096 ******** 
2026-10-23T15:06:07.9380648Z 
2026-10-23T15:06:07.9381223Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-23T15:06:07.9381397Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:07.9416326Z Friday 23 October 2026  12:06:07 -0300 (0:00:00.260)       0:00:12.356 ******** 
2026-10-23T15:06:08.8670003Z 
2026-10-23T15:06:08.8671226Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-23T15:06:08.8671451Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:08.8716580Z Friday 23 October 2026  12:06:08 -0300 (0:00:00.929)       0:00:13.286 ******** 
2026-10-23T15:06:09.1352923Z 
2026-10-23T15:06:09.1353498Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-23T15:06:09.1353691Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:09.1386559Z Friday 23 October 2026  12:06:09 -0300 (0:00:00.266)       0:00:13.553 ******** 
2026-10-23T15:06:19.5577773Z 
2026-10-23T15:06:19.5578758Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-23T15:06:19.5578970Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:19.5613752Z Friday 23 October 2026  12:06:19 -0300 (0:00:10.422)       0:00:23.976 ******** 
2026-10-23T15:06:19.9957792Z 
2026-10-23T15:06:19.9958378Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-23T15:06:19.9958550Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:19.9992605Z Friday 23 October 2026  12:06:19 -0300 (0:00:00.437)       0:00:24.414 ******** 
2026-10-23T15:06:20.0452978Z Friday 23 October 2026  12:06:20 -0300 (0:00:00.045)       0:00:24.460 ******** 
2026-10-23T15:06:20.1032189Z 
2026-10-23T15:06:20.1033118Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-23T15:06:20.1033477Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:20.1064224Z Friday 23 October 2026  12:06:20 -0300 (0:00:00.061)       0:00:24.521 ******** 
2026-10-23T15:06:20.1662434Z 
2026-10-23T15:06:20.1663355Z TASK [nfs : debug] *************************************************************
2026-10-23T15:06:20.1663735Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-23T15:06:20.1663897Z     "msg": {
2026-10-23T15:06:20.1664534Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX", 
2026-10-23T15:06:20.1664741Z         "NFS_MOUNT_POINT": "/SIIFX_B2B"
2026-10-23T15:06:20.1664844Z     }
2026-10-23T15:06:20.1664944Z }
2026-10-23T15:06:20.1699276Z Friday 23 October 2026  12:06:20 -0300 (0:00:00.063)       0:00:24.584 ******** 
2026-10-23T15:06:20.2285168Z 
2026-10-23T15:06:20.2285878Z TASK [nfs : debug] *************************************************************
2026-10-23T15:06:20.2286079Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-23T15:06:20.2286221Z     "msg": "/SIIFX_B2B"
2026-10-23T15:06:20.2286315Z }
2026-10-23T15:06:20.2321815Z Friday 23 October 2026  12:06:20 -0300 (0:00:00.062)       0:00:24.647 ******** 
2026-10-23T15:06:20.2897979Z 
2026-10-23T15:06:20.2898674Z TASK [nfs : debug] *************************************************************
2026-10-23T15:06:20.2899238Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-23T15:06:20.2899802Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIRJ/NPRD/B2B/SIIFX"
2026-10-23T15:06:20.2899940Z }
2026-10-23T15:06:20.2934464Z Friday 23 October 2026  12:06:20 -0300 (0:00:00.061)       0:00:24.708 ******** 
2026-10-23T15:06:20.3556264Z 
2026-10-23T15:06:20.3556742Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-23T15:06:20.3556926Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-23T15:06:20.3557060Z     "changed": false, 
2026-10-23T15:06:20.3557485Z     "msg": "All assertions passed"
2026-10-23T15:06:20.3557605Z }
2026-10-23T15:06:20.3589890Z Friday 23 October 2026  12:06:20 -0300 (0:00:00.065)       0:00:24.774 ******** 
2026-10-23T15:06:22.9778031Z 
2026-10-23T15:06:22.9778997Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-23T15:06:22.9779221Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:22.9812671Z Friday 23 October 2026  12:06:22 -0300 (0:00:02.622)       0:00:27.396 ******** 
2026-10-23T15:06:23.7889033Z 
2026-10-23T15:06:23.7889997Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-23T15:06:23.7894285Z fatal: [caddeapllx2695.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.560736", "end": "2026-10-23 12:06:23.771090", "msg": "non-zero return code", "rc": 1, "start": "2026-10-23 12:06:23.210354", "stderr": "aviso: /var/tmp/rpm-tmp.26QnAm: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.26QnAm: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-23T15:06:23.7894964Z ...ignoring
2026-10-23T15:06:23.7928879Z Friday 23 October 2026  12:06:23 -0300 (0:00:00.811)       0:00:28.208 ******** 
2026-10-23T15:06:24.5321072Z 
2026-10-23T15:06:24.5321766Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-23T15:06:24.5326352Z fatal: [caddeapllx2695.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.492280", "end": "2026-10-23 12:06:24.515506", "msg": "non-zero return code", "rc": 1, "start": "2026-10-23 12:06:24.023226", "stderr": "aviso: /var/tmp/rpm-tmp.0xb9Uk: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.0xb9Uk: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-23T15:06:24.5327005Z ...ignoring
2026-10-23T15:06:24.5361847Z Friday 23 October 2026  12:06:24 -0300 (0:00:00.743)       0:00:28.951 ******** 
2026-10-23T15:06:24.7856635Z 
2026-10-23T15:06:24.7857420Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-23T15:06:24.7857596Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:24.7899047Z Friday 23 October 2026  12:06:24 -0300 (0:00:00.253)       0:00:29.205 ******** 
2026-10-23T15:06:25.0435947Z 
2026-10-23T15:06:25.0436455Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-23T15:06:25.0436636Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:25.0470662Z Friday 23 October 2026  12:06:25 -0300 (0:00:00.257)       0:00:29.462 ******** 
2026-10-23T15:06:25.6779774Z 
2026-10-23T15:06:25.6780316Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-23T15:06:25.6780501Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:25.6830177Z Friday 23 October 2026  12:06:25 -0300 (0:00:00.635)       0:00:30.098 ******** 
2026-10-23T15:06:25.9415387Z 
2026-10-23T15:06:25.9415977Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-23T15:06:25.9416164Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:25.9450374Z Friday 23 October 2026  12:06:25 -0300 (0:00:00.262)       0:00:30.360 ******** 
2026-10-23T15:06:36.3643098Z 
2026-10-23T15:06:36.3644005Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-23T15:06:36.3644274Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:36.3678672Z Friday 23 October 2026  12:06:36 -0300 (0:00:10.422)       0:00:40.782 ******** 
2026-10-23T15:06:36.6410516Z 
2026-10-23T15:06:36.6411004Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-23T15:06:36.6447479Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:36.6447900Z Friday 23 October 2026  12:06:36 -0300 (0:00:00.277)       0:00:41.059 ******** 
2026-10-23T15:06:36.6887366Z 
2026-10-23T15:06:36.6887893Z PLAY [jboss] *******************************************************************
2026-10-23T15:06:36.6914753Z 
2026-10-23T15:06:36.6915393Z PLAY [Copiando deployments adicionais] *****************************************
2026-10-23T15:06:36.6943461Z 
2026-10-23T15:06:36.6943653Z PLAY [Copiando modules adicionais] *********************************************
2026-10-23T15:06:36.6972467Z 
2026-10-23T15:06:36.6972722Z PLAY [jboss] *******************************************************************
2026-10-23T15:06:36.7012715Z 
2026-10-23T15:06:36.7012988Z PLAY [jboss] *******************************************************************
2026-10-23T15:06:36.7042008Z 
2026-10-23T15:06:36.7042217Z PLAY [jboss] *******************************************************************
2026-10-23T15:06:36.7075647Z 
2026-10-23T15:06:36.7075866Z PLAY [jboss] *******************************************************************
2026-10-23T15:06:36.7103525Z 
2026-10-23T15:06:36.7103682Z PLAY [jboss] *******************************************************************
2026-10-23T15:06:36.7128788Z 
2026-10-23T15:06:36.7129187Z PLAY [local] *******************************************************************
2026-10-23T15:06:36.7161715Z [WARNING]: Could not match supplied host pattern, ignoring: instance_restart
2026-10-23T15:06:36.7164752Z 
2026-10-23T15:06:36.7164919Z PLAY [instance_restart] ********************************************************
2026-10-23T15:06:36.7165160Z skipping: no hosts matched
2026-10-23T15:06:36.7168655Z [WARNING]: Could not match supplied host pattern, ignoring: machine_reboot
2026-10-23T15:06:36.7171279Z 
2026-10-23T15:06:36.7171444Z PLAY [machine_reboot] **********************************************************
2026-10-23T15:06:36.7171599Z skipping: no hosts matched
2026-10-23T15:06:36.7177914Z 
2026-10-23T15:06:36.7178077Z PLAY [local] *******************************************************************
2026-10-23T15:06:36.7203605Z [WARNING]: Could not match supplied host pattern, ignoring: instance_stop
2026-10-23T15:06:36.7206203Z 
2026-10-23T15:06:36.7206731Z PLAY [instance_stop] ***********************************************************
2026-10-23T15:06:36.7206879Z skipping: no hosts matched
2026-10-23T15:06:36.7209997Z 
2026-10-23T15:06:36.7210134Z PLAY [machine_reboot] **********************************************************
2026-10-23T15:06:36.7210287Z skipping: no hosts matched
2026-10-23T15:06:36.7216632Z 
2026-10-23T15:06:36.7217120Z PLAY [local] *******************************************************************
2026-10-23T15:06:36.7240622Z [WARNING]: Could not match supplied host pattern, ignoring: escopo_execucao
2026-10-23T15:06:36.7243464Z 
2026-10-23T15:06:36.7243626Z PLAY [Executar o Start do Sirot Connector no escopo definido] ******************
2026-10-23T15:06:36.7243781Z skipping: no hosts matched
2026-10-23T15:06:36.7250534Z 
2026-10-23T15:06:36.7250680Z PLAY [local] *******************************************************************
2026-10-23T15:06:36.7272683Z 
2026-10-23T15:06:36.7272888Z PLAY [Executar o Stop do Sirot Connector] **************************************
2026-10-23T15:06:36.7273079Z skipping: no hosts matched
2026-10-23T15:06:36.7282650Z 
2026-10-23T15:06:36.7282957Z PLAY [Configura TSM] ***********************************************************
2026-10-23T15:06:36.7308450Z 
2026-10-23T15:06:36.7308620Z PLAY [jboss] *******************************************************************
2026-10-23T15:06:36.7348599Z Friday 23 October 2026  12:06:36 -0300 (0:00:00.090)       0:00:41.150 ******** 
2026-10-23T15:06:36.7922505Z 
2026-10-23T15:06:36.7923213Z TASK [Cria variável build_repository_name] *************************************
2026-10-23T15:06:36.7923416Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:36.7955153Z Friday 23 October 2026  12:06:36 -0300 (0:00:00.060)       0:00:41.210 ******** 
2026-10-23T15:06:36.8539651Z 
2026-10-23T15:06:36.8540187Z TASK [Buscando diretorio de config] ********************************************
2026-10-23T15:06:36.8540367Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:36.8643653Z Friday 23 October 2026  12:06:36 -0300 (0:00:00.068)       0:00:41.279 ******** 
2026-10-23T15:06:37.2351422Z 
2026-10-23T15:06:37.2352375Z TASK [Verifica se o arquivo {{ item }}/etc/hosts-{{ sistema_ambiente }} existe] ***
2026-10-23T15:06:37.2352849Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r19403/a/_SIIFX-caixinhas-batch-config)
2026-10-23T15:06:37.5318010Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r19403/a/_SIIFX-caixinhas-batch-config/so)
2026-10-23T15:06:37.5358398Z Friday 23 October 2026  12:06:37 -0300 (0:00:00.671)       0:00:41.950 ******** 
2026-10-23T15:06:37.9591193Z 
2026-10-23T15:06:37.9591768Z TASK [Altera arquivo /etc/hosts] ***********************************************
2026-10-23T15:06:37.9593441Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r19403/a/_SIIFX-caixinhas-batch-config', u'stat': {u'charset': u'us-ascii', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1792767904.5651233, u'block_size': 4096, u'inode': 415244605, u'isgid': False, u'size': 30, u'wgrp': False, u'executable': False, u'isuid': False, u'readable': True, u'isreg': True, u'version': u'18446744072115270223', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'text/plain', u'blocks': 8, u'xoth': False, u'islnk': False, u'nlink': 1, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r19403/a/_SIIFX-caixinhas-batch-config/etc/hosts-des', u'xusr': False, u'atime': 1792767904.5661232, u'isdir': False, u'ctime': 1792767904.5651233, u'isblk': False, u'checksum': u'4a057994371ed4eef904eb2508abb8c246f35ff5', u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0644', u'xgrp': False, u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r19403/a/_SIIFX-caixinhas-batch-config/etc/hosts-des', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-23T15:06:37.9683292Z 
2026-10-23T15:06:37.9683606Z PLAY [Configura Control-M] *****************************************************
2026-10-23T15:06:37.9737267Z Friday 23 October 2026  12:06:37 -0300 (0:00:00.437)       0:00:42.388 ******** 
2026-10-23T15:06:38.6017957Z 
2026-10-23T15:06:38.6018507Z TASK [Gathering Facts] *********************************************************
2026-10-23T15:06:38.6019048Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:38.6216743Z Friday 23 October 2026  12:06:38 -0300 (0:00:00.647)       0:00:43.036 ******** 
2026-10-23T15:06:38.8732233Z 
2026-10-23T15:06:38.8732800Z TASK [stat] ********************************************************************
2026-10-23T15:06:38.8732976Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:38.8887304Z Friday 23 October 2026  12:06:38 -0300 (0:00:00.267)       0:00:43.303 ******** 
2026-10-23T15:06:38.9479426Z 
2026-10-23T15:06:38.9480329Z TASK [assert] ******************************************************************
2026-10-23T15:06:38.9480555Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br] => {
2026-10-23T15:06:38.9480688Z     "changed": false, 
2026-10-23T15:06:38.9480812Z     "msg": "All assertions passed"
2026-10-23T15:06:38.9480910Z }
2026-10-23T15:06:38.9631267Z Friday 23 October 2026  12:06:38 -0300 (0:00:00.074)       0:00:43.378 ******** 
2026-10-23T15:06:39.0384077Z 
2026-10-23T15:06:39.0384836Z TASK [control_m : Cria variável ansible] ***************************************
2026-10-23T15:06:39.0385038Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:39.0539562Z Friday 23 October 2026  12:06:39 -0300 (0:00:00.090)       0:00:43.468 ******** 
2026-10-23T15:06:39.8695813Z 
2026-10-23T15:06:39.8696363Z TASK [control_m : Copiando arquivo de certificado] *****************************
2026-10-23T15:06:39.8696565Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:39.8844549Z Friday 23 October 2026  12:06:39 -0300 (0:00:00.830)       0:00:44.299 ******** 
2026-10-23T15:06:40.1468154Z 
2026-10-23T15:06:40.1469255Z TASK [control_m : Executando add-user.sh] **************************************
2026-10-23T15:06:40.1469522Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:40.1618957Z Friday 23 October 2026  12:06:40 -0300 (0:00:00.277)       0:00:44.576 ******** 
2026-10-23T15:06:40.5854110Z 
2026-10-23T15:06:40.5854929Z TASK [control_m : Removendo add-user.sh] ***************************************
2026-10-23T15:06:40.5855148Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:40.6052096Z Friday 23 October 2026  12:06:40 -0300 (0:00:00.443)       0:00:45.020 ******** 
2026-10-23T15:06:40.8623245Z 
2026-10-23T15:06:40.8624323Z TASK [control_m : Criacao diretorio /producao/carga] ***************************
2026-10-23T15:06:40.8624578Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:40.8783189Z Friday 23 October 2026  12:06:40 -0300 (0:00:00.273)       0:00:45.293 ******** 
2026-10-23T15:06:41.1372623Z 
2026-10-23T15:06:41.1373127Z TASK [control_m : Criacao diretorio /producao/suporte] *************************
2026-10-23T15:06:41.1373340Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:41.1524119Z Friday 23 October 2026  12:06:41 -0300 (0:00:00.274)       0:00:45.567 ******** 
2026-10-23T15:06:41.7229702Z 
2026-10-23T15:06:41.7230314Z TASK [control_m : Garante bash_profile] ****************************************
2026-10-23T15:06:41.7230524Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:41.7448922Z Friday 23 October 2026  12:06:41 -0300 (0:00:00.592)       0:00:46.159 ******** 
2026-10-23T15:06:42.0030624Z 
2026-10-23T15:06:42.0031390Z TASK [control_m : Cria Diretório de Scripts] ***********************************
2026-10-23T15:06:42.0031570Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:42.0184630Z Friday 23 October 2026  12:06:42 -0300 (0:00:00.273)       0:00:46.433 ******** 
2026-10-23T15:06:43.6191416Z 
2026-10-23T15:06:43.6192150Z TASK [control_m : Copia Scripts] ***********************************************
2026-10-23T15:06:43.6192675Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:43.6364775Z Friday 23 October 2026  12:06:43 -0300 (0:00:01.617)       0:00:48.051 ******** 
2026-10-23T15:06:43.8980060Z 
2026-10-23T15:06:43.8980631Z TASK [control_m : Verifica se o arquivo /producao//configuration/custom.sh existe] ***
2026-10-23T15:06:43.8980810Z ok: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:43.9136849Z Friday 23 October 2026  12:06:43 -0300 (0:00:00.277)       0:00:48.328 ******** 
2026-10-23T15:06:44.1737627Z 
2026-10-23T15:06:44.1738162Z TASK [control_m : Executa shell customizada] ***********************************
2026-10-23T15:06:44.1738351Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:44.1899047Z Friday 23 October 2026  12:06:44 -0300 (0:00:00.276)       0:00:48.604 ******** 
2026-10-23T15:06:44.8500360Z 
2026-10-23T15:06:44.8501394Z TASK [control_m : Configuração Control-M] **************************************
2026-10-23T15:06:44.8501677Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:06:44.8652544Z Friday 23 October 2026  12:06:44 -0300 (0:00:00.675)       0:00:49.280 ******** 
2026-10-23T15:07:09.8896626Z 
2026-10-23T15:07:09.8899174Z TASK [control_m : Restart ControlM] ********************************************
2026-10-23T15:07:09.8899359Z changed: [caddeapllx2695.agil.nprd.caixa.gov.br]
2026-10-23T15:07:09.8935547Z 
2026-10-23T15:07:09.8935897Z PLAY [jboss] *******************************************************************
2026-10-23T15:07:09.8982305Z 
2026-10-23T15:07:09.8982508Z PLAY [jboss] *******************************************************************
2026-10-23T15:07:09.9024511Z 
2026-10-23T15:07:09.9024831Z PLAY [jboss] *******************************************************************
2026-10-23T15:07:09.9047905Z 
2026-10-23T15:07:09.9048450Z PLAY [jboss] *******************************************************************
2026-10-23T15:07:09.9080516Z 
2026-10-23T15:07:09.9081006Z PLAY [localhost] ***************************************************************
2026-10-23T15:07:09.9104756Z 
2026-10-23T15:07:09.9105107Z PLAY [jboss] *******************************************************************
2026-10-23T15:07:09.9151157Z 
2026-10-23T15:07:09.9190142Z PLAY [jboss] *******************************************************************
2026-10-23T15:07:09.9190252Z 
2026-10-23T15:07:09.9190397Z PLAY [jboss] *******************************************************************
2026-10-23T15:07:09.9225998Z 
2026-10-23T15:07:09.9226253Z PLAY RECAP *********************************************************************
2026-10-23T15:07:09.9226932Z caddeapllx2695.agil.nprd.caixa.gov.br : ok=62   changed=21   unreachable=0    failed=0    skipped=2    rescued=0    ignored=4   
2026-10-23T15:07:09.9227058Z 
2026-10-23T15:07:09.9228402Z Friday 23 October 2026  12:07:09 -0300 (0:00:25.057)       0:01:14.338 ******** 
2026-10-23T15:07:09.9228603Z =============================================================================== 
2026-10-23T15:07:09.9234252Z control_m : Restart ControlM ------------------------------------------- 25.06s
2026-10-23T15:07:09.9234476Z nfs : Networker | Restart networker ------------------------------------ 10.42s
2026-10-23T15:07:09.9237244Z nfs : Networker | Restart networker ------------------------------------ 10.42s
2026-10-23T15:07:09.9237547Z nfs : execute montagem script ------------------------------------------- 4.02s
2026-10-23T15:07:09.9237789Z nfs : Instalando o NFS Client ------------------------------------------- 3.52s
2026-10-23T15:07:09.9238050Z nfs : Instalando o NFS Client ------------------------------------------- 2.62s
2026-10-23T15:07:09.9238291Z control_m : Copia Scripts ----------------------------------------------- 1.62s
2026-10-23T15:07:09.9238522Z nfs : Networker | Start networker --------------------------------------- 0.93s
2026-10-23T15:07:09.9239625Z control_m : Copiando arquivo de certificado ----------------------------- 0.83s
2026-10-23T15:07:09.9239883Z nfs : Install networker lgtoclnt_url ------------------------------------ 0.81s
2026-10-23T15:07:09.9240214Z nfs : Install networker lgtoclnt_url ------------------------------------ 0.79s
2026-10-23T15:07:09.9240448Z nfs : Install networker lgtonmda_url ------------------------------------ 0.76s
2026-10-23T15:07:09.9241355Z nfs : Install networker lgtonmda_url ------------------------------------ 0.74s
2026-10-23T15:07:09.9242249Z control_m : Configuração Control-M -------------------------------------- 0.68s
2026-10-23T15:07:09.9242863Z Verifica se o arquivo {{ item }}/etc/hosts-{{ sistema_ambiente }} existe --- 0.67s
2026-10-23T15:07:09.9243650Z Gathering Facts --------------------------------------------------------- 0.65s
2026-10-23T15:07:09.9243937Z nfs : Networker | Start networker --------------------------------------- 0.64s
2026-10-23T15:07:09.9244192Z control_m : Garante bash_profile ---------------------------------------- 0.59s
2026-10-23T15:07:09.9244424Z Verifica se o arquivo nfs_config.json existe ---------------------------- 0.51s
2026-10-23T15:07:09.9244671Z nfs : Coletar variáveis de ambiente ------------------------------------- 0.47s
2026-10-23T15:07:09.9244934Z Playbook run took 0 days, 0 hours, 1 minutes, 14 seconds
2026-10-23T15:07:09.9984656Z ##[section]Finishing: Configura Control-M
