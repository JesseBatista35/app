Fazer a verificação dos erros na release abaixo:



Suporte ao ambiente de aplicação nas esteiras DevOps
Qual o nome do Sistema?*:	siopi
Qual o ambiente*:	DES
Selecione a sua Comunidade*:	Habitação
Formas de contato*:	teams
Descrição da necessidade*:	Solicito a verificação dos erros na release abaixo:

2026-10-06T19:33:46.1629262Z ##[error]Bash exited with code '2'.
2026-10-06T19:33:46.1646876Z ##[section]Finishing: Deploy Config no JBOSS

https://devops.caixa/Legado/SIOPI/_releaseProgress?_a=release-environment-logs&releaseId=9870&environmentId=97329

Att.


2026-10-06T19:32:21.4776593Z ##[section]Starting: Deploy Config no JBOSS
2026-10-06T19:32:21.4779755Z ==============================================================================
2026-10-06T19:32:21.4779841Z Task         : Bash
2026-10-06T19:32:21.4779886Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-06T19:32:21.4779962Z Version      : 3.227.0
2026-10-06T19:32:21.4780008Z Author       : Microsoft Corporation
2026-10-06T19:32:21.4780061Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-06T19:32:21.4780145Z ==============================================================================
2026-10-06T19:32:22.5564113Z Generating script.
2026-10-06T19:32:22.5574309Z ========================== Starting Command Output ===========================
2026-10-06T19:32:22.5612887Z [command]/bin/bash /opt/ads-agent/_work/_temp/1e620e59-034d-4868-81de-088383d25c87.sh
2026-10-06T19:32:22.5659943Z /opt/ads-agent/_work/_temp/1e620e59-034d-4868-81de-088383d25c87.sh: line 2: quantidade_vm: comando não encontrado
2026-10-06T19:32:22.5674275Z /opt/ads-agent/_work/_temp/1e620e59-034d-4868-81de-088383d25c87.sh: line 2: USE_WMQ: comando não encontrado
2026-10-06T19:32:24.6073846Z 
2026-10-06T19:32:24.6074354Z PLAY [local] *******************************************************************
2026-10-06T19:32:24.6340387Z 
2026-10-06T19:32:24.6340895Z PLAY [Configurando o DNS] ******************************************************
2026-10-06T19:32:24.8217312Z 
2026-10-06T19:32:24.8217785Z PLAY [local] *******************************************************************
2026-10-06T19:32:24.8252128Z 
2026-10-06T19:32:24.8252629Z PLAY [Verificando serviços] ****************************************************
2026-10-06T19:32:24.8345274Z 
2026-10-06T19:32:24.8345610Z PLAY [Configuração LDAP] *******************************************************
2026-10-06T19:32:24.8378469Z [WARNING]: Found variable using reserved name: when
2026-10-06T19:32:24.8383889Z 
2026-10-06T19:32:24.8384042Z PLAY [jboss] *******************************************************************
2026-10-06T19:32:24.8475455Z 
2026-10-06T19:32:24.8475842Z PLAY [Stack Jboss] *************************************************************
2026-10-06T19:32:24.8710174Z Tuesday 06 October 2026  16:32:24 -0300 (0:00:00.323)       0:00:00.323 ******* 
2026-10-06T19:32:25.3422875Z 
2026-10-06T19:32:25.3423558Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-10-06T19:32:25.3424038Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:25.3445990Z 
2026-10-06T19:32:25.3446228Z PLAY [jboss] *******************************************************************
2026-10-06T19:32:25.3516522Z Tuesday 06 October 2026  16:32:25 -0300 (0:00:00.480)       0:00:00.803 ******* 
2026-10-06T19:32:25.7660449Z 
2026-10-06T19:32:25.7660959Z TASK [Verifica se o arquivo nfs_config.json existe] ****************************
2026-10-06T19:32:25.7661123Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:25.7694963Z Tuesday 06 October 2026  16:32:25 -0300 (0:00:00.417)       0:00:01.221 ******* 
2026-10-06T19:32:25.8158206Z included: /opt/ads-agent/_work/r12246/a/esteira-jboss-vm-v2/roles/nfs/tasks/get_nfs.yml for caddeapllx1537.agil.nprd.caixa.gov.br
2026-10-06T19:32:25.8203249Z Tuesday 06 October 2026  16:32:25 -0300 (0:00:00.050)       0:00:01.272 ******* 
2026-10-06T19:32:25.8784560Z 
2026-10-06T19:32:25.8785315Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-06T19:32:25.8785923Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:25.8863785Z Tuesday 06 October 2026  16:32:25 -0300 (0:00:00.062)       0:00:01.335 ******* 
2026-10-06T19:32:26.3716885Z 
2026-10-06T19:32:26.3717961Z TASK [nfs : Coletar variáveis de ambiente] *************************************
2026-10-06T19:32:26.3718590Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:26.3750802Z Tuesday 06 October 2026  16:32:26 -0300 (0:00:00.491)       0:00:01.827 ******* 
2026-10-06T19:32:26.4356838Z 
2026-10-06T19:32:26.4357883Z TASK [nfs : Exibir resultado em JSON] ******************************************
2026-10-06T19:32:26.4360651Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => {
2026-10-06T19:32:26.4361009Z     "nfs_vars_json": {
2026-10-06T19:32:26.4361599Z         "changed": false, 
2026-10-06T19:32:26.4361951Z         "cmd": "cat /opt/ads-agent/_work/r12246/a/nfs_config.json", 
2026-10-06T19:32:26.4362105Z         "delta": "0:00:00.043808", 
2026-10-06T19:32:26.4362282Z         "end": "2026-10-06 16:32:26.351984", 
2026-10-06T19:32:26.4362404Z         "failed": false, 
2026-10-06T19:32:26.4362519Z         "rc": 0, 
2026-10-06T19:32:26.4362674Z         "start": "2026-10-06 16:32:26.308176", 
2026-10-06T19:32:26.4362905Z         "stderr": "", 
2026-10-06T19:32:26.4363026Z         "stderr_lines": [], 
2026-10-06T19:32:26.4363196Z         "stdout": "[{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI\",\"NFS_MOUNT_POINT_ISILON\": \"/opt/sistemas\"}]", 
2026-10-06T19:32:26.4363365Z         "stdout_lines": [
2026-10-06T19:32:26.4363524Z             "[{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI\",\"NFS_MOUNT_POINT_ISILON\": \"/opt/sistemas\"}]"
2026-10-06T19:32:26.4363660Z         ]
2026-10-06T19:32:26.4363750Z     }
2026-10-06T19:32:26.4363837Z }
2026-10-06T19:32:26.4389909Z Tuesday 06 October 2026  16:32:26 -0300 (0:00:00.063)       0:00:01.891 ******* 
2026-10-06T19:32:26.4987831Z 
2026-10-06T19:32:26.4988427Z TASK [nfs : Criar variáveis] ***************************************************
2026-10-06T19:32:26.4988594Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:26.5035640Z Tuesday 06 October 2026  16:32:26 -0300 (0:00:00.064)       0:00:01.955 ******* 
2026-10-06T19:32:28.7476521Z 
2026-10-06T19:32:28.7477289Z TASK [nfs : execute montagem script] *******************************************
2026-10-06T19:32:28.7478028Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:28.7510823Z Tuesday 06 October 2026  16:32:28 -0300 (0:00:02.247)       0:00:04.203 ******* 
2026-10-06T19:32:28.8096474Z 
2026-10-06T19:32:28.8096956Z TASK [nfs : ansible.builtin.debug] *********************************************
2026-10-06T19:32:28.8100965Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => {
2026-10-06T19:32:28.8101091Z     "changed": false, 
2026-10-06T19:32:28.8101361Z     "msg": {
2026-10-06T19:32:28.8101553Z         "changed": true, 
2026-10-06T19:32:28.8101665Z         "cmd": [
2026-10-06T19:32:28.8101811Z             "python", 
2026-10-06T19:32:28.8103084Z             "/opt/ads-agent/_work/r12246/a/esteira-jboss-vm-v2/roles/nfs/files/nfs.py", 
2026-10-06T19:32:28.8103557Z             "montagem", 
2026-10-06T19:32:28.8103856Z             "siopi-ws-2", 
2026-10-06T19:32:28.8104228Z             "des", 
2026-10-06T19:32:28.8104426Z             "ctc_nprd", 
2026-10-06T19:32:28.8104677Z             "/opt/ads-agent/_work/r12246/a/esteira-jboss-vm-v2", 
2026-10-06T19:32:28.8104856Z             "C&t@d02", 
2026-10-06T19:32:28.8105007Z             "@ut0m@c@0!", 
2026-10-06T19:32:28.8105165Z             "s736651@corp.caixa.gov.br", 
2026-10-06T19:32:28.8105316Z             "8As4jL6Q", 
2026-10-06T19:32:28.8105546Z             "[{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI\",\"NFS_MOUNT_POINT_ISILON\": \"/opt/sistemas\"}]"
2026-10-06T19:32:28.8105763Z         ], 
2026-10-06T19:32:28.8105927Z         "delta": "0:00:01.906311", 
2026-10-06T19:32:28.8106167Z         "end": "2026-10-06 16:32:28.729794", 
2026-10-06T19:32:28.8106326Z         "failed": false, 
2026-10-06T19:32:28.8106471Z         "rc": 0, 
2026-10-06T19:32:28.8106692Z         "start": "2026-10-06 16:32:26.823483", 
2026-10-06T19:32:28.8106865Z         "stderr": "", 
2026-10-06T19:32:28.8107009Z         "stderr_lines": [], 
2026-10-06T19:32:28.8108687Z         "stdout": "[{u'NFS_MOUNT_POINT_ISILON': u'/opt/sistemas', u'NFS_ENDPOINT_ISILON': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI'}]\nNome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           \n------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI /opt/sistemas                       ISILON                              nfsctcnprd.ctc.caixa                des                                \nException when callin ProtocolsApi->get_nfs_expor: (500)\nReason: Internal Server Error\nHTTP response headers: HTTPHeaderDict({'Transfer-Encoding': 'chunked', 'Server': 'Apache', 'Connection': 'close', 'Allow': 'GET, PUT, DELETE, HEAD', 'Date': 'Tue, 06 Oct 2026 19:32:27 GMT', 'X-Frame-Options': 'sameorigin', 'Content-Type': 'application/json'})\nHTTP response body: \n{\n\"errors\" : \n[\n\n{\n\"code\" : \"AEC_EXCEPTION\",\n\"message\" : \"bad hostname 192.168.236.109,10.188.254.80\"\n}\n]\n}\n\n\n\nnfs_path=/opt/sistemas\nnfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI\nnfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI /opt/sistemas                       ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-06T19:32:28.8109511Z         "stdout_lines": [
2026-10-06T19:32:28.8109774Z             "[{u'NFS_MOUNT_POINT_ISILON': u'/opt/sistemas', u'NFS_ENDPOINT_ISILON': u'nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI'}]", 
2026-10-06T19:32:28.8109962Z             "Nome                                Endpoint                            Mountpoint                          Tipo                                Ip                                  Ambiente                           ", 
2026-10-06T19:32:28.8110318Z             "------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------", 
2026-10-06T19:32:28.8110556Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI /opt/sistemas                       ISILON                              nfsctcnprd.ctc.caixa                des                                ", 
2026-10-06T19:32:28.8110792Z             "Exception when callin ProtocolsApi->get_nfs_expor: (500)", 
2026-10-06T19:32:28.8110933Z             "Reason: Internal Server Error", 
2026-10-06T19:32:28.8111335Z             "HTTP response headers: HTTPHeaderDict({'Transfer-Encoding': 'chunked', 'Server': 'Apache', 'Connection': 'close', 'Allow': 'GET, PUT, DELETE, HEAD', 'Date': 'Tue, 06 Oct 2026 19:32:27 GMT', 'X-Frame-Options': 'sameorigin', 'Content-Type': 'application/json'})", 
2026-10-06T19:32:28.8111611Z             "HTTP response body: ", 
2026-10-06T19:32:28.8111715Z             "{", 
2026-10-06T19:32:28.8111807Z             "\"errors\" : ", 
2026-10-06T19:32:28.8111901Z             "[", 
2026-10-06T19:32:28.8111989Z             "", 
2026-10-06T19:32:28.8112080Z             "{", 
2026-10-06T19:32:28.8112170Z             "\"code\" : \"AEC_EXCEPTION\",", 
2026-10-06T19:32:28.8112298Z             "\"message\" : \"bad hostname 192.168.236.109,10.188.254.80\"", 
2026-10-06T19:32:28.8112413Z             "}", 
2026-10-06T19:32:28.8112517Z             "]", 
2026-10-06T19:32:28.8112602Z             "}", 
2026-10-06T19:32:28.8112691Z             "", 
2026-10-06T19:32:28.8112851Z             "", 
2026-10-06T19:32:28.8112942Z             "", 
2026-10-06T19:32:28.8113046Z             "nfs_path=/opt/sistemas", 
2026-10-06T19:32:28.8113183Z             "nfs_src=nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI", 
2026-10-06T19:32:28.8113366Z             "nfsctcnprd.ctc.caixa                /ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI /opt/sistemas                       ISILON                              nfsctcnprd.ctc.caixa                des                                "
2026-10-06T19:32:28.8113568Z         ]
2026-10-06T19:32:28.8113651Z     }
2026-10-06T19:32:28.8113736Z }
2026-10-06T19:32:28.8154651Z Tuesday 06 October 2026  16:32:28 -0300 (0:00:00.062)       0:00:04.265 ******* 
2026-10-06T19:32:29.0774638Z 
2026-10-06T19:32:29.0775483Z TASK [nfs : execute clean json] ************************************************
2026-10-06T19:32:29.0776187Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:29.0848119Z Tuesday 06 October 2026  16:32:29 -0300 (0:00:00.268)       0:00:04.534 ******* 
2026-10-06T19:32:29.1544838Z 
2026-10-06T19:32:29.1545626Z TASK [nfs : result_new_string_json] ********************************************
2026-10-06T19:32:29.1551299Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => {
2026-10-06T19:32:29.1551476Z     "msg": {
2026-10-06T19:32:29.1551587Z         "changed": true, 
2026-10-06T19:32:29.1552487Z         "cmd": "echo '[{\"NFS_ENDPOINT_ISILON\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI\",\"NFS_MOUNT_POINT_ISILON\": \"/opt/sistemas\"}]' | sed 's/NFS_ENDPOINT_ISILON[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_ISILON[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_HUAWEI[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_HUAWEI[^\"]*/NFS_MOUNT_POINT/g; s/NFS_ENDPOINT_VM[^\"]*/NFS_ENDPOINT/g; s/NFS_MOUNT_POINT_VM[^\"]*/NFS_MOUNT_POINT/g'", 
2026-10-06T19:32:29.1552917Z         "delta": "0:00:00.008844", 
2026-10-06T19:32:29.1553119Z         "end": "2026-10-06 16:32:29.062521", 
2026-10-06T19:32:29.1553241Z         "failed": false, 
2026-10-06T19:32:29.1553349Z         "rc": 0, 
2026-10-06T19:32:29.1553517Z         "start": "2026-10-06 16:32:29.053677", 
2026-10-06T19:32:29.1553638Z         "stderr": "", 
2026-10-06T19:32:29.1553738Z         "stderr_lines": [], 
2026-10-06T19:32:29.1553906Z         "stdout": "[{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI\",\"NFS_MOUNT_POINT\": \"/opt/sistemas\"}]", 
2026-10-06T19:32:29.1554065Z         "stdout_lines": [
2026-10-06T19:32:29.1554230Z             "[{\"NFS_ENDPOINT\": \"nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI\",\"NFS_MOUNT_POINT\": \"/opt/sistemas\"}]"
2026-10-06T19:32:29.1554379Z         ]
2026-10-06T19:32:29.1554461Z     }
2026-10-06T19:32:29.1554554Z }
2026-10-06T19:32:29.1597129Z Tuesday 06 October 2026  16:32:29 -0300 (0:00:00.077)       0:00:04.611 ******* 
2026-10-06T19:32:29.2331907Z 
2026-10-06T19:32:29.2332271Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-06T19:32:29.2333030Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:29.2370423Z Tuesday 06 October 2026  16:32:29 -0300 (0:00:00.077)       0:00:04.689 ******* 
2026-10-06T19:32:29.3113172Z 
2026-10-06T19:32:29.3113849Z TASK [nfs : result_new_json] ***************************************************
2026-10-06T19:32:29.3114249Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => {
2026-10-06T19:32:29.3114415Z     "msg": [
2026-10-06T19:32:29.3114514Z         {
2026-10-06T19:32:29.3114666Z             "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI", 
2026-10-06T19:32:29.3116800Z             "NFS_MOUNT_POINT": "/opt/sistemas"
2026-10-06T19:32:29.3117239Z         }
2026-10-06T19:32:29.3117590Z     ]
2026-10-06T19:32:29.3118153Z }
2026-10-06T19:32:29.3159787Z Tuesday 06 October 2026  16:32:29 -0300 (0:00:00.078)       0:00:04.767 ******* 
2026-10-06T19:32:29.3952660Z included: /opt/ads-agent/_work/r12246/a/esteira-jboss-vm-v2/roles/nfs/tasks/stack_nfs.yml for caddeapllx1537.agil.nprd.caixa.gov.br
2026-10-06T19:32:29.4010898Z Tuesday 06 October 2026  16:32:29 -0300 (0:00:00.085)       0:00:04.853 ******* 
2026-10-06T19:32:29.4561968Z 
2026-10-06T19:32:29.4562667Z TASK [nfs : Parse JSON data] ***************************************************
2026-10-06T19:32:29.4563392Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:29.4591583Z Tuesday 06 October 2026  16:32:29 -0300 (0:00:00.058)       0:00:04.911 ******* 
2026-10-06T19:32:29.5133091Z 
2026-10-06T19:32:29.5133434Z TASK [nfs : debug] *************************************************************
2026-10-06T19:32:29.5136984Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => {
2026-10-06T19:32:29.5137355Z     "msg": {
2026-10-06T19:32:29.5137706Z         "NFS_ENDPOINT": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI", 
2026-10-06T19:32:29.5137880Z         "NFS_MOUNT_POINT": "/opt/sistemas"
2026-10-06T19:32:29.5137998Z     }
2026-10-06T19:32:29.5139663Z }
2026-10-06T19:32:29.5164515Z Tuesday 06 October 2026  16:32:29 -0300 (0:00:00.057)       0:00:04.968 ******* 
2026-10-06T19:32:29.5693705Z 
2026-10-06T19:32:29.5694085Z TASK [nfs : debug] *************************************************************
2026-10-06T19:32:29.5694856Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => {
2026-10-06T19:32:29.5695086Z     "msg": "/opt/sistemas"
2026-10-06T19:32:29.5695199Z }
2026-10-06T19:32:29.5725038Z Tuesday 06 October 2026  16:32:29 -0300 (0:00:00.055)       0:00:05.024 ******* 
2026-10-06T19:32:29.6250367Z 
2026-10-06T19:32:29.6250653Z TASK [nfs : debug] *************************************************************
2026-10-06T19:32:29.6251289Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => {
2026-10-06T19:32:29.6251479Z     "msg": "nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CETAD/SIOPI"
2026-10-06T19:32:29.6251599Z }
2026-10-06T19:32:29.6284160Z Tuesday 06 October 2026  16:32:29 -0300 (0:00:00.055)       0:00:05.080 ******* 
2026-10-06T19:32:29.6835333Z 
2026-10-06T19:32:29.6835685Z TASK [nfs : Verificando as variaveis] ******************************************
2026-10-06T19:32:29.6836260Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => {
2026-10-06T19:32:29.6836421Z     "changed": false, 
2026-10-06T19:32:29.6836550Z     "msg": "All assertions passed"
2026-10-06T19:32:29.6836713Z }
2026-10-06T19:32:29.6867852Z Tuesday 06 October 2026  16:32:29 -0300 (0:00:00.058)       0:00:05.138 ******* 
2026-10-06T19:32:37.2227263Z 
2026-10-06T19:32:37.2228158Z TASK [nfs : Instalando o NFS Client] *******************************************
2026-10-06T19:32:37.2228410Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:37.2264085Z Tuesday 06 October 2026  16:32:37 -0300 (0:00:07.539)       0:00:12.678 ******* 
2026-10-06T19:32:39.3025973Z 
2026-10-06T19:32:39.3026526Z TASK [nfs : Install networker lgtoclnt_url] ************************************
2026-10-06T19:32:39.3027170Z [WARNING]: Consider using the yum, dnf or zypper module rather than running
2026-10-06T19:32:39.3027526Z 'rpm'.  If you need to use command because yum, dnf or zypper is insufficient
2026-10-06T19:32:39.3027747Z you can add 'warn: false' to this command task or set 'command_warnings=False'
2026-10-06T19:32:39.3027897Z in ansible.cfg to get rid of this message.
2026-10-06T19:32:39.3028265Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:39.3061993Z Tuesday 06 October 2026  16:32:39 -0300 (0:00:02.079)       0:00:14.758 ******* 
2026-10-06T19:32:41.3104259Z 
2026-10-06T19:32:41.3104768Z TASK [nfs : Install networker lgtonmda_url] ************************************
2026-10-06T19:32:41.3168213Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:41.3168633Z Tuesday 06 October 2026  16:32:41 -0300 (0:00:02.008)       0:00:16.766 ******* 
2026-10-06T19:32:41.7164862Z 
2026-10-06T19:32:41.7165690Z TASK [nfs : Remove pacote jbcs-httpd] ******************************************
2026-10-06T19:32:41.7165890Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:41.7199000Z Tuesday 06 October 2026  16:32:41 -0300 (0:00:00.405)       0:00:17.171 ******* 
2026-10-06T19:32:41.9761174Z 
2026-10-06T19:32:41.9763777Z TASK [nfs : Create a symbolic link] ********************************************
2026-10-06T19:32:41.9765802Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:41.9795503Z Tuesday 06 October 2026  16:32:41 -0300 (0:00:00.259)       0:00:17.431 ******* 
2026-10-06T19:32:42.9947837Z 
2026-10-06T19:32:42.9948520Z TASK [nfs : Networker | Start networker] ***************************************
2026-10-06T19:32:42.9949417Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:42.9985733Z Tuesday 06 October 2026  16:32:42 -0300 (0:00:01.019)       0:00:18.450 ******* 
2026-10-06T19:32:43.2602562Z 
2026-10-06T19:32:43.2603514Z TASK [nfs : Executar o comando abaixo para limitar as portas] ******************
2026-10-06T19:32:43.2603747Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:32:43.2634950Z Tuesday 06 October 2026  16:32:43 -0300 (0:00:00.264)       0:00:18.715 ******* 
2026-10-06T19:33:03.7675015Z 
2026-10-06T19:33:03.7675701Z TASK [nfs : Networker | Restart networker] *************************************
2026-10-06T19:33:03.7675976Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:03.7707375Z Tuesday 06 October 2026  16:33:03 -0300 (0:00:20.507)       0:00:39.222 ******* 
2026-10-06T19:33:04.4193293Z 
2026-10-06T19:33:04.4193755Z TASK [nfs : Montando volume remoto] ********************************************
2026-10-06T19:33:04.4225930Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:04.4226370Z Tuesday 06 October 2026  16:33:04 -0300 (0:00:00.651)       0:00:39.874 ******* 
2026-10-06T19:33:04.4649484Z 
2026-10-06T19:33:04.4649829Z PLAY [jboss] *******************************************************************
2026-10-06T19:33:04.4692485Z 
2026-10-06T19:33:04.4693125Z PLAY [jboss] *******************************************************************
2026-10-06T19:33:04.4731255Z Tuesday 06 October 2026  16:33:04 -0300 (0:00:00.050)       0:00:39.925 ******* 
2026-10-06T19:33:05.2512493Z 
2026-10-06T19:33:05.2513126Z TASK [Gathering Facts] *********************************************************
2026-10-06T19:33:05.2513285Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:05.2705920Z Tuesday 06 October 2026  16:33:05 -0300 (0:00:00.797)       0:00:40.722 ******* 
2026-10-06T19:33:06.7216859Z 
2026-10-06T19:33:06.7217375Z TASK [Gerando fatos de servicos] ***********************************************
2026-10-06T19:33:06.7217541Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:06.7544828Z Tuesday 06 October 2026  16:33:06 -0300 (0:00:01.483)       0:00:42.206 ******* 
2026-10-06T19:33:06.8136496Z 
2026-10-06T19:33:06.8136887Z TASK [Gerando lista de units jboss] ********************************************
2026-10-06T19:33:06.8137045Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:06.8415805Z Tuesday 06 October 2026  16:33:06 -0300 (0:00:00.086)       0:00:42.293 ******* 
2026-10-06T19:33:06.9107227Z Tuesday 06 October 2026  16:33:06 -0300 (0:00:00.069)       0:00:42.362 ******* 
2026-10-06T19:33:06.9228745Z 
2026-10-06T19:33:06.9229086Z PLAY [Copiando deployments adicionais] *****************************************
2026-10-06T19:33:06.9514757Z Tuesday 06 October 2026  16:33:06 -0300 (0:00:00.040)       0:00:42.403 ******* 
2026-10-06T19:33:07.0067906Z 
2026-10-06T19:33:07.0068864Z TASK [Cria variável build_repository_name] *************************************
2026-10-06T19:33:07.0069386Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:07.0341130Z Tuesday 06 October 2026  16:33:07 -0300 (0:00:00.082)       0:00:42.486 ******* 
2026-10-06T19:33:07.0882249Z 
2026-10-06T19:33:07.0883403Z TASK [Buscando diretorio de config] ********************************************
2026-10-06T19:33:07.0883620Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:07.1171246Z Tuesday 06 October 2026  16:33:07 -0300 (0:00:00.082)       0:00:42.569 ******* 
2026-10-06T19:33:07.1710696Z 
2026-10-06T19:33:07.1711190Z TASK [Buscando diretorio de config] ********************************************
2026-10-06T19:33:07.1711551Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:07.2042117Z Tuesday 06 October 2026  16:33:07 -0300 (0:00:00.087)       0:00:42.656 ******* 
2026-10-06T19:33:07.6900469Z 
2026-10-06T19:33:07.6901224Z TASK [Create a symbolic link] **************************************************
2026-10-06T19:33:07.6901658Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config)
2026-10-06T19:33:07.9705479Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/jboss)
2026-10-06T19:33:08.0016908Z Tuesday 06 October 2026  16:33:08 -0300 (0:00:00.797)       0:00:43.453 ******* 
2026-10-06T19:33:08.4144688Z 
2026-10-06T19:33:08.4145216Z TASK [Verifica se o arquivo  existe] *******************************************
2026-10-06T19:33:08.4145605Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config)
2026-10-06T19:33:08.6841080Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/jboss)
2026-10-06T19:33:08.7125085Z Tuesday 06 October 2026  16:33:08 -0300 (0:00:00.710)       0:00:44.164 ******* 
2026-10-06T19:33:08.8009979Z included: /opt/ads-agent/_work/r12246/a/esteira-jboss-vm-v2/roles/jboss/tasks/stack_deployments_custom_block.yml for caddeapllx1537.agil.nprd.caixa.gov.br
2026-10-06T19:33:08.8307101Z Tuesday 06 October 2026  16:33:08 -0300 (0:00:00.118)       0:00:44.282 ******* 
2026-10-06T19:33:09.2977504Z 
2026-10-06T19:33:09.2978321Z TASK [Lendo artefatos do arquivo CSV] ******************************************
2026-10-06T19:33:09.2978689Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:09.3276873Z Tuesday 06 October 2026  16:33:09 -0300 (0:00:00.496)       0:00:44.779 ******* 
2026-10-06T19:33:09.3359096Z [WARNING]: The loop variable 'item' is already in use. You should set the
2026-10-06T19:33:09.3359490Z `loop_var` value in the `loop_control` option for the task to something else to
2026-10-06T19:33:09.3359976Z avoid variable collisions and unexpected behavior.
2026-10-06T19:33:09.3732953Z 
2026-10-06T19:33:09.3733349Z TASK [Mostra artefatos] ********************************************************
2026-10-06T19:33:09.3735284Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item={u'version': u'9.3.3.0', u'group_id': u'br.gov.caixa.wmq.jmsra', u'extension': u'rar', u'artifact_id': u'wmq.jmsra'}) => {
2026-10-06T19:33:09.3735720Z     "msg": "Artefato: wmq.jmsra - versao 9.3.3.0"
2026-10-06T19:33:09.3736165Z }
2026-10-06T19:33:09.4027039Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item={u'version': u'1.1.1', u'group_id': u'br.gov.caixa', u'extension': u'jar', u'artifact_id': u'framework'}) => {
2026-10-06T19:33:09.4027487Z     "msg": "Artefato: framework - versao 1.1.1"
2026-10-06T19:33:09.4027727Z }
2026-10-06T19:33:09.4329566Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item={u'version': u'3.3.1', u'group_id': u'com.microsoft.azure', u'extension': u'jar', u'artifact_id': u'applicationinsights-agent'}) => {
2026-10-06T19:33:09.4330161Z     "msg": "Artefato: applicationinsights-agent - versao 3.3.1"
2026-10-06T19:33:09.4330686Z }
2026-10-06T19:33:09.4649640Z Tuesday 06 October 2026  16:33:09 -0300 (0:00:00.137)       0:00:44.916 ******* 
2026-10-06T19:33:10.1448552Z 
2026-10-06T19:33:10.1449422Z TASK [maven_artifact] **********************************************************
2026-10-06T19:33:10.1449995Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item={u'version': u'9.3.3.0', u'group_id': u'br.gov.caixa.wmq.jmsra', u'extension': u'rar', u'artifact_id': u'wmq.jmsra'})
2026-10-06T19:33:10.5150380Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item={u'version': u'1.1.1', u'group_id': u'br.gov.caixa', u'extension': u'jar', u'artifact_id': u'framework'})
2026-10-06T19:33:11.0452246Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item={u'version': u'3.3.1', u'group_id': u'com.microsoft.azure', u'extension': u'jar', u'artifact_id': u'applicationinsights-agent'})
2026-10-06T19:33:11.0753370Z Tuesday 06 October 2026  16:33:11 -0300 (0:00:01.610)       0:00:46.527 ******* 
2026-10-06T19:33:14.7325978Z 
2026-10-06T19:33:14.7326574Z TASK [Copiando artefatos para o(s) servidor(es) Jboss] *************************
2026-10-06T19:33:14.7326894Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:14.7600688Z Tuesday 06 October 2026  16:33:14 -0300 (0:00:03.684)       0:00:50.212 ******* 
2026-10-06T19:33:14.8016870Z 
2026-10-06T19:33:14.8017255Z PLAY [Copiando modules adicionais] *********************************************
2026-10-06T19:33:14.8336544Z Tuesday 06 October 2026  16:33:14 -0300 (0:00:00.073)       0:00:50.285 ******* 
2026-10-06T19:33:14.8895499Z 
2026-10-06T19:33:14.8896256Z TASK [Cria variável build_repository_name] *************************************
2026-10-06T19:33:14.8896968Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:14.9170573Z Tuesday 06 October 2026  16:33:14 -0300 (0:00:00.083)       0:00:50.369 ******* 
2026-10-06T19:33:14.9725269Z 
2026-10-06T19:33:14.9725803Z TASK [Buscando diretorio de config] ********************************************
2026-10-06T19:33:14.9726163Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:15.0002024Z Tuesday 06 October 2026  16:33:14 -0300 (0:00:00.083)       0:00:50.452 ******* 
2026-10-06T19:33:15.0520246Z 
2026-10-06T19:33:15.0520733Z TASK [Buscando diretorio de config] ********************************************
2026-10-06T19:33:15.0521448Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:15.0830857Z Tuesday 06 October 2026  16:33:15 -0300 (0:00:00.082)       0:00:50.535 ******* 
2026-10-06T19:33:15.4259358Z 
2026-10-06T19:33:15.4259872Z TASK [Create a directory] ******************************************************
2026-10-06T19:33:15.4261567Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config)
2026-10-06T19:33:15.7087068Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/jboss)
2026-10-06T19:33:15.7414329Z Tuesday 06 October 2026  16:33:15 -0300 (0:00:00.658)       0:00:51.193 ******* 
2026-10-06T19:33:16.1544477Z 
2026-10-06T19:33:16.1544972Z TASK [Verifica se o arquivo  existe] *******************************************
2026-10-06T19:33:16.1545372Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config)
2026-10-06T19:33:16.4265567Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/jboss)
2026-10-06T19:33:16.4541342Z Tuesday 06 October 2026  16:33:16 -0300 (0:00:00.712)       0:00:51.906 ******* 
2026-10-06T19:33:16.5506298Z included: /opt/ads-agent/_work/r12246/a/esteira-jboss-vm-v2/roles/jboss/tasks/stack_modules_custom_block.yml for caddeapllx1537.agil.nprd.caixa.gov.br
2026-10-06T19:33:16.5797732Z Tuesday 06 October 2026  16:33:16 -0300 (0:00:00.125)       0:00:52.031 ******* 
2026-10-06T19:33:16.8936710Z 
2026-10-06T19:33:16.8937465Z TASK [Lendo artefatos do arquivo CSV] ******************************************
2026-10-06T19:33:16.8938024Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:16.9247317Z Tuesday 06 October 2026  16:33:16 -0300 (0:00:00.344)       0:00:52.376 ******* 
2026-10-06T19:33:16.9344197Z [WARNING]: The loop variable 'item' is already in use. You should set the
2026-10-06T19:33:16.9344603Z `loop_var` value in the `loop_control` option for the task to something else to
2026-10-06T19:33:16.9345038Z avoid variable collisions and unexpected behavior.
2026-10-06T19:33:16.9715289Z 
2026-10-06T19:33:16.9715768Z TASK [Mostra lista de artefatos] ***********************************************
2026-10-06T19:33:16.9718522Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item={u'version': u'4', u'group_id': u'com.sybase', u'extension': u'jar', u'artifact_id': u'jconn4'}) => {
2026-10-06T19:33:16.9718979Z     "msg": "Artefato: jconn4 - versao 4"
2026-10-06T19:33:16.9719352Z }
2026-10-06T19:33:17.0010558Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item={u'version': u'4.0', u'group_id': u'com.microsoft.sqlserver', u'extension': u'jar', u'artifact_id': u'sqljdbc4'}) => {
2026-10-06T19:33:17.0011079Z     "msg": "Artefato: sqljdbc4 - versao 4.0"
2026-10-06T19:33:17.0011496Z }
2026-10-06T19:33:17.0299832Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item={u'version': u'11.5.8.0', u'group_id': u'com.ibm.db2', u'extension': u'jar', u'artifact_id': u'jcc'}) => {
2026-10-06T19:33:17.0300522Z     "msg": "Artefato: jcc - versao 11.5.8.0"
2026-10-06T19:33:17.0300882Z }
2026-10-06T19:33:17.0584804Z Tuesday 06 October 2026  16:33:17 -0300 (0:00:00.133)       0:00:52.510 ******* 
2026-10-06T19:33:17.4117056Z 
2026-10-06T19:33:17.4118131Z TASK [Listar arquivos no diretório baixados anteriormente] *********************
2026-10-06T19:33:17.4118378Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:17.4429274Z Tuesday 06 October 2026  16:33:17 -0300 (0:00:00.384)       0:00:52.894 ******* 
2026-10-06T19:33:17.4825035Z [WARNING]: conditional statements should not include jinja2 templating
2026-10-06T19:33:17.4825322Z delimiters such as {{ }} or {% %}. Found: '{{ inner_item.artifact_id }}-{{
2026-10-06T19:33:17.4825561Z inner_item.version }}.{{ inner_item.extension|default('jar',true) }}' not in
2026-10-06T19:33:17.4827676Z files_found.files | map(attribute='path') | map('basename') | list
2026-10-06T19:33:17.8720472Z 
2026-10-06T19:33:17.8720937Z TASK [maven_artifact] **********************************************************
2026-10-06T19:33:17.8721361Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item={u'version': u'4', u'group_id': u'com.sybase', u'extension': u'jar', u'artifact_id': u'jconn4'})
2026-10-06T19:33:19.0326418Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item={u'version': u'4.0', u'group_id': u'com.microsoft.sqlserver', u'extension': u'jar', u'artifact_id': u'sqljdbc4'})
2026-10-06T19:33:19.4233098Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item={u'version': u'11.5.8.0', u'group_id': u'com.ibm.db2', u'extension': u'jar', u'artifact_id': u'jcc'})
2026-10-06T19:33:19.4546798Z Tuesday 06 October 2026  16:33:19 -0300 (0:00:02.011)       0:00:54.906 ******* 
2026-10-06T19:33:19.8630136Z 
2026-10-06T19:33:19.8630790Z TASK [Verifica se o arquivo jboss-modules-custom tem conteudo] *****************
2026-10-06T19:33:19.8630990Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:19.8907468Z Tuesday 06 October 2026  16:33:19 -0300 (0:00:00.436)       0:00:55.342 ******* 
2026-10-06T19:33:21.6036516Z 
2026-10-06T19:33:21.6037009Z TASK [Copiando artefatos (Modules) para o(s) servidor(es) Jboss] ***************
2026-10-06T19:33:21.6037214Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:21.6313854Z Tuesday 06 October 2026  16:33:21 -0300 (0:00:01.740)       0:00:57.083 ******* 
2026-10-06T19:33:22.2335638Z 
2026-10-06T19:33:22.2336337Z TASK [Copiando artefato (jboss-custom.cli) para o(s) servidor(es) Jboss] *******
2026-10-06T19:33:22.2336586Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:22.2612147Z Tuesday 06 October 2026  16:33:22 -0300 (0:00:00.629)       0:00:57.713 ******* 
2026-10-06T19:33:22.3298217Z Tuesday 06 October 2026  16:33:22 -0300 (0:00:00.068)       0:00:57.781 ******* 
2026-10-06T19:33:22.3973082Z Tuesday 06 October 2026  16:33:22 -0300 (0:00:00.067)       0:00:57.849 ******* 
2026-10-06T19:33:22.4647134Z Tuesday 06 October 2026  16:33:22 -0300 (0:00:00.067)       0:00:57.916 ******* 
2026-10-06T19:33:22.5334244Z Tuesday 06 October 2026  16:33:22 -0300 (0:00:00.068)       0:00:57.985 ******* 
2026-10-06T19:33:22.6020964Z Tuesday 06 October 2026  16:33:22 -0300 (0:00:00.068)       0:00:58.054 ******* 
2026-10-06T19:33:22.6431596Z 
2026-10-06T19:33:22.6431874Z PLAY [jboss] *******************************************************************
2026-10-06T19:33:22.6728396Z Tuesday 06 October 2026  16:33:22 -0300 (0:00:00.070)       0:00:58.124 ******* 
2026-10-06T19:33:22.7313430Z 
2026-10-06T19:33:22.7313844Z TASK [Setando a versão do Jboss] ***********************************************
2026-10-06T19:33:22.7314120Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:22.7587425Z Tuesday 06 October 2026  16:33:22 -0300 (0:00:00.085)       0:00:58.210 ******* 
2026-10-06T19:33:22.8125969Z 
2026-10-06T19:33:22.8126390Z TASK [Cria variável build_repository_name_tfs] *********************************
2026-10-06T19:33:22.8126556Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:22.8402121Z Tuesday 06 October 2026  16:33:22 -0300 (0:00:00.081)       0:00:58.292 ******* 
2026-10-06T19:33:22.8943813Z 
2026-10-06T19:33:22.8944340Z TASK [Buscando diretorio de config] ********************************************
2026-10-06T19:33:22.8944906Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:22.9215456Z Tuesday 06 October 2026  16:33:22 -0300 (0:00:00.081)       0:00:58.373 ******* 
2026-10-06T19:33:23.4866826Z 
2026-10-06T19:33:23.4867741Z TASK [Copy common_start.sh] ****************************************************
2026-10-06T19:33:23.4867955Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:23.5141733Z Tuesday 06 October 2026  16:33:23 -0300 (0:00:00.592)       0:00:58.966 ******* 
2026-10-06T19:33:24.0978137Z 
2026-10-06T19:33:24.0979032Z TASK [Copy template script] ****************************************************
2026-10-06T19:33:24.0979256Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:24.1256605Z Tuesday 06 October 2026  16:33:24 -0300 (0:00:00.611)       0:00:59.577 ******* 
2026-10-06T19:33:24.7303779Z 
2026-10-06T19:33:24.7304278Z TASK [JBoss systemd wrapper for sysvinit script mode domain] *******************
2026-10-06T19:33:24.7304440Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:24.7579799Z Tuesday 06 October 2026  16:33:24 -0300 (0:00:00.632)       0:01:00.209 ******* 
2026-10-06T19:33:25.4878418Z 
2026-10-06T19:33:25.4878943Z TASK [Realiza copia do arquivo de Trust Store] *********************************
2026-10-06T19:33:25.4879154Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:25.5156886Z Tuesday 06 October 2026  16:33:25 -0300 (0:00:00.757)       0:01:00.967 ******* 
2026-10-06T19:33:25.5867304Z Tuesday 06 October 2026  16:33:25 -0300 (0:00:00.070)       0:01:01.038 ******* 
2026-10-06T19:33:25.6712680Z Tuesday 06 October 2026  16:33:25 -0300 (0:00:00.084)       0:01:01.123 ******* 
2026-10-06T19:33:26.0965461Z 
2026-10-06T19:33:26.0966386Z TASK [Check directory configuration exists] ************************************
2026-10-06T19:33:26.0966956Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config)
2026-10-06T19:33:26.3688636Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/jboss)
2026-10-06T19:33:26.3963193Z Tuesday 06 October 2026  16:33:26 -0300 (0:00:00.725)       0:01:01.848 ******* 
2026-10-06T19:33:33.4548006Z 
2026-10-06T19:33:33.4548610Z TASK [Copiando arquivos para jboss.server.config.dir] **************************
2026-10-06T19:33:33.4550139Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config', u'stat': {u'charset': u'binary', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1791315085.9530697, u'block_size': 4096, u'inode': 176184902, u'isgid': False, u'size': 234, u'wgrp': False, u'executable': True, u'isuid': False, u'readable': True, u'isreg': False, u'version': u'18446744073369022448', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'inode/directory', u'blocks': 0, u'xoth': True, u'islnk': False, u'nlink': 5, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/configuration', u'xusr': True, u'atime': 1791315087.2290523, u'isdir': True, u'ctime': 1791315085.9530697, u'isblk': False, u'xgrp': True, u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0755', u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/configuration', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-06T19:33:33.4890395Z Tuesday 06 October 2026  16:33:33 -0300 (0:00:07.092)       0:01:08.940 ******* 
2026-10-06T19:33:33.9095833Z 
2026-10-06T19:33:33.9096537Z TASK [Get standalone-full-ha.xml status] ***************************************
2026-10-06T19:33:33.9096806Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config)
2026-10-06T19:33:34.1843961Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/jboss)
2026-10-06T19:33:34.2114191Z Tuesday 06 October 2026  16:33:34 -0300 (0:00:00.721)       0:01:09.662 ******* 
2026-10-06T19:33:34.8039877Z 
2026-10-06T19:33:34.8040687Z TASK [Copiando arquivo standalone-full-ha.xml] *********************************
2026-10-06T19:33:34.8042657Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config', u'stat': {u'charset': u'us-ascii', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1791315087.249052, u'block_size': 4096, u'inode': 104869455, u'isgid': False, u'size': 110383, u'wgrp': False, u'executable': False, u'isuid': False, u'readable': True, u'isreg': True, u'version': u'18446744073637709816', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'application/xml', u'blocks': 216, u'xoth': False, u'islnk': False, u'nlink': 1, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/standalone-full-ha.xml', u'xusr': False, u'atime': 1791315087.250052, u'isdir': False, u'ctime': 1791315087.249052, u'isblk': False, u'checksum': u'dbd86f531ec009a080ba3b4ada4a225fcf0a6db6', u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0644', u'xgrp': False, u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/standalone-full-ha.xml', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-06T19:33:34.8443888Z Tuesday 06 October 2026  16:33:34 -0300 (0:00:00.633)       0:01:10.296 ******* 
2026-10-06T19:33:35.2343212Z 
2026-10-06T19:33:35.2343906Z TASK [Get standalone-ha.xml status] ********************************************
2026-10-06T19:33:35.2344182Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config)
2026-10-06T19:33:35.5394372Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/jboss)
2026-10-06T19:33:35.5678368Z Tuesday 06 October 2026  16:33:35 -0300 (0:00:00.723)       0:01:11.019 ******* 
2026-10-06T19:33:35.6492341Z Tuesday 06 October 2026  16:33:35 -0300 (0:00:00.081)       0:01:11.101 ******* 
2026-10-06T19:33:35.9750313Z 
2026-10-06T19:33:35.9750704Z TASK [Get standalone.xml status] ***********************************************
2026-10-06T19:33:35.9751127Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config)
2026-10-06T19:33:36.2516290Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/jboss)
2026-10-06T19:33:36.2774238Z Tuesday 06 October 2026  16:33:36 -0300 (0:00:00.628)       0:01:11.729 ******* 
2026-10-06T19:33:36.3605165Z Tuesday 06 October 2026  16:33:36 -0300 (0:00:00.082)       0:01:11.812 ******* 
2026-10-06T19:33:36.7802046Z 
2026-10-06T19:33:36.7803027Z TASK [Get standalone.conf status] **********************************************
2026-10-06T19:33:36.7803834Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config)
2026-10-06T19:33:37.0643459Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/jboss)
2026-10-06T19:33:37.0929260Z Tuesday 06 October 2026  16:33:37 -0300 (0:00:00.732)       0:01:12.544 ******* 
2026-10-06T19:33:37.6927144Z 
2026-10-06T19:33:37.6927652Z TASK [Copiando arquivo standalone.conf] ****************************************
2026-10-06T19:33:37.6929518Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item={u'item': u'/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config', u'stat': {u'charset': u'utf-8', u'uid': 1000, u'exists': True, u'attr_flags': u'', u'woth': False, u'device_type': 0, u'mtime': 1791315087.3140512, u'block_size': 4096, u'inode': 104869456, u'isgid': False, u'size': 4762, u'wgrp': False, u'executable': False, u'isuid': False, u'readable': True, u'isreg': True, u'version': u'18446744072518596639', u'pw_name': u'sadscp01', u'gid': 1000, u'ischr': False, u'wusr': True, u'writeable': True, u'mimetype': u'text/plain', u'blocks': 16, u'xoth': False, u'islnk': False, u'nlink': 1, u'issock': False, u'rgrp': True, u'gr_name': u'sadscp01', u'path': u'/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/standalone.conf', u'xusr': False, u'atime': 1791315087.3140512, u'isdir': False, u'ctime': 1791315087.3140512, u'isblk': False, u'checksum': u'7fa606e163edcdaa6fbf0c5951b6dca9811267e2', u'dev': 64771, u'roth': True, u'isfifo': False, u'mode': u'0644', u'xgrp': False, u'rusr': True, u'attributes': []}, u'ansible_loop_var': u'item', u'failed': False, u'invocation': {u'module_args': {u'follow': False, u'get_checksum': True, u'path': u'/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/standalone.conf', u'checksum_algorithm': u'sha1', u'get_md5': False, u'get_mime': True, u'get_attributes': True}}, u'changed': False})
2026-10-06T19:33:37.7285816Z Tuesday 06 October 2026  16:33:37 -0300 (0:00:00.635)       0:01:13.180 ******* 
2026-10-06T19:33:38.0301917Z 
2026-10-06T19:33:38.0303009Z TASK [Restart Zabbix] **********************************************************
2026-10-06T19:33:38.0303511Z fatal: [caddeapllx1537.agil.nprd.caixa.gov.br]: FAILED! => {"changed": false, "msg": "Could not find the requested service zabbix-agent: host"}
2026-10-06T19:33:38.0303691Z ...ignoring
2026-10-06T19:33:38.0580631Z Tuesday 06 October 2026  16:33:38 -0300 (0:00:00.329)       0:01:13.510 ******* 
2026-10-06T19:33:38.1255189Z Tuesday 06 October 2026  16:33:38 -0300 (0:00:00.067)       0:01:13.577 ******* 
2026-10-06T19:33:38.1587466Z [WARNING]: conditional statements should not include jinja2 templating
2026-10-06T19:33:38.1587699Z delimiters such as {{ }} or {% %}. Found: {{ lookup('env','HSM') |
2026-10-06T19:33:38.1588274Z default('false', true) | bool }}
2026-10-06T19:33:38.1671073Z Tuesday 06 October 2026  16:33:38 -0300 (0:00:00.041)       0:01:13.619 ******* 
2026-10-06T19:33:44.6014740Z 
2026-10-06T19:33:44.6015663Z RUNNING HANDLER [Restart Jboss] ************************************************
2026-10-06T19:33:44.6015868Z changed: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:44.6044754Z 
2026-10-06T19:33:44.6044962Z PLAY [jboss] *******************************************************************
2026-10-06T19:33:44.6080110Z 
2026-10-06T19:33:44.6080317Z PLAY [jboss] *******************************************************************
2026-10-06T19:33:44.6111650Z 
2026-10-06T19:33:44.6111792Z PLAY [jboss] *******************************************************************
2026-10-06T19:33:44.6398392Z Tuesday 06 October 2026  16:33:44 -0300 (0:00:06.472)       0:01:20.091 ******* 
2026-10-06T19:33:44.6966366Z 
2026-10-06T19:33:44.6966815Z TASK [Cria variável build_repository_name] *************************************
2026-10-06T19:33:44.6966980Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:44.7240022Z Tuesday 06 October 2026  16:33:44 -0300 (0:00:00.084)       0:01:20.175 ******* 
2026-10-06T19:33:44.7795306Z 
2026-10-06T19:33:44.7795899Z TASK [Buscando diretorio de config] ********************************************
2026-10-06T19:33:44.7796112Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:44.8122049Z Tuesday 06 October 2026  16:33:44 -0300 (0:00:00.088)       0:01:20.264 ******* 
2026-10-06T19:33:45.1479554Z 
2026-10-06T19:33:45.1480227Z TASK [Verifica se o arquivo {{ item }}/etc/hosts-{{ sistema_ambiente }} existe] ***
2026-10-06T19:33:45.1480499Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config)
2026-10-06T19:33:45.4284540Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br] => (item=/opt/ads-agent/_work/r12246/a/_SIOPI-ws-config/so)
2026-10-06T19:33:45.4535448Z Tuesday 06 October 2026  16:33:45 -0300 (0:00:00.641)       0:01:20.905 ******* 
2026-10-06T19:33:45.5056770Z 
2026-10-06T19:33:45.5057276Z PLAY [jboss] *******************************************************************
2026-10-06T19:33:45.5365332Z Tuesday 06 October 2026  16:33:45 -0300 (0:00:00.083)       0:01:20.988 ******* 
2026-10-06T19:33:45.7962265Z 
2026-10-06T19:33:45.7963049Z TASK [Verifica se o arquivo /opt/jboss-eap/standalone/configuration/custom.sh existe] ***
2026-10-06T19:33:45.7963225Z ok: [caddeapllx1537.agil.nprd.caixa.gov.br]
2026-10-06T19:33:45.8240736Z Tuesday 06 October 2026  16:33:45 -0300 (0:00:00.287)       0:01:21.276 ******* 
2026-10-06T19:33:46.0944208Z 
2026-10-06T19:33:46.0945260Z TASK [Executa shell customizada (jboss_home)] **********************************
2026-10-06T19:33:46.0946169Z fatal: [caddeapllx1537.agil.nprd.caixa.gov.br]: FAILED! => {"changed": true, "cmd": "/opt/jboss-eap/standalone/configuration/custom.sh", "delta": "0:00:00.026230", "end": "2026-10-06 16:33:46.080514", "msg": "non-zero return code", "rc": 32, "start": "2026-10-06 16:33:46.054284", "stderr": "umount: /arquivos-recebidos: mountpoint not found\nmount.nfs: mount point /arquivos-recebidos does not exist", "stderr_lines": ["umount: /arquivos-recebidos: mountpoint not found", "mount.nfs: mount point /arquivos-recebidos does not exist"], "stdout": "", "stdout_lines": []}
2026-10-06T19:33:46.0952897Z 
2026-10-06T19:33:46.0953066Z PLAY RECAP *********************************************************************
2026-10-06T19:33:46.0953807Z caddeapllx1537.agil.nprd.caixa.gov.br : ok=75   changed=25   unreachable=0    failed=1    skipped=17   rescued=0    ignored=1   
2026-10-06T19:33:46.0953903Z 
2026-10-06T19:33:46.0955195Z Tuesday 06 October 2026  16:33:46 -0300 (0:00:00.271)       0:01:21.547 ******* 
2026-10-06T19:33:46.0955398Z =============================================================================== 
2026-10-06T19:33:46.0961078Z nfs : Networker | Restart networker ------------------------------------ 20.51s
2026-10-06T19:33:46.0961474Z nfs : Instalando o NFS Client ------------------------------------------- 7.54s
2026-10-06T19:33:46.0961708Z Copiando arquivos para jboss.server.config.dir -------------------------- 7.09s
2026-10-06T19:33:46.0961923Z Restart Jboss ----------------------------------------------------------- 6.47s
2026-10-06T19:33:46.0962145Z Copiando artefatos para o(s) servidor(es) Jboss ------------------------- 3.68s
2026-10-06T19:33:46.0962366Z nfs : execute montagem script ------------------------------------------- 2.25s
2026-10-06T19:33:46.0965154Z nfs : Install networker lgtoclnt_url ------------------------------------ 2.08s
2026-10-06T19:33:46.0965429Z maven_artifact ---------------------------------------------------------- 2.01s
2026-10-06T19:33:46.0965655Z nfs : Install networker lgtonmda_url ------------------------------------ 2.01s
2026-10-06T19:33:46.0965892Z Copiando artefatos (Modules) para o(s) servidor(es) Jboss --------------- 1.74s
2026-10-06T19:33:46.0966105Z maven_artifact ---------------------------------------------------------- 1.61s
2026-10-06T19:33:46.0966331Z Gerando fatos de servicos ----------------------------------------------- 1.48s
2026-10-06T19:33:46.0966551Z nfs : Networker | Start networker --------------------------------------- 1.02s
2026-10-06T19:33:46.0967092Z Gathering Facts --------------------------------------------------------- 0.80s
2026-10-06T19:33:46.0967362Z Create a symbolic link -------------------------------------------------- 0.80s
2026-10-06T19:33:46.0967589Z Realiza copia do arquivo de Trust Store --------------------------------- 0.76s
2026-10-06T19:33:46.0967824Z Get standalone.conf status ---------------------------------------------- 0.73s
2026-10-06T19:33:46.0968034Z Check directory configuration exists ------------------------------------ 0.73s
2026-10-06T19:33:46.0968449Z Get standalone-ha.xml status -------------------------------------------- 0.72s
2026-10-06T19:33:46.0968675Z Get standalone-full-ha.xml status --------------------------------------- 0.72s
2026-10-06T19:33:46.0968827Z Playbook run took 0 days, 0 hours, 1 minutes, 21 seconds
2026-10-06T19:33:46.1629262Z ##[error]Bash exited with code '2'.
2026-10-06T19:33:46.1646876Z ##[section]Finishing: Deploy Config no JBOSS
