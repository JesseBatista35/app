2026-10-13T22:26:08.0596179Z ##[debug]Evaluating condition for step: 'Deploy Config no JBOSS'
2026-10-13T22:26:08.0596656Z ##[debug]Evaluating: succeeded()
2026-10-13T22:26:08.0596804Z ##[debug]Evaluating succeeded:
2026-10-13T22:26:08.0597063Z ##[debug]=> True
2026-10-13T22:26:08.0597233Z ##[debug]Result: True
2026-10-13T22:26:08.0597415Z ##[section]Starting: Deploy Config no JBOSS
2026-10-13T22:26:08.0600087Z ==============================================================================
2026-10-13T22:26:08.0600162Z Task         : Bash
2026-10-13T22:26:08.0600210Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-13T22:26:08.0600282Z Version      : 3.227.0
2026-10-13T22:26:08.0600324Z Author       : Microsoft Corporation
2026-10-13T22:26:08.0600371Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-13T22:26:08.0600447Z ==============================================================================
2026-10-13T22:26:08.7426508Z ##[debug]Using node path: /opt/ads-agent/externals/node16/bin/node
2026-10-13T22:26:08.8098205Z ##[debug]agent.TempDirectory=/opt/ads-agent/_work/_temp
2026-10-13T22:26:08.8106430Z ##[debug]loading inputs and endpoints
2026-10-13T22:26:08.8109598Z ##[debug]loading INPUT_TARGETTYPE
2026-10-13T22:26:08.8118165Z ##[debug]loading INPUT_FILEPATH
2026-10-13T22:26:08.8118726Z ##[debug]loading INPUT_SCRIPT
2026-10-13T22:26:08.8119696Z ##[debug]loading INPUT_WORKINGDIRECTORY
2026-10-13T22:26:08.8120250Z ##[debug]loading INPUT_FAILONSTDERR
2026-10-13T22:26:08.8121740Z ##[debug]loading ENDPOINT_AUTH_SYSTEMVSSCONNECTION
2026-10-13T22:26:08.8123061Z ##[debug]loading ENDPOINT_AUTH_SCHEME_SYSTEMVSSCONNECTION
2026-10-13T22:26:08.8124748Z ##[debug]loading ENDPOINT_AUTH_PARAMETER_SYSTEMVSSCONNECTION_ACCESSTOKEN
2026-10-13T22:26:08.8130208Z ##[debug]loading SECRET_TOKEN_INFRAFACIL_MUDANCA
2026-10-13T22:26:08.8131730Z ##[debug]loading SECRET_ARM_ACCESS_KEY
2026-10-13T22:26:08.8133306Z ##[debug]loading SECRET_PW_ISILON
2026-10-13T22:26:08.8134810Z ##[debug]loading SECRET_OKD_TOKEN_PRODUTOS
2026-10-13T22:26:08.8136295Z ##[debug]loading SECRET_AZPAT
2026-10-13T22:26:08.8137577Z ##[debug]loading SECRET_BT_SECRETS_PATH
2026-10-13T22:26:08.8138187Z ##[debug]loading SECRET_FORTIFY_APITOKEN
2026-10-13T22:26:08.8138752Z ##[debug]loading SECRET_GRAYLOG_PASSWORD
2026-10-13T22:26:08.8139278Z ##[debug]loading SECRET_TERRAFORM_ESX_PASSWORD
2026-10-13T22:26:08.8139746Z ##[debug]loading SECRET_FORTIFY_PASS
2026-10-13T22:26:08.8140223Z ##[debug]loading SECRET_PW_ALOCAIP
2026-10-13T22:26:08.8141210Z ##[debug]loading SECRET_ANSIBLE_VAULT
2026-10-13T22:26:08.8141836Z ##[debug]loading SECRET_TOKEN_CRQ
2026-10-13T22:26:08.8142511Z ##[debug]loading SECRET_OKD_TOKEN_KAFKA
2026-10-13T22:26:08.8143663Z ##[debug]loaded 22
2026-10-13T22:26:08.8148775Z ##[debug]Agent.ProxyUrl=undefined
2026-10-13T22:26:08.8149254Z ##[debug]Agent.CAInfo=undefined
2026-10-13T22:26:08.8149867Z ##[debug]Agent.ClientCert=undefined
2026-10-13T22:26:08.8150140Z ##[debug]Agent.SkipCertValidation=True
2026-10-13T22:26:08.8163987Z ##[debug]check path : /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-13T22:26:08.8166018Z ##[debug]adding resource file: /opt/ads-agent/_work/_tasks/Bash_6c731c3c-3c68-459a-a5c9-bde6e6595b5b/3.227.0/task.json
2026-10-13T22:26:08.8166302Z ##[debug]system.culture=en-US
2026-10-13T22:26:08.8175788Z ##[debug]failOnStderr=false
2026-10-13T22:26:08.8176418Z ##[debug]workingDirectory=/opt/ads-agent/_work/r12364/a
2026-10-13T22:26:08.8176815Z ##[debug]check path : /opt/ads-agent/_work/r12364/a
2026-10-13T22:26:08.8177310Z ##[debug]targetType=inline
2026-10-13T22:26:08.8177774Z ##[debug]bashEnvValue=undefined
2026-10-13T22:26:08.8179067Z ##[debug]script=REPO=$(echo _SIEXC-web-aplicacao | sed 's/_//')
ansible-playbook /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/site.yml --tags git_conf -e sistema_ambiente=des -e sistema_nome=siexc-web-aplicacao -e default_working_directory_tfs=/opt/ads-agent/_work/r12364/a -e build_repository_name_tfs=$REPO -e quantidade_vm=$(quantidade_vm) -e package_path=/opt/ads-agent/_work/r12364/a/binario/`basename http://binario.caixa:8081/repository/thirdparty/br/com/caixa/siexc/siexc-web-aplicacao/1.1.14/siexc-web-aplicacao-1.1.14.ear` -e use_wmq=$(USE_WMQ) -e jks_file=/opt/ads-agent/_work/_temp/caixa-truststore-acteste-nprd.jks -e site=ctc_nprd -e url_deploy="`echo "http://binario.caixa:8081/repository/thirdparty/br/com/caixa/siexc/siexc-web-aplicacao/1.1.14/siexc-web-aplicacao-1.1.14.ear" | tr -d "\'"`"
2026-10-13T22:26:08.8186760Z Generating script.
2026-10-13T22:26:08.8189182Z ##[debug]which 'bash'
2026-10-13T22:26:08.8194134Z ##[debug]found: '/bin/bash'
2026-10-13T22:26:08.8194613Z ##[debug]Agent.Version=3.225.2
2026-10-13T22:26:08.8205821Z ##[debug]agent.tempDirectory=/opt/ads-agent/_work/_temp
2026-10-13T22:26:08.8206210Z ##[debug]check path : /opt/ads-agent/_work/_temp
2026-10-13T22:26:08.8206507Z ========================== Starting Command Output ===========================
2026-10-13T22:26:08.8206851Z ##[debug]which '/bin/bash'
2026-10-13T22:26:08.8207214Z ##[debug]found: '/bin/bash'
2026-10-13T22:26:08.8207607Z ##[debug]/bin/bash arg: /opt/ads-agent/_work/_temp/e2806a45-e312-4252-84ac-2c844b1f1376.sh
2026-10-13T22:26:08.8208011Z ##[debug]exec tool: /bin/bash
2026-10-13T22:26:08.8208346Z ##[debug]arguments:
2026-10-13T22:26:08.8208727Z ##[debug]   /opt/ads-agent/_work/_temp/e2806a45-e312-4252-84ac-2c844b1f1376.sh
2026-10-13T22:26:08.8209293Z [command]/bin/bash /opt/ads-agent/_work/_temp/e2806a45-e312-4252-84ac-2c844b1f1376.sh
2026-10-13T22:26:08.8278783Z /opt/ads-agent/_work/_temp/e2806a45-e312-4252-84ac-2c844b1f1376.sh: line 2: quantidade_vm: comando não encontrado
2026-10-13T22:26:08.8289874Z /opt/ads-agent/_work/_temp/e2806a45-e312-4252-84ac-2c844b1f1376.sh: line 2: USE_WMQ: comando não encontrado
2026-10-13T22:26:10.8475084Z 
2026-10-13T22:26:10.8475592Z PLAY [local] *******************************************************************
2026-10-13T22:26:10.8745413Z 
2026-10-13T22:26:10.8745846Z PLAY [Configurando o DNS] ******************************************************
2026-10-13T22:26:11.0752797Z 
2026-10-13T22:26:11.0753271Z PLAY [local] *******************************************************************
2026-10-13T22:26:11.0790621Z 
2026-10-13T22:26:11.0791408Z PLAY [Verificando serviços] ****************************************************
2026-10-13T22:26:11.0873061Z 
2026-10-13T22:26:11.0873734Z PLAY [Configuração LDAP] *******************************************************
2026-10-13T22:26:11.0905391Z [WARNING]: Found variable using reserved name: when
2026-10-13T22:26:11.0911270Z 
2026-10-13T22:26:11.0911639Z PLAY [jboss] *******************************************************************
2026-10-13T22:26:11.0995113Z 
2026-10-13T22:26:11.0995337Z PLAY [Stack Jboss] *************************************************************
2026-10-13T22:26:11.1220119Z Tuesday 13 October 2026  19:26:11 -0300 (0:00:00.334)       0:00:00.334 ******* 
2026-10-13T22:26:11.6537247Z 
2026-10-13T22:26:11.6537927Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-10-13T22:26:11.6539002Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-13T22:26:11.6539296Z caddeapllx2193.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-13T22:26:11.6539534Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-13T22:26:11.6539769Z releases. A future Ansible release will default to using the discovered 
2026-10-13T22:26:11.6539992Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-13T22:26:11.6540416Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-13T22:26:11.6540579Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-13T22:26:11.6540730Z setting deprecation_warnings=False in ansible.cfg.
2026-10-13T22:26:11.6540864Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:11.6562157Z 
2026-10-13T22:26:11.6562720Z PLAY [jboss] *******************************************************************
2026-10-13T22:26:11.6628998Z Tuesday 13 October 2026  19:26:11 -0300 (0:00:00.541)       0:00:00.875 ******* 
2026-10-13T22:26:11.9654963Z 
2026-10-13T22:26:11.9655441Z TASK [Verifica se o arquivo nfs_config.json existe] ****************************
2026-10-13T22:26:11.9655600Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:11.9682288Z Tuesday 13 October 2026  19:26:11 -0300 (0:00:00.305)       0:00:01.180 ******* 
2026-10-13T22:26:12.0138831Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/tasks/get_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:26:12.0177503Z Tuesday 13 October 2026  19:26:12 -0300 (0:00:00.049)       0:00:01.230 ******* 
2026-10-13T22:26:12.0766096Z 
2026-10-13T22:26:12.0766766Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-13T22:26:12.0766939Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:12.0806391Z Tuesday 13 October 2026  19:26:12 -0300 (0:00:00.062)       0:00:01.292 ******* 
2026-10-13T22:26:12.4797340Z 
2026-10-13T22:26:12.4798017Z TASK [nfs : Coletar variáveis de ambiente] *************************************
2026-10-13T22:26:12.4798177Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:12.4824770Z Tuesday 13 October 2026  19:26:12 -0300 (0:00:00.401)       0:00:01.694 ******* 
2026-10-13T22:26:12.5376047Z 
2026-10-13T22:26:12.5376572Z TASK [nfs : Exibir resultado em JSON] ******************************************
2026-10-13T22:26:12.5376779Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:26:12.5376892Z     "nfs_vars_json": {
2026-10-13T22:26:12.5377012Z         "changed": false, 
2026-10-13T22:26:12.5377321Z         "cmd": "cat /opt/ads-agent/_work/r12364/a/nfs_config.json", 
2026-10-13T22:26:12.5377477Z         "delta": "0:00:00.003124", 
2026-10-13T22:26:12.5377658Z         "end": "2026-10-13 19:26:12.465751", 
2026-10-13T22:26:12.5377775Z         "failed": false, 
2026-10-13T22:26:12.5377875Z         "rc": 0, 
2026-10-13T22:26:12.5378035Z         "start": "2026-10-13 19:26:12.462627", 
2026-10-13T22:26:12.5378148Z         "stderr": "", 
2026-10-13T22:26:12.5378253Z         "stderr_lines": [], 
2026-10-13T22:26:12.5379157Z         "stdout": "[{\"NFS_ENDPOINT_VM\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM\": \"/SIEXC_SWIFT\"},{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON\": \"/siexc_incoming\"},{\"NFS_ENDPOINT_ISILON_3\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC\",\"NFS_MOUNT_POINT_ISILON_3\": \"/SIAPC\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF\",\"NFS_MOUNT_POINT_ISILON_2\": \"/integracoes/SIISF\"},{\"NFS_ENDPOINT_ISILON_5\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_5\": \"/legado\"},{\"NFS_ENDPOINT_ISILON_4\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_4\": \"/SIGPL\"},{\"NFS_ENDPOINT_ISILON_7\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_7\": \"/eFinanceira/siexc/entrada\"},{\"NFS_ENDPOINT_ISILON_6\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_6\": \"/eFinanceira_ctc/siexc\"},{\"NFS_ENDPOINT_VM_2\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_2\": \"/opt/sigdb\"},{\"NFS_ENDPOINT_ISILON_9\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_9\": \"/siexc\"},{\"NFS_ENDPOINT_VM_3\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_3\": \"/producao\"},{\"NFS_ENDPOINT_ISILON_8\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_8\": \"/suporte\"},{\"NFS_ENDPOINT_VM_4\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_4\": \"/producao/SWIFT\"},{\"NFS_ENDPOINT_VM_5\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_5\": \"/SIEXC_SWIFT\"}]", 
2026-10-13T22:26:12.5380357Z         "stdout_lines": [
2026-10-13T22:26:12.5381240Z             "[{\"NFS_ENDPOINT_VM\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM\": \"/SIEXC_SWIFT\"},{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON\": \"/siexc_incoming\"},{\"NFS_ENDPOINT_ISILON_3\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC\",\"NFS_MOUNT_POINT_ISILON_3\": \"/SIAPC\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF\",\"NFS_MOUNT_POINT_ISILON_2\": \"/integracoes/SIISF\"},{\"NFS_ENDPOINT_ISILON_5\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_5\": \"/legado\"},{\"NFS_ENDPOINT_ISILON_4\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_4\": \"/SIGPL\"},{\"NFS_ENDPOINT_ISILON_7\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_7\": \"/eFinanceira/siexc/entrada\"},{\"NFS_ENDPOINT_ISILON_6\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_6\": \"/eFinanceira_ctc/siexc\"},{\"NFS_ENDPOINT_VM_2\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_2\": \"/opt/sigdb\"},{\"NFS_ENDPOINT_ISILON_9\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_9\": \"/siexc\"},{\"NFS_ENDPOINT_VM_3\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_3\": \"/producao\"},{\"NFS_ENDPOINT_ISILON_8\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_8\": \"/suporte\"},{\"NFS_ENDPOINT_VM_4\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_4\": \"/producao/SWIFT\"},{\"NFS_ENDPOINT_VM_5\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_5\": \"/SIEXC_SWIFT\"}]"
2026-10-13T22:26:12.5382234Z         ]
2026-10-13T22:26:12.5382327Z     }
2026-10-13T22:26:12.5382414Z }
2026-10-13T22:26:12.5396834Z Tuesday 13 October 2026  19:26:12 -0300 (0:00:00.057)       0:00:01.752 ******* 
2026-10-13T22:26:12.5968222Z 
2026-10-13T22:26:12.5968905Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-13T22:26:12.5969078Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:12.6006439Z Tuesday 13 October 2026  19:26:12 -0300 (0:00:00.060)       0:00:01.812 ******* 
2026-10-13T22:26:31.3369893Z 
2026-10-13T22:26:31.3370648Z TASK [nfs : execute montagem script] *******************************************
2026-10-13T22:26:31.3370979Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:31.3398430Z Tuesday 13 October 2026  19:26:31 -0300 (0:00:18.739)       0:00:20.552 ******* 
2026-10-13T22:26:31.3995438Z 
2026-10-13T22:26:31.3996255Z TASK [nfs : ansible.builtin.debug] *********************************************
2026-10-13T22:26:31.4002475Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:26:31.4003040Z     "changed": false, 
2026-10-13T22:26:31.4003206Z     "msg": {
2026-10-13T22:26:31.4003328Z         "changed": true, 
2026-10-13T22:26:31.4003419Z         "cmd": [
2026-10-13T22:26:31.4003520Z             "python", 
2026-10-13T22:26:31.4003842Z             "/opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/files/nfs.py", 
2026-10-13T22:26:31.4003976Z             "montagem", 
2026-10-13T22:26:31.4004118Z             "siexc-web-aplicacao", 
2026-10-13T22:26:31.4004597Z             "des", 
2026-10-13T22:26:31.4004719Z             "ctc_nprd", 
2026-10-13T22:26:31.4005175Z             "/opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2", 
2026-10-13T22:26:31.4005304Z             "C&t@d02", 
2026-10-13T22:26:31.4005504Z             "***", 
2026-10-13T22:26:31.4005619Z             "s736651@corp.caixa.gov.br", 
2026-10-13T22:26:31.4005733Z             "***", 
2026-10-13T22:26:31.4006638Z             "[{\"NFS_ENDPOINT_VM\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM\": \"/SIEXC_SWIFT\"},{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON\": \"/siexc_incoming\"},{\"NFS_ENDPOINT_ISILON_3\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC\",\"NFS_MOUNT_POINT_ISILON_3\": \"/SIAPC\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF\",\"NFS_MOUNT_POINT_ISILON_2\": \"/integracoes/SIISF\"},{\"NFS_ENDPOINT_ISILON_5\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_5\": \"/legado\"},{\"NFS_ENDPOINT_ISILON_4\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_4\": \"/SIGPL\"},{\"NFS_ENDPOINT_ISILON_7\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_7\": \"/eFinanceira/siexc/entrada\"},{\"NFS_ENDPOINT_ISILON_6\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_6\": \"/eFinanceira_ctc/siexc\"},{\"NFS_ENDPOINT_VM_2\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_2\": \"/opt/sigdb\"},{\"NFS_ENDPOINT_ISILON_9\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_9\": \"/siexc\"},{\"NFS_ENDPOINT_VM_3\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_3\": \"/producao\"},{\"NFS_ENDPOINT_ISILON_8\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_8\": \"/suporte\"},{\"NFS_ENDPOINT_VM_4\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_4\": \"/producao/SWIFT\"},{\"NFS_ENDPOINT_VM_5\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_5\": \"/SIEXC_SWIFT\"}]"
2026-10-13T22:26:31.4007602Z         ], 
2026-10-13T22:26:31.4007732Z         "delta": "0:00:18.411763", 
2026-10-13T22:26:31.4007925Z         "end": "2026-10-13 19:26:31.319423", 
2026-10-13T22:26:31.4008046Z         "failed": false, 
2026-10-13T22:26:31.4008164Z         "rc": 0, 
2026-10-13T22:26:31.4008329Z         "start": "2026-10-13 19:26:12.907660", 
2026-10-13T22:26:31.4008440Z         "stderr": "", 
2026-10-13T22:26:31.4008544Z         "stderr_lines": [], 
2026-10-13T22:26:31.4016825Z         "stdout": "[{u'NFS_MOUNT_POINT_VM': u'/SIEXC_SWIFT', u'NFS_ENDPOINT_VM': u'192.168.227.59:/export/sicql_bovespa'}, {u'NFS_MOUNT_POINT_ISILON': u'/siexc_incoming', u'NFS_ENDPOINT_ISILON': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC'}, {u'NFS_MOUNT_POINT_ISILON_3': u'/SIAPC', u'NFS_ENDPOINT_ISILON_3': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC'}, {u'NFS_MOUNT_POINT_ISILON_2': u'/integracoes/SIISF', u'NFS_ENDPOINT_ISILON_2': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF'}, {u'NFS_ENDPOINT_ISILON_5': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_5': u'/legado'}, {u'NFS_ENDPOINT_ISILON_4': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_4': u'/SIGPL'}, {u'NFS_ENDPOINT_ISILON_7': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_7': u'/eFinanceira/siexc/entrada'}, {u'NFS_ENDPOINT_ISILON_6': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_6': u'/eFinanceira_ctc/siexc'}, {u'NFS_ENDPOINT_VM_2': u'192.168.227.59:/export/sicql_bovespa', u'NFS_MOUNT_POINT_VM_2': u'/opt/sigdb'}, {u'NFS_ENDPOINT_ISILON_9': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_9': u'/siexc'}, {u'NFS_ENDPOINT_VM_3': u'192.168.227.59:/export/sicql_bovespa', u'NFS_MOUNT_POINT_VM_3': u'/producao'}, {u'NFS_MOUNT_POINT_ISILON_8': u'/suporte', u'NFS_ENDPOINT_ISILON_8': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC'}, {u'NFS_MOUNT_POINT_VM_4': u'/producao/SWIFT', u'NFS_ENDPOINT_VM_4': u'192.168.227.59:/export/sicql_bovespa'}, {u'NFS_MOUNT_POINT_VM_5': u'/SIEXC_SWIFT', u'NFS_ENDPOINT_VM_5': u'192.168.227.59:/export/sicql_bovespa'}]\nNome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           \n------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /integracoes/SIISF                  ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/integracoes/SIISF\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /integracoes/SIISF                  ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF /SIGPL                              ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/SIGPL\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF /SIGPL                              ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC /legado                             ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/legado\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC /legado                             ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /SIEXC_SWIFT                        ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/SIEXC_SWIFT\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /SIEXC_SWIFT                        ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao/SWIFT                     ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/producao/SWIFT\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao/SWIFT                     ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao                           ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/producao\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao                           ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /opt/sigdb                          ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/opt/sigdb\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /opt/sigdb                          ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira_ctc/siexc              ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/eFinanceira_ctc/siexc\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira_ctc/siexc              ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira/siexc/entrada          ISILON                              nfsctcnprd.ctc.caixa                des                                \nnfs_path=/eFinanceira/siexc/entrada\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira/siexc/entrada          ISILON                              nfsctcnprd.ctc.caixa                des                                \n192.168.227.59                      /export/sicql_bovespa               /siexc_incoming                     VM                                  192.168.227.59                      des                                \nnfs_path=/siexc_incoming\nnfs_src=192.168.227.59:/export/sicql_bovespa\n192.168.227.59                      /export/sicql_bovespa               /siexc_incoming                     VM                                  192.168.227.59                      des                                \n192.168.227.59                      /export/sicql_bovespa               /SIEXC_SWIFT                        VM                                  192.168.227.59                      des                                \nnfs_path=/SIEXC_SWIFT\nnfs_src=192.168.227.59:/export/sicql_bovespa\n192.168.227.59                      /export/sicql_bovespa               /SIEXC_SWIFT                        VM                                  192.168.227.59                      des                                \n192.168.227.59                      /export/sicql_bovespa               /SIAPC                              VM                                  192.168.227.59                      des                                \nnfs_path=/SIAPC\nnfs_src=192.168.227.59:/export/sicql_bovespa\n192.168.227.59                      /export/sicql_bovespa               /SIAPC                              VM                                  192.168.227.59                      des                                \n192.168.227.59                      /export/sicql_bovespa               /siexc                              VM                                  192.168.227.59                      des                                \nnfs_path=/siexc\nnfs_src=192.168.227.59:/export/sicql_bovespa\n192.168.227.59                      /export/sicql_bovespa               /siexc                              VM                                  192.168.227.59                      des                                \n192.168.227.59                      /export/sicql_bovespa               /suporte                            VM                                  192.168.227.59                      des                                \nnfs_path=/suporte\nnfs_src=192.168.227.59:/export/sicql_bovespa\n192.168.227.59                      /export/sicql_bovespa               /suporte                            VM                                  192.168.227.59                      des                                ", 
2026-10-13T22:26:31.4019995Z         "stdout_lines": [
2026-10-13T22:26:31.4021840Z             "[{u'NFS_MOUNT_POINT_VM': u'/SIEXC_SWIFT', u'NFS_ENDPOINT_VM': u'192.168.227.59:/export/sicql_bovespa'}, {u'NFS_MOUNT_POINT_ISILON': u'/siexc_incoming', u'NFS_ENDPOINT_ISILON': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC'}, {u'NFS_MOUNT_POINT_ISILON_3': u'/SIAPC', u'NFS_ENDPOINT_ISILON_3': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC'}, {u'NFS_MOUNT_POINT_ISILON_2': u'/integracoes/SIISF', u'NFS_ENDPOINT_ISILON_2': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF'}, {u'NFS_ENDPOINT_ISILON_5': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_5': u'/legado'}, {u'NFS_ENDPOINT_ISILON_4': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_4': u'/SIGPL'}, {u'NFS_ENDPOINT_ISILON_7': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_7': u'/eFinanceira/siexc/entrada'}, {u'NFS_ENDPOINT_ISILON_6': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_6': u'/eFinanceira_ctc/siexc'}, {u'NFS_ENDPOINT_VM_2': u'192.168.227.59:/export/sicql_bovespa', u'NFS_MOUNT_POINT_VM_2': u'/opt/sigdb'}, {u'NFS_ENDPOINT_ISILON_9': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC', u'NFS_MOUNT_POINT_ISILON_9': u'/siexc'}, {u'NFS_ENDPOINT_VM_3': u'192.168.227.59:/export/sicql_bovespa', u'NFS_MOUNT_POINT_VM_3': u'/producao'}, {u'NFS_MOUNT_POINT_ISILON_8': u'/suporte', u'NFS_ENDPOINT_ISILON_8': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC'}, {u'NFS_MOUNT_POINT_VM_4': u'/producao/SWIFT', u'NFS_ENDPOINT_VM_4': u'192.168.227.59:/export/sicql_bovespa'}, {u'NFS_MOUNT_POINT_VM_5': u'/SIEXC_SWIFT', u'NFS_ENDPOINT_VM_5': u'192.168.227.59:/export/sicql_bovespa'}]", 
2026-10-13T22:26:31.4022870Z             "Nome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           ", 
2026-10-13T22:26:31.4023233Z             "------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------", 
2026-10-13T22:26:31.4023477Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /integracoes/SIISF                  ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4023641Z             "nfs_path=/integracoes/SIISF", 
2026-10-13T22:26:31.4023779Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:26:31.4023960Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /integracoes/SIISF                  ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4024163Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF /SIGPL                              ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4024371Z             "nfs_path=/SIGPL", 
2026-10-13T22:26:31.4024504Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF", 
2026-10-13T22:26:31.4024675Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF /SIGPL                              ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4024860Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC /legado                             ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4025065Z             "nfs_path=/legado", 
2026-10-13T22:26:31.4025233Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC", 
2026-10-13T22:26:31.4025410Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC /legado                             ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4025645Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /SIEXC_SWIFT                        ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4025796Z             "nfs_path=/SIEXC_SWIFT", 
2026-10-13T22:26:31.4025926Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:26:31.4026101Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /SIEXC_SWIFT                        ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4026297Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao/SWIFT                     ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4026449Z             "nfs_path=/producao/SWIFT", 
2026-10-13T22:26:31.4026587Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:26:31.4026768Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao/SWIFT                     ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4026957Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao                           ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4027105Z             "nfs_path=/producao", 
2026-10-13T22:26:31.4027270Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:26:31.4027441Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /producao                           ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4027631Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /opt/sigdb                          ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4027777Z             "nfs_path=/opt/sigdb", 
2026-10-13T22:26:31.4027902Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:26:31.4028064Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /opt/sigdb                          ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4028260Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira_ctc/siexc              ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4028417Z             "nfs_path=/eFinanceira_ctc/siexc", 
2026-10-13T22:26:31.4028614Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:26:31.4028792Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira_ctc/siexc              ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4029074Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira/siexc/entrada          ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4029239Z             "nfs_path=/eFinanceira/siexc/entrada", 
2026-10-13T22:26:31.4029380Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:26:31.4029560Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC /eFinanceira/siexc/entrada          ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-13T22:26:31.4029780Z             "192.168.227.59                      /export/sicql_bovespa               /siexc_incoming                     VM                                  192.168.227.59                      des                                ", 
2026-10-13T22:26:31.4029928Z             "nfs_path=/siexc_incoming", 
2026-10-13T22:26:31.4030105Z             "nfs_src=192.168.227.59:/export/sicql_bovespa", 
2026-10-13T22:26:31.4030264Z             "192.168.227.59                      /export/sicql_bovespa               /siexc_incoming                     VM                                  192.168.227.59                      des                                ", 
2026-10-13T22:26:31.4030436Z             "192.168.227.59                      /export/sicql_bovespa               /SIEXC_SWIFT                        VM                                  192.168.227.59                      des                                ", 
2026-10-13T22:26:31.4030579Z             "nfs_path=/SIEXC_SWIFT", 
2026-10-13T22:26:31.4030699Z             "nfs_src=192.168.227.59:/export/sicql_bovespa", 
2026-10-13T22:26:31.4030841Z             "192.168.227.59                      /export/sicql_bovespa               /SIEXC_SWIFT                        VM                                  192.168.227.59                      des                                ", 
2026-10-13T22:26:31.4031007Z             "192.168.227.59                      /export/sicql_bovespa               /SIAPC                              VM                                  192.168.227.59                      des                                ", 
2026-10-13T22:26:31.4031140Z             "nfs_path=/SIAPC", 
2026-10-13T22:26:31.4031257Z             "nfs_src=192.168.227.59:/export/sicql_bovespa", 
2026-10-13T22:26:31.4031406Z             "192.168.227.59                      /export/sicql_bovespa               /SIAPC                              VM                                  192.168.227.59                      des                                ", 
2026-10-13T22:26:31.4031565Z             "192.168.227.59                      /export/sicql_bovespa               /siexc                              VM                                  192.168.227.59                      des                                ", 
2026-10-13T22:26:31.4031695Z             "nfs_path=/siexc", 
2026-10-13T22:26:31.4031814Z             "nfs_src=192.168.227.59:/export/sicql_bovespa", 
2026-10-13T22:26:31.4032010Z             "192.168.227.59                      /export/sicql_bovespa               /siexc                              VM                                  192.168.227.59                      des                                ", 
2026-10-13T22:26:31.4032181Z             "192.168.227.59                      /export/sicql_bovespa               /suporte                            VM                                  192.168.227.59                      des                                ", 
2026-10-13T22:26:31.4032315Z             "nfs_path=/suporte", 
2026-10-13T22:26:31.4032433Z             "nfs_src=192.168.227.59:/export/sicql_bovespa", 
2026-10-13T22:26:31.4032569Z             "192.168.227.59                      /export/sicql_bovespa               /suporte                            VM                                  192.168.227.59                      des                                "
2026-10-13T22:26:31.4032721Z         ]
2026-10-13T22:26:31.4032811Z     }
2026-10-13T22:26:31.4032897Z }
2026-10-13T22:26:31.4033125Z Tuesday 13 October 2026  19:26:31 -0300 (0:00:00.063)       0:00:20.615 ******* 
2026-10-13T22:26:31.6622114Z 
2026-10-13T22:26:31.6622669Z TASK [nfs : execute clean json] ************************************************
2026-10-13T22:26:31.6622956Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:31.6647763Z Tuesday 13 October 2026  19:26:31 -0300 (0:00:00.261)       0:00:20.877 ******* 
2026-10-13T22:26:31.7233444Z 
2026-10-13T22:26:31.7234002Z TASK [nfs : result_new_string_json] ********************************************
2026-10-13T22:26:31.7237876Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:26:31.7238174Z     "msg": {
2026-10-13T22:26:31.7238273Z         "changed": true, 
2026-10-13T22:26:31.7240460Z         "cmd": "echo '[{\"NFS_ENDPOINT_VM\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM\": \"/SIEXC_SWIFT\"},{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON\": \"/siexc_incoming\"},{\"NFS_ENDPOINT_ISILON_3\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC\",\"NFS_MOUNT_POINT_ISILON_3\": \"/SIAPC\"},{\"NFS_ENDPOINT_ISILON_2\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF\",\"NFS_MOUNT_POINT_ISILON_2\": \"/integracoes/SIISF\"},{\"NFS_ENDPOINT_ISILON_5\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_5\": \"/legado\"},{\"NFS_ENDPOINT_ISILON_4\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_4\": \"/SIGPL\"},{\"NFS_ENDPOINT_ISILON_7\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_7\": \"/eFinanceira/siexc/entrada\"},{\"NFS_ENDPOINT_ISILON_6\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_6\": \"/eFinanceira_ctc/siexc\"},{\"NFS_ENDPOINT_VM_2\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_2\": \"/opt/sigdb\"},{\"NFS_ENDPOINT_ISILON_9\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_9\": \"/siexc\"},{\"NFS_ENDPOINT_VM_3\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_3\": \"/producao\"},{\"NFS_ENDPOINT_ISILON_8\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT_ISILON_8\": \"/suporte\"},{\"NFS_ENDPOINT_VM_4\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_4\": \"/producao/SWIFT\"},{\"NFS_ENDPOINT_VM_5\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT_VM_5\": \"/SIEXC_SWIFT\"}]' | sed 's/NFS_ENDPOINT_ISILON[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_ISILON[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_HUAWEI[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_HUAWEI[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_VM[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_VM[^\"]*/NFS_MOUNT_POINT/g'", 
2026-10-13T22:26:31.7241748Z         "delta": "0:00:00.003718", 
2026-10-13T22:26:31.7242078Z         "end": "2026-10-13 19:26:31.645292", 
2026-10-13T22:26:31.7242231Z         "failed": false, 
2026-10-13T22:26:31.7242372Z         "rc": 0, 
2026-10-13T22:26:31.7242532Z         "start": "2026-10-13 19:26:31.641574", 
2026-10-13T22:26:31.7242668Z         "stderr": "", 
2026-10-13T22:26:31.7242792Z         "stderr_lines": [], 
2026-10-13T22:26:31.7243601Z         "stdout": "[{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/SIEXC_SWIFT\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/siexc_incoming\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC\",\"NFS_MOUNT_POINT\": \"/SIAPC\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF\",\"NFS_MOUNT_POINT\": \"/integracoes/SIISF\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/legado\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/SIGPL\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/eFinanceira/siexc/entrada\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/eFinanceira_ctc/siexc\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/opt/sigdb\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/siexc\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/producao\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/suporte\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/producao/SWIFT\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/SIEXC_SWIFT\"}]", 
2026-10-13T22:26:31.7244750Z         "stdout_lines": [
2026-10-13T22:26:31.7245571Z             "[{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/SIEXC_SWIFT\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/siexc_incoming\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC\",\"NFS_MOUNT_POINT\": \"/SIAPC\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF\",\"NFS_MOUNT_POINT\": \"/integracoes/SIISF\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/legado\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/SIGPL\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/eFinanceira/siexc/entrada\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/eFinanceira_ctc/siexc\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/opt/sigdb\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/siexc\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/producao\"},{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC\",\"NFS_MOUNT_POINT\": \"/suporte\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/producao/SWIFT\"},{\"NFS_ENDPOINT\": \"192.168.227.59:/export/sicql_bovespa\",\"NFS_MOUNT_POINT\": \"/SIEXC_SWIFT\"}]"
2026-10-13T22:26:31.7246524Z         ]
2026-10-13T22:26:31.7246635Z     }
2026-10-13T22:26:31.7246774Z }
2026-10-13T22:26:31.7265554Z Tuesday 13 October 2026  19:26:31 -0300 (0:00:00.061)       0:00:20.938 ******* 
2026-10-13T22:26:31.7835356Z 
2026-10-13T22:26:31.7836033Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T22:26:31.7836514Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:31.7862219Z Tuesday 13 October 2026  19:26:31 -0300 (0:00:00.059)       0:00:20.998 ******* 
2026-10-13T22:26:31.8451005Z 
2026-10-13T22:26:31.8451560Z TASK [nfs : result_new_json] ***************************************************
2026-10-13T22:26:31.8455022Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:26:31.8455185Z     "msg": [
2026-10-13T22:26:31.8455326Z         {
2026-10-13T22:26:31.8455475Z             "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T22:26:31.8455647Z             "NFS_MOUNT_POINT": "/SIEXC_SWIFT"
2026-10-13T22:26:31.8455746Z         }, 
2026-10-13T22:26:31.8455967Z         {
2026-10-13T22:26:31.8456143Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:26:31.8456313Z             "NFS_MOUNT_POINT": "/siexc_incoming"
2026-10-13T22:26:31.8456749Z         }, 
2026-10-13T22:26:31.8456858Z         {
2026-10-13T22:26:31.8457020Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC", 
2026-10-13T22:26:31.8457150Z             "NFS_MOUNT_POINT": "/SIAPC"
2026-10-13T22:26:31.8457277Z         }, 
2026-10-13T22:26:31.8457399Z         {
2026-10-13T22:26:31.8457550Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF", 
2026-10-13T22:26:31.8457726Z             "NFS_MOUNT_POINT": "/integracoes/SIISF"
2026-10-13T22:26:31.8457918Z         }, 
2026-10-13T22:26:31.8458021Z         {
2026-10-13T22:26:31.8458141Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:26:31.8458303Z             "NFS_MOUNT_POINT": "/legado"
2026-10-13T22:26:31.8458422Z         }, 
2026-10-13T22:26:31.8458523Z         {
2026-10-13T22:26:31.8458676Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:26:31.8458831Z             "NFS_MOUNT_POINT": "/SIGPL"
2026-10-13T22:26:31.8458942Z         }, 
2026-10-13T22:26:31.8459020Z         {
2026-10-13T22:26:31.8459188Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:26:31.8459351Z             "NFS_MOUNT_POINT": "/eFinanceira/siexc/entrada"
2026-10-13T22:26:31.8459477Z         }, 
2026-10-13T22:26:31.8459582Z         {
2026-10-13T22:26:31.8459718Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:26:31.8459908Z             "NFS_MOUNT_POINT": "/eFinanceira_ctc/siexc"
2026-10-13T22:26:31.8460006Z         }, 
2026-10-13T22:26:31.8460109Z         {
2026-10-13T22:26:31.8460240Z             "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T22:26:31.8460394Z             "NFS_MOUNT_POINT": "/opt/sigdb"
2026-10-13T22:26:31.8460510Z         }, 
2026-10-13T22:26:31.8460609Z         {
2026-10-13T22:26:31.8460728Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:26:31.8460881Z             "NFS_MOUNT_POINT": "/siexc"
2026-10-13T22:26:31.8460994Z         }, 
2026-10-13T22:26:31.8461105Z         {
2026-10-13T22:26:31.8461231Z             "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T22:26:31.8461381Z             "NFS_MOUNT_POINT": "/producao"
2026-10-13T22:26:31.8461521Z         }, 
2026-10-13T22:26:31.8461599Z         {
2026-10-13T22:26:31.8461738Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:26:31.8461894Z             "NFS_MOUNT_POINT": "/suporte"
2026-10-13T22:26:31.8462109Z         }, 
2026-10-13T22:26:31.8462216Z         {
2026-10-13T22:26:31.8462355Z             "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T22:26:31.8462502Z             "NFS_MOUNT_POINT": "/producao/SWIFT"
2026-10-13T22:26:31.8462597Z         }, 
2026-10-13T22:26:31.8462697Z         {
2026-10-13T22:26:31.8462829Z             "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T22:26:31.8462973Z             "NFS_MOUNT_POINT": "/SIEXC_SWIFT"
2026-10-13T22:26:31.8463087Z         }
2026-10-13T22:26:31.8463189Z     ]
2026-10-13T22:26:31.8463267Z }
2026-10-13T22:26:31.8482964Z Tuesday 13 October 2026  19:26:31 -0300 (0:00:00.062)       0:00:21.060 ******* 
2026-10-13T22:26:31.9664715Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:26:31.9737015Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:26:31.9808512Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:26:31.9880799Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:26:31.9953992Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:26:32.0028014Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:26:32.0102175Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:26:32.0182421Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:26:32.0253586Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:26:32.0325635Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:26:32.0398914Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:26:32.0471741Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:26:32.0543960Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:26:32.0615030Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:26:32.0669552Z Tuesday 13 October 2026  19:26:32 -0300 (0:00:00.218)       0:00:21.279 ******* 
2026-10-13T22:26:32.1227094Z 
2026-10-13T22:26:32.1227541Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T22:26:32.1227740Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:32.1253112Z Tuesday 13 October 2026  19:26:32 -0300 (0:00:00.058)       0:00:21.337 ******* 
2026-10-13T22:26:32.1794356Z 
2026-10-13T22:26:32.1795277Z TASK [nfs : debug] *************************************************************
2026-10-13T22:26:32.1795674Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:26:32.1795823Z     "msg": {
2026-10-13T22:26:32.1795988Z         "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T22:26:32.1796142Z         "NFS_MOUNT_POINT": "/SIEXC_SWIFT"
2026-10-13T22:26:32.1796237Z     }
2026-10-13T22:26:32.1796352Z }
2026-10-13T22:26:32.1822805Z Tuesday 13 October 2026  19:26:32 -0300 (0:00:00.056)       0:00:21.394 ******* 
2026-10-13T22:26:32.2385284Z 
2026-10-13T22:26:32.2386219Z TASK [nfs : debug] *************************************************************
2026-10-13T22:26:32.2386509Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:26:32.2386765Z     "msg": "/SIEXC_SWIFT"
2026-10-13T22:26:32.2386890Z }
2026-10-13T22:26:32.2410076Z Tuesday 13 October 2026  19:26:32 -0300 (0:00:00.058)       0:00:21.453 ******* 
2026-10-13T22:26:32.2950530Z 
2026-10-13T22:26:32.2951344Z TASK [nfs : debug] *************************************************************
2026-10-13T22:26:32.2951583Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:26:32.2951746Z     "msg": "192.168.227.59:/export/sicql_bovespa"
2026-10-13T22:26:32.2951878Z }
2026-10-13T22:26:32.2996954Z Tuesday 13 October 2026  19:26:32 -0300 (0:00:00.058)       0:00:21.511 ******* 
2026-10-13T22:26:32.3572703Z 
2026-10-13T22:26:32.3573297Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T22:26:32.3573596Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:26:32.3606168Z     "changed": false, 
2026-10-13T22:26:32.3606415Z     "msg": "All assertions passed"
2026-10-13T22:26:32.3606565Z }
2026-10-13T22:26:32.3606974Z Tuesday 13 October 2026  19:26:32 -0300 (0:00:00.060)       0:00:21.572 ******* 
2026-10-13T22:26:36.0115359Z 
2026-10-13T22:26:36.0115829Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T22:26:36.0116283Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:36.0157354Z Tuesday 13 October 2026  19:26:36 -0300 (0:00:03.655)       0:00:25.228 ******* 
2026-10-13T22:26:39.3374270Z 
2026-10-13T22:26:39.3374790Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T22:26:39.3374973Z [WARNING]: Consider using the yum, dnf or zypper module rather than running
2026-10-13T22:26:39.3375306Z 'rpm'.  If you need to use command because yum, dnf or zypper is insufficient
2026-10-13T22:26:39.3375840Z you can add 'warn: false' to this command task or set 'command_warnings=False'
2026-10-13T22:26:39.3375989Z in ansible.cfg to get rid of this message.
2026-10-13T22:26:39.3376124Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:39.3403628Z Tuesday 13 October 2026  19:26:39 -0300 (0:00:03.324)       0:00:28.552 ******* 
2026-10-13T22:26:42.0289801Z 
2026-10-13T22:26:42.0290294Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T22:26:42.0290488Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:42.0326524Z Tuesday 13 October 2026  19:26:42 -0300 (0:00:02.692)       0:00:31.244 ******* 
2026-10-13T22:26:42.4513277Z 
2026-10-13T22:26:42.4513940Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T22:26:42.4514109Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:42.4543850Z Tuesday 13 October 2026  19:26:42 -0300 (0:00:00.421)       0:00:31.666 ******* 
2026-10-13T22:26:42.7102918Z 
2026-10-13T22:26:42.7103779Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T22:26:42.7104043Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:42.7133425Z Tuesday 13 October 2026  19:26:42 -0300 (0:00:00.258)       0:00:31.925 ******* 
2026-10-13T22:26:43.8732672Z 
2026-10-13T22:26:43.8733278Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T22:26:43.8733561Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:43.8771115Z Tuesday 13 October 2026  19:26:43 -0300 (0:00:01.163)       0:00:33.089 ******* 
2026-10-13T22:26:44.1421277Z 
2026-10-13T22:26:44.1421774Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T22:26:44.1421950Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:44.1447672Z Tuesday 13 October 2026  19:26:44 -0300 (0:00:00.267)       0:00:33.357 ******* 
2026-10-13T22:26:54.5666822Z 
2026-10-13T22:26:54.5667926Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T22:26:54.5668132Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:54.5701276Z Tuesday 13 October 2026  19:26:54 -0300 (0:00:10.425)       0:00:43.782 ******* 
2026-10-13T22:26:55.2981164Z 
2026-10-13T22:26:55.2981653Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T22:26:55.2981829Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:55.3010562Z Tuesday 13 October 2026  19:26:55 -0300 (0:00:00.730)       0:00:44.513 ******* 
2026-10-13T22:26:55.3465152Z Tuesday 13 October 2026  19:26:55 -0300 (0:00:00.045)       0:00:44.558 ******* 
2026-10-13T22:26:55.4002992Z 
2026-10-13T22:26:55.4003854Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T22:26:55.4004080Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:55.4028983Z Tuesday 13 October 2026  19:26:55 -0300 (0:00:00.056)       0:00:44.615 ******* 
2026-10-13T22:26:55.4589342Z 
2026-10-13T22:26:55.4589821Z TASK [nfs : debug] *************************************************************
2026-10-13T22:26:55.4590072Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:26:55.4590250Z     "msg": {
2026-10-13T22:26:55.4590457Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:26:55.4590607Z         "NFS_MOUNT_POINT": "/siexc_incoming"
2026-10-13T22:26:55.4590954Z     }
2026-10-13T22:26:55.4591049Z }
2026-10-13T22:26:55.4614357Z Tuesday 13 October 2026  19:26:55 -0300 (0:00:00.058)       0:00:44.673 ******* 
2026-10-13T22:26:55.5153828Z 
2026-10-13T22:26:55.5154617Z TASK [nfs : debug] *************************************************************
2026-10-13T22:26:55.5155102Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:26:55.5155728Z     "msg": "/siexc_incoming"
2026-10-13T22:26:55.5155876Z }
2026-10-13T22:26:55.5185196Z Tuesday 13 October 2026  19:26:55 -0300 (0:00:00.057)       0:00:44.730 ******* 
2026-10-13T22:26:55.5724253Z 
2026-10-13T22:26:55.5725011Z TASK [nfs : debug] *************************************************************
2026-10-13T22:26:55.5725377Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:26:55.5726481Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC"
2026-10-13T22:26:55.5726648Z }
2026-10-13T22:26:55.5751231Z Tuesday 13 October 2026  19:26:55 -0300 (0:00:00.056)       0:00:44.787 ******* 
2026-10-13T22:26:55.6314446Z 
2026-10-13T22:26:55.6315198Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T22:26:55.6316283Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:26:55.6316685Z     "changed": false, 
2026-10-13T22:26:55.6316862Z     "msg": "All assertions passed"
2026-10-13T22:26:55.6317011Z }
2026-10-13T22:26:55.6339579Z Tuesday 13 October 2026  19:26:55 -0300 (0:00:00.058)       0:00:44.846 ******* 
2026-10-13T22:26:58.5917474Z 
2026-10-13T22:26:58.5917991Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T22:26:58.5918155Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:26:58.5944286Z Tuesday 13 October 2026  19:26:58 -0300 (0:00:02.960)       0:00:47.806 ******* 
2026-10-13T22:26:59.8249206Z 
2026-10-13T22:26:59.8249807Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T22:26:59.8257004Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.906037", "end": "2026-10-13 19:26:59.808325", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:26:58.902288", "stderr": "aviso: /var/tmp/rpm-tmp.KSh99z: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.KSh99z: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:26:59.8257725Z ...ignoring
2026-10-13T22:26:59.8284609Z Tuesday 13 October 2026  19:26:59 -0300 (0:00:01.234)       0:00:49.040 ******* 
2026-10-13T22:27:00.8260815Z 
2026-10-13T22:27:00.8261299Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T22:27:00.8265087Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.751314", "end": "2026-10-13 19:27:00.809410", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:27:00.058096", "stderr": "aviso: /var/tmp/rpm-tmp.4FfUcf: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.4FfUcf: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:27:00.8266056Z ...ignoring
2026-10-13T22:27:00.8293132Z Tuesday 13 October 2026  19:27:00 -0300 (0:00:01.000)       0:00:50.041 ******* 
2026-10-13T22:27:01.0896584Z 
2026-10-13T22:27:01.0897565Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T22:27:01.0897810Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:01.0925951Z Tuesday 13 October 2026  19:27:01 -0300 (0:00:00.263)       0:00:50.304 ******* 
2026-10-13T22:27:01.3500825Z 
2026-10-13T22:27:01.3501302Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T22:27:01.3501476Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:01.3529006Z Tuesday 13 October 2026  19:27:01 -0300 (0:00:00.260)       0:00:50.565 ******* 
2026-10-13T22:27:02.0160439Z 
2026-10-13T22:27:02.0160918Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T22:27:02.0161104Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:02.0199665Z Tuesday 13 October 2026  19:27:02 -0300 (0:00:00.667)       0:00:51.232 ******* 
2026-10-13T22:27:02.2906558Z 
2026-10-13T22:27:02.2907956Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T22:27:02.2908205Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:02.2934353Z Tuesday 13 October 2026  19:27:02 -0300 (0:00:00.273)       0:00:51.505 ******* 
2026-10-13T22:27:12.7259342Z 
2026-10-13T22:27:12.7260115Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T22:27:12.7260283Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:12.7285077Z Tuesday 13 October 2026  19:27:12 -0300 (0:00:10.435)       0:01:01.940 ******* 
2026-10-13T22:27:13.3811112Z 
2026-10-13T22:27:13.3811581Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T22:27:13.3811750Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:13.3844121Z Tuesday 13 October 2026  19:27:13 -0300 (0:00:00.655)       0:01:02.596 ******* 
2026-10-13T22:27:13.4258169Z Tuesday 13 October 2026  19:27:13 -0300 (0:00:00.041)       0:01:02.637 ******* 
2026-10-13T22:27:13.4808088Z 
2026-10-13T22:27:13.4808567Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T22:27:13.4808741Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:13.4832186Z Tuesday 13 October 2026  19:27:13 -0300 (0:00:00.057)       0:01:02.695 ******* 
2026-10-13T22:27:13.5381136Z 
2026-10-13T22:27:13.5381632Z TASK [nfs : debug] *************************************************************
2026-10-13T22:27:13.5381806Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:27:13.5381915Z     "msg": {
2026-10-13T22:27:13.5382167Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC", 
2026-10-13T22:27:13.5382309Z         "NFS_MOUNT_POINT": "/SIAPC"
2026-10-13T22:27:13.5382428Z     }
2026-10-13T22:27:13.5382515Z }
2026-10-13T22:27:13.5409288Z Tuesday 13 October 2026  19:27:13 -0300 (0:00:00.057)       0:01:02.753 ******* 
2026-10-13T22:27:13.5960689Z 
2026-10-13T22:27:13.5961119Z TASK [nfs : debug] *************************************************************
2026-10-13T22:27:13.5961335Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:27:13.5961506Z     "msg": "/SIAPC"
2026-10-13T22:27:13.5961602Z }
2026-10-13T22:27:13.5987693Z Tuesday 13 October 2026  19:27:13 -0300 (0:00:00.058)       0:01:02.811 ******* 
2026-10-13T22:27:13.6529251Z 
2026-10-13T22:27:13.6529853Z TASK [nfs : debug] *************************************************************
2026-10-13T22:27:13.6530332Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:27:13.6530814Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC"
2026-10-13T22:27:13.6530983Z }
2026-10-13T22:27:13.6556408Z Tuesday 13 October 2026  19:27:13 -0300 (0:00:00.056)       0:01:02.867 ******* 
2026-10-13T22:27:13.7118023Z 
2026-10-13T22:27:13.7118456Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T22:27:13.7118631Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:27:13.7118754Z     "changed": false, 
2026-10-13T22:27:13.7118865Z     "msg": "All assertions passed"
2026-10-13T22:27:13.7118963Z }
2026-10-13T22:27:13.7151726Z Tuesday 13 October 2026  19:27:13 -0300 (0:00:00.059)       0:01:02.927 ******* 
2026-10-13T22:27:16.6622283Z 
2026-10-13T22:27:16.6622930Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T22:27:16.6623325Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:16.6648894Z Tuesday 13 October 2026  19:27:16 -0300 (0:00:02.949)       0:01:05.877 ******* 
2026-10-13T22:27:18.0368036Z 
2026-10-13T22:27:18.0368974Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T22:27:18.0373908Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:01.114196", "end": "2026-10-13 19:27:18.019713", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:27:16.905517", "stderr": "aviso: /var/tmp/rpm-tmp.W1h4s2: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.W1h4s2: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:27:18.0374807Z ...ignoring
2026-10-13T22:27:18.0401511Z Tuesday 13 October 2026  19:27:18 -0300 (0:00:01.375)       0:01:07.252 ******* 
2026-10-13T22:27:19.0589206Z 
2026-10-13T22:27:19.0589696Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T22:27:19.0593722Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.758348", "end": "2026-10-13 19:27:19.041948", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:27:18.283600", "stderr": "aviso: /var/tmp/rpm-tmp.zb00UP: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.zb00UP: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:27:19.0594640Z ...ignoring
2026-10-13T22:27:19.0622212Z Tuesday 13 October 2026  19:27:19 -0300 (0:00:01.022)       0:01:08.274 ******* 
2026-10-13T22:27:19.3219833Z 
2026-10-13T22:27:19.3220493Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T22:27:19.3220663Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:19.3248696Z Tuesday 13 October 2026  19:27:19 -0300 (0:00:00.262)       0:01:08.537 ******* 
2026-10-13T22:27:19.5840835Z 
2026-10-13T22:27:19.5841339Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T22:27:19.5841500Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:19.5867999Z Tuesday 13 October 2026  19:27:19 -0300 (0:00:00.261)       0:01:08.799 ******* 
2026-10-13T22:27:20.2347647Z 
2026-10-13T22:27:20.2348474Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T22:27:20.2348734Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:20.2387206Z Tuesday 13 October 2026  19:27:20 -0300 (0:00:00.651)       0:01:09.451 ******* 
2026-10-13T22:27:20.4953458Z 
2026-10-13T22:27:20.4953990Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T22:27:20.4954170Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:20.4981429Z Tuesday 13 October 2026  19:27:20 -0300 (0:00:00.259)       0:01:09.710 ******* 
2026-10-13T22:27:30.9365123Z 
2026-10-13T22:27:30.9365612Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T22:27:30.9365782Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:30.9391369Z Tuesday 13 October 2026  19:27:30 -0300 (0:00:10.441)       0:01:20.151 ******* 
2026-10-13T22:27:31.3601324Z 
2026-10-13T22:27:31.3601775Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T22:27:31.3601947Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:31.3632167Z Tuesday 13 October 2026  19:27:31 -0300 (0:00:00.424)       0:01:20.575 ******* 
2026-10-13T22:27:31.4062718Z Tuesday 13 October 2026  19:27:31 -0300 (0:00:00.042)       0:01:20.618 ******* 
2026-10-13T22:27:31.4625512Z 
2026-10-13T22:27:31.4626001Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T22:27:31.4626160Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:31.4652412Z Tuesday 13 October 2026  19:27:31 -0300 (0:00:00.059)       0:01:20.677 ******* 
2026-10-13T22:27:31.5204975Z 
2026-10-13T22:27:31.5205443Z TASK [nfs : debug] *************************************************************
2026-10-13T22:27:31.5205950Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:27:31.5206131Z     "msg": {
2026-10-13T22:27:31.5206270Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF", 
2026-10-13T22:27:31.5206427Z         "NFS_MOUNT_POINT": "/integracoes/SIISF"
2026-10-13T22:27:31.5206550Z     }
2026-10-13T22:27:31.5206638Z }
2026-10-13T22:27:31.5240456Z Tuesday 13 October 2026  19:27:31 -0300 (0:00:00.058)       0:01:20.736 ******* 
2026-10-13T22:27:31.5782841Z 
2026-10-13T22:27:31.5783338Z TASK [nfs : debug] *************************************************************
2026-10-13T22:27:31.5783506Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:27:31.5783628Z     "msg": "/integracoes/SIISF"
2026-10-13T22:27:31.5783730Z }
2026-10-13T22:27:31.5817976Z Tuesday 13 October 2026  19:27:31 -0300 (0:00:00.057)       0:01:20.794 ******* 
2026-10-13T22:27:31.6372183Z 
2026-10-13T22:27:31.6372682Z TASK [nfs : debug] *************************************************************
2026-10-13T22:27:31.6373386Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:27:31.6373704Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF"
2026-10-13T22:27:31.6373902Z }
2026-10-13T22:27:31.6407255Z Tuesday 13 October 2026  19:27:31 -0300 (0:00:00.058)       0:01:20.852 ******* 
2026-10-13T22:27:31.6990802Z 
2026-10-13T22:27:31.6991300Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T22:27:31.6991473Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:27:31.6991598Z     "changed": false, 
2026-10-13T22:27:31.6991712Z     "msg": "All assertions passed"
2026-10-13T22:27:31.6991801Z }
2026-10-13T22:27:31.7016312Z Tuesday 13 October 2026  19:27:31 -0300 (0:00:00.060)       0:01:20.913 ******* 
2026-10-13T22:27:34.6462617Z 
2026-10-13T22:27:34.6463100Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T22:27:34.6463259Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:34.6488136Z Tuesday 13 October 2026  19:27:34 -0300 (0:00:02.947)       0:01:23.861 ******* 
2026-10-13T22:27:35.7336507Z 
2026-10-13T22:27:35.7336995Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T22:27:35.7344192Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.843393", "end": "2026-10-13 19:27:35.717440", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:27:34.874047", "stderr": "aviso: /var/tmp/rpm-tmp.jstB3A: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.jstB3A: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:27:35.7344919Z ...ignoring
2026-10-13T22:27:35.7373165Z Tuesday 13 October 2026  19:27:35 -0300 (0:00:01.088)       0:01:24.949 ******* 
2026-10-13T22:27:36.5948267Z 
2026-10-13T22:27:36.5948741Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T22:27:36.5953251Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.610397", "end": "2026-10-13 19:27:36.577566", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:27:35.967169", "stderr": "aviso: /var/tmp/rpm-tmp.nVIB8r: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.nVIB8r: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:27:36.5953862Z ...ignoring
2026-10-13T22:27:36.5980096Z Tuesday 13 October 2026  19:27:36 -0300 (0:00:00.860)       0:01:25.810 ******* 
2026-10-13T22:27:36.8654841Z 
2026-10-13T22:27:36.8655929Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T22:27:36.8656135Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:36.8682992Z Tuesday 13 October 2026  19:27:36 -0300 (0:00:00.270)       0:01:26.080 ******* 
2026-10-13T22:27:37.1312788Z 
2026-10-13T22:27:37.1313260Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T22:27:37.1313427Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:37.1336297Z Tuesday 13 October 2026  19:27:37 -0300 (0:00:00.265)       0:01:26.346 ******* 
2026-10-13T22:27:37.7757971Z 
2026-10-13T22:27:37.7758651Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T22:27:37.7759129Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:37.7800486Z Tuesday 13 October 2026  19:27:37 -0300 (0:00:00.646)       0:01:26.992 ******* 
2026-10-13T22:27:38.0439880Z 
2026-10-13T22:27:38.0440329Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T22:27:38.0440566Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:38.0469138Z Tuesday 13 October 2026  19:27:38 -0300 (0:00:00.266)       0:01:27.259 ******* 
2026-10-13T22:27:48.5036839Z 
2026-10-13T22:27:48.5037277Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T22:27:48.5037475Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:48.5061421Z Tuesday 13 October 2026  19:27:48 -0300 (0:00:10.459)       0:01:37.718 ******* 
2026-10-13T22:27:48.9160870Z 
2026-10-13T22:27:48.9161351Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T22:27:48.9161932Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:48.9187572Z Tuesday 13 October 2026  19:27:48 -0300 (0:00:00.412)       0:01:38.130 ******* 
2026-10-13T22:27:48.9609676Z Tuesday 13 October 2026  19:27:48 -0300 (0:00:00.042)       0:01:38.173 ******* 
2026-10-13T22:27:49.0149039Z 
2026-10-13T22:27:49.0149992Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T22:27:49.0150245Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:49.0175829Z Tuesday 13 October 2026  19:27:49 -0300 (0:00:00.056)       0:01:38.229 ******* 
2026-10-13T22:27:49.0734307Z 
2026-10-13T22:27:49.0735232Z TASK [nfs : debug] *************************************************************
2026-10-13T22:27:49.0735444Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:27:49.0735554Z     "msg": {
2026-10-13T22:27:49.0735694Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:27:49.0735927Z         "NFS_MOUNT_POINT": "/legado"
2026-10-13T22:27:49.0736049Z     }
2026-10-13T22:27:49.0736139Z }
2026-10-13T22:27:49.0758823Z Tuesday 13 October 2026  19:27:49 -0300 (0:00:00.058)       0:01:38.288 ******* 
2026-10-13T22:27:49.1317172Z 
2026-10-13T22:27:49.1318033Z TASK [nfs : debug] *************************************************************
2026-10-13T22:27:49.1318275Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:27:49.1318411Z     "msg": "/legado"
2026-10-13T22:27:49.1318508Z }
2026-10-13T22:27:49.1342630Z Tuesday 13 October 2026  19:27:49 -0300 (0:00:00.058)       0:01:38.346 ******* 
2026-10-13T22:27:49.1890915Z 
2026-10-13T22:27:49.1891422Z TASK [nfs : debug] *************************************************************
2026-10-13T22:27:49.1891596Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:27:49.1891747Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC"
2026-10-13T22:27:49.1891866Z }
2026-10-13T22:27:49.1915442Z Tuesday 13 October 2026  19:27:49 -0300 (0:00:00.057)       0:01:38.403 ******* 
2026-10-13T22:27:49.2508282Z 
2026-10-13T22:27:49.2508778Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T22:27:49.2508954Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:27:49.2509076Z     "changed": false, 
2026-10-13T22:27:49.2509182Z     "msg": "All assertions passed"
2026-10-13T22:27:49.2509281Z }
2026-10-13T22:27:49.2532558Z Tuesday 13 October 2026  19:27:49 -0300 (0:00:00.061)       0:01:38.465 ******* 
2026-10-13T22:27:52.1980209Z 
2026-10-13T22:27:52.1980870Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T22:27:52.1981111Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:52.2008162Z Tuesday 13 October 2026  19:27:52 -0300 (0:00:02.947)       0:01:41.413 ******* 
2026-10-13T22:27:53.2625328Z 
2026-10-13T22:27:53.2625920Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T22:27:53.2629759Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.810467", "end": "2026-10-13 19:27:53.246563", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:27:52.436096", "stderr": "aviso: /var/tmp/rpm-tmp.PFMsoJ: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.PFMsoJ: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:27:53.2630620Z ...ignoring
2026-10-13T22:27:53.2654733Z Tuesday 13 October 2026  19:27:53 -0300 (0:00:01.064)       0:01:42.477 ******* 
2026-10-13T22:27:54.0962373Z 
2026-10-13T22:27:54.0962876Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T22:27:54.0966516Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.571502", "end": "2026-10-13 19:27:54.079703", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:27:53.508201", "stderr": "aviso: /var/tmp/rpm-tmp.QM65Du: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.QM65Du: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:27:54.0967140Z ...ignoring
2026-10-13T22:27:54.0993788Z Tuesday 13 October 2026  19:27:54 -0300 (0:00:00.833)       0:01:43.311 ******* 
2026-10-13T22:27:54.3835158Z 
2026-10-13T22:27:54.3836018Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T22:27:54.3836316Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:54.3862231Z Tuesday 13 October 2026  19:27:54 -0300 (0:00:00.286)       0:01:43.598 ******* 
2026-10-13T22:27:54.6426468Z 
2026-10-13T22:27:54.6426945Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T22:27:54.6427116Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:54.6452133Z Tuesday 13 October 2026  19:27:54 -0300 (0:00:00.259)       0:01:43.857 ******* 
2026-10-13T22:27:55.3274617Z 
2026-10-13T22:27:55.3275233Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T22:27:55.3275671Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:55.3312669Z Tuesday 13 October 2026  19:27:55 -0300 (0:00:00.685)       0:01:44.543 ******* 
2026-10-13T22:27:55.6020549Z 
2026-10-13T22:27:55.6020974Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T22:27:55.6021141Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:27:55.6045718Z Tuesday 13 October 2026  19:27:55 -0300 (0:00:00.273)       0:01:44.816 ******* 
2026-10-13T22:28:06.0294567Z 
2026-10-13T22:28:06.0295126Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T22:28:06.0295406Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:06.0320420Z Tuesday 13 October 2026  19:28:06 -0300 (0:00:10.427)       0:01:55.244 ******* 
2026-10-13T22:28:06.3599562Z 
2026-10-13T22:28:06.3600044Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T22:28:06.3600221Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:06.3636117Z Tuesday 13 October 2026  19:28:06 -0300 (0:00:00.331)       0:01:55.575 ******* 
2026-10-13T22:28:06.4076902Z Tuesday 13 October 2026  19:28:06 -0300 (0:00:00.043)       0:01:55.619 ******* 
2026-10-13T22:28:06.4626621Z 
2026-10-13T22:28:06.4627097Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T22:28:06.4627256Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:06.4651404Z Tuesday 13 October 2026  19:28:06 -0300 (0:00:00.057)       0:01:55.677 ******* 
2026-10-13T22:28:06.5210731Z 
2026-10-13T22:28:06.5211351Z TASK [nfs : debug] *************************************************************
2026-10-13T22:28:06.5211612Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:06.5211822Z     "msg": {
2026-10-13T22:28:06.5212127Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:28:06.5212364Z         "NFS_MOUNT_POINT": "/SIGPL"
2026-10-13T22:28:06.5212523Z     }
2026-10-13T22:28:06.5212663Z }
2026-10-13T22:28:06.5236228Z Tuesday 13 October 2026  19:28:06 -0300 (0:00:00.058)       0:01:55.735 ******* 
2026-10-13T22:28:06.5802268Z 
2026-10-13T22:28:06.5802703Z TASK [nfs : debug] *************************************************************
2026-10-13T22:28:06.5802909Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:06.5803042Z     "msg": "/SIGPL"
2026-10-13T22:28:06.5803139Z }
2026-10-13T22:28:06.5825008Z Tuesday 13 October 2026  19:28:06 -0300 (0:00:00.058)       0:01:55.794 ******* 
2026-10-13T22:28:06.6375334Z 
2026-10-13T22:28:06.6375888Z TASK [nfs : debug] *************************************************************
2026-10-13T22:28:06.6376069Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:06.6376225Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC"
2026-10-13T22:28:06.6376405Z }
2026-10-13T22:28:06.6412979Z Tuesday 13 October 2026  19:28:06 -0300 (0:00:00.058)       0:01:55.853 ******* 
2026-10-13T22:28:06.6983341Z 
2026-10-13T22:28:06.6983807Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T22:28:06.6983982Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:06.6984110Z     "changed": false, 
2026-10-13T22:28:06.6984210Z     "msg": "All assertions passed"
2026-10-13T22:28:06.6984321Z }
2026-10-13T22:28:06.7009152Z Tuesday 13 October 2026  19:28:06 -0300 (0:00:00.059)       0:01:55.913 ******* 
2026-10-13T22:28:09.6307749Z 
2026-10-13T22:28:09.6308290Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T22:28:09.6308526Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:09.6333856Z Tuesday 13 October 2026  19:28:09 -0300 (0:00:02.932)       0:01:58.845 ******* 
2026-10-13T22:28:10.7331444Z 
2026-10-13T22:28:10.7332345Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T22:28:10.7335968Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.844615", "end": "2026-10-13 19:28:10.716055", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:28:09.871440", "stderr": "aviso: /var/tmp/rpm-tmp.q9Ilcy: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.q9Ilcy: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:28:10.7337104Z ...ignoring
2026-10-13T22:28:10.7360922Z Tuesday 13 October 2026  19:28:10 -0300 (0:00:01.102)       0:01:59.948 ******* 
2026-10-13T22:28:11.7973115Z 
2026-10-13T22:28:11.7973650Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T22:28:11.7977787Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.803004", "end": "2026-10-13 19:28:11.780657", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:28:10.977653", "stderr": "aviso: /var/tmp/rpm-tmp.QzCTLF: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.QzCTLF: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:28:11.7978379Z ...ignoring
2026-10-13T22:28:11.8005909Z Tuesday 13 October 2026  19:28:11 -0300 (0:00:01.064)       0:02:01.012 ******* 
2026-10-13T22:28:12.0568642Z 
2026-10-13T22:28:12.0596090Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T22:28:12.0596311Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:12.0596592Z Tuesday 13 October 2026  19:28:12 -0300 (0:00:00.258)       0:02:01.271 ******* 
2026-10-13T22:28:12.3285776Z 
2026-10-13T22:28:12.3286251Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T22:28:12.3286414Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:12.3314214Z Tuesday 13 October 2026  19:28:12 -0300 (0:00:00.271)       0:02:01.543 ******* 
2026-10-13T22:28:12.9714273Z 
2026-10-13T22:28:12.9715071Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T22:28:12.9715457Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:12.9755181Z Tuesday 13 October 2026  19:28:12 -0300 (0:00:00.644)       0:02:02.187 ******* 
2026-10-13T22:28:13.2425751Z 
2026-10-13T22:28:13.2426583Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T22:28:13.2427113Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:13.2453741Z Tuesday 13 October 2026  19:28:13 -0300 (0:00:00.269)       0:02:02.457 ******* 
2026-10-13T22:28:23.6941897Z 
2026-10-13T22:28:23.6942852Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T22:28:23.6943211Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:23.6967066Z Tuesday 13 October 2026  19:28:23 -0300 (0:00:10.451)       0:02:12.909 ******* 
2026-10-13T22:28:24.0188213Z 
2026-10-13T22:28:24.0189055Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T22:28:24.0189511Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:24.0216859Z Tuesday 13 October 2026  19:28:24 -0300 (0:00:00.324)       0:02:13.234 ******* 
2026-10-13T22:28:24.0638143Z Tuesday 13 October 2026  19:28:24 -0300 (0:00:00.041)       0:02:13.276 ******* 
2026-10-13T22:28:24.1189254Z 
2026-10-13T22:28:24.1190242Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T22:28:24.1190450Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:24.1215587Z Tuesday 13 October 2026  19:28:24 -0300 (0:00:00.057)       0:02:13.333 ******* 
2026-10-13T22:28:24.1772156Z 
2026-10-13T22:28:24.1772852Z TASK [nfs : debug] *************************************************************
2026-10-13T22:28:24.1774409Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:24.1774909Z     "msg": {
2026-10-13T22:28:24.1775300Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:28:24.1775629Z         "NFS_MOUNT_POINT": "/eFinanceira/siexc/entrada"
2026-10-13T22:28:24.1775871Z     }
2026-10-13T22:28:24.1775988Z }
2026-10-13T22:28:24.1802308Z Tuesday 13 October 2026  19:28:24 -0300 (0:00:00.058)       0:02:13.392 ******* 
2026-10-13T22:28:24.2356374Z 
2026-10-13T22:28:24.2356857Z TASK [nfs : debug] *************************************************************
2026-10-13T22:28:24.2357020Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:24.2357165Z     "msg": "/eFinanceira/siexc/entrada"
2026-10-13T22:28:24.2357283Z }
2026-10-13T22:28:24.2380942Z Tuesday 13 October 2026  19:28:24 -0300 (0:00:00.057)       0:02:13.450 ******* 
2026-10-13T22:28:24.2936236Z 
2026-10-13T22:28:24.2937142Z TASK [nfs : debug] *************************************************************
2026-10-13T22:28:24.2938856Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:24.2939001Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC"
2026-10-13T22:28:24.2939131Z }
2026-10-13T22:28:24.2963042Z Tuesday 13 October 2026  19:28:24 -0300 (0:00:00.058)       0:02:13.508 ******* 
2026-10-13T22:28:24.3536468Z 
2026-10-13T22:28:24.3537479Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T22:28:24.3537680Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:24.3537815Z     "changed": false, 
2026-10-13T22:28:24.3537933Z     "msg": "All assertions passed"
2026-10-13T22:28:24.3538035Z }
2026-10-13T22:28:24.3560535Z Tuesday 13 October 2026  19:28:24 -0300 (0:00:00.059)       0:02:13.568 ******* 
2026-10-13T22:28:27.3296288Z 
2026-10-13T22:28:27.3297143Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T22:28:27.3297348Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:27.3330022Z Tuesday 13 October 2026  19:28:27 -0300 (0:00:02.976)       0:02:16.545 ******* 
2026-10-13T22:28:28.8454855Z 
2026-10-13T22:28:28.8455353Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T22:28:28.8459652Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:01.269717", "end": "2026-10-13 19:28:28.828460", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:28:27.558743", "stderr": "aviso: /var/tmp/rpm-tmp.DD0hkJ: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.DD0hkJ: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:28:28.8460554Z ...ignoring
2026-10-13T22:28:28.8491016Z Tuesday 13 October 2026  19:28:28 -0300 (0:00:01.515)       0:02:18.061 ******* 
2026-10-13T22:28:29.8486503Z 
2026-10-13T22:28:29.8487117Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T22:28:29.8492164Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.736124", "end": "2026-10-13 19:28:29.831338", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:28:29.095214", "stderr": "aviso: /var/tmp/rpm-tmp.27gGFh: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.27gGFh: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:28:29.8493129Z ...ignoring
2026-10-13T22:28:29.8522289Z Tuesday 13 October 2026  19:28:29 -0300 (0:00:01.003)       0:02:19.064 ******* 
2026-10-13T22:28:30.1124856Z 
2026-10-13T22:28:30.1125935Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T22:28:30.1126145Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:30.1151856Z Tuesday 13 October 2026  19:28:30 -0300 (0:00:00.263)       0:02:19.327 ******* 
2026-10-13T22:28:30.3719506Z 
2026-10-13T22:28:30.3719980Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T22:28:30.3720148Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:30.3746528Z Tuesday 13 October 2026  19:28:30 -0300 (0:00:00.259)       0:02:19.586 ******* 
2026-10-13T22:28:31.0160090Z 
2026-10-13T22:28:31.0160921Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T22:28:31.0161184Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:31.0198521Z Tuesday 13 October 2026  19:28:31 -0300 (0:00:00.645)       0:02:20.232 ******* 
2026-10-13T22:28:31.2900760Z 
2026-10-13T22:28:31.2901207Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T22:28:31.2901405Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:31.2928074Z Tuesday 13 October 2026  19:28:31 -0300 (0:00:00.272)       0:02:20.505 ******* 
2026-10-13T22:28:41.7193670Z 
2026-10-13T22:28:41.7194788Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T22:28:41.7194995Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:41.7222538Z Tuesday 13 October 2026  19:28:41 -0300 (0:00:10.429)       0:02:30.934 ******* 
2026-10-13T22:28:42.0314797Z 
2026-10-13T22:28:42.0315582Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T22:28:42.0316111Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:42.0340108Z Tuesday 13 October 2026  19:28:42 -0300 (0:00:00.311)       0:02:31.246 ******* 
2026-10-13T22:28:42.0761893Z Tuesday 13 October 2026  19:28:42 -0300 (0:00:00.041)       0:02:31.288 ******* 
2026-10-13T22:28:42.1318301Z 
2026-10-13T22:28:42.1318733Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T22:28:42.1318927Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:42.1342167Z Tuesday 13 October 2026  19:28:42 -0300 (0:00:00.058)       0:02:31.346 ******* 
2026-10-13T22:28:42.1876753Z 
2026-10-13T22:28:42.1877577Z TASK [nfs : debug] *************************************************************
2026-10-13T22:28:42.1877895Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:42.1878036Z     "msg": {
2026-10-13T22:28:42.1878182Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:28:42.1878355Z         "NFS_MOUNT_POINT": "/eFinanceira_ctc/siexc"
2026-10-13T22:28:42.1878466Z     }
2026-10-13T22:28:42.1878542Z }
2026-10-13T22:28:42.1905043Z Tuesday 13 October 2026  19:28:42 -0300 (0:00:00.056)       0:02:31.402 ******* 
2026-10-13T22:28:42.2449413Z 
2026-10-13T22:28:42.2449825Z TASK [nfs : debug] *************************************************************
2026-10-13T22:28:42.2450454Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:42.2450635Z     "msg": "/eFinanceira_ctc/siexc"
2026-10-13T22:28:42.2450743Z }
2026-10-13T22:28:42.2475316Z Tuesday 13 October 2026  19:28:42 -0300 (0:00:00.056)       0:02:31.459 ******* 
2026-10-13T22:28:42.3023728Z 
2026-10-13T22:28:42.3024205Z TASK [nfs : debug] *************************************************************
2026-10-13T22:28:42.3024364Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:42.3024520Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC"
2026-10-13T22:28:42.3024641Z }
2026-10-13T22:28:42.3048020Z Tuesday 13 October 2026  19:28:42 -0300 (0:00:00.057)       0:02:31.517 ******* 
2026-10-13T22:28:42.3615520Z 
2026-10-13T22:28:42.3616310Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T22:28:42.3616542Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:42.3616669Z     "changed": false, 
2026-10-13T22:28:42.3616782Z     "msg": "All assertions passed"
2026-10-13T22:28:42.3616881Z }
2026-10-13T22:28:42.3639731Z Tuesday 13 October 2026  19:28:42 -0300 (0:00:00.059)       0:02:31.576 ******* 
2026-10-13T22:28:45.3184395Z 
2026-10-13T22:28:45.3184892Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T22:28:45.3185051Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:45.3209879Z Tuesday 13 October 2026  19:28:45 -0300 (0:00:02.956)       0:02:34.533 ******* 
2026-10-13T22:28:46.3540164Z 
2026-10-13T22:28:46.3540654Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T22:28:46.3544748Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.789308", "end": "2026-10-13 19:28:46.336353", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:28:45.547045", "stderr": "aviso: /var/tmp/rpm-tmp.rctxbk: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.rctxbk: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:28:46.3545585Z ...ignoring
2026-10-13T22:28:46.3571224Z Tuesday 13 October 2026  19:28:46 -0300 (0:00:01.036)       0:02:35.569 ******* 
2026-10-13T22:28:47.3020097Z 
2026-10-13T22:28:47.3020602Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T22:28:47.3024789Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.685517", "end": "2026-10-13 19:28:47.284765", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:28:46.599248", "stderr": "aviso: /var/tmp/rpm-tmp.xgAHpm: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.xgAHpm: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:28:47.3025674Z ...ignoring
2026-10-13T22:28:47.3052345Z Tuesday 13 October 2026  19:28:47 -0300 (0:00:00.948)       0:02:36.517 ******* 
2026-10-13T22:28:47.5554997Z 
2026-10-13T22:28:47.5555980Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T22:28:47.5556178Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:47.5583498Z Tuesday 13 October 2026  19:28:47 -0300 (0:00:00.253)       0:02:36.770 ******* 
2026-10-13T22:28:47.8215686Z 
2026-10-13T22:28:47.8216184Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T22:28:47.8216350Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:47.8242187Z Tuesday 13 October 2026  19:28:47 -0300 (0:00:00.265)       0:02:37.036 ******* 
2026-10-13T22:28:48.4667832Z 
2026-10-13T22:28:48.4668491Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T22:28:48.4668675Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:48.4707476Z Tuesday 13 October 2026  19:28:48 -0300 (0:00:00.646)       0:02:37.683 ******* 
2026-10-13T22:28:48.7311681Z 
2026-10-13T22:28:48.7312587Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T22:28:48.7312882Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:48.7339139Z Tuesday 13 October 2026  19:28:48 -0300 (0:00:00.263)       0:02:37.946 ******* 
2026-10-13T22:28:59.1547346Z 
2026-10-13T22:28:59.1547823Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T22:28:59.1547994Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:59.1573562Z Tuesday 13 October 2026  19:28:59 -0300 (0:00:10.423)       0:02:48.369 ******* 
2026-10-13T22:28:59.5028515Z 
2026-10-13T22:28:59.5029170Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T22:28:59.5029468Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:59.5056317Z Tuesday 13 October 2026  19:28:59 -0300 (0:00:00.348)       0:02:48.717 ******* 
2026-10-13T22:28:59.5478036Z Tuesday 13 October 2026  19:28:59 -0300 (0:00:00.041)       0:02:48.759 ******* 
2026-10-13T22:28:59.6023209Z 
2026-10-13T22:28:59.6023689Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T22:28:59.6023856Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:28:59.6046731Z Tuesday 13 October 2026  19:28:59 -0300 (0:00:00.057)       0:02:48.817 ******* 
2026-10-13T22:28:59.6578581Z 
2026-10-13T22:28:59.6579029Z TASK [nfs : debug] *************************************************************
2026-10-13T22:28:59.6579200Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:59.6579318Z     "msg": {
2026-10-13T22:28:59.6579440Z         "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T22:28:59.6579827Z         "NFS_MOUNT_POINT": "/opt/sigdb"
2026-10-13T22:28:59.6579920Z     }
2026-10-13T22:28:59.6580015Z }
2026-10-13T22:28:59.6607581Z Tuesday 13 October 2026  19:28:59 -0300 (0:00:00.055)       0:02:48.873 ******* 
2026-10-13T22:28:59.7152481Z 
2026-10-13T22:28:59.7152976Z TASK [nfs : debug] *************************************************************
2026-10-13T22:28:59.7153180Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:59.7153306Z     "msg": "/opt/sigdb"
2026-10-13T22:28:59.7153490Z }
2026-10-13T22:28:59.7180096Z Tuesday 13 October 2026  19:28:59 -0300 (0:00:00.057)       0:02:48.930 ******* 
2026-10-13T22:28:59.7715670Z 
2026-10-13T22:28:59.7716163Z TASK [nfs : debug] *************************************************************
2026-10-13T22:28:59.7716339Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:59.7716477Z     "msg": "192.168.227.59:/export/sicql_bovespa"
2026-10-13T22:28:59.7716584Z }
2026-10-13T22:28:59.7740163Z Tuesday 13 October 2026  19:28:59 -0300 (0:00:00.056)       0:02:48.986 ******* 
2026-10-13T22:28:59.8303310Z 
2026-10-13T22:28:59.8303802Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T22:28:59.8303975Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:28:59.8304099Z     "changed": false, 
2026-10-13T22:28:59.8304203Z     "msg": "All assertions passed"
2026-10-13T22:28:59.8304298Z }
2026-10-13T22:28:59.8329966Z Tuesday 13 October 2026  19:28:59 -0300 (0:00:00.058)       0:02:49.045 ******* 
2026-10-13T22:29:02.7375485Z 
2026-10-13T22:29:02.7375980Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T22:29:02.7376146Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:02.7403496Z Tuesday 13 October 2026  19:29:02 -0300 (0:00:02.907)       0:02:51.952 ******* 
2026-10-13T22:29:04.0708683Z 
2026-10-13T22:29:04.0709157Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T22:29:04.0715590Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:01.064800", "end": "2026-10-13 19:29:04.053066", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:29:02.988266", "stderr": "aviso: /var/tmp/rpm-tmp.nwlrdt: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.nwlrdt: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:29:04.0716443Z ...ignoring
2026-10-13T22:29:04.0744768Z Tuesday 13 October 2026  19:29:04 -0300 (0:00:01.334)       0:02:53.286 ******* 
2026-10-13T22:29:04.9474993Z 
2026-10-13T22:29:04.9475582Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T22:29:04.9479916Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.620028", "end": "2026-10-13 19:29:04.930828", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:29:04.310800", "stderr": "aviso: /var/tmp/rpm-tmp.p9gwQ5: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.p9gwQ5: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:29:04.9481183Z ...ignoring
2026-10-13T22:29:04.9508283Z Tuesday 13 October 2026  19:29:04 -0300 (0:00:00.876)       0:02:54.163 ******* 
2026-10-13T22:29:05.1999934Z 
2026-10-13T22:29:05.2001076Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T22:29:05.2001315Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:05.2026939Z Tuesday 13 October 2026  19:29:05 -0300 (0:00:00.251)       0:02:54.415 ******* 
2026-10-13T22:29:05.4581653Z 
2026-10-13T22:29:05.4582444Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T22:29:05.4582600Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:05.4608870Z Tuesday 13 October 2026  19:29:05 -0300 (0:00:00.258)       0:02:54.673 ******* 
2026-10-13T22:29:06.1173195Z 
2026-10-13T22:29:06.1173688Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T22:29:06.1173873Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:06.1212053Z Tuesday 13 October 2026  19:29:06 -0300 (0:00:00.660)       0:02:55.333 ******* 
2026-10-13T22:29:06.3878416Z 
2026-10-13T22:29:06.3878880Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T22:29:06.3879081Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:06.3908453Z Tuesday 13 October 2026  19:29:06 -0300 (0:00:00.269)       0:02:55.603 ******* 
2026-10-13T22:29:16.8386369Z 
2026-10-13T22:29:16.8386830Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T22:29:16.8386990Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:16.8413789Z Tuesday 13 October 2026  19:29:16 -0300 (0:00:10.450)       0:03:06.053 ******* 
2026-10-13T22:29:17.1454890Z 
2026-10-13T22:29:17.1455372Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T22:29:17.1455565Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:17.1475397Z Tuesday 13 October 2026  19:29:17 -0300 (0:00:00.306)       0:03:06.359 ******* 
2026-10-13T22:29:17.1910789Z Tuesday 13 October 2026  19:29:17 -0300 (0:00:00.043)       0:03:06.403 ******* 
2026-10-13T22:29:17.2466446Z 
2026-10-13T22:29:17.2466953Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T22:29:17.2467116Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:17.2489190Z Tuesday 13 October 2026  19:29:17 -0300 (0:00:00.058)       0:03:06.461 ******* 
2026-10-13T22:29:17.3025671Z 
2026-10-13T22:29:17.3026152Z TASK [nfs : debug] *************************************************************
2026-10-13T22:29:17.3026328Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:29:17.3026436Z     "msg": {
2026-10-13T22:29:17.3026576Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:29:17.3026717Z         "NFS_MOUNT_POINT": "/siexc"
2026-10-13T22:29:17.3027120Z     }
2026-10-13T22:29:17.3027212Z }
2026-10-13T22:29:17.3058220Z Tuesday 13 October 2026  19:29:17 -0300 (0:00:00.056)       0:03:06.518 ******* 
2026-10-13T22:29:17.3602506Z 
2026-10-13T22:29:17.3602947Z TASK [nfs : debug] *************************************************************
2026-10-13T22:29:17.3603169Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:29:17.3603294Z     "msg": "/siexc"
2026-10-13T22:29:17.3603392Z }
2026-10-13T22:29:17.3627663Z Tuesday 13 October 2026  19:29:17 -0300 (0:00:00.056)       0:03:06.575 ******* 
2026-10-13T22:29:17.4167234Z 
2026-10-13T22:29:17.4167726Z TASK [nfs : debug] *************************************************************
2026-10-13T22:29:17.4167903Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:29:17.4168052Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC"
2026-10-13T22:29:17.4168172Z }
2026-10-13T22:29:17.4194250Z Tuesday 13 October 2026  19:29:17 -0300 (0:00:00.056)       0:03:06.631 ******* 
2026-10-13T22:29:17.4762211Z 
2026-10-13T22:29:17.4762700Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T22:29:17.4762867Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:29:17.4763001Z     "changed": false, 
2026-10-13T22:29:17.4763112Z     "msg": "All assertions passed"
2026-10-13T22:29:17.4763200Z }
2026-10-13T22:29:17.4786964Z Tuesday 13 October 2026  19:29:17 -0300 (0:00:00.059)       0:03:06.691 ******* 
2026-10-13T22:29:20.6089987Z 
2026-10-13T22:29:20.6090469Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T22:29:20.6090638Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:20.6116698Z Tuesday 13 October 2026  19:29:20 -0300 (0:00:03.132)       0:03:09.824 ******* 
2026-10-13T22:29:22.1216294Z 
2026-10-13T22:29:22.1216899Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T22:29:22.1221089Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:01.268124", "end": "2026-10-13 19:29:22.105451", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:29:20.837327", "stderr": "aviso: /var/tmp/rpm-tmp.QsCMJf: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.QsCMJf: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:29:22.1222165Z ...ignoring
2026-10-13T22:29:22.1248249Z Tuesday 13 October 2026  19:29:22 -0300 (0:00:01.513)       0:03:11.337 ******* 
2026-10-13T22:29:23.2106950Z 
2026-10-13T22:29:23.2107452Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T22:29:23.2114288Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.831595", "end": "2026-10-13 19:29:23.194503", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:29:22.362908", "stderr": "aviso: /var/tmp/rpm-tmp.Ca1iR4: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.Ca1iR4: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:29:23.2115232Z ...ignoring
2026-10-13T22:29:23.2139286Z Tuesday 13 October 2026  19:29:23 -0300 (0:00:01.089)       0:03:12.426 ******* 
2026-10-13T22:29:23.4758932Z 
2026-10-13T22:29:23.4759626Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T22:29:23.4759804Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:23.4786808Z Tuesday 13 October 2026  19:29:23 -0300 (0:00:00.264)       0:03:12.691 ******* 
2026-10-13T22:29:23.7386652Z 
2026-10-13T22:29:23.7387725Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T22:29:23.7388044Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:23.7412766Z Tuesday 13 October 2026  19:29:23 -0300 (0:00:00.262)       0:03:12.953 ******* 
2026-10-13T22:29:24.3771916Z 
2026-10-13T22:29:24.3772534Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T22:29:24.3772722Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:24.3835139Z Tuesday 13 October 2026  19:29:24 -0300 (0:00:00.642)       0:03:13.595 ******* 
2026-10-13T22:29:24.6568238Z 
2026-10-13T22:29:24.6568808Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T22:29:24.6569079Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:24.6596845Z Tuesday 13 October 2026  19:29:24 -0300 (0:00:00.276)       0:03:13.872 ******* 
2026-10-13T22:29:35.0975887Z 
2026-10-13T22:29:35.0976368Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T22:29:35.0976539Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:35.1002714Z Tuesday 13 October 2026  19:29:35 -0300 (0:00:10.440)       0:03:24.312 ******* 
2026-10-13T22:29:35.4274270Z 
2026-10-13T22:29:35.4274757Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T22:29:35.4274948Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:35.4309534Z Tuesday 13 October 2026  19:29:35 -0300 (0:00:00.330)       0:03:24.643 ******* 
2026-10-13T22:29:35.4740619Z Tuesday 13 October 2026  19:29:35 -0300 (0:00:00.042)       0:03:24.686 ******* 
2026-10-13T22:29:35.5305366Z 
2026-10-13T22:29:35.5305857Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T22:29:35.5306116Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:35.5330143Z Tuesday 13 October 2026  19:29:35 -0300 (0:00:00.059)       0:03:24.745 ******* 
2026-10-13T22:29:35.5871163Z 
2026-10-13T22:29:35.5871643Z TASK [nfs : debug] *************************************************************
2026-10-13T22:29:35.5871823Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:29:35.5871939Z     "msg": {
2026-10-13T22:29:35.5872191Z         "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T22:29:35.5872316Z         "NFS_MOUNT_POINT": "/producao"
2026-10-13T22:29:35.5872436Z     }
2026-10-13T22:29:35.5872526Z }
2026-10-13T22:29:35.5898244Z Tuesday 13 October 2026  19:29:35 -0300 (0:00:00.056)       0:03:24.802 ******* 
2026-10-13T22:29:35.6430935Z 
2026-10-13T22:29:35.6431505Z TASK [nfs : debug] *************************************************************
2026-10-13T22:29:35.6431715Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:29:35.6431838Z     "msg": "/producao"
2026-10-13T22:29:35.6431934Z }
2026-10-13T22:29:35.6456416Z Tuesday 13 October 2026  19:29:35 -0300 (0:00:00.055)       0:03:24.857 ******* 
2026-10-13T22:29:35.6987749Z 
2026-10-13T22:29:35.6988222Z TASK [nfs : debug] *************************************************************
2026-10-13T22:29:35.6988389Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:29:35.6988530Z     "msg": "192.168.227.59:/export/sicql_bovespa"
2026-10-13T22:29:35.6988637Z }
2026-10-13T22:29:35.7012675Z Tuesday 13 October 2026  19:29:35 -0300 (0:00:00.055)       0:03:24.913 ******* 
2026-10-13T22:29:35.7571077Z 
2026-10-13T22:29:35.7571600Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T22:29:35.7571800Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:29:35.7572069Z     "changed": false, 
2026-10-13T22:29:35.7572194Z     "msg": "All assertions passed"
2026-10-13T22:29:35.7572294Z }
2026-10-13T22:29:35.7599177Z Tuesday 13 October 2026  19:29:35 -0300 (0:00:00.058)       0:03:24.972 ******* 
2026-10-13T22:29:38.6478755Z 
2026-10-13T22:29:38.6479646Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T22:29:38.6479843Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:38.6504602Z Tuesday 13 October 2026  19:29:38 -0300 (0:00:02.890)       0:03:27.862 ******* 
2026-10-13T22:29:39.6090492Z 
2026-10-13T22:29:39.6090948Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T22:29:39.6096473Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.681621", "end": "2026-10-13 19:29:39.592375", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:29:38.910754", "stderr": "aviso: /var/tmp/rpm-tmp.OVqfKl: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.OVqfKl: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:29:39.6097081Z ...ignoring
2026-10-13T22:29:39.6126225Z Tuesday 13 October 2026  19:29:39 -0300 (0:00:00.962)       0:03:28.824 ******* 
2026-10-13T22:29:40.5351315Z 
2026-10-13T22:29:40.5351894Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T22:29:40.5359968Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.669780", "end": "2026-10-13 19:29:40.518809", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:29:39.849029", "stderr": "aviso: /var/tmp/rpm-tmp.TpSExA: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.TpSExA: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:29:40.5360885Z ...ignoring
2026-10-13T22:29:40.5390127Z Tuesday 13 October 2026  19:29:40 -0300 (0:00:00.926)       0:03:29.751 ******* 
2026-10-13T22:29:40.7903152Z 
2026-10-13T22:29:40.7903809Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T22:29:40.7903985Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:40.7931396Z Tuesday 13 October 2026  19:29:40 -0300 (0:00:00.254)       0:03:30.005 ******* 
2026-10-13T22:29:41.0542519Z 
2026-10-13T22:29:41.0543186Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T22:29:41.0543356Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:41.0568210Z Tuesday 13 October 2026  19:29:41 -0300 (0:00:00.263)       0:03:30.269 ******* 
2026-10-13T22:29:41.7137081Z 
2026-10-13T22:29:41.7137564Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T22:29:41.7137756Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:41.7175937Z Tuesday 13 October 2026  19:29:41 -0300 (0:00:00.660)       0:03:30.929 ******* 
2026-10-13T22:29:41.9746128Z 
2026-10-13T22:29:41.9746580Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T22:29:41.9746791Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:41.9772755Z Tuesday 13 October 2026  19:29:41 -0300 (0:00:00.259)       0:03:31.189 ******* 
2026-10-13T22:29:52.4147979Z 
2026-10-13T22:29:52.4148597Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T22:29:52.4148867Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:52.4173235Z Tuesday 13 October 2026  19:29:52 -0300 (0:00:10.440)       0:03:41.629 ******* 
2026-10-13T22:29:52.7269093Z 
2026-10-13T22:29:52.7269567Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T22:29:52.7270111Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:52.7295927Z Tuesday 13 October 2026  19:29:52 -0300 (0:00:00.312)       0:03:41.941 ******* 
2026-10-13T22:29:52.7719166Z Tuesday 13 October 2026  19:29:52 -0300 (0:00:00.042)       0:03:41.984 ******* 
2026-10-13T22:29:52.8271456Z 
2026-10-13T22:29:52.8271935Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T22:29:52.8272246Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:52.8297054Z Tuesday 13 October 2026  19:29:52 -0300 (0:00:00.057)       0:03:42.042 ******* 
2026-10-13T22:29:52.8851845Z 
2026-10-13T22:29:52.8852459Z TASK [nfs : debug] *************************************************************
2026-10-13T22:29:52.8852634Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:29:52.8852757Z     "msg": {
2026-10-13T22:29:52.8852882Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC", 
2026-10-13T22:29:52.8854242Z         "NFS_MOUNT_POINT": "/suporte"
2026-10-13T22:29:52.8854680Z     }
2026-10-13T22:29:52.8854824Z }
2026-10-13T22:29:52.8877784Z Tuesday 13 October 2026  19:29:52 -0300 (0:00:00.058)       0:03:42.100 ******* 
2026-10-13T22:29:52.9416752Z 
2026-10-13T22:29:52.9417202Z TASK [nfs : debug] *************************************************************
2026-10-13T22:29:52.9417418Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:29:52.9417546Z     "msg": "/suporte"
2026-10-13T22:29:52.9417646Z }
2026-10-13T22:29:52.9442483Z Tuesday 13 October 2026  19:29:52 -0300 (0:00:00.056)       0:03:42.156 ******* 
2026-10-13T22:29:52.9978531Z 
2026-10-13T22:29:52.9979017Z TASK [nfs : debug] *************************************************************
2026-10-13T22:29:52.9979351Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:29:52.9979512Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC"
2026-10-13T22:29:52.9979633Z }
2026-10-13T22:29:53.0008222Z Tuesday 13 October 2026  19:29:52 -0300 (0:00:00.056)       0:03:42.213 ******* 
2026-10-13T22:29:53.0584398Z 
2026-10-13T22:29:53.0585104Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T22:29:53.0585410Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:29:53.0585541Z     "changed": false, 
2026-10-13T22:29:53.0585657Z     "msg": "All assertions passed"
2026-10-13T22:29:53.0585755Z }
2026-10-13T22:29:53.0610524Z Tuesday 13 October 2026  19:29:53 -0300 (0:00:00.060)       0:03:42.273 ******* 
2026-10-13T22:29:55.9583745Z 
2026-10-13T22:29:55.9584786Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T22:29:55.9585045Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:55.9611399Z Tuesday 13 October 2026  19:29:55 -0300 (0:00:02.900)       0:03:45.173 ******* 
2026-10-13T22:29:56.8821600Z 
2026-10-13T22:29:56.8822214Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T22:29:56.8826236Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.675378", "end": "2026-10-13 19:29:56.866529", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:29:56.191151", "stderr": "aviso: /var/tmp/rpm-tmp.hBaC62: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.hBaC62: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:29:56.8826872Z ...ignoring
2026-10-13T22:29:56.8851950Z Tuesday 13 October 2026  19:29:56 -0300 (0:00:00.924)       0:03:46.097 ******* 
2026-10-13T22:29:57.7634837Z 
2026-10-13T22:29:57.7635279Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T22:29:57.7636651Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.635121", "end": "2026-10-13 19:29:57.746526", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:29:57.111405", "stderr": "aviso: /var/tmp/rpm-tmp.yc1SRo: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.yc1SRo: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:29:57.7637257Z ...ignoring
2026-10-13T22:29:57.7659744Z Tuesday 13 October 2026  19:29:57 -0300 (0:00:00.880)       0:03:46.978 ******* 
2026-10-13T22:29:58.0161714Z 
2026-10-13T22:29:58.0162960Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T22:29:58.0163210Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:58.0194847Z Tuesday 13 October 2026  19:29:58 -0300 (0:00:00.253)       0:03:47.231 ******* 
2026-10-13T22:29:58.2683715Z 
2026-10-13T22:29:58.2684894Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T22:29:58.2685138Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:58.2711107Z Tuesday 13 October 2026  19:29:58 -0300 (0:00:00.251)       0:03:47.483 ******* 
2026-10-13T22:29:58.9132173Z 
2026-10-13T22:29:58.9133107Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T22:29:58.9133354Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:58.9178785Z Tuesday 13 October 2026  19:29:58 -0300 (0:00:00.646)       0:03:48.130 ******* 
2026-10-13T22:29:59.1873741Z 
2026-10-13T22:29:59.1874253Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T22:29:59.1874422Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:29:59.1902433Z Tuesday 13 October 2026  19:29:59 -0300 (0:00:00.272)       0:03:48.402 ******* 
2026-10-13T22:30:09.6247670Z 
2026-10-13T22:30:09.6248305Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T22:30:09.6248577Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:09.6278221Z Tuesday 13 October 2026  19:30:09 -0300 (0:00:10.437)       0:03:58.840 ******* 
2026-10-13T22:30:09.9539221Z 
2026-10-13T22:30:09.9540097Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T22:30:09.9540302Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:09.9604407Z Tuesday 13 October 2026  19:30:09 -0300 (0:00:00.330)       0:03:59.170 ******* 
2026-10-13T22:30:10.0019195Z Tuesday 13 October 2026  19:30:10 -0300 (0:00:00.043)       0:03:59.214 ******* 
2026-10-13T22:30:10.0604581Z 
2026-10-13T22:30:10.0605070Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T22:30:10.0605221Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:10.0624690Z Tuesday 13 October 2026  19:30:10 -0300 (0:00:00.060)       0:03:59.274 ******* 
2026-10-13T22:30:10.1203376Z 
2026-10-13T22:30:10.1203847Z TASK [nfs : debug] *************************************************************
2026-10-13T22:30:10.1204017Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:30:10.1204125Z     "msg": {
2026-10-13T22:30:10.1204247Z         "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T22:30:10.1204380Z         "NFS_MOUNT_POINT": "/producao/SWIFT"
2026-10-13T22:30:10.1204484Z     }
2026-10-13T22:30:10.1204589Z }
2026-10-13T22:30:10.1228989Z Tuesday 13 October 2026  19:30:10 -0300 (0:00:00.060)       0:03:59.335 ******* 
2026-10-13T22:30:10.1763071Z 
2026-10-13T22:30:10.1763572Z TASK [nfs : debug] *************************************************************
2026-10-13T22:30:10.1763743Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:30:10.1763870Z     "msg": "/producao/SWIFT"
2026-10-13T22:30:10.1763969Z }
2026-10-13T22:30:10.1792458Z Tuesday 13 October 2026  19:30:10 -0300 (0:00:00.056)       0:03:59.391 ******* 
2026-10-13T22:30:10.2355241Z 
2026-10-13T22:30:10.2356113Z TASK [nfs : debug] *************************************************************
2026-10-13T22:30:10.2356327Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:30:10.2356459Z     "msg": "192.168.227.59:/export/sicql_bovespa"
2026-10-13T22:30:10.2356574Z }
2026-10-13T22:30:10.2383292Z Tuesday 13 October 2026  19:30:10 -0300 (0:00:00.059)       0:03:59.450 ******* 
2026-10-13T22:30:10.2947749Z 
2026-10-13T22:30:10.2948201Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T22:30:10.2948411Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:30:10.2948537Z     "changed": false, 
2026-10-13T22:30:10.2948657Z     "msg": "All assertions passed"
2026-10-13T22:30:10.2948754Z }
2026-10-13T22:30:10.2978572Z Tuesday 13 October 2026  19:30:10 -0300 (0:00:00.059)       0:03:59.510 ******* 
2026-10-13T22:30:13.2810943Z 
2026-10-13T22:30:13.2811424Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T22:30:13.2811879Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:13.2835218Z Tuesday 13 October 2026  19:30:13 -0300 (0:00:02.985)       0:04:02.495 ******* 
2026-10-13T22:30:14.8492757Z 
2026-10-13T22:30:14.8493245Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T22:30:14.8497506Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:01.311075", "end": "2026-10-13 19:30:14.831711", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:30:13.520636", "stderr": "aviso: /var/tmp/rpm-tmp.zVp8f7: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.zVp8f7: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:30:14.8498387Z ...ignoring
2026-10-13T22:30:14.8523381Z Tuesday 13 October 2026  19:30:14 -0300 (0:00:01.568)       0:04:04.064 ******* 
2026-10-13T22:30:16.2407705Z 
2026-10-13T22:30:16.2408200Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T22:30:16.2412409Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:01.133484", "end": "2026-10-13 19:30:16.223051", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:30:15.089567", "stderr": "aviso: /var/tmp/rpm-tmp.cadvC0: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.cadvC0: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:30:16.2413045Z ...ignoring
2026-10-13T22:30:16.2440286Z Tuesday 13 October 2026  19:30:16 -0300 (0:00:01.391)       0:04:05.456 ******* 
2026-10-13T22:30:16.5113020Z 
2026-10-13T22:30:16.5113771Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T22:30:16.5114040Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:16.5147606Z Tuesday 13 October 2026  19:30:16 -0300 (0:00:00.270)       0:04:05.727 ******* 
2026-10-13T22:30:16.7793136Z 
2026-10-13T22:30:16.7793864Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T22:30:16.7794085Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:16.7820197Z Tuesday 13 October 2026  19:30:16 -0300 (0:00:00.267)       0:04:05.994 ******* 
2026-10-13T22:30:17.4624181Z 
2026-10-13T22:30:17.4624718Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T22:30:17.4624960Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:17.4661787Z Tuesday 13 October 2026  19:30:17 -0300 (0:00:00.684)       0:04:06.678 ******* 
2026-10-13T22:30:17.7697745Z 
2026-10-13T22:30:17.7698243Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T22:30:17.7698408Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:17.7724082Z Tuesday 13 October 2026  19:30:17 -0300 (0:00:00.306)       0:04:06.984 ******* 
2026-10-13T22:30:28.2211085Z 
2026-10-13T22:30:28.2211563Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T22:30:28.2212075Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:28.2237520Z Tuesday 13 October 2026  19:30:28 -0300 (0:00:10.451)       0:04:17.436 ******* 
2026-10-13T22:30:28.5240926Z 
2026-10-13T22:30:28.5241366Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T22:30:28.5241563Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:28.5265959Z Tuesday 13 October 2026  19:30:28 -0300 (0:00:00.302)       0:04:17.738 ******* 
2026-10-13T22:30:28.5703315Z Tuesday 13 October 2026  19:30:28 -0300 (0:00:00.043)       0:04:17.782 ******* 
2026-10-13T22:30:28.6256309Z 
2026-10-13T22:30:28.6256813Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-13T22:30:28.6256974Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:28.6281896Z Tuesday 13 October 2026  19:30:28 -0300 (0:00:00.057)       0:04:17.840 ******* 
2026-10-13T22:30:28.6825996Z 
2026-10-13T22:30:28.6826433Z TASK [nfs : debug] *************************************************************
2026-10-13T22:30:28.6826643Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:30:28.6827704Z     "msg": {
2026-10-13T22:30:28.6828881Z         "NFS_ENDPOINT": "192.168.227.59:/export/sicql_bovespa", 
2026-10-13T22:30:28.6829982Z         "NFS_MOUNT_POINT": "/SIEXC_SWIFT"
2026-10-13T22:30:28.6831048Z     }
2026-10-13T22:30:28.6832271Z }
2026-10-13T22:30:28.6853026Z Tuesday 13 October 2026  19:30:28 -0300 (0:00:00.057)       0:04:17.897 ******* 
2026-10-13T22:30:28.7406199Z 
2026-10-13T22:30:28.7407055Z TASK [nfs : debug] *************************************************************
2026-10-13T22:30:28.7407262Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:30:28.7407378Z     "msg": "/SIEXC_SWIFT"
2026-10-13T22:30:28.7407495Z }
2026-10-13T22:30:28.7431152Z Tuesday 13 October 2026  19:30:28 -0300 (0:00:00.057)       0:04:17.955 ******* 
2026-10-13T22:30:28.7987380Z 
2026-10-13T22:30:28.7988190Z TASK [nfs : debug] *************************************************************
2026-10-13T22:30:28.7988436Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:30:28.7988577Z     "msg": "192.168.227.59:/export/sicql_bovespa"
2026-10-13T22:30:28.7988693Z }
2026-10-13T22:30:28.8015672Z Tuesday 13 October 2026  19:30:28 -0300 (0:00:00.058)       0:04:18.013 ******* 
2026-10-13T22:30:28.8604119Z 
2026-10-13T22:30:28.8605013Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-13T22:30:28.8605273Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => {
2026-10-13T22:30:28.8605442Z     "changed": false, 
2026-10-13T22:30:28.8605586Z     "msg": "All assertions passed"
2026-10-13T22:30:28.8606260Z }
2026-10-13T22:30:28.8629789Z Tuesday 13 October 2026  19:30:28 -0300 (0:00:00.061)       0:04:18.075 ******* 
2026-10-13T22:30:31.8695276Z 
2026-10-13T22:30:31.8695767Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-13T22:30:31.8695942Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:31.8721266Z Tuesday 13 October 2026  19:30:31 -0300 (0:00:03.009)       0:04:21.084 ******* 
2026-10-13T22:30:32.9978483Z 
2026-10-13T22:30:32.9978924Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-13T22:30:32.9983728Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.866992", "end": "2026-10-13 19:30:32.981035", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:30:32.114043", "stderr": "aviso: /var/tmp/rpm-tmp.vFNjvy: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.vFNjvy: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:30:32.9984705Z ...ignoring
2026-10-13T22:30:33.0011857Z Tuesday 13 October 2026  19:30:33 -0300 (0:00:01.128)       0:04:22.213 ******* 
2026-10-13T22:30:33.9604668Z 
2026-10-13T22:30:33.9605153Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-13T22:30:33.9606468Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.705975", "end": "2026-10-13 19:30:33.943674", "msg": "non-zero return code", "rc": 1, "start": "2026-10-13 19:30:33.237699", "stderr": "aviso: /var/tmp/rpm-tmp.xzjre3: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.xzjre3: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-13T22:30:33.9607057Z ...ignoring
2026-10-13T22:30:33.9631554Z Tuesday 13 October 2026  19:30:33 -0300 (0:00:00.962)       0:04:23.175 ******* 
2026-10-13T22:30:34.2161028Z 
2026-10-13T22:30:34.2161818Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-13T22:30:34.2162295Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:34.2189824Z Tuesday 13 October 2026  19:30:34 -0300 (0:00:00.255)       0:04:23.431 ******* 
2026-10-13T22:30:34.4641058Z 
2026-10-13T22:30:34.4641503Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-13T22:30:34.4641732Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:34.4672372Z Tuesday 13 October 2026  19:30:34 -0300 (0:00:00.248)       0:04:23.679 ******* 
2026-10-13T22:30:35.1204128Z 
2026-10-13T22:30:35.1205059Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-13T22:30:35.1205256Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:35.1240994Z Tuesday 13 October 2026  19:30:35 -0300 (0:00:00.656)       0:04:24.336 ******* 
2026-10-13T22:30:35.4019471Z 
2026-10-13T22:30:35.4020216Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-13T22:30:35.4020675Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:35.4047299Z Tuesday 13 October 2026  19:30:35 -0300 (0:00:00.280)       0:04:24.617 ******* 
2026-10-13T22:30:45.8430276Z 
2026-10-13T22:30:45.8431096Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-13T22:30:45.8431626Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:45.8455890Z Tuesday 13 October 2026  19:30:45 -0300 (0:00:10.440)       0:04:35.057 ******* 
2026-10-13T22:30:46.1089866Z 
2026-10-13T22:30:46.1090504Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-13T22:30:46.1090761Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:46.1118156Z Tuesday 13 October 2026  19:30:46 -0300 (0:00:00.266)       0:04:35.324 ******* 
2026-10-13T22:30:46.1574716Z 
2026-10-13T22:30:46.1575150Z PLAY [jboss] *******************************************************************
2026-10-13T22:30:46.1607609Z 
2026-10-13T22:30:46.1608353Z PLAY [jboss] *******************************************************************
2026-10-13T22:30:46.1640586Z Tuesday 13 October 2026  19:30:46 -0300 (0:00:00.052)       0:04:35.376 ******* 
2026-10-13T22:30:46.8014026Z 
2026-10-13T22:30:46.8014503Z TASK [Gathering Facts] *********************************************************
2026-10-13T22:30:46.8014682Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:46.8251723Z Tuesday 13 October 2026  19:30:46 -0300 (0:00:00.660)       0:04:36.037 ******* 
2026-10-13T22:30:48.2609339Z 
2026-10-13T22:30:48.2609827Z TASK [Gerando fatos de servicos] ***********************************************
2026-10-13T22:30:48.2610514Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:48.2946806Z Tuesday 13 October 2026  19:30:48 -0300 (0:00:01.469)       0:04:37.506 ******* 
2026-10-13T22:30:48.3534408Z 
2026-10-13T22:30:48.3534914Z TASK [Gerando lista de units jboss] ********************************************
2026-10-13T22:30:48.3535073Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:48.3826013Z Tuesday 13 October 2026  19:30:48 -0300 (0:00:00.087)       0:04:37.594 ******* 
2026-10-13T22:30:48.4503704Z Tuesday 13 October 2026  19:30:48 -0300 (0:00:00.067)       0:04:37.662 ******* 
2026-10-13T22:30:48.4618791Z 
2026-10-13T22:30:48.4619247Z PLAY [Copiando deployments adicionais] *****************************************
2026-10-13T22:30:48.4924977Z Tuesday 13 October 2026  19:30:48 -0300 (0:00:00.042)       0:04:37.704 ******* 
2026-10-13T22:30:48.5474194Z 
2026-10-13T22:30:48.5474863Z TASK [Cria variável build_repository_name] *************************************
2026-10-13T22:30:48.5475043Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:48.5762368Z Tuesday 13 October 2026  19:30:48 -0300 (0:00:00.083)       0:04:37.788 ******* 
2026-10-13T22:30:48.6311760Z 
2026-10-13T22:30:48.6312326Z TASK [Buscando diretorio de config] ********************************************
2026-10-13T22:30:48.6312519Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:48.6615511Z Tuesday 13 October 2026  19:30:48 -0300 (0:00:00.085)       0:04:37.873 ******* 
2026-10-13T22:30:48.7164007Z 
2026-10-13T22:30:48.7164832Z TASK [Buscando diretorio de config] ********************************************
2026-10-13T22:30:48.7165096Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:48.7509995Z Tuesday 13 October 2026  19:30:48 -0300 (0:00:00.089)       0:04:37.963 ******* 
2026-10-13T22:30:49.2334672Z 
2026-10-13T22:30:49.2335160Z TASK [Create a symbolic link] **************************************************
2026-10-13T22:30:49.2335576Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config)
2026-10-13T22:30:49.4878574Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T22:30:49.5207372Z Tuesday 13 October 2026  19:30:49 -0300 (0:00:00.769)       0:04:38.732 ******* 
2026-10-13T22:30:49.8226743Z 
2026-10-13T22:30:49.8227602Z TASK [Verifica se o arquivo  existe] *******************************************
2026-10-13T22:30:49.8228068Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config)
2026-10-13T22:30:50.0880346Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T22:30:50.1195758Z Tuesday 13 October 2026  19:30:50 -0300 (0:00:00.598)       0:04:39.331 ******* 
2026-10-13T22:30:50.2141426Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/jboss/tasks/stack_deployments_custom_block.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:30:50.2453674Z Tuesday 13 October 2026  19:30:50 -0300 (0:00:00.125)       0:04:39.457 ******* 
2026-10-13T22:30:50.7028871Z 
2026-10-13T22:30:50.7029418Z TASK [Lendo artefatos do arquivo CSV] ******************************************
2026-10-13T22:30:50.7029683Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:50.7385515Z Tuesday 13 October 2026  19:30:50 -0300 (0:00:00.493)       0:04:39.950 ******* 
2026-10-13T22:30:50.7462955Z [WARNING]: The loop variable 'item' is already in use. You should set the
2026-10-13T22:30:50.7463601Z `loop_var` value in the `loop_control` option for the task to something else to
2026-10-13T22:30:50.7463845Z avoid variable collisions and unexpected behavior.
2026-10-13T22:30:50.7850146Z 
2026-10-13T22:30:50.7850636Z TASK [Mostra artefatos] ********************************************************
2026-10-13T22:30:50.7851097Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'7.0.1.12', u'group_id': u'com.ibm.wmq', u'extension': u'rar', u'artifact_id': u'wmq.jmsra'}) => {
2026-10-13T22:30:50.7851332Z     "msg": "Artefato: wmq.jmsra - versao 7.0.1.12"
2026-10-13T22:30:50.7851461Z }
2026-10-13T22:30:50.8153450Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'0.0.2', u'group_id': u'br.com.treesolution', u'extension': u'war', u'artifact_id': u'exc_web'}) => {
2026-10-13T22:30:50.8153790Z     "msg": "Artefato: exc_web - versao 0.0.2"
2026-10-13T22:30:50.8153905Z }
2026-10-13T22:30:50.8481225Z Tuesday 13 October 2026  19:30:50 -0300 (0:00:00.109)       0:04:40.060 ******* 
2026-10-13T22:30:51.4662110Z 
2026-10-13T22:30:51.4662781Z TASK [maven_artifact] **********************************************************
2026-10-13T22:30:51.4663459Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'7.0.1.12', u'group_id': u'com.ibm.wmq', u'extension': u'rar', u'artifact_id': u'wmq.jmsra'})
2026-10-13T22:30:51.8034032Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'0.0.2', u'group_id': u'br.com.treesolution', u'extension': u'war', u'artifact_id': u'exc_web'})
2026-10-13T22:30:51.8340410Z Tuesday 13 October 2026  19:30:51 -0300 (0:00:00.985)       0:04:41.046 ******* 
2026-10-13T22:30:53.4495689Z 
2026-10-13T22:30:53.4496531Z TASK [Copiando artefatos para o(s) servidor(es) Jboss] *************************
2026-10-13T22:30:53.4496776Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:53.4799544Z Tuesday 13 October 2026  19:30:53 -0300 (0:00:01.645)       0:04:42.692 ******* 
2026-10-13T22:30:53.5210585Z 
2026-10-13T22:30:53.5211064Z PLAY [Copiando modules adicionais] *********************************************
2026-10-13T22:30:53.5514562Z Tuesday 13 October 2026  19:30:53 -0300 (0:00:00.071)       0:04:42.763 ******* 
2026-10-13T22:30:53.6225844Z 
2026-10-13T22:30:53.6226928Z TASK [Cria variável build_repository_name] *************************************
2026-10-13T22:30:53.6227553Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:53.6513645Z Tuesday 13 October 2026  19:30:53 -0300 (0:00:00.099)       0:04:42.863 ******* 
2026-10-13T22:30:53.7060239Z 
2026-10-13T22:30:53.7061025Z TASK [Buscando diretorio de config] ********************************************
2026-10-13T22:30:53.7061671Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:53.7363901Z Tuesday 13 October 2026  19:30:53 -0300 (0:00:00.084)       0:04:42.948 ******* 
2026-10-13T22:30:53.7894706Z 
2026-10-13T22:30:53.7895177Z TASK [Buscando diretorio de config] ********************************************
2026-10-13T22:30:53.7895348Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:53.8218228Z Tuesday 13 October 2026  19:30:53 -0300 (0:00:00.085)       0:04:43.033 ******* 
2026-10-13T22:30:54.1365690Z 
2026-10-13T22:30:54.1366514Z TASK [Create a directory] ******************************************************
2026-10-13T22:30:54.1367222Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config)
2026-10-13T22:30:54.3930854Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T22:30:54.4276782Z Tuesday 13 October 2026  19:30:54 -0300 (0:00:00.605)       0:04:43.639 ******* 
2026-10-13T22:30:54.7347711Z 
2026-10-13T22:30:54.7348622Z TASK [Verifica se o arquivo  existe] *******************************************
2026-10-13T22:30:54.7349065Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config)
2026-10-13T22:30:54.9984900Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T22:30:55.0311795Z Tuesday 13 October 2026  19:30:55 -0300 (0:00:00.603)       0:04:44.243 ******* 
2026-10-13T22:30:55.1318701Z included: /opt/ads-agent/_work/r12364/a/esteira-jboss-vm-v2/roles/jboss/tasks/stack_modules_custom_block.yml for caddeapllx2193.agil.nprd.caixa.gov.br
2026-10-13T22:30:55.1629210Z Tuesday 13 October 2026  19:30:55 -0300 (0:00:00.131)       0:04:44.375 ******* 
2026-10-13T22:30:55.6656818Z 
2026-10-13T22:30:55.6657293Z TASK [Lendo artefatos do arquivo CSV] ******************************************
2026-10-13T22:30:55.6657477Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:55.7028208Z Tuesday 13 October 2026  19:30:55 -0300 (0:00:00.539)       0:04:44.914 ******* 
2026-10-13T22:30:55.7128211Z [WARNING]: The loop variable 'item' is already in use. You should set the
2026-10-13T22:30:55.7128435Z `loop_var` value in the `loop_control` option for the task to something else to
2026-10-13T22:30:55.7128576Z avoid variable collisions and unexpected behavior.
2026-10-13T22:30:55.7496011Z 
2026-10-13T22:30:55.7496613Z TASK [Mostra lista de artefatos] ***********************************************
2026-10-13T22:30:55.7497264Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.6.redhat-6', u'group_id': u'commons-pool', u'extension': u'xml', u'artifact_id': u'commons-pool'}) => {
2026-10-13T22:30:55.7497695Z     "msg": "Artefato: commons-pool - versao 1.6.redhat-6"
2026-10-13T22:30:55.7497876Z }
2026-10-13T22:30:55.7795634Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.6.redhat-6', u'group_id': u'commons-pool', u'extension': u'jar', u'artifact_id': u'commons-pool'}) => {
2026-10-13T22:30:55.7796155Z     "msg": "Artefato: commons-pool - versao 1.6.redhat-6"
2026-10-13T22:30:55.7796348Z }
2026-10-13T22:30:55.8116473Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'42.7.7', u'group_id': u'org.postgres', u'extension': u'jar', u'artifact_id': u'postgresql'}) => {
2026-10-13T22:30:55.8116802Z     "msg": "Artefato: postgresql - versao 42.7.7"
2026-10-13T22:30:55.8116921Z }
2026-10-13T22:30:55.8419745Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'19.3.0.0', u'group_id': u'com.oracle.ojdbc', u'extension': u'jar', u'artifact_id': u'ojdbc8'}) => {
2026-10-13T22:30:55.8420048Z     "msg": "Artefato: ojdbc8 - versao 19.3.0.0"
2026-10-13T22:30:55.8420157Z }
2026-10-13T22:30:55.8728446Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.1', u'group_id': u'org.apache.commons.jexl', u'extension': u'jar', u'artifact_id': u'commons-jexl'}) => {
2026-10-13T22:30:55.8728795Z     "msg": "Artefato: commons-jexl - versao 1.1"
2026-10-13T22:30:55.8728907Z }
2026-10-13T22:30:55.9035828Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.2.5', u'group_id': u'net.sourceforge', u'extension': u'jar', u'artifact_id': u'jtds'}) => {
2026-10-13T22:30:55.9036145Z     "msg": "Artefato: jtds - versao 1.2.5"
2026-10-13T22:30:55.9036252Z }
2026-10-13T22:30:55.9353775Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.3.1', u'group_id': u'net.sourceforge', u'extension': u'jar', u'artifact_id': u'jtds'}) => {
2026-10-13T22:30:55.9354062Z     "msg": "Artefato: jtds - versao 1.3.1"
2026-10-13T22:30:55.9354171Z }
2026-10-13T22:30:55.9662856Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.0.0', u'group_id': u'br.com.treebpm', u'extension': u'jar', u'artifact_id': u'treebpm'}) => {
2026-10-13T22:30:55.9663181Z     "msg": "Artefato: treebpm - versao 1.0.0"
2026-10-13T22:30:55.9663593Z }
2026-10-13T22:30:55.9968661Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.0.0', u'group_id': u'br.com.concepting.framework', u'extension': u'jar', u'artifact_id': u'concepting-framework'}) => {
2026-10-13T22:30:55.9968975Z     "msg": "Artefato: concepting-framework - versao 3.0.0"
2026-10-13T22:30:55.9969094Z }
2026-10-13T22:30:56.0823580Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'2.2', u'group_id': u'cglib', u'extension': u'jar', u'artifact_id': u'cglib-nodep'}) => {
2026-10-13T22:30:56.0823887Z     "msg": "Artefato: cglib-nodep - versao 2.2"
2026-10-13T22:30:56.0823999Z }
2026-10-13T22:30:56.1134583Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.4.1', u'group_id': u'javax.mail', u'extension': u'jar', u'artifact_id': u'mail'}) => {
2026-10-13T22:30:56.1135415Z     "msg": "Artefato: mail - versao 1.4.1"
2026-10-13T22:30:56.1135951Z }
2026-10-13T22:30:56.1445873Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.10.1', u'group_id': u'org.apache.poi', u'extension': u'jar', u'artifact_id': u'poi'}) => {
2026-10-13T22:30:56.1446199Z     "msg": "Artefato: poi - versao 3.10.1"
2026-10-13T22:30:56.1446304Z }
2026-10-13T22:30:56.1748213Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.10.1', u'group_id': u'org.apache.poi', u'extension': u'jar', u'artifact_id': u'poi-ooxml'}) => {
2026-10-13T22:30:56.1748513Z     "msg": "Artefato: poi-ooxml - versao 3.10.1"
2026-10-13T22:30:56.1748641Z }
2026-10-13T22:30:56.2048756Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.10.1', u'group_id': u'org.apache.poi', u'extension': u'jar', u'artifact_id': u'poi-ooxml-schemas'}) => {
2026-10-13T22:30:56.2049100Z     "msg": "Artefato: poi-ooxml-schemas - versao 3.10.1"
2026-10-13T22:30:56.2049254Z }
2026-10-13T22:30:56.2354519Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'2.6.0', u'group_id': u'org.apache.xmlbeans', u'extension': u'jar', u'artifact_id': u'xmlbeans'}) => {
2026-10-13T22:30:56.2354875Z     "msg": "Artefato: xmlbeans - versao 2.6.0"
2026-10-13T22:30:56.2354986Z }
2026-10-13T22:30:56.2691420Z Tuesday 13 October 2026  19:30:56 -0300 (0:00:00.566)       0:04:45.481 ******* 
2026-10-13T22:30:56.6856407Z 
2026-10-13T22:30:56.6857468Z TASK [Listar arquivos no diretório baixados anteriormente] *********************
2026-10-13T22:30:56.6857674Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:30:56.7177939Z Tuesday 13 October 2026  19:30:56 -0300 (0:00:00.448)       0:04:45.929 ******* 
2026-10-13T22:30:56.7615774Z [WARNING]: conditional statements should not include jinja2 templating
2026-10-13T22:30:56.7616203Z delimiters such as {{ }} or {% %}. Found: '{{ inner_item.artifact_id }}-{{
2026-10-13T22:30:56.7616425Z inner_item.version }}.{{ inner_item.extension|default('jar',true) }}' not in
2026-10-13T22:30:56.7616634Z files_found.files | map(attribute='path') | map('basename') | list
2026-10-13T22:30:57.1334167Z 
2026-10-13T22:30:57.1335020Z TASK [maven_artifact] **********************************************************
2026-10-13T22:30:57.1335948Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.6.redhat-6', u'group_id': u'commons-pool', u'extension': u'xml', u'artifact_id': u'commons-pool'})
2026-10-13T22:30:57.4743741Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.6.redhat-6', u'group_id': u'commons-pool', u'extension': u'jar', u'artifact_id': u'commons-pool'})
2026-10-13T22:30:57.8209334Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'42.7.7', u'group_id': u'org.postgres', u'extension': u'jar', u'artifact_id': u'postgresql'})
2026-10-13T22:30:58.1782082Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'19.3.0.0', u'group_id': u'com.oracle.ojdbc', u'extension': u'jar', u'artifact_id': u'ojdbc8'})
2026-10-13T22:30:58.5179302Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.1', u'group_id': u'org.apache.commons.jexl', u'extension': u'jar', u'artifact_id': u'commons-jexl'})
2026-10-13T22:30:58.8630306Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.2.5', u'group_id': u'net.sourceforge', u'extension': u'jar', u'artifact_id': u'jtds'})
2026-10-13T22:30:59.2084764Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.3.1', u'group_id': u'net.sourceforge', u'extension': u'jar', u'artifact_id': u'jtds'})
2026-10-13T22:30:59.5470252Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.0.0', u'group_id': u'br.com.treebpm', u'extension': u'jar', u'artifact_id': u'treebpm'})
2026-10-13T22:30:59.9038551Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.0.0', u'group_id': u'br.com.concepting.framework', u'extension': u'jar', u'artifact_id': u'concepting-framework'})
2026-10-13T22:31:00.2507670Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'2.2', u'group_id': u'cglib', u'extension': u'jar', u'artifact_id': u'cglib-nodep'})
2026-10-13T22:31:00.6090819Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'1.4.1', u'group_id': u'javax.mail', u'extension': u'jar', u'artifact_id': u'mail'})
2026-10-13T22:31:00.9785035Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.10.1', u'group_id': u'org.apache.poi', u'extension': u'jar', u'artifact_id': u'poi'})
2026-10-13T22:31:01.3454557Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.10.1', u'group_id': u'org.apache.poi', u'extension': u'jar', u'artifact_id': u'poi-ooxml'})
2026-10-13T22:31:01.7085221Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'3.10.1', u'group_id': u'org.apache.poi', u'extension': u'jar', u'artifact_id': u'poi-ooxml-schemas'})
2026-10-13T22:31:02.0638538Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'version': u'2.6.0', u'group_id': u'org.apache.xmlbeans', u'extension': u'jar', u'artifact_id': u'xmlbeans'})
2026-10-13T22:31:02.1097652Z Tuesday 13 October 2026  19:31:02 -0300 (0:00:05.391)       0:04:51.321 ******* 
2026-10-13T22:31:02.4272575Z 
2026-10-13T22:31:02.4273320Z TASK [Verifica se o arquivo jboss-modules-custom tem conteudo] *****************
2026-10-13T22:31:02.4273484Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:31:02.4587822Z Tuesday 13 October 2026  19:31:02 -0300 (0:00:00.348)       0:04:51.670 ******* 
2026-10-13T22:31:10.4907578Z 
2026-10-13T22:31:10.4908523Z TASK [Copiando artefatos (Modules) para o(s) servidor(es) Jboss] ***************
2026-10-13T22:31:10.4908806Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:31:10.5197295Z Tuesday 13 October 2026  19:31:10 -0300 (0:00:08.060)       0:04:59.731 ******* 
2026-10-13T22:31:11.1708918Z 
2026-10-13T22:31:11.1709585Z TASK [Copiando artefato (jboss-custom.cli) para o(s) servidor(es) Jboss] *******
2026-10-13T22:31:11.1709754Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:31:11.2000697Z Tuesday 13 October 2026  19:31:11 -0300 (0:00:00.680)       0:05:00.412 ******* 
2026-10-13T22:31:19.3139996Z 
2026-10-13T22:31:19.3140667Z TASK [Executando o jboss-custom.cli] *******************************************
2026-10-13T22:31:19.3140841Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:31:19.3451408Z Tuesday 13 October 2026  19:31:19 -0300 (0:00:08.145)       0:05:08.557 ******* 
2026-10-13T22:31:21.3422490Z 
2026-10-13T22:31:21.3423333Z TASK [Encontrar todos os arquivos module.xml] **********************************
2026-10-13T22:31:21.3423893Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:31:21.7109332Z Tuesday 13 October 2026  19:31:21 -0300 (0:00:02.365)       0:05:10.923 ******* 
2026-10-13T22:31:23.1190609Z 
2026-10-13T22:31:23.1191279Z TASK [Filtrar arquivos dentro da pasta system na raiz] *************************
2026-10-13T22:31:23.1191444Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:31:23.4812094Z Tuesday 13 October 2026  19:31:23 -0300 (0:00:01.770)       0:05:12.693 ******* 
2026-10-13T22:31:23.8632889Z 
2026-10-13T22:31:23.8633435Z TASK [Filtrar arquivos fora da pasta system na raiz] ***************************
2026-10-13T22:31:23.8635421Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:31:23.8922309Z Tuesday 13 October 2026  19:31:23 -0300 (0:00:00.410)       0:05:13.104 ******* 
2026-10-13T22:31:23.9329525Z Tuesday 13 October 2026  19:31:23 -0300 (0:00:00.040)       0:05:13.144 ******* 
2026-10-13T22:31:23.9746313Z 
2026-10-13T22:31:23.9746867Z PLAY [jboss] *******************************************************************
2026-10-13T22:31:24.0066574Z Tuesday 13 October 2026  19:31:24 -0300 (0:00:00.073)       0:05:13.218 ******* 
2026-10-13T22:31:24.0697125Z 
2026-10-13T22:31:24.0698122Z TASK [Setando a versão do Jboss] ***********************************************
2026-10-13T22:31:24.0698373Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:31:24.0992408Z Tuesday 13 October 2026  19:31:24 -0300 (0:00:00.092)       0:05:13.311 ******* 
2026-10-13T22:31:24.1537126Z 
2026-10-13T22:31:24.1537756Z TASK [Cria variável build_repository_name_tfs] *********************************
2026-10-13T22:31:24.1537938Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:31:24.1834675Z Tuesday 13 October 2026  19:31:24 -0300 (0:00:00.084)       0:05:13.395 ******* 
2026-10-13T22:31:24.2394342Z 
2026-10-13T22:31:24.2395251Z TASK [Buscando diretorio de config] ********************************************
2026-10-13T22:31:24.2395544Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:31:24.2687579Z Tuesday 13 October 2026  19:31:24 -0300 (0:00:00.085)       0:05:13.480 ******* 
2026-10-13T22:31:24.8965308Z 
2026-10-13T22:31:24.8965784Z TASK [Copy common_start.sh] ****************************************************
2026-10-13T22:31:24.8966067Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:31:24.9260071Z Tuesday 13 October 2026  19:31:24 -0300 (0:00:00.657)       0:05:14.138 ******* 
2026-10-13T22:31:25.6600224Z 
2026-10-13T22:31:25.6600729Z TASK [Copy template script] ****************************************************
2026-10-13T22:31:25.6600897Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:31:25.7036889Z Tuesday 13 October 2026  19:31:25 -0300 (0:00:00.777)       0:05:14.915 ******* 
2026-10-13T22:31:26.3974166Z 
2026-10-13T22:31:26.3974647Z TASK [JBoss systemd wrapper for sysvinit script mode domain] *******************
2026-10-13T22:31:26.3974822Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:31:26.4265272Z Tuesday 13 October 2026  19:31:26 -0300 (0:00:00.722)       0:05:15.638 ******* 
2026-10-13T22:31:27.2124775Z 
2026-10-13T22:31:27.2125264Z TASK [Realiza copia do arquivo de Trust Store] *********************************
2026-10-13T22:31:27.2125439Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:31:27.2413473Z Tuesday 13 October 2026  19:31:27 -0300 (0:00:00.814)       0:05:16.453 ******* 
2026-10-13T22:31:27.3127423Z Tuesday 13 October 2026  19:31:27 -0300 (0:00:00.071)       0:05:16.524 ******* 
2026-10-13T22:31:27.4006335Z Tuesday 13 October 2026  19:31:27 -0300 (0:00:00.087)       0:05:16.612 ******* 
2026-10-13T22:31:27.7185028Z 
2026-10-13T22:31:27.7185494Z TASK [Check directory configuration exists] ************************************
2026-10-13T22:31:27.7185911Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config)
2026-10-13T22:31:27.9709173Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T22:31:28.0009200Z Tuesday 13 October 2026  19:31:27 -0300 (0:00:00.600)       0:05:17.213 ******* 
2026-10-13T22:32:02.0128415Z 
2026-10-13T22:32:02.0130423Z TASK [Copiando arquivos para jboss.server.config.dir] **************************
2026-10-13T22:32:02.0132144Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config', u'stat': {u'charset': u'binary', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1791930207.5585706, u'block_size': 4096, u'inode': 746586290, u'isgid': False, u'size': 102, u'wgrp': False, u'executable': True, u'isuid': False, u'readable': True, u'isreg': False, u'version': u'18446744072571881568', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'inode/directory', u'blocks': 0, u'xoth': True, u'islnk': False, u'nlink': 5, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/configuration', u'xusr': True, u'atime': 1791930211.7115169, u'isdir': True, u'ctime': 1791930207.5585706, u'isblk': False, u'xgrp': True, u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0755', u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/configuration', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-13T22:32:02.0545484Z Tuesday 13 October 2026  19:32:02 -0300 (0:00:34.053)       0:05:51.266 ******* 
2026-10-13T22:32:02.3705452Z 
2026-10-13T22:32:02.3706150Z TASK [Get standalone-full-ha.xml status] ***************************************
2026-10-13T22:32:02.3706437Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config)
2026-10-13T22:32:02.6435468Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T22:32:02.6741025Z Tuesday 13 October 2026  19:32:02 -0300 (0:00:00.619)       0:05:51.886 ******* 
2026-10-13T22:32:03.4369695Z 
2026-10-13T22:32:03.4370310Z TASK [Copiando arquivo standalone-full-ha.xml] *********************************
2026-10-13T22:32:03.4373228Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/jboss', u'stat': {u'charset': u'us-ascii', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1791930211.7415164, u'block_size': 4096, u'inode': 54530859, u'isgid': False, u'size': 53658, u'wgrp': False, u'executable': False, u'isuid': False, u'readable': True, u'isreg': True, u'version': u'18446744072184623877', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'application/xml', u'blocks': 112, u'xoth': False, u'islnk': False, u'nlink': 1, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/jboss/standalone-full-ha.xml', u'xusr': False, u'atime': 1791930212.8765016, u'isdir': False, u'ctime': 1791930211.7415164, u'isblk': False, u'checksum': u'068865c141f587f59187503ef73ad9fe4fe8fb3e', u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0644', u'xgrp': False, u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/jboss/standalone-full-ha.xml', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-13T22:32:03.4716445Z Tuesday 13 October 2026  19:32:03 -0300 (0:00:00.797)       0:05:52.683 ******* 
2026-10-13T22:32:03.8047265Z 
2026-10-13T22:32:03.8048576Z TASK [Get standalone-ha.xml status] ********************************************
2026-10-13T22:32:03.8048994Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config)
2026-10-13T22:32:04.0776418Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T22:32:04.1098380Z Tuesday 13 October 2026  19:32:04 -0300 (0:00:00.638)       0:05:53.321 ******* 
2026-10-13T22:32:04.1914383Z Tuesday 13 October 2026  19:32:04 -0300 (0:00:00.081)       0:05:53.403 ******* 
2026-10-13T22:32:04.4989369Z 
2026-10-13T22:32:04.4990232Z TASK [Get standalone.xml status] ***********************************************
2026-10-13T22:32:04.4992468Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config)
2026-10-13T22:32:04.7661914Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T22:32:04.7973189Z Tuesday 13 October 2026  19:32:04 -0300 (0:00:00.605)       0:05:54.009 ******* 
2026-10-13T22:32:04.8807704Z Tuesday 13 October 2026  19:32:04 -0300 (0:00:00.083)       0:05:54.092 ******* 
2026-10-13T22:32:05.1933856Z 
2026-10-13T22:32:05.1934735Z TASK [Get standalone.conf status] **********************************************
2026-10-13T22:32:05.1935201Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config)
2026-10-13T22:32:05.4779483Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/jboss)
2026-10-13T22:32:05.5101918Z Tuesday 13 October 2026  19:32:05 -0300 (0:00:00.629)       0:05:54.722 ******* 
2026-10-13T22:32:06.2272307Z 
2026-10-13T22:32:06.2272937Z TASK [Copiando arquivo standalone.conf] ****************************************
2026-10-13T22:32:06.2278141Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/jboss', u'stat': {u'charset': u'us-ascii', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1791930211.7475164, u'block_size': 4096, u'inode': 54532547, u'isgid': False, u'size': 4820, u'wgrp': False, u'executable': False, u'isuid': False, u'readable': True, u'isreg': True, u'version': u'1379144951', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'text/plain', u'blocks': 16, u'xoth': False, u'islnk': False, u'nlink': 1, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/jboss/standalone.conf', u'xusr': False, u'atime': 1791930211.7475164, u'isdir': False, u'ctime': 1791930211.7475164, u'isblk': False, u'checksum': u'c8ab4145a3767cb7fbb7957a7732cf1973517f8e', u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0644', u'xgrp': False, u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/jboss/standalone.conf', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-13T22:32:06.2599339Z Tuesday 13 October 2026  19:32:06 -0300 (0:00:00.749)       0:05:55.472 ******* 
2026-10-13T22:32:06.6073377Z 
2026-10-13T22:32:06.6073867Z TASK [Restart Zabbix] **********************************************************
2026-10-13T22:32:06.6074331Z fatal: [caddeapllx2193.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "msg": "Could not find the requested service zabbix-agent: host"}
2026-10-13T22:32:06.6074490Z ...ignoring
2026-10-13T22:32:06.6387373Z Tuesday 13 October 2026  19:32:06 -0300 (0:00:00.378)       0:05:55.850 ******* 
2026-10-13T22:32:06.7171246Z Tuesday 13 October 2026  19:32:06 -0300 (0:00:00.078)       0:05:55.929 ******* 
2026-10-13T22:32:06.7508162Z [WARNING]: conditional statements should not include jinja2 templating
2026-10-13T22:32:06.7508885Z delimiters such as {{ }} or {% %}. Found: {{ lookup('env','HSM') |
2026-10-13T22:32:06.7509207Z default('false', true) | bool }}
2026-10-13T22:32:06.7599992Z Tuesday 13 October 2026  19:32:06 -0300 (0:00:00.043)       0:05:55.972 ******* 
2026-10-13T22:32:13.6687694Z 
2026-10-13T22:32:13.6688459Z RUNNING HANDLER [Restart Jboss] ************************************************
2026-10-13T22:32:13.6689136Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:32:13.6737436Z 
2026-10-13T22:32:13.6737846Z PLAY [jboss] *******************************************************************
2026-10-13T22:32:13.6785015Z 
2026-10-13T22:32:13.6785486Z PLAY [jboss] *******************************************************************
2026-10-13T22:32:13.6818426Z 
2026-10-13T22:32:13.6818710Z PLAY [jboss] *******************************************************************
2026-10-13T22:32:13.7125101Z Tuesday 13 October 2026  19:32:13 -0300 (0:00:06.952)       0:06:02.924 ******* 
2026-10-13T22:32:13.7684811Z 
2026-10-13T22:32:13.7685659Z TASK [Cria variável build_repository_name] *************************************
2026-10-13T22:32:13.7685829Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:32:13.7978753Z Tuesday 13 October 2026  19:32:13 -0300 (0:00:00.085)       0:06:03.010 ******* 
2026-10-13T22:32:13.8524787Z 
2026-10-13T22:32:13.8525277Z TASK [Buscando diretorio de config] ********************************************
2026-10-13T22:32:13.8525467Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:32:13.8852873Z Tuesday 13 October 2026  19:32:13 -0300 (0:00:00.087)       0:06:03.097 ******* 
2026-10-13T22:32:14.2121437Z 
2026-10-13T22:32:14.2122185Z TASK [Verifica se o arquivo {{ item }}/etc/hosts-{{ sistema_ambiente }} existe] ***
2026-10-13T22:32:14.2122485Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config)
2026-10-13T22:32:14.4707198Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12364/a/_SIEXC-web-aplicacao-config/so)
2026-10-13T22:32:14.5005512Z Tuesday 13 October 2026  19:32:14 -0300 (0:00:00.615)       0:06:03.712 ******* 
2026-10-13T22:32:14.5541402Z 
2026-10-13T22:32:14.5541892Z PLAY [jboss] *******************************************************************
2026-10-13T22:32:14.5861126Z Tuesday 13 October 2026  19:32:14 -0300 (0:00:00.085)       0:06:03.798 ******* 
2026-10-13T22:32:14.9715051Z 
2026-10-13T22:32:14.9715821Z TASK [Verifica se o arquivo /opt/jboss-eap/standalone/configuration/custom.sh existe] ***
2026-10-13T22:32:14.9716012Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:32:15.0029590Z Tuesday 13 October 2026  19:32:15 -0300 (0:00:00.416)       0:06:04.215 ******* 
2026-10-13T22:32:23.3726592Z 
2026-10-13T22:32:23.3727082Z TASK [Executa shell customizada (jboss_home)] **********************************
2026-10-13T22:32:23.3727256Z changed: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:32:23.4041584Z Tuesday 13 October 2026  19:32:23 -0300 (0:00:08.401)       0:06:12.616 ******* 
2026-10-13T22:32:23.8126823Z 
2026-10-13T22:32:23.8127391Z TASK [Verifica se o arquivo /opt/batch/config/configuration/custom.sh existe] ***
2026-10-13T22:32:23.8127635Z ok: [caddeapllx2193.agil.nprd.caixa.gov.br]
2026-10-13T22:32:23.8427844Z Tuesday 13 October 2026  19:32:23 -0300 (0:00:00.438)       0:06:13.054 ******* 
2026-10-13T22:32:23.8834454Z 
2026-10-13T22:32:23.8834936Z PLAY [local] *******************************************************************
2026-10-13T22:32:23.8858102Z [WARNING]: Could not match supplied host pattern, ignoring: instance_restart
2026-10-13T22:32:23.8860736Z 
2026-10-13T22:32:23.8861248Z PLAY [instance_restart] ********************************************************
2026-10-13T22:32:23.8861432Z skipping: no hosts matched
2026-10-13T22:32:23.8864133Z [WARNING]: Could not match supplied host pattern, ignoring: machine_reboot
2026-10-13T22:32:23.8867810Z 
2026-10-13T22:32:23.8868291Z PLAY [machine_reboot] **********************************************************
2026-10-13T22:32:23.8868426Z skipping: no hosts matched
2026-10-13T22:32:23.8877386Z 
2026-10-13T22:32:23.8877654Z PLAY [local] *******************************************************************
2026-10-13T22:32:23.8899738Z [WARNING]: Could not match supplied host pattern, ignoring: instance_stop
2026-10-13T22:32:23.8902511Z 
2026-10-13T22:32:23.8902847Z PLAY [instance_stop] ***********************************************************
2026-10-13T22:32:23.8903112Z skipping: no hosts matched
2026-10-13T22:32:23.8905867Z 
2026-10-13T22:32:23.8906067Z PLAY [machine_reboot] **********************************************************
2026-10-13T22:32:23.8906221Z skipping: no hosts matched
2026-10-13T22:32:23.8914949Z 
2026-10-13T22:32:23.8915221Z PLAY [local] *******************************************************************
2026-10-13T22:32:23.8936740Z [WARNING]: Could not match supplied host pattern, ignoring: escopo_execucao
2026-10-13T22:32:23.8938851Z 
2026-10-13T22:32:23.8939175Z PLAY [Executar o Start do Sirot Connector no escopo definido] ******************
2026-10-13T22:32:23.8939348Z skipping: no hosts matched
2026-10-13T22:32:23.8945055Z 
2026-10-13T22:32:23.8945278Z PLAY [local] *******************************************************************
2026-10-13T22:32:23.8971525Z 
2026-10-13T22:32:23.8971760Z PLAY [Executar o Stop do Sirot Connector] **************************************
2026-10-13T22:32:23.8971901Z skipping: no hosts matched
2026-10-13T22:32:23.8978479Z 
2026-10-13T22:32:23.8978856Z PLAY [Configura TSM] ***********************************************************
2026-10-13T22:32:23.9006443Z 
2026-10-13T22:32:23.9006993Z PLAY [jboss] *******************************************************************
2026-10-13T22:32:23.9036775Z 
2026-10-13T22:32:23.9037324Z PLAY [Configura Control-M] *****************************************************
2026-10-13T22:32:23.9077559Z 
2026-10-13T22:32:23.9077949Z PLAY [jboss] *******************************************************************
2026-10-13T22:32:23.9117730Z 
2026-10-13T22:32:23.9118077Z PLAY [jboss] *******************************************************************
2026-10-13T22:32:23.9158153Z 
2026-10-13T22:32:23.9158571Z PLAY [jboss] *******************************************************************
2026-10-13T22:32:23.9181661Z 
2026-10-13T22:32:23.9181900Z PLAY [jboss] *******************************************************************
2026-10-13T22:32:23.9209770Z 
2026-10-13T22:32:23.9210205Z PLAY [localhost] ***************************************************************
2026-10-13T22:32:23.9233553Z 
2026-10-13T22:32:23.9234011Z PLAY [jboss] *******************************************************************
2026-10-13T22:32:23.9275388Z 
2026-10-13T22:32:23.9275715Z PLAY [jboss] *******************************************************************
2026-10-13T22:32:23.9312602Z 
2026-10-13T22:32:23.9313040Z PLAY [jboss] *******************************************************************
2026-10-13T22:32:23.9347865Z 
2026-10-13T22:32:23.9348525Z PLAY RECAP *********************************************************************
2026-10-13T22:32:23.9348872Z caddeapllx2193.agil.nprd.caixa.gov.br : ok=276  changed=116  unreachable=0    failed=0    skipped=27   rescued=0    ignored=27  
2026-10-13T22:32:23.9349015Z 
2026-10-13T22:32:23.9350370Z Tuesday 13 October 2026  19:32:23 -0300 (0:00:00.092)       0:06:13.147 ******* 
2026-10-13T22:32:23.9350554Z =============================================================================== 
2026-10-13T22:32:23.9356200Z Copiando arquivos para jboss.server.config.dir ------------------------- 34.05s
2026-10-13T22:32:23.9356437Z nfs : execute montagem script ------------------------------------------ 18.74s
2026-10-13T22:32:23.9356658Z nfs : Networker | Restart networker ------------------------------------ 10.46s
2026-10-13T22:32:23.9356882Z nfs : Networker | Restart networker ------------------------------------ 10.45s
2026-10-13T22:32:23.9358221Z nfs : Networker | Restart networker ------------------------------------ 10.45s
2026-10-13T22:32:23.9358826Z nfs : Networker | Restart networker ------------------------------------ 10.45s
2026-10-13T22:32:23.9359128Z nfs : Networker | Restart networker ------------------------------------ 10.44s
2026-10-13T22:32:23.9359439Z nfs : Networker | Restart networker ------------------------------------ 10.44s
2026-10-13T22:32:23.9359713Z nfs : Networker | Restart networker ------------------------------------ 10.44s
2026-10-13T22:32:23.9360107Z nfs : Networker | Restart networker ------------------------------------ 10.44s
2026-10-13T22:32:23.9360360Z nfs : Networker | Restart networker ------------------------------------ 10.44s
2026-10-13T22:32:23.9360572Z nfs : Networker | Restart networker ------------------------------------ 10.44s
2026-10-13T22:32:23.9360779Z nfs : Networker | Restart networker ------------------------------------ 10.43s
2026-10-13T22:32:23.9360988Z nfs : Networker | Restart networker ------------------------------------ 10.43s
2026-10-13T22:32:23.9361198Z nfs : Networker | Restart networker ------------------------------------ 10.43s
2026-10-13T22:32:23.9361547Z nfs : Networker | Restart networker ------------------------------------ 10.42s
2026-10-13T22:32:23.9361760Z Executa shell customizada (jboss_home) ---------------------------------- 8.40s
2026-10-13T22:32:23.9362077Z Executando o jboss-custom.cli ------------------------------------------- 8.15s
2026-10-13T22:32:23.9362316Z Copiando artefatos (Modules) para o(s) servidor(es) Jboss --------------- 8.06s
2026-10-13T22:32:23.9362535Z Restart Jboss ----------------------------------------------------------- 6.95s
2026-10-13T22:32:23.9362682Z Playbook run took 0 days, 0 hours, 6 minutes, 13 seconds
2026-10-13T22:32:24.0113676Z ##[debug]Exit code 0 received from tool '/bin/bash'
2026-10-13T22:32:24.0114029Z ##[debug]STDIO streams have closed for tool '/bin/bash'
2026-10-13T22:32:24.0114286Z ##[debug]task result: Succeeded
2026-10-13T22:32:24.0117282Z ##[debug]Processed: ##vso[task.complete result=Succeeded;done=true;]
2026-10-13T22:32:24.0137404Z ##[section]Finishing: Deploy Config no JBOSS


