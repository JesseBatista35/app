Verificar os problemas para avançar com a esteira DevOps do SICOW.
 
No último deploy do CONRES, os logs não apresentam mais erros além da ocorrência de timeout. Poderia, por gentileza, nos apoiar na análise dessa situação? 404 - Not Found

Correção conforme o SICOW-PENHOR-OKD

/opt/jboss/bin/standalone.conf: line 37: =org.jboss.byteman: command not found
=========================================================================

  JBoss Bootstrap Environment

  JBOSS_HOME: /opt/jboss

  JAVA: /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.372.b07-1.el7_9.x86_64/jre/bin/java

  JAVA_OPTS:  -verbose:gc -Xloggc:"/opt/jboss/standalone/log/gc.log" -XX:+PrintGCDetails -XX:+PrintGCDateStamps -XX:+UseGCLogFileRotation -XX:NumberOfGCLogFiles=5 -XX:GCLogFileSize=3M -XX:-TraceClassUnloading -Xms1024m -Xmx1024m -XX:MetaspaceSize=96m -XX:MaxMetaspaceSize=512m -Djava.net.preferIPv4Stack=true -Djboss.modules.system.pkgs= -Djava.awt.headless=true -Djavax.net.ssl.trustStore=/opt/jboss/standalone/configuration/caixa-truststore-acteste-nprd.jks -Djavax.net.ssl.trustStorePassword=changeit -Dhttps.proxyHost=proxydes.caixa -Dhttps.proxyPort=80 -Dhttp.proxyHost=proxydes.caixa -Dhttp.proxyPort=80 -Dhttp.nonProxyHosts=*.caixa -Djboss.modules.policy-permissions=true -server -XX:+ExplicitGCInvokesConcurrent -XX:+UseG1GC -XX:MaxGCPauseMillis=500 -Xbootclasspath/p:/opt/jboss/modules/system/layers/base/org/wildfly/common/main/wildfly-common-1.5.4.Final-redhat-00001.jar -Xbootclasspath/p:/opt/jboss/modules/system/layers/base/org/jboss/logmanager/main/jboss-logmanager-2.1.18.Final-redhat-00001.jar -Djboss.modules.system.pkgs=org.jboss.byteman,org.jboss.logmanager -Djava.util.logging.manager=org.jboss.logmanager.LogManager -javaagent:/opt/jmx_exporter/jmx_prometheus.jar=8778:/opt/jmx_exporter/jmx_prometheus.yaml -javaagent:/opt/jboss/standalone/deployments/applicationinsights-agent-3.7.1.jar -Djava.net.useSystemProxies=false -Dhttp.proxyHost=proxydes.caixa -Dhttp.proxyPort=80 -Dhttps.proxyHost=proxydes.caixa -Dhttps.proxyPort=80 -Dhttp.nonProxyHosts=localhost\|127.0.0.1\|*.caixa 

=========================================================================

