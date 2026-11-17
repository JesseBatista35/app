Generating script.
========================== Starting Command Output ===========================
/usr/bin/bash /opt/ads-agent/_work/_temp/081f5572-fd7d-412a-86e9-138fbdd71315.sh
-rwxr-xr-x. 1 10940372 30000004 17000 set 12  2023 /usr/java/open-jdk-17.0.8/bin/javac
Finishing: Bash Script



2026-11-17T17:43:38.7186316Z ##[section]Starting: Maven
2026-11-17T17:43:38.7191935Z ==============================================================================
2026-11-17T17:43:38.7192023Z Task         : Maven
2026-11-17T17:43:38.7192107Z Description  : Build, test, and deploy with Apache Maven
2026-11-17T17:43:38.7192173Z Version      : 4.225.0
2026-11-17T17:43:38.7192262Z Author       : Microsoft Corporation
2026-11-17T17:43:38.7192317Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/build/maven
2026-11-17T17:43:38.7192385Z ==============================================================================
2026-11-17T17:43:39.3022731Z [command]/opt/apache-maven/apache-maven-3.8.5/bin/mvn -version
2026-11-17T17:43:39.3958764Z Apache Maven 3.8.5 (3599d3414f046de2324203b78ddcf9b5e4388aa0)
2026-11-17T17:43:39.3959326Z Maven home: /opt/apache-maven/apache-maven-3.8.5
2026-11-17T17:43:39.3959553Z Java version: 17.0.8, vendor: OpenLogic, runtime: /usr/java/open-jdk-17.0.8
2026-11-17T17:43:39.3959860Z Default locale: pt_BR, platform encoding: UTF-8
2026-11-17T17:43:39.3960287Z OS name: "linux", version: "5.18.5-100.fc35.x86_64", arch: "amd64", family: "unix"
2026-11-17T17:43:39.4139121Z [command]/opt/apache-maven/apache-maven-3.8.5/bin/mvn -f /opt/ads-agent/_work/29/s/pom.xml clean verify -Dversion.app= -U
2026-11-17T17:43:40.0490619Z [INFO] Scanning for projects...
2026-11-17T17:43:40.1510702Z [INFO] ------------------------------------------------------------------------
2026-11-17T17:43:40.1511580Z [INFO] Reactor Build Order:
2026-11-17T17:43:40.1511698Z [INFO] 
2026-11-17T17:43:40.1514954Z [INFO] siemp application                                                  [pom]
2026-11-17T17:43:40.1515498Z [INFO] SIEMP Web module                                                   [war]
2026-11-17T17:43:40.1518666Z [INFO] SIEMP EAR module                                                   [ear]
2026-11-17T17:43:40.1557494Z [INFO] 
2026-11-17T17:43:40.1558190Z [INFO] ----------------------< br.gov.caixa.siemp:siemp >----------------------
2026-11-17T17:43:40.1558762Z [INFO] Building siemp application 14.37.0.6                               [1/3]
2026-11-17T17:43:40.1559286Z [INFO] --------------------------------[ pom ]---------------------------------
2026-11-17T17:43:40.1968915Z [INFO] 
2026-11-17T17:43:40.1969642Z [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ siemp ---
2026-11-17T17:43:40.2321394Z [INFO] 
2026-11-17T17:43:40.2321965Z [INFO] --- jacoco-maven-plugin:0.8.13:prepare-agent (prepare-agent) @ siemp ---
2026-11-17T17:43:40.3089450Z [INFO] argLine set to -javaagent:/opt/ads-agent/cache-tools/.m2/repository/org/jacoco/org.jacoco.agent/0.8.13/org.jacoco.agent-0.8.13-runtime.jar=destfile=/opt/ads-agent/_work/29/s/target/jacoco.exec
2026-11-17T17:43:40.3089916Z [INFO] 
2026-11-17T17:43:40.3090177Z [INFO] --- jacoco-maven-plugin:0.8.13:report (generate-report) @ siemp ---
2026-11-17T17:43:40.3105917Z [INFO] Skipping JaCoCo execution due to missing execution data file.
2026-11-17T17:43:40.3107459Z [INFO] 
2026-11-17T17:43:40.3109024Z [INFO] --------------------< br.gov.caixa.siemp:siemp-web >--------------------
2026-11-17T17:43:40.3109191Z [INFO] Building SIEMP Web module 14.37.0.6                                [2/3]
2026-11-17T17:43:40.3109435Z [INFO] --------------------------------[ war ]---------------------------------
2026-11-17T17:43:40.8284770Z [INFO] 
2026-11-17T17:43:40.8285539Z [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ siemp-web ---
2026-11-17T17:43:40.8302912Z [INFO] 
2026-11-17T17:43:40.8303341Z [INFO] --- jacoco-maven-plugin:0.8.13:prepare-agent (prepare-agent) @ siemp-web ---
2026-11-17T17:43:40.8310930Z [INFO] argLine set to -javaagent:/opt/ads-agent/cache-tools/.m2/repository/org/jacoco/org.jacoco.agent/0.8.13/org.jacoco.agent-0.8.13-runtime.jar=destfile=/opt/ads-agent/_work/29/s/siemp-web/target/jacoco.exec
2026-11-17T17:43:40.8311748Z [INFO] 
2026-11-17T17:43:40.8312532Z [INFO] --- maven-resources-plugin:3.3.1:resources (default-resources) @ siemp-web ---
2026-11-17T17:43:40.8695641Z [INFO] Copying 6 resources from src/main/resources to target/classes
2026-11-17T17:43:40.9534401Z [INFO] Copying 682 resources from src/main/java to target/classes
2026-11-17T17:43:40.9995551Z [INFO] The encoding used to copy filtered properties files have not been set. This means that the same encoding will be used to copy filtered properties files as when copying other filtered resources. This might not be what you want! Run your build with --debug to see which files might be affected. Read more at https://maven.apache.org/plugins/maven-resources-plugin/examples/filtering-properties-files.html
2026-11-17T17:43:40.9996845Z [INFO] 
2026-11-17T17:43:40.9997151Z [INFO] --- maven-compiler-plugin:3.11.0:compile (default-compile) @ siemp-web ---
2026-11-17T17:43:41.1848521Z [INFO] Changes detected - recompiling the module! :source
2026-11-17T17:43:41.1923855Z [INFO] Compiling 2259 source files with javac [debug release 17] to target/classes
2026-11-17T17:43:48.6588416Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(288,23): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[288,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6597796Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(302,23): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[302,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6600392Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(310,21): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[310,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6601365Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[288,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6602267Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[302,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6602646Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[310,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6604733Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(318,21): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[318,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6607086Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(334,20): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[334,20] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6609384Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(342,21): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[342,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6611726Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(350,20): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[350,20] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6614401Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(361,21): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[361,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6617273Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(621,21): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[621,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6619649Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(629,23): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[629,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6621988Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(844,23): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[844,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6624561Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(964,35): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[964,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6627025Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java(95,28): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[95,28] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6629163Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java(106,24): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[106,24] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6632038Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java(608,85): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[608,85] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6634702Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java(608,36): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[608,36] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6637336Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/TratarTOForm.java(528,51): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/TratarTOForm.java:[528,51] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6640190Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java(558,51): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[558,51] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6642717Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java(601,85): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[601,85] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6645448Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java(601,36): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[601,36] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6648184Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterTabelaHelper.java(17,8): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterTabelaHelper.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6650747Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterSelectMultipleHelper.java(17,8): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterSelectMultipleHelper.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6653074Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/filtros/formatador/FormatadorDeRotulo.java(108,23): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/filtros/formatador/FormatadorDeRotulo.java:[108,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6655515Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(53,50): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[53,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6657936Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(70,50): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[70,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6658707Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[318,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6659091Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[334,20] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6659466Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[342,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6659863Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[350,20] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6660232Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[361,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6660806Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[621,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6661187Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[629,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6661563Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[844,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6662826Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[964,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6663195Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[95,28] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6663624Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[106,24] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6664045Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[608,85] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6664470Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[608,36] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6664902Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/TratarTOForm.java:[528,51] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6665339Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[558,51] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6665741Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[601,85] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6666152Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[601,36] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6666597Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterTabelaHelper.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6666968Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterSelectMultipleHelper.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6667365Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/filtros/formatador/FormatadorDeRotulo.java:[108,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6667768Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[53,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6668178Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[70,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6668609Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[121,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6669023Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[128,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6669448Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[134,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6669871Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[140,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6670334Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[145,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6670850Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[150,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6671324Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[155,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6671741Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[160,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6672153Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[166,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6672564Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[176,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6672975Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[182,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6673387Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[188,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6673820Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[356,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6674280Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[371,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6674724Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[386,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6675584Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[416,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6676023Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[431,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6676450Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[446,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6676879Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[462,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6677307Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[478,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6677762Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[520,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6678193Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[989,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6678602Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/FabricaDeCombos.java:[24,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6678958Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/IObjetoParaCombo.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6679312Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java:[203,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6679656Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java:[297,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6679999Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java:[24,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6680545Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/IObjetoParaComboComAtributos.java:[20,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6680994Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/fachada/SiempFacade.java:[22,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6681442Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/BusinessDelegate.java:[230,59] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6682132Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[76,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6682487Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[87,28] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6684784Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java(97,31): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[97,31] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6687360Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java(118,55): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[118,55] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6688051Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[97,31] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6688412Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[118,55] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6690846Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java(183,28): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[183,28] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6693309Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java(193,41): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[193,41] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6695553Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java(205,33): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[205,33] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6698072Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/persistencia/SiempDAOMainframe.java(142,59): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/persistencia/SiempDAOMainframe.java:[142,59] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6701077Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/XMLProgramAnalyzer.java(353,41): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/XMLProgramAnalyzer.java:[353,41] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6703871Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(89,109): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[89,109] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6704554Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[183,28] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6704931Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[193,41] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6705297Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[205,33] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6705710Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/persistencia/SiempDAOMainframe.java:[142,59] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6706219Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/XMLProgramAnalyzer.java:[353,41] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6706668Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[89,109] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6706914Z   cast to java.lang.Object for a varargs call
2026-11-17T17:43:48.6707154Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:43:48.6709128Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(97,108): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[97,108] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6712003Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(105,107): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[105,107] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6714490Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(112,110): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[112,110] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6716991Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(120,109): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[120,109] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6719411Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(129,108): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[129,108] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6724309Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(137,107): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[137,107] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6726524Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(145,110): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[145,110] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6729182Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(150,99): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[150,99] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6731920Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(164,94): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[164,94] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6734280Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(136,32): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[136,32] Double(java.lang.String) in java.lang.Double has been deprecated and marked for removal
2026-11-17T17:43:48.6736504Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(148,32): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[148,32] Float(java.lang.String) in java.lang.Float has been deprecated and marked for removal
2026-11-17T17:43:48.6739231Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(157,32): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[157,32] Long(java.lang.String) in java.lang.Long has been deprecated and marked for removal
2026-11-17T17:43:48.6742017Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(166,32): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[166,32] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6744714Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(180,32): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[180,32] Double(java.lang.String) in java.lang.Double has been deprecated and marked for removal
2026-11-17T17:43:48.6745433Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[97,108] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6745714Z   cast to java.lang.Object for a varargs call
2026-11-17T17:43:48.6745985Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:43:48.6746343Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[105,107] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6746621Z   cast to java.lang.Object for a varargs call
2026-11-17T17:43:48.6746858Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:43:48.6747210Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[112,110] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6747428Z   cast to java.lang.Object for a varargs call
2026-11-17T17:43:48.6747662Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:43:48.6748022Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[120,109] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6748257Z   cast to java.lang.Object for a varargs call
2026-11-17T17:43:48.6748458Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:43:48.6749062Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[129,108] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6749277Z   cast to java.lang.Object for a varargs call
2026-11-17T17:43:48.6749513Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:43:48.6749867Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[137,107] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6750095Z   cast to java.lang.Object for a varargs call
2026-11-17T17:43:48.6750329Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:43:48.6750745Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[145,110] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6750999Z   cast to java.lang.Object for a varargs call
2026-11-17T17:43:48.6751232Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:43:48.6751578Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[150,99] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6751794Z   cast to java.lang.Object for a varargs call
2026-11-17T17:43:48.6752021Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:43:48.6752332Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[164,94] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:43:48.6752544Z   cast to java.lang.Object for a varargs call
2026-11-17T17:43:48.6752779Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:43:48.6753150Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[136,32] Double(java.lang.String) in java.lang.Double has been deprecated and marked for removal
2026-11-17T17:43:48.6753578Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[148,32] Float(java.lang.String) in java.lang.Float has been deprecated and marked for removal
2026-11-17T17:43:48.6754273Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[157,32] Long(java.lang.String) in java.lang.Long has been deprecated and marked for removal
2026-11-17T17:43:48.6754737Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[166,32] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6755147Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[180,32] Double(java.lang.String) in java.lang.Double has been deprecated and marked for removal
2026-11-17T17:43:48.6757232Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(192,32): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[192,32] Float(java.lang.String) in java.lang.Float has been deprecated and marked for removal
2026-11-17T17:43:48.6759845Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(201,32): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[201,32] Long(java.lang.String) in java.lang.Long has been deprecated and marked for removal
2026-11-17T17:43:48.6762538Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(210,32): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[210,32] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6764901Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(34,41): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[34,41] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6767200Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(111,41): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[111,41] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6770356Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(122,36): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[122,36] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6773017Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(132,30): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[132,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6775369Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(143,30): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[143,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6777529Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(154,44): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[154,44] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6780208Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(165,36): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[165,36] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6783182Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(175,42): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[175,42] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6785695Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(187,25): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[187,25] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6787814Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(204,30): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[204,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6790176Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(214,30): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[214,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6792646Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(225,30): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[225,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6794748Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(236,30): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[236,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6797247Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(247,30): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[247,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6799577Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(257,30): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[257,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6802194Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(267,30): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[267,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6804271Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(278,30): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[278,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6806695Z ##[warning] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(288,30): warning :  /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[288,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6807428Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[192,32] Float(java.lang.String) in java.lang.Float has been deprecated and marked for removal
2026-11-17T17:43:48.6807847Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[201,32] Long(java.lang.String) in java.lang.Long has been deprecated and marked for removal
2026-11-17T17:43:48.6808266Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[210,32] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:43:48.6808658Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[34,41] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6809366Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[111,41] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6809728Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[122,36] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6810131Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[132,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6810561Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[143,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6810930Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[154,44] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6811289Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[165,36] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6811643Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[175,42] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6812001Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[187,25] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6812352Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[204,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6812704Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[214,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6813053Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[225,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6813422Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[236,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6813775Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[247,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6814130Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[257,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6814490Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[267,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6814836Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[278,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6815513Z [WARNING] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[288,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:43:48.6815865Z [INFO] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java: Some input files use or override a deprecated API.
2026-11-17T17:43:48.6816247Z [INFO] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java: Recompile with -Xlint:deprecation for details.
2026-11-17T17:43:48.6816653Z [INFO] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/persistencia/LoginDAO.java: Some input files additionally use or override a deprecated API that is marked for removal.
2026-11-17T17:43:48.6817024Z [INFO] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java: Some input files use unchecked or unsafe operations.
2026-11-17T17:43:48.6817420Z [INFO] /opt/ads-agent/_work/29/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java: Recompile with -Xlint:unchecked for details.
2026-11-17T17:43:48.6817619Z [INFO] 
2026-11-17T17:43:48.6817865Z [INFO] --- maven-resources-plugin:3.3.1:testResources (default-testResources) @ siemp-web ---
2026-11-17T17:43:48.6818131Z [INFO] Copying 1 resource from src/test/resources to target/test-classes
2026-11-17T17:43:48.6818317Z [INFO] 
2026-11-17T17:43:48.6818555Z [INFO] --- maven-compiler-plugin:3.11.0:testCompile (default-testCompile) @ siemp-web ---
2026-11-17T17:43:48.6818812Z [INFO] Changes detected - recompiling the module! :dependency
2026-11-17T17:43:48.6819082Z [INFO] Compiling 30 source files with javac [debug release 17] to target/test-classes
2026-11-17T17:43:49.0933827Z [INFO] /opt/ads-agent/_work/29/s/siemp-web/src/test/java/br/gov/caixa/siemp/apresentacao/consignacao/consultaTabelaDeTACDeConvenio/ConsultaTabelaDeTACDeConvenioHelpersTest.java: Some input files use or override a deprecated API.
2026-11-17T17:43:49.0934408Z [INFO] /opt/ads-agent/_work/29/s/siemp-web/src/test/java/br/gov/caixa/siemp/apresentacao/consignacao/consultaTabelaDeTACDeConvenio/ConsultaTabelaDeTACDeConvenioHelpersTest.java: Recompile with -Xlint:deprecation for details.
2026-11-17T17:43:49.0934962Z [INFO] /opt/ads-agent/_work/29/s/siemp-web/src/test/java/br/gov/caixa/siemp/comum/apresentacao/login/LoginMenuConsultasTest.java: /opt/ads-agent/_work/29/s/siemp-web/src/test/java/br/gov/caixa/siemp/comum/apresentacao/login/LoginMenuConsultasTest.java uses unchecked or unsafe operations.
2026-11-17T17:43:49.0935423Z [INFO] /opt/ads-agent/_work/29/s/siemp-web/src/test/java/br/gov/caixa/siemp/comum/apresentacao/login/LoginMenuConsultasTest.java: Recompile with -Xlint:unchecked for details.
2026-11-17T17:43:49.0935724Z [INFO] 
2026-11-17T17:43:49.0935958Z [INFO] --- maven-surefire-plugin:3.2.5:test (default-test) @ siemp-web ---
2026-11-17T17:43:49.2096072Z [INFO] Using auto detected provider org.apache.maven.surefire.junit4.JUnit4Provider
2026-11-17T17:43:49.2515009Z [INFO] 
2026-11-17T17:43:49.2515543Z [INFO] -------------------------------------------------------
2026-11-17T17:43:49.2515717Z [INFO]  T E S T S
2026-11-17T17:43:49.2516090Z [INFO] -------------------------------------------------------
2026-11-17T17:43:49.7423459Z [INFO] Running br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.atualizarvaloresnamatrizdeexcepcionacao.AtualizarValoresNaMatrizDeExcepcionacaoFormTest
2026-11-17T17:43:49.8131643Z [INFO] Tests run: 13, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.064 s -- in br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.atualizarvaloresnamatrizdeexcepcionacao.AtualizarValoresNaMatrizDeExcepcionacaoFormTest
2026-11-17T17:43:49.8132721Z [INFO] Running br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.manterpercentualdetaxasdejuros.CopiarEstruturaDeTabelaDeTaxasFormTest
2026-11-17T17:43:49.8172966Z [INFO] Tests run: 8, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.manterpercentualdetaxasdejuros.CopiarEstruturaDeTabelaDeTaxasFormTest
2026-11-17T17:43:49.8173386Z [INFO] Running br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.manterpercentualdetaxasdejuros.ReceberVigenciaFormTest
2026-11-17T17:43:49.8973468Z [INFO] Tests run: 10, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.077 s -- in br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.manterpercentualdetaxasdejuros.ReceberVigenciaFormTest
2026-11-17T17:43:49.8973898Z [INFO] Running br.gov.caixa.siemp.relatorios.ModelosJasperTest
2026-11-17T17:43:50.0879550Z log4j:WARN No appenders could be found for logger (net.sf.jasperreports.engine.xml.JRXmlDigesterFactory).
2026-11-17T17:43:50.0879946Z log4j:WARN Please initialize the log4j system properly.
2026-11-17T17:44:09.1449782Z [INFO] Tests run: 52, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 19.24 s -- in br.gov.caixa.siemp.relatorios.ModelosJasperTest
2026-11-17T17:44:09.1452986Z [INFO] Running br.gov.caixa.siemp.relatorios.RelatorioPosicaoDividaCalculatorTest
2026-11-17T17:44:10.0009126Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:235: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0009520Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0015306Z                                             ^
2026-11-17T17:44:10.0015851Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:245: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0016088Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0016490Z                                             ^
2026-11-17T17:44:10.0017011Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:255: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0017311Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:44:10.0017533Z                                             ^
2026-11-17T17:44:10.0017799Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:270: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0018134Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:44:10.0018287Z                                             ^
2026-11-17T17:44:10.0018663Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:365: warning: [removal] Boolean(boolean) in Boolean has been deprecated and marked for removal
2026-11-17T17:44:10.0018910Z                 value = (java.lang.Boolean)(new Boolean(((java.lang.String)field_nuParcela.getValue()) != null));
2026-11-17T17:44:10.0019088Z                                             ^
2026-11-17T17:44:10.0019383Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:370: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0019596Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:44:10.0019755Z                                             ^
2026-11-17T17:44:10.0020045Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:380: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0020277Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0020655Z                                             ^
2026-11-17T17:44:10.0020921Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:415: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0021131Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0021282Z                                             ^
2026-11-17T17:44:10.0021578Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:420: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0021811Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0021960Z                                             ^
2026-11-17T17:44:10.0022255Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:445: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0022487Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0022630Z                                             ^
2026-11-17T17:44:10.0022920Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:450: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0023132Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:44:10.0023240Z                                             ^
2026-11-17T17:44:10.0023525Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:503: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0023907Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0024058Z                                             ^
2026-11-17T17:44:10.0024353Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:513: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0024653Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0024799Z                                             ^
2026-11-17T17:44:10.0025089Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:523: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0025311Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:44:10.0025456Z                                             ^
2026-11-17T17:44:10.0025749Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:538: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0025925Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:44:10.0026074Z                                             ^
2026-11-17T17:44:10.0026375Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:633: warning: [removal] Boolean(boolean) in Boolean has been deprecated and marked for removal
2026-11-17T17:44:10.0026637Z                 value = (java.lang.Boolean)(new Boolean(((java.lang.String)field_nuParcela.getOldValue()) != null));
2026-11-17T17:44:10.0026805Z                                             ^
2026-11-17T17:44:10.0027096Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:638: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0027317Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:44:10.0027464Z                                             ^
2026-11-17T17:44:10.0027781Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:648: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0027993Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0028134Z                                             ^
2026-11-17T17:44:10.0028438Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:683: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0028642Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0028750Z                                             ^
2026-11-17T17:44:10.0029041Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:688: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0029245Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0029390Z                                             ^
2026-11-17T17:44:10.0029668Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:713: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0029879Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0030022Z                                             ^
2026-11-17T17:44:10.0030323Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:718: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0030622Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:44:10.0030791Z                                             ^
2026-11-17T17:44:10.0031082Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:771: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0031285Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0031433Z                                             ^
2026-11-17T17:44:10.0031721Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:781: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0031932Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0032077Z                                             ^
2026-11-17T17:44:10.0032428Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:791: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0032640Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:44:10.0032779Z                                             ^
2026-11-17T17:44:10.0033089Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:806: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0033307Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:44:10.0033453Z                                             ^
2026-11-17T17:44:10.0033713Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:901: warning: [removal] Boolean(boolean) in Boolean has been deprecated and marked for removal
2026-11-17T17:44:10.0033950Z                 value = (java.lang.Boolean)(new Boolean(((java.lang.String)field_nuParcela.getValue()) != null));
2026-11-17T17:44:10.0034120Z                                             ^
2026-11-17T17:44:10.0034433Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:906: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0034643Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:44:10.0034785Z                                             ^
2026-11-17T17:44:10.0035067Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:916: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0035279Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0035421Z                                             ^
2026-11-17T17:44:10.0035707Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:951: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0035940Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0036097Z                                             ^
2026-11-17T17:44:10.0036345Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:956: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0036545Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0036686Z                                             ^
2026-11-17T17:44:10.0036966Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:981: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0037175Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:44:10.0037319Z                                             ^
2026-11-17T17:44:10.0037603Z /opt/ads-agent/_work/29/s/siemp-web/relatorioPosicaoDivida.java:986: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:44:10.0037819Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:44:10.0037974Z                                             ^
2026-11-17T17:44:10.0038097Z 33 warnings
2026-11-17T17:44:10.0222075Z [INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.873 s -- in br.gov.caixa.siemp.relatorios.RelatorioPosicaoDividaCalculatorTest
2026-11-17T17:44:10.0222423Z [INFO] Running br.gov.caixa.siemp.relatorios.ExportacaoPdfTest
2026-11-17T17:44:10.6740148Z [ERROR] Tests run: 6, Failures: 0, Errors: 6, Skipped: 0, Time elapsed: 0.647 s <<< FAILURE! -- in br.gov.caixa.siemp.relatorios.ExportacaoPdfTest
2026-11-17T17:44:10.6750327Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[nce: 0 registros] -- Time elapsed: 0.220 s <<< ERROR!
2026-11-17T17:44:10.6750785Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:44:10.6751200Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:44:10.6751441Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:44:10.6751903Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:44:10.6752168Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:44:10.6752428Z 	at net.sf.jasperreports.engine.fill.JRFillTextField.prepare(JRFillTextField.java:554)
2026-11-17T17:44:10.6752926Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:44:10.6753260Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:44:10.6753688Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:44:10.6753944Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:44:10.6754150Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:164)
2026-11-17T17:44:10.6754380Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:44:10.6754594Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:44:10.6754818Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:44:10.6755048Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:44:10.6755356Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:44:10.6755609Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:44:10.6755830Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:44:10.6756079Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:44:10.6756302Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:44:10.6756562Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:44:10.6756809Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:44:10.6756998Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:44:10.6757215Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:44:10.6757428Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:44:10.6757634Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:44:10.6758792Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:44:10.6759054Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:44:10.6759257Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:44:10.6759460Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:44:10.6759659Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:44:10.6759857Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:44:10.6760019Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:44:10.6760205Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:44:10.6760596Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:44:10.6760822Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:44:10.6761025Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:44:10.6761226Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:44:10.6761427Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:44:10.6761668Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:44:10.6761861Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:44:10.6762070Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:44:10.6762270Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:44:10.6762515Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:44:10.6762755Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:44:10.6762980Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:44:10.6763198Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:44:10.6763404Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:44:10.6763613Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:44:10.6763693Z 
2026-11-17T17:44:10.6764077Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[nce: 1 registros] -- Time elapsed: 0.014 s <<< ERROR!
2026-11-17T17:44:10.6764502Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:44:10.6764748Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:44:10.6764999Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:44:10.6765224Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:44:10.6765453Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:44:10.6765683Z 	at net.sf.jasperreports.engine.fill.JRFillTextField.prepare(JRFillTextField.java:554)
2026-11-17T17:44:10.6765917Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:44:10.6766108Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:44:10.6766314Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:44:10.6766603Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:44:10.6766833Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReportStart(JRVerticalFiller.java:262)
2026-11-17T17:44:10.6767114Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:128)
2026-11-17T17:44:10.6767333Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:44:10.6767544Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:44:10.6767748Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:44:10.6767962Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:44:10.6768204Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:44:10.6768443Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:44:10.6768625Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:44:10.6768864Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:44:10.6769149Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:44:10.6769357Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:44:10.6769578Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:44:10.6769823Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:44:10.6770051Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:44:10.6770263Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:44:10.6770549Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:44:10.6770782Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:44:10.6771005Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:44:10.6771174Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:44:10.6771375Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:44:10.6771574Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:44:10.6771776Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:44:10.6771985Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:44:10.6772175Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:44:10.6772356Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:44:10.6772540Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:44:10.6772750Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:44:10.6772915Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:44:10.6773112Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:44:10.6773394Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:44:10.6773657Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:44:10.6773865Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:44:10.6774097Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:44:10.6774363Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:44:10.6774584Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:44:10.6774814Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:44:10.6775032Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:44:10.6775207Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:44:10.6775417Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:44:10.6775541Z 
2026-11-17T17:44:10.6775852Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[nce: 100 registros] -- Time elapsed: 0.051 s <<< ERROR!
2026-11-17T17:44:10.6776188Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:44:10.6776416Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:44:10.6776605Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:44:10.6776830Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:44:10.6777077Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:44:10.6777366Z 	at net.sf.jasperreports.engine.fill.JRFillTextField.prepare(JRFillTextField.java:554)
2026-11-17T17:44:10.6777608Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:44:10.6777836Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:44:10.6778041Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:44:10.6778294Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:44:10.6778518Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReportStart(JRVerticalFiller.java:262)
2026-11-17T17:44:10.6778745Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:128)
2026-11-17T17:44:10.6778974Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:44:10.6779148Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:44:10.6779365Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:44:10.6779581Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:44:10.6779826Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:44:10.6780060Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:44:10.6780272Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:44:10.6780575Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:44:10.6780798Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:44:10.6781029Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:44:10.6781250Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:44:10.6781469Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:44:10.6781656Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:44:10.6781860Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:44:10.6782072Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:44:10.6782326Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:44:10.6782534Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:44:10.6782887Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:44:10.6783146Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:44:10.6783346Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:44:10.6783552Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:44:10.6783745Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:44:10.6783896Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:44:10.6784080Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:44:10.6784269Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:44:10.6784470Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:44:10.6784678Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:44:10.6784893Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:44:10.6785087Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:44:10.6785275Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:44:10.6785476Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:44:10.6785712Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:44:10.6785941Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:44:10.6786160Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:44:10.6786387Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:44:10.6786639Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:44:10.6786870Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:44:10.6787187Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:44:10.6787307Z 
2026-11-17T17:44:10.6787783Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[rural: 0 registros] -- Time elapsed: 0.034 s <<< ERROR!
2026-11-17T17:44:10.6788228Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:44:10.6788526Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:44:10.6788847Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:44:10.6789080Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:44:10.6789302Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:44:10.6789643Z 	at net.sf.jasperreports.engine.fill.JRFillStaticText.prepare(JRFillStaticText.java:183)
2026-11-17T17:44:10.6789981Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:44:10.6790178Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:44:10.6790382Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:44:10.6790710Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:44:10.6790940Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReportStart(JRVerticalFiller.java:262)
2026-11-17T17:44:10.6791176Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:128)
2026-11-17T17:44:10.6791398Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:44:10.6791607Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:44:10.6791832Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:44:10.6792046Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:44:10.6792296Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:44:10.6792528Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:44:10.6792709Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:44:10.6792964Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:44:10.6793293Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:44:10.6793508Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:44:10.6793731Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:44:10.6793969Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:44:10.6794188Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:44:10.6794395Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:44:10.6794672Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:44:10.6794973Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:44:10.6795254Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:44:10.6795481Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:44:10.6795811Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:44:10.6796021Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:44:10.6796239Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:44:10.6796431Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:44:10.6796628Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:44:10.6796811Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:44:10.6797043Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:44:10.6797336Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:44:10.6797533Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:44:10.6797733Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:44:10.6797926Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:44:10.6798137Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:44:10.6798340Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:44:10.6798690Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:44:10.6798924Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:44:10.6799152Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:44:10.6799372Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:44:10.6799585Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:44:10.6799792Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:44:10.6799967Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:44:10.6800099Z 
2026-11-17T17:44:10.6800507Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[rural: 1 registros] -- Time elapsed: 0.017 s <<< ERROR!
2026-11-17T17:44:10.6800859Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:44:10.6801083Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:44:10.6801273Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:44:10.6801496Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:44:10.6801728Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:44:10.6802017Z 	at net.sf.jasperreports.engine.fill.JRFillStaticText.prepare(JRFillStaticText.java:183)
2026-11-17T17:44:10.6802275Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:44:10.6802540Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:44:10.6802746Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:44:10.6802965Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:44:10.6803189Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReportStart(JRVerticalFiller.java:262)
2026-11-17T17:44:10.6803412Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:128)
2026-11-17T17:44:10.6803684Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:44:10.6803860Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:44:10.6804063Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:44:10.6804326Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:44:10.6804595Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:44:10.6804827Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:44:10.6805041Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:44:10.6805276Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:44:10.6805496Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:44:10.6805802Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:44:10.6806103Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:44:10.6806367Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:44:10.6806558Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:44:10.6806825Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:44:10.6807030Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:44:10.6807289Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:44:10.6807579Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:44:10.6807879Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:44:10.6808088Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:44:10.6808294Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:44:10.6808488Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:44:10.6808698Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:44:10.6808849Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:44:10.6809030Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:44:10.6809219Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:44:10.6809412Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:44:10.6809663Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:44:10.6809877Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:44:10.6810074Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:44:10.6810313Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:44:10.6810663Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:44:10.6810856Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:44:10.6811082Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:44:10.6811301Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:44:10.6811520Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:44:10.6811736Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:44:10.6811958Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:44:10.6812168Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:44:10.6812301Z 
2026-11-17T17:44:10.6812640Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[rural: 100 registros] -- Time elapsed: 0.310 s <<< ERROR!
2026-11-17T17:44:10.6813085Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:44:10.6813359Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:44:10.6813583Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:44:10.6813816Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:44:10.6814046Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:44:10.6814278Z 	at net.sf.jasperreports.engine.fill.JRFillStaticText.prepare(JRFillStaticText.java:183)
2026-11-17T17:44:10.6814549Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:44:10.6814776Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:44:10.6814945Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:44:10.6815180Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:44:10.6815405Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReportStart(JRVerticalFiller.java:262)
2026-11-17T17:44:10.6815631Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:128)
2026-11-17T17:44:10.6815857Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:44:10.6816063Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:44:10.6816267Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:44:10.6816479Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:44:10.6816721Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:44:10.6816970Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:44:10.6817184Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:44:10.6817393Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:44:10.6817619Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:44:10.6817829Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:44:10.6818049Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:44:10.6818271Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:44:10.6818484Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:44:10.6818690Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:44:10.6818911Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:44:10.6819126Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:44:10.6819341Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:44:10.6819504Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:44:10.6819702Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:44:10.6819898Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:44:10.6820092Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:44:10.6820310Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:44:10.6820682Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:44:10.6820891Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:44:10.6821092Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:44:10.6821287Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:44:10.6821525Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:44:10.6821690Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:44:10.6821886Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:44:10.6822115Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:44:10.6822321Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:44:10.6822543Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:44:10.6822796Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:44:10.6823017Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:44:10.6823237Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:44:10.6823457Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:44:10.6823664Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:44:10.6823839Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:44:10.6823953Z 
2026-11-17T17:44:10.6824137Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaTabelaDeTaxasDeConvenio.ConsultaTabelaDeTaxasDeConvenioHelpersTest
2026-11-17T17:44:10.6824823Z [INFO] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.001 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaTabelaDeTaxasDeConvenio.ConsultaTabelaDeTaxasDeConvenioHelpersTest
2026-11-17T17:44:10.6825122Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaTabelaDeTACDeConvenio.ConsultaTabelaDeTACDeConvenioHelpersTest
2026-11-17T17:44:10.6825526Z [INFO] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.003 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaTabelaDeTACDeConvenio.ConsultaTabelaDeTACDeConvenioHelpersTest
2026-11-17T17:44:10.6825799Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioParametroHelperTest
2026-11-17T17:44:10.6841760Z [INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioParametroHelperTest
2026-11-17T17:44:10.6842273Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioHistoricosHelperTest
2026-11-17T17:44:10.6870300Z [INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioHistoricosHelperTest
2026-11-17T17:44:10.6870859Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioHelperTest
2026-11-17T17:44:10.6981681Z [INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioHelperTest
2026-11-17T17:44:10.6982235Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaMovimentoDeAcertoDoConvenioNovo.ConsultaMovimentoDeAcertoDoConvenioHelperTest
2026-11-17T17:44:10.6982662Z [INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.001 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaMovimentoDeAcertoDoConvenioNovo.ConsultaMovimentoDeAcertoDoConvenioHelperTest
2026-11-17T17:44:10.6983135Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaConveniosExtratoAtraso.ConsultaConveniosExtratoAtrasoHelperColecoesTest
2026-11-17T17:44:10.6983538Z [INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaConveniosExtratoAtraso.ConsultaConveniosExtratoAtrasoHelperColecoesTest
2026-11-17T17:44:10.6983886Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultarComiteDeAutorizacoes.ConsultarComiteDeAutorizacoesHelpersTest
2026-11-17T17:44:10.6984270Z [INFO] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.001 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultarComiteDeAutorizacoes.ConsultarComiteDeAutorizacoesHelpersTest
2026-11-17T17:44:10.6984547Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.ajustaExtratoDoConvenio.AjustaExtratoDoConvenioTotalizadorHelperTest
2026-11-17T17:44:10.6984929Z [INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in br.gov.caixa.siemp.apresentacao.consignacao.ajustaExtratoDoConvenio.AjustaExtratoDoConvenioTotalizadorHelperTest
2026-11-17T17:44:10.6985216Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultarDadosConvenio.ConsultarDadosConvenioHelpersTest
2026-11-17T17:44:10.7051743Z [INFO] Tests run: 10, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.004 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultarDadosConvenio.ConsultarDadosConvenioHelpersTest
2026-11-17T17:44:10.7052284Z [INFO] Running br.gov.caixa.siemp.apresentacao.evolucao.estornarpagamento.EstornarPagamentoACTTest
2026-11-17T17:44:10.7713879Z Criando Log de Sistema
2026-11-17T17:44:10.7714093Z Log do Sitema inicializada!
2026-11-17T17:44:10.7988718Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.7989269Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:44:10.7989596Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.7989776Z GRAVE: falha na procedure
2026-11-17T17:44:10.7989950Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.7990128Z GRAVE: Erro ao fechar PreparedStatement do SIRIC: 
2026-11-17T17:44:10.7990327Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.7990560Z GRAVE: falha ao fechar
2026-11-17T17:44:10.7990730Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.7990901Z GRAVE: Erro ao fechar conexao com o SIRIC: 
2026-11-17T17:44:10.7991076Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.7991260Z GRAVE: falha ao fechar
2026-11-17T17:44:10.8759947Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8761870Z GRAVE: Erro de SQL: jdbc/SybaseSiempDS
2026-11-17T17:44:10.8913902Z [INFO] Tests run: 26, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.185 s -- in br.gov.caixa.siemp.apresentacao.evolucao.estornarpagamento.EstornarPagamentoACTTest
2026-11-17T17:44:10.8914201Z [INFO] Running br.gov.caixa.siemp.apresentacao.evolucao.SiricEstornoTest
2026-11-17T17:44:10.8926678Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8926958Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:44:10.8927166Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8927334Z GRAVE: falha na execucao
2026-11-17T17:44:10.8927644Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8927871Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:44:10.8928072Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8928203Z GRAVE: falha na execucao
2026-11-17T17:44:10.8950632Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8950885Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:44:10.8951268Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8951431Z GRAVE: falha na execucao
2026-11-17T17:44:10.8951645Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8951820Z GRAVE: Erro ao fechar PreparedStatement do SIRIC: 
2026-11-17T17:44:10.8952012Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8952239Z GRAVE: falha ao fechar statement
2026-11-17T17:44:10.8952409Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8952547Z GRAVE: Erro ao fechar conexao com o SIRIC: 
2026-11-17T17:44:10.8952719Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8952882Z GRAVE: falha ao fechar conexao
2026-11-17T17:44:10.8953050Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8953300Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:44:10.8953494Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8953661Z GRAVE: falha na execucao
2026-11-17T17:44:10.8953829Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8954001Z GRAVE: Erro ao fechar PreparedStatement do SIRIC: 
2026-11-17T17:44:10.8954140Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8954303Z GRAVE: falha ao fechar statement
2026-11-17T17:44:10.8954471Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8954638Z GRAVE: Erro ao fechar conexao com o SIRIC: 
2026-11-17T17:44:10.8954833Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8954996Z GRAVE: falha ao fechar conexao
2026-11-17T17:44:10.8961532Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8961783Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:44:10.8962430Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8962573Z GRAVE: falha na preparacao
2026-11-17T17:44:10.8962736Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8962975Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:44:10.8963158Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.8963358Z GRAVE: falha na preparacao
2026-11-17T17:44:10.8986552Z [INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.005 s -- in br.gov.caixa.siemp.apresentacao.evolucao.SiricEstornoTest
2026-11-17T17:44:10.8986803Z [INFO] Running br.gov.caixa.siemp.apresentacao.evolucao.estornarconcessaoemprestimo.EstornarConcessaoEmprestimoACTTest
2026-11-17T17:44:10.9047448Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.9047715Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:44:10.9047895Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.9048065Z GRAVE: falha na procedure
2026-11-17T17:44:10.9048198Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.9048427Z GRAVE: Erro ao fechar PreparedStatement do SIRIC: 
2026-11-17T17:44:10.9048599Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.9048761Z GRAVE: falha ao fechar
2026-11-17T17:44:10.9048927Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.9049091Z GRAVE: Erro ao fechar conexao com o SIRIC: 
2026-11-17T17:44:10.9049262Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.9049417Z GRAVE: falha ao fechar
2026-11-17T17:44:10.9107289Z nov. 17, 2026 2:44:10 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:44:10.9107589Z GRAVE: Erro de SQL: jdbc/SybaseSiempDS
2026-11-17T17:44:10.9191730Z [INFO] Tests run: 11, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.018 s -- in br.gov.caixa.siemp.apresentacao.evolucao.estornarconcessaoemprestimo.EstornarConcessaoEmprestimoACTTest
2026-11-17T17:44:10.9192239Z [INFO] Running br.gov.caixa.siemp.creditorural.extrato.ExtratoCreditoRuralActionTest
2026-11-17T17:44:10.9216134Z [INFO] Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.001 s -- in br.gov.caixa.siemp.creditorural.extrato.ExtratoCreditoRuralActionTest
2026-11-17T17:44:10.9216387Z [INFO] Running br.gov.caixa.siemp.creditorural.bndes.CobrancaBNDESActionTest
2026-11-17T17:44:10.9302997Z [INFO] Tests run: 6, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.007 s -- in br.gov.caixa.siemp.creditorural.bndes.CobrancaBNDESActionTest
2026-11-17T17:44:10.9303250Z [INFO] Running br.gov.caixa.siemp.consultas.ConsultasContratoTest
2026-11-17T17:44:11.4305285Z [WARNING] Tests run: 180, Failures: 0, Errors: 0, Skipped: 13, Time elapsed: 0.494 s -- in br.gov.caixa.siemp.consultas.ConsultasContratoTest
2026-11-17T17:44:11.4305707Z [INFO] Running br.gov.caixa.siemp.consultas.ConfiguracaoJstlValidatorTest
2026-11-17T17:44:11.4445384Z [INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.012 s -- in br.gov.caixa.siemp.consultas.ConfiguracaoJstlValidatorTest
2026-11-17T17:44:11.4445718Z [INFO] Running br.gov.caixa.siemp.consultas.ConveniosActionsTest
2026-11-17T17:44:11.4558538Z [INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.010 s -- in br.gov.caixa.siemp.consultas.ConveniosActionsTest
2026-11-17T17:44:11.4558848Z [INFO] Running br.gov.caixa.siemp.comum.apresentacao.SiempActionTest
2026-11-17T17:44:11.4607043Z [INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.004 s -- in br.gov.caixa.siemp.comum.apresentacao.SiempActionTest
2026-11-17T17:44:11.4607351Z [INFO] Running br.gov.caixa.siemp.comum.apresentacao.login.LoginMenuConsultasTest
2026-11-17T17:44:11.4645524Z [INFO] Tests run: 12, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.002 s -- in br.gov.caixa.siemp.comum.apresentacao.login.LoginMenuConsultasTest
2026-11-17T17:44:11.4646515Z [INFO] Running br.gov.caixa.siemp.comum.apresentacao.login.LoginActionTest
2026-11-17T17:44:11.4660854Z [INFO] Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in br.gov.caixa.siemp.comum.apresentacao.login.LoginActionTest
2026-11-17T17:44:11.4661327Z [INFO] Running br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest
2026-11-17T17:44:11.5236844Z org.apache.commons.fileupload.FileUploadBase$SizeLimitExceededException: the request was rejected because its size (5243003) exceeds the configured maximum (5242880)
2026-11-17T17:44:11.5237172Z 	at org.apache.commons.fileupload.FileUploadBase$FileItemIteratorImpl.<init>(FileUploadBase.java:965)
2026-11-17T17:44:11.5237434Z 	at org.apache.commons.fileupload.FileUploadBase.getItemIterator(FileUploadBase.java:310)
2026-11-17T17:44:11.5237664Z 	at org.apache.commons.fileupload.FileUploadBase.parseRequest(FileUploadBase.java:334)
2026-11-17T17:44:11.5237910Z 	at org.apache.commons.fileupload.FileUploadBase.parseRequest(FileUploadBase.java:288)
2026-11-17T17:44:11.5238170Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServlet.obterArquivoLegivel(AtualizarIndiceBovespaServlet.java:77)
2026-11-17T17:44:11.5238466Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServlet.doPost(AtualizarIndiceBovespaServlet.java:55)
2026-11-17T17:44:11.5238930Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest.deveRejeitarUploadAcimaDeCincoMegabytes(AtualizarIndiceBovespaServletTest.java:111)
2026-11-17T17:44:11.5239192Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:44:11.5239411Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:44:11.5239658Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:44:11.5239876Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:44:11.5240086Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:44:11.5240572Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:44:11.5240822Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:44:11.5241010Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:44:11.5241315Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:44:11.5241599Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:44:11.5241819Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:44:11.5242024Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:44:11.5242227Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:44:11.5242429Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:44:11.5242643Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:44:11.5242845Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:44:11.5243059Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:44:11.5243232Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:44:11.5243462Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:44:11.5243692Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:44:11.5243913Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:44:11.5244132Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:44:11.5244352Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:44:11.5244572Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:44:11.5244785Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:44:11.5251394Z java.lang.Exception: falha
2026-11-17T17:44:11.5251651Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest$3.atualizarIndice(AtualizarIndiceBovespaServletTest.java:206)
2026-11-17T17:44:11.5251941Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServlet.processarAtualizacao(AtualizarIndiceBovespaServlet.java:112)
2026-11-17T17:44:11.5252208Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServlet.doPost(AtualizarIndiceBovespaServlet.java:63)
2026-11-17T17:44:11.5252448Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest.executarComDelegate(AtualizarIndiceBovespaServletTest.java:249)
2026-11-17T17:44:11.5252819Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest.deveTratarFalhaNaAtualizacao(AtualizarIndiceBovespaServletTest.java:212)
2026-11-17T17:44:11.5253083Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:44:11.5253299Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:44:11.5253563Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:44:11.5253794Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:44:11.5253999Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:44:11.5254221Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:44:11.5254440Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:44:11.5254656Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:44:11.5254868Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:44:11.5255173Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:44:11.5255407Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:44:11.5255578Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:44:11.5255896Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:44:11.5256101Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:44:11.5256301Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:44:11.5256509Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:44:11.5256703Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:44:11.5256910Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:44:11.5257133Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:44:11.5257378Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:44:11.5257603Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:44:11.5257787Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:44:11.5258010Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:44:11.5258241Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:44:11.5258476Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:44:11.5317115Z [INFO] Tests run: 14, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.064 s -- in br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest
2026-11-17T17:44:11.5317512Z [INFO] Running teste.br.gov.caixa.siemp.comum.apresentacao.testeerromultiplo.TesteErroMultiploActionTest
2026-11-17T17:44:11.5331874Z [INFO] Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in teste.br.gov.caixa.siemp.comum.apresentacao.testeerromultiplo.TesteErroMultiploActionTest
2026-11-17T17:44:11.5884587Z [INFO] 
2026-11-17T17:44:11.5884940Z [INFO] Results:
2026-11-17T17:44:11.5885079Z [INFO] 
2026-11-17T17:44:11.5885254Z [ERROR] Errors: 
2026-11-17T17:44:11.5885840Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:44:11.5886253Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:44:11.5886654Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:44:11.5887080Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:44:11.5887456Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:44:11.5888016Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:44:11.5888228Z [INFO] 
2026-11-17T17:44:11.5888382Z [ERROR] Tests run: 403, Failures: 0, Errors: 6, Skipped: 13
2026-11-17T17:44:11.5888546Z [INFO] 
2026-11-17T17:44:11.5910283Z [INFO] ------------------------------------------------------------------------
2026-11-17T17:44:11.5910549Z [INFO] Reactor Summary for siemp application 14.37.0.6:
2026-11-17T17:44:11.5910926Z [INFO] 
2026-11-17T17:44:11.5912836Z [INFO] siemp application .................................. SUCCESS [  0.155 s]
2026-11-17T17:44:11.5913891Z [INFO] SIEMP Web module ................................... FAILURE [ 31.280 s]
2026-11-17T17:44:11.5914082Z [INFO] SIEMP EAR module ................................... SKIPPED
2026-11-17T17:44:11.5914352Z [INFO] ------------------------------------------------------------------------
2026-11-17T17:44:11.5914592Z [INFO] BUILD FAILURE
2026-11-17T17:44:11.5914791Z [INFO] ------------------------------------------------------------------------
2026-11-17T17:44:11.5914975Z [INFO] Total time:  31.556 s
2026-11-17T17:44:11.5916858Z [INFO] Finished at: 2026-11-17T14:44:11-03:00
2026-11-17T17:44:11.5917108Z [INFO] ------------------------------------------------------------------------
2026-11-17T17:44:11.5923326Z [ERROR] Failed to execute goal org.apache.maven.plugins:maven-surefire-plugin:3.2.5:test (default-test) on project siemp-web: 
2026-11-17T17:44:11.5923529Z [ERROR] 
2026-11-17T17:44:11.5923798Z [ERROR] Please refer to /opt/ads-agent/_work/29/s/siemp-web/target/surefire-reports for the individual test results.
2026-11-17T17:44:11.5924095Z [ERROR] Please refer to dump files (if any exist) [date].dump, [date]-jvmRun[N].dump and [date].dumpstream.
2026-11-17T17:44:11.5924298Z [ERROR] -> [Help 1]
2026-11-17T17:44:11.5924551Z [ERROR] 
2026-11-17T17:44:11.5924786Z [ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
2026-11-17T17:44:11.5925050Z [ERROR] Re-run Maven using the -X switch to enable full debug logging.
2026-11-17T17:44:11.5925165Z [ERROR] 
2026-11-17T17:44:11.5925358Z [ERROR] For more information about the errors and possible solutions, please read the following articles:
2026-11-17T17:44:11.5929302Z [ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoFailureException
2026-11-17T17:44:11.5929468Z [ERROR] 
2026-11-17T17:44:11.5929625Z [ERROR] After correcting the problems, you can resume the build with the command
2026-11-17T17:44:11.5929852Z [ERROR]   mvn <args> -rf :siemp-web
2026-11-17T17:44:11.6701177Z The process '/opt/apache-maven/apache-maven-3.8.5/bin/mvn' failed with exit code 1
2026-11-17T17:44:11.6701668Z Could not retrieve code analysis results - Maven run failed.
2026-11-17T17:44:11.6705104Z ##[error]Build failed.
2026-11-17T17:44:11.6774691Z ##[section]Finishing: Maven
