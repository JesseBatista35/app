2026-11-10T13:52:03.5565299Z ##[section]Starting: Check Deployments [JBOSS]
2026-11-10T13:52:03.5568401Z ==============================================================================
2026-11-10T13:52:03.5568486Z Task         : Bash
2026-11-10T13:52:03.5568531Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-11-10T13:52:03.5568683Z Version      : 3.227.0
2026-11-10T13:52:03.5568730Z Author       : Microsoft Corporation
2026-11-10T13:52:03.5568786Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-11-10T13:52:03.5568868Z ==============================================================================
2026-11-10T13:52:03.6720067Z Generating script.
2026-11-10T13:52:03.6727984Z Script contents:
2026-11-10T13:52:03.6728481Z ansible-playbook /opt/ads-agent/_work/r19325/a/esteira-jboss-vm-v2/site.yml --tags check_deployments -e sistema_ambiente=des -e sistema_nome=sigsj-internet -e site=ctc_nprd
2026-11-10T13:52:03.6731224Z ========================== Starting Command Output ===========================
2026-11-10T13:52:03.6738459Z [command]/bin/bash /opt/ads-agent/_work/_temp/a3f5f546-534c-4f44-9a5b-7a671fad0a59.sh
2026-11-10T13:52:05.8974783Z 
2026-11-10T13:52:05.8975424Z PLAY [local] *******************************************************************
2026-11-10T13:52:05.9261272Z 
2026-11-10T13:52:05.9261900Z PLAY [Configurando o DNS] ******************************************************
2026-11-10T13:52:06.1430959Z 
2026-11-10T13:52:06.1431624Z PLAY [local] *******************************************************************
2026-11-10T13:52:06.1469675Z 
2026-11-10T13:52:06.1470464Z PLAY [Verificando serviços] ****************************************************
2026-11-10T13:52:06.1564378Z 
2026-11-10T13:52:06.1564891Z PLAY [Configuração LDAP] *******************************************************
2026-11-10T13:52:06.1598525Z [WARNING]: Found variable using reserved name: when
2026-11-10T13:52:06.1603029Z 
2026-11-10T13:52:06.1603234Z PLAY [jboss] *******************************************************************
2026-11-10T13:52:06.1687838Z 
2026-11-10T13:52:06.1688378Z PLAY [Stack Jboss] *************************************************************
2026-11-10T13:52:06.1935040Z Tuesday 10 November 2026  10:52:06 -0300 (0:00:00.357)       0:00:00.357 ****** 
2026-11-10T13:52:06.8659925Z 
2026-11-10T13:52:06.8660668Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-11-10T13:52:06.8661351Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-11-10T13:52:06.8662041Z caddeapllx2854.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-11-10T13:52:06.8662758Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-11-10T13:52:06.8663428Z releases. A future Ansible release will default to using the discovered 
2026-11-10T13:52:06.8663599Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-11-10T13:52:06.8663780Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-11-10T13:52:06.8663967Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-11-10T13:52:06.8664124Z setting deprecation_warnings=False in ansible.cfg.
2026-11-10T13:52:06.8664272Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-10T13:52:06.8689220Z 
2026-11-10T13:52:06.8690007Z PLAY [jboss] *******************************************************************
2026-11-10T13:52:06.8732502Z 
2026-11-10T13:52:06.8732984Z PLAY [jboss] *******************************************************************
2026-11-10T13:52:06.8772982Z 
2026-11-10T13:52:06.8773312Z PLAY [jboss] *******************************************************************
2026-11-10T13:52:06.8802718Z 
2026-11-10T13:52:06.8803273Z PLAY [Copiando deployments adicionais] *****************************************
2026-11-10T13:52:06.8829032Z 
2026-11-10T13:52:06.8829451Z PLAY [Copiando modules adicionais] *********************************************
2026-11-10T13:52:06.8856004Z 
2026-11-10T13:52:06.8856363Z PLAY [jboss] *******************************************************************
2026-11-10T13:52:06.8892210Z 
2026-11-10T13:52:06.8892469Z PLAY [jboss] *******************************************************************
2026-11-10T13:52:06.8923043Z 
2026-11-10T13:52:06.8923494Z PLAY [jboss] *******************************************************************
2026-11-10T13:52:06.8967614Z Tuesday 10 November 2026  10:52:06 -0300 (0:00:00.703)       0:00:01.060 ****** 
2026-11-10T13:52:07.3302802Z 
2026-11-10T13:52:07.3303333Z TASK [Wait for Jboss Management port] ******************************************
2026-11-10T13:52:07.3303504Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-10T13:52:07.3339642Z Tuesday 10 November 2026  10:52:07 -0300 (0:00:00.437)       0:00:01.498 ****** 
2026-11-10T13:52:08.3134705Z FAILED - RETRYING: Check if Jboss is Running (120 retries left).
2026-11-10T13:52:13.8581023Z 
2026-11-10T13:52:13.8581549Z TASK [Check if Jboss is Running] ***********************************************
2026-11-10T13:52:13.8581730Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-10T13:52:13.8616446Z Tuesday 10 November 2026  10:52:13 -0300 (0:00:06.527)       0:00:08.025 ****** 
2026-11-10T13:52:14.3513821Z FAILED - RETRYING: Check Deployment details looking for status OK (60 retries left).
2026-11-10T13:52:19.9556523Z FAILED - RETRYING: Check Deployment details looking for status OK (59 retries left).
2026-11-10T13:52:25.4199654Z FAILED - RETRYING: Check Deployment details looking for status OK (58 retries left).
2026-11-10T13:52:30.8126608Z FAILED - RETRYING: Check Deployment details looking for status OK (57 retries left).
2026-11-10T13:52:36.1928282Z FAILED - RETRYING: Check Deployment details looking for status OK (56 retries left).
2026-11-10T13:52:41.5907186Z FAILED - RETRYING: Check Deployment details looking for status OK (55 retries left).
2026-11-10T13:52:46.9713215Z FAILED - RETRYING: Check Deployment details looking for status OK (54 retries left).
2026-11-10T13:52:52.3562157Z FAILED - RETRYING: Check Deployment details looking for status OK (53 retries left).
2026-11-10T13:52:57.7517968Z FAILED - RETRYING: Check Deployment details looking for status OK (52 retries left).
2026-11-10T13:53:03.1316674Z FAILED - RETRYING: Check Deployment details looking for status OK (51 retries left).
2026-11-10T13:53:08.5188391Z FAILED - RETRYING: Check Deployment details looking for status OK (50 retries left).
2026-11-10T13:53:13.9068868Z FAILED - RETRYING: Check Deployment details looking for status OK (49 retries left).
2026-11-10T13:53:19.2856177Z FAILED - RETRYING: Check Deployment details looking for status OK (48 retries left).
2026-11-10T13:53:24.6697748Z FAILED - RETRYING: Check Deployment details looking for status OK (47 retries left).
2026-11-10T13:53:30.0651159Z FAILED - RETRYING: Check Deployment details looking for status OK (46 retries left).
2026-11-10T13:53:35.4422276Z FAILED - RETRYING: Check Deployment details looking for status OK (45 retries left).
2026-11-10T13:53:40.8208048Z FAILED - RETRYING: Check Deployment details looking for status OK (44 retries left).
2026-11-10T13:53:46.1997649Z FAILED - RETRYING: Check Deployment details looking for status OK (43 retries left).
2026-11-10T13:53:51.5840831Z FAILED - RETRYING: Check Deployment details looking for status OK (42 retries left).
2026-11-10T13:53:56.9599227Z FAILED - RETRYING: Check Deployment details looking for status OK (41 retries left).
2026-11-10T13:54:02.3682687Z FAILED - RETRYING: Check Deployment details looking for status OK (40 retries left).
2026-11-10T13:54:07.7607555Z FAILED - RETRYING: Check Deployment details looking for status OK (39 retries left).
2026-11-10T13:54:13.1363143Z FAILED - RETRYING: Check Deployment details looking for status OK (38 retries left).
2026-11-10T13:54:18.5353856Z FAILED - RETRYING: Check Deployment details looking for status OK (37 retries left).
2026-11-10T13:54:23.9263879Z FAILED - RETRYING: Check Deployment details looking for status OK (36 retries left).
2026-11-10T13:54:29.3055670Z FAILED - RETRYING: Check Deployment details looking for status OK (35 retries left).
2026-11-10T13:54:34.6906332Z FAILED - RETRYING: Check Deployment details looking for status OK (34 retries left).
2026-11-10T13:54:40.0703698Z FAILED - RETRYING: Check Deployment details looking for status OK (33 retries left).
2026-11-10T13:54:45.4506929Z FAILED - RETRYING: Check Deployment details looking for status OK (32 retries left).
2026-11-10T13:54:50.8445608Z FAILED - RETRYING: Check Deployment details looking for status OK (31 retries left).
2026-11-10T13:54:56.2230852Z FAILED - RETRYING: Check Deployment details looking for status OK (30 retries left).
2026-11-10T13:55:01.6081373Z FAILED - RETRYING: Check Deployment details looking for status OK (29 retries left).
2026-11-10T13:55:07.0016476Z FAILED - RETRYING: Check Deployment details looking for status OK (28 retries left).
2026-11-10T13:55:12.3850022Z FAILED - RETRYING: Check Deployment details looking for status OK (27 retries left).
2026-11-10T13:55:17.7695647Z FAILED - RETRYING: Check Deployment details looking for status OK (26 retries left).
2026-11-10T13:55:23.1987736Z FAILED - RETRYING: Check Deployment details looking for status OK (25 retries left).
2026-11-10T13:55:28.5786436Z FAILED - RETRYING: Check Deployment details looking for status OK (24 retries left).
2026-11-10T13:55:33.9728993Z FAILED - RETRYING: Check Deployment details looking for status OK (23 retries left).
2026-11-10T13:55:39.3626557Z FAILED - RETRYING: Check Deployment details looking for status OK (22 retries left).
2026-11-10T13:55:44.7405403Z FAILED - RETRYING: Check Deployment details looking for status OK (21 retries left).
2026-11-10T13:55:50.1256540Z FAILED - RETRYING: Check Deployment details looking for status OK (20 retries left).
2026-11-10T13:55:55.5242273Z FAILED - RETRYING: Check Deployment details looking for status OK (19 retries left).
2026-11-10T13:56:00.9100869Z FAILED - RETRYING: Check Deployment details looking for status OK (18 retries left).
2026-11-10T13:56:06.2896015Z FAILED - RETRYING: Check Deployment details looking for status OK (17 retries left).
2026-11-10T13:56:11.6774562Z FAILED - RETRYING: Check Deployment details looking for status OK (16 retries left).
2026-11-10T13:56:17.0542729Z FAILED - RETRYING: Check Deployment details looking for status OK (15 retries left).
2026-11-10T13:56:22.4454298Z FAILED - RETRYING: Check Deployment details looking for status OK (14 retries left).
2026-11-10T13:56:27.8389630Z FAILED - RETRYING: Check Deployment details looking for status OK (13 retries left).
2026-11-10T13:56:33.2169134Z FAILED - RETRYING: Check Deployment details looking for status OK (12 retries left).
2026-11-10T13:56:38.5924525Z FAILED - RETRYING: Check Deployment details looking for status OK (11 retries left).
2026-11-10T13:56:43.9810527Z FAILED - RETRYING: Check Deployment details looking for status OK (10 retries left).
2026-11-10T13:56:49.3551454Z FAILED - RETRYING: Check Deployment details looking for status OK (9 retries left).
2026-11-10T13:56:54.7331462Z FAILED - RETRYING: Check Deployment details looking for status OK (8 retries left).
2026-11-10T13:57:00.1595384Z FAILED - RETRYING: Check Deployment details looking for status OK (7 retries left).
2026-11-10T13:57:05.5554765Z FAILED - RETRYING: Check Deployment details looking for status OK (6 retries left).
2026-11-10T13:57:10.9401605Z FAILED - RETRYING: Check Deployment details looking for status OK (5 retries left).
2026-11-10T13:57:16.3509602Z FAILED - RETRYING: Check Deployment details looking for status OK (4 retries left).
2026-11-10T13:57:21.7314109Z FAILED - RETRYING: Check Deployment details looking for status OK (3 retries left).
2026-11-10T13:57:27.1173776Z FAILED - RETRYING: Check Deployment details looking for status OK (2 retries left).
2026-11-10T13:57:32.5256422Z FAILED - RETRYING: Check Deployment details looking for status OK (1 retries left).
2026-11-10T13:57:37.9117133Z 
2026-11-10T13:57:37.9118216Z TASK [Check Deployment details looking for status OK] **************************
2026-11-10T13:57:37.9125371Z fatal: [caddeapllx2854.agil.nprd.caixa.gov.br]: FAILED! => {"attempts": 60, "changed": false, "connection": "close", "content": "{\"outcome\" : \"success\", \"result\" : {\"ojdbc8.jar\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"Fj3DWG0Y7U3HRZ/bKwfzUOqmSTk=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1794318722505, \"enabled-timestamp\" : \"2026-11-10 10:52:02,505 BRT\", \"managed\" : true, \"name\" : \"ojdbc8.jar\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"ojdbc8.jar\", \"status\" : \"OK\", \"subdeployment\" : null, \"subsystem\" : {\"logging\" : null}}, \"sigsj_internet-ear.ear\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"fMdjrhnJGcY5oK3heP/8IKgECzs=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1794318722460, \"enabled-timestamp\" : \"2026-11-10 10:52:02,460 BRT\", \"managed\" : true, \"name\" : \"sigsj_internet-ear.ear\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"sigsj_internet-ear.ear\", \"status\" : \"FAILED\", \"subdeployment\" : {\"br.gov.caixa-sigsj_internet-war-2.67.war\" : null, \"br.gov.caixa.farm-sirotcon-ejb-2.3.0.2-farm.jar\" : null}, \"subsystem\" : null}, \"sirotcon-ejb.jar\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"cLE7JH7Axwql5UcepAdPvwrhtws=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1794318722474, \"enabled-timestamp\" : \"2026-11-10 10:52:02,474 BRT\", \"managed\" : true, \"name\" : \"sirotcon-ejb.jar\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"sirotcon-ejb.jar\", \"status\" : \"OK\", \"subdeployment\" : null, \"subsystem\" : {\"ejb3\" : null, \"logging\" : null}}}}", "content_encoding": "identity", "content_length": "1691", "content_type": "application/json; charset=utf-8", "cookies": {}, "cookies_string": "", "date": "Tue, 10 Nov 2026 13:57:37 GMT", "elapsed": 0, "json": {"outcome": "success", "result": {"ojdbc8.jar": {"content": [{"hash": {"BYTES_VALUE": "Fj3DWG0Y7U3HRZ/bKwfzUOqmSTk="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1794318722505, "enabled-timestamp": "2026-11-10 10:52:02,505 BRT", "managed": true, "name": "ojdbc8.jar", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "ojdbc8.jar", "status": "OK", "subdeployment": null, "subsystem": {"logging": null}}, "sigsj_internet-ear.ear": {"content": [{"hash": {"BYTES_VALUE": "fMdjrhnJGcY5oK3heP/8IKgECzs="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1794318722460, "enabled-timestamp": "2026-11-10 10:52:02,460 BRT", "managed": true, "name": "sigsj_internet-ear.ear", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "sigsj_internet-ear.ear", "status": "FAILED", "subdeployment": {"br.gov.caixa-sigsj_internet-war-2.67.war": null, "br.gov.caixa.farm-sirotcon-ejb-2.3.0.2-farm.jar": null}, "subsystem": null}, "sirotcon-ejb.jar": {"content": [{"hash": {"BYTES_VALUE": "cLE7JH7Axwql5UcepAdPvwrhtws="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1794318722474, "enabled-timestamp": "2026-11-10 10:52:02,474 BRT", "managed": true, "name": "sirotcon-ejb.jar", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "sirotcon-ejb.jar", "status": "OK", "subdeployment": null, "subsystem": {"ejb3": null, "logging": null}}}}, "msg": "OK (1691 bytes)", "redirected": false, "status": 200, "url": "http://10.116.202.45:9990/management/", "x_content_type_options": "nosniff", "x_frame_options": "SAMEORIGIN"}
2026-11-10T13:57:37.9158052Z Tuesday 10 November 2026  10:57:37 -0300 (0:05:24.054)       0:05:32.079 ****** 
2026-11-10T13:57:50.7213719Z 
2026-11-10T13:57:50.7214385Z TASK [systemd] *****************************************************************
2026-11-10T13:57:50.7214663Z changed: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-10T13:57:50.7260406Z Tuesday 10 November 2026  10:57:50 -0300 (0:00:12.810)       0:05:44.890 ****** 
2026-11-10T13:57:51.0538463Z 
2026-11-10T13:57:51.0539462Z TASK [Wait for Jboss Management port] ******************************************
2026-11-10T13:57:51.0539699Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-10T13:57:51.0575979Z Tuesday 10 November 2026  10:57:51 -0300 (0:00:00.331)       0:05:45.221 ****** 
2026-11-10T13:57:52.0065761Z FAILED - RETRYING: Check if Jboss is Running (120 retries left).
2026-11-10T13:57:57.4855994Z FAILED - RETRYING: Check if Jboss is Running (119 retries left).
2026-11-10T13:58:02.9096625Z 
2026-11-10T13:58:02.9097157Z TASK [Check if Jboss is Running] ***********************************************
2026-11-10T13:58:02.9097343Z ok: [caddeapllx2854.agil.nprd.caixa.gov.br]
2026-11-10T13:58:02.9132408Z Tuesday 10 November 2026  10:58:02 -0300 (0:00:11.855)       0:05:57.077 ****** 
2026-11-10T13:58:03.3802604Z FAILED - RETRYING: Check Deployment details looking for status OK (60 retries left).
2026-11-10T13:58:08.9106389Z FAILED - RETRYING: Check Deployment details looking for status OK (59 retries left).
2026-11-10T13:58:14.2971958Z FAILED - RETRYING: Check Deployment details looking for status OK (58 retries left).
2026-11-10T13:58:19.6768586Z FAILED - RETRYING: Check Deployment details looking for status OK (57 retries left).
2026-11-10T13:58:25.0791469Z FAILED - RETRYING: Check Deployment details looking for status OK (56 retries left).
2026-11-10T13:58:30.4621072Z FAILED - RETRYING: Check Deployment details looking for status OK (55 retries left).
2026-11-10T13:58:35.8392831Z FAILED - RETRYING: Check Deployment details looking for status OK (54 retries left).
2026-11-10T13:58:41.2392799Z FAILED - RETRYING: Check Deployment details looking for status OK (53 retries left).
2026-11-10T13:58:46.6191516Z FAILED - RETRYING: Check Deployment details looking for status OK (52 retries left).
2026-11-10T13:58:52.0005322Z FAILED - RETRYING: Check Deployment details looking for status OK (51 retries left).
2026-11-10T13:58:57.3849217Z FAILED - RETRYING: Check Deployment details looking for status OK (50 retries left).
2026-11-10T13:59:02.7708784Z FAILED - RETRYING: Check Deployment details looking for status OK (49 retries left).
2026-11-10T13:59:08.1661341Z FAILED - RETRYING: Check Deployment details looking for status OK (48 retries left).
2026-11-10T13:59:13.5659775Z FAILED - RETRYING: Check Deployment details looking for status OK (47 retries left).
2026-11-10T13:59:18.9476425Z FAILED - RETRYING: Check Deployment details looking for status OK (46 retries left).
2026-11-10T13:59:24.3196709Z FAILED - RETRYING: Check Deployment details looking for status OK (45 retries left).
2026-11-10T13:59:29.7224763Z FAILED - RETRYING: Check Deployment details looking for status OK (44 retries left).
2026-11-10T13:59:35.1034493Z FAILED - RETRYING: Check Deployment details looking for status OK (43 retries left).
2026-11-10T13:59:40.4864800Z FAILED - RETRYING: Check Deployment details looking for status OK (42 retries left).
2026-11-10T13:59:45.8947077Z FAILED - RETRYING: Check Deployment details looking for status OK (41 retries left).
2026-11-10T13:59:51.2895718Z FAILED - RETRYING: Check Deployment details looking for status OK (40 retries left).
2026-11-10T13:59:56.6642523Z FAILED - RETRYING: Check Deployment details looking for status OK (39 retries left).
2026-11-10T14:00:02.0653104Z FAILED - RETRYING: Check Deployment details looking for status OK (38 retries left).
2026-11-10T14:00:07.4555199Z FAILED - RETRYING: Check Deployment details looking for status OK (37 retries left).
2026-11-10T14:00:12.8408412Z FAILED - RETRYING: Check Deployment details looking for status OK (36 retries left).
2026-11-10T14:00:18.2413639Z FAILED - RETRYING: Check Deployment details looking for status OK (35 retries left).
2026-11-10T14:00:23.6290940Z FAILED - RETRYING: Check Deployment details looking for status OK (34 retries left).
2026-11-10T14:00:29.0088292Z FAILED - RETRYING: Check Deployment details looking for status OK (33 retries left).
2026-11-10T14:00:34.4023549Z FAILED - RETRYING: Check Deployment details looking for status OK (32 retries left).
2026-11-10T14:00:39.7894370Z FAILED - RETRYING: Check Deployment details looking for status OK (31 retries left).
2026-11-10T14:00:45.1728858Z FAILED - RETRYING: Check Deployment details looking for status OK (30 retries left).
2026-11-10T14:00:50.5794873Z FAILED - RETRYING: Check Deployment details looking for status OK (29 retries left).
2026-11-10T14:00:55.9570990Z FAILED - RETRYING: Check Deployment details looking for status OK (28 retries left).
2026-11-10T14:01:01.3384699Z FAILED - RETRYING: Check Deployment details looking for status OK (27 retries left).
2026-11-10T14:01:06.7391220Z FAILED - RETRYING: Check Deployment details looking for status OK (26 retries left).
2026-11-10T14:01:12.1410551Z FAILED - RETRYING: Check Deployment details looking for status OK (25 retries left).
2026-11-10T14:01:17.5239072Z FAILED - RETRYING: Check Deployment details looking for status OK (24 retries left).
2026-11-10T14:01:22.9287761Z FAILED - RETRYING: Check Deployment details looking for status OK (23 retries left).
2026-11-10T14:01:28.3146785Z FAILED - RETRYING: Check Deployment details looking for status OK (22 retries left).
2026-11-10T14:01:33.7023853Z FAILED - RETRYING: Check Deployment details looking for status OK (21 retries left).
2026-11-10T14:01:39.0943042Z FAILED - RETRYING: Check Deployment details looking for status OK (20 retries left).
2026-11-10T14:01:44.4768425Z FAILED - RETRYING: Check Deployment details looking for status OK (19 retries left).
2026-11-10T14:01:49.8577388Z FAILED - RETRYING: Check Deployment details looking for status OK (18 retries left).
2026-11-10T14:01:55.2641431Z FAILED - RETRYING: Check Deployment details looking for status OK (17 retries left).
2026-11-10T14:02:00.6506611Z FAILED - RETRYING: Check Deployment details looking for status OK (16 retries left).
2026-11-10T14:02:06.0315543Z FAILED - RETRYING: Check Deployment details looking for status OK (15 retries left).
2026-11-10T14:02:11.4220357Z FAILED - RETRYING: Check Deployment details looking for status OK (14 retries left).
2026-11-10T14:02:16.7963021Z FAILED - RETRYING: Check Deployment details looking for status OK (13 retries left).
2026-11-10T14:02:22.1907835Z FAILED - RETRYING: Check Deployment details looking for status OK (12 retries left).
2026-11-10T14:02:27.5792616Z FAILED - RETRYING: Check Deployment details looking for status OK (11 retries left).
2026-11-10T14:02:32.9608961Z FAILED - RETRYING: Check Deployment details looking for status OK (10 retries left).
2026-11-10T14:02:38.3765890Z FAILED - RETRYING: Check Deployment details looking for status OK (9 retries left).
2026-11-10T14:02:43.7615273Z FAILED - RETRYING: Check Deployment details looking for status OK (8 retries left).
2026-11-10T14:02:49.1365035Z FAILED - RETRYING: Check Deployment details looking for status OK (7 retries left).
2026-11-10T14:02:54.5157307Z FAILED - RETRYING: Check Deployment details looking for status OK (6 retries left).
2026-11-10T14:02:59.9045184Z FAILED - RETRYING: Check Deployment details looking for status OK (5 retries left).
2026-11-10T14:03:05.2805853Z FAILED - RETRYING: Check Deployment details looking for status OK (4 retries left).
2026-11-10T14:03:10.6680414Z FAILED - RETRYING: Check Deployment details looking for status OK (3 retries left).
2026-11-10T14:03:16.0712828Z FAILED - RETRYING: Check Deployment details looking for status OK (2 retries left).
2026-11-10T14:03:21.4662807Z FAILED - RETRYING: Check Deployment details looking for status OK (1 retries left).
2026-11-10T14:03:26.8447624Z 
2026-11-10T14:03:26.8448085Z TASK [Check Deployment details looking for status OK] **************************
2026-11-10T14:03:26.8460475Z fatal: [caddeapllx2854.agil.nprd.caixa.gov.br]: FAILED! => {"attempts": 60, "changed": false, "connection": "close", "content": "{\"outcome\" : \"success\", \"result\" : {\"ojdbc8.jar\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"Fj3DWG0Y7U3HRZ/bKwfzUOqmSTk=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1794319069757, \"enabled-timestamp\" : \"2026-11-10 10:57:49,757 BRT\", \"managed\" : true, \"name\" : \"ojdbc8.jar\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"ojdbc8.jar\", \"status\" : \"OK\", \"subdeployment\" : null, \"subsystem\" : {\"logging\" : null}}, \"sigsj_internet-ear.ear\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"fMdjrhnJGcY5oK3heP/8IKgECzs=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1794319069717, \"enabled-timestamp\" : \"2026-11-10 10:57:49,717 BRT\", \"managed\" : true, \"name\" : \"sigsj_internet-ear.ear\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"sigsj_internet-ear.ear\", \"status\" : \"FAILED\", \"subdeployment\" : {\"br.gov.caixa-sigsj_internet-war-2.67.war\" : null, \"br.gov.caixa.farm-sirotcon-ejb-2.3.0.2-farm.jar\" : null}, \"subsystem\" : null}, \"sirotcon-ejb.jar\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"cLE7JH7Axwql5UcepAdPvwrhtws=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1794319069726, \"enabled-timestamp\" : \"2026-11-10 10:57:49,726 BRT\", \"managed\" : true, \"name\" : \"sirotcon-ejb.jar\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"sirotcon-ejb.jar\", \"status\" : \"OK\", \"subdeployment\" : null, \"subsystem\" : {\"ejb3\" : null, \"logging\" : null}}}}", "content_encoding": "identity", "content_length": "1691", "content_type": "application/json; charset=utf-8", "cookies": {}, "cookies_string": "", "date": "Tue, 10 Nov 2026 14:03:26 GMT", "elapsed": 0, "json": {"outcome": "success", "result": {"ojdbc8.jar": {"content": [{"hash": {"BYTES_VALUE": "Fj3DWG0Y7U3HRZ/bKwfzUOqmSTk="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1794319069757, "enabled-timestamp": "2026-11-10 10:57:49,757 BRT", "managed": true, "name": "ojdbc8.jar", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "ojdbc8.jar", "status": "OK", "subdeployment": null, "subsystem": {"logging": null}}, "sigsj_internet-ear.ear": {"content": [{"hash": {"BYTES_VALUE": "fMdjrhnJGcY5oK3heP/8IKgECzs="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1794319069717, "enabled-timestamp": "2026-11-10 10:57:49,717 BRT", "managed": true, "name": "sigsj_internet-ear.ear", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "sigsj_internet-ear.ear", "status": "FAILED", "subdeployment": {"br.gov.caixa-sigsj_internet-war-2.67.war": null, "br.gov.caixa.farm-sirotcon-ejb-2.3.0.2-farm.jar": null}, "subsystem": null}, "sirotcon-ejb.jar": {"content": [{"hash": {"BYTES_VALUE": "cLE7JH7Axwql5UcepAdPvwrhtws="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1794319069726, "enabled-timestamp": "2026-11-10 10:57:49,726 BRT", "managed": true, "name": "sirotcon-ejb.jar", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "sirotcon-ejb.jar", "status": "OK", "subdeployment": null, "subsystem": {"ejb3": null, "logging": null}}}}, "msg": "OK (1691 bytes)", "redirected": false, "status": 200, "url": "http://10.116.202.45:9990/management/", "x_content_type_options": "nosniff", "x_frame_options": "SAMEORIGIN"}
2026-11-10T14:03:26.8477837Z 
2026-11-10T14:03:26.8478589Z PLAY RECAP *********************************************************************
2026-11-10T14:03:26.8479028Z caddeapllx2854.agil.nprd.caixa.gov.br : ok=6    changed=1    unreachable=0    failed=1    skipped=0    rescued=1    ignored=0   
2026-11-10T14:03:26.8479122Z 
2026-11-10T14:03:26.8479425Z Tuesday 10 November 2026  11:03:26 -0300 (0:05:23.934)       0:11:21.012 ****** 
2026-11-10T14:03:26.8479687Z =============================================================================== 
2026-11-10T14:03:26.8481396Z Check Deployment details looking for status OK ------------------------ 324.05s
2026-11-10T14:03:26.8481676Z Check Deployment details looking for status OK ------------------------ 323.93s
2026-11-10T14:03:26.8481912Z systemd ---------------------------------------------------------------- 12.81s
2026-11-10T14:03:26.8482139Z Check if Jboss is Running ---------------------------------------------- 11.86s
2026-11-10T14:03:26.8482429Z Check if Jboss is Running ----------------------------------------------- 6.53s
2026-11-10T14:03:26.8482669Z Verifica ser o Jboss já foi instalado ----------------------------------- 0.70s
2026-11-10T14:03:26.8482906Z Wait for Jboss Management port ------------------------------------------ 0.44s
2026-11-10T14:03:26.8484738Z Wait for Jboss Management port ------------------------------------------ 0.33s
2026-11-10T14:03:26.8485010Z Playbook run took 0 days, 0 hours, 11 minutes, 20 seconds
2026-11-10T14:03:26.9208565Z ##[error]Bash exited with code '2'.
2026-11-10T14:03:26.9224950Z ##[section]Finishing: Check Deployments [JBOSS]


Tudo bem?
Tem como você verificar porque a release da internet não está subindo?
https://devops.caixa/projetos/Caixa/_releaseProgress?_a=release-environment-logs&releaseId=553319&environmentId=2571963


eles subuirma algima coisa aqui que quebrou



Last login: Thu Oct 22 16:27:03 2026 from 10.122.150.31
[p585600@caddeapllx2854 ~]$
[p585600@caddeapllx2854 ~]$
[p585600@caddeapllx2854 ~]$
[p585600@caddeapllx2854 ~]$
[p585600@caddeapllx2854 ~]$
[p585600@caddeapllx2854 ~]$
[p585600@caddeapllx2854 ~]$


