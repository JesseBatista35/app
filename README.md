Agora, já logado na VM 765
bash
ip -4 a | grep -E '10.116.(180.23|193.253)'
ss -ltnp 2>/dev/null | grep -E ':(80|443|8080|8443) '
systemctl is-active httpd 2>/dev/null
grep -RniE '^\s*(Timeout|ProxyTimeout)\b|timeout=' /etc/httpd/conf /etc/httpd/conf.d 2>/dev/null
Se o 10.116.180.23 não aparecer na VM, é VIP mesmo.
Se o httpd estiver ativo aqui, o último grep já mostra o timeout dele.
Se o Apache não estiver na 765

No Azure DevOps, abra o log da task "Configurando o Apache" dessa mesma release (SIGEC-CSC-1012, EC TQS). Na linha ok:/changed: do PLAY [apache_tqs] aparece o host do Apache. Entre nele e rode:

bash
grep -RniE '^\s*(Timeout|ProxyTimeout)\b|timeout=' /etc/httpd/conf /etc/httpd/conf.d 2>/dev/null
grep -Rln 'sigec-csc' /etc/httpd/conf.d 2>/dev/null

Me manda as saídas. Se aparecer Timeout 120 ou ProxyTimeout 120, achamos a causa.

Como o Claude está se saindo nesta sessão?