OpenJDK 64-Bit Server VM warning: If the number of processors is expected to increase from one, then you should configure the number of parallel GC threads appropriately using -XX:ParallelGCThreads=N
2026-10-16 15:12:17.623-03:00 WARN  i.o.s.a.ResourceConfiguration - Found reference to io.opentelemetry.sdk.autoconfigure.internal.EnvironmentResourceProvider in otel.java.enabled.resource.providers. Please update to io.opentelemetry.sdk.autoconfigure.EnvironmentResourceProvider. Support for the old provider name will be removed after 1.49.0.
2026-10-16 15:12:35.093-03:00 INFO  c.m.applicationinsights.agent - Application Insights Java Agent 3.7.1 started successfully (PID 172, JVM running for 31.745 s)
2026-10-16 15:12:35.095-03:00 INFO  c.m.applicationinsights.agent - Java version: 1.8.0_372, vendor: Red Hat, Inc., home: /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.372.b07-1.el7_9.x86_64/jre
[0m15:12:36,455 INFO  [org.jboss.modules] (main) JBoss Modules version 1.12.0.Final-redhat-00001
[0m[0m15:12:37,675 INFO  [org.jboss.msc] (main) JBoss MSC version 1.4.12.Final-redhat-00001
[0m[0m15:12:37,855 INFO  [org.jboss.threads] (main) JBoss Threads version 2.4.0.Final-redhat-00001
[0m[0m15:12:38,451 INFO  [org.jboss.as] (MSC service thread 1-2) WFLYSRV0049: JBoss EAP 7.4.11.GA (WildFly Core 15.0.26.Final-redhat-00001) starting
[0m[0m15:12:38,668 INFO  [org.jboss.vfs] (MSC service thread 1-1) VFS000002: Failed to clean existing content for temp file provider of type temp. Enable DEBUG level log to find what caused this
[0m[0m15:12:42,072 INFO  [org.wildfly.security] (ServerService Thread Pool -- 30) ELY00001: WildFly Elytron version 1.15.16.Final-redhat-00001
[0m[0m15:12:42,957 INFO  [org.jboss.as.controller.management-deprecated] (ServerService Thread Pool -- 20) WFLYCTL0033: Extension 'security' is deprecated and may not be supported in future versions
[0m[0m15:12:44,371 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/core-service=management/management-interface=http-interface' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
[0m[0m15:12:44,455 INFO  [org.jboss.as.controller.management-deprecated] (ServerService Thread Pool -- 34) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/subsystem=undertow/server=default-server/https-listener=https' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
[0m[0m15:12:45,481 INFO  [org.jboss.as.repository] (ServerService Thread Pool -- 24) WFLYDR0001: Content added at location /opt/jboss/standalone/data/content/43/10e3eda419b2f2c7d4fb432f9cf7908f535920/content
[0m[0m15:12:45,979 INFO  [org.jboss.as.repository] (ServerService Thread Pool -- 24) WFLYDR0001: Content added at location /opt/jboss/standalone/data/content/03/260c94acbe38ed76f6cacd76dae0a416620ba2/content
[0m[0m15:12:46,050 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0039: Creating http management service using socket-binding (management-http)
[0m[0m15:12:46,083 INFO  [org.xnio] (MSC service thread 1-1) XNIO version 3.8.9.Final-redhat-00001
[0m[0m15:12:46,144 INFO  [org.xnio.nio] (MSC service thread 1-1) XNIO NIO Implementation Version 3.8.9.Final-redhat-00001
[0m[33m15:12:46,254 WARN  [org.jboss.as.txn] (ServerService Thread Pool -- 74) WFLYTX0013: The node-identifier attribute on the /subsystem=transactions is set to the default value. This is a danger for environments running multiple servers. Please make sure the attribute value is unique.
[0m[0m15:12:46,345 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 54) WFLYCLINF0001: Activating Infinispan subsystem.
[0m[0m15:12:46,360 INFO  [org.wildfly.extension.io] (ServerService Thread Pool -- 55) WFLYIO001: Worker 'default' has auto-configured to 2 IO threads with 16 max task threads based on your 1 available processors
[0m[0m15:12:46,362 INFO  [org.jboss.as.clustering.jgroups] (ServerService Thread Pool -- 59) WFLYCLJG0001: Activating JGroups subsystem. JGroups version 4.2.11
[0m[0m15:12:46,363 INFO  [org.jboss.as.naming] (ServerService Thread Pool -- 66) WFLYNAM0001: Activating Naming Subsystem
[0m[0m15:12:46,365 INFO  [org.wildfly.extension.health] (ServerService Thread Pool -- 52) WFLYHEALTH0001: Activating Base Health Subsystem
[0m[0m15:12:46,364 INFO  [org.jboss.as.jaxrs] (ServerService Thread Pool -- 56) WFLYRS0016: RESTEasy version 3.15.7.Final-redhat-00001
[0m[0m15:12:46,444 INFO  [org.jboss.as.security] (ServerService Thread Pool -- 72) WFLYSEC0002: Activating Security Subsystem
[0m[0m15:12:46,446 INFO  [org.wildfly.extension.metrics] (ServerService Thread Pool -- 65) WFLYMETRICS0001: Activating Base Metrics Subsystem
[0m[0m15:12:46,547 INFO  [org.jboss.as.webservices] (ServerService Thread Pool -- 76) WFLYWS0002: Activating WebServices Extension
[0m[0m15:12:46,548 INFO  [org.jboss.as.jsf] (ServerService Thread Pool -- 62) WFLYJSF0007: Activated the following Jakarta Server Faces Implementations: [main]
[0m[0m15:12:46,647 INFO  [org.wildfly.iiop.openjdk] (ServerService Thread Pool -- 53) WFLYIIOP0001: Activating IIOP Subsystem
[0m[0m15:12:46,743 INFO  [org.jboss.as.security] (MSC service thread 1-1) WFLYSEC0001: Current PicketBox version=5.0.3.Final-redhat-00009
[0m[0m15:12:47,350 INFO  [org.jboss.as.connector] (MSC service thread 1-2) WFLYJCA0009: Starting Jakarta Connectors Subsystem (WildFly/IronJacamar 1.5.11.Final-redhat-00001)
[0m[0m15:12:47,744 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-2) WFLYUT0003: Undertow 2.2.24.SP1-redhat-00001 starting
[0m[0m15:12:47,762 INFO  [org.jboss.remoting] (MSC service thread 1-2) JBoss Remoting version 5.0.27.Final-redhat-00001
[0m[0m15:12:48,245 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 75) WFLYUT0014: Creating file handler for path '/opt/jboss/welcome-content' with options [directory-listing: 'false', follow-symlink: 'false', case-sensitive: 'true', safe-symlink-paths: '[]']
[0m[0m15:12:48,248 INFO  [org.jboss.as.ejb3] (MSC service thread 1-2) WFLYEJB0481: Strict pool slsb-strict-max-pool is using a max instance size of 16 (per class), which is derived from thread worker pool sizing.
[0m[0m15:12:48,248 INFO  [org.jboss.as.ejb3] (MSC service thread 1-1) WFLYEJB0482: Strict pool mdb-strict-max-pool is using a max instance size of 4 (per class), which is derived from the number of CPUs on this host.
[0m[0m15:12:48,356 INFO  [org.jboss.as.naming] (MSC service thread 1-1) WFLYNAM0003: Starting Naming Service
[0m[0m15:12:48,455 INFO  [org.jboss.as.mail.extension] (MSC service thread 1-1) WFLYMAIL0001: Bound mail session [java:jboss/mail/Default]
[0m[33m15:12:48,654 WARN  [org.wildfly.extension.elytron] (MSC service thread 1-1) WFLYELY00023: KeyStore file '/opt/jboss/standalone/configuration/application.keystore' does not exist. Used blank.
[0m[33m15:12:49,162 WARN  [org.wildfly.extension.elytron] (MSC service thread 1-1) WFLYELY01084: KeyStore /opt/jboss/standalone/configuration/application.keystore not found, it will be auto generated on first use with a self-signed certificate for host localhost
[0m[0m15:12:49,445 INFO  [org.wildfly.iiop.openjdk] (MSC service thread 1-2) WFLYIIOP0009: CORBA ORB Service started
[0m[0m15:12:49,458 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-2) WFLYUT0012: Started server default-server.
[0m[0m15:12:49,751 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-1) Queuing requests.
[0m[0m15:12:49,752 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-1) WFLYUT0018: Host default-host starting
[0m[0m15:12:49,766 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-2) WFLYUT0006: Undertow AJP listener ajp listening on 0.0.0.0:8009
[0m[0m15:12:49,852 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-1) WFLYUT0006: Undertow HTTP listener default listening on 0.0.0.0:8080
[0m[0m15:12:49,853 INFO  [org.jboss.as.ejb3] (MSC service thread 1-1) WFLYEJB0493: Jakarta Enterprise Beans subsystem suspension complete
[0m[0m15:12:50,747 INFO  [org.jboss.as.patching] (MSC service thread 1-1) WFLYPAT0050: JBoss EAP cumulative patch ID is: base, one-off patches include: none
[0m
