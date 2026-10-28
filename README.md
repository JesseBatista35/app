Solicitamos verificar a release do SICCP Intra que está travada desde ontem.

https://devops.caixa/projetos/Caixa/_releaseProgress?_a=release-environment-logs&releaseId=546592&environmentId=2540164


2026-10-28T14:10:33.8311666Z ##[section]Starting: Deploy Config no JBOSS
2026-10-28T14:10:33.8314996Z ==============================================================================
2026-10-28T14:10:33.8315077Z Task         : Bash
2026-10-28T14:10:33.8315122Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-28T14:10:33.8315196Z Version      : 3.227.0
2026-10-28T14:10:33.8315240Z Author       : Microsoft Corporation
2026-10-28T14:10:33.8315300Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-28T14:10:33.8315374Z ==============================================================================
2026-10-28T14:10:34.5499749Z Generating script.
2026-10-28T14:10:34.5510964Z ========================== Starting Command Output ===========================
2026-10-28T14:10:34.5526283Z [command]/bin/bash /opt/ads-agent/_work/_temp/408a1c05-88c5-41b9-b2b6-3b49fe1cbffb.sh
2026-10-28T14:10:34.5600587Z /opt/ads-agent/_work/_temp/408a1c05-88c5-41b9-b2b6-3b49fe1cbffb.sh: line 2: quantidade_vm: comando não encontrado
2026-10-28T14:10:34.5616587Z /opt/ads-agent/_work/_temp/408a1c05-88c5-41b9-b2b6-3b49fe1cbffb.sh: line 2: USE_WMQ: comando não encontrado
2026-10-28T14:10:36.8322836Z 
2026-10-28T14:10:36.8323422Z PLAY [local] *******************************************************************
2026-10-28T14:10:36.8629177Z 
2026-10-28T14:10:36.8629790Z PLAY [Configurando o DNS] ******************************************************
2026-10-28T14:10:37.0652712Z 
2026-10-28T14:10:37.0653272Z PLAY [local] *******************************************************************
2026-10-28T14:10:37.0695743Z 
2026-10-28T14:10:37.0696417Z PLAY [Verificando serviços] ****************************************************
2026-10-28T14:10:37.0787901Z 
2026-10-28T14:10:37.0788561Z PLAY [Configuração LDAP] *******************************************************
2026-10-28T14:10:37.0832378Z [WARNING]: Found variable using reserved name: when
2026-10-28T14:10:37.0840928Z 
2026-10-28T14:10:37.0841243Z PLAY [jboss] *******************************************************************
2026-10-28T14:10:37.0942459Z 
2026-10-28T14:10:37.0942994Z PLAY [Stack Jboss] *************************************************************
2026-10-28T14:10:37.1187521Z Wednesday 28 October 2026  11:10:37 -0300 (0:00:00.346)       0:00:00.346 ***** 
2026-10-28T14:10:37.6599057Z 
2026-10-28T14:10:37.6601607Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-10-28T14:10:37.6601990Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-28T14:10:37.6602231Z caddeapllx2651.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-28T14:10:37.6602434Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-28T14:10:37.6602604Z releases. A future Ansible release will default to using the discovered 
2026-10-28T14:10:37.6602771Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-28T14:10:37.6602936Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-28T14:10:37.6603130Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-28T14:10:37.6603276Z setting deprecation_warnings=False in ansible.cfg.
2026-10-28T14:10:37.6603411Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:37.6624941Z 
2026-10-28T14:10:37.6625425Z PLAY [jboss] *******************************************************************
2026-10-28T14:10:37.6700880Z Wednesday 28 October 2026  11:10:37 -0300 (0:00:00.551)       0:00:00.898 ***** 
2026-10-28T14:10:38.0552428Z 
2026-10-28T14:10:38.0552998Z TASK [Verifica se o arquivo nfs_config.json existe] ****************************
2026-10-28T14:10:38.0553162Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:38.0588018Z Wednesday 28 October 2026  11:10:38 -0300 (0:00:00.388)       0:00:01.287 ***** 
2026-10-28T14:10:38.1099623Z included: /opt/ads-agent/_work/r13477/a/esteira-jboss-vm-v2/roles/nfs/tasks/get_nfs.yml for caddeapllx2651.agil.nprd.caixa.gov.br
2026-10-28T14:10:38.1143630Z Wednesday 28 October 2026  11:10:38 -0300 (0:00:00.055)       0:00:01.342 ***** 
2026-10-28T14:10:38.1753874Z 
2026-10-28T14:10:38.1754806Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-28T14:10:38.1755071Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:38.1805896Z Wednesday 28 October 2026  11:10:38 -0300 (0:00:00.066)       0:00:01.408 ***** 
2026-10-28T14:10:38.6399507Z 
2026-10-28T14:10:38.6400298Z TASK [nfs : Coletar variáveis de ambiente] *************************************
2026-10-28T14:10:38.6400467Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:38.6434919Z Wednesday 28 October 2026  11:10:38 -0300 (0:00:00.462)       0:00:01.871 ***** 
2026-10-28T14:10:38.7004439Z 
2026-10-28T14:10:38.7004898Z TASK [nfs : Exibir resultado em JSON] ******************************************
2026-10-28T14:10:38.7005229Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T14:10:38.7005364Z     "nfs_vars_json": {
2026-10-28T14:10:38.7005857Z         "changed": false, 
2026-10-28T14:10:38.7006182Z         "cmd": "cat /opt/ads-agent/_work/r13477/a/nfs_config.json", 
2026-10-28T14:10:38.7006344Z         "delta": "0:00:00.006040", 
2026-10-28T14:10:38.7006526Z         "end": "2026-10-28 11:10:38.623048", 
2026-10-28T14:10:38.7006648Z         "failed": false, 
2026-10-28T14:10:38.7006754Z         "rc": 0, 
2026-10-28T14:10:38.7006923Z         "start": "2026-10-28 11:10:38.617008", 
2026-10-28T14:10:38.7007045Z         "stderr": "", 
2026-10-28T14:10:38.7007155Z         "stderr_lines": [], 
2026-10-28T14:10:38.7007297Z         "stdout": "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]", 
2026-10-28T14:10:38.7007446Z         "stdout_lines": [
2026-10-28T14:10:38.7007588Z             "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]"
2026-10-28T14:10:38.7007717Z         ]
2026-10-28T14:10:38.7007813Z     }
2026-10-28T14:10:38.7007918Z }
2026-10-28T14:10:38.7038328Z Wednesday 28 October 2026  11:10:38 -0300 (0:00:00.060)       0:00:01.932 ***** 
2026-10-28T14:10:38.7651624Z 
2026-10-28T14:10:38.7652229Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-28T14:10:38.7652396Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:38.7706259Z Wednesday 28 October 2026  11:10:38 -0300 (0:00:00.066)       0:00:01.999 ***** 
2026-10-28T14:10:39.4712369Z 
2026-10-28T14:10:39.4712910Z TASK [nfs : execute montagem script] *******************************************
2026-10-28T14:10:39.4713072Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:39.4750932Z Wednesday 28 October 2026  11:10:39 -0300 (0:00:00.704)       0:00:02.703 ***** 
2026-10-28T14:10:39.5359023Z 
2026-10-28T14:10:39.5359329Z TASK [nfs : ansible.builtin.debug] *********************************************
2026-10-28T14:10:39.5362017Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T14:10:39.5362154Z     "changed": false, 
2026-10-28T14:10:39.5362300Z     "msg": {
2026-10-28T14:10:39.5362411Z         "changed": true, 
2026-10-28T14:10:39.5362513Z         "cmd": [
2026-10-28T14:10:39.5362601Z             "python", 
2026-10-28T14:10:39.5362907Z             "/opt/ads-agent/_work/r13477/a/esteira-jboss-vm-v2/roles/nfs/files/nfs.py", 
2026-10-28T14:10:39.5363065Z             "montagem", 
2026-10-28T14:10:39.5363205Z             "siccp-intra", 
2026-10-28T14:10:39.5363309Z             "des", 
2026-10-28T14:10:39.5363411Z             "ctc_nprd", 
2026-10-28T14:10:39.5363593Z             "/opt/ads-agent/_work/r13477/a/esteira-jboss-vm-v2", 
2026-10-28T14:10:39.5363721Z             "C&t@d02", 
2026-10-28T14:10:39.5363909Z             "***", 
2026-10-28T14:10:39.5364020Z             "s736651@corp.caixa.gov.br", 
2026-10-28T14:10:39.5364137Z             "***", 
2026-10-28T14:10:39.5364378Z             "[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]"
2026-10-28T14:10:39.5364518Z         ], 
2026-10-28T14:10:39.5364955Z         "delta": "0:00:00.335438", 
2026-10-28T14:10:39.5365138Z         "end": "2026-10-28 11:10:39.452478", 
2026-10-28T14:10:39.5365269Z         "failed": false, 
2026-10-28T14:10:39.5365371Z         "rc": 0, 
2026-10-28T14:10:39.5365539Z         "start": "2026-10-28 11:10:39.117040", 
2026-10-28T14:10:39.5365646Z         "stderr": "", 
2026-10-28T14:10:39.5365752Z         "stderr_lines": [], 
2026-10-28T14:10:39.5366690Z         "stdout": "[{u'NFS_MOUNT_POINT_VM': u'/siccp', u'NFS_ENDPOINT_VM': u'hypernprd12.ad.caixa:/fs_siccp'}]\nNome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           \n------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------\nhypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                                \nnfs_path=/siccp\nnfs_src=hypernprd12.ad.caixa:/fs_siccp\nhypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                                ", 
2026-10-28T14:10:39.5367209Z         "stdout_lines": [
2026-10-28T14:10:39.5367441Z             "[{u'NFS_MOUNT_POINT_VM': u'/siccp', u'NFS_ENDPOINT_VM': u'hypernprd12.ad.caixa:/fs_siccp'}]", 
2026-10-28T14:10:39.5367611Z             "Nome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           ", 
2026-10-28T14:10:39.5367976Z             "------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------", 
2026-10-28T14:10:39.5368204Z             "hypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                                ", 
2026-10-28T14:10:39.5368345Z             "nfs_path=/siccp", 
2026-10-28T14:10:39.5368463Z             "nfs_src=hypernprd12.ad.caixa:/fs_siccp", 
2026-10-28T14:10:39.5368616Z             "hypernprd12.ad.caixa                /fs_siccp                           /siccp                              VM                                  hypernprd12.ad.caixa                des                                "
2026-10-28T14:10:39.5368743Z         ]
2026-10-28T14:10:39.5368834Z     }
2026-10-28T14:10:39.5368924Z }
2026-10-28T14:10:39.5394655Z Wednesday 28 October 2026  11:10:39 -0300 (0:00:00.064)       0:00:02.767 ***** 
2026-10-28T14:10:39.8059468Z 
2026-10-28T14:10:39.8059896Z TASK [nfs : execute clean json] ************************************************
2026-10-28T14:10:39.8060047Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:39.8092223Z Wednesday 28 October 2026  11:10:39 -0300 (0:00:00.269)       0:00:03.037 ***** 
2026-10-28T14:10:39.8682934Z 
2026-10-28T14:10:39.8683300Z TASK [nfs : result_new_string_json] ********************************************
2026-10-28T14:10:39.8684445Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T14:10:39.8684649Z     "msg": {
2026-10-28T14:10:39.8684767Z         "changed": true, 
2026-10-28T14:10:39.8685388Z         "cmd": "echo '[{\"NFS_ENDPOINT_VM\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT_VM\": \"/siccp\"}]' | sed 's/NFS_ENDPOINT_ISILON[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_ISILON[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_HUAWEI[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_HUAWEI[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_VM[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_VM[^\"]*/NFS_MOUNT_POINT/g'", 
2026-10-28T14:10:39.8686054Z         "delta": "0:00:00.003728", 
2026-10-28T14:10:39.8686239Z         "end": "2026-10-28 11:10:39.788192", 
2026-10-28T14:10:39.8686363Z         "failed": false, 
2026-10-28T14:10:39.8686472Z         "rc": 0, 
2026-10-28T14:10:39.8686658Z         "start": "2026-10-28 11:10:39.784464", 
2026-10-28T14:10:39.8686782Z         "stderr": "", 
2026-10-28T14:10:39.8686887Z         "stderr_lines": [], 
2026-10-28T14:10:39.8687034Z         "stdout": "[{\"NFS_ENDPOINT\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT\": \"/siccp\"}]", 
2026-10-28T14:10:39.8687181Z         "stdout_lines": [
2026-10-28T14:10:39.8687316Z             "[{\"NFS_ENDPOINT\": \"hypernprd12.ad.caixa:/fs_siccp\",\"NFS_MOUNT_POINT\": \"/siccp\"}]"
2026-10-28T14:10:39.8687432Z         ]
2026-10-28T14:10:39.8687524Z     }
2026-10-28T14:10:39.8687609Z }
2026-10-28T14:10:39.8717957Z Wednesday 28 October 2026  11:10:39 -0300 (0:00:00.062)       0:00:03.100 ***** 
2026-10-28T14:10:39.9311641Z 
2026-10-28T14:10:39.9312187Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-28T14:10:39.9312353Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:39.9351177Z Wednesday 28 October 2026  11:10:39 -0300 (0:00:00.063)       0:00:03.163 ***** 
2026-10-28T14:10:39.9950657Z 
2026-10-28T14:10:39.9951036Z TASK [nfs : result_new_json] ***************************************************
2026-10-28T14:10:39.9952099Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T14:10:39.9952275Z     "msg": [
2026-10-28T14:10:39.9952374Z         {
2026-10-28T14:10:39.9952511Z             "NFS_ENDPOINT": "hypernprd12.ad.caixa:/fs_siccp", 
2026-10-28T14:10:39.9952644Z             "NFS_MOUNT_POINT": "/siccp"
2026-10-28T14:10:39.9952744Z         }
2026-10-28T14:10:39.9952837Z     ]
2026-10-28T14:10:39.9952928Z }
2026-10-28T14:10:39.9984084Z Wednesday 28 October 2026  11:10:39 -0300 (0:00:00.063)       0:00:03.226 ***** 
2026-10-28T14:10:40.0611037Z included: /opt/ads-agent/_work/r13477/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx2651.agil.nprd.caixa.gov.br
2026-10-28T14:10:40.0670960Z Wednesday 28 October 2026  11:10:40 -0300 (0:00:00.068)       0:00:03.295 ***** 
2026-10-28T14:10:40.1240104Z 
2026-10-28T14:10:40.1240610Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-28T14:10:40.1240776Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:40.1271803Z Wednesday 28 October 2026  11:10:40 -0300 (0:00:00.060)       0:00:03.355 ***** 
2026-10-28T14:10:40.1832759Z 
2026-10-28T14:10:40.1833460Z TASK [nfs : debug] *************************************************************
2026-10-28T14:10:40.1833757Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T14:10:40.1833915Z     "msg": {
2026-10-28T14:10:40.1834092Z         "NFS_ENDPOINT": "hypernprd12.ad.caixa:/fs_siccp", 
2026-10-28T14:10:40.1834650Z         "NFS_MOUNT_POINT": "/siccp"
2026-10-28T14:10:40.1834777Z     }
2026-10-28T14:10:40.1834879Z }
2026-10-28T14:10:40.1864459Z Wednesday 28 October 2026  11:10:40 -0300 (0:00:00.059)       0:00:03.414 ***** 
2026-10-28T14:10:40.2418851Z 
2026-10-28T14:10:40.2420594Z TASK [nfs : debug] *************************************************************
2026-10-28T14:10:40.2421130Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T14:10:40.2421271Z     "msg": "/siccp"
2026-10-28T14:10:40.2421640Z }
2026-10-28T14:10:40.2452133Z Wednesday 28 October 2026  11:10:40 -0300 (0:00:00.058)       0:00:03.473 ***** 
2026-10-28T14:10:40.3003682Z 
2026-10-28T14:10:40.3004548Z TASK [nfs : debug] *************************************************************
2026-10-28T14:10:40.3004984Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T14:10:40.3005276Z     "msg": "hypernprd12.ad.caixa:/fs_siccp"
2026-10-28T14:10:40.3005397Z }
2026-10-28T14:10:40.3039366Z Wednesday 28 October 2026  11:10:40 -0300 (0:00:00.058)       0:00:03.532 ***** 
2026-10-28T14:10:40.3613162Z 
2026-10-28T14:10:40.3614013Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-28T14:10:40.3614186Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br] => {
2026-10-28T14:10:40.3614425Z     "changed": false, 
2026-10-28T14:10:40.3614546Z     "msg": "All assertions passed"
2026-10-28T14:10:40.3614649Z }
2026-10-28T14:10:40.3649112Z Wednesday 28 October 2026  11:10:40 -0300 (0:00:00.061)       0:00:03.593 ***** 
2026-10-28T14:10:43.8160170Z 
2026-10-28T14:10:43.8161067Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-28T14:10:43.8161302Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:43.8199105Z Wednesday 28 October 2026  11:10:43 -0300 (0:00:03.454)       0:00:07.048 ***** 
2026-10-28T14:10:44.7217316Z 
2026-10-28T14:10:44.7218369Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-28T14:10:44.7218619Z [WARNING]: Consider using the yum, dnf or zypper module rather than running
2026-10-28T14:10:44.7219032Z 'rpm'.  If you need to use command because yum, dnf or zypper is insufficient
2026-10-28T14:10:44.7219635Z you can add 'warn: false' to this command task or set 'command_warnings=False'
2026-10-28T14:10:44.7219793Z in ansible.cfg to get rid of this message.
2026-10-28T14:10:44.7222117Z fatal: [caddeapllx2651.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.635486", "end": "2026-10-28 11:10:44.705017", "msg": "non-zero return code", "rc": 1, "start": "2026-10-28 11:10:44.069531", "stderr": "aviso: /var/tmp/rpm-tmp.7pveoy: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.7pveoy: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtoclnt-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtoclnt-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-28T14:10:44.7223079Z ...ignoring
2026-10-28T14:10:44.7267138Z Wednesday 28 October 2026  11:10:44 -0300 (0:00:00.906)       0:00:07.955 ***** 
2026-10-28T14:10:45.5510874Z 
2026-10-28T14:10:45.5511697Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-28T14:10:45.5516756Z fatal: [caddeapllx2651.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": ["rpm", "-ivh", "--relocate", "/usr=/opt/networker", "http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm"], "delta": "0:00:00.576309", "end": "2026-10-28 11:10:45.533456", "msg": "non-zero return code", "rc": 1, "start": "2026-10-28 11:10:44.957147", "stderr": "aviso: /var/tmp/rpm-tmp.GW4wYg: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY\n\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado", "stderr_lines": ["aviso: /var/tmp/rpm-tmp.GW4wYg: Cabeçalho V3 RSA/SHA256 Signature, ID da chave ff48d101: NOKEY", "\to pacote lgtonmda-19.8.0.2-1.x86_64 já está instalado"], "stdout": "Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm\nVerifying...                          ########################################\nPreparando...                         ########################################", "stdout_lines": ["Obtendo http://10.122.154.12/deploy/lgtonmda-19.8.0.2-1.x86_64.rpm", "Verifying...                          ########################################", "Preparando...                         ########################################"]}
2026-10-28T14:10:45.5517392Z ...ignoring
2026-10-28T14:10:45.5554898Z Wednesday 28 October 2026  11:10:45 -0300 (0:00:00.828)       0:00:08.783 ***** 
2026-10-28T14:10:45.9719821Z 
2026-10-28T14:10:45.9720744Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-28T14:10:45.9720997Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:45.9763036Z Wednesday 28 October 2026  11:10:45 -0300 (0:00:00.420)       0:00:09.204 ***** 
2026-10-28T14:10:46.2275547Z 
2026-10-28T14:10:46.2276076Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-28T14:10:46.2276296Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:46.2314779Z Wednesday 28 October 2026  11:10:46 -0300 (0:00:00.255)       0:00:09.459 ***** 
2026-10-28T14:10:47.1663137Z 
2026-10-28T14:10:47.1664048Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-28T14:10:47.1664536Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:47.1710022Z Wednesday 28 October 2026  11:10:47 -0300 (0:00:00.939)       0:00:10.399 ***** 
2026-10-28T14:10:47.4293312Z 
2026-10-28T14:10:47.4294543Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-28T14:10:47.4295162Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:47.4328519Z Wednesday 28 October 2026  11:10:47 -0300 (0:00:00.261)       0:00:10.661 ***** 
2026-10-28T14:10:57.8508810Z 
2026-10-28T14:10:57.8509777Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-28T14:10:57.8510035Z changed: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:57.8542143Z Wednesday 28 October 2026  11:10:57 -0300 (0:00:10.421)       0:00:21.082 ***** 
2026-10-28T14:10:58.3232693Z 
2026-10-28T14:10:58.3233251Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-28T14:10:58.3233413Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:58.3273577Z Wednesday 28 October 2026  11:10:58 -0300 (0:00:00.473)       0:00:21.555 ***** 
2026-10-28T14:10:58.3714031Z 
2026-10-28T14:10:58.3714628Z PLAY [jboss] *******************************************************************
2026-10-28T14:10:58.3759388Z 
2026-10-28T14:10:58.3759689Z PLAY [jboss] *******************************************************************
2026-10-28T14:10:58.3800017Z Wednesday 28 October 2026  11:10:58 -0300 (0:00:00.052)       0:00:21.608 ***** 
2026-10-28T14:10:58.9910744Z 
2026-10-28T14:10:58.9911311Z TASK [Gathering Facts] *********************************************************
2026-10-28T14:10:58.9911485Z ok: [caddeapllx2651.agil.nprd.caixa.gov.br]
2026-10-28T14:10:59.0114531Z Wednesday 28 October 2026  11:10:59 -0300 (0:00:00.631)       0:00:22.239 ***** 
2026-10-28T14:34:59.5941275Z ##[error]The operation was canceled.
2026-10-28T14:34:59.5944089Z ##[section]Finishing: Deploy Config no JBOSS




Last login: Wed Oct 28 11:01:32 2026 from 10.211.12.27
[p585600@cadsvitrlx100 ~]$ ssh 10.116.201.111
p585600@10.116.201.111's password:
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ ps -ef | grep jboss
jboss      29106       1  0 out19 ?        00:00:00 /bin/sh /connector/exec-connector.sh
jboss      29126   29106  0 out19 ?        00:02:10 /connector/java-1.8.0-openjdk/jre//bin/java -server -classpath /connector/lib/ceflib2.0.5.jar:/connector/lib/connector-2.2.2.jar:/connector/lib/parser.jar:/connector/lib/xercesImpl.jar:/connector/lib/xml-apis.jar:/connector/lib/crimson.jar:/connector/lib/jaxp-api.jar:/connector/lib/ceflog2.0.1.jar:/connector/lib/mail.jar:/connector/lib/activation.jar:/connector/lib/sirotconEjb-lib_v2.2.7.jar:/connector/lib/log4j-1.2.8.jar:/connector/config:/connector/lib/jcert.jar:/connector/lib/jnet.jar:/connector/lib/jsse.jar:/connector/lib/ceflib2.0.5.jar:/connector/lib/connector-2.2.2.jar:/connector/lib/parser.jar:/connector/lib/xercesImpl.jar:/connector/lib/xml-apis.jar:/connector/lib/crimson.jar:/connector/lib/jaxp-api.jar:/connector/lib/ceflog2.0.1.jar:/connector/lib/mail.jar:/connector/lib/activation.jar:/connector/lib/sirotconEjb-lib_v2.2.7.jar:/connector/lib/log4j-1.2.8.jar:/connector/config:/connector/lib/jcert.jar:/connector/lib/jnet.jar:/connector/lib/jsse.jar: br.gov.caixa.sirot.connector.Connector /connector/config/connector.properties /connector/config/map.properties
root      150438       1  0 12:04 ?        00:00:00 runuser jboss -c LAUNCH_JBOSS_IN_BACKGROUND=1 JBOSS_PIDFILE=/opt/jboss-eap/standalone/tmp/jboss-eap-standalone.pid /opt/jboss-eap/bin/standalone.sh                -b 0.0.0.0                -bmanagement 0.0.0.0                -Djboss.server.base.dir=/opt/jboss-eap/standalone                -Djboss.server.log.dir=/logs/jboss/jboss-eap/standalone/siccp-intra -c standalone-full-ha.xml
jboss     150441  150438  0 12:04 ?        00:00:00 /bin/sh /opt/jboss-eap/bin/standalone.sh -b 0.0.0.0 -bmanagement 0.0.0.0 -Djboss.server.base.dir=/opt/jboss-eap/standalone -Djboss.server.log.dir=/logs/jboss/jboss-eap/standalone/siccp-intra -c standalone-full-ha.xml
jboss     150679  150441 18 12:04 ?        00:00:29 java -D[Standalone] -Xlog:gc*:file=/logs/jboss/jboss-eap/standalone/siccp-intra/gc.log:time,uptimemillis:filecount=5,filesize=3M -Djdk.serialFilter=maxbytes=10485760;maxdepth=128;maxarray=100000;maxrefs=300000 -Xms1024m -Xmx2048m -XX:MetaspaceSize=256m -XX:MaxMetaspaceSize=512m -Djava.net.preferIPv4Stack=true -Djavax.net.ssl.trustStore=/opt/jboss-eap/standalone/configuration/caixa-truststore-acteste-nprd.jks -Djboss.modules.system.pkgs=org.jboss.byteman,org.jboss.logmanager -Djava.awt.headless=true -Djboss.modules.policy-permissions=true -Djboss.as.management.blocking.timeout=900 -server -XX:+ExplicitGCInvokesConcurrent -XX:+UseG1GC -XX:MaxGCPauseMillis=500 -Xbootclasspath/a:/opt/jboss-eap/modules/system/layers/base/org/wildfly/common/main/wildfly-common-1.5.4.Final-redhat-00001.jar -Xbootclasspath/a:/opt/jboss-eap/modules/system/layers/base/org/jboss/logmanager/main/jboss-logmanager-2.1.18.Final-redhat-00001.jar -Dsun.util.logging.disableCallerCheck=true -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Djava.security.properties=/opt/jboss-eap/standalone/configuration/java.security --add-opens=java.base/java.lang=ALL-UNNAMED --add-opens=java.base/java.util=ALL-UNNAMED --add-exports=java.base/sun.nio.ch=ALL-UNNAMED --add-exports=jdk.unsupported/sun.misc=ALL-UNNAMED --add-exports=jdk.unsupported/sun.reflect=ALL-UNNAMED --add-exports=java.desktop/sun.awt=ALL-UNNAMED --add-exports=java.naming/com.sun.jndi.ldap=ALL-UNNAMED --add-exports=java.naming/com.sun.jndi.url.ldap=ALL-UNNAMED --add-exports=java.naming/com.sun.jndi.url.ldaps=ALL-UNNAMED --add-opens=java.base/java.lang=ALL-UNNAMED --add-opens=java.base/java.lang.invoke=ALL-UNNAMED --add-opens=java.base/java.lang.reflect=ALL-UNNAMED --add-opens=java.base/java.io=ALL-UNNAMED --add-opens=java.base/java.security=ALL-UNNAMED --add-opens=java.base/java.util=ALL-UNNAMED --add-opens=java.base/java.util.concurrent=ALL-UNNAMED --add-opens=java.management/javax.management=ALL-UNNAMED --add-opens=java.naming/javax.naming=ALL-UNNAMED -Dorg.jboss.boot.log.file=/logs/jboss/jboss-eap/standalone/siccp-intra/server.log -Dlogging.configuration=file:/opt/jboss-eap/standalone/configuration/logging.properties -jar /opt/jboss-eap/jboss-modules.jar -mp /opt/jboss-eap/modules:/opt/jboss-eap/modules-caixa org.jboss.as.standalone -Djboss.home.dir=/opt/jboss-eap -Djboss.server.base.dir=/opt/jboss-eap/standalone -b 0.0.0.0 -bmanagement 0.0.0.0 -Djboss.server.base.dir=/opt/jboss-eap/standalone -Djboss.server.log.dir=/logs/jboss/jboss-eap/standalone/siccp-intra -c standalone-full-ha.xml
p585600   150948  150921  0 12:06 pts/1    00:00:00 grep --color=auto jboss
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$

