2026-10-20T18:27:58.7504731Z ##[section]Starting: Check Deployments [JBOSS]
2026-10-20T18:27:58.7508189Z ==============================================================================
2026-10-20T18:27:58.7508266Z Task         : Bash
2026-10-20T18:27:58.7508307Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-20T18:27:58.7508388Z Version      : 3.227.0
2026-10-20T18:27:58.7508431Z Author       : Microsoft Corporation
2026-10-20T18:27:58.7508479Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-20T18:27:58.7508558Z ==============================================================================
2026-10-20T18:27:59.5483141Z Generating script.
2026-10-20T18:27:59.5491433Z Script contents:
2026-10-20T18:27:59.5491925Z ansible-playbook /opt/ads-agent/_work/r18036/a/esteira-jboss-vm-v2/site.yml --tags check_deployments -e sistema_ambiente=des -e sistema_nome=sigsj-intranet -e site=ctc_nprd
2026-10-20T18:27:59.5495169Z ========================== Starting Command Output ===========================
2026-10-20T18:27:59.5502214Z [command]/bin/bash /opt/ads-agent/_work/_temp/95f68bba-1484-4a62-9aad-e7a787c55bc6.sh
2026-10-20T18:28:01.6556308Z 
2026-10-20T18:28:01.6557046Z PLAY [local] *******************************************************************
2026-10-20T18:28:01.6840699Z 
2026-10-20T18:28:01.6841881Z PLAY [Configurando o DNS] ******************************************************
2026-10-20T18:28:01.8753417Z 
2026-10-20T18:28:01.8754328Z PLAY [local] *******************************************************************
2026-10-20T18:28:01.8785541Z 
2026-10-20T18:28:01.8786254Z PLAY [Verificando serviços] ****************************************************
2026-10-20T18:28:01.8873154Z 
2026-10-20T18:28:01.8873812Z PLAY [Configuração LDAP] *******************************************************
2026-10-20T18:28:01.8905874Z [WARNING]: Found variable using reserved name: when
2026-10-20T18:28:01.8910548Z 
2026-10-20T18:28:01.8911126Z PLAY [jboss] *******************************************************************
2026-10-20T18:28:01.9002478Z 
2026-10-20T18:28:01.9002835Z PLAY [Stack Jboss] *************************************************************
2026-10-20T18:28:01.9251183Z Tuesday 20 October 2026  15:28:01 -0300 (0:00:00.330)       0:00:00.330 ******* 
2026-10-20T18:28:02.4572562Z 
2026-10-20T18:28:02.4575677Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-10-20T18:28:02.4575893Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-20T18:28:02.4576217Z caddeapllx955.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-20T18:28:02.4576376Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-20T18:28:02.4576544Z releases. A future Ansible release will default to using the discovered 
2026-10-20T18:28:02.4576716Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-20T18:28:02.4576883Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-20T18:28:02.4577059Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-20T18:28:02.4577207Z setting deprecation_warnings=False in ansible.cfg.
2026-10-20T18:28:02.4577342Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T18:28:02.4600088Z 
2026-10-20T18:28:02.4600331Z PLAY [jboss] *******************************************************************
2026-10-20T18:28:02.4641565Z 
2026-10-20T18:28:02.4641947Z PLAY [jboss] *******************************************************************
2026-10-20T18:28:02.4682190Z 
2026-10-20T18:28:02.4682504Z PLAY [jboss] *******************************************************************
2026-10-20T18:28:02.4710060Z 
2026-10-20T18:28:02.4710576Z PLAY [Copiando deployments adicionais] *****************************************
2026-10-20T18:28:02.4741603Z 
2026-10-20T18:28:02.4742481Z PLAY [Copiando modules adicionais] *********************************************
2026-10-20T18:28:02.4773320Z 
2026-10-20T18:28:02.4773914Z PLAY [jboss] *******************************************************************
2026-10-20T18:28:02.4816069Z 
2026-10-20T18:28:02.4816984Z PLAY [jboss] *******************************************************************
2026-10-20T18:28:02.4858039Z 
2026-10-20T18:28:02.4858616Z PLAY [jboss] *******************************************************************
2026-10-20T18:28:02.4911411Z Tuesday 20 October 2026  15:28:02 -0300 (0:00:00.565)       0:00:00.896 ******* 
2026-10-20T18:28:02.8645742Z 
2026-10-20T18:28:02.8646276Z TASK [Wait for Jboss Management port] ******************************************
2026-10-20T18:28:02.8646437Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T18:28:02.8673852Z Tuesday 20 October 2026  15:28:02 -0300 (0:00:00.376)       0:00:01.272 ******* 
2026-10-20T18:28:03.5623816Z 
2026-10-20T18:28:03.5624364Z TASK [Check if Jboss is Running] ***********************************************
2026-10-20T18:28:03.5624538Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T18:28:03.5651699Z Tuesday 20 October 2026  15:28:03 -0300 (0:00:00.697)       0:00:01.970 ******* 
2026-10-20T18:28:04.0002155Z FAILED - RETRYING: Check Deployment details looking for status OK (60 retries left).
2026-10-20T18:28:09.3769004Z FAILED - RETRYING: Check Deployment details looking for status OK (59 retries left).
2026-10-20T18:28:14.7545309Z FAILED - RETRYING: Check Deployment details looking for status OK (58 retries left).
2026-10-20T18:28:20.1193797Z FAILED - RETRYING: Check Deployment details looking for status OK (57 retries left).
2026-10-20T18:28:25.4762780Z FAILED - RETRYING: Check Deployment details looking for status OK (56 retries left).
2026-10-20T18:28:30.8393425Z FAILED - RETRYING: Check Deployment details looking for status OK (55 retries left).
2026-10-20T18:28:36.2017251Z FAILED - RETRYING: Check Deployment details looking for status OK (54 retries left).
2026-10-20T18:28:41.5656593Z FAILED - RETRYING: Check Deployment details looking for status OK (53 retries left).
2026-10-20T18:28:46.9409903Z FAILED - RETRYING: Check Deployment details looking for status OK (52 retries left).
2026-10-20T18:28:52.3029692Z FAILED - RETRYING: Check Deployment details looking for status OK (51 retries left).
2026-10-20T18:28:57.6569794Z FAILED - RETRYING: Check Deployment details looking for status OK (50 retries left).
2026-10-20T18:29:03.0260029Z FAILED - RETRYING: Check Deployment details looking for status OK (49 retries left).
2026-10-20T18:29:08.3783074Z FAILED - RETRYING: Check Deployment details looking for status OK (48 retries left).
2026-10-20T18:29:13.7299730Z FAILED - RETRYING: Check Deployment details looking for status OK (47 retries left).
2026-10-20T18:29:19.0954046Z FAILED - RETRYING: Check Deployment details looking for status OK (46 retries left).
2026-10-20T18:29:24.4528581Z FAILED - RETRYING: Check Deployment details looking for status OK (45 retries left).
2026-10-20T18:29:29.8121121Z FAILED - RETRYING: Check Deployment details looking for status OK (44 retries left).
2026-10-20T18:29:35.1814339Z FAILED - RETRYING: Check Deployment details looking for status OK (43 retries left).
2026-10-20T18:29:40.5365410Z FAILED - RETRYING: Check Deployment details looking for status OK (42 retries left).
2026-10-20T18:29:45.8906758Z FAILED - RETRYING: Check Deployment details looking for status OK (41 retries left).
2026-10-20T18:29:51.2705317Z FAILED - RETRYING: Check Deployment details looking for status OK (40 retries left).
2026-10-20T18:29:56.6459956Z FAILED - RETRYING: Check Deployment details looking for status OK (39 retries left).
2026-10-20T18:30:02.0174344Z FAILED - RETRYING: Check Deployment details looking for status OK (38 retries left).
2026-10-20T18:30:07.3838228Z FAILED - RETRYING: Check Deployment details looking for status OK (37 retries left).
2026-10-20T18:30:12.7379188Z FAILED - RETRYING: Check Deployment details looking for status OK (36 retries left).
2026-10-20T18:30:18.0937021Z FAILED - RETRYING: Check Deployment details looking for status OK (35 retries left).
2026-10-20T18:30:23.4543855Z FAILED - RETRYING: Check Deployment details looking for status OK (34 retries left).
2026-10-20T18:30:28.8034231Z FAILED - RETRYING: Check Deployment details looking for status OK (33 retries left).
2026-10-20T18:30:34.1626434Z FAILED - RETRYING: Check Deployment details looking for status OK (32 retries left).
2026-10-20T18:30:39.5419598Z FAILED - RETRYING: Check Deployment details looking for status OK (31 retries left).
2026-10-20T18:30:44.8951537Z FAILED - RETRYING: Check Deployment details looking for status OK (30 retries left).
2026-10-20T18:30:50.2574107Z FAILED - RETRYING: Check Deployment details looking for status OK (29 retries left).
2026-10-20T18:30:55.6233197Z FAILED - RETRYING: Check Deployment details looking for status OK (28 retries left).
2026-10-20T18:31:00.9866981Z FAILED - RETRYING: Check Deployment details looking for status OK (27 retries left).
2026-10-20T18:31:06.3418329Z FAILED - RETRYING: Check Deployment details looking for status OK (26 retries left).
2026-10-20T18:31:11.7104273Z FAILED - RETRYING: Check Deployment details looking for status OK (25 retries left).
2026-10-20T18:31:17.0669491Z FAILED - RETRYING: Check Deployment details looking for status OK (24 retries left).
2026-10-20T18:31:22.4314284Z FAILED - RETRYING: Check Deployment details looking for status OK (23 retries left).
2026-10-20T18:31:27.8004146Z FAILED - RETRYING: Check Deployment details looking for status OK (22 retries left).
2026-10-20T18:31:33.1602759Z FAILED - RETRYING: Check Deployment details looking for status OK (21 retries left).
2026-10-20T18:31:38.5194051Z FAILED - RETRYING: Check Deployment details looking for status OK (20 retries left).
2026-10-20T18:31:43.8827560Z FAILED - RETRYING: Check Deployment details looking for status OK (19 retries left).
2026-10-20T18:31:49.2466939Z FAILED - RETRYING: Check Deployment details looking for status OK (18 retries left).
2026-10-20T18:31:54.6107638Z FAILED - RETRYING: Check Deployment details looking for status OK (17 retries left).
2026-10-20T18:31:59.9939668Z FAILED - RETRYING: Check Deployment details looking for status OK (16 retries left).
2026-10-20T18:32:05.3539001Z FAILED - RETRYING: Check Deployment details looking for status OK (15 retries left).
2026-10-20T18:32:10.7185161Z FAILED - RETRYING: Check Deployment details looking for status OK (14 retries left).
2026-10-20T18:32:16.0849428Z FAILED - RETRYING: Check Deployment details looking for status OK (13 retries left).
2026-10-20T18:32:21.4462089Z FAILED - RETRYING: Check Deployment details looking for status OK (12 retries left).
2026-10-20T18:32:26.8024270Z FAILED - RETRYING: Check Deployment details looking for status OK (11 retries left).
2026-10-20T18:32:32.1690894Z FAILED - RETRYING: Check Deployment details looking for status OK (10 retries left).
2026-10-20T18:32:37.5276801Z FAILED - RETRYING: Check Deployment details looking for status OK (9 retries left).
2026-10-20T18:32:42.8806682Z FAILED - RETRYING: Check Deployment details looking for status OK (8 retries left).
2026-10-20T18:32:48.2529902Z FAILED - RETRYING: Check Deployment details looking for status OK (7 retries left).
2026-10-20T18:32:53.6108156Z FAILED - RETRYING: Check Deployment details looking for status OK (6 retries left).
2026-10-20T18:32:58.9746283Z FAILED - RETRYING: Check Deployment details looking for status OK (5 retries left).
2026-10-20T18:33:04.3407717Z FAILED - RETRYING: Check Deployment details looking for status OK (4 retries left).
2026-10-20T18:33:09.7017366Z FAILED - RETRYING: Check Deployment details looking for status OK (3 retries left).
2026-10-20T18:33:15.0617190Z FAILED - RETRYING: Check Deployment details looking for status OK (2 retries left).
2026-10-20T18:33:20.4310062Z FAILED - RETRYING: Check Deployment details looking for status OK (1 retries left).
2026-10-20T18:33:25.7883000Z 
2026-10-20T18:33:25.7883541Z TASK [Check Deployment details looking for status OK] **************************
2026-10-20T18:33:25.7891334Z fatal: [caddeapllx955.agil.nprd.caixa.gov.br]: FAILED! => {"attempts": 60, "changed": false, "connection": "close", "content": "{\"outcome\" : \"success\", \"result\" : {\"sigsj_intranet-ear.ear\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"zDAjxGeD6I65CycLTstCisreKJ4=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1792520865511, \"enabled-timestamp\" : \"2026-10-20 15:27:45,511 BRT\", \"managed\" : true, \"name\" : \"sigsj_intranet-ear.ear\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"sigsj_intranet-ear.ear\", \"status\" : \"FAILED\", \"subdeployment\" : {\"sigsj_intranet.war\" : null}, \"subsystem\" : {\"logging\" : null}}}}", "content_encoding": "identity", "content_length": "598", "content_type": "application/json; charset=utf-8", "cookies": {}, "cookies_string": "", "date": "Tue, 20 Oct 2026 18:33:25 GMT", "elapsed": 0, "json": {"outcome": "success", "result": {"sigsj_intranet-ear.ear": {"content": [{"hash": {"BYTES_VALUE": "zDAjxGeD6I65CycLTstCisreKJ4="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1792520865511, "enabled-timestamp": "2026-10-20 15:27:45,511 BRT", "managed": true, "name": "sigsj_intranet-ear.ear", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "sigsj_intranet-ear.ear", "status": "FAILED", "subdeployment": {"sigsj_intranet.war": null}, "subsystem": {"logging": null}}}}, "msg": "OK (598 bytes)", "redirected": false, "status": 200, "url": "http://10.116.194.179:9990/management/", "x_content_type_options": "nosniff", "x_frame_options": "SAMEORIGIN"}
2026-10-20T18:33:25.7920276Z Tuesday 20 October 2026  15:33:25 -0300 (0:05:22.226)       0:05:24.197 ******* 
2026-10-20T18:33:38.5604241Z 
2026-10-20T18:33:38.5604808Z TASK [systemd] *****************************************************************
2026-10-20T18:33:38.5608882Z changed: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T18:33:38.5642884Z Tuesday 20 October 2026  15:33:38 -0300 (0:00:12.772)       0:05:36.969 ******* 
2026-10-20T18:33:38.8715411Z 
2026-10-20T18:33:38.8715942Z TASK [Wait for Jboss Management port] ******************************************
2026-10-20T18:33:38.8716115Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T18:33:38.8748318Z Tuesday 20 October 2026  15:33:38 -0300 (0:00:00.310)       0:05:37.280 ******* 
2026-10-20T18:33:39.5227772Z FAILED - RETRYING: Check if Jboss is Running (120 retries left).
2026-10-20T18:33:44.9278601Z 
2026-10-20T18:33:44.9279498Z TASK [Check if Jboss is Running] ***********************************************
2026-10-20T18:33:44.9279752Z ok: [caddeapllx955.agil.nprd.caixa.gov.br]
2026-10-20T18:33:44.9310718Z Tuesday 20 October 2026  15:33:44 -0300 (0:00:06.056)       0:05:43.336 ******* 
2026-10-20T18:33:45.3932543Z FAILED - RETRYING: Check Deployment details looking for status OK (60 retries left).
2026-10-20T18:33:50.8054961Z FAILED - RETRYING: Check Deployment details looking for status OK (59 retries left).
2026-10-20T18:33:56.2027165Z FAILED - RETRYING: Check Deployment details looking for status OK (58 retries left).
2026-10-20T18:34:01.5704864Z FAILED - RETRYING: Check Deployment details looking for status OK (57 retries left).
2026-10-20T18:34:06.9331412Z FAILED - RETRYING: Check Deployment details looking for status OK (56 retries left).
2026-10-20T18:34:12.3122821Z FAILED - RETRYING: Check Deployment details looking for status OK (55 retries left).
2026-10-20T18:34:17.6758973Z FAILED - RETRYING: Check Deployment details looking for status OK (54 retries left).
2026-10-20T18:34:23.0466539Z FAILED - RETRYING: Check Deployment details looking for status OK (53 retries left).
2026-10-20T18:34:28.4288809Z FAILED - RETRYING: Check Deployment details looking for status OK (52 retries left).
2026-10-20T18:34:33.7927365Z FAILED - RETRYING: Check Deployment details looking for status OK (51 retries left).
2026-10-20T18:34:39.1538971Z FAILED - RETRYING: Check Deployment details looking for status OK (50 retries left).
2026-10-20T18:34:44.5273376Z FAILED - RETRYING: Check Deployment details looking for status OK (49 retries left).
2026-10-20T18:34:49.8934491Z FAILED - RETRYING: Check Deployment details looking for status OK (48 retries left).
2026-10-20T18:34:55.2513285Z FAILED - RETRYING: Check Deployment details looking for status OK (47 retries left).
2026-10-20T18:35:00.6286079Z FAILED - RETRYING: Check Deployment details looking for status OK (46 retries left).
2026-10-20T18:35:05.9865855Z FAILED - RETRYING: Check Deployment details looking for status OK (45 retries left).
2026-10-20T18:35:11.3518404Z FAILED - RETRYING: Check Deployment details looking for status OK (44 retries left).
2026-10-20T18:35:16.7351506Z FAILED - RETRYING: Check Deployment details looking for status OK (43 retries left).
2026-10-20T18:35:22.0919536Z FAILED - RETRYING: Check Deployment details looking for status OK (42 retries left).
2026-10-20T18:35:27.4522187Z FAILED - RETRYING: Check Deployment details looking for status OK (41 retries left).
2026-10-20T18:35:32.8277136Z FAILED - RETRYING: Check Deployment details looking for status OK (40 retries left).
2026-10-20T18:35:38.1835981Z FAILED - RETRYING: Check Deployment details looking for status OK (39 retries left).
2026-10-20T18:35:43.5425279Z FAILED - RETRYING: Check Deployment details looking for status OK (38 retries left).
2026-10-20T18:35:48.9100370Z FAILED - RETRYING: Check Deployment details looking for status OK (37 retries left).
2026-10-20T18:35:54.2759066Z FAILED - RETRYING: Check Deployment details looking for status OK (36 retries left).
2026-10-20T18:35:59.6359103Z FAILED - RETRYING: Check Deployment details looking for status OK (35 retries left).
2026-10-20T18:36:05.0024824Z FAILED - RETRYING: Check Deployment details looking for status OK (34 retries left).
2026-10-20T18:36:10.3693498Z FAILED - RETRYING: Check Deployment details looking for status OK (33 retries left).
2026-10-20T18:36:15.7221295Z FAILED - RETRYING: Check Deployment details looking for status OK (32 retries left).
2026-10-20T18:36:21.0881353Z FAILED - RETRYING: Check Deployment details looking for status OK (31 retries left).
2026-10-20T18:36:26.4441053Z FAILED - RETRYING: Check Deployment details looking for status OK (30 retries left).
2026-10-20T18:36:31.8028774Z FAILED - RETRYING: Check Deployment details looking for status OK (29 retries left).
2026-10-20T18:36:37.1681604Z FAILED - RETRYING: Check Deployment details looking for status OK (28 retries left).
2026-10-20T18:36:42.5316775Z FAILED - RETRYING: Check Deployment details looking for status OK (27 retries left).
2026-10-20T18:36:47.8886985Z FAILED - RETRYING: Check Deployment details looking for status OK (26 retries left).
2026-10-20T18:36:53.2662452Z FAILED - RETRYING: Check Deployment details looking for status OK (25 retries left).
2026-10-20T18:36:58.6237337Z FAILED - RETRYING: Check Deployment details looking for status OK (24 retries left).
2026-10-20T18:37:03.9866368Z FAILED - RETRYING: Check Deployment details looking for status OK (23 retries left).
2026-10-20T18:37:09.3652939Z FAILED - RETRYING: Check Deployment details looking for status OK (22 retries left).
2026-10-20T18:37:14.7219358Z FAILED - RETRYING: Check Deployment details looking for status OK (21 retries left).
2026-10-20T18:37:20.0766407Z FAILED - RETRYING: Check Deployment details looking for status OK (20 retries left).
2026-10-20T18:37:25.4451943Z FAILED - RETRYING: Check Deployment details looking for status OK (19 retries left).
2026-10-20T18:37:30.8121111Z FAILED - RETRYING: Check Deployment details looking for status OK (18 retries left).
2026-10-20T18:37:36.1739958Z FAILED - RETRYING: Check Deployment details looking for status OK (17 retries left).
2026-10-20T18:37:41.5490218Z FAILED - RETRYING: Check Deployment details looking for status OK (16 retries left).
2026-10-20T18:37:46.9121436Z FAILED - RETRYING: Check Deployment details looking for status OK (15 retries left).
2026-10-20T18:37:52.2774430Z FAILED - RETRYING: Check Deployment details looking for status OK (14 retries left).
2026-10-20T18:37:57.6470348Z FAILED - RETRYING: Check Deployment details looking for status OK (13 retries left).
2026-10-20T18:38:03.0042915Z FAILED - RETRYING: Check Deployment details looking for status OK (12 retries left).
2026-10-20T18:38:08.3681841Z FAILED - RETRYING: Check Deployment details looking for status OK (11 retries left).
2026-10-20T18:38:13.7433407Z FAILED - RETRYING: Check Deployment details looking for status OK (10 retries left).
2026-10-20T18:38:19.0995327Z FAILED - RETRYING: Check Deployment details looking for status OK (9 retries left).
2026-10-20T18:38:24.4633728Z FAILED - RETRYING: Check Deployment details looking for status OK (8 retries left).
2026-10-20T18:38:29.8364803Z FAILED - RETRYING: Check Deployment details looking for status OK (7 retries left).
2026-10-20T18:38:35.1998633Z FAILED - RETRYING: Check Deployment details looking for status OK (6 retries left).
2026-10-20T18:38:40.5596981Z FAILED - RETRYING: Check Deployment details looking for status OK (5 retries left).
2026-10-20T18:38:45.9293629Z FAILED - RETRYING: Check Deployment details looking for status OK (4 retries left).
2026-10-20T18:38:51.2878903Z FAILED - RETRYING: Check Deployment details looking for status OK (3 retries left).
2026-10-20T18:38:56.6479548Z FAILED - RETRYING: Check Deployment details looking for status OK (2 retries left).
2026-10-20T18:39:02.0202715Z FAILED - RETRYING: Check Deployment details looking for status OK (1 retries left).
2026-10-20T18:39:07.3850340Z 
2026-10-20T18:39:07.3850809Z TASK [Check Deployment details looking for status OK] **************************
2026-10-20T18:39:07.3857461Z fatal: [caddeapllx955.agil.nprd.caixa.gov.br]: FAILED! => {"attempts": 60, "changed": false, "connection": "close", "content": "{\"outcome\" : \"success\", \"result\" : {\"sigsj_intranet-ear.ear\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"zDAjxGeD6I65CycLTstCisreKJ4=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1792521216723, \"enabled-timestamp\" : \"2026-10-20 15:33:36,723 BRT\", \"managed\" : true, \"name\" : \"sigsj_intranet-ear.ear\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"sigsj_intranet-ear.ear\", \"status\" : \"FAILED\", \"subdeployment\" : {\"sigsj_intranet.war\" : null}, \"subsystem\" : {\"logging\" : null}}}}", "content_encoding": "identity", "content_length": "598", "content_type": "application/json; charset=utf-8", "cookies": {}, "cookies_string": "", "date": "Tue, 20 Oct 2026 18:39:07 GMT", "elapsed": 0, "json": {"outcome": "success", "result": {"sigsj_intranet-ear.ear": {"content": [{"hash": {"BYTES_VALUE": "zDAjxGeD6I65CycLTstCisreKJ4="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1792521216723, "enabled-timestamp": "2026-10-20 15:33:36,723 BRT", "managed": true, "name": "sigsj_intranet-ear.ear", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "sigsj_intranet-ear.ear", "status": "FAILED", "subdeployment": {"sigsj_intranet.war": null}, "subsystem": {"logging": null}}}}, "msg": "OK (598 bytes)", "redirected": false, "status": 200, "url": "http://10.116.194.179:9990/management/", "x_content_type_options": "nosniff", "x_frame_options": "SAMEORIGIN"}
2026-10-20T18:39:07.3870302Z 
2026-10-20T18:39:07.3870859Z PLAY RECAP *********************************************************************
2026-10-20T18:39:07.3871087Z caddeapllx955.agil.nprd.caixa.gov.br : ok=6    changed=1    unreachable=0    failed=1    skipped=0    rescued=1    ignored=0   
2026-10-20T18:39:07.3871192Z 
2026-10-20T18:39:07.3871597Z Tuesday 20 October 2026  15:39:07 -0300 (0:05:22.456)       0:11:05.792 ******* 
2026-10-20T18:39:07.3871786Z =============================================================================== 
2026-10-20T18:39:07.3875980Z Check Deployment details looking for status OK ------------------------ 322.46s
2026-10-20T18:39:07.3876258Z Check Deployment details looking for status OK ------------------------ 322.23s
2026-10-20T18:39:07.3876792Z systemd ---------------------------------------------------------------- 12.77s
2026-10-20T18:39:07.3877021Z Check if Jboss is Running ----------------------------------------------- 6.06s
2026-10-20T18:39:07.3877311Z Check if Jboss is Running ----------------------------------------------- 0.70s
2026-10-20T18:39:07.3877559Z Verifica ser o Jboss já foi instalado ----------------------------------- 0.57s
2026-10-20T18:39:07.3877771Z Wait for Jboss Management port ------------------------------------------ 0.38s
2026-10-20T18:39:07.3880331Z Wait for Jboss Management port ------------------------------------------ 0.31s
2026-10-20T18:39:07.3880535Z Playbook run took 0 days, 0 hours, 11 minutes, 5 seconds
2026-10-20T18:39:07.4460120Z ##[error]Bash exited with code '2'.
2026-10-20T18:39:07.4494334Z ##[section]Finishing: Check Deployments [JBOSS]



