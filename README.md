
-sh-4.1$ cd /logs/jboss-eap/hc/servers/sipen_node3_lx0006/
-sh-4.1$
-sh-4.1$
-sh-4.1$ ls -lh
total 235M
-rw-rw-r-- 1 jboss jboss  22M Nov 10 10:06 server.log
-rw-rw-r-- 1 jboss jboss  51M Nov  8 00:53 server.log.1
-rw-rw-r-- 1 jboss jboss 871K Nov 10 10:06 sipen.log
-rw-rw-r-- 1 jboss jboss  45M Nov  5 18:23 sipen.log.2026-11-04
-rw-rw-r-- 1 jboss jboss  70M Nov  6 13:23 sipen.log.2026-11-05
-rw-rw-r-- 1 jboss jboss  30M Nov  8 14:27 sipen.log.2026-11-06
-rw-rw-r-- 1 jboss jboss 6.6M Nov  9 18:28 sipen.log.2026-11-08
-rw-rw-r-- 1 jboss jboss  12M Nov 10 09:28 sipen.log.2026-11-09
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$ grep -c "LoginException\|Erro na montagem do Menu" server.log server.log.1
server.log:94
server.log.1:9
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$ grep -n -B10 -A40 "LoginException" server.log | head -200]
head: invalid trailing option -- ]
Try `head --help' for more information.
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$ grep -n -i "Caused by\|ECI\|CTG\|CICS\|Connection refused\|timed out\|SocketException\|obtenção dos dados de login" server.log | head -100
34143:2026-11-08 12:59:43,461DEBUG(ajp-/10.116.88.25:13309-1)206 read class attr -- 'br/gov/caixa/sipen/exception/MensagemCicsSipenException'
34423:2026-11-08 12:59:43,472DEBUG(ajp-/10.116.88.25:13309-1)421 read class attr -- 'Lbr/gov/caixa/sipen/exception/MensagemCicsSipenException;'
35741:2026-11-08 12:59:53,922DEBUG(ajp-/10.116.88.25:13309-6)375 read class attr -- 'relatorioLimiteEspecialEmprestimoForm'
35743:2026-11-08 12:59:53,922DEBUG(ajp-/10.116.88.25:13309-6)377 read class attr -- 'br/gov/caixa/sipen/action/relatoriolimiteespecialemprestimo/RelatorioLimiteEspecialEmprestimoForm'
36076:2026-11-08 12:59:53,937DEBUG(ajp-/10.116.88.25:13309-6)710 read class attr -- 'consultaReciboComunicadoOcorrenciaForm'
36078:2026-11-08 12:59:53,937DEBUG(ajp-/10.116.88.25:13309-6)712 read class attr -- 'br/gov/caixa/sipen/action/licitacao/siscoaf/consultarecibocomunicadoocorrencia/ConsultaReciboComunicadoOcorrenciaForm'
36101:2026-11-08 12:59:53,938DEBUG(ajp-/10.116.88.25:13309-6)735 read class attr -- 'balancaPrecisaoForm'
36103:2026-11-08 12:59:53,938DEBUG(ajp-/10.116.88.25:13309-6)737 read class attr -- 'br/gov/caixa/sipen/action/balancaprecisao/BalancaPrecisaoForm'
36865:2026-11-08 12:59:53,969DEBUG(ajp-/10.116.88.25:13309-6)1393 read class attr -- 'Lbr/gov/caixa/sipen/action/relatoriolimiteespecialemprestimo/RelatorioLimiteEspecialEmprestimoForm;'
36932:2026-11-08 12:59:53,973DEBUG(ajp-/10.116.88.25:13309-6)1460 read class attr -- 'Lbr/gov/caixa/sipen/action/licitacao/siscoaf/consultarecibocomunicadoocorrencia/ConsultaReciboComunicadoOcorrenciaForm;'
36937:2026-11-08 12:59:53,973DEBUG(ajp-/10.116.88.25:13309-6)1465 read class attr -- 'Lbr/gov/caixa/sipen/action/balancaprecisao/BalancaPrecisaoForm;'
37148:2026-11-08 12:59:53,983DEBUG(ajp-/10.116.88.25:13309-6)1676 read class attr -- '${balancaPrecisaoForm.codigosMensagens}'
37163:2026-11-08 12:59:53,984DEBUG(ajp-/10.116.88.25:13309-6)1691 read class attr -- '${consultaReciboComunicadoOcorrenciaForm.codigosMensagens}'
38136:2026-11-08 13:00:44,845DEBUG(ajp-/10.116.88.25:13309-5)218 read class attr -- 'balancaPrecisaoForm'
38138:2026-11-08 13:00:44,845DEBUG(ajp-/10.116.88.25:13309-5)220 read class attr -- 'br/gov/caixa/sipen/action/balancaprecisao/BalancaPrecisaoForm'
38276:2026-11-08 13:00:44,849DEBUG(ajp-/10.116.88.25:13309-5)332 read class attr -- '            * BR201506925_RTC1050490 - Balanca Precisao
38653:2026-11-08 13:00:44,864DEBUG(ajp-/10.116.88.25:13309-5)678 read class attr -- 'Lbr/gov/caixa/sipen/action/balancaprecisao/BalancaPrecisaoForm;'
39607:2026-11-08 13:00:58,803DEBUG(ajp-/10.116.88.25:13309-5)632 read class attr -- 'seleciona('0001'); '
39658:2026-11-08 13:00:58,805DEBUG(ajp-/10.116.88.25:13309-5)683 read class attr -- 'seleciona('0002'); '
39710:2026-11-08 13:00:58,808DEBUG(ajp-/10.116.88.25:13309-5)735 read class attr -- 'seleciona('0003'); '
39761:2026-11-08 13:00:58,810DEBUG(ajp-/10.116.88.25:13309-5)786 read class attr -- 'seleciona('0004'); '
39810:2026-11-08 13:00:58,812DEBUG(ajp-/10.116.88.25:13309-5)835 read class attr -- 'seleciona('0005'); '
44627:2026-11-08 14:02:03,446ERROR(ContainerBackgroundProcessor[StandardEngine[jboss.web]])MODCLUSTER000043: Failed to send STATUS to 10.116.84.136/10.116.84.136:6666: java.net.SocketException: Connection reset
44648:2026-11-08 14:02:03,468ERROR(ContainerBackgroundProcessor[StandardEngine[jboss.web]])MODCLUSTER000043: Failed to send STATUS to 10.116.84.137/10.116.84.137:6666: java.net.SocketException: Connection reset
63374:  java.specification.maintenance.version = 6
63375:  java.specification.name = Java Platform API Specification
63376:  java.specification.vendor = Oracle Corporation
63377:  java.specification.version = 1.8
63385:  java.vm.specification.name = Java Virtual Machine Specification
63386:  java.vm.specification.vendor = Oracle Corporation
63387:  java.vm.specification.version = 1.8
64003:2026-11-08 20:00:33,208INFO (MSC service thread 1-3)JNDI bindings for session bean named JCicsDirectBean in deployment unit deployment "framework.jar" are as follows:
64005:  java:global/framework/JCicsDirectBean!br.gov.caixa.util.jcicsdirect.JCicsDirectBean
64006:  java:app/framework/JCicsDirectBean!br.gov.caixa.util.jcicsdirect.JCicsDirectBean
64007:  java:module/JCicsDirectBean!br.gov.caixa.util.jcicsdirect.JCicsDirectBean
64008:  java:global/framework/JCicsDirectBean
64009:  java:app/framework/JCicsDirectBean
64010:  java:module/JCicsDirectBean
64013:2026-11-08 20:00:33,247DEBUG(MSC service thread 1-6)Configuring component class: br.gov.caixa.util.jcicsdirect.JCicsDirectBean named JCicsDirectBean
64014:2026-11-08 20:00:33,302DEBUG(MSC service thread 1-6)Security is *not* enabled on EJB: JCicsDirectBean, since no explicit security domain is configured for the bean, nor is there any default security domain configured in the EJB3 subsystem
64019:2026-11-08 20:00:33,355DEBUG(MSC service thread 1-8)Using pool config StrictMaxPoolConfig{name=slsb-strict-max-pool, maxPoolSize=20, timeoutUnit=MINUTES, timeout=5} to create pool for Stateless EJB JCicsDirectBean
100679:2026-11-09 08:22:42,992ERROR(ajp-/10.116.88.25:13309-2)JBAS014134: A Invoca▒▒o EJB falhou no JCicsDirectBean do componente para o public br.gov.caixa.util.jcicsconnect.MensagemCics br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(br.gov.caixa.util.jcicsconnect.MensagemCics) throws br.gov.caixa.seguranca.LoginException,br.gov.caixa.util.jcicsconnect.LeMensagemException do m▒todo: javax.ejb.EJBException: java.lang.NullPointerException
100714: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean$$$view1.login(Unknown Source) [framework.jar:]
100740:Caused by: java.lang.NullPointerException
100741: at br.gov.caixa.util.jcicsconnect.JCicsConnect.login(JCicsConnect.java:182) [framework.jar:]
100742: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(JCicsDirectBean.java:79) [framework.jar:]
100868:2026-11-09 08:24:50,858ERROR(ajp-/10.116.88.25:13309-1)JBAS014134: A Invoca▒▒o EJB falhou no JCicsDirectBean do componente para o public br.gov.caixa.util.jcicsconnect.MensagemCics br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(br.gov.caixa.util.jcicsconnect.MensagemCics) throws br.gov.caixa.seguranca.LoginException,br.gov.caixa.util.jcicsconnect.LeMensagemException do m▒todo: javax.ejb.EJBException: java.lang.NullPointerException
100903: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean$$$view1.login(Unknown Source) [framework.jar:]
100929:Caused by: java.lang.NullPointerException
100930: at br.gov.caixa.util.jcicsconnect.JCicsConnect.login(JCicsConnect.java:182) [framework.jar:]
100931: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(JCicsDirectBean.java:79) [framework.jar:]
100968:2026-11-09 08:25:08,669ERROR(ajp-/10.116.88.25:13309-5)JBAS014134: A Invoca▒▒o EJB falhou no JCicsDirectBean do componente para o public br.gov.caixa.util.jcicsconnect.MensagemCics br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(br.gov.caixa.util.jcicsconnect.MensagemCics) throws br.gov.caixa.seguranca.LoginException,br.gov.caixa.util.jcicsconnect.LeMensagemException do m▒todo: javax.ejb.EJBException: java.lang.NullPointerException
101003: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean$$$view1.login(Unknown Source) [framework.jar:]
101029:Caused by: java.lang.NullPointerException
101030: at br.gov.caixa.util.jcicsconnect.JCicsConnect.login(JCicsConnect.java:182) [framework.jar:]
101031: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(JCicsDirectBean.java:79) [framework.jar:]
102075:2026-11-09 08:46:59,664ERROR(ajp-/10.116.88.25:13309-1)JBAS014134: A Invoca▒▒o EJB falhou no JCicsDirectBean do componente para o public br.gov.caixa.util.jcicsconnect.MensagemCics br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(br.gov.caixa.util.jcicsconnect.MensagemCics) throws br.gov.caixa.seguranca.LoginException,br.gov.caixa.util.jcicsconnect.LeMensagemException do m▒todo: javax.ejb.EJBException: java.lang.NullPointerException
102110: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean$$$view1.login(Unknown Source) [framework.jar:]
102136:Caused by: java.lang.NullPointerException
102137: at br.gov.caixa.util.jcicsconnect.JCicsConnect.login(JCicsConnect.java:182) [framework.jar:]
102138: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(JCicsDirectBean.java:79) [framework.jar:]
102798:2026-11-09 08:59:59,654ERROR(ajp-/10.116.88.25:13309-3)JBAS014134: A Invoca▒▒o EJB falhou no JCicsDirectBean do componente para o public br.gov.caixa.util.jcicsconnect.MensagemCics br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(br.gov.caixa.util.jcicsconnect.MensagemCics) throws br.gov.caixa.seguranca.LoginException,br.gov.caixa.util.jcicsconnect.LeMensagemException do m▒todo: javax.ejb.EJBException: java.lang.NullPointerException
102833: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean$$$view1.login(Unknown Source) [framework.jar:]
102859:Caused by: java.lang.NullPointerException
102860: at br.gov.caixa.util.jcicsconnect.JCicsConnect.login(JCicsConnect.java:182) [framework.jar:]
102861: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(JCicsDirectBean.java:79) [framework.jar:]
103125:2026-11-09 09:05:01,356ERROR(ajp-/10.116.88.25:13309-2)JBAS014134: A Invoca▒▒o EJB falhou no JCicsDirectBean do componente para o public br.gov.caixa.util.jcicsconnect.MensagemCics br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(br.gov.caixa.util.jcicsconnect.MensagemCics) throws br.gov.caixa.seguranca.LoginException,br.gov.caixa.util.jcicsconnect.LeMensagemException do m▒todo: javax.ejb.EJBException: java.lang.NullPointerException
103160: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean$$$view1.login(Unknown Source) [framework.jar:]
103186:Caused by: java.lang.NullPointerException
103187: at br.gov.caixa.util.jcicsconnect.JCicsConnect.login(JCicsConnect.java:182) [framework.jar:]
103188: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(JCicsDirectBean.java:79) [framework.jar:]
103419:2026-11-09 09:09:29,706ERROR(ajp-/10.116.88.25:13309-2)JBAS014134: A Invoca▒▒o EJB falhou no JCicsDirectBean do componente para o public br.gov.caixa.util.jcicsconnect.MensagemCics br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(br.gov.caixa.util.jcicsconnect.MensagemCics) throws br.gov.caixa.seguranca.LoginException,br.gov.caixa.util.jcicsconnect.LeMensagemException do m▒todo: javax.ejb.EJBException: java.lang.NullPointerException
103454: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean$$$view1.login(Unknown Source) [framework.jar:]
103480:Caused by: java.lang.NullPointerException
103481: at br.gov.caixa.util.jcicsconnect.JCicsConnect.login(JCicsConnect.java:182) [framework.jar:]
103482: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(JCicsDirectBean.java:79) [framework.jar:]
103604:2026-11-09 09:11:07,084ERROR(ajp-/10.116.88.25:13309-3)JBAS014134: A Invoca▒▒o EJB falhou no JCicsDirectBean do componente para o public br.gov.caixa.util.jcicsconnect.MensagemCics br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(br.gov.caixa.util.jcicsconnect.MensagemCics) throws br.gov.caixa.seguranca.LoginException,br.gov.caixa.util.jcicsconnect.LeMensagemException do m▒todo: javax.ejb.EJBException: java.lang.NullPointerException
103639: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean$$$view1.login(Unknown Source) [framework.jar:]
103665:Caused by: java.lang.NullPointerException
103666: at br.gov.caixa.util.jcicsconnect.JCicsConnect.login(JCicsConnect.java:182) [framework.jar:]
103667: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(JCicsDirectBean.java:79) [framework.jar:]
103695:2026-11-09 09:11:11,664ERROR(ajp-/10.116.88.25:13309-4)JBAS014134: A Invoca▒▒o EJB falhou no JCicsDirectBean do componente para o public br.gov.caixa.util.jcicsconnect.MensagemCics br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(br.gov.caixa.util.jcicsconnect.MensagemCics) throws br.gov.caixa.seguranca.LoginException,br.gov.caixa.util.jcicsconnect.LeMensagemException do m▒todo: javax.ejb.EJBException: java.lang.NullPointerException
103730: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean$$$view1.login(Unknown Source) [framework.jar:]
103756:Caused by: java.lang.NullPointerException
103757: at br.gov.caixa.util.jcicsconnect.JCicsConnect.login(JCicsConnect.java:182) [framework.jar:]
103758: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(JCicsDirectBean.java:79) [framework.jar:]
103794:2026-11-09 09:11:28,671ERROR(ajp-/10.116.88.25:13309-3)JBAS014134: A Invoca▒▒o EJB falhou no JCicsDirectBean do componente para o public br.gov.caixa.util.jcicsconnect.MensagemCics br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(br.gov.caixa.util.jcicsconnect.MensagemCics) throws br.gov.caixa.seguranca.LoginException,br.gov.caixa.util.jcicsconnect.LeMensagemException do m▒todo: javax.ejb.EJBException: java.lang.NullPointerException
103829: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean$$$view1.login(Unknown Source) [framework.jar:]
103855:Caused by: java.lang.NullPointerException
103856: at br.gov.caixa.util.jcicsconnect.JCicsConnect.login(JCicsConnect.java:182) [framework.jar:]
103857: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(JCicsDirectBean.java:79) [framework.jar:]
103918:2026-11-09 09:11:45,717ERROR(ajp-/10.116.88.25:13309-3)JBAS014134: A Invoca▒▒o EJB falhou no JCicsDirectBean do componente para o public br.gov.caixa.util.jcicsconnect.MensagemCics br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(br.gov.caixa.util.jcicsconnect.MensagemCics) throws br.gov.caixa.seguranca.LoginException,br.gov.caixa.util.jcicsconnect.LeMensagemException do m▒todo: javax.ejb.EJBException: java.lang.NullPointerException
103953: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean$$$view1.login(Unknown Source) [framework.jar:]
103979:Caused by: java.lang.NullPointerException
103980: at br.gov.caixa.util.jcicsconnect.JCicsConnect.login(JCicsConnect.java:182) [framework.jar:]
103981: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(JCicsDirectBean.java:79) [framework.jar:]
104101:2026-11-09 09:13:12,469ERROR(ajp-/10.116.88.25:13309-1)JBAS014134: A Invoca▒▒o EJB falhou no JCicsDirectBean do componente para o public br.gov.caixa.util.jcicsconnect.MensagemCics br.gov.caixa.util.jcicsdirect.JCicsDirectBean.login(br.gov.caixa.util.jcicsconnect.MensagemCics) throws br.gov.caixa.seguranca.LoginException,br.gov.caixa.util.jcicsconnect.LeMensagemException do m▒todo: javax.ejb.EJBException: java.lang.NullPointerException
104136: at br.gov.caixa.util.jcicsdirect.JCicsDirectBean$$$view1.login(Unknown Source) [framework.jar:]
104162:Caused by: java.lang.NullPointerException
104163: at br.gov.caixa.util.jcicsconnect.JCicsConnect.login(JCicsConnect.java:182) [framework.jar:]
-sh-4.1$
-sh-4.1$
-sh-4.1$ grep -n "JBAS015874\|WFLYSRV0025\|started in" server.log server.log.1
server.log:63467:2026-11-08 20:00:29,788DEBUG(MSC service thread 1-7)JBoss EAP 6.4.24.GA (AS 7.5.24.Final-redhat-00001) root service started in 20245506314.414062 ms
server.log:64864:2026-11-08 20:00:38,101INFO (Controller Boot Thread)JBAS015874: JBoss EAP 6.4.24.GA (AS 7.5.24.Final-redhat-00001) iniciado em 10843ms - Iniciado 1055 de servi▒os 1156 (os servi▒os 133 s▒o lazy, passivos ou em demanda)
server.log:200843:2026-11-09 20:00:32,301DEBUG(MSC service thread 1-7)JBoss EAP 6.4.24.GA (AS 7.5.24.Final-redhat-00001) root service started in 20331908828.062967 ms
server.log:202238:2026-11-09 20:00:40,746INFO (Controller Boot Thread)JBAS015874: JBoss EAP 6.4.24.GA (AS 7.5.24.Final-redhat-00001) iniciado em 10811ms - Iniciado 1055 de servi▒os 1156 (os servi▒os 133 s▒o lazy, passivos ou em demanda)
server.log:247237:2026-11-10 09:30:25,423DEBUG(MSC service thread 1-7)JBoss EAP 6.4.24.GA (AS 7.5.24.Final-redhat-00001) root service started in 20380501949.788138 ms
server.log:248632:2026-11-10 09:30:29,630INFO (Controller Boot Thread)JBAS015874: JBoss EAP 6.4.24.GA (AS 7.5.24.Final-redhat-00001) iniciado em 4725ms - Iniciado 1055 de servi▒os 1156 (os servi▒os 133 s▒o lazy, passivos ou em demanda)
server.log.1:1345:2026-11-04 13:57:56,825INFO (Controller Boot Thread)JBAS015874: JBoss EAP 6.4.24.GA (AS 7.5.24.Final-redhat-00001) iniciado em 12729ms - Iniciado 1055 de servi▒os 1156 (os servi▒os 133 s▒o lazy, passivos ou em demanda)
server.log.1:142168:2026-11-04 20:00:30,415DEBUG(MSC service thread 1-7)JBoss EAP 6.4.24.GA (AS 7.5.24.Final-redhat-00001) root service started in 19899906941.576650 ms
server.log.1:143565:2026-11-04 20:00:39,318INFO (Controller Boot Thread)JBAS015874: JBoss EAP 6.4.24.GA (AS 7.5.24.Final-redhat-00001) iniciado em 10955ms - Iniciado 1055 de servi▒os 1156 (os servi▒os 133 s▒o lazy, passivos ou em demanda)
server.log.1:358858:2026-11-05 20:00:32,927DEBUG(MSC service thread 1-7)JBoss EAP 6.4.24.GA (AS 7.5.24.Final-redhat-00001) root service started in 19986309453.864647 ms
server.log.1:360257:2026-11-05 20:00:41,708INFO (Controller Boot Thread)JBAS015874: JBoss EAP 6.4.24.GA (AS 7.5.24.Final-redhat-00001) iniciado em 11257ms - Iniciado 1055 de servi▒os 1156 (os servi▒os 133 s▒o lazy, passivos ou em demanda)
server.log.1:496635:2026-11-06 20:00:41,603DEBUG(MSC service thread 1-7)JBoss EAP 6.4.24.GA (AS 7.5.24.Final-redhat-00001) root service started in 20072718130.139050 ms
server.log.1:498030:2026-11-06 20:00:50,578INFO (Controller Boot Thread)JBAS015874: JBoss EAP 6.4.24.GA (AS 7.5.24.Final-redhat-00001) iniciado em 11081ms - Iniciado 1055 de servi▒os 1156 (os servi▒os 133 s▒o lazy, passivos ou em demanda)
server.log.1:565485:2026-11-07 20:00:40,517DEBUG(MSC service thread 1-7)JBoss EAP 6.4.24.GA (AS 7.5.24.Final-redhat-00001) root service started in 20159117044.047415 ms
server.log.1:566882:2026-11-07 20:00:49,061INFO (Controller Boot Thread)JBAS015874: JBoss EAP 6.4.24.GA (AS 7.5.24.Final-redhat-00001) iniciado em 10757ms - Iniciado 1055 de servi▒os 1156 (os servi▒os 133 s▒o lazy, passivos ou em demanda)
-sh-4.1$
