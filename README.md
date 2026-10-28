
Prezados(as),

Solicitamos apoio para analisar e corrigir erro que está impedindo criação de release do SIACG-gde conforme link a seguir: https://devops.caixa/projetos/Caixa/_releaseProgress?_a=release-environment-logs&releaseId=547332&environmentId=2543723

Atenciosamente,

Welinton da Silva Oliveira
Assistente Sênior - CESOA

2026-10-28T14:29:09.8537059Z ##[section]Starting: Verificando Status do Deployment
2026-10-28T14:29:09.8540246Z ==============================================================================
2026-10-28T14:29:09.8540329Z Task         : Bash
2026-10-28T14:29:09.8540379Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-28T14:29:09.8540457Z Version      : 3.227.0
2026-10-28T14:29:09.8540507Z Author       : Microsoft Corporation
2026-10-28T14:29:09.8540565Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-28T14:29:09.8540651Z ==============================================================================
2026-10-28T14:29:09.9849862Z Generating script.
2026-10-28T14:29:09.9863154Z ========================== Starting Command Output ===========================
2026-10-28T14:29:09.9870362Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/b754f29d-d367-42e0-b1ea-1955fe816f26.sh
2026-10-28T14:29:10.0753523Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-28T14:29:12.0093007Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-28T14:29:12.0711919Z Waiting for rollout to finish: 1 old replicas are pending termination...
2026-10-28T14:30:46.8861170Z ##[error]The Operation will be canceled. The next steps may not contain expected logs.
2026-10-28T14:30:54.4049686Z ##[error]The operation was canceled.
2026-10-28T14:30:54.4052492Z ##[section]Finishing: Verificando Status do Deployment


