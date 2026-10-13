2026-10-13T18:26:08.1295645Z ##[debug]Evaluating condition for step: 'Configura Control-M'
2026-10-13T18:26:08.1296171Z ##[debug]Evaluating: succeeded()
2026-10-13T18:26:08.1296339Z ##[debug]Evaluating succeeded:
2026-10-13T18:26:08.1296641Z ##[debug]=> True
2026-10-13T18:26:08.1296847Z ##[debug]Result: True
2026-10-13T18:26:08.1297054Z ##[section]Starting: Configura Control-M
2026-10-13T18:26:08.1300284Z ==============================================================================
2026-10-13T18:26:08.1300365Z Task         : Bash
2026-10-13T18:26:08.1300410Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-13T18:26:08.1300489Z Version      : 3.227.0
2026-10-13T18:26:08.1300533Z Author       : Microsoft Corporation
2026-10-13T18:26:08.1300585Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-13T18:26:08.1300668Z ==============================================================================
2026-10-13T18:26:08.8793897Z ##[debug]Invoking Method: System.Threading.Tasks.Task <RunAsync>b__9(). Attempt count: 0
2026-10-13T18:26:08.8835539Z ##[debug]Using node path: /opt/ads-agent/externals/node16/bin/node
2026-10-13T18:26:08.9544566Z ##[debug]agent.TempDirectory=/opt/ads-agent/_work/_temp
2026-10-13T18:26:08.9552553Z ##[debug]loading inputs and endpoints
2026-10-13T18:26:08.9555779Z ##[debug]loading INPUT_TARGETTYPE
2026-10-13T18:26:08.9563265Z ##[debug]loading INPUT_FILEPATH
2026-10-13T18:26:08.9564287Z ##[debug]loading INPUT_SCRIPT
2026-10-13T18:26:08.9565116Z ##[debug]loading INPUT_WORKINGDIRECTORY
2026-10-13T18:26:08.9565722Z ##[debug]loading INPUT_FAILONSTDERR
2026-10-13T18:26:08.9567451Z ##[debug]loading ENDPOINT_AUTH_SYSTEMVSSCONNECTION
2026-10-13T18:26:08.9568167Z ##[debug]loading ENDPOINT_AUTH_SCHEME_SYSTEMVSSCONNECTION
2026-10-13T18:26:08.9569837Z ##[debug]loading ENDPOINT_AUTH_PARAMETER_SYSTEMVSSCONNECTION_ACCESSTOKEN
2026-10-13T18:26:08.9574961Z ##[debug]loading SECRET_GRAYLOG_PASSWORD
2026-10-13T18:26:08.9576746Z ##[debug]loading SECRET_ANSIBLE_VAULT
2026-10-13T18:26:08.9578421Z ##[debug]loading SECRET_SENHASERVICO
2026-10-13T18:26:08.9580794Z ##[debug]loading SECRET_OKD_TOKEN_KAFKA
2026-10-13T18:26:08.9582954Z ##[debug]loading SECRET_ARM_ACCESS_KEY
2026-10-13T18:26:08.9585254Z ##[debug]loading SECRET_FORTIFY_PASS
2026-10-13T18:26:08.9586471Z ##[debug]loading SECRET_CV_SENHAORACLE
2026-10-13T18:26:08.9587002Z ##[debug]loading SECRET_BT_SECRETS_PATH
2026-10-13T18:26:08.9587516Z ##[debug]loading SECRET_OKD_TOKEN_PRODUTOS
2026-10-13T18:26:08.9588155Z ##[debug]loading SECRET_TOKEN_INFRAFACIL_MUDANCA
2026-10-13T18:26:08.9588725Z ##[debug]loading SECRET_PW_ISILON
2026-10-13T18:26:08.9590034Z ##[debug]loading SECRET_AZPAT
2026-10-13T18:26:08.9591304Z ##[debug]loading SECRET_FORTIFY_APITOKEN
2026-10-13T18:26:08.9591563Z ##[debug]loading SECRET_TERRAFORM_ESX_PASSWORD
2026-10-13T18:26:08.9593126Z ##[debug]loading SECRET_TOKEN_CRQ
2026-10-13T18:26:08.9593794Z ##[debug]loading SECRET_PW_ALOCAIP
2026-10-13T18:26:08.9594457Z ##[debug]loaded 24
2026-10-13T18:26:08.9599317Z ##[debug]Agent.ProxyUrl=undefined
2026-10-13T18:26:08.9599688Z ##[debug]Agent.CAInfo=undefined
2026-10-13T18:26:08.9599919Z ##[debug]Agent.ClientCert=undefined
2026-10-13T18:26:08.9600673Z ##[debug]Agent.SkipCertValidation=True
2026-10-13T18:26:08.9615433Z ##[debug]check path : /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-13T18:26:08.9617831Z ##[debug]adding resource file: /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-13T18:26:08.9618107Z ##[debug]system.culture=en-US
2026-10-13T18:26:08.9626486Z ##[debug]failOnStderr=false
2026-10-13T18:26:08.9627367Z ##[debug]workingDirectory=/opt/ads-agent/_work/r13380/a
2026-10-13T18:26:08.9627625Z ##[debug]check path : /opt/ads-agent/_work/r13380/a
2026-10-13T18:26:08.9634925Z ##[debug]targetType=inline
2026-10-13T18:26:08.9650780Z ##[debug]bashEnvValue=undefined
2026-10-13T18:26:08.9651332Z ##[debug]script=REPO=$(echo _SICCV-batch | sed 's/_//')
ansible-playbook /opt/ads-agent/_work/r13380/a/esteira-jboss-vm-v2/site.yml --tags controlm,nfs --skip-tags "vm,dns,monitoracao,apache,git_conf,jboss,restart_jboss,stop_jboss,tsm" -e sistema_ambiente=tqs -e sistema_nome=SICCV-batch -e site=ctc_nprd -e centralizadora_operacoes=7261 -e centralizadora_desenvolvimento=7266 -e default_working_directory_tfs=/opt/ads-agent/_work/r13380/a -e build_repository_name_tfs=$REPO -e CTMSHOST=crjdeaprlx038 -e CTMPERMHOSTS=crjdeaprlx038,crjdeaprlx039 -e ATCMNDATA=18007 -e AGCMNDATA=18008
2026-10-13T18:26:08.9651935Z Generating script.
2026-10-13T18:26:08.9652132Z ##[debug]which 'bash'
2026-10-13T18:26:08.9652359Z ##[debug]found: '/bin/bash'
2026-10-13T18:26:08.9652588Z ##[debug]Agent.Version=3.225.2
2026-10-13T18:26:08.9652834Z ##[debug]agent.tempDirectory=/opt/ads-agent/_work/_temp
2026-10-13T18:26:08.9653091Z ##[debug]check path : /opt/ads-agent/_work/_temp
2026-10-13T18:26:08.9653275Z ========================== Starting Command Output ===========================
2026-10-13T18:26:08.9653490Z ##[debug]which '/bin/bash'
2026-10-13T18:26:08.9653724Z ##[debug]found: '/bin/bash'
2026-10-13T18:26:08.9654037Z ##[debug]/bin/bash arg: /opt/ads-agent/_work/_temp/5c7bf6e5-f0cb-4480-9c7b-d0b10943ca76.sh
2026-10-13T18:26:08.9656461Z ##[debug]exec tool: /bin/bash
2026-10-13T18:26:08.9656713Z ##[debug]arguments:
2026-10-13T18:26:08.9656980Z ##[debug]   /opt/ads-agent/_work/_temp/5c7bf6e5-f0cb-4480-9c7b-d0b10943ca76.sh
2026-10-13T18:26:08.9658608Z [command]/bin/bash /opt/ads-agent/_work/_temp/5c7bf6e5-f0cb-4480-9c7b-d0b10943ca76.sh
2026-10-13T18:26:11.1630384Z 
2026-10-13T18:26:11.1631190Z PLAY [local] *******************************************************************
2026-10-13T18:26:11.1916662Z 
2026-10-13T18:26:11.1917170Z PLAY [Configurando o DNS] ******************************************************
2026-10-13T18:26:11.3935124Z 
2026-10-13T18:26:11.3935626Z PLAY [local] *******************************************************************
2026-10-13T18:26:11.3969553Z 
2026-10-13T18:26:11.3969933Z PLAY [Verificando serviços] ****************************************************
2026-10-13T18:26:11.4060472Z 
2026-10-13T18:26:11.4061064Z PLAY [Configuração LDAP] *******************************************************
2026-10-13T18:26:11.4096227Z [WARNING]: Found variable using reserved name: when
2026-10-13T18:26:11.4103325Z 
2026-10-13T18:26:11.4103591Z PLAY [jboss] *******************************************************************
2026-10-13T18:26:11.4195952Z 
2026-10-13T18:26:11.4196324Z PLAY [Stack Jboss] *************************************************************
2026-10-13T18:26:11.4223894Z 
2026-10-13T18:26:11.4264704Z PLAY [jboss] *******************************************************************
2026-10-13T18:26:11.4264813Z 
2026-10-13T18:26:11.4264957Z PLAY [jboss] *******************************************************************
2026-10-13T18:26:11.4546069Z Tuesday 13 October 2026  15:26:11 -0300 (0:00:00.352)       0:00:00.352 ******* 
2026-10-13T18:26:11.9541855Z 
2026-10-13T18:26:11.9542427Z TASK [Verifica se o arquivo nfs_config.json existe] ****************************
2026-10-13T18:26:11.9542637Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:26:11.9572605Z Tuesday 13 October 2026  15:26:11 -0300 (0:00:00.502)       0:00:00.855 ******* 
2026-10-13T18:26:12.0047000Z included: /opt/ads-agent/_work/r13380/a/esteira-jboss-vm-v2/roles/nfs/tasks/get_nfs.yml for caddeapllx2821.agil.nprd.caixa.gov.br
2026-10-13T18:26:12.0090532Z Tuesday 13 October 2026  15:26:12 -0300 (0:00:00.051)       0:00:00.906 ******* 
2026-10-13T18:26:12.0676407Z 
2026-10-13T18:26:12.0677723Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-13T18:26:12.0677950Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:26:12.0723700Z Tuesday 13 October 2026  15:26:12 -0300 (0:00:00.063)       0:00:00.970 ******* 
2026-10-13T18:26:12.5275403Z 
2026-10-13T18:26:12.5276191Z TASK [nfs : Coletar variáveis de ambiente] *************************************
2026-10-13T18:26:12.5276369Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:26:12.5313314Z Tuesday 13 October 2026  15:26:12 -0300 (0:00:00.458)       0:00:01.429 ******* 
2026-10-13T18:26:12.5886047Z 
2026-10-13T18:26:12.5886258Z TASK [nfs : Exibir resultado em JSON] ******************************************
2026-10-13T18:26:12.5888834Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:26:12.5888988Z     "nfs_vars_json": {
2026-10-13T18:26:12.5889103Z         "changed": false, 
2026-10-13T18:26:12.5889316Z         "cmd": "cat /opt/ads-agent/_work/r13380/a/nfs_config.json", 
2026-10-13T18:26:12.5889472Z         "delta": "0:00:00.005585", 
2026-10-13T18:26:12.5889666Z         "end": "2026-10-13 15:26:12.511606", 
2026-10-13T18:26:12.5889792Z         "failed": false, 
2026-10-13T18:26:12.5889900Z         "rc": 0, 
2026-10-13T18:26:12.5890058Z         "start": "2026-10-13 15:26:12.506021", 
2026-10-13T18:26:12.5890189Z         "stderr": "", 
2026-10-13T18:26:12.5890296Z         "stderr_lines": [], 
2026-10-13T18:26:12.5890453Z         "stdout": "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT_VM\": \"/SICCV\"}]", 
2026-10-13T18:26:12.5890609Z         "stdout_lines": [
2026-10-13T18:26:12.5890754Z             "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT_VM\": \"/SICCV\"}]"
2026-10-13T18:26:12.5891049Z         ]
2026-10-13T18:26:12.5891133Z     }
2026-10-13T18:26:12.5891224Z }
2026-10-13T18:26:12.5919669Z Tuesday 13 October 2026  15:26:12 -0300 (0:00:00.060)       0:00:01.489 ******* 
2026-10-13T18:26:12.6515246Z 
2026-10-13T18:26:12.6515817Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-13T18:26:12.6515996Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:26:12.6563514Z Tuesday 13 October 2026  15:26:12 -0300 (0:00:00.064)       0:00:01.554 ******* 
2026-10-13T18:26:13.3242488Z 
2026-10-13T18:26:13.3243135Z TASK [nfs : execute montagem script] *******************************************
2026-10-13T18:26:13.3243377Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:26:13.3278184Z Tuesday 13 October 2026  15:26:13 -0300 (0:00:00.671)       0:00:02.225 ******* 
2026-10-13T18:26:13.3890289Z 
2026-10-13T18:26:13.3890681Z TASK [nfs : ansible.builtin.debug] *********************************************
2026-10-13T18:26:13.3892918Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:26:13.3893060Z     "changed": false, 
2026-10-13T18:26:13.3893167Z     "msg": {
2026-10-13T18:26:13.3893674Z         "changed": true, 
2026-10-13T18:26:13.3893837Z         "cmd": [
2026-10-13T18:26:13.3893959Z             "python", 
2026-10-13T18:26:13.3894370Z             "/opt/ads-agent/_work/r13380/a/esteira-jboss-vm-v2/roles/nfs/files/nfs.py", 
2026-10-13T18:26:13.3894528Z             "montagem", 
2026-10-13T18:26:13.3894680Z             "SICCV-batch", 
2026-10-13T18:26:13.3894793Z             "tqs", 
2026-10-13T18:26:13.3894900Z             "ctc_nprd", 
2026-10-13T18:26:13.3895105Z             "/opt/ads-agent/_work/r13380/a/esteira-jboss-vm-v2", 
2026-10-13T18:26:13.3895246Z             "C&t@d02", 
2026-10-13T18:26:13.3895419Z             "***", 
2026-10-13T18:26:13.3895537Z             "s736651@corp.caixa.gov.br", 
2026-10-13T18:26:13.3895663Z             "***", 
2026-10-13T18:26:13.3895799Z             "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT_VM\": \"/SICCV\"}]"
2026-10-13T18:26:13.3895934Z         ], 
2026-10-13T18:26:13.3896063Z         "delta": "0:00:00.324974", 
2026-10-13T18:26:13.3896247Z         "end": "2026-10-13 15:26:13.306036", 
2026-10-13T18:26:13.3896359Z         "failed": false, 
2026-10-13T18:26:13.3926495Z         "rc": 0, 
2026-10-13T18:26:13.3926760Z         "start": "2026-10-13 15:26:12.981062", 
2026-10-13T18:26:13.3926891Z         "stderr": "", 
2026-10-13T18:26:13.3927004Z         "stderr_lines": [], 
2026-10-13T18:26:13.3927957Z         "stdout": "[{u'NFS_MOUNT_POINT_VM': u'/SICCV', u'NFS_ENDPOINT_VM': u'hypernprd12.ad.caixa:/fs_siccv'}]\nNome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           \n------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------\nhypernprd12.ad.caixa                /fs_siccv                           /SICCV                              VM                                  hypernprd12.ad.caixa                tqs                                \nnfs_path=/SICCV\nnfs_src=hypernprd12.ad.caixa:/fs_siccv\nhypernprd12.ad.caixa                /fs_siccv                           /SICCV                              VM                                  hypernprd12.ad.caixa                tqs                                ", 
2026-10-13T18:26:13.3928618Z         "stdout_lines": [
2026-10-13T18:26:13.3928857Z             "[{u'NFS_MOUNT_POINT_VM': u'/SICCV', u'NFS_ENDPOINT_VM': u'hypernprd12.ad.caixa:/fs_siccv'}]", 
2026-10-13T18:26:13.3929040Z             "Nome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           ", 
2026-10-13T18:26:13.3929518Z             "------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------", 
2026-10-13T18:26:13.3929749Z             "hypernprd12.ad.caixa                /fs_siccv                           /SICCV                              VM                                  hypernprd12.ad.caixa                tqs                                ", 
2026-10-13T18:26:13.3929891Z             "nfs_path=/SICCV", 
2026-10-13T18:26:13.3930004Z             "nfs_src=hypernprd12.ad.caixa:/fs_siccv", 
2026-10-13T18:26:13.3930157Z             "hypernprd12.ad.caixa                /fs_siccv                           /SICCV                              VM                                  hypernprd12.ad.caixa                tqs                                "
2026-10-13T18:26:13.3930288Z         ]
2026-10-13T18:26:13.3930379Z     }
2026-10-13T18:26:13.3930470Z }
2026-10-13T18:26:13.3930703Z Tuesday 13 October 2026  15:26:13 -0300 (0:00:00.064)       0:00:02.290 ******* 
2026-10-13T18:26:13.7542637Z 
2026-10-13T18:26:13.7543181Z TASK [nfs : execute clean json] ************************************************
2026-10-13T18:26:13.7545783Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-13T18:26:13.7546232Z caddeapllx2821.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-13T18:26:13.7546417Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-13T18:26:13.7546592Z releases. A future Ansible release will default to using the discovered 
2026-10-13T18:26:13.7546773Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-13T18:26:13.7546972Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-13T18:26:13.7547139Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-13T18:26:13.7547310Z setting deprecation_warnings=False in ansible.cfg.
2026-10-13T18:26:13.7547454Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:26:13.7577388Z Tuesday 13 October 2026  15:26:13 -0300 (0:00:00.365)       0:00:02.655 ******* 
2026-10-13T18:26:13.8178664Z 
2026-10-13T18:26:13.8179157Z TASK [nfs : result_new_string_json] ********************************************
2026-10-13T18:26:13.8181323Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:26:13.8181838Z     "msg": {
2026-10-13T18:26:13.8182015Z         "ansible_facts": {
2026-10-13T18:26:13.8182156Z             "discovered_interpreter_python": "/usr/bin/python"
2026-10-13T18:26:13.8182269Z         }, 
2026-10-13T18:26:13.8182406Z         "changed": true, 
2026-10-13T18:26:13.8183486Z         "cmd": "echo '[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT_VM\": \"/SICCV\"}]' | sed 's/NFS_ENDPOINT_ISILON[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_ISILON[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_HUAWEI[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_HUAWEI[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_VM[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_VM[^\"]*/NFS_MOUNT_POINT/g'", 
2026-10-13T18:26:13.8183802Z         "delta": "0:00:00.003510", 
2026-10-13T18:26:13.8183919Z         "deprecations": [
2026-10-13T18:26:13.8184023Z             {
2026-10-13T18:26:13.8184693Z                 "msg": "Distribution rhel 9.3 on host caddeapllx2821.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, but is using /usr/bin/python for backward compatibility with prior Ansible releases. A future Ansible release will default to using the discovered platform python for this host. See https://docs.ansible.com/ansible/2.9/reference_appendices/interpreter_discovery.html for more information", 
2026-10-13T18:26:13.8185001Z                 "version": "2.12"
2026-10-13T18:26:13.8185102Z             }
2026-10-13T18:26:13.8185197Z         ], 
2026-10-13T18:26:13.8185358Z         "end": "2026-10-13 15:26:13.737080", 
2026-10-13T18:26:13.8185579Z         "failed": false, 
2026-10-13T18:26:13.8185685Z         "rc": 0, 
2026-10-13T18:26:13.8185859Z         "start": "2026-10-13 15:26:13.733570", 
2026-10-13T18:26:13.8185978Z         "stderr": "", 
2026-10-13T18:26:13.8186078Z         "stderr_lines": [], 
2026-10-13T18:26:13.8186227Z         "stdout": "[{\"NFS_ENDPOINT\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT\": \"/SICCV\"}]", 
2026-10-13T18:26:13.8186371Z         "stdout_lines": [
2026-10-13T18:26:13.8186512Z             "[{\"NFS_ENDPOINT\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT\": \"/SICCV\"}]"
2026-10-13T18:26:13.8186639Z         ]
2026-10-13T18:26:13.8186729Z     }
2026-10-13T18:26:13.8186810Z }
2026-10-13T18:26:13.8212759Z Tuesday 13 October 2026  15:26:13 -0300 (0:00:00.063)       0:00:02.719 ******* 
2026-10-13T18:26:13.8805254Z 
2026-10-13T18:26:13.8805591Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T18:26:13.8805769Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:26:13.8835574Z Tuesday 13 October 2026  15:26:13 -0300 (0:00:00.062)       0:00:02.781 ******* 
2026-10-13T18:26:13.9421610Z 
2026-10-13T18:26:13.9422526Z TASK [nfs : result_new_json] ***************************************************
2026-10-13T18:26:13.9423031Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:26:13.9423425Z     "msg": [
2026-10-13T18:26:13.9423559Z         {
2026-10-13T18:26:13.9423685Z             "NFS_ENDPOINT": "hypernprd12.ad.caixa:/fs_siccv", 
2026-10-13T18:26:13.9423830Z             "NFS_MOUNT_POINT": "/SICCV"
2026-10-13T18:26:13.9423929Z         }
2026-10-13T18:26:13.9425712Z     ]
2026-10-13T18:26:13.9427700Z }
2026-10-13T18:26:13.9452688Z Tuesday 13 October 2026  15:26:13 -0300 (0:00:00.061)       0:00:02.843 ******* 
2026-10-13T18:26:14.0072768Z included: /opt/ads-agent/_work/r13380/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2821.agil.nprd.caixa.gov.br
2026-10-13T18:26:14.0132418Z Tuesday 13 October 2026  15:26:14 -0300 (0:00:00.067)       0:00:02.910 ******* 
2026-10-13T18:26:14.0695894Z 
2026-10-13T18:26:14.0696304Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T18:26:14.0696474Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:26:14.0725571Z Tuesday 13 October 2026  15:26:14 -0300 (0:00:00.059)       0:00:02.970 ******* 
2026-10-13T18:26:14.1280848Z 
2026-10-13T18:26:14.1281240Z TASK [nfs : debug] *************************************************************
2026-10-13T18:26:14.1282283Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:26:14.1282819Z     "msg": {
2026-10-13T18:26:14.1283003Z         "NFS_ENDPOINT": "hypernprd12.ad.caixa:/fs_siccv", 
2026-10-13T18:26:14.1283141Z         "NFS_MOUNT_POINT": "/SICCV"
2026-10-13T18:26:14.1283582Z     }
2026-10-13T18:26:14.1283665Z }
2026-10-13T18:26:14.1314560Z Tuesday 13 October 2026  15:26:14 -0300 (0:00:00.058)       0:00:03.029 ******* 
2026-10-13T18:26:14.1874597Z 
2026-10-13T18:26:14.1875033Z TASK [nfs : debug] *************************************************************
2026-10-13T18:26:14.1875228Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:26:14.1875364Z     "msg": "/SICCV"
2026-10-13T18:26:14.1875465Z }
2026-10-13T18:26:14.1905713Z Tuesday 13 October 2026  15:26:14 -0300 (0:00:00.059)       0:00:03.088 ******* 
2026-10-13T18:26:14.2475963Z 
2026-10-13T18:26:14.2476571Z TASK [nfs : debug] *************************************************************
2026-10-13T18:26:14.2477087Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:26:14.2477302Z     "msg": "hypernprd12.ad.caixa:/fs_siccv"
2026-10-13T18:26:14.2477416Z }
2026-10-13T18:26:14.2509342Z Tuesday 13 October 2026  15:26:14 -0300 (0:00:00.060)       0:00:03.148 ******* 
2026-10-13T18:26:14.3090416Z 
2026-10-13T18:26:14.3091269Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T18:26:14.3091527Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:26:14.3091920Z     "changed": false, 
2026-10-13T18:26:14.3092051Z     "msg": "All assertions passed"
2026-10-13T18:26:14.3092156Z }
2026-10-13T18:26:14.3125463Z Tuesday 13 October 2026  15:26:14 -0300 (0:00:00.061)       0:00:03.210 ******* 
2026-10-13T18:26:17.6285710Z 
2026-10-13T18:26:17.6286242Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T18:26:17.6286466Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:26:17.6321351Z Tuesday 13 October 2026  15:26:17 -0300 (0:00:03.319)       0:00:06.529 ******* 
2026-10-13T18:26:18.5409893Z 
2026-10-13T18:26:18.5410395Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T18:26:18.5410630Z [WARNING]: Consider using the yum, dnf or zypper module rather than running
2026-10-13T18:26:18.5411026Z 'rpm'.  If you need to use command because yum, dnf or zypper is insufficient
2026-10-13T18:26:18.5411275Z you can add 'warn: false' to this command task or set 'command_warnings=False'
2026-10-13T18:26:18.5411444Z in ansible.cfg to get rid of this message.
2026-10-13T18:26:18.5415612Z fatal: [caddeapllx2821.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.658911", "end": "2026-10-13 15:26:18.524689", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 15:26:17.865778", "stderr": "aviso: /var/tmp/rpm-tmp.DZoBgx: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.DZoBgx: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T18:26:18.5416230Z ...ignoring
2026-10-13T18:26:18.5457768Z Tuesday 13 October 2026  15:26:18 -0300 (0:00:00.913)       0:00:07.443 ******* 
2026-10-13T18:26:19.4720516Z 
2026-10-13T18:26:19.4721133Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T18:26:19.4725654Z fatal: [caddeapllx2821.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.685207", "end": "2026-10-13 15:26:19.454525", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 15:26:18.769318", "stderr": "aviso: /var/tmp/rpm-tmp.GfsTd1: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.GfsTd1: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T18:26:19.4726644Z ...ignoring
2026-10-13T18:26:19.4761812Z Tuesday 13 October 2026  15:26:19 -0300 (0:00:00.930)       0:00:08.373 ******* 
2026-10-13T18:26:19.8869385Z 
2026-10-13T18:26:19.8869939Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T18:26:19.8870272Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:26:19.8905033Z Tuesday 13 October 2026  15:26:19 -0300 (0:00:00.414)       0:00:08.788 ******* 
2026-10-13T18:26:20.1365675Z 
2026-10-13T18:26:20.1366222Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T18:26:20.1366801Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:26:20.1404180Z Tuesday 13 October 2026  15:26:20 -0300 (0:00:00.249)       0:00:09.038 ******* 
2026-10-13T18:26:21.0321761Z 
2026-10-13T18:26:21.0322246Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T18:26:21.0322465Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:26:21.0367069Z Tuesday 13 October 2026  15:26:21 -0300 (0:00:00.896)       0:00:09.934 ******* 
2026-10-13T18:26:21.2909320Z 
2026-10-13T18:26:21.2909907Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T18:26:21.2910249Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:26:21.2943608Z Tuesday 13 October 2026  15:26:21 -0300 (0:00:00.257)       0:00:10.192 ******* 
2026-10-13T18:26:31.6818445Z 
2026-10-13T18:26:31.6818997Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T18:26:31.6819168Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:26:31.6851496Z Tuesday 13 October 2026  15:26:31 -0300 (0:00:10.390)       0:00:20.582 ******* 
2026-10-13T18:28:43.9889774Z 
2026-10-13T18:28:43.9890283Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T18:28:43.9890507Z fatal: [caddeapllx2821.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "msg": "Error mounting /SICCV: mount.nfs: No route to host\n"}
2026-10-13T18:28:43.9895083Z ...ignoring
2026-10-13T18:28:43.9925774Z Tuesday 13 October 2026  15:28:43 -0300 (0:02:12.307)       0:02:32.890 ******* 
2026-10-13T18:28:44.0560779Z 
2026-10-13T18:28:44.0561587Z TASK [nfs : Validando Montagem] ************************************************
2026-10-13T18:28:44.0561835Z fatal: [caddeapllx2821.agil.nprd.caixa.gov.br]: FAILED! => {
2026-10-13T18:28:44.0562187Z     "assertion": "'Connection refused' in mountnfs.msg", 
2026-10-13T18:28:44.0562316Z     "changed": false, 
2026-10-13T18:28:44.0563239Z     "evaluated_to": false, 
2026-10-13T18:28:44.0563581Z     "msg": "Erro desconhecido: Error mounting /SICCV: mount.nfs: No route to host\n"
2026-10-13T18:28:44.0563848Z }
2026-10-13T18:28:44.0569774Z 
2026-10-13T18:28:44.0570026Z PLAY RECAP *********************************************************************
2026-10-13T18:28:44.0570249Z caddeapllx2821.agil.nprd.caixa.gov.br : ok=27   changed=8    unreachable=0    failed=1    skipped=0    rescued=0    ignored=3   
2026-10-13T18:28:44.0570681Z 
2026-10-13T18:28:44.0571315Z Tuesday 13 October 2026  15:28:44 -0300 (0:00:00.064)       0:02:32.954 ******* 
2026-10-13T18:28:44.0571494Z =============================================================================== 
2026-10-13T18:28:44.0575218Z nfs : Montando volume remoto ------------------------------------------ 132.31s
2026-10-13T18:28:44.0575586Z nfs : Networker | Restart networker ------------------------------------ 10.39s
2026-10-13T18:28:44.0575820Z nfs : Instalando o NFS Client ------------------------------------------- 3.32s
2026-10-13T18:28:44.0576058Z nfs : Install networker lgtonmda_url ------------------------------------ 0.93s
2026-10-13T18:28:44.0576283Z nfs : Install networker lgtoclnt_url ------------------------------------ 0.91s
2026-10-13T18:28:44.0576509Z nfs : Networker | Start networker --------------------------------------- 0.90s
2026-10-13T18:28:44.0576738Z nfs : execute montagem script ------------------------------------------- 0.67s
2026-10-13T18:28:44.0576948Z Verifica se o arquivo nfs_config.json existe ---------------------------- 0.50s
2026-10-13T18:28:44.0577184Z nfs : Coletar variáveis de ambiente ------------------------------------- 0.46s
2026-10-13T18:28:44.0577518Z nfs : Remove pacote jbcs-httpd ------------------------------------------ 0.41s
2026-10-13T18:28:44.0577741Z nfs : execute clean json ------------------------------------------------ 0.37s
2026-10-13T18:28:44.0577962Z nfs : Executar o comando abaixo para limitar as portas ------------------ 0.26s
2026-10-13T18:28:44.0578185Z nfs : Create a symbolic link -------------------------------------------- 0.25s
2026-10-13T18:28:44.0578409Z nfs : include_tasks ----------------------------------------------------- 0.07s
2026-10-13T18:28:44.0578618Z nfs : Validando Montagem ------------------------------------------------ 0.06s
2026-10-13T18:28:44.0578836Z nfs : ansible.builtin.debug --------------------------------------------- 0.06s
2026-10-13T18:28:44.0579054Z nfs : Criar variáveis --------------------------------------------------- 0.06s
2026-10-13T18:28:44.0579280Z nfs : result_new_string_json -------------------------------------------- 0.06s
2026-10-13T18:28:44.0579494Z nfs : Criar variáveis --------------------------------------------------- 0.06s
2026-10-13T18:28:44.0579717Z nfs : Parse JSON data --------------------------------------------------- 0.06s
2026-10-13T18:28:44.0579866Z Playbook run took 0 days, 0 hours, 2 minutes, 32 seconds
2026-10-13T18:28:44.1267037Z ##[debug]Exit code 2 received from tool '/bin/bash'
2026-10-13T18:28:44.1267401Z ##[debug]STDIO streams have closed for tool '/bin/bash'
2026-10-13T18:28:44.1296764Z ##[error]Bash exited with code '2'.
2026-10-13T18:28:44.1297292Z ##[debug]Processed: ##vso[task.issue type=error;]Bash exited with code '2'.
2026-10-13T18:28:44.1297743Z ##[debug]task result: Failed
2026-10-13T18:28:44.1298790Z ##[debug]Processed: ##vso[task.complete result=Failed;done=true;]
2026-10-13T18:28:44.1300113Z ##[warning]RetryHelper encountered task failure, will retry (attempt #: 1 out of 2) after 1000 ms
2026-10-13T18:28:45.1299420Z ##[debug]PERF: RetryHelper Method:System.Threading.Tasks.Task <RunAsync>b__9() : took 156250.5097 ms
2026-10-13T18:28:45.1299671Z ##[debug]PERF WARNING: RetryHelper Method:System.Threading.Tasks.Task <RunAsync>b__9() : took 156250.5097 ms
2026-10-13T18:28:45.1302295Z ##[debug]Invoking Method: System.Threading.Tasks.Task <RunAsync>b__9(). Attempt count: 1
2026-10-13T18:28:45.1345143Z ##[debug]Using node path: /opt/ads-agent/externals/node16/bin/node
2026-10-13T18:28:45.2054580Z ##[debug]agent.TempDirectory=/opt/ads-agent/_work/_temp
2026-10-13T18:28:45.2062278Z ##[debug]loading inputs and endpoints
2026-10-13T18:28:45.2093493Z ##[debug]loading INPUT_TARGETTYPE
2026-10-13T18:28:45.2094254Z ##[debug]loading INPUT_FILEPATH
2026-10-13T18:28:45.2094558Z ##[debug]loading INPUT_SCRIPT
2026-10-13T18:28:45.2094792Z ##[debug]loading INPUT_WORKINGDIRECTORY
2026-10-13T18:28:45.2095059Z ##[debug]loading INPUT_FAILONSTDERR
2026-10-13T18:28:45.2095309Z ##[debug]loading ENDPOINT_AUTH_SYSTEMVSSCONNECTION
2026-10-13T18:28:45.2095761Z ##[debug]loading ENDPOINT_AUTH_SCHEME_SYSTEMVSSCONNECTION
2026-10-13T18:28:45.2096026Z ##[debug]loading ENDPOINT_AUTH_PARAMETER_SYSTEMVSSCONNECTION_ACCESSTOKEN
2026-10-13T18:28:45.2096299Z ##[debug]loading SECRET_GRAYLOG_PASSWORD
2026-10-13T18:28:45.2096537Z ##[debug]loading SECRET_ANSIBLE_VAULT
2026-10-13T18:28:45.2096764Z ##[debug]loading SECRET_SENHASERVICO
2026-10-13T18:28:45.2097002Z ##[debug]loading SECRET_OKD_TOKEN_KAFKA
2026-10-13T18:28:45.2097242Z ##[debug]loading SECRET_ARM_ACCESS_KEY
2026-10-13T18:28:45.2097462Z ##[debug]loading SECRET_FORTIFY_PASS
2026-10-13T18:28:45.2097694Z ##[debug]loading SECRET_CV_SENHAORACLE
2026-10-13T18:28:45.2097925Z ##[debug]loading SECRET_BT_SECRETS_PATH
2026-10-13T18:28:45.2099477Z ##[debug]loading SECRET_OKD_TOKEN_PRODUTOS
2026-10-13T18:28:45.2099721Z ##[debug]loading SECRET_TOKEN_INFRAFACIL_MUDANCA
2026-10-13T18:28:45.2099968Z ##[debug]loading SECRET_PW_ISILON
2026-10-13T18:28:45.2100208Z ##[debug]loading SECRET_AZPAT
2026-10-13T18:28:45.2100443Z ##[debug]loading SECRET_FORTIFY_APITOKEN
2026-10-13T18:28:45.2100694Z ##[debug]loading SECRET_TERRAFORM_ESX_PASSWORD
2026-10-13T18:28:45.2100941Z ##[debug]loading SECRET_TOKEN_CRQ
2026-10-13T18:28:45.2101265Z ##[debug]loading SECRET_PW_ALOCAIP
2026-10-13T18:28:45.2101494Z ##[debug]loaded 24
2026-10-13T18:28:45.2103201Z ##[debug]Agent.ProxyUrl=undefined
2026-10-13T18:28:45.2103587Z ##[debug]Agent.CAInfo=undefined
2026-10-13T18:28:45.2103825Z ##[debug]Agent.ClientCert=undefined
2026-10-13T18:28:45.2104497Z ##[debug]Agent.SkipCertValidation=True
2026-10-13T18:28:45.2120039Z ##[debug]check path : /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-13T18:28:45.2121134Z ##[debug]adding resource file: /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-13T18:28:45.2121442Z ##[debug]system.culture=en-US
2026-10-13T18:28:45.2129693Z ##[debug]failOnStderr=false
2026-10-13T18:28:45.2130628Z ##[debug]workingDirectory=/opt/ads-agent/_work/r13380/a
2026-10-13T18:28:45.2130897Z ##[debug]check path : /opt/ads-agent/_work/r13380/a
2026-10-13T18:28:45.2131482Z ##[debug]targetType=inline
2026-10-13T18:28:45.2131717Z ##[debug]bashEnvValue=undefined
2026-10-13T18:28:45.2133097Z ##[debug]script=REPO=$(echo _SICCV-batch | sed 's/_//')
ansible-playbook /opt/ads-agent/_work/r13380/a/esteira-jboss-vm-v2/site.yml --tags controlm,nfs --skip-tags "vm,dns,monitoracao,apache,git_conf,jboss,restart_jboss,stop_jboss,tsm" -e sistema_ambiente=tqs -e sistema_nome=SICCV-batch -e site=ctc_nprd -e centralizadora_operacoes=7261 -e centralizadora_desenvolvimento=7266 -e default_working_directory_tfs=/opt/ads-agent/_work/r13380/a -e build_repository_name_tfs=$REPO -e CTMSHOST=crjdeaprlx038 -e CTMPERMHOSTS=crjdeaprlx038,crjdeaprlx039 -e ATCMNDATA=18007 -e AGCMNDATA=18008
2026-10-13T18:28:45.2141767Z Generating script.
2026-10-13T18:28:45.2143512Z ##[debug]which 'bash'
2026-10-13T18:28:45.2149249Z ##[debug]found: '/bin/bash'
2026-10-13T18:28:45.2149772Z ##[debug]Agent.Version=3.225.2
2026-10-13T18:28:45.2150129Z ##[debug]agent.tempDirectory=/opt/ads-agent/_work/_temp
2026-10-13T18:28:45.2150389Z ##[debug]check path : /opt/ads-agent/_work/_temp
2026-10-13T18:28:45.2153705Z ========================== Starting Command Output ===========================
2026-10-13T18:28:45.2153989Z ##[debug]which '/bin/bash'
2026-10-13T18:28:45.2154305Z ##[debug]found: '/bin/bash'
2026-10-13T18:28:45.2155116Z ##[debug]/bin/bash arg: /opt/ads-agent/_work/_temp/dae9e89a-4722-4c10-a934-04ac5c3879a7.sh
2026-10-13T18:28:45.2157535Z ##[debug]exec tool: /bin/bash
2026-10-13T18:28:45.2157773Z ##[debug]arguments:
2026-10-13T18:28:45.2158016Z ##[debug]   /opt/ads-agent/_work/_temp/dae9e89a-4722-4c10-a934-04ac5c3879a7.sh
2026-10-13T18:28:45.2159703Z [command]/bin/bash /opt/ads-agent/_work/_temp/dae9e89a-4722-4c10-a934-04ac5c3879a7.sh
2026-10-13T18:28:47.4308114Z 
2026-10-13T18:28:47.4308636Z PLAY [local] *******************************************************************
2026-10-13T18:28:47.4588634Z 
2026-10-13T18:28:47.4589361Z PLAY [Configurando o DNS] ******************************************************
2026-10-13T18:28:47.6440038Z 
2026-10-13T18:28:47.6440574Z PLAY [local] *******************************************************************
2026-10-13T18:28:47.6475295Z 
2026-10-13T18:28:47.6475727Z PLAY [Verificando serviços] ****************************************************
2026-10-13T18:28:47.6563421Z 
2026-10-13T18:28:47.6563685Z PLAY [Configuração LDAP] *******************************************************
2026-10-13T18:28:47.6600093Z [WARNING]: Found variable using reserved name: when
2026-10-13T18:28:47.6604655Z 
2026-10-13T18:28:47.6604845Z PLAY [jboss] *******************************************************************
2026-10-13T18:28:47.6693315Z 
2026-10-13T18:28:47.6693792Z PLAY [Stack Jboss] *************************************************************
2026-10-13T18:28:47.6721397Z 
2026-10-13T18:28:47.6721564Z PLAY [jboss] *******************************************************************
2026-10-13T18:28:47.6765040Z 
2026-10-13T18:28:47.6765238Z PLAY [jboss] *******************************************************************
2026-10-13T18:28:47.7042083Z Tuesday 13 October 2026  15:28:47 -0300 (0:00:00.336)       0:00:00.336 ******* 
2026-10-13T18:28:48.2125049Z 
2026-10-13T18:28:48.2125729Z TASK [Verifica se o arquivo nfs_config.json existe] ****************************
2026-10-13T18:28:48.2126700Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:28:48.2159160Z Tuesday 13 October 2026  15:28:48 -0300 (0:00:00.511)       0:00:00.847 ******* 
2026-10-13T18:28:48.2646721Z included: /opt/ads-agent/_work/r13380/a/esteira-jboss-vm-v2/roles/nfs/tasks/get_nfs.yml for caddeapllx2821.agil.nprd.caixa.gov.br
2026-10-13T18:28:48.2689994Z Tuesday 13 October 2026  15:28:48 -0300 (0:00:00.053)       0:00:00.901 ******* 
2026-10-13T18:28:48.3284353Z 
2026-10-13T18:28:48.3285047Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-13T18:28:48.3285246Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:28:48.3334666Z Tuesday 13 October 2026  15:28:48 -0300 (0:00:00.064)       0:00:00.965 ******* 
2026-10-13T18:28:48.7836622Z 
2026-10-13T18:28:48.7837363Z TASK [nfs : Coletar variáveis de ambiente] *************************************
2026-10-13T18:28:48.7837556Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:28:48.7871352Z Tuesday 13 October 2026  15:28:48 -0300 (0:00:00.453)       0:00:01.419 ******* 
2026-10-13T18:28:48.8461906Z 
2026-10-13T18:28:48.8462120Z TASK [nfs : Exibir resultado em JSON] ******************************************
2026-10-13T18:28:48.8463550Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:28:48.8464141Z     "nfs_vars_json": {
2026-10-13T18:28:48.8464381Z         "changed": false, 
2026-10-13T18:28:48.8464709Z         "cmd": "cat /opt/ads-agent/_work/r13380/a/nfs_config.json", 
2026-10-13T18:28:48.8464871Z         "delta": "0:00:00.005951", 
2026-10-13T18:28:48.8465078Z         "end": "2026-10-13 15:28:48.767354", 
2026-10-13T18:28:48.8465213Z         "failed": false, 
2026-10-13T18:28:48.8465319Z         "rc": 0, 
2026-10-13T18:28:48.8465478Z         "start": "2026-10-13 15:28:48.761403", 
2026-10-13T18:28:48.8465611Z         "stderr": "", 
2026-10-13T18:28:48.8465719Z         "stderr_lines": [], 
2026-10-13T18:28:48.8465874Z         "stdout": "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT_VM\": \"/SICCV\"}]", 
2026-10-13T18:28:48.8466021Z         "stdout_lines": [
2026-10-13T18:28:48.8466160Z             "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT_VM\": \"/SICCV\"}]"
2026-10-13T18:28:48.8466286Z         ]
2026-10-13T18:28:48.8466379Z     }
2026-10-13T18:28:48.8466469Z }
2026-10-13T18:28:48.8494384Z Tuesday 13 October 2026  15:28:48 -0300 (0:00:00.062)       0:00:01.481 ******* 
2026-10-13T18:28:48.9100257Z 
2026-10-13T18:28:48.9100774Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-13T18:28:48.9101177Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:28:48.9151798Z Tuesday 13 October 2026  15:28:48 -0300 (0:00:00.065)       0:00:01.547 ******* 
2026-10-13T18:28:49.5665519Z 
2026-10-13T18:28:49.5666075Z TASK [nfs : execute montagem script] *******************************************
2026-10-13T18:28:49.5666242Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:28:49.5700297Z Tuesday 13 October 2026  15:28:49 -0300 (0:00:00.654)       0:00:02.202 ******* 
2026-10-13T18:28:49.6304572Z 
2026-10-13T18:28:49.6304820Z TASK [nfs : ansible.builtin.debug] *********************************************
2026-10-13T18:28:49.6308110Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:28:49.6308304Z     "changed": false, 
2026-10-13T18:28:49.6308427Z     "msg": {
2026-10-13T18:28:49.6308537Z         "changed": true, 
2026-10-13T18:28:49.6308634Z         "cmd": [
2026-10-13T18:28:49.6308739Z             "python", 
2026-10-13T18:28:49.6309047Z             "/opt/ads-agent/_work/r13380/a/esteira-jboss-vm-v2/roles/nfs/files/nfs.py", 
2026-10-13T18:28:49.6309203Z             "montagem", 
2026-10-13T18:28:49.6309345Z             "SICCV-batch", 
2026-10-13T18:28:49.6309754Z             "tqs", 
2026-10-13T18:28:49.6309865Z             "ctc_nprd", 
2026-10-13T18:28:49.6310055Z             "/opt/ads-agent/_work/r13380/a/esteira-jboss-vm-v2", 
2026-10-13T18:28:49.6310187Z             "C&t@d02", 
2026-10-13T18:28:49.6310391Z             "***", 
2026-10-13T18:28:49.6310506Z             "s736651@corp.caixa.gov.br", 
2026-10-13T18:28:49.6310622Z             "***", 
2026-10-13T18:28:49.6310759Z             "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT_VM\": \"/SICCV\"}]"
2026-10-13T18:28:49.6310887Z         ], 
2026-10-13T18:28:49.6311006Z         "delta": "0:00:00.294529", 
2026-10-13T18:28:49.6311183Z         "end": "2026-10-13 15:28:49.547179", 
2026-10-13T18:28:49.6311307Z         "failed": false, 
2026-10-13T18:28:49.6311412Z         "rc": 0, 
2026-10-13T18:28:49.6311584Z         "start": "2026-10-13 15:28:49.252650", 
2026-10-13T18:28:49.6311694Z         "stderr": "", 
2026-10-13T18:28:49.6311799Z         "stderr_lines": [], 
2026-10-13T18:28:49.6312747Z         "stdout": "[{u'NFS_MOUNT_POINT_VM': u'/SICCV', u'NFS_ENDPOINT_VM': u'hypernprd12.ad.caixa:/fs_siccv'}]\nNome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           \n------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------\nhypernprd12.ad.caixa                /fs_siccv                           /SICCV                              VM                                  hypernprd12.ad.caixa                tqs                                \nnfs_path=/SICCV\nnfs_src=hypernprd12.ad.caixa:/fs_siccv\nhypernprd12.ad.caixa                /fs_siccv                           /SICCV                              VM                                  hypernprd12.ad.caixa                tqs                                ", 
2026-10-13T18:28:49.6313137Z         "stdout_lines": [
2026-10-13T18:28:49.6313352Z             "[{u'NFS_MOUNT_POINT_VM': u'/SICCV', u'NFS_ENDPOINT_VM': u'hypernprd12.ad.caixa:/fs_siccv'}]", 
2026-10-13T18:28:49.6313525Z             "Nome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           ", 
2026-10-13T18:28:49.6313894Z             "------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------", 
2026-10-13T18:28:49.6314119Z             "hypernprd12.ad.caixa                /fs_siccv                           /SICCV                              VM                                  hypernprd12.ad.caixa                tqs                                ", 
2026-10-13T18:28:49.6314492Z             "nfs_path=/SICCV", 
2026-10-13T18:28:49.6314617Z             "nfs_src=hypernprd12.ad.caixa:/fs_siccv", 
2026-10-13T18:28:49.6314771Z             "hypernprd12.ad.caixa                /fs_siccv                           /SICCV                              VM                                  hypernprd12.ad.caixa                tqs                                "
2026-10-13T18:28:49.6314906Z         ]
2026-10-13T18:28:49.6315000Z     }
2026-10-13T18:28:49.6315080Z }
2026-10-13T18:28:49.6339379Z Tuesday 13 October 2026  15:28:49 -0300 (0:00:00.063)       0:00:02.266 ******* 
2026-10-13T18:28:50.0230039Z 
2026-10-13T18:28:50.0230559Z TASK [nfs : execute clean json] ************************************************
2026-10-13T18:28:50.0232983Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-13T18:28:50.0233389Z caddeapllx2821.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-13T18:28:50.0233597Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-13T18:28:50.0234155Z releases. A future Ansible release will default to using the discovered 
2026-10-13T18:28:50.0234604Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-13T18:28:50.0234775Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-13T18:28:50.0234929Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-13T18:28:50.0235085Z setting deprecation_warnings=False in ansible.cfg.
2026-10-13T18:28:50.0235231Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:28:50.0267844Z Tuesday 13 October 2026  15:28:50 -0300 (0:00:00.392)       0:00:02.658 ******* 
2026-10-13T18:28:50.0889322Z 
2026-10-13T18:28:50.0889820Z TASK [nfs : result_new_string_json] ********************************************
2026-10-13T18:28:50.0891367Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:28:50.0891499Z     "msg": {
2026-10-13T18:28:50.0892106Z         "ansible_facts": {
2026-10-13T18:28:50.0892287Z             "discovered_interpreter_python": "/usr/bin/python"
2026-10-13T18:28:50.0892414Z         }, 
2026-10-13T18:28:50.0892524Z         "changed": true, 
2026-10-13T18:28:50.0893171Z         "cmd": "echo '[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT_VM\": \"/SICCV\"}]' | sed 's/NFS_ENDPOINT_ISILON[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_ISILON[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_HUAWEI[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_HUAWEI[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_VM[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_VM[^\"]*/NFS_MOUNT_POINT/g'", 
2026-10-13T18:28:50.0893603Z         "delta": "0:00:00.003838", 
2026-10-13T18:28:50.0893723Z         "deprecations": [
2026-10-13T18:28:50.0893828Z             {
2026-10-13T18:28:50.0894472Z                 "msg": "Distribution rhel 9.3 on host caddeapllx2821.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, but is using /usr/bin/python for backward compatibility with prior Ansible releases. A future Ansible release will default to using the discovered platform python for this host. See https://docs.ansible.com/ansible/2.9/reference_appendices/interpreter_discovery.html for more information", 
2026-10-13T18:28:50.0894783Z                 "version": "2.12"
2026-10-13T18:28:50.0894886Z             }
2026-10-13T18:28:50.0894969Z         ], 
2026-10-13T18:28:50.0895135Z         "end": "2026-10-13 15:28:50.004945", 
2026-10-13T18:28:50.0895261Z         "failed": false, 
2026-10-13T18:28:50.0895363Z         "rc": 0, 
2026-10-13T18:28:50.0895535Z         "start": "2026-10-13 15:28:50.001107", 
2026-10-13T18:28:50.0895658Z         "stderr": "", 
2026-10-13T18:28:50.0895753Z         "stderr_lines": [], 
2026-10-13T18:28:50.0895898Z         "stdout": "[{\"NFS_ENDPOINT\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT\": \"/SICCV\"}]", 
2026-10-13T18:28:50.0896307Z         "stdout_lines": [
2026-10-13T18:28:50.0896448Z             "[{\"NFS_ENDPOINT\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT\": \"/SICCV\"}]"
2026-10-13T18:28:50.0896580Z         ]
2026-10-13T18:28:50.0896673Z     }
2026-10-13T18:28:50.0896755Z }
2026-10-13T18:28:50.0926115Z Tuesday 13 October 2026  15:28:50 -0300 (0:00:00.065)       0:00:02.724 ******* 
2026-10-13T18:28:50.1548632Z 
2026-10-13T18:28:50.1549109Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T18:28:50.1549321Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:28:50.1577455Z Tuesday 13 October 2026  15:28:50 -0300 (0:00:00.065)       0:00:02.789 ******* 
2026-10-13T18:28:50.2177335Z 
2026-10-13T18:28:50.2178902Z TASK [nfs : result_new_json] ***************************************************
2026-10-13T18:28:50.2179495Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:28:50.2179692Z     "msg": [
2026-10-13T18:28:50.2179880Z         {
2026-10-13T18:28:50.2180081Z             "NFS_ENDPOINT": "hypernprd12.ad.caixa:/fs_siccv", 
2026-10-13T18:28:50.2180278Z             "NFS_MOUNT_POINT": "/SICCV"
2026-10-13T18:28:50.2180744Z         }
2026-10-13T18:28:50.2180840Z     ]
2026-10-13T18:28:50.2180932Z }
2026-10-13T18:28:50.2212750Z Tuesday 13 October 2026  15:28:50 -0300 (0:00:00.063)       0:00:02.853 ******* 
2026-10-13T18:28:50.2846529Z included: /opt/ads-agent/_work/r13380/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2821.agil.nprd.caixa.gov.br
2026-10-13T18:28:50.2905827Z Tuesday 13 October 2026  15:28:50 -0300 (0:00:00.069)       0:00:02.922 ******* 
2026-10-13T18:28:50.3499549Z 
2026-10-13T18:28:50.3500042Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T18:28:50.3500218Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:28:50.3531994Z Tuesday 13 October 2026  15:28:50 -0300 (0:00:00.062)       0:00:02.985 ******* 
2026-10-13T18:28:50.4118945Z 
2026-10-13T18:28:50.4119410Z TASK [nfs : debug] *************************************************************
2026-10-13T18:28:50.4119590Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:28:50.4119725Z     "msg": {
2026-10-13T18:28:50.4119856Z         "NFS_ENDPOINT": "hypernprd12.ad.caixa:/fs_siccv", 
2026-10-13T18:28:50.4119988Z         "NFS_MOUNT_POINT": "/SICCV"
2026-10-13T18:28:50.4120092Z     }
2026-10-13T18:28:50.4120186Z }
2026-10-13T18:28:50.4151199Z Tuesday 13 October 2026  15:28:50 -0300 (0:00:00.061)       0:00:03.047 ******* 
2026-10-13T18:28:50.4708396Z 
2026-10-13T18:28:50.4709130Z TASK [nfs : debug] *************************************************************
2026-10-13T18:28:50.4709644Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:28:50.4709952Z     "msg": "/SICCV"
2026-10-13T18:28:50.4710043Z }
2026-10-13T18:28:50.4741683Z Tuesday 13 October 2026  15:28:50 -0300 (0:00:00.059)       0:00:03.106 ******* 
2026-10-13T18:28:50.5290889Z 
2026-10-13T18:28:50.5291782Z TASK [nfs : debug] *************************************************************
2026-10-13T18:28:50.5292021Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:28:50.5292175Z     "msg": "hypernprd12.ad.caixa:/fs_siccv"
2026-10-13T18:28:50.5292283Z }
2026-10-13T18:28:50.5325613Z Tuesday 13 October 2026  15:28:50 -0300 (0:00:00.058)       0:00:03.164 ******* 
2026-10-13T18:28:50.5909679Z 
2026-10-13T18:28:50.5910210Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T18:28:50.5910390Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:28:50.5910508Z     "changed": false, 
2026-10-13T18:28:50.5910637Z     "msg": "All assertions passed"
2026-10-13T18:28:50.5910742Z }
2026-10-13T18:28:50.5946699Z Tuesday 13 October 2026  15:28:50 -0300 (0:00:00.062)       0:00:03.226 ******* 
2026-10-13T18:28:53.9873725Z 
2026-10-13T18:28:53.9874625Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T18:28:53.9875220Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:28:53.9910855Z Tuesday 13 October 2026  15:28:53 -0300 (0:00:03.396)       0:00:06.623 ******* 
2026-10-13T18:28:54.9938871Z 
2026-10-13T18:28:54.9939174Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T18:28:54.9940696Z [WARNING]: Consider using the yum, dnf or zypper module rather than running
2026-10-13T18:28:54.9941077Z 'rpm'.  If you need to use command because yum, dnf or zypper is insufficient
2026-10-13T18:28:54.9941304Z you can add 'warn: false' to this command task or set 'command_warnings=False'
2026-10-13T18:28:54.9941457Z in ansible.cfg to get rid of this message.
2026-10-13T18:28:54.9945348Z fatal: [caddeapllx2821.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.761197", "end": "2026-10-13 15:28:54.978246", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 15:28:54.217049", "stderr": "aviso: /var/tmp/rpm-tmp.ojhZHl: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.ojhZHl: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T18:28:54.9946123Z ...ignoring
2026-10-13T18:28:54.9979263Z Tuesday 13 October 2026  15:28:54 -0300 (0:00:01.006)       0:00:07.630 ******* 
2026-10-13T18:28:55.8135244Z 
2026-10-13T18:28:55.8135709Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T18:28:55.8140058Z fatal: [caddeapllx2821.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.573773", "end": "2026-10-13 15:28:55.797135", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 15:28:55.223362", "stderr": "aviso: /var/tmp/rpm-tmp.l3kRL0: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.l3kRL0: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T18:28:55.8140710Z ...ignoring
2026-10-13T18:28:55.8176134Z Tuesday 13 October 2026  15:28:55 -0300 (0:00:00.819)       0:00:08.449 ******* 
2026-10-13T18:28:56.2245863Z 
2026-10-13T18:28:56.2246610Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T18:28:56.2246791Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:28:56.2289063Z Tuesday 13 October 2026  15:28:56 -0300 (0:00:00.411)       0:00:08.860 ******* 
2026-10-13T18:28:56.4741510Z 
2026-10-13T18:28:56.4742408Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T18:28:56.4742622Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:28:56.4786561Z Tuesday 13 October 2026  15:28:56 -0300 (0:00:00.249)       0:00:09.110 ******* 
2026-10-13T18:28:57.3762786Z 
2026-10-13T18:28:57.3763408Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T18:28:57.3763595Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:28:57.3807503Z Tuesday 13 October 2026  15:28:57 -0300 (0:00:00.902)       0:00:10.012 ******* 
2026-10-13T18:28:57.6332434Z 
2026-10-13T18:28:57.6332958Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T18:28:57.6333131Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:28:57.6365432Z Tuesday 13 October 2026  15:28:57 -0300 (0:00:00.255)       0:00:10.268 ******* 
2026-10-13T18:29:08.0259876Z 
2026-10-13T18:29:08.0260348Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T18:29:08.0260526Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:29:08.0292224Z Tuesday 13 October 2026  15:29:08 -0300 (0:00:10.392)       0:00:20.661 ******* 
2026-10-13T18:31:20.3413977Z 
2026-10-13T18:31:20.3414672Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T18:31:20.3415316Z fatal: [caddeapllx2821.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "msg": "Error mounting /SICCV: mount.nfs: No route to host\n"}
2026-10-13T18:31:20.3419607Z ...ignoring
2026-10-13T18:31:20.3450486Z Tuesday 13 October 2026  15:31:20 -0300 (0:02:12.315)       0:02:32.977 ******* 
2026-10-13T18:31:20.4067445Z 
2026-10-13T18:31:20.4067905Z TASK [nfs : Validando Montagem] ************************************************
2026-10-13T18:31:20.4068110Z fatal: [caddeapllx2821.agil.nprd.caixa.gov.br]: FAILED! => {
2026-10-13T18:31:20.4068445Z     "assertion": "'Connection refused' in mountnfs.msg", 
2026-10-13T18:31:20.4070584Z     "changed": false, 
2026-10-13T18:31:20.4070749Z     "evaluated_to": false, 
2026-10-13T18:31:20.4070904Z     "msg": "Erro desconhecido: Error mounting /SICCV: mount.nfs: No route to host\n"
2026-10-13T18:31:20.4071077Z }
2026-10-13T18:31:20.4077095Z 
2026-10-13T18:31:20.4077288Z PLAY RECAP *********************************************************************
2026-10-13T18:31:20.4077502Z caddeapllx2821.agil.nprd.caixa.gov.br : ok=27   changed=8    unreachable=0    failed=1    skipped=0    rescued=0    ignored=3   
2026-10-13T18:31:20.4077605Z 
2026-10-13T18:31:20.4078437Z Tuesday 13 October 2026  15:31:20 -0300 (0:00:00.062)       0:02:33.040 ******* 
2026-10-13T18:31:20.4078626Z =============================================================================== 
2026-10-13T18:31:20.4082604Z nfs : Montando volume remoto ------------------------------------------ 132.32s
2026-10-13T18:31:20.4082890Z nfs : Networker | Restart networker ------------------------------------ 10.39s
2026-10-13T18:31:20.4083136Z nfs : Instalando o NFS Client ------------------------------------------- 3.40s
2026-10-13T18:31:20.4083379Z nfs : Install networker lgtoclnt_url ------------------------------------ 1.01s
2026-10-13T18:31:20.4083631Z nfs : Networker | Start networker --------------------------------------- 0.90s
2026-10-13T18:31:20.4083870Z nfs : Install networker lgtonmda_url ------------------------------------ 0.82s
2026-10-13T18:31:20.4084125Z nfs : execute montagem script ------------------------------------------- 0.65s
2026-10-13T18:31:20.4084498Z Verifica se o arquivo nfs_config.json existe ---------------------------- 0.51s
2026-10-13T18:31:20.4084752Z nfs : Coletar variáveis de ambiente ------------------------------------- 0.45s
2026-10-13T18:31:20.4084986Z nfs : Remove pacote jbcs-httpd ------------------------------------------ 0.41s
2026-10-13T18:31:20.4085256Z nfs : execute clean json ------------------------------------------------ 0.39s
2026-10-13T18:31:20.4085572Z nfs : Executar o comando abaixo para limitar as portas ------------------ 0.26s
2026-10-13T18:31:20.4085877Z nfs : Create a symbolic link -------------------------------------------- 0.25s
2026-10-13T18:31:20.4086339Z nfs : include_tasks ----------------------------------------------------- 0.07s
2026-10-13T18:31:20.4086581Z nfs : result_new_string_json -------------------------------------------- 0.07s
2026-10-13T18:31:20.4086813Z nfs : Criar variáveis --------------------------------------------------- 0.07s
2026-10-13T18:31:20.4087036Z nfs : Parse JSON data --------------------------------------------------- 0.07s
2026-10-13T18:31:20.4087260Z nfs : Criar variáveis --------------------------------------------------- 0.06s
2026-10-13T18:31:20.4087565Z nfs : ansible.builtin.debug --------------------------------------------- 0.06s
2026-10-13T18:31:20.4087869Z nfs : result_new_json --------------------------------------------------- 0.06s
2026-10-13T18:31:20.4088079Z Playbook run took 0 days, 0 hours, 2 minutes, 32 seconds
2026-10-13T18:31:20.4766367Z ##[debug]Exit code 2 received from tool '/bin/bash'
2026-10-13T18:31:20.4768240Z ##[debug]STDIO streams have closed for tool '/bin/bash'
2026-10-13T18:31:20.4775594Z ##[error]Bash exited with code '2'.
2026-10-13T18:31:20.4776150Z ##[debug]Processed: ##vso[task.issue type=error;]Bash exited with code '2'.
2026-10-13T18:31:20.4776453Z ##[debug]task result: Failed
2026-10-13T18:31:20.4777560Z ##[debug]Processed: ##vso[task.complete result=Failed;done=true;]
2026-10-13T18:31:20.4806061Z ##[warning]RetryHelper encountered task failure, will retry (attempt #: 2 out of 2) after 4000 ms
2026-10-13T18:31:24.4810861Z ##[debug]PERF: RetryHelper Method:System.Threading.Tasks.Task <RunAsync>b__9() : took 159351.0448 ms
2026-10-13T18:31:24.4811299Z ##[debug]PERF WARNING: RetryHelper Method:System.Threading.Tasks.Task <RunAsync>b__9() : took 159351.0448 ms
2026-10-13T18:31:24.4812022Z ##[debug]Invoking Method: System.Threading.Tasks.Task <RunAsync>b__9(). Attempt count: 2
2026-10-13T18:31:24.4869084Z ##[debug]Using node path: /opt/ads-agent/externals/node16/bin/node
2026-10-13T18:31:24.5609762Z ##[debug]agent.TempDirectory=/opt/ads-agent/_work/_temp
2026-10-13T18:31:24.5617183Z ##[debug]loading inputs and endpoints
2026-10-13T18:31:24.5620303Z ##[debug]loading INPUT_TARGETTYPE
2026-10-13T18:31:24.5628287Z ##[debug]loading INPUT_FILEPATH
2026-10-13T18:31:24.5629038Z ##[debug]loading INPUT_SCRIPT
2026-10-13T18:31:24.5629913Z ##[debug]loading INPUT_WORKINGDIRECTORY
2026-10-13T18:31:24.5630943Z ##[debug]loading INPUT_FAILONSTDERR
2026-10-13T18:31:24.5632315Z ##[debug]loading ENDPOINT_AUTH_SYSTEMVSSCONNECTION
2026-10-13T18:31:24.5633121Z ##[debug]loading ENDPOINT_AUTH_SCHEME_SYSTEMVSSCONNECTION
2026-10-13T18:31:24.5634662Z ##[debug]loading ENDPOINT_AUTH_PARAMETER_SYSTEMVSSCONNECTION_ACCESSTOKEN
2026-10-13T18:31:24.5639675Z ##[debug]loading SECRET_GRAYLOG_PASSWORD
2026-10-13T18:31:24.5641442Z ##[debug]loading SECRET_ANSIBLE_VAULT
2026-10-13T18:31:24.5642766Z ##[debug]loading SECRET_SENHASERVICO
2026-10-13T18:31:24.5644548Z ##[debug]loading SECRET_OKD_TOKEN_KAFKA
2026-10-13T18:31:24.5646235Z ##[debug]loading SECRET_ARM_ACCESS_KEY
2026-10-13T18:31:24.5647626Z ##[debug]loading SECRET_FORTIFY_PASS
2026-10-13T18:31:24.5648297Z ##[debug]loading SECRET_CV_SENHAORACLE
2026-10-13T18:31:24.5649104Z ##[debug]loading SECRET_BT_SECRETS_PATH
2026-10-13T18:31:24.5649544Z ##[debug]loading SECRET_OKD_TOKEN_PRODUTOS
2026-10-13T18:31:24.5650273Z ##[debug]loading SECRET_TOKEN_INFRAFACIL_MUDANCA
2026-10-13T18:31:24.5651075Z ##[debug]loading SECRET_PW_ISILON
2026-10-13T18:31:24.5652172Z ##[debug]loading SECRET_AZPAT
2026-10-13T18:31:24.5652723Z ##[debug]loading SECRET_FORTIFY_APITOKEN
2026-10-13T18:31:24.5653421Z ##[debug]loading SECRET_TERRAFORM_ESX_PASSWORD
2026-10-13T18:31:24.5654637Z ##[debug]loading SECRET_TOKEN_CRQ
2026-10-13T18:31:24.5655128Z ##[debug]loading SECRET_PW_ALOCAIP
2026-10-13T18:31:24.5655617Z ##[debug]loaded 24
2026-10-13T18:31:24.5659974Z ##[debug]Agent.ProxyUrl=undefined
2026-10-13T18:31:24.5660235Z ##[debug]Agent.CAInfo=undefined
2026-10-13T18:31:24.5660469Z ##[debug]Agent.ClientCert=undefined
2026-10-13T18:31:24.5660969Z ##[debug]Agent.SkipCertValidation=True
2026-10-13T18:31:24.5676212Z ##[debug]check path : /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-13T18:31:24.5678260Z ##[debug]adding resource file: /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-13T18:31:24.5678550Z ##[debug]system.culture=en-US
2026-10-13T18:31:24.5686855Z ##[debug]failOnStderr=false
2026-10-13T18:31:24.5687887Z ##[debug]workingDirectory=/opt/ads-agent/_work/r13380/a
2026-10-13T18:31:24.5688371Z ##[debug]check path : /opt/ads-agent/_work/r13380/a
2026-10-13T18:31:24.5688793Z ##[debug]targetType=inline
2026-10-13T18:31:24.5689199Z ##[debug]bashEnvValue=undefined
2026-10-13T18:31:24.5690455Z ##[debug]script=REPO=$(echo _SICCV-batch | sed 's/_//')
ansible-playbook /opt/ads-agent/_work/r13380/a/esteira-jboss-vm-v2/site.yml --tags controlm,nfs --skip-tags "vm,dns,monitoracao,apache,git_conf,jboss,restart_jboss,stop_jboss,tsm" -e sistema_ambiente=tqs -e sistema_nome=SICCV-batch -e site=ctc_nprd -e centralizadora_operacoes=7261 -e centralizadora_desenvolvimento=7266 -e default_working_directory_tfs=/opt/ads-agent/_work/r13380/a -e build_repository_name_tfs=$REPO -e CTMSHOST=crjdeaprlx038 -e CTMPERMHOSTS=crjdeaprlx038,crjdeaprlx039 -e ATCMNDATA=18007 -e AGCMNDATA=18008
2026-10-13T18:31:24.5699100Z Generating script.
2026-10-13T18:31:24.5700893Z ##[debug]which 'bash'
2026-10-13T18:31:24.5706711Z ##[debug]found: '/bin/bash'
2026-10-13T18:31:24.5707105Z ##[debug]Agent.Version=3.225.2
2026-10-13T18:31:24.5707502Z ##[debug]agent.tempDirectory=/opt/ads-agent/_work/_temp
2026-10-13T18:31:24.5707906Z ##[debug]check path : /opt/ads-agent/_work/_temp
2026-10-13T18:31:24.5709578Z ========================== Starting Command Output ===========================
2026-10-13T18:31:24.5711408Z ##[debug]which '/bin/bash'
2026-10-13T18:31:24.5712024Z ##[debug]found: '/bin/bash'
2026-10-13T18:31:24.5712288Z ##[debug]/bin/bash arg: /opt/ads-agent/_work/_temp/5d0a7f71-20c5-4c52-aac2-7f8e2eaf4451.sh
2026-10-13T18:31:24.5714701Z ##[debug]exec tool: /bin/bash
2026-10-13T18:31:24.5715043Z ##[debug]arguments:
2026-10-13T18:31:24.5715423Z ##[debug]   /opt/ads-agent/_work/_temp/5d0a7f71-20c5-4c52-aac2-7f8e2eaf4451.sh
2026-10-13T18:31:24.5717116Z [command]/bin/bash /opt/ads-agent/_work/_temp/5d0a7f71-20c5-4c52-aac2-7f8e2eaf4451.sh
2026-10-13T18:31:26.7006507Z 
2026-10-13T18:31:26.7007024Z PLAY [local] *******************************************************************
2026-10-13T18:31:26.7292533Z 
2026-10-13T18:31:26.7292819Z PLAY [Configurando o DNS] ******************************************************
2026-10-13T18:31:26.9329895Z 
2026-10-13T18:31:26.9330497Z PLAY [local] *******************************************************************
2026-10-13T18:31:26.9364879Z 
2026-10-13T18:31:26.9365323Z PLAY [Verificando serviços] ****************************************************
2026-10-13T18:31:26.9451961Z 
2026-10-13T18:31:26.9452272Z PLAY [Configuração LDAP] *******************************************************
2026-10-13T18:31:26.9486097Z [WARNING]: Found variable using reserved name: when
2026-10-13T18:31:26.9491709Z 
2026-10-13T18:31:26.9491865Z PLAY [jboss] *******************************************************************
2026-10-13T18:31:26.9578797Z 
2026-10-13T18:31:26.9579044Z PLAY [Stack Jboss] *************************************************************
2026-10-13T18:31:26.9606346Z 
2026-10-13T18:31:26.9606537Z PLAY [jboss] *******************************************************************
2026-10-13T18:31:26.9648249Z 
2026-10-13T18:31:26.9648600Z PLAY [jboss] *******************************************************************
2026-10-13T18:31:26.9925410Z Tuesday 13 October 2026  15:31:26 -0300 (0:00:00.351)       0:00:00.351 ******* 
2026-10-13T18:31:27.5078627Z 
2026-10-13T18:31:27.5079131Z TASK [Verifica se o arquivo nfs_config.json existe] ****************************
2026-10-13T18:31:27.5079301Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:31:27.5109036Z Tuesday 13 October 2026  15:31:27 -0300 (0:00:00.518)       0:00:00.870 ******* 
2026-10-13T18:31:27.5588233Z included: /opt/ads-agent/_work/r13380/a/esteira-jboss-vm-v2/roles/nfs/tasks/get_nfs.yml for caddeapllx2821.agil.nprd.caixa.gov.br
2026-10-13T18:31:27.5630436Z Tuesday 13 October 2026  15:31:27 -0300 (0:00:00.052)       0:00:00.922 ******* 
2026-10-13T18:31:27.6218640Z 
2026-10-13T18:31:27.6219201Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-13T18:31:27.6219413Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:31:27.6268822Z Tuesday 13 October 2026  15:31:27 -0300 (0:00:00.063)       0:00:00.986 ******* 
2026-10-13T18:31:28.0678843Z 
2026-10-13T18:31:28.0679566Z TASK [nfs : Coletar variáveis de ambiente] *************************************
2026-10-13T18:31:28.0679759Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:31:28.0713114Z Tuesday 13 October 2026  15:31:28 -0300 (0:00:00.444)       0:00:01.430 ******* 
2026-10-13T18:31:28.1299555Z 
2026-10-13T18:31:28.1300083Z TASK [nfs : Exibir resultado em JSON] ******************************************
2026-10-13T18:31:28.1300577Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:31:28.1300713Z     "nfs_vars_json": {
2026-10-13T18:31:28.1301146Z         "changed": false, 
2026-10-13T18:31:28.1301871Z         "cmd": "cat /opt/ads-agent/_work/r13380/a/nfs_config.json", 
2026-10-13T18:31:28.1302045Z         "delta": "0:00:00.006021", 
2026-10-13T18:31:28.1302224Z         "end": "2026-10-13 15:31:28.050789", 
2026-10-13T18:31:28.1302346Z         "failed": false, 
2026-10-13T18:31:28.1302443Z         "rc": 0, 
2026-10-13T18:31:28.1302627Z         "start": "2026-10-13 15:31:28.044768", 
2026-10-13T18:31:28.1302752Z         "stderr": "", 
2026-10-13T18:31:28.1302862Z         "stderr_lines": [], 
2026-10-13T18:31:28.1304455Z         "stdout": "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT_VM\": \"/SICCV\"}]", 
2026-10-13T18:31:28.1304658Z         "stdout_lines": [
2026-10-13T18:31:28.1304808Z             "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT_VM\": \"/SICCV\"}]"
2026-10-13T18:31:28.1304954Z         ]
2026-10-13T18:31:28.1305050Z     }
2026-10-13T18:31:28.1305131Z }
2026-10-13T18:31:28.1335013Z Tuesday 13 October 2026  15:31:28 -0300 (0:00:00.062)       0:00:01.492 ******* 
2026-10-13T18:31:28.1965547Z 
2026-10-13T18:31:28.1966145Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-13T18:31:28.1966338Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:31:28.2014482Z Tuesday 13 October 2026  15:31:28 -0300 (0:00:00.067)       0:00:01.560 ******* 
2026-10-13T18:31:28.8487206Z 
2026-10-13T18:31:28.8487777Z TASK [nfs : execute montagem script] *******************************************
2026-10-13T18:31:28.8487948Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:31:28.8521922Z Tuesday 13 October 2026  15:31:28 -0300 (0:00:00.650)       0:00:02.211 ******* 
2026-10-13T18:31:28.9123464Z 
2026-10-13T18:31:28.9123975Z TASK [nfs : ansible.builtin.debug] *********************************************
2026-10-13T18:31:28.9125895Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:31:28.9126080Z     "changed": false, 
2026-10-13T18:31:28.9126228Z     "msg": {
2026-10-13T18:31:28.9126407Z         "changed": true, 
2026-10-13T18:31:28.9126518Z         "cmd": [
2026-10-13T18:31:28.9126623Z             "python", 
2026-10-13T18:31:28.9126980Z             "/opt/ads-agent/_work/r13380/a/esteira-jboss-vm-v2/roles/nfs/files/nfs.py", 
2026-10-13T18:31:28.9127128Z             "montagem", 
2026-10-13T18:31:28.9127267Z             "SICCV-batch", 
2026-10-13T18:31:28.9127371Z             "tqs", 
2026-10-13T18:31:28.9127472Z             "ctc_nprd", 
2026-10-13T18:31:28.9127660Z             "/opt/ads-agent/_work/r13380/a/esteira-jboss-vm-v2", 
2026-10-13T18:31:28.9127780Z             "C&t@d02", 
2026-10-13T18:31:28.9127963Z             "***", 
2026-10-13T18:31:28.9128074Z             "s736651@corp.caixa.gov.br", 
2026-10-13T18:31:28.9128191Z             "***", 
2026-10-13T18:31:28.9128629Z             "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT_VM\": \"/SICCV\"}]"
2026-10-13T18:31:28.9128764Z         ], 
2026-10-13T18:31:28.9128899Z         "delta": "0:00:00.298266", 
2026-10-13T18:31:28.9129075Z         "end": "2026-10-13 15:31:28.830399", 
2026-10-13T18:31:28.9129197Z         "failed": false, 
2026-10-13T18:31:28.9129305Z         "rc": 0, 
2026-10-13T18:31:28.9129474Z         "start": "2026-10-13 15:31:28.532133", 
2026-10-13T18:31:28.9129596Z         "stderr": "", 
2026-10-13T18:31:28.9129701Z         "stderr_lines": [], 
2026-10-13T18:31:28.9130658Z         "stdout": "[{u'NFS_MOUNT_POINT_VM': u'/SICCV', u'NFS_ENDPOINT_VM': u'hypernprd12.ad.caixa:/fs_siccv'}]\nNome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           \n------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------\nhypernprd12.ad.caixa                /fs_siccv                           /SICCV                              VM                                  hypernprd12.ad.caixa                tqs                                \nnfs_path=/SICCV\nnfs_src=hypernprd12.ad.caixa:/fs_siccv\nhypernprd12.ad.caixa                /fs_siccv                           /SICCV                              VM                                  hypernprd12.ad.caixa                tqs                                ", 
2026-10-13T18:31:28.9131260Z         "stdout_lines": [
2026-10-13T18:31:28.9131484Z             "[{u'NFS_MOUNT_POINT_VM': u'/SICCV', u'NFS_ENDPOINT_VM': u'hypernprd12.ad.caixa:/fs_siccv'}]", 
2026-10-13T18:31:28.9131659Z             "Nome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           ", 
2026-10-13T18:31:28.9132026Z             "------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------", 
2026-10-13T18:31:28.9132255Z             "hypernprd12.ad.caixa                /fs_siccv                           /SICCV                              VM                                  hypernprd12.ad.caixa                tqs                                ", 
2026-10-13T18:31:28.9132399Z             "nfs_path=/SICCV", 
2026-10-13T18:31:28.9132520Z             "nfs_src=hypernprd12.ad.caixa:/fs_siccv", 
2026-10-13T18:31:28.9132674Z             "hypernprd12.ad.caixa                /fs_siccv                           /SICCV                              VM                                  hypernprd12.ad.caixa                tqs                                "
2026-10-13T18:31:28.9132804Z         ]
2026-10-13T18:31:28.9132899Z     }
2026-10-13T18:31:28.9132981Z }
2026-10-13T18:31:28.9158443Z Tuesday 13 October 2026  15:31:28 -0300 (0:00:00.063)       0:00:02.275 ******* 
2026-10-13T18:31:29.3014835Z 
2026-10-13T18:31:29.3015597Z TASK [nfs : execute clean json] ************************************************
2026-10-13T18:31:29.3017543Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-13T18:31:29.3017943Z caddeapllx2821.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-13T18:31:29.3018140Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-13T18:31:29.3018314Z releases. A future Ansible release will default to using the discovered 
2026-10-13T18:31:29.3018477Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-13T18:31:29.3018654Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-13T18:31:29.3018820Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-13T18:31:29.3019293Z setting deprecation_warnings=False in ansible.cfg.
2026-10-13T18:31:29.3019439Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:31:29.3051770Z Tuesday 13 October 2026  15:31:29 -0300 (0:00:00.389)       0:00:02.664 ******* 
2026-10-13T18:31:29.3651535Z 
2026-10-13T18:31:29.3651984Z TASK [nfs : result_new_string_json] ********************************************
2026-10-13T18:31:29.3654016Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:31:29.3654147Z     "msg": {
2026-10-13T18:31:29.3654364Z         "ansible_facts": {
2026-10-13T18:31:29.3654504Z             "discovered_interpreter_python": "/usr/bin/python"
2026-10-13T18:31:29.3654645Z         }, 
2026-10-13T18:31:29.3654753Z         "changed": true, 
2026-10-13T18:31:29.3655341Z         "cmd": "echo '[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT_VM\": \"/SICCV\"}]' | sed 's/NFS_ENDPOINT_ISILON[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_ISILON[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_HUAWEI[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_HUAWEI[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_VM[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_VM[^\"]*/NFS_MOUNT_POINT/g'", 
2026-10-13T18:31:29.3655971Z         "delta": "0:00:00.003740", 
2026-10-13T18:31:29.3656090Z         "deprecations": [
2026-10-13T18:31:29.3656189Z             {
2026-10-13T18:31:29.3656723Z                 "msg": "Distribution rhel 9.3 on host caddeapllx2821.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, but is using /usr/bin/python for backward compatibility with prior Ansible releases. A future Ansible release will default to using the discovered platform python for this host. See https://docs.ansible.com/ansible/2.9/reference_appendices/interpreter_discovery.html for more information", 
2026-10-13T18:31:29.3657036Z                 "version": "2.12"
2026-10-13T18:31:29.3657126Z             }
2026-10-13T18:31:29.3657220Z         ], 
2026-10-13T18:31:29.3657387Z         "end": "2026-10-13 15:31:29.283828", 
2026-10-13T18:31:29.3657517Z         "failed": false, 
2026-10-13T18:31:29.3657621Z         "rc": 0, 
2026-10-13T18:31:29.3657780Z         "start": "2026-10-13 15:31:29.280088", 
2026-10-13T18:31:29.3657903Z         "stderr": "", 
2026-10-13T18:31:29.3658012Z         "stderr_lines": [], 
2026-10-13T18:31:29.3658162Z         "stdout": "[{\"NFS_ENDPOINT\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT\": \"/SICCV\"}]", 
2026-10-13T18:31:29.3658307Z         "stdout_lines": [
2026-10-13T18:31:29.3658445Z             "[{\"NFS_ENDPOINT\": \"hypernprd12.ad.caixa:/fs_siccv\",\"NFS_MOUNT_POINT\": \"/SICCV\"}]"
2026-10-13T18:31:29.3658560Z         ]
2026-10-13T18:31:29.3658651Z     }
2026-10-13T18:31:29.3658739Z }
2026-10-13T18:31:29.3685635Z Tuesday 13 October 2026  15:31:29 -0300 (0:00:00.063)       0:00:02.727 ******* 
2026-10-13T18:31:29.4275651Z 
2026-10-13T18:31:29.4275937Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T18:31:29.4276513Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:31:29.4304141Z Tuesday 13 October 2026  15:31:29 -0300 (0:00:00.061)       0:00:02.789 ******* 
2026-10-13T18:31:29.4904584Z 
2026-10-13T18:31:29.4905125Z TASK [nfs : result_new_json] ***************************************************
2026-10-13T18:31:29.4905308Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:31:29.4905439Z     "msg": [
2026-10-13T18:31:29.4905543Z         {
2026-10-13T18:31:29.4905667Z             "NFS_ENDPOINT": "hypernprd12.ad.caixa:/fs_siccv", 
2026-10-13T18:31:29.4905837Z             "NFS_MOUNT_POINT": "/SICCV"
2026-10-13T18:31:29.4905991Z         }
2026-10-13T18:31:29.4906073Z     ]
2026-10-13T18:31:29.4906162Z }
2026-10-13T18:31:29.4939093Z Tuesday 13 October 2026  15:31:29 -0300 (0:00:00.063)       0:00:02.853 ******* 
2026-10-13T18:31:29.5551533Z included: /opt/ads-agent/_work/r13380/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2821.agil.nprd.caixa.gov.br
2026-10-13T18:31:29.5609521Z Tuesday 13 October 2026  15:31:29 -0300 (0:00:00.067)       0:00:02.920 ******* 
2026-10-13T18:31:29.6158792Z 
2026-10-13T18:31:29.6159190Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T18:31:29.6159380Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:31:29.6188246Z Tuesday 13 October 2026  15:31:29 -0300 (0:00:00.057)       0:00:02.978 ******* 
2026-10-13T18:31:29.6746778Z 
2026-10-13T18:31:29.6747608Z TASK [nfs : debug] *************************************************************
2026-10-13T18:31:29.6747838Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:31:29.6747964Z     "msg": {
2026-10-13T18:31:29.6748090Z         "NFS_ENDPOINT": "hypernprd12.ad.caixa:/fs_siccv", 
2026-10-13T18:31:29.6748235Z         "NFS_MOUNT_POINT": "/SICCV"
2026-10-13T18:31:29.6748332Z     }
2026-10-13T18:31:29.6748428Z }
2026-10-13T18:31:29.6778676Z Tuesday 13 October 2026  15:31:29 -0300 (0:00:00.059)       0:00:03.037 ******* 
2026-10-13T18:31:29.7325667Z 
2026-10-13T18:31:29.7326073Z TASK [nfs : debug] *************************************************************
2026-10-13T18:31:29.7326260Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:31:29.7326391Z     "msg": "/SICCV"
2026-10-13T18:31:29.7326796Z }
2026-10-13T18:31:29.7358495Z Tuesday 13 October 2026  15:31:29 -0300 (0:00:00.057)       0:00:03.095 ******* 
2026-10-13T18:31:29.7921567Z 
2026-10-13T18:31:29.7921927Z TASK [nfs : debug] *************************************************************
2026-10-13T18:31:29.7922100Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:31:29.7922247Z     "msg": "hypernprd12.ad.caixa:/fs_siccv"
2026-10-13T18:31:29.7922349Z }
2026-10-13T18:31:29.7953278Z Tuesday 13 October 2026  15:31:29 -0300 (0:00:00.059)       0:00:03.154 ******* 
2026-10-13T18:31:29.8512697Z 
2026-10-13T18:31:29.8513052Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T18:31:29.8513841Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br] => {
2026-10-13T18:31:29.8514023Z     "changed": false, 
2026-10-13T18:31:29.8514145Z     "msg": "All assertions passed"
2026-10-13T18:31:29.8514350Z }
2026-10-13T18:31:29.8547107Z Tuesday 13 October 2026  15:31:29 -0300 (0:00:00.059)       0:00:03.214 ******* 
2026-10-13T18:31:33.2766420Z 
2026-10-13T18:31:33.2767013Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T18:31:33.2767187Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:31:33.2802936Z Tuesday 13 October 2026  15:31:33 -0300 (0:00:03.425)       0:00:06.639 ******* 
2026-10-13T18:31:34.1671715Z 
2026-10-13T18:31:34.1672456Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T18:31:34.1672726Z [WARNING]: Consider using the yum, dnf or zypper module rather than running
2026-10-13T18:31:34.1673110Z 'rpm'.  If you need to use command because yum, dnf or zypper is insufficient
2026-10-13T18:31:34.1673337Z you can add 'warn: false' to this command task or set 'command_warnings=False'
2026-10-13T18:31:34.1673515Z in ansible.cfg to get rid of this message.
2026-10-13T18:31:34.1676281Z fatal: [caddeapllx2821.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.642026", "end": "2026-10-13 15:31:34.150157", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 15:31:33.508131", "stderr": "aviso: /var/tmp/rpm-tmp.O8Q0AO: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.O8Q0AO: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T18:31:34.1677188Z ...ignoring
2026-10-13T18:31:34.1710742Z Tuesday 13 October 2026  15:31:34 -0300 (0:00:00.890)       0:00:07.530 ******* 
2026-10-13T18:31:35.1130612Z 
2026-10-13T18:31:35.1131141Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T18:31:35.1135341Z fatal: [caddeapllx2821.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.696978", "end": "2026-10-13 15:31:35.096604", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 15:31:34.399626", "stderr": "aviso: /var/tmp/rpm-tmp.Pqtm2T: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.Pqtm2T: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T18:31:35.1136292Z ...ignoring
2026-10-13T18:31:35.1170892Z Tuesday 13 October 2026  15:31:35 -0300 (0:00:00.946)       0:00:08.476 ******* 
2026-10-13T18:31:35.5298848Z 
2026-10-13T18:31:35.5299589Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T18:31:35.5299855Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:31:35.5335833Z Tuesday 13 October 2026  15:31:35 -0300 (0:00:00.416)       0:00:08.892 ******* 
2026-10-13T18:31:35.7823453Z 
2026-10-13T18:31:35.7824081Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T18:31:35.7824397Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:31:35.7863443Z Tuesday 13 October 2026  15:31:35 -0300 (0:00:00.252)       0:00:09.145 ******* 
2026-10-13T18:31:36.6842185Z 
2026-10-13T18:31:36.6843002Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T18:31:36.6843257Z ok: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:31:36.6887195Z Tuesday 13 October 2026  15:31:36 -0300 (0:00:00.902)       0:00:10.048 ******* 
2026-10-13T18:31:36.9413002Z 
2026-10-13T18:31:36.9413616Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T18:31:36.9413800Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:31:36.9446678Z Tuesday 13 October 2026  15:31:36 -0300 (0:00:00.255)       0:00:10.304 ******* 
2026-10-13T18:31:47.3543527Z 
2026-10-13T18:31:47.3544179Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T18:31:47.3544660Z changed: [caddeapllx2821.agil.nprd.caixa.gov.br]
2026-10-13T18:31:47.3578296Z Tuesday 13 October 2026  15:31:47 -0300 (0:00:10.413)       0:00:20.717 ******* 
2026-10-13T18:33:59.6366129Z 
2026-10-13T18:33:59.6368184Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T18:33:59.6368448Z fatal: [caddeapllx2821.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "msg": "Error mounting /SICCV: mount.nfs: No route to host\n"}
2026-10-13T18:33:59.6368612Z ...ignoring
2026-10-13T18:33:59.6402041Z Tuesday 13 October 2026  15:33:59 -0300 (0:02:12.282)       0:02:32.999 ******* 
2026-10-13T18:33:59.7033097Z 
2026-10-13T18:33:59.7033894Z TASK [nfs : Validando Montagem] ************************************************
2026-10-13T18:33:59.7034575Z fatal: [caddeapllx2821.agil.nprd.caixa.gov.br]: FAILED! => {
2026-10-13T18:33:59.7034931Z     "assertion": "'Connection refused' in mountnfs.msg", 
2026-10-13T18:33:59.7036508Z     "changed": false, 
2026-10-13T18:33:59.7036745Z     "evaluated_to": false, 
2026-10-13T18:33:59.7036965Z     "msg": "Erro desconhecido: Error mounting /SICCV: mount.nfs: No route to host\n"
2026-10-13T18:33:59.7037161Z }
2026-10-13T18:33:59.7042501Z 
2026-10-13T18:33:59.7042841Z PLAY RECAP *********************************************************************
2026-10-13T18:33:59.7043159Z caddeapllx2821.agil.nprd.caixa.gov.br : ok=27   changed=8    unreachable=0    failed=1    skipped=0    rescued=0    ignored=3   
2026-10-13T18:33:59.7043261Z 
2026-10-13T18:33:59.7051995Z Tuesday 13 October 2026  15:33:59 -0300 (0:00:00.064)       0:02:33.063 ******* 
2026-10-13T18:33:59.7052182Z =============================================================================== 
2026-10-13T18:33:59.7052439Z nfs : Montando volume remoto ------------------------------------------ 132.28s
2026-10-13T18:33:59.7052765Z nfs : Networker | Restart networker ------------------------------------ 10.41s
2026-10-13T18:33:59.7053182Z nfs : Instalando o NFS Client ------------------------------------------- 3.43s
2026-10-13T18:33:59.7053417Z nfs : Install networker lgtonmda_url ------------------------------------ 0.95s
2026-10-13T18:33:59.7053633Z nfs : Networker | Start networker --------------------------------------- 0.90s
2026-10-13T18:33:59.7053871Z nfs : Install networker lgtoclnt_url ------------------------------------ 0.89s
2026-10-13T18:33:59.7054101Z nfs : execute montagem script ------------------------------------------- 0.65s
2026-10-13T18:33:59.7054489Z Verifica se o arquivo nfs_config.json existe ---------------------------- 0.52s
2026-10-13T18:33:59.7054735Z nfs : Coletar variáveis de ambiente ------------------------------------- 0.44s
2026-10-13T18:33:59.7054963Z nfs : Remove pacote jbcs-httpd ------------------------------------------ 0.42s
2026-10-13T18:33:59.7056959Z nfs : execute clean json ------------------------------------------------ 0.39s
2026-10-13T18:33:59.7057198Z nfs : Executar o comando abaixo para limitar as portas ------------------ 0.26s
2026-10-13T18:33:59.7057439Z nfs : Create a symbolic link -------------------------------------------- 0.25s
2026-10-13T18:33:59.7057665Z nfs : Criar variáveis --------------------------------------------------- 0.07s
2026-10-13T18:33:59.7057892Z nfs : include_tasks ----------------------------------------------------- 0.07s
2026-10-13T18:33:59.7058114Z nfs : Validando Montagem ------------------------------------------------ 0.06s
2026-10-13T18:33:59.7058324Z nfs : Criar variáveis --------------------------------------------------- 0.06s
2026-10-13T18:33:59.7061493Z nfs : ansible.builtin.debug --------------------------------------------- 0.06s
2026-10-13T18:33:59.7061764Z nfs : result_new_string_json -------------------------------------------- 0.06s
2026-10-13T18:33:59.7062039Z nfs : result_new_json --------------------------------------------------- 0.06s
2026-10-13T18:33:59.7062218Z Playbook run took 0 days, 0 hours, 2 minutes, 33 seconds
2026-10-13T18:33:59.7745175Z ##[debug]Exit code 2 received from tool '/bin/bash'
2026-10-13T18:33:59.7747357Z ##[debug]STDIO streams have closed for tool '/bin/bash'
2026-10-13T18:33:59.7754401Z ##[error]Bash exited with code '2'.
2026-10-13T18:33:59.7756310Z ##[debug]Processed: ##vso[task.issue type=error;]Bash exited with code '2'.
2026-10-13T18:33:59.7756616Z ##[debug]task result: Failed
2026-10-13T18:33:59.7757633Z ##[debug]Processed: ##vso[task.complete result=Failed;done=true;]
2026-10-13T18:33:59.7787698Z ##[debug]Failure attempting to call the restapi and retry counter is exhausted
2026-10-13T18:33:59.7788048Z ##[debug]PERF: RetryHelper Method:System.Threading.Tasks.Task <RunAsync>b__9() : took 155297.6293 ms
2026-10-13T18:33:59.7788228Z ##[debug]PERF WARNING: RetryHelper Method:System.Threading.Tasks.Task <RunAsync>b__9() : took 155297.6293 ms
2026-10-13T18:33:59.7789083Z ##[section]Finishing: Configura Control-M
