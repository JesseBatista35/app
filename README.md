_ENV.SPRING_CONFIG_IMPORT = optional:configtree:/usr/src/app/secrets_files/SINAF_DES/



OKD


Jesse Mouta Pereira Batista

Administrator
Home
Operators
Workloads
Networking
Storage
Builds
Observe
Compute
User Management
Administration

Project: sinaf-des
Pods
Pod details
Pod
P
sinaf-acoes-em-lote-mensageria-des-92-gcl6h
Running

Actions
Details
Metrics
YAML
Environment
Logs
Events
Terminal
Info alert:Environment variables set from parent
View environment for resource ReplicationController
RC
sinaf-acoes-em-lote-mensageria-des-92
Container:

Container
C
sinaf-acoes-em-lote-mensageria-des
Single values (env)
NameValue
TZ
America/Sao_Paulo
INSTANCE_IP
FieldRef
status.podIP
JAVA_OPTIONS
-Dserver.address=0.0.0.0 -Dserver.port=8080
JAVA_OPTS_MONITORING
-javaagent:/opt/apm_agent/elastic-apm-agent.jar -Delastic.apm.config_file=/opt/apm_agent/elasticapm.properties -Delastic.apm.service_name=sinaf-acoes-em-lote-mensageria -Delastic.apm.environment=des -Delastic.apm.application_packages=br.gov.caixa -Delastic.apm.server_urls=http://apm-server-devops.produtos.caixa -Delastic.apm.global_labels=deployment=sinaf-acoes-em-lote-mensageria
SPRING_APPLICATION_NAME
acoes-em-lote-mensageria
SPRING_CONFIG_IMPORT
optional:configtree:/usr/src/app/secrets_files/SINAF_DES/
SPRING_DATASOURCE_PASSWORD
${DATASOURCE_PASSWORD_SNAFPB01}
SPRING_DATASOURCE_URL
jdbc:db2://10.192.224.76:5021/CSD1
SPRING_DATASOURCE_USERNAME
SNAFBD01
SPRING_KAFKA_BOOTSTRAP_SERVERS
cp4i-des-kafka-bootstrap-cp4i.apps.kafka-nprd.caixa:443
SPRING_KAFKA_PASSWORD
${KAFKA_PASS}
SPRING_KAFKA_PROPERTIES_SASL_JAAS_CONFIG
org.apache.kafka.common.security.scram.ScramLoginModule required username=sinaf-des password='${KAFKA_PASS}';
SPRING_KAFKA_PROPERTIES_SSL_TRUSTSTORE_PASSWORD
${KAFKA_TRUSTSTORE_PASS}
SPRING_KAFKA_TOPIC_NAME_CONSUMER_AUTORIZACAO_EM_LOTE_APROVAR
sinaf-des-autorizacao-aprovar
SPRING_KAFKA_TOPIC_NAME_CONSUMER_AUTORIZACAO_EM_LOTE_CANCELAMENTO
sinaf-des-cancelamento
SPRING_KAFKA_TOPIC_NAME_CONSUMER_AUTORIZACAO_EM_LOTE_DEVOLVER_COMPLEMENTO
sinaf-des-autorizacao-devolver-complemento
SPRING_KAFKA_TOPIC_NAME_CONSUMER_AUTORIZACAO_EM_LOTE_EXCLUSAO
sinaf-des-excluir
SPRING_KAFKA_TOPIC_NAME_CONSUMER_AUTORIZACAO_EM_LOTE_REPROVAR
sinaf-des-autorizacao-reprovar
SPRING_KAFKA_TOPIC_NAME_CONSUMER_FINALIZACAO_EM_LOTE
sinaf-des-finalizacao
SPRING_KAFKA_USERNAME
sinaf-des
SMALLRYE_CONFIG_SOURCE_FILE_LOCATIONS
sinaf-acoes-em-lote-mensageria-des - Secret
SMALLRYE_CONFIG_SOURCE_FILE_LOCATIONS
All values from existing ConfigMaps or Secrets (envFrom)
ConfigMap/SecretPrefix (optional)
ConfigMap/Secret





sinaf-acoes-em-lote-mensageria-des-92-gcl6h
Running
1/1	0	
ReplicationController
RC
sinaf-acoes-em-lote-mensageria-des-92
401,6 MiB	0,011 cores	
13 de out. de 2026, 12:19



exec java -Dserver.address=0.0.0.0 -Dserver.port=8080 -javaagent:/opt/apm_agent/elastic-apm-agent.jar -Delastic.apm.config_file=/opt/apm_agent/elasticapm.properties -Delastic.apm.service_name=sinaf-acoes-em-lote-mensageria -Delastic.apm.environment=des -Delastic.apm.application_packages=br.gov.caixa -Delastic.apm.server_urls=http://apm-server-devops.produtos.caixa -Delastic.apm.global_labels=deployment=sinaf-acoes-em-lote-mensageria -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/demo-1.2.03.jar
OpenJDK 64-Bit Server VM warning: Sharing is only supported for boot loader classes because bootstrap classpath has been appended
WARNING: sun.reflect.Reflection.getCallerClass is not supported. This will impact performance.
Failed to start agent
java.lang.reflect.InvocationTargetException
	at java.base/jdk.internal.reflect.DirectMethodHandleAccessor.invoke(DirectMethodHandleAccessor.java:118)
	at java.base/java.lang.reflect.Method.invoke(Method.java:580)
	at co.elastic.apm.agent.premain.AgentMain.loadAndInitializeAgent(AgentMain.java:155)
	at co.elastic.apm.agent.premain.AgentMain.init(AgentMain.java:100)
	at co.elastic.apm.agent.premain.AgentMain.premain(AgentMain.java:56)
	at java.base/jdk.internal.reflect.DirectMethodHandleAccessor.invoke(DirectMethodHandleAccessor.java:103)
	at java.base/java.lang.reflect.Method.invoke(Method.java:580)
	at java.instrument/sun.instrument.InstrumentationImpl.loadClassAndStartAgent(InstrumentationImpl.java:560)
	at java.instrument/sun.instrument.InstrumentationImpl.loadClassAndCallPremain(InstrumentationImpl.java:572)