2026-10-28T14:30:54.4074149Z ##[section]Starting: Logs da Aplicação
2026-10-28T14:30:54.4077191Z ==============================================================================
2026-10-28T14:30:54.4077272Z Task         : Bash
2026-10-28T14:30:54.4077316Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-28T14:30:54.4077392Z Version      : 3.227.0
2026-10-28T14:30:54.4077436Z Author       : Microsoft Corporation
2026-10-28T14:30:54.4077489Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-28T14:30:54.4077587Z ==============================================================================
2026-10-28T14:30:54.5411870Z Generating script.
2026-10-28T14:30:54.5414124Z ========================== Starting Command Output ===========================
2026-10-28T14:30:54.5421081Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/f3eddf00-323b-4fb7-8f82-c28de80bb486.sh
2026-10-28T14:30:54.5477671Z + shopt -s expand_aliases
2026-10-28T14:30:54.5477877Z + [[ -n okd4_nprd ]]
2026-10-28T14:30:54.5478045Z + [[ okd4_nprd =~ ocp ]]
2026-10-28T14:30:54.5478188Z + [[ -n okd4_nprd ]]
2026-10-28T14:30:54.5478307Z + [[ okd4_nprd =~ (okd4|openshift) ]]
2026-10-28T14:30:54.5478456Z + app=siacg-gde-tqs
2026-10-28T14:30:54.5478566Z + oc version
2026-10-28T14:30:54.6206299Z Client Version: v4.2.0-alpha.0-1394-g45460a5
2026-10-28T14:30:54.6206592Z Server Version: 4.12.0-0.okd-2023-04-16-041331
2026-10-28T14:30:54.6206809Z Kubernetes Version: v1.25.0-2824+27e744f55d2e99-dirty
2026-10-28T14:30:54.6236304Z ++ oc get pod -l name=siacg-gde-tqs -n siacg-tqs -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-10-28T14:30:54.6237587Z ++ tac
2026-10-28T14:30:54.6237734Z ++ grep -v '^$'
2026-10-28T14:30:54.6239438Z ++ head -n1
2026-10-28T14:30:54.7051256Z + last_pod=siacg-gde-tqs-60-9zgh2
2026-10-28T14:30:54.7051498Z + echo 'Logs do POD: siacg-gde-tqs-60-9zgh2'
2026-10-28T14:30:54.7051703Z + oc logs siacg-gde-tqs-60-9zgh2 -c siacg-gde-tqs -n siacg-tqs
2026-10-28T14:30:54.7051901Z Logs do POD: siacg-gde-tqs-60-9zgh2
2026-10-28T14:30:54.7848574Z exec java -Dquarkus.http.host=0.0.0.0 -Dquarkus.http.port=8080 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Dfile.encoding=UTF-8 -Xms3072m -Xmx3072m -Djavax.net.ssl.trustStore=/deployments/caixa-truststore-acteste-nprd.jks -Dhttps.proxyHost=proxydes.caixa -Dhttps.proxyPort=80 -Dhttp.proxyHost=proxydes.caixa -Dhttp.proxyPort=80 -Dhttp.nonProxyHosts=*.caixa|*.corecaixa|*.extranet.caixa|*.svc -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/quarkus-run.jar
2026-10-28T14:30:54.7849062Z Oct 28, 2026 11:30:15 AM io.quarkus.config
2026-10-28T14:30:54.7849263Z WARN: Unrecognized configuration key "%s" was provided; it will be ignored; verify that the dependency extension for this configuration is set or that you did not make a typo
2026-10-28T14:30:54.7849484Z Oct 28, 2026 11:30:16 AM org.hibernate.Version
2026-10-28T14:30:54.7849632Z INFO: HHH000412: Hibernate ORM core version %s
2026-10-28T14:30:54.7849766Z Oct 28, 2026 11:30:16 AM org.hibernate.cfg.Environment
2026-10-28T14:30:54.7849926Z INFO: HHH000406: Using bytecode reflection optimizer
2026-10-28T14:30:54.7850083Z Oct 28, 2026 11:30:17 AM org.hibernate.validator.internal.util.Version
2026-10-28T14:30:54.7850228Z INFO: HV000001: Hibernate Validator %s
2026-10-28T14:30:54.7850507Z LogManager error of type WRITE_FAILURE: The delayed handler's queue was overrun and log record(s) were lost (Did you forget to configure logging?): 
2026-10-28T14:30:54.7851057Z 	 - io.netty.channel.DefaultChannelId: [DEBUG]
2026-10-28T14:30:54.7851249Z 	 - io.netty.util.internal.CleanerJava9: [DEBUG]
2026-10-28T14:30:54.7851441Z 	 - io.netty.util.internal.InternalThreadLocalMap: [DEBUG]
2026-10-28T14:30:54.7851682Z 	 - io.netty.util.internal.PlatformDependent: [DEBUG]
2026-10-28T14:30:54.7851874Z 	 - io.netty.util.internal.PlatformDependent0: [DEBUG]
2026-10-28T14:30:54.7852077Z 	 - io.netty.util.internal.logging.InternalLoggerFactory: [DEBUG]
2026-10-28T14:30:54.7852253Z 	 - io.quarkus.arc.impl: [DEBUG]
2026-10-28T14:30:54.7852671Z 	 - io.quarkus.arc.runtime.ArcRecorder: [DEBUG]
2026-10-28T14:30:54.7852919Z 	 - io.quarkus.arc.runtime.BeanContainerImpl: [DEBUG]
2026-10-28T14:30:54.7853096Z 	 - io.quarkus.hibernate.orm: [DEBUG]
2026-10-28T14:30:54.7853376Z 	 - org.hibernate.boot.internal.BootstrapContextImpl: [DEBUG]
2026-10-28T14:30:54.7853591Z 	 - org.hibernate.boot.internal.ClassLoaderAccessImpl: [DEBUG]
2026-10-28T14:30:54.7853809Z 	 - org.hibernate.boot.internal.InFlightMetadataCollectorImpl: [DEBUG]
2026-10-28T14:30:54.7854090Z 	 - org.hibernate.boot.model.convert.internal.AttributeConverterManager: [DEBUG]
2026-10-28T14:30:54.7854310Z 	 - org.hibernate.boot.model.internal.AbstractPropertyHolder: [DEBUG]
2026-10-28T14:30:54.7854517Z 	 - org.hibernate.boot.model.internal.AnnotatedColumn: [DEBUG]
2026-10-28T14:30:54.7854711Z 	 - org.hibernate.boot.model.internal.BasicValueBinder: [DEBUG]
2026-10-28T14:30:54.7854912Z 	 - org.hibernate.boot.model.internal.BinderHelper: [DEBUG]
2026-10-28T14:30:54.7855107Z 	 - org.hibernate.boot.model.internal.CollectionBinder: [DEBUG]
2026-10-28T14:30:54.7855309Z 	 - org.hibernate.boot.model.internal.CollectionSecondPass: [DEBUG]
2026-10-28T14:30:54.7855509Z 	 - org.hibernate.boot.model.internal.EntityBinder: [DEBUG]
2026-10-28T14:30:54.7855702Z 	 - org.hibernate.boot.model.internal.PropertyBinder: [DEBUG]
2026-10-28T14:30:54.7855899Z 	 - org.hibernate.boot.model.internal.TableBinder: [DEBUG]
2026-10-28T14:30:54.7856094Z 	 - org.hibernate.boot.model.relational.Namespace: [DEBUG]
2026-10-28T14:30:54.7856343Z 	 - org.hibernate.boot.model.source.internal.annotations.AnnotationMetadataSourceProcessorImpl: [DEBUG]
2026-10-28T14:30:54.7856591Z 	 - org.hibernate.boot.registry.internal.BootstrapServiceRegistryImpl: [DEBUG]
2026-10-28T14:30:54.7856783Z 	 - org.hibernate.cfg.Environment: [DEBUG]
2026-10-28T14:30:54.7856968Z 	 - org.hibernate.jpa.internal.util.LogHelper: [DEBUG]
2026-10-28T14:30:54.7857148Z 	 - org.hibernate.mapping.BasicValue: [DEBUG]
2026-10-28T14:30:54.7857331Z 	 - org.hibernate.mapping.PrimaryKey: [DEBUG]
2026-10-28T14:30:54.7857497Z 	 - org.hibernate.orm.dialect: [DEBUG]
2026-10-28T14:30:54.7857676Z 	 - org.hibernate.orm.idgen.factory: [DEBUG]
2026-10-28T14:30:54.7857843Z 	 - org.hibernate.orm.jdbc.lob: [DEBUG]
2026-10-28T14:30:54.7858110Z 	 - org.hibernate.quarkus.feature: [DEBUG]
2026-10-28T14:30:54.7858334Z 	 - org.hibernate.resource.beans.container.internal.ContainerManagedLifecycleStrategy: [DEBUG]
2026-10-28T14:30:54.7858542Z 	 - org.hibernate.type.BasicTypeRegistry: [DEBUG]
2026-10-28T14:30:54.7858745Z 	 - org.hibernate.type.descriptor.jdbc.spi.JdbcTypeRegistry: [DEBUG]
2026-10-28T14:30:54.7858948Z 	 - org.hibernate.type.spi.TypeConfiguration$Scope: [DEBUG]
2026-10-28T14:30:54.7859222Z 	 - org.hibernate.validator.internal.engine.AbstractConfigurationImpl: [DEBUG]
2026-10-28T14:30:54.7859505Z 	 - org.hibernate.validator.internal.engine.ValidatorFactoryConfigurationHelper: [DEBUG]
2026-10-28T14:30:54.7859754Z 	 - org.hibernate.validator.messageinterpolation.ResourceBundleMessageInterpolator: [DEBUG]
2026-10-28T14:30:54.7859999Z 	 - org.hibernate.validator.resourceloading.PlatformResourceBundleLocator: [DEBUG]
2026-10-28T14:30:54.7860232Z 	 - org.infinispan.quarkus.hibernate.cache.QuarkusInfinispanRegionFactory: [DEBUG]
2026-10-28T14:30:54.7860411Z 	 - org.jboss.logging: [DEBUG]
2026-10-28T14:30:54.7860463Z 
2026-10-28T14:30:54.7860616Z Oct 28, 2026 11:30:18 AM org.hibernate.resource.beans.container.spi.AbstractCdiBeanContainer stop
2026-10-28T14:30:54.7860846Z INFO: HHH10005004: Stopping BeanContainer : %s
2026-10-28T14:30:54.7861000Z Oct 28, 2026 11:30:18 AM io.quarkus.runtime.ApplicationLifecycleManager run
2026-10-28T14:30:54.7861165Z ERROR: Failed to start application (with profile [prod])
2026-10-28T14:30:54.7861305Z java.lang.RuntimeException: Failed to start quarkus
2026-10-28T14:30:54.7861456Z 	at io.quarkus.runner.ApplicationImpl.doStart(Unknown Source)
2026-10-28T14:30:54.7861617Z 	at io.quarkus.runtime.Application.start(Application.java:101)
2026-10-28T14:30:54.7861887Z 	at io.quarkus.runtime.ApplicationLifecycleManager.run(ApplicationLifecycleManager.java:111)
2026-10-28T14:30:54.7862064Z 	at io.quarkus.runtime.Quarkus.run(Quarkus.java:71)
2026-10-28T14:30:54.7862223Z 	at io.quarkus.runtime.Quarkus.run(Quarkus.java:44)
2026-10-28T14:30:54.7862377Z 	at io.quarkus.runtime.Quarkus.run(Quarkus.java:124)
2026-10-28T14:30:54.7862529Z 	at io.quarkus.runner.GeneratedMain.main(Unknown Source)
2026-10-28T14:30:54.7862829Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-10-28T14:30:54.7863039Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-10-28T14:30:54.7863337Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-10-28T14:30:54.7863563Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-10-28T14:30:54.7863753Z 	at io.quarkus.bootstrap.runner.QuarkusEntryPoint.doRun(QuarkusEntryPoint.java:61)
2026-10-28T14:30:54.7863945Z 	at io.quarkus.bootstrap.runner.QuarkusEntryPoint.main(QuarkusEntryPoint.java:32)
2026-10-28T14:30:54.7864136Z Caused by: io.smallrye.config.ConfigValidationException: Configuration validation failed:
2026-10-28T14:30:54.7864343Z 	java.util.NoSuchElementException: SRCFG00011: Could not expand value JANELA_ENVIO_HORA_FINAL in property gde.janela.envio.hora-fim
2026-10-28T14:30:54.7864661Z 	java.util.NoSuchElementException: SRCFG00011: Could not expand value JANELA_ENVIO_HORA_INICIAL in property gde.janela.envio.hora-inicio
2026-10-28T14:30:54.7864897Z 	at io.smallrye.config.ConfigMappingProvider.mapConfigurationInternal(ConfigMappingProvider.java:1001)
2026-10-28T14:30:54.7865126Z 	at io.smallrye.config.ConfigMappingProvider.lambda$mapConfiguration$3(ConfigMappingProvider.java:957)
2026-10-28T14:30:54.7865323Z 	at io.smallrye.config.SecretKeys.doUnlocked(SecretKeys.java:28)
2026-10-28T14:30:54.7865513Z 	at io.smallrye.config.ConfigMappingProvider.mapConfiguration(ConfigMappingProvider.java:957)
2026-10-28T14:30:54.7865722Z 	at io.smallrye.config.ConfigMappings.mapConfiguration(ConfigMappings.java:91)
2026-10-28T14:30:54.7865913Z 	at io.smallrye.config.SmallRyeConfigBuilder.build(SmallRyeConfigBuilder.java:630)
2026-10-28T14:30:54.7866091Z 	at io.quarkus.runtime.generated.Config.readConfig(Unknown Source)
2026-10-28T14:30:54.7866257Z 	at io.quarkus.deployment.steps.RuntimeConfigSetup.deploy(Unknown Source)
2026-10-28T14:30:54.7866386Z 	... 13 more
2026-10-28T14:30:54.7866431Z 
2026-10-28T14:30:54.7926637Z ##[section]Finishing: Logs da Aplicação






