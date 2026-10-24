<img width="1894" height="985" alt="image" src="https://github.com/user-attachments/assets/f3e62aa0-42ea-48a0-b757-4a53ddca0531" />


=========================================================================

  JBoss Bootstrap Environment

  JBOSS_HOME: /opt/jboss

  JAVA: /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.372.b07-1.el7_9.x86_64/jre/bin/java

  JAVA_OPTS:  -verbose:gc -Xloggc:"/opt/jboss/standalone/log/gc.log" -XX:+PrintGCDetails -XX:+PrintGCDateStamps -XX:+UseGCLogFileRotation -XX:NumberOfGCLogFiles=5 -XX:GCLogFileSize=3M -XX:-TraceClassUnloading -Xms1024m -Xmx1024m -XX:MetaspaceSize=96m -XX:MaxMetaspaceSize=512m -Djava.net.preferIPv4Stack=true -Djboss.modules.system.pkgs=org.jboss.byteman -Djava.awt.headless=true -Djavax.net.ssl.trustStore=/opt/jboss/standalone/configuration/caixa-truststore-acteste-nprd.jks -Djavax.net.ssl.trustStorePassword=changeit -Dhttps.proxyHost=proxydes.caixa -Dhttps.proxyPort=80 -Dhttp.proxyHost=proxydes.caixa -Dhttp.proxyPort=80 -Dhttp.nonProxyHosts=*.caixa -Djboss.modules.policy-permissions=true -server -XX:+ExplicitGCInvokesConcurrent -XX:+UseG1GC -XX:MaxGCPauseMillis=500 -Xbootclasspath/p:/opt/jboss/modules/system/layers/base/org/wildfly/common/main/wildfly-common-1.5.4.Final-redhat-00001.jar -Xbootclasspath/p:/opt/jboss/modules/system/layers/base/org/jboss/logmanager/main/jboss-logmanager-2.1.18.Final-redhat-00001.jar -Djboss.modules.system.pkgs=org.jboss.byteman,org.jboss.logmanager -Djava.util.logging.manager=org.jboss.logmanager.LogManager -javaagent:/opt/jmx_exporter/jmx_prometheus.jar=8778:/opt/jmx_exporter/jmx_prometheus.yaml -javaagent:/opt/jboss/standalone/deployments/applicationinsights-agent-3.7.1.jar -Djava.net.useSystemProxies=false -Dhttp.proxyHost=proxydes.caixa -Dhttp.proxyPort=80 -Dhttps.proxyHost=proxydes.caixa -Dhttps.proxyPort=80 -Dhttp.nonProxyHosts=localhost\|127.0.0.1\|*.caixa 

=========================================================================