Caused by: java.lang.RuntimeException: java.lang.UnsupportedOperationException: Could not access Unsafe class: sun.misc.Unsafe.defineClass(java.lang.String,[B,int,int,java.lang.ClassLoader,java.security.ProtectionDomain)
	at co.elastic.apm.agent.bci.IndyBootstrap.getIndyBootstrapMethod(IndyBootstrap.java:221)
	at co.elastic.apm.agent.bci.ElasticApmAgent.getTransformer(ElasticApmAgent.java:436)
	at co.elastic.apm.agent.bci.ElasticApmAgent.applyAdvice(ElasticApmAgent.java:398)
	at co.elastic.apm.agent.bci.ElasticApmAgent.initAgentBuilder(ElasticApmAgent.java:321)
	at co.elastic.apm.agent.bci.ElasticApmAgent.initInstrumentation(ElasticApmAgent.java:267)
	at co.elastic.apm.agent.bci.ElasticApmAgent.initInstrumentation(ElasticApmAgent.java:171)
	at co.elastic.apm.agent.bci.ElasticApmAgent.initialize(ElasticApmAgent.java:157)
	at java.base/jdk.internal.reflect.DirectMethodHandleAccessor.invoke(DirectMethodHandleAccessor.java:103)
	... 8 more
Caused by: java.lang.UnsupportedOperationException: Could not access Unsafe class: sun.misc.Unsafe.defineClass(java.lang.String,[B,int,int,java.lang.ClassLoader,java.security.ProtectionDomain)
	at co.elastic.apm.agent.shaded.bytebuddy.dynamic.loading.ClassInjector$UsingUnsafe$Dispatcher$Unavailable.initialize(ClassInjector.java:2133)
	at co.elastic.apm.agent.shaded.bytebuddy.dynamic.loading.ClassInjector$UsingUnsafe.injectRaw(ClassInjector.java:1865)
	at co.elastic.apm.agent.bci.IndyBootstrap.initIndyBootstrap(IndyBootstrap.java:234)
	at co.elastic.apm.agent.bci.IndyBootstrap.getIndyBootstrapMethod(IndyBootstrap.java:215)
	... 15 more

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/

 :: Spring Boot ::                (v3.4.5)

2026-10-13T12:20:06.052-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] g.c.b.s.AcoesEmLoteMensageriaApplication : Starting AcoesEmLoteMensageriaApplication v1.2.03 using Java 21.0.1 with PID 8 (/deployments/demo-1.2.03.jar started by 185 in /deployments)
2026-10-13T12:20:06.055-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] g.c.b.s.AcoesEmLoteMensageriaApplication : No active profile set, falling back to 1 default profile: "default"
2026-10-13T12:20:08.156-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] .s.d.r.c.RepositoryConfigurationDelegate : Bootstrapping Spring Data JPA repositories in DEFAULT mode.
2026-10-13T12:20:08.232-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] .s.d.r.c.RepositoryConfigurationDelegate : Finished Spring Data repository scanning in 13 ms. Found 0 JPA repository interfaces.
2026-10-13T12:20:08.636-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] b.g.c.b.s.c.DatasourcePropertiesLogger   : DATASOURCE url=jdbc:db2://10.192.224.76:5021/CSD1
2026-10-13T12:20:08.637-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] b.g.c.b.s.c.DatasourcePropertiesLogger   : DATASOURCE username=SNAFBD01
2026-10-13T12:20:08.639-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] b.g.c.b.s.c.DatasourcePropertiesLogger   : DATASOURCE password=sna2006
2026-10-13T12:20:09.643-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat initialized with port 8080 (http)
2026-10-13T12:20:09.654-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.apache.catalina.core.StandardService   : Starting service [Tomcat]
2026-10-13T12:20:09.655-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.apache.catalina.core.StandardEngine    : Starting Servlet engine: [Apache Tomcat/10.1.40]
2026-10-13T12:20:09.757-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring embedded WebApplicationContext
2026-10-13T12:20:09.758-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] w.s.c.ServletWebServerApplicationContext : Root WebApplicationContext: initialization completed in 3619 ms
2026-10-13T12:20:10.743-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.hibernate.jpa.internal.util.LogHelper  : HHH000204: Processing PersistenceUnitInfo [name: default]
2026-10-13T12:20:10.830-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] org.hibernate.Version                    : HHH000412: Hibernate ORM core version 6.6.13.Final
2026-10-13T12:20:10.860-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.h.c.internal.RegionFactoryInitiator    : HHH000026: Second-level cache disabled
2026-10-13T12:20:12.729-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.s.o.j.p.SpringPersistenceUnitInfo      : No LoadTimeWeaver setup: ignoring JPA class transformer
2026-10-13T12:20:12.751-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Starting...
2026-10-13T12:20:13.236-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] com.zaxxer.hikari.pool.HikariPool        : HikariPool-1 - Added connection com.ibm.db2.jcc.t4.b@748015f8
2026-10-13T12:20:13.237-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Start completed.
2026-10-13T12:20:13.352-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] org.hibernate.orm.connections.pooling    : HHH10001005: Database info:
	Database JDBC URL [Connecting through datasource 'HikariDataSource (HikariPool-1)']
	Database driver: undefined/unknown
	Database version: 13.1
	Autocommit mode: undefined/unknown
	Isolation level: undefined/unknown
	Minimum pool size: undefined/unknown
	Maximum pool size: undefined/unknown
