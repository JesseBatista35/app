Using openshift launcher.
2026-10-13 17:57:07 Launching WildFly Server
INFO Access log is disabled, ignoring configuration.
INFO Clustering feature is not enabled, no jgroups subsystem present in server configuration.
INFO Server started in admin mode, CLI script executed during server boot.
INFO Running jboss-eap-8/eap8-openjdk21-builder-openshift-rhel9 image, version 1.0.1.GA
JAVA_OPTS already set in environment; overriding default settings with values:  -XX:MaxRAMPercentage=80.0 -XX:+UseParallelGC -XX:MinHeapFreeRatio=10 -XX:MaxHeapFreeRatio=20 -XX:GCTimeRatio=4 -XX:AdaptiveSizePolicyWeight=90 -XX:MetaspaceSize=96m -XX:+ExitOnOutOfMemoryError -Djava.security.egd=file:/dev/./urandom -Djava.net.preferIPv4Stack=true -Djboss.modules.system.pkgs=jdk.nashorn.api,com.sun.crypto.provider -Djavax.net.ssl.trustStore=/opt/server/standalone/configuration/caixa-truststore-acteste-nprd.jks -Djava.security.properties=/opt/server/bin/java.security.override -Djava.security.disableSystemPropertiesFile=true
=========================================================================

  JBoss Bootstrap Environment

  JBOSS_HOME: /opt/server

  JAVA: /usr/lib/jvm/java-21/bin/java

  JAVA_OPTS:  -Xlog:gc*:file="/opt/server/standalone/log/gc.log":time,uptimemillis:filecount=5,filesize=3M -Djdk.serialFilter="maxbytes=10485760;maxdepth=128;maxarray=100000;maxrefs=300000"  -XX:MaxRAMPercentage=80.0 -XX:+UseParallelGC -XX:MinHeapFreeRatio=10 -XX:MaxHeapFreeRatio=20 -XX:GCTimeRatio=4 -XX:AdaptiveSizePolicyWeight=90 -XX:MetaspaceSize=96m -XX:+ExitOnOutOfMemoryError -Djava.security.egd=file:/dev/./urandom -Djava.net.preferIPv4Stack=true -Djboss.modules.system.pkgs=jdk.nashorn.api,com.sun.crypto.provider -Djavax.net.ssl.trustStore=/opt/server/standalone/configuration/caixa-truststore-acteste-nprd.jks -Djava.security.properties=/opt/server/bin/java.security.override -Djava.security.disableSystemPropertiesFile=true  --add-exports=java.desktop/sun.awt=ALL-UNNAMED --add-exports=java.naming/com.sun.jndi.ldap=ALL-UNNAMED --add-exports=java.naming/com.sun.jndi.url.ldap=ALL-UNNAMED --add-exports=java.naming/com.sun.jndi.url.ldaps=ALL-UNNAMED --add-exports=jdk.naming.dns/com.sun.jndi.dns=ALL-UNNAMED --add-opens=java.base/java.lang=ALL-UNNAMED --add-opens=java.base/java.lang.invoke=ALL-UNNAMED --add-opens=java.base/java.lang.reflect=ALL-UNNAMED --add-opens=java.base/java.io=ALL-UNNAMED --add-opens=java.base/java.net=ALL-UNNAMED --add-opens=java.base/java.security=ALL-UNNAMED --add-opens=java.base/java.util=ALL-UNNAMED --add-opens=java.base/java.util.concurrent=ALL-UNNAMED --add-opens=java.management/javax.management=ALL-UNNAMED --add-opens=java.naming/javax.naming=ALL-UNNAMED

=========================================================================