2026-11-19T16:43:55.5516112Z ##[section]Starting: Configurando o Apache
2026-11-19T16:43:55.5519338Z ==============================================================================
2026-11-19T16:43:55.5519421Z Task         : Bash
2026-11-19T16:43:55.5519463Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-11-19T16:43:55.5519523Z Version      : 3.227.0
2026-11-19T16:43:55.5519573Z Author       : Microsoft Corporation
2026-11-19T16:43:55.5519629Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-11-19T16:43:55.5519695Z ==============================================================================
2026-11-19T16:43:55.6649710Z Generating script.
2026-11-19T16:43:55.6658356Z Script contents:
2026-11-19T16:43:55.6658895Z ansible-playbook /opt/ads-agent/esteira-jboss-vm/site.yml --tags apache -e sistema_ambiente=tqs -e http_sso=no  -e sistema_nome=sigec-csc -e quantidade_vm=1 -e http_context_default=csc-api -e '{"http_context_additional":[]}' -e site=$(site)
2026-11-19T16:43:55.6661272Z ========================== Starting Command Output ===========================
2026-11-19T16:43:55.6668424Z [command]/bin/bash /opt/ads-agent/_work/_temp/0341a9ba-9468-43e7-8600-3b442631afbd.sh
2026-11-19T16:43:55.6728841Z /opt/ads-agent/_work/_temp/0341a9ba-9468-43e7-8600-3b442631afbd.sh: line 1: site: comando não encontrado
2026-11-19T16:43:57.7789925Z 
2026-11-19T16:43:57.7790518Z PLAY [local] *******************************************************************
2026-11-19T16:43:57.8333613Z 
2026-11-19T16:43:57.8334052Z PLAY [Configurando o DNS] ******************************************************
2026-11-19T16:43:58.0644364Z 
2026-11-19T16:43:58.0644910Z PLAY [local] *******************************************************************
2026-11-19T16:43:58.0670266Z 
2026-11-19T16:43:58.0670594Z PLAY [local] *******************************************************************
2026-11-19T16:43:58.0701452Z 
2026-11-19T16:43:58.0701965Z PLAY [Verificando serviços] ****************************************************
2026-11-19T16:43:58.0790902Z 
2026-11-19T16:43:58.0791771Z PLAY [Configuração LDAP] *******************************************************
2026-11-19T16:43:58.0852661Z 
2026-11-19T16:43:58.0852987Z PLAY [apache_tqs] **************************************************************
2026-11-19T16:43:58.0904802Z Thursday 19 November 2026  13:43:58 -0300 (0:00:00.371)       0:00:00.371 ***** 
2026-11-19T16:43:58.1495286Z 
2026-11-19T16:43:58.1495856Z TASK [Sobrescrevendo groups vars] **********************************************
2026-11-19T16:43:58.1496017Z ok: [caddeapllx137.extra.caixa.gov.br]
2026-11-19T16:43:58.1520929Z ok: [caddeapllx138.extra.caixa.gov.br]
2026-11-19T16:43:58.1563529Z Thursday 19 November 2026  13:43:58 -0300 (0:00:00.066)       0:00:00.437 ***** 
2026-11-19T16:43:58.2233630Z 
2026-11-19T16:43:58.2234230Z TASK [vhost : Definindo o nome do Virtual Host] ********************************
2026-11-19T16:43:58.2234442Z ok: [caddeapllx137.extra.caixa.gov.br]
2026-11-19T16:43:58.2294388Z ok: [caddeapllx138.extra.caixa.gov.br]
2026-11-19T16:43:58.2333049Z Thursday 19 November 2026  13:43:58 -0300 (0:00:00.076)       0:00:00.514 ***** 
2026-11-19T16:44:00.2789628Z 
2026-11-19T16:44:00.2790081Z TASK [vhost : Deploy Virtual Host] *********************************************
2026-11-19T16:44:00.2790387Z changed: [caddeapllx137.extra.caixa.gov.br]
2026-11-19T16:44:00.8764145Z changed: [caddeapllx138.extra.caixa.gov.br]
2026-11-19T16:44:00.8796327Z Thursday 19 November 2026  13:44:00 -0300 (0:00:02.646)       0:00:03.161 ***** 
2026-11-19T16:44:01.4337232Z 
2026-11-19T16:44:01.4338280Z TASK [vhost : Enable Virtual Host] *********************************************
2026-11-19T16:44:01.4338729Z ok: [caddeapllx137.extra.caixa.gov.br]
2026-11-19T16:44:01.5022115Z ok: [caddeapllx138.extra.caixa.gov.br]
2026-11-19T16:44:01.5030677Z Thursday 19 November 2026  13:44:01 -0300 (0:00:00.623)       0:00:03.784 ***** 
2026-11-19T16:44:02.8188759Z 
2026-11-19T16:44:02.8189347Z RUNNING HANDLER [vhost : Reload Apache] ****************************************
2026-11-19T16:44:02.8189868Z changed: [caddeapllx137.extra.caixa.gov.br]
2026-11-19T16:44:03.5723545Z changed: [caddeapllx138.extra.caixa.gov.br]
2026-11-19T16:44:03.5752499Z 
2026-11-19T16:44:03.5753463Z PLAY [jboss] *******************************************************************
2026-11-19T16:44:03.5781083Z 
2026-11-19T16:44:03.5781291Z PLAY [Instalando stack Jboss] **************************************************
2026-11-19T16:44:03.5913936Z Thursday 19 November 2026  13:44:03 -0300 (0:00:02.088)       0:00:05.872 ***** 
2026-11-19T16:44:04.0070832Z 
2026-11-19T16:44:04.0071498Z TASK [Verificando o java versão esta instalado: 1.8.0_221] *********************
2026-11-19T16:44:04.0071792Z ok: [caddeapllx765.agil.nprd.caixa.gov.br]
2026-11-19T16:44:04.0117479Z Thursday 19 November 2026  13:44:04 -0300 (0:00:00.420)       0:00:06.293 ***** 
2026-11-19T16:44:04.5835047Z 
2026-11-19T16:44:04.5835905Z TASK [Verificando a versão do Java] ********************************************
2026-11-19T16:44:04.5836141Z changed: [caddeapllx765.agil.nprd.caixa.gov.br]
2026-11-19T16:44:04.5873927Z Thursday 19 November 2026  13:44:04 -0300 (0:00:00.575)       0:00:06.868 ***** 
2026-11-19T16:44:04.6424539Z Thursday 19 November 2026  13:44:04 -0300 (0:00:00.054)       0:00:06.923 ***** 
2026-11-19T16:44:04.9947518Z 
2026-11-19T16:44:04.9948653Z TASK [Verifica ser o Jboss já foi instalado] ***********************************
2026-11-19T16:44:04.9949013Z ok: [caddeapllx765.agil.nprd.caixa.gov.br]
2026-11-19T16:44:04.9990009Z Thursday 19 November 2026  13:44:04 -0300 (0:00:00.357)       0:00:07.280 ***** 
2026-11-19T16:44:05.0618660Z 
2026-11-19T16:44:05.0619424Z TASK [Setando a versão do Jboss] ***********************************************
2026-11-19T16:44:05.0619761Z ok: [caddeapllx765.agil.nprd.caixa.gov.br]
2026-11-19T16:44:05.0654892Z Thursday 19 November 2026  13:44:05 -0300 (0:00:00.066)       0:00:07.347 ***** 
2026-11-19T16:44:05.1097696Z Thursday 19 November 2026  13:44:05 -0300 (0:00:00.043)       0:00:07.391 ***** 
2026-11-19T16:44:05.1533913Z Thursday 19 November 2026  13:44:05 -0300 (0:00:00.043)       0:00:07.434 ***** 
2026-11-19T16:44:05.1980384Z Thursday 19 November 2026  13:44:05 -0300 (0:00:00.044)       0:00:07.479 ***** 
2026-11-19T16:44:05.2426784Z Thursday 19 November 2026  13:44:05 -0300 (0:00:00.044)       0:00:07.523 ***** 
2026-11-19T16:44:05.2880991Z Thursday 19 November 2026  13:44:05 -0300 (0:00:00.045)       0:00:07.569 ***** 
2026-11-19T16:44:05.3322641Z Thursday 19 November 2026  13:44:05 -0300 (0:00:00.044)       0:00:07.613 ***** 
2026-11-19T16:44:05.3770845Z Thursday 19 November 2026  13:44:05 -0300 (0:00:00.044)       0:00:07.658 ***** 
2026-11-19T16:44:05.4194852Z 
2026-11-19T16:44:05.4195283Z PLAY [jboss] *******************************************************************
2026-11-19T16:44:05.4221586Z 
2026-11-19T16:44:05.4221891Z PLAY [jboss] *******************************************************************
2026-11-19T16:44:05.4255628Z 
2026-11-19T16:44:05.4255945Z PLAY [jboss] *******************************************************************
2026-11-19T16:44:05.4293413Z 
2026-11-19T16:44:05.4293603Z PLAY [local] *******************************************************************
2026-11-19T16:44:05.4316489Z 
2026-11-19T16:44:05.4316779Z PLAY [jboss] *******************************************************************
2026-11-19T16:44:05.4342363Z 
2026-11-19T16:44:05.4342591Z PLAY [jboss] *******************************************************************
2026-11-19T16:44:05.4372488Z 
2026-11-19T16:44:05.4372792Z PLAY [Copiando deployments adicionais] *****************************************
2026-11-19T16:44:05.4404149Z 
2026-11-19T16:44:05.4404282Z PLAY [Copiando modules adicionais] *********************************************
2026-11-19T16:44:05.4436538Z 
2026-11-19T16:44:05.4437069Z PLAY [local] *******************************************************************
2026-11-19T16:44:05.4465839Z [WARNING]: Could not match supplied host pattern, ignoring: instance_restart
2026-11-19T16:44:05.4469898Z 
2026-11-19T16:44:05.4470169Z PLAY [instance_restart] ********************************************************
2026-11-19T16:44:05.4470364Z skipping: no hosts matched
2026-11-19T16:44:05.4471719Z [WARNING]: Could not match supplied host pattern, ignoring: machine_reboot
2026-11-19T16:44:05.4476969Z 
2026-11-19T16:44:05.4477247Z PLAY [machine_reboot] **********************************************************
2026-11-19T16:44:05.4477472Z skipping: no hosts matched
2026-11-19T16:44:05.4483992Z 
2026-11-19T16:44:05.4484169Z PLAY [local] *******************************************************************
2026-11-19T16:44:05.4507597Z [WARNING]: Could not match supplied host pattern, ignoring: instance_stop
2026-11-19T16:44:05.4509934Z 
2026-11-19T16:44:05.4510111Z PLAY [instance_stop] ***********************************************************
2026-11-19T16:44:05.4510285Z skipping: no hosts matched
2026-11-19T16:44:05.4513672Z 
2026-11-19T16:44:05.4513842Z PLAY [machine_reboot] **********************************************************
2026-11-19T16:44:05.4513982Z skipping: no hosts matched
2026-11-19T16:44:05.4523246Z 
2026-11-19T16:44:05.4523735Z PLAY [Configura TSM] ***********************************************************
2026-11-19T16:44:05.4549959Z 
2026-11-19T16:44:05.4550607Z PLAY [Configura Control-M] *****************************************************
2026-11-19T16:44:05.4572142Z 
2026-11-19T16:44:05.4572373Z PLAY RECAP *********************************************************************
2026-11-19T16:44:05.4572616Z caddeapllx137.extra.caixa.gov.br : ok=5    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
2026-11-19T16:44:05.4573519Z caddeapllx138.extra.caixa.gov.br : ok=5    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
2026-11-19T16:44:05.4573756Z caddeapllx765.agil.nprd.caixa.gov.br : ok=4    changed=1    unreachable=0    failed=0    skipped=9    rescued=0    ignored=0   
2026-11-19T16:44:05.4573851Z 
2026-11-19T16:44:05.4574829Z Thursday 19 November 2026  13:44:05 -0300 (0:00:00.080)       0:00:07.739 ***** 
2026-11-19T16:44:05.4575049Z =============================================================================== 
2026-11-19T16:44:05.4577900Z vhost : Deploy Virtual Host --------------------------------------------- 2.65s
2026-11-19T16:44:05.4578544Z vhost : Reload Apache --------------------------------------------------- 2.09s
2026-11-19T16:44:05.4579110Z vhost : Enable Virtual Host --------------------------------------------- 0.62s
2026-11-19T16:44:05.4579411Z Verificando a versão do Java -------------------------------------------- 0.58s
2026-11-19T16:44:05.4579680Z Verificando o java versão esta instalado: 1.8.0_221 --------------------- 0.42s
2026-11-19T16:44:05.4581615Z Verifica ser o Jboss já foi instalado ----------------------------------- 0.36s
2026-11-19T16:44:05.4582115Z jboss : Copy template script -------------------------------------------- 0.08s
2026-11-19T16:44:05.4582539Z vhost : Definindo o nome do Virtual Host -------------------------------- 0.08s
2026-11-19T16:44:05.4582912Z Setando a versão do Jboss ----------------------------------------------- 0.07s
2026-11-19T16:44:05.4583248Z Sobrescrevendo groups vars ---------------------------------------------- 0.07s
2026-11-19T16:44:05.4583530Z java : include ---------------------------------------------------------- 0.05s
2026-11-19T16:44:05.4583820Z jboss : Update domain.xml to use LDAP ----------------------------------- 0.05s
2026-11-19T16:44:05.4584088Z jboss : Domain | Set service name --------------------------------------- 0.04s
2026-11-19T16:44:05.4584359Z jboss : Set file config to use domain.xml subsystem management ---------- 0.04s
2026-11-19T16:44:05.4584584Z Determine variable jboss_domain_instance standalone --------------------- 0.04s
2026-11-19T16:44:05.4584855Z jboss : Standalone | Set service name ----------------------------------- 0.04s
2026-11-19T16:44:05.4585120Z Determine variable jboss_domain_instance DC ----------------------------- 0.04s
2026-11-19T16:44:05.4585539Z Determine variable jboss_domain_instance HC ----------------------------- 0.04s
2026-11-19T16:44:05.4585990Z Playbook run took 0 days, 0 hours, 0 minutes, 7 seconds
2026-11-19T16:44:05.5181568Z ##[section]Finishing: Configurando o Apache