[p585600@caddeapllx2193 ~]$
[p585600@caddeapllx2193 ~]$ df -h -T
Sist. Arq.                                                     Tipo      Tam. Usado Disp. Uso% Montado em
devtmpfs                                                       devtmpfs  4,0M     0  4,0M   0% /dev
tmpfs                                                          tmpfs     1,8G     0  1,8G   0% /dev/shm
tmpfs                                                          tmpfs     730M   11M  719M   2% /run
/dev/mapper/VG_PRINCIPAL-LV_BARRA                              xfs       9,0G  2,7G  6,3G  30% /
/dev/mapper/VG_PRINCIPAL-LV_LOGS                               xfs       2,0G   99M  1,9G   5% /logs
/dev/mapper/VG_PRINCIPAL-LV_VAR                                xfs       5,0G  917M  4,1G  19% /var
/dev/mapper/VG_PRINCIPAL-LV_OPT                                xfs        10G  2,2G  7,9G  22% /opt
/dev/mapper/VG_PRINCIPAL-LV_TMP                                xfs       960M   57M  904M   6% /tmp
/dev/sda1                                                      xfs       960M  224M  737M  24% /boot
tmpfs                                                          tmpfs     365M  4,0K  365M   1% /run/user/20003846
192.168.227.59:/export/sicql_bovespa                           nfs4       97M  5,3M   92M   6% /producao
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC nfs4      5,0G 1022M  4,1G  20% /siexc_incoming
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIAPC   nfs4       16G   41M   16G   1% /SIAPC
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTISP/SIISF nfs4      7,0G  5,1G  1,9G  73% /integracoes/SIISF
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC nfs4      5,0G 1022M  4,1G  20% /legado
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC nfs4      5,0G 1022M  4,1G  20% /SIGPL
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC nfs4      5,0G 1022M  4,1G  20% /siexc
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC nfs4      5,0G 1022M  4,1G  20% /eFinanceira_ctc/siexc
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/SIEXC nfs4      5,0G 1022M  4,1G  20% /suporte
tmpfs                                                          tmpfs     365M  4,0K  365M   1% /run/user/10585600
[p585600@caddeapllx2193 ~]$



