ddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# ls -la /log_jboss/sigsj_internet/
total 212
drwxr-xr-x 2 jboss jboss    232 nov 19 03:09 .
drwxr-xr-x 4 jboss jboss     48 nov 12 16:47 ..
-rw-r--r-- 1 jboss jboss 122053 nov 19 11:32 sigsj_internet.log
-rw-r--r-- 1 jboss jboss   2519 nov 12 19:36 sigsj_internet.log.2026-11-12-PM
-rw-r--r-- 1 jboss jboss   1937 nov 13 03:17 sigsj_internet.log.2026-11-13-AM
-rw-r--r-- 1 jboss jboss   3874 nov 13 22:12 sigsj_internet.log.2026-11-13-PM
-rw-r--r-- 1 jboss jboss   1937 nov 17 17:09 sigsj_internet.log.2026-11-17-PM
-rw-r--r-- 1 jboss jboss   1937 nov 18 15:28 sigsj_internet.log.2026-11-18-PM
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# tail -80 /log_jboss/sigsj_internet/sigsj_internet.log
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
Caused by: org.apache.jasper.JasperException: java.lang.NullPointerException
        at org.apache.jasper.servlet.JspServletWrapper.service(JspServletWrapper.java:473)
        at org.apache.jasper.servlet.JspServlet.serviceJspFile(JspServlet.java:403)
        at org.apache.jasper.servlet.JspServlet.service(JspServlet.java:347)
        at javax.servlet.http.HttpServlet.service(HttpServlet.java:590)
        at io.undertow.servlet.handlers.ServletHandler.handleRequest(ServletHandler.java:74)
        at io.undertow.servlet.handlers.FilterHandler.handleRequest(FilterHandler.java:81)
        at io.undertow.jsp.JspFileHandler.handleRequest(JspFileHandler.java:32)
        at io.undertow.servlet.handlers.ServletChain$1.handleRequest(ServletChain.java:68)
        at io.undertow.servlet.handlers.ServletDispatchingHandler.handleRequest(ServletDispatchingHandler.java:36)
        at io.undertow.servlet.handlers.RedirectDirHandler.handleRequest(RedirectDirHandler.java:68)
        at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
        at io.undertow.servlet.handlers.ServletInitialHandler.dispatchRequest(ServletInitialHandler.java:257)
        at io.undertow.servlet.handlers.ServletInitialHandler.dispatchToPath(ServletInitialHandler.java:182)
        at io.undertow.servlet.spec.RequestDispatcherImpl.forwardImpl(RequestDispatcherImpl.java:188)
        at io.undertow.servlet.spec.RequestDispatcherImpl.forwardImplSetup(RequestDispatcherImpl.java:136)
        at io.undertow.servlet.spec.RequestDispatcherImpl.forward(RequestDispatcherImpl.java:99)
        at br.gov.caixa.sigsj.internet.filter.ExceptionFilter.forwardErrorPage(ExceptionFilter.java:55)
        ... 32 more
Caused by: java.lang.NullPointerException
        at org.apache.jsp.error_jsp._jspService(error_jsp.java:115)
        at org.apache.jasper.runtime.HttpJspBase.service(HttpJspBase.java:70)
        at javax.servlet.http.HttpServlet.service(HttpServlet.java:590)
        at org.apache.jasper.servlet.JspServletWrapper.service(JspServletWrapper.java:433)
        ... 48 more
[ERROR] 2026/11/19 11:32:36 undertow.request[default task-2] - UT005022: Exception generating error page /mensagem/erro.jsp
org.apache.jasper.JasperException: java.lang.NullPointerException
        at org.apache.jasper.servlet.JspServletWrapper.service(JspServletWrapper.java:473)
        at org.apache.jasper.servlet.JspServlet.serviceJspFile(JspServlet.java:403)
        at org.apache.jasper.servlet.JspServlet.service(JspServlet.java:347)
        at javax.servlet.http.HttpServlet.service(HttpServlet.java:590)
        at io.undertow.servlet.handlers.ServletHandler.handleRequest(ServletHandler.java:74)
        at io.undertow.servlet.handlers.FilterHandler.handleRequest(FilterHandler.java:81)
        at io.undertow.jsp.JspFileHandler.handleRequest(JspFileHandler.java:32)
        at io.undertow.servlet.handlers.ServletChain$1.handleRequest(ServletChain.java:68)
        at io.undertow.servlet.handlers.ServletDispatchingHandler.handleRequest(ServletDispatchingHandler.java:36)
        at io.undertow.servlet.handlers.RedirectDirHandler.handleRequest(RedirectDirHandler.java:68)
        at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
        at io.undertow.servlet.handlers.ServletInitialHandler.dispatchRequest(ServletInitialHandler.java:257)
        at io.undertow.servlet.handlers.ServletInitialHandler.dispatchToPath(ServletInitialHandler.java:182)
        at io.undertow.servlet.spec.RequestDispatcherImpl.error(RequestDispatcherImpl.java:414)
        at io.undertow.servlet.spec.RequestDispatcherImpl.error(RequestDispatcherImpl.java:372)
        at io.undertow.servlet.handlers.ServletInitialHandler.handleFirstRequest(ServletInitialHandler.java:314)
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
        at org.apache.jsp.mensagem.erro_jsp._jspService(erro_jsp.java:113)
        at org.apache.jasper.runtime.HttpJspBase.service(HttpJspBase.java:70)
        at javax.servlet.http.HttpServlet.service(HttpServlet.java:590)
        at org.apache.jasper.servlet.JspServletWrapper.service(JspServletWrapper.java:433)
        ... 36 more
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# ls -la /opt/jboss-eap/standalone/log/
total 48
drwxrwxr-x 2 jboss jboss   122 out 22 12:01 .
drwxrwxr-x 8 jboss jboss    91 set 30  2024 ..
-rwxrwxr-x 1 jboss jboss     0 set 30  2024 audit.log
-rwxrwxr-x 1 jboss jboss     0 set 30  2024 backupgc.log.current
-rwxrwxr-x 1 jboss jboss     0 set 30  2024 gc.log.0.current
-rw-r--r-- 1 jboss jboss 47660 out 22 12:31 server.log
-rwxrwxr-x 1 jboss jboss     0 set 30  2024 server.log.2024-09-30
[root@caddeapllx2854 ~]# grep -n "2026-11-19 11:3" /opt/jboss-eap/standalone/log/server.log | tail -5
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