networks
hosts
      networks VLANs lines AS CM import/export manage help
search result

GestióIP
#interno.todos



IP	hostname	description-SD	site	type	AI	comment	reservado	vendor	hostname_Manual	OS	CM	model	Localização	network			

    	10.116.196.110	 CADDEAPLLX1370	Esteira Agil: Servidor Jboss - SITES	CEPTISP											

    	10.116.196.111	 CADDEAPLLX1371	Esteira Agil: Servidor Jboss - SIATD-PAUTAS-FUNCEF	CEPTISP											

    	10.116.196.112	 CADDEAPLLX1372	Esteira Agil: Servidor Jboss - SIACG-AGENDA	CEPTISP											

    	10.116.196.113	 CADDEAPLLX1373	Esteira Agil: Servidor Jboss - SIRCL-BATCH	CEPTISP											

    	10.116.196.114	 CADDEAPLLX1374	Esteira Agil: Servidor Jboss - SIRCL-BATCH	CEPTISP											

    	10.116.196.115	 CADDEAPLLX1375	Esteira Agil: Servidor Jboss - SIRCL-BATCH	CEPTISP											

    	10.116.196.116	 CADDEAPLLX1376	Esteira Agil: Servidor Jboss - SIRCL-BATCH	CEPTISP											

    	10.116.196.117	 CADDEAPLLX1378	Esteira Agil: Servidor Jboss - SIACG-AGENDA	CEPTISP											

    	10.116.196.118	 CADDEAPLLX1379	Esteira Agil: Servidor Jboss - SIFGG-BATCH-VM	CEPTISP											

    	10.116.220.33	 CADDEAPLLX1377	Esteira Agil - Teste de aloca��o de IP	CEPTISP											

    	10.116.223.233	 CADDEAPLLX137	[esteiras ageis] Servidor APACHE DES WILD	CEPTISP											

    	10.184.26.160	 CADDEAPLLX1370	WO0000082032363	Estendido_DTC-CTC											

    	10.184.26.161	 CADDEAPLLX1375	WO0000082032363	Estendido_DTC-CTC											

    	10.188.9.255	 CADDEAPLLX1372	WO0000081031468	CTC											

    	10.188.10.0	 CADDEAPLLX1378	WO0000081031468	CTC											

    	10.188.15.112	 CADDEAPLLX1375	WO0000082032363												

    	10.188.15.113	 CADDEAPLLX1370	WO0000082032363												

    	192.168.236.193	 CADDEAPLLX1375	CADDEAPLLX1375 - BKP	CTC											

 


  editdelete   descriptionsitetypecommentAIUTreservadovendorhostname_ManualOSCMmodelLocalização

          GestióIP v3.1




