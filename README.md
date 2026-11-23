] senha para p585600:
Último login: seg nov 23 10:07:02 -03 2026
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# tail -60 /log_jboss/sigsj_internet/sigsj_internet.log
        at io.undertow.servlet.handlers.ServletInitialHandler.dispatchRequest(ServletInitialHandler.java:255)
        at io.undertow.servlet.handlers.ServletInitialHandler.access$000(ServletInitialHandler.java:79)
        at io.undertow.servlet.handlers.ServletInitialHandler$1.handleRequest(ServletInitialHandler.java:100)
        at io.undertow.server.Connectors.executeRootHandler(Connectors.java:393)
        at io.undertow.server.HttpServerExchange$1.run(HttpServerExchange.java:852)
        at org.jboss.threads.ContextClassLoaderSavingRunnable.run(ContextClassLoaderSavingRunnable.java:35)
        at org.jboss.threads.EnhancedQueueExecutor.safeRun(EnhancedQueueExecutor.java:1990)
        at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.doRunTask(EnhancedQueueExecutor.java:1486)
        at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.run(EnhancedQueueExecutor.java:1377)
        at org.xnio.XnioWorker$WorkerThreadFactory$1$1.run(XnioWorker.java:1282)
        at java.lang.Thread.run(Thread.java:750)
