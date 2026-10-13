sinaf-acoes-em-lote-mensageria-des-91-8fzgx-secrets-agent-sidecar


2026-10-13 15:14:31,618 INFO Getting secrets just once, POLLING_WAIT_BETWEEN_REQUESTS_MINUTES was not configured
2026-10-13 15:14:31,619 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) APP VERSION: 2.1.0
2026-10-13 15:14:31,619 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) Starting Execution...ca87216e-c718-11f1-80ca-0a58190122f0
2026-10-13 15:14:31,619 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) You are using: <,> as List delimiter
2026-10-13 15:14:31,619 WARNING (ca87216e-c718-11f1-80ca-0a58190122f0) InsecureRequestWarning: Unverified HTTPS request is being made to host https://sicsn.caixa/BeyondTrust/api/public/v3'. Adding certificate verification isstrongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
2026-10-13 15:14:31,619 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) Certificate was not configured
2026-10-13 15:14:31,622 DEBUG (ca87216e-c718-11f1-80ca-0a58190122f0) How long to wait for the server to connect and send data before giving up: connection timeout: 30 seconds, request timeout 30 seconds
2026-10-13 15:14:31,622 WARNING (ca87216e-c718-11f1-80ca-0a58190122f0) verify_ca=false is insecure, it instructs the caller to not verify the certificate authority when making API calls.
2026-10-13 15:14:31,774 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) Calling sign_app_in endpoint: https://sicsn.caixa/BeyondTrust/api/public/v3
2026-10-13 15:14:31,824 DEBUG (ca87216e-c718-11f1-80ca-0a58190122f0) Running get_secret method in SecretsSafe class
2026-10-13 15:14:31,824 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) **************** secret path: SINAF_DES/KAFKA_PASS *****************
2026-10-13 15:14:31,829 DEBUG (ca87216e-c718-11f1-80ca-0a58190122f0) Calling get_secret_by_path endpoint: /secrets-safe/secrets?path=SINAF_DES&separator=%2F&version=3.1&title=KAFKA_PASS
2026-10-13 15:14:31,830 DEBUG (ca87216e-c718-11f1-80ca-0a58190122f0) GET request to URL: https://sicsn.caixa/BeyondTrust/api/public/v3/secrets-safe/secrets?path=SINAF_DES&separator=%2F&version=3.1&title=KAFKA_PASS
2026-10-13 15:14:31,938 DEBUG (ca87216e-c718-11f1-80ca-0a58190122f0) Secret type: Text
2026-10-13 15:14:31,938 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) Secret was successfully retrieved
2026-10-13 15:14:31,938 DEBUG (ca87216e-c718-11f1-80ca-0a58190122f0) Running get_secret method in SecretsSafe class
2026-10-13 15:14:31,938 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) **************** secret path: SINAF_DES/KAFKA_TRUSTSTORE_PASS *****************
2026-10-13 15:14:31,939 DEBUG (ca87216e-c718-11f1-80ca-0a58190122f0) Calling get_secret_by_path endpoint: /secrets-safe/secrets?path=SINAF_DES&separator=%2F&version=3.1&title=KAFKA_TRUSTSTORE_PASS
2026-10-13 15:14:31,939 DEBUG (ca87216e-c718-11f1-80ca-0a58190122f0) GET request to URL: https://sicsn.caixa/BeyondTrust/api/public/v3/secrets-safe/secrets?path=SINAF_DES&separator=%2F&version=3.1&title=KAFKA_TRUSTSTORE_PASS
2026-10-13 15:14:32,017 DEBUG (ca87216e-c718-11f1-80ca-0a58190122f0) Secret type: Text
2026-10-13 15:14:32,017 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) Secret was successfully retrieved
2026-10-13 15:14:32,017 DEBUG (ca87216e-c718-11f1-80ca-0a58190122f0) Running get_secret method in SecretsSafe class
2026-10-13 15:14:32,017 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) **************** secret path: SINAF_DES/DATASOURCE_PASSWORD_SNAFPB01 *****************
2026-10-13 15:14:32,018 DEBUG (ca87216e-c718-11f1-80ca-0a58190122f0) Calling get_secret_by_path endpoint: /secrets-safe/secrets?path=SINAF_DES&separator=%2F&version=3.1&title=DATASOURCE_PASSWORD_SNAFPB01
2026-10-13 15:14:32,018 DEBUG (ca87216e-c718-11f1-80ca-0a58190122f0) GET request to URL: https://sicsn.caixa/BeyondTrust/api/public/v3/secrets-safe/secrets?path=SINAF_DES&separator=%2F&version=3.1&title=DATASOURCE_PASSWORD_SNAFPB01
2026-10-13 15:14:32,086 DEBUG (ca87216e-c718-11f1-80ca-0a58190122f0) Secret type: Text
2026-10-13 15:14:32,086 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) Secret was successfully retrieved
2026-10-13 15:14:32,086 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) Secrets folder Path /usr/src/app/secrets_files
2026-10-13 15:14:32,086 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) Creating files with the secrets as content, number of files 6
2026-10-13 15:14:32,086 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) File saved succesfully: /usr/src/app/secrets_files/SINAF_DES/KAFKA_PASS_Metadata
2026-10-13 15:14:32,086 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) File saved succesfully: /usr/src/app/secrets_files/SINAF_DES/KAFKA_PASS
2026-10-13 15:14:32,087 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) File saved succesfully: /usr/src/app/secrets_files/SINAF_DES/KAFKA_TRUSTSTORE_PASS_Metadata
2026-10-13 15:14:32,087 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) File saved succesfully: /usr/src/app/secrets_files/SINAF_DES/KAFKA_TRUSTSTORE_PASS
2026-10-13 15:14:32,087 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) File saved succesfully: /usr/src/app/secrets_files/SINAF_DES/DATASOURCE_PASSWORD_SNAFPB01_Metadata
2026-10-13 15:14:32,087 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) File saved succesfully: /usr/src/app/secrets_files/SINAF_DES/DATASOURCE_PASSWORD_SNAFPB01
2026-10-13 15:14:32,087 DEBUG (ca87216e-c718-11f1-80ca-0a58190122f0) Calling sign_app_out endpoint: https://sicsn.caixa/BeyondTrust/api/public/v3/Auth/Signout
2026-10-13 15:14:32,100 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) {
    "execution_id": "ca87216e-c718-11f1-80ca-0a58190122f0",
    "input": {
        "secret_list": [
            "SINAF_DES/KAFKA_PASS",
            "SINAF_DES/KAFKA_TRUSTSTORE_PASS",
            "SINAF_DES/DATASOURCE_PASSWORD_SNAFPB01"
        ],
        "folder_list": [],
        "managed_account_list": [],
        "secret_safe_url": "https://sicsn.caixa/BeyondTrust/api/public/v3",
        "user": {
            "UserId": 1777,
            "SID": null,
            "EmailAddress": null,
            "UserName": "SNAFDB02",
            "Name": "SNAFDB02"
        }
    },
    "output": {
        "secrets": [
            {
                "path": "SINAF_DES/KAFKA_PASS_Metadata",
                "content": "{\"Username\": null, \"Group\": null, \"FileName\": null, \"FileHash\": null, \"Text\": null, \"SecretType\": \"Text\", \"Id\": \"7bf0fb34-fde6-41cb-fd89-08deb1ca7e32\", \"Title\": \"KAFKA_PASS\", \"Description\": \"\", \"OwnerId\": null, \"GroupId\": null, \"FolderId\": \"203ee177-8d91-4f0d-6204-08ddf245f8ef\", \"CreatedOn\": \"2026-05-25T19:04:15.19Z\", \"CreatedBy\": \"Pedro Souza\", \"ModifiedOn\": \"2026-05-25T19:04:26.3063232Z\", \"ModifiedBy\": \"Pedro Souza\", \"Owner\": null, \"Folder\": \"SINAF_DES\", \"FolderPath\": \"SINAF_DES\", \"Owners\": [{\"OwnerId\": null, \"GroupId\": null, \"UserId\": 1226, \"Owner\": null, \"Name\": \"clientid_SNAFDB01\", \"Email\": null}], \"OwnerType\": null, \"Notes\": \"\", \"Urls\": []}"
            },
            {
                "path": "SINAF_DES/KAFKA_PASS",
                "content": "***************"
            },
            {
                "path": "SINAF_DES/KAFKA_TRUSTSTORE_PASS_Metadata",
                "content": "{\"Username\": null, \"Group\": null, \"FileName\": null, \"FileHash\": null, \"Text\": null, \"SecretType\": \"Text\", \"Id\": \"717059c0-9841-46fc-fd8a-08deb1ca7e32\", \"Title\": \"KAFKA_TRUSTSTORE_PASS\", \"Description\": \"\", \"OwnerId\": null, \"GroupId\": null, \"FolderId\": \"203ee177-8d91-4f0d-6204-08ddf245f8ef\", \"CreatedOn\": \"2026-05-25T19:05:20.6833333Z\", \"CreatedBy\": \"Pedro Souza\", \"ModifiedOn\": \"2026-05-25T19:05:38.9762677Z\", \"ModifiedBy\": \"Pedro Souza\", \"Owner\": null, \"Folder\": \"SINAF_DES\", \"FolderPath\": \"SINAF_DES\", \"Owners\": [{\"OwnerId\": null, \"GroupId\": null, \"UserId\": 1226, \"Owner\": null, \"Name\": \"clientid_SNAFDB01\", \"Email\": null}], \"OwnerType\": null, \"Notes\": \"\", \"Urls\": []}"
            },
            {
                "path": "SINAF_DES/KAFKA_TRUSTSTORE_PASS",
                "content": "***************"
            },
            {
                "path": "SINAF_DES/DATASOURCE_PASSWORD_SNAFPB01_Metadata",
                "content": "{\"Username\": null, \"Group\": null, \"FileName\": null, \"FileHash\": null, \"Text\": null, \"SecretType\": \"Text\", \"Id\": \"e2e996a8-ae94-42cf-2b75-08df2567bc35\", \"Title\": \"DATASOURCE_PASSWORD_SNAFPB01\", \"Description\": \"\", \"OwnerId\": null, \"GroupId\": null, \"FolderId\": \"203ee177-8d91-4f0d-6204-08ddf245f8ef\", \"CreatedOn\": \"2026-10-08T19:40:51.57Z\", \"CreatedBy\": \"Lucas Santos\", \"ModifiedOn\": \"2026-10-08T19:41:09.6007804Z\", \"ModifiedBy\": \"Lucas Santos\", \"Owner\": null, \"Folder\": \"SINAF_DES\", \"FolderPath\": \"SINAF_DES\", \"Owners\": [{\"OwnerId\": null, \"GroupId\": 221, \"UserId\": null, \"Owner\": null, \"Name\": \"SINAF_DES\", \"Email\": null}], \"OwnerType\": null, \"Notes\": \"\", \"Urls\": []}"
            },
            {
                "path": "SINAF_DES/DATASOURCE_PASSWORD_SNAFPB01",
                "content": "***************"
            }
        ],
        "messages": [
            {
                "message": "Creating files with the secrets as content, number of files 6",
                "type": "INFO"
            }
        ],
        "errors": []
    }
}
2026-10-13 15:14:32,100 INFO (ca87216e-c718-11f1-80ca-0a58190122f0) Ending Execution...ca87216e-c718-11f1-80ca-0a58190122f0



