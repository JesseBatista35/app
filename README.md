<img width="1898" height="991" alt="image" src="https://github.com/user-attachments/assets/61dba3a1-2937-46f4-b61a-afb816f14448" />


pod novo
P
sispi-med-gestao-des-23-465cq
Running


exec java -Dquarkus.http.host=0.0.0.0 -Dquarkus.http.port=8080 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Djavax.net.ssl.trustStore=/deployments/caixa-truststore-acteste-nprd.jks -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/quarkus-run.jar
__ ____ __ _____ ___ __ ____ ______
--/ __ \/ / / / _ | / _ \/ //_/ / / / __/
-/ /_/ / /_/ / __ |/ , _/ ,< / /_/ /\ \
--\___\_\____/_/ |_/_/|_/_/|_|\____/___/
14:54:10 WARN [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.config] (main) [SISPI][MED][GESTAO] Unrecognized configuration key "quarkus.http.cors" was provided; it will be ignored; verify that the dependency extension for this configuration is set or that you did not make a typo
14:54:10 WARN [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.config] (main) [SISPI][MED][GESTAO] Unrecognized configuration key "quarkus.log.console.charset" was provided; it will be ignored; verify that the dependency extension for this configuration is set or that you did not make a typo
14:54:10 WARN [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.config] (main) [SISPI][MED][GESTAO] Unrecognized configuration key "quarkus.http.encoding.default-charset" was provided; it will be ignored; verify that the dependency extension for this configuration is set or that you did not make a typo
14:54:10 WARN [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.config] (main) [SISPI][MED][GESTAO] Unrecognized configuration key "quarkus.http.encoding.force" was provided; it will be ignored; verify that the dependency extension for this configuration is set or that you did not make a typo
14:54:10 WARN [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.config] (main) [SISPI][MED][GESTAO] Unrecognized configuration key "quarkus.resteasy-reactive.json.default-charset" was provided; it will be ignored; verify that the dependency extension for this configuration is set or that you did not make a typo
14:54:10 WARN [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.config] (main) [SISPI][MED][GESTAO] Unrecognized configuration key "quarkus.http.encoding.enabled" was provided; it will be ignored; verify that the dependency extension for this configuration is set or that you did not make a typo
14:54:10 WARN [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.tl.ru.CertificateRecorder] (main) [SISPI][MED][GESTAO] TLS certificate validation disabled via trust-all configuration - name: <default>
14:54:10 WARN [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.qu.tl.ru.CertificateRecorder] (main) [SISPI][MED][GESTAO] This configuration is INSECURE and must not be used in production
14:54:11 INFO [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.quarkus] (main) [SISPI][MED][GESTAO] sispi-med-gestao 1.0.0-SNAPSHOT on JVM (powered by Quarkus 3.40.1) started in 4.404s. Listening on: http://0.0.0.0:8080
14:54:11 INFO [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.quarkus] (main) [SISPI][MED][GESTAO] Profile prod activated.
14:54:11 INFO [CORRELATION-ID - ] [MED-CALLER - ] [ORIGINAL-CLIENT-ID - ] [io.quarkus] (main) [SISPI][MED][GESTAO] Installed features: [agroal, cache, cdi, correlation-id, hibernate-orm, hibernate-validator, jdbc-oracle, narayana-jta, problem-details, rest, rest-client, rest-client-jackson, rest-jackson, scheduler, servlet, smallrye-context-propagation, smallrye-fault-tolerance, smallrye-health, smallrye-openapi, swagger-ui, token-service, validacao-token, vertx]


<img width="1585" height="861" alt="image" src="https://github.com/user-attachments/assets/557fca9e-51c6-45a7-b175-097c22f092fc" />


exec java -Dquarkus.http.host=0.0.0.0 -Dquarkus.http.port=8080 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Xms1536m -Xmx1536m -Dquarkus.log.category."br.gov.caixa.med".level=DEBUG -Dquarkus.log.category."br.gov.caixa.med".min-level=DEBUG -javaagent:/opt/apm_agent/elastic-apm-agent.jar -Delastic.apm.config_file=/opt/apm_agent/elasticapm.properties -Delastic.apm.service_name=sispi -Delastic.apm.environment=des -Delastic.apm.application_packages=br.gov.caixa -Delastic.apm.server_urls=http://apm-server-devops.apps.produtos4.caixa -Delastic.apm.global_labels=deployment=sispi-med-auditoria -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/quarkus-run.jar
Picked up JAVA_TOOL_OPTIONS: -Dfile.encoding=UTF8
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
__  ____  __  _____   ___  __ ____  ______ 
 --/ __ \/ / / / _ | / _ \/ //_/ / / / __/ 
 -/ /_/ / /_/ / __ |/ , _/ ,< / /_/ /\ \   