[ERROR] 2026/11/23 09:46:57 undertow.request[default task-5] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
java.lang.NoClassDefFoundError: Could not initialize class br.gov.caixa.util.SenhasSIIBC
        at br.gov.caixa.sigsj.common.sirot.siper.AbstractSiperDTO.encriptar(AbstractSiperDTO.java:113)
        at br.gov.caixa.sigsj.common.sirot.siper.LoginDTO.compoeMensagem(LoginDTO.java:59)
        at br.gov.caixa.sigsj.common.sirot.siper.AbstractSiperDTO.getISOMsg(AbstractSiperDTO.java:40)
        at br.gov.caixa.sigsj.common.dao.CommonDAO.sendRajada(CommonDAO.java:56)
        at br.gov.caixa.sigsj.common.dao.CommonDAO.sendRajadaResponseDataRajada(CommonDAO.java:26)
        at br.gov.caixa.sigsj.internet.dao.sirot.siper.LoginDAOSiperImpl.consultar(LoginDAOSiperImpl.java:90)
        at br.gov.caixa.sigsj.internet.service.impl.LoginServiceImpl.consultarUsuario(LoginServiceImpl.java:39)
        at br.gov.caixa.sigsj.internet.servlet.AutenticadorServlet.logarUsuario(AutenticadorServlet.java:229)
        at br.gov.caixa.sigsj.internet.servlet.AutenticadorServlet.autenticarPorLogin(AutenticadorServlet.java:136)
        at br.gov.caixa.sigsj.internet.servlet.AutenticadorServlet.processarAutenticacao(AutenticadorServlet.java:94)
        at br.gov.caixa.sigsj.internet.servlet.AutenticadorServlet.doPost(AutenticadorServlet.java:62)
        at javax.servlet.http.HttpServlet.service(HttpServlet.java:523)
        at javax.servlet.http.HttpServlet.service(HttpServlet.java:590)
        at io.undertow.servlet.handlers.ServletHandler.handleRequest(ServletHandler.java:74)
        at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:129)
        at br.gov.caixa.sigsj.internet.filter.ExceptionFilter.doFilter(ExceptionFilter.java:33)
        at io.undertow.servlet.core.ManagedFilter.doFilter(ManagedFilter.java:67)
        at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:131)
        at io.undertow.servlet.handlers.FilterHandler.handleRequest(FilterHandler.java:84)
        at io.undertow.servlet.handlers.ServletChain$1.handleRequest(ServletChain.java:68)
        at io.undertow.servlet.handlers.ServletDispatchingHandler.handleRequest(ServletDispatchingHandler.java:36)
        at io.undertow.servlet.handlers.RedirectDirHandler.handleRequest(RedirectDirHandler.java:68)
        at org.wildfly.extension.undertow.deployment.GlobalRequestControllerHandler.handleRequest(GlobalRequestControllerHandler.java:68)
        at io.undertow.servlet.handlers.SendErrorPageHandler.handleRequest(SendErrorPageHandler.java:52)
        at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
        at io.undertow.servlet.handlers.ServletInitialHandler.handleFirstRequest(ServletInitialHandler.java:275)
        at io.undertow.servlet.handlers.ServletInitialHandler.access$100(ServletInitialHandler.java:79)
        at io.undertow.servlet.handlers.ServletInitialHandler$2.call(ServletInitialHandler.java:134)
        at io.undertow.servlet.handlers.ServletInitialHandler$2.call(ServletInitialHandler.java:131)
        at io.undertow.servlet.core.ServletRequestContextThreadSetupAction$1.call(ServletRequestContextThreadSetupAction.java:48)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at org.wildfly.extension.undertow.deployment.UndertowDeploymentInfoService$UndertowThreadSetupAction.lambda$create$0(UndertowDeploymentInfoService.java:1555)
        at org.wildfly.extension.undertow.deployment.UndertowDeploymentInfoService$UndertowThreadSetupAction.lambda$create$0(UndertowDeploymentInfoService.java:1555)
        at org.wildfly.extension.undertow.deployment.UndertowDeploymentInfoService$UndertowThreadSetupAction.lambda$create$0(UndertowDeploymentInfoService.java:1555)
        at org.wildfly.extension.undertow.deployment.UndertowDeploymentInfoService$UndertowThreadSetupAction.lambda$create$0(UndertowDeploymentInfoService.java:1555)
        at org.wildfly.extension.undertow.deployment.UndertowDeploymentInfoService$UndertowThreadSetupAction.lambda$create$0(UndertowDeploymentInfoService.java:1555)
        at io.undertow.servlet.handlers.ServletInitialHandler.dispatchRequest(ServletInitialHandler.java:255)
        at io.undertow.servlet.handlers.ServletInitialHandler.access$000(ServletInitialHandler.java:79)
        at io.undertow.servlet.handlers.ServletInitialHandler$1.handleRequest(ServletInitialHandler.java:100)
        at io.undertow.server.Connectors.executeRootHandler(Connectors.java:393)
        at io.undertow.server.HttpServerExchange$1.run(HttpServerExchange.java:852)
        at org.jboss.threads.ContextClassLoaderSavingRunnable.run(ContextClassLoaderSavingRunnable.java:35)
        at org.jboss.threads.EnhancedQueueExecutor.safeRun(EnhancedQueueExecutor.java:1990)
        at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.doRunTask(EnhancedQueueExecutor.java:1486)
        at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.run(EnhancedQueueExecutor.java:1377)
        at org.xnio.XnioWorker$WorkerThreadFactory$1$1.run(XnioWorker.java:1282)
        at java.lang.Thread.run(Thread.java:750)
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# grep -nE "ERROR|Exception|Caused by|ORA-|SenhasSIIBC|SIROT|SIPER|getResponse|Connection" /log_jboss/sigsj_internet/sigsj_internet.log | tail -40
grep: /log_jboss/sigsj_internet/sigsj_internet.log: arquivo binário coincide com o padrão
17:[ INFO] 2026/11/23 03:37:38 connector.deployment[MSC service thread 1-3] - WFLYJCA0011: Sem limite de conectores de Jakarta ConnectionFactory [java:/JmsXA]
57:[ERROR] 2026/11/23 03:41:45 undertow.request[default task-3] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
58:java.lang.UnsatisfiedLinkError: no SenhasSIIBC in java.library.path
62:     at br.gov.caixa.util.SenhasSIIBC.<clinit>(Unknown Source)
78:     at br.gov.caixa.sigsj.internet.filter.ExceptionFilter.doFilter(ExceptionFilter.java:33)
110:[ERROR] 2026/11/23 03:41:51 undertow.request[default task-3] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
111:java.lang.NoClassDefFoundError: Could not initialize class br.gov.caixa.util.SenhasSIIBC
127:    at br.gov.caixa.sigsj.internet.filter.ExceptionFilter.doFilter(ExceptionFilter.java:33)
161:[ERROR] 2026/11/23 08:45:43 undertow.request[default task-3] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
162:java.lang.NoClassDefFoundError: Could not initialize class br.gov.caixa.util.SenhasSIIBC
178:    at br.gov.caixa.sigsj.internet.filter.ExceptionFilter.doFilter(ExceptionFilter.java:33)
210:[ERROR] 2026/11/23 08:45:49 undertow.request[default task-5] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
211:java.lang.NoClassDefFoundError: Could not initialize class br.gov.caixa.util.SenhasSIIBC
227:    at br.gov.caixa.sigsj.internet.filter.ExceptionFilter.doFilter(ExceptionFilter.java:33)
259:[ERROR] 2026/11/23 08:45:57 undertow.request[default task-5] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
260:java.lang.NoClassDefFoundError: Could not initialize class br.gov.caixa.util.SenhasSIIBC
276:    at br.gov.caixa.sigsj.internet.filter.ExceptionFilter.doFilter(ExceptionFilter.java:33)
308:[ERROR] 2026/11/23 08:46:13 undertow.request[default task-5] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
309:java.lang.NoClassDefFoundError: Could not initialize class br.gov.caixa.util.SenhasSIIBC
325:    at br.gov.caixa.sigsj.internet.filter.ExceptionFilter.doFilter(ExceptionFilter.java:33)
357:[ERROR] 2026/11/23 08:48:58 undertow.request[default task-5] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
358:java.lang.NoClassDefFoundError: Could not initialize class br.gov.caixa.util.SenhasSIIBC
374:    at br.gov.caixa.sigsj.internet.filter.ExceptionFilter.doFilter(ExceptionFilter.java:33)
406:[ERROR] 2026/11/23 09:46:57 undertow.request[default task-5] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
407:java.lang.NoClassDefFoundError: Could not initialize class br.gov.caixa.util.SenhasSIIBC
423:    at br.gov.caixa.sigsj.internet.filter.ExceptionFilter.doFilter(ExceptionFilter.java:33)
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
