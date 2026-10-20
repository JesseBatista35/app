2026-10-20T19:42:03.9460895Z ##[section]Starting: Check Deployments [JBOSS]
2026-10-20T19:42:03.9464369Z ==============================================================================
2026-10-20T19:42:03.9464458Z Task         : Bash
2026-10-20T19:42:03.9464500Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-20T19:42:03.9464575Z Version      : 3.227.0
2026-10-20T19:42:03.9464618Z Author       : Microsoft Corporation
2026-10-20T19:42:03.9464668Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-20T19:42:03.9464752Z ==============================================================================
2026-10-20T19:42:04.0609779Z Generating script.
2026-10-20T19:42:04.0617992Z Script contents:
2026-10-20T19:42:04.0618529Z ansible-playbook /opt/ads-agent/_work/r19265/a/esteira-jboss-vm-v2/site.yml --tags check_deployments -e sistema_ambiente=des -e sistema_nome=sigsj-intranet -e site=ctc_nprd
2026-10-20T19:42:04.0621647Z ========================== Starting Command Output ===========================
2026-10-20T19:42:04.0629759Z [command]/bin/bash /opt/ads-agent/_work/_temp/41c8db4a-24cb-4d93-8fd7-1cd9a7afb70b.sh
2026-10-20T19:42:06.2901869Z 
2026-10-20T19:42:06.2902743Z PLAY [local] *******************************************************************
2026-10-20T19:42:06.3198236Z 
2026-10-20T19:42:06.3198684Z PLAY [Configurando o DNS] ******************************************************
2026-10-20T19:42:06.5148848Z 
2026-10-20T19:42:06.5149570Z PLAY [local] *******************************************************************
2026-10-20T19:42:06.5177600Z 
2026-10-20T19:42:06.5177996Z PLAY [Verificando serviços] ****************************************************
2026-10-20T19:42:06.5286092Z 
2026-10-20T19:42:06.5286602Z PLAY [Configuração LDAP] *******************************************************
2026-10-20T19:42:06.5329156Z [WARNING]: Found variable using reserved name: when
2026-10-20T19:42:06.5333854Z 
2026-10-20T19:42:06.5334004Z PLAY [jboss] *******************************************************************
2026-10-20T19:42:06.5423518Z 
2026-10-20T19:42:06.5423763Z PLAY [Stack Jboss] *************************************************************
2026-10-20T19:42:06.5665242Z Tuesday 20 October 2026  16:42:06 -0300 (0:00:00.337)       0:00:00.337 ******* 
2026-10-20T19:42:07.0818413Z 
2026-10-20T19:42:07.0819154Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-10-20T19:42:07.0822535Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-20T19:42:07.0822765Z caddeapllx955.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-20T19:42:07.0822921Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-20T19:42:07.0823089Z releases. A future Ansible release will default to using the discovered 
2026-10-20T19:42:07.0823245Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-20T19:42:07.0823405Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-20T19:42:07.0823588Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-20T19:42:07.0824045Z setting deprecation_warnings=False in ansible.cfg.
2026-10-20T19:42:07.0824180Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T19:42:07.0853409Z 
2026-10-20T19:42:07.0853974Z PLAY [jboss] *******************************************************************
2026-10-20T19:42:07.0910506Z 
2026-10-20T19:42:07.0910754Z PLAY [jboss] *******************************************************************
2026-10-20T19:42:07.0963036Z 
2026-10-20T19:42:07.0963340Z PLAY [jboss] *******************************************************************
2026-10-20T19:42:07.0998491Z 
2026-10-20T19:42:07.0998789Z PLAY [Copiando deployments adicionais] *****************************************
2026-10-20T19:42:07.1032119Z 
2026-10-20T19:42:07.1032553Z PLAY [Copiando modules adicionais] *********************************************
2026-10-20T19:42:07.1069719Z 
2026-10-20T19:42:07.1069922Z PLAY [jboss] *******************************************************************
2026-10-20T19:42:07.1114753Z 
2026-10-20T19:42:07.1114935Z PLAY [jboss] *******************************************************************
2026-10-20T19:42:07.1155507Z 
2026-10-20T19:42:07.1155857Z PLAY [jboss] *******************************************************************
2026-10-20T19:42:07.1217451Z Tuesday 20 October 2026  16:42:07 -0300 (0:00:00.555)       0:00:00.892 ******* 
2026-10-20T19:42:07.5259477Z 
2026-10-20T19:42:07.5260022Z TASK [Wait for Jboss Management port] ******************************************
2026-10-20T19:42:07.5260185Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T19:42:07.5295500Z Tuesday 20 October 2026  16:42:07 -0300 (0:00:00.407)       0:00:01.300 ******* 
2026-10-20T19:42:08.2498661Z 
2026-10-20T19:42:08.2499478Z TASK [Check if Jboss is Running] ***********************************************
2026-10-20T19:42:08.2499675Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T19:42:08.2532005Z Tuesday 20 October 2026  16:42:08 -0300 (0:00:00.723)       0:00:02.024 ******* 
2026-10-20T19:42:08.7774812Z FAILED - RETRYING: Check Deployment details looking for status OK (60 retries left).
2026-10-20T19:42:14.1669981Z FAILED - RETRYING: Check Deployment details looking for status OK (59 retries left).
2026-10-20T19:42:19.5398425Z FAILED - RETRYING: Check Deployment details looking for status OK (58 retries left).
2026-10-20T19:42:24.9039669Z FAILED - RETRYING: Check Deployment details looking for status OK (57 retries left).
2026-10-20T19:42:30.2792153Z FAILED - RETRYING: Check Deployment details looking for status OK (56 retries left).
2026-10-20T19:42:35.6426051Z FAILED - RETRYING: Check Deployment details looking for status OK (55 retries left).
2026-10-20T19:42:41.0052731Z FAILED - RETRYING: Check Deployment details looking for status OK (54 retries left).
2026-10-20T19:42:46.3832768Z FAILED - RETRYING: Check Deployment details looking for status OK (53 retries left).
2026-10-20T19:42:51.7574954Z FAILED - RETRYING: Check Deployment details looking for status OK (52 retries left).
2026-10-20T19:42:57.1222464Z FAILED - RETRYING: Check Deployment details looking for status OK (51 retries left).
2026-10-20T19:43:02.5122776Z FAILED - RETRYING: Check Deployment details looking for status OK (50 retries left).
2026-10-20T19:43:07.8818109Z FAILED - RETRYING: Check Deployment details looking for status OK (49 retries left).
2026-10-20T19:43:13.2513509Z FAILED - RETRYING: Check Deployment details looking for status OK (48 retries left).
2026-10-20T19:43:18.6616618Z FAILED - RETRYING: Check Deployment details looking for status OK (47 retries left).
2026-10-20T19:43:24.0239878Z FAILED - RETRYING: Check Deployment details looking for status OK (46 retries left).
2026-10-20T19:43:29.3893841Z FAILED - RETRYING: Check Deployment details looking for status OK (45 retries left).
2026-10-20T19:43:34.7697539Z FAILED - RETRYING: Check Deployment details looking for status OK (44 retries left).
2026-10-20T19:43:40.1332935Z FAILED - RETRYING: Check Deployment details looking for status OK (43 retries left).
2026-10-20T19:43:45.5101888Z FAILED - RETRYING: Check Deployment details looking for status OK (42 retries left).
2026-10-20T19:43:50.8926170Z FAILED - RETRYING: Check Deployment details looking for status OK (41 retries left).
2026-10-20T19:43:56.2639923Z FAILED - RETRYING: Check Deployment details looking for status OK (40 retries left).
2026-10-20T19:44:01.6295326Z FAILED - RETRYING: Check Deployment details looking for status OK (39 retries left).
2026-10-20T19:44:07.0159872Z FAILED - RETRYING: Check Deployment details looking for status OK (38 retries left).
2026-10-20T19:44:12.3804323Z FAILED - RETRYING: Check Deployment details looking for status OK (37 retries left).
2026-10-20T19:44:17.7415894Z FAILED - RETRYING: Check Deployment details looking for status OK (36 retries left).
2026-10-20T19:44:23.1372447Z FAILED - RETRYING: Check Deployment details looking for status OK (35 retries left).
2026-10-20T19:44:28.5009384Z FAILED - RETRYING: Check Deployment details looking for status OK (34 retries left).
2026-10-20T19:44:33.8680228Z FAILED - RETRYING: Check Deployment details looking for status OK (33 retries left).
2026-10-20T19:44:39.2432822Z FAILED - RETRYING: Check Deployment details looking for status OK (32 retries left).
2026-10-20T19:44:44.6063617Z FAILED - RETRYING: Check Deployment details looking for status OK (31 retries left).
2026-10-20T19:44:49.9683611Z FAILED - RETRYING: Check Deployment details looking for status OK (30 retries left).
2026-10-20T19:44:55.3479503Z FAILED - RETRYING: Check Deployment details looking for status OK (29 retries left).
2026-10-20T19:45:00.7203711Z FAILED - RETRYING: Check Deployment details looking for status OK (28 retries left).
2026-10-20T19:45:06.0893336Z FAILED - RETRYING: Check Deployment details looking for status OK (27 retries left).
2026-10-20T19:45:11.4670566Z FAILED - RETRYING: Check Deployment details looking for status OK (26 retries left).
2026-10-20T19:45:16.8359413Z FAILED - RETRYING: Check Deployment details looking for status OK (25 retries left).
2026-10-20T19:45:22.1993309Z FAILED - RETRYING: Check Deployment details looking for status OK (24 retries left).
2026-10-20T19:45:27.5779706Z FAILED - RETRYING: Check Deployment details looking for status OK (23 retries left).
2026-10-20T19:45:32.9487406Z FAILED - RETRYING: Check Deployment details looking for status OK (22 retries left).
2026-10-20T19:45:38.3123550Z FAILED - RETRYING: Check Deployment details looking for status OK (21 retries left).
2026-10-20T19:45:43.6880163Z FAILED - RETRYING: Check Deployment details looking for status OK (20 retries left).
2026-10-20T19:45:49.0539977Z FAILED - RETRYING: Check Deployment details looking for status OK (19 retries left).
2026-10-20T19:45:54.4251912Z FAILED - RETRYING: Check Deployment details looking for status OK (18 retries left).
2026-10-20T19:45:59.7975909Z FAILED - RETRYING: Check Deployment details looking for status OK (17 retries left).
2026-10-20T19:46:05.1657107Z FAILED - RETRYING: Check Deployment details looking for status OK (16 retries left).
2026-10-20T19:46:10.5274783Z FAILED - RETRYING: Check Deployment details looking for status OK (15 retries left).
2026-10-20T19:46:15.9017460Z FAILED - RETRYING: Check Deployment details looking for status OK (14 retries left).
2026-10-20T19:46:21.2633230Z FAILED - RETRYING: Check Deployment details looking for status OK (13 retries left).
2026-10-20T19:46:26.6315883Z FAILED - RETRYING: Check Deployment details looking for status OK (12 retries left).
2026-10-20T19:46:32.0096824Z FAILED - RETRYING: Check Deployment details looking for status OK (11 retries left).
2026-10-20T19:46:37.3765780Z FAILED - RETRYING: Check Deployment details looking for status OK (10 retries left).
2026-10-20T19:46:42.7384635Z FAILED - RETRYING: Check Deployment details looking for status OK (9 retries left).
2026-10-20T19:46:48.1097421Z FAILED - RETRYING: Check Deployment details looking for status OK (8 retries left).
2026-10-20T19:46:53.4711840Z FAILED - RETRYING: Check Deployment details looking for status OK (7 retries left).
2026-10-20T19:46:58.8240054Z FAILED - RETRYING: Check Deployment details looking for status OK (6 retries left).
2026-10-20T19:47:04.2131693Z FAILED - RETRYING: Check Deployment details looking for status OK (5 retries left).
2026-10-20T19:47:09.5755953Z FAILED - RETRYING: Check Deployment details looking for status OK (4 retries left).
2026-10-20T19:47:14.9399836Z FAILED - RETRYING: Check Deployment details looking for status OK (3 retries left).
2026-10-20T19:47:20.3305446Z FAILED - RETRYING: Check Deployment details looking for status OK (2 retries left).
2026-10-20T19:47:25.6919676Z FAILED - RETRYING: Check Deployment details looking for status OK (1 retries left).
2026-10-20T19:47:31.0559478Z 
2026-10-20T19:47:31.0560004Z TASK [Check Deployment details looking for status OK] **************************
2026-10-20T19:47:31.0569577Z fatal: [caddeapllx955.agil.nprd.caixa.gov.br]: FAILED! => {"attempts": 60, "changed": false, "connection": "close", "content": "{\"outcome\" : \"success\", \"result\" : {\"sigsj_intranet-ear.ear\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"zDAjxGeD6I65CycLTstCisreKJ4=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1792525312126, \"enabled-timestamp\" : \"2026-10-20 16:41:52,126 BRT\", \"managed\" : true, \"name\" : \"sigsj_intranet-ear.ear\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"sigsj_intranet-ear.ear\", \"status\" : \"FAILED\", \"subdeployment\" : {\"sigsj_intranet.war\" : null}, \"subsystem\" : {\"logging\" : null}}, \"sirotcon-ejb.jar\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"cLE7JH7Axwql5UcepAdPvwrhtws=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1792525312140, \"enabled-timestamp\" : \"2026-10-20 16:41:52,140 BRT\", \"managed\" : true, \"name\" : \"sirotcon-ejb.jar\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"sirotcon-ejb.jar\", \"status\" : \"OK\", \"subdeployment\" : null, \"subsystem\" : {\"ejb3\" : null, \"logging\" : null}}}}", "content_encoding": "identity", "content_length": "1128", "content_type": "application/json; charset=utf-8", "cookies": {}, "cookies_string": "", "date": "Tue, 20 Oct 2026 19:47:30 GMT", "elapsed": 0, "json": {"outcome": "success", "result": {"sigsj_intranet-ear.ear": {"content": [{"hash": {"BYTES_VALUE": "zDAjxGeD6I65CycLTstCisreKJ4="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1792525312126, "enabled-timestamp": "2026-10-20 16:41:52,126 BRT", "managed": true, "name": "sigsj_intranet-ear.ear", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "sigsj_intranet-ear.ear", "status": "FAILED", "subdeployment": {"sigsj_intranet.war": null}, "subsystem": {"logging": null}}, "sirotcon-ejb.jar": {"content": [{"hash": {"BYTES_VALUE": "cLE7JH7Axwql5UcepAdPvwrhtws="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1792525312140, "enabled-timestamp": "2026-10-20 16:41:52,140 BRT", "managed": true, "name": "sirotcon-ejb.jar", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "sirotcon-ejb.jar", "status": "OK", "subdeployment": null, "subsystem": {"ejb3": null, "logging": null}}}}, "msg": "OK (1128 bytes)", "redirected": false, "status": 200, "url": "http://10.116.194.179:9990/management/", "x_content_type_options": "nosniff", "x_frame_options": "SAMEORIGIN"}
2026-10-20T19:47:31.0605124Z Tuesday 20 October 2026  16:47:31 -0300 (0:05:22.807)       0:05:24.831 ******* 
2026-10-20T19:47:43.8513544Z 
2026-10-20T19:47:43.8514014Z TASK [systemd] *****************************************************************
2026-10-20T19:47:43.8514207Z changed: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T19:47:43.8561680Z Tuesday 20 October 2026  16:47:43 -0300 (0:00:12.795)       0:05:37.626 ******* 
2026-10-20T19:47:44.1953789Z 
2026-10-20T19:47:44.1954280Z TASK [Wait for Jboss Management port] ******************************************
2026-10-20T19:47:44.1954482Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T19:47:44.1988655Z Tuesday 20 October 2026  16:47:44 -0300 (0:00:00.342)       0:05:37.969 ******* 
2026-10-20T19:47:45.0267917Z FAILED - RETRYING: Check if Jboss is Running (120 retries left).
2026-10-20T19:47:50.4372610Z 
2026-10-20T19:47:50.4373182Z TASK [Check if Jboss is Running] ***********************************************
2026-10-20T19:47:50.4373450Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T19:47:50.4409808Z Tuesday 20 October 2026  16:47:50 -0300 (0:00:06.242)       0:05:44.211 ******* 
2026-10-20T19:47:50.9198506Z FAILED - RETRYING: Check Deployment details looking for status OK (60 retries left).
2026-10-20T19:47:56.3589691Z FAILED - RETRYING: Check Deployment details looking for status OK (59 retries left).
2026-10-20T19:48:01.7580695Z FAILED - RETRYING: Check Deployment details looking for status OK (58 retries left).
2026-10-20T19:48:07.1228866Z FAILED - RETRYING: Check Deployment details looking for status OK (57 retries left).
2026-10-20T19:48:12.4938363Z FAILED - RETRYING: Check Deployment details looking for status OK (56 retries left).
2026-10-20T19:48:17.8647863Z FAILED - RETRYING: Check Deployment details looking for status OK (55 retries left).
2026-10-20T19:48:23.2343451Z FAILED - RETRYING: Check Deployment details looking for status OK (54 retries left).
2026-10-20T19:48:28.5968853Z FAILED - RETRYING: Check Deployment details looking for status OK (53 retries left).
2026-10-20T19:48:33.9710013Z FAILED - RETRYING: Check Deployment details looking for status OK (52 retries left).
2026-10-20T19:48:39.3369874Z FAILED - RETRYING: Check Deployment details looking for status OK (51 retries left).
2026-10-20T19:48:44.7060938Z FAILED - RETRYING: Check Deployment details looking for status OK (50 retries left).
2026-10-20T19:48:50.0880302Z FAILED - RETRYING: Check Deployment details looking for status OK (49 retries left).
2026-10-20T19:48:55.4574872Z FAILED - RETRYING: Check Deployment details looking for status OK (48 retries left).
2026-10-20T19:49:00.8275782Z FAILED - RETRYING: Check Deployment details looking for status OK (47 retries left).
2026-10-20T19:49:06.2151580Z FAILED - RETRYING: Check Deployment details looking for status OK (46 retries left).
2026-10-20T19:49:11.5871820Z FAILED - RETRYING: Check Deployment details looking for status OK (45 retries left).
2026-10-20T19:49:16.9506118Z FAILED - RETRYING: Check Deployment details looking for status OK (44 retries left).
2026-10-20T19:49:22.3858432Z FAILED - RETRYING: Check Deployment details looking for status OK (43 retries left).
2026-10-20T19:49:27.7484021Z FAILED - RETRYING: Check Deployment details looking for status OK (42 retries left).
2026-10-20T19:49:33.1187052Z FAILED - RETRYING: Check Deployment details looking for status OK (41 retries left).
2026-10-20T19:49:38.4938964Z FAILED - RETRYING: Check Deployment details looking for status OK (40 retries left).
2026-10-20T19:49:43.8489112Z FAILED - RETRYING: Check Deployment details looking for status OK (39 retries left).
2026-10-20T19:49:49.2104564Z FAILED - RETRYING: Check Deployment details looking for status OK (38 retries left).
2026-10-20T19:49:54.5835594Z FAILED - RETRYING: Check Deployment details looking for status OK (37 retries left).
2026-10-20T19:49:59.9514218Z FAILED - RETRYING: Check Deployment details looking for status OK (36 retries left).
2026-10-20T19:50:05.3229589Z FAILED - RETRYING: Check Deployment details looking for status OK (35 retries left).
2026-10-20T19:50:10.6933051Z FAILED - RETRYING: Check Deployment details looking for status OK (34 retries left).
2026-10-20T19:50:16.0704867Z FAILED - RETRYING: Check Deployment details looking for status OK (33 retries left).
2026-10-20T19:50:21.4345553Z FAILED - RETRYING: Check Deployment details looking for status OK (32 retries left).
2026-10-20T19:50:26.8110279Z FAILED - RETRYING: Check Deployment details looking for status OK (31 retries left).
2026-10-20T19:50:32.1701682Z FAILED - RETRYING: Check Deployment details looking for status OK (30 retries left).
2026-10-20T19:50:37.5367409Z FAILED - RETRYING: Check Deployment details looking for status OK (29 retries left).
2026-10-20T19:50:42.9106218Z FAILED - RETRYING: Check Deployment details looking for status OK (28 retries left).
2026-10-20T19:50:48.2742491Z FAILED - RETRYING: Check Deployment details looking for status OK (27 retries left).
2026-10-20T19:50:53.6457164Z FAILED - RETRYING: Check Deployment details looking for status OK (26 retries left).
2026-10-20T19:50:59.0196397Z FAILED - RETRYING: Check Deployment details looking for status OK (25 retries left).
2026-10-20T19:51:04.3847268Z FAILED - RETRYING: Check Deployment details looking for status OK (24 retries left).
2026-10-20T19:51:09.7474303Z FAILED - RETRYING: Check Deployment details looking for status OK (23 retries left).
2026-10-20T19:51:15.1244216Z FAILED - RETRYING: Check Deployment details looking for status OK (22 retries left).
2026-10-20T19:51:20.4896379Z FAILED - RETRYING: Check Deployment details looking for status OK (21 retries left).
2026-10-20T19:51:25.8587366Z FAILED - RETRYING: Check Deployment details looking for status OK (20 retries left).
2026-10-20T19:51:31.2374050Z FAILED - RETRYING: Check Deployment details looking for status OK (19 retries left).
2026-10-20T19:51:36.5983983Z FAILED - RETRYING: Check Deployment details looking for status OK (18 retries left).
2026-10-20T19:51:41.9654286Z FAILED - RETRYING: Check Deployment details looking for status OK (17 retries left).
2026-10-20T19:51:47.3403933Z FAILED - RETRYING: Check Deployment details looking for status OK (16 retries left).
2026-10-20T19:51:52.7274802Z FAILED - RETRYING: Check Deployment details looking for status OK (15 retries left).
2026-10-20T19:51:58.0908423Z FAILED - RETRYING: Check Deployment details looking for status OK (14 retries left).
2026-10-20T19:52:03.4701622Z FAILED - RETRYING: Check Deployment details looking for status OK (13 retries left).
2026-10-20T19:52:08.8331420Z FAILED - RETRYING: Check Deployment details looking for status OK (12 retries left).
2026-10-20T19:52:14.1985559Z FAILED - RETRYING: Check Deployment details looking for status OK (11 retries left).
2026-10-20T19:52:19.5715583Z FAILED - RETRYING: Check Deployment details looking for status OK (10 retries left).
2026-10-20T19:52:24.9365509Z FAILED - RETRYING: Check Deployment details looking for status OK (9 retries left).
2026-10-20T19:52:30.3032266Z FAILED - RETRYING: Check Deployment details looking for status OK (8 retries left).
2026-10-20T19:52:35.6813555Z FAILED - RETRYING: Check Deployment details looking for status OK (7 retries left).
2026-10-20T19:52:41.0458773Z FAILED - RETRYING: Check Deployment details looking for status OK (6 retries left).
2026-10-20T19:52:46.4114472Z FAILED - RETRYING: Check Deployment details looking for status OK (5 retries left).
2026-10-20T19:52:51.7855814Z FAILED - RETRYING: Check Deployment details looking for status OK (4 retries left).
2026-10-20T19:52:57.1654297Z FAILED - RETRYING: Check Deployment details looking for status OK (3 retries left).
2026-10-20T19:53:02.5299766Z FAILED - RETRYING: Check Deployment details looking for status OK (2 retries left).
2026-10-20T19:53:07.9027103Z FAILED - RETRYING: Check Deployment details looking for status OK (1 retries left).
2026-10-20T19:53:13.2704829Z 
2026-10-20T19:53:13.2705481Z TASK [Check Deployment details looking for status OK] **************************
2026-10-20T19:53:13.2715200Z fatal: [caddeapllx955.agil.nprd.caixa.gov.br]: FAILED! => {"attempts": 60, "changed": false, "connection": "close", "content": "{\"outcome\" : \"success\", \"result\" : {\"sigsj_intranet-ear.ear\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"zDAjxGeD6I65CycLTstCisreKJ4=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1792525661748, \"enabled-timestamp\" : \"2026-10-20 16:47:41,748 BRT\", \"managed\" : true, \"name\" : \"sigsj_intranet-ear.ear\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"sigsj_intranet-ear.ear\", \"status\" : \"FAILED\", \"subdeployment\" : {\"sigsj_intranet.war\" : null}, \"subsystem\" : {\"logging\" : null}}, \"sirotcon-ejb.jar\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"cLE7JH7Axwql5UcepAdPvwrhtws=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1792525661758, \"enabled-timestamp\" : \"2026-10-20 16:47:41,758 BRT\", \"managed\" : true, \"name\" : \"sirotcon-ejb.jar\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"sirotcon-ejb.jar\", \"status\" : \"OK\", \"subdeployment\" : null, \"subsystem\" : {\"ejb3\" : null, \"logging\" : null}}}}", "content_encoding": "identity", "content_length": "1128", "content_type": "application/json; charset=utf-8", "cookies": {}, "cookies_string": "", "date": "Tue, 20 Oct 2026 19:53:13 GMT", "elapsed": 0, "json": {"outcome": "success", "result": {"sigsj_intranet-ear.ear": {"content": [{"hash": {"BYTES_VALUE": "zDAjxGeD6I65CycLTstCisreKJ4="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1792525661748, "enabled-timestamp": "2026-10-20 16:47:41,748 BRT", "managed": true, "name": "sigsj_intranet-ear.ear", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "sigsj_intranet-ear.ear", "status": "FAILED", "subdeployment": {"sigsj_intranet.war": null}, "subsystem": {"logging": null}}, "sirotcon-ejb.jar": {"content": [{"hash": {"BYTES_VALUE": "cLE7JH7Axwql5UcepAdPvwrhtws="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1792525661758, "enabled-timestamp": "2026-10-20 16:47:41,758 BRT", "managed": true, "name": "sirotcon-ejb.jar", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "sirotcon-ejb.jar", "status": "OK", "subdeployment": null, "subsystem": {"ejb3": null, "logging": null}}}}, "msg": "OK (1128 bytes)", "redirected": false, "status": 200, "url": "http://10.116.194.179:9990/management/", "x_content_type_options": "nosniff", "x_frame_options": "SAMEORIGIN"}
2026-10-20T19:53:13.2734756Z 
2026-10-20T19:53:13.2735122Z PLAY RECAP *********************************************************************
2026-10-20T19:53:13.2735433Z caddeapllx955.agil.nprd.caixa.gov.br : ok=6    changed=1    unreachable=0    failed=1    skipped=0    rescued=1    ignored=0   
2026-10-20T19:53:13.2735579Z 
2026-10-20T19:53:13.2739217Z Tuesday 20 October 2026  16:53:13 -0300 (0:05:22.832)       0:11:07.044 ******* 
2026-10-20T19:53:13.2740296Z =============================================================================== 
2026-10-20T19:53:13.2740576Z Check Deployment details looking for status OK ------------------------ 322.83s
2026-10-20T19:53:13.2740898Z Check Deployment details looking for status OK ------------------------ 322.81s
2026-10-20T19:53:13.2741167Z systemd ---------------------------------------------------------------- 12.80s
2026-10-20T19:53:13.2741421Z Check if Jboss is Running ----------------------------------------------- 6.24s
2026-10-20T19:53:13.2741636Z Check if Jboss is Running ----------------------------------------------- 0.72s
2026-10-20T19:53:13.2741869Z Verifica ser o Jboss já foi instalado ----------------------------------- 0.56s
2026-10-20T19:53:13.2742089Z Wait for Jboss Management port ------------------------------------------ 0.41s
2026-10-20T19:53:13.2742296Z Wait for Jboss Management port ------------------------------------------ 0.34s
2026-10-20T19:53:13.2745536Z Playbook run took 0 days, 0 hours, 11 minutes, 7 seconds
2026-10-20T19:53:13.3369305Z ##[error]Bash exited with code '2'.
2026-10-20T19:53:13.3403217Z ##[section]Finishing: Check Deployments [JBOSS]





quevour denovo