--\___\_\____/_/ |_/_/|_/_/|_|\____/___/   
2026-10-27 14:56:20,905 WARN  [org.hibernate.orm.jdbc.error] (JPA Startup Thread) HHH000247: ErrorCode: 0, SQLState: null
2026-10-27 14:56:20,907 WARN  [org.hibernate.orm.jdbc.error] (JPA Startup Thread) Acquisition timeout while waiting for new connection
2026-10-27 14:56:20,908 WARN  [org.hibernate.orm.jdbc] (JPA Startup Thread) HHH100046: Could not obtain connection to query JDBC database metadata: org.hibernate.exception.GenericJDBCException: Unable to obtain isolated JDBC connection [Acquisition timeout while waiting for new connection] [n/a]
	at org.hibernate.exception.internal.StandardSQLExceptionConverter.convert(StandardSQLExceptionConverter.java:39)
	at org.hibernate.engine.jdbc.spi.SqlExceptionHelper.convert(SqlExceptionHelper.java:115)
	at org.hibernate.engine.jdbc.spi.SqlExceptionHelper.convert(SqlExceptionHelper.java:101)
	at org.hibernate.resource.transaction.backend.jta.internal.JtaIsolationDelegate.convert(JtaIsolationDelegate.java:228)
	at org.hibernate.resource.transaction.backend.jta.internal.JtaIsolationDelegate.doTheWork(JtaIsolationDelegate.java:196)
	at org.hibernate.resource.transaction.backend.jta.internal.JtaIsolationDelegate.lambda$delegateWork$0(JtaIsolationDelegate.java:75)
	at org.hibernate.resource.transaction.backend.jta.internal.JtaIsolationDelegate.doInSuspendedTransaction(JtaIsolationDelegate.java:111)
	at org.hibernate.resource.transaction.backend.jta.internal.JtaIsolationDelegate.delegateWork(JtaIsolationDelegate.java:72)
	at org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator.getJdbcEnvironmentUsingJdbcMetadata(JdbcEnvironmentInitiator.java:366)
	at org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator.getJdbcEnvironment(JdbcEnvironmentInitiator.java:143)
	at org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator.initiateService(JdbcEnvironmentInitiator.java:120)
	at org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator.initiateService(JdbcEnvironmentInitiator.java:80)
	at org.hibernate.boot.registry.internal.StandardServiceRegistryImpl.initiateService(StandardServiceRegistryImpl.java:133)
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.createService(AbstractServiceRegistryImpl.java:260)
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.initializeService(AbstractServiceRegistryImpl.java:235)
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.getService(AbstractServiceRegistryImpl.java:212)
	at org.hibernate.service.ServiceRegistry.requireService(ServiceRegistry.java:66)
	at org.hibernate.engine.jdbc.internal.JdbcServicesImpl.configure(JdbcServicesImpl.java:50)
	at org.hibernate.boot.registry.internal.StandardServiceRegistryImpl.configureService(StandardServiceRegistryImpl.java:139)
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.initializeService(AbstractServiceRegistryImpl.java:244)
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.getService(AbstractServiceRegistryImpl.java:212)
	at org.hibernate.service.ServiceRegistry.requireService(ServiceRegistry.java:66)
	at org.hibernate.boot.internal.SessionFactoryOptionsBuilder.<init>(SessionFactoryOptionsBuilder.java:273)
	at io.quarkus.hibernate.orm.runtime.recording.PrevalidatedQuarkusMetadata.buildSessionFactoryOptionsBuilder(PrevalidatedQuarkusMetadata.java:70)
	at io.quarkus.hibernate.orm.runtime.boot.FastBootEntityManagerFactoryBuilder.build(FastBootEntityManagerFactoryBuilder.java:94)
	at io.quarkus.hibernate.orm.runtime.FastBootHibernatePersistenceProvider.createEntityManagerFactory(FastBootHibernatePersistenceProvider.java:90)
	at jakarta.persistence.Persistence.createEntityManagerFactory(Persistence.java:90)
	at io.quarkus.hibernate.orm.runtime.JPAConfig$LazyPersistenceUnit.get(JPAConfig.java:178)
	at io.quarkus.hibernate.orm.runtime.JPAConfig$1.run(JPAConfig.java:65)
	at java.base/java.lang.Thread.run(Thread.java:1583)
