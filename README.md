2026-10-28T13:17:07.1862050Z ##[section]Starting: Verificando Status do Deployment
2026-10-28T13:17:07.1865621Z ==============================================================================
2026-10-28T13:17:07.1865712Z Task         : Bash
2026-10-28T13:17:07.1865755Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-28T13:17:07.1865816Z Version      : 3.227.0
2026-10-28T13:17:07.1865868Z Author       : Microsoft Corporation
2026-10-28T13:17:07.1865917Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-28T13:17:07.1865984Z ==============================================================================
2026-10-28T13:17:07.3288766Z Generating script.
2026-10-28T13:17:07.3299405Z ========================== Starting Command Output ===========================
2026-10-28T13:17:07.3309820Z [command]/bin/bash /opt/ads-agent/_work/_temp/7a63f2c2-ef51-421f-8335-f41904b7006a.sh
2026-10-28T13:17:07.5880853Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-28T13:17:07.6689712Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-10-28T13:17:07.7431563Z Waiting for rollout to finish: 0 of 1 updated replicas are available...
2026-10-28T13:23:14.6977639Z ##[error]The task has timed out.
2026-10-28T13:23:14.6978712Z ##[section]Finishing: Verificando Status do Deployment


2026-10-28T13:23:14.6999521Z ##[section]Starting: Logs da Aplicação
2026-10-28T13:23:14.7004330Z ==============================================================================
2026-10-28T13:23:14.7004413Z Task         : Bash
2026-10-28T13:23:14.7004467Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-10-28T13:23:14.7004527Z Version      : 3.227.0
2026-10-28T13:23:14.7004569Z Author       : Microsoft Corporation
2026-10-28T13:23:14.7004625Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-10-28T13:23:14.7004693Z ==============================================================================
2026-10-28T13:23:14.8258442Z Generating script.
2026-10-28T13:23:14.8269324Z ========================== Starting Command Output ===========================
2026-10-28T13:23:14.8277366Z [command]/bin/bash /opt/ads-agent/_work/_temp/fbd0d4f4-b3e1-483f-b4b8-8caa4733251c.sh
2026-10-28T13:23:14.8328482Z + shopt -s expand_aliases
2026-10-28T13:23:14.8328744Z + [[ -n okd4_nprd ]]
2026-10-28T13:23:14.8328956Z + [[ okd4_nprd =~ ocp ]]
2026-10-28T13:23:14.8329765Z + [[ -n okd4_nprd ]]
2026-10-28T13:23:14.8329945Z + [[ okd4_nprd =~ (okd4|openshift) ]]
2026-10-28T13:23:14.8330193Z + app=sisib-arquivos-de-quebra-des
2026-10-28T13:23:14.8330354Z + oc version
2026-10-28T13:23:14.9998581Z oc v3.11.0+0cbc58b
2026-10-28T13:23:14.9999298Z kubernetes v1.11.0+d4cacc0
2026-10-28T13:23:14.9999668Z features: Basic-Auth GSSAPI Kerberos SPNEGO
2026-10-28T13:23:15.0108628Z 
2026-10-28T13:23:15.0109726Z Server https://api.nprd.caixa:6443
2026-10-28T13:23:15.0110323Z kubernetes v1.25.0-2824+27e744f55d2e99-dirty
2026-10-28T13:23:15.0158183Z ++ oc get pod -l name=sisib-arquivos-de-quebra-des -n sisib-des -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-10-28T13:23:15.0158462Z ++ tac
2026-10-28T13:23:15.0158605Z ++ grep -v '^$'
2026-10-28T13:23:15.0159120Z ++ head -n1
2026-10-28T13:23:16.3249691Z + last_pod=sisib-arquivos-de-quebra-des-5-77mj2
2026-10-28T13:23:16.3249985Z + echo 'Logs do POD: sisib-arquivos-de-quebra-des-5-77mj2'
2026-10-28T13:23:16.3250509Z + oc logs sisib-arquivos-de-quebra-des-5-77mj2 -c sisib-arquivos-de-quebra-des -n sisib-des
2026-10-28T13:23:16.3250806Z Logs do POD: sisib-arquivos-de-quebra-des-5-77mj2
2026-10-28T13:23:16.7785346Z exec java -Dserver.address=0.0.0.0 -Dserver.port=8080 -javaagent:/opt/apm_agent/elastic-apm-agent.jar -Delastic.apm.config_file=/opt/apm_agent/elasticapm.properties -Delastic.apm.service_name=sisib-arquivos-de-quebra -Delastic.apm.environment=des -Delastic.apm.application_packages=br.gov.caixa -Delastic.apm.server_urls=http://apm-server-devops.produtos.caixa -Delastic.apm.global_labels=deployment=sisib-arquivos-de-quebra -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/sisib-arquivos-de-quebra-1.0.0-SNAPSHOT.jar
2026-10-28T13:23:16.7786208Z OpenJDK 64-Bit Server VM warning: Sharing is only supported for boot loader classes because bootstrap classpath has been appended
2026-10-28T13:23:16.7786410Z WARNING: sun.reflect.Reflection.getCallerClass is not supported. This will impact performance.
2026-10-28T13:23:16.7786498Z 
2026-10-28T13:23:16.7786597Z   .   ____          _            __ _ _
2026-10-28T13:23:16.7786756Z  /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
2026-10-28T13:23:16.7786900Z ( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
2026-10-28T13:23:16.7787009Z  \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
2026-10-28T13:23:16.7787159Z   '  |____| .__|_| |_|_| |_\__, | / / / /
2026-10-28T13:23:16.7787272Z  =========|_|==============|___/=/_/_/_/
2026-10-28T13:23:16.7787319Z 
2026-10-28T13:23:16.7787433Z  :: Spring Boot ::                (v3.4.5)
2026-10-28T13:23:16.7787480Z 
2026-10-28T13:23:16.7787899Z 2026-10-28T10:21:11.993-03:00  INFO 8 --- [sisib-arquivos-de-quebra] [           main] b.c.c.s.a.ArquivoQuebraApplication       : Starting ArquivoQuebraApplication v1.0.0-SNAPSHOT using Java 17.0.7 with PID 8 (/deployments/sisib-arquivos-de-quebra-1.0.0-SNAPSHOT.jar started by 1001 in /deployments)
2026-10-28T13:23:16.7789267Z 2026-10-28T10:21:11.997-03:00  INFO 8 --- [sisib-arquivos-de-quebra] [           main] b.c.c.s.a.ArquivoQuebraApplication       : No active profile set, falling back to 1 default profile: "default"
2026-10-28T13:23:16.7790135Z 2026-10-28T10:21:13.497-03:00  INFO 8 --- [sisib-arquivos-de-quebra] [           main] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Starting...
2026-10-28T13:23:16.7790627Z 2026-10-28T10:21:13.921-03:00  INFO 8 --- [sisib-arquivos-de-quebra] [           main] com.zaxxer.hikari.pool.HikariPool        : HikariPool-1 - Added connection conn0: url=jdbc:h2:mem:batchdb user=SA
2026-10-28T13:23:16.7791000Z 2026-10-28T10:21:13.923-03:00  INFO 8 --- [sisib-arquivos-de-quebra] [           main] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Start completed.
2026-10-28T13:23:16.7791381Z 2026-10-28T10:21:14.705-03:00  INFO 8 --- [sisib-arquivos-de-quebra] [           main] b.c.c.s.a.ArquivoQuebraApplication       : Started ArquivoQuebraApplication in 3.686 seconds (process running for 6.286)
2026-10-28T13:23:16.7791742Z 2026-10-28T10:21:14.709-03:00  INFO 8 --- [sisib-arquivos-de-quebra] [           main] o.s.b.a.b.JobLauncherApplicationRunner   : Running default command line with: []
2026-10-28T13:23:16.7792235Z 2026-10-28T10:21:14.923-03:00  INFO 8 --- [sisib-arquivos-de-quebra] [           main] o.s.b.c.l.s.TaskExecutorJobLauncher      : Job: [SimpleJob: [name=validarArquivoJob]] launched with the following parameters: [{'run.id':'{value=1, type=class java.lang.Long, identifying=true}'}]
2026-10-28T13:23:16.7792780Z 2026-10-28T10:21:14.993-03:00  INFO 8 --- [sisib-arquivos-de-quebra] [           main] o.s.batch.core.job.SimpleStepHandler     : Executing step: [validarArquivoStep]
2026-10-28T13:23:16.7793159Z 2026-10-28T10:21:15.025-03:00 ERROR 8 --- [sisib-arquivos-de-quebra] [           main] o.s.batch.core.step.AbstractStep         : Encountered an error executing step validarArquivoStep in job validarArquivoJob
2026-10-28T13:23:16.7793288Z 
2026-10-28T13:23:16.7793482Z br.com.caixa.sisib.arquivosquebra.ValidadorArquivoTxt$ArquivoInvalidoException: PARAMETRO_OBRIGATORIO | linha 0 | Informe o parametro arquivo
2026-10-28T13:23:16.7793962Z 	at br.com.caixa.sisib.arquivosquebra.ValidacaoTxtJobConfig.lambda$validarArquivoTasklet$0(ValidacaoTxtJobConfig.java:30) ~[!/:1.0.0-SNAPSHOT]
2026-10-28T13:23:16.7794199Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[na:na]
2026-10-28T13:23:16.7794405Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77) ~[na:na]
2026-10-28T13:23:16.7794627Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[na:na]
2026-10-28T13:23:16.7794826Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568) ~[na:na]
2026-10-28T13:23:16.7795113Z 	at org.springframework.aop.support.AopUtils.invokeJoinpointUsingReflection(AopUtils.java:359) ~[spring-aop-6.2.6.jar!/:6.2.6]
2026-10-28T13:23:16.7795460Z 	at org.springframework.aop.framework.ReflectiveMethodInvocation.invokeJoinpoint(ReflectiveMethodInvocation.java:196) ~[spring-aop-6.2.6.jar!/:6.2.6]
2026-10-28T13:23:16.7795820Z 	at org.springframework.aop.framework.ReflectiveMethodInvocation.proceed(ReflectiveMethodInvocation.java:163) ~[spring-aop-6.2.6.jar!/:6.2.6]
2026-10-28T13:23:16.7796179Z 	at org.springframework.aop.support.DelegatingIntroductionInterceptor.doProceed(DelegatingIntroductionInterceptor.java:137) ~[spring-aop-6.2.6.jar!/:6.2.6]
2026-10-28T13:23:16.7796541Z 	at org.springframework.aop.support.DelegatingIntroductionInterceptor.invoke(DelegatingIntroductionInterceptor.java:124) ~[spring-aop-6.2.6.jar!/:6.2.6]
2026-10-28T13:23:16.7796870Z 	at org.springframework.aop.framework.ReflectiveMethodInvocation.proceed(ReflectiveMethodInvocation.java:184) ~[spring-aop-6.2.6.jar!/:6.2.6]
2026-10-28T13:23:16.7797285Z 	at org.springframework.aop.framework.JdkDynamicAopProxy.invoke(JdkDynamicAopProxy.java:223) ~[spring-aop-6.2.6.jar!/:6.2.6]
2026-10-28T13:23:16.7797477Z 	at jdk.proxy2/jdk.proxy2.$Proxy70.execute(Unknown Source) ~[na:na]
2026-10-28T13:23:16.7797916Z 	at org.springframework.batch.core.step.tasklet.TaskletStep$ChunkTransactionCallback.doInTransaction(TaskletStep.java:383) ~[spring-batch-core-5.2.2.jar!/:5.2.2]
2026-10-28T13:23:16.7798303Z 	at org.springframework.batch.core.step.tasklet.TaskletStep$ChunkTransactionCallback.doInTransaction(TaskletStep.java:307) ~[spring-batch-core-5.2.2.jar!/:5.2.2]
2026-10-28T13:23:16.7798641Z 	at org.springframework.transaction.support.TransactionTemplate.execute(TransactionTemplate.java:140) ~[spring-tx-6.2.6.jar!/:6.2.6]
2026-10-28T13:23:16.7799093Z 	at org.springframework.batch.core.step.tasklet.TaskletStep$2.doInChunkContext(TaskletStep.java:250) ~[spring-batch-core-5.2.2.jar!/:5.2.2]
2026-10-28T13:23:16.7799506Z 	at org.springframework.batch.core.scope.context.StepContextRepeatCallback.doInIteration(StepContextRepeatCallback.java:82) ~[spring-batch-core-5.2.2.jar!/:5.2.2]
2026-10-28T13:23:16.7799862Z 	at org.springframework.batch.repeat.support.RepeatTemplate.getNextResult(RepeatTemplate.java:369) ~[spring-batch-infrastructure-5.2.2.jar!/:5.2.2]
2026-10-28T13:23:16.7800217Z 	at org.springframework.batch.repeat.support.RepeatTemplate.executeInternal(RepeatTemplate.java:206) ~[spring-batch-infrastructure-5.2.2.jar!/:5.2.2]
2026-10-28T13:23:16.7800614Z 	at org.springframework.batch.repeat.support.RepeatTemplate.iterate(RepeatTemplate.java:140) ~[spring-batch-infrastructure-5.2.2.jar!/:5.2.2]
2026-10-28T13:23:16.7800934Z 	at org.springframework.batch.core.step.tasklet.TaskletStep.doExecute(TaskletStep.java:235) ~[spring-batch-core-5.2.2.jar!/:5.2.2]
2026-10-28T13:23:16.7801247Z 	at org.springframework.batch.core.step.AbstractStep.execute(AbstractStep.java:230) ~[spring-batch-core-5.2.2.jar!/:5.2.2]
2026-10-28T13:23:16.7801569Z 	at org.springframework.batch.core.job.SimpleStepHandler.handleStep(SimpleStepHandler.java:153) ~[spring-batch-core-5.2.2.jar!/:5.2.2]
2026-10-28T13:23:16.7801878Z 	at org.springframework.batch.core.job.AbstractJob.handleStep(AbstractJob.java:408) ~[spring-batch-core-5.2.2.jar!/:5.2.2]
2026-10-28T13:23:16.7802176Z 	at org.springframework.batch.core.job.SimpleJob.doExecute(SimpleJob.java:127) ~[spring-batch-core-5.2.2.jar!/:5.2.2]
2026-10-28T13:23:16.7802592Z 	at org.springframework.batch.core.job.AbstractJob.execute(AbstractJob.java:307) ~[spring-batch-core-5.2.2.jar!/:5.2.2]
2026-10-28T13:23:16.7802941Z 	at org.springframework.batch.core.launch.support.TaskExecutorJobLauncher$1.run(TaskExecutorJobLauncher.java:155) ~[spring-batch-core-5.2.2.jar!/:5.2.2]
2026-10-28T13:23:16.7803259Z 	at org.springframework.core.task.SyncTaskExecutor.execute(SyncTaskExecutor.java:50) ~[spring-core-6.2.6.jar!/:6.2.6]
2026-10-28T13:23:16.7803595Z 	at org.springframework.batch.core.launch.support.TaskExecutorJobLauncher.run(TaskExecutorJobLauncher.java:146) ~[spring-batch-core-5.2.2.jar!/:5.2.2]
2026-10-28T13:23:16.7803969Z 	at org.springframework.boot.autoconfigure.batch.JobLauncherApplicationRunner.execute(JobLauncherApplicationRunner.java:210) ~[spring-boot-autoconfigure-3.4.5.jar!/:3.4.5]
2026-10-28T13:23:16.7804352Z 	at org.springframework.boot.autoconfigure.batch.JobLauncherApplicationRunner.executeLocalJobs(JobLauncherApplicationRunner.java:194) ~[spring-boot-autoconfigure-3.4.5.jar!/:3.4.5]
2026-10-28T13:23:16.7804749Z 	at org.springframework.boot.autoconfigure.batch.JobLauncherApplicationRunner.launchJobFromProperties(JobLauncherApplicationRunner.java:174) ~[spring-boot-autoconfigure-3.4.5.jar!/:3.4.5]
2026-10-28T13:23:16.7805135Z 	at org.springframework.boot.autoconfigure.batch.JobLauncherApplicationRunner.run(JobLauncherApplicationRunner.java:169) ~[spring-boot-autoconfigure-3.4.5.jar!/:3.4.5]
2026-10-28T13:23:16.7805504Z 	at org.springframework.boot.autoconfigure.batch.JobLauncherApplicationRunner.run(JobLauncherApplicationRunner.java:164) ~[spring-boot-autoconfigure-3.4.5.jar!/:3.4.5]
2026-10-28T13:23:16.7805916Z 	at org.springframework.boot.SpringApplication.lambda$callRunner$4(SpringApplication.java:785) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-28T13:23:16.7806297Z 	at org.springframework.util.function.ThrowingConsumer$1.acceptWithException(ThrowingConsumer.java:82) ~[spring-core-6.2.6.jar!/:6.2.6]
2026-10-28T13:23:16.7806599Z 	at org.springframework.util.function.ThrowingConsumer.accept(ThrowingConsumer.java:60) ~[spring-core-6.2.6.jar!/:6.2.6]
2026-10-28T13:23:16.7806903Z 	at org.springframework.util.function.ThrowingConsumer$1.accept(ThrowingConsumer.java:86) ~[spring-core-6.2.6.jar!/:6.2.6]
2026-10-28T13:23:16.7807204Z 	at org.springframework.boot.SpringApplication.callRunner(SpringApplication.java:797) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-28T13:23:16.7807508Z 	at org.springframework.boot.SpringApplication.callRunner(SpringApplication.java:785) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-28T13:23:16.7807956Z 	at org.springframework.boot.SpringApplication.lambda$callRunners$3(SpringApplication.java:773) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-28T13:23:16.7808166Z 	at java.base/java.util.stream.ForEachOps$ForEachOp$OfRef.accept(ForEachOps.java:183) ~[na:na]
2026-10-28T13:23:16.7808368Z 	at java.base/java.util.stream.SortedOps$SizedRefSortingSink.end(SortedOps.java:357) ~[na:na]
2026-10-28T13:23:16.7808562Z 	at java.base/java.util.stream.AbstractPipeline.copyInto(AbstractPipeline.java:510) ~[na:na]
2026-10-28T13:23:16.7808758Z 	at java.base/java.util.stream.AbstractPipeline.wrapAndCopyInto(AbstractPipeline.java:499) ~[na:na]
2026-10-28T13:23:16.7808949Z 	at java.base/java.util.stream.ForEachOps$ForEachOp.evaluateSequential(ForEachOps.java:150) ~[na:na]
2026-10-28T13:23:16.7809152Z 	at java.base/java.util.stream.ForEachOps$ForEachOp$OfRef.evaluateSequential(ForEachOps.java:173) ~[na:na]
2026-10-28T13:23:16.7809354Z 	at java.base/java.util.stream.AbstractPipeline.evaluate(AbstractPipeline.java:234) ~[na:na]
2026-10-28T13:23:16.7809548Z 	at java.base/java.util.stream.ReferencePipeline.forEach(ReferencePipeline.java:596) ~[na:na]
2026-10-28T13:23:16.7809849Z 	at org.springframework.boot.SpringApplication.callRunners(SpringApplication.java:773) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-28T13:23:16.7810135Z 	at org.springframework.boot.SpringApplication.run(SpringApplication.java:325) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-28T13:23:16.7810421Z 	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1362) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-28T13:23:16.7810713Z 	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1351) ~[spring-boot-3.4.5.jar!/:3.4.5]
2026-10-28T13:23:16.7811018Z 	at br.com.caixa.sisib.arquivosquebra.ArquivoQuebraApplication.main(ArquivoQuebraApplication.java:10) ~[!/:1.0.0-SNAPSHOT]
2026-10-28T13:23:16.7811211Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[na:na]
2026-10-28T13:23:16.7811412Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77) ~[na:na]
2026-10-28T13:23:16.7811629Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[na:na]
2026-10-28T13:23:16.7811823Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568) ~[na:na]
2026-10-28T13:23:16.7812132Z 	at org.springframework.boot.loader.launch.Launcher.launch(Launcher.java:102) ~[sisib-arquivos-de-quebra-1.0.0-SNAPSHOT.jar:1.0.0-SNAPSHOT]
2026-10-28T13:23:16.7812540Z 	at org.springframework.boot.loader.launch.Launcher.launch(Launcher.java:64) ~[sisib-arquivos-de-quebra-1.0.0-SNAPSHOT.jar:1.0.0-SNAPSHOT]
2026-10-28T13:23:16.7812898Z 	at org.springframework.boot.loader.launch.JarLauncher.main(JarLauncher.java:40) ~[sisib-arquivos-de-quebra-1.0.0-SNAPSHOT.jar:1.0.0-SNAPSHOT]
2026-10-28T13:23:16.7813021Z 
2026-10-28T13:23:16.7813297Z 2026-10-28T10:21:15.028-03:00  INFO 8 --- [sisib-arquivos-de-quebra] [           main] o.s.batch.core.step.AbstractStep         : Step: [validarArquivoStep] executed in 33ms
2026-10-28T13:23:16.7813908Z 2026-10-28T10:21:15.094-03:00  INFO 8 --- [sisib-arquivos-de-quebra] [           main] o.s.b.c.l.s.TaskExecutorJobLauncher      : Job: [SimpleJob: [name=validarArquivoJob]] completed with the following parameters: [{'run.id':'{value=1, type=class java.lang.Long, identifying=true}'}] and the following status: [FAILED] in 160ms
2026-10-28T13:23:16.7814393Z 2026-10-28T10:21:15.102-03:00  INFO 8 --- [sisib-arquivos-de-quebra] [ionShutdownHook] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Shutdown initiated...
2026-10-28T13:23:16.7814737Z 2026-10-28T10:21:15.104-03:00  INFO 8 --- [sisib-arquivos-de-quebra] [ionShutdownHook] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Shutdown completed.
2026-10-28T13:23:16.7915709Z ##[section]Finishing: Logs da Aplicação


ta ai a falha
