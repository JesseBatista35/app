
Bash Script

View raw log
Starting: Bash Script
==============================================================================
Task         : Bash
Description  : Run a Bash script on macOS, Linux, or Windows
Version      : 3.227.0
Author       : Microsoft Corporation
Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
==============================================================================
Generating script.
========================== Starting Command Output ===========================
/usr/bin/bash /opt/ads-agent/_work/_temp/1ae76dd0-a1ab-43c9-9f60-d9d8e1a0a5df.sh
-rwxr-xr-x. 1 10940372 30000004 17000 set 12  2023 /usr/java/open-jdk-17.0.8/bin/javac

Finishing: Bash Script



2026-11-17T17:40:54.6579683Z ##[section]Starting: Maven
2026-11-17T17:40:54.6585808Z ==============================================================================
2026-11-17T17:40:54.6585892Z Task         : Maven
2026-11-17T17:40:54.6585972Z Description  : Build, test, and deploy with Apache Maven
2026-11-17T17:40:54.6586036Z Version      : 4.225.0
2026-11-17T17:40:54.6586081Z Author       : Microsoft Corporation
2026-11-17T17:40:54.6586164Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/build/maven
2026-11-17T17:40:54.6586236Z ==============================================================================
2026-11-17T17:40:56.4709461Z [command]/opt/apache-maven/apache-maven-3.8.5/bin/mvn -version
2026-11-17T17:40:56.6207608Z Apache Maven 3.8.5 (3599d3414f046de2324203b78ddcf9b5e4388aa0)
2026-11-17T17:40:56.6208118Z Maven home: /opt/apache-maven/apache-maven-3.8.5
2026-11-17T17:40:56.6208367Z Java version: 17.0.8, vendor: OpenLogic, runtime: /usr/java/open-jdk-17.0.8
2026-11-17T17:40:56.6208739Z Default locale: pt_BR, platform encoding: UTF-8
2026-11-17T17:40:56.6209051Z OS name: "linux", version: "5.18.5-100.fc35.x86_64", arch: "amd64", family: "unix"
2026-11-17T17:40:56.6398094Z [command]/opt/apache-maven/apache-maven-3.8.5/bin/mvn -f /opt/ads-agent/_work/6/s/pom.xml clean verify -Dversion.app= -U
2026-11-17T17:40:57.3366610Z [INFO] Scanning for projects...
2026-11-17T17:40:57.4047561Z [INFO] ------------------------------------------------------------------------
2026-11-17T17:40:57.4048443Z [INFO] Reactor Build Order:
2026-11-17T17:40:57.4049208Z [INFO] 
2026-11-17T17:40:57.4052666Z [INFO] siemp application                                                  [pom]
2026-11-17T17:40:57.4053110Z [INFO] SIEMP Web module                                                   [war]
2026-11-17T17:40:57.4061253Z [INFO] SIEMP EAR module                                                   [ear]
2026-11-17T17:40:57.4097044Z [INFO] 
2026-11-17T17:40:57.4097594Z [INFO] ----------------------< br.gov.caixa.siemp:siemp >----------------------
2026-11-17T17:40:57.4097833Z [INFO] Building siemp application 14.37.0.6                               [1/3]
2026-11-17T17:40:57.4098892Z [INFO] --------------------------------[ pom ]---------------------------------
2026-11-17T17:40:57.4464691Z [INFO] 
2026-11-17T17:40:57.4465812Z [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ siemp ---
2026-11-17T17:40:57.4843981Z [INFO] 
2026-11-17T17:40:57.4844937Z [INFO] --- jacoco-maven-plugin:0.8.13:prepare-agent (prepare-agent) @ siemp ---
2026-11-17T17:40:57.5536149Z [INFO] argLine set to -javaagent:/opt/ads-agent/cache-tools/.m2/repository/org/jacoco/org.jacoco.agent/0.8.13/org.jacoco.agent-0.8.13-runtime.jar=destfile=/opt/ads-agent/_work/6/s/target/jacoco.exec
2026-11-17T17:40:57.5536588Z [INFO] 
2026-11-17T17:40:57.5536849Z [INFO] --- jacoco-maven-plugin:0.8.13:report (generate-report) @ siemp ---
2026-11-17T17:40:57.5553744Z [INFO] Skipping JaCoCo execution due to missing execution data file.
2026-11-17T17:40:57.5555523Z [INFO] 
2026-11-17T17:40:57.5555899Z [INFO] --------------------< br.gov.caixa.siemp:siemp-web >--------------------
2026-11-17T17:40:57.5556938Z [INFO] Building SIEMP Web module 14.37.0.6                                [2/3]
2026-11-17T17:40:57.5557520Z [INFO] --------------------------------[ war ]---------------------------------
2026-11-17T17:40:57.7300944Z [INFO] 
2026-11-17T17:40:57.7303215Z [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ siemp-web ---
2026-11-17T17:40:57.7317858Z [INFO] 
2026-11-17T17:40:57.7318610Z [INFO] --- jacoco-maven-plugin:0.8.13:prepare-agent (prepare-agent) @ siemp-web ---
2026-11-17T17:40:57.7326923Z [INFO] argLine set to -javaagent:/opt/ads-agent/cache-tools/.m2/repository/org/jacoco/org.jacoco.agent/0.8.13/org.jacoco.agent-0.8.13-runtime.jar=destfile=/opt/ads-agent/_work/6/s/siemp-web/target/jacoco.exec
2026-11-17T17:40:57.7327418Z [INFO] 
2026-11-17T17:40:57.7328439Z [INFO] --- maven-resources-plugin:3.3.1:resources (default-resources) @ siemp-web ---
2026-11-17T17:40:57.7761697Z [INFO] Copying 6 resources from src/main/resources to target/classes
2026-11-17T17:40:57.8669446Z [INFO] Copying 682 resources from src/main/java to target/classes
2026-11-17T17:40:57.9229413Z [INFO] The encoding used to copy filtered properties files have not been set. This means that the same encoding will be used to copy filtered properties files as when copying other filtered resources. This might not be what you want! Run your build with --debug to see which files might be affected. Read more at https://maven.apache.org/plugins/maven-resources-plugin/examples/filtering-properties-files.html
2026-11-17T17:40:57.9230400Z [INFO] 
2026-11-17T17:40:57.9232360Z [INFO] --- maven-compiler-plugin:3.11.0:compile (default-compile) @ siemp-web ---
2026-11-17T17:40:58.0728562Z [INFO] Changes detected - recompiling the module! :source
2026-11-17T17:40:58.0807803Z [INFO] Compiling 2259 source files with javac [debug release 17] to target/classes
2026-11-17T17:41:05.6124420Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(288,23): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[288,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6133450Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(302,23): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[302,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6134616Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[288,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6135227Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[302,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6138259Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(310,21): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[310,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6140588Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(318,21): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[318,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6180634Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(334,20): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[334,20] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6184816Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(342,21): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[342,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6187037Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(350,20): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[350,20] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6189353Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(361,21): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[361,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6192120Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(621,21): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[621,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6196822Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(629,23): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[629,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6199289Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(844,23): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[844,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6201714Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(964,35): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[964,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6204077Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java(95,28): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[95,28] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6206368Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java(106,24): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[106,24] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6208691Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java(608,85): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[608,85] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6211139Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java(608,36): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[608,36] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6213544Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/TratarTOForm.java(528,51): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/TratarTOForm.java:[528,51] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6215986Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java(558,51): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[558,51] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6218258Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java(601,85): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[601,85] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6220737Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java(601,36): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[601,36] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6223469Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterTabelaHelper.java(17,8): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterTabelaHelper.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6225690Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterSelectMultipleHelper.java(17,8): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterSelectMultipleHelper.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6227913Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/filtros/formatador/FormatadorDeRotulo.java(108,23): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/filtros/formatador/FormatadorDeRotulo.java:[108,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6230264Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(53,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[53,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6232664Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(70,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[70,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6235090Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(121,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[121,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6237529Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(128,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[128,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6239927Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(134,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[134,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6242564Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(140,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[140,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6244949Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(145,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[145,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6247488Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(150,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[150,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6249821Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(155,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[155,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6250835Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[310,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6251329Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[318,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6251708Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[334,20] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6252165Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[342,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6252557Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[350,20] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6252922Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[361,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6253344Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[621,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6253732Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[629,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6254092Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[844,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6254453Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[964,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6254819Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[95,28] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6255181Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[106,24] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6255594Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[608,85] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6256093Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[608,36] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6256524Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/TratarTOForm.java:[528,51] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6256972Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[558,51] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6257740Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[601,85] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6258159Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[601,36] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6258599Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterTabelaHelper.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6258969Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterSelectMultipleHelper.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6259381Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/filtros/formatador/FormatadorDeRotulo.java:[108,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6259785Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[53,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6260222Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[70,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6260634Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[121,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6261151Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[128,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6261635Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[134,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6262058Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[140,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6262465Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[145,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6262893Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[150,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6263318Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[155,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6265540Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(160,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[160,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6267938Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(166,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[166,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6270141Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(176,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[176,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6272724Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(182,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[182,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6274951Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(188,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[188,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6277168Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(356,42): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[356,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6279530Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(371,42): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[371,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6282094Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(386,42): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[386,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6284418Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(416,42): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[416,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6286775Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(431,42): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[431,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6289027Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(446,42): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[446,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6291364Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(462,42): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[462,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6293673Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(478,42): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[478,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6296004Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(520,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[520,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6298344Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(989,50): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[989,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6300523Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/FabricaDeCombos.java(24,8): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/FabricaDeCombos.java:[24,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6303044Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/IObjetoParaCombo.java(17,8): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/IObjetoParaCombo.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6305286Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java(203,23): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java:[203,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6307674Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java(297,23): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java:[297,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6309861Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java(24,8): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java:[24,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6312190Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/IObjetoParaComboComAtributos.java(20,8): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/IObjetoParaComboComAtributos.java:[20,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6314398Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(78,31): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[78,31] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6316661Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(93,35): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[93,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6318806Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(106,35): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[106,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6320968Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(136,21): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[136,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6323345Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(284,26): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[284,26] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6325522Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(291,35): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[291,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6327768Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(301,26): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[301,26] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6329911Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(308,26): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[308,26] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6332283Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(322,27): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[322,27] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6334564Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(345,24): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[345,24] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6336763Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(352,26): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[352,26] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6338879Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(368,26): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[368,26] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6341837Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(407,24): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[407,24] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6345656Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(539,26): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[539,26] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6347944Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(557,26): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[557,26] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6350891Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java(564,24): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[564,24] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6353481Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/BusinessDelegate.java(230,59): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/BusinessDelegate.java:[230,59] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6356391Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/XMLProgramAnalyzer.java(353,41): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/XMLProgramAnalyzer.java:[353,41] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6359181Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(89,109): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[89,109] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6361527Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(97,108): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[97,108] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6363920Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(105,107): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[105,107] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6366818Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(112,110): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[112,110] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6369253Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(120,109): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[120,109] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6371703Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(129,108): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[129,108] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6373965Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(137,107): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[137,107] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6376244Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(145,110): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[145,110] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6379576Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(150,99): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[150,99] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6383285Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(164,94): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[164,94] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6385740Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(136,32): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[136,32] Double(java.lang.String) in java.lang.Double has been deprecated and marked for removal
2026-11-17T17:41:05.6388826Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(148,32): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[148,32] Float(java.lang.String) in java.lang.Float has been deprecated and marked for removal
2026-11-17T17:41:05.6391371Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(157,32): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[157,32] Long(java.lang.String) in java.lang.Long has been deprecated and marked for removal
2026-11-17T17:41:05.6394167Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(166,32): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[166,32] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6396609Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(180,32): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[180,32] Double(java.lang.String) in java.lang.Double has been deprecated and marked for removal
2026-11-17T17:41:05.6398817Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(192,32): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[192,32] Float(java.lang.String) in java.lang.Float has been deprecated and marked for removal
2026-11-17T17:41:05.6401218Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(201,32): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[201,32] Long(java.lang.String) in java.lang.Long has been deprecated and marked for removal
2026-11-17T17:41:05.6403605Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(210,32): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[210,32] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6406630Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java(38,39): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[38,39] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6410474Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java(56,42): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[56,42] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6414338Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java(66,46): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[66,46] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6418129Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java(76,45): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[76,45] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6422007Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java(86,35): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[86,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6426095Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java(97,35): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[97,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6429313Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java(107,35): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[107,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6432210Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java(117,35): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[117,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6434727Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java(127,35): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[127,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6436980Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java(137,35): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[137,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6439198Z ##[warning] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java(147,35): warning :  /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[147,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6440128Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[160,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6440571Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[166,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6441082Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[176,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6441567Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[182,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6441983Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[188,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6442426Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[356,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6442866Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[371,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6443465Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[386,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6444204Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[416,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6445057Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[431,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6445644Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[446,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6446233Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[462,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6446735Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[478,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6447296Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[520,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6447803Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[989,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6448441Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/FabricaDeCombos.java:[24,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6448850Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/IObjetoParaCombo.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6449281Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java:[203,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6449804Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java:[297,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6450236Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java:[24,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6450729Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/IObjetoParaComboComAtributos.java:[20,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6451249Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[78,31] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6451798Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[93,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6452195Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[106,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6452597Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[136,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6452994Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[284,26] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6453349Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[291,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6453789Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[301,26] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6454145Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[308,26] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6454497Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[322,27] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6454853Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[345,24] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6455216Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[352,26] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6455579Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[368,26] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6455956Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[407,24] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6456310Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[539,26] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6456706Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[557,26] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6457058Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempAction.java:[564,24] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6457684Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/BusinessDelegate.java:[230,59] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6458140Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/XMLProgramAnalyzer.java:[353,41] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6458552Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[89,109] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6458773Z   cast to java.lang.Object for a varargs call
2026-11-17T17:41:05.6459039Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:41:05.6459388Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[97,108] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6459606Z   cast to java.lang.Object for a varargs call
2026-11-17T17:41:05.6459846Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:41:05.6460298Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[105,107] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6460527Z   cast to java.lang.Object for a varargs call
2026-11-17T17:41:05.6460830Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:41:05.6461309Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[112,110] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6461616Z   cast to java.lang.Object for a varargs call
2026-11-17T17:41:05.6461961Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:41:05.6462447Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[120,109] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6462671Z   cast to java.lang.Object for a varargs call
2026-11-17T17:41:05.6462903Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:41:05.6463247Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[129,108] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6463478Z   cast to java.lang.Object for a varargs call
2026-11-17T17:41:05.6463711Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:41:05.6464055Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[137,107] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6464293Z   cast to java.lang.Object for a varargs call
2026-11-17T17:41:05.6464520Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:41:05.6464860Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[145,110] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6465074Z   cast to java.lang.Object for a varargs call
2026-11-17T17:41:05.6465317Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:41:05.6465672Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[150,99] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6465888Z   cast to java.lang.Object for a varargs call
2026-11-17T17:41:05.6466124Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:41:05.6466465Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[164,94] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:41:05.6466725Z   cast to java.lang.Object for a varargs call
2026-11-17T17:41:05.6466955Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:41:05.6467306Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[136,32] Double(java.lang.String) in java.lang.Double has been deprecated and marked for removal
2026-11-17T17:41:05.6467722Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[148,32] Float(java.lang.String) in java.lang.Float has been deprecated and marked for removal
2026-11-17T17:41:05.6468121Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[157,32] Long(java.lang.String) in java.lang.Long has been deprecated and marked for removal
2026-11-17T17:41:05.6468524Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[166,32] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6468924Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[180,32] Double(java.lang.String) in java.lang.Double has been deprecated and marked for removal
2026-11-17T17:41:05.6469316Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[192,32] Float(java.lang.String) in java.lang.Float has been deprecated and marked for removal
2026-11-17T17:41:05.6469720Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[201,32] Long(java.lang.String) in java.lang.Long has been deprecated and marked for removal
2026-11-17T17:41:05.6470150Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[210,32] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:41:05.6470534Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[38,39] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6470970Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[56,42] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6471403Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[66,46] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6471755Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[76,45] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6472184Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[86,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6472596Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[97,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6472976Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[107,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6473385Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[117,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6473745Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[127,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6474102Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[137,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6474455Z [WARNING] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/FabricaDeFacade.java:[147,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:41:05.6474774Z [INFO] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java: Some input files use or override a deprecated API.
2026-11-17T17:41:05.6475280Z [INFO] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java: Recompile with -Xlint:deprecation for details.
2026-11-17T17:41:05.6475675Z [INFO] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/persistencia/SiempDAOMainframe.java: Some input files additionally use or override a deprecated API that is marked for removal.
2026-11-17T17:41:05.6476057Z [INFO] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java: Some input files use unchecked or unsafe operations.
2026-11-17T17:41:05.6476434Z [INFO] /opt/ads-agent/_work/6/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java: Recompile with -Xlint:unchecked for details.
2026-11-17T17:41:05.6476626Z [INFO] 
2026-11-17T17:41:05.6476869Z [INFO] --- maven-resources-plugin:3.3.1:testResources (default-testResources) @ siemp-web ---
2026-11-17T17:41:05.6477137Z [INFO] Copying 1 resource from src/test/resources to target/test-classes
2026-11-17T17:41:05.6477286Z [INFO] 
2026-11-17T17:41:05.6477534Z [INFO] --- maven-compiler-plugin:3.11.0:testCompile (default-testCompile) @ siemp-web ---
2026-11-17T17:41:05.6477793Z [INFO] Changes detected - recompiling the module! :dependency
2026-11-17T17:41:05.6478050Z [INFO] Compiling 30 source files with javac [debug release 17] to target/test-classes
2026-11-17T17:41:06.0911207Z [INFO] /opt/ads-agent/_work/6/s/siemp-web/src/test/java/br/gov/caixa/siemp/apresentacao/consignacao/consultaTabelaDeTACDeConvenio/ConsultaTabelaDeTACDeConvenioHelpersTest.java: Some input files use or override a deprecated API.
2026-11-17T17:41:06.0911959Z [INFO] /opt/ads-agent/_work/6/s/siemp-web/src/test/java/br/gov/caixa/siemp/apresentacao/consignacao/consultaTabelaDeTACDeConvenio/ConsultaTabelaDeTACDeConvenioHelpersTest.java: Recompile with -Xlint:deprecation for details.
2026-11-17T17:41:06.0912825Z [INFO] /opt/ads-agent/_work/6/s/siemp-web/src/test/java/br/gov/caixa/siemp/comum/apresentacao/login/LoginMenuConsultasTest.java: /opt/ads-agent/_work/6/s/siemp-web/src/test/java/br/gov/caixa/siemp/comum/apresentacao/login/LoginMenuConsultasTest.java uses unchecked or unsafe operations.
2026-11-17T17:41:06.0913602Z [INFO] /opt/ads-agent/_work/6/s/siemp-web/src/test/java/br/gov/caixa/siemp/comum/apresentacao/login/LoginMenuConsultasTest.java: Recompile with -Xlint:unchecked for details.
2026-11-17T17:41:06.0913926Z [INFO] 
2026-11-17T17:41:06.0914325Z [INFO] --- maven-surefire-plugin:3.2.5:test (default-test) @ siemp-web ---
2026-11-17T17:41:06.2113192Z [INFO] Using auto detected provider org.apache.maven.surefire.junit4.JUnit4Provider
2026-11-17T17:41:06.2392348Z [INFO] 
2026-11-17T17:41:06.2393065Z [INFO] -------------------------------------------------------
2026-11-17T17:41:06.2393232Z [INFO]  T E S T S
2026-11-17T17:41:06.2393449Z [INFO] -------------------------------------------------------
2026-11-17T17:41:06.6798463Z [INFO] Running br.gov.caixa.siemp.comum.apresentacao.login.LoginActionTest
2026-11-17T17:41:06.7413784Z log4j:WARN No appenders could be found for logger (org.apache.struts.util.PropertyMessageResources).
2026-11-17T17:41:06.7415519Z log4j:WARN Please initialize the log4j system properly.
2026-11-17T17:41:06.7586399Z [INFO] Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.068 s -- in br.gov.caixa.siemp.comum.apresentacao.login.LoginActionTest
2026-11-17T17:41:06.7587089Z [INFO] Running br.gov.caixa.siemp.comum.apresentacao.login.LoginMenuConsultasTest
2026-11-17T17:41:06.7853112Z [INFO] Tests run: 12, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.006 s -- in br.gov.caixa.siemp.comum.apresentacao.login.LoginMenuConsultasTest
2026-11-17T17:41:06.7853523Z [INFO] Running br.gov.caixa.siemp.comum.apresentacao.SiempActionTest
2026-11-17T17:41:06.8028839Z [INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.031 s -- in br.gov.caixa.siemp.comum.apresentacao.SiempActionTest
2026-11-17T17:41:06.8029164Z [INFO] Running br.gov.caixa.siemp.consultas.ConsultasContratoTest
2026-11-17T17:41:07.3918444Z [WARNING] Tests run: 180, Failures: 0, Errors: 0, Skipped: 13, Time elapsed: 0.571 s -- in br.gov.caixa.siemp.consultas.ConsultasContratoTest
2026-11-17T17:41:07.3918895Z [INFO] Running br.gov.caixa.siemp.consultas.ConfiguracaoJstlValidatorTest
2026-11-17T17:41:07.4014758Z [INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.004 s -- in br.gov.caixa.siemp.consultas.ConfiguracaoJstlValidatorTest
2026-11-17T17:41:07.4015067Z [INFO] Running br.gov.caixa.siemp.consultas.ConveniosActionsTest
2026-11-17T17:41:07.4121440Z [INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.008 s -- in br.gov.caixa.siemp.consultas.ConveniosActionsTest
2026-11-17T17:41:07.4121740Z [INFO] Running br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest
2026-11-17T17:41:07.5298906Z Criando Log de Sistema
2026-11-17T17:41:07.5299142Z Log do Sitema inicializada!
2026-11-17T17:41:07.6238276Z org.apache.commons.fileupload.FileUploadBase$SizeLimitExceededException: the request was rejected because its size (5243003) exceeds the configured maximum (5242880)
2026-11-17T17:41:07.6246200Z 	at org.apache.commons.fileupload.FileUploadBase$FileItemIteratorImpl.<init>(FileUploadBase.java:965)
2026-11-17T17:41:07.6246412Z 	at org.apache.commons.fileupload.FileUploadBase.getItemIterator(FileUploadBase.java:310)
2026-11-17T17:41:07.6246876Z 	at org.apache.commons.fileupload.FileUploadBase.parseRequest(FileUploadBase.java:334)
2026-11-17T17:41:07.6247105Z 	at org.apache.commons.fileupload.FileUploadBase.parseRequest(FileUploadBase.java:288)
2026-11-17T17:41:07.6247419Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServlet.obterArquivoLegivel(AtualizarIndiceBovespaServlet.java:77)
2026-11-17T17:41:07.6260845Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServlet.doPost(AtualizarIndiceBovespaServlet.java:55)
2026-11-17T17:41:07.6261457Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest.deveRejeitarUploadAcimaDeCincoMegabytes(AtualizarIndiceBovespaServletTest.java:111)
2026-11-17T17:41:07.6261727Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:07.6261951Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:07.6262207Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:07.6262430Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:07.6262643Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:07.6262897Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:07.6263117Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:07.6263456Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:07.6263668Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:07.6263877Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:07.6264116Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:07.6264328Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:07.6264533Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:07.6264735Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:07.6281178Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:07.6281825Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:07.6282040Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:07.6282313Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:07.6282551Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:07.6282863Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:07.6283090Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:07.6283389Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:07.6283630Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:07.6283813Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:07.6284029Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:07.6284828Z java.lang.Exception: falha
2026-11-17T17:41:07.6285164Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest$3.atualizarIndice(AtualizarIndiceBovespaServletTest.java:206)
2026-11-17T17:41:07.6285470Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServlet.processarAtualizacao(AtualizarIndiceBovespaServlet.java:112)
2026-11-17T17:41:07.6285753Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServlet.doPost(AtualizarIndiceBovespaServlet.java:63)
2026-11-17T17:41:07.6286299Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest.executarComDelegate(AtualizarIndiceBovespaServletTest.java:249)
2026-11-17T17:41:07.6286812Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest.deveTratarFalhaNaAtualizacao(AtualizarIndiceBovespaServletTest.java:212)
2026-11-17T17:41:07.6287158Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:07.6287383Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:07.6287632Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:07.6287854Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:07.6288032Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:07.6288263Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:07.6288487Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:07.6304061Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:07.6304462Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:07.6304808Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:07.6305151Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:07.6305549Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:07.6305750Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:07.6306037Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:07.6306242Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:07.6306444Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:07.6306610Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:07.6306823Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:07.6307050Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:07.6307369Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:07.6307674Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:07.6307905Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:07.6308167Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:07.6308379Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:07.6308588Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:07.6362606Z [INFO] Tests run: 14, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.220 s -- in br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest
2026-11-17T17:41:07.6363206Z [INFO] Running br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.manterpercentualdetaxasdejuros.CopiarEstruturaDeTabelaDeTaxasFormTest
2026-11-17T17:41:07.6363628Z [INFO] Tests run: 8, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.manterpercentualdetaxasdejuros.CopiarEstruturaDeTabelaDeTaxasFormTest
2026-11-17T17:41:07.6363921Z [INFO] Running br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.manterpercentualdetaxasdejuros.ReceberVigenciaFormTest
2026-11-17T17:41:07.6901374Z [INFO] Tests run: 10, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.051 s -- in br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.manterpercentualdetaxasdejuros.ReceberVigenciaFormTest
2026-11-17T17:41:07.6901904Z [INFO] Running br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.atualizarvaloresnamatrizdeexcepcionacao.AtualizarValoresNaMatrizDeExcepcionacaoFormTest
2026-11-17T17:41:07.7000184Z [INFO] Tests run: 13, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.008 s -- in br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.atualizarvaloresnamatrizdeexcepcionacao.AtualizarValoresNaMatrizDeExcepcionacaoFormTest
2026-11-17T17:41:07.7000529Z [INFO] Running br.gov.caixa.siemp.relatorios.ModelosJasperTest
2026-11-17T17:41:09.1473140Z [ERROR] Tests run: 52, Failures: 0, Errors: 26, Skipped: 0, Time elapsed: 1.436 s <<< FAILURE! -- in br.gov.caixa.siemp.relatorios.ModelosJasperTest
2026-11-17T17:41:09.1481315Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarParametrosDoConvenio.jasper] -- Time elapsed: 0.550 s <<< ERROR!
2026-11-17T17:41:09.1481734Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarParametrosDoConvenio_1794937268241_468811.java 
2026-11-17T17:41:09.1482098Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1482355Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1483831Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1484079Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1484488Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1484753Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1484982Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1485201Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1485445Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1485662Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1485841Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1486104Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1486331Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1486566Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1486772Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1486978Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1487199Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1487439Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1487634Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1487846Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1488015Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1488213Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1488419Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1488603Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1488784Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1488971Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1489169Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1489422Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1489631Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1489837Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1489995Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1490199Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1490504Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1490743Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1490965Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1491262Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1491485Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1491720Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1491930Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1492260Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1492434Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1492635Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1492998Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1493179Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1493454Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1493634Z 	... 38 more
2026-11-17T17:41:09.1493872Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1494058Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1494252Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1494412Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1494604Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1494789Z 	... 42 more
2026-11-17T17:41:09.1494862Z 
2026-11-17T17:41:09.1495152Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarParametrosDoConvenioReport.jasper] -- Time elapsed: 0.056 s <<< ERROR!
2026-11-17T17:41:09.1495559Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarParametrosDoConvenioReport_1794937268352_668265.java 
2026-11-17T17:41:09.1495816Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1496074Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1496314Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1496717Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1497004Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1497284Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1497511Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1497813Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1498055Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1498355Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1498571Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1498791Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1498977Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1499197Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1499402Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1499632Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1499845Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1500046Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1500265Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1500461Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1500652Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1500842Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1501000Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1501263Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1501442Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1501671Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1501880Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1502119Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1502336Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1502555Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1502747Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1502914Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1503133Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1503357Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1503577Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1503863Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1504098Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1504302Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1504514Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1504808Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1615991Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1616273Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1616493Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1616722Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1616953Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1617149Z 	... 38 more
2026-11-17T17:41:09.1617635Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1617858Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1618014Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1618377Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1618579Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1618743Z 	... 42 more
2026-11-17T17:41:09.1618783Z 
2026-11-17T17:41:09.1619108Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarTabelaDeTACDoConvenio.jasper] -- Time elapsed: 0.100 s <<< ERROR!
2026-11-17T17:41:09.1619525Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarTabelaDeTACDoConvenio_1794937268457_629512.java 
2026-11-17T17:41:09.1619797Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1620043Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1620303Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1620605Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1620842Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1621225Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1621482Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1621790Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1622041Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1622263Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1622472Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1622668Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1622890Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1623136Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1623369Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1623585Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1623808Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1624031Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1624234Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1624436Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1624635Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1624806Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1625029Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1625238Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1625423Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1625612Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1625810Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1626011Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1626227Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1626433Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1626637Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1626809Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1627083Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1627326Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1627569Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1627795Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1628017Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1628229Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1628449Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1628746Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1628952Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1629167Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1629324Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1629506Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1629710Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1629921Z 	... 38 more
2026-11-17T17:41:09.1630143Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1630391Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1631251Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1631475Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1631672Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1631848Z 	... 42 more
2026-11-17T17:41:09.1631895Z 
2026-11-17T17:41:09.1632228Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarTabelaDeTACDoConvenioNovo.jasper] -- Time elapsed: 0.049 s <<< ERROR!
2026-11-17T17:41:09.1632633Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarTabelaDeTACDoConvenioNovo_1794937268517_732892.java 
2026-11-17T17:41:09.1632893Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1633138Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1633380Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1633622Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1633873Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1634092Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1634323Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1634536Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1634773Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1634989Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1635192Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1635423Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1635641Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1635920Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1636123Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1636328Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1636510Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1636712Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1636914Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1637122Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1637316Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1637513Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1637721Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1637906Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1638125Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1638278Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1638473Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1638670Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1638878Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1639114Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1639303Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1639520Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1639744Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1639969Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1640196Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1640382Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1640610Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1640819Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1641097Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1641600Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1641849Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1642048Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1642237Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1642430Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1642638Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1642816Z 	... 38 more
2026-11-17T17:41:09.1643004Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1643186Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1643369Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1643581Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1643775Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1643936Z 	... 42 more
2026-11-17T17:41:09.1643976Z 
2026-11-17T17:41:09.1644337Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarTabelaDeTACDoConvenioSubReport.jasper] -- Time elapsed: 0.058 s <<< ERROR!
2026-11-17T17:41:09.1644780Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarTabelaDeTACDoConvenioSubReport_1794937268580_79752.java 
2026-11-17T17:41:09.1645039Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1645277Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1645522Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1645793Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1646035Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1646283Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1646481Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1646691Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1646931Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1647148Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1647355Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1647615Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1647859Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1648079Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1648281Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1648485Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1648701Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1648875Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1649068Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1649263Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1649465Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1649687Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1649879Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1650060Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1650237Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1650420Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1650579Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1650776Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1650969Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1651308Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1651519Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1651727Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1651948Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1652197Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1652499Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1652873Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1653224Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1653407Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1653616Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1653934Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1654144Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1654340Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1654529Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1654708Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1654908Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1655095Z 	... 38 more
2026-11-17T17:41:09.1655279Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1655460Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1655658Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1655848Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1656046Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1656250Z 	... 42 more
2026-11-17T17:41:09.1656292Z 
2026-11-17T17:41:09.1656633Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarTabelaDeTaxasDoConvenio.jasper] -- Time elapsed: 0.047 s <<< ERROR!
2026-11-17T17:41:09.1657270Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarTabelaDeTaxasDoConvenio_1794937268633_629952.java 
2026-11-17T17:41:09.1657536Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1657773Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1658036Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1658275Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1658505Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1658753Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1658985Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1659168Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1659410Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1659623Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1659824Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1660062Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1660281Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1660499Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1660704Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1660922Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1661240Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1661495Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1661659Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1661860Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1662072Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1662275Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1662466Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1662662Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1662841Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1663023Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1663215Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1663379Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1663580Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1663788Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1663976Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1664189Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1664408Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1664671Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1664896Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1665111Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1665329Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1665556Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1665732Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1666033Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1666235Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1666431Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1666619Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1666797Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1667002Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1667173Z 	... 38 more
2026-11-17T17:41:09.1667400Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1667547Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1667745Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1667933Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1668125Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1668320Z 	... 42 more
2026-11-17T17:41:09.1668359Z 
2026-11-17T17:41:09.1668683Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarTabelaDeTaxasDoConvenioNovo.jasper] -- Time elapsed: 0.040 s <<< ERROR!
2026-11-17T17:41:09.1669089Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarTabelaDeTaxasDoConvenioNovo_1794937268679_570157.java 
2026-11-17T17:41:09.1669347Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1669610Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1669902Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1670140Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1670372Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1670621Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1670856Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1671191Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1671460Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1671646Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1671874Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1672098Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1672316Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1672532Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1672789Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1672994Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1673218Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1673419Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1673627Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1673796Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1673996Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1674193Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1674382Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1674563Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1674742Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1674944Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1675135Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1675445Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1675608Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1675802Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1676023Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1676222Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1676441Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1676666Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1676887Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1677117Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1677360Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1677567Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1677773Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1678078Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1678282Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1678478Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1678662Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1678852Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1679056Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1679247Z 	... 38 more
2026-11-17T17:41:09.1679460Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1679637Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1679787Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1679975Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1680171Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1680334Z 	... 42 more
2026-11-17T17:41:09.1680374Z 
2026-11-17T17:41:09.1680697Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarTabelaDeTaxasDoConvenioSubReport.jasper] -- Time elapsed: 0.021 s <<< ERROR!
2026-11-17T17:41:09.1681158Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarTabelaDeTaxasDoConvenioSubReport_1794937268703_26467.java 
2026-11-17T17:41:09.1681477Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1681716Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1681957Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1682187Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1682424Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1682669Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1682894Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1683103Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1683373Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1683588Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1683760Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1683985Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1684207Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1684432Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1684632Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1684834Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1685049Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1685268Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1685462Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1685655Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1685821Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1686060Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1686251Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1686433Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1686608Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1686795Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1687003Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1687201Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1687407Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1687573Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1687758Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1687957Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1688176Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1688402Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1688619Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1688850Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1689065Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1689309Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1689516Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1689807Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1689978Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1690175Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1690358Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1690553Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1690775Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1690960Z 	... 38 more
2026-11-17T17:41:09.1691329Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1691520Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1691699Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1691856Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1692049Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1692205Z 	... 42 more
2026-11-17T17:41:09.1692281Z 
2026-11-17T17:41:09.1692565Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/relatorioExtratoCreditoRural.jasper] -- Time elapsed: 0.035 s <<< ERROR!
2026-11-17T17:41:09.1692976Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/relatorioExtratoCreditoRural_1794937268740_190611.java 
2026-11-17T17:41:09.1693231Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1693476Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1693715Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1693948Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1694179Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1694465Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1694703Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1694930Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1695167Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1695384Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1695591Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1695784Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1696002Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1696217Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1696418Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1696631Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1696857Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1697064Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1697256Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1697486Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1697678Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1697841Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1698049Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1698244Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1698423Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1698623Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1698816Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1699009Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1699199Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1699394Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1699552Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1699763Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1699983Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1700207Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1700444Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1700663Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1700878Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1701149Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1701358Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1701665Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1701865Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1702030Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1702213Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1702445Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1702647Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1702819Z 	... 38 more
2026-11-17T17:41:09.1703035Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1703223Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1703402Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1703593Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1703750Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1703905Z 	... 42 more
2026-11-17T17:41:09.1703989Z 
2026-11-17T17:41:09.1704296Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/subRelatorioExtrato.jasper] -- Time elapsed: 0.010 s <<< ERROR!
2026-11-17T17:41:09.1704644Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioExtrato_1794937268754_393449.java 
2026-11-17T17:41:09.1704892Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1705140Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1705394Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1705663Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1705889Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1706135Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1706374Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1706590Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1706835Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1707050Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1707252Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1707476Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1707661Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1707874Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1708075Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1708289Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1708503Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1708713Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1708907Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1709097Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1709294Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1709492Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1709652Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1709834Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1710025Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1710219Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1710442Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1710638Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1710833Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1711190Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1711409Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1711582Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1711806Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1712063Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1712287Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1712508Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1712756Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1712968Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1713176Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1713475Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1713679Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1713950Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1714110Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1714291Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1714496Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1714675Z 	... 38 more
2026-11-17T17:41:09.1714892Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1715069Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1715249Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1715447Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1715650Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1715774Z 	... 42 more
2026-11-17T17:41:09.1715848Z 
2026-11-17T17:41:09.1716152Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/subRelatorioLiberacoes.jasper] -- Time elapsed: 0.010 s <<< ERROR!
2026-11-17T17:41:09.1716529Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioLiberacoes_1794937268765_617251.java 
2026-11-17T17:41:09.1716777Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1716985Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1717231Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1717474Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1717702Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1717968Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1718193Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1718404Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1718638Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1718885Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1719098Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1719316Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1719502Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1719718Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1719936Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1720162Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1720375Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1720577Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1720773Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1720975Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1721339Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1721538Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1721698Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1721942Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1722123Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1722311Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1722505Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1722717Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1722912Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1723111Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1723303Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1723521Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1723710Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1723936Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1724160Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1724392Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1724610Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1724853Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1725059Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1725356Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1725568Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1725762Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1725918Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1726101Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1726314Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1726494Z 	... 38 more
2026-11-17T17:41:09.1726706Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1726885Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1727113Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1727340Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1727531Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1727656Z 	... 42 more
2026-11-17T17:41:09.1727738Z 
2026-11-17T17:41:09.1728043Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/subRelatorioOcorrencias.jasper] -- Time elapsed: 0.010 s <<< ERROR!
2026-11-17T17:41:09.1728428Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioOcorrencias_1794937268775_943016.java 
2026-11-17T17:41:09.1728679Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1728912Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1729125Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1729356Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1729600Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1729854Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1730079Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1730317Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1730628Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1730841Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1731146Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1731398Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1731636Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1731821Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1732026Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1732232Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1732458Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1732663Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1732858Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1733058Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1733260Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1733467Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1733655Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1733805Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1733991Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1734179Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1734375Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1734571Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1734798Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1735077Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1735329Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1735598Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1735791Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1736019Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1736244Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1736463Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1736684Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1736895Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1737102Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1737431Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1737637Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1737833Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1738018Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1738169Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1738376Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1738551Z 	... 38 more
2026-11-17T17:41:09.1738809Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1739003Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1739211Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1739402Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1739593Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1739755Z 	... 42 more
2026-11-17T17:41:09.1739797Z 
2026-11-17T17:41:09.1740111Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/subRelatorioPosicaoDivida.jasper] -- Time elapsed: 0.011 s <<< ERROR!
2026-11-17T17:41:09.1740493Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioPosicaoDivida_1794937268787_695668.java 
2026-11-17T17:41:09.1740745Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1740993Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1741309Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1741512Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1741743Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1741991Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1742216Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1742456Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1742692Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1742917Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1743120Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1743353Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1743569Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1743827Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1744001Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1744206Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1744419Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1744632Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1744827Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1745023Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1745234Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1745428Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1745620Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1745801Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1745947Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1746131Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1746335Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1746529Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1746720Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1753928Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1754133Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1754331Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1754551Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1754751Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1754992Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1755214Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1755433Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1755640Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1755870Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1756208Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1756411Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1756670Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1756872Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1757056Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1757231Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1757408Z 	... 38 more
2026-11-17T17:41:09.1757630Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1757823Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1758015Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1758203Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1758412Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1758628Z 	... 42 more
2026-11-17T17:41:09.1758694Z 
2026-11-17T17:41:09.1759016Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/subRelatorioProAgro.jasper] -- Time elapsed: 0.011 s <<< ERROR!
2026-11-17T17:41:09.1759474Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioProAgro_1794937268800_111797.java 
2026-11-17T17:41:09.1759725Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1759980Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1760221Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1760462Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1760659Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1760904Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1761192Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1761407Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1761641Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1761854Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1762071Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1762354Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1762574Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1762793Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1762998Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1763172Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1763388Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1763595Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1763794Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1764015Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1764247Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1764448Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1764644Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1764829Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1765007Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1765163Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1765358Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1765555Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1765781Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1765978Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1766172Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1766387Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1766613Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1766846Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1767041Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1767305Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1767538Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1767771Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1767985Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1768287Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1768497Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1768698Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1768887Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1769080Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1769260Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1769442Z 	... 38 more
2026-11-17T17:41:09.1769685Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1769862Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1770040Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1770230Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1770421Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1770612Z 	... 42 more
2026-11-17T17:41:09.1770654Z 
2026-11-17T17:41:09.1770962Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/subRelatorioReembolsos.jasper] -- Time elapsed: 0.008 s <<< ERROR!
2026-11-17T17:41:09.1771410Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioReembolsos_1794937268810_930945.java 
2026-11-17T17:41:09.1771697Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1771932Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1772172Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1772406Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1772635Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1772846Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1773082Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1773294Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1773533Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1773763Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1773969Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1774193Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1774409Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1774634Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1774836Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1775039Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1775221Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1775459Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1775670Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1775867Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1776063Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1776267Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1776456Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1776639Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1776816Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1776971Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1777165Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1777376Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1777571Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1777763Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1777962Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1778162Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1778381Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1778662Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1778883Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1779070Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1779297Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1779509Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1779725Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1780007Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1780210Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1780406Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1780597Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1780771Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1780983Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1781419Z 	... 38 more
2026-11-17T17:41:09.1781664Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1781849Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1782029Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1782218Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1782410Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1782564Z 	... 42 more
2026-11-17T17:41:09.1782604Z 
2026-11-17T17:41:09.1782922Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/subRelatorioReembolsosVencidos.jasper] -- Time elapsed: 0.013 s <<< ERROR!
2026-11-17T17:41:09.1783333Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioReembolsosVencidos_1794937268823_877128.java 
2026-11-17T17:41:09.1783596Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1783833Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1784114Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1784347Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1784575Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1784821Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1785016Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.1785228Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.1785487Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1785706Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1785969Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1786192Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1786411Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1786652Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1786852Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1787097Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1787325Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1787496Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1787690Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1787891Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1788087Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1788281Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1788472Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1788665Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1788840Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1789039Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1789201Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1789397Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1789592Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1789783Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1789971Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1790171Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1790401Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1790627Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1790861Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1791138Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1791331Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1791537Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1791743Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1792062Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1792275Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1792472Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1792657Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1792847Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1793129Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1793420Z 	... 38 more
2026-11-17T17:41:09.1793693Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1793993Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1794207Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1794398Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1794594Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1794749Z 	... 42 more
2026-11-17T17:41:09.1794790Z 
2026-11-17T17:41:09.1795157Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPlanilhaEvolucaoDivida/relatorioEvolucaoDivida.jasper] -- Time elapsed: 0.078 s <<< ERROR!
2026-11-17T17:41:09.1795549Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/relatorioEvolucaoDivida_1794937268901_206609.java 
2026-11-17T17:41:09.1795840Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1796074Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1796317Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1796550Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1796774Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1797030Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1797263Z 	at jdk.internal.reflect.GeneratedMethodAccessor27.invoke(Unknown Source)
2026-11-17T17:41:09.1797445Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1797661Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1797868Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1798086Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1798300Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1798519Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1798731Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1798935Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1799163Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1799364Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1799555Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1799718Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1799911Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1800104Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1800291Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1800511Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1800688Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1800884Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1801127Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1801401Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1801584Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1801784Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1801971Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1802181Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1802399Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1802628Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1802873Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1803096Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1803310Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1803518Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1803734Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1804035Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1804237Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1804434Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1804626Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1804818Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1805018Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1805189Z 	... 37 more
2026-11-17T17:41:09.1805416Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1805591Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1805739Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1805929Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1806117Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1806267Z 	... 41 more
2026-11-17T17:41:09.1806307Z 
2026-11-17T17:41:09.1806654Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPlanilhaEvolucaoDivida/subRelatorioEvolucaoDivida.jasper] -- Time elapsed: 0.017 s <<< ERROR!
2026-11-17T17:41:09.1807054Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioEvolucaoDivida_1794937268923_556901.java 
2026-11-17T17:41:09.1807301Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1807551Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1807792Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1808022Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1808246Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1808486Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1808790Z 	at jdk.internal.reflect.GeneratedMethodAccessor27.invoke(Unknown Source)
2026-11-17T17:41:09.1809001Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1809222Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1809395Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1809614Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1809833Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1810048Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1810253Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1810456Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1810686Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1810899Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1811154Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1811357Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1811521Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1811754Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1811946Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1812131Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1812306Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1812515Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1812709Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1812903Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1813096Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1813289Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1813447Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1813649Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1813872Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1814095Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1814337Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1814555Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1814776Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1814985Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1815190Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1815476Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1815645Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1815845Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1816058Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1816250Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1816452Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1816626Z 	... 37 more
2026-11-17T17:41:09.1816876Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1817049Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1817227Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1817383Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1817581Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1817737Z 	... 41 more
2026-11-17T17:41:09.1817824Z 
2026-11-17T17:41:09.1818139Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPlanilhaEvolucaoDivida/subRelatorioEvolucaoDividaAmortiz.jasper] -- Time elapsed: 0.017 s <<< ERROR!
2026-11-17T17:41:09.1818532Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioEvolucaoDivida_1794937268941_177756.java 
2026-11-17T17:41:09.1818784Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1819024Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1819263Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1819494Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1819730Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1820000Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1820233Z 	at jdk.internal.reflect.GeneratedMethodAccessor27.invoke(Unknown Source)
2026-11-17T17:41:09.1820444Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1820659Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1820861Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1821136Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1821333Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1821559Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1821764Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1821970Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1822197Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1822401Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1822591Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1822787Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1822988Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1823179Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1823340Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1823540Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1823717Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1823918Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1824114Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1824310Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1824506Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1824707Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1824934Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1825106Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1825324Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1825551Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1825781Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1825996Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1826208Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1826429Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1826635Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1826920Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1827121Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1827319Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1827474Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1827664Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1827866Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1828081Z 	... 37 more
2026-11-17T17:41:09.1828294Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1828471Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1828652Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1828838Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1829029Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1829154Z 	... 41 more
2026-11-17T17:41:09.1829241Z 
2026-11-17T17:41:09.1829590Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPlanilhaEvolucaoDivida/subRelatorioEvolucaoDividaReneg.jasper] -- Time elapsed: 0.020 s <<< ERROR!
2026-11-17T17:41:09.1829986Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioEvolucaoDivida_1794937268963_373978.java 
2026-11-17T17:41:09.1830241Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1830496Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1830707Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1830941Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1831227Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1831552Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1831796Z 	at jdk.internal.reflect.GeneratedMethodAccessor27.invoke(Unknown Source)
2026-11-17T17:41:09.1832024Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1832242Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1832447Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1832667Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1832925Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1833141Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1833313Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1833518Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1833757Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1833957Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1834150Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1834347Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1834545Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1834741Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1834933Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1835126Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1835272Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1835470Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1835660Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1835855Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1836081Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1836273Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1836460Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1836667Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1836889Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1837084Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1837320Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1837540Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1837756Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1837986Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1838193Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1838488Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1838699Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1838890Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1839091Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1839266Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1839440Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1839613Z 	... 37 more
2026-11-17T17:41:09.1839828Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1840005Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1840197Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1840384Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1840572Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1840736Z 	... 41 more
2026-11-17T17:41:09.1840778Z 
2026-11-17T17:41:09.1841174Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPlanilhaEvolucaoDividaSeguradora/relatorioEvolucaoDividaSeguradora.jasper] -- Time elapsed: 0.043 s <<< ERROR!
2026-11-17T17:41:09.1841753Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/relatorioEvolucaoDividaSeguradora_1794937269007_101524.java 
2026-11-17T17:41:09.1842006Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1842251Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1842495Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1842725Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1842953Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1843212Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1843438Z 	at jdk.internal.reflect.GeneratedMethodAccessor27.invoke(Unknown Source)
2026-11-17T17:41:09.1843621Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1843840Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1844047Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1844312Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1844532Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1844753Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1844956Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1845179Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1845418Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1845620Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1845782Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1845984Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1846180Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1846377Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1846567Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1846750Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1846941Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1847125Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1847328Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1847490Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1847685Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1847879Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1848129Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1848333Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1848554Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1848794Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1849012Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1849228Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1849510Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1849730Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1849905Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1850190Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1850391Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1850589Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1850788Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1850966Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1851234Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1851411Z 	... 37 more
2026-11-17T17:41:09.1851639Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1851784Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1851967Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1852155Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1852345Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1852544Z 	... 41 more
2026-11-17T17:41:09.1852619Z 
2026-11-17T17:41:09.1852975Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPlanilhaEvolucaoDividaSeguradora/subRelatorioEvolucaoDividaSeguradora.jasper] -- Time elapsed: 0.009 s <<< ERROR!
2026-11-17T17:41:09.1853390Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioEvolucaoDividaSeguradora_1794937269019_961036.java 
2026-11-17T17:41:09.1853658Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1853893Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1854136Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1854370Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1854598Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1854858Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1855077Z 	at jdk.internal.reflect.GeneratedMethodAccessor27.invoke(Unknown Source)
2026-11-17T17:41:09.1855299Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1855516Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1855689Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1855911Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1856132Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1856350Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1856557Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1856970Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1857196Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1857409Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1857646Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1857840Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1858006Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1858200Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1858389Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1858572Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1858766Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1858961Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1859154Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1859345Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1859540Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1859705Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1859893Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1860118Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1860337Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1860584Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1860834Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1861105Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1861407Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1861620Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1861827Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1862120Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1862289Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1862491Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1862694Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1862874Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1863082Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1863262Z 	... 37 more
2026-11-17T17:41:09.1863480Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1863656Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1863840Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1864000Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1864203Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1864377Z 	... 41 more
2026-11-17T17:41:09.1864449Z 
2026-11-17T17:41:09.1864740Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPosicaoDivida/relatorioPosicaoDivida.jasper] -- Time elapsed: 0.040 s <<< ERROR!
2026-11-17T17:41:09.1865126Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida_1794937269059_342914.java 
2026-11-17T17:41:09.1865377Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1865613Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1865852Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1866141Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1866372Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1866629Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1866853Z 	at jdk.internal.reflect.GeneratedMethodAccessor27.invoke(Unknown Source)
2026-11-17T17:41:09.1867067Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1867280Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1867480Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1867730Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1867922Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1868137Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1868340Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1868561Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1868775Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1869017Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1869214Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1869420Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1869616Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1869815Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1869977Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1870158Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1870370Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1870557Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1870753Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1870951Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1871246Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1871443Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1871632Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1871805Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1872026Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1872273Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1872493Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1872709Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1872934Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1873145Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1873351Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1873643Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1873844Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1874009Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1874257Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1874436Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1874652Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1874858Z 	... 37 more
2026-11-17T17:41:09.1875810Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1876333Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1876561Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1876759Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1877063Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1877201Z 	... 41 more
2026-11-17T17:41:09.1877280Z 
2026-11-17T17:41:09.1877771Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPosicaoDivida/relatorioPosicaoDividaSeguradora.jasper] -- Time elapsed: 0.022 s <<< ERROR!
2026-11-17T17:41:09.1878177Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDividaSeguradora_1794937269086_343461.java 
2026-11-17T17:41:09.1878434Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1878645Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1879086Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1879330Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1879564Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1879864Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1880111Z 	at jdk.internal.reflect.GeneratedMethodAccessor27.invoke(Unknown Source)
2026-11-17T17:41:09.1880333Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1880553Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1880763Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1880990Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1881327Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1881547Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1881724Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1881965Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1882183Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1882387Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1882584Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1882785Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1882986Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1883182Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1883375Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1883529Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1883732Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1883925Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1884263Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1884526Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1884723Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1884917Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1885106Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1885316Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1885868Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1886100Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1886326Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1886552Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1886775Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1886990Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1887199Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1887535Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1887798Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1888013Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1888206Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1888355Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1888563Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1888744Z 	... 37 more
2026-11-17T17:41:09.1888978Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1889170Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1889357Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1889556Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1889874Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1890038Z 	... 41 more
2026-11-17T17:41:09.1890080Z 
2026-11-17T17:41:09.1890413Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/evolucaoDividaNCE/relatorioEvolucaoDividaNCE.jasper] -- Time elapsed: 0.024 s <<< ERROR!
2026-11-17T17:41:09.1890811Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/relatorioEvolucaoDividaNCE_1794937269112_828347.java 
2026-11-17T17:41:09.1891186Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1891460Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1891703Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1891935Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1892188Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1892464Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1892690Z 	at jdk.internal.reflect.GeneratedMethodAccessor27.invoke(Unknown Source)
2026-11-17T17:41:09.1892871Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1893146Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1893367Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1893592Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1893819Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1894038Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1894339Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1894549Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1894763Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1894976Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1895143Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1895345Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1895943Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1896256Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1896471Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1896764Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1897114Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1897322Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1897526Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1897732Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1897903Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1898111Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1898305Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1898512Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1898762Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1898992Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1899230Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1899447Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1899664Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1899873Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1900050Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1900434Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1900675Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1900890Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1901239Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1901428Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1901644Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1901819Z 	... 37 more
2026-11-17T17:41:09.1902048Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1902201Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1902387Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1902640Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1902865Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1903024Z 	... 41 more
2026-11-17T17:41:09.1903067Z 
2026-11-17T17:41:09.1903385Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/simularPrestacoes/simularPrestacoes.jasper] -- Time elapsed: 0.016 s <<< ERROR!
2026-11-17T17:41:09.1903769Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/simularPrestacoes_1794937269130_982546.java 
2026-11-17T17:41:09.1904022Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:41:09.1904261Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:41:09.1904503Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:41:09.1904743Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:41:09.1904997Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:41:09.1905244Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:41:09.1905471Z 	at jdk.internal.reflect.GeneratedMethodAccessor27.invoke(Unknown Source)
2026-11-17T17:41:09.1905724Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.1905940Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.1906116Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.1906338Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.1906560Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.1906790Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.1907012Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.1907218Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.1907519Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.1907725Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1907916Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1908131Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1908299Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1908495Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1908691Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1908884Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.1909075Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.1909262Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.1909455Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.1909650Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.1909847Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.1910008Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.1910689Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.1910937Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.1911306Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.1911610Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.1911840Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.1912064Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.1912294Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.1912502Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.1912715Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.1912992Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1913208Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:41:09.1913423Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:41:09.1913620Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:41:09.1913801Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:41:09.1914010Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:41:09.1914188Z 	... 37 more
2026-11-17T17:41:09.1914408Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:41:09.1914586Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:41:09.1914820Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:41:09.1914978Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:41:09.1915191Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:41:09.1915348Z 	... 41 more
2026-11-17T17:41:09.1915419Z 
2026-11-17T17:41:09.1915533Z [INFO] Running br.gov.caixa.siemp.relatorios.ExportacaoPdfTest
2026-11-17T17:41:09.7385007Z [ERROR] Tests run: 6, Failures: 0, Errors: 6, Skipped: 0, Time elapsed: 0.586 s <<< FAILURE! -- in br.gov.caixa.siemp.relatorios.ExportacaoPdfTest
2026-11-17T17:41:09.7388915Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[nce: 0 registros] -- Time elapsed: 0.194 s <<< ERROR!
2026-11-17T17:41:09.7389379Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:41:09.7389633Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:41:09.7389856Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:41:09.7390088Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:41:09.7390367Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:41:09.7390611Z 	at net.sf.jasperreports.engine.fill.JRFillTextField.prepare(JRFillTextField.java:554)
2026-11-17T17:41:09.7390865Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:41:09.7391323Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:41:09.7391538Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:41:09.7391758Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:41:09.7391995Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:164)
2026-11-17T17:41:09.7392230Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:41:09.7392442Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:41:09.7392613Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:41:09.7392837Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:41:09.7393275Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:41:09.7393550Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.7393773Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.7394093Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.7394331Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.7394541Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.7394766Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.7394986Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.7395208Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.7395385Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.7395612Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.7395828Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.7396031Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.7396313Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.7396517Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.7396716Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.7396918Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.7397135Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.7397338Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.7397490Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.7397708Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.7397914Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.7398112Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.7398311Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.7398514Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.7398710Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.7398915Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.7399144Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.7399409Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.7399601Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.7399826Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.7400050Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.7400260Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.7400469Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.7400550Z 
2026-11-17T17:41:09.7400882Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[nce: 1 registros] -- Time elapsed: 0.014 s <<< ERROR!
2026-11-17T17:41:09.7401307Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:41:09.7401592Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:41:09.7401849Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:41:09.7402076Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:41:09.7402311Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:41:09.7402614Z 	at net.sf.jasperreports.engine.fill.JRFillTextField.prepare(JRFillTextField.java:554)
2026-11-17T17:41:09.7402853Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:41:09.7403077Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:41:09.7403291Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:41:09.7403473Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:41:09.7403910Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReportStart(JRVerticalFiller.java:262)
2026-11-17T17:41:09.7404177Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:128)
2026-11-17T17:41:09.7404397Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:41:09.7404604Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:41:09.7404811Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:41:09.7405035Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:41:09.7405296Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:41:09.7405532Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.7405749Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.7406007Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.7406223Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.7406432Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.7406651Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.7406874Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.7407097Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.7407302Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.7407475Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.7407691Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.7407934Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.7408130Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.7408326Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.7408524Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.7408732Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.7408930Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.7409115Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.7409294Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.7409448Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.7409660Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.7409885Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.7410143Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.7410348Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.7410540Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.7410741Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.7410960Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.7411303Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.7411511Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.7411747Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.7411964Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.7412175Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.7412393Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.7412472Z 
2026-11-17T17:41:09.7412785Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[nce: 100 registros] -- Time elapsed: 0.051 s <<< ERROR!
2026-11-17T17:41:09.7413204Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:41:09.7413480Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:41:09.7413704Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:41:09.7414013Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:41:09.7414249Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:41:09.7414491Z 	at net.sf.jasperreports.engine.fill.JRFillTextField.prepare(JRFillTextField.java:554)
2026-11-17T17:41:09.7414722Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:41:09.7414943Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:41:09.7415145Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:41:09.7415468Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:41:09.7415770Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReportStart(JRVerticalFiller.java:262)
2026-11-17T17:41:09.7416001Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:128)
2026-11-17T17:41:09.7416237Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:41:09.7416462Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:41:09.7416668Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:41:09.7416888Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:41:09.7417139Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:41:09.7417373Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.7417589Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.7417872Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.7418181Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.7418361Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.7418728Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.7418948Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.7419167Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.7419371Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.7419584Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.7419801Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.7420011Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.7420257Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.7420453Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.7420621Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.7420823Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.7421137Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.7421342Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.7421528Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.7421717Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.7421973Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.7422186Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.7422382Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.7422543Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.7422735Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.7422938Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.7423160Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.7423387Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.7423618Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.7423868Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.7424182Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.7424391Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.7424600Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.7424683Z 
2026-11-17T17:41:09.7425004Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[rural: 0 registros] -- Time elapsed: 0.028 s <<< ERROR!
2026-11-17T17:41:09.7425356Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:41:09.7425584Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:41:09.7425814Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:41:09.7426169Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:41:09.7426369Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:41:09.7426621Z 	at net.sf.jasperreports.engine.fill.JRFillStaticText.prepare(JRFillStaticText.java:183)
2026-11-17T17:41:09.7426858Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:41:09.7427137Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:41:09.7427343Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:41:09.7427557Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:41:09.7427795Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReportStart(JRVerticalFiller.java:262)
2026-11-17T17:41:09.7428019Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:128)
2026-11-17T17:41:09.7428236Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:41:09.7428457Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:41:09.7428662Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:41:09.7428842Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:41:09.7429091Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:41:09.7429320Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.7429544Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.7429785Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.7430034Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.7430240Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.7430481Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.7430700Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.7430916Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.7431203Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.7431378Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.7431596Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.7431799Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.7431995Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.7432191Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.7432407Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.7432607Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.7432797Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.7432989Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.7433173Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.7433327Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.7433527Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.7433802Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.7434077Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.7434297Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.7434499Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.7434713Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.7434936Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.7435162Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.7435435Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.7435623Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.7435840Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.7436048Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.7436272Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.7436397Z 
2026-11-17T17:41:09.7436676Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[rural: 1 registros] -- Time elapsed: 0.018 s <<< ERROR!
2026-11-17T17:41:09.7437022Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:41:09.7437251Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:41:09.7437474Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:41:09.7437694Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:41:09.7437917Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:41:09.7438148Z 	at net.sf.jasperreports.engine.fill.JRFillStaticText.prepare(JRFillStaticText.java:183)
2026-11-17T17:41:09.7438396Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:41:09.7438667Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:41:09.7438869Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:41:09.7439183Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:41:09.7439379Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReportStart(JRVerticalFiller.java:262)
2026-11-17T17:41:09.7439606Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:128)
2026-11-17T17:41:09.7439816Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:41:09.7440029Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:41:09.7440233Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:41:09.7440461Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:41:09.7440711Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:41:09.7440953Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.7441560Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.7441871Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.7442093Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.7442266Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.7442488Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.7442705Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.7442949Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.7443166Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.7443376Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.7443597Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.7443902Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.7444122Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.7444318Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.7444487Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.7444684Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.7444903Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.7445089Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.7445271Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.7445459Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.7445658Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.7445855Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.7446049Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.7446244Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.7446400Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.7446627Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.7446848Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.7447121Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.7447339Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.7447559Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.7447777Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.7447987Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.7448198Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.7448280Z 
2026-11-17T17:41:09.7448611Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[rural: 100 registros] -- Time elapsed: 0.281 s <<< ERROR!
2026-11-17T17:41:09.7448956Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:41:09.7449252Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:41:09.7449551Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:41:09.7449799Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:41:09.7450106Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:41:09.7450395Z 	at net.sf.jasperreports.engine.fill.JRFillStaticText.prepare(JRFillStaticText.java:183)
2026-11-17T17:41:09.7450728Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:41:09.7451110Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:41:09.7451452Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:41:09.7451782Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:41:09.7452104Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReportStart(JRVerticalFiller.java:262)
2026-11-17T17:41:09.7452421Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:128)
2026-11-17T17:41:09.7452711Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:41:09.7453003Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:41:09.7453410Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:41:09.7453700Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:41:09.7454004Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:41:09.7454281Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:41:09.7454507Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:41:09.7454747Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:41:09.7454963Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:41:09.7455171Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:41:09.7455409Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:41:09.7455631Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:41:09.7455849Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:41:09.7456073Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:41:09.7456279Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:41:09.7456542Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:41:09.7456882Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.7457134Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.7457343Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.7457541Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.7457742Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.7457937Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.7458144Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:41:09.7458395Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:41:09.7458552Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:41:09.7458751Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:41:09.7458964Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:41:09.7459166Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:41:09.7459366Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:41:09.7459560Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:41:09.7459767Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:41:09.7460005Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:41:09.7460229Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:41:09.7460469Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:41:09.7460654Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:41:09.7460883Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:41:09.7461211Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:41:09.7461428Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:41:09.7461542Z 
2026-11-17T17:41:09.7461666Z [INFO] Running br.gov.caixa.siemp.relatorios.RelatorioPosicaoDividaCalculatorTest
2026-11-17T17:41:10.4382442Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:235: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.4382754Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.4382940Z                                             ^
2026-11-17T17:41:10.4383288Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:245: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.4383507Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.4383641Z                                             ^
2026-11-17T17:41:10.4383933Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:255: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.4384141Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:41:10.4384392Z                                             ^
2026-11-17T17:41:10.4384686Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:270: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.4384890Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:41:10.4385032Z                                             ^
2026-11-17T17:41:10.4385335Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:365: warning: [removal] Boolean(boolean) in Boolean has been deprecated and marked for removal
2026-11-17T17:41:10.4385817Z                 value = (java.lang.Boolean)(new Boolean(((java.lang.String)field_nuParcela.getValue()) != null));
2026-11-17T17:41:10.4385989Z                                             ^
2026-11-17T17:41:10.4386283Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:370: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.4386533Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:41:10.4386650Z                                             ^
2026-11-17T17:41:10.4386938Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:380: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.4387264Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.4387490Z                                             ^
2026-11-17T17:41:10.4387783Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:415: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.4387995Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.4388133Z                                             ^
2026-11-17T17:41:10.4388413Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:420: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.4388636Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.4388777Z                                             ^
2026-11-17T17:41:10.4389024Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:445: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.4389238Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.4389380Z                                             ^
2026-11-17T17:41:10.4389657Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:450: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.4389862Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:41:10.4390083Z                                             ^
2026-11-17T17:41:10.5375522Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:503: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5375892Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.5376302Z                                             ^
2026-11-17T17:41:10.5376619Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:513: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5376843Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.5376996Z                                             ^
2026-11-17T17:41:10.5377257Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:523: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5377649Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:41:10.5377760Z                                             ^
2026-11-17T17:41:10.5378046Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:538: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5378267Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:41:10.5378427Z                                             ^
2026-11-17T17:41:10.5378717Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:633: warning: [removal] Boolean(boolean) in Boolean has been deprecated and marked for removal
2026-11-17T17:41:10.5378959Z                 value = (java.lang.Boolean)(new Boolean(((java.lang.String)field_nuParcela.getOldValue()) != null));
2026-11-17T17:41:10.5379136Z                                             ^
2026-11-17T17:41:10.5379503Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:638: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5379749Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:41:10.5379892Z                                             ^
2026-11-17T17:41:10.5380194Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:648: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5380374Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.5380521Z                                             ^
2026-11-17T17:41:10.5380801Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:683: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5381094Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.5381246Z                                             ^
2026-11-17T17:41:10.5381533Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:688: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5381756Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.5381910Z                                             ^
2026-11-17T17:41:10.5382275Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:713: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5382496Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.5382633Z                                             ^
2026-11-17T17:41:10.5382881Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:718: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5383092Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:41:10.5383233Z                                             ^
2026-11-17T17:41:10.5383545Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:771: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5383768Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.5383920Z                                             ^
2026-11-17T17:41:10.5384198Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:781: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5384449Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.5384588Z                                             ^
2026-11-17T17:41:10.5384867Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:791: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5385070Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:41:10.5385181Z                                             ^
2026-11-17T17:41:10.5385455Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:806: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5385688Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:41:10.5385830Z                                             ^
2026-11-17T17:41:10.5386117Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:901: warning: [removal] Boolean(boolean) in Boolean has been deprecated and marked for removal
2026-11-17T17:41:10.5386356Z                 value = (java.lang.Boolean)(new Boolean(((java.lang.String)field_nuParcela.getValue()) != null));
2026-11-17T17:41:10.5386525Z                                             ^
2026-11-17T17:41:10.5386804Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:906: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5387009Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:41:10.5387190Z                                             ^
2026-11-17T17:41:10.5387485Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:916: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5387685Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.5387792Z                                             ^
2026-11-17T17:41:10.5388071Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:951: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5388268Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.5388405Z                                             ^
2026-11-17T17:41:10.5388681Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:956: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5388901Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.5389036Z                                             ^
2026-11-17T17:41:10.5389331Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:981: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5389530Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:41:10.5389665Z                                             ^
2026-11-17T17:41:10.5389913Z /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida.java:986: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:41:10.5390114Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:41:10.5390249Z                                             ^
2026-11-17T17:41:10.5390390Z 33 warnings
2026-11-17T17:41:10.5457699Z [INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.803 s -- in br.gov.caixa.siemp.relatorios.RelatorioPosicaoDividaCalculatorTest
2026-11-17T17:41:10.5458082Z [INFO] Running br.gov.caixa.siemp.apresentacao.evolucao.estornarpagamento.EstornarPagamentoACTTest
2026-11-17T17:41:10.5754640Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.5755645Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:41:10.5756012Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.5757523Z GRAVE: falha na procedure
2026-11-17T17:41:10.5757759Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.5757945Z GRAVE: Erro ao fechar PreparedStatement do SIRIC: 
2026-11-17T17:41:10.5758147Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.5758308Z GRAVE: falha ao fechar
2026-11-17T17:41:10.5758442Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.5758735Z GRAVE: Erro ao fechar conexao com o SIRIC: 
2026-11-17T17:41:10.5758915Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.5759095Z GRAVE: falha ao fechar
2026-11-17T17:41:10.6638686Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6638936Z GRAVE: Erro de SQL: jdbc/SybaseSiempDS
2026-11-17T17:41:10.6782667Z [INFO] Tests run: 26, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.130 s -- in br.gov.caixa.siemp.apresentacao.evolucao.estornarpagamento.EstornarPagamentoACTTest
2026-11-17T17:41:10.6783009Z [INFO] Running br.gov.caixa.siemp.apresentacao.evolucao.SiricEstornoTest
2026-11-17T17:41:10.6795565Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6796012Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:41:10.6796205Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6796343Z GRAVE: falha na execucao
2026-11-17T17:41:10.6796519Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6796953Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:41:10.6797137Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6797304Z GRAVE: falha na execucao
2026-11-17T17:41:10.6815825Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6817190Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:41:10.6817603Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6817825Z GRAVE: falha na execucao
2026-11-17T17:41:10.6818020Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6818251Z GRAVE: Erro ao fechar PreparedStatement do SIRIC: 
2026-11-17T17:41:10.6818458Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6818661Z GRAVE: falha ao fechar statement
2026-11-17T17:41:10.6818852Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6819013Z GRAVE: Erro ao fechar conexao com o SIRIC: 
2026-11-17T17:41:10.6819226Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6819431Z GRAVE: falha ao fechar conexao
2026-11-17T17:41:10.6819617Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6819869Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:41:10.6820146Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6820338Z GRAVE: falha na execucao
2026-11-17T17:41:10.6820524Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6820688Z GRAVE: Erro ao fechar PreparedStatement do SIRIC: 
2026-11-17T17:41:10.6820885Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6821255Z GRAVE: falha ao fechar statement
2026-11-17T17:41:10.6821586Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6821822Z GRAVE: Erro ao fechar conexao com o SIRIC: 
2026-11-17T17:41:10.6822017Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6822195Z GRAVE: falha ao fechar conexao
2026-11-17T17:41:10.6842500Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6842991Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:41:10.6843211Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6843366Z GRAVE: falha na preparacao
2026-11-17T17:41:10.6843760Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6844144Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:41:10.6844346Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6844523Z GRAVE: falha na preparacao
2026-11-17T17:41:10.6850510Z [INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.005 s -- in br.gov.caixa.siemp.apresentacao.evolucao.SiricEstornoTest
2026-11-17T17:41:10.6850835Z [INFO] Running br.gov.caixa.siemp.apresentacao.evolucao.estornarconcessaoemprestimo.EstornarConcessaoEmprestimoACTTest
2026-11-17T17:41:10.6914824Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6915297Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:41:10.6915514Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6915873Z GRAVE: falha na procedure
2026-11-17T17:41:10.6916122Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6916349Z GRAVE: Erro ao fechar PreparedStatement do SIRIC: 
2026-11-17T17:41:10.6916555Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6916744Z GRAVE: falha ao fechar
2026-11-17T17:41:10.6916929Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6917129Z GRAVE: Erro ao fechar conexao com o SIRIC: 
2026-11-17T17:41:10.6917322Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6917668Z GRAVE: falha ao fechar
2026-11-17T17:41:10.6939023Z nov. 17, 2026 2:41:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:41:10.6939222Z GRAVE: Erro de SQL: jdbc/SybaseSiempDS
2026-11-17T17:41:10.7026994Z [INFO] Tests run: 11, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.015 s -- in br.gov.caixa.siemp.apresentacao.evolucao.estornarconcessaoemprestimo.EstornarConcessaoEmprestimoACTTest
2026-11-17T17:41:10.7027624Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaTabelaDeTACDeConvenio.ConsultaTabelaDeTACDeConvenioHelpersTest
2026-11-17T17:41:10.7042609Z [INFO] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.001 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaTabelaDeTACDeConvenio.ConsultaTabelaDeTACDeConvenioHelpersTest
2026-11-17T17:41:10.7043180Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioParametroHelperTest
2026-11-17T17:41:10.7055433Z [INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioParametroHelperTest
2026-11-17T17:41:10.7056118Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioHelperTest
2026-11-17T17:41:10.7076001Z [INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioHelperTest
2026-11-17T17:41:10.7076467Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioHistoricosHelperTest
2026-11-17T17:41:10.7122701Z [INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.001 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioHistoricosHelperTest
2026-11-17T17:41:10.7123253Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaConveniosExtratoAtraso.ConsultaConveniosExtratoAtrasoHelperColecoesTest
2026-11-17T17:41:10.7123795Z [INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaConveniosExtratoAtraso.ConsultaConveniosExtratoAtrasoHelperColecoesTest
2026-11-17T17:41:10.7124150Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaMovimentoDeAcertoDoConvenioNovo.ConsultaMovimentoDeAcertoDoConvenioHelperTest
2026-11-17T17:41:10.7124820Z [INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaMovimentoDeAcertoDoConvenioNovo.ConsultaMovimentoDeAcertoDoConvenioHelperTest
2026-11-17T17:41:10.7125158Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultarComiteDeAutorizacoes.ConsultarComiteDeAutorizacoesHelpersTest
2026-11-17T17:41:10.7141268Z [INFO] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultarComiteDeAutorizacoes.ConsultarComiteDeAutorizacoesHelpersTest
2026-11-17T17:41:10.7141748Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaTabelaDeTaxasDeConvenio.ConsultaTabelaDeTaxasDeConvenioHelpersTest
2026-11-17T17:41:10.7166723Z [INFO] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.002 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaTabelaDeTaxasDeConvenio.ConsultaTabelaDeTaxasDeConvenioHelpersTest
2026-11-17T17:41:10.7167155Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultarDadosConvenio.ConsultarDadosConvenioHelpersTest
2026-11-17T17:41:10.7205677Z [INFO] Tests run: 10, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.002 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultarDadosConvenio.ConsultarDadosConvenioHelpersTest
2026-11-17T17:41:10.7206174Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.ajustaExtratoDoConvenio.AjustaExtratoDoConvenioTotalizadorHelperTest
2026-11-17T17:41:10.7217747Z [INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in br.gov.caixa.siemp.apresentacao.consignacao.ajustaExtratoDoConvenio.AjustaExtratoDoConvenioTotalizadorHelperTest
2026-11-17T17:41:10.7218211Z [INFO] Running br.gov.caixa.siemp.creditorural.bndes.CobrancaBNDESActionTest
2026-11-17T17:41:10.7304713Z [INFO] Tests run: 6, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.007 s -- in br.gov.caixa.siemp.creditorural.bndes.CobrancaBNDESActionTest
2026-11-17T17:41:10.7305165Z [INFO] Running br.gov.caixa.siemp.creditorural.extrato.ExtratoCreditoRuralActionTest
2026-11-17T17:41:10.7337742Z [INFO] Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.001 s -- in br.gov.caixa.siemp.creditorural.extrato.ExtratoCreditoRuralActionTest
2026-11-17T17:41:10.7338189Z [INFO] Running teste.br.gov.caixa.siemp.comum.apresentacao.testeerromultiplo.TesteErroMultiploActionTest
2026-11-17T17:41:10.7349958Z [INFO] Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in teste.br.gov.caixa.siemp.comum.apresentacao.testeerromultiplo.TesteErroMultiploActionTest
2026-11-17T17:41:10.8010555Z [INFO] 
2026-11-17T17:41:10.8010893Z [INFO] Results:
2026-11-17T17:41:10.8011244Z [INFO] 
2026-11-17T17:41:10.8011854Z [ERROR] Errors: 
2026-11-17T17:41:10.8012446Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:41:10.8012900Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:41:10.8013299Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:41:10.8013703Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:41:10.8014133Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:41:10.8014599Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:41:10.8015317Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarParametrosDoConvenio_1794937268241_468811.java 
2026-11-17T17:41:10.8015775Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarParametrosDoConvenioReport_1794937268352_668265.java 
2026-11-17T17:41:10.8016231Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarTabelaDeTACDoConvenio_1794937268457_629512.java 
2026-11-17T17:41:10.8016698Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarTabelaDeTACDoConvenioNovo_1794937268517_732892.java 
2026-11-17T17:41:10.8017180Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarTabelaDeTACDoConvenioSubReport_1794937268580_79752.java 
2026-11-17T17:41:10.8017630Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarTabelaDeTaxasDoConvenio_1794937268633_629952.java 
2026-11-17T17:41:10.8018098Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarTabelaDeTaxasDoConvenioNovo_1794937268679_570157.java 
2026-11-17T17:41:10.8018680Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/consultarTabelaDeTaxasDoConvenioSubReport_1794937268703_26467.java 
2026-11-17T17:41:10.8019125Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/relatorioExtratoCreditoRural_1794937268740_190611.java 
2026-11-17T17:41:10.8019557Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioExtrato_1794937268754_393449.java 
2026-11-17T17:41:10.8019982Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioLiberacoes_1794937268765_617251.java 
2026-11-17T17:41:10.8020432Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioOcorrencias_1794937268775_943016.java 
2026-11-17T17:41:10.8020860Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioPosicaoDivida_1794937268787_695668.java 
2026-11-17T17:41:10.8021375Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioProAgro_1794937268800_111797.java 
2026-11-17T17:41:10.8021814Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioReembolsos_1794937268810_930945.java 
2026-11-17T17:41:10.8022250Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioReembolsosVencidos_1794937268823_877128.java 
2026-11-17T17:41:10.8022687Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/relatorioEvolucaoDivida_1794937268901_206609.java 
2026-11-17T17:41:10.8023152Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioEvolucaoDivida_1794937268923_556901.java 
2026-11-17T17:41:10.8023591Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioEvolucaoDivida_1794937268941_177756.java 
2026-11-17T17:41:10.8024012Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioEvolucaoDivida_1794937268963_373978.java 
2026-11-17T17:41:10.8024453Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/relatorioEvolucaoDividaSeguradora_1794937269007_101524.java 
2026-11-17T17:41:10.8024899Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/subRelatorioEvolucaoDividaSeguradora_1794937269019_961036.java 
2026-11-17T17:41:10.8025367Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDivida_1794937269059_342914.java 
2026-11-17T17:41:10.8025800Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/relatorioPosicaoDividaSeguradora_1794937269086_343461.java 
2026-11-17T17:41:10.8026265Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/relatorioEvolucaoDividaNCE_1794937269112_828347.java 
2026-11-17T17:41:10.8026699Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/6/s/siemp-web/simularPrestacoes_1794937269130_982546.java 
2026-11-17T17:41:10.8026911Z [INFO] 
2026-11-17T17:41:10.8027061Z [ERROR] Tests run: 403, Failures: 0, Errors: 32, Skipped: 13
2026-11-17T17:41:10.8027175Z [INFO] 
2026-11-17T17:41:10.8041152Z [INFO] ------------------------------------------------------------------------
2026-11-17T17:41:10.8041356Z [INFO] Reactor Summary for siemp application 14.37.0.6:
2026-11-17T17:41:10.8041525Z [INFO] 
2026-11-17T17:41:10.8045172Z [INFO] siemp application .................................. SUCCESS [  0.146 s]
2026-11-17T17:41:10.8045581Z [INFO] SIEMP Web module ................................... FAILURE [ 13.248 s]
2026-11-17T17:41:10.8046131Z [INFO] SIEMP EAR module ................................... SKIPPED
2026-11-17T17:41:10.8046717Z [INFO] ------------------------------------------------------------------------
2026-11-17T17:41:10.8047003Z [INFO] BUILD FAILURE
2026-11-17T17:41:10.8047418Z [INFO] ------------------------------------------------------------------------
2026-11-17T17:41:10.8047988Z [INFO] Total time:  13.482 s
2026-11-17T17:41:10.8048587Z [INFO] Finished at: 2026-11-17T14:41:10-03:00
2026-11-17T17:41:10.8049018Z [INFO] ------------------------------------------------------------------------
2026-11-17T17:41:10.8054645Z [ERROR] Failed to execute goal org.apache.maven.plugins:maven-surefire-plugin:3.2.5:test (default-test) on project siemp-web: 
2026-11-17T17:41:10.8054963Z [ERROR] 
2026-11-17T17:41:10.8055245Z [ERROR] Please refer to /opt/ads-agent/_work/6/s/siemp-web/target/surefire-reports for the individual test results.
2026-11-17T17:41:10.8055544Z [ERROR] Please refer to dump files (if any exist) [date].dump, [date]-jvmRun[N].dump and [date].dumpstream.
2026-11-17T17:41:10.8055748Z [ERROR] -> [Help 1]
2026-11-17T17:41:10.8055886Z [ERROR] 
2026-11-17T17:41:10.8056196Z [ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
2026-11-17T17:41:10.8057059Z [ERROR] Re-run Maven using the -X switch to enable full debug logging.
2026-11-17T17:41:10.8057177Z [ERROR] 
2026-11-17T17:41:10.8057359Z [ERROR] For more information about the errors and possible solutions, please read the following articles:
2026-11-17T17:41:10.8057563Z [ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoFailureException
2026-11-17T17:41:10.8057721Z [ERROR] 
2026-11-17T17:41:10.8057878Z [ERROR] After correcting the problems, you can resume the build with the command
2026-11-17T17:41:10.8058097Z [ERROR]   mvn <args> -rf :siemp-web
2026-11-17T17:41:10.8995630Z The process '/opt/apache-maven/apache-maven-3.8.5/bin/mvn' failed with exit code 1
2026-11-17T17:41:10.8995984Z Could not retrieve code analysis results - Maven run failed.
2026-11-17T17:41:10.8998602Z ##[error]Build failed.
2026-11-17T17:41:10.9065270Z ##[section]Finishing: Maven