secrets-check

--- Resultados da Comparacao ---
Sucesso! O conteudo do diretorio corresponde a lista esperada.




sinaf-acoes-em-lote-mensageria-des-91-8fzgx
CrashLoopBackOff



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

2026-10-13T12:15:41.653-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] g.c.b.s.AcoesEmLoteMensageriaApplication : Starting AcoesEmLoteMensageriaApplication v1.2.03 using Java 21.0.1 with PID 8 (/deployments/demo-1.2.03.jar started by 185 in /deployments)
2026-10-13T12:15:41.655-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] g.c.b.s.AcoesEmLoteMensageriaApplication : No active profile set, falling back to 1 default profile: "default"
2026-10-13T12:15:43.739-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] .s.d.r.c.RepositoryConfigurationDelegate : Bootstrapping Spring Data JPA repositories in DEFAULT mode.
2026-10-13T12:15:43.758-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] .s.d.r.c.RepositoryConfigurationDelegate : Finished Spring Data repository scanning in 12 ms. Found 0 JPA repository interfaces.
2026-10-13T12:15:44.154-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] b.g.c.b.s.c.DatasourcePropertiesLogger   : DATASOURCE url=jdbc:db2://10.192.224.76:5021/CSD1
2026-10-13T12:15:44.155-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] b.g.c.b.s.c.DatasourcePropertiesLogger   : DATASOURCE username=SNAFBD01
2026-10-13T12:15:44.156-03:00  WARN 8 --- [acoes-em-lote-mensageria] [           main] ConfigServletWebServerApplicationContext : Exception encountered during context initialization - cancelling refresh attempt: org.springframework.util.PlaceholderResolutionException: Could not resolve placeholder 'DATASOURCE_PASSWORD_SNAFPB01' in value "${DATASOURCE_PASSWORD_SNAFPB01}"
2026-10-13T12:15:44.228-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] .s.b.a.l.ConditionEvaluationReportLogger : 

