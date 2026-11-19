
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# grep -n "2026/11/19 11:32\|11:32:" /log_jboss/sigsj_internet/sigsj_internet.log | head -20
1054:[ERROR] 2026/11/19 11:32:36 filter.ExceptionFilter[default task-2] - Erro ao processar /sigsj_internet/Autenticacao
1105:[ERROR] 2026/11/19 11:32:36 undertow.request[default task-2] - UT005023: Exception handling request to /sigsj_internet/error.jsp
1165:[ERROR] 2026/11/19 11:32:36 undertow.request[default task-2] - UT005022: Exception generating error page /mensagem/erro.jsp
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# awk '/11:32:3[0-6]/{p=1} p' /log_jboss/sigsj_internet/sigsj_internet.log | grep -vE "erro\.jsp|error_jsp|erro_jsp|ExceptionFilter.forwardErrorPage|generating error page" | grep -A25 -iE "ERROR|Exception|Caused by" | head -60
grep: (entrada padrão): arquivo binário coincide com o padrão
[ERROR] 2026/11/19 11:32:36 filter.ExceptionFilter[default task-2] - Erro ao processar /sigsj_internet/Autenticacao
        at br.gov.caixa.sigsj.common.sirot.siper.SiperProcessar.enviaRecebeRajada(SiperProcessar.java:31)
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
Caused by: java.lang.NullPointerException
        at br.gov.caixa.sirot.transacoes.SIROTTrans.getResponse(SIROTTrans.java:191)
        at br.gov.caixa.sigsj.common.sirot.siper.SiperProcessar.enviaRecebeRajada(SiperProcessar.java:29)
        ... 44 more
[ERROR] 2026/11/19 11:32:36 undertow.request[default task-2] - UT005023: Exception handling request to /sigsj_internet/error.jsp
java.lang.RuntimeException: #######  Erro ao Tentar parsear o StackTrace e enviar para a p�gina de erro interno!
        at br.gov.caixa.sigsj.internet.filter.ExceptionFilter.doFilter(ExceptionFilter.java:36)
        at io.undertow.servlet.core.ManagedFilter.doFilter(ManagedFilter.java:67)
        at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:131)
        at io.undertow.servlet.handlers.FilterHandler.handleRequest(FilterHandler.java:84)
        at io.undertow.servlet.handlers.ServletChain$1.handleRequest(ServletChain.java:68)
        at io.undertow.servlet.handlers.ServletDispatchingHandler.handleRequest(ServletDispatchingHandler.java:36)
        at io.undertow.servlet.handlers.RedirectDirHandler.handleRequest(RedirectDirHandler.java:68)
        at org.wildfly.extension.undertow.deployment.GlobalRequestControllerHandler.handleRequest(GlobalRequestControllerHandler.java:68)
[root@caddeapllx2854 ~]#
