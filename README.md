2026-10-21T18:39:35.8471096Z ##[section]Starting: Check Deployments [JBOSS]
2026-10-21T18:39:35.8474211Z ==============================================================================
2026-10-21T18:39:35.8474300Z Task         : Bash
2026-10-21T18:39:35.8474339Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-21T18:39:35.8474412Z Version      : 3.227.0
2026-10-21T18:39:35.8474452Z Author       : Microsoft Corporation
2026-10-21T18:39:35.8474499Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-21T18:39:35.8474569Z ==============================================================================
2026-10-21T18:39:35.9786027Z Generating script.
2026-10-21T18:39:35.9796271Z Script contents:
2026-10-21T18:39:35.9796837Z ansible-playbook /opt/ads-agent/_work/r19318/a/esteira-jboss-vm-v2/site.yml --tags check_deployments -e sistema_ambiente=des -e sistema_nome=sigsj-boleto -e site=ctc_nprd
2026-10-21T18:39:35.9800155Z ========================== Starting Command Output ===========================
2026-10-21T18:39:35.9810632Z [command]/bin/bash /opt/ads-agent/_work/_temp/66d120d4-1427-4cb4-8aa7-86a7b80f4582.sh
2026-10-21T18:39:38.2492468Z 
2026-10-21T18:39:38.2493381Z PLAY [local] *******************************************************************
2026-10-21T18:39:38.2809332Z 
2026-10-21T18:39:38.2809799Z PLAY [Configurando o DNS] ******************************************************
2026-10-21T18:39:38.4890311Z 
2026-10-21T18:39:38.4890767Z PLAY [local] *******************************************************************
2026-10-21T18:39:38.4927664Z 
2026-10-21T18:39:38.4928192Z PLAY [Verificando serviços] ****************************************************
2026-10-21T18:39:38.5021549Z 
2026-10-21T18:39:38.5022533Z PLAY [Configuração LDAP] *******************************************************
2026-10-21T18:39:38.5058105Z [WARNING]: Found variable using reserved name: when
2026-10-21T18:39:38.5062201Z 
2026-10-21T18:39:38.5062365Z PLAY [jboss] *******************************************************************
2026-10-21T18:39:38.5155746Z 
2026-10-21T18:39:38.5156077Z PLAY [Stack Jboss] *************************************************************
2026-10-21T18:39:38.5412172Z Wednesday 21 October 2026  15:39:38 -0300 (0:00:00.353)       0:00:00.353 ***** 
2026-10-21T18:39:39.0851091Z 
2026-10-21T18:39:39.0851797Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-10-21T18:39:39.0853518Z [DEPRECATION WARNING]: Distribution rhel 9.3 on host 
2026-10-21T18:39:39.0853989Z caddeapllx2557.agil.nprd.caixa.gov.br should use /usr/libexec/platform-python, 
2026-10-21T18:39:39.0854250Z but is using /usr/bin/python for backward compatibility with prior Ansible 
2026-10-21T18:39:39.0854411Z releases. A future Ansible release will default to using the discovered 
2026-10-21T18:39:39.0854567Z platform python for this host. See https://docs.ansible.com/ansible/2.9/referen
2026-10-21T18:39:39.0854721Z ce_appendices/interpreter_discovery.html for more information. This feature 
2026-10-21T18:39:39.0854940Z will be removed in version 2.12. Deprecation warnings can be disabled by 
2026-10-21T18:39:39.0855095Z setting deprecation_warnings=False in ansible.cfg.
2026-10-21T18:39:39.0856068Z ok: [caddeapllx2557.agil.nprd.caixa.gov.br]
2026-10-21T18:39:39.0880549Z 
2026-10-21T18:39:39.0880805Z PLAY [jboss] *******************************************************************
2026-10-21T18:39:39.0924836Z 
2026-10-21T18:39:39.0925584Z PLAY [jboss] *******************************************************************
2026-10-21T18:39:39.0964035Z 
2026-10-21T18:39:39.0964334Z PLAY [jboss] *******************************************************************
2026-10-21T18:39:39.0988630Z 
2026-10-21T18:39:39.0989067Z PLAY [Copiando deployments adicionais] *****************************************
2026-10-21T18:39:39.1017067Z 
2026-10-21T18:39:39.1017281Z PLAY [Copiando modules adicionais] *********************************************
2026-10-21T18:39:39.1042741Z 
2026-10-21T18:39:39.1042926Z PLAY [jboss] *******************************************************************
2026-10-21T18:39:39.1082859Z 
2026-10-21T18:39:39.1083086Z PLAY [jboss] *******************************************************************
2026-10-21T18:39:39.1112972Z 
2026-10-21T18:39:39.1113384Z PLAY [jboss] *******************************************************************
2026-10-21T18:39:39.1162195Z Wednesday 21 October 2026  15:39:39 -0300 (0:00:00.575)       0:00:00.929 ***** 
2026-10-21T18:39:39.4890080Z 
2026-10-21T18:39:39.4890853Z TASK [Wait for Jboss Management port] ******************************************
2026-10-21T18:39:39.4891099Z ok: [caddeapllx2557.agil.nprd.caixa.gov.br]
2026-10-21T18:39:39.4927389Z Wednesday 21 October 2026  15:39:39 -0300 (0:00:00.376)       0:00:01.305 ***** 
2026-10-21T18:39:40.1504126Z 
2026-10-21T18:39:40.1504728Z TASK [Check if Jboss is Running] ***********************************************
2026-10-21T18:39:40.1505433Z ok: [caddeapllx2557.agil.nprd.caixa.gov.br]
2026-10-21T18:39:40.1539500Z Wednesday 21 October 2026  15:39:40 -0300 (0:00:00.661)       0:00:01.966 ***** 
2026-10-21T18:39:40.5940933Z FAILED - RETRYING: Check Deployment details looking for status OK (60 retries left).
2026-10-21T18:39:45.9750136Z FAILED - RETRYING: Check Deployment details looking for status OK (59 retries left).
2026-10-21T18:39:51.3427321Z FAILED - RETRYING: Check Deployment details looking for status OK (58 retries left).
2026-10-21T18:39:56.7114872Z FAILED - RETRYING: Check Deployment details looking for status OK (57 retries left).
2026-10-21T18:40:02.0979099Z FAILED - RETRYING: Check Deployment details looking for status OK (56 retries left).
2026-10-21T18:40:07.4686441Z FAILED - RETRYING: Check Deployment details looking for status OK (55 retries left).
2026-10-21T18:40:12.8346211Z FAILED - RETRYING: Check Deployment details looking for status OK (54 retries left).
2026-10-21T18:40:18.2087392Z FAILED - RETRYING: Check Deployment details looking for status OK (53 retries left).
2026-10-21T18:40:23.5764816Z FAILED - RETRYING: Check Deployment details looking for status OK (52 retries left).
2026-10-21T18:40:28.9417794Z FAILED - RETRYING: Check Deployment details looking for status OK (51 retries left).
2026-10-21T18:40:34.3238855Z FAILED - RETRYING: Check Deployment details looking for status OK (50 retries left).
2026-10-21T18:40:39.6868332Z FAILED - RETRYING: Check Deployment details looking for status OK (49 retries left).
2026-10-21T18:40:45.0720440Z FAILED - RETRYING: Check Deployment details looking for status OK (48 retries left).
2026-10-21T18:40:50.4541948Z FAILED - RETRYING: Check Deployment details looking for status OK (47 retries left).
2026-10-21T18:40:55.8250577Z FAILED - RETRYING: Check Deployment details looking for status OK (46 retries left).
2026-10-21T18:41:01.1931336Z FAILED - RETRYING: Check Deployment details looking for status OK (45 retries left).
2026-10-21T18:41:06.5734007Z FAILED - RETRYING: Check Deployment details looking for status OK (44 retries left).
2026-10-21T18:41:11.9426319Z FAILED - RETRYING: Check Deployment details looking for status OK (43 retries left).
2026-10-21T18:41:17.3105081Z FAILED - RETRYING: Check Deployment details looking for status OK (42 retries left).
2026-10-21T18:41:22.6851006Z FAILED - RETRYING: Check Deployment details looking for status OK (41 retries left).
2026-10-21T18:41:28.0533502Z FAILED - RETRYING: Check Deployment details looking for status OK (40 retries left).
2026-10-21T18:41:33.4292236Z FAILED - RETRYING: Check Deployment details looking for status OK (39 retries left).
2026-10-21T18:41:38.8062935Z FAILED - RETRYING: Check Deployment details looking for status OK (38 retries left).
2026-10-21T18:41:44.1772227Z FAILED - RETRYING: Check Deployment details looking for status OK (37 retries left).
2026-10-21T18:41:49.5453627Z FAILED - RETRYING: Check Deployment details looking for status OK (36 retries left).
2026-10-21T18:41:54.9252367Z FAILED - RETRYING: Check Deployment details looking for status OK (35 retries left).
2026-10-21T18:42:00.2947068Z FAILED - RETRYING: Check Deployment details looking for status OK (34 retries left).
2026-10-21T18:42:05.6616516Z FAILED - RETRYING: Check Deployment details looking for status OK (33 retries left).
2026-10-21T18:42:11.0455066Z FAILED - RETRYING: Check Deployment details looking for status OK (32 retries left).
2026-10-21T18:42:16.4944154Z FAILED - RETRYING: Check Deployment details looking for status OK (31 retries left).
2026-10-21T18:42:21.8605374Z FAILED - RETRYING: Check Deployment details looking for status OK (30 retries left).
2026-10-21T18:42:27.2396647Z FAILED - RETRYING: Check Deployment details looking for status OK (29 retries left).
2026-10-21T18:42:32.6110842Z FAILED - RETRYING: Check Deployment details looking for status OK (28 retries left).
2026-10-21T18:42:37.9761985Z FAILED - RETRYING: Check Deployment details looking for status OK (27 retries left).
2026-10-21T18:42:43.3507381Z FAILED - RETRYING: Check Deployment details looking for status OK (26 retries left).
2026-10-21T18:42:48.7098145Z FAILED - RETRYING: Check Deployment details looking for status OK (25 retries left).
2026-10-21T18:42:54.0751287Z FAILED - RETRYING: Check Deployment details looking for status OK (24 retries left).
2026-10-21T18:42:59.4619873Z FAILED - RETRYING: Check Deployment details looking for status OK (23 retries left).
2026-10-21T18:43:04.8278498Z FAILED - RETRYING: Check Deployment details looking for status OK (22 retries left).
2026-10-21T18:43:10.1966070Z FAILED - RETRYING: Check Deployment details looking for status OK (21 retries left).
2026-10-21T18:43:15.5757020Z FAILED - RETRYING: Check Deployment details looking for status OK (20 retries left).
2026-10-21T18:43:20.9427879Z FAILED - RETRYING: Check Deployment details looking for status OK (19 retries left).
2026-10-21T18:43:26.3091036Z FAILED - RETRYING: Check Deployment details looking for status OK (18 retries left).
2026-10-21T18:43:31.6760226Z FAILED - RETRYING: Check Deployment details looking for status OK (17 retries left).
2026-10-21T18:43:37.0396955Z FAILED - RETRYING: Check Deployment details looking for status OK (16 retries left).
2026-10-21T18:43:42.4149699Z FAILED - RETRYING: Check Deployment details looking for status OK (15 retries left).
2026-10-21T18:43:47.8041044Z FAILED - RETRYING: Check Deployment details looking for status OK (14 retries left).
2026-10-21T18:43:53.1702329Z FAILED - RETRYING: Check Deployment details looking for status OK (13 retries left).
2026-10-21T18:43:58.5337885Z FAILED - RETRYING: Check Deployment details looking for status OK (12 retries left).
2026-10-21T18:44:03.9094422Z FAILED - RETRYING: Check Deployment details looking for status OK (11 retries left).
2026-10-21T18:44:09.2790158Z FAILED - RETRYING: Check Deployment details looking for status OK (10 retries left).
2026-10-21T18:44:14.6436579Z FAILED - RETRYING: Check Deployment details looking for status OK (9 retries left).
2026-10-21T18:44:20.0175141Z FAILED - RETRYING: Check Deployment details looking for status OK (8 retries left).
2026-10-21T18:44:25.3904930Z FAILED - RETRYING: Check Deployment details looking for status OK (7 retries left).
2026-10-21T18:44:30.7624609Z FAILED - RETRYING: Check Deployment details looking for status OK (6 retries left).
2026-10-21T18:44:36.1508850Z FAILED - RETRYING: Check Deployment details looking for status OK (5 retries left).
2026-10-21T18:44:41.5206343Z FAILED - RETRYING: Check Deployment details looking for status OK (4 retries left).
2026-10-21T18:44:46.8884489Z FAILED - RETRYING: Check Deployment details looking for status OK (3 retries left).
2026-10-21T18:44:52.2826307Z FAILED - RETRYING: Check Deployment details looking for status OK (2 retries left).
2026-10-21T18:44:57.6560004Z FAILED - RETRYING: Check Deployment details looking for status OK (1 retries left).
2026-10-21T18:45:03.0249789Z 
2026-10-21T18:45:03.0250739Z TASK [Check Deployment details looking for status OK] **************************
2026-10-21T18:45:03.0258355Z fatal: [caddeapllx2557.agil.nprd.caixa.gov.br]: FAILED! => {"attempts": 60, "changed": false, "connection": "close", "content": "{\"outcome\" : \"success\", \"result\" : {\"boletoService-ear.ear\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"X38w/tfh1zWKGxN4weA3puw/djQ=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1792607963299, \"enabled-timestamp\" : \"2026-10-21 15:39:23,299 BRT\", \"managed\" : true, \"name\" : \"boletoService-ear.ear\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"boletoService-ear.ear\", \"status\" : \"FAILED\", \"subdeployment\" : {\"boletoService-war-2.0.2.8.war\" : null}, \"subsystem\" : null}, \"sirotcon-ejb.jar\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"cLE7JH7Axwql5UcepAdPvwrhtws=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1792607963312, \"enabled-timestamp\" : \"2026-10-21 15:39:23,312 BRT\", \"managed\" : true, \"name\" : \"sirotcon-ejb.jar\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"sirotcon-ejb.jar\", \"status\" : \"OK\", \"subdeployment\" : null, \"subsystem\" : {\"ejb3\" : null, \"logging\" : null}}}}", "content_encoding": "identity", "content_length": "1122", "content_type": "application/json; charset=utf-8", "cookies": {}, "cookies_string": "", "date": "Wed, 21 Oct 2026 18:45:02 GMT", "elapsed": 0, "json": {"outcome": "success", "result": {"boletoService-ear.ear": {"content": [{"hash": {"BYTES_VALUE": "X38w/tfh1zWKGxN4weA3puw/djQ="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1792607963299, "enabled-timestamp": "2026-10-21 15:39:23,299 BRT", "managed": true, "name": "boletoService-ear.ear", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "boletoService-ear.ear", "status": "FAILED", "subdeployment": {"boletoService-war-2.0.2.8.war": null}, "subsystem": null}, "sirotcon-ejb.jar": {"content": [{"hash": {"BYTES_VALUE": "cLE7JH7Axwql5UcepAdPvwrhtws="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1792607963312, "enabled-timestamp": "2026-10-21 15:39:23,312 BRT", "managed": true, "name": "sirotcon-ejb.jar", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "sirotcon-ejb.jar", "status": "OK", "subdeployment": null, "subsystem": {"ejb3": null, "logging": null}}}}, "msg": "OK (1122 bytes)", "redirected": false, "status": 200, "url": "http://10.116.201.25:9990/management/", "x_content_type_options": "nosniff", "x_frame_options": "SAMEORIGIN"}
2026-10-21T18:45:03.0297029Z Wednesday 21 October 2026  15:45:03 -0300 (0:05:22.875)       0:05:24.842 ***** 
2026-10-21T18:45:15.9033291Z 
2026-10-21T18:45:15.9033873Z TASK [systemd] *****************************************************************
2026-10-21T18:45:15.9034052Z changed: [caddeapllx2557.agil.nprd.caixa.gov.br]
2026-10-21T18:45:15.9081149Z Wednesday 21 October 2026  15:45:15 -0300 (0:00:12.878)       0:05:37.720 ***** 
2026-10-21T18:45:16.2366731Z 
2026-10-21T18:45:16.2367198Z TASK [Wait for Jboss Management port] ******************************************
2026-10-21T18:45:16.2367403Z ok: [caddeapllx2557.agil.nprd.caixa.gov.br]
2026-10-21T18:45:16.2404215Z Wednesday 21 October 2026  15:45:16 -0300 (0:00:00.332)       0:05:38.053 ***** 
2026-10-21T18:45:16.9916356Z FAILED - RETRYING: Check if Jboss is Running (120 retries left).
2026-10-21T18:45:22.3776673Z 
2026-10-21T18:45:22.3777125Z TASK [Check if Jboss is Running] ***********************************************
2026-10-21T18:45:22.3779163Z ok: [caddeapllx2557.agil.nprd.caixa.gov.br]
2026-10-21T18:45:22.3824837Z Wednesday 21 October 2026  15:45:22 -0300 (0:00:06.142)       0:05:44.195 ***** 
2026-10-21T18:45:22.8315032Z FAILED - RETRYING: Check Deployment details looking for status OK (60 retries left).
2026-10-21T18:45:28.2020340Z FAILED - RETRYING: Check Deployment details looking for status OK (59 retries left).
2026-10-21T18:45:33.5753281Z FAILED - RETRYING: Check Deployment details looking for status OK (58 retries left).
2026-10-21T18:45:38.9447900Z FAILED - RETRYING: Check Deployment details looking for status OK (57 retries left).
2026-10-21T18:45:44.3155848Z FAILED - RETRYING: Check Deployment details looking for status OK (56 retries left).
2026-10-21T18:45:49.6968504Z FAILED - RETRYING: Check Deployment details looking for status OK (55 retries left).
2026-10-21T18:45:55.0751871Z FAILED - RETRYING: Check Deployment details looking for status OK (54 retries left).
2026-10-21T18:46:00.4468438Z FAILED - RETRYING: Check Deployment details looking for status OK (53 retries left).
2026-10-21T18:46:05.8383034Z FAILED - RETRYING: Check Deployment details looking for status OK (52 retries left).
2026-10-21T18:46:11.2061310Z FAILED - RETRYING: Check Deployment details looking for status OK (51 retries left).
2026-10-21T18:46:16.5734783Z FAILED - RETRYING: Check Deployment details looking for status OK (50 retries left).
2026-10-21T18:46:21.9533542Z FAILED - RETRYING: Check Deployment details looking for status OK (49 retries left).
2026-10-21T18:46:27.3238794Z FAILED - RETRYING: Check Deployment details looking for status OK (48 retries left).
2026-10-21T18:46:32.6917414Z FAILED - RETRYING: Check Deployment details looking for status OK (47 retries left).
2026-10-21T18:46:38.0675472Z FAILED - RETRYING: Check Deployment details looking for status OK (46 retries left).
2026-10-21T18:46:43.4444330Z FAILED - RETRYING: Check Deployment details looking for status OK (45 retries left).
2026-10-21T18:46:48.8177723Z FAILED - RETRYING: Check Deployment details looking for status OK (44 retries left).
2026-10-21T18:46:54.2049765Z FAILED - RETRYING: Check Deployment details looking for status OK (43 retries left).
2026-10-21T18:46:59.5698692Z FAILED - RETRYING: Check Deployment details looking for status OK (42 retries left).
2026-10-21T18:47:04.9365027Z FAILED - RETRYING: Check Deployment details looking for status OK (41 retries left).
2026-10-21T18:47:10.3210379Z FAILED - RETRYING: Check Deployment details looking for status OK (40 retries left).
2026-10-21T18:47:15.6924576Z FAILED - RETRYING: Check Deployment details looking for status OK (39 retries left).
2026-10-21T18:47:21.0575756Z FAILED - RETRYING: Check Deployment details looking for status OK (38 retries left).
2026-10-21T18:47:26.4534030Z FAILED - RETRYING: Check Deployment details looking for status OK (37 retries left).
2026-10-21T18:47:31.8178199Z FAILED - RETRYING: Check Deployment details looking for status OK (36 retries left).
2026-10-21T18:47:37.1899798Z FAILED - RETRYING: Check Deployment details looking for status OK (35 retries left).
2026-10-21T18:47:42.5704956Z FAILED - RETRYING: Check Deployment details looking for status OK (34 retries left).
2026-10-21T18:47:47.9401888Z FAILED - RETRYING: Check Deployment details looking for status OK (33 retries left).
2026-10-21T18:47:53.3120210Z FAILED - RETRYING: Check Deployment details looking for status OK (32 retries left).
2026-10-21T18:47:58.6912644Z FAILED - RETRYING: Check Deployment details looking for status OK (31 retries left).
2026-10-21T18:48:04.0633189Z FAILED - RETRYING: Check Deployment details looking for status OK (30 retries left).
2026-10-21T18:48:09.4383364Z FAILED - RETRYING: Check Deployment details looking for status OK (29 retries left).
2026-10-21T18:48:14.8248375Z FAILED - RETRYING: Check Deployment details looking for status OK (28 retries left).
2026-10-21T18:48:20.1888581Z FAILED - RETRYING: Check Deployment details looking for status OK (27 retries left).
2026-10-21T18:48:25.5631781Z FAILED - RETRYING: Check Deployment details looking for status OK (26 retries left).
2026-10-21T18:48:30.9441728Z FAILED - RETRYING: Check Deployment details looking for status OK (25 retries left).
2026-10-21T18:48:36.3167123Z FAILED - RETRYING: Check Deployment details looking for status OK (24 retries left).
2026-10-21T18:48:41.6860919Z FAILED - RETRYING: Check Deployment details looking for status OK (23 retries left).
2026-10-21T18:48:47.0724785Z FAILED - RETRYING: Check Deployment details looking for status OK (22 retries left).
2026-10-21T18:48:52.4469269Z FAILED - RETRYING: Check Deployment details looking for status OK (21 retries left).
2026-10-21T18:48:57.8175109Z FAILED - RETRYING: Check Deployment details looking for status OK (20 retries left).
2026-10-21T18:49:03.2028229Z FAILED - RETRYING: Check Deployment details looking for status OK (19 retries left).
2026-10-21T18:49:08.5745081Z FAILED - RETRYING: Check Deployment details looking for status OK (18 retries left).
2026-10-21T18:49:13.9468662Z FAILED - RETRYING: Check Deployment details looking for status OK (17 retries left).
2026-10-21T18:49:19.3250630Z FAILED - RETRYING: Check Deployment details looking for status OK (16 retries left).
2026-10-21T18:49:24.7021214Z FAILED - RETRYING: Check Deployment details looking for status OK (15 retries left).
2026-10-21T18:49:30.0718732Z FAILED - RETRYING: Check Deployment details looking for status OK (14 retries left).
2026-10-21T18:49:35.4501310Z FAILED - RETRYING: Check Deployment details looking for status OK (13 retries left).
2026-10-21T18:49:40.8222978Z FAILED - RETRYING: Check Deployment details looking for status OK (12 retries left).
2026-10-21T18:49:46.1982005Z FAILED - RETRYING: Check Deployment details looking for status OK (11 retries left).
2026-10-21T18:49:51.5819249Z FAILED - RETRYING: Check Deployment details looking for status OK (10 retries left).
2026-10-21T18:49:56.9544951Z FAILED - RETRYING: Check Deployment details looking for status OK (9 retries left).
2026-10-21T18:50:02.3273587Z FAILED - RETRYING: Check Deployment details looking for status OK (8 retries left).
2026-10-21T18:50:07.7087800Z FAILED - RETRYING: Check Deployment details looking for status OK (7 retries left).
2026-10-21T18:50:13.0821965Z FAILED - RETRYING: Check Deployment details looking for status OK (6 retries left).
2026-10-21T18:50:18.4529272Z FAILED - RETRYING: Check Deployment details looking for status OK (5 retries left).
2026-10-21T18:50:23.8370877Z FAILED - RETRYING: Check Deployment details looking for status OK (4 retries left).
2026-10-21T18:50:29.2115417Z FAILED - RETRYING: Check Deployment details looking for status OK (3 retries left).
2026-10-21T18:50:34.5788605Z FAILED - RETRYING: Check Deployment details looking for status OK (2 retries left).
2026-10-21T18:50:39.9649639Z FAILED - RETRYING: Check Deployment details looking for status OK (1 retries left).
2026-10-21T18:50:45.3510486Z 
2026-10-21T18:50:45.3511172Z TASK [Check Deployment details looking for status OK] **************************
2026-10-21T18:50:45.3523425Z fatal: [caddeapllx2557.agil.nprd.caixa.gov.br]: FAILED! => {"attempts": 60, "changed": false, "connection": "close", "content": "{\"outcome\" : \"success\", \"result\" : {\"boletoService-ear.ear\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"X38w/tfh1zWKGxN4weA3puw/djQ=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1792608313728, \"enabled-timestamp\" : \"2026-10-21 15:45:13,728 BRT\", \"managed\" : true, \"name\" : \"boletoService-ear.ear\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"boletoService-ear.ear\", \"status\" : \"FAILED\", \"subdeployment\" : {\"boletoService-war-2.0.2.8.war\" : null}, \"subsystem\" : null}, \"sirotcon-ejb.jar\" : {\"content\" : [{\"hash\" : { \"BYTES_VALUE\" : \"cLE7JH7Axwql5UcepAdPvwrhtws=\" }}], \"disabled-time\" : null, \"disabled-timestamp\" : null, \"enabled\" : true, \"enabled-time\" : 1792608313743, \"enabled-timestamp\" : \"2026-10-21 15:45:13,743 BRT\", \"managed\" : true, \"name\" : \"sirotcon-ejb.jar\", \"owner\" : [{ \"subsystem\" : \"deployment-scanner\" },{ \"scanner\" : \"default\" }], \"persistent\" : false, \"runtime-name\" : \"sirotcon-ejb.jar\", \"status\" : \"OK\", \"subdeployment\" : null, \"subsystem\" : {\"ejb3\" : null, \"logging\" : null}}}}", "content_encoding": "identity", "content_length": "1122", "content_type": "application/json; charset=utf-8", "cookies": {}, "cookies_string": "", "date": "Wed, 21 Oct 2026 18:50:45 GMT", "elapsed": 0, "json": {"outcome": "success", "result": {"boletoService-ear.ear": {"content": [{"hash": {"BYTES_VALUE": "X38w/tfh1zWKGxN4weA3puw/djQ="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1792608313728, "enabled-timestamp": "2026-10-21 15:45:13,728 BRT", "managed": true, "name": "boletoService-ear.ear", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "boletoService-ear.ear", "status": "FAILED", "subdeployment": {"boletoService-war-2.0.2.8.war": null}, "subsystem": null}, "sirotcon-ejb.jar": {"content": [{"hash": {"BYTES_VALUE": "cLE7JH7Axwql5UcepAdPvwrhtws="}}], "disabled-time": null, "disabled-timestamp": null, "enabled": true, "enabled-time": 1792608313743, "enabled-timestamp": "2026-10-21 15:45:13,743 BRT", "managed": true, "name": "sirotcon-ejb.jar", "owner": [{"subsystem": "deployment-scanner"}, {"scanner": "default"}], "persistent": false, "runtime-name": "sirotcon-ejb.jar", "status": "OK", "subdeployment": null, "subsystem": {"ejb3": null, "logging": null}}}}, "msg": "OK (1122 bytes)", "redirected": false, "status": 200, "url": "http://10.116.201.25:9990/management/", "x_content_type_options": "nosniff", "x_frame_options": "SAMEORIGIN"}
2026-10-21T18:50:45.3542702Z 
2026-10-21T18:50:45.3543495Z PLAY RECAP *********************************************************************
2026-10-21T18:50:45.3543754Z caddeapllx2557.agil.nprd.caixa.gov.br : ok=6    changed=1    unreachable=0    failed=1    skipped=0    rescued=1    ignored=0   
2026-10-21T18:50:45.3543873Z 
2026-10-21T18:50:45.3547580Z Wednesday 21 October 2026  15:50:45 -0300 (0:05:22.972)       0:11:07.167 ***** 
2026-10-21T18:50:45.3547815Z =============================================================================== 
2026-10-21T18:50:45.3552019Z Check Deployment details looking for status OK ------------------------ 322.97s
2026-10-21T18:50:45.3552253Z Check Deployment details looking for status OK ------------------------ 322.88s
2026-10-21T18:50:45.3552468Z systemd ---------------------------------------------------------------- 12.88s
2026-10-21T18:50:45.3552695Z Check if Jboss is Running ----------------------------------------------- 6.14s
2026-10-21T18:50:45.3553209Z Check if Jboss is Running ----------------------------------------------- 0.66s
2026-10-21T18:50:45.3553666Z Verifica ser o Jboss já foi instalado ----------------------------------- 0.58s
2026-10-21T18:50:45.3553900Z Wait for Jboss Management port ------------------------------------------ 0.38s
2026-10-21T18:50:45.3555686Z Wait for Jboss Management port ------------------------------------------ 0.33s
2026-10-21T18:50:45.3555903Z Playbook run took 0 days, 0 hours, 11 minutes, 7 seconds
2026-10-21T18:50:45.4312386Z ##[error]Bash exited with code '2'.
2026-10-21T18:50:45.4355483Z ##[section]Finishing: Check Deployments [JBOSS]




vamos la esse é do boleto

Skip to main content
Azure DevOps
projetos
/
Caixa
/
Pipelines
/
Releases
/
SIGSJ-boleto
Search


Caixa

Overview

Boards

Repos

Pipelines
Pipelines
Environments
Releases
Library
Task groups
Deployment groups
Portal Infra

Test Plans

Artifacts
Project settings
All pipelines

SIGSJ

SIGSJ-boleto
Predefined variables
Usuario-Azure-DevOps (12)
Scopes: Release
OKD-PRODUTOS (8)
Credenciais para o Cluster OKD4 de PRODUTOS
Scopes: Release
SonarQube Variables (1)
Variáveis com dados do SonarQube
Scopes: Release
MONITORACAO_LOGS (4)
REQ000143540550 - Conforme autorizado na req por FLAVIO ALMEIDA GAGLIARDI, removido as variáveis JAVA_OPTS_MONITORING e URL_APM_SERVER, por entrar em conflitos com releases que utilizam o Application Insights
Scopes: Release
TERRAFORM-ESTEIRA-COMMON (6)
WO0000079295714 - add variável INFRAFACIL
Scopes: Release
ANSIBLE_JBOSS_VM_VERSION_3 (11)
WO0000072264656 - Config Portal Infrafácil NO_PROXY cadsvgerap027-1.intra.caixa.gov.br, 10.122.144.168
Scopes: Release
TERRAFORM-ESTEIRA-NPRD (17)
Variáveis do terraform para automação de ambientes
Scopes: EC DES,EC TQS,EC HMP
SIGSJ-BOLETO-DES (10)
Grupo de variáveis de SIGSJ-BOLETO-DES

Scopes: EC DES
CGC_UNIDADE_DES
7390
CGC_UNIDADE_OPS
7259
JVM_HEAP_MAX
2048m
JVM_HEAP_MIN
1024m
JVM_METASPACE_MAX
512m
JVM_METASPACE_MIN
256m
PASSWORD_TRUSTSTORE
changeit
URL_APM_SERVER
http://localhost:8200
http_context_default
boletoService
sistema_nome
sigsj-boleto
SIGSJ-BOLETO-TQS (1)
Grupo de variáveis de SIGSJ-BOLETO-TQS
Scopes: EC TQS
SIGSJ-BOLETO-HMP (1)
Grupo de variáveis de SIGSJ-BOLETO-HMP
Scopes: EC HMP
TERRAFORM-ESTEIRA-PRD-CTC-NPCN (17)
Variáveis do terraform para automação de ambientes TERRAFORM_VSPHERE_POOL - RP_ESTEIRAS_AGEIS_NPCN_CTC_V7 13/03/2025
Scopes: EC PRD CTC
SIGSJ-BOLETO-PRD (1)
Grupo de variáveis de SIGSJ-BOLETO-PRD
Scopes: EC PRD CTC,EC PRD DTC
TERRAFORM-ESTEIRA-PRD-DTC-PCN (15)
Variáveis do terraform para automação de ambientes
Scopes: EC PRD DTC
|Manage variable groups
Select a release pipeline to view its releases

60 pipelines found

Select a release pipeline to view its releases

60 pipelines found

Select a release pipeline to view its releases

1 pipelines found

Row 2

Row 2

Showing filters 1 through 2

Row 2

Showing filters 1 through 2

Showing filters 1 through 2

Showing filters 1 through 2