Error starting ApplicationContext. To display the condition evaluation report re-run your application with 'debug' enabled.
2026-10-13T12:15:44.242-03:00 ERROR 8 --- [acoes-em-lote-mensageria] [           main] o.s.boot.SpringApplication               : Application run failed

org.springframework.util.PlaceholderResolutionException: Could not resolve placeholder 'DATASOURCE_PASSWORD_SNAFPB01' in value "${DATASOURCE_PASSWORD_SNAFPB01}"
	at org.springframework.util.PlaceholderResolutionException.withValue(PlaceholderResolutionException.java:81) ~[spring-core-6.2.6.jar!/:6.2.6]
	at org.springframework.util.PlaceholderParser$ParsedValue.resolve(PlaceholderParser.java:423) ~[spring-core-6.2.6.jar!/:6.2.6]
	at org.springframework.util.PlaceholderParser.replacePlaceholders(PlaceholderParser.java:128) ~[spring-core-6.2.6.jar!/:6.2.6]
	at org.springframework.util.PropertyPlaceholderHelper.parseStringValue(PropertyPlaceholderHelper.java:118) ~[spring-core-6.2.6.jar!/:6.2.6]
	at org.springframework.util.PropertyPlaceholderHelper.replacePlaceholders(PropertyPlaceholderHelper.java:114) ~[spring-core-6.2.6.jar!/:6.2.6]
	at org.springframework.core.env.AbstractPropertyResolver.doResolvePlaceholders(AbstractPropertyResolver.java:255) ~[spring-core-6.2.6.jar!/:6.2.6]
	at org.springframework.core.env.AbstractPropertyResolver.resolveRequiredPlaceholders(AbstractPropertyResolver.java:226) ~[spring-core-6.2.6.jar!/:6.2.6]
	at org.springframework.core.env.AbstractPropertyResolver.resolveNestedPlaceholders(AbstractPropertyResolver.java:246) ~[spring-core-6.2.6.jar!/:6.2.6]
	at org.springframework.boot.context.properties.source.ConfigurationPropertySourcesPropertyResolver.getProperty(ConfigurationPropertySourcesPropertyResolver.java:81) ~[spring-boot-3.4.5.jar!/:3.4.5]
	at org.springframework.boot.context.properties.source.ConfigurationPropertySourcesPropertyResolver.getProperty(ConfigurationPropertySourcesPropertyResolver.java:62) ~[spring-boot-3.4.5.jar!/:3.4.5]
	at org.springframework.core.env.AbstractEnvironment.getProperty(AbstractEnvironment.java:557) ~[spring-core-6.2.6.jar!/:6.2.6]
	at br.gov.caixa.bsb.sinaf.config.DatasourcePropertiesLogger.postProcessBeanFactory(DatasourcePropertiesLogger.java:32) ~[!/:1.2.03]
	at org.springframework.context.support.PostProcessorRegistrationDelegate.invokeBeanFactoryPostProcessors(PostProcessorRegistrationDelegate.java:363) ~[spring-context-6.2.6.jar!/:6.2.6]
	at org.springframework.context.support.PostProcessorRegistrationDelegate.invokeBeanFactoryPostProcessors(PostProcessorRegistrationDelegate.java:204) ~[spring-context-6.2.6.jar!/:6.2.6]
	at org.springframework.context.support.AbstractApplicationContext.invokeBeanFactoryPostProcessors(AbstractApplicationContext.java:791) ~[spring-context-6.2.6.jar!/:6.2.6]
	at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:609) ~[spring-context-6.2.6.jar!/:6.2.6]
	at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.refresh(ServletWebServerApplicationContext.java:146) ~[spring-boot-3.4.5.jar!/:3.4.5]
	at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:753) ~[spring-boot-3.4.5.jar!/:3.4.5]
	at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:439) ~[spring-boot-3.4.5.jar!/:3.4.5]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:318) ~[spring-boot-3.4.5.jar!/:3.4.5]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1362) ~[spring-boot-3.4.5.jar!/:3.4.5]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1351) ~[spring-boot-3.4.5.jar!/:3.4.5]
	at br.gov.caixa.bsb.sinaf.AcoesEmLoteMensageriaApplication.main(AcoesEmLoteMensageriaApplication.java:10) ~[!/:1.2.03]
	at java.base/jdk.internal.reflect.DirectMethodHandleAccessor.invoke(DirectMethodHandleAccessor.java:103) ~[na:na]
	at java.base/java.lang.reflect.Method.invoke(Method.java:580) ~[na:na]
	at org.springframework.boot.loader.launch.Launcher.launch(Launcher.java:102) ~[demo-1.2.03.jar:1.2.03]
	at org.springframework.boot.loader.launch.Launcher.launch(Launcher.java:64) ~[demo-1.2.03.jar:1.2.03]
	at org.springframework.boot.loader.launch.JarLauncher.main(JarLauncher.java:40) ~[demo-1.2.03.jar:1.2.03]



