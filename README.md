
[root@caddeapllx955 earx]#
[root@caddeapllx955 earx]# exit
exit
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$ sudo su
[sudo] senha para p585600:
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]# tail -40 /log_jboss/sigsj_intranet/sigsj_intranet.log
        at io.undertow.servlet.handlers.ServletInitialHandler.handleFirstRequest(ServletInitialHandler.java:314)
        at io.undertow.servlet.handlers.ServletInitialHandler.access$100(ServletInitialHandler.java:79)
        at io.undertow.servlet.handlers.ServletInitialHandler$2.call(ServletInitialHandler.java:134)
        at io.undertow.servlet.handlers.ServletInitialHandler$2.call(ServletInitialHandler.java:131)
        at io.undertow.servlet.core.ServletRequestContextThreadSetupAction$1.call(ServletRequestContextThreadSetupAction.java:48)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at org.wildfly.extension.undertow.security.SecurityContextThreadSetupAction.lambda$create$0(SecurityContextThreadSetupAction.java:105)
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
        ... 39 more
[DEBUG] 2026/11/19 14:54:43 ldap.AcessoLdap[default task-19] - Consulta utilizando usuario an▒nimo
[ INFO] 2026/11/19 14:54:43 support.AbstractContextSource[default task-19] - Property 'userDn' not set - anonymous context will be used for read-write operations
[DEBUG] 2026/11/19 14:54:43 ldap.AcessoLdap[default task-19] - Consulta utilizando filter atual [(&(objectclass=cefusuario)(uid=C897834))]
[ INFO] 2026/11/19 14:54:44 sirot.SirotConnector[default task-19] -
EXECUTANDO TRANSACAO: GJ01
[DEBUG] 2026/11/19 14:54:44 sirot.SirotProcessar[default task-19] - Subida [ Rajada: 0 ] >>>
[DEBUG] 2026/11/19 14:54:44 sirot.SirotProcessar[default task-19] -     C▒digo da Mensagem [0]: 0205
[DEBUG] 2026/11/19 14:54:44 sirot.SirotProcessar[default task-19] -     C▒digo de Processamento [3]: 041098
[DEBUG] 2026/11/19 14:54:44 sirot.SirotProcessar[default task-19] -     Rede Transmissora [33]: 9777
[DEBUG] 2026/11/19 14:54:44 sirot.SirotProcessar[default task-19] -     Dados para TS [41]: 5444
[DEBUG] 2026/11/19 14:54:44 sirot.SirotProcessar[default task-19] -     Subida [63]: GJ01C897834 027952320001000106010305060809
[DEBUG] 2026/11/19 14:54:44 sirot.SirotProcessar[default task-19] -     Rede Receptora [100]: 0104
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]# grep -n "ERROR\|SIROT\|SIPER\|getResponse\|Connection\|SenhasSIIBC" /log_jboss/sigsj_intranet/sigsj_intranet.log | tail -20
1525:[ERROR] 2026/11/19 14:52:27 facelets.viewhandler[default task-19] - Error Rendering View[/bemVindo.xhtml]
1662:[ERROR] 2026/11/19 14:52:27 jsf.lifecycle[default task-19] - JSF1054: (Phase ID: RENDER_RESPONSE 6, View ID: /bemVindo.xhtml) Exception thrown during phase execution: javax.faces.event.PhaseEvent[source=com.sun.faces.lifecycle.LifecycleImpl@292b8c3a]
1663:[ERROR] 2026/11/19 14:52:27 webapp.BaseXMLFilter[default task-19] - Exception in the filter chain
1800:[ERROR] 2026/11/19 14:52:27 undertow.request[default task-19] - UT005023: Exception handling request to /sigsj_intranet/error.jsp
1881:[ERROR] 2026/11/19 14:52:27 undertow.request[default task-19] - UT005022: Exception generating error page /mensagem/erro.jsp
1929:[ERROR] 2026/11/19 14:53:20 facelets.viewhandler[default task-19] - Error Rendering View[/bemVindo.xhtml]
2066:[ERROR] 2026/11/19 14:53:20 jsf.lifecycle[default task-19] - JSF1054: (Phase ID: RENDER_RESPONSE 6, View ID: /bemVindo.xhtml) Exception thrown during phase execution: javax.faces.event.PhaseEvent[source=com.sun.faces.lifecycle.LifecycleImpl@292b8c3a]
2067:[ERROR] 2026/11/19 14:53:20 webapp.BaseXMLFilter[default task-19] - Exception in the filter chain
2204:[ERROR] 2026/11/19 14:53:20 undertow.request[default task-19] - UT005023: Exception handling request to /sigsj_intranet/error.jsp
2285:[ERROR] 2026/11/19 14:53:20 undertow.request[default task-19] - UT005022: Exception generating error page /mensagem/erro.jsp
2333:[ERROR] 2026/11/19 14:53:20 facelets.viewhandler[default task-19] - Error Rendering View[/bemVindo.xhtml]
2470:[ERROR] 2026/11/19 14:53:20 jsf.lifecycle[default task-19] - JSF1054: (Phase ID: RENDER_RESPONSE 6, View ID: /bemVindo.xhtml) Exception thrown during phase execution: javax.faces.event.PhaseEvent[source=com.sun.faces.lifecycle.LifecycleImpl@292b8c3a]
2471:[ERROR] 2026/11/19 14:53:20 webapp.BaseXMLFilter[default task-19] - Exception in the filter chain
2608:[ERROR] 2026/11/19 14:53:20 undertow.request[default task-19] - UT005023: Exception handling request to /sigsj_intranet/error.jsp
2689:[ERROR] 2026/11/19 14:53:20 undertow.request[default task-19] - UT005022: Exception generating error page /mensagem/erro.jsp
2737:[ERROR] 2026/11/19 14:53:20 facelets.viewhandler[default task-19] - Error Rendering View[/bemVindo.xhtml]
2874:[ERROR] 2026/11/19 14:53:20 jsf.lifecycle[default task-19] - JSF1054: (Phase ID: RENDER_RESPONSE 6, View ID: /bemVindo.xhtml) Exception thrown during phase execution: javax.faces.event.PhaseEvent[source=com.sun.faces.lifecycle.LifecycleImpl@292b8c3a]
2875:[ERROR] 2026/11/19 14:53:20 webapp.BaseXMLFilter[default task-19] - Exception in the filter chain
3012:[ERROR] 2026/11/19 14:53:20 undertow.request[default task-19] - UT005023: Exception handling request to /sigsj_intranet/error.jsp
3093:[ERROR] 2026/11/19 14:53:20 undertow.request[default task-19] - UT005022: Exception generating error page /mensagem/erro.jsp
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#


cara sera se a rede reutilixou um mesmo vip apontoad pra meso balanceador



<img width="1633" height="888" alt="image" src="https://github.com/user-attachments/assets/2189f84e-b48d-4eb9-af24-16341db0e9ac" />