networks
hosts
      networks VLANs lines AS CM import/export manage help
search result

GestióIP
#interno.todos



IP	hostname	description-SD	site	type	AI	comment	reservado	vendor	hostname_Manual	OS	CM	model	Localização	network			

    	10.116.196.119	 CADDEAPLLX1380	Esteira Agil: Servidor Jboss - SIACC-API-CONVENIOS	CEPTISP											

    	10.116.196.130	 CADDEAPLLX1381	Esteira Agil: Servidor Jboss - SISDE-PIX-BATCH	CEPTISP											

    	10.116.196.131	 CADDEAPLLX1382	Esteira Agil: Servidor Jboss - SITES	CEPTISP											

    	10.116.196.132	 CADDEAPLLX1383	Esteira Agil: Servidor Jboss - SIACG-AGENDA	CEPTISP											

    	10.116.196.133	 CADDEAPLLX1384	Esteira Agil: Servidor Jboss - SIACG-AGENDA	CEPTISP											

    	10.116.196.134	 CADDEAPLLX1385	Esteira Agil: Servidor Jboss - SIMIL	CEPTISP											

    	10.116.196.135	 CADDEAPLLX1386	Esteira Agil: Servidor Jboss - SIFES-INTRANET	CEPTISP											

    	10.116.196.136	 CADDEAPLLX1387	Esteira Agil: Servidor Jboss - SIFES-INTRANET	CEPTISP											

    	10.116.196.137	 CADDEAPLLX1388	Esteira Agil: Servidor Jboss - SIMIL-WEB	CEPTISP											

    	10.116.196.138	 CADDEAPLLX1389	Esteira Agil: Servidor Jboss - SIMIL-WEB	CEPTISP											

    	10.116.223.234	 CADDEAPLLX138	[esteiras ageis] Servidor APACHE DES WILD	CEPTISP											

 


  editdelete   descriptionsitetypecommentAIUTreservadovendorhostname_ManualOSCMmodelLocalização

          GestióIP v3.1