rodaram outra e passou


2026-10-28T14:31:39.4349785Z ##[section]Starting: Verificando Status do Deployment
2026-10-28T14:31:39.4353236Z ==============================================================================
2026-10-28T14:31:39.4353321Z Task         : Bash
2026-10-28T14:31:39.4353371Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-28T14:31:39.4353450Z Version      : 3.227.0
2026-10-28T14:31:39.4353498Z Author       : Microsoft Corporation
2026-10-28T14:31:39.4353555Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-28T14:31:39.4353646Z ==============================================================================
2026-10-28T14:31:39.5647059Z Generating script.
2026-10-28T14:31:39.5660393Z ========================== Starting Command Output ===========================
2026-10-28T14:31:39.5670256Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/6162681e-1c1c-4199-bc70-da8871b2920f.sh
2026-10-28T14:31:39.6555157Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-28T14:31:41.8129867Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-28T14:31:41.8843330Z Waiting for rollout to finish: 1 old replicas are pending termination...
2026-10-28T14:32:02.5858178Z Waiting for rollout to finish: 1 old replicas are pending termination...
2026-10-28T14:32:03.1364273Z Waiting for latest deployment config spec to be observed by the controller loop...
2026-10-28T14:32:07.9478465Z replication controller "siacg-gde-tqs-61" successfully rolled out
2026-10-28T14:32:07.9571775Z ##[section]Finishing: Verificando Status do Deployment


