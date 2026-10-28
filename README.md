2026-10-28T17:32:47.8040637Z ##[section]Starting: Deploy Config no JBOSS
2026-10-28T17:32:47.8043539Z ==============================================================================
2026-10-28T17:32:47.8043624Z Task         : Bash
2026-10-28T17:32:47.8043666Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-28T17:32:47.8043727Z Version      : 3.227.0
2026-10-28T17:32:47.8043780Z Author       : Microsoft Corporation
2026-10-28T17:32:47.8043830Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-28T17:32:47.8043899Z ==============================================================================
2026-10-28T17:32:48.7023687Z Generating script.
2026-10-28T17:32:48.7031531Z ========================== Starting Command Output ===========================
2026-10-28T17:32:48.7042267Z [command]/bin/bash /opt/ads-agent/_work/_temp/7feb0b15-839c-473a-ba69-bd89611a4050.sh
2026-10-28T17:32:48.7108268Z /opt/ads-agent/_work/_temp/7feb0b15-839c-473a-ba69-bd89611a4050.sh: line 2: quantidade_vm: comando não encontrado
2026-10-28T17:32:48.7119012Z /opt/ads-agent/_work/_temp/7feb0b15-839c-473a-ba69-bd89611a4050.sh: line 2: USE_WMQ: comando não encontrado
2026-10-28T17:32:50.7612232Z 
2026-10-28T17:32:50.7612728Z PLAY [local] *******************************************************************
2026-10-28T17:32:50.7886693Z 
2026-10-28T17:32:50.7887429Z PLAY [Configurando o DNS] ******************************************************
2026-10-28T17:32:50.9640724Z 
2026-10-28T17:32:50.9641220Z PLAY [local] *******************************************************************
2026-10-28T17:32:50.9671371Z 
2026-10-28T17:32:50.9671908Z PLAY [Verificando serviços] ****************************************************
2026-10-28T17:32:50.9753077Z 
2026-10-28T17:32:50.9753788Z PLAY [Configuração LDAP] *******************************************************
2026-10-28T17:32:50.9784590Z [WARNING]: Found variable using reserved name: when
2026-10-28T17:32:50.9789096Z 
2026-10-28T17:32:50.9789365Z PLAY [jboss] *******************************************************************
2026-10-28T17:32:50.9872666Z 
2026-10-28T17:32:50.9873400Z PLAY [Stack Jboss] *************************************************************
2026-10-28T17:32:51.0098047Z Wednesday 28 October 2026  14:32:51 -0300 (0:00:00.307)       0:00:00.307 ***** 
2026-10-28T17:32:51.5194286Z 
2026-10-28T17:32:51.5195007Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-10-28T17:32:51.5196634Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-28T17:32:51.5196878Z caddeapllx2651.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-28T17:32:51.5197068Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-28T17:32:51.5197248Z releases. A future Ansible release will default to using the discovered 
2026-10-28T17:32:51.5197413Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-28T17:32:51.5197581Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-28T17:32:51.5197751Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-28T17:32:51.5197903Z setting deprecation_warnings=False in ansible.cfg.
2026-10-28T17:32:51.5198041Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:32:51.5217645Z 
2026-10-28T17:32:51.5217877Z PLAY [jboss] *******************************************************************
2026-10-28T17:32:51.5279544Z Wednesday 28 October 2026  14:32:51 -0300 (0:00:00.518)       0:00:00.825 ***** 
2026-10-28T17:32:51.8276428Z 
2026-10-28T17:32:51.8276887Z TASK [Verifica se o arquivo nfs_config.json existe] ****************************
2026-10-28T17:32:51.8277223Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:32:51.8304820Z Wednesday 28 October 2026  14:32:51 -0300 (0:00:00.302)       0:00:01.128 ***** 
2026-10-28T17:32:51.8734670Z included: /opt/ads-agent/_work/r6179/a/esteira-jboss-vm-v2/roles/nfs/tasks/get_nfs.yml for caddeapllx2651.agil.nprd.caixa.gov.br
2026-10-28T17:32:51.8773694Z Wednesday 28 October 2026  14:32:51 -0300 (0:00:00.047)       0:00:01.175 ***** 
2026-10-28T17:32:51.9313553Z 
2026-10-28T17:32:51.9314135Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-28T17:32:51.9314310Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:32:51.9350788Z Wednesday 28 October 2026  14:32:51 -0300 (0:00:00.057)       0:00:01.233 ***** 
2026-10-28T17:32:52.3321271Z 
2026-10-28T17:32:52.3322209Z TASK [nfs : Coletar variáveis de ambiente] *************************************
2026-10-28T17:32:52.3322593Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:32:52.3347961Z Wednesday 28 October 2026  14:32:52 -0300 (0:00:00.399)       0:00:01.632 ***** 
2026-10-28T17:32:52.3889135Z 
2026-10-28T17:32:52.3889838Z TASK [nfs : Exibir resultado em JSON] ******************************************
2026-10-28T17:32:52.3890448Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:32:52.3891055Z     "nfs_vars_json": {
2026-10-28T17:32:52.3891252Z         "changed": false, 
2026-10-28T17:32:52.3891561Z         "cmd": "cat /opt/ads-agent/_work/r6179/a/nfs_config.json", 
2026-10-28T17:32:52.3891723Z         "delta": "0:00:00.002867", 
2026-10-28T17:32:52.3891928Z         "end": "2026-10-28 14:32:52.318829", 
2026-10-28T17:32:52.3892053Z         "failed": false, 
2026-10-28T17:32:52.3892152Z         "rc": 0, 
2026-10-28T17:32:52.3892323Z         "start": "2026-10-28 14:32:52.315962", 
2026-10-28T17:32:52.3892445Z         "stderr": "", 
2026-10-28T17:32:52.3892554Z         "stderr_lines": [], 
2026-10-28T17:32:52.3892705Z         "stdout": "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]", 
2026-10-28T17:32:52.3892865Z         "stdout_lines": [
2026-10-28T17:32:52.3893007Z             "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]"
2026-10-28T17:32:52.3893135Z         ]
2026-10-28T17:32:52.3893229Z     }
2026-10-28T17:32:52.3893321Z }
2026-10-28T17:32:52.3920692Z Wednesday 28 October 2026  14:32:52 -0300 (0:00:00.057)       0:00:01.690 ***** 
2026-10-28T17:32:52.4494903Z 
2026-10-28T17:32:52.4495445Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-28T17:32:52.4495620Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:32:52.4532670Z Wednesday 28 October 2026  14:32:52 -0300 (0:00:00.061)       0:00:01.751 ***** 
2026-10-28T17:32:53.0334086Z 
2026-10-28T17:32:53.0334704Z TASK [nfs : execute montagem script] *******************************************
2026-10-28T17:32:53.0334877Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:32:53.0360946Z Wednesday 28 October 2026  14:32:53 -0300 (0:00:00.582)       0:00:02.334 ***** 
2026-10-28T17:32:53.0926553Z 
2026-10-28T17:32:53.0926987Z TASK [nfs : ansible.builtin.debug] *********************************************
2026-10-28T17:32:53.0928462Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:32:53.0928594Z     "changed": false, 
2026-10-28T17:32:53.0928735Z     "msg": {
2026-10-28T17:32:53.0928849Z         "changed": true, 
2026-10-28T17:32:53.0928972Z         "cmd": [
2026-10-28T17:32:53.0929077Z             "python", 
2026-10-28T17:32:53.0929385Z             "/opt/ads-agent/_work/r6179/a/esteira-jboss-vm-v2/roles/nfs/files/nfs.py", 
2026-10-28T17:32:53.0929534Z             "montagem", 
2026-10-28T17:32:53.0929677Z             "siccp-intra", 
2026-10-28T17:32:53.0929780Z             "des", 
2026-10-28T17:32:53.0929883Z             "ctc_nprd", 
2026-10-28T17:32:53.0930061Z             "/opt/ads-agent/_work/r6179/a/esteira-jboss-vm-v2", 
2026-10-28T17:32:53.0930543Z             "C&t@d02", 
2026-10-28T17:32:53.0930730Z             "***", 
2026-10-28T17:32:53.0930844Z             "s736651@corp.caixa.gov.br", 
2026-10-28T17:32:53.0930964Z             "***", 
2026-10-28T17:32:53.0931105Z             "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]"
2026-10-28T17:32:53.0931241Z         ], 
2026-10-28T17:32:53.0931433Z         "delta": "0:00:00.284929", 
2026-10-28T17:32:53.0931619Z         "end": "2026-10-28 14:32:53.019185", 
2026-10-28T17:32:53.0931745Z         "failed": false, 
2026-10-28T17:32:53.0931850Z         "rc": 0, 
2026-10-28T17:32:53.0932017Z         "start": "2026-10-28 14:32:52.734256", 
2026-10-28T17:32:53.0932136Z         "stderr": "", 
2026-10-28T17:32:53.0932243Z         "stderr_lines": [], 
2026-10-28T17:32:53.0933332Z         "stdout": "[{u'NFS_MOUNT_POINT_VM': u'/siccp', u'NFS_ENDPOINT_VM': u'hypernprd12.ad.caixa:/fs_siccp'}]\nNome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           \n------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------\nhypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                                \nnfs_path=/siccp\nnfs_src=hypernprd12.ad.caixa:/fs_siccp\nhypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                                ", 
2026-10-28T17:32:53.0933750Z         "stdout_lines": [
2026-10-28T17:32:53.0933977Z             "[{u'NFS_MOUNT_POINT_VM': u'/siccp', u'NFS_ENDPOINT_VM': u'hypernprd12.ad.caixa:/fs_siccp'}]", 
2026-10-28T17:32:53.0934143Z             "Nome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           ", 
2026-10-28T17:32:53.0934514Z             "------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------", 
2026-10-28T17:32:53.0934739Z             "hypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                                ", 
2026-10-28T17:32:53.0934882Z             "nfs_path=/siccp", 
2026-10-28T17:32:53.0935004Z             "nfs_src=hypernprd12.ad.caixa:/fs_siccp", 
2026-10-28T17:32:53.0935157Z             "hypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                                "
2026-10-28T17:32:53.0935289Z         ]
2026-10-28T17:32:53.0935372Z     }
2026-10-28T17:32:53.0935465Z }
2026-10-28T17:32:53.0953683Z Wednesday 28 October 2026  14:32:53 -0300 (0:00:00.059)       0:00:02.393 ***** 
2026-10-28T17:32:53.3466935Z 
2026-10-28T17:32:53.3467443Z TASK [nfs : execute clean json] ************************************************
2026-10-28T17:32:53.3467618Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:32:53.3491368Z Wednesday 28 October 2026  14:32:53 -0300 (0:00:00.253)       0:00:02.647 ***** 
2026-10-28T17:32:53.4162227Z 
2026-10-28T17:32:53.4162642Z TASK [nfs : result_new_string_json] ********************************************
2026-10-28T17:32:53.4163916Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:32:53.4164317Z     "msg": {
2026-10-28T17:32:53.4164715Z         "changed": true, 
2026-10-28T17:32:53.4165301Z         "cmd": "echo '[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]' | sed 's/NFS_ENDPOINT_ISILON[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_ISILON[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_HUAWEI[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_HUAWEI[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_VM[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_VM[^\"]*/NFS_MOUNT_POINT/g'", 
2026-10-28T17:32:53.4165694Z         "delta": "0:00:00.003788", 
2026-10-28T17:32:53.4165898Z         "end": "2026-10-28 14:32:53.331538", 
2026-10-28T17:32:53.4166024Z         "failed": false, 
2026-10-28T17:32:53.4166130Z         "rc": 0, 
2026-10-28T17:32:53.4166304Z         "start": "2026-10-28 14:32:53.327750", 
2026-10-28T17:32:53.4166430Z         "stderr": "", 
2026-10-28T17:32:53.4166539Z         "stderr_lines": [], 
2026-10-28T17:32:53.4166690Z         "stdout": "[{\"NFS_ENDPOINT\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT\": \"/siccp\"}]", 
2026-10-28T17:32:53.4166839Z         "stdout_lines": [
2026-10-28T17:32:53.4166978Z             "[{\"NFS_ENDPOINT\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT\": \"/siccp\"}]"
2026-10-28T17:32:53.4167105Z         ]
2026-10-28T17:32:53.4167199Z     }
2026-10-28T17:32:53.4167285Z }
2026-10-28T17:32:53.4187626Z Wednesday 28 October 2026  14:32:53 -0300 (0:00:00.069)       0:00:02.716 ***** 
2026-10-28T17:32:53.4740030Z 
2026-10-28T17:32:53.4740578Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-28T17:32:53.4740745Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:32:53.4761648Z Wednesday 28 October 2026  14:32:53 -0300 (0:00:00.057)       0:00:02.774 ***** 
2026-10-28T17:32:53.5308074Z 
2026-10-28T17:32:53.5308899Z TASK [nfs : result_new_json] ***************************************************
2026-10-28T17:32:53.5309140Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:32:53.5309269Z     "msg": [
2026-10-28T17:32:53.5309383Z         {
2026-10-28T17:32:53.5309544Z             "NFS_ENDPOINT": "hypernprd12.ad.caixa:/fs_siccp", 
2026-10-28T17:32:53.5309687Z             "NFS_MOUNT_POINT": "/siccp"
2026-10-28T17:32:53.5309836Z         }
2026-10-28T17:32:53.5309927Z     ]
2026-10-28T17:32:53.5310011Z }
2026-10-28T17:32:53.5330309Z Wednesday 28 October 2026  14:32:53 -0300 (0:00:00.056)       0:00:02.831 ***** 
2026-10-28T17:32:53.5898211Z included: /opt/ads-agent/_work/r6179/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2651.agil.nprd.caixa.gov.br
2026-10-28T17:32:53.5950498Z Wednesday 28 October 2026  14:32:53 -0300 (0:00:00.061)       0:00:02.892 ***** 
2026-10-28T17:32:53.6468881Z 
2026-10-28T17:32:53.6469329Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-28T17:32:53.6469511Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:32:53.6490551Z Wednesday 28 October 2026  14:32:53 -0300 (0:00:00.054)       0:00:02.947 ***** 
2026-10-28T17:32:53.7013241Z 
2026-10-28T17:32:53.7013648Z TASK [nfs : debug] *************************************************************
2026-10-28T17:32:53.7015141Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:32:53.7015286Z     "msg": {
2026-10-28T17:32:53.7015412Z         "NFS_ENDPOINT": "hypernprd12.ad.caixa:/fs_siccp", 
2026-10-28T17:32:53.7015547Z         "NFS_MOUNT_POINT": "/siccp"
2026-10-28T17:32:53.7015650Z     }
2026-10-28T17:32:53.7015756Z }
2026-10-28T17:32:53.7037153Z Wednesday 28 October 2026  14:32:53 -0300 (0:00:00.054)       0:00:03.001 ***** 
2026-10-28T17:32:53.7559207Z 
2026-10-28T17:32:53.7559950Z TASK [nfs : debug] *************************************************************
2026-10-28T17:32:53.7560305Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:32:53.7560445Z     "msg": "/siccp"
2026-10-28T17:32:53.7560545Z }
2026-10-28T17:32:53.7584188Z Wednesday 28 October 2026  14:32:53 -0300 (0:00:00.054)       0:00:03.056 ***** 
2026-10-28T17:32:53.8098525Z 
2026-10-28T17:32:53.8098981Z TASK [nfs : debug] *************************************************************
2026-10-28T17:32:53.8099428Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:32:53.8099569Z     "msg": "hypernprd12.ad.caixa:/fs_siccp"
2026-10-28T17:32:53.8099680Z }
2026-10-28T17:32:53.8126505Z Wednesday 28 October 2026  14:32:53 -0300 (0:00:00.054)       0:00:03.110 ***** 
2026-10-28T17:32:53.8678330Z 
2026-10-28T17:32:53.8678721Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-28T17:32:53.8679557Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:32:53.8679696Z     "changed": false, 
2026-10-28T17:32:53.8679847Z     "msg": "All assertions passed"
2026-10-28T17:32:53.8679998Z }
2026-10-28T17:32:53.8704912Z Wednesday 28 October 2026  14:32:53 -0300 (0:00:00.057)       0:00:03.168 ***** 
2026-10-28T17:32:57.3220400Z 
2026-10-28T17:32:57.3220900Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-28T17:32:57.3221066Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:32:57.3248908Z Wednesday 28 October 2026  14:32:57 -0300 (0:00:03.454)       0:00:06.622 ***** 
2026-10-28T17:32:58.2814785Z 
2026-10-28T17:32:58.2815691Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-28T17:32:58.2815915Z [WARNING]: Consider using the yum, dnf or zypper module rather than running
2026-10-28T17:32:58.2816274Z 'rpm'.  If you need to use command because yum, dnf or zypper is insufficient
2026-10-28T17:32:58.2816497Z you can add 'warn: false' to this command task or set 'command_warnings=False'
2026-10-28T17:32:58.2816645Z in ansible.cfg to get rid of this message.
2026-10-28T17:32:58.2819109Z fatal: [caddeapllx2651.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.711653", "end": "2026-10-28 14:32:58.266739", "msg": "non-zero return code", "rc": 1, "start": "2026-10-28 14:32:57.555086", "stderr": "aviso: /var/tmp/rpm-tmp.aqloec: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.aqloec: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-28T17:32:58.2819704Z ...ignoring
2026-10-28T17:32:58.2845704Z Wednesday 28 October 2026  14:32:58 -0300 (0:00:00.959)       0:00:07.582 ***** 
2026-10-28T17:32:59.0883644Z 
2026-10-28T17:32:59.0884146Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-28T17:32:59.0888016Z fatal: [caddeapllx2651.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.559718", "end": "2026-10-28 14:32:59.073425", "msg": "non-zero return code", "rc": 1, "start": "2026-10-28 14:32:58.513707", "stderr": "aviso: /var/tmp/rpm-tmp.fblxUD: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.fblxUD: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-28T17:32:59.0888954Z ...ignoring
2026-10-28T17:32:59.0914447Z Wednesday 28 October 2026  14:32:59 -0300 (0:00:00.806)       0:00:08.389 ***** 
2026-10-28T17:32:59.4921570Z 
2026-10-28T17:32:59.4922284Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-28T17:32:59.4922458Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:32:59.4950537Z Wednesday 28 October 2026  14:32:59 -0300 (0:00:00.403)       0:00:08.793 ***** 
2026-10-28T17:32:59.7430097Z 
2026-10-28T17:32:59.7431092Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-28T17:32:59.7431288Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:32:59.7459215Z Wednesday 28 October 2026  14:32:59 -0300 (0:00:00.250)       0:00:09.043 ***** 
2026-10-28T17:33:00.6411569Z 
2026-10-28T17:33:00.6412223Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-28T17:33:00.6412390Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:00.6449154Z Wednesday 28 October 2026  14:33:00 -0300 (0:00:00.898)       0:00:09.942 ***** 
2026-10-28T17:33:00.9635488Z 
2026-10-28T17:33:00.9635903Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-28T17:33:00.9636072Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:00.9662743Z Wednesday 28 October 2026  14:33:00 -0300 (0:00:00.321)       0:00:10.264 ***** 
2026-10-28T17:33:11.4194562Z 
2026-10-28T17:33:11.4195097Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-28T17:33:11.4195269Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:11.4219055Z Wednesday 28 October 2026  14:33:11 -0300 (0:00:10.455)       0:00:20.719 ***** 
2026-10-28T17:33:11.8177405Z 
2026-10-28T17:33:11.8177941Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-28T17:33:11.8178105Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:11.8204324Z Wednesday 28 October 2026  14:33:11 -0300 (0:00:00.398)       0:00:21.118 ***** 
2026-10-28T17:33:11.8600724Z 
2026-10-28T17:33:11.8600962Z PLAY [jboss] *******************************************************************
2026-10-28T17:33:11.8640444Z 
2026-10-28T17:33:11.8640612Z PLAY [jboss] *******************************************************************
2026-10-28T17:33:11.8671982Z Wednesday 28 October 2026  14:33:11 -0300 (0:00:00.046)       0:00:21.165 ***** 
2026-10-28T17:33:12.4917905Z 
2026-10-28T17:33:12.4918490Z TASK [Gathering Facts] *********************************************************
2026-10-28T17:33:12.4918659Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:12.5117164Z Wednesday 28 October 2026  14:33:12 -0300 (0:00:00.644)       0:00:21.809 ***** 
2026-10-28T17:33:13.9467711Z 
2026-10-28T17:33:13.9468239Z TASK [Gerando fatos de servicos] ***********************************************
2026-10-28T17:33:13.9814449Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:13.9814890Z Wednesday 28 October 2026  14:33:13 -0300 (0:00:01.469)       0:00:23.279 ***** 
2026-10-28T17:33:14.0392978Z 
2026-10-28T17:33:14.0393419Z TASK [Gerando lista de units jboss] ********************************************
2026-10-28T17:33:14.0393581Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:14.0658477Z Wednesday 28 October 2026  14:33:14 -0300 (0:00:00.084)       0:00:23.363 ***** 
2026-10-28T17:33:14.1295124Z Wednesday 28 October 2026  14:33:14 -0300 (0:00:00.063)       0:00:23.427 ***** 
2026-10-28T17:33:14.1392362Z 
2026-10-28T17:33:14.1392952Z PLAY [Copiando deployments adicionais] *****************************************
2026-10-28T17:33:14.1669733Z Wednesday 28 October 2026  14:33:14 -0300 (0:00:00.037)       0:00:23.464 ***** 
2026-10-28T17:33:14.2193393Z 
2026-10-28T17:33:14.2194144Z TASK [Cria variável build_repository_name] *************************************
2026-10-28T17:33:14.2194373Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:14.2462228Z Wednesday 28 October 2026  14:33:14 -0300 (0:00:00.079)       0:00:23.544 ***** 
2026-10-28T17:33:14.2988661Z 
2026-10-28T17:33:14.2989416Z TASK [Buscando diretorio de config] ********************************************
2026-10-28T17:33:14.2989656Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:14.3256176Z Wednesday 28 October 2026  14:33:14 -0300 (0:00:00.079)       0:00:23.623 ***** 
2026-10-28T17:33:14.3774276Z 
2026-10-28T17:33:14.3774720Z TASK [Buscando diretorio de config] ********************************************
2026-10-28T17:33:14.3774894Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:14.4096594Z Wednesday 28 October 2026  14:33:14 -0300 (0:00:00.083)       0:00:23.707 ***** 
2026-10-28T17:33:14.8730444Z 
2026-10-28T17:33:14.8730967Z TASK [Create a symbolic link] **************************************************
2026-10-28T17:33:14.8731383Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config)
2026-10-28T17:33:15.1273134Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss)
2026-10-28T17:33:15.1584156Z Wednesday 28 October 2026  14:33:15 -0300 (0:00:00.748)       0:00:24.456 ***** 
2026-10-28T17:33:15.4462949Z 
2026-10-28T17:33:15.4463471Z TASK [Verifica se o arquivo  existe] *******************************************
2026-10-28T17:33:15.4463876Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config)
2026-10-28T17:33:15.7032282Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss)
2026-10-28T17:33:15.7341354Z Wednesday 28 October 2026  14:33:15 -0300 (0:00:00.575)       0:00:25.032 ***** 
2026-10-28T17:33:15.8186155Z included: /opt/ads-agent/_work/r6179/a/esteira-jboss-vm-v2/roles/jboss/tasks/stack_deployments_custom_block.yml for caddeapllx2651.agil.nprd.caixa.gov.br
2026-10-28T17:33:15.8471646Z Wednesday 28 October 2026  14:33:15 -0300 (0:00:00.113)       0:00:25.145 ***** 
2026-10-28T17:33:16.2705571Z 
2026-10-28T17:33:16.2706231Z TASK [Lendo artefatos do arquivo CSV] ******************************************
2026-10-28T17:33:16.2706513Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:16.3032189Z Wednesday 28 October 2026  14:33:16 -0300 (0:00:00.455)       0:00:25.600 ***** 
2026-10-28T17:33:16.3104536Z [WARNING]: The loop variable 'item' is already in use. You should set the
2026-10-28T17:33:16.3104773Z `loop_var` value in the `loop_control` option for the task to something else to
2026-10-28T17:33:16.3104936Z avoid variable collisions and unexpected behavior.
2026-10-28T17:33:16.3472476Z 
2026-10-28T17:33:16.3472891Z TASK [Mostra artefatos] ********************************************************
2026-10-28T17:33:16.3473323Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item={u'version': u'0.0.0', u'group_id': u'com.ibm.mq', u'extension': u'rar', u'artifact_id': u'wmq.jmsra'}) => {
2026-10-28T17:33:16.3473566Z     "msg": "Artefato: wmq.jmsra - versao 0.0.0"
2026-10-28T17:33:16.3473682Z }
2026-10-28T17:33:16.3776396Z Wednesday 28 October 2026  14:33:16 -0300 (0:00:00.074)       0:00:25.675 ***** 
2026-10-28T17:33:16.9436004Z 
2026-10-28T17:33:16.9436540Z TASK [maven_artifact] **********************************************************
2026-10-28T17:33:16.9436991Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item={u'version': u'0.0.0', u'group_id': u'com.ibm.mq', u'extension': u'rar', u'artifact_id': u'wmq.jmsra'})
2026-10-28T17:33:16.9721159Z Wednesday 28 October 2026  14:33:16 -0300 (0:00:00.594)       0:00:26.270 ***** 
2026-10-28T17:33:17.5429463Z 
2026-10-28T17:33:17.5430007Z TASK [Copiando artefatos para o(s) servidor(es) Jboss] *************************
2026-10-28T17:33:17.5430609Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:17.5705424Z Wednesday 28 October 2026  14:33:17 -0300 (0:00:00.598)       0:00:26.868 ***** 
2026-10-28T17:33:17.6097859Z 
2026-10-28T17:33:17.6098305Z PLAY [Copiando modules adicionais] *********************************************
2026-10-28T17:33:17.6379454Z Wednesday 28 October 2026  14:33:17 -0300 (0:00:00.067)       0:00:26.935 ***** 
2026-10-28T17:33:17.6906160Z 
2026-10-28T17:33:17.6906821Z TASK [Cria variável build_repository_name] *************************************
2026-10-28T17:33:17.6907002Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:17.7190723Z Wednesday 28 October 2026  14:33:17 -0300 (0:00:00.080)       0:00:27.016 ***** 
2026-10-28T17:33:17.7728363Z 
2026-10-28T17:33:17.7728824Z TASK [Buscando diretorio de config] ********************************************
2026-10-28T17:33:17.7729135Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:17.8002516Z Wednesday 28 October 2026  14:33:17 -0300 (0:00:00.081)       0:00:27.097 ***** 
2026-10-28T17:33:17.8516147Z 
2026-10-28T17:33:17.8516560Z TASK [Buscando diretorio de config] ********************************************
2026-10-28T17:33:17.8516751Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:17.8822912Z Wednesday 28 October 2026  14:33:17 -0300 (0:00:00.082)       0:00:27.180 ***** 
2026-10-28T17:33:18.1751138Z 
2026-10-28T17:33:18.1751664Z TASK [Create a directory] ******************************************************
2026-10-28T17:33:18.1752070Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config)
2026-10-28T17:33:18.4258668Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss)
2026-10-28T17:33:18.4570681Z Wednesday 28 October 2026  14:33:18 -0300 (0:00:00.574)       0:00:27.754 ***** 
2026-10-28T17:33:18.7434688Z 
2026-10-28T17:33:18.7435192Z TASK [Verifica se o arquivo  existe] *******************************************
2026-10-28T17:33:18.7435602Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config)
2026-10-28T17:33:19.0100636Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss)
2026-10-28T17:33:19.0395498Z Wednesday 28 October 2026  14:33:19 -0300 (0:00:00.582)       0:00:28.337 ***** 
2026-10-28T17:33:19.1349177Z included: /opt/ads-agent/_work/r6179/a/esteira-jboss-vm-v2/roles/jboss/tasks/stack_modules_custom_block.yml for caddeapllx2651.agil.nprd.caixa.gov.br
2026-10-28T17:33:19.1649052Z Wednesday 28 October 2026  14:33:19 -0300 (0:00:00.125)       0:00:28.462 ***** 
2026-10-28T17:33:19.4575041Z 
2026-10-28T17:33:19.4575587Z TASK [Lendo artefatos do arquivo CSV] ******************************************
2026-10-28T17:33:19.4575760Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:19.4856771Z Wednesday 28 October 2026  14:33:19 -0300 (0:00:00.320)       0:00:28.783 ***** 
2026-10-28T17:33:19.5225695Z Wednesday 28 October 2026  14:33:19 -0300 (0:00:00.036)       0:00:28.820 ***** 
2026-10-28T17:33:19.8788149Z 
2026-10-28T17:33:19.8788879Z TASK [Listar arquivos no diretório baixados anteriormente] *********************
2026-10-28T17:33:19.8789060Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:19.9082611Z Wednesday 28 October 2026  14:33:19 -0300 (0:00:00.385)       0:00:29.205 ***** 
2026-10-28T17:33:19.9462048Z Wednesday 28 October 2026  14:33:19 -0300 (0:00:00.038)       0:00:29.244 ***** 
2026-10-28T17:33:20.2598065Z 
2026-10-28T17:33:20.2598726Z TASK [Verifica se o arquivo jboss-modules-custom tem conteudo] *****************
2026-10-28T17:33:20.2598914Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:20.2875893Z Wednesday 28 October 2026  14:33:20 -0300 (0:00:00.341)       0:00:29.585 ***** 
2026-10-28T17:33:20.4607551Z 
2026-10-28T17:33:20.4608080Z TASK [Copiando artefatos (Modules) para o(s) servidor(es) Jboss] ***************
2026-10-28T17:33:20.4608505Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:20.4885201Z Wednesday 28 October 2026  14:33:20 -0300 (0:00:00.200)       0:00:29.786 ***** 
2026-10-28T17:33:21.0392600Z 
2026-10-28T17:33:21.0393290Z TASK [Copiando artefato (jboss-custom.cli) para o(s) servidor(es) Jboss] *******
2026-10-28T17:33:21.0393467Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:21.0662113Z Wednesday 28 October 2026  14:33:21 -0300 (0:00:00.577)       0:00:30.364 ***** 
2026-10-28T17:33:21.1353609Z Wednesday 28 October 2026  14:33:21 -0300 (0:00:00.069)       0:00:30.433 ***** 
2026-10-28T17:33:21.2020381Z Wednesday 28 October 2026  14:33:21 -0300 (0:00:00.066)       0:00:30.499 ***** 
2026-10-28T17:33:21.2671236Z Wednesday 28 October 2026  14:33:21 -0300 (0:00:00.065)       0:00:30.564 ***** 
2026-10-28T17:33:21.3316755Z Wednesday 28 October 2026  14:33:21 -0300 (0:00:00.064)       0:00:30.629 ***** 
2026-10-28T17:33:21.3979614Z Wednesday 28 October 2026  14:33:21 -0300 (0:00:00.066)       0:00:30.695 ***** 
2026-10-28T17:33:21.4513109Z 
2026-10-28T17:33:21.4513569Z TASK [Sem modules adicionais] **************************************************
2026-10-28T17:33:21.4514684Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:33:21.4515927Z     "msg": "Sem modules adicional"
2026-10-28T17:33:21.4517047Z }
2026-10-28T17:33:21.4531767Z 
2026-10-28T17:33:21.4533083Z PLAY [jboss] *******************************************************************
2026-10-28T17:33:21.4819179Z Wednesday 28 October 2026  14:33:21 -0300 (0:00:00.084)       0:00:30.779 ***** 
2026-10-28T17:33:21.5406827Z 
2026-10-28T17:33:21.5407891Z TASK [Setando a versão do Jboss] ***********************************************
2026-10-28T17:33:21.5408300Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:21.5676661Z Wednesday 28 October 2026  14:33:21 -0300 (0:00:00.085)       0:00:30.865 ***** 
2026-10-28T17:33:21.6407707Z 
2026-10-28T17:33:21.6408554Z TASK [Cria variável build_repository_name_tfs] *********************************
2026-10-28T17:33:21.6409016Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:21.6677359Z Wednesday 28 October 2026  14:33:21 -0300 (0:00:00.100)       0:00:30.965 ***** 
2026-10-28T17:33:21.7398000Z 
2026-10-28T17:33:21.7398446Z TASK [Buscando diretorio de config] ********************************************
2026-10-28T17:33:21.7398617Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:21.7686380Z Wednesday 28 October 2026  14:33:21 -0300 (0:00:00.100)       0:00:31.066 ***** 
2026-10-28T17:33:22.3558663Z 
2026-10-28T17:33:22.3559241Z TASK [Copy common_start.sh] ****************************************************
2026-10-28T17:33:22.3559407Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:22.3838642Z Wednesday 28 October 2026  14:33:22 -0300 (0:00:00.615)       0:00:31.681 ***** 
2026-10-28T17:33:22.9465015Z 
2026-10-28T17:33:22.9465531Z TASK [Copy template script] ****************************************************
2026-10-28T17:33:22.9465701Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:22.9741916Z Wednesday 28 October 2026  14:33:22 -0300 (0:00:00.590)       0:00:32.272 ***** 
2026-10-28T17:33:23.5353306Z 
2026-10-28T17:33:23.5353816Z TASK [JBoss systemd wrapper for sysvinit script mode domain] *******************
2026-10-28T17:33:23.5353987Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:23.5631919Z Wednesday 28 October 2026  14:33:23 -0300 (0:00:00.588)       0:00:32.860 ***** 
2026-10-28T17:33:24.3003159Z 
2026-10-28T17:33:24.3003668Z TASK [Realiza copia do arquivo de Trust Store] *********************************
2026-10-28T17:33:24.3003836Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:24.3274369Z Wednesday 28 October 2026  14:33:24 -0300 (0:00:00.764)       0:00:33.625 ***** 
2026-10-28T17:33:24.3947489Z Wednesday 28 October 2026  14:33:24 -0300 (0:00:00.067)       0:00:33.692 ***** 
2026-10-28T17:33:24.4758024Z Wednesday 28 October 2026  14:33:24 -0300 (0:00:00.081)       0:00:33.773 ***** 
2026-10-28T17:33:24.7811009Z 
2026-10-28T17:33:24.7811523Z TASK [Check directory configuration exists] ************************************
2026-10-28T17:33:24.7811931Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config)
2026-10-28T17:33:25.0388876Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss)
2026-10-28T17:33:25.0674710Z Wednesday 28 October 2026  14:33:25 -0300 (0:00:00.591)       0:00:34.365 ***** 
2026-10-28T17:33:30.2010709Z 
2026-10-28T17:33:30.2011800Z TASK [Copiando arquivos para jboss.server.config.dir] **************************
2026-10-28T17:33:30.2014467Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss', u'stat': {u'charset': u'binary', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1793208665.3279984, u'block_size': 4096, u'inode': 109056187, u'isgid': False, u'size': 86, u'wgrp': False, u'executable': True, u'isuid': False, u'readable': True, u'isreg': False, u'version': u'225038262', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'inode/directory', u'blocks': 0, u'xoth': True, u'islnk': False, u'nlink': 3, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss/configuration', u'xusr': True, u'atime': 1793208666.355984, u'isdir': True, u'ctime': 1793208665.3279984, u'isblk': False, u'xgrp': True, u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0755', u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss/configuration', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-28T17:33:30.2337382Z Wednesday 28 October 2026  14:33:30 -0300 (0:00:05.166)       0:00:39.531 ***** 
2026-10-28T17:33:30.5226297Z 
2026-10-28T17:33:30.5226981Z TASK [Get standalone-full-ha.xml status] ***************************************
2026-10-28T17:33:30.5227425Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config)
2026-10-28T17:33:30.7793919Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss)
2026-10-28T17:33:30.8076863Z Wednesday 28 October 2026  14:33:30 -0300 (0:00:00.573)       0:00:40.105 ***** 
2026-10-28T17:33:31.3843137Z 
2026-10-28T17:33:31.3843817Z TASK [Copiando arquivo standalone-full-ha.xml] *********************************
2026-10-28T17:33:31.3845396Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss', u'stat': {u'charset': u'us-ascii', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1793208666.3729837, u'block_size': 4096, u'inode': 104864194, u'isgid': False, u'size': 37587, u'wgrp': False, u'executable': False, u'isuid': False, u'readable': True, u'isreg': True, u'version': u'18446744072126457704', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'application/xml', u'blocks': 80, u'xoth': False, u'islnk': False, u'nlink': 1, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss/standalone-full-ha.xml', u'xusr': False, u'atime': 1793208666.3749838, u'isdir': False, u'ctime': 1793208666.3729837, u'isblk': False, u'checksum': u'fa4a2662b02ae34b61216425bbb53804dd4502b5', u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0644', u'xgrp': False, u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss/standalone-full-ha.xml', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-28T17:33:31.4170312Z Wednesday 28 October 2026  14:33:31 -0300 (0:00:00.609)       0:00:40.714 ***** 
2026-10-28T17:33:31.7041561Z 
2026-10-28T17:33:31.7042249Z TASK [Get standalone-ha.xml status] ********************************************
2026-10-28T17:33:31.7042543Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config)
2026-10-28T17:33:31.9555001Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss)
2026-10-28T17:33:31.9835716Z Wednesday 28 October 2026  14:33:31 -0300 (0:00:00.566)       0:00:41.281 ***** 
2026-10-28T17:33:32.0612270Z Wednesday 28 October 2026  14:33:32 -0300 (0:00:00.077)       0:00:41.359 ***** 
2026-10-28T17:33:32.3487446Z 
2026-10-28T17:33:32.3487958Z TASK [Get standalone.xml status] ***********************************************
2026-10-28T17:33:32.3488377Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config)
2026-10-28T17:33:32.5934575Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss)
2026-10-28T17:33:32.6211866Z Wednesday 28 October 2026  14:33:32 -0300 (0:00:00.559)       0:00:41.919 ***** 
2026-10-28T17:33:32.6997171Z Wednesday 28 October 2026  14:33:32 -0300 (0:00:00.078)       0:00:41.997 ***** 
2026-10-28T17:33:32.9951439Z 
2026-10-28T17:33:32.9952124Z TASK [Get standalone.conf status] **********************************************
2026-10-28T17:33:32.9952530Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config)
2026-10-28T17:33:33.2572160Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss)
2026-10-28T17:33:33.2855465Z Wednesday 28 October 2026  14:33:33 -0300 (0:00:00.585)       0:00:42.583 ***** 
2026-10-28T17:33:33.8571625Z 
2026-10-28T17:33:33.8572158Z TASK [Copiando arquivo standalone.conf] ****************************************
2026-10-28T17:33:33.8576877Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss', u'stat': {u'charset': u'us-ascii', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1793208666.3799837, u'block_size': 4096, u'inode': 104864195, u'isgid': False, u'size': 3976, u'wgrp': False, u'executable': False, u'isuid': False, u'readable': True, u'isreg': True, u'version': u'18446744072279853179', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'text/plain', u'blocks': 8, u'xoth': False, u'islnk': False, u'nlink': 1, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss/standalone.conf', u'xusr': False, u'atime': 1793208666.3849835, u'isdir': False, u'ctime': 1793208666.3799837, u'isblk': False, u'checksum': u'd3f13d68f3ea0dd6506d8aec0c5e8f3c8ccddf38', u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0644', u'xgrp': False, u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/jboss/standalone.conf', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-28T17:33:33.8905387Z Wednesday 28 October 2026  14:33:33 -0300 (0:00:00.604)       0:00:43.188 ***** 
2026-10-28T17:33:34.2256174Z 
2026-10-28T17:33:34.2256686Z TASK [Restart Zabbix] **********************************************************
2026-10-28T17:33:34.2257126Z fatal: [caddeapllx2651.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "msg": "Could not find the requested service zabbix-agent: host"}
2026-10-28T17:33:34.2257297Z ...ignoring
2026-10-28T17:33:34.2529597Z Wednesday 28 October 2026  14:33:34 -0300 (0:00:00.362)       0:00:43.550 ***** 
2026-10-28T17:33:34.3177029Z Wednesday 28 October 2026  14:33:34 -0300 (0:00:00.064)       0:00:43.615 ***** 
2026-10-28T17:33:34.3496064Z [WARNING]: conditional statements should not include jinja2 templating
2026-10-28T17:33:34.3496398Z delimiters such as {{ }} or {% %}. Found: {{ lookup('env','HSM') |
2026-10-28T17:33:34.3496579Z default('false', true) | bool }}
2026-10-28T17:33:34.3572033Z Wednesday 28 October 2026  14:33:34 -0300 (0:00:00.039)       0:00:43.655 ***** 
2026-10-28T17:33:41.8989993Z 
2026-10-28T17:33:41.8990573Z RUNNING HANDLER [Restart Jboss] ************************************************
2026-10-28T17:33:41.8990745Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:41.9031361Z 
2026-10-28T17:33:41.9031922Z PLAY [jboss] *******************************************************************
2026-10-28T17:33:41.9063198Z 
2026-10-28T17:33:41.9063435Z PLAY [jboss] *******************************************************************
2026-10-28T17:33:41.9092483Z 
2026-10-28T17:33:41.9092714Z PLAY [jboss] *******************************************************************
2026-10-28T17:33:41.9374671Z Wednesday 28 October 2026  14:33:41 -0300 (0:00:07.580)       0:00:51.235 ***** 
2026-10-28T17:33:42.0089923Z 
2026-10-28T17:33:42.0090674Z TASK [Cria variável build_repository_name] *************************************
2026-10-28T17:33:42.0090867Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:42.0350611Z Wednesday 28 October 2026  14:33:42 -0300 (0:00:00.097)       0:00:51.332 ***** 
2026-10-28T17:33:42.0880590Z 
2026-10-28T17:33:42.0881006Z TASK [Buscando diretorio de config] ********************************************
2026-10-28T17:33:42.0881175Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:42.1185471Z Wednesday 28 October 2026  14:33:42 -0300 (0:00:00.083)       0:00:51.416 ***** 
2026-10-28T17:33:42.4233112Z 
2026-10-28T17:33:42.4233786Z TASK [Verifica se o arquivo {{ item }}/etc/hosts-{{ sistema_ambiente }} existe] ***
2026-10-28T17:33:42.4234096Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config)
2026-10-28T17:33:42.6660255Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/so)
2026-10-28T17:33:42.6939399Z Wednesday 28 October 2026  14:33:42 -0300 (0:00:00.575)       0:00:51.991 ***** 
2026-10-28T17:33:43.0937340Z 
2026-10-28T17:33:43.0937845Z TASK [Altera arquivo /etc/hosts] ***********************************************
2026-10-28T17:33:43.0939487Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r6179/a/_SICCP-intra-config', u'stat': {u'charset': u'us-ascii', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1793208665.3269985, u'block_size': 4096, u'inode': 96470388, u'isgid': False, u'size': 141, u'wgrp': False, u'executable': False, u'isuid': False, u'readable': True, u'isreg': True, u'version': u'1322688521', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'text/plain', u'blocks': 8, u'xoth': False, u'islnk': False, u'nlink': 1, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/etc/hosts-des', u'xusr': False, u'atime': 1793208665.3269985, u'isdir': False, u'ctime': 1793208665.3269985, u'isblk': False, u'checksum': u'595cead82ca435bc6a45a58870a958603d6cf328', u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0644', u'xgrp': False, u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r6179/a/_SICCP-intra-config/etc/hosts-des', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-28T17:33:43.1013441Z 
2026-10-28T17:33:43.1014043Z PLAY [jboss] *******************************************************************
2026-10-28T17:33:43.1305059Z Wednesday 28 October 2026  14:33:43 -0300 (0:00:00.436)       0:00:52.428 ***** 
2026-10-28T17:33:43.4439865Z 
2026-10-28T17:33:43.4440719Z TASK [Verifica se o arquivo /opt/jboss-eap/standalone/configuration/custom.sh existe] ***
2026-10-28T17:33:43.4440896Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:43.4713559Z Wednesday 28 October 2026  14:33:43 -0300 (0:00:00.340)       0:00:52.769 ***** 
2026-10-28T17:33:45.6947257Z 
2026-10-28T17:33:45.6947770Z TASK [Executa shell customizada (jboss_home)] **********************************
2026-10-28T17:33:45.6947939Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:45.7234333Z Wednesday 28 October 2026  14:33:45 -0300 (0:00:02.252)       0:00:55.021 ***** 
2026-10-28T17:33:46.0599865Z 
2026-10-28T17:33:46.0600503Z TASK [Verifica se o arquivo /opt/batch/config/configuration/custom.sh existe] ***
2026-10-28T17:33:46.0600673Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:33:46.0871835Z Wednesday 28 October 2026  14:33:46 -0300 (0:00:00.363)       0:00:55.384 ***** 
2026-10-28T17:33:46.1264821Z 
2026-10-28T17:33:46.1265173Z PLAY [local] *******************************************************************
2026-10-28T17:33:46.1290700Z [WARNING]: Could not match supplied host pattern, ignoring: instance_restart
2026-10-28T17:33:46.1293130Z 
2026-10-28T17:33:46.1293361Z PLAY [instance_restart] ********************************************************
2026-10-28T17:33:46.1293522Z skipping: no hosts matched
2026-10-28T17:33:46.1296318Z [WARNING]: Could not match supplied host pattern, ignoring: machine_reboot
2026-10-28T17:33:46.1298975Z 
2026-10-28T17:33:46.1299386Z PLAY [machine_reboot] **********************************************************
2026-10-28T17:33:46.1299597Z skipping: no hosts matched
2026-10-28T17:33:46.1305209Z 
2026-10-28T17:33:46.1305441Z PLAY [local] *******************************************************************
2026-10-28T17:33:46.1329481Z [WARNING]: Could not match supplied host pattern, ignoring: instance_stop
2026-10-28T17:33:46.1332196Z 
2026-10-28T17:33:46.1332331Z PLAY [instance_stop] ***********************************************************
2026-10-28T17:33:46.1332481Z skipping: no hosts matched
2026-10-28T17:33:46.1335853Z 
2026-10-28T17:33:46.1336097Z PLAY [machine_reboot] **********************************************************
2026-10-28T17:33:46.1336257Z skipping: no hosts matched
2026-10-28T17:33:46.1341483Z 
2026-10-28T17:33:46.1341917Z PLAY [local] *******************************************************************
2026-10-28T17:33:46.1365291Z [WARNING]: Could not match supplied host pattern, ignoring: escopo_execucao
2026-10-28T17:33:46.1367826Z 
2026-10-28T17:33:46.1367984Z PLAY [Executar o Start do Sirot Connector no escopo definido] ******************
2026-10-28T17:33:46.1368139Z skipping: no hosts matched
2026-10-28T17:33:46.1373973Z 
2026-10-28T17:33:46.1374194Z PLAY [local] *******************************************************************
2026-10-28T17:33:46.1394275Z 
2026-10-28T17:33:46.1394472Z PLAY [Executar o Stop do Sirot Connector] **************************************
2026-10-28T17:33:46.1394621Z skipping: no hosts matched
2026-10-28T17:33:46.1403754Z 
2026-10-28T17:33:46.1403945Z PLAY [Configura TSM] ***********************************************************
2026-10-28T17:33:46.1428675Z 
2026-10-28T17:33:46.1428895Z PLAY [jboss] *******************************************************************
2026-10-28T17:33:46.1454806Z 
2026-10-28T17:33:46.1455434Z PLAY [Configura Control-M] *****************************************************
2026-10-28T17:33:46.1502971Z 
2026-10-28T17:33:46.1503175Z PLAY [jboss] *******************************************************************
2026-10-28T17:33:46.1541857Z 
2026-10-28T17:33:46.1542082Z PLAY [jboss] *******************************************************************
2026-10-28T17:33:46.1579586Z 
2026-10-28T17:33:46.1579821Z PLAY [jboss] *******************************************************************
2026-10-28T17:33:46.1601360Z 
2026-10-28T17:33:46.1601585Z PLAY [jboss] *******************************************************************
2026-10-28T17:33:46.1628553Z 
2026-10-28T17:33:46.1628781Z PLAY [localhost] ***************************************************************
2026-10-28T17:33:46.1651715Z 
2026-10-28T17:33:46.1652227Z PLAY [jboss] *******************************************************************
2026-10-28T17:33:46.1693104Z 
2026-10-28T17:33:46.1693410Z PLAY [jboss] *******************************************************************
2026-10-28T17:33:46.1730319Z 
2026-10-28T17:33:46.1730668Z PLAY [jboss] *******************************************************************
2026-10-28T17:33:46.1764312Z 
2026-10-28T17:33:46.1764527Z PLAY RECAP *********************************************************************
2026-10-28T17:33:46.1764725Z caddeapllx2651.agil.nprd.caixa.gov.br : ok=77   changed=14   unreachable=0    failed=0    skipped=18   rescued=0    ignored=3   
2026-10-28T17:33:46.1764835Z 
2026-10-28T17:33:46.1765970Z Wednesday 28 October 2026  14:33:46 -0300 (0:00:00.089)       0:00:55.474 ***** 
2026-10-28T17:33:46.1766151Z =============================================================================== 
2026-10-28T17:33:46.1768199Z nfs : Networker | Restart networker ------------------------------------ 10.46s
2026-10-28T17:33:46.1768536Z Restart Jboss ----------------------------------------------------------- 7.58s
2026-10-28T17:33:46.1768845Z Copiando arquivos para jboss.server.config.dir -------------------------- 5.17s
2026-10-28T17:33:46.1769167Z nfs : Instalando o NFS Client ------------------------------------------- 3.45s
2026-10-28T17:33:46.1769493Z Executa shell customizada (jboss_home) ---------------------------------- 2.25s
2026-10-28T17:33:46.1769808Z Gerando fatos de servicos ----------------------------------------------- 1.47s
2026-10-28T17:33:46.1770106Z nfs : Install networker lgtoclnt_url ------------------------------------ 0.96s
2026-10-28T17:33:46.1770551Z nfs : Networker | Start networker --------------------------------------- 0.90s
2026-10-28T17:33:46.1770899Z nfs : Install networker lgtonmda_url ------------------------------------ 0.81s
2026-10-28T17:33:46.1771228Z Realiza copia do arquivo de Trust Store --------------------------------- 0.76s
2026-10-28T17:33:46.1771562Z Create a symbolic link -------------------------------------------------- 0.75s
2026-10-28T17:33:46.1771909Z Gathering Facts --------------------------------------------------------- 0.64s
2026-10-28T17:33:46.1772262Z Copy common_start.sh ---------------------------------------------------- 0.62s
2026-10-28T17:33:46.1772615Z Copiando arquivo standalone-full-ha.xml --------------------------------- 0.61s
2026-10-28T17:33:46.1772964Z Copiando arquivo standalone.conf ---------------------------------------- 0.60s
2026-10-28T17:33:46.1773318Z Copiando artefatos para o(s) servidor(es) Jboss ------------------------- 0.60s
2026-10-28T17:33:46.1773665Z maven_artifact ---------------------------------------------------------- 0.59s
2026-10-28T17:33:46.1774040Z Check directory configuration exists ------------------------------------ 0.59s
2026-10-28T17:33:46.1774385Z Copy template script ---------------------------------------------------- 0.59s
2026-10-28T17:33:46.1774741Z JBoss systemd wrapper for sysvinit script mode domain ------------------- 0.59s
2026-10-28T17:33:46.1774993Z Playbook run took 0 days, 0 hours, 0 minutes, 55 seconds
2026-10-28T17:33:46.2381907Z ##[section]Finishing: Deploy Config no JBOSS






fiz as alteraçoes na master mesmo, ja tinha feito uma vez e deu certo



[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ systemctl status sigdb --no-pager; ps -ef | grep -i [A]gtSigdb
× sigdb.service - SIGDB Agent
     Loaded: loaded (/etc/systemd/system/sigdb.service; enabled; preset: disabled)
     Active: failed (Result: exit-code) since Wed 2026-10-28 14:35:17 -03; 44s ago
   Duration: 1ms
    Process: 192739 ExecStart=/sigdb/run (code=exited, status=1/FAILURE)
   Main PID: 192739 (code=exited, status=1/FAILURE)
        CPU: 1ms
[p585600@caddeapllx2651 ~]$ ps -ef | grep -i [A]gtSigdb
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$



passou