Caused by: java.sql.SQLException: Acquisition timeout while waiting for new connection
	at io.agroal.pool.ConnectionPool.handlerFromSharedCache(ConnectionPool.java:428)
	at io.agroal.pool.ConnectionPool.internalGetConnection(ConnectionPool.java:321)
	at io.agroal.pool.ConnectionPool.getConnection(ConnectionPool.java:294)
	at io.agroal.pool.DataSource.getConnection(DataSource.java:86)
	at io.quarkus.hibernate.orm.runtime.customized.QuarkusConnectionProvider.getConnection(QuarkusConnectionProvider.java:27)
	at org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator$ConnectionProviderJdbcConnectionAccess.obtainConnection(JdbcEnvironmentInitiator.java:508)
	at org.hibernate.resource.transaction.backend.jta.internal.JtaIsolationDelegate.doTheWork(JtaIsolationDelegate.java:193)
	... 25 more
Caused by: java.util.concurrent.TimeoutException
	at java.base/java.util.concurrent.FutureTask.get(FutureTask.java:204)
	at io.agroal.pool.ConnectionPool.handlerFromSharedCache(ConnectionPool.java:390)
	... 31 more

2026-10-27 14:56:21,714 WARN  [org.hibernate.orm.dialect] (JPA Startup Thread) Persistence unit <default>: Could not retrieve the database version to check it is at least 19.0.0
2026-10-27 14:56:21,717 INFO  [org.apache.camel.quarkus.core.CamelBootstrapRecorder] (main) Apache Camel Quarkus 3.33.1 is starting
2026-10-27 14:56:21,718 INFO  [org.apache.camel.main.MainSupport] (main) Apache Camel (Main) 4.18.2 is starting
2026-10-27 14:56:21,977 INFO  [org.apache.camel.impl.engine.AbstractCamelContext] (main) Apache Camel 4.18.2 (camel-1) is starting
2026-10-27 14:56:21,987 INFO  [org.apache.camel.impl.engine.AbstractCamelContext] (main) Routes startup (total:0)
2026-10-27 14:56:21,988 INFO  [org.apache.camel.impl.engine.AbstractCamelContext] (main) Apache Camel 4.18.2 (camel-1) started in 9ms (build:0ms init:0ms start:9ms boot:10s94ms)
2026-10-27 14:56:22,175 INFO  [io.smallrye.reactive.messaging.kafka] (main) SRMSG18229: Configured topics for channel 'mensagensLogAuditoria': [PIX.MED.AUDITORIA.EVENTO.REQUISICAO]
2026-10-27 14:56:22,195 INFO  [io.smallrye.reactive.messaging.kafka] (main) SRMSG18214: Key deserializer omitted, using String as default
2026-10-27 14:56:23,078 INFO  [io.smallrye.reactive.messaging.kafka] (smallrye-kafka-producer-thread-0) SRMSG18258: Kafka producer kafka-dead-letter-topic-producer-kafka-consumer-mensagensLogAuditoria, connected to Kafka brokers 'development-kafka-tlsext-bootstrap-cp4i.apps.pixnprd4.caixa:443', is configured to write records to 'PIX.MED.AUDITORIA.EVENTO.REQUISICAO.DLQ'
2026-10-27 14:56:23,490 INFO  [io.smallrye.reactive.messaging.kafka] (smallrye-kafka-consumer-thread-0) SRMSG18257: Kafka consumer kafka-consumer-mensagensLogAuditoria, connected to Kafka brokers 'development-kafka-tlsext-bootstrap-cp4i.apps.pixnprd4.caixa:443', belongs to the 'auditoria' consumer group and is configured to poll records from [PIX.MED.AUDITORIA.EVENTO.REQUISICAO]
2026-10-27 14:56:24,165 INFO  [io.quarkus] (main) SISPI-med-auditoria 1.0 on JVM (powered by Quarkus 3.33.2.redhat-00004) started in 13.769s. Listening on: http://0.0.0.0:8080
2026-10-27 14:56:24,165 INFO  [io.quarkus] (main) Profile prod activated. 
2026-10-27 14:56:24,165 INFO  [io.quarkus] (main) Installed features: [agroal, camel-core, camel-reactive-streams, camel-smallrye-reactive-messaging, cdi, hibernate-orm, jdbc-oracle, kafka-client, messaging, messaging-kafka, micrometer, narayana-jta, rest, rest-jackson, smallrye-context-propagation, smallrye-fault-tolerance, smallrye-health, vertx]
2026-10-27 14:56:38,243 INFO  [io.smallrye.health] (vert.x-eventloop-thread-0) [!dt dt.trace_sampled=true, dt.trace_id=2ee35040d774f2daabac1666e2cd9752, dt.span_id=3300255499a14310] SRHCK01001: Reporting health down status: {"status":"DOWN","checks":[{"name":"Database connections health check","status":"DOWN","data":{"<default>":"Unable to execute the validation check for the default DataSource: Acquisition timeout while waiting for new connection"}},{"name":"SmallRye Reactive Messaging - readiness check","status":"UP","data":{"mensagensLogAuditoria":"[OK]"}}]}
2026-10-27 14:56:48,220 INFO  [io.smallrye.health] (vert.x-eventloop-thread-1) [!dt dt.trace_sampled=true, dt.trace_id=d215359fe146c8c1b0e985ca3baadba0, dt.span_id=8908a8ae0da3a60d] SRHCK01001: Reporting health down status: {"status":"DOWN","checks":[{"name":"Database connections health check","status":"DOWN","data":{"<default>":"Unable to execute the validation check for the default DataSource: Acquisition timeout while waiting for new connection"}},{"name":"SmallRye Reactive Messaging - readiness check","status":"UP","data":{"mensagensLogAuditoria":"[OK]"}}]}
2026-10-27 14:56:58,219 INFO  [io.smallrye.health] (vert.x-eventloop-thread-1) [!dt dt.trace_sampled=true, dt.trace_id=234d967add4baa4c1ee0f7de96d3ef08, dt.span_id=b11d795108a59647] SRHCK01001: Reporting health down status: {"status":"DOWN","checks":[{"name":"Database connections health check","status":"DOWN","data":{"<default>":"Unable to execute the validation check for the default DataSource: Acquisition timeout while waiting for new connection"}},{"name":"SmallRye Reactive Messaging - readiness check","status":"UP","data":{"mensagensLogAuditoria":"[OK]"}}]}
2026-10-27 14:57:08,219 INFO  [io.smallrye.health] (vert.x-eventloop-thread-1) [!dt dt.trace_sampled=true, dt.trace_id=8858525b546e8b638a507eba104fb2d1, dt.span_id=f1c4ce9b28db55ef] SRHCK01001: Reporting health down status: {"status":"DOWN","checks":[{"name":"Database connections health check","status":"DOWN","data":{"<default>":"Unable to execute the validation check for the default DataSource: Acquisition timeout while waiting for new connection"}},{"name":"SmallRye Reactive Messaging - readiness check","status":"UP","data":{"mensagensLogAuditoria":"[OK]"}}]}
2026-10-27 14:57:15,643 INFO  [io.smallrye.health] (vert.x-eventloop-thread-0) [!dt dt.trace_sampled=true, dt.trace_id=d7354370ef5f50e86aa76bd80c37a48d, dt.span_id=af38ef9875a146b9] SRHCK01001: Reporting health down status: {"status":"DOWN","checks":[{"name":"Database connections health check","status":"DOWN","data":{"<default>":"Unable to execute the validation check for the default DataSource: Acquisition timeout while waiting for new connection"}},{"name":"SmallRye Reactive Messaging - readiness check","status":"UP","data":{"mensagensLogAuditoria":"[OK]"}}]}
2026-10-27 14:57:20,644 INFO  [io.smallrye.health] (vert.x-eventloop-thread-0) [!dt dt.trace_sampled=true, dt.trace_id=c72dfd8e61d1e7a9ea3767e7bcf9a547, dt.span_id=14b61cf98af67373] SRHCK01001: Reporting health down status: {"status":"DOWN","checks":[{"name":"Database connections health check","status":"DOWN","data":{"<default>":"Unable to execute the validation check for the default DataSource: Acquisition timeout while waiting for new connection"}},{"name":"SmallRye Reactive Messaging - readiness check","status":"UP","data":{"mensagensLogAuditoria":"[OK]"}}]}
2026-10-27 14:57:28,218 INFO  [io.smallrye.health] (vert.x-eventloop-thread-0) [!dt dt.trace_sampled=true, dt.trace_id=ce8ba33ef6206fe73fe0f8bfd49ecd8e, dt.span_id=2eafc0402c6e52d3] SRHCK01001: Reporting health down status: {"status":"DOWN","checks":[{"name":"Database connections health check","status":"DOWN","data":{"<default>":"Unable to execute the validation check for the default DataSource: Acquisition timeout while waiting for new connection"}},{"name":"SmallRye Reactive Messaging - readiness check","status":"UP","data":{"mensagensLogAuditoria":"[OK]"}}]}
2026-10-27 14:57:38,219 INFO  [io.smallrye.health] (vert.x-eventloop-thread-0) [!dt dt.trace_sampled=true, dt.trace_id=06f927ae386a79b85854b3c7e8b5673f, dt.span_id=012bf38f851c247a] SRHCK01001: Reporting health down status: {"status":"DOWN","checks":[{"name":"Database connections health check","status":"DOWN","data":{"<default>":"Unable to execute the validation check for the default DataSource: Acquisition timeout while waiting for new connection"}},{"name":"SmallRye Reactive Messaging - readiness check","status":"UP","data":{"mensagensLogAuditoria":"[OK]"}}]}
2026-10-27 14:57:48,218 INFO  [io.smallrye.health] (vert.x-eventloop-thread-0) [!dt dt.trace_sampled=true, dt.trace_id=bcfd026dd207ea1354e1934710980e20, dt.span_id=1035af56c58cb119] SRHCK01001: Reporting health down status: {"status":"DOWN","checks":[{"name":"Database connections health check","status":"DOWN","data":{"<default>":"Unable to execute the validation check for the default DataSource: Acquisition timeout while waiting for new connection"}},{"name":"SmallRye Reactive Messaging - readiness check","status":"UP","data":{"mensagensLogAuditoria":"[OK]"}}]}
2026-10-27 14:57:58,219 INFO  [io.smallrye.health] (vert.x-eventloop-thread-0) [!dt dt.trace_sampled=true, dt.trace_id=ecf6a5bade2fe59f400d13ee59813ee9, dt.span_id=fd62514bf5ea862e] SRHCK01001: Reporting health down status: {"status":"DOWN","checks":[{"name":"Database connections health check","status":"DOWN","data":{"<default>":"Unable to execute the validation check for the default DataSource: Acquisition timeout while waiting for new connection"}},{"name":"SmallRye Reactive Messaging - readiness check","status":"UP","data":{"mensagensLogAuditoria":"[OK]"}}]}
2026-10-27 14:58:08,219 INFO  [io.smallrye.health] (vert.x-eventloop-thread-0) [!dt dt.trace_sampled=true, dt.trace_id=7c0765be36b47918a6a91a426707527e, dt.span_id=37c56b5347e25609] SRHCK01001: Reporting health down status: {"status":"DOWN","checks":[{"name":"Database connections health check","status":"DOWN","data":{"<default>":"Unable to execute the validation check for the default DataSource: Acquisition timeout while waiting for new connection"}},{"name":"SmallRye Reactive Messaging - readiness check","status":"UP","data":{"mensagensLogAuditoria":"[OK]"}}]}
2026-10-27 14:58:18,218 INFO  [io.smallrye.health] (vert.x-eventloop-thread-0) [!dt dt.trace_sampled=true, dt.trace_id=16e3fea6d36543b963323bdce4573a82, dt.span_id=e7081dfeac27ddbf] SRHCK01001: Reporting health down status: {"status":"DOWN","checks":[{"name":"Database connections health check","status":"DOWN","data":{"<default>":"Unable to execute the validation check for the default DataSource: Acquisition timeout while waiting for new connection"}},{"name":"SmallRye Reactive Messaging - readiness check","status":"UP","data":{"mensagensLogAuditoria":"[OK]"}}]}
2026-10-27 14:58:28,219 INFO  [io.smallrye.health] (vert.x-eventloop-thread-1) [!dt dt.trace_sampled=true, dt.trace_id=433ad6d77fdbbe024b42693aa461884a, dt.span_id=d86612ae55cfe5cf] SRHCK01001: Reporting health down status: {"status":"DOWN","checks":[{"name":"Database connections health check","status":"DOWN","data":{"<default>":"Unable to execute the validation check for the default DataSource: Acquisition timeout while waiting for new connection"}},{"name":"SmallRye Reactive Messaging - readiness check","status":"UP","data":{"mensagensLogAuditoria":"[OK]"}}]}