OKD


Jesse Mouta Pereira Batista

Administrator
Home
Overview
Projects
Search
API Explorer
Events
Operators
OperatorHub
Installed Operators
Workloads
Pods
Deployments
DeploymentConfigs
StatefulSets
Secrets
ConfigMaps
CronJobs
Jobs
DaemonSets
ReplicaSets
ReplicationControllers
HorizontalPodAutoscalers
PodDisruptionBudgets
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
sinaf-acoes-em-lote-mensageria-des-91-8fzgx
CrashLoopBackOff

Actions
Details
Metrics
YAML
Environment
Logs
Events
Terminal
Streaming events...
Showing 16 events
Older events are not stored.
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:15
Generated from kubelet on ceadecldlx071.nprd.caixa
Successfully pulled image "default-route-openshift-image-registry.apps.produtos4.caixa/build-images-ads/sinaf-acoes-em-lote-mensageria:20261009.1436-1.2.03-SNAPSHOT" in 68.786398ms (68.795263ms including waiting)
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:15
Generated from kubelet on ceadecldlx071.nprd.caixa
4 times in the last 1 minute
Created container sinaf-acoes-em-lote-mensageria-des
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:15
Generated from kubelet on ceadecldlx071.nprd.caixa
4 times in the last 1 minute
Pulling image "default-route-openshift-image-registry.apps.produtos4.caixa/build-images-ads/sinaf-acoes-em-lote-mensageria:20261009.1436-1.2.03-SNAPSHOT"
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:15
Generated from kubelet on ceadecldlx071.nprd.caixa
4 times in the last 1 minute
Back-off restarting failed container
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:15
Generated from kubelet on ceadecldlx071.nprd.caixa
Successfully pulled image "default-route-openshift-image-registry.apps.produtos4.caixa/build-images-ads/sinaf-acoes-em-lote-mensageria:20261009.1436-1.2.03-SNAPSHOT" in 89.64033ms (89.652869ms including waiting)
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:15
Generated from kubelet on ceadecldlx071.nprd.caixa
3 times in the last 1 minute
Started container sinaf-acoes-em-lote-mensageria-des
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:14
Generated from kubelet on ceadecldlx071.nprd.caixa
Successfully pulled image "default-route-openshift-image-registry.apps.produtos4.caixa/build-images-ads/sinaf-acoes-em-lote-mensageria:20261009.1436-1.2.03-SNAPSHOT" in 56.058214ms (56.068471ms including waiting)
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:14
Generated from kubelet on ceadecldlx071.nprd.caixa
Successfully pulled image "default-route-openshift-image-registry.apps.produtos4.caixa/build-images-ads/sinaf-acoes-em-lote-mensageria:20261009.1436-1.2.03-SNAPSHOT" in 2.740826223s (2.740834896s including waiting)
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:14
Generated from kubelet on ceadecldlx071.nprd.caixa
Container image "default-route-openshift-image-registry.apps.produtos4.caixa/openshift/ubi:9.3-1552" already present on machine
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:14
Generated from kubelet on ceadecldlx071.nprd.caixa
Created container secrets-check
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:14
Generated from kubelet on ceadecldlx071.nprd.caixa
Started container secrets-check
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:14
Generated from multus
Add eth0 [25.1.34.240/23] from openshift-sdn
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:14
Generated from kubelet on ceadecldlx071.nprd.caixa
Container image "default-route-openshift-image-registry.apps.produtos4.caixa/openshift/secrets-agent:v23.3.2" already present on machine
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:14
Generated from kubelet on ceadecldlx071.nprd.caixa
Created container secrets-agent-sidecar
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:14
Generated from kubelet on ceadecldlx071.nprd.caixa
Started container secrets-agent-sidecar
PodPsinaf-acoes-em-lote-mensageria-des-91-8fzgx
NamespaceNSsinaf-des
13 de out. de 2026, 12:14
Generated from default-scheduler
Successfully assigned sinaf-des/sinaf-acoes-em-lote-mensageria-des-91-8fzgx to ceadecldlx071.nprd.caixa

OKD


Jesse Mouta Pereira Batista

Administrator
Home
Overview
Projects
Search
API Explorer
Events
Operators
OperatorHub
Installed Operators
Workloads
Pods
Deployments
DeploymentConfigs
StatefulSets
Secrets
ConfigMaps
CronJobs
Jobs
DaemonSets
ReplicaSets
ReplicationControllers
HorizontalPodAutoscalers
PodDisruptionBudgets
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
sinaf-acoes-em-lote-mensageria-des-91-8fzgx
CrashLoopBackOff

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
sinaf-acoes-em-lote-mensageria-des-91
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

