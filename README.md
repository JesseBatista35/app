
[root@caddeapllx2557 bolchk]#
[root@caddeapllx2557 bolchk]# grep -o "server_urls=[^ ]* *[^ ]*" /opt/jboss-eap/bin/standalone.conf
server_urls=https://sigsj-frontend-des.apps.nprd.caixa/ -Delastic.apm.global_labels=deployment=sigsj-boleto-des-esteiras"
[root@caddeapllx2557 bolchk]#
[root@caddeapllx2557 bolchk]#
[root@caddeapllx2557 bolchk]# grep -n "WFLYUT0021" /logs/jboss/jboss-eap/standalone/sigsj-boleto/server.log | tail -3
1149:2026-10-21 16:07:53,881 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 81) WFLYUT0021: Contexto web registrado: '/boletoService' para servidor 'default-server'
1451:2026-10-21 16:53:19,235 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 74) WFLYUT0021: Contexto web registrado: '/boletoService' para servidor 'default-server'
[root@caddeapllx2557 bolchk]#
[root@caddeapllx2557 bolchk]#
[root@caddeapllx2557 bolchk]#
[root@caddeapllx2557 bolchk]# grep -nE "ERROR|FileNotFound|log_jboss" /logs/jboss/jboss-eap/standalone/sigsj-boleto/server.log | tail -20
1431:2026-10-21 16:53:18,734 ERROR [stderr] (ServerService Thread Pool -- 74)   at io.undertow.servlet.core.DeploymentManagerImpl$2.call(DeploymentManagerImpl.java:589)
1432:2026-10-21 16:53:18,734 ERROR [stderr] (ServerService Thread Pool -- 74)   at io.undertow.servlet.core.DeploymentManagerImpl$2.call(DeploymentManagerImpl.java:559)
1433:2026-10-21 16:53:18,734 ERROR [stderr] (ServerService Thread Pool -- 74)   at io.undertow.servlet.core.ServletRequestContextThreadSetupAction$1.call(ServletRequestContextThreadSetupAction.java:42)
1434:2026-10-21 16:53:18,734 ERROR [stderr] (ServerService Thread Pool -- 74)   at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
1435:2026-10-21 16:53:18,734 ERROR [stderr] (ServerService Thread Pool -- 74)   at org.wildfly.extension.undertow.deployment.UndertowDeploymentInfoService$UndertowThreadSetupAction.lambda$create$0(UndertowDeploymentInfoService.java:1555)
1436:2026-10-21 16:53:18,734 ERROR [stderr] (ServerService Thread Pool -- 74)   at org.wildfly.extension.undertow.deployment.UndertowDeploymentInfoService$UndertowThreadSetupAction.lambda$create$0(UndertowDeploymentInfoService.java:1555)
1437:2026-10-21 16:53:18,734 ERROR [stderr] (ServerService Thread Pool -- 74)   at org.wildfly.extension.undertow.deployment.UndertowDeploymentInfoService$UndertowThreadSetupAction.lambda$create$0(UndertowDeploymentInfoService.java:1555)
1438:2026-10-21 16:53:18,734 ERROR [stderr] (ServerService Thread Pool -- 74)   at org.wildfly.extension.undertow.deployment.UndertowDeploymentInfoService$UndertowThreadSetupAction.lambda$create$0(UndertowDeploymentInfoService.java:1555)
1439:2026-10-21 16:53:18,734 ERROR [stderr] (ServerService Thread Pool -- 74)   at io.undertow.servlet.core.DeploymentManagerImpl.start(DeploymentManagerImpl.java:605)
1440:2026-10-21 16:53:18,734 ERROR [stderr] (ServerService Thread Pool -- 74)   at org.wildfly.extension.undertow.deployment.UndertowDeploymentService.startContext(UndertowDeploymentService.java:97)
1441:2026-10-21 16:53:18,734 ERROR [stderr] (ServerService Thread Pool -- 74)   at org.wildfly.extension.undertow.deployment.UndertowDeploymentService$1.run(UndertowDeploymentService.java:78)
1442:2026-10-21 16:53:18,734 ERROR [stderr] (ServerService Thread Pool -- 74)   at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
1443:2026-10-21 16:53:18,734 ERROR [stderr] (ServerService Thread Pool -- 74)   at java.util.concurrent.FutureTask.run(FutureTask.java:266)
1444:2026-10-21 16:53:18,734 ERROR [stderr] (ServerService Thread Pool -- 74)   at org.jboss.threads.ContextClassLoaderSavingRunnable.run(ContextClassLoaderSavingRunnable.java:35)
1445:2026-10-21 16:53:18,734 ERROR [stderr] (ServerService Thread Pool -- 74)   at org.jboss.threads.EnhancedQueueExecutor.safeRun(EnhancedQueueExecutor.java:1990)
1446:2026-10-21 16:53:18,735 ERROR [stderr] (ServerService Thread Pool -- 74)   at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.doRunTask(EnhancedQueueExecutor.java:1486)
1447:2026-10-21 16:53:18,735 ERROR [stderr] (ServerService Thread Pool -- 74)   at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.run(EnhancedQueueExecutor.java:1377)
1448:2026-10-21 16:53:18,735 ERROR [stderr] (ServerService Thread Pool -- 74)   at java.lang.Thread.run(Thread.java:750)
1449:2026-10-21 16:53:18,735 ERROR [stderr] (ServerService Thread Pool -- 74)   at org.jboss.threads.JBossThread.run(JBossThread.java:513)
1458:2026-10-21 16:53:25,395 ERROR [org.jboss.modcluster] (UndertowEventHandlerAdapterService - 1) MODCLUSTER000043: Failed to send INFO command to localhost/127.0.0.1:6666: Conexão recusada (Connection refused)
[root@caddeapllx2557 bolchk]#
[root@caddeapllx2557 bolchk]#
[root@caddeapllx2557 bolchk]#