| condicoes deste aviso
| ***********************************************************************
End of banner message from server
Keyboard-interactive authentication prompts from server:
| Verification code:
End of keyboard-interactive prompts from server
    ┌──────────────────────────────────────────────────────────────────────┐
    │               • MobaXterm Professional Edition v24.2 •               │
    │               (SSH client, X server and network tools)               │
    │                                                                      │
    │ ⮞ SSH session to p585600@10.122.150.31                               │
    │   • Direct SSH      :  ✓                                             │
    │   • SSH compression :  ✓                                             │
    │   • SSH-browser     :  ✓                                             │
    │   • X11-forwarding  :  ✓  (remote display is forwarded through SSH)  │
    │                                                                      │
    │ ⮞ For more info, ctrl+click on help or visit our website.            │
    └──────────────────────────────────────────────────────────────────────┘

Last login: Tue Nov 24 10:07:31 2026 from 10.111.14.49
[p585600@cadsvitrlx100 ~]$ ssh 10.116.193.253
The authenticity of host '10.116.193.253 (10.116.193.253)' can't be established.
ED25519 key fingerprint is SHA256:KO10dr3WhBOs9ag9MpNZh2LtGRR7P9KoXXpaIqma8eg.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:32: 10.116.194.28
    ~/.ssh/known_hosts:50: 10.116.194.157
    ~/.ssh/known_hosts:59: 10.116.198.41
    ~/.ssh/known_hosts:72: 10.116.194.156
    ~/.ssh/known_hosts:133: 10.116.193.244
    ~/.ssh/known_hosts:185: 10.116.195.93
    ~/.ssh/known_hosts:222: 10.116.200.45
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '10.116.193.253' (ED25519) to the list of known hosts.
p585600@10.116.193.253's password:
Permission denied, please try again.
p585600@10.116.193.253's password:
Creating home directory for p585600.
Last failed login: Tue Nov 24 10:34:49 -03 2026 from 10.122.150.31 on ssh:notty
There was 1 failed login attempt since the last successful login.
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ ip -4 a | grep -E '10.116.(180.23|193.253)'
    inet 10.116.193.253/19 brd 10.116.223.255 scope global noprefixroute ens192
-sh-4.2$
-sh-4.2$
-sh-4.2$ ss -ltnp 2>/dev/null | grep -E ':(80|443|8080|8443) '
LISTEN     0      128    10.116.193.253:8443                     *:*
LISTEN     0      128    10.116.193.253:8080                     *:*
-sh-4.2$
-sh-4.2$ systemctl is-active httpd 2>/dev/null
unknown
-sh-4.2$
-sh-4.2$
-sh-4.2$ grep -RniE '^\s*(Timeout|ProxyTimeout)\b|timeout=' /etc/httpd/conf /etc/httpd/conf.d 2>/dev/null
-sh-4.2$
-sh-4.2$
-sh-4.2$