2026-10-13T12:20:14.357-03:00  WARN 8 --- [acoes-em-lote-mensageria] [           main] org.hibernate.mapping.RootClass          : HHH000038: Composite-id class does not override equals(): br.gov.caixa.bsb.sinaf.model.DocumentoLancamentoPK
2026-10-13T12:20:14.357-03:00  WARN 8 --- [acoes-em-lote-mensageria] [           main] org.hibernate.mapping.RootClass          : HHH000039: Composite-id class does not override hashCode(): br.gov.caixa.bsb.sinaf.model.DocumentoLancamentoPK
2026-10-13T12:20:16.626-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.h.e.t.j.p.i.JtaPlatformInitiator       : HHH000489: No JTA platform available (set 'hibernate.transaction.jta.platform' to enable JTA platform integration)
2026-10-13T12:20:18.750-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] j.LocalContainerEntityManagerFactoryBean : Initialized JPA EntityManagerFactory for persistence unit 'default'
2026-10-13T12:20:20.042-03:00  WARN 8 --- [acoes-em-lote-mensageria] [           main] JpaBaseConfiguration$JpaWebConfiguration : spring.jpa.open-in-view is enabled by default. Therefore, database queries may be performed during view rendering. Explicitly configure spring.jpa.open-in-view to disable this warning
2026-10-13T12:20:21.620-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.s.b.a.e.web.EndpointLinksResolver      : Exposing 3 endpoints beneath base path '/actuator'
2026-10-13T12:20:21.857-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat started on port 8080 (http) with context path '/'
2026-10-13T12:20:21.949-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.clients.consumer.ConsumerConfig    : ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.include.jmx.reporter = true
	auto.offset.reset = latest
	bootstrap.servers = [cp4i-des-kafka-bootstrap-cp4i.apps.kafka-nprd.caixa:443]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-acoes-em-lote-group-1
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = false
	enable.metrics.push = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = acoes-em-lote-group
	group.instance.id = null
	group.protocol = classic
	group.remote.assignor = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metadata.recovery.strategy = none
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.max.ms = 1000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = [hidden]
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = SCRAM-SHA-512
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = SASL_SSL
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = /tmp/truststore-kafka4170702909817137176.jks
	ssl.truststore.password = [hidden]
	ssl.truststore.type = JKS
	value.deserializer = class org.springframework.kafka.support.serializer.JsonDeserializer

2026-10-13T12:20:22.041-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.c.t.i.KafkaMetricsCollector        : initializing Kafka metrics collector
2026-10-13T12:20:22.260-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.c.s.authenticator.AbstractLogin    : Successfully logged in.
2026-10-13T12:20:22.525-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka version: 3.8.1
2026-10-13T12:20:22.525-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka commitId: 70d6ff42debf7e17
2026-10-13T12:20:22.525-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka startTimeMs: 1791904822524
2026-10-13T12:20:22.529-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.c.c.internals.LegacyKafkaConsumer  : [Consumer clientId=consumer-acoes-em-lote-group-1, groupId=acoes-em-lote-group] Subscribed to topic(s): sinaf-des-autorizacao-reprovar
2026-10-13T12:20:22.537-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.clients.consumer.ConsumerConfig    : ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.include.jmx.reporter = true
	auto.offset.reset = latest
	bootstrap.servers = [cp4i-des-kafka-bootstrap-cp4i.apps.kafka-nprd.caixa:443]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-acoes-em-lote-group-2
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = false
	enable.metrics.push = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = acoes-em-lote-group
	group.instance.id = null
	group.protocol = classic
	group.remote.assignor = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metadata.recovery.strategy = none
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.max.ms = 1000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = [hidden]
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = SCRAM-SHA-512
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = SASL_SSL
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = /tmp/truststore-kafka4170702909817137176.jks
	ssl.truststore.password = [hidden]
	ssl.truststore.type = JKS
	value.deserializer = class org.springframework.kafka.support.serializer.JsonDeserializer

2026-10-13T12:20:22.538-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.c.t.i.KafkaMetricsCollector        : initializing Kafka metrics collector
2026-10-13T12:20:22.545-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka version: 3.8.1
2026-10-13T12:20:22.545-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka commitId: 70d6ff42debf7e17
2026-10-13T12:20:22.545-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka startTimeMs: 1791904822545
2026-10-13T12:20:22.545-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.c.c.internals.LegacyKafkaConsumer  : [Consumer clientId=consumer-acoes-em-lote-group-2, groupId=acoes-em-lote-group] Subscribed to topic(s): sinaf-des-cancelamento
2026-10-13T12:20:22.547-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.clients.consumer.ConsumerConfig    : ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.include.jmx.reporter = true
	auto.offset.reset = latest
	bootstrap.servers = [cp4i-des-kafka-bootstrap-cp4i.apps.kafka-nprd.caixa:443]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-acoes-em-lote-group-3
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = false
	enable.metrics.push = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = acoes-em-lote-group
	group.instance.id = null
	group.protocol = classic
	group.remote.assignor = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metadata.recovery.strategy = none
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.max.ms = 1000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = [hidden]
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = SCRAM-SHA-512
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = SASL_SSL
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = /tmp/truststore-kafka4170702909817137176.jks
	ssl.truststore.password = [hidden]
	ssl.truststore.type = JKS
	value.deserializer = class org.springframework.kafka.support.serializer.JsonDeserializer

