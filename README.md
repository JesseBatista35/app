systemctl status sigdb --no-pager; ps -ef | grep -i [A]gtSigdb

2026-10-28T17:49:52.0962743Z ##[section]Starting: Deploy Config no JBOSS
2026-10-28T17:49:52.0965732Z ==============================================================================
2026-10-28T17:49:52.0965816Z Task         : Bash
2026-10-28T17:49:52.0965871Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-28T17:49:52.0965936Z Version      : 3.227.0
2026-10-28T17:49:52.0965981Z Author       : Microsoft Corporation
2026-10-28T17:49:52.0966043Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-28T17:49:52.0966118Z ==============================================================================
2026-10-28T17:49:53.0017973Z Generating script.
2026-10-28T17:49:53.0028688Z ========================== Starting Command Output ===========================
2026-10-28T17:49:53.0035524Z [command]/bin/bash /opt/ads-agent/_work/_temp/de506d48-31cd-43c5-a455-59dcd7b70bc7.sh
2026-10-28T17:49:53.0103200Z /opt/ads-agent/_work/_temp/de506d48-31cd-43c5-a455-59dcd7b70bc7.sh: line 2: quantidade_vm: comando não encontrado
2026-10-28T17:49:53.0113281Z /opt/ads-agent/_work/_temp/de506d48-31cd-43c5-a455-59dcd7b70bc7.sh: line 2: USE_WMQ: comando não encontrado
2026-10-28T17:49:55.0676634Z 
2026-10-28T17:49:55.0677605Z PLAY [local] *******************************************************************
2026-10-28T17:49:55.0960238Z 
2026-10-28T17:49:55.0960762Z PLAY [Configurando o DNS] ******************************************************
2026-10-28T17:49:55.2751018Z 
2026-10-28T17:49:55.2751564Z PLAY [local] *******************************************************************
2026-10-28T17:49:55.2781213Z 
2026-10-28T17:49:55.2781654Z PLAY [Verificando serviços] ****************************************************
2026-10-28T17:49:55.2861463Z 
2026-10-28T17:49:55.2861794Z PLAY [Configuração LDAP] *******************************************************
2026-10-28T17:49:55.2894090Z [WARNING]: Found variable using reserved name: when
2026-10-28T17:49:55.2899488Z 
2026-10-28T17:49:55.2899724Z PLAY [jboss] *******************************************************************
2026-10-28T17:49:55.2983359Z 
2026-10-28T17:49:55.2983638Z PLAY [Stack Jboss] *************************************************************
2026-10-28T17:49:55.3208582Z Wednesday 28 October 2026  14:49:55 -0300 (0:00:00.313)       0:00:00.313 ***** 
2026-10-28T17:49:55.8129912Z 
2026-10-28T17:49:55.8131326Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-10-28T17:49:55.8133684Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-28T17:49:55.8134124Z caddeapllx2651.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-28T17:49:55.8134453Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-28T17:49:55.8134748Z releases. A future Ansible release will default to using the discovered 
2026-10-28T17:49:55.8135055Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-28T17:49:55.8135700Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-28T17:49:55.8136009Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-28T17:49:55.8136299Z setting deprecation_warnings=False in ansible.cfg.
2026-10-28T17:49:55.8136555Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:49:55.8155224Z 
2026-10-28T17:49:55.8155574Z PLAY [jboss] *******************************************************************
2026-10-28T17:49:55.8217343Z Wednesday 28 October 2026  14:49:55 -0300 (0:00:00.500)       0:00:00.813 ***** 
2026-10-28T17:49:56.1250002Z 
2026-10-28T17:49:56.1250526Z TASK [Verifica se o arquivo nfs_config.json existe] ****************************
2026-10-28T17:49:56.1250696Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:49:56.1278367Z Wednesday 28 October 2026  14:49:56 -0300 (0:00:00.306)       0:00:01.119 ***** 
2026-10-28T17:49:56.1727870Z included: /opt/ads-agent/_work/r12326/a/esteira-jboss-vm-v2/roles/nfs/tasks/get_nfs.yml for caddeapllx2651.agil.nprd.caixa.gov.br
2026-10-28T17:49:56.1763416Z Wednesday 28 October 2026  14:49:56 -0300 (0:00:00.048)       0:00:01.168 ***** 
2026-10-28T17:49:56.2320902Z 
2026-10-28T17:49:56.2321522Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-28T17:49:56.2321809Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:49:56.2363188Z Wednesday 28 October 2026  14:49:56 -0300 (0:00:00.059)       0:00:01.228 ***** 
2026-10-28T17:49:56.6407525Z 
2026-10-28T17:49:56.6408247Z TASK [nfs : Coletar variáveis de ambiente] *************************************
2026-10-28T17:49:56.6408421Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:49:56.6434211Z Wednesday 28 October 2026  14:49:56 -0300 (0:00:00.407)       0:00:01.635 ***** 
2026-10-28T17:49:56.6981770Z 
2026-10-28T17:49:56.6982296Z TASK [nfs : Exibir resultado em JSON] ******************************************
2026-10-28T17:49:56.6986264Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:49:56.6986471Z     "nfs_vars_json": {
2026-10-28T17:49:56.6986606Z         "changed": false, 
2026-10-28T17:49:56.6986939Z         "cmd": "cat /opt/ads-agent/_work/r12326/a/nfs_config.json", 
2026-10-28T17:49:56.6987104Z         "delta": "0:00:00.003037", 
2026-10-28T17:49:56.6987298Z         "end": "2026-10-28 14:49:56.627629", 
2026-10-28T17:49:56.6987430Z         "failed": false, 
2026-10-28T17:49:56.6987542Z         "rc": 0, 
2026-10-28T17:49:56.6987718Z         "start": "2026-10-28 14:49:56.624592", 
2026-10-28T17:49:56.6987848Z         "stderr": "", 
2026-10-28T17:49:56.6987962Z         "stderr_lines": [], 
2026-10-28T17:49:56.6988118Z         "stdout": "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]", 
2026-10-28T17:49:56.6988285Z         "stdout_lines": [
2026-10-28T17:49:56.6988435Z             "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]"
2026-10-28T17:49:56.6988581Z         ]
2026-10-28T17:49:56.6988679Z     }
2026-10-28T17:49:56.6988780Z }
2026-10-28T17:49:56.7019021Z Wednesday 28 October 2026  14:49:56 -0300 (0:00:00.058)       0:00:01.694 ***** 
2026-10-28T17:49:56.7591830Z 
2026-10-28T17:49:56.7592655Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-28T17:49:56.7592836Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:49:56.7630265Z Wednesday 28 October 2026  14:49:56 -0300 (0:00:00.061)       0:00:01.755 ***** 
2026-10-28T17:49:57.3870350Z 
2026-10-28T17:49:57.3871039Z TASK [nfs : execute montagem script] *******************************************
2026-10-28T17:49:57.3871325Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:49:57.3897876Z Wednesday 28 October 2026  14:49:57 -0300 (0:00:00.626)       0:00:02.381 ***** 
2026-10-28T17:49:57.4471521Z 
2026-10-28T17:49:57.4472341Z TASK [nfs : ansible.builtin.debug] *********************************************
2026-10-28T17:49:57.4472955Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:49:57.4473554Z     "changed": false, 
2026-10-28T17:49:57.4473753Z     "msg": {
2026-10-28T17:49:57.4475682Z         "changed": true, 
2026-10-28T17:49:57.4476152Z         "cmd": [
2026-10-28T17:49:57.4476468Z             "python", 
2026-10-28T17:49:57.4476952Z             "/opt/ads-agent/_work/r12326/a/esteira-jboss-vm-v2/roles/nfs/files/nfs.py", 
2026-10-28T17:49:57.4477215Z             "montagem", 
2026-10-28T17:49:57.4477452Z             "siccp-intra", 
2026-10-28T17:49:57.4477634Z             "des", 
2026-10-28T17:49:57.4477811Z             "ctc_nprd", 
2026-10-28T17:49:57.4478103Z             "/opt/ads-agent/_work/r12326/a/esteira-jboss-vm-v2", 
2026-10-28T17:49:57.4478313Z             "C&t@d02", 
2026-10-28T17:49:57.4478564Z             "***", 
2026-10-28T17:49:57.4478757Z             "s736651@corp.caixa.gov.br", 
2026-10-28T17:49:57.4478974Z             "***", 
2026-10-28T17:49:57.4479215Z             "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]"
2026-10-28T17:49:57.4479453Z         ], 
2026-10-28T17:49:57.4479787Z         "delta": "0:00:00.291079", 
2026-10-28T17:49:57.4480075Z         "end": "2026-10-28 14:49:57.371049", 
2026-10-28T17:49:57.4480290Z         "failed": false, 
2026-10-28T17:49:57.4480471Z         "rc": 0, 
2026-10-28T17:49:57.4480739Z         "start": "2026-10-28 14:49:57.079970", 
2026-10-28T17:49:57.4480943Z         "stderr": "", 
2026-10-28T17:49:57.4481124Z         "stderr_lines": [], 
2026-10-28T17:49:57.4482648Z         "stdout": "[{u'NFS_MOUNT_POINT_VM': u'/siccp', u'NFS_ENDPOINT_VM': u'hypernprd12.ad.caixa:/fs_siccp'}]\nNome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           \n------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------\nhypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                                \nnfs_path=/siccp\nnfs_src=hypernprd12.ad.caixa:/fs_siccp\nhypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                                ", 
2026-10-28T17:49:57.4483377Z         "stdout_lines": [
2026-10-28T17:49:57.4483857Z             "[{u'NFS_MOUNT_POINT_VM': u'/siccp', u'NFS_ENDPOINT_VM': u'hypernprd12.ad.caixa:/fs_siccp'}]", 
2026-10-28T17:49:57.4484177Z             "Nome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           ", 
2026-10-28T17:49:57.4484757Z             "------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------", 
2026-10-28T17:49:57.4485169Z             "hypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                                ", 
2026-10-28T17:49:57.4485418Z             "nfs_path=/siccp", 
2026-10-28T17:49:57.4485630Z             "nfs_src=hypernprd12.ad.caixa:/fs_siccp", 
2026-10-28T17:49:57.4485902Z             "hypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                                "
2026-10-28T17:49:57.4486136Z         ]
2026-10-28T17:49:57.4486294Z     }
2026-10-28T17:49:57.4486445Z }
2026-10-28T17:49:57.4498525Z Wednesday 28 October 2026  14:49:57 -0300 (0:00:00.060)       0:00:02.442 ***** 
2026-10-28T17:49:57.7056853Z 
2026-10-28T17:49:57.7057276Z TASK [nfs : execute clean json] ************************************************
2026-10-28T17:49:57.7057453Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:49:57.7082794Z Wednesday 28 October 2026  14:49:57 -0300 (0:00:00.258)       0:00:02.700 ***** 
2026-10-28T17:49:57.7640707Z 
2026-10-28T17:49:57.7641196Z TASK [nfs : result_new_string_json] ********************************************
2026-10-28T17:49:57.7642622Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:49:57.7643071Z     "msg": {
2026-10-28T17:49:57.7643234Z         "changed": true, 
2026-10-28T17:49:57.7643845Z         "cmd": "echo '[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]' | sed 's/NFS_ENDPOINT_ISILON[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_ISILON[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_HUAWEI[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_HUAWEI[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_VM[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_VM[^\"]*/NFS_MOUNT_POINT/g'", 
2026-10-28T17:49:57.7644557Z         "delta": "0:00:00.003918", 
2026-10-28T17:49:57.7644749Z         "end": "2026-10-28 14:49:57.688434", 
2026-10-28T17:49:57.7644880Z         "failed": false, 
2026-10-28T17:49:57.7644994Z         "rc": 0, 
2026-10-28T17:49:57.7645167Z         "start": "2026-10-28 14:49:57.684516", 
2026-10-28T17:49:57.7645295Z         "stderr": "", 
2026-10-28T17:49:57.7645411Z         "stderr_lines": [], 
2026-10-28T17:49:57.7645562Z         "stdout": "[{\"NFS_ENDPOINT\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT\": \"/siccp\"}]", 
2026-10-28T17:49:57.7645713Z         "stdout_lines": [
2026-10-28T17:49:57.7645859Z             "[{\"NFS_ENDPOINT\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT\": \"/siccp\"}]"
2026-10-28T17:49:57.7645995Z         ]
2026-10-28T17:49:57.7646095Z     }
2026-10-28T17:49:57.7646191Z }
2026-10-28T17:49:57.7667888Z Wednesday 28 October 2026  14:49:57 -0300 (0:00:00.058)       0:00:02.759 ***** 
2026-10-28T17:49:57.8228964Z 
2026-10-28T17:49:57.8229851Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-28T17:49:57.8230137Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:49:57.8252784Z Wednesday 28 October 2026  14:49:57 -0300 (0:00:00.058)       0:00:02.817 ***** 
2026-10-28T17:49:57.8803366Z 
2026-10-28T17:49:57.8803872Z TASK [nfs : result_new_json] ***************************************************
2026-10-28T17:49:57.8804057Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:49:57.8804188Z     "msg": [
2026-10-28T17:49:57.8804289Z         {
2026-10-28T17:49:57.8804416Z             "NFS_ENDPOINT": "hypernprd12.ad.caixa:/fs_siccp", 
2026-10-28T17:49:57.8804553Z             "NFS_MOUNT_POINT": "/siccp"
2026-10-28T17:49:57.8804664Z         }
2026-10-28T17:49:57.8804769Z     ]
2026-10-28T17:49:57.8804864Z }
2026-10-28T17:49:57.8827365Z Wednesday 28 October 2026  14:49:57 -0300 (0:00:00.057)       0:00:02.874 ***** 
2026-10-28T17:49:57.9407866Z included: /opt/ads-agent/_work/r12326/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2651.agil.nprd.caixa.gov.br
2026-10-28T17:49:57.9460402Z Wednesday 28 October 2026  14:49:57 -0300 (0:00:00.063)       0:00:02.938 ***** 
2026-10-28T17:49:57.9994020Z 
2026-10-28T17:49:57.9994486Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-28T17:49:57.9994663Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:49:58.0019562Z Wednesday 28 October 2026  14:49:58 -0300 (0:00:00.055)       0:00:02.994 ***** 
2026-10-28T17:49:58.0551464Z 
2026-10-28T17:49:58.0552102Z TASK [nfs : debug] *************************************************************
2026-10-28T17:49:58.0552305Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:49:58.0552440Z     "msg": {
2026-10-28T17:49:58.0552570Z         "NFS_ENDPOINT": "hypernprd12.ad.caixa:/fs_siccp", 
2026-10-28T17:49:58.0553013Z         "NFS_MOUNT_POINT": "/siccp"
2026-10-28T17:49:58.0553131Z     }
2026-10-28T17:49:58.0553227Z }
2026-10-28T17:49:58.0577594Z Wednesday 28 October 2026  14:49:58 -0300 (0:00:00.055)       0:00:03.049 ***** 
2026-10-28T17:49:58.1117066Z 
2026-10-28T17:49:58.1117773Z TASK [nfs : debug] *************************************************************
2026-10-28T17:49:58.1118217Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:49:58.1118542Z     "msg": "/siccp"
2026-10-28T17:49:58.1118665Z }
2026-10-28T17:49:58.1141909Z Wednesday 28 October 2026  14:49:58 -0300 (0:00:00.056)       0:00:03.106 ***** 
2026-10-28T17:49:58.1666772Z 
2026-10-28T17:49:58.1667456Z TASK [nfs : debug] *************************************************************
2026-10-28T17:49:58.1667761Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:49:58.1668015Z     "msg": "hypernprd12.ad.caixa:/fs_siccp"
2026-10-28T17:49:58.1668211Z }
2026-10-28T17:49:58.1694277Z Wednesday 28 October 2026  14:49:58 -0300 (0:00:00.055)       0:00:03.161 ***** 
2026-10-28T17:49:58.2252351Z 
2026-10-28T17:49:58.2253420Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-28T17:49:58.2253726Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:49:58.2253960Z     "changed": false, 
2026-10-28T17:49:58.2254199Z     "msg": "All assertions passed"
2026-10-28T17:49:58.2254385Z }
2026-10-28T17:49:58.2278781Z Wednesday 28 October 2026  14:49:58 -0300 (0:00:00.058)       0:00:03.219 ***** 
2026-10-28T17:50:01.7329490Z 
2026-10-28T17:50:01.7330340Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-28T17:50:01.7330658Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:01.7359906Z Wednesday 28 October 2026  14:50:01 -0300 (0:00:03.508)       0:00:06.728 ***** 
2026-10-28T17:50:02.7024787Z 
2026-10-28T17:50:02.7025497Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-28T17:50:02.7025735Z [WARNING]: Consider using the yum, dnf or zypper module rather than running
2026-10-28T17:50:02.7026123Z 'rpm'.  If you need to use command because yum, dnf or zypper is insufficient
2026-10-28T17:50:02.7026354Z you can add 'warn: false' to this command task or set 'command_warnings=False'
2026-10-28T17:50:02.7026512Z in ansible.cfg to get rid of this message.
2026-10-28T17:50:02.7029737Z fatal: [caddeapllx2651.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.707278", "end": "2026-10-28 14:50:02.683558", "msg": "non-zero return code", "rc": 1, "start": "2026-10-28 14:50:01.976280", "stderr": "aviso: /var/tmp/rpm-tmp.ApO0Sv: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.ApO0Sv: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-28T17:50:02.7030308Z ...ignoring
2026-10-28T17:50:02.7057254Z Wednesday 28 October 2026  14:50:02 -0300 (0:00:00.969)       0:00:07.697 ***** 
2026-10-28T17:50:03.5445415Z 
2026-10-28T17:50:03.5445962Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-28T17:50:03.5450004Z fatal: [caddeapllx2651.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.592114", "end": "2026-10-28 14:50:03.528870", "msg": "non-zero return code", "rc": 1, "start": "2026-10-28 14:50:02.936756", "stderr": "aviso: /var/tmp/rpm-tmp.rwSLSs: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.rwSLSs: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-28T17:50:03.5450971Z ...ignoring
2026-10-28T17:50:03.5478758Z Wednesday 28 October 2026  14:50:03 -0300 (0:00:00.842)       0:00:08.540 ***** 
2026-10-28T17:50:03.9565652Z 
2026-10-28T17:50:03.9566772Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-28T17:50:03.9566980Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:03.9594925Z Wednesday 28 October 2026  14:50:03 -0300 (0:00:00.411)       0:00:08.951 ***** 
2026-10-28T17:50:04.2105026Z 
2026-10-28T17:50:04.2105575Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-28T17:50:04.2105769Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:04.2133561Z Wednesday 28 October 2026  14:50:04 -0300 (0:00:00.253)       0:00:09.205 ***** 
2026-10-28T17:50:05.1142705Z 
2026-10-28T17:50:05.1143246Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-28T17:50:05.1143422Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:05.1192548Z Wednesday 28 October 2026  14:50:05 -0300 (0:00:00.905)       0:00:10.111 ***** 
2026-10-28T17:50:05.3810732Z 
2026-10-28T17:50:05.3811280Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-28T17:50:05.3811462Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:05.3837747Z Wednesday 28 October 2026  14:50:05 -0300 (0:00:00.264)       0:00:10.375 ***** 
2026-10-28T17:50:15.8301195Z 
2026-10-28T17:50:15.8301746Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-28T17:50:15.8301918Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:15.8326881Z Wednesday 28 October 2026  14:50:15 -0300 (0:00:10.448)       0:00:20.824 ***** 
2026-10-28T17:50:16.2954367Z 
2026-10-28T17:50:16.2954971Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-28T17:50:16.2955149Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:16.2983119Z Wednesday 28 October 2026  14:50:16 -0300 (0:00:00.465)       0:00:21.290 ***** 
2026-10-28T17:50:16.3393029Z 
2026-10-28T17:50:16.3393558Z PLAY [jboss] *******************************************************************
2026-10-28T17:50:16.3433503Z 
2026-10-28T17:50:16.3433842Z PLAY [jboss] *******************************************************************
2026-10-28T17:50:16.3468499Z Wednesday 28 October 2026  14:50:16 -0300 (0:00:00.048)       0:00:21.339 ***** 
2026-10-28T17:50:16.9594071Z 
2026-10-28T17:50:16.9595062Z TASK [Gathering Facts] *********************************************************
2026-10-28T17:50:16.9595252Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:16.9790737Z Wednesday 28 October 2026  14:50:16 -0300 (0:00:00.632)       0:00:21.971 ***** 
2026-10-28T17:50:18.4128108Z 
2026-10-28T17:50:18.4128822Z TASK [Gerando fatos de servicos] ***********************************************
2026-10-28T17:50:18.4129078Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:18.4478929Z Wednesday 28 October 2026  14:50:18 -0300 (0:00:01.468)       0:00:23.439 ***** 
2026-10-28T17:50:18.5067518Z 
2026-10-28T17:50:18.5068090Z TASK [Gerando lista de units jboss] ********************************************
2026-10-28T17:50:18.5068267Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:18.5339990Z Wednesday 28 October 2026  14:50:18 -0300 (0:00:00.086)       0:00:23.526 ***** 
2026-10-28T17:50:18.6002852Z Wednesday 28 October 2026  14:50:18 -0300 (0:00:00.066)       0:00:23.592 ***** 
2026-10-28T17:50:18.6121097Z 
2026-10-28T17:50:18.6121714Z PLAY [Copiando deployments adicionais] *****************************************
2026-10-28T17:50:18.6416507Z Wednesday 28 October 2026  14:50:18 -0300 (0:00:00.041)       0:00:23.633 ***** 
2026-10-28T17:50:18.6971322Z 
2026-10-28T17:50:18.6972315Z TASK [Cria variável build_repository_name] *************************************
2026-10-28T17:50:18.6972637Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:18.7242714Z Wednesday 28 October 2026  14:50:18 -0300 (0:00:00.082)       0:00:23.716 ***** 
2026-10-28T17:50:18.7774224Z 
2026-10-28T17:50:18.7774747Z TASK [Buscando diretorio de config] ********************************************
2026-10-28T17:50:18.7775268Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:18.8050976Z Wednesday 28 October 2026  14:50:18 -0300 (0:00:00.080)       0:00:23.797 ***** 
2026-10-28T17:50:18.8595295Z 
2026-10-28T17:50:18.8595863Z TASK [Buscando diretorio de config] ********************************************
2026-10-28T17:50:18.8596371Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:18.8927979Z Wednesday 28 October 2026  14:50:18 -0300 (0:00:00.087)       0:00:23.884 ***** 
2026-10-28T17:50:19.4040221Z 
2026-10-28T17:50:19.4040764Z TASK [Create a symbolic link] **************************************************
2026-10-28T17:50:19.4042313Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config)
2026-10-28T17:50:19.6588496Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss)
2026-10-28T17:50:19.6908099Z Wednesday 28 October 2026  14:50:19 -0300 (0:00:00.798)       0:00:24.682 ***** 
2026-10-28T17:50:19.9887856Z 
2026-10-28T17:50:19.9888387Z TASK [Verifica se o arquivo  existe] *******************************************
2026-10-28T17:50:19.9888796Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config)
2026-10-28T17:50:20.2603899Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss)
2026-10-28T17:50:20.2893425Z Wednesday 28 October 2026  14:50:20 -0300 (0:00:00.598)       0:00:25.281 ***** 
2026-10-28T17:50:20.3793421Z included: /opt/ads-agent/_work/r12326/a/esteira-jboss-vm-v2/roles/jboss/tasks/stack_deployments_custom_block.yml for caddeapllx2651.agil.nprd.caixa.gov.br
2026-10-28T17:50:20.4082882Z Wednesday 28 October 2026  14:50:20 -0300 (0:00:00.118)       0:00:25.400 ***** 
2026-10-28T17:50:20.8914453Z 
2026-10-28T17:50:20.8915229Z TASK [Lendo artefatos do arquivo CSV] ******************************************
2026-10-28T17:50:20.8915427Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:20.9433951Z Wednesday 28 October 2026  14:50:20 -0300 (0:00:00.535)       0:00:25.935 ***** 
2026-10-28T17:50:20.9524482Z [WARNING]: The loop variable 'item' is already in use. You should set the
2026-10-28T17:50:20.9525306Z `loop_var` value in the `loop_control` option for the task to something else to
2026-10-28T17:50:20.9525528Z avoid variable collisions and unexpected behavior.
2026-10-28T17:50:20.9887441Z 
2026-10-28T17:50:20.9887935Z TASK [Mostra artefatos] ********************************************************
2026-10-28T17:50:20.9888372Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item={u'version': u'0.0.0', u'group_id': u'com.ibm.mq', u'extension': u'rar', u'artifact_id': u'wmq.jmsra'}) => {
2026-10-28T17:50:20.9888615Z     "msg": "Artefato: wmq.jmsra - versao 0.0.0"
2026-10-28T17:50:20.9889086Z }
2026-10-28T17:50:21.0199377Z Wednesday 28 October 2026  14:50:21 -0300 (0:00:00.076)       0:00:26.011 ***** 
2026-10-28T17:50:21.6093299Z 
2026-10-28T17:50:21.6093867Z TASK [maven_artifact] **********************************************************
2026-10-28T17:50:21.6094352Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item={u'version': u'0.0.0', u'group_id': u'com.ibm.mq', u'extension': u'rar', u'artifact_id': u'wmq.jmsra'})
2026-10-28T17:50:21.6389720Z Wednesday 28 October 2026  14:50:21 -0300 (0:00:00.619)       0:00:26.631 ***** 
2026-10-28T17:50:22.2255152Z 
2026-10-28T17:50:22.2256111Z TASK [Copiando artefatos para o(s) servidor(es) Jboss] *************************
2026-10-28T17:50:22.2256330Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:22.2537887Z Wednesday 28 October 2026  14:50:22 -0300 (0:00:00.614)       0:00:27.245 ***** 
2026-10-28T17:50:22.2947899Z 
2026-10-28T17:50:22.2948771Z PLAY [Copiando modules adicionais] *********************************************
2026-10-28T17:50:22.3235998Z Wednesday 28 October 2026  14:50:22 -0300 (0:00:00.069)       0:00:27.315 ***** 
2026-10-28T17:50:22.3773339Z 
2026-10-28T17:50:22.3774118Z TASK [Cria variável build_repository_name] *************************************
2026-10-28T17:50:22.3774302Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:22.4067702Z Wednesday 28 October 2026  14:50:22 -0300 (0:00:00.083)       0:00:27.398 ***** 
2026-10-28T17:50:22.4608284Z 
2026-10-28T17:50:22.4608823Z TASK [Buscando diretorio de config] ********************************************
2026-10-28T17:50:22.4609007Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:22.4901093Z Wednesday 28 October 2026  14:50:22 -0300 (0:00:00.083)       0:00:27.482 ***** 
2026-10-28T17:50:22.5414699Z 
2026-10-28T17:50:22.5415205Z TASK [Buscando diretorio de config] ********************************************
2026-10-28T17:50:22.5415381Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:22.5744571Z Wednesday 28 October 2026  14:50:22 -0300 (0:00:00.084)       0:00:27.566 ***** 
2026-10-28T17:50:22.8930838Z 
2026-10-28T17:50:22.8931412Z TASK [Create a directory] ******************************************************
2026-10-28T17:50:22.8931900Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config)
2026-10-28T17:50:23.1482369Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss)
2026-10-28T17:50:23.1804662Z Wednesday 28 October 2026  14:50:23 -0300 (0:00:00.605)       0:00:28.172 ***** 
2026-10-28T17:50:23.4701444Z 
2026-10-28T17:50:23.4702315Z TASK [Verifica se o arquivo  existe] *******************************************
2026-10-28T17:50:23.4702925Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config)
2026-10-28T17:50:23.7345319Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss)
2026-10-28T17:50:23.7638677Z Wednesday 28 October 2026  14:50:23 -0300 (0:00:00.583)       0:00:28.755 ***** 
2026-10-28T17:50:23.8975161Z included: /opt/ads-agent/_work/r12326/a/esteira-jboss-vm-v2/roles/jboss/tasks/stack_modules_custom_block.yml for caddeapllx2651.agil.nprd.caixa.gov.br
2026-10-28T17:50:23.9274714Z Wednesday 28 October 2026  14:50:23 -0300 (0:00:00.163)       0:00:28.919 ***** 
2026-10-28T17:50:24.2232614Z 
2026-10-28T17:50:24.2233160Z TASK [Lendo artefatos do arquivo CSV] ******************************************
2026-10-28T17:50:24.2233329Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:24.2527555Z Wednesday 28 October 2026  14:50:24 -0300 (0:00:00.325)       0:00:29.244 ***** 
2026-10-28T17:50:24.2896280Z Wednesday 28 October 2026  14:50:24 -0300 (0:00:00.036)       0:00:29.281 ***** 
2026-10-28T17:50:24.6553310Z 
2026-10-28T17:50:24.6563192Z TASK [Listar arquivos no diretório baixados anteriormente] *********************
2026-10-28T17:50:24.6563508Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:24.7095081Z Wednesday 28 October 2026  14:50:24 -0300 (0:00:00.419)       0:00:29.701 ***** 
2026-10-28T17:50:24.7712110Z Wednesday 28 October 2026  14:50:24 -0300 (0:00:00.061)       0:00:29.763 ***** 
2026-10-28T17:50:25.0761729Z 
2026-10-28T17:50:25.0762581Z TASK [Verifica se o arquivo jboss-modules-custom tem conteudo] *****************
2026-10-28T17:50:25.0762838Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:25.1029928Z Wednesday 28 October 2026  14:50:25 -0300 (0:00:00.331)       0:00:30.094 ***** 
2026-10-28T17:50:25.2716142Z 
2026-10-28T17:50:25.2716721Z TASK [Copiando artefatos (Modules) para o(s) servidor(es) Jboss] ***************
2026-10-28T17:50:25.2716901Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:25.2994030Z Wednesday 28 October 2026  14:50:25 -0300 (0:00:00.196)       0:00:30.291 ***** 
2026-10-28T17:50:25.9179518Z 
2026-10-28T17:50:25.9181062Z TASK [Copiando artefato (jboss-custom.cli) para o(s) servidor(es) Jboss] *******
2026-10-28T17:50:25.9181296Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:25.9460659Z Wednesday 28 October 2026  14:50:25 -0300 (0:00:00.646)       0:00:30.938 ***** 
2026-10-28T17:50:26.0153874Z Wednesday 28 October 2026  14:50:26 -0300 (0:00:00.069)       0:00:31.007 ***** 
2026-10-28T17:50:26.0826271Z Wednesday 28 October 2026  14:50:26 -0300 (0:00:00.067)       0:00:31.074 ***** 
2026-10-28T17:50:26.1500170Z Wednesday 28 October 2026  14:50:26 -0300 (0:00:00.067)       0:00:31.141 ***** 
2026-10-28T17:50:26.2180152Z Wednesday 28 October 2026  14:50:26 -0300 (0:00:00.067)       0:00:31.209 ***** 
2026-10-28T17:50:26.2869251Z Wednesday 28 October 2026  14:50:26 -0300 (0:00:00.068)       0:00:31.278 ***** 
2026-10-28T17:50:26.3417508Z 
2026-10-28T17:50:26.3418062Z TASK [Sem modules adicionais] **************************************************
2026-10-28T17:50:26.3418246Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T17:50:26.3418392Z     "msg": "Sem modules adicional"
2026-10-28T17:50:26.3418525Z }
2026-10-28T17:50:26.3436859Z 
2026-10-28T17:50:26.3437219Z PLAY [jboss] *******************************************************************
2026-10-28T17:50:26.3734253Z Wednesday 28 October 2026  14:50:26 -0300 (0:00:00.086)       0:00:31.365 ***** 
2026-10-28T17:50:26.4327003Z 
2026-10-28T17:50:26.4327759Z TASK [Setando a versão do Jboss] ***********************************************
2026-10-28T17:50:26.4327981Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:26.4604008Z Wednesday 28 October 2026  14:50:26 -0300 (0:00:00.087)       0:00:31.452 ***** 
2026-10-28T17:50:26.5151373Z 
2026-10-28T17:50:26.5152221Z TASK [Cria variável build_repository_name_tfs] *********************************
2026-10-28T17:50:26.5152415Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:26.5424187Z Wednesday 28 October 2026  14:50:26 -0300 (0:00:00.082)       0:00:31.534 ***** 
2026-10-28T17:50:26.5971366Z 
2026-10-28T17:50:26.5972334Z TASK [Buscando diretorio de config] ********************************************
2026-10-28T17:50:26.5972624Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:26.6254800Z Wednesday 28 October 2026  14:50:26 -0300 (0:00:00.082)       0:00:31.617 ***** 
2026-10-28T17:50:27.1928440Z 
2026-10-28T17:50:27.1929205Z TASK [Copy common_start.sh] ****************************************************
2026-10-28T17:50:27.1929522Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:27.2303661Z Wednesday 28 October 2026  14:50:27 -0300 (0:00:00.604)       0:00:32.222 ***** 
2026-10-28T17:50:27.8027254Z 
2026-10-28T17:50:27.8027647Z TASK [Copy template script] ****************************************************
2026-10-28T17:50:27.8027823Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:27.8308805Z Wednesday 28 October 2026  14:50:27 -0300 (0:00:00.600)       0:00:32.822 ***** 
2026-10-28T17:50:28.3957731Z 
2026-10-28T17:50:28.3958277Z TASK [JBoss systemd wrapper for sysvinit script mode domain] *******************
2026-10-28T17:50:28.3958444Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:28.4230282Z Wednesday 28 October 2026  14:50:28 -0300 (0:00:00.592)       0:00:33.415 ***** 
2026-10-28T17:50:29.1776704Z 
2026-10-28T17:50:29.1777244Z TASK [Realiza copia do arquivo de Trust Store] *********************************
2026-10-28T17:50:29.1777419Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:29.2053664Z Wednesday 28 October 2026  14:50:29 -0300 (0:00:00.782)       0:00:34.197 ***** 
2026-10-28T17:50:29.2781283Z Wednesday 28 October 2026  14:50:29 -0300 (0:00:00.072)       0:00:34.270 ***** 
2026-10-28T17:50:29.3632805Z Wednesday 28 October 2026  14:50:29 -0300 (0:00:00.085)       0:00:34.355 ***** 
2026-10-28T17:50:29.6729685Z 
2026-10-28T17:50:29.6730226Z TASK [Check directory configuration exists] ************************************
2026-10-28T17:50:29.6730621Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config)
2026-10-28T17:50:29.9331012Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss)
2026-10-28T17:50:29.9621430Z Wednesday 28 October 2026  14:50:29 -0300 (0:00:00.598)       0:00:34.954 ***** 
2026-10-28T17:50:35.1210349Z 
2026-10-28T17:50:35.1210868Z TASK [Copiando arquivos para jboss.server.config.dir] **************************
2026-10-28T17:50:35.1213101Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss', u'stat': {u'charset': u'binary', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1793209686.2811842, u'block_size': 4096, u'inode': 599814663, u'isgid': False, u'size': 86, u'wgrp': False, u'executable': True, u'isuid': False, u'readable': True, u'isreg': False, u'version': u'18446744071576254824', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'inode/directory', u'blocks': 0, u'xoth': True, u'islnk': False, u'nlink': 3, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss/configuration', u'xusr': True, u'atime': 1793209687.3691704, u'isdir': True, u'ctime': 1793209686.2811842, u'isblk': False, u'xgrp': True, u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0755', u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss/configuration', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-28T17:50:35.1541916Z Wednesday 28 October 2026  14:50:35 -0300 (0:00:05.192)       0:00:40.146 ***** 
2026-10-28T17:50:35.4754914Z 
2026-10-28T17:50:35.4755623Z TASK [Get standalone-full-ha.xml status] ***************************************
2026-10-28T17:50:35.4755924Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config)
2026-10-28T17:50:35.7395715Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss)
2026-10-28T17:50:35.7685665Z Wednesday 28 October 2026  14:50:35 -0300 (0:00:00.614)       0:00:40.760 ***** 
2026-10-28T17:50:36.3443516Z 
2026-10-28T17:50:36.3444319Z TASK [Copiando arquivo standalone-full-ha.xml] *********************************
2026-10-28T17:50:36.3445884Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss', u'stat': {u'charset': u'us-ascii', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1793209687.38817, u'block_size': 4096, u'inode': 595605314, u'isgid': False, u'size': 37587, u'wgrp': False, u'executable': False, u'isuid': False, u'readable': True, u'isreg': True, u'version': u'18446744072103640675', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'application/xml', u'blocks': 80, u'xoth': False, u'islnk': False, u'nlink': 1, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss/standalone-full-ha.xml', u'xusr': False, u'atime': 1793209688.2741587, u'isdir': False, u'ctime': 1793209687.38817, u'isblk': False, u'checksum': u'fa4a2662b02ae34b61216425bbb53804dd4502b5', u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0644', u'xgrp': False, u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss/standalone-full-ha.xml', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-28T17:50:36.3781296Z Wednesday 28 October 2026  14:50:36 -0300 (0:00:00.609)       0:00:41.370 ***** 
2026-10-28T17:50:36.6966044Z 
2026-10-28T17:50:36.6967110Z TASK [Get standalone-ha.xml status] ********************************************
2026-10-28T17:50:36.6967884Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config)
2026-10-28T17:50:36.9604796Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss)
2026-10-28T17:50:36.9881019Z Wednesday 28 October 2026  14:50:36 -0300 (0:00:00.610)       0:00:41.980 ***** 
2026-10-28T17:50:37.0739114Z Wednesday 28 October 2026  14:50:37 -0300 (0:00:00.085)       0:00:42.065 ***** 
2026-10-28T17:50:37.3766483Z 
2026-10-28T17:50:37.3767068Z TASK [Get standalone.xml status] ***********************************************
2026-10-28T17:50:37.3767488Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config)
2026-10-28T17:50:37.6296744Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss)
2026-10-28T17:50:37.6585816Z Wednesday 28 October 2026  14:50:37 -0300 (0:00:00.584)       0:00:42.650 ***** 
2026-10-28T17:50:37.7455653Z Wednesday 28 October 2026  14:50:37 -0300 (0:00:00.086)       0:00:42.736 ***** 
2026-10-28T17:50:38.0378399Z 
2026-10-28T17:50:38.0378923Z TASK [Get standalone.conf status] **********************************************
2026-10-28T17:50:38.0379344Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config)
2026-10-28T17:50:38.2999107Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss)
2026-10-28T17:50:38.3290945Z Wednesday 28 October 2026  14:50:38 -0300 (0:00:00.584)       0:00:43.321 ***** 
2026-10-28T17:50:38.8961617Z 
2026-10-28T17:50:38.8962471Z TASK [Copiando arquivo standalone.conf] ****************************************
2026-10-28T17:50:38.8964412Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss', u'stat': {u'charset': u'us-ascii', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1793209687.39617, u'block_size': 4096, u'inode': 595605316, u'isgid': False, u'size': 3976, u'wgrp': False, u'executable': False, u'isuid': False, u'readable': True, u'isreg': True, u'version': u'602532546', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'text/plain', u'blocks': 8, u'xoth': False, u'islnk': False, u'nlink': 1, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss/standalone.conf', u'xusr': False, u'atime': 1793209687.39617, u'isdir': False, u'ctime': 1793209687.39617, u'isblk': False, u'checksum': u'd3f13d68f3ea0dd6506d8aec0c5e8f3c8ccddf38', u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0644', u'xgrp': False, u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/jboss/standalone.conf', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-28T17:50:38.9275891Z Wednesday 28 October 2026  14:50:38 -0300 (0:00:00.598)       0:00:43.919 ***** 
2026-10-28T17:50:39.2838358Z 
2026-10-28T17:50:39.2839140Z TASK [Restart Zabbix] **********************************************************
2026-10-28T17:50:39.2839778Z fatal: [caddeapllx2651.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "msg": "Could not find the requested service zabbix-agent: host"}
2026-10-28T17:50:39.2840082Z ...ignoring
2026-10-28T17:50:39.3135458Z Wednesday 28 October 2026  14:50:39 -0300 (0:00:00.385)       0:00:44.305 ***** 
2026-10-28T17:50:39.3796029Z Wednesday 28 October 2026  14:50:39 -0300 (0:00:00.066)       0:00:44.371 ***** 
2026-10-28T17:50:39.4153407Z [WARNING]: conditional statements should not include jinja2 templating
2026-10-28T17:50:39.4153858Z delimiters such as {{ }} or {% %}. Found: {{ lookup('env','HSM') |
2026-10-28T17:50:39.4154336Z default('false', true) | bool }}
2026-10-28T17:50:39.4247819Z Wednesday 28 October 2026  14:50:39 -0300 (0:00:00.045)       0:00:44.416 ***** 
2026-10-28T17:50:46.9471362Z 
2026-10-28T17:50:46.9472112Z RUNNING HANDLER [Restart Jboss] ************************************************
2026-10-28T17:50:46.9472321Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:46.9501157Z 
2026-10-28T17:50:46.9501658Z PLAY [jboss] *******************************************************************
2026-10-28T17:50:46.9537723Z 
2026-10-28T17:50:46.9538127Z PLAY [jboss] *******************************************************************
2026-10-28T17:50:46.9569578Z 
2026-10-28T17:50:46.9569994Z PLAY [jboss] *******************************************************************
2026-10-28T17:50:46.9856430Z Wednesday 28 October 2026  14:50:46 -0300 (0:00:07.560)       0:00:51.977 ***** 
2026-10-28T17:50:47.0412740Z 
2026-10-28T17:50:47.0413515Z TASK [Cria variável build_repository_name] *************************************
2026-10-28T17:50:47.0413702Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:47.0684921Z Wednesday 28 October 2026  14:50:47 -0300 (0:00:00.082)       0:00:52.060 ***** 
2026-10-28T17:50:47.1227811Z 
2026-10-28T17:50:47.1228618Z TASK [Buscando diretorio de config] ********************************************
2026-10-28T17:50:47.1228985Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:47.1549314Z Wednesday 28 October 2026  14:50:47 -0300 (0:00:00.086)       0:00:52.146 ***** 
2026-10-28T17:50:47.4675413Z 
2026-10-28T17:50:47.4676209Z TASK [Verifica se o arquivo {{ item }}/etc/hosts-{{ sistema_ambiente }} existe] ***
2026-10-28T17:50:47.4676503Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config)
2026-10-28T17:50:47.7228957Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/so)
2026-10-28T17:50:47.7511202Z Wednesday 28 October 2026  14:50:47 -0300 (0:00:00.596)       0:00:52.743 ***** 
2026-10-28T17:50:48.2098990Z 
2026-10-28T17:50:48.2099528Z TASK [Altera arquivo /etc/hosts] ***********************************************
2026-10-28T17:50:48.2101207Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r12326/a/_SICCP-intra-config', u'stat': {u'charset': u'us-ascii', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1793209686.2801843, u'block_size': 4096, u'inode': 587328805, u'isgid': False, u'size': 141, u'wgrp': False, u'executable': False, u'isuid': False, u'readable': True, u'isreg': True, u'version': u'18446744073039048849', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'text/plain', u'blocks': 8, u'xoth': False, u'islnk': False, u'nlink': 1, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/etc/hosts-des', u'xusr': False, u'atime': 1793209686.2801843, u'isdir': False, u'ctime': 1793209686.2801843, u'isblk': False, u'checksum': u'595cead82ca435bc6a45a58870a958603d6cf328', u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0644', u'xgrp': False, u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r12326/a/_SICCP-intra-config/etc/hosts-des', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-28T17:50:48.2168263Z 
2026-10-28T17:50:48.2168506Z PLAY [jboss] *******************************************************************
2026-10-28T17:50:48.2468064Z Wednesday 28 October 2026  14:50:48 -0300 (0:00:00.495)       0:00:53.238 ***** 
2026-10-28T17:50:48.5586084Z 
2026-10-28T17:50:48.5586816Z TASK [Verifica se o arquivo /opt/jboss-eap/standalone/configuration/custom.sh existe] ***
2026-10-28T17:50:48.5587014Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:48.5866595Z Wednesday 28 October 2026  14:50:48 -0300 (0:00:00.339)       0:00:53.578 ***** 
2026-10-28T17:50:50.7320380Z 
2026-10-28T17:50:50.7320931Z TASK [Executa shell customizada (jboss_home)] **********************************
2026-10-28T17:50:50.7321112Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:50.7613052Z Wednesday 28 October 2026  14:50:50 -0300 (0:00:02.174)       0:00:55.753 ***** 
2026-10-28T17:50:51.0883028Z 
2026-10-28T17:50:51.0883572Z TASK [Verifica se o arquivo /opt/batch/config/configuration/custom.sh existe] ***
2026-10-28T17:50:51.0883752Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T17:50:51.1156346Z Wednesday 28 October 2026  14:50:51 -0300 (0:00:00.354)       0:00:56.107 ***** 
2026-10-28T17:50:51.1550600Z 
2026-10-28T17:50:51.1551139Z PLAY [local] *******************************************************************
2026-10-28T17:50:51.1573866Z [WARNING]: Could not match supplied host pattern, ignoring: instance_restart
2026-10-28T17:50:51.1576705Z 
2026-10-28T17:50:51.1576864Z PLAY [instance_restart] ********************************************************
2026-10-28T17:50:51.1577170Z skipping: no hosts matched
2026-10-28T17:50:51.1580072Z [WARNING]: Could not match supplied host pattern, ignoring: machine_reboot
2026-10-28T17:50:51.1582730Z 
2026-10-28T17:50:51.1583297Z PLAY [machine_reboot] **********************************************************
2026-10-28T17:50:51.1583502Z skipping: no hosts matched
2026-10-28T17:50:51.1591797Z 
2026-10-28T17:50:51.1592113Z PLAY [local] *******************************************************************
2026-10-28T17:50:51.1613325Z [WARNING]: Could not match supplied host pattern, ignoring: instance_stop
2026-10-28T17:50:51.1615880Z 
2026-10-28T17:50:51.1616200Z PLAY [instance_stop] ***********************************************************
2026-10-28T17:50:51.1616364Z skipping: no hosts matched
2026-10-28T17:50:51.1619080Z 
2026-10-28T17:50:51.1619327Z PLAY [machine_reboot] **********************************************************
2026-10-28T17:50:51.1619504Z skipping: no hosts matched
2026-10-28T17:50:51.1627479Z 
2026-10-28T17:50:51.1627713Z PLAY [local] *******************************************************************
2026-10-28T17:50:51.1649080Z [WARNING]: Could not match supplied host pattern, ignoring: escopo_execucao
2026-10-28T17:50:51.1650835Z 
2026-10-28T17:50:51.1651436Z PLAY [Executar o Start do Sirot Connector no escopo definido] ******************
2026-10-28T17:50:51.1651635Z skipping: no hosts matched
2026-10-28T17:50:51.1657199Z 
2026-10-28T17:50:51.1657434Z PLAY [local] *******************************************************************
2026-10-28T17:50:51.1680540Z 
2026-10-28T17:50:51.1680813Z PLAY [Executar o Stop do Sirot Connector] **************************************
2026-10-28T17:50:51.1680964Z skipping: no hosts matched
2026-10-28T17:50:51.1688075Z 
2026-10-28T17:50:51.1688290Z PLAY [Configura TSM] ***********************************************************
2026-10-28T17:50:51.1712641Z 
2026-10-28T17:50:51.1713242Z PLAY [jboss] *******************************************************************
2026-10-28T17:50:51.1738766Z 
2026-10-28T17:50:51.1739212Z PLAY [Configura Control-M] *****************************************************
2026-10-28T17:50:51.1773191Z 
2026-10-28T17:50:51.1773530Z PLAY [jboss] *******************************************************************
2026-10-28T17:50:51.1812557Z 
2026-10-28T17:50:51.1812737Z PLAY [jboss] *******************************************************************
2026-10-28T17:50:51.1853802Z 
2026-10-28T17:50:51.1854265Z PLAY [jboss] *******************************************************************
2026-10-28T17:50:51.1875923Z 
2026-10-28T17:50:51.1876150Z PLAY [jboss] *******************************************************************
2026-10-28T17:50:51.1904931Z 
2026-10-28T17:50:51.1905158Z PLAY [localhost] ***************************************************************
2026-10-28T17:50:51.1928490Z 
2026-10-28T17:50:51.1928820Z PLAY [jboss] *******************************************************************
2026-10-28T17:50:51.1970399Z 
2026-10-28T17:50:51.1970798Z PLAY [jboss] *******************************************************************
2026-10-28T17:50:51.2008068Z 
2026-10-28T17:50:51.2008309Z PLAY [jboss] *******************************************************************
2026-10-28T17:50:51.2043064Z 
2026-10-28T17:50:51.2043449Z PLAY RECAP *********************************************************************
2026-10-28T17:50:51.2043670Z caddeapllx2651.agil.nprd.caixa.gov.br : ok=77   changed=14   unreachable=0    failed=0    skipped=18   rescued=0    ignored=3   
2026-10-28T17:50:51.2043763Z 
2026-10-28T17:50:51.2044089Z Wednesday 28 October 2026  14:50:51 -0300 (0:00:00.088)       0:00:56.196 ***** 
2026-10-28T17:50:51.2044273Z =============================================================================== 
2026-10-28T17:50:51.2045908Z nfs : Networker | Restart networker ------------------------------------ 10.45s
2026-10-28T17:50:51.2046169Z Restart Jboss ----------------------------------------------------------- 7.56s
2026-10-28T17:50:51.2046413Z Copiando arquivos para jboss.server.config.dir -------------------------- 5.19s
2026-10-28T17:50:51.2046659Z nfs : Instalando o NFS Client ------------------------------------------- 3.51s
2026-10-28T17:50:51.2046895Z Executa shell customizada (jboss_home) ---------------------------------- 2.17s
2026-10-28T17:50:51.2047138Z Gerando fatos de servicos ----------------------------------------------- 1.47s
2026-10-28T17:50:51.2047546Z nfs : Install networker lgtoclnt_url ------------------------------------ 0.97s
2026-10-28T17:50:51.2047789Z nfs : Networker | Start networker --------------------------------------- 0.91s
2026-10-28T17:50:51.2048020Z nfs : Install networker lgtonmda_url ------------------------------------ 0.84s
2026-10-28T17:50:51.2048265Z Create a symbolic link -------------------------------------------------- 0.80s
2026-10-28T17:50:51.2048501Z Realiza copia do arquivo de Trust Store --------------------------------- 0.78s
2026-10-28T17:50:51.2048744Z Copiando artefato (jboss-custom.cli) para o(s) servidor(es) Jboss ------- 0.65s
2026-10-28T17:50:51.2048982Z Gathering Facts --------------------------------------------------------- 0.63s
2026-10-28T17:50:51.2049231Z nfs : execute montagem script ------------------------------------------- 0.63s
2026-10-28T17:50:51.2049467Z maven_artifact ---------------------------------------------------------- 0.62s
2026-10-28T17:50:51.2049702Z Copiando artefatos para o(s) servidor(es) Jboss ------------------------- 0.61s
2026-10-28T17:50:51.2053006Z Get standalone-full-ha.xml status --------------------------------------- 0.61s
2026-10-28T17:50:51.2053298Z Get standalone-ha.xml status -------------------------------------------- 0.61s
2026-10-28T17:50:51.2053560Z Copiando arquivo standalone-full-ha.xml --------------------------------- 0.61s
2026-10-28T17:50:51.2053990Z Create a directory ------------------------------------------------------ 0.61s
2026-10-28T17:50:51.2054165Z Playbook run took 0 days, 0 hours, 0 minutes, 56 seconds
2026-10-28T17:50:51.2708378Z ##[section]Finishing: Deploy Config no JBOSS




sys     0m0,014s
[p585600@caddeapllx2651 ~]$ systemctl status sigdb --no-pager; ps -ef | grep -i [A]gtSigdb
● sigdb.service - SIGDB Agent
     Loaded: loaded (/etc/systemd/system/sigdb.service; enabled; preset: disabled)
     Active: active (running) since Wed 2026-10-28 14:52:21 -03; 42s ago
   Main PID: 212393 (AgtSigdb)
      Tasks: 3 (limit: 23083)
     Memory: 2.4M
        CPU: 12ms
     CGroup: /system.slice/sigdb.service
             └─212393 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
root      212393       1  0 14:52 ?        00:00:00 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
[p585600@caddeapllx2651 ~]$

