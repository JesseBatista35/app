Prezados,

Solicito uma verificação das scripts referentes ao Cofre de Senhas Beyond Trust, no modulo SINAF-acoes-em-lote-mensageria, visto que a aplicação não esta tendo acesso a variável ${DATASOURCE_PASSWORD_SNAFPB01}, com a senha do banco de dados. Esse erro ocorre apenas com essa variável as outras que também estão no cofre de senha funcionam normalmente. Quando colocamos a senha direto na biblioteca, sem passar pelo cofre, funciona normalmente

Segue log da aplicação para consulta

Fico a disposição para responder quaisquer duvidas que venham a surgir


2026-10-09T17:45:52.0262315Z ##[section]Starting: Logs da Aplicação
2026-10-09T17:45:52.0265382Z ==============================================================================
2026-10-09T17:45:52.0265475Z Task         : Bash
2026-10-09T17:45:52.0265521Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-09T17:45:52.0265587Z Version      : 3.227.0
2026-10-09T17:45:52.0265641Z Author       : Microsoft Corporation
2026-10-09T17:45:52.0265695Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-09T17:45:52.0265767Z ==============================================================================
2026-10-09T17:45:53.1893095Z Generating script.
2026-10-09T17:45:53.1906774Z ========================== Starting Command Output ===========================
2026-10-09T17:45:53.1916800Z [command]/bin/bash /opt/ads-agent/_work/_temp/3526e2f7-25d0-46f8-abc2-e471ff7a9c42.sh
2026-10-09T17:45:53.1970665Z + shopt -s expand_aliases
2026-10-09T17:45:53.1970886Z + [[ -n okd4_nprd ]]
2026-10-09T17:45:53.1971046Z + [[ okd4_nprd =~ ocp ]]
2026-10-09T17:45:53.1972164Z + [[ -n okd4_nprd ]]
2026-10-09T17:45:53.1972300Z + [[ okd4_nprd =~ (okd4|openshift) ]]
2026-10-09T17:45:53.1972746Z + app=sinaf-acoes-em-lote-mensageria-des
2026-10-09T17:45:53.1972907Z + oc version
2026-10-09T17:45:53.3590998Z oc v3.11.0+0cbc58b
2026-10-09T17:45:53.3591212Z kubernetes v1.11.0+d4cacc0
2026-10-09T17:45:53.3591510Z features: Basic-Auth GSSAPI Kerberos SPNEGO
2026-10-09T17:45:53.3704661Z 
2026-10-09T17:45:53.3705309Z Server https://api.nprd.caixa:6443
2026-10-09T17:45:53.3705612Z kubernetes v1.25.0-2824+27e744f55d2e99-dirty
2026-10-09T17:45:53.3740368Z ++ oc get pod -l name=sinaf-acoes-em-lote-mensageria-des -n sinaf-des -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-10-09T17:45:53.3741064Z ++ tac
2026-10-09T17:45:53.3741210Z ++ grep -v '^$'
2026-10-09T17:45:53.3742985Z ++ head -n1
2026-10-09T17:45:53.6484184Z + last_pod=sinaf-acoes-em-lote-mensageria-des-90-bkzvw
2026-10-09T17:45:53.6484669Z + echo 'Logs do POD: sinaf-acoes-em-lote-mensageria-des-90-bkzvw'
2026-10-09T17:45:53.6484926Z + oc logs sinaf-acoes-em-lote-mensageria-des-90-bkzvw -c sinaf-acoes-em-lote-mensageria-des -n sinaf-des
2026-10-09T17:45:53.6485214Z Logs do POD: sinaf-acoes-em-lote-mensageria-des-90-bkzvw
2026-10-09T17:45:53.9969012Z exec java -Dserver.address=0.0.0.0 -Dserver.port=8080 -javaagent:/opt/apm_agent/elastic-apm-agent.jar -Delastic.apm.config_file=/opt/apm_agent/elasticapm.properties -Delastic.apm.service_name=sinaf-acoes-em-lote-mensageria -Delastic.apm.environment=des -Delastic.apm.application_packages=br.gov.caixa -Delastic.apm.server_urls=http://apm-server-devops.produtos.caixa -Delastic.apm.global_labels=deployment=sinaf-acoes-em-lote-mensageria -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/demo-1.2.03.jar
2026-10-09T17:45:53.9969858Z OpenJDK 64-Bit Server VM warning: Sharing is only supported for boot loader classes because bootstrap classpath has been appended
2026-10-09T17:45:53.9970151Z WARNING: sun.reflect.Reflection.getCallerClass is not supported. This will impact performance.
2026-10-09T17:45:53.9970387Z Failed to start agent
2026-10-09T17:45:53.9970570Z java.lang.reflect.InvocationTargetException
2026-10-09T17:45:53.9970830Z 	at java.base/jdk.internal.reflect.DirectMethodHandleAccessor.invoke(DirectMethodHandleAccessor.java:118)
2026-10-09T17:45:53.9971108Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:580)
2026-10-09T17:45:53.9971380Z 	at co.elastic.apm.agent.premain.AgentMain.loadAndInitializeAgent(AgentMain.java:155)
2026-10-09T17:45:53.9971777Z 	at co.elastic.apm.agent.premain.AgentMain.init(AgentMain.java:100)
2026-10-09T17:45:53.9972054Z 	at co.elastic.apm.agent.premain.AgentMain.premain(AgentMain.java:56)
2026-10-09T17:45:53.9972352Z 	at java.base/jdk.internal.reflect.DirectMethodHandleAccessor.invoke(DirectMethodHandleAccessor.java:103)
2026-10-09T17:45:53.9972622Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:580)
2026-10-09T17:45:53.9972910Z 	at java.instrument/sun.instrument.InstrumentationImpl.loadClassAndStartAgent(InstrumentationImpl.java:560)
2026-10-09T17:45:53.9973562Z 	at java.instrument/sun.instrument.InstrumentationImpl.loadClassAndCallPremain(InstrumentationImpl.java:572)
2026-10-09T17:45:53.9973951Z Caused by: java.lang.RuntimeException: java.lang.UnsupportedOperationException: Could not access Unsafe class: sun.misc.Unsafe.defineClass(java.lang.String,[B,int,int,java.lang.ClassLoader,java.security.ProtectionDomain)
2026-10-09T17:45:53.9974337Z 	at co.elastic.apm.agent.bci.IndyBootstrap.getIndyBootstrapMethod(IndyBootstrap.java:221)
2026-10-09T17:45:53.9974637Z 	at co.elastic.apm.agent.bci.ElasticApmAgent.getTransformer(ElasticApmAgent.java:436)
2026-10-09T17:45:53.9975110Z 	at co.elastic.apm.agent.bci.ElasticApmAgent.applyAdvice(ElasticApmAgent.java:398)
2026-10-09T17:45:53.9975408Z 	at co.elastic.apm.agent.bci.ElasticApmAgent.initAgentBuilder(ElasticApmAgent.java:321)
2026-10-09T17:45:53.9977437Z 	at co.elastic.apm.agent.bci.ElasticApmAgent.initInstrumentation(ElasticApmAgent.java:267)
2026-10-09T17:45:53.9977709Z 	at co.elastic.apm.agent.bci.ElasticApmAgent.initInstrumentation(ElasticApmAgent.java:171)
2026-10-09T17:45:53.9977911Z 	at co.elastic.apm.agent.bci.ElasticApmAgent.initialize(ElasticApmAgent.java:157)
2026-10-09T17:45:53.9978204Z 	at java.base/jdk.internal.reflect.DirectMethodHandleAccessor.invoke(DirectMethodHandleAccessor.java:103)
2026-10-09T17:45:53.9978366Z 	... 8 more
2026-10-09T17:45:53.9978548Z Caused by: java.lang.UnsupportedOperationException: Could not access Unsafe class: sun.misc.Unsafe.defineClass(java.lang.String,[B,int,int,java.lang.ClassLoader,java.security.ProtectionDomain)
2026-10-09T17:45:53.9978826Z 	at co.elastic.apm.agent.shaded.bytebuddy.dynamic.loading.ClassInjector$UsingUnsafe$Dispatcher$Unavailable.initialize(ClassInjector.java:2133)
2026-10-09T17:45:53.9979072Z 	at co.elastic.apm.agent.shaded.bytebuddy.dynamic.loading.ClassInjector$UsingUnsafe.injectRaw(ClassInjector.java:1865)
2026-10-09T17:45:53.9979284Z 	at co.elastic.apm.agent.bci.IndyBootstrap.initIndyBootstrap(IndyBootstrap.java:234)
2026-10-09T17:45:53.9979477Z 	at co.elastic.apm.agent.bci.IndyBootstrap.getIndyBootstrapMethod(IndyBootstrap.java:215)
2026-10-09T17:45:53.9979620Z 	... 15 more
2026-10-09T17:45:53.9979660Z 
2026-10-09T17:45:53.9979760Z   .   ____          _            __ _ _
2026-10-09T17:45:53.9979991Z  /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
2026-10-09T17:45:53.9980137Z ( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
2026-10-09T17:45:53.9980244Z  \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
2026-10-09T17:45:53.9980389Z   '  |____| .__|_| |_|_| |_\__, | / / / /
2026-10-09T17:45:53.9980501Z  =========|_|==============|___/=/_/_/_/
2026-10-09T17:45:53.9980550Z 
2026-10-09T17:45:53.9980649Z  :: Spring Boot ::                (v3.4.5)
2026-10-09T17:45:53.9980697Z 
2026-10-09T17:45:53.9981074Z 2026-10-09T14:43:19.938-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] g.c.b.s.AcoesEmLoteMensageriaApplication : Starting AcoesEmLoteMensageriaApplication v1.2.03 using Java 21.0.1 with PID 8 (/deployments/demo-1.2.03.jar started by 185 in /deployments)
2026-10-09T17:45:53.9981573Z 2026-10-09T14:43:19.940-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] g.c.b.s.AcoesEmLoteMensageriaApplication : No active profile set, falling back to 1 default profile: "default"
2026-10-09T17:45:53.9981955Z 2026-10-09T14:43:22.140-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] .s.d.r.c.RepositoryConfigurationDelegate : Bootstrapping Spring Data JPA repositories in DEFAULT mode.
2026-10-09T17:45:53.9982346Z 2026-10-09T14:43:22.159-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] .s.d.r.c.RepositoryConfigurationDelegate : Finished Spring Data repository scanning in 12 ms. Found 0 JPA repository interfaces.
2026-10-09T17:45:53.9982753Z 2026-10-09T14:43:22.542-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] b.g.c.b.s.c.DatasourcePropertiesLogger   : DATASOURCE url=jdbc:db2://10.192.224.76:5021/CSD1
2026-10-09T17:45:53.9983351Z 2026-10-09T14:43:22.543-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] b.g.c.b.s.c.DatasourcePropertiesLogger   : DATASOURCE username=SNAFBD01
2026-10-09T17:45:53.9983899Z 2026-10-09T14:43:22.544-03:00  WARN 8 --- [acoes-em-lote-mensageria] [           main] ConfigServletWebServerApplicationContext : Exception encountered during context initialization - cancelling refresh attempt: org.springframework.util.PlaceholderResolutionException: Could not resolve placeholder 'DATASOURCE_PASSWORD_SNAFPB01' in value "${DATASOURCE_PASSWORD_SNAFPB01}"
2026-10-09T17:45:53.9984304Z 2026-10-09T14:43:22.618-03:00  INFO 8 --- [acoes-em-lote-mensageria] [           main] .s.b.a.l.ConditionEvaluationReportLogger : 
2026-10-09T17:45:53.9984438Z 
2026-10-09T17:45:53.9984672Z Error starting ApplicationContext. To display the condition evaluation report re-run your application with 'debug' enabled.
2026-10-09T17:45:53.9985080Z 2026-10-09T14:43:22.640-03:00 ERROR 8 --- [acoes-em-lote-mensageria] [           main] o.s.boot.SpringApplication               : Application run failed
2026-10-09T17:45:53.9985180Z 
2026-10-09T17:45:53.9985455Z org.springframework.util.PlaceholderResolutionException: Could not resolve placeholder 'DATASOURCE_PASSWORD_SNAFPB01' in value "${DATASOURCE_PASSWORD_SNAFPB01}"
2026-10-09T17:45:53.9985794Z 	at org.springframework.util.PlaceholderResolutionException.withValue(PlaceholderResolutionException.java:81) ~[spring-core-6.2.6.jar!/:6.2.6]
2026-10-09T17:45:53.9986118Z 	at org.springframework.util.PlaceholderParser$ParsedValue.resolve(PlaceholderParser.java:423) ~[spring-core-6.2.6.jar!/:6.2.6]
2026-10-09T17:45:53.9986438Z 	at org.springframework.util.PlaceholderParser.replacePlaceholders(PlaceholderParser.java:128) ~[spring-core-6.2.6.jar!/:6.2.6]
2026-10-09T17:45:53.9986768Z 	at org.springframework.util.PropertyPlaceholderHelper.parseStringValue(PropertyPlaceholderHelper.java:118) ~[spring-core-6.2.6.jar!/:6.2.6]
2026-10-09T17:45:53.9987097Z 	at org.springframework.util.PropertyPlaceholderHelper.replacePlaceholders(PropertyPlaceholderHelper.java:114) ~[spring-core-6.2.6.jar!/:6.2.6]
2026-10-09T17:45:53.9987447Z 	at org.springframework.core.env.AbstractPropertyResolver.doResolvePlaceholders(AbstractPropertyResolver.java:255) ~[spring-core-6.2.6.jar!/:6.2.6]
2026-10-09T17:45:53.9987812Z 	at org.springframework.core.env.AbstractPropertyResolver.resolveRequiredPlaceholders(AbstractPropertyResolver.java:226) ~[spring-core-6.2.6.jar!/:6.2.6]
2026-10-09T17:45:53.9988172Z 	at org.springframework.core.env.AbstractPropertyResolver.resolveNestedPlaceholders(AbstractPropertyResolver.java:246) ~[spring-core-6.2.6.jar!/:6.2.6]
2026-10-09T17:45:53.9988602Z 	at org.springframework.boot.context.properties.source.ConfigurationPropertySourcesPropertyResolver.getProperty(ConfigurationPropertySourcesPropertyResolver.java:81) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-09T17:45:53.9989041Z 	at org.springframework.boot.context.properties.source.ConfigurationPropertySourcesPropertyResolver.getProperty(ConfigurationPropertySourcesPropertyResolver.java:62) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-09T17:45:53.9989401Z 	at org.springframework.core.env.AbstractEnvironment.getProperty(AbstractEnvironment.java:557) ~[spring-core-6.2.6.jar!/:6.2.6]
2026-10-09T17:45:53.9989632Z 	at br.gov.caixa.bsb.sinaf.config.DatasourcePropertiesLogger.postProcessBeanFactory(DatasourcePropertiesLogger.java:32) ~[!/:1.2.03]
2026-10-09T17:45:53.9990018Z 	at org.springframework.context.support.PostProcessorRegistrationDelegate.invokeBeanFactoryPostProcessors(PostProcessorRegistrationDelegate.java:363) ~[spring-context-6.2.6.jar!/:6.2.6]
2026-10-09T17:45:54.0031795Z 	at org.springframework.context.support.PostProcessorRegistrationDelegate.invokeBeanFactoryPostProcessors(PostProcessorRegistrationDelegate.java:204) ~[spring-context-6.2.6.jar!/:6.2.6]
2026-10-09T17:45:54.0032559Z 	at org.springframework.context.support.AbstractApplicationContext.invokeBeanFactoryPostProcessors(AbstractApplicationContext.java:791) ~[spring-context-6.2.6.jar!/:6.2.6]
2026-10-09T17:45:54.0033329Z 	at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:609) ~[spring-context-6.2.6.jar!/:6.2.6]
2026-10-09T17:45:54.0033917Z 	at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.refresh(ServletWebServerApplicationContext.java:146) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-09T17:45:54.0034428Z 	at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:753) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-09T17:45:54.0034914Z 	at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:439) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-09T17:45:54.0035627Z 	at org.springframework.boot.SpringApplication.run(SpringApplication.java:318) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-09T17:45:54.0036111Z 	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1362) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-09T17:45:54.0036573Z 	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1351) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-09T17:45:54.0036961Z 	at br.gov.caixa.bsb.sinaf.AcoesEmLoteMensageriaApplication.main(AcoesEmLoteMensageriaApplication.java:10) ~[!/:1.2.03]
2026-10-09T17:45:54.0037341Z 	at java.base/jdk.internal.reflect.DirectMethodHandleAccessor.invoke(DirectMethodHandleAccessor.java:103) ~[na:na]
2026-10-09T17:45:54.0037692Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:580) ~[na:na]
2026-10-09T17:45:54.0038143Z 	at org.springframework.boot.loader.launch.Launcher.launch(Launcher.java:102) ~[demo-1.2.03.jar:1.2.03]
2026-10-09T17:45:54.0038623Z 	at org.springframework.boot.loader.launch.Launcher.launch(Launcher.java:64) ~[demo-1.2.03.jar:1.2.03]
2026-10-09T17:45:54.0039115Z 	at org.springframework.boot.loader.launch.JarLauncher.main(JarLauncher.java:40) ~[demo-1.2.03.jar:1.2.03]
2026-10-09T17:45:54.0039286Z 
2026-10-09T17:45:54.0053504Z ##[section]Finishing: Logs da Aplicação
