
-sh-4.2$
-sh-4.2$ POD=sicow-conres-okd-des-27-jftds
-sh-4.2$ oc exec $POD -n sicow-des -- ls -la /opt/jboss/standalone/log/
total 124
drwxrwxr-x. 1 185 root   122 Oct 24 10:56 .
drwxrwxr-x. 1 185 root    80 Feb  6  2024 ..
-rwxrwxr--. 1 185 root     0 Feb  6  2024 audit.log
-rw-r--r--. 1 185 root  1041 Oct 14 18:05 backupgc.log.current
-rw-r--r--. 1 185 root 16561 Oct 24 10:56 gc.log.0.current
-rw-r--r--. 1 185 root 57544 Oct 24 10:59 server.log
-rwxrwxr--. 1 185 root 22068 Feb  6  2024 server.log.2024-02-06
-rw-r--r--. 1 185 root 13188 Oct 14 18:05 server.log.2026-10-14
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec $POD -n sicow-des -- grep -E "ModuleNotFound|WFLYUT0021|WFLYSRV0010|WFLYSRV0025|WFLYSRV0026|veio sem valor|Login failed|scowdb01|ERROR" /opt/jboss/standalone/log/server.log | head -40
2026-10-24 10:56:47,501 ERROR [org.jboss.msc.service.fail] (MSC service thread 1-1) MSC000001: Failed to start service jboss.deployment.unit."sicow-conres-okd.war".INSTALL: org.jboss.msc.service.StartException in service jboss.deployment.unit."sicow-conres-okd.war".INSTALL: WFLYSRV0153: Failed to process phase INSTALL of deployment "sicow-conres-okd.war"
2026-10-24 10:56:47,998 ERROR [org.jboss.as.controller.management-operation] (Controller Boot Thread) WFLYCTL0013: Operation ("deploy") failed - address: ([("deployment" => "sicow-conres-okd.war")]) - failure description: {
2026-10-24 10:56:48,016 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 45) WFLYSRV0010: Deployed "sicow-conres-okd.war" (runtime-name : "sicow-conres-okd.war")
2026-10-24 10:56:48,017 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 45) WFLYSRV0010: Deployed "applicationinsights-agent-3.7.1.jar" (runtime-name : "applicationinsights-agent-3.7.1.jar")
2026-10-24 10:56:48,179 ERROR [org.jboss.as] (Controller Boot Thread) WFLYSRV0026: JBoss EAP 7.4.11.GA (WildFly Core 15.0.26.Final-redhat-00001) started (with errors) in 34495ms - Started 557 of 798 services (6 services failed or missing dependencies, 451 services are lazy, passive or on-demand)
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec $POD -n sicow-des -- grep -n -A8 "<root-logger>" /opt/jboss/standalone/configuration/standalone-okd.xml
142:            <root-logger>
143-                <level name="INFO"/>
144-                <handlers>
145-                    <handler name="FILE"/>
146-                </handlers>
147-            </root-logger>
148-            <formatter name="PATTERN">
149-                <pattern-formatter pattern="%d{yyyy-MM-dd HH:mm:ss,SSS} %-5p [%c] (%t) %s%e%n"/>
150-            </formatter>
-sh-4.2$