2026-10-13T12:20:22.548-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.c.t.i.KafkaMetricsCollector        : initializing Kafka metrics collector
2026-10-13T12:20:22.619-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka version: 3.8.1
2026-10-13T12:20:22.619-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka commitId: 70d6ff42debf7e17
2026-10-13T12:20:22.619-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka startTimeMs: 1791904822619
2026-10-13T12:20:22.619-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.c.c.internals.LegacyKafkaConsumer  : [Consumer clientId=consumer-acoes-em-lote-group-3, groupId=acoes-em-lote-group] Subscribed to topic(s): sinaf-des-excluir
2026-10-13T12:20:22.621-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.clients.consumer.ConsumerConfig    : ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.include.jmx.reporter = true
	auto.offset.reset = latest
	bootstrap.servers = [cp4i-des-kafka-bootstrap-cp4i.apps.kafka-nprd.caixa:443]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-acoes-em-lote-group-4
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = false
	enable.metrics.push = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = acoes-em-lote-group
	group.instance.id = null
	group.protocol = classic
	group.remote.assignor = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metadata.recovery.strategy = none
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.max.ms = 1000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = [hidden]
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = SCRAM-SHA-512
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = SASL_SSL
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = /tmp/truststore-kafka4170702909817137176.jks
	ssl.truststore.password = [hidden]
	ssl.truststore.type = JKS
	value.deserializer = class org.springframework.kafka.support.serializer.JsonDeserializer

2026-10-13T12:20:22.622-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.c.t.i.KafkaMetricsCollector        : initializing Kafka metrics collector
2026-10-13T12:20:22.628-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka version: 3.8.1
2026-10-13T12:20:22.628-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka commitId: 70d6ff42debf7e17
2026-10-13T12:20:22.628-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka startTimeMs: 1791904822628
2026-10-13T12:20:22.628-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.c.c.internals.LegacyKafkaConsumer  : [Consumer clientId=consumer-acoes-em-lote-group-4, groupId=acoes-em-lote-group] Subscribed to topic(s): sinaf-des-finalizacao
2026-10-13T12:20:22.630-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.clients.consumer.ConsumerConfig    : ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.include.jmx.reporter = true
	auto.offset.reset = latest
	bootstrap.servers = [cp4i-des-kafka-bootstrap-cp4i.apps.kafka-nprd.caixa:443]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-acoes-em-lote-group-5
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = false
	enable.metrics.push = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = acoes-em-lote-group
	group.instance.id = null
	group.protocol = classic
	group.remote.assignor = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metadata.recovery.strategy = none
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.max.ms = 1000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = [hidden]
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = SCRAM-SHA-512
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = SASL_SSL
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = /tmp/truststore-kafka4170702909817137176.jks
	ssl.truststore.password = [hidden]
	ssl.truststore.type = JKS
	value.deserializer = class org.springframework.kafka.support.serializer.JsonDeserializer

2026-10-13T12:20:22.630-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.c.t.i.KafkaMetricsCollector        : initializing Kafka metrics collector
2026-10-13T12:20:22.635-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka version: 3.8.1
2026-10-13T12:20:22.635-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka commitId: 70d6ff42debf7e17
2026-10-13T12:20:22.635-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka startTimeMs: 1791904822635
2026-10-13T12:20:22.635-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.c.c.internals.LegacyKafkaConsumer  : [Consumer clientId=consumer-acoes-em-lote-group-5, groupId=acoes-em-lote-group] Subscribed to topic(s): sinaf-des-autorizacao-aprovar
2026-10-13T12:20:22.637-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.clients.consumer.ConsumerConfig    : ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.include.jmx.reporter = true
	auto.offset.reset = latest
	bootstrap.servers = [cp4i-des-kafka-bootstrap-cp4i.apps.kafka-nprd.caixa:443]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-acoes-em-lote-group-6
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = false
	enable.metrics.push = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = acoes-em-lote-group
	group.instance.id = null
	group.protocol = classic
	group.remote.assignor = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metadata.recovery.strategy = none
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.max.ms = 1000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = [hidden]
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = SCRAM-SHA-512
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = SASL_SSL
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = /tmp/truststore-kafka4170702909817137176.jks
	ssl.truststore.password = [hidden]
	ssl.truststore.type = JKS
	value.deserializer = class org.springframework.kafka.support.serializer.JsonDeserializer