[0m14:57:08,899 INFO  [org.jboss.modules] (main) JBoss Modules version 2.1.6.Final-redhat-00001
[0m[0m14:57:09,689 INFO  [org.jboss.msc] (main) JBoss MSC version 1.5.5.Final-redhat-00001
[0m[0m14:57:09,694 INFO  [org.jboss.threads] (main) JBoss Threads version 2.4.0.Final-redhat-00001
[0m[0m14:57:09,866 INFO  [org.jboss.as] (MSC service thread 1-2) WFLYSRV0049: JBoss EAP 8.0 Update 12.0 (WildFly Core 21.0.20.Final-redhat-00001) starting
[0m[32m14:57:09,867 DEBUG [org.jboss.as.config] (MSC service thread 1-2) Configured system properties:
	[Standalone] = 
	file.encoding = UTF-8
	file.separator = /
	java.class.path = /opt/server/jboss-modules.jar
	java.class.version = 65.0
	java.home = /usr/lib/jvm/java-21-openjdk-21.0.10.0.7-1.el9.x86_64
	java.io.tmpdir = /tmp
	java.library.path = /usr/java/packages/lib:/usr/lib64:/lib64:/lib:/usr/lib
	java.net.preferIPv4Stack = true
	java.runtime.name = OpenJDK Runtime Environment
	java.runtime.version = 21.0.10+7-LTS
	java.security.disableSystemPropertiesFile = true
	java.security.egd = file:/dev/./urandom
	java.security.properties = /opt/server/bin/java.security.override
	java.specification.name = Java Platform API Specification
	java.specification.vendor = Oracle Corporation
	java.specification.version = 21
	java.util.logging.manager = org.jboss.logmanager.LogManager
	java.vendor = Red Hat, Inc.
	java.vendor.url = https://www.redhat.com/
	java.vendor.url.bug = https://access.redhat.com/support/cases/
	java.vendor.version = (Red_Hat-21.0.10.0.7-1)
	java.version = 21.0.10
	java.version.date = 2026-01-20
	java.vm.compressedOopsMode = 32-bit
	java.vm.info = mixed mode, sharing
	java.vm.name = OpenJDK 64-Bit Server VM
	java.vm.specification.name = Java Virtual Machine Specification
	java.vm.specification.vendor = Oracle Corporation
	java.vm.specification.version = 21
	java.vm.vendor = Red Hat, Inc.
	java.vm.version = 21.0.10+7-LTS
	javax.management.builder.initial = org.jboss.as.jmx.PluggableMBeanServerBuilder
	javax.net.ssl.trustStore = /opt/server/standalone/configuration/caixa-truststore-acteste-nprd.jks
	jboss.bind.address = 25.1.38.69
	jboss.bind.address.management = 0.0.0.0
	jboss.bind.address.private = 25.1.38.69
	jboss.home.dir = /opt/server
	jboss.host.name = sihdg-jboss8-tqs-40-hs678
	jboss.messaging.cluster.password = <redacted>
	jboss.messaging.host = 25.1.38.69
	jboss.modules.system.pkgs = jdk.nashorn.api,com.sun.crypto.provider
	jboss.node.name = sihdg-jboss8-tqs-40-hs678
	jboss.qualified.host.name = sihdg-jboss8-tqs-40-hs678
	jboss.server.base.dir = /opt/server/standalone
	jboss.server.config.dir = /opt/server/standalone/configuration
	jboss.server.data.dir = /opt/server/standalone/data
	jboss.server.log.dir = /opt/server/standalone/log
	jboss.server.name = sihdg-jboss8-tqs-40-hs678
	jboss.server.persist.config = true
	jboss.server.temp.dir = /opt/server/standalone/tmp
	jboss.tx.node.id = hdg-jboss8-tqs-40-hs678
	jdk.debug = release
	jdk.serialFilter = maxbytes=10485760;maxdepth=128;maxarray=100000;maxrefs=300000
	line.separator = 

	logging.configuration = file:/opt/server/standalone/configuration/logging.properties
	module.path = /opt/server/modules
	native.encoding = ANSI_X3.4-1968
	org.jboss.boot.log.file = /opt/server/standalone/log/server.log
	org.jboss.resolver.warning = true
	org.wildfly.internal.cli.boot.hook.marker.dir = /tmp/cli-boot-reload-marker-1791914227
	org.wildfly.internal.cli.boot.hook.script = /tmp/cli-script-1791914227.cli
	org.wildfly.internal.cli.boot.hook.script.error.file = /tmp/cli-script-error-1791914227.cli
	org.wildfly.internal.cli.boot.hook.script.output.file = /tmp/cli-script-output-1791914227.cli
	org.wildfly.internal.cli.boot.hook.script.properties = /tmp/cli-script-property-1791914227.cli
	org.wildfly.internal.cli.boot.hook.script.warn.file = /tmp/cli-warning-1791914227.log
	os.arch = amd64
	os.name = Linux
	os.version = 6.1.18-200.fc37.x86_64
	path.separator = :
	stderr.encoding = ANSI_X3.4-1968
	stdout.encoding = ANSI_X3.4-1968
	sun.arch.data.model = 64
	sun.boot.library.path = /usr/lib/jvm/java-21-openjdk-21.0.10.0.7-1.el9.x86_64/lib
	sun.cpu.endian = little
	sun.io.unicode.encoding = UnicodeLittle
	sun.java.command = /opt/server/jboss-modules.jar -mp /opt/server/modules org.jboss.as.standalone -Djboss.home.dir=/opt/server -Djboss.server.base.dir=/opt/server/standalone -c standalone.xml -Djboss.messaging.host=25.1.38.69 -Djboss.messaging.cluster.password=<redacted> --start-mode=admin-only -Dorg.wildfly.internal.cli.boot.hook.script=/tmp/cli-script-1791914227.cli -Dorg.wildfly.internal.cli.boot.hook.marker.dir=/tmp/cli-boot-reload-marker-1791914227 -Dorg.wildfly.internal.cli.boot.hook.script.properties=/tmp/cli-script-property-1791914227.cli -Dorg.wildfly.internal.cli.boot.hook.script.error.file=/tmp/cli-script-error-1791914227.cli -Dorg.wildfly.internal.cli.boot.hook.script.warn.file=/tmp/cli-warning-1791914227.log -Dorg.wildfly.internal.cli.boot.hook.script.output.file=/tmp/cli-script-output-1791914227.cli -Djboss.node.name=sihdg-jboss8-tqs-40-hs678 -Djboss.tx.node.id=hdg-jboss8-tqs-40-hs678 -bprivate 25.1.38.69 -b 25.1.38.69 -bmanagement 0.0.0.0 -Dwildfly.statistics-enabled=true
	sun.java.launcher = SUN_STANDARD
	sun.jnu.encoding = ANSI_X3.4-1968
	sun.management.compiler = HotSpot 64-Bit Tiered Compilers
	user.country = US
	user.dir = /home/jboss
	user.home = /home/jboss
	user.language = en
	user.name = jboss
	user.timezone = America/Sao_Paulo
	wildfly.statistics-enabled = true
[0m[32m14:57:09,868 DEBUG [org.jboss.as.config] (MSC service thread 1-2) VM Arguments: -D[Standalone] -Xlog:gc*:file=/opt/server/standalone/log/gc.log:time,uptimemillis:filecount=5,filesize=3M -Djdk.serialFilter=maxbytes=10485760;maxdepth=128;maxarray=100000;maxrefs=300000 -XX:MaxRAMPercentage=80.0 -XX:+UseParallelGC -XX:MinHeapFreeRatio=10 -XX:MaxHeapFreeRatio=20 -XX:GCTimeRatio=4 -XX:AdaptiveSizePolicyWeight=90 -XX:MetaspaceSize=96m -XX:+ExitOnOutOfMemoryError -Djava.security.egd=file:/dev/./urandom -Djava.net.preferIPv4Stack=true -Djboss.modules.system.pkgs=jdk.nashorn.api,com.sun.crypto.provider -Djavax.net.ssl.trustStore=/opt/server/standalone/configuration/caixa-truststore-acteste-nprd.jks -Djava.security.properties=/opt/server/bin/java.security.override -Djava.security.disableSystemPropertiesFile=true --add-exports=java.desktop/sun.awt=ALL-UNNAMED --add-exports=java.naming/com.sun.jndi.ldap=ALL-UNNAMED --add-exports=java.naming/com.sun.jndi.url.ldap=ALL-UNNAMED --add-exports=java.naming/com.sun.jndi.url.ldaps=ALL-UNNAMED --add-exports=jdk.naming.dns/com.sun.jndi.dns=ALL-UNNAMED --add-opens=java.base/java.lang=ALL-UNNAMED --add-opens=java.base/java.lang.invoke=ALL-UNNAMED --add-opens=java.base/java.lang.reflect=ALL-UNNAMED --add-opens=java.base/java.io=ALL-UNNAMED --add-opens=java.base/java.net=ALL-UNNAMED --add-opens=java.base/java.security=ALL-UNNAMED --add-opens=java.base/java.util=ALL-UNNAMED --add-opens=java.base/java.util.concurrent=ALL-UNNAMED --add-opens=java.management/javax.management=ALL-UNNAMED --add-opens=java.naming/javax.naming=ALL-UNNAMED -Dorg.jboss.boot.log.file=/opt/server/standalone/log/server.log -Dlogging.configuration=file:/opt/server/standalone/configuration/logging.properties 
[0m[0m14:57:10,978 INFO  [org.wildfly.security] (ServerService Thread Pool -- 16) ELY00001: WildFly Elytron version 2.2.14.Final-redhat-00001
[0m[0m14:57:11,990 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0039: Creating http management service using socket-binding (management-http)
[0m[0m14:57:12,064 INFO  [org.xnio] (MSC service thread 1-2) XNIO version 3.8.16.Final-redhat-00001
[0m[0m14:57:12,067 INFO  [org.xnio.nio] (MSC service thread 1-2) XNIO NIO Implementation Version 3.8.16.Final-redhat-00001
[0m[33m14:57:12,160 WARN  [org.wildfly.extension.elytron] (MSC service thread 1-1) WFLYELY00023: KeyStore file '/opt/server/standalone/configuration/application.keystore' does not exist. Used blank.
[0m[0m14:57:12,163 INFO  [org.jboss.remoting] (MSC service thread 1-2) JBoss Remoting version 5.0.31.Final-redhat-00001
[0m[33m14:57:12,178 WARN  [org.wildfly.extension.elytron] (MSC service thread 1-1) WFLYELY01084: KeyStore /opt/server/standalone/configuration/application.keystore not found, it will be auto-generated on first use with a self-signed certificate for host localhost
[0m[0m14:57:12,486 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0212: Resuming server
[0m[0m14:57:12,488 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0060: Http management interface listening on http://0.0.0.0:9990/management
[0m[0m14:57:12,488 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0054: Admin console is not enabled
[0m[0m14:57:12,488 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0025: JBoss EAP 8.0 Update 12.0 (WildFly Core 21.0.20.Final-redhat-00001) started in 4067ms - Started 72 of 84 services (26 services are lazy, passive or on-demand) - Server configuration file in use: standalone.xml
[0m[0m14:57:12,489 INFO  [org.jboss.as.controller] (Controller Boot Thread) WFLYCTL0472: Checking for presence of marker file indicating that the server has been restarted following execution of the additional commands from the CLI script
[0m[0m14:57:12,489 INFO  [org.jboss.as.controller] (Controller Boot Thread) WFLYCTL0474: No marker file found indicating that the server has been restarted following execution of the additional commands from the CLI script
[0m[0m14:57:12,489 INFO  [org.jboss.as.controller] (Controller Boot Thread) WFLYCTL0466: Initialised the additional boot CLI script functionality. The CLI commands will be read from /tmp/cli-script-1791914227.cli. The server will be rebooted to normal mode after these have been executed
[0m[0m14:57:12,494 INFO  [org.jboss.as.controller] (Controller Boot Thread) WFLYCTL0467: Running the additional commands from the CLI script /tmp/cli-script-1791914227.cli against the server which is running in admin-only mode
[0m[0m14:57:12,495 INFO  [org.jboss.as.cli] (Controller Boot Thread) WFLYCLI0001: Processing CLI script /tmp/cli-script-1791914227.cli
[0m[0m14:57:12,884 INFO  [org.jboss.as.cli] (Controller Boot Thread) WFLYCLI0005: Done processing CLI script /tmp/cli-script-1791914227.cli
[0m[0m14:57:12,884 INFO  [org.jboss.as.controller] (Controller Boot Thread) WFLYCTL0468: Completed running the commands from the CLI script
[0m[0m14:57:12,884 INFO  [org.jboss.as.controller] (Controller Boot Thread) WFLYCTL0470: Reloading the server to normal mode after execution of the additional commands from the CLI script. This will clear the properties triggering the additional boot cli script functionality if they were set (org.wildfly.internal.cli.boot.hook.script, org.wildfly.internal.cli.boot.hook.reload.skip, org.wildfly.internal.cli.boot.hook.marker.dir), and delete the marker file indicating the server was restarted
[0m[0m14:57:12,894 INFO  [org.jboss.as] (MSC service thread 1-2) WFLYSRV0050: JBoss EAP 8.0 Update 12.0 (WildFly Core 21.0.20.Final-redhat-00001) stopped in 8ms
[0m[0m14:57:12,895 INFO  [org.jboss.as] (MSC service thread 1-1) WFLYSRV0049: JBoss EAP 8.0 Update 12.0 (WildFly Core 21.0.20.Final-redhat-00001) starting
[0m[32m14:57:12,895 DEBUG [org.jboss.as.config] (MSC service thread 1-1) Configured system properties:
	[Standalone] = 
	br.gov.caixa.sisgr.auth.url = https://webservice.acessoseguro.des.corerj.caixa/sisgrauth-web/
	file.encoding = UTF-8
	file.separator = /
	java.class.path = /opt/server/jboss-modules.jar
	java.class.version = 65.0
	java.home = /usr/lib/jvm/java-21-openjdk-21.0.10.0.7-1.el9.x86_64
	java.io.tmpdir = /tmp
	java.library.path = /usr/java/packages/lib:/usr/lib64:/lib64:/lib:/usr/lib
	java.net.preferIPv4Stack = true
	java.runtime.name = OpenJDK Runtime Environment
	java.runtime.version = 21.0.10+7-LTS
	java.security.disableSystemPropertiesFile = true
	java.security.egd = file:/dev/./urandom
	java.security.properties = /opt/server/bin/java.security.override
	java.specification.name = Java Platform API Specification
	java.specification.vendor = Oracle Corporation
	java.specification.version = 21
	java.util.logging.manager = org.jboss.logmanager.LogManager
	java.vendor = Red Hat, Inc.
	java.vendor.url = https://www.redhat.com/
	java.vendor.url.bug = https://access.redhat.com/support/cases/
	java.vendor.version = (Red_Hat-21.0.10.0.7-1)
	java.version = 21.0.10
	java.version.date = 2026-01-20
	java.vm.compressedOopsMode = 32-bit
	java.vm.info = mixed mode, sharing
	java.vm.name = OpenJDK 64-Bit Server VM
	java.vm.specification.name = Java Virtual Machine Specification
	java.vm.specification.vendor = Oracle Corporation
	java.vm.specification.version = 21
	java.vm.vendor = Red Hat, Inc.
	java.vm.version = 21.0.10+7-LTS
	javax.management.builder.initial = org.jboss.as.jmx.PluggableMBeanServerBuilder
	javax.net.ssl.trustStore = /opt/server/standalone/configuration/caixa-truststore-acteste-nprd.jks
	jboss.bind.address = 25.1.38.69
	jboss.bind.address.management = 0.0.0.0
	jboss.bind.address.private = 25.1.38.69
	jboss.home.dir = /opt/server
	jboss.host.name = sihdg-jboss8-tqs-40-hs678
	jboss.messaging.cluster.password = <redacted>
	jboss.messaging.host = 25.1.38.69
	jboss.modules.system.pkgs = jdk.nashorn.api,com.sun.crypto.provider
	jboss.node.name = sihdg-jboss8-tqs-40-hs678
	jboss.qualified.host.name = sihdg-jboss8-tqs-40-hs678
	jboss.server.base.dir = /opt/server/standalone
	jboss.server.config.dir = /opt/server/standalone/configuration
	jboss.server.data.dir = /opt/server/standalone/data
	jboss.server.log.dir = /opt/server/standalone/log
	jboss.server.name = sihdg-jboss8-tqs-40-hs678
	jboss.server.persist.config = true
	jboss.server.temp.dir = /opt/server/standalone/tmp
	jboss.tx.node.id = hdg-jboss8-tqs-40-hs678
	jdk.debug = release
	jdk.serialFilter = maxbytes=10485760;maxdepth=128;maxarray=100000;maxrefs=300000
	line.separator = 

	logging.configuration = file:/opt/server/standalone/configuration/logging.properties
	module.path = /opt/server/modules
	native.encoding = ANSI_X3.4-1968
	org.jboss.boot.log.file = /opt/server/standalone/log/server.log
	org.jboss.resolver.warning = true
	org.wildfly.internal.cli.boot.hook.script.error.file = /tmp/cli-script-error-1791914227.cli
	org.wildfly.internal.cli.boot.hook.script.output.file = /tmp/cli-script-output-1791914227.cli
	org.wildfly.internal.cli.boot.hook.script.properties = /tmp/cli-script-property-1791914227.cli
	org.wildfly.internal.cli.boot.hook.script.warn.file = /tmp/cli-warning-1791914227.log
	os.arch = amd64
	os.name = Linux
	os.version = 6.1.18-200.fc37.x86_64
	path.separator = :
	siaud.INT_URL_API_MANAGER = http://des.web.corerj.caixa:8642/
	siaud.int.siico.api.key = l75b3690bee55a4994a4efb88fe248b4d9
	siaud.int.url.api.manager = http://api.des.caixa:8080/
	siaud.int.url.legado = https://des.web.corerj.caixa:8605/siaud/
	stderr.encoding = ANSI_X3.4-1968
	stdout.encoding = ANSI_X3.4-1968
	sun.arch.data.model = 64
	sun.boot.library.path = /usr/lib/jvm/java-21-openjdk-21.0.10.0.7-1.el9.x86_64/lib
	sun.cpu.endian = little
	sun.io.unicode.encoding = UnicodeLittle
	sun.java.command = /opt/server/jboss-modules.jar -mp /opt/server/modules org.jboss.as.standalone -Djboss.home.dir=/opt/server -Djboss.server.base.dir=/opt/server/standalone -c standalone.xml -Djboss.messaging.host=25.1.38.69 -Djboss.messaging.cluster.password=<redacted> --start-mode=admin-only -Dorg.wildfly.internal.cli.boot.hook.script=/tmp/cli-script-1791914227.cli -Dorg.wildfly.internal.cli.boot.hook.marker.dir=/tmp/cli-boot-reload-marker-1791914227 -Dorg.wildfly.internal.cli.boot.hook.script.properties=/tmp/cli-script-property-1791914227.cli -Dorg.wildfly.internal.cli.boot.hook.script.error.file=/tmp/cli-script-error-1791914227.cli -Dorg.wildfly.internal.cli.boot.hook.script.warn.file=/tmp/cli-warning-1791914227.log -Dorg.wildfly.internal.cli.boot.hook.script.output.file=/tmp/cli-script-output-1791914227.cli -Djboss.node.name=sihdg-jboss8-tqs-40-hs678 -Djboss.tx.node.id=hdg-jboss8-tqs-40-hs678 -bprivate 25.1.38.69 -b 25.1.38.69 -bmanagement 0.0.0.0 -Dwildfly.statistics-enabled=true
	sun.java.launcher = SUN_STANDARD
	sun.jnu.encoding = ANSI_X3.4-1968
	sun.management.compiler = HotSpot 64-Bit Tiered Compilers
	sun.nio.ch.bugLevel = 
	url_key_cloack = https://login.des.caixa/auth
	url_key_cloack_realm = intranet
	url_siaud_acompanhamento = http://localhost:8888/siaud/siaud-acompanhamento-service
	url_siaud_acompanhamentoweb = http://localhost:8888/siaud/acompanhamento
	url_siaud_execucao = http://localhost:8898/siaud
	url_siaud_planejamento = http://localhost:8898/siaud
	url_siico = http://des.web.corerj.caixa:8642/siicorjapi/v1/
	url_sisgr = https://webservice.acessoseguro.sso.des.intra.corerj.caixa/sisgrauth-web/v1/
	user.country = US
	user.dir = /home/jboss
	user.home = /home/jboss
	user.language = en
	user.name = jboss
	user.timezone = America/Sao_Paulo
	wildfly.statistics-enabled = true
[0m[32m14:57:12,896 DEBUG [org.jboss.as.config] (MSC service thread 1-1) VM Arguments: -D[Standalone] -Xlog:gc*:file=/opt/server/standalone/log/gc.log:time,uptimemillis:filecount=5,filesize=3M -Djdk.serialFilter=maxbytes=10485760;maxdepth=128;maxarray=100000;maxrefs=300000 -XX:MaxRAMPercentage=80.0 -XX:+UseParallelGC -XX:MinHeapFreeRatio=10 -XX:MaxHeapFreeRatio=20 -XX:GCTimeRatio=4 -XX:AdaptiveSizePolicyWeight=90 -XX:MetaspaceSize=96m -XX:+ExitOnOutOfMemoryError -Djava.security.egd=file:/dev/./urandom -Djava.net.preferIPv4Stack=true -Djboss.modules.system.pkgs=jdk.nashorn.api,com.sun.crypto.provider -Djavax.net.ssl.trustStore=/opt/server/standalone/configuration/caixa-truststore-acteste-nprd.jks -Djava.security.properties=/opt/server/bin/java.security.override -Djava.security.disableSystemPropertiesFile=true --add-exports=java.desktop/sun.awt=ALL-UNNAMED --add-exports=java.naming/com.sun.jndi.ldap=ALL-UNNAMED --add-exports=java.naming/com.sun.jndi.url.ldap=ALL-UNNAMED --add-exports=java.naming/com.sun.jndi.url.ldaps=ALL-UNNAMED --add-exports=jdk.naming.dns/com.sun.jndi.dns=ALL-UNNAMED --add-opens=java.base/java.lang=ALL-UNNAMED --add-opens=java.base/java.lang.invoke=ALL-UNNAMED --add-opens=java.base/java.lang.reflect=ALL-UNNAMED --add-opens=java.base/java.io=ALL-UNNAMED --add-opens=java.base/java.net=ALL-UNNAMED --add-opens=java.base/java.security=ALL-UNNAMED --add-opens=java.base/java.util=ALL-UNNAMED --add-opens=java.base/java.util.concurrent=ALL-UNNAMED --add-opens=java.management/javax.management=ALL-UNNAMED --add-opens=java.naming/javax.naming=ALL-UNNAMED -Dorg.jboss.boot.log.file=/opt/server/standalone/log/server.log -Dlogging.configuration=file:/opt/server/standalone/configuration/logging.properties 
[0m[0m14:57:13,662 INFO  [org.jboss.as.repository] (ServerService Thread Pool -- 16) WFLYDR0001: Content added at location /opt/server/standalone/data/content/31/d59efd1d799e0c47503eb3b788bb1270496057/content
[0m[0m14:57:13,676 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0039: Creating http management service using socket-binding (management-http)
[0m[0m14:57:13,686 INFO  [org.wildfly.extension.elytron.oidc._private] (ServerService Thread Pool -- 32) WFLYOIDC0001: Activating WildFly Elytron OIDC Subsystem
[0m[0m14:57:13,695 INFO  [org.wildfly.extension.health] (ServerService Thread Pool -- 33) WFLYHEALTH0001: Activating Base Health Subsystem
[0m[0m14:57:13,696 INFO  [org.wildfly.extension.io] (ServerService Thread Pool -- 35) WFLYIO001: Worker 'default' has auto-configured to 2 IO threads with 16 max task threads based on your 1 available processors
[0m[0m14:57:13,759 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 34) WFLYCLINF0001: Activating Infinispan subsystem.
[0m[0m14:57:13,760 INFO  [org.jboss.as.naming] (ServerService Thread Pool -- 40) WFLYNAM0001: Activating Naming Subsystem
[0m[0m14:57:13,761 INFO  [org.jboss.as.jaxrs] (ServerService Thread Pool -- 36) WFLYRS0016: RESTEasy version 6.2.15.Final-redhat-00002
[0m[0m14:57:13,873 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 44) WFLYUT0112: The value 'require-host-http11' attribute in the '/subsystem=undertow/server=default-server/http-listener=default' resource is 'false', which will be ignored. The server now always enforces the RFC 9112 requirement that HTTP/1.1 request messages include a Host header.
[0m[0m14:57:13,961 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0027: Starting deployment of "sihdg-3.18.0.1.ear" (runtime-name: "sihdg-3.18.0.1.ear")
[0m[0m14:57:13,964 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-1) WFLYUT0003: Undertow 2.3.23.SP3-redhat-00001 starting
[0m[33m14:57:14,066 WARN  [org.wildfly.extension.elytron] (MSC service thread 1-1) WFLYELY00023: KeyStore file '/opt/server/standalone/configuration/application.keystore' does not exist. Used blank.
[0m[0m14:57:14,069 INFO  [org.jboss.as.connector] (MSC service thread 1-1) WFLYJCA0009: Starting Jakarta Connectors Subsystem (WildFly/IronJacamar 3.0.14.Final-redhat-00001)
[0m[33m14:57:14,160 WARN  [org.wildfly.extension.elytron] (MSC service thread 1-1) WFLYELY01084: KeyStore /opt/server/standalone/configuration/application.keystore not found, it will be auto-generated on first use with a self-signed certificate for host localhost
[0m[0m14:57:14,164 INFO  [org.jboss.as.naming] (MSC service thread 1-2) WFLYNAM0003: Starting Naming Service
[0m[0m14:57:14,259 INFO  [org.jboss.as.ejb3] (MSC service thread 1-1) WFLYEJB0481: Strict pool slsb-strict-max-pool is using a max instance size of 16 (per class), which is derived from thread worker pool sizing.
[0m[0m14:57:14,266 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-1) WFLYUT0012: Started server default-server.
[0m[0m14:57:14,269 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-2) Queuing requests.
[0m[0m14:57:14,270 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-2) WFLYUT0018: Host default-host starting
[0m[0m14:57:14,270 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-1) WFLYUT0006: Undertow HTTP listener default listening on 0.0.0.0:8080
[0m[0m14:57:14,271 INFO  [org.jboss.as.connector.subsystems.datasources] (ServerService Thread Pool -- 27) WFLYJCA0004: Deploying JDBC-compliant driver class com.microsoft.sqlserver.jdbc.SQLServerDriver (version 12.6)
[0m[0m14:57:14,460 INFO  [org.jboss.as.connector.deployers.jdbc] (MSC service thread 1-2) WFLYJCA0018: Started Driver service with driver-name = sqlserver
[0m[0m14:57:14,473 INFO  [org.jboss.as.server.deployment.scanner] (MSC service thread 1-2) WFLYDS0013: Started FileSystemDeploymentService for directory /opt/server/standalone/deployments
[0m[0m14:57:14,486 INFO  [org.jboss.as.ejb3] (MSC service thread 1-2) WFLYEJB0493: Jakarta Enterprise Beans subsystem suspension complete
[0m[0m14:57:14,591 INFO  [org.jboss.as.connector.subsystems.datasources] (MSC service thread 1-2) WFLYJCA0001: Bound data source [java:jboss/jdbc/sihdgDS]
[0m[0m14:57:15,300 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0207: Starting subdeployment (runtime-name: "sihdg-api.war")
[0m[33m14:57:20,897 WARN  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0001: /content/sihdg-3.18.0.1.ear/sihdg-api.war/WEB-INF/jboss-deployment-structure.xml in subdeployment ignored. jboss-deployment-structure.xml is only parsed for top level deployments.
[0m[0m14:57:21,491 INFO  [org.jboss.as.jpa] (MSC service thread 1-2) WFLYJPA0002: Read persistence.xml for sihdgDS
[0m[0m14:57:21,494 INFO  [org.wildfly.extension.elytron.oidc._private] (MSC service thread 1-2) WFLYOIDC0002: Elytron OIDC Client subsystem override for deployment 'sihdg-api.war'
[0m[0m14:57:21,874 INFO  [org.jipijapa] (MSC service thread 1-1) JIPIORMV6020260: Second level cache enabled for sihdg-3.18.0.1.ear/sihdg-api.war#sihdgDS
[0m[0m14:57:21,971 INFO  [org.jboss.weld.deployer] (MSC service thread 1-2) WFLYWELD0003: Processing weld deployment sihdg-3.18.0.1.ear
[0m[0m14:57:22,263 INFO  [org.hibernate.validator.internal.util.Version] (MSC service thread 1-2) HV000001: Hibernate Validator 8.0.2.Final-redhat-00001
[0m[0m14:57:22,695 INFO  [org.infinispan.CONTAINER] (ServerService Thread Pool -- 46) ISPN000556: Starting user marshaller 'org.wildfly.clustering.infinispan.marshalling.jboss.JBossMarshaller'
[0m[0m14:57:22,866 INFO  [org.jboss.weld.deployer] (MSC service thread 1-2) WFLYWELD0003: Processing weld deployment sihdg-api.war
[0m[0m14:57:22,961 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'GestaoCargaFcAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/GestaoCargaFcAS!br.gov.caixa.bsb.sihdg.core.service.GestaoCargaFcAS
	java:app/sihdg-api/GestaoCargaFcAS!br.gov.caixa.bsb.sihdg.core.service.GestaoCargaFcAS
	java:module/GestaoCargaFcAS!br.gov.caixa.bsb.sihdg.core.service.GestaoCargaFcAS
	java:global/sihdg-3.18.0.1/sihdg-api/GestaoCargaFcAS
	java:app/sihdg-api/GestaoCargaFcAS
	java:module/GestaoCargaFcAS

[0m[0m14:57:22,962 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'MovimentacaoItemDerivativoFcAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/MovimentacaoItemDerivativoFcAS!br.gov.caixa.bsb.sihdg.core.service.MovimentacaoItemDerivativoFcAS
	java:app/sihdg-api/MovimentacaoItemDerivativoFcAS!br.gov.caixa.bsb.sihdg.core.service.MovimentacaoItemDerivativoFcAS
	java:module/MovimentacaoItemDerivativoFcAS!br.gov.caixa.bsb.sihdg.core.service.MovimentacaoItemDerivativoFcAS
	java:global/sihdg-3.18.0.1/sihdg-api/MovimentacaoItemDerivativoFcAS
	java:app/sihdg-api/MovimentacaoItemDerivativoFcAS
	java:module/MovimentacaoItemDerivativoFcAS

[0m[0m14:57:22,962 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'CtcfAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/CtcfAS!br.gov.caixa.bsb.sihdg.core.service.CtcfAS
	java:app/sihdg-api/CtcfAS!br.gov.caixa.bsb.sihdg.core.service.CtcfAS
	java:module/CtcfAS!br.gov.caixa.bsb.sihdg.core.service.CtcfAS
	java:global/sihdg-3.18.0.1/sihdg-api/CtcfAS
	java:app/sihdg-api/CtcfAS
	java:module/CtcfAS

[0m[0m14:57:22,962 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'RelatorioAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/RelatorioAS!br.gov.caixa.bsb.sihdg.core.service.RelatorioAS
	java:app/sihdg-api/RelatorioAS!br.gov.caixa.bsb.sihdg.core.service.RelatorioAS
	java:module/RelatorioAS!br.gov.caixa.bsb.sihdg.core.service.RelatorioAS
	java:global/sihdg-3.18.0.1/sihdg-api/RelatorioAS
	java:app/sihdg-api/RelatorioAS
	java:module/RelatorioAS

[0m[0m14:57:22,962 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'MovimentacaoTransacaoAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/MovimentacaoTransacaoAS!br.gov.caixa.bsb.sihdg.core.service.MovimentacaoTransacaoAS
	java:app/sihdg-api/MovimentacaoTransacaoAS!br.gov.caixa.bsb.sihdg.core.service.MovimentacaoTransacaoAS
	java:module/MovimentacaoTransacaoAS!br.gov.caixa.bsb.sihdg.core.service.MovimentacaoTransacaoAS
	java:global/sihdg-3.18.0.1/sihdg-api/MovimentacaoTransacaoAS
	java:app/sihdg-api/MovimentacaoTransacaoAS
	java:module/MovimentacaoTransacaoAS

[0m[0m14:57:22,962 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'SafraFcAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/SafraFcAS!br.gov.caixa.bsb.sihdg.core.service.SafraFcAS
	java:app/sihdg-api/SafraFcAS!br.gov.caixa.bsb.sihdg.core.service.SafraFcAS
	java:module/SafraFcAS!br.gov.caixa.bsb.sihdg.core.service.SafraFcAS
	java:global/sihdg-3.18.0.1/sihdg-api/SafraFcAS
	java:app/sihdg-api/SafraFcAS
	java:module/SafraFcAS

[0m[0m14:57:22,962 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'DerivativoAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/DerivativoAS!br.gov.caixa.bsb.sihdg.core.service.DerivativoAS
	java:app/sihdg-api/DerivativoAS!br.gov.caixa.bsb.sihdg.core.service.DerivativoAS
	java:module/DerivativoAS!br.gov.caixa.bsb.sihdg.core.service.DerivativoAS
	java:global/sihdg-3.18.0.1/sihdg-api/DerivativoAS
	java:app/sihdg-api/DerivativoAS
	java:module/DerivativoAS

[0m[0m14:57:22,962 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'MovimentacaoTransacaoFcAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/MovimentacaoTransacaoFcAS!br.gov.caixa.bsb.sihdg.core.service.MovimentacaoTransacaoFcAS
	java:app/sihdg-api/MovimentacaoTransacaoFcAS!br.gov.caixa.bsb.sihdg.core.service.MovimentacaoTransacaoFcAS
	java:module/MovimentacaoTransacaoFcAS!br.gov.caixa.bsb.sihdg.core.service.MovimentacaoTransacaoFcAS
	java:global/sihdg-3.18.0.1/sihdg-api/MovimentacaoTransacaoFcAS
	java:app/sihdg-api/MovimentacaoTransacaoFcAS
	java:module/MovimentacaoTransacaoFcAS

[0m[0m14:57:22,962 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'LogImportacaoSiapcAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/LogImportacaoSiapcAS!br.gov.caixa.bsb.sihdg.core.service.LogImportacaoSiapcAS
	java:app/sihdg-api/LogImportacaoSiapcAS!br.gov.caixa.bsb.sihdg.core.service.LogImportacaoSiapcAS
	java:module/LogImportacaoSiapcAS!br.gov.caixa.bsb.sihdg.core.service.LogImportacaoSiapcAS
	java:global/sihdg-3.18.0.1/sihdg-api/LogImportacaoSiapcAS
	java:app/sihdg-api/LogImportacaoSiapcAS
	java:module/LogImportacaoSiapcAS

[0m[0m14:57:22,962 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'PerfilAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/PerfilAS!br.gov.caixa.arquitetura.javaee.core.seguranca.PerfilAS
	java:app/sihdg-api/PerfilAS!br.gov.caixa.arquitetura.javaee.core.seguranca.PerfilAS
	java:module/PerfilAS!br.gov.caixa.arquitetura.javaee.core.seguranca.PerfilAS
	java:global/sihdg-3.18.0.1/sihdg-api/PerfilAS
	java:app/sihdg-api/PerfilAS
	java:module/PerfilAS

[0m[0m14:57:22,962 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ItemDerivativoAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ItemDerivativoAS!br.gov.caixa.bsb.sihdg.core.service.ItemDerivativoAS
	java:app/sihdg-api/ItemDerivativoAS!br.gov.caixa.bsb.sihdg.core.service.ItemDerivativoAS
	java:module/ItemDerivativoAS!br.gov.caixa.bsb.sihdg.core.service.ItemDerivativoAS
	java:global/sihdg-3.18.0.1/sihdg-api/ItemDerivativoAS
	java:app/sihdg-api/ItemDerivativoAS
	java:module/ItemDerivativoAS

[0m[0m14:57:22,962 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'TabelasAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/TabelasAS!br.gov.caixa.bsb.sihdg.core.service.TabelasAS
	java:app/sihdg-api/TabelasAS!br.gov.caixa.bsb.sihdg.core.service.TabelasAS
	java:module/TabelasAS!br.gov.caixa.bsb.sihdg.core.service.TabelasAS
	java:global/sihdg-3.18.0.1/sihdg-api/TabelasAS
	java:app/sihdg-api/TabelasAS
	java:module/TabelasAS

[0m[0m14:57:22,962 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'SafraAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/SafraAS!br.gov.caixa.bsb.sihdg.core.service.SafraAS
	java:app/sihdg-api/SafraAS!br.gov.caixa.bsb.sihdg.core.service.SafraAS
	java:module/SafraAS!br.gov.caixa.bsb.sihdg.core.service.SafraAS
	java:global/sihdg-3.18.0.1/sihdg-api/SafraAS
	java:app/sihdg-api/SafraAS
	java:module/SafraAS

[0m[0m14:57:22,962 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ContratoDesignadoPrograma1AS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ContratoDesignadoPrograma1AS!br.gov.caixa.bsb.sihdg.core.service.ContratoDesignadoPrograma1AS
	java:app/sihdg-api/ContratoDesignadoPrograma1AS!br.gov.caixa.bsb.sihdg.core.service.ContratoDesignadoPrograma1AS
	java:module/ContratoDesignadoPrograma1AS!br.gov.caixa.bsb.sihdg.core.service.ContratoDesignadoPrograma1AS
	java:global/sihdg-3.18.0.1/sihdg-api/ContratoDesignadoPrograma1AS
	java:app/sihdg-api/ContratoDesignadoPrograma1AS
	java:module/ContratoDesignadoPrograma1AS

[0m[0m14:57:22,963 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ParametroEventoAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ParametroEventoAS!br.gov.caixa.bsb.sihdg.core.service.ParametroEventoAS
	java:app/sihdg-api/ParametroEventoAS!br.gov.caixa.bsb.sihdg.core.service.ParametroEventoAS
	java:module/ParametroEventoAS!br.gov.caixa.bsb.sihdg.core.service.ParametroEventoAS
	java:global/sihdg-3.18.0.1/sihdg-api/ParametroEventoAS
	java:app/sihdg-api/ParametroEventoAS
	java:module/ParametroEventoAS

[0m[0m14:57:22,963 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'HistoricoCargaAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/HistoricoCargaAS!br.gov.caixa.bsb.sihdg.core.service.HistoricoCargaAS
	java:app/sihdg-api/HistoricoCargaAS!br.gov.caixa.bsb.sihdg.core.service.HistoricoCargaAS
	java:module/HistoricoCargaAS!br.gov.caixa.bsb.sihdg.core.service.HistoricoCargaAS
	java:global/sihdg-3.18.0.1/sihdg-api/HistoricoCargaAS
	java:app/sihdg-api/HistoricoCargaAS
	java:module/HistoricoCargaAS

[0m[0m14:57:22,963 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ProgramaAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ProgramaAS!br.gov.caixa.bsb.sihdg.core.service.ProgramaAS
	java:app/sihdg-api/ProgramaAS!br.gov.caixa.bsb.sihdg.core.service.ProgramaAS
	java:module/ProgramaAS!br.gov.caixa.bsb.sihdg.core.service.ProgramaAS
	java:global/sihdg-3.18.0.1/sihdg-api/ProgramaAS
	java:app/sihdg-api/ProgramaAS
	java:module/ProgramaAS

[0m[0m14:57:22,963 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'CtcfHabitacaoAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/CtcfHabitacaoAS!br.gov.caixa.bsb.sihdg.core.service.CtcfHabitacaoAS
	java:app/sihdg-api/CtcfHabitacaoAS!br.gov.caixa.bsb.sihdg.core.service.CtcfHabitacaoAS
	java:module/CtcfHabitacaoAS!br.gov.caixa.bsb.sihdg.core.service.CtcfHabitacaoAS
	java:global/sihdg-3.18.0.1/sihdg-api/CtcfHabitacaoAS
	java:app/sihdg-api/CtcfHabitacaoAS
	java:module/CtcfHabitacaoAS

[0m[0m14:57:22,963 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'VencimentoItemDerivativoTask' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/VencimentoItemDerivativoTask!br.gov.caixa.bsb.sihdg.core.service.jobs.VencimentoItemDerivativoTask
	java:app/sihdg-api/VencimentoItemDerivativoTask!br.gov.caixa.bsb.sihdg.core.service.jobs.VencimentoItemDerivativoTask
	java:module/VencimentoItemDerivativoTask!br.gov.caixa.bsb.sihdg.core.service.jobs.VencimentoItemDerivativoTask
	java:global/sihdg-3.18.0.1/sihdg-api/VencimentoItemDerivativoTask
	java:app/sihdg-api/VencimentoItemDerivativoTask
	java:module/VencimentoItemDerivativoTask

[0m[0m14:57:22,963 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ProcessarStatusDerivativoTask' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ProcessarStatusDerivativoTask!br.gov.caixa.bsb.sihdg.core.service.jobs.ProcessarStatusDerivativoTask
	java:app/sihdg-api/ProcessarStatusDerivativoTask!br.gov.caixa.bsb.sihdg.core.service.jobs.ProcessarStatusDerivativoTask
	java:module/ProcessarStatusDerivativoTask!br.gov.caixa.bsb.sihdg.core.service.jobs.ProcessarStatusDerivativoTask
	java:global/sihdg-3.18.0.1/sihdg-api/ProcessarStatusDerivativoTask
	java:app/sihdg-api/ProcessarStatusDerivativoTask
	java:module/ProcessarStatusDerivativoTask

[0m[0m14:57:22,963 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'RegistroEfetividadeAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/RegistroEfetividadeAS!br.gov.caixa.bsb.sihdg.core.service.RegistroEfetividadeAS
	java:app/sihdg-api/RegistroEfetividadeAS!br.gov.caixa.bsb.sihdg.core.service.RegistroEfetividadeAS
	java:module/RegistroEfetividadeAS!br.gov.caixa.bsb.sihdg.core.service.RegistroEfetividadeAS
	java:global/sihdg-3.18.0.1/sihdg-api/RegistroEfetividadeAS
	java:app/sihdg-api/RegistroEfetividadeAS
	java:module/RegistroEfetividadeAS

[0m[0m14:57:22,963 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'RegistroContabilidadeAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/RegistroContabilidadeAS!br.gov.caixa.bsb.sihdg.core.service.RegistroContabilidadeAS
	java:app/sihdg-api/RegistroContabilidadeAS!br.gov.caixa.bsb.sihdg.core.service.RegistroContabilidadeAS
	java:module/RegistroContabilidadeAS!br.gov.caixa.bsb.sihdg.core.service.RegistroContabilidadeAS
	java:global/sihdg-3.18.0.1/sihdg-api/RegistroContabilidadeAS
	java:app/sihdg-api/RegistroContabilidadeAS
	java:module/RegistroContabilidadeAS

[0m[0m14:57:22,963 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'HistoricoContratoPrograma1AS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/HistoricoContratoPrograma1AS!br.gov.caixa.bsb.sihdg.core.service.HistoricoContratoPrograma1AS
	java:app/sihdg-api/HistoricoContratoPrograma1AS!br.gov.caixa.bsb.sihdg.core.service.HistoricoContratoPrograma1AS
	java:module/HistoricoContratoPrograma1AS!br.gov.caixa.bsb.sihdg.core.service.HistoricoContratoPrograma1AS
	java:global/sihdg-3.18.0.1/sihdg-api/HistoricoContratoPrograma1AS
	java:app/sihdg-api/HistoricoContratoPrograma1AS
	java:module/HistoricoContratoPrograma1AS

[0m[0m14:57:22,963 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'HistoricoCargaFcAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/HistoricoCargaFcAS!br.gov.caixa.bsb.sihdg.core.service.HistoricoCargaFcAS
	java:app/sihdg-api/HistoricoCargaFcAS!br.gov.caixa.bsb.sihdg.core.service.HistoricoCargaFcAS
	java:module/HistoricoCargaFcAS!br.gov.caixa.bsb.sihdg.core.service.HistoricoCargaFcAS
	java:global/sihdg-3.18.0.1/sihdg-api/HistoricoCargaFcAS
	java:app/sihdg-api/HistoricoCargaFcAS
	java:module/HistoricoCargaFcAS

[0m[0m14:57:22,963 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'AtualizacaoCurvaAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/AtualizacaoCurvaAS!br.gov.caixa.bsb.sihdg.core.service.AtualizacaoCurvaAS
	java:app/sihdg-api/AtualizacaoCurvaAS!br.gov.caixa.bsb.sihdg.core.service.AtualizacaoCurvaAS
	java:module/AtualizacaoCurvaAS!br.gov.caixa.bsb.sihdg.core.service.AtualizacaoCurvaAS
	java:global/sihdg-3.18.0.1/sihdg-api/AtualizacaoCurvaAS
	java:app/sihdg-api/AtualizacaoCurvaAS
	java:module/AtualizacaoCurvaAS

[0m[0m14:57:22,963 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'PerfilRecursoAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/PerfilRecursoAS!br.gov.caixa.arquitetura.javaee.core.seguranca.PerfilRecursoAS
	java:app/sihdg-api/PerfilRecursoAS!br.gov.caixa.arquitetura.javaee.core.seguranca.PerfilRecursoAS
	java:module/PerfilRecursoAS!br.gov.caixa.arquitetura.javaee.core.seguranca.PerfilRecursoAS
	java:global/sihdg-3.18.0.1/sihdg-api/PerfilRecursoAS
	java:app/sihdg-api/PerfilRecursoAS
	java:module/PerfilRecursoAS

[0m[0m14:57:22,963 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ParametroChoqueAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ParametroChoqueAS!br.gov.caixa.bsb.sihdg.core.service.ParametroChoqueAS
	java:app/sihdg-api/ParametroChoqueAS!br.gov.caixa.bsb.sihdg.core.service.ParametroChoqueAS
	java:module/ParametroChoqueAS!br.gov.caixa.bsb.sihdg.core.service.ParametroChoqueAS
	java:global/sihdg-3.18.0.1/sihdg-api/ParametroChoqueAS
	java:app/sihdg-api/ParametroChoqueAS
	java:module/ParametroChoqueAS

[0m[0m14:57:22,964 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'SolicitacaoHabilitacaoDerivativoAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/SolicitacaoHabilitacaoDerivativoAS!br.gov.caixa.bsb.sihdg.core.service.SolicitacaoHabilitacaoDerivativoAS
	java:app/sihdg-api/SolicitacaoHabilitacaoDerivativoAS!br.gov.caixa.bsb.sihdg.core.service.SolicitacaoHabilitacaoDerivativoAS
	java:module/SolicitacaoHabilitacaoDerivativoAS!br.gov.caixa.bsb.sihdg.core.service.SolicitacaoHabilitacaoDerivativoAS
	java:global/sihdg-3.18.0.1/sihdg-api/SolicitacaoHabilitacaoDerivativoAS
	java:app/sihdg-api/SolicitacaoHabilitacaoDerivativoAS
	java:module/SolicitacaoHabilitacaoDerivativoAS

[0m[0m14:57:22,964 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'AtualizadorCacheAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/AtualizadorCacheAS!br.gov.caixa.arquitetura.javaee.core.util.AtualizadorCacheAS
	java:app/sihdg-api/AtualizadorCacheAS!br.gov.caixa.arquitetura.javaee.core.util.AtualizadorCacheAS
	java:module/AtualizadorCacheAS!br.gov.caixa.arquitetura.javaee.core.util.AtualizadorCacheAS
	java:global/sihdg-3.18.0.1/sihdg-api/AtualizadorCacheAS
	java:app/sihdg-api/AtualizadorCacheAS
	java:module/AtualizadorCacheAS

[0m[0m14:57:22,964 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ExecucaoAtualizacaoDaCurvaAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ExecucaoAtualizacaoDaCurvaAS!br.gov.caixa.bsb.sihdg.core.service.ExecucaoAtualizacaoDaCurvaAS
	java:app/sihdg-api/ExecucaoAtualizacaoDaCurvaAS!br.gov.caixa.bsb.sihdg.core.service.ExecucaoAtualizacaoDaCurvaAS
	java:module/ExecucaoAtualizacaoDaCurvaAS!br.gov.caixa.bsb.sihdg.core.service.ExecucaoAtualizacaoDaCurvaAS
	java:global/sihdg-3.18.0.1/sihdg-api/ExecucaoAtualizacaoDaCurvaAS
	java:app/sihdg-api/ExecucaoAtualizacaoDaCurvaAS
	java:module/ExecucaoAtualizacaoDaCurvaAS

[0m[0m14:57:22,964 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ArquivoSinafAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ArquivoSinafAS!br.gov.caixa.bsb.sihdg.core.service.ArquivoSinafAS
	java:app/sihdg-api/ArquivoSinafAS!br.gov.caixa.bsb.sihdg.core.service.ArquivoSinafAS
	java:module/ArquivoSinafAS!br.gov.caixa.bsb.sihdg.core.service.ArquivoSinafAS
	java:global/sihdg-3.18.0.1/sihdg-api/ArquivoSinafAS
	java:app/sihdg-api/ArquivoSinafAS
	java:module/ArquivoSinafAS

[0m[0m14:57:22,964 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'TaxaCdiAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/TaxaCdiAS!br.gov.caixa.bsb.sihdg.core.service.TaxaCdiAS
	java:app/sihdg-api/TaxaCdiAS!br.gov.caixa.bsb.sihdg.core.service.TaxaCdiAS
	java:module/TaxaCdiAS!br.gov.caixa.bsb.sihdg.core.service.TaxaCdiAS
	java:global/sihdg-3.18.0.1/sihdg-api/TaxaCdiAS
	java:app/sihdg-api/TaxaCdiAS
	java:module/TaxaCdiAS

[0m[0m14:57:22,964 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'SecurityConfig' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/SecurityConfig!br.gov.caixa.arquitetura.javaee.core.comum.config.seguranca.SecurityConfig
	java:app/sihdg-api/SecurityConfig!br.gov.caixa.arquitetura.javaee.core.comum.config.seguranca.SecurityConfig
	java:module/SecurityConfig!br.gov.caixa.arquitetura.javaee.core.comum.config.seguranca.SecurityConfig
	java:global/sihdg-3.18.0.1/sihdg-api/SecurityConfig
	java:app/sihdg-api/SecurityConfig
	java:module/SecurityConfig

[0m[0m14:57:22,964 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'TrilhaAuditoriaAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/TrilhaAuditoriaAS!br.gov.caixa.bsb.sihdg.core.service.TrilhaAuditoriaAS
	java:app/sihdg-api/TrilhaAuditoriaAS!br.gov.caixa.bsb.sihdg.core.service.TrilhaAuditoriaAS
	java:module/TrilhaAuditoriaAS!br.gov.caixa.bsb.sihdg.core.service.TrilhaAuditoriaAS
	java:global/sihdg-3.18.0.1/sihdg-api/TrilhaAuditoriaAS
	java:app/sihdg-api/TrilhaAuditoriaAS
	java:module/TrilhaAuditoriaAS

[0m[0m14:57:22,964 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ProspectivaSolicitacaoAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ProspectivaSolicitacaoAS!br.gov.caixa.bsb.sihdg.core.service.ProspectivaSolicitacaoAS
	java:app/sihdg-api/ProspectivaSolicitacaoAS!br.gov.caixa.bsb.sihdg.core.service.ProspectivaSolicitacaoAS
	java:module/ProspectivaSolicitacaoAS!br.gov.caixa.bsb.sihdg.core.service.ProspectivaSolicitacaoAS
	java:global/sihdg-3.18.0.1/sihdg-api/ProspectivaSolicitacaoAS
	java:app/sihdg-api/ProspectivaSolicitacaoAS
	java:module/ProspectivaSolicitacaoAS

[0m[0m14:57:22,964 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'AtualizacaoCurvaTask' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/AtualizacaoCurvaTask!br.gov.caixa.bsb.sihdg.core.service.jobs.AtualizacaoCurvaTask
	java:app/sihdg-api/AtualizacaoCurvaTask!br.gov.caixa.bsb.sihdg.core.service.jobs.AtualizacaoCurvaTask
	java:module/AtualizacaoCurvaTask!br.gov.caixa.bsb.sihdg.core.service.jobs.AtualizacaoCurvaTask
	java:global/sihdg-3.18.0.1/sihdg-api/AtualizacaoCurvaTask
	java:app/sihdg-api/AtualizacaoCurvaTask
	java:module/AtualizacaoCurvaTask

[0m[0m14:57:22,964 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'CurvaAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/CurvaAS!br.gov.caixa.bsb.sihdg.core.service.CurvaAS
	java:app/sihdg-api/CurvaAS!br.gov.caixa.bsb.sihdg.core.service.CurvaAS
	java:module/CurvaAS!br.gov.caixa.bsb.sihdg.core.service.CurvaAS
	java:global/sihdg-3.18.0.1/sihdg-api/CurvaAS
	java:app/sihdg-api/CurvaAS
	java:module/CurvaAS

[0m[0m14:57:22,964 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'CacheConfig' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/CacheConfig!br.gov.caixa.arquitetura.javaee.core.comum.config.cache.CacheConfig
	java:app/sihdg-api/CacheConfig!br.gov.caixa.arquitetura.javaee.core.comum.config.cache.CacheConfig
	java:module/CacheConfig!br.gov.caixa.arquitetura.javaee.core.comum.config.cache.CacheConfig
	java:global/sihdg-3.18.0.1/sihdg-api/CacheConfig
	java:app/sihdg-api/CacheConfig
	java:module/CacheConfig

[0m[0m14:57:22,964 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'FluxoAlmSafraAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/FluxoAlmSafraAS!br.gov.caixa.bsb.sihdg.core.service.FluxoAlmSafraAS
	java:app/sihdg-api/FluxoAlmSafraAS!br.gov.caixa.bsb.sihdg.core.service.FluxoAlmSafraAS
	java:module/FluxoAlmSafraAS!br.gov.caixa.bsb.sihdg.core.service.FluxoAlmSafraAS
	java:global/sihdg-3.18.0.1/sihdg-api/FluxoAlmSafraAS
	java:app/sihdg-api/FluxoAlmSafraAS
	java:module/FluxoAlmSafraAS

[0m[0m14:57:22,964 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ContratoAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ContratoAS!br.gov.caixa.bsb.sihdg.core.service.ContratoAS
	java:app/sihdg-api/ContratoAS!br.gov.caixa.bsb.sihdg.core.service.ContratoAS
	java:module/ContratoAS!br.gov.caixa.bsb.sihdg.core.service.ContratoAS
	java:global/sihdg-3.18.0.1/sihdg-api/ContratoAS
	java:app/sihdg-api/ContratoAS
	java:module/ContratoAS

[0m[0m14:57:22,964 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'MovimentacaoItemDerivativoAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/MovimentacaoItemDerivativoAS!br.gov.caixa.bsb.sihdg.core.service.MovimentacaoItemDerivativoAS
	java:app/sihdg-api/MovimentacaoItemDerivativoAS!br.gov.caixa.bsb.sihdg.core.service.MovimentacaoItemDerivativoAS
	java:module/MovimentacaoItemDerivativoAS!br.gov.caixa.bsb.sihdg.core.service.MovimentacaoItemDerivativoAS
	java:global/sihdg-3.18.0.1/sihdg-api/MovimentacaoItemDerivativoAS
	java:app/sihdg-api/MovimentacaoItemDerivativoAS
	java:module/MovimentacaoItemDerivativoAS

[0m[0m14:57:22,964 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'OrdemCompraAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/OrdemCompraAS!br.gov.caixa.bsb.sihdg.core.service.OrdemCompraAS
	java:app/sihdg-api/OrdemCompraAS!br.gov.caixa.bsb.sihdg.core.service.OrdemCompraAS
	java:module/OrdemCompraAS!br.gov.caixa.bsb.sihdg.core.service.OrdemCompraAS
	java:global/sihdg-3.18.0.1/sihdg-api/OrdemCompraAS
	java:app/sihdg-api/OrdemCompraAS
	java:module/OrdemCompraAS

[0m[0m14:57:22,965 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ProgramaFluxoCaixaAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ProgramaFluxoCaixaAS!br.gov.caixa.bsb.sihdg.core.service.ProgramaFluxoCaixaAS
	java:app/sihdg-api/ProgramaFluxoCaixaAS!br.gov.caixa.bsb.sihdg.core.service.ProgramaFluxoCaixaAS
	java:module/ProgramaFluxoCaixaAS!br.gov.caixa.bsb.sihdg.core.service.ProgramaFluxoCaixaAS
	java:global/sihdg-3.18.0.1/sihdg-api/ProgramaFluxoCaixaAS
	java:app/sihdg-api/ProgramaFluxoCaixaAS
	java:module/ProgramaFluxoCaixaAS

[0m[0m14:57:22,965 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ItemDerivativoGerencialAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ItemDerivativoGerencialAS!br.gov.caixa.bsb.sihdg.core.service.ItemDerivativoGerencialAS
	java:app/sihdg-api/ItemDerivativoGerencialAS!br.gov.caixa.bsb.sihdg.core.service.ItemDerivativoGerencialAS
	java:module/ItemDerivativoGerencialAS!br.gov.caixa.bsb.sihdg.core.service.ItemDerivativoGerencialAS
	java:global/sihdg-3.18.0.1/sihdg-api/ItemDerivativoGerencialAS
	java:app/sihdg-api/ItemDerivativoGerencialAS
	java:module/ItemDerivativoGerencialAS

[0m[0m14:57:22,965 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'GestaoCargaAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/GestaoCargaAS!br.gov.caixa.bsb.sihdg.core.service.GestaoCargaAS
	java:app/sihdg-api/GestaoCargaAS!br.gov.caixa.bsb.sihdg.core.service.GestaoCargaAS
	java:module/GestaoCargaAS!br.gov.caixa.bsb.sihdg.core.service.GestaoCargaAS
	java:global/sihdg-3.18.0.1/sihdg-api/GestaoCargaAS
	java:app/sihdg-api/GestaoCargaAS
	java:module/GestaoCargaAS

[0m[0m14:57:22,965 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ProdutoEventoAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ProdutoEventoAS!br.gov.caixa.bsb.sihdg.core.service.ProdutoEventoAS
	java:app/sihdg-api/ProdutoEventoAS!br.gov.caixa.bsb.sihdg.core.service.ProdutoEventoAS
	java:module/ProdutoEventoAS!br.gov.caixa.bsb.sihdg.core.service.ProdutoEventoAS
	java:global/sihdg-3.18.0.1/sihdg-api/ProdutoEventoAS
	java:app/sihdg-api/ProdutoEventoAS
	java:module/ProdutoEventoAS

[0m[0m14:57:22,965 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ItemDerivativoGerencialFcAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ItemDerivativoGerencialFcAS!br.gov.caixa.bsb.sihdg.core.service.ItemDerivativoGerencialFcAS
	java:app/sihdg-api/ItemDerivativoGerencialFcAS!br.gov.caixa.bsb.sihdg.core.service.ItemDerivativoGerencialFcAS
	java:module/ItemDerivativoGerencialFcAS!br.gov.caixa.bsb.sihdg.core.service.ItemDerivativoGerencialFcAS
	java:global/sihdg-3.18.0.1/sihdg-api/ItemDerivativoGerencialFcAS
	java:app/sihdg-api/ItemDerivativoGerencialFcAS
	java:module/ItemDerivativoGerencialFcAS

[0m[0m14:57:22,965 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'RecursoAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/RecursoAS!br.gov.caixa.arquitetura.javaee.core.seguranca.RecursoAS
	java:app/sihdg-api/RecursoAS!br.gov.caixa.arquitetura.javaee.core.seguranca.RecursoAS
	java:module/RecursoAS!br.gov.caixa.arquitetura.javaee.core.seguranca.RecursoAS
	java:global/sihdg-3.18.0.1/sihdg-api/RecursoAS
	java:app/sihdg-api/RecursoAS
	java:module/RecursoAS

[0m[0m14:57:22,965 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ContratoTemporarioAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ContratoTemporarioAS!br.gov.caixa.bsb.sihdg.core.service.ContratoTemporarioAS
	java:app/sihdg-api/ContratoTemporarioAS!br.gov.caixa.bsb.sihdg.core.service.ContratoTemporarioAS
	java:module/ContratoTemporarioAS!br.gov.caixa.bsb.sihdg.core.service.ContratoTemporarioAS
	java:global/sihdg-3.18.0.1/sihdg-api/ContratoTemporarioAS
	java:app/sihdg-api/ContratoTemporarioAS
	java:module/ContratoTemporarioAS

[0m[0m14:57:22,965 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'AtualizacaoCurvaFcAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/AtualizacaoCurvaFcAS!br.gov.caixa.bsb.sihdg.core.service.AtualizacaoCurvaFcAS
	java:app/sihdg-api/AtualizacaoCurvaFcAS!br.gov.caixa.bsb.sihdg.core.service.AtualizacaoCurvaFcAS
	java:module/AtualizacaoCurvaFcAS!br.gov.caixa.bsb.sihdg.core.service.AtualizacaoCurvaFcAS
	java:global/sihdg-3.18.0.1/sihdg-api/AtualizacaoCurvaFcAS
	java:app/sihdg-api/AtualizacaoCurvaFcAS
	java:module/AtualizacaoCurvaFcAS

[0m[0m14:57:22,965 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'GestaoEfetividadeAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/GestaoEfetividadeAS!br.gov.caixa.bsb.sihdg.core.service.GestaoEfetividadeAS
	java:app/sihdg-api/GestaoEfetividadeAS!br.gov.caixa.bsb.sihdg.core.service.GestaoEfetividadeAS
	java:module/GestaoEfetividadeAS!br.gov.caixa.bsb.sihdg.core.service.GestaoEfetividadeAS
	java:global/sihdg-3.18.0.1/sihdg-api/GestaoEfetividadeAS
	java:app/sihdg-api/GestaoEfetividadeAS
	java:module/GestaoEfetividadeAS

[0m[0m14:57:22,965 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ControleCacheTask' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ControleCacheTask!br.gov.caixa.arquitetura.javaee.core.comum.servico.ControleCacheTask
	java:app/sihdg-api/ControleCacheTask!br.gov.caixa.arquitetura.javaee.core.comum.servico.ControleCacheTask
	java:module/ControleCacheTask!br.gov.caixa.arquitetura.javaee.core.comum.servico.ControleCacheTask
	java:global/sihdg-3.18.0.1/sihdg-api/ControleCacheTask
	java:app/sihdg-api/ControleCacheTask
	java:module/ControleCacheTask

[0m[0m14:57:22,965 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: JNDI bindings for session bean named 'ControleCacheAS' in deployment unit 'subdeployment "sihdg-api.war" of deployment "sihdg-3.18.0.1.ear"' are as follows:

	java:global/sihdg-3.18.0.1/sihdg-api/ControleCacheAS!br.gov.caixa.arquitetura.javaee.core.util.ControleCacheAS
	java:app/sihdg-api/ControleCacheAS!br.gov.caixa.arquitetura.javaee.core.util.ControleCacheAS
	java:module/ControleCacheAS!br.gov.caixa.arquitetura.javaee.core.util.ControleCacheAS
	java:global/sihdg-3.18.0.1/sihdg-api/ControleCacheAS
	java:app/sihdg-api/ControleCacheAS
	java:module/ControleCacheAS

[0m[0m14:57:23,182 INFO  [org.jboss.weld.Version] (MSC service thread 1-2) WELD-000900: 5.1.6 (redhat)
[0m[0m14:57:23,678 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 46) WFLYJPA0010: Starting Persistence Unit (phase 1 of 2) Service 'sihdg-3.18.0.1.ear/sihdg-api.war#sihdgDS'
[0m[0m14:57:23,689 INFO  [org.hibernate.jpa.internal.util.LogHelper] (ServerService Thread Pool -- 46) HHH000204: Processing PersistenceUnitInfo [name: sihdgDS]
[0m[33m14:57:23,860 WARN  [org.jboss.as.ejb3] (MSC service thread 1-1) WFLYEJB0131: Jakarta Enterprise Beans br.gov.caixa.bsb.sihdg.core.service.RegistroContabilidadeAS should not have a final or static method (toSingleton)
[0m[0m14:57:23,868 INFO  [org.hibernate.Version] (ServerService Thread Pool -- 46) HHH000412: Hibernate ORM core version 6.2.49.Final-redhat-00001
[0m[0m14:57:23,870 INFO  [org.hibernate.cfg.Environment] (ServerService Thread Pool -- 46) HHH000406: Using bytecode reflection optimizer
[0m[33m14:57:23,976 WARN  [org.hibernate.orm.deprecation] (ServerService Thread Pool -- 46) HHH90000025: SQLServer2012Dialect does not need to be specified explicitly using 'hibernate.dialect' (remove the property setting and it will be selected by default)
[0m[33m14:57:23,977 WARN  [org.hibernate.orm.deprecation] (ServerService Thread Pool -- 46) HHH90000026: SQLServer2012Dialect has been deprecated; use org.hibernate.dialect.SQLServerDialect instead
[0m[0m14:57:24,191 INFO  [org.jipijapa] (MSC service thread 1-1) JIPIORMV6020260: Second level cache enabled for sihdg-3.18.0.1.ear/sihdg-api.war#sihdgDS
[0m[0m14:57:24,262 INFO  [org.hibernate.envers.boot.internal.EnversServiceImpl] (ServerService Thread Pool -- 46) Envers integration enabled? : true
[0m[33m14:57:24,374 WARN  [org.jboss.as.jaxrs] (MSC service thread 1-1) WFLYRS0018: Explicit usage of Jackson annotation in a Jakarta RESTful Web Services deployment; the system will disable Jakarta JSON Binding processing for the current deployment. Consider setting the 'resteasy.preferJacksonOverJsonB' property to 'false' to restore Jakarta JSON Binding.
[0m[0m14:57:24,681 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 46) WFLYJPA0010: Starting Persistence Unit (phase 2 of 2) Service 'sihdg-3.18.0.1.ear/sihdg-api.war#sihdgDS'
[0m[0m14:57:26,461 INFO  [org.hibernate.engine.transaction.jta.platform.internal.JtaPlatformInitiator] (ServerService Thread Pool -- 46) HHH000490: Using JTA platform [org.hibernate.engine.transaction.jta.platform.internal.JBossAppServerJtaPlatform]
[0m[0m14:57:32,964 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.config.cache.CacheConfig] (ServerService Thread Pool -- 62) Atualizando o cache inicial ...
[0m[0m14:57:33,079 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Perfil.createQuery
[0m[33m14:57:33,168 WARNING [com.hazelcast.instance.HazelcastInstanceFactory] (ServerService Thread Pool -- 62) Hazelcast is starting in a Java modular environment (Java 9 and newer) but without proper access to required Java packages. Use additional Java arguments to provide Hazelcast access to Java internal API. The internal API access is used to get the best performance results. Arguments to be used:
 --add-modules java.se --add-exports java.base/jdk.internal.ref=ALL-UNNAMED --add-opens java.base/java.lang=ALL-UNNAMED --add-opens java.base/java.nio=ALL-UNNAMED --add-opens java.base/sun.nio.ch=ALL-UNNAMED --add-opens java.management/sun.management=ALL-UNNAMED --add-opens jdk.management/com.sun.management.internal=ALL-UNNAMED
[0m[0m14:57:33,185 INFO  [com.hazelcast.instance.AddressPicker] (ServerService Thread Pool -- 62) [LOCAL] [dev] [3.12.12] Prefer IPv4 stack is true, prefer IPv6 addresses is false
[0m[0m14:57:33,187 INFO  [com.hazelcast.instance.AddressPicker] (ServerService Thread Pool -- 62) [LOCAL] [dev] [3.12.12] Picked [25.1.38.69]:5701, using socket ServerSocket[addr=/0.0.0.0,localport=5701], bind any local is true
[0m[0m14:57:33,259 INFO  [com.hazelcast.system] (ServerService Thread Pool -- 62) [25.1.38.69]:5701 [dev] [3.12.12] Hazelcast 3.12.12 (20210209 - 35096ec) starting at [25.1.38.69]:5701
[0m[0m14:57:33,260 INFO  [com.hazelcast.system] (ServerService Thread Pool -- 62) [25.1.38.69]:5701 [dev] [3.12.12] Copyright (c) 2008-2020, Hazelcast, Inc. All Rights Reserved.
[0m[0m14:57:33,471 INFO  [com.hazelcast.spi.impl.operationservice.impl.BackpressureRegulator] (ServerService Thread Pool -- 62) [25.1.38.69]:5701 [dev] [3.12.12] Backpressure is disabled
[0m[0m14:57:33,784 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:33,785 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:33,785 INFO  [stdout] (ServerService Thread Pool -- 51)         p1_0.CO_PERFIL_ID,
[0m[0m14:57:33,785 INFO  [stdout] (ServerService Thread Pool -- 51)         p1_0.TS_ATLZO_PERFIL,
[0m[0m14:57:33,785 INFO  [stdout] (ServerService Thread Pool -- 51)         p1_0.DE_PERFIL_ACESSO,
[0m[0m14:57:33,785 INFO  [stdout] (ServerService Thread Pool -- 51)         p1_0.NO_PERFIL_ACESSO,
[0m[0m14:57:33,785 INFO  [stdout] (ServerService Thread Pool -- 51)         p1_0.CO_TRMNL_ATLZO_PERFIL,
[0m[0m14:57:33,785 INFO  [stdout] (ServerService Thread Pool -- 51)         p1_0.CO_USUARIO_ATLZO_PERFIL 
[0m[0m14:57:33,785 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:33,785 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB011_PERFIL_ACESSO p1_0 
[0m[0m14:57:33,785 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:33,785 INFO  [stdout] (ServerService Thread Pool -- 51)         p1_0.NO_PERFIL_ACESSO=?
[0m[0m14:57:34,273 INFO  [com.hazelcast.spi.impl.operationexecutor.impl.OperationExecutorImpl] (ServerService Thread Pool -- 62) [25.1.38.69]:5701 [dev] [3.12.12] Starting 2 partition threads and 3 generic threads (1 dedicated for priority tasks)
[0m[0m14:57:34,274 INFO  [com.hazelcast.internal.diagnostics.Diagnostics] (ServerService Thread Pool -- 62) [25.1.38.69]:5701 [dev] [3.12.12] Diagnostics disabled. To enable add -Dhazelcast.diagnostics.enabled=true to the JVM arguments.
[0m[0m14:57:34,276 INFO  [com.hazelcast.core.LifecycleService] (ServerService Thread Pool -- 62) [25.1.38.69]:5701 [dev] [3.12.12] [25.1.38.69]:5701 is STARTING
[0m[33m14:57:34,282 WARNING [com.hazelcast.instance.Node] (ServerService Thread Pool -- 62) [25.1.38.69]:5701 [dev] [3.12.12] No join method is enabled! Starting standalone.
[0m[0m14:57:34,365 INFO  [com.hazelcast.core.LifecycleService] (ServerService Thread Pool -- 62) [25.1.38.69]:5701 [dev] [3.12.12] [25.1.38.69]:5701 is STARTED
[0m[0m14:57:34,366 INFO  [br.gov.caixa.arquitetura.javaee.core.util.AtualizadorCacheAS] (ServerService Thread Pool -- 62) Atualizando o cache de 'PERFIL_RECURSO'
[0m[0m14:57:34,368 INFO  [com.hazelcast.internal.diagnostics.HealthMonitor] (hz._hzInstance_1_dev.HealthMonitor) [25.1.38.69]:5701 [dev] [3.12.12] processors=1, physical.memory.total=2.0G, physical.memory.free=1.3G, swap.space.total=0, swap.space.free=0, heap.memory.used=209.1M, heap.memory.free=6.9M, heap.memory.total=216.0M, heap.memory.max=1.4G, heap.memory.used/total=96.72%, heap.memory.used/max=14.33%, minor.gc.count=0, minor.gc.time=0ms, major.gc.count=0, major.gc.time=0ms, load.process=0.00%, load.system=0.00%, load.systemAverage=8.72, thread.count=134, thread.peakCount=134, cluster.timeDiff=0, event.q.size=0, executor.q.async.size=0, executor.q.client.size=0, executor.q.client.query.size=0, executor.q.client.blocking.size=0, executor.q.query.size=0, executor.q.scheduled.size=0, executor.q.io.size=0, executor.q.system.size=0, executor.q.operations.size=0, executor.q.priorityOperation.size=0, operations.completed.count=1, executor.q.mapLoad.size=0, executor.q.mapLoadAllKeys.size=0, executor.q.cluster.size=0, executor.q.response.size=0, operations.running.count=0, operations.pending.invocations.percentage=0.00%, operations.pending.invocations.count=0, proxy.count=0, clientEndpoint.count=0, connection.active.count=0, client.connection.count=0, connection.count=0
[0m[0m14:57:34,370 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 62) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: PerfilRecurso.createQuery
[0m[0m14:57:34,379 INFO  [stdout] (ServerService Thread Pool -- 62) Hibernate: 
[0m[0m14:57:34,379 INFO  [stdout] (ServerService Thread Pool -- 62)     select
[0m[0m14:57:34,379 INFO  [stdout] (ServerService Thread Pool -- 62)         distinct p2_0.NO_PERFIL_ACESSO 
[0m[0m14:57:34,379 INFO  [stdout] (ServerService Thread Pool -- 62)     from
[0m[0m14:57:34,379 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB013_PERMISSAO_PERFIL p1_0 
[0m[0m14:57:34,379 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,379 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB011_PERFIL_ACESSO p2_0 
[0m[0m14:57:34,379 INFO  [stdout] (ServerService Thread Pool -- 62)             on p2_0.CO_PERFIL_ID=p1_0.CO_PERFIL_ID
[0m[0m14:57:34,592 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 62) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: PerfilRecurso.createQuery
[0m[0m14:57:34,593 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Perfil.consultarPorId
[0m[0m14:57:34,597 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Perfil.consultarPorId
[0m[0m14:57:34,671 INFO  [stdout] (ServerService Thread Pool -- 62) Hibernate: 
[0m[0m14:57:34,671 INFO  [stdout] (ServerService Thread Pool -- 62)     select
[0m[0m14:57:34,671 INFO  [stdout] (ServerService Thread Pool -- 62)         distinct r1_0.NO_RECURSO_FNCNE 
[0m[0m14:57:34,671 INFO  [stdout] (ServerService Thread Pool -- 62)     from
[0m[0m14:57:34,672 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB013_PERMISSAO_PERFIL p1_0 
[0m[0m14:57:34,672 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,672 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:34,672 INFO  [stdout] (ServerService Thread Pool -- 62)             on r1_0.CO_RECURSO_ID=p1_0.CO_RECURSO_ID 
[0m[0m14:57:34,672 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,672 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB011_PERFIL_ACESSO p2_0 
[0m[0m14:57:34,672 INFO  [stdout] (ServerService Thread Pool -- 62)             on p2_0.CO_PERFIL_ID=p1_0.CO_PERFIL_ID 
[0m[0m14:57:34,672 INFO  [stdout] (ServerService Thread Pool -- 62)     where
[0m[0m14:57:34,672 INFO  [stdout] (ServerService Thread Pool -- 62)         (
[0m[0m14:57:34,672 INFO  [stdout] (ServerService Thread Pool -- 62)             p2_0.NO_PERFIL_ACESSO in (?)
[0m[0m14:57:34,672 INFO  [stdout] (ServerService Thread Pool -- 62)         )
[0m[0m14:57:34,675 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Perfil.merge
[0m[0m14:57:34,685 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.createQuery
[0m[0m14:57:34,693 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 62) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: PerfilRecurso.createQuery
[0m[0m14:57:34,694 INFO  [stdout] (ServerService Thread Pool -- 62) Hibernate: 
[0m[0m14:57:34,694 INFO  [stdout] (ServerService Thread Pool -- 62)     select
[0m[0m14:57:34,694 INFO  [stdout] (ServerService Thread Pool -- 62)         distinct r1_0.NO_RECURSO_FNCNE 
[0m[0m14:57:34,695 INFO  [stdout] (ServerService Thread Pool -- 62)     from
[0m[0m14:57:34,695 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB013_PERMISSAO_PERFIL p1_0 
[0m[0m14:57:34,695 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,695 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:34,695 INFO  [stdout] (ServerService Thread Pool -- 62)             on r1_0.CO_RECURSO_ID=p1_0.CO_RECURSO_ID 
[0m[0m14:57:34,695 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,695 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB011_PERFIL_ACESSO p2_0 
[0m[0m14:57:34,695 INFO  [stdout] (ServerService Thread Pool -- 62)             on p2_0.CO_PERFIL_ID=p1_0.CO_PERFIL_ID 
[0m[0m14:57:34,695 INFO  [stdout] (ServerService Thread Pool -- 62)     where
[0m[0m14:57:34,695 INFO  [stdout] (ServerService Thread Pool -- 62)         (
[0m[0m14:57:34,695 INFO  [stdout] (ServerService Thread Pool -- 62)             p2_0.NO_PERFIL_ACESSO in (?)
[0m[0m14:57:34,695 INFO  [stdout] (ServerService Thread Pool -- 62)         )
[0m[0m14:57:34,766 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 62) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: PerfilRecurso.createQuery
[0m[0m14:57:34,767 INFO  [stdout] (ServerService Thread Pool -- 62) Hibernate: 
[0m[0m14:57:34,767 INFO  [stdout] (ServerService Thread Pool -- 62)     select
[0m[0m14:57:34,767 INFO  [stdout] (ServerService Thread Pool -- 62)         distinct r1_0.NO_RECURSO_FNCNE 
[0m[0m14:57:34,767 INFO  [stdout] (ServerService Thread Pool -- 62)     from
[0m[0m14:57:34,767 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB013_PERMISSAO_PERFIL p1_0 
[0m[0m14:57:34,767 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,767 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:34,767 INFO  [stdout] (ServerService Thread Pool -- 62)             on r1_0.CO_RECURSO_ID=p1_0.CO_RECURSO_ID 
[0m[0m14:57:34,767 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,767 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB011_PERFIL_ACESSO p2_0 
[0m[0m14:57:34,767 INFO  [stdout] (ServerService Thread Pool -- 62)             on p2_0.CO_PERFIL_ID=p1_0.CO_PERFIL_ID 
[0m[0m14:57:34,767 INFO  [stdout] (ServerService Thread Pool -- 62)     where
[0m[0m14:57:34,767 INFO  [stdout] (ServerService Thread Pool -- 62)         (
[0m[0m14:57:34,767 INFO  [stdout] (ServerService Thread Pool -- 62)             p2_0.NO_PERFIL_ACESSO in (?)
[0m[0m14:57:34,767 INFO  [stdout] (ServerService Thread Pool -- 62)         )
[0m[0m14:57:34,768 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:34,768 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:34,768 INFO  [stdout] (ServerService Thread Pool -- 51)         distinct c1_0.CO_CONTROLE_ID,
[0m[0m14:57:34,768 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.IC_CONTROLE_ATUALIZACAO,
[0m[0m14:57:34,768 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_CONTROLE_ATUALIZACAO,
[0m[0m14:57:34,768 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_SERVIDOR_APLICACAO 
[0m[0m14:57:34,768 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:34,768 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB014_CONTROLE_ATUALIZACAO c1_0 
[0m[0m14:57:34,768 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:34,768 INFO  [stdout] (ServerService Thread Pool -- 51)         (
[0m[0m14:57:34,768 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_CONTROLE_ATUALIZACAO=?
[0m[0m14:57:34,768 INFO  [stdout] (ServerService Thread Pool -- 51)         ) 
[0m[0m14:57:34,768 INFO  [stdout] (ServerService Thread Pool -- 51)         and (
[0m[0m14:57:34,768 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_SERVIDOR_APLICACAO=?
[0m[0m14:57:34,768 INFO  [stdout] (ServerService Thread Pool -- 51)         )
[0m[0m14:57:34,771 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 62) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: PerfilRecurso.createQuery
[0m[0m14:57:34,772 INFO  [stdout] (ServerService Thread Pool -- 62) Hibernate: 
[0m[0m14:57:34,772 INFO  [stdout] (ServerService Thread Pool -- 62)     select
[0m[0m14:57:34,772 INFO  [stdout] (ServerService Thread Pool -- 62)         distinct r1_0.NO_RECURSO_FNCNE 
[0m[0m14:57:34,772 INFO  [stdout] (ServerService Thread Pool -- 62)     from
[0m[0m14:57:34,772 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB013_PERMISSAO_PERFIL p1_0 
[0m[0m14:57:34,772 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,772 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:34,772 INFO  [stdout] (ServerService Thread Pool -- 62)             on r1_0.CO_RECURSO_ID=p1_0.CO_RECURSO_ID 
[0m[0m14:57:34,772 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,772 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB011_PERFIL_ACESSO p2_0 
[0m[0m14:57:34,772 INFO  [stdout] (ServerService Thread Pool -- 62)             on p2_0.CO_PERFIL_ID=p1_0.CO_PERFIL_ID 
[0m[0m14:57:34,772 INFO  [stdout] (ServerService Thread Pool -- 62)     where
[0m[0m14:57:34,772 INFO  [stdout] (ServerService Thread Pool -- 62)         (
[0m[0m14:57:34,772 INFO  [stdout] (ServerService Thread Pool -- 62)             p2_0.NO_PERFIL_ACESSO in (?)
[0m[0m14:57:34,772 INFO  [stdout] (ServerService Thread Pool -- 62)         )
[0m[0m14:57:34,776 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 62) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: PerfilRecurso.createQuery
[0m[0m14:57:34,777 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.persist
[0m[0m14:57:34,777 INFO  [stdout] (ServerService Thread Pool -- 62) Hibernate: 
[0m[0m14:57:34,777 INFO  [stdout] (ServerService Thread Pool -- 62)     select
[0m[0m14:57:34,777 INFO  [stdout] (ServerService Thread Pool -- 62)         distinct r1_0.NO_RECURSO_FNCNE 
[0m[0m14:57:34,777 INFO  [stdout] (ServerService Thread Pool -- 62)     from
[0m[0m14:57:34,777 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB013_PERMISSAO_PERFIL p1_0 
[0m[0m14:57:34,777 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,777 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:34,777 INFO  [stdout] (ServerService Thread Pool -- 62)             on r1_0.CO_RECURSO_ID=p1_0.CO_RECURSO_ID 
[0m[0m14:57:34,777 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,777 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB011_PERFIL_ACESSO p2_0 
[0m[0m14:57:34,777 INFO  [stdout] (ServerService Thread Pool -- 62)             on p2_0.CO_PERFIL_ID=p1_0.CO_PERFIL_ID 
[0m[0m14:57:34,777 INFO  [stdout] (ServerService Thread Pool -- 62)     where
[0m[0m14:57:34,777 INFO  [stdout] (ServerService Thread Pool -- 62)         (
[0m[0m14:57:34,777 INFO  [stdout] (ServerService Thread Pool -- 62)             p2_0.NO_PERFIL_ACESSO in (?)
[0m[0m14:57:34,777 INFO  [stdout] (ServerService Thread Pool -- 62)         )
[0m[0m14:57:34,781 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 62) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: PerfilRecurso.createQuery
[0m[0m14:57:34,782 INFO  [stdout] (ServerService Thread Pool -- 62) Hibernate: 
[0m[0m14:57:34,782 INFO  [stdout] (ServerService Thread Pool -- 62)     select
[0m[0m14:57:34,782 INFO  [stdout] (ServerService Thread Pool -- 62)         distinct r1_0.NO_RECURSO_FNCNE 
[0m[0m14:57:34,782 INFO  [stdout] (ServerService Thread Pool -- 62)     from
[0m[0m14:57:34,782 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB013_PERMISSAO_PERFIL p1_0 
[0m[0m14:57:34,782 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,782 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:34,782 INFO  [stdout] (ServerService Thread Pool -- 62)             on r1_0.CO_RECURSO_ID=p1_0.CO_RECURSO_ID 
[0m[0m14:57:34,782 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,782 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB011_PERFIL_ACESSO p2_0 
[0m[0m14:57:34,782 INFO  [stdout] (ServerService Thread Pool -- 62)             on p2_0.CO_PERFIL_ID=p1_0.CO_PERFIL_ID 
[0m[0m14:57:34,782 INFO  [stdout] (ServerService Thread Pool -- 62)     where
[0m[0m14:57:34,782 INFO  [stdout] (ServerService Thread Pool -- 62)         (
[0m[0m14:57:34,782 INFO  [stdout] (ServerService Thread Pool -- 62)             p2_0.NO_PERFIL_ACESSO in (?)
[0m[0m14:57:34,782 INFO  [stdout] (ServerService Thread Pool -- 62)         )
[0m[0m14:57:34,784 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 62) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: PerfilRecurso.createQuery
[0m[0m14:57:34,785 INFO  [stdout] (ServerService Thread Pool -- 62) Hibernate: 
[0m[0m14:57:34,785 INFO  [stdout] (ServerService Thread Pool -- 62)     select
[0m[0m14:57:34,785 INFO  [stdout] (ServerService Thread Pool -- 62)         distinct r1_0.NO_RECURSO_FNCNE 
[0m[0m14:57:34,785 INFO  [stdout] (ServerService Thread Pool -- 62)     from
[0m[0m14:57:34,785 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB013_PERMISSAO_PERFIL p1_0 
[0m[0m14:57:34,785 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,785 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:34,785 INFO  [stdout] (ServerService Thread Pool -- 62)             on r1_0.CO_RECURSO_ID=p1_0.CO_RECURSO_ID 
[0m[0m14:57:34,785 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,785 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB011_PERFIL_ACESSO p2_0 
[0m[0m14:57:34,785 INFO  [stdout] (ServerService Thread Pool -- 62)             on p2_0.CO_PERFIL_ID=p1_0.CO_PERFIL_ID 
[0m[0m14:57:34,785 INFO  [stdout] (ServerService Thread Pool -- 62)     where
[0m[0m14:57:34,785 INFO  [stdout] (ServerService Thread Pool -- 62)         (
[0m[0m14:57:34,785 INFO  [stdout] (ServerService Thread Pool -- 62)             p2_0.NO_PERFIL_ACESSO in (?)
[0m[0m14:57:34,785 INFO  [stdout] (ServerService Thread Pool -- 62)         )
[0m[0m14:57:34,787 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 62) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: PerfilRecurso.createQuery
[0m[0m14:57:34,788 INFO  [stdout] (ServerService Thread Pool -- 62) Hibernate: 
[0m[0m14:57:34,788 INFO  [stdout] (ServerService Thread Pool -- 62)     select
[0m[0m14:57:34,788 INFO  [stdout] (ServerService Thread Pool -- 62)         distinct r1_0.NO_RECURSO_FNCNE 
[0m[0m14:57:34,788 INFO  [stdout] (ServerService Thread Pool -- 62)     from
[0m[0m14:57:34,788 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB013_PERMISSAO_PERFIL p1_0 
[0m[0m14:57:34,788 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,788 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:34,788 INFO  [stdout] (ServerService Thread Pool -- 62)             on r1_0.CO_RECURSO_ID=p1_0.CO_RECURSO_ID 
[0m[0m14:57:34,788 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,788 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB011_PERFIL_ACESSO p2_0 
[0m[0m14:57:34,788 INFO  [stdout] (ServerService Thread Pool -- 62)             on p2_0.CO_PERFIL_ID=p1_0.CO_PERFIL_ID 
[0m[0m14:57:34,788 INFO  [stdout] (ServerService Thread Pool -- 62)     where
[0m[0m14:57:34,788 INFO  [stdout] (ServerService Thread Pool -- 62)         (
[0m[0m14:57:34,788 INFO  [stdout] (ServerService Thread Pool -- 62)             p2_0.NO_PERFIL_ACESSO in (?)
[0m[0m14:57:34,788 INFO  [stdout] (ServerService Thread Pool -- 62)         )
[0m[0m14:57:34,790 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 62) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: PerfilRecurso.createQuery
[0m[0m14:57:34,790 INFO  [stdout] (ServerService Thread Pool -- 62) Hibernate: 
[0m[0m14:57:34,790 INFO  [stdout] (ServerService Thread Pool -- 62)     select
[0m[0m14:57:34,791 INFO  [stdout] (ServerService Thread Pool -- 62)         distinct r1_0.NO_RECURSO_FNCNE 
[0m[0m14:57:34,791 INFO  [stdout] (ServerService Thread Pool -- 62)     from
[0m[0m14:57:34,791 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB013_PERMISSAO_PERFIL p1_0 
[0m[0m14:57:34,791 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,791 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:34,791 INFO  [stdout] (ServerService Thread Pool -- 62)             on r1_0.CO_RECURSO_ID=p1_0.CO_RECURSO_ID 
[0m[0m14:57:34,791 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,791 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB011_PERFIL_ACESSO p2_0 
[0m[0m14:57:34,791 INFO  [stdout] (ServerService Thread Pool -- 62)             on p2_0.CO_PERFIL_ID=p1_0.CO_PERFIL_ID 
[0m[0m14:57:34,791 INFO  [stdout] (ServerService Thread Pool -- 62)     where
[0m[0m14:57:34,791 INFO  [stdout] (ServerService Thread Pool -- 62)         (
[0m[0m14:57:34,791 INFO  [stdout] (ServerService Thread Pool -- 62)             p2_0.NO_PERFIL_ACESSO in (?)
[0m[0m14:57:34,791 INFO  [stdout] (ServerService Thread Pool -- 62)         )
[0m[0m14:57:34,793 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 62) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: PerfilRecurso.createQuery
[0m[0m14:57:34,793 INFO  [stdout] (ServerService Thread Pool -- 62) Hibernate: 
[0m[0m14:57:34,793 INFO  [stdout] (ServerService Thread Pool -- 62)     select
[0m[0m14:57:34,793 INFO  [stdout] (ServerService Thread Pool -- 62)         distinct r1_0.NO_RECURSO_FNCNE 
[0m[0m14:57:34,793 INFO  [stdout] (ServerService Thread Pool -- 62)     from
[0m[0m14:57:34,794 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB013_PERMISSAO_PERFIL p1_0 
[0m[0m14:57:34,859 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,859 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:34,859 INFO  [stdout] (ServerService Thread Pool -- 62)             on r1_0.CO_RECURSO_ID=p1_0.CO_RECURSO_ID 
[0m[0m14:57:34,859 INFO  [stdout] (ServerService Thread Pool -- 62)     join
[0m[0m14:57:34,859 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB011_PERFIL_ACESSO p2_0 
[0m[0m14:57:34,859 INFO  [stdout] (ServerService Thread Pool -- 62)             on p2_0.CO_PERFIL_ID=p1_0.CO_PERFIL_ID 
[0m[0m14:57:34,859 INFO  [stdout] (ServerService Thread Pool -- 62)     where
[0m[0m14:57:34,859 INFO  [stdout] (ServerService Thread Pool -- 62)         (
[0m[0m14:57:34,859 INFO  [stdout] (ServerService Thread Pool -- 62)             p2_0.NO_PERFIL_ACESSO in (?)
[0m[0m14:57:34,859 INFO  [stdout] (ServerService Thread Pool -- 62)         )
[0m[0m14:57:34,861 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:34,862 INFO  [stdout] (ServerService Thread Pool -- 51)     insert 
[0m[0m14:57:34,862 INFO  [stdout] (ServerService Thread Pool -- 51)     into
[0m[0m14:57:34,862 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB014_CONTROLE_ATUALIZACAO
[0m[0m14:57:34,862 INFO  [stdout] (ServerService Thread Pool -- 51)         (IC_CONTROLE_ATUALIZACAO,NO_CONTROLE_ATUALIZACAO,NO_SERVIDOR_APLICACAO) 
[0m[0m14:57:34,862 INFO  [stdout] (ServerService Thread Pool -- 51)     values
[0m[0m14:57:34,862 INFO  [stdout] (ServerService Thread Pool -- 51)         (?,?,?)
[0m[0m14:57:34,862 INFO  [com.hazelcast.instance.AddressPicker] (ServerService Thread Pool -- 62) [LOCAL] [dev] [3.12.12] Prefer IPv4 stack is true, prefer IPv6 addresses is false
[0m[0m14:57:34,863 INFO  [com.hazelcast.instance.AddressPicker] (ServerService Thread Pool -- 62) [LOCAL] [dev] [3.12.12] Picked [25.1.38.69]:5702, using socket ServerSocket[addr=/0.0.0.0,localport=5702], bind any local is true
[0m[0m14:57:34,863 INFO  [com.hazelcast.system] (ServerService Thread Pool -- 62) [25.1.38.69]:5702 [dev] [3.12.12] Hazelcast 3.12.12 (20210209 - 35096ec) starting at [25.1.38.69]:5702
[0m[0m14:57:34,863 INFO  [com.hazelcast.system] (ServerService Thread Pool -- 62) [25.1.38.69]:5702 [dev] [3.12.12] Copyright (c) 2008-2020, Hazelcast, Inc. All Rights Reserved.
[0m[0m14:57:34,865 INFO  [com.hazelcast.spi.impl.operationservice.impl.BackpressureRegulator] (ServerService Thread Pool -- 62) [25.1.38.69]:5702 [dev] [3.12.12] Backpressure is disabled
[0m[0m14:57:34,872 INFO  [com.hazelcast.spi.impl.operationexecutor.impl.OperationExecutorImpl] (ServerService Thread Pool -- 62) [25.1.38.69]:5702 [dev] [3.12.12] Starting 2 partition threads and 3 generic threads (1 dedicated for priority tasks)
[0m[0m14:57:34,873 INFO  [com.hazelcast.internal.diagnostics.Diagnostics] (ServerService Thread Pool -- 62) [25.1.38.69]:5702 [dev] [3.12.12] Diagnostics disabled. To enable add -Dhazelcast.diagnostics.enabled=true to the JVM arguments.
[0m[0m14:57:34,873 INFO  [com.hazelcast.core.LifecycleService] (ServerService Thread Pool -- 62) [25.1.38.69]:5702 [dev] [3.12.12] [25.1.38.69]:5702 is STARTING
[0m[0m14:57:34,874 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Perfil.createQuery
[0m[33m14:57:34,875 WARNING [com.hazelcast.instance.Node] (ServerService Thread Pool -- 62) [25.1.38.69]:5702 [dev] [3.12.12] No join method is enabled! Starting standalone.
[0m[33m14:57:34,875 WARNING [com.hazelcast.instance.Node] (ServerService Thread Pool -- 62) [25.1.38.69]:5702 [dev] [3.12.12] Config seed port is 5701 and cluster size is 1. Some of the ports seem occupied!
[0m[0m14:57:34,875 INFO  [com.hazelcast.core.LifecycleService] (ServerService Thread Pool -- 62) [25.1.38.69]:5702 [dev] [3.12.12] [25.1.38.69]:5702 is STARTED
[0m[0m14:57:34,877 INFO  [com.hazelcast.internal.diagnostics.HealthMonitor] (hz._hzInstance_2_dev.HealthMonitor) [25.1.38.69]:5702 [dev] [3.12.12] processors=1, physical.memory.total=2.0G, physical.memory.free=1.3G, swap.space.total=0, swap.space.free=0, heap.memory.used=209.3M, heap.memory.free=8.2M, heap.memory.total=217.5M, heap.memory.max=1.4G, heap.memory.used/total=96.15%, heap.memory.used/max=14.34%, minor.gc.count=0, minor.gc.time=0ms, major.gc.count=0, major.gc.time=0ms, load.process=0.00%, load.system=0.00%, load.systemAverage=8.72, thread.count=163, thread.peakCount=163, cluster.timeDiff=0, event.q.size=0, executor.q.async.size=0, executor.q.client.size=0, executor.q.client.query.size=0, executor.q.client.blocking.size=0, executor.q.query.size=0, executor.q.scheduled.size=0, executor.q.io.size=0, executor.q.system.size=0, executor.q.operations.size=0, executor.q.priorityOperation.size=0, operations.completed.count=1, executor.q.mapLoad.size=0, executor.q.mapLoadAllKeys.size=0, executor.q.cluster.size=0, executor.q.response.size=0, operations.running.count=0, operations.pending.invocations.percentage=0.00%, operations.pending.invocations.count=0, proxy.count=0, clientEndpoint.count=0, connection.active.count=0, client.connection.count=0, connection.count=0
[0m[0m14:57:34,882 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:34,882 INFO  [stdout] (ServerService Thread Pool -- 51)     update
[0m[0m14:57:34,882 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB011_PERFIL_ACESSO 
[0m[0m14:57:34,882 INFO  [stdout] (ServerService Thread Pool -- 51)     set
[0m[0m14:57:34,882 INFO  [stdout] (ServerService Thread Pool -- 51)         TS_ATLZO_PERFIL=?,
[0m[0m14:57:34,882 INFO  [stdout] (ServerService Thread Pool -- 51)         DE_PERFIL_ACESSO=?,
[0m[0m14:57:34,882 INFO  [stdout] (ServerService Thread Pool -- 51)         NO_PERFIL_ACESSO=?,
[0m[0m14:57:34,882 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_TRMNL_ATLZO_PERFIL=?,
[0m[0m14:57:34,883 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_USUARIO_ATLZO_PERFIL=? 
[0m[0m14:57:34,883 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:34,883 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_PERFIL_ID=?
[0m[0m14:57:34,971 INFO  [com.hazelcast.internal.partition.impl.PartitionStateManager] (ServerService Thread Pool -- 62) [25.1.38.69]:5702 [dev] [3.12.12] Initializing cluster partition table arrangement...
[0m[0m14:57:34,973 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:34,974 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:34,974 INFO  [stdout] (ServerService Thread Pool -- 51)         p1_0.CO_PERFIL_ID,
[0m[0m14:57:34,974 INFO  [stdout] (ServerService Thread Pool -- 51)         p1_0.TS_ATLZO_PERFIL,
[0m[0m14:57:34,974 INFO  [stdout] (ServerService Thread Pool -- 51)         p1_0.DE_PERFIL_ACESSO,
[0m[0m14:57:34,974 INFO  [stdout] (ServerService Thread Pool -- 51)         p1_0.NO_PERFIL_ACESSO,
[0m[0m14:57:34,974 INFO  [stdout] (ServerService Thread Pool -- 51)         p1_0.CO_TRMNL_ATLZO_PERFIL,
[0m[0m14:57:34,974 INFO  [stdout] (ServerService Thread Pool -- 51)         p1_0.CO_USUARIO_ATLZO_PERFIL 
[0m[0m14:57:34,974 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:34,974 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB011_PERFIL_ACESSO p1_0 
[0m[0m14:57:34,974 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:34,974 INFO  [stdout] (ServerService Thread Pool -- 51)         p1_0.NO_PERFIL_ACESSO=?
[0m[0m14:57:34,976 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Perfil.consultarPorId
[0m[0m14:57:34,976 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Perfil.consultarPorId
[0m[0m14:57:34,977 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Perfil.merge
[0m[0m14:57:34,977 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.createQuery
[0m[0m14:57:34,978 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:34,978 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:34,978 INFO  [stdout] (ServerService Thread Pool -- 51)         distinct c1_0.CO_CONTROLE_ID,
[0m[0m14:57:34,978 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.IC_CONTROLE_ATUALIZACAO,
[0m[0m14:57:34,978 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_CONTROLE_ATUALIZACAO,
[0m[0m14:57:34,978 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_SERVIDOR_APLICACAO 
[0m[0m14:57:34,978 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:34,978 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB014_CONTROLE_ATUALIZACAO c1_0 
[0m[0m14:57:34,978 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:34,978 INFO  [stdout] (ServerService Thread Pool -- 51)         (
[0m[0m14:57:34,978 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_CONTROLE_ATUALIZACAO=?
[0m[0m14:57:34,978 INFO  [stdout] (ServerService Thread Pool -- 51)         ) 
[0m[0m14:57:34,978 INFO  [stdout] (ServerService Thread Pool -- 51)         and (
[0m[0m14:57:34,978 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_SERVIDOR_APLICACAO=?
[0m[0m14:57:34,978 INFO  [stdout] (ServerService Thread Pool -- 51)         )
[0m[0m14:57:34,981 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.consultarPorId
[0m[0m14:57:34,981 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.merge
[0m[0m14:57:34,985 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.createQuery
[0m[0m14:57:34,987 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:34,987 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:34,987 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_RECURSO_ID,
[0m[0m14:57:34,987 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.TS_ATLZO_RECURSO,
[0m[0m14:57:34,987 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.DE_RECURSO_FNCNE,
[0m[0m14:57:34,987 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.NO_RECURSO_FNCNE,
[0m[0m14:57:34,987 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_TRMNL_ATLZO_RECURSO,
[0m[0m14:57:34,987 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_USUARIO_ATLZO_RECURSO 
[0m[0m14:57:34,987 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:34,987 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:34,987 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:34,987 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.NO_RECURSO_FNCNE=?
[0m[0m14:57:34,991 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.consultarPorId
[0m[0m14:57:34,991 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.consultarPorId
[0m[0m14:57:34,992 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.merge
[0m[0m14:57:34,993 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.createQuery
[0m[0m14:57:35,059 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,059 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:35,059 INFO  [stdout] (ServerService Thread Pool -- 51)         distinct c1_0.CO_CONTROLE_ID,
[0m[0m14:57:35,059 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.IC_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,059 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,059 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_SERVIDOR_APLICACAO 
[0m[0m14:57:35,059 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:35,059 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB014_CONTROLE_ATUALIZACAO c1_0 
[0m[0m14:57:35,059 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,059 INFO  [stdout] (ServerService Thread Pool -- 51)         (
[0m[0m14:57:35,059 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_CONTROLE_ATUALIZACAO=?
[0m[0m14:57:35,059 INFO  [stdout] (ServerService Thread Pool -- 51)         ) 
[0m[0m14:57:35,059 INFO  [stdout] (ServerService Thread Pool -- 51)         and (
[0m[0m14:57:35,059 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_SERVIDOR_APLICACAO=?
[0m[0m14:57:35,059 INFO  [stdout] (ServerService Thread Pool -- 51)         )
[0m[0m14:57:35,062 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.consultarPorId
[0m[0m14:57:35,063 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.merge
[0m[0m14:57:35,063 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.createQuery
[0m[0m14:57:35,064 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,064 INFO  [stdout] (ServerService Thread Pool -- 51)     update
[0m[0m14:57:35,064 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB011_PERFIL_ACESSO 
[0m[0m14:57:35,064 INFO  [stdout] (ServerService Thread Pool -- 51)     set
[0m[0m14:57:35,064 INFO  [stdout] (ServerService Thread Pool -- 51)         TS_ATLZO_PERFIL=?,
[0m[0m14:57:35,064 INFO  [stdout] (ServerService Thread Pool -- 51)         DE_PERFIL_ACESSO=?,
[0m[0m14:57:35,064 INFO  [stdout] (ServerService Thread Pool -- 51)         NO_PERFIL_ACESSO=?,
[0m[0m14:57:35,064 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_TRMNL_ATLZO_PERFIL=?,
[0m[0m14:57:35,064 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_USUARIO_ATLZO_PERFIL=? 
[0m[0m14:57:35,064 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,064 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_PERFIL_ID=?
[0m[0m14:57:35,067 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,067 INFO  [stdout] (ServerService Thread Pool -- 51)     update
[0m[0m14:57:35,067 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB012_RECURSO_FNCNE 
[0m[0m14:57:35,067 INFO  [stdout] (ServerService Thread Pool -- 51)     set
[0m[0m14:57:35,067 INFO  [stdout] (ServerService Thread Pool -- 51)         TS_ATLZO_RECURSO=?,
[0m[0m14:57:35,067 INFO  [stdout] (ServerService Thread Pool -- 51)         DE_RECURSO_FNCNE=?,
[0m[0m14:57:35,067 INFO  [stdout] (ServerService Thread Pool -- 51)         NO_RECURSO_FNCNE=?,
[0m[0m14:57:35,067 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_TRMNL_ATLZO_RECURSO=?,
[0m[0m14:57:35,067 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_USUARIO_ATLZO_RECURSO=? 
[0m[0m14:57:35,067 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,067 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_RECURSO_ID=?
[0m[0m14:57:35,071 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,071 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:35,071 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_RECURSO_ID,
[0m[0m14:57:35,071 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.TS_ATLZO_RECURSO,
[0m[0m14:57:35,071 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.DE_RECURSO_FNCNE,
[0m[0m14:57:35,071 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.NO_RECURSO_FNCNE,
[0m[0m14:57:35,071 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_TRMNL_ATLZO_RECURSO,
[0m[0m14:57:35,071 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_USUARIO_ATLZO_RECURSO 
[0m[0m14:57:35,071 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:35,071 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:35,071 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,071 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.NO_RECURSO_FNCNE=?
[0m[0m14:57:35,073 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.consultarPorId
[0m[0m14:57:35,073 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.consultarPorId
[0m[0m14:57:35,073 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.merge
[0m[0m14:57:35,074 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.createQuery
[0m[0m14:57:35,074 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,074 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:35,074 INFO  [stdout] (ServerService Thread Pool -- 51)         distinct c1_0.CO_CONTROLE_ID,
[0m[0m14:57:35,074 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.IC_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,074 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,074 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_SERVIDOR_APLICACAO 
[0m[0m14:57:35,074 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:35,075 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB014_CONTROLE_ATUALIZACAO c1_0 
[0m[0m14:57:35,075 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,075 INFO  [stdout] (ServerService Thread Pool -- 51)         (
[0m[0m14:57:35,075 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_CONTROLE_ATUALIZACAO=?
[0m[0m14:57:35,075 INFO  [stdout] (ServerService Thread Pool -- 51)         ) 
[0m[0m14:57:35,075 INFO  [stdout] (ServerService Thread Pool -- 51)         and (
[0m[0m14:57:35,075 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_SERVIDOR_APLICACAO=?
[0m[0m14:57:35,075 INFO  [stdout] (ServerService Thread Pool -- 51)         )
[0m[0m14:57:35,076 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.consultarPorId
[0m[0m14:57:35,077 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.merge
[0m[0m14:57:35,077 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.createQuery
[0m[0m14:57:35,078 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,078 INFO  [stdout] (ServerService Thread Pool -- 51)     update
[0m[0m14:57:35,078 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB012_RECURSO_FNCNE 
[0m[0m14:57:35,078 INFO  [stdout] (ServerService Thread Pool -- 51)     set
[0m[0m14:57:35,078 INFO  [stdout] (ServerService Thread Pool -- 51)         TS_ATLZO_RECURSO=?,
[0m[0m14:57:35,078 INFO  [stdout] (ServerService Thread Pool -- 51)         DE_RECURSO_FNCNE=?,
[0m[0m14:57:35,078 INFO  [stdout] (ServerService Thread Pool -- 51)         NO_RECURSO_FNCNE=?,
[0m[0m14:57:35,078 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_TRMNL_ATLZO_RECURSO=?,
[0m[0m14:57:35,078 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_USUARIO_ATLZO_RECURSO=? 
[0m[0m14:57:35,078 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,078 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_RECURSO_ID=?
[0m[0m14:57:35,079 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,079 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:35,079 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_RECURSO_ID,
[0m[0m14:57:35,079 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.TS_ATLZO_RECURSO,
[0m[0m14:57:35,079 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.DE_RECURSO_FNCNE,
[0m[0m14:57:35,079 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.NO_RECURSO_FNCNE,
[0m[0m14:57:35,079 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_TRMNL_ATLZO_RECURSO,
[0m[0m14:57:35,079 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_USUARIO_ATLZO_RECURSO 
[0m[0m14:57:35,079 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:35,079 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:35,079 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,080 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.NO_RECURSO_FNCNE=?
[0m[0m14:57:35,081 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.consultarPorId
[0m[0m14:57:35,081 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.consultarPorId
[0m[0m14:57:35,082 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.merge
[0m[0m14:57:35,082 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.createQuery
[0m[0m14:57:35,083 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,083 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:35,083 INFO  [stdout] (ServerService Thread Pool -- 51)         distinct c1_0.CO_CONTROLE_ID,
[0m[0m14:57:35,083 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.IC_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,083 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,083 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_SERVIDOR_APLICACAO 
[0m[0m14:57:35,083 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:35,083 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB014_CONTROLE_ATUALIZACAO c1_0 
[0m[0m14:57:35,083 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,083 INFO  [stdout] (ServerService Thread Pool -- 51)         (
[0m[0m14:57:35,083 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_CONTROLE_ATUALIZACAO=?
[0m[0m14:57:35,083 INFO  [stdout] (ServerService Thread Pool -- 51)         ) 
[0m[0m14:57:35,083 INFO  [stdout] (ServerService Thread Pool -- 51)         and (
[0m[0m14:57:35,083 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_SERVIDOR_APLICACAO=?
[0m[0m14:57:35,083 INFO  [stdout] (ServerService Thread Pool -- 51)         )
[0m[0m14:57:35,085 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.consultarPorId
[0m[0m14:57:35,085 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.merge
[0m[0m14:57:35,085 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.createQuery
[0m[0m14:57:35,086 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,086 INFO  [stdout] (ServerService Thread Pool -- 51)     update
[0m[0m14:57:35,086 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB012_RECURSO_FNCNE 
[0m[0m14:57:35,086 INFO  [stdout] (ServerService Thread Pool -- 51)     set
[0m[0m14:57:35,086 INFO  [stdout] (ServerService Thread Pool -- 51)         TS_ATLZO_RECURSO=?,
[0m[0m14:57:35,086 INFO  [stdout] (ServerService Thread Pool -- 51)         DE_RECURSO_FNCNE=?,
[0m[0m14:57:35,086 INFO  [stdout] (ServerService Thread Pool -- 51)         NO_RECURSO_FNCNE=?,
[0m[0m14:57:35,086 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_TRMNL_ATLZO_RECURSO=?,
[0m[0m14:57:35,086 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_USUARIO_ATLZO_RECURSO=? 
[0m[0m14:57:35,086 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,086 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_RECURSO_ID=?
[0m[0m14:57:35,087 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,087 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:35,088 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_RECURSO_ID,
[0m[0m14:57:35,088 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.TS_ATLZO_RECURSO,
[0m[0m14:57:35,088 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.DE_RECURSO_FNCNE,
[0m[0m14:57:35,088 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.NO_RECURSO_FNCNE,
[0m[0m14:57:35,088 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_TRMNL_ATLZO_RECURSO,
[0m[0m14:57:35,088 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_USUARIO_ATLZO_RECURSO 
[0m[0m14:57:35,088 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:35,088 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:35,088 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,088 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.NO_RECURSO_FNCNE=?
[0m[0m14:57:35,089 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.consultarPorId
[0m[0m14:57:35,089 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.consultarPorId
[0m[0m14:57:35,090 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.merge
[0m[0m14:57:35,090 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.createQuery
[0m[0m14:57:35,159 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,159 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:35,159 INFO  [stdout] (ServerService Thread Pool -- 51)         distinct c1_0.CO_CONTROLE_ID,
[0m[0m14:57:35,159 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.IC_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,159 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,159 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_SERVIDOR_APLICACAO 
[0m[0m14:57:35,159 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:35,159 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB014_CONTROLE_ATUALIZACAO c1_0 
[0m[0m14:57:35,159 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,159 INFO  [stdout] (ServerService Thread Pool -- 51)         (
[0m[0m14:57:35,159 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_CONTROLE_ATUALIZACAO=?
[0m[0m14:57:35,159 INFO  [stdout] (ServerService Thread Pool -- 51)         ) 
[0m[0m14:57:35,159 INFO  [stdout] (ServerService Thread Pool -- 51)         and (
[0m[0m14:57:35,159 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_SERVIDOR_APLICACAO=?
[0m[0m14:57:35,159 INFO  [stdout] (ServerService Thread Pool -- 51)         )
[0m[0m14:57:35,162 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.consultarPorId
[0m[0m14:57:35,162 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.merge
[0m[0m14:57:35,162 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.createQuery
[0m[0m14:57:35,163 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 51)     update
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB012_RECURSO_FNCNE 
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 51)     set
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 51)         TS_ATLZO_RECURSO=?,
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 51)         DE_RECURSO_FNCNE=?,
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 51)         NO_RECURSO_FNCNE=?,
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_TRMNL_ATLZO_RECURSO=?,
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_USUARIO_ATLZO_RECURSO=? 
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_RECURSO_ID=?
[0m[0m14:57:35,164 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 62) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.createQuery
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 62) Hibernate: 
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 62)     select
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 62)         distinct c1_0.CO_CONTROLE_ID,
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 62)         c1_0.IC_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 62)         c1_0.NO_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 62)         c1_0.NO_SERVIDOR_APLICACAO 
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 62)     from
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB014_CONTROLE_ATUALIZACAO c1_0 
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 62)     where
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 62)         (
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 62)             c1_0.NO_CONTROLE_ATUALIZACAO=?
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 62)         ) 
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 62)         and (
[0m[0m14:57:35,164 INFO  [stdout] (ServerService Thread Pool -- 62)             c1_0.NO_SERVIDOR_APLICACAO=?
[0m[0m14:57:35,165 INFO  [stdout] (ServerService Thread Pool -- 62)         )
[0m[0m14:57:35,165 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,165 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:35,165 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_RECURSO_ID,
[0m[0m14:57:35,165 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.TS_ATLZO_RECURSO,
[0m[0m14:57:35,165 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.DE_RECURSO_FNCNE,
[0m[0m14:57:35,165 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.NO_RECURSO_FNCNE,
[0m[0m14:57:35,165 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_TRMNL_ATLZO_RECURSO,
[0m[0m14:57:35,165 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_USUARIO_ATLZO_RECURSO 
[0m[0m14:57:35,165 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:35,165 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:35,165 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,165 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.NO_RECURSO_FNCNE=?
[0m[0m14:57:35,167 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.consultarPorId
[0m[0m14:57:35,167 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.consultarPorId
[0m[0m14:57:35,168 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.merge
[0m[0m14:57:35,175 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.createQuery
[0m[0m14:57:35,176 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,176 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:35,176 INFO  [stdout] (ServerService Thread Pool -- 51)         distinct c1_0.CO_CONTROLE_ID,
[0m[0m14:57:35,176 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.IC_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,176 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,176 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_SERVIDOR_APLICACAO 
[0m[0m14:57:35,176 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:35,176 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB014_CONTROLE_ATUALIZACAO c1_0 
[0m[0m14:57:35,176 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,176 INFO  [stdout] (ServerService Thread Pool -- 51)         (
[0m[0m14:57:35,176 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_CONTROLE_ATUALIZACAO=?
[0m[0m14:57:35,176 INFO  [stdout] (ServerService Thread Pool -- 51)         ) 
[0m[0m14:57:35,176 INFO  [stdout] (ServerService Thread Pool -- 51)         and (
[0m[0m14:57:35,176 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_SERVIDOR_APLICACAO=?
[0m[0m14:57:35,176 INFO  [stdout] (ServerService Thread Pool -- 51)         )
[0m[0m14:57:35,178 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.consultarPorId
[0m[0m14:57:35,179 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.merge
[0m[0m14:57:35,179 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.createQuery
[0m[0m14:57:35,180 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,180 INFO  [stdout] (ServerService Thread Pool -- 51)     update
[0m[0m14:57:35,180 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB012_RECURSO_FNCNE 
[0m[0m14:57:35,180 INFO  [stdout] (ServerService Thread Pool -- 51)     set
[0m[0m14:57:35,180 INFO  [stdout] (ServerService Thread Pool -- 51)         TS_ATLZO_RECURSO=?,
[0m[0m14:57:35,180 INFO  [stdout] (ServerService Thread Pool -- 51)         DE_RECURSO_FNCNE=?,
[0m[0m14:57:35,180 INFO  [stdout] (ServerService Thread Pool -- 51)         NO_RECURSO_FNCNE=?,
[0m[0m14:57:35,180 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_TRMNL_ATLZO_RECURSO=?,
[0m[0m14:57:35,180 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_USUARIO_ATLZO_RECURSO=? 
[0m[0m14:57:35,180 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,180 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_RECURSO_ID=?
[0m[0m14:57:35,181 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,181 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:35,181 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_RECURSO_ID,
[0m[0m14:57:35,181 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.TS_ATLZO_RECURSO,
[0m[0m14:57:35,181 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.DE_RECURSO_FNCNE,
[0m[0m14:57:35,181 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.NO_RECURSO_FNCNE,
[0m[0m14:57:35,181 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_TRMNL_ATLZO_RECURSO,
[0m[0m14:57:35,181 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_USUARIO_ATLZO_RECURSO 
[0m[0m14:57:35,181 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:35,181 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:35,181 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,181 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.NO_RECURSO_FNCNE=?
[0m[0m14:57:35,183 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.consultarPorId
[0m[0m14:57:35,183 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.consultarPorId
[0m[0m14:57:35,184 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.merge
[0m[0m14:57:35,184 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.createQuery
[0m[0m14:57:35,185 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,185 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:35,185 INFO  [stdout] (ServerService Thread Pool -- 51)         distinct c1_0.CO_CONTROLE_ID,
[0m[0m14:57:35,185 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.IC_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,185 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,185 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_SERVIDOR_APLICACAO 
[0m[0m14:57:35,185 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:35,185 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB014_CONTROLE_ATUALIZACAO c1_0 
[0m[0m14:57:35,185 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,185 INFO  [stdout] (ServerService Thread Pool -- 51)         (
[0m[0m14:57:35,185 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_CONTROLE_ATUALIZACAO=?
[0m[0m14:57:35,185 INFO  [stdout] (ServerService Thread Pool -- 51)         ) 
[0m[0m14:57:35,185 INFO  [stdout] (ServerService Thread Pool -- 51)         and (
[0m[0m14:57:35,185 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_SERVIDOR_APLICACAO=?
[0m[0m14:57:35,185 INFO  [stdout] (ServerService Thread Pool -- 51)         )
[0m[0m14:57:35,186 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.consultarPorId
[0m[0m14:57:35,186 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.merge
[0m[0m14:57:35,187 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.createQuery
[0m[0m14:57:35,187 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,188 INFO  [stdout] (ServerService Thread Pool -- 51)     update
[0m[0m14:57:35,188 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB012_RECURSO_FNCNE 
[0m[0m14:57:35,188 INFO  [stdout] (ServerService Thread Pool -- 51)     set
[0m[0m14:57:35,188 INFO  [stdout] (ServerService Thread Pool -- 51)         TS_ATLZO_RECURSO=?,
[0m[0m14:57:35,188 INFO  [stdout] (ServerService Thread Pool -- 51)         DE_RECURSO_FNCNE=?,
[0m[0m14:57:35,188 INFO  [stdout] (ServerService Thread Pool -- 51)         NO_RECURSO_FNCNE=?,
[0m[0m14:57:35,188 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_TRMNL_ATLZO_RECURSO=?,
[0m[0m14:57:35,188 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_USUARIO_ATLZO_RECURSO=? 
[0m[0m14:57:35,188 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,188 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_RECURSO_ID=?
[0m[0m14:57:35,189 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,189 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:35,189 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_RECURSO_ID,
[0m[0m14:57:35,189 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.TS_ATLZO_RECURSO,
[0m[0m14:57:35,189 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.DE_RECURSO_FNCNE,
[0m[0m14:57:35,189 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.NO_RECURSO_FNCNE,
[0m[0m14:57:35,189 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_TRMNL_ATLZO_RECURSO,
[0m[0m14:57:35,189 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.CO_USUARIO_ATLZO_RECURSO 
[0m[0m14:57:35,189 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:35,189 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB012_RECURSO_FNCNE r1_0 
[0m[0m14:57:35,189 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,189 INFO  [stdout] (ServerService Thread Pool -- 51)         r1_0.NO_RECURSO_FNCNE=?
[0m[0m14:57:35,190 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.consultarPorId
[0m[0m14:57:35,191 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.consultarPorId
[0m[0m14:57:35,191 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: Recurso.merge
[0m[0m14:57:35,191 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.createQuery
[0m[0m14:57:35,192 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,192 INFO  [stdout] (ServerService Thread Pool -- 51)     select
[0m[0m14:57:35,192 INFO  [stdout] (ServerService Thread Pool -- 51)         distinct c1_0.CO_CONTROLE_ID,
[0m[0m14:57:35,192 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.IC_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,192 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_CONTROLE_ATUALIZACAO,
[0m[0m14:57:35,192 INFO  [stdout] (ServerService Thread Pool -- 51)         c1_0.NO_SERVIDOR_APLICACAO 
[0m[0m14:57:35,192 INFO  [stdout] (ServerService Thread Pool -- 51)     from
[0m[0m14:57:35,192 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB014_CONTROLE_ATUALIZACAO c1_0 
[0m[0m14:57:35,192 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,192 INFO  [stdout] (ServerService Thread Pool -- 51)         (
[0m[0m14:57:35,192 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_CONTROLE_ATUALIZACAO=?
[0m[0m14:57:35,192 INFO  [stdout] (ServerService Thread Pool -- 51)         ) 
[0m[0m14:57:35,192 INFO  [stdout] (ServerService Thread Pool -- 51)         and (
[0m[0m14:57:35,192 INFO  [stdout] (ServerService Thread Pool -- 51)             c1_0.NO_SERVIDOR_APLICACAO=?
[0m[0m14:57:35,192 INFO  [stdout] (ServerService Thread Pool -- 51)         )
[0m[0m14:57:35,194 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.consultarPorId
[0m[0m14:57:35,194 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 51) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.merge
[0m[0m14:57:35,195 INFO  [stdout] (ServerService Thread Pool -- 51) Hibernate: 
[0m[0m14:57:35,196 INFO  [stdout] (ServerService Thread Pool -- 51)     update
[0m[0m14:57:35,196 INFO  [stdout] (ServerService Thread Pool -- 51)         dbo.HDGTB012_RECURSO_FNCNE 
[0m[0m14:57:35,196 INFO  [stdout] (ServerService Thread Pool -- 51)     set
[0m[0m14:57:35,196 INFO  [stdout] (ServerService Thread Pool -- 51)         TS_ATLZO_RECURSO=?,
[0m[0m14:57:35,196 INFO  [stdout] (ServerService Thread Pool -- 51)         DE_RECURSO_FNCNE=?,
[0m[0m14:57:35,196 INFO  [stdout] (ServerService Thread Pool -- 51)         NO_RECURSO_FNCNE=?,
[0m[0m14:57:35,196 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_TRMNL_ATLZO_RECURSO=?,
[0m[0m14:57:35,196 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_USUARIO_ATLZO_RECURSO=? 
[0m[0m14:57:35,196 INFO  [stdout] (ServerService Thread Pool -- 51)     where
[0m[0m14:57:35,196 INFO  [stdout] (ServerService Thread Pool -- 51)         CO_RECURSO_ID=?
[0m[0m14:57:35,204 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 62) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.consultarPorId
[0m[0m14:57:35,204 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 62) SEGURANCA - Operacao durante inicializacao permitida sem contexto. Operacao: ControleCache.merge
[0m[0m14:57:35,260 INFO  [stdout] (ServerService Thread Pool -- 62) Hibernate: 
[0m[0m14:57:35,260 INFO  [stdout] (ServerService Thread Pool -- 62)     update
[0m[0m14:57:35,260 INFO  [stdout] (ServerService Thread Pool -- 62)         dbo.HDGTB014_CONTROLE_ATUALIZACAO 
[0m[0m14:57:35,260 INFO  [stdout] (ServerService Thread Pool -- 62)     set
[0m[0m14:57:35,260 INFO  [stdout] (ServerService Thread Pool -- 62)         IC_CONTROLE_ATUALIZACAO=?,
[0m[0m14:57:35,260 INFO  [stdout] (ServerService Thread Pool -- 62)         NO_CONTROLE_ATUALIZACAO=?,
[0m[0m14:57:35,260 INFO  [stdout] (ServerService Thread Pool -- 62)         NO_SERVIDOR_APLICACAO=? 
[0m[0m14:57:35,260 INFO  [stdout] (ServerService Thread Pool -- 62)     where
[0m[0m14:57:35,260 INFO  [stdout] (ServerService Thread Pool -- 62)         CO_CONTROLE_ID=?
[0m[0m14:57:35,291 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.seguranca.ContextoSegurancaHelper] (ServerService Thread Pool -- 62) SEGURANCA - Aplicacao inicializada. Verificacao de contexto autenticado ativada.
[0m[33m14:57:35,399 WARN  [io.undertow.servlet] (ServerService Thread Pool -- 62) UT015020: Path /health is secured for some HTTP methods, however it is not secured for [TRACE, HEAD, CONNECT, OPTIONS]
[0m[33m14:57:35,399 WARN  [io.undertow.servlet] (ServerService Thread Pool -- 62) UT015020: Path /api/swagger.json is secured for some HTTP methods, however it is not secured for [TRACE, HEAD, CONNECT, OPTIONS]
[0m[33m14:57:35,399 WARN  [io.undertow.servlet] (ServerService Thread Pool -- 62) UT015020: Path /swagger/* is secured for some HTTP methods, however it is not secured for [TRACE, HEAD, CONNECT, OPTIONS]
[0m[33m14:57:35,399 WARN  [io.undertow.servlet] (ServerService Thread Pool -- 62) UT015020: Path /health/* is secured for some HTTP methods, however it is not secured for [TRACE, HEAD, CONNECT, OPTIONS]
[0m[33m14:57:35,399 WARN  [io.undertow.servlet] (ServerService Thread Pool -- 62) UT015020: Path /api/seguranca/configuracao-seguranca/* is secured for some HTTP methods, however it is not secured for [TRACE, HEAD, CONNECT, OPTIONS]
[0m[33m14:57:35,399 WARN  [io.undertow.servlet] (ServerService Thread Pool -- 62) UT015020: Path /api/* is secured for some HTTP methods, however it is not secured for [TRACE, HEAD, CONNECT, OPTIONS]
[0m[33m14:57:35,471 WARN  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 62) RESTEASY002150: resteasy.scan is no longer supported.  Use a servlet 3.0 container and the ResteasyServletInitializer
[0m[0m14:57:36,792 INFO  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 62) RESTEASY002225: Deploying jakarta.ws.rs.core.Application: class br.gov.caixa.arquitetura.javaee.api.comum.config.web.RestConfig$Proxy$_$$_WeldClientProxy
[0m[33m14:57:36,801 WARN  [org.jboss.as.weld] (ServerService Thread Pool -- 62) WFLYWELD0052: Using deployment classloader to load proxy classes for module com.fasterxml.jackson.jakarta.jackson-jakarta-json-provider. Package-private access will not work. To fix this the module should declare dependencies on [org.jboss.weld.core, org.jboss.weld.spi, org.jboss.weld.api]
[0m[0m14:57:36,890 INFO  [br.gov.caixa.arquitetura.javaee7.api.comum.seguranca.keycloak.AuthorizationFilter] (ServerService Thread Pool -- 62) Iniciando filtro de OIDC Authorization ...
[0m[0m14:57:37,161 INFO  [br.gov.caixa.arquitetura.javaee.api.comum.config.swagger.SwaggerDocConfig] (ServerService Thread Pool -- 62) Swagger iniciado
[0m[0m14:57:37,162 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.config.BaseSettings] (ServerService Thread Pool -- 62) Propriedade: [SIHDG-version.project]
[0m[0m14:57:37,162 INFO  [br.gov.caixa.arquitetura.javaee.core.comum.config.BaseSettings] (ServerService Thread Pool -- 62) Valor retornado: [null]
[0m[0m14:57:37,278 INFO  [br.gov.caixa.arquitetura.javaee.api.comum.config.AppConfig] (ServerService Thread Pool -- 62) Contexto de aplicação iniciado
[0m[0m14:57:37,290 INFO  [br.gov.caixa.arquitetura.javaee.api.comum.config.web.WebAppConfig] (ServerService Thread Pool -- 62) Aplicação SIHDG iniciada nos endereços:
	Local: 	http://127.0.0.1:8080
	Externo: 	http://25.1.38.69:8080
[0m[0m14:57:37,290 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 62) WFLYUT0021: Registered web context: '/sihdg-api' for server 'default-server'
[0m[0m14:57:37,295 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 28) WFLYSRV0010: Deployed "sihdg-3.18.0.1.ear" (runtime-name : "sihdg-3.18.0.1.ear")
[0m[0m14:57:37,381 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0212: Resuming server
[0m[0m14:57:37,382 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0060: Http management interface listening on http://0.0.0.0:9990/management
[0m[0m14:57:37,383 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0054: Admin console is not enabled
[0m[0m14:57:37,383 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0025: JBoss EAP 8.0 Update 12.0 (WildFly Core 21.0.20.Final-redhat-00001) started in 24486ms - Started 1183 of 1265 services (162 services are lazy, passive or on-demand) - Server configuration file in use: standalone.xml
[0m[0m14:57:44,261 INFO  [org.wildfly.security.http.oidc] (default task-1) ELY23004: Loaded OpenID provider metadata from 'https://login.tqs.caixa/auth/realms/intranet/.well-known/openid-configuration'
[0m[0m14:57:44,264 INFO  [br.gov.caixa.arquitetura.javaee.api.comum.web.CORSFilter] (default task-1) Iniciando filtro CORS ...
[0m[0m14:58:00,004 INFO  [br.gov.caixa.arquitetura.javaee.core.util.AtualizadorCacheAS] (EJB default - 1) Verificando o cache de 'PERFIL_RECURSO'
[0m[0m14:58:00,006 INFO  [stdout] (EJB default - 1) Hibernate: 
[0m[0m14:58:00,006 INFO  [stdout] (EJB default - 1)     select
[0m[0m14:58:00,006 INFO  [stdout] (EJB default - 1)         distinct c1_0.CO_CONTROLE_ID,
[0m[0m14:58:00,006 INFO  [stdout] (EJB default - 1)         c1_0.IC_CONTROLE_ATUALIZACAO,
[0m[0m14:58:00,006 INFO  [stdout] (EJB default - 1)         c1_0.NO_CONTROLE_ATUALIZACAO,
[0m[0m14:58:00,006 INFO  [stdout] (EJB default - 1)         c1_0.NO_SERVIDOR_APLICACAO 
[0m[0m14:58:00,006 INFO  [stdout] (EJB default - 1)     from
[0m[0m14:58:00,006 INFO  [stdout] (EJB default - 1)         dbo.HDGTB014_CONTROLE_ATUALIZACAO c1_0 
[0m[0m14:58:00,006 INFO  [stdout] (EJB default - 1)     where
[0m[0m14:58:00,006 INFO  [stdout] (EJB default - 1)         (
[0m[0m14:58:00,006 INFO  [stdout] (EJB default - 1)             c1_0.NO_CONTROLE_ATUALIZACAO=?
[0m[0m14:58:00,006 INFO  [stdout] (EJB default - 1)         ) 
[0m[0m14:58:00,006 INFO  [stdout] (EJB default - 1)         and (
[0m[0m14:58:00,006 INFO  [stdout] (EJB default - 1)             c1_0.NO_SERVIDOR_APLICACAO=?
[0m[0m14:58:00,006 INFO  [stdout] (EJB default - 1)         )
[0m


Skip to main content
Azure DevOps
projetos
/
Caixa
/
Pipelines
/
Releases
/
SIHDG-jboss8
/
SIHDG-jboss8-3.19.1.0(3)
Search


Caixa

Overview

Boards

Repos

Pipelines
Pipelines
Environments
Releases
Library
Task groups
Deployment groups
Portal Infra

Test Plans

Artifacts
Project settings
SIHDG-jboss8

SIHDG-jboss8-3.19.1.0(3)


EC TQS

Succeeded


Pipeline

Tasks

Variables

Logs

Tests
Agent job
Started: 13/10/2026, 14:56:23
Pool:
Release-Linux-OKD4
·
Agent: azp-ads-agent-release-5cd876f98-968x9

1m 36s

Initialize job
·
succeeded
<1s

Pre-job: Download secure file
·
succeeded
<1s

Download Artifacts
·
succeeded
1 warning
<1s

Exportando as variáveis do arquivo Trust Store
·
succeeded
<1s

Valida Variáveis Obrigatórias
·
succeeded
<1s

Recuperando URL Pacote Nexus
·
succeeded
1s

Recupera Pacote
·
succeeded
<1s

Convertendo Minúsculo e Definindo nome do Projeto/Repositório
·
succeeded
<1s

Corrigindo Codificação Arquivos dos2unix
·
succeeded
<1s

Alterando Valores placeholders nos arquivos de config
·
succeeded
<1s

Git clone https://devops.caixa/projetos/Infraestrutura/_git/esteira-logs
·
succeeded
<1s

Cria Streams Graylog
·
succeeded
3s

Recupera VEC
·
succeeded
1s

VEC - Aferição
·
succeeded
<1s

Login OpenShift
·
succeeded
<1s

Exportando Variáveis de Ambiente "_ENV."
·
succeeded
<1s

Criando novo Projeto
·
succeeded
<1s

Adicionando ISTIO_INJECTION
·
skipped


Criando nova APP
·
succeeded
<1s

Atualizando Variáveis de Ambiente
·
succeeded
<1s

Criando Rota Customizada
·
succeeded
<1s

Aplicando Service Mesh
·
skipped


Criando arquivo PV
·
succeeded
<1s

Criando Persistente Volume
·
succeeded
<1s

Criando arquivo PVC
·
succeeded
<1s

Criando Persistente Volume Claim
·
succeeded
<1s

Verificando se o Volume foi configurado corretamente.
·
succeeded
<1s

Configurando DeploymentConfig para utilizar o Volume Criado
·
succeeded
<1s

Adicionando Multiplas Secrets
·
succeeded
<1s

Excluindo ConfigMap jboss-config
·
succeeded
<1s

Criando o ConfigMap jboss-config
·
succeeded
<1s

Configurando o ConfigMap jboss-config
·
succeeded
<1s

Excluindo ConfigMap java-config
·
succeeded
<1s

Criando o ConfigMap java-config
·
succeeded
<1s

Configurando o ConfigMap java-config
·
succeeded
<1s

Executando Tag na Imagem do ambiente de build OKD3, OKD4 e OCP
·
succeeded
20s

Concedendo Acesso OKD
·
succeeded
<1s

Verificando IP de Saída
·
succeeded
<1s

Configurando IP de Saída - deployment
·
skipped


Configurando IP de Saída - deploymentconfig
·
succeeded
<1s

Cadastrando no Portal IIF
·
succeeded
<1s

Verificando Status do Deployment
·
succeeded
48s

Logs da Aplicação
·
succeeded
<1s

Resumo da Release
·
succeeded
<1s

Coletando dados da imagem
·
succeeded
8s

Atualizando versão no PortalIF
·
succeeded
<1s

Realizando Logout OKD
·
succeeded
<1s

Finalize Job
·
succeeded
<1s
Select a release pipeline to view its releases

3 pipelines found

Select a release pipeline to view its releases

1 pipelines found

Row 2

Row 2

Showing filters 1 through 2

15 pipelines found

Select a release pipeline to view its releases

5 pipelines found

Row 6

Row 6

Row 2

Showing 26 deployments

Row 2

EC TQSDeploy release

Row 2

Row 2

passou deu certo caraio