2026-10-28T14:32:07.9596046Z ##[section]Starting: Logs da Aplicação
2026-10-28T14:32:07.9599337Z ==============================================================================
2026-10-28T14:32:07.9599427Z Task         : Bash
2026-10-28T14:32:07.9599503Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-28T14:32:07.9599567Z Version      : 3.227.0
2026-10-28T14:32:07.9599644Z Author       : Microsoft Corporation
2026-10-28T14:32:07.9599698Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-28T14:32:07.9599773Z ==============================================================================
2026-10-28T14:32:08.1056880Z Generating script.
2026-10-28T14:32:08.1068410Z ========================== Starting Command Output ===========================
2026-10-28T14:32:08.1075404Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/f4ce0bd2-ca19-40f1-8e1a-f97898d933bd.sh
2026-10-28T14:32:08.1131563Z + shopt -s expand_aliases
2026-10-28T14:32:08.1131787Z + [[ -n okd4_nprd ]]
2026-10-28T14:32:08.1132012Z + [[ okd4_nprd =~ ocp ]]
2026-10-28T14:32:08.1132157Z + [[ -n okd4_nprd ]]
2026-10-28T14:32:08.1132474Z + [[ okd4_nprd =~ (okd4|openshift) ]]
2026-10-28T14:32:08.1134972Z + app=siacg-gde-tqs
2026-10-28T14:32:08.1135170Z + oc version
2026-10-28T14:32:08.1820323Z Client Version: v4.2.0-alpha.0-1394-g45460a5
2026-10-28T14:32:08.1820677Z Server Version: 4.12.0-0.okd-2023-04-16-041331
2026-10-28T14:32:08.1820908Z Kubernetes Version: v1.25.0-2824+27e744f55d2e99-dirty
2026-10-28T14:32:08.1859700Z ++ oc get pod -l name=siacg-gde-tqs -n siacg-tqs -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-10-28T14:32:08.1860115Z ++ tac
2026-10-28T14:32:08.1861954Z ++ grep -v '^$'
2026-10-28T14:32:08.1862175Z ++ head -n1
2026-10-28T14:32:08.2812960Z + last_pod=siacg-gde-tqs-61-p4sj8
2026-10-28T14:32:08.2813287Z + echo 'Logs do POD: siacg-gde-tqs-61-p4sj8'
2026-10-28T14:32:08.2813517Z + oc logs siacg-gde-tqs-61-p4sj8 -c siacg-gde-tqs -n siacg-tqs
2026-10-28T14:32:08.2813745Z Logs do POD: siacg-gde-tqs-61-p4sj8
2026-10-28T14:32:08.3620259Z exec java -Dquarkus.http.host=0.0.0.0 -Dquarkus.http.port=8080 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Dfile.encoding=UTF-8 -Xms3072m -Xmx3072m -Djavax.net.ssl.trustStore=/deployments/caixa-truststore-acteste-nprd.jks -Dhttps.proxyHost=proxydes.caixa -Dhttps.proxyPort=80 -Dhttp.proxyHost=proxydes.caixa -Dhttp.proxyPort=80 -Dhttp.nonProxyHosts=*.caixa|*.corecaixa|*.extranet.caixa|*.svc -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/quarkus-run.jar
2026-10-28T14:32:08.3620780Z __  ____  __  _____   ___  __ ____  ______ 
2026-10-28T14:32:08.3620983Z  --/ __ \/ / / / _ | / _ \/ //_/ / / / __/ 
2026-10-28T14:32:08.3621167Z  -/ /_/ / /_/ / __ |/ , _/ ,< / /_/ /\ \   
2026-10-28T14:32:08.3621352Z --\___\_\____/_/ |_/_/|_/_/|_|\____/___/   
2026-10-28T14:32:08.3621764Z 2026-10-28 11:31:45,224 WARN  [io.qua.config] (main) Unrecognized configuration key "quarkus.smallrye-openapi.store-schema-file-name" was provided; it will be ignored; verify that the dependency extension for this configuration is set or that you did not make a typo
2026-10-28T14:32:08.3622224Z 2026-10-28 11:31:50,827 INFO  [br.gov.cai.sia.aut.aut.PermissionRepositoryXlsImpl] (main) Carregando MAP: baseDir='/SIACG/login-module/DES', sigla='SIACG', nome='MAP.xlsx', aba='MAP'
2026-10-28T14:32:08.3623060Z 2026-10-28 11:31:50,836 INFO  [br.gov.cai.sia.aut.aut.MatrizAcesssoXlsImpl] (main) SIACG-autorizacao -> MAP com dados para importação: [/SIACG/login-module/DES/SIACG/MAP.xlsx]
2026-10-28T14:32:08.3623441Z 2026-10-28 11:31:51,015 INFO  [br.gov.cai.sia.gde.cor.age.AgendadorConsultaSolicitacoes] (executor-thread-1) Consulta de solicitações desabilitada.
2026-10-28T14:32:08.3623798Z 2026-10-28 11:31:52,929 INFO  [br.gov.cai.sia.aut.aut.MatrizAcesssoXlsImpl] (main) SIACG-Security -> Dados importados da MAP Qtde linhas: [2,586]
2026-10-28T14:32:08.3624099Z 2026-10-28 11:31:53,007 INFO  [br.gov.cai.sia.aut.aut.PermissionRepositoryXlsImpl] (main) MAP carregado. Perfis encontrados: 28
2026-10-28T14:32:08.3624594Z 2026-10-28 11:31:53,010 INFO  [br.gov.cai.sia.aut.aut.AutorizacaoStartup] (main) Matriz de permissões carregada com sucesso (startup).
2026-10-28T14:32:08.3624992Z 2026-10-28 11:31:53,712 INFO  [io.quarkus] (main) siacg-gde 1.0.0.0 on JVM (powered by Quarkus 3.2.0.Final) started in 9.261s. Listening on: http://0.0.0.0:8080
2026-10-28T14:32:08.3625290Z 2026-10-28 11:31:53,712 INFO  [io.quarkus] (main) Profile prod activated. 
2026-10-28T14:32:08.3625866Z 2026-10-28 11:31:53,713 INFO  [io.quarkus] (main) Installed features: [agroal, cdi, hibernate-orm, hibernate-orm-panache, hibernate-validator, jdbc-oracle, micrometer, narayana-jta, oidc, reactive-routes, rest-client-reactive, rest-client-reactive-jackson, resteasy-reactive, resteasy-reactive-jackson, scheduler, security, smallrye-context-propagation, smallrye-jwt, smallrye-openapi, swagger-ui, vertx]
2026-10-28T14:32:08.3704542Z ##[section]Finishing: Logs da Aplicação






<img width="1787" height="907" alt="image" src="https://github.com/user-attachments/assets/d0bd95ef-ebae-4c10-b084-4ddf4c0c1d1f" />



me ajdua com texto para fechar a demanda