2026-10-13T12:20:22.637-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.c.t.i.KafkaMetricsCollector        : initializing Kafka metrics collector
2026-10-13T12:20:22.642-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka version: 3.8.1
2026-10-13T12:20:22.642-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka commitId: 70d6ff42debf7e17
2026-10-13T12:20:22.642-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.kafka.common.utils.AppInfoParser     : Kafka startTimeMs: 1791904822642
2026-10-13T12:20:22.642-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] o.a.k.c.c.internals.LegacyKafkaConsumer  : [Consumer clientId=consumer-acoes-em-lote-group-6, groupId=acoes-em-lote-group] Subscribed to topic(s): sinaf-des-autorizacao-devolver-complemento
2026-10-13T12:20:22.730-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] g.c.b.s.AcoesEmLoteMensageriaApplication : Started AcoesEmLoteMensageriaApplication in 17.71 seconds (process running for 19.586)
2026-10-13T12:20:24.928-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#3-0-C-1] org.apache.kafka.clients.Metadata        : [Consumer clientId=consumer-acoes-em-lote-group-2, groupId=acoes-em-lote-group] Cluster ID: lL6QTmn1Qx29SdmKVKjTyQ
2026-10-13T12:20:24.930-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#3-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-2, groupId=acoes-em-lote-group] Discovered group coordinator cp4i-des-kafka-2-cp4i.apps.kafka-nprd.caixa:443 (id: 2147483645 rack: null)
2026-10-13T12:20:25.019-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#4-0-C-1] org.apache.kafka.clients.Metadata        : [Consumer clientId=consumer-acoes-em-lote-group-3, groupId=acoes-em-lote-group] Cluster ID: lL6QTmn1Qx29SdmKVKjTyQ
2026-10-13T12:20:25.020-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#3-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-2, groupId=acoes-em-lote-group] (Re-)joining group
2026-10-13T12:20:25.020-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#4-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-3, groupId=acoes-em-lote-group] Discovered group coordinator cp4i-des-kafka-2-cp4i.apps.kafka-nprd.caixa:443 (id: 2147483645 rack: null)
2026-10-13T12:20:25.021-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#0-0-C-1] org.apache.kafka.clients.Metadata        : [Consumer clientId=consumer-acoes-em-lote-group-5, groupId=acoes-em-lote-group] Cluster ID: lL6QTmn1Qx29SdmKVKjTyQ
2026-10-13T12:20:25.021-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#4-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-3, groupId=acoes-em-lote-group] (Re-)joining group
2026-10-13T12:20:25.021-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#0-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-5, groupId=acoes-em-lote-group] Discovered group coordinator cp4i-des-kafka-2-cp4i.apps.kafka-nprd.caixa:443 (id: 2147483645 rack: null)
2026-10-13T12:20:25.022-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#0-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-5, groupId=acoes-em-lote-group] (Re-)joining group
2026-10-13T12:20:25.026-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#1-0-C-1] org.apache.kafka.clients.Metadata        : [Consumer clientId=consumer-acoes-em-lote-group-6, groupId=acoes-em-lote-group] Cluster ID: lL6QTmn1Qx29SdmKVKjTyQ
2026-10-13T12:20:25.026-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#5-0-C-1] org.apache.kafka.clients.Metadata        : [Consumer clientId=consumer-acoes-em-lote-group-4, groupId=acoes-em-lote-group] Cluster ID: lL6QTmn1Qx29SdmKVKjTyQ
2026-10-13T12:20:25.026-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#2-0-C-1] org.apache.kafka.clients.Metadata        : [Consumer clientId=consumer-acoes-em-lote-group-1, groupId=acoes-em-lote-group] Cluster ID: lL6QTmn1Qx29SdmKVKjTyQ
2026-10-13T12:20:25.027-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#1-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-6, groupId=acoes-em-lote-group] Discovered group coordinator cp4i-des-kafka-2-cp4i.apps.kafka-nprd.caixa:443 (id: 2147483645 rack: null)
2026-10-13T12:20:25.027-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#5-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-4, groupId=acoes-em-lote-group] Discovered group coordinator cp4i-des-kafka-2-cp4i.apps.kafka-nprd.caixa:443 (id: 2147483645 rack: null)
2026-10-13T12:20:25.027-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#2-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-1, groupId=acoes-em-lote-group] Discovered group coordinator cp4i-des-kafka-2-cp4i.apps.kafka-nprd.caixa:443 (id: 2147483645 rack: null)
2026-10-13T12:20:25.028-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#1-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-6, groupId=acoes-em-lote-group] (Re-)joining group
2026-10-13T12:20:25.028-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#5-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-4, groupId=acoes-em-lote-group] (Re-)joining group
2026-10-13T12:20:25.028-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#2-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-1, groupId=acoes-em-lote-group] (Re-)joining group
2026-10-13T12:20:25.119-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#2-0-C-1] o.a.k.c.t.i.ClientTelemetryReporter      : Client telemetry registered with client instance id: zYmzZlB4T2q1pBtSnrlwqw
2026-10-13T12:20:25.119-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#1-0-C-1] o.a.k.c.t.i.ClientTelemetryReporter      : Client telemetry registered with client instance id: negcpchZR3eaN4rcMlY13Q
2026-10-13T12:20:25.119-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#3-0-C-1] o.a.k.c.t.i.ClientTelemetryReporter      : Client telemetry registered with client instance id: FevpU01RRfaPgLug6nagxg
2026-10-13T12:20:25.119-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#5-0-C-1] o.a.k.c.t.i.ClientTelemetryReporter      : Client telemetry registered with client instance id: tyJe5KmMQcWdzdWEa_VuCQ
2026-10-13T12:20:25.119-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#0-0-C-1] o.a.k.c.t.i.ClientTelemetryReporter      : Client telemetry registered with client instance id: zthFYmwAR_eOhAImwfzd5g
2026-10-13T12:20:25.425-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#0-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-5, groupId=acoes-em-lote-group] Request joining group due to: need to re-join with the given member-id: consumer-acoes-em-lote-group-5-04826bf5-55bb-4a15-b81a-80dfa0199cc3
2026-10-13T12:20:25.425-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#0-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-5, groupId=acoes-em-lote-group] (Re-)joining group
2026-10-13T12:20:25.434-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#1-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-6, groupId=acoes-em-lote-group] Request joining group due to: need to re-join with the given member-id: consumer-acoes-em-lote-group-6-aef4fa6e-b746-44cc-9ced-8362e761a9d6
2026-10-13T12:20:25.434-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#1-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-6, groupId=acoes-em-lote-group] (Re-)joining group
2026-10-13T12:20:25.434-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#3-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-2, groupId=acoes-em-lote-group] Request joining group due to: need to re-join with the given member-id: consumer-acoes-em-lote-group-2-ee42d37b-bc3a-441d-8cc2-727772707714
2026-10-13T12:20:25.435-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#3-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-2, groupId=acoes-em-lote-group] (Re-)joining group
2026-10-13T12:20:25.518-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#2-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-1, groupId=acoes-em-lote-group] Request joining group due to: need to re-join with the given member-id: consumer-acoes-em-lote-group-1-68382f63-7219-41e7-a05c-bb91f4e33290
2026-10-13T12:20:25.518-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#5-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-4, groupId=acoes-em-lote-group] Request joining group due to: need to re-join with the given member-id: consumer-acoes-em-lote-group-4-e995d2f3-0359-4c62-91c8-5b12a4204a51
2026-10-13T12:20:25.518-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#2-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-1, groupId=acoes-em-lote-group] (Re-)joining group
2026-10-13T12:20:25.518-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#5-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-4, groupId=acoes-em-lote-group] (Re-)joining group
2026-10-13T12:20:25.522-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#4-0-C-1] o.a.k.c.t.i.ClientTelemetryReporter      : Client telemetry registered with client instance id: mHQJx5NORciQzysXsKiQ-g
2026-10-13T12:20:25.522-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#4-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-3, groupId=acoes-em-lote-group] Request joining group due to: need to re-join with the given member-id: consumer-acoes-em-lote-group-3-6224b05f-149a-4119-8063-fd52d6b3e752
2026-10-13T12:20:25.523-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#4-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-3, groupId=acoes-em-lote-group] (Re-)joining group
2026-10-13T12:20:28.330-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#1-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-6, groupId=acoes-em-lote-group] Successfully joined group with generation Generation{generationId=458, memberId='consumer-acoes-em-lote-group-6-aef4fa6e-b746-44cc-9ced-8362e761a9d6', protocol='range'}
2026-10-13T12:20:28.330-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#4-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-3, groupId=acoes-em-lote-group] Successfully joined group with generation Generation{generationId=458, memberId='consumer-acoes-em-lote-group-3-6224b05f-149a-4119-8063-fd52d6b3e752', protocol='range'}
2026-10-13T12:20:28.330-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#0-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-5, groupId=acoes-em-lote-group] Successfully joined group with generation Generation{generationId=458, memberId='consumer-acoes-em-lote-group-5-04826bf5-55bb-4a15-b81a-80dfa0199cc3', protocol='range'}
2026-10-13T12:20:28.330-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#2-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-1, groupId=acoes-em-lote-group] Successfully joined group with generation Generation{generationId=458, memberId='consumer-acoes-em-lote-group-1-68382f63-7219-41e7-a05c-bb91f4e33290', protocol='range'}
2026-10-13T12:20:28.330-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#5-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-4, groupId=acoes-em-lote-group] Successfully joined group with generation Generation{generationId=458, memberId='consumer-acoes-em-lote-group-4-e995d2f3-0359-4c62-91c8-5b12a4204a51', protocol='range'}
2026-10-13T12:20:28.330-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#3-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-2, groupId=acoes-em-lote-group] Successfully joined group with generation Generation{generationId=458, memberId='consumer-acoes-em-lote-group-2-ee42d37b-bc3a-441d-8cc2-727772707714', protocol='range'}
2026-10-13T12:20:28.341-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#0-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-5, groupId=acoes-em-lote-group] Successfully synced group in generation Generation{generationId=458, memberId='consumer-acoes-em-lote-group-5-04826bf5-55bb-4a15-b81a-80dfa0199cc3', protocol='range'}
2026-10-13T12:20:28.341-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#5-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-4, groupId=acoes-em-lote-group] Successfully synced group in generation Generation{generationId=458, memberId='consumer-acoes-em-lote-group-4-e995d2f3-0359-4c62-91c8-5b12a4204a51', protocol='range'}
2026-10-13T12:20:28.341-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#2-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-1, groupId=acoes-em-lote-group] Successfully synced group in generation Generation{generationId=458, memberId='consumer-acoes-em-lote-group-1-68382f63-7219-41e7-a05c-bb91f4e33290', protocol='range'}
2026-10-13T12:20:28.341-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#3-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-2, groupId=acoes-em-lote-group] Successfully synced group in generation Generation{generationId=458, memberId='consumer-acoes-em-lote-group-2-ee42d37b-bc3a-441d-8cc2-727772707714', protocol='range'}
2026-10-13T12:20:28.341-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#4-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-3, groupId=acoes-em-lote-group] Successfully synced group in generation Generation{generationId=458, memberId='consumer-acoes-em-lote-group-3-6224b05f-149a-4119-8063-fd52d6b3e752', protocol='range'}
2026-10-13T12:20:28.342-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#1-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-6, groupId=acoes-em-lote-group] Successfully synced group in generation Generation{generationId=458, memberId='consumer-acoes-em-lote-group-6-aef4fa6e-b746-44cc-9ced-8362e761a9d6', protocol='range'}
2026-10-13T12:20:28.344-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#1-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-6, groupId=acoes-em-lote-group] Notifying assignor about the new Assignment(partitions=[sinaf-des-autorizacao-devolver-complemento-2])
2026-10-13T12:20:28.344-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#2-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-1, groupId=acoes-em-lote-group] Notifying assignor about the new Assignment(partitions=[sinaf-des-autorizacao-reprovar-0])
2026-10-13T12:20:28.344-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#4-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-3, groupId=acoes-em-lote-group] Notifying assignor about the new Assignment(partitions=[sinaf-des-excluir-1])
2026-10-13T12:20:28.344-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#3-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-2, groupId=acoes-em-lote-group] Notifying assignor about the new Assignment(partitions=[sinaf-des-cancelamento-2])
2026-10-13T12:20:28.344-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#5-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-4, groupId=acoes-em-lote-group] Notifying assignor about the new Assignment(partitions=[sinaf-des-finalizacao-2])
2026-10-13T12:20:28.344-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#0-0-C-1] o.a.k.c.c.internals.ConsumerCoordinator  : [Consumer clientId=consumer-acoes-em-lote-group-5, groupId=acoes-em-lote-group] Notifying assignor about the new Assignment(partitions=[sinaf-des-autorizacao-aprovar-0])
2026-10-13T12:20:28.346-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#5-0-C-1] k.c.c.i.ConsumerRebalanceListenerInvoker : [Consumer clientId=consumer-acoes-em-lote-group-4, groupId=acoes-em-lote-group] Adding newly assigned partitions: sinaf-des-finalizacao-2
2026-10-13T12:20:28.346-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#2-0-C-1] k.c.c.i.ConsumerRebalanceListenerInvoker : [Consumer clientId=consumer-acoes-em-lote-group-1, groupId=acoes-em-lote-group] Adding newly assigned partitions: sinaf-des-autorizacao-reprovar-0
2026-10-13T12:20:28.346-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#4-0-C-1] k.c.c.i.ConsumerRebalanceListenerInvoker : [Consumer clientId=consumer-acoes-em-lote-group-3, groupId=acoes-em-lote-group] Adding newly assigned partitions: sinaf-des-excluir-1
2026-10-13T12:20:28.346-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#1-0-C-1] k.c.c.i.ConsumerRebalanceListenerInvoker : [Consumer clientId=consumer-acoes-em-lote-group-6, groupId=acoes-em-lote-group] Adding newly assigned partitions: sinaf-des-autorizacao-devolver-complemento-2
2026-10-13T12:20:28.346-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#3-0-C-1] k.c.c.i.ConsumerRebalanceListenerInvoker : [Consumer clientId=consumer-acoes-em-lote-group-2, groupId=acoes-em-lote-group] Adding newly assigned partitions: sinaf-des-cancelamento-2
2026-10-13T12:20:28.346-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#0-0-C-1] k.c.c.i.ConsumerRebalanceListenerInvoker : [Consumer clientId=consumer-acoes-em-lote-group-5, groupId=acoes-em-lote-group] Adding newly assigned partitions: sinaf-des-autorizacao-aprovar-0
2026-10-13T12:20:28.355-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#1-0-C-1] o.a.k.c.c.internals.ConsumerUtils        : Setting offset for partition sinaf-des-autorizacao-devolver-complemento-2 to the committed offset FetchPosition{offset=4, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[cp4i-des-kafka-2-cp4i.apps.kafka-nprd.caixa:443 (id: 2 rack: null)], epoch=69}}
2026-10-13T12:20:28.355-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#0-0-C-1] o.a.k.c.c.internals.ConsumerUtils        : Setting offset for partition sinaf-des-autorizacao-aprovar-0 to the committed offset FetchPosition{offset=41, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[cp4i-des-kafka-0-cp4i.apps.kafka-nprd.caixa:443 (id: 0 rack: null)], epoch=67}}
2026-10-13T12:20:28.355-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#4-0-C-1] o.a.k.c.c.internals.ConsumerUtils        : Setting offset for partition sinaf-des-excluir-1 to the committed offset FetchPosition{offset=62, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[cp4i-des-kafka-1-cp4i.apps.kafka-nprd.caixa:443 (id: 1 rack: null)], epoch=71}}
2026-10-13T12:20:28.356-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#0-0-C-1] o.s.k.l.KafkaMessageListenerContainer    : acoes-em-lote-group: partitions assigned: [sinaf-des-autorizacao-aprovar-0]
2026-10-13T12:20:28.417-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#1-0-C-1] o.s.k.l.KafkaMessageListenerContainer    : acoes-em-lote-group: partitions assigned: [sinaf-des-autorizacao-devolver-complemento-2]
2026-10-13T12:20:28.417-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#2-0-C-1] o.a.k.c.c.internals.ConsumerUtils        : Setting offset for partition sinaf-des-autorizacao-reprovar-0 to the committed offset FetchPosition{offset=9, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[cp4i-des-kafka-2-cp4i.apps.kafka-nprd.caixa:443 (id: 2 rack: null)], epoch=69}}
2026-10-13T12:20:28.417-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#3-0-C-1] o.a.k.c.c.internals.ConsumerUtils        : Setting offset for partition sinaf-des-cancelamento-2 to the committed offset FetchPosition{offset=7, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[cp4i-des-kafka-0-cp4i.apps.kafka-nprd.caixa:443 (id: 0 rack: null)], epoch=67}}
2026-10-13T12:20:28.417-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#5-0-C-1] o.a.k.c.c.internals.ConsumerUtils        : Setting offset for partition sinaf-des-finalizacao-2 to the committed offset FetchPosition{offset=25, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[cp4i-des-kafka-0-cp4i.apps.kafka-nprd.caixa:443 (id: 0 rack: null)], epoch=67}}
2026-10-13T12:20:28.418-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#3-0-C-1] o.s.k.l.KafkaMessageListenerContainer    : acoes-em-lote-group: partitions assigned: [sinaf-des-cancelamento-2]
2026-10-13T12:20:28.418-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#5-0-C-1] o.s.k.l.KafkaMessageListenerContainer    : acoes-em-lote-group: partitions assigned: [sinaf-des-finalizacao-2]
2026-10-13T12:20:28.418-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#4-0-C-1] o.s.k.l.KafkaMessageListenerContainer    : acoes-em-lote-group: partitions assigned: [sinaf-des-excluir-1]
2026-10-13T12:20:28.418-03:00  INFO 8 --- [acoes-em-lote-mensageria] [ntainer#2-0-C-1] o.s.k.l.KafkaMessageListenerContainer    : acoes-em-lote-group: partitions assigned: [sinaf-des-autorizacao-reprovar-0]
2026-10-13T12:21:12.819-03:00  INFO 8 --- [acoes-em-lote-mensageria] [0.0-8080-exec-1] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring DispatcherServlet 'dispatcherServlet'
2026-10-13T12:21:12.819-03:00  INFO 8 --- [acoes-em-lote-mensageria] [0.0-8080-exec-1] o.s.web.servlet.DispatcherServlet        : Initializing Servlet 'dispatcherServlet'
2026-10-13T12:21:12.820-03:00  INFO 8 --- [acoes-em-lote-mensageria] [0.0-8080-exec-1] o.s.web.servlet.DispatcherServlet        : Completed initialization in 1 ms




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
SINAF-acoes-em-lote-mensageria
/
SINAF-acoes-em-lote-mensageria-20261009.1436-1.2.03-SNAPSHOT(2)
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
SINAF-acoes-em-lote-mensageria

SINAF-acoes-em-lote-mensageria-20261009.1436-1.2.03-SNAPSHOT(2)


EC DES

Succeeded


Pipeline

Tasks

Variables

Logs

Tests
Agent job
Started: 13/10/2026, 12:18:43
Pool:
Release-Linux
·
Agent: cadsvaprlx072.intra.caixa.gov.br

3m 5s

Initialize job
·
succeeded
<1s

Download Artifacts
·
succeeded
1 warning
<1s

Recuperando nome do repositório
·
succeeded
2s

Convertendo Minúsculo e Definindo nome do Projeto/Repositório
·
succeeded
<1s

Git clone https://devops.caixa/projetos/Infraestrutura/_git/esteira-logs
·
succeeded
1s

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
1 warning
<1s

Login OpenShift
·
succeeded
1s

Exportando Variáveis de Ambiente "_ENV."
·
succeeded
<1s

Criando novo Projeto
·
succeeded
2s

Adicionando ISTIO_INJECTION
·
skipped


Criando nova APP
·
succeeded
1s

Atualizando Variáveis de Ambiente
·
succeeded
6s

Criando Rota Customizada
·
succeeded
1s

Aplicando Service Mesh
·
skipped


Git clone https://devops.caixa/projetos/Infraestrutura/_git/esteira-beyondtrust-check
·
succeeded
<1s

Create BT Secret
·
succeeded
1s

Create BT Shared Volume
·
succeeded
<1s

Create BT Sidecar
·
succeeded
1s

Create Secret Check Script
·
succeeded
1s

Create Secret Check
·
succeeded
1s

Create BT App Mount Volume
·
succeeded
2s

Exporta Variáveis de Ambiente "_SECRET."
·
succeeded
<1s

Alterando valores placeholder no exec_secret.sh
·
succeeded
<1s

Criando Secrets
·
succeeded
1s

Vinculando Secrets
·
succeeded
1s

Adicionando Multiplas Secrets
·
succeeded
<1s

Executando Tag na Imagem do ambiente de build OKD3, OKD4 e OCP
·
succeeded
22s

Concedendo Acesso OKD
·
succeeded
1s

Verificando IP de Saída
·
succeeded
1s

Configurando IP de Saída - deployment
·
skipped


Configurando IP de Saída - deploymentconfig
·
succeeded
1s

Cadastrando no Portal IIF
·
succeeded
<1s

Verificando Status do Deployment
·
succeeded
1m 25s

Logs da Aplicação
·
succeeded
1s

Resumo da Release
·
succeeded
1s

Coletando dados da imagem
·
succeeded
25s

Atualizando versão no PortalIF
·
succeeded
1s

Realizando Logout OKD
·
succeeded
<1s

Finalize Job
·
succeeded
<1s
View detailed logs
Expanded

Collapsed

1 pipelines found

Row 2

Row 2

Row 2

Showing filters 1 through 2

Showing 26 deployments

Row 2

Row 2