OpenJDK 64-Bit Server VM warning: If the number of processors is expected to increase from one, then you should configure the number of parallel GC threads appropriately using -XX:ParallelGCThreads=N
2026-10-24 12:44:03.653-03:00 WARN  i.o.s.a.ResourceConfiguration - Found reference to io.opentelemetry.sdk.autoconfigure.internal.EnvironmentResourceProvider in otel.java.enabled.resource.providers. Please update to io.opentelemetry.sdk.autoconfigure.EnvironmentResourceProvider. Support for the old provider name will be removed after 1.49.0.
2026-10-24 12:44:21.383-03:00 INFO  c.m.applicationinsights.agent - Application Insights Java Agent 3.7.1 started successfully (PID 171, JVM running for 32.237 s)
2026-10-24 12:44:21.385-03:00 INFO  c.m.applicationinsights.agent - Java version: 1.8.0_372, vendor: Red Hat, Inc., home: /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.372.b07-1.el7_9.x86_64/jre
[0m12:44:22,773 INFO  [org.jboss.modules] (main) JBoss Modules version 1.12.0.Final-redhat-00001
[0m[0m12:44:24,065 INFO  [org.jboss.msc] (main) JBoss MSC version 1.4.12.Final-redhat-00001
[0m[0m12:44:24,188 INFO  [org.jboss.threads] (main) JBoss Threads version 2.4.0.Final-redhat-00001
[0m[0m12:44:24,778 INFO  [org.jboss.as] (MSC service thread 1-2) WFLYSRV0049: JBoss EAP 7.4.11.GA (WildFly Core 15.0.26.Final-redhat-00001) starting
[0m[0m12:44:25,063 INFO  [org.jboss.vfs] (MSC service thread 1-1) VFS000002: Failed to clean existing content for temp file provider of type temp. Enable DEBUG level log to find what caused this
[0m[33m12:44:25,865 WARN  [org.jboss.as.controller] (Controller Boot Thread) WFLYCTL0456: System property "user.timezone" is already set in the <system-properties> section of the configuration file. The value set in the command line will be overridden by that value.
[0m[0m12:44:28,680 INFO  [org.wildfly.security] (ServerService Thread Pool -- 31) ELY00001: WildFly Elytron version 1.15.16.Final-redhat-00001
[0m[0m12:44:29,563 INFO  [org.jboss.as.controller.management-deprecated] (ServerService Thread Pool -- 14) WFLYCTL0033: Extension 'security' is deprecated and may not be supported in future versions
[0m[0m12:44:31,257 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/core-service=management/management-interface=native-interface' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
[0m[0m12:44:31,259 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/core-service=management/management-interface=http-interface' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
[0m[0m12:44:31,286 INFO  [org.jboss.as.controller.management-deprecated] (ServerService Thread Pool -- 35) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/subsystem=undertow/server=default-server/https-listener=https' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
[0m[0m12:44:32,163 INFO  [org.jboss.as.repository] (ServerService Thread Pool -- 5) WFLYDR0001: Content added at location /opt/jboss/standalone/data/content/43/10e3eda419b2f2c7d4fb432f9cf7908f535920/content
[0m[0m12:44:32,671 INFO  [org.jboss.as.repository] (ServerService Thread Pool -- 5) WFLYDR0001: Content added at location /opt/jboss/standalone/data/content/8f/a714485f427852e3aa59ff367a6b9db506f167/content
[0m[0m12:44:33,164 INFO  [org.jboss.security] (Controller Boot Thread) PBOX00361: Default Security Vault Implementation Initialized and Ready
[0m[0m12:44:33,182 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0039: Creating http management service using socket-binding (management-http)
[0m[0m12:44:33,185 INFO  [org.xnio] (MSC service thread 1-1) XNIO version 3.8.9.Final-redhat-00001
[0m[0m12:44:33,264 INFO  [org.xnio.nio] (MSC service thread 1-1) XNIO NIO Implementation Version 3.8.9.Final-redhat-00001
[0m[33m12:44:33,361 WARN  [org.jboss.as.txn] (ServerService Thread Pool -- 60) WFLYTX0013: The node-identifier attribute on the /subsystem=transactions is set to the default value. This is a danger for environments running multiple servers. Please make sure the attribute value is unique.
[0m[0m12:44:33,375 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 42) WFLYCLINF0001: Activating Infinispan subsystem.
[0m[0m12:44:33,466 INFO  [org.jboss.as.security] (ServerService Thread Pool -- 58) WFLYSEC0002: Activating Security Subsystem
[0m[0m12:44:33,558 INFO  [org.jboss.as.webservices] (ServerService Thread Pool -- 62) WFLYWS0002: Activating WebServices Extension
[0m[0m12:44:33,560 INFO  [org.jboss.as.jaxrs] (ServerService Thread Pool -- 44) WFLYRS0016: RESTEasy version 3.15.7.Final-redhat-00001
[0m[0m12:44:33,566 INFO  [org.wildfly.extension.io] (ServerService Thread Pool -- 43) WFLYIO001: Worker 'default' has auto-configured to 2 IO threads with 16 max task threads based on your 1 available processors
[0m[0m12:44:33,570 INFO  [org.jboss.as.jsf] (ServerService Thread Pool -- 49) WFLYJSF0007: Activated the following Jakarta Server Faces Implementations: [main]
[0m[0m12:44:33,664 INFO  [org.jboss.as.naming] (ServerService Thread Pool -- 52) WFLYNAM0001: Activating Naming Subsystem
[0m[0m12:44:33,870 INFO  [org.jboss.as.security] (MSC service thread 1-2) WFLYSEC0001: Current PicketBox version=5.0.3.Final-redhat-00009
[0m[0m12:44:33,873 INFO  [org.jboss.as.connector] (MSC service thread 1-1) WFLYJCA0009: Starting Jakarta Connectors Subsystem (WildFly/IronJacamar 1.5.11.Final-redhat-00001)
[0m[0m12:44:34,265 INFO  [org.jboss.as.connector.subsystems.datasources] (ServerService Thread Pool -- 26) WFLYJCA0005: Deploying non-JDBC-compliant driver class org.postgresql.Driver (version 42.2)
[0m[0m12:44:34,270 INFO  [org.jboss.remoting] (MSC service thread 1-1) JBoss Remoting version 5.0.27.Final-redhat-00001
[0m[33m12:44:34,359 WARN  [org.wildfly.clustering.web.undertow] (ServerService Thread Pool -- 61) WFLYCLWEBUT0007: No routing provider found for default-server; using legacy provider based on static configuration
[0m[0m12:44:34,360 INFO  [org.jboss.as.connector.subsystems.datasources] (ServerService Thread Pool -- 26) WFLYJCA0004: Deploying JDBC-compliant driver class org.h2.Driver (version 1.4)
[0m[0m12:44:34,562 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-1) WFLYUT0003: Undertow 2.2.24.SP1-redhat-00001 starting
[0m[0m12:44:35,065 INFO  [org.jboss.as.connector.deployers.jdbc] (MSC service thread 1-1) WFLYJCA0018: Started Driver service with driver-name = postgresql
[0m[0m12:44:35,068 INFO  [org.jboss.as.connector.deployers.jdbc] (MSC service thread 1-1) WFLYJCA0018: Started Driver service with driver-name = h2
[0m[0m12:44:35,167 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 61) WFLYUT0014: Creating file handler for path '/opt/jboss/welcome-content' with options [directory-listing: 'false', follow-symlink: 'false', case-sensitive: 'true', safe-symlink-paths: '[]']
[0m[0m12:44:35,171 INFO  [org.jboss.as.ejb3] (MSC service thread 1-1) WFLYEJB0481: Strict pool slsb-strict-max-pool is using a max instance size of 16 (per class), which is derived from thread worker pool sizing.
[0m[0m12:44:35,171 INFO  [org.jboss.as.ejb3] (MSC service thread 1-2) WFLYEJB0482: Strict pool mdb-strict-max-pool is using a max instance size of 4 (per class), which is derived from the number of CPUs on this host.
[0m[0m12:44:35,369 INFO  [org.jboss.as.naming] (MSC service thread 1-2) WFLYNAM0003: Starting Naming Service
[0m[0m12:44:35,470 INFO  [org.jboss.as.mail.extension] (MSC service thread 1-1) WFLYMAIL0001: Bound mail session [java:jboss/mail/expresso]
[0m[0m12:44:35,478 INFO  [org.jboss.as.mail.extension] (MSC service thread 1-1) WFLYMAIL0001: Bound mail session [java:jboss/mail/Default]
[0m[0m12:44:35,970 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-2) WFLYUT0012: Started server default-server.
[0m[0m12:44:36,257 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-2) WFLYUT0006: Undertow HTTP listener http listening on 0.0.0.0:8080
[0m[0m12:44:36,258 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-1) WFLYUT0006: Undertow AJP listener ajp listening on 0.0.0.0:8009
[0m[0m12:44:36,259 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-2) Queuing requests.
[0m[0m12:44:36,260 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-2) WFLYUT0018: Host default-host starting
[0m[0m12:44:36,570 INFO  [org.jboss.as.ejb3] (MSC service thread 1-1) WFLYEJB0493: Jakarta Enterprise Beans subsystem suspension complete
[0m[0m12:44:36,664 INFO  [org.jboss.as.patching] (MSC service thread 1-1) WFLYPAT0050: JBoss EAP cumulative patch ID is: base, one-off patches include: none
[0m2026-10-24 12:44:37,011 INFO  [org.wildfly.extension.messaging-activemq] (MSC service thread 1-2) WFLYMSGAMQ0075: AIO wasn't located on this platform, it will fall back to using pure Java NIO. Your platform is Linux, install LibAIO to enable the AIO journal and achieve optimal performance.
2026-10-24 12:44:37,015 WARN  [org.jboss.as.domain.management.security] (MSC service thread 1-1) WFLYDM0111: Keystore /opt/jboss/standalone/configuration/application.keystore not found, it will be auto generated on first use with a self signed certificate for host localhost
2026-10-24 12:44:37,068 INFO  [org.jboss.as.server.deployment.scanner] (MSC service thread 1-1) WFLYDS0013: Started FileSystemDeploymentService for directory /opt/jboss/standalone/deployments
2026-10-24 12:44:37,077 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0027: Starting deployment of "sicow-conres-okd.war" (runtime-name: "sicow-conres-okd.war")
2026-10-24 12:44:37,079 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0027: Starting deployment of "applicationinsights-agent-3.7.1.jar" (runtime-name: "applicationinsights-agent-3.7.1.jar")
2026-10-24 12:44:37,368 INFO  [org.jboss.as.remoting] (MSC service thread 1-1) WFLYRMT0001: Listening on 0.0.0.0:9999
2026-10-24 12:44:37,572 WARN  [org.jboss.jca.core.connectionmanager.pool.strategy.OnePool] (JCA PoolFiller) IJ000610: Unable to fill pool: java:/jboss/datasources/sicow-ds: javax.resource.ResourceException: IJ031084: Unable to create connection
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.createLocalManagedConnection(LocalManagedConnectionFactory.java:364)
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.getLocalManagedConnection(LocalManagedConnectionFactory.java:371)
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.createManagedConnection(LocalManagedConnectionFactory.java:287)
	at org.jboss.jca.core.connectionmanager.pool.mcp.SemaphoreConcurrentLinkedDequeManagedConnectionPool.createConnectionEventListener(SemaphoreConcurrentLinkedDequeManagedConnectionPool.java:1328)
	at org.jboss.jca.core.connectionmanager.pool.mcp.SemaphoreConcurrentLinkedDequeManagedConnectionPool.fillTo(SemaphoreConcurrentLinkedDequeManagedConnectionPool.java:1148)
	at org.jboss.jca.core.connectionmanager.pool.mcp.PoolFiller.run(PoolFiller.java:97)
	at java.lang.Thread.run(Thread.java:750)
Caused by: org.postgresql.util.PSQLException: FATAL: password authentication failed for user "scowdb01"
	at org.postgresql.core.v3.ConnectionFactoryImpl.doAuthentication(ConnectionFactoryImpl.java:525)
	at org.postgresql.core.v3.ConnectionFactoryImpl.tryConnect(ConnectionFactoryImpl.java:146)
	at org.postgresql.core.v3.ConnectionFactoryImpl.openConnectionImpl(ConnectionFactoryImpl.java:197)
	at org.postgresql.core.ConnectionFactory.openConnection(ConnectionFactory.java:49)
	at org.postgresql.jdbc.PgConnection.<init>(PgConnection.java:217)
	at org.postgresql.Driver.makeConnection(Driver.java:458)
	at org.postgresql.Driver.connect(Driver.java:260)
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.createLocalManagedConnection(LocalManagedConnectionFactory.java:335)
	... 6 more

2026-10-24 12:44:43,881 INFO  [org.jboss.as.connector.subsystems.datasources] (MSC service thread 1-1) WFLYJCA0001: Bound data source [java:jboss/datasources/ExampleDS]
2026-10-24 12:44:43,963 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-1) WFLYUT0006: Undertow HTTPS listener https listening on 0.0.0.0:8443
2026-10-24 12:44:43,966 INFO  [org.jboss.as.remoting] (MSC service thread 1-1) WFLYRMT0001: Listening on 0.0.0.0:4447
2026-10-24 12:44:43,966 INFO  [org.jboss.as.connector.subsystems.datasources] (MSC service thread 1-1) WFLYJCA0001: Bound data source [java:/jboss/datasources/sicow-ds]
2026-10-24 12:44:44,077 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221000: live Message Broker is starting with configuration Broker Configuration (clustered=false,journalDirectory=/opt/jboss/standalone/data/activemq/journal,bindingsDirectory=/opt/jboss/standalone/data/activemq/bindings,largeMessagesDirectory=/opt/jboss/standalone/data/activemq/largemessages,pagingDirectory=/opt/jboss/standalone/data/activemq/paging)
2026-10-24 12:44:44,157 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221006: Waiting to obtain live lock
2026-10-24 12:44:44,168 INFO  [org.jboss.ws.common.management] (MSC service thread 1-1) JBWS022052: Starting JBossWS 5.4.8.Final-redhat-00001 (Apache CXF 3.4.10.redhat-00001) 
2026-10-24 12:44:44,364 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221043: Protocol module found: [artemis-server]. Adding protocol support for: CORE
2026-10-24 12:44:44,364 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221043: Protocol module found: [artemis-hornetq-protocol]. Adding protocol support for: HORNETQ
2026-10-24 12:44:44,565 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221003: Deploying ANYCAST queue jms.queue.ExpiryQueue on address jms.queue.ExpiryQueue
2026-10-24 12:44:44,963 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221003: Deploying ANYCAST queue jms.queue.DLQ on address jms.queue.DLQ
2026-10-24 12:44:44,964 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221003: Deploying ANYCAST queue jms.queue.sipnlReq on address jms.queue.sipnlReq
2026-10-24 12:44:44,964 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221003: Deploying ANYCAST queue jms.queue.sipnlRet on address jms.queue.sipnlRet
2026-10-24 12:44:44,964 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221003: Deploying ANYCAST queue jms.queue.totemReq on address jms.queue.totemReq
2026-10-24 12:44:44,965 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221003: Deploying ANYCAST queue jms.queue.totemRet on address jms.queue.totemRet
2026-10-24 12:44:44,965 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221003: Deploying ANYCAST queue jms.queue.painelReq on address jms.queue.painelReq
2026-10-24 12:44:44,966 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221003: Deploying ANYCAST queue jms.queue.painelRet on address jms.queue.painelRet
2026-10-24 12:44:44,966 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221003: Deploying ANYCAST queue jms.queue.siicoReq on address jms.queue.siicoReq
2026-10-24 12:44:44,967 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221003: Deploying ANYCAST queue jms.queue.siicoRet on address jms.queue.siicoRet
2026-10-24 12:44:44,967 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221003: Deploying ANYCAST queue jms.queue.painelWebReq on address jms.queue.painelWebReq
2026-10-24 12:44:44,968 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221003: Deploying ANYCAST queue jms.queue.painelWebRet on address jms.queue.painelWebRet
2026-10-24 12:44:46,564 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221020: Started NIO Acceptor at 0.0.0.0:5455 for protocols [CORE,HORNETQ]
2026-10-24 12:44:46,570 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221020: Started NIO Acceptor at 0.0.0.0:5445 for protocols [CORE,HORNETQ]
2026-10-24 12:44:46,570 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221007: Server is now live
2026-10-24 12:44:46,570 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 65) AMQ221001: Apache ActiveMQ Artemis Message Broker version 2.16.0.redhat-00047 [default, nodeID=d55fd098-cfc1-11f1-b3ce-0a58190118ff] 
2026-10-24 12:44:47,471 WARN  [org.apache.activemq.artemis.jms.server] (ServerService Thread Pool -- 67) AMQ122005: Invalid "host" value "0.0.0.0" detected for "netty" connector. Switching to "sicow-conres-okd-des-31-sjr9k". If this new address is incorrect please manually configure the connector to use the proper one.
2026-10-24 12:44:47,558 INFO  [org.wildfly.extension.messaging-activemq] (ServerService Thread Pool -- 67) WFLYMSGAMQ0002: Bound messaging object to jndi name RemoteConnectionFactory
2026-10-24 12:44:47,559 INFO  [org.wildfly.extension.messaging-activemq] (ServerService Thread Pool -- 67) WFLYMSGAMQ0002: Bound messaging object to jndi name java:jboss/exported/jms/RemoteConnectionFactory
2026-10-24 12:44:47,560 INFO  [org.wildfly.extension.messaging-activemq] (ServerService Thread Pool -- 71) WFLYMSGAMQ0002: Bound messaging object to jndi name java:/ConnectionFactory
2026-10-24 12:44:47,665 INFO  [org.jboss.as.connector.deployment] (MSC service thread 1-1) WFLYJCA0007: Registered connection factory java:/JmsXA
2026-10-24 12:44:47,877 INFO  [org.apache.activemq.artemis.ra] (MSC service thread 1-1) AMQ151007: Resource adaptor started
2026-10-24 12:44:47,878 INFO  [org.jboss.as.connector.services.resourceadapters.ResourceAdapterActivatorService$ResourceAdapterActivator] (MSC service thread 1-1) IJ020002: Deployed: file://RaActivatorhornetq-ra
2026-10-24 12:44:48,267 INFO  [org.jboss.as.connector.deployment] (MSC service thread 1-1) WFLYJCA0002: Bound Jakarta Connectors ConnectionFactory [java:/JmsXA]
2026-10-24 12:44:49,473 WARN  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0119: [Enterprise Beans 3.1 spec, section 4.9.2] Session bean implementation class MUST be public, not abstract and not final - br.gov.caixa.pr.sicow.bean.SicowCrudBean won't be considered as a session bean, since it doesn't meet that requirement
2026-10-24 12:44:49,783 INFO  [org.jboss.as.jpa] (MSC service thread 1-2) WFLYJPA0002: Read persistence.xml for SicowConresPersistUnit
2026-10-24 12:44:50,064 INFO  [org.infinispan.CONTAINER] (ServerService Thread Pool -- 66) ISPN000128: Infinispan version: Infinispan 'Corona Extra' 11.0.17.Final-redhat-00001
2026-10-24 12:44:50,376 INFO  [org.infinispan.CONFIG] (MSC service thread 1-1) ISPN000152: Passivation configured without an eviction policy being selected. Only manually evicted entities will be passivated.
2026-10-24 12:44:50,377 INFO  [org.infinispan.CONFIG] (MSC service thread 1-1) ISPN000152: Passivation configured without an eviction policy being selected. Only manually evicted entities will be passivated.
2026-10-24 12:44:50,589 INFO  [org.infinispan.PERSISTENCE] (ServerService Thread Pool -- 66) ISPN000556: Starting user marshaller 'org.wildfly.clustering.infinispan.spi.marshalling.InfinispanProtoStreamMarshaller'
2026-10-24 12:44:51,276 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 66) WFLYCLINF0002: Started http-remoting-connector cache from ejb container
2026-10-24 12:44:51,594 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 66) WFLYJPA0010: Starting Persistence Unit (phase 1 of 2) Service 'sicow-conres-okd.war#SicowConresPersistUnit'
2026-10-24 12:44:51,677 INFO  [org.hibernate.jpa.internal.util.LogHelper] (ServerService Thread Pool -- 66) HHH000204: Processing PersistenceUnitInfo [
	name: SicowConresPersistUnit
	...]
2026-10-24 12:44:51,876 INFO  [org.hibernate.Version] (ServerService Thread Pool -- 66) HHH000412: Hibernate Core {5.3.29.Final-redhat-00001}
2026-10-24 12:44:51,878 INFO  [org.hibernate.cfg.Environment] (ServerService Thread Pool -- 66) HHH000206: hibernate.properties not found
2026-10-24 12:44:52,361 INFO  [org.hibernate.annotations.common.Version] (ServerService Thread Pool -- 66) HCANN000001: Hibernate Commons Annotations {5.0.5.Final-redhat-00002}
2026-10-24 12:44:52,363 INFO  [org.jboss.weld.deployer] (MSC service thread 1-2) WFLYWELD0003: Processing weld deployment sicow-conres-okd.war
2026-10-24 12:44:52,567 INFO  [org.hibernate.validator.internal.util.Version] (MSC service thread 1-2) HV000001: Hibernate Validator 6.0.23.Final-redhat-00001
2026-10-24 12:44:52,896 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'SubMotivoDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/SubMotivoDao!br.gov.caixa.pr.sicow.conres.dao.SubMotivoDao
	java:app/sicow-conres-okd/SubMotivoDao!br.gov.caixa.pr.sicow.conres.dao.SubMotivoDao
	java:module/SubMotivoDao!br.gov.caixa.pr.sicow.conres.dao.SubMotivoDao
	java:global/sicow-conres-okd/SubMotivoDao
	java:app/sicow-conres-okd/SubMotivoDao
	java:module/SubMotivoDao

2026-10-24 12:44:52,896 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'SicowConresAuditInterceptor' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/SicowConresAuditInterceptor!br.gov.caixa.pr.sicow.conres.audit.SicowConresAuditInterceptor
	java:app/sicow-conres-okd/SicowConresAuditInterceptor!br.gov.caixa.pr.sicow.conres.audit.SicowConresAuditInterceptor
	java:module/SicowConresAuditInterceptor!br.gov.caixa.pr.sicow.conres.audit.SicowConresAuditInterceptor
	java:global/sicow-conres-okd/SicowConresAuditInterceptor
	java:app/sicow-conres-okd/SicowConresAuditInterceptor
	java:module/SicowConresAuditInterceptor

2026-10-24 12:44:52,896 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ArquivoGeradoHistoricoDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/ArquivoGeradoHistoricoDao!br.gov.caixa.pr.sicow.conres.dao.ArquivoGeradoHistoricoDao
	java:app/sicow-conres-okd/ArquivoGeradoHistoricoDao!br.gov.caixa.pr.sicow.conres.dao.ArquivoGeradoHistoricoDao
	java:module/ArquivoGeradoHistoricoDao!br.gov.caixa.pr.sicow.conres.dao.ArquivoGeradoHistoricoDao
	java:global/sicow-conres-okd/ArquivoGeradoHistoricoDao
	java:app/sicow-conres-okd/ArquivoGeradoHistoricoDao
	java:module/ArquivoGeradoHistoricoDao

2026-10-24 12:44:52,896 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ArquivoRecebidoDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/ArquivoRecebidoDao!br.gov.caixa.pr.sicow.conres.dao.ArquivoRecebidoDao
	java:app/sicow-conres-okd/ArquivoRecebidoDao!br.gov.caixa.pr.sicow.conres.dao.ArquivoRecebidoDao
	java:module/ArquivoRecebidoDao!br.gov.caixa.pr.sicow.conres.dao.ArquivoRecebidoDao
	java:global/sicow-conres-okd/ArquivoRecebidoDao
	java:app/sicow-conres-okd/ArquivoRecebidoDao
	java:module/ArquivoRecebidoDao

2026-10-24 12:44:52,897 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ImportacaoConresSiricDAO' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/ImportacaoConresSiricDAO!br.gov.caixa.pr.sicow.conres.dao.ImportacaoConresSiricDAO
	java:app/sicow-conres-okd/ImportacaoConresSiricDAO!br.gov.caixa.pr.sicow.conres.dao.ImportacaoConresSiricDAO
	java:module/ImportacaoConresSiricDAO!br.gov.caixa.pr.sicow.conres.dao.ImportacaoConresSiricDAO
	java:global/sicow-conres-okd/ImportacaoConresSiricDAO
	java:app/sicow-conres-okd/ImportacaoConresSiricDAO
	java:module/ImportacaoConresSiricDAO

2026-10-24 12:44:52,897 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'OcorrenciaDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/OcorrenciaDao!br.gov.caixa.pr.sicow.conres.dao.OcorrenciaDao
	java:app/sicow-conres-okd/OcorrenciaDao!br.gov.caixa.pr.sicow.conres.dao.OcorrenciaDao
	java:module/OcorrenciaDao!br.gov.caixa.pr.sicow.conres.dao.OcorrenciaDao
	java:global/sicow-conres-okd/OcorrenciaDao
	java:app/sicow-conres-okd/OcorrenciaDao
	java:module/OcorrenciaDao

2026-10-24 12:44:52,897 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'SicowConresAuditDAO' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/SicowConresAuditDAO!br.gov.caixa.pr.sicow.conres.dao.SicowConresAuditDAO
	java:app/sicow-conres-okd/SicowConresAuditDAO!br.gov.caixa.pr.sicow.conres.dao.SicowConresAuditDAO
	java:module/SicowConresAuditDAO!br.gov.caixa.pr.sicow.conres.dao.SicowConresAuditDAO
	java:global/sicow-conres-okd/SicowConresAuditDAO
	java:app/sicow-conres-okd/SicowConresAuditDAO
	java:module/SicowConresAuditDAO

2026-10-24 12:44:52,897 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ImportacaoDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/ImportacaoDao!br.gov.caixa.pr.sicow.conres.dao.ImportacaoDao
	java:app/sicow-conres-okd/ImportacaoDao!br.gov.caixa.pr.sicow.conres.dao.ImportacaoDao
	java:module/ImportacaoDao!br.gov.caixa.pr.sicow.conres.dao.ImportacaoDao
	java:global/sicow-conres-okd/ImportacaoDao
	java:app/sicow-conres-okd/ImportacaoDao
	java:module/ImportacaoDao

2026-10-24 12:44:52,897 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'MotivoLegadoConresDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/MotivoLegadoConresDao!br.gov.caixa.pr.sicow.conres.dao.MotivoLegadoConresDao
	java:app/sicow-conres-okd/MotivoLegadoConresDao!br.gov.caixa.pr.sicow.conres.dao.MotivoLegadoConresDao
	java:module/MotivoLegadoConresDao!br.gov.caixa.pr.sicow.conres.dao.MotivoLegadoConresDao
	java:global/sicow-conres-okd/MotivoLegadoConresDao
	java:app/sicow-conres-okd/MotivoLegadoConresDao
	java:module/MotivoLegadoConresDao

2026-10-24 12:44:52,897 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'WsServicosDAO' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/WsServicosDAO!br.gov.caixa.pr.sicow.conres.dao.WsServicosDAO
	java:app/sicow-conres-okd/WsServicosDAO!br.gov.caixa.pr.sicow.conres.dao.WsServicosDAO
	java:module/WsServicosDAO!br.gov.caixa.pr.sicow.conres.dao.WsServicosDAO
	java:global/sicow-conres-okd/WsServicosDAO
	java:app/sicow-conres-okd/WsServicosDAO
	java:module/WsServicosDAO

2026-10-24 12:44:52,897 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'MotivoDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/MotivoDao!br.gov.caixa.pr.sicow.conres.dao.MotivoDao
	java:app/sicow-conres-okd/MotivoDao!br.gov.caixa.pr.sicow.conres.dao.MotivoDao
	java:module/MotivoDao!br.gov.caixa.pr.sicow.conres.dao.MotivoDao
	java:global/sicow-conres-okd/MotivoDao
	java:app/sicow-conres-okd/MotivoDao
	java:module/MotivoDao

2026-10-24 12:44:52,897 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'LogDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/LogDao!br.gov.caixa.pr.sicow.conres.dao.LogDao
	java:app/sicow-conres-okd/LogDao!br.gov.caixa.pr.sicow.conres.dao.LogDao
	java:module/LogDao!br.gov.caixa.pr.sicow.conres.dao.LogDao
	java:global/sicow-conres-okd/LogDao
	java:app/sicow-conres-okd/LogDao
	java:module/LogDao

2026-10-24 12:44:52,898 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'StatusRecebidoDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/StatusRecebidoDao!br.gov.caixa.pr.sicow.conres.dao.StatusRecebidoDao
	java:app/sicow-conres-okd/StatusRecebidoDao!br.gov.caixa.pr.sicow.conres.dao.StatusRecebidoDao
	java:module/StatusRecebidoDao!br.gov.caixa.pr.sicow.conres.dao.StatusRecebidoDao
	java:global/sicow-conres-okd/StatusRecebidoDao
	java:app/sicow-conres-okd/StatusRecebidoDao
	java:module/StatusRecebidoDao

2026-10-24 12:44:52,898 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ArquivoGeradoDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/ArquivoGeradoDao!br.gov.caixa.pr.sicow.conres.dao.ArquivoGeradoDao
	java:app/sicow-conres-okd/ArquivoGeradoDao!br.gov.caixa.pr.sicow.conres.dao.ArquivoGeradoDao
	java:module/ArquivoGeradoDao!br.gov.caixa.pr.sicow.conres.dao.ArquivoGeradoDao
	java:global/sicow-conres-okd/ArquivoGeradoDao
	java:app/sicow-conres-okd/ArquivoGeradoDao
	java:module/ArquivoGeradoDao

2026-10-24 12:44:52,898 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'EmailServiceCONRES' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/EmailServiceCONRES!br.gov.caixa.pr.sicow.conres.service.EmailServiceCONRES
	java:app/sicow-conres-okd/EmailServiceCONRES!br.gov.caixa.pr.sicow.conres.service.EmailServiceCONRES
	java:module/EmailServiceCONRES!br.gov.caixa.pr.sicow.conres.service.EmailServiceCONRES
	java:global/sicow-conres-okd/EmailServiceCONRES
	java:app/sicow-conres-okd/EmailServiceCONRES
	java:module/EmailServiceCONRES

2026-10-24 12:44:52,898 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'CONRESImportacaoArquivoJob' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/CONRESImportacaoArquivoJob!br.gov.caixa.pr.sicow.conres.service.CONRESImportacaoArquivoJob
	java:app/sicow-conres-okd/CONRESImportacaoArquivoJob!br.gov.caixa.pr.sicow.conres.service.CONRESImportacaoArquivoJob
	java:module/CONRESImportacaoArquivoJob!br.gov.caixa.pr.sicow.conres.service.CONRESImportacaoArquivoJob
	java:global/sicow-conres-okd/CONRESImportacaoArquivoJob
	java:app/sicow-conres-okd/CONRESImportacaoArquivoJob
	java:module/CONRESImportacaoArquivoJob

2026-10-24 12:44:52,898 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ListaEmailConresDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/ListaEmailConresDao!br.gov.caixa.pr.sicow.conres.dao.ListaEmailConresDao
	java:app/sicow-conres-okd/ListaEmailConresDao!br.gov.caixa.pr.sicow.conres.dao.ListaEmailConresDao
	java:module/ListaEmailConresDao!br.gov.caixa.pr.sicow.conres.dao.ListaEmailConresDao
	java:global/sicow-conres-okd/ListaEmailConresDao
	java:app/sicow-conres-okd/ListaEmailConresDao
	java:module/ListaEmailConresDao

2026-10-24 12:44:52,898 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'MotivoUnidadeDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/MotivoUnidadeDao!br.gov.caixa.pr.sicow.conres.dao.MotivoUnidadeDao
	java:app/sicow-conres-okd/MotivoUnidadeDao!br.gov.caixa.pr.sicow.conres.dao.MotivoUnidadeDao
	java:module/MotivoUnidadeDao!br.gov.caixa.pr.sicow.conres.dao.MotivoUnidadeDao
	java:global/sicow-conres-okd/MotivoUnidadeDao
	java:app/sicow-conres-okd/MotivoUnidadeDao
	java:module/MotivoUnidadeDao

2026-10-24 12:44:52,898 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'PassWordSistemaDAO' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/PassWordSistemaDAO!br.gov.caixa.pr.sicow.conres.dao.PassWordSistemaDAO
	java:app/sicow-conres-okd/PassWordSistemaDAO!br.gov.caixa.pr.sicow.conres.dao.PassWordSistemaDAO
	java:module/PassWordSistemaDAO!br.gov.caixa.pr.sicow.conres.dao.PassWordSistemaDAO
	java:global/sicow-conres-okd/PassWordSistemaDAO
	java:app/sicow-conres-okd/PassWordSistemaDAO
	java:module/PassWordSistemaDAO

2026-10-24 12:44:52,898 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'OcorrenciaImportadaDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/OcorrenciaImportadaDao!br.gov.caixa.pr.sicow.conres.dao.OcorrenciaImportadaDao
	java:app/sicow-conres-okd/OcorrenciaImportadaDao!br.gov.caixa.pr.sicow.conres.dao.OcorrenciaImportadaDao
	java:module/OcorrenciaImportadaDao!br.gov.caixa.pr.sicow.conres.dao.OcorrenciaImportadaDao
	java:global/sicow-conres-okd/OcorrenciaImportadaDao
	java:app/sicow-conres-okd/OcorrenciaImportadaDao
	java:module/OcorrenciaImportadaDao

2026-10-24 12:44:52,898 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'HistoricoOcorrenciaDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/HistoricoOcorrenciaDao!br.gov.caixa.pr.sicow.conres.dao.HistoricoOcorrenciaDao
	java:app/sicow-conres-okd/HistoricoOcorrenciaDao!br.gov.caixa.pr.sicow.conres.dao.HistoricoOcorrenciaDao
	java:module/HistoricoOcorrenciaDao!br.gov.caixa.pr.sicow.conres.dao.HistoricoOcorrenciaDao
	java:global/sicow-conres-okd/HistoricoOcorrenciaDao
	java:app/sicow-conres-okd/HistoricoOcorrenciaDao
	java:module/HistoricoOcorrenciaDao

2026-10-24 12:44:52,898 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'OcorrenciaConresWS' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:


2026-10-24 12:44:52,899 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ImportConresService' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/ImportConresService!br.gov.caixa.pr.sicow.conres.service.ImportConresService
	java:app/sicow-conres-okd/ImportConresService!br.gov.caixa.pr.sicow.conres.service.ImportConresService
	java:module/ImportConresService!br.gov.caixa.pr.sicow.conres.service.ImportConresService
	java:global/sicow-conres-okd/ImportConresService
	java:app/sicow-conres-okd/ImportConresService
	java:module/ImportConresService

2026-10-24 12:44:52,899 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'TipoExclusaoOcorrenciaDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/TipoExclusaoOcorrenciaDao!br.gov.caixa.pr.sicow.conres.dao.TipoExclusaoOcorrenciaDao
	java:app/sicow-conres-okd/TipoExclusaoOcorrenciaDao!br.gov.caixa.pr.sicow.conres.dao.TipoExclusaoOcorrenciaDao
	java:module/TipoExclusaoOcorrenciaDao!br.gov.caixa.pr.sicow.conres.dao.TipoExclusaoOcorrenciaDao
	java:global/sicow-conres-okd/TipoExclusaoOcorrenciaDao
	java:app/sicow-conres-okd/TipoExclusaoOcorrenciaDao
	java:module/TipoExclusaoOcorrenciaDao

2026-10-24 12:44:52,899 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'UnidadeSiicoCaixaDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/UnidadeSiicoCaixaDao!br.gov.caixa.pr.sicow.siico.dao.UnidadeSiicoCaixaDao
	java:app/sicow-conres-okd/UnidadeSiicoCaixaDao!br.gov.caixa.pr.sicow.siico.dao.UnidadeSiicoCaixaDao
	java:module/UnidadeSiicoCaixaDao!br.gov.caixa.pr.sicow.siico.dao.UnidadeSiicoCaixaDao
	java:global/sicow-conres-okd/UnidadeSiicoCaixaDao
	java:app/sicow-conres-okd/UnidadeSiicoCaixaDao
	java:module/UnidadeSiicoCaixaDao

2026-10-24 12:44:52,899 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'WsServicosSistemaDAO' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/WsServicosSistemaDAO!br.gov.caixa.pr.sicow.conres.dao.WsServicosSistemaDAO
	java:app/sicow-conres-okd/WsServicosSistemaDAO!br.gov.caixa.pr.sicow.conres.dao.WsServicosSistemaDAO
	java:module/WsServicosSistemaDAO!br.gov.caixa.pr.sicow.conres.dao.WsServicosSistemaDAO
	java:global/sicow-conres-okd/WsServicosSistemaDAO
	java:app/sicow-conres-okd/WsServicosSistemaDAO
	java:module/WsServicosSistemaDAO

2026-10-24 12:44:52,899 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ServicosWebService' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/ServicosWebService!br.gov.caixa.pr.sicow.service.ws.InterfaceServicosWebService
	java:app/sicow-conres-okd/ServicosWebService!br.gov.caixa.pr.sicow.service.ws.InterfaceServicosWebService
	java:module/ServicosWebService!br.gov.caixa.pr.sicow.service.ws.InterfaceServicosWebService
	java:global/sicow-conres-okd/ServicosWebService
	java:app/sicow-conres-okd/ServicosWebService
	java:module/ServicosWebService

2026-10-24 12:44:52,899 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'EmpregadoSiicoDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/EmpregadoSiicoDao!br.gov.caixa.pr.sicow.siico.dao.EmpregadoSiicoDao
	java:app/sicow-conres-okd/EmpregadoSiicoDao!br.gov.caixa.pr.sicow.siico.dao.EmpregadoSiicoDao
	java:module/EmpregadoSiicoDao!br.gov.caixa.pr.sicow.siico.dao.EmpregadoSiicoDao
	java:global/sicow-conres-okd/EmpregadoSiicoDao
	java:app/sicow-conres-okd/EmpregadoSiicoDao
	java:module/EmpregadoSiicoDao

2026-10-24 12:44:52,899 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'CONRESImportacaoArquivosConresService' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/CONRESImportacaoArquivosConresService!br.gov.caixa.pr.sicow.conres.service.CONRESImportacaoArquivosConresService
	java:app/sicow-conres-okd/CONRESImportacaoArquivosConresService!br.gov.caixa.pr.sicow.conres.service.CONRESImportacaoArquivosConresService
	java:module/CONRESImportacaoArquivosConresService!br.gov.caixa.pr.sicow.conres.service.CONRESImportacaoArquivosConresService
	java:global/sicow-conres-okd/CONRESImportacaoArquivosConresService
	java:app/sicow-conres-okd/CONRESImportacaoArquivosConresService
	java:module/CONRESImportacaoArquivosConresService

2026-10-24 12:44:52,899 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'SistemaWSDAO' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/SistemaWSDAO!br.gov.caixa.pr.sicow.conres.dao.SistemaWSDAO
	java:app/sicow-conres-okd/SistemaWSDAO!br.gov.caixa.pr.sicow.conres.dao.SistemaWSDAO
	java:module/SistemaWSDAO!br.gov.caixa.pr.sicow.conres.dao.SistemaWSDAO
	java:global/sicow-conres-okd/SistemaWSDAO
	java:app/sicow-conres-okd/SistemaWSDAO
	java:module/SistemaWSDAO

2026-10-24 12:44:52,899 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'SubMotivoUnidadeDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/SubMotivoUnidadeDao!br.gov.caixa.pr.sicow.conres.dao.SubMotivoUnidadeDao
	java:app/sicow-conres-okd/SubMotivoUnidadeDao!br.gov.caixa.pr.sicow.conres.dao.SubMotivoUnidadeDao
	java:module/SubMotivoUnidadeDao!br.gov.caixa.pr.sicow.conres.dao.SubMotivoUnidadeDao
	java:global/sicow-conres-okd/SubMotivoUnidadeDao
	java:app/sicow-conres-okd/SubMotivoUnidadeDao
	java:module/SubMotivoUnidadeDao

2026-10-24 12:44:52,899 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ImportacaoArquivoConresDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/ImportacaoArquivoConresDao!br.gov.caixa.pr.sicow.conres.dao.ImportacaoArquivoConresDao
	java:app/sicow-conres-okd/ImportacaoArquivoConresDao!br.gov.caixa.pr.sicow.conres.dao.ImportacaoArquivoConresDao
	java:module/ImportacaoArquivoConresDao!br.gov.caixa.pr.sicow.conres.dao.ImportacaoArquivoConresDao
	java:global/sicow-conres-okd/ImportacaoArquivoConresDao
	java:app/sicow-conres-okd/ImportacaoArquivoConresDao
	java:module/ImportacaoArquivoConresDao

2026-10-24 12:44:52,900 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'LogBean' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/LogBean!br.gov.caixa.pr.sicow.conres.bean.LogBean
	java:app/sicow-conres-okd/LogBean!br.gov.caixa.pr.sicow.conres.bean.LogBean
	java:module/LogBean!br.gov.caixa.pr.sicow.conres.bean.LogBean
	java:global/sicow-conres-okd/LogBean
	java:app/sicow-conres-okd/LogBean
	java:module/LogBean

2026-10-24 12:44:52,900 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'CONRESFinalizaOcorrenciaService' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/CONRESFinalizaOcorrenciaService!br.gov.caixa.pr.sicow.conres.service.CONRESFinalizaOcorrenciaService
	java:app/sicow-conres-okd/CONRESFinalizaOcorrenciaService!br.gov.caixa.pr.sicow.conres.service.CONRESFinalizaOcorrenciaService
	java:module/CONRESFinalizaOcorrenciaService!br.gov.caixa.pr.sicow.conres.service.CONRESFinalizaOcorrenciaService
	java:global/sicow-conres-okd/CONRESFinalizaOcorrenciaService
	java:app/sicow-conres-okd/CONRESFinalizaOcorrenciaService
	java:module/CONRESFinalizaOcorrenciaService

2026-10-24 12:44:52,900 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ImportacaoOcorrenciaSiricService' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/ImportacaoOcorrenciaSiricService!br.gov.caixa.pr.sicow.conres.service.ImportacaoOcorrenciaSiricService
	java:app/sicow-conres-okd/ImportacaoOcorrenciaSiricService!br.gov.caixa.pr.sicow.conres.service.ImportacaoOcorrenciaSiricService
	java:module/ImportacaoOcorrenciaSiricService!br.gov.caixa.pr.sicow.conres.service.ImportacaoOcorrenciaSiricService
	java:global/sicow-conres-okd/ImportacaoOcorrenciaSiricService
	java:app/sicow-conres-okd/ImportacaoOcorrenciaSiricService
	java:module/ImportacaoOcorrenciaSiricService

2026-10-24 12:44:52,900 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'StatusArquivoGeradoDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/StatusArquivoGeradoDao!br.gov.caixa.pr.sicow.conres.dao.StatusArquivoGeradoDao
	java:app/sicow-conres-okd/StatusArquivoGeradoDao!br.gov.caixa.pr.sicow.conres.dao.StatusArquivoGeradoDao
	java:module/StatusArquivoGeradoDao!br.gov.caixa.pr.sicow.conres.dao.StatusArquivoGeradoDao
	java:global/sicow-conres-okd/StatusArquivoGeradoDao
	java:app/sicow-conres-okd/StatusArquivoGeradoDao
	java:module/StatusArquivoGeradoDao

2026-10-24 12:44:52,957 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'AlertaImportacaoArquivoConresDao' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/AlertaImportacaoArquivoConresDao!br.gov.caixa.pr.sicow.conres.dao.AlertaImportacaoArquivoConresDao
	java:app/sicow-conres-okd/AlertaImportacaoArquivoConresDao!br.gov.caixa.pr.sicow.conres.dao.AlertaImportacaoArquivoConresDao
	java:module/AlertaImportacaoArquivoConresDao!br.gov.caixa.pr.sicow.conres.dao.AlertaImportacaoArquivoConresDao
	java:global/sicow-conres-okd/AlertaImportacaoArquivoConresDao
	java:app/sicow-conres-okd/AlertaImportacaoArquivoConresDao
	java:module/AlertaImportacaoArquivoConresDao

2026-10-24 12:44:52,957 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'EmailExpurgoConres' in deployment unit 'deployment "sicow-conres-okd.war"' are as follows:

	java:global/sicow-conres-okd/EmailExpurgoConres!br.gov.caixa.pr.sicow.conres.service.EmailExpurgoConres
	java:app/sicow-conres-okd/EmailExpurgoConres!br.gov.caixa.pr.sicow.conres.service.EmailExpurgoConres
	java:module/EmailExpurgoConres!br.gov.caixa.pr.sicow.conres.service.EmailExpurgoConres
	java:global/sicow-conres-okd/EmailExpurgoConres
	java:app/sicow-conres-okd/EmailExpurgoConres
	java:module/EmailExpurgoConres

2026-10-24 12:44:53,868 WARN  [org.jboss.as.ejb3] (MSC service thread 1-2) WFLYEJB0131: Jakarta Enterprise Beans br.gov.caixa.pr.sicow.conres.service.CONRESImportacaoArquivosConresService should not have a final or static method (getInputStreamSize)
2026-10-24 12:44:54,494 INFO  [org.jboss.weld.Version] (MSC service thread 1-2) WELD-000900: 3.1.6 (redhat)
2026-10-24 12:44:54,590 INFO  [org.jboss.ws.cxf.metadata] (MSC service thread 1-2) JBWS024061: Adding service endpoint metadata: id=OcorrenciaConresWS
 address=http://25.1.24.255:8080/sicow-conres/OcorrenciaConresWS/SicowconresWS
 implementor=br.gov.caixa.pr.sicow.conres.ws.OcorrenciaConresWS
 serviceName={http://ws.conres.sicow.pr.caixa.gov.br/}OcorrenciaConresWS
 portName={http://ws.conres.sicow.pr.caixa.gov.br/}SicowconresWSPort
 annotationWsdlLocation=null
 wsdlLocationOverride=null
 mtomEnabled=false
2026-10-24 12:44:55,470 INFO  [org.apache.cxf.wsdl.service.factory.ReflectionServiceFactoryBean] (MSC service thread 1-2) Creating Service {http://ws.conres.sicow.pr.caixa.gov.br/}OcorrenciaConresWS from class br.gov.caixa.pr.sicow.conres.ws.OcorrenciaConresWS
2026-10-24 12:44:56,263 INFO  [org.apache.cxf.endpoint.ServerImpl] (MSC service thread 1-2) Setting the server's publish address to be http://25.1.24.255:8080/sicow-conres/OcorrenciaConresWS/SicowconresWS
2026-10-24 12:44:56,371 INFO  [org.jboss.ws.cxf.deployment] (MSC service thread 1-2) JBWS024074: WSDL published to: file:/opt/jboss-eap-7.4/standalone/data/wsdl/sicow-conres-okd.war/OcorrenciaConresWS.wsdl
2026-10-24 12:44:56,483 INFO  [org.jboss.as.webservices] (MSC service thread 1-1) WFLYWS0003: Starting service jboss.ws.endpoint."sicow-conres-okd.war".OcorrenciaConresWS
2026-10-24 12:44:56,764 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 66) WFLYJPA0010: Starting Persistence Unit (phase 2 of 2) Service 'sicow-conres-okd.war#SicowConresPersistUnit'
2026-10-24 12:44:56,793 WARN  [org.jboss.jca.core.connectionmanager.pool.strategy.OnePool] (ServerService Thread Pool -- 66) IJ000604: Throwable while attempting to get a new connection: null: javax.resource.ResourceException: IJ031084: Unable to create connection
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.createLocalManagedConnection(LocalManagedConnectionFactory.java:364)
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.getLocalManagedConnection(LocalManagedConnectionFactory.java:371)
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.createManagedConnection(LocalManagedConnectionFactory.java:287)
	at org.jboss.jca.core.connectionmanager.pool.mcp.SemaphoreConcurrentLinkedDequeManagedConnectionPool.createConnectionEventListener(SemaphoreConcurrentLinkedDequeManagedConnectionPool.java:1328)
	at org.jboss.jca.core.connectionmanager.pool.mcp.SemaphoreConcurrentLinkedDequeManagedConnectionPool.getConnection(SemaphoreConcurrentLinkedDequeManagedConnectionPool.java:505)
	at org.jboss.jca.core.connectionmanager.pool.AbstractPool.getSimpleConnection(AbstractPool.java:640)
	at org.jboss.jca.core.connectionmanager.pool.AbstractPool.getConnection(AbstractPool.java:605)
	at org.jboss.jca.core.connectionmanager.AbstractConnectionManager.getManagedConnection(AbstractConnectionManager.java:624)
	at org.jboss.jca.core.connectionmanager.tx.TxConnectionManagerImpl.getManagedConnection(TxConnectionManagerImpl.java:440)
	at org.jboss.jca.core.connectionmanager.AbstractConnectionManager.allocateConnection(AbstractConnectionManager.java:789)
	at org.jboss.jca.adapters.jdbc.WrapperDataSource.getConnection(WrapperDataSource.java:150)
	at org.jboss.as.connector.subsystems.datasources.WildFlyDataSource.getConnection(WildFlyDataSource.java:64)
	at org.hibernate.engine.jdbc.connections.internal.DatasourceConnectionProviderImpl.getConnection(DatasourceConnectionProviderImpl.java:122)
	at org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator$ConnectionProviderJdbcConnectionAccess.obtainConnection(JdbcEnvironmentInitiator.java:180)
	at org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator.initiateService(JdbcEnvironmentInitiator.java:68)
	at org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator.initiateService(JdbcEnvironmentInitiator.java:35)
	at org.hibernate.boot.registry.internal.StandardServiceRegistryImpl.initiateService(StandardServiceRegistryImpl.java:94)
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.createService(AbstractServiceRegistryImpl.java:263)
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.initializeService(AbstractServiceRegistryImpl.java:237)
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.getService(AbstractServiceRegistryImpl.java:214)
	at org.hibernate.id.factory.internal.DefaultIdentifierGeneratorFactory.injectServices(DefaultIdentifierGeneratorFactory.java:152)
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.injectDependencies(AbstractServiceRegistryImpl.java:286)
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.initializeService(AbstractServiceRegistryImpl.java:243)
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.getService(AbstractServiceRegistryImpl.java:214)
	at org.hibernate.boot.internal.InFlightMetadataCollectorImpl.<init>(InFlightMetadataCollectorImpl.java:179)
	at org.hibernate.boot.model.process.spi.MetadataBuildingProcess.complete(MetadataBuildingProcess.java:119)
	at org.hibernate.jpa.boot.internal.EntityManagerFactoryBuilderImpl.metadata(EntityManagerFactoryBuilderImpl.java:1215)
	at org.hibernate.jpa.boot.internal.EntityManagerFactoryBuilderImpl.build(EntityManagerFactoryBuilderImpl.java:1246)
	at org.jboss.as.jpa.hibernate5.TwoPhaseBootstrapImpl.build(TwoPhaseBootstrapImpl.java:44)
	at org.jboss.as.jpa.service.PersistenceUnitServiceImpl$1$1.run(PersistenceUnitServiceImpl.java:170)
	at org.jboss.as.jpa.service.PersistenceUnitServiceImpl$1$1.run(PersistenceUnitServiceImpl.java:128)
	at java.security.AccessController.doPrivileged(Native Method)
	at org.wildfly.security.manager.WildFlySecurityManager.doChecked(WildFlySecurityManager.java:664)
	at org.jboss.as.jpa.service.PersistenceUnitServiceImpl$1.run(PersistenceUnitServiceImpl.java:213)
	at org.jboss.threads.ContextClassLoaderSavingRunnable.run(ContextClassLoaderSavingRunnable.java:35)
	at org.jboss.threads.EnhancedQueueExecutor.safeRun(EnhancedQueueExecutor.java:1990)
	at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.doRunTask(EnhancedQueueExecutor.java:1486)
	at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.run(EnhancedQueueExecutor.java:1377)
	at java.lang.Thread.run(Thread.java:750)
	at org.jboss.threads.JBossThread.run(JBossThread.java:513)
Caused by: org.postgresql.util.PSQLException: FATAL: password authentication failed for user "scowdb01"
	at org.postgresql.core.v3.ConnectionFactoryImpl.doAuthentication(ConnectionFactoryImpl.java:525)
	at org.postgresql.core.v3.ConnectionFactoryImpl.tryConnect(ConnectionFactoryImpl.java:146)
	at org.postgresql.core.v3.ConnectionFactoryImpl.openConnectionImpl(ConnectionFactoryImpl.java:197)
	at org.postgresql.core.ConnectionFactory.openConnection(ConnectionFactory.java:49)
	at org.postgresql.jdbc.PgConnection.<init>(PgConnection.java:217)
	at org.postgresql.Driver.makeConnection(Driver.java:458)
	at org.postgresql.Driver.connect(Driver.java:260)
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.createLocalManagedConnection(LocalManagedConnectionFactory.java:335)
	... 39 more

2026-10-24 12:44:56,795 WARN  [org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator] (ServerService Thread Pool -- 66) HHH000342: Could not obtain connection to query metadata : javax.resource.ResourceException: IJ000453: Unable to get managed connection for java:/jboss/datasources/sicow-ds
2026-10-24 12:44:56,805 INFO  [org.hibernate.dialect.Dialect] (ServerService Thread Pool -- 66) HHH000400: Using dialect: org.hibernate.dialect.PostgreSQLDialect
2026-10-24 12:44:56,819 INFO  [org.hibernate.engine.jdbc.env.internal.LobCreatorBuilderImpl] (ServerService Thread Pool -- 66) HHH000422: Disabling contextual LOB creation as connection was null
2026-10-24 12:44:56,823 INFO  [org.hibernate.type.BasicTypeRegistry] (ServerService Thread Pool -- 66) HHH000270: Type registration [java.util.UUID] overrides previous : org.hibernate.type.UUIDBinaryType@38fa8c9
2026-10-24 12:44:56,828 INFO  [org.hibernate.envers.boot.internal.EnversServiceImpl] (ServerService Thread Pool -- 66) Envers integration enabled? : true
2026-10-24 12:44:57,258 WARN  [org.hibernate.orm.deprecation] (ServerService Thread Pool -- 66) HHH90000021: Encountered deprecated setting [hibernate.ejb.interceptor], use [hibernate.session_factory.interceptor] instead
2026-10-24 12:44:59,191 WARN  [org.jboss.weld.Bootstrap] (MSC service thread 1-1) WELD-000146: BeforeBeanDiscovery.addAnnotatedType(AnnotatedType<?>) used for class com.sun.faces.flow.FlowDiscoveryCDIHelper is deprecated from CDI 1.1!
2026-10-24 12:45:01,173 INFO  [javax.enterprise.resource.webcontainer.jsf.config] (ServerService Thread Pool -- 83) Initializing Mojarra 2.3.14.SP06 for context '/sicow-conres'
2026-10-24 12:45:03,802 INFO  [org.primefaces.webapp.PostConstructApplicationEventListener] (ServerService Thread Pool -- 83) Running on PrimeFaces 3.5
2026-10-24 12:45:03,983 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 83) WFLYUT0021: Registered web context: '/sicow-conres' for server 'default-server'
2026-10-24 12:45:03,997 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 29) WFLYSRV0010: Deployed "sicow-conres-okd.war" (runtime-name : "sicow-conres-okd.war")
2026-10-24 12:45:03,997 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 29) WFLYSRV0010: Deployed "applicationinsights-agent-3.7.1.jar" (runtime-name : "applicationinsights-agent-3.7.1.jar")
2026-10-24 12:45:04,175 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0212: Resuming server
2026-10-24 12:45:04,178 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0025: JBoss EAP 7.4.11.GA (WildFly Core 15.0.26.Final-redhat-00001) started in 42489ms - Started 1448 of 1621 services (369 services are lazy, passive or on-demand)
2026-10-24 12:45:04,180 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0060: Http management interface listening on http://0.0.0.0:9990/management
2026-10-24 12:45:04,180 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0051: Admin console listening on http://0.0.0.0:9990
2026-10-24 12:46:50,386 WARN  [org.jboss.as.domain.management.security] (default I/O-2) WFLYDM0113: Generated self signed certificate at /opt/jboss/standalone/configuration/application.keystore. Please note that self signed certificates are not secure, and should only be used for testing purposes. Do not use this self signed certificate in production.
SHA-1 fingerprint of the generated key is 0d:e6:4a:d8:97:dd:d4:20:88:87:be:0e:3b:73:eb:55:db:0a:b4:5d
SHA-256 fingerprint of the generated key is 0a:cf:9e:6a:ac:ff:d6:be:e0:44:3f:b3:ec:a6:b6:1c:0d:83:0c:89:a6:f3:f0:1e:cd:72:fe:99:35:c5:c9:a1
2026-10-24 12:46:53,078 INFO  [br.gov.caixa.pr.sicow.conres.filter.SicowIECompatibleFixFilter] (default task-1) SicowIECompatibleFixFilter - init - @Override
2026-10-24 12:46:53,193 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] siusrEndPoint http://hmp.autentica.proinfo.caixa/siusr-service/SiusrService/SiusrWS.
2026-10-24 12:46:53,194 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] sgSistema SICOW.
2026-10-24 12:46:53,194 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] secretKey null.
2026-10-24 12:46:53,194 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] cpf false.
2026-10-24 12:46:53,194 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] autenticaEndPoint http://hmp.autentica.proinfo.caixa/siusr-service/AutenticaService/AutenticaWS.
2026-10-24 12:46:53,518 INFO  [org.apache.cxf.wsdl.service.factory.ReflectionServiceFactoryBean] (default task-1) Creating Service {http://bean.siusr.caixa.gov.br/}SiusrService from WSDL: http://hmp.autentica.proinfo.caixa/siusr-service/SiusrService/SiusrWS?wsdl
2026-10-24 12:46:55,840 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaUser "CaixaUser [nuMatricula=585600, deMatricula=p585600, nuCpf=1599531119, deCpf=015.995.311-19, noUsuario=JESSE MOUTA PEREIRA BATISTA, coUnidadeFsc=7366, coUnidadeAdm=7366, sgUf=DF, coMuncipioIbge=10, dhUltimoAcesso=, roles=[CaixaRole [noFuncionalidade=consultar_log, noAcao=null, tipoAbrangencia=null, abrangencia=null, nuProcesso=null], CaixaRole [noFuncionalidade=consultar_log, noAcao=listar, tipoAbrangencia=IRRESTRITA, abrangencia=null, nuProcesso=null], CaixaRole [noFuncionalidade=importacao_ocorrencia, noAcao=null, tipoAbrangencia=null, abrangencia=null, nuProcesso=null], CaixaRole [noFuncionalidade=importacao_ocorrencia, noAcao=incluir, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null], CaixaRole [noFuncionalidade=mantem_motivo, noAcao=null, tipoAbrangencia=null, abrangencia=null, nuProcesso=null], CaixaRole [noFuncionalidade=mantem_motivo, noAcao=consultar, tipoAbrangencia=IRRESTRITA, abrangencia=null, nuProcesso=null], CaixaRole [noFuncionalidade=mantem_motivo, noAcao=listar, tipoAbrangencia=IRRESTRITA, abrangencia=null, nuProcesso=null], CaixaRole [noFuncionalidade=mantem_ocorrencia, noAcao=null, tipoAbrangencia=null, abrangencia=null, nuProcesso=null], CaixaRole [noFuncionalidade=mantem_ocorrencia, noAcao=alterar, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null], CaixaRole [noFuncionalidade=mantem_ocorrencia, noAcao=consultar, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_TODAS, nuProcesso=null], CaixaRole [noFuncionalidade=mantem_ocorrencia, noAcao=excluidas, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null], CaixaRole [noFuncionalidade=mantem_ocorrencia, noAcao=excluir, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null], CaixaRole [noFuncionalidade=mantem_ocorrencia, noAcao=incluir, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null], CaixaRole [noFuncionalidade=mantem_ocorrencia, noAcao=listar, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_TODAS, nuProcesso=null], CaixaRole [noFuncionalidade=relatorio_ocorrencia, noAcao=null, tipoAbrangencia=null, abrangencia=null, nuProcesso=null], CaixaRole [noFuncionalidade=relatorio_ocorrencia, noAcao=consultar, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null], CaixaRole [noFuncionalidade=relatorio_ocorrencia, noAcao=excluidas, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null], CaixaRole [noFuncionalidade=relatorio_ocorrencia, noAcao=listar, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null], CaixaRole [noFuncionalidade=relatorio_ocorrencia, noAcao=todos_motivos, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null]], perfils=[CaixaPerfil [noPerfil=UNIDADES, dePerfil=UNIDADES EXECUTORAS, icAutomatico=Sim, ixPrioridade=3, lotacao=ADMINISTRATIVA]], selecionarPerfis=false]".
2026-10-24 12:46:55,841 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=consultar_log, noAcao=null, tipoAbrangencia=null, abrangencia=null, nuProcesso=null]".
2026-10-24 12:46:55,841 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=consultar_log, noAcao=listar, tipoAbrangencia=IRRESTRITA, abrangencia=null, nuProcesso=null]".
2026-10-24 12:46:55,841 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=importacao_ocorrencia, noAcao=null, tipoAbrangencia=null, abrangencia=null, nuProcesso=null]".
2026-10-24 12:46:55,841 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=importacao_ocorrencia, noAcao=incluir, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null]".
2026-10-24 12:46:55,841 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=mantem_motivo, noAcao=null, tipoAbrangencia=null, abrangencia=null, nuProcesso=null]".
2026-10-24 12:46:55,841 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=mantem_motivo, noAcao=consultar, tipoAbrangencia=IRRESTRITA, abrangencia=null, nuProcesso=null]".
2026-10-24 12:46:55,841 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=mantem_motivo, noAcao=listar, tipoAbrangencia=IRRESTRITA, abrangencia=null, nuProcesso=null]".
2026-10-24 12:46:55,841 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=mantem_ocorrencia, noAcao=null, tipoAbrangencia=null, abrangencia=null, nuProcesso=null]".
2026-10-24 12:46:55,841 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=mantem_ocorrencia, noAcao=alterar, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null]".
2026-10-24 12:46:55,841 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=mantem_ocorrencia, noAcao=consultar, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_TODAS, nuProcesso=null]".
2026-10-24 12:46:55,842 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=mantem_ocorrencia, noAcao=excluidas, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null]".
2026-10-24 12:46:55,842 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=mantem_ocorrencia, noAcao=excluir, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null]".
2026-10-24 12:46:55,842 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=mantem_ocorrencia, noAcao=incluir, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null]".
2026-10-24 12:46:55,842 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=mantem_ocorrencia, noAcao=listar, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_TODAS, nuProcesso=null]".
2026-10-24 12:46:55,842 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=relatorio_ocorrencia, noAcao=null, tipoAbrangencia=null, abrangencia=null, nuProcesso=null]".
2026-10-24 12:46:55,842 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=relatorio_ocorrencia, noAcao=consultar, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null]".
2026-10-24 12:46:55,842 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=relatorio_ocorrencia, noAcao=excluidas, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null]".
2026-10-24 12:46:55,842 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=relatorio_ocorrencia, noAcao=listar, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null]".
2026-10-24 12:46:55,842 INFO  [CaixaLoginModule] (default task-1) [CaixaLoginModule] Adicionado CaixaRole "CaixaRole [noFuncionalidade=relatorio_ocorrencia, noAcao=todos_motivos, tipoAbrangencia=RESTRITA_UNIDADES, abrangencia=UNIDADES_UNIDADE, nuProcesso=null]".
2026-10-24 12:46:56,111 INFO  [br.gov.caixa.pr.sicow.portal.login.phaseListener.SicowLoginHttpsPhaseListener] (default task-1) false
2026-10-24 12:46:56,197 INFO  [br.gov.caixa.pr.sicow.portal.login.phaseListener.SicowLoginHttpsPhaseListener] (default task-1) false
2026-10-24 12:46:57,064 INFO  [org.hibernate.hql.internal.QueryTranslatorFactoryInitiator] (default task-1) HHH000397: Using ASTQueryTranslatorFactory
2026-10-24 12:46:57,214 WARN  [org.jboss.jca.core.connectionmanager.pool.strategy.OnePool] (default task-1) IJ000604: Throwable while attempting to get a new connection: null: javax.resource.ResourceException: IJ031084: Unable to create connection
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.createLocalManagedConnection(LocalManagedConnectionFactory.java:364)
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.getLocalManagedConnection(LocalManagedConnectionFactory.java:371)
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.createManagedConnection(LocalManagedConnectionFactory.java:287)
	at org.jboss.jca.core.connectionmanager.pool.mcp.SemaphoreConcurrentLinkedDequeManagedConnectionPool.createConnectionEventListener(SemaphoreConcurrentLinkedDequeManagedConnectionPool.java:1328)
	at org.jboss.jca.core.connectionmanager.pool.mcp.SemaphoreConcurrentLinkedDequeManagedConnectionPool.getConnection(SemaphoreConcurrentLinkedDequeManagedConnectionPool.java:505)
	at org.jboss.jca.core.connectionmanager.pool.AbstractPool.getTransactionNewConnection(AbstractPool.java:722)
	at org.jboss.jca.core.connectionmanager.pool.AbstractPool.getConnection(AbstractPool.java:618)
	at org.jboss.jca.core.connectionmanager.AbstractConnectionManager.getManagedConnection(AbstractConnectionManager.java:624)
	at org.jboss.jca.core.connectionmanager.tx.TxConnectionManagerImpl.getManagedConnection(TxConnectionManagerImpl.java:440)
	at org.jboss.jca.core.connectionmanager.AbstractConnectionManager.allocateConnection(AbstractConnectionManager.java:789)
	at org.jboss.jca.adapters.jdbc.WrapperDataSource.getConnection(WrapperDataSource.java:150)
	at org.jboss.as.connector.subsystems.datasources.WildFlyDataSource.getConnection(WildFlyDataSource.java:64)
	at org.hibernate.engine.jdbc.connections.internal.DatasourceConnectionProviderImpl.getConnection(DatasourceConnectionProviderImpl.java:122)
	at org.hibernate.internal.NonContextualJdbcConnectionAccess.obtainConnection(NonContextualJdbcConnectionAccess.java:35)
	at org.hibernate.resource.jdbc.internal.LogicalConnectionManagedImpl.acquireConnectionIfNeeded(LogicalConnectionManagedImpl.java:106)
	at org.hibernate.resource.jdbc.internal.LogicalConnectionManagedImpl.getPhysicalConnection(LogicalConnectionManagedImpl.java:136)
	at org.hibernate.engine.jdbc.internal.StatementPreparerImpl.connection(StatementPreparerImpl.java:50)
	at org.hibernate.engine.jdbc.internal.StatementPreparerImpl$5.doPrepare(StatementPreparerImpl.java:149)
	at org.hibernate.engine.jdbc.internal.StatementPreparerImpl$StatementPreparationTemplate.prepareStatement(StatementPreparerImpl.java:176)
	at org.hibernate.engine.jdbc.internal.StatementPreparerImpl.prepareQueryStatement(StatementPreparerImpl.java:151)
	at org.hibernate.loader.Loader.prepareQueryStatement(Loader.java:2082)
	at org.hibernate.loader.Loader.executeQueryStatement(Loader.java:2012)
	at org.hibernate.loader.Loader.executeQueryStatement(Loader.java:1990)
	at org.hibernate.loader.Loader.doQuery(Loader.java:949)
	at org.hibernate.loader.Loader.doQueryAndInitializeNonLazyCollections(Loader.java:351)
	at org.hibernate.loader.Loader.doList(Loader.java:2787)
	at org.hibernate.loader.Loader.doList(Loader.java:2770)
	at org.hibernate.loader.Loader.listIgnoreQueryCache(Loader.java:2604)
	at org.hibernate.loader.Loader.list(Loader.java:2599)
	at org.hibernate.loader.hql.QueryLoader.list(QueryLoader.java:505)
	at org.hibernate.hql.internal.ast.QueryTranslatorImpl.list(QueryTranslatorImpl.java:395)
	at org.hibernate.engine.query.spi.HQLQueryPlan.performList(HQLQueryPlan.java:220)
	at org.hibernate.internal.SessionImpl.list(SessionImpl.java:1526)
	at org.hibernate.query.internal.AbstractProducedQuery.doList(AbstractProducedQuery.java:1598)
	at org.hibernate.query.internal.AbstractProducedQuery.list(AbstractProducedQuery.java:1566)
	at org.hibernate.query.Query.getResultList(Query.java:132)
	at br.gov.caixa.pr.sicow.conres.dao.AlertaImportacaoArquivoConresDao.listAll(AlertaImportacaoArquivoConresDao.java:77)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:498)
	at org.jboss.as.ee.component.ManagedReferenceMethodInterceptor.processInvocation(ManagedReferenceMethodInterceptor.java:52)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.InterceptorContext$Invocation.proceed(InterceptorContext.java:509)
	at org.jboss.as.weld.interceptors.Jsr299BindingsInterceptor.delegateInterception(Jsr299BindingsInterceptor.java:79)
	at org.jboss.as.weld.interceptors.Jsr299BindingsInterceptor.doMethodInterception(Jsr299BindingsInterceptor.java:89)
	at org.jboss.as.weld.interceptors.Jsr299BindingsInterceptor.processInvocation(Jsr299BindingsInterceptor.java:102)
	at org.jboss.as.ee.component.interceptors.UserInterceptorFactory$1.processInvocation(UserInterceptorFactory.java:63)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.component.invocationmetrics.ExecutionTimeInterceptor.processInvocation(ExecutionTimeInterceptor.java:43)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.jpa.interceptor.SBInvocationInterceptor.processInvocation(SBInvocationInterceptor.java:47)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ee.concurrent.ConcurrentContextInterceptor.processInvocation(ConcurrentContextInterceptor.java:45)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.InitialInterceptor.processInvocation(InitialInterceptor.java:40)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.ChainedInterceptor.processInvocation(ChainedInterceptor.java:53)
	at org.jboss.as.ee.component.interceptors.ComponentDispatcherInterceptor.processInvocation(ComponentDispatcherInterceptor.java:52)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.component.pool.PooledInstanceInterceptor.processInvocation(PooledInstanceInterceptor.java:51)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.component.interceptors.AdditionalSetupInterceptor.processInvocation(AdditionalSetupInterceptor.java:54)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.tx.CMTTxInterceptor.invokeInOurTx(CMTTxInterceptor.java:254)
	at org.jboss.as.ejb3.tx.CMTTxInterceptor.required(CMTTxInterceptor.java:390)
	at org.jboss.as.ejb3.tx.CMTTxInterceptor.processInvocation(CMTTxInterceptor.java:160)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.InterceptorContext$Invocation.proceed(InterceptorContext.java:509)
	at org.jboss.weld.module.ejb.AbstractEJBRequestScopeActivationInterceptor.aroundInvoke(AbstractEJBRequestScopeActivationInterceptor.java:72)
	at org.jboss.as.weld.ejb.EjbRequestScopeActivationInterceptor.processInvocation(EjbRequestScopeActivationInterceptor.java:89)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.component.interceptors.CurrentInvocationContextInterceptor.processInvocation(CurrentInvocationContextInterceptor.java:41)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.component.invocationmetrics.WaitTimeInterceptor.processInvocation(WaitTimeInterceptor.java:47)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.security.SecurityContextInterceptor.processInvocation(SecurityContextInterceptor.java:100)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.deployment.processors.StartupAwaitInterceptor.processInvocation(StartupAwaitInterceptor.java:22)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.component.interceptors.ShutDownInterceptorFactory$1.processInvocation(ShutDownInterceptorFactory.java:64)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.component.interceptors.LoggingInterceptor.processInvocation(LoggingInterceptor.java:67)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ee.component.NamespaceContextInterceptor.processInvocation(NamespaceContextInterceptor.java:50)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.ContextClassLoaderInterceptor.processInvocation(ContextClassLoaderInterceptor.java:60)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.InterceptorContext.run(InterceptorContext.java:438)
	at org.wildfly.security.manager.WildFlySecurityManager.doChecked(WildFlySecurityManager.java:633)
	at org.jboss.invocation.AccessCheckingInterceptor.processInvocation(AccessCheckingInterceptor.java:57)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.ChainedInterceptor.processInvocation(ChainedInterceptor.java:53)
	at org.jboss.as.ee.component.ViewService$View.invoke(ViewService.java:198)
	at org.jboss.as.ee.component.ViewDescription$1.processInvocation(ViewDescription.java:191)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.security.IdentityInterceptor.processInvocation(IdentityInterceptor.java:49)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.ChainedInterceptor.processInvocation(ChainedInterceptor.java:53)
	at org.jboss.as.ee.component.ProxyInvocationHandler.invoke(ProxyInvocationHandler.java:81)
	at br.gov.caixa.pr.sicow.conres.dao.AlertaImportacaoArquivoConresDao$$$view37.listAll(Unknown Source)
	at br.gov.caixa.pr.sicow.conres.bean.HomeBean.carregarBase(HomeBean.java:55)
	at br.gov.caixa.pr.sicow.conres.bean.HomeBean.init(HomeBean.java:42)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:498)
	at org.jboss.weld.injection.producer.DefaultLifecycleCallbackInvoker.invokeMethods(DefaultLifecycleCallbackInvoker.java:83)
	at org.jboss.weld.injection.producer.DefaultLifecycleCallbackInvoker.postConstruct(DefaultLifecycleCallbackInvoker.java:66)
	at org.jboss.weld.injection.producer.BasicInjectionTarget.postConstruct(BasicInjectionTarget.java:122)
	at org.jboss.as.weld.deployment.processors.WeldComponentIntegrationProcessor$3.run(WeldComponentIntegrationProcessor.java:234)
	at org.jboss.as.weld.deployment.processors.WeldComponentIntegrationProcessor$AbstractInjectionTargetDelegatingInterceptor.processInvocation(WeldComponentIntegrationProcessor.java:299)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.weld.injection.WeldInjectionInterceptor.processInvocation(WeldInjectionInterceptor.java:53)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ee.component.ManagedReferenceFieldInjectionInterceptorFactory$ManagedReferenceFieldInjectionInterceptor.processInvocation(ManagedReferenceFieldInjectionInterceptorFactory.java:112)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ee.component.ManagedReferenceFieldInjectionInterceptorFactory$ManagedReferenceFieldInjectionInterceptor.processInvocation(ManagedReferenceFieldInjectionInterceptorFactory.java:112)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ee.component.AroundConstructInterceptorFactory$1.processInvocation(AroundConstructInterceptorFactory.java:28)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.weld.injection.WeldInterceptorInjectionInterceptor.processInvocation(WeldInterceptorInjectionInterceptor.java:56)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.weld.injection.WeldInjectionContextInterceptor.processInvocation(WeldInjectionContextInterceptor.java:43)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ee.concurrent.ConcurrentContextInterceptor.processInvocation(ConcurrentContextInterceptor.java:45)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.ContextClassLoaderInterceptor.processInvocation(ContextClassLoaderInterceptor.java:60)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.ChainedInterceptor.processInvocation(ChainedInterceptor.java:53)
	at org.jboss.as.ee.component.BasicComponent.constructComponentInstance(BasicComponent.java:168)
	at org.jboss.as.ee.component.BasicComponent.constructComponentInstance(BasicComponent.java:141)
	at org.jboss.as.ee.component.BasicComponent.createInstance(BasicComponent.java:99)
	at org.jboss.as.ee.component.ComponentRegistry$ComponentManagedReferenceFactory.createReference(ComponentRegistry.java:184)
	at org.jboss.as.ee.component.ComponentRegistry.createInstance(ComponentRegistry.java:92)
	at org.jboss.as.web.common.CachingWebInjectionContainer.newInstance(CachingWebInjectionContainer.java:70)
	at org.jboss.as.jsf.injection.JSFInjectionProvider.invokePostConstruct(JSFInjectionProvider.java:70)
	at com.sun.faces.mgbean.BeanBuilder.invokePostConstruct(BeanBuilder.java:197)
	at com.sun.faces.mgbean.BeanBuilder.build(BeanBuilder.java:79)
	at com.sun.faces.mgbean.BeanManager.createAndPush(BeanManager.java:387)
	at com.sun.faces.mgbean.BeanManager.create(BeanManager.java:247)
	at com.sun.faces.el.ManagedBeanELResolver.resolveBean(ManagedBeanELResolver.java:200)
	at com.sun.faces.el.ManagedBeanELResolver.getValue(ManagedBeanELResolver.java:55)
	at com.sun.faces.el.DemuxCompositeELResolver._getValue(DemuxCompositeELResolver.java:156)
	at com.sun.faces.el.DemuxCompositeELResolver.getValue(DemuxCompositeELResolver.java:184)
	at com.sun.el.parser.AstIdentifier.getValue(AstIdentifier.java:91)
	at com.sun.el.parser.AstValue.getBase(AstValue.java:125)
	at com.sun.el.parser.AstValue.getValue(AstValue.java:173)
	at com.sun.el.ValueExpressionImpl.getValue(ValueExpressionImpl.java:183)
	at org.jboss.weld.module.web.el.WeldValueExpression.getValue(WeldValueExpression.java:50)
	at org.jboss.weld.module.web.el.WeldValueExpression.getValue(WeldValueExpression.java:50)
	at com.sun.faces.facelets.el.TagValueExpression.getValue(TagValueExpression.java:73)
	at javax.faces.component.ComponentStateHelper.eval(ComponentStateHelper.java:170)
	at javax.faces.component.ComponentStateHelper.eval(ComponentStateHelper.java:157)
	at javax.faces.component.UIOutput.getValue(UIOutput.java:140)
	at javax.faces.component.UIInput.getValue(UIInput.java:287)
	at org.primefaces.component.selectoneradio.SelectOneRadioRenderer.encodeSelectItems(SelectOneRadioRenderer.java:108)
	at org.primefaces.component.selectoneradio.SelectOneRadioRenderer.encodeMarkup(SelectOneRadioRenderer.java:78)
	at org.primefaces.component.selectoneradio.SelectOneRadioRenderer.encodeEnd(SelectOneRadioRenderer.java:46)
	at javax.faces.component.UIComponentBase.encodeEnd(UIComponentBase.java:595)
	at com.sun.faces.renderkit.html_basic.HtmlBasicRenderer.encodeRecursive(HtmlBasicRenderer.java:286)
	at com.sun.faces.renderkit.html_basic.GroupRenderer.encodeChildren(GroupRenderer.java:90)
	at javax.faces.component.UIComponentBase.encodeChildren(UIComponentBase.java:566)
	at com.sun.faces.renderkit.html_basic.HtmlBasicRenderer.encodeRecursive(HtmlBasicRenderer.java:278)
	at com.sun.faces.renderkit.html_basic.GroupRenderer.encodeChildren(GroupRenderer.java:90)
	at javax.faces.component.UIComponentBase.encodeChildren(UIComponentBase.java:566)
	at javax.faces.component.UIComponent.encodeAll(UIComponent.java:1647)
	at javax.faces.render.Renderer.encodeChildren(Renderer.java:152)
	at javax.faces.component.UIComponentBase.encodeChildren(UIComponentBase.java:566)
	at javax.faces.component.UIComponent.encodeAll(UIComponent.java:1647)
	at javax.faces.component.UIComponent.encodeAll(UIComponent.java:1650)
	at javax.faces.component.UIComponent.encodeAll(UIComponent.java:1650)
	at com.sun.faces.application.view.FaceletViewHandlingStrategy.renderView(FaceletViewHandlingStrategy.java:468)
	at com.sun.faces.application.view.MultiViewHandler.renderView(MultiViewHandler.java:170)
	at javax.faces.application.ViewHandlerWrapper.renderView(ViewHandlerWrapper.java:132)
	at javax.faces.application.ViewHandlerWrapper.renderView(ViewHandlerWrapper.java:132)
	at com.sun.faces.lifecycle.RenderResponsePhase.execute(RenderResponsePhase.java:102)
	at com.sun.faces.lifecycle.Phase.doPhase(Phase.java:76)
	at com.sun.faces.lifecycle.LifecycleImpl.render(LifecycleImpl.java:199)
	at javax.faces.webapp.FacesServlet.executeLifecyle(FacesServlet.java:708)
	at javax.faces.webapp.FacesServlet.service(FacesServlet.java:451)
	at io.undertow.servlet.handlers.ServletHandler.handleRequest(ServletHandler.java:74)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:129)
	at org.primefaces.webapp.filter.FileUploadFilter.doFilter(FileUploadFilter.java:79)
	at io.undertow.servlet.core.ManagedFilter.doFilter(ManagedFilter.java:67)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:131)
	at br.gov.caixa.pr.sicow.conres.filter.SicowIECompatibleFixFilter.doFilter(SicowIECompatibleFixFilter.java:32)
	at io.undertow.servlet.core.ManagedFilter.doFilter(ManagedFilter.java:67)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:131)
	at br.gov.caixa.core.filter.UnexpectedErrorFilter.doFilter(UnexpectedErrorFilter.java:31)
	at io.undertow.servlet.core.ManagedFilter.doFilter(ManagedFilter.java:67)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:131)
	at io.undertow.servlet.handlers.FilterHandler.handleRequest(FilterHandler.java:84)
	at io.undertow.servlet.handlers.security.ServletSecurityRoleHandler.handleRequest(ServletSecurityRoleHandler.java:62)
	at io.undertow.servlet.handlers.ServletChain$1.handleRequest(ServletChain.java:68)
	at io.undertow.servlet.handlers.ServletDispatchingHandler.handleRequest(ServletDispatchingHandler.java:36)
	at org.wildfly.extension.undertow.security.SecurityContextAssociationHandler.handleRequest(SecurityContextAssociationHandler.java:78)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.servlet.handlers.RedirectDirHandler.handleRequest(RedirectDirHandler.java:68)
	at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:117)
	at io.undertow.servlet.handlers.security.ServletAuthenticationCallHandler.handleRequest(ServletAuthenticationCallHandler.java:57)
	at io.undertow.server.handlers.DisableCacheHandler.handleRequest(DisableCacheHandler.java:33)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.security.handlers.AuthenticationConstraintHandler.handleRequest(AuthenticationConstraintHandler.java:53)
	at io.undertow.security.handlers.AbstractConfidentialityHandler.handleRequest(AbstractConfidentialityHandler.java:46)
	at io.undertow.servlet.handlers.security.ServletConfidentialityConstraintHandler.handleRequest(ServletConfidentialityConstraintHandler.java:64)
	at io.undertow.servlet.handlers.security.ServletSecurityConstraintHandler.handleRequest(ServletSecurityConstraintHandler.java:60)
	at io.undertow.security.handlers.AuthenticationMechanismsHandler.handleRequest(AuthenticationMechanismsHandler.java:60)
	at io.undertow.servlet.handlers.security.CachedAuthenticatedSessionHandler.handleRequest(CachedAuthenticatedSessionHandler.java:77)
	at io.undertow.security.handlers.NotificationReceiverHandler.handleRequest(NotificationReceiverHandler.java:50)
	at io.undertow.security.handlers.AbstractSecurityContextAssociationHandler.handleRequest(AbstractSecurityContextAssociationHandler.java:43)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at org.wildfly.extension.undertow.security.jacc.JACCContextIdHandler.handleRequest(JACCContextIdHandler.java:61)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at org.wildfly.extension.undertow.deployment.GlobalRequestControllerHandler.handleRequest(GlobalRequestControllerHandler.java:68)
	at io.undertow.servlet.handlers.SendErrorPageHandler.handleRequest(SendErrorPageHandler.java:52)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.servlet.handlers.ServletInitialHandler.handleFirstRequest(ServletInitialHandler.java:275)
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
Caused by: org.postgresql.util.PSQLException: FATAL: password authentication failed for user "scowdb01"
	at org.postgresql.core.v3.ConnectionFactoryImpl.doAuthentication(ConnectionFactoryImpl.java:525)
	at org.postgresql.core.v3.ConnectionFactoryImpl.tryConnect(ConnectionFactoryImpl.java:146)
	at org.postgresql.core.v3.ConnectionFactoryImpl.openConnectionImpl(ConnectionFactoryImpl.java:197)
	at org.postgresql.core.ConnectionFactory.openConnection(ConnectionFactory.java:49)
	at org.postgresql.jdbc.PgConnection.<init>(PgConnection.java:217)
	at org.postgresql.Driver.makeConnection(Driver.java:458)
	at org.postgresql.Driver.connect(Driver.java:260)
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.createLocalManagedConnection(LocalManagedConnectionFactory.java:335)
	... 239 more

2026-10-24 12:46:57,269 WARN  [org.hibernate.engine.jdbc.spi.SqlExceptionHelper] (default task-1) SQL Error: 0, SQLState: null
2026-10-24 12:46:57,269 ERROR [org.hibernate.engine.jdbc.spi.SqlExceptionHelper] (default task-1) javax.resource.ResourceException: IJ000453: Unable to get managed connection for java:/jboss/datasources/sicow-ds
2026-10-24 12:46:57,283 ERROR [org.jboss.as.ejb3.invocation] (default task-1) WFLYEJB0034: Jakarta Enterprise Beans Invocation failed on component AlertaImportacaoArquivoConresDao for method public java.util.List br.gov.caixa.core.dao.CaixaDao.listAll(): javax.ejb.EJBException: javax.persistence.PersistenceException: org.hibernate.exception.GenericJDBCException: Unable to acquire JDBC Connection
	at org.jboss.as.ejb3.tx.CMTTxInterceptor.invokeInOurTx(CMTTxInterceptor.java:268)
	at org.jboss.as.ejb3.tx.CMTTxInterceptor.required(CMTTxInterceptor.java:390)
	at org.jboss.as.ejb3.tx.CMTTxInterceptor.processInvocation(CMTTxInterceptor.java:160)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.InterceptorContext$Invocation.proceed(InterceptorContext.java:509)
	at org.jboss.weld.module.ejb.AbstractEJBRequestScopeActivationInterceptor.aroundInvoke(AbstractEJBRequestScopeActivationInterceptor.java:72)
	at org.jboss.as.weld.ejb.EjbRequestScopeActivationInterceptor.processInvocation(EjbRequestScopeActivationInterceptor.java:89)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.component.interceptors.CurrentInvocationContextInterceptor.processInvocation(CurrentInvocationContextInterceptor.java:41)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.component.invocationmetrics.WaitTimeInterceptor.processInvocation(WaitTimeInterceptor.java:47)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.security.SecurityContextInterceptor.processInvocation(SecurityContextInterceptor.java:100)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.deployment.processors.StartupAwaitInterceptor.processInvocation(StartupAwaitInterceptor.java:22)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.component.interceptors.ShutDownInterceptorFactory$1.processInvocation(ShutDownInterceptorFactory.java:64)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.component.interceptors.LoggingInterceptor.processInvocation(LoggingInterceptor.java:67)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ee.component.NamespaceContextInterceptor.processInvocation(NamespaceContextInterceptor.java:50)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.ContextClassLoaderInterceptor.processInvocation(ContextClassLoaderInterceptor.java:60)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.InterceptorContext.run(InterceptorContext.java:438)
	at org.wildfly.security.manager.WildFlySecurityManager.doChecked(WildFlySecurityManager.java:633)
	at org.jboss.invocation.AccessCheckingInterceptor.processInvocation(AccessCheckingInterceptor.java:57)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.ChainedInterceptor.processInvocation(ChainedInterceptor.java:53)
	at org.jboss.as.ee.component.ViewService$View.invoke(ViewService.java:198)
	at org.jboss.as.ee.component.ViewDescription$1.processInvocation(ViewDescription.java:191)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.security.IdentityInterceptor.processInvocation(IdentityInterceptor.java:49)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.ChainedInterceptor.processInvocation(ChainedInterceptor.java:53)
	at org.jboss.as.ee.component.ProxyInvocationHandler.invoke(ProxyInvocationHandler.java:81)
	at br.gov.caixa.pr.sicow.conres.dao.AlertaImportacaoArquivoConresDao$$$view37.listAll(Unknown Source)
	at br.gov.caixa.pr.sicow.conres.bean.HomeBean.carregarBase(HomeBean.java:55)
	at br.gov.caixa.pr.sicow.conres.bean.HomeBean.init(HomeBean.java:42)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:498)
	at org.jboss.weld.injection.producer.DefaultLifecycleCallbackInvoker.invokeMethods(DefaultLifecycleCallbackInvoker.java:83)
	at org.jboss.weld.injection.producer.DefaultLifecycleCallbackInvoker.postConstruct(DefaultLifecycleCallbackInvoker.java:66)
	at org.jboss.weld.injection.producer.BasicInjectionTarget.postConstruct(BasicInjectionTarget.java:122)
	at org.jboss.as.weld.deployment.processors.WeldComponentIntegrationProcessor$3.run(WeldComponentIntegrationProcessor.java:234)
	at org.jboss.as.weld.deployment.processors.WeldComponentIntegrationProcessor$AbstractInjectionTargetDelegatingInterceptor.processInvocation(WeldComponentIntegrationProcessor.java:299)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.weld.injection.WeldInjectionInterceptor.processInvocation(WeldInjectionInterceptor.java:53)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ee.component.ManagedReferenceFieldInjectionInterceptorFactory$ManagedReferenceFieldInjectionInterceptor.processInvocation(ManagedReferenceFieldInjectionInterceptorFactory.java:112)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ee.component.ManagedReferenceFieldInjectionInterceptorFactory$ManagedReferenceFieldInjectionInterceptor.processInvocation(ManagedReferenceFieldInjectionInterceptorFactory.java:112)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ee.component.AroundConstructInterceptorFactory$1.processInvocation(AroundConstructInterceptorFactory.java:28)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.weld.injection.WeldInterceptorInjectionInterceptor.processInvocation(WeldInterceptorInjectionInterceptor.java:56)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.weld.injection.WeldInjectionContextInterceptor.processInvocation(WeldInjectionContextInterceptor.java:43)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ee.concurrent.ConcurrentContextInterceptor.processInvocation(ConcurrentContextInterceptor.java:45)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.ContextClassLoaderInterceptor.processInvocation(ContextClassLoaderInterceptor.java:60)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.ChainedInterceptor.processInvocation(ChainedInterceptor.java:53)
	at org.jboss.as.ee.component.BasicComponent.constructComponentInstance(BasicComponent.java:168)
	at org.jboss.as.ee.component.BasicComponent.constructComponentInstance(BasicComponent.java:141)
	at org.jboss.as.ee.component.BasicComponent.createInstance(BasicComponent.java:99)
	at org.jboss.as.ee.component.ComponentRegistry$ComponentManagedReferenceFactory.createReference(ComponentRegistry.java:184)
	at org.jboss.as.ee.component.ComponentRegistry.createInstance(ComponentRegistry.java:92)
	at org.jboss.as.web.common.CachingWebInjectionContainer.newInstance(CachingWebInjectionContainer.java:70)
	at org.jboss.as.jsf.injection.JSFInjectionProvider.invokePostConstruct(JSFInjectionProvider.java:70)
	at com.sun.faces.mgbean.BeanBuilder.invokePostConstruct(BeanBuilder.java:197)
	at com.sun.faces.mgbean.BeanBuilder.build(BeanBuilder.java:79)
	at com.sun.faces.mgbean.BeanManager.createAndPush(BeanManager.java:387)
	at com.sun.faces.mgbean.BeanManager.create(BeanManager.java:247)
	at com.sun.faces.el.ManagedBeanELResolver.resolveBean(ManagedBeanELResolver.java:200)
	at com.sun.faces.el.ManagedBeanELResolver.getValue(ManagedBeanELResolver.java:55)
	at com.sun.faces.el.DemuxCompositeELResolver._getValue(DemuxCompositeELResolver.java:156)
	at com.sun.faces.el.DemuxCompositeELResolver.getValue(DemuxCompositeELResolver.java:184)
	at com.sun.el.parser.AstIdentifier.getValue(AstIdentifier.java:91)
	at com.sun.el.parser.AstValue.getBase(AstValue.java:125)
	at com.sun.el.parser.AstValue.getValue(AstValue.java:173)
	at com.sun.el.ValueExpressionImpl.getValue(ValueExpressionImpl.java:183)
	at org.jboss.weld.module.web.el.WeldValueExpression.getValue(WeldValueExpression.java:50)
	at org.jboss.weld.module.web.el.WeldValueExpression.getValue(WeldValueExpression.java:50)
	at com.sun.faces.facelets.el.TagValueExpression.getValue(TagValueExpression.java:73)
	at javax.faces.component.ComponentStateHelper.eval(ComponentStateHelper.java:170)
	at javax.faces.component.ComponentStateHelper.eval(ComponentStateHelper.java:157)
	at javax.faces.component.UIOutput.getValue(UIOutput.java:140)
	at javax.faces.component.UIInput.getValue(UIInput.java:287)
	at org.primefaces.component.selectoneradio.SelectOneRadioRenderer.encodeSelectItems(SelectOneRadioRenderer.java:108)
	at org.primefaces.component.selectoneradio.SelectOneRadioRenderer.encodeMarkup(SelectOneRadioRenderer.java:78)
	at org.primefaces.component.selectoneradio.SelectOneRadioRenderer.encodeEnd(SelectOneRadioRenderer.java:46)
	at javax.faces.component.UIComponentBase.encodeEnd(UIComponentBase.java:595)
	at com.sun.faces.renderkit.html_basic.HtmlBasicRenderer.encodeRecursive(HtmlBasicRenderer.java:286)
	at com.sun.faces.renderkit.html_basic.GroupRenderer.encodeChildren(GroupRenderer.java:90)
	at javax.faces.component.UIComponentBase.encodeChildren(UIComponentBase.java:566)
	at com.sun.faces.renderkit.html_basic.HtmlBasicRenderer.encodeRecursive(HtmlBasicRenderer.java:278)
	at com.sun.faces.renderkit.html_basic.GroupRenderer.encodeChildren(GroupRenderer.java:90)
	at javax.faces.component.UIComponentBase.encodeChildren(UIComponentBase.java:566)
	at javax.faces.component.UIComponent.encodeAll(UIComponent.java:1647)
	at javax.faces.render.Renderer.encodeChildren(Renderer.java:152)
	at javax.faces.component.UIComponentBase.encodeChildren(UIComponentBase.java:566)
	at javax.faces.component.UIComponent.encodeAll(UIComponent.java:1647)
	at javax.faces.component.UIComponent.encodeAll(UIComponent.java:1650)
	at javax.faces.component.UIComponent.encodeAll(UIComponent.java:1650)
	at com.sun.faces.application.view.FaceletViewHandlingStrategy.renderView(FaceletViewHandlingStrategy.java:468)
	at com.sun.faces.application.view.MultiViewHandler.renderView(MultiViewHandler.java:170)
	at javax.faces.application.ViewHandlerWrapper.renderView(ViewHandlerWrapper.java:132)
	at javax.faces.application.ViewHandlerWrapper.renderView(ViewHandlerWrapper.java:132)
	at com.sun.faces.lifecycle.RenderResponsePhase.execute(RenderResponsePhase.java:102)
	at com.sun.faces.lifecycle.Phase.doPhase(Phase.java:76)
	at com.sun.faces.lifecycle.LifecycleImpl.render(LifecycleImpl.java:199)
	at javax.faces.webapp.FacesServlet.executeLifecyle(FacesServlet.java:708)
	at javax.faces.webapp.FacesServlet.service(FacesServlet.java:451)
	at io.undertow.servlet.handlers.ServletHandler.handleRequest(ServletHandler.java:74)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:129)
	at org.primefaces.webapp.filter.FileUploadFilter.doFilter(FileUploadFilter.java:79)
	at io.undertow.servlet.core.ManagedFilter.doFilter(ManagedFilter.java:67)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:131)
	at br.gov.caixa.pr.sicow.conres.filter.SicowIECompatibleFixFilter.doFilter(SicowIECompatibleFixFilter.java:32)
	at io.undertow.servlet.core.ManagedFilter.doFilter(ManagedFilter.java:67)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:131)
	at br.gov.caixa.core.filter.UnexpectedErrorFilter.doFilter(UnexpectedErrorFilter.java:31)
	at io.undertow.servlet.core.ManagedFilter.doFilter(ManagedFilter.java:67)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:131)
	at io.undertow.servlet.handlers.FilterHandler.handleRequest(FilterHandler.java:84)
	at io.undertow.servlet.handlers.security.ServletSecurityRoleHandler.handleRequest(ServletSecurityRoleHandler.java:62)
	at io.undertow.servlet.handlers.ServletChain$1.handleRequest(ServletChain.java:68)
	at io.undertow.servlet.handlers.ServletDispatchingHandler.handleRequest(ServletDispatchingHandler.java:36)
	at org.wildfly.extension.undertow.security.SecurityContextAssociationHandler.handleRequest(SecurityContextAssociationHandler.java:78)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.servlet.handlers.RedirectDirHandler.handleRequest(RedirectDirHandler.java:68)
	at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:117)
	at io.undertow.servlet.handlers.security.ServletAuthenticationCallHandler.handleRequest(ServletAuthenticationCallHandler.java:57)
	at io.undertow.server.handlers.DisableCacheHandler.handleRequest(DisableCacheHandler.java:33)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.security.handlers.AuthenticationConstraintHandler.handleRequest(AuthenticationConstraintHandler.java:53)
	at io.undertow.security.handlers.AbstractConfidentialityHandler.handleRequest(AbstractConfidentialityHandler.java:46)
	at io.undertow.servlet.handlers.security.ServletConfidentialityConstraintHandler.handleRequest(ServletConfidentialityConstraintHandler.java:64)
	at io.undertow.servlet.handlers.security.ServletSecurityConstraintHandler.handleRequest(ServletSecurityConstraintHandler.java:60)
	at io.undertow.security.handlers.AuthenticationMechanismsHandler.handleRequest(AuthenticationMechanismsHandler.java:60)
	at io.undertow.servlet.handlers.security.CachedAuthenticatedSessionHandler.handleRequest(CachedAuthenticatedSessionHandler.java:77)
	at io.undertow.security.handlers.NotificationReceiverHandler.handleRequest(NotificationReceiverHandler.java:50)
	at io.undertow.security.handlers.AbstractSecurityContextAssociationHandler.handleRequest(AbstractSecurityContextAssociationHandler.java:43)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at org.wildfly.extension.undertow.security.jacc.JACCContextIdHandler.handleRequest(JACCContextIdHandler.java:61)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at org.wildfly.extension.undertow.deployment.GlobalRequestControllerHandler.handleRequest(GlobalRequestControllerHandler.java:68)
	at io.undertow.servlet.handlers.SendErrorPageHandler.handleRequest(SendErrorPageHandler.java:52)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.servlet.handlers.ServletInitialHandler.handleFirstRequest(ServletInitialHandler.java:275)
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
Caused by: javax.persistence.PersistenceException: org.hibernate.exception.GenericJDBCException: Unable to acquire JDBC Connection
	at org.hibernate.internal.ExceptionConverterImpl.convert(ExceptionConverterImpl.java:154)
	at org.hibernate.query.internal.AbstractProducedQuery.list(AbstractProducedQuery.java:1575)
	at org.hibernate.query.Query.getResultList(Query.java:132)
	at br.gov.caixa.pr.sicow.conres.dao.AlertaImportacaoArquivoConresDao.listAll(AlertaImportacaoArquivoConresDao.java:77)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:498)
	at org.jboss.as.ee.component.ManagedReferenceMethodInterceptor.processInvocation(ManagedReferenceMethodInterceptor.java:52)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.InterceptorContext$Invocation.proceed(InterceptorContext.java:509)
	at org.jboss.as.weld.interceptors.Jsr299BindingsInterceptor.delegateInterception(Jsr299BindingsInterceptor.java:79)
	at org.jboss.as.weld.interceptors.Jsr299BindingsInterceptor.doMethodInterception(Jsr299BindingsInterceptor.java:89)
	at org.jboss.as.weld.interceptors.Jsr299BindingsInterceptor.processInvocation(Jsr299BindingsInterceptor.java:102)
	at org.jboss.as.ee.component.interceptors.UserInterceptorFactory$1.processInvocation(UserInterceptorFactory.java:63)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.component.invocationmetrics.ExecutionTimeInterceptor.processInvocation(ExecutionTimeInterceptor.java:43)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.jpa.interceptor.SBInvocationInterceptor.processInvocation(SBInvocationInterceptor.java:47)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ee.concurrent.ConcurrentContextInterceptor.processInvocation(ConcurrentContextInterceptor.java:45)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.InitialInterceptor.processInvocation(InitialInterceptor.java:40)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.invocation.ChainedInterceptor.processInvocation(ChainedInterceptor.java:53)
	at org.jboss.as.ee.component.interceptors.ComponentDispatcherInterceptor.processInvocation(ComponentDispatcherInterceptor.java:52)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.component.pool.PooledInstanceInterceptor.processInvocation(PooledInstanceInterceptor.java:51)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.component.interceptors.AdditionalSetupInterceptor.processInvocation(AdditionalSetupInterceptor.java:54)
	at org.jboss.invocation.InterceptorContext.proceed(InterceptorContext.java:422)
	at org.jboss.as.ejb3.tx.CMTTxInterceptor.invokeInOurTx(CMTTxInterceptor.java:254)
	... 175 more
Caused by: org.hibernate.exception.GenericJDBCException: Unable to acquire JDBC Connection
	at org.hibernate.exception.internal.StandardSQLExceptionConverter.convert(StandardSQLExceptionConverter.java:47)
	at org.hibernate.engine.jdbc.spi.SqlExceptionHelper.convert(SqlExceptionHelper.java:113)
	at org.hibernate.engine.jdbc.spi.SqlExceptionHelper.convert(SqlExceptionHelper.java:99)
	at org.hibernate.resource.jdbc.internal.LogicalConnectionManagedImpl.acquireConnectionIfNeeded(LogicalConnectionManagedImpl.java:109)
	at org.hibernate.resource.jdbc.internal.LogicalConnectionManagedImpl.getPhysicalConnection(LogicalConnectionManagedImpl.java:136)
	at org.hibernate.engine.jdbc.internal.StatementPreparerImpl.connection(StatementPreparerImpl.java:50)
	at org.hibernate.engine.jdbc.internal.StatementPreparerImpl$5.doPrepare(StatementPreparerImpl.java:149)
	at org.hibernate.engine.jdbc.internal.StatementPreparerImpl$StatementPreparationTemplate.prepareStatement(StatementPreparerImpl.java:176)
	at org.hibernate.engine.jdbc.internal.StatementPreparerImpl.prepareQueryStatement(StatementPreparerImpl.java:151)
	at org.hibernate.loader.Loader.prepareQueryStatement(Loader.java:2082)
	at org.hibernate.loader.Loader.executeQueryStatement(Loader.java:2012)
	at org.hibernate.loader.Loader.executeQueryStatement(Loader.java:1990)
	at org.hibernate.loader.Loader.doQuery(Loader.java:949)
	at org.hibernate.loader.Loader.doQueryAndInitializeNonLazyCollections(Loader.java:351)
	at org.hibernate.loader.Loader.doList(Loader.java:2787)
	at org.hibernate.loader.Loader.doList(Loader.java:2770)
	at org.hibernate.loader.Loader.listIgnoreQueryCache(Loader.java:2604)
	at org.hibernate.loader.Loader.list(Loader.java:2599)
	at org.hibernate.loader.hql.QueryLoader.list(QueryLoader.java:505)
	at org.hibernate.hql.internal.ast.QueryTranslatorImpl.list(QueryTranslatorImpl.java:395)
	at org.hibernate.engine.query.spi.HQLQueryPlan.performList(HQLQueryPlan.java:220)
	at org.hibernate.internal.SessionImpl.list(SessionImpl.java:1526)
	at org.hibernate.query.internal.AbstractProducedQuery.doList(AbstractProducedQuery.java:1598)
	at org.hibernate.query.internal.AbstractProducedQuery.list(AbstractProducedQuery.java:1566)
	... 205 more
Caused by: java.sql.SQLException: javax.resource.ResourceException: IJ000453: Unable to get managed connection for java:/jboss/datasources/sicow-ds
	at org.jboss.jca.adapters.jdbc.WrapperDataSource.getConnection(WrapperDataSource.java:158)
	at org.jboss.as.connector.subsystems.datasources.WildFlyDataSource.getConnection(WildFlyDataSource.java:64)
	at org.hibernate.engine.jdbc.connections.internal.DatasourceConnectionProviderImpl.getConnection(DatasourceConnectionProviderImpl.java:122)
	at org.hibernate.internal.NonContextualJdbcConnectionAccess.obtainConnection(NonContextualJdbcConnectionAccess.java:35)
	at org.hibernate.resource.jdbc.internal.LogicalConnectionManagedImpl.acquireConnectionIfNeeded(LogicalConnectionManagedImpl.java:106)
	... 225 more
Caused by: javax.resource.ResourceException: IJ000453: Unable to get managed connection for java:/jboss/datasources/sicow-ds
	at org.jboss.jca.core.connectionmanager.AbstractConnectionManager.getManagedConnection(AbstractConnectionManager.java:690)
	at org.jboss.jca.core.connectionmanager.tx.TxConnectionManagerImpl.getManagedConnection(TxConnectionManagerImpl.java:440)
	at org.jboss.jca.core.connectionmanager.AbstractConnectionManager.allocateConnection(AbstractConnectionManager.java:789)
	at org.jboss.jca.adapters.jdbc.WrapperDataSource.getConnection(WrapperDataSource.java:150)
	... 229 more
Caused by: javax.resource.ResourceException: IJ031084: Unable to create connection
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.createLocalManagedConnection(LocalManagedConnectionFactory.java:364)
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.getLocalManagedConnection(LocalManagedConnectionFactory.java:371)
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.createManagedConnection(LocalManagedConnectionFactory.java:287)
	at org.jboss.jca.core.connectionmanager.pool.mcp.SemaphoreConcurrentLinkedDequeManagedConnectionPool.createConnectionEventListener(SemaphoreConcurrentLinkedDequeManagedConnectionPool.java:1328)
	at org.jboss.jca.core.connectionmanager.pool.mcp.SemaphoreConcurrentLinkedDequeManagedConnectionPool.getConnection(SemaphoreConcurrentLinkedDequeManagedConnectionPool.java:505)
	at org.jboss.jca.core.connectionmanager.pool.AbstractPool.getTransactionNewConnection(AbstractPool.java:722)
	at org.jboss.jca.core.connectionmanager.pool.AbstractPool.getConnection(AbstractPool.java:618)
	at org.jboss.jca.core.connectionmanager.AbstractConnectionManager.getManagedConnection(AbstractConnectionManager.java:624)
	... 232 more
Caused by: org.postgresql.util.PSQLException: FATAL: password authentication failed for user "scowdb01"
	at org.postgresql.core.v3.ConnectionFactoryImpl.doAuthentication(ConnectionFactoryImpl.java:525)
	at org.postgresql.core.v3.ConnectionFactoryImpl.tryConnect(ConnectionFactoryImpl.java:146)
	at org.postgresql.core.v3.ConnectionFactoryImpl.openConnectionImpl(ConnectionFactoryImpl.java:197)
	at org.postgresql.core.ConnectionFactory.openConnection(ConnectionFactory.java:49)
	at org.postgresql.jdbc.PgConnection.<init>(PgConnection.java:217)
	at org.postgresql.Driver.makeConnection(Driver.java:458)
	at org.postgresql.Driver.connect(Driver.java:260)
	at org.jboss.jca.adapters.jdbc.local.LocalManagedConnectionFactory.createLocalManagedConnection(LocalManagedConnectionFactory.java:335)
	... 239 more

2026-10-24 12:46:57,662 INFO  [br.gov.caixa.pr.sicow.portal.login.phaseListener.SicowLoginHttpsPhaseListener] (default task-6) false
2026-10-24 12:46:57,667 INFO  [br.gov.caixa.pr.sicow.portal.login.phaseListener.SicowLoginHttpsPhaseListener] (default task-6) false
