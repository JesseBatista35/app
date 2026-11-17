2026-11-17T17:34:14.1585588Z ##[section]Starting: Maven
2026-11-17T17:34:14.1591647Z ==============================================================================
2026-11-17T17:34:14.1591767Z Task         : Maven
2026-11-17T17:34:14.1591814Z Description  : Build, test, and deploy with Apache Maven
2026-11-17T17:34:14.1591877Z Version      : 4.225.0
2026-11-17T17:34:14.1592290Z Author       : Microsoft Corporation
2026-11-17T17:34:14.1592349Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/build/maven
2026-11-17T17:34:14.1592418Z ==============================================================================
2026-11-17T17:34:14.7394013Z [command]/opt/apache-maven/apache-maven-3.8.5/bin/mvn -version
2026-11-17T17:34:14.8342258Z Apache Maven 3.8.5 (3599d3414f046de2324203b78ddcf9b5e4388aa0)
2026-11-17T17:34:14.8342817Z Maven home: /opt/apache-maven/apache-maven-3.8.5
2026-11-17T17:34:14.8343088Z Java version: 17.0.8, vendor: OpenLogic, runtime: /usr/java/open-jdk-17.0.8
2026-11-17T17:34:14.8343238Z Default locale: pt_BR, platform encoding: UTF-8
2026-11-17T17:34:14.8343717Z OS name: "linux", version: "5.18.5-100.fc35.x86_64", arch: "amd64", family: "unix"
2026-11-17T17:34:14.8525269Z [command]/opt/apache-maven/apache-maven-3.8.5/bin/mvn -f /opt/ads-agent/_work/36/s/pom.xml clean verify -Dversion.app= -U
2026-11-17T17:34:15.5190335Z [INFO] Scanning for projects...
2026-11-17T17:34:15.6294745Z [INFO] ------------------------------------------------------------------------
2026-11-17T17:34:15.6295771Z [INFO] Reactor Build Order:
2026-11-17T17:34:15.6295912Z [INFO] 
2026-11-17T17:34:15.6298404Z [INFO] siemp application                                                  [pom]
2026-11-17T17:34:15.6298645Z [INFO] SIEMP Web module                                                   [war]
2026-11-17T17:34:15.6300340Z [INFO] SIEMP EAR module                                                   [ear]
2026-11-17T17:34:15.6343781Z [INFO] 
2026-11-17T17:34:15.6345327Z [INFO] ----------------------< br.gov.caixa.siemp:siemp >----------------------
2026-11-17T17:34:15.6345716Z [INFO] Building siemp application 14.37.0.6                               [1/3]
2026-11-17T17:34:15.6346231Z [INFO] --------------------------------[ pom ]---------------------------------
2026-11-17T17:34:15.6842918Z [INFO] 
2026-11-17T17:34:15.6843934Z [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ siemp ---
2026-11-17T17:34:15.7201419Z [INFO] 
2026-11-17T17:34:15.7203321Z [INFO] --- jacoco-maven-plugin:0.8.13:prepare-agent (prepare-agent) @ siemp ---
2026-11-17T17:34:15.8243727Z [INFO] argLine set to -javaagent:/opt/ads-agent/cache-tools/.m2/repository/org/jacoco/org.jacoco.agent/0.8.13/org.jacoco.agent-0.8.13-runtime.jar=destfile=/opt/ads-agent/_work/36/s/target/jacoco.exec
2026-11-17T17:34:15.8244150Z [INFO] 
2026-11-17T17:34:15.8244406Z [INFO] --- jacoco-maven-plugin:0.8.13:report (generate-report) @ siemp ---
2026-11-17T17:34:15.8261000Z [INFO] Skipping JaCoCo execution due to missing execution data file.
2026-11-17T17:34:15.8263251Z [INFO] 
2026-11-17T17:34:15.8263921Z [INFO] --------------------< br.gov.caixa.siemp:siemp-web >--------------------
2026-11-17T17:34:15.8264122Z [INFO] Building SIEMP Web module 14.37.0.6                                [2/3]
2026-11-17T17:34:15.8264334Z [INFO] --------------------------------[ war ]---------------------------------
2026-11-17T17:34:16.4679138Z [INFO] 
2026-11-17T17:34:16.4679875Z [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ siemp-web ---
2026-11-17T17:34:16.4695860Z [INFO] 
2026-11-17T17:34:16.4696419Z [INFO] --- jacoco-maven-plugin:0.8.13:prepare-agent (prepare-agent) @ siemp-web ---
2026-11-17T17:34:16.4704741Z [INFO] argLine set to -javaagent:/opt/ads-agent/cache-tools/.m2/repository/org/jacoco/org.jacoco.agent/0.8.13/org.jacoco.agent-0.8.13-runtime.jar=destfile=/opt/ads-agent/_work/36/s/siemp-web/target/jacoco.exec
2026-11-17T17:34:16.4705390Z [INFO] 
2026-11-17T17:34:16.4705648Z [INFO] --- maven-resources-plugin:3.3.1:resources (default-resources) @ siemp-web ---
2026-11-17T17:34:16.5199330Z [INFO] Copying 6 resources from src/main/resources to target/classes
2026-11-17T17:34:16.6027635Z [INFO] Copying 682 resources from src/main/java to target/classes
2026-11-17T17:34:16.6523395Z [INFO] The encoding used to copy filtered properties files have not been set. This means that the same encoding will be used to copy filtered properties files as when copying other filtered resources. This might not be what you want! Run your build with --debug to see which files might be affected. Read more at https://maven.apache.org/plugins/maven-resources-plugin/examples/filtering-properties-files.html
2026-11-17T17:34:16.6523823Z [INFO] 
2026-11-17T17:34:16.6526332Z [INFO] --- maven-compiler-plugin:3.11.0:compile (default-compile) @ siemp-web ---
2026-11-17T17:34:16.8567776Z [INFO] Changes detected - recompiling the module! :source
2026-11-17T17:34:16.8652630Z [INFO] Compiling 2259 source files with javac [debug release 17] to target/classes
2026-11-17T17:34:24.7993359Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(288,23): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[288,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8004564Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(302,23): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[302,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8005563Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[288,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8006030Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[302,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8008102Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(310,21): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[310,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8010281Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(318,21): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[318,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8012679Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(334,20): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[334,20] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8015496Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(342,21): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[342,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8017652Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(350,20): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[350,20] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8020455Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(361,21): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[361,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8022815Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(621,21): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[621,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8025196Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(629,23): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[629,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8027629Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(844,23): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[844,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8029998Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java(964,35): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[964,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8032335Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java(95,28): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[95,28] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8034811Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java(106,24): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[106,24] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8036982Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java(608,85): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[608,85] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8039185Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java(608,36): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[608,36] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8041446Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/apoio/apresentacao/mantertabelas/ManterTabelaForm.java(1684,23): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/apoio/apresentacao/mantertabelas/ManterTabelaForm.java:[1684,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8043729Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java(558,51): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[558,51] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8045888Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java(601,85): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[601,85] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8048199Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java(601,36): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[601,36] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8050430Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java(203,23): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java:[203,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8052599Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java(297,23): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java:[297,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8054717Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java(24,8): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java:[24,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8056884Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterTabelaHelper.java(17,8): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterTabelaHelper.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8059193Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterSelectMultipleHelper.java(17,8): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterSelectMultipleHelper.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8061459Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/IObjetoParaCombo.java(17,8): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/IObjetoParaCombo.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8063732Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(53,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[53,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8065943Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(70,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[70,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8068191Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(121,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[121,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8070430Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(128,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[128,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8072750Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(134,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[134,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8075071Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(140,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[140,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8077354Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(145,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[145,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8079594Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(150,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[150,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8081951Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(155,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[155,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8084163Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(160,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[160,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8086421Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(166,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[166,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8088721Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(176,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[176,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8089645Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[310,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8090015Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[318,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8090385Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[334,20] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8090770Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[342,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8091196Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[350,20] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8091564Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[361,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8091996Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[621,21] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8092363Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[629,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8092764Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[844,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8093134Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java:[964,35] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8093496Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[95,28] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8093825Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[106,24] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8094213Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[608,85] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8094633Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempFiltroForm.java:[608,36] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8095038Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/apoio/apresentacao/mantertabelas/ManterTabelaForm.java:[1684,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8095541Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[558,51] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8095944Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[601,85] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8096351Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/SiempHelper.java:[601,36] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8096825Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java:[203,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8097163Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java:[297,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8097506Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/Combo.java:[24,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8097869Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterTabelaHelper.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8098244Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/ManterSelectMultipleHelper.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8098634Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/IObjetoParaCombo.java:[17,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8099030Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[53,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8099448Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[70,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8099916Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[121,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8100372Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[128,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8100790Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[134,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8101260Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[140,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8101761Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[145,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8102267Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[150,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8102705Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[155,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8103111Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[160,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8103526Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[166,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8103941Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[176,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8106214Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(182,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[182,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8108493Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(188,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[188,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8110735Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(356,42): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[356,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8113108Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(371,42): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[371,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8115735Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(386,42): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[386,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8117996Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(416,42): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[416,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8120456Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(431,42): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[431,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8122772Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(446,42): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[446,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8124967Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(462,42): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[462,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8127262Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(478,42): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[478,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8129445Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(520,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[520,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8131921Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java(989,50): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[989,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8134106Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/filtros/formatador/FormatadorDeRotulo.java(108,23): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/filtros/formatador/FormatadorDeRotulo.java:[108,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8136334Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/FabricaDeCombos.java(24,8): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/FabricaDeCombos.java:[24,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8138532Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/IObjetoParaComboComAtributos.java(20,8): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/IObjetoParaComboComAtributos.java:[20,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8140814Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/TratarTOForm.java(528,51): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/TratarTOForm.java:[528,51] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8143425Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/BusinessDelegate.java(230,59): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/BusinessDelegate.java:[230,59] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8145672Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java(76,30): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[76,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8147843Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java(87,28): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[87,28] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8150053Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java(97,31): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[97,31] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8152259Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java(118,55): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[118,55] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8154365Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java(183,28): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[183,28] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8156564Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java(193,41): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[193,41] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8158669Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java(205,33): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[205,33] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8160839Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/persistencia/SiempDAOMainframe.java(142,59): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/persistencia/SiempDAOMainframe.java:[142,59] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8163197Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/XMLProgramAnalyzer.java(353,41): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/XMLProgramAnalyzer.java:[353,41] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8165408Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(89,109): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[89,109] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8167943Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(97,108): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[97,108] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8170376Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(105,107): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[105,107] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8175237Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(112,110): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[112,110] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8177550Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(120,109): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[120,109] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8179681Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(129,108): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[129,108] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8181954Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(137,107): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[137,107] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8184217Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(145,110): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[145,110] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8186498Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(150,99): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[150,99] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8188696Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java(164,94): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[164,94] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8191506Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(136,32): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[136,32] Double(java.lang.String) in java.lang.Double has been deprecated and marked for removal
2026-11-17T17:34:24.8193734Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(148,32): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[148,32] Float(java.lang.String) in java.lang.Float has been deprecated and marked for removal
2026-11-17T17:34:24.8196016Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(157,32): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[157,32] Long(java.lang.String) in java.lang.Long has been deprecated and marked for removal
2026-11-17T17:34:24.8198358Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(166,32): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[166,32] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8200619Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(180,32): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[180,32] Double(java.lang.String) in java.lang.Double has been deprecated and marked for removal
2026-11-17T17:34:24.8202940Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(192,32): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[192,32] Float(java.lang.String) in java.lang.Float has been deprecated and marked for removal
2026-11-17T17:34:24.8205190Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(201,32): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[201,32] Long(java.lang.String) in java.lang.Long has been deprecated and marked for removal
2026-11-17T17:34:24.8207369Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java(210,32): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[210,32] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8209606Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(34,41): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[34,41] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8211818Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(111,41): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[111,41] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8214468Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(122,36): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[122,36] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8216911Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(132,30): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[132,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8219023Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(143,30): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[143,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8221309Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(154,44): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[154,44] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8223495Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(165,36): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[165,36] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8225710Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(175,42): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[175,42] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8228063Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(187,25): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[187,25] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8230137Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(204,30): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[204,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8232400Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(214,30): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[214,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8234534Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(225,30): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[225,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8236627Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(236,30): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[236,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8239532Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(247,30): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[247,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8241786Z ##[warning] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java(257,30): warning :  /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[257,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8242694Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[182,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8243124Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[188,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8243689Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[356,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8244139Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[371,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8244577Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[386,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8245003Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[416,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8245490Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[431,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8245960Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[446,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8246413Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[462,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8246851Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[478,42] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8247267Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[520,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8247683Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/helper/FabricaDeHelperDeMensagemDeErro.java:[989,50] Integer(int) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8248043Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/filtros/formatador/FormatadorDeRotulo.java:[108,23] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8248409Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/FabricaDeCombos.java:[24,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8248778Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/util/IObjetoParaComboComAtributos.java:[20,8] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8249208Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/TratarTOForm.java:[528,51] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8249655Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/framework/transferobject/BusinessDelegate.java:[230,59] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8250071Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[76,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8250423Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[87,28] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8250771Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[97,31] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8251235Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[118,55] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8251609Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[183,28] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8251966Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[193,41] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8252327Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/negocio/SiempModel.java:[205,33] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8252781Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/persistencia/SiempDAOMainframe.java:[142,59] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8253246Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/XMLProgramAnalyzer.java:[353,41] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8253659Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[89,109] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8253883Z   cast to java.lang.Object for a varargs call
2026-11-17T17:34:24.8254115Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:34:24.8254463Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[97,108] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8254686Z   cast to java.lang.Object for a varargs call
2026-11-17T17:34:24.8254885Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:34:24.8255364Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[105,107] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8255590Z   cast to java.lang.Object for a varargs call
2026-11-17T17:34:24.8255823Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:34:24.8256167Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[112,110] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8256388Z   cast to java.lang.Object for a varargs call
2026-11-17T17:34:24.8256614Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:34:24.8256954Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[120,109] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8257175Z   cast to java.lang.Object for a varargs call
2026-11-17T17:34:24.8257415Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:34:24.8257722Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[129,108] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8257932Z   cast to java.lang.Object for a varargs call
2026-11-17T17:34:24.8258165Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:34:24.8258514Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[137,107] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8258732Z   cast to java.lang.Object for a varargs call
2026-11-17T17:34:24.8258960Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:34:24.8259317Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[145,110] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8259529Z   cast to java.lang.Object for a varargs call
2026-11-17T17:34:24.8259770Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:34:24.8260159Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[150,99] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8260374Z   cast to java.lang.Object for a varargs call
2026-11-17T17:34:24.8260599Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:34:24.8260946Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Group.java:[164,94] non-varargs call of varargs method with inexact argument type for last parameter;
2026-11-17T17:34:24.8261251Z   cast to java.lang.Object for a varargs call
2026-11-17T17:34:24.8261498Z   cast to java.lang.Object[] for a non-varargs call and to suppress this warning
2026-11-17T17:34:24.8261851Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[136,32] Double(java.lang.String) in java.lang.Double has been deprecated and marked for removal
2026-11-17T17:34:24.8262258Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[148,32] Float(java.lang.String) in java.lang.Float has been deprecated and marked for removal
2026-11-17T17:34:24.8262681Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[157,32] Long(java.lang.String) in java.lang.Long has been deprecated and marked for removal
2026-11-17T17:34:24.8263090Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[166,32] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8263494Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[180,32] Double(java.lang.String) in java.lang.Double has been deprecated and marked for removal
2026-11-17T17:34:24.8263888Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[192,32] Float(java.lang.String) in java.lang.Float has been deprecated and marked for removal
2026-11-17T17:34:24.8264290Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[201,32] Long(java.lang.String) in java.lang.Long has been deprecated and marked for removal
2026-11-17T17:34:24.8264685Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/com/politec/bsb/fsw/jmainframe/xml/Param.java:[210,32] Integer(java.lang.String) in java.lang.Integer has been deprecated and marked for removal
2026-11-17T17:34:24.8265052Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[34,41] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8265407Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[111,41] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8265776Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[122,36] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8266127Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[132,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8266441Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[143,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8266796Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[154,44] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8267146Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[165,36] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8267500Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[175,42] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8267892Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[187,25] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8268234Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[204,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8268613Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[214,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8268977Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[225,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8269320Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[236,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8269671Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[247,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8270012Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[257,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8270353Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[267,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8270689Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[278,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8271180Z [WARNING] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/FabricaDeDAOComum.java:[288,30] deprecated item is not annotated with @Deprecated
2026-11-17T17:34:24.8271553Z [INFO] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java: Some input files use or override a deprecated API.
2026-11-17T17:34:24.8271958Z [INFO] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java: Recompile with -Xlint:deprecation for details.
2026-11-17T17:34:24.8272341Z [INFO] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/persistencia/LoginDAO.java: Some input files additionally use or override a deprecated API that is marked for removal.
2026-11-17T17:34:24.8272717Z [INFO] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java: Some input files use unchecked or unsafe operations.
2026-11-17T17:34:24.8273038Z [INFO] /opt/ads-agent/_work/36/s/siemp-web/src/main/java/br/gov/caixa/siemp/comum/apresentacao/SiempActionForm.java: Recompile with -Xlint:unchecked for details.
2026-11-17T17:34:24.8273233Z [INFO] 
2026-11-17T17:34:24.8273476Z [INFO] --- maven-resources-plugin:3.3.1:testResources (default-testResources) @ siemp-web ---
2026-11-17T17:34:24.8273781Z [INFO] Copying 1 resource from src/test/resources to target/test-classes
2026-11-17T17:34:24.8273932Z [INFO] 
2026-11-17T17:34:24.8274165Z [INFO] --- maven-compiler-plugin:3.11.0:testCompile (default-testCompile) @ siemp-web ---
2026-11-17T17:34:24.8274434Z [INFO] Changes detected - recompiling the module! :dependency
2026-11-17T17:34:24.8274696Z [INFO] Compiling 30 source files with javac [debug release 17] to target/test-classes
2026-11-17T17:34:25.2534595Z [INFO] /opt/ads-agent/_work/36/s/siemp-web/src/test/java/br/gov/caixa/siemp/apresentacao/consignacao/consultaTabelaDeTACDeConvenio/ConsultaTabelaDeTACDeConvenioHelpersTest.java: Some input files use or override a deprecated API.
2026-11-17T17:34:25.2535288Z [INFO] /opt/ads-agent/_work/36/s/siemp-web/src/test/java/br/gov/caixa/siemp/apresentacao/consignacao/consultaTabelaDeTACDeConvenio/ConsultaTabelaDeTACDeConvenioHelpersTest.java: Recompile with -Xlint:deprecation for details.
2026-11-17T17:34:25.2536118Z [INFO] /opt/ads-agent/_work/36/s/siemp-web/src/test/java/br/gov/caixa/siemp/comum/apresentacao/login/LoginMenuConsultasTest.java: /opt/ads-agent/_work/36/s/siemp-web/src/test/java/br/gov/caixa/siemp/comum/apresentacao/login/LoginMenuConsultasTest.java uses unchecked or unsafe operations.
2026-11-17T17:34:25.2536653Z [INFO] /opt/ads-agent/_work/36/s/siemp-web/src/test/java/br/gov/caixa/siemp/comum/apresentacao/login/LoginMenuConsultasTest.java: Recompile with -Xlint:unchecked for details.
2026-11-17T17:34:25.2536947Z [INFO] 
2026-11-17T17:34:25.2537404Z [INFO] --- maven-surefire-plugin:3.2.5:test (default-test) @ siemp-web ---
2026-11-17T17:34:25.3772092Z [INFO] Using auto detected provider org.apache.maven.surefire.junit4.JUnit4Provider
2026-11-17T17:34:25.4046554Z [INFO] 
2026-11-17T17:34:25.4047191Z [INFO] -------------------------------------------------------
2026-11-17T17:34:25.4047592Z [INFO]  T E S T S
2026-11-17T17:34:25.4047813Z [INFO] -------------------------------------------------------
2026-11-17T17:34:25.8509250Z [INFO] Running teste.br.gov.caixa.siemp.comum.apresentacao.testeerromultiplo.TesteErroMultiploActionTest
2026-11-17T17:34:25.9108922Z log4j:WARN No appenders could be found for logger (org.apache.struts.util.PropertyMessageResources).
2026-11-17T17:34:25.9109246Z log4j:WARN Please initialize the log4j system properly.
2026-11-17T17:34:25.9636090Z [INFO] Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.094 s -- in teste.br.gov.caixa.siemp.comum.apresentacao.testeerromultiplo.TesteErroMultiploActionTest
2026-11-17T17:34:25.9636441Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaTabelaDeTaxasDeConvenio.ConsultaTabelaDeTaxasDeConvenioHelpersTest
2026-11-17T17:34:25.9714701Z [INFO] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.001 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaTabelaDeTaxasDeConvenio.ConsultaTabelaDeTaxasDeConvenioHelpersTest
2026-11-17T17:34:25.9715059Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaTabelaDeTACDeConvenio.ConsultaTabelaDeTACDeConvenioHelpersTest
2026-11-17T17:34:25.9894382Z [INFO] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.001 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaTabelaDeTACDeConvenio.ConsultaTabelaDeTACDeConvenioHelpersTest
2026-11-17T17:34:25.9923010Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultarDadosConvenio.ConsultarDadosConvenioHelpersTest
2026-11-17T17:34:25.9964675Z [INFO] Tests run: 10, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.002 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultarDadosConvenio.ConsultarDadosConvenioHelpersTest
2026-11-17T17:34:25.9965157Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.ajustaExtratoDoConvenio.AjustaExtratoDoConvenioTotalizadorHelperTest
2026-11-17T17:34:26.0003533Z [INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.003 s -- in br.gov.caixa.siemp.apresentacao.consignacao.ajustaExtratoDoConvenio.AjustaExtratoDoConvenioTotalizadorHelperTest
2026-11-17T17:34:26.0004089Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultarComiteDeAutorizacoes.ConsultarComiteDeAutorizacoesHelpersTest
2026-11-17T17:34:26.0093316Z [INFO] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.004 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultarComiteDeAutorizacoes.ConsultarComiteDeAutorizacoesHelpersTest
2026-11-17T17:34:26.0093751Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaMovimentoDeAcertoDoConvenioNovo.ConsultaMovimentoDeAcertoDoConvenioHelperTest
2026-11-17T17:34:26.0097471Z [INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.002 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaMovimentoDeAcertoDoConvenioNovo.ConsultaMovimentoDeAcertoDoConvenioHelperTest
2026-11-17T17:34:26.0097783Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioParametroHelperTest
2026-11-17T17:34:26.0189561Z [INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.004 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioParametroHelperTest
2026-11-17T17:34:26.0189973Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioHelperTest
2026-11-17T17:34:26.0227540Z [INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.002 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioHelperTest
2026-11-17T17:34:26.0227952Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioHistoricosHelperTest
2026-11-17T17:34:26.0248207Z [INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.002 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaHistoricoDoConvenio.ConsultaHistoricoDoConvenioHistoricosHelperTest
2026-11-17T17:34:26.0248565Z [INFO] Running br.gov.caixa.siemp.apresentacao.consignacao.consultaConveniosExtratoAtraso.ConsultaConveniosExtratoAtrasoHelperColecoesTest
2026-11-17T17:34:26.0265569Z [INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.001 s -- in br.gov.caixa.siemp.apresentacao.consignacao.consultaConveniosExtratoAtraso.ConsultaConveniosExtratoAtrasoHelperColecoesTest
2026-11-17T17:34:26.0265937Z [INFO] Running br.gov.caixa.siemp.apresentacao.evolucao.estornarpagamento.EstornarPagamentoACTTest
2026-11-17T17:34:26.1979748Z Criando Log de Sistema
2026-11-17T17:34:26.1980118Z Log do Sitema inicializada!
2026-11-17T17:34:26.2803715Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.2804386Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:34:26.2804581Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.2804748Z GRAVE: falha na procedure
2026-11-17T17:34:26.2804916Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.2805119Z GRAVE: Erro ao fechar PreparedStatement do SIRIC: 
2026-11-17T17:34:26.2805308Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.2805435Z GRAVE: falha ao fechar
2026-11-17T17:34:26.2805601Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.2805881Z GRAVE: Erro ao fechar conexao com o SIRIC: 
2026-11-17T17:34:26.2806053Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.2806223Z GRAVE: falha ao fechar
2026-11-17T17:34:26.4564398Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4564720Z GRAVE: Erro de SQL: jdbc/SybaseSiempDS
2026-11-17T17:34:26.4763938Z [INFO] Tests run: 26, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.445 s -- in br.gov.caixa.siemp.apresentacao.evolucao.estornarpagamento.EstornarPagamentoACTTest
2026-11-17T17:34:26.4764432Z [INFO] Running br.gov.caixa.siemp.apresentacao.evolucao.SiricEstornoTest
2026-11-17T17:34:26.4771469Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4771841Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:34:26.4772124Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4772347Z GRAVE: falha na execucao
2026-11-17T17:34:26.4772550Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4772876Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:34:26.4773257Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4773471Z GRAVE: falha na execucao
2026-11-17T17:34:26.4802699Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4803065Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:34:26.4803249Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4803434Z GRAVE: falha na execucao
2026-11-17T17:34:26.4803659Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4809035Z GRAVE: Erro ao fechar PreparedStatement do SIRIC: 
2026-11-17T17:34:26.4809250Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4809530Z GRAVE: falha ao fechar statement
2026-11-17T17:34:26.4809969Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4810284Z GRAVE: Erro ao fechar conexao com o SIRIC: 
2026-11-17T17:34:26.4810475Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4810645Z GRAVE: falha ao fechar conexao
2026-11-17T17:34:26.4810777Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4851648Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:34:26.4852081Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4852257Z GRAVE: falha na execucao
2026-11-17T17:34:26.4852536Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4852736Z GRAVE: Erro ao fechar PreparedStatement do SIRIC: 
2026-11-17T17:34:26.4852911Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4853042Z GRAVE: falha ao fechar statement
2026-11-17T17:34:26.4853238Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4853416Z GRAVE: Erro ao fechar conexao com o SIRIC: 
2026-11-17T17:34:26.4853588Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4853749Z GRAVE: falha ao fechar conexao
2026-11-17T17:34:26.4853950Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4854200Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:34:26.4854733Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4855081Z GRAVE: falha na preparacao
2026-11-17T17:34:26.4855501Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4855874Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:34:26.4856061Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.4856227Z GRAVE: falha na preparacao
2026-11-17T17:34:26.4865992Z [INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.006 s -- in br.gov.caixa.siemp.apresentacao.evolucao.SiricEstornoTest
2026-11-17T17:34:26.4866275Z [INFO] Running br.gov.caixa.siemp.apresentacao.evolucao.estornarconcessaoemprestimo.EstornarConcessaoEmprestimoACTTest
2026-11-17T17:34:26.5041165Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.5041818Z GRAVE: Não foi possível executar a procedure do SIRIC: 
2026-11-17T17:34:26.5041975Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.5042168Z GRAVE: falha na procedure
2026-11-17T17:34:26.5042336Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.5042510Z GRAVE: Erro ao fechar PreparedStatement do SIRIC: 
2026-11-17T17:34:26.5042710Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.5042866Z GRAVE: falha ao fechar
2026-11-17T17:34:26.5043136Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.5043269Z GRAVE: Erro ao fechar conexao com o SIRIC: 
2026-11-17T17:34:26.5043640Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.5043819Z GRAVE: falha ao fechar
2026-11-17T17:34:26.5117418Z nov. 17, 2026 2:34:26 PM br.gov.caixa.framework.log.Log4Java error
2026-11-17T17:34:26.5117605Z GRAVE: Erro de SQL: jdbc/SybaseSiempDS
2026-11-17T17:34:26.5222073Z [INFO] Tests run: 11, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.033 s -- in br.gov.caixa.siemp.apresentacao.evolucao.estornarconcessaoemprestimo.EstornarConcessaoEmprestimoACTTest
2026-11-17T17:34:26.5222352Z [INFO] Running br.gov.caixa.siemp.comum.apresentacao.login.LoginActionTest
2026-11-17T17:34:26.5240742Z [INFO] Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.001 s -- in br.gov.caixa.siemp.comum.apresentacao.login.LoginActionTest
2026-11-17T17:34:26.5241401Z [INFO] Running br.gov.caixa.siemp.comum.apresentacao.login.LoginMenuConsultasTest
2026-11-17T17:34:26.5284699Z [INFO] Tests run: 12, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.003 s -- in br.gov.caixa.siemp.comum.apresentacao.login.LoginMenuConsultasTest
2026-11-17T17:34:26.5285157Z [INFO] Running br.gov.caixa.siemp.comum.apresentacao.SiempActionTest
2026-11-17T17:34:26.5377743Z [INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.007 s -- in br.gov.caixa.siemp.comum.apresentacao.SiempActionTest
2026-11-17T17:34:26.5377965Z [INFO] Running br.gov.caixa.siemp.consultas.ConsultasContratoTest
2026-11-17T17:34:27.0960855Z [WARNING] Tests run: 180, Failures: 0, Errors: 0, Skipped: 13, Time elapsed: 0.550 s -- in br.gov.caixa.siemp.consultas.ConsultasContratoTest
2026-11-17T17:34:27.0961721Z [INFO] Running br.gov.caixa.siemp.consultas.ConfiguracaoJstlValidatorTest
2026-11-17T17:34:27.1117192Z [INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.013 s -- in br.gov.caixa.siemp.consultas.ConfiguracaoJstlValidatorTest
2026-11-17T17:34:27.1117488Z [INFO] Running br.gov.caixa.siemp.consultas.ConveniosActionsTest
2026-11-17T17:34:27.1296504Z [INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.016 s -- in br.gov.caixa.siemp.consultas.ConveniosActionsTest
2026-11-17T17:34:27.1296780Z [INFO] Running br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest
2026-11-17T17:34:27.2046168Z org.apache.commons.fileupload.FileUploadBase$SizeLimitExceededException: the request was rejected because its size (5243003) exceeds the configured maximum (5242880)
2026-11-17T17:34:27.2046656Z 	at org.apache.commons.fileupload.FileUploadBase$FileItemIteratorImpl.<init>(FileUploadBase.java:965)
2026-11-17T17:34:27.2046900Z 	at org.apache.commons.fileupload.FileUploadBase.getItemIterator(FileUploadBase.java:310)
2026-11-17T17:34:27.2047176Z 	at org.apache.commons.fileupload.FileUploadBase.parseRequest(FileUploadBase.java:334)
2026-11-17T17:34:27.2047420Z 	at org.apache.commons.fileupload.FileUploadBase.parseRequest(FileUploadBase.java:288)
2026-11-17T17:34:27.2047833Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServlet.obterArquivoLegivel(AtualizarIndiceBovespaServlet.java:77)
2026-11-17T17:34:27.2048119Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServlet.doPost(AtualizarIndiceBovespaServlet.java:55)
2026-11-17T17:34:27.2048407Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest.deveRejeitarUploadAcimaDeCincoMegabytes(AtualizarIndiceBovespaServletTest.java:111)
2026-11-17T17:34:27.2048665Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:27.2048878Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:27.2049123Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:27.2049344Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:27.2049520Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:27.2049759Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:27.2050003Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:27.2050219Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:27.2050424Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:27.2050633Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:27.2050848Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:27.2051400Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:27.2051568Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:27.2051926Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:27.2052128Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:27.2052424Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:27.2052619Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:27.2052824Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:27.2053048Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:27.2053280Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:27.2053469Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:27.2053701Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:27.2054006Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:27.2054219Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:27.2054447Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:27.2061623Z java.lang.Exception: falha
2026-11-17T17:34:27.2061851Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest$3.atualizarIndice(AtualizarIndiceBovespaServletTest.java:206)
2026-11-17T17:34:27.2062143Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServlet.processarAtualizacao(AtualizarIndiceBovespaServlet.java:112)
2026-11-17T17:34:27.2062430Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServlet.doPost(AtualizarIndiceBovespaServlet.java:63)
2026-11-17T17:34:27.2062707Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest.executarComDelegate(AtualizarIndiceBovespaServletTest.java:249)
2026-11-17T17:34:27.2062968Z 	at br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest.deveTratarFalhaNaAtualizacao(AtualizarIndiceBovespaServletTest.java:212)
2026-11-17T17:34:27.2063594Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:27.2063798Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:27.2064045Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:27.2064265Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:27.2064603Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:27.2064826Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:27.2065065Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:27.2065294Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:27.2065527Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:27.2065704Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:27.2065921Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:27.2066123Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:27.2066318Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:27.2066523Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:27.2066732Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:27.2066927Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:27.2067272Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:27.2067441Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:27.2067681Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:27.2067946Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:27.2068170Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:27.2068401Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:27.2068631Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:27.2068842Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:27.2069045Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:27.2132151Z [INFO] Tests run: 14, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.081 s -- in br.gov.caixa.siemp.indicebovespa.atualiza.AtualizarIndiceBovespaServletTest
2026-11-17T17:34:27.2132541Z [INFO] Running br.gov.caixa.siemp.creditorural.bndes.CobrancaBNDESActionTest
2026-11-17T17:34:27.2249496Z [INFO] Tests run: 6, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.009 s -- in br.gov.caixa.siemp.creditorural.bndes.CobrancaBNDESActionTest
2026-11-17T17:34:27.2249823Z [INFO] Running br.gov.caixa.siemp.creditorural.extrato.ExtratoCreditoRuralActionTest
2026-11-17T17:34:27.2287225Z [INFO] Tests run: 2, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.002 s -- in br.gov.caixa.siemp.creditorural.extrato.ExtratoCreditoRuralActionTest
2026-11-17T17:34:27.2287488Z [INFO] Running br.gov.caixa.siemp.relatorios.ModelosJasperTest
2026-11-17T17:34:29.0723962Z [ERROR] Tests run: 52, Failures: 0, Errors: 26, Skipped: 0, Time elapsed: 1.828 s <<< FAILURE! -- in br.gov.caixa.siemp.relatorios.ModelosJasperTest
2026-11-17T17:34:29.0724684Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarParametrosDoConvenio.jasper] -- Time elapsed: 0.946 s <<< ERROR!
2026-11-17T17:34:29.0725120Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarParametrosDoConvenio_1794936868163_643305.java 
2026-11-17T17:34:29.0725415Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0725709Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0725959Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0726209Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0726472Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0726693Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0726930Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0727151Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0727398Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0727629Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0727861Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0728089Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0728442Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0729022Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0729207Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0729487Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0729756Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0730170Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0730372Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0730569Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0730871Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0731196Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0731393Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0731585Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0731732Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0731929Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0732124Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0732497Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0732700Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0732918Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0733112Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0733281Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0733504Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0733741Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0733967Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0734190Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0734406Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0734617Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0734834Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0735236Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0735410Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0735622Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0735810Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0736007Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0736221Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0736559Z 	... 38 more
2026-11-17T17:34:29.0736791Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0736975Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0737124Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0737323Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0737881Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0738047Z 	... 42 more
2026-11-17T17:34:29.0738087Z 
2026-11-17T17:34:29.0738422Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarParametrosDoConvenioReport.jasper] -- Time elapsed: 0.055 s <<< ERROR!
2026-11-17T17:34:29.0738874Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarParametrosDoConvenioReport_1794936868270_191526.java 
2026-11-17T17:34:29.0739131Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0739367Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0739641Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0739875Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0740467Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0740717Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0741075Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0741303Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0741543Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0741884Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0742104Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0742376Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0742691Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0743036Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0743363Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0743670Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0744015Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0744359Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0744695Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0744974Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0745305Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0745588Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0745868Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0746180Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0746447Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0746695Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0746983Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0747234Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0747540Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0747746Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0747934Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0748137Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0748437Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0748756Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0749029Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0749215Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0749558Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0749773Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0749979Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0750474Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0750686Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0750950Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0751311Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0751485Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0751705Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0751888Z 	... 38 more
2026-11-17T17:34:29.0752124Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0752305Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0752486Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0752678Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0752884Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0753009Z 	... 42 more
2026-11-17T17:34:29.0753084Z 
2026-11-17T17:34:29.0753413Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarTabelaDeTACDoConvenio.jasper] -- Time elapsed: 0.105 s <<< ERROR!
2026-11-17T17:34:29.0753776Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarTabelaDeTACDoConvenio_1794936868377_930329.java 
2026-11-17T17:34:29.0754035Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0754269Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0754581Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0754828Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0755055Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0755317Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0755557Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0755768Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0756005Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0756186Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0756392Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0756617Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0756838Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0757051Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0757273Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0757492Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0757704Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0757956Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0758118Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0758314Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0758509Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0758985Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0759214Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0759411Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0759594Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0759746Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0760728Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0761141Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0761403Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0761599Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0761791Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0762012Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0762286Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0762479Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0762703Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0762925Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0763145Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0763358Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0763564Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0763900Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0764108Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0764324Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0764543Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0764742Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0764947Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0765126Z 	... 38 more
2026-11-17T17:34:29.0765347Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0765527Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0765724Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0765879Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0766071Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0766248Z 	... 42 more
2026-11-17T17:34:29.0766324Z 
2026-11-17T17:34:29.0766605Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarTabelaDeTACDoConvenioNovo.jasper] -- Time elapsed: 0.070 s <<< ERROR!
2026-11-17T17:34:29.0767005Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarTabelaDeTACDoConvenioNovo_1794936868449_607773.java 
2026-11-17T17:34:29.0767262Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0767499Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0767873Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0768112Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0768362Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0768662Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0768893Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0769133Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0769341Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0769568Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0769782Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0770009Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0770231Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0770473Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0770677Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0770944Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0771317Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0771555Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0771755Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0771964Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0772195Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0772439Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0772637Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0772837Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0772987Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0773195Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0773405Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0773603Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0773805Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0774003Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0774417Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0774690Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0774878Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0775111Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0775335Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0775572Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0775806Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0776051Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0776260Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0776651Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0776873Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0777039Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0777244Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0777466Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0777688Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0777893Z 	... 38 more
2026-11-17T17:34:29.0778134Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0778315Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0778510Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0778665Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0778875Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0779051Z 	... 42 more
2026-11-17T17:34:29.0779091Z 
2026-11-17T17:34:29.0779421Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarTabelaDeTACDoConvenioSubReport.jasper] -- Time elapsed: 0.050 s <<< ERROR!
2026-11-17T17:34:29.0779834Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarTabelaDeTACDoConvenioSubReport_1794936868518_229155.java 
2026-11-17T17:34:29.0780096Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0780349Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0780589Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0780839Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0781168Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0781426Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0781749Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0782042Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0782252Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0782465Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0782694Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0782915Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0783147Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0783362Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0784184Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0784423Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0784678Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0784848Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0785043Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0785239Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0785437Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0785689Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0785867Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0786076Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0786254Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0786435Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0786629Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0786823Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0787017Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0787211Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0787401Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0787665Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0787915Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0788107Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0788330Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0788552Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0788766Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0788973Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0789180Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0789479Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0789691Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0789860Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0790068Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0790244Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0790447Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0790627Z 	... 38 more
2026-11-17T17:34:29.0790896Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0791190Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0791387Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0791542Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0791734Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0791911Z 	... 42 more
2026-11-17T17:34:29.0791951Z 
2026-11-17T17:34:29.0792282Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarTabelaDeTaxasDoConvenio.jasper] -- Time elapsed: 0.041 s <<< ERROR!
2026-11-17T17:34:29.0792674Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarTabelaDeTaxasDoConvenio_1794936868566_790441.java 
2026-11-17T17:34:29.0792936Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0793170Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0793413Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0793657Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0793885Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0794191Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0794446Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0794706Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0795086Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0795360Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0795657Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0795934Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0796153Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0796368Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0796596Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0796798Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0796979Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0797182Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0797378Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0797668Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0797948Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0798147Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0798333Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0798532Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0798681Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0798867Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0799087Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0799295Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0799493Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0799685Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0799875Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0800046Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0800264Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0800540Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0800871Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0801220Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0801447Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0801658Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0801943Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0802327Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0802502Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0802702Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0802909Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0803155Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0804273Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0804549Z 	... 38 more
2026-11-17T17:34:29.0804805Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0805050Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0805201Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0805392Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0805589Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0805787Z 	... 42 more
2026-11-17T17:34:29.0805830Z 
2026-11-17T17:34:29.0806167Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarTabelaDeTaxasDoConvenioNovo.jasper] -- Time elapsed: 0.032 s <<< ERROR!
2026-11-17T17:34:29.0806569Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarTabelaDeTaxasDoConvenioNovo_1794936868604_68899.java 
2026-11-17T17:34:29.0806828Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0807061Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0807304Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0807531Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0807759Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0808034Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0808227Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0808474Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0808712Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0808927Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0809129Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0809352Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0809567Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0809786Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0810016Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0810193Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0810404Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0810608Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0810801Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0811000Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0811382Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0811577Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0811735Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0811928Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0812622Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0812813Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0813074Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0813269Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0813997Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0814267Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0814546Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0814790Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0815008Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0815270Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0815491Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0815712Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0815935Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0816145Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0816317Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0816631Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0816984Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0817277Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0817513Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0817692Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0817897Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0818074Z 	... 38 more
2026-11-17T17:34:29.0818268Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0818450Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0818640Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0818832Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0819028Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0819200Z 	... 42 more
2026-11-17T17:34:29.0819240Z 
2026-11-17T17:34:29.0819567Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[consignacao/consultarTabelaDeTaxasDoConvenioSubReport.jasper] -- Time elapsed: 0.020 s <<< ERROR!
2026-11-17T17:34:29.0819975Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarTabelaDeTaxasDoConvenioSubReport_1794936868627_803957.java 
2026-11-17T17:34:29.0820238Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0820481Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0820724Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0820954Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0821316Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0821562Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0821803Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0822016Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0822316Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0822539Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0822743Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0823002Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0823220Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0823405Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0823608Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0823826Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0824041Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0824253Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0824491Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0824752Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0824950Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0825114Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0825327Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0825507Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0825701Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0825884Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0826083Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0826279Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0826478Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0826638Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0826833Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0827031Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0827252Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0827495Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0827724Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0827939Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0828149Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0828323Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0828523Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0828814Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0829012Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0829214Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0829417Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0829603Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0829803Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0829943Z 	... 38 more
2026-11-17T17:34:29.0830163Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0830342Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0830564Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0830750Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0830941Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0831193Z 	... 42 more
2026-11-17T17:34:29.0831287Z 
2026-11-17T17:34:29.0831604Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/relatorioExtratoCreditoRural.jasper] -- Time elapsed: 0.037 s <<< ERROR!
2026-11-17T17:34:29.0831988Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/relatorioExtratoCreditoRural_1794936868665_322636.java 
2026-11-17T17:34:29.0832238Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0832499Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0832708Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0832940Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0833172Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0833429Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0833672Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0833881Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0834115Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0834325Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0834611Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0834804Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0835023Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0835247Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0835448Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0835669Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0835880Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0836085Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0836281Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0836479Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0836643Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0836837Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0837039Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0837222Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0837504Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0837700Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0837892Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0838053Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0838246Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0838440Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0838698Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0838901Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0839120Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0839368Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0839616Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0839800Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0840015Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0840255Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0840469Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0840767Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0840973Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0841259Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0841466Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0841648Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0841820Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0841997Z 	... 38 more
2026-11-17T17:34:29.0842228Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0842410Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0842590Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0842778Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0842974Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0843097Z 	... 42 more
2026-11-17T17:34:29.0843186Z 
2026-11-17T17:34:29.0843496Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/subRelatorioExtrato.jasper] -- Time elapsed: 0.009 s <<< ERROR!
2026-11-17T17:34:29.0843875Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioExtrato_1794936868679_474975.java 
2026-11-17T17:34:29.0844089Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0844336Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0844689Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0844939Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0845166Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0845405Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0845650Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0845861Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0846108Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0846408Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0846657Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0846960Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0847341Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0847724Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0848027Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0848408Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0848796Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0849098Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0849369Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0849683Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0849981Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0850305Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0850603Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0850901Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0851480Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0851813Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0852090Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0852433Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0852715Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0852973Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0853272Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0853611Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0853990Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0854419Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0854743Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0855104Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0855476Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0855828Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0856174Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0856727Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0857069Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0857407Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0857682Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0858011Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0858360Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0858655Z 	... 38 more
2026-11-17T17:34:29.0859013Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0859312Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0859615Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0859926Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0860203Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0860474Z 	... 42 more
2026-11-17T17:34:29.0860614Z 
2026-11-17T17:34:29.0861170Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/subRelatorioLiberacoes.jasper] -- Time elapsed: 0.010 s <<< ERROR!
2026-11-17T17:34:29.0861998Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioLiberacoes_1794936868690_265321.java 
2026-11-17T17:34:29.0862484Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0862878Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0863290Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0863698Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0864087Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0864494Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0864919Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0865281Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0865648Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0866016Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0866364Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0866739Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0867127Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0867499Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0867839Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0868212Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0868579Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0868890Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0869212Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0869553Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0869898Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0870230Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0870546Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0870857Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0871187Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0871530Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0871863Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0872196Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0872534Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0872874Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0873193Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0873534Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0873865Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0874286Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0874672Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0875140Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0875507Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0875881Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0879528Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0880065Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0880409Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0881464Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0882085Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0882457Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0882816Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0883131Z 	... 38 more
2026-11-17T17:34:29.0883504Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0883801Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0884065Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0884373Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0884669Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0884908Z 	... 42 more
2026-11-17T17:34:29.0884972Z 
2026-11-17T17:34:29.0885482Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/subRelatorioOcorrencias.jasper] -- Time elapsed: 0.008 s <<< ERROR!
2026-11-17T17:34:29.0886139Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioOcorrencias_1794936868699_229619.java 
2026-11-17T17:34:29.0886574Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0886990Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0887408Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0887803Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0888189Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0888613Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0888956Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0889342Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0889759Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0890119Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0890461Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0890837Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0891298Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0891713Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0892057Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0892368Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0892902Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0893244Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0893570Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0893898Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0894288Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0894598Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0895479Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0895742Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0896029Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0896388Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0896723Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0897066Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0897395Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0897715Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0897991Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0898335Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0898733Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0899119Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0899510Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0899876Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0900235Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0900587Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0900940Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0901481Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0901826Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0902393Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0902708Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0903025Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0903372Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0903659Z 	... 38 more
2026-11-17T17:34:29.0904019Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0904274Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0904605Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0904928Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0905246Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0905511Z 	... 42 more
2026-11-17T17:34:29.0905580Z 
2026-11-17T17:34:29.0906115Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/subRelatorioPosicaoDivida.jasper] -- Time elapsed: 0.009 s <<< ERROR!
2026-11-17T17:34:29.0906746Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioPosicaoDivida_1794936868711_813344.java 
2026-11-17T17:34:29.0907166Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0907662Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0908087Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0908480Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0908893Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0909310Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0909691Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0910033Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0910387Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0910695Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0910987Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0911381Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0911696Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0911918Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0912134Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0912338Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0912574Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0912779Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0912975Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0913186Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0913665Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0913895Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0914096Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0914282Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0914513Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0914808Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0915017Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0915224Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0915451Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0915616Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0915814Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0916017Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0916241Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0916473Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0916711Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0916933Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0917163Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0917338Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0917544Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0917938Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0918148Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0918350Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0918589Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0918796Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0919004Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0919217Z 	... 38 more
2026-11-17T17:34:29.0919511Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0919771Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0920035Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0920331Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0920635Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0920865Z 	... 42 more
2026-11-17T17:34:29.0920928Z 
2026-11-17T17:34:29.0921406Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/subRelatorioProAgro.jasper] -- Time elapsed: 0.012 s <<< ERROR!
2026-11-17T17:34:29.0921800Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioProAgro_1794936868724_87303.java 
2026-11-17T17:34:29.0922050Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0922285Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0922494Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0922733Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0922959Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0923203Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0923437Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0923670Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0923936Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0924148Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0924350Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0924642Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0924827Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0925045Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0925252Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0925465Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0925696Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0925898Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0926087Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0926279Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0926443Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0926705Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0926899Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0927090Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0927274Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0927515Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0927707Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0927874Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0928068Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0928260Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0928448Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0928658Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0928893Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0929241Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0929629Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0929992Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0930281Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0930497Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0930706Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0931091Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0931305Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0931504Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0931690Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0932052Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0932240Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0932419Z 	... 38 more
2026-11-17T17:34:29.0932649Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0932835Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0933039Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0933291Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0933483Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0933610Z 	... 42 more
2026-11-17T17:34:29.0933687Z 
2026-11-17T17:34:29.0934022Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/subRelatorioReembolsos.jasper] -- Time elapsed: 0.008 s <<< ERROR!
2026-11-17T17:34:29.0934421Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioReembolsos_1794936868733_789753.java 
2026-11-17T17:34:29.0934720Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0934924Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0935179Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0935409Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0935640Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0935955Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0936199Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0936434Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0936733Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0936954Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0937126Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0937347Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0937562Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0937778Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0937983Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0938193Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0938423Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0938641Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0938802Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0939007Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0939213Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0939513Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0939826Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0940164Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0940447Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0940706Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0940865Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0941156Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0941357Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0941555Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0941749Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0941957Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0942176Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0942402Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0942592Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0942841Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0943061Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0943275Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0943485Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0943793Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0944000Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0944198Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0944354Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0944659Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0944931Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0945112Z 	... 38 more
2026-11-17T17:34:29.0945335Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0945558Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0945740Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0945929Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0946088Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0946260Z 	... 42 more
2026-11-17T17:34:29.0946333Z 
2026-11-17T17:34:29.0946618Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[creditoRural/subRelatorioReembolsosVencidos.jasper] -- Time elapsed: 0.012 s <<< ERROR!
2026-11-17T17:34:29.0947057Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioReembolsosVencidos_1794936868746_947092.java 
2026-11-17T17:34:29.0947424Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0947742Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0948048Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0948286Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0948559Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0948818Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0949045Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:29.0949281Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:29.0949482Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0949701Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0949908Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0950225Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0950551Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0950901Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0951318Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0951541Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0951780Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0951951Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0952151Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0952353Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0952546Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0952740Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0952944Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0953128Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0953383Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0953586Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0953878Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0954074Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0954270Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0954509Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0954769Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0954968Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0955156Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0955379Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0955600Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0955841Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0956057Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0956264Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0956520Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0956844Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0957049Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0957214Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0957399Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0957653Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0957883Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0958066Z 	... 38 more
2026-11-17T17:34:29.0958302Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0958482Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0958632Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0958828Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0959030Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0959190Z 	... 42 more
2026-11-17T17:34:29.0959230Z 
2026-11-17T17:34:29.0959572Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPlanilhaEvolucaoDivida/relatorioEvolucaoDivida.jasper] -- Time elapsed: 0.065 s <<< ERROR!
2026-11-17T17:34:29.0959980Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/relatorioEvolucaoDivida_1794936868811_995881.java 
2026-11-17T17:34:29.0960233Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0960479Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0960720Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0961160Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0961527Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0961905Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0962249Z 	at jdk.internal.reflect.GeneratedMethodAccessor123.invoke(Unknown Source)
2026-11-17T17:34:29.0962442Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0962747Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0962972Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0963195Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0963454Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0963669Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0963876Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0964079Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0964263Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0964534Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0964765Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0964969Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0965190Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0965385Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0965578Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0965761Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0965906Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0966093Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0966296Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0966512Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0966709Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0966906Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0967097Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0967299Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0967490Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0967717Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0967939Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0968166Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0968400Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0968607Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0968811Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0969121Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0969290Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0969490Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0969681Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0969867Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0970071Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0970257Z 	... 37 more
2026-11-17T17:34:29.0970478Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0970657Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0970805Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0971228Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0971526Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0971771Z 	... 41 more
2026-11-17T17:34:29.0971832Z 
2026-11-17T17:34:29.0972372Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPlanilhaEvolucaoDivida/subRelatorioEvolucaoDivida.jasper] -- Time elapsed: 0.020 s <<< ERROR!
2026-11-17T17:34:29.0973055Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioEvolucaoDivida_1794936868835_316059.java 
2026-11-17T17:34:29.0973504Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0973892Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0974233Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0974523Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0974771Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0975012Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0975204Z 	at jdk.internal.reflect.GeneratedMethodAccessor123.invoke(Unknown Source)
2026-11-17T17:34:29.0975419Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0975631Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0975855Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0976075Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0976297Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0976511Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0976722Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0976930Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0977112Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0977318Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0977513Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0977724Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0977919Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0978114Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0978317Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0978499Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0978647Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0978834Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0979026Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0979221Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0979432Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0979622Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0979807Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0979976Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0980235Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0980653Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0981094Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0981340Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0981622Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0981855Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0982070Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0982381Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0982554Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0982748Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0982946Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0983129Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0983331Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0983512Z 	... 37 more
2026-11-17T17:34:29.0983746Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0983964Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0984246Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0984535Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0984817Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0985065Z 	... 41 more
2026-11-17T17:34:29.0985130Z 
2026-11-17T17:34:29.0985661Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPlanilhaEvolucaoDivida/subRelatorioEvolucaoDividaAmortiz.jasper] -- Time elapsed: 0.021 s <<< ERROR!
2026-11-17T17:34:29.0986284Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioEvolucaoDivida_1794936868858_501042.java 
2026-11-17T17:34:29.0986657Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.0987066Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.0987428Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.0987866Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.0988232Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.0988517Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.0988746Z 	at jdk.internal.reflect.GeneratedMethodAccessor123.invoke(Unknown Source)
2026-11-17T17:34:29.0988964Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.0989183Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.0989385Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.0989647Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.0989867Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.0990081Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.0990284Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.0990535Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.0990753Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.0990955Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0991264Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0991519Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0991736Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0991930Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0992139Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0992392Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.0992670Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.0992975Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.0993287Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.0993613Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.0993934Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.0994288Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.0994584Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.0994830Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.0995057Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.0995284Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.0995507Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.0995738Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.0995956Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.0996160Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.0996384Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.0996679Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0996884Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.0997078Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.0997262Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.0997439Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.0997652Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.0997831Z 	... 37 more
2026-11-17T17:34:29.0998049Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.0998216Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.0998415Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.0998607Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.0998797Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.0998953Z 	... 41 more
2026-11-17T17:34:29.0998995Z 
2026-11-17T17:34:29.0999347Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPlanilhaEvolucaoDivida/subRelatorioEvolucaoDividaReneg.jasper] -- Time elapsed: 0.026 s <<< ERROR!
2026-11-17T17:34:29.0999765Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioEvolucaoDivida_1794936868885_573554.java 
2026-11-17T17:34:29.1000086Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.1000322Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.1000580Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.1000879Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.1001183Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.1001400Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.1001643Z 	at jdk.internal.reflect.GeneratedMethodAccessor123.invoke(Unknown Source)
2026-11-17T17:34:29.1001951Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.1002263Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.1002550Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.1002828Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.1003071Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.1003348Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.1003608Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.1003782Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.1003998Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.1004203Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.1004429Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.1004726Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.1004941Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.1005159Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.1005359Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.1005511Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.1005698Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.1005883Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.1006077Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.1006274Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.1006467Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.1006681Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.1006840Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.1007055Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.1007285Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.1007518Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.1007763Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.1007979Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.1008195Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.1008399Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.1008572Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.1008962Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.1009193Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.1009390Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.1009619Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.1009796Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.1010000Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.1010169Z 	... 37 more
2026-11-17T17:34:29.1010355Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.1010537Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.1010729Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.1010937Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.1011207Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.1011363Z 	... 41 more
2026-11-17T17:34:29.1011405Z 
2026-11-17T17:34:29.1011763Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPlanilhaEvolucaoDividaSeguradora/relatorioEvolucaoDividaSeguradora.jasper] -- Time elapsed: 0.041 s <<< ERROR!
2026-11-17T17:34:29.1012368Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/relatorioEvolucaoDividaSeguradora_1794936868928_392269.java 
2026-11-17T17:34:29.1012622Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.1012856Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.1013160Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.1013658Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.1013937Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.1014184Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.1014383Z 	at jdk.internal.reflect.GeneratedMethodAccessor123.invoke(Unknown Source)
2026-11-17T17:34:29.1014657Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.1014871Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.1015081Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.1015310Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.1015532Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.1015766Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.1015972Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.1016202Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.1016386Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.1016589Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.1016782Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.1016980Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.1017187Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.1017381Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.1017757Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.1017945Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.1018091Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.1018277Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.1018504Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.1018715Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.1018913Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.1019104Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.1019293Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.1019458Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.1019696Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.1019921Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.1020140Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.1020357Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.1020579Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.1020784Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.1020986Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.1021354Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.1021525Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.1021739Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.1021923Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.1022099Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.1022313Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.1022489Z 	... 37 more
2026-11-17T17:34:29.1022705Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.1022849Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.1023027Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.1023213Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.1023454Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.1023612Z 	... 41 more
2026-11-17T17:34:29.1023653Z 
2026-11-17T17:34:29.1024009Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPlanilhaEvolucaoDividaSeguradora/subRelatorioEvolucaoDividaSeguradora.jasper] -- Time elapsed: 0.009 s <<< ERROR!
2026-11-17T17:34:29.1024480Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioEvolucaoDividaSeguradora_1794936868940_666494.java 
2026-11-17T17:34:29.1024767Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.1024998Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.1025234Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.1025461Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.1025703Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.1025992Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.1026183Z 	at jdk.internal.reflect.GeneratedMethodAccessor123.invoke(Unknown Source)
2026-11-17T17:34:29.1026404Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.1026647Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.1026849Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.1027068Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.1027282Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.1027498Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.1027718Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.1027890Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.1028113Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.1028314Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.1028510Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.1028707Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.1028901Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.1029095Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.1029285Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.1029435Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.1029633Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.1029820Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.1030011Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.1030205Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.1030438Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.1030788Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.1031133Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.1031381Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.1031920Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.1032182Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.1032406Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.1032630Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.1032849Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.1033086Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.1033297Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.1033569Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.1033774Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.1033982Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.1034185Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.1034367Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.1034666Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.1034963Z 	... 37 more
2026-11-17T17:34:29.1035186Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.1035332Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.1035518Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.1035769Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.1035962Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.1036137Z 	... 41 more
2026-11-17T17:34:29.1036180Z 
2026-11-17T17:34:29.1036507Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPosicaoDivida/relatorioPosicaoDivida.jasper] -- Time elapsed: 0.036 s <<< ERROR!
2026-11-17T17:34:29.1036893Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida_1794936868976_238824.java 
2026-11-17T17:34:29.1037148Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.1037383Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.1037638Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.1037881Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.1038107Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.1038316Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.1038555Z 	at jdk.internal.reflect.GeneratedMethodAccessor123.invoke(Unknown Source)
2026-11-17T17:34:29.1038771Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.1038987Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.1039187Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.1039411Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.1039689Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.1039906Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.1040109Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.1040281Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.1040509Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.1040713Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.1040906Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.1041166Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.1041380Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.1041577Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.1041768Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.1041917Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.1042094Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.1042294Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.1042488Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.1042771Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.1043050Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.1043417Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.1043629Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.1043838Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.1044105Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.1044332Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.1044635Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.1044857Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.1045087Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.1045293Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.1045503Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.1045773Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.1045980Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.1046181Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.1046367Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.1046562Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.1046763Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.1046942Z 	... 37 more
2026-11-17T17:34:29.1047130Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.1047308Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.1047525Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.1047717Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.1047910Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.1048063Z 	... 41 more
2026-11-17T17:34:29.1048104Z 
2026-11-17T17:34:29.1048452Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/consultarPosicaoDivida/relatorioPosicaoDividaSeguradora.jasper] -- Time elapsed: 0.023 s <<< ERROR!
2026-11-17T17:34:29.1048865Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDividaSeguradora_1794936869001_898561.java 
2026-11-17T17:34:29.1049122Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.1049359Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.1049600Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.1049831Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.1050024Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.1050269Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.1050491Z 	at jdk.internal.reflect.GeneratedMethodAccessor123.invoke(Unknown Source)
2026-11-17T17:34:29.1050717Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.1050940Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.1051218Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.1051443Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.1051708Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.1051927Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.1052095Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.1052330Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.1052555Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.1052771Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.1052964Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.1053159Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.1053353Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.1053554Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.1053712Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.1053892Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.1054068Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.1054265Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.1054530Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.1054737Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.1054950Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.1055142Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.1055297Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.1055501Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.1055722Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.1055972Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.1056194Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.1056427Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.1056641Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.1056844Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.1057017Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.1057311Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.1057565Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.1057781Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.1057975Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.1058152Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.1058367Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.1058542Z 	... 37 more
2026-11-17T17:34:29.1058733Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.1058909Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.1059083Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.1059269Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.1059468Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.1059623Z 	... 41 more
2026-11-17T17:34:29.1059663Z 
2026-11-17T17:34:29.1060025Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/evolucaoDividaNCE/relatorioEvolucaoDividaNCE.jasper] -- Time elapsed: 0.026 s <<< ERROR!
2026-11-17T17:34:29.1060429Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/relatorioEvolucaoDividaNCE_1794936869026_651265.java 
2026-11-17T17:34:29.1060708Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.1060939Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.1061244Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.1061444Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.1061683Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.1061927Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.1062149Z 	at jdk.internal.reflect.GeneratedMethodAccessor123.invoke(Unknown Source)
2026-11-17T17:34:29.1062361Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.1062590Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.1062812Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.1063029Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.1063255Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.1063439Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.1063642Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.1063848Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.1064062Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.1064262Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.1064528Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.1064731Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.1064921Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.1065085Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.1065286Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.1065470Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.1065645Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.1065833Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.1066025Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.1066232Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.1066421Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.1066584Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.1066783Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.1066985Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.1067207Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.1067433Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.1067652Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.1068000Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.1068235Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.1068410Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.1068668Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.1068963Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.1069167Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.1069361Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.1069546Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.1069721Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.1069947Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.1070089Z 	... 37 more
2026-11-17T17:34:29.1070335Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.1070512Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.1070696Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.1070886Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.1071145Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.1071301Z 	... 41 more
2026-11-17T17:34:29.1071342Z 
2026-11-17T17:34:29.1071660Z [ERROR] br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual[evolucao/simularPrestacoes/simularPrestacoes.jasper] -- Time elapsed: 0.018 s <<< ERROR!
2026-11-17T17:34:29.1072055Z net.sf.jasperreports.engine.JRException: Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/simularPrestacoes_1794936869051_108161.java 
2026-11-17T17:34:29.1072322Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:89)
2026-11-17T17:34:29.1072553Z 	at net.sf.jasperreports.engine.design.JRAbstractClassCompiler.compileUnits(JRAbstractClassCompiler.java:63)
2026-11-17T17:34:29.1072790Z 	at net.sf.jasperreports.engine.design.JRAbstractCompiler.compileReport(JRAbstractCompiler.java:188)
2026-11-17T17:34:29.1072991Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:215)
2026-11-17T17:34:29.1073218Z 	at net.sf.jasperreports.engine.JasperCompileManager.compileReport(JasperCompileManager.java:148)
2026-11-17T17:34:29.1073459Z 	at br.gov.caixa.siemp.relatorios.ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual(ModelosJasperTest.java:67)
2026-11-17T17:34:29.1073681Z 	at jdk.internal.reflect.GeneratedMethodAccessor123.invoke(Unknown Source)
2026-11-17T17:34:29.1073899Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:29.1074126Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:29.1074343Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:29.1074669Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:29.1074970Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:29.1075208Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:29.1075413Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:29.1075616Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:29.1075826Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:29.1076037Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.1076281Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.1076490Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.1076683Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.1076847Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.1077069Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.1077249Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:29.1077426Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:29.1077638Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:29.1077826Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:29.1078020Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:29.1078180Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:29.1078392Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:29.1078582Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:29.1078780Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:29.1079000Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:29.1079235Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:29.1079456Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:29.1079670Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:29.1079884Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:29.1080059Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:29.1080284Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:29.1080573Z Caused by: java.io.IOException: Cannot run program "javac": error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.1080776Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1143)
2026-11-17T17:34:29.1080979Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1073)
2026-11-17T17:34:29.1081238Z 	at java.base/java.lang.Runtime.exec(Runtime.java:594)
2026-11-17T17:34:29.1081413Z 	at java.base/java.lang.Runtime.exec(Runtime.java:453)
2026-11-17T17:34:29.1081613Z 	at net.sf.jasperreports.engine.design.JRJavacCompiler.compileClasses(JRJavacCompiler.java:58)
2026-11-17T17:34:29.1081754Z 	... 37 more
2026-11-17T17:34:29.1081971Z Caused by: java.io.IOException: error=2, Arquivo ou diretório inexistente
2026-11-17T17:34:29.1082165Z 	at java.base/java.lang.ProcessImpl.forkAndExec(Native Method)
2026-11-17T17:34:29.1082345Z 	at java.base/java.lang.ProcessImpl.<init>(ProcessImpl.java:314)
2026-11-17T17:34:29.1082536Z 	at java.base/java.lang.ProcessImpl.start(ProcessImpl.java:244)
2026-11-17T17:34:29.1082736Z 	at java.base/java.lang.ProcessBuilder.start(ProcessBuilder.java:1110)
2026-11-17T17:34:29.1082888Z 	... 41 more
2026-11-17T17:34:29.1082931Z 
2026-11-17T17:34:29.1083082Z [INFO] Running br.gov.caixa.siemp.relatorios.RelatorioPosicaoDividaCalculatorTest
2026-11-17T17:34:29.7047870Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:235: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.7048255Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.7048575Z                                             ^
2026-11-17T17:34:29.7048876Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:245: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.7049091Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.7049486Z                                             ^
2026-11-17T17:34:29.7049793Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:255: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.7050011Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:34:29.7050345Z                                             ^
2026-11-17T17:34:29.7050635Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:270: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.7050846Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:34:29.8322601Z                                             ^
2026-11-17T17:34:29.8323245Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:365: warning: [removal] Boolean(boolean) in Boolean has been deprecated and marked for removal
2026-11-17T17:34:29.8323502Z                 value = (java.lang.Boolean)(new Boolean(((java.lang.String)field_nuParcela.getValue()) != null));
2026-11-17T17:34:29.8323666Z                                             ^
2026-11-17T17:34:29.8324060Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:370: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8324316Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:34:29.8324430Z                                             ^
2026-11-17T17:34:29.8324732Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:380: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8324948Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8325096Z                                             ^
2026-11-17T17:34:29.8325451Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:415: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8325676Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8325820Z                                             ^
2026-11-17T17:34:29.8326104Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:420: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8326337Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8326444Z                                             ^
2026-11-17T17:34:29.8326730Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:445: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8326941Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8327088Z                                             ^
2026-11-17T17:34:29.8327368Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:450: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8327580Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:34:29.8327723Z                                             ^
2026-11-17T17:34:29.8328012Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:503: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8328252Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8328359Z                                             ^
2026-11-17T17:34:29.8328647Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:513: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8328856Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8328997Z                                             ^
2026-11-17T17:34:29.8329280Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:523: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8329704Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:34:29.8329924Z                                             ^
2026-11-17T17:34:29.8330226Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:538: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8330462Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:34:29.8330620Z                                             ^
2026-11-17T17:34:29.8330910Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:633: warning: [removal] Boolean(boolean) in Boolean has been deprecated and marked for removal
2026-11-17T17:34:29.8331258Z                 value = (java.lang.Boolean)(new Boolean(((java.lang.String)field_nuParcela.getOldValue()) != null));
2026-11-17T17:34:29.8331426Z                                             ^
2026-11-17T17:34:29.8331713Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:638: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8331928Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:34:29.8332083Z                                             ^
2026-11-17T17:34:29.8332367Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:648: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8332540Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8332704Z                                             ^
2026-11-17T17:34:29.8332995Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:683: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8333201Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8333344Z                                             ^
2026-11-17T17:34:29.8333635Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:688: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8333854Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8333993Z                                             ^
2026-11-17T17:34:29.8334277Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:713: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8334446Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8334598Z                                             ^
2026-11-17T17:34:29.8334885Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:718: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8335094Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:34:29.8335236Z                                             ^
2026-11-17T17:34:29.8335525Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:771: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8335830Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8336009Z                                             ^
2026-11-17T17:34:29.8336262Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:781: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8336469Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8336629Z                                             ^
2026-11-17T17:34:29.8336917Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:791: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8337126Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:34:29.8337264Z                                             ^
2026-11-17T17:34:29.8337637Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:806: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8337842Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:34:29.8337983Z                                             ^
2026-11-17T17:34:29.8338267Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:901: warning: [removal] Boolean(boolean) in Boolean has been deprecated and marked for removal
2026-11-17T17:34:29.8338504Z                 value = (java.lang.Boolean)(new Boolean(((java.lang.String)field_nuParcela.getValue()) != null));
2026-11-17T17:34:29.8338684Z                                             ^
2026-11-17T17:34:29.8338990Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:906: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8339192Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:34:29.8339345Z                                             ^
2026-11-17T17:34:29.8339627Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:916: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8339832Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8339971Z                                             ^
2026-11-17T17:34:29.8340250Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:951: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8340468Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8340573Z                                             ^
2026-11-17T17:34:29.8340859Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:956: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8341206Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8341356Z                                             ^
2026-11-17T17:34:29.8341643Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:981: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8341850Z                 value = (java.lang.Integer)(new Integer(1));
2026-11-17T17:34:29.8341991Z                                             ^
2026-11-17T17:34:29.8342270Z /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida.java:986: warning: [removal] Integer(int) in Integer has been deprecated and marked for removal
2026-11-17T17:34:29.8342440Z                 value = (java.lang.Integer)(new Integer(0));
2026-11-17T17:34:29.8342593Z                                             ^
2026-11-17T17:34:29.8342724Z 33 warnings
2026-11-17T17:34:29.8495354Z [INFO] Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.772 s -- in br.gov.caixa.siemp.relatorios.RelatorioPosicaoDividaCalculatorTest
2026-11-17T17:34:29.8495854Z [INFO] Running br.gov.caixa.siemp.relatorios.ExportacaoPdfTest
2026-11-17T17:34:30.4250390Z [ERROR] Tests run: 6, Failures: 0, Errors: 6, Skipped: 0, Time elapsed: 0.571 s <<< FAILURE! -- in br.gov.caixa.siemp.relatorios.ExportacaoPdfTest
2026-11-17T17:34:30.4261772Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[nce: 0 registros] -- Time elapsed: 0.189 s <<< ERROR!
2026-11-17T17:34:30.4262183Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:34:30.4262461Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:34:30.4262697Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:34:30.4262888Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:34:30.4263140Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:34:30.4263603Z 	at net.sf.jasperreports.engine.fill.JRFillTextField.prepare(JRFillTextField.java:554)
2026-11-17T17:34:30.4263843Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:34:30.4264138Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:34:30.4264342Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:34:30.4264554Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:34:30.4264778Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:164)
2026-11-17T17:34:30.4264992Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:34:30.4265163Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:34:30.4265397Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:34:30.4265614Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:34:30.4265863Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:34:30.4266095Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:30.4266315Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:30.4266558Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:30.4266776Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:30.4267001Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:30.4267195Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:30.4267444Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:30.4267761Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:30.4267988Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:30.4268195Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:30.4268408Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:30.4268613Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:30.4268807Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:30.4268972Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:30.4269170Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:30.4269386Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:30.4269587Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:30.4269773Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:30.4269954Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:30.4270140Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:30.4270335Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:30.4270499Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:30.4270697Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:30.4270888Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:30.4271175Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:30.4271379Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:30.4271644Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:30.4271867Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:30.4272082Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:30.4272298Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:30.4272512Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:30.4272719Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:30.4272935Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:30.4273014Z 
2026-11-17T17:34:30.4273350Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[nce: 1 registros] -- Time elapsed: 0.011 s <<< ERROR!
2026-11-17T17:34:30.4273687Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:34:30.4273914Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:34:30.4274139Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:34:30.4274373Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:34:30.4274598Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:34:30.4274842Z 	at net.sf.jasperreports.engine.fill.JRFillTextField.prepare(JRFillTextField.java:554)
2026-11-17T17:34:30.4275116Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:34:30.4275422Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:34:30.4275891Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:34:30.4276199Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:34:30.4276471Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReportStart(JRVerticalFiller.java:262)
2026-11-17T17:34:30.4276694Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:128)
2026-11-17T17:34:30.4276879Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:34:30.4277081Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:34:30.4277294Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:34:30.4277508Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:34:30.4277773Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:34:30.4278008Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:30.4278224Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:30.4278460Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:30.4278676Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:30.4278847Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:30.4279078Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:30.4279294Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:30.4279789Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:30.4280061Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:30.4280323Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:30.4280536Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:30.4280739Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:30.4280932Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:30.4281220Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:30.4281420Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:30.4281615Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:30.4281809Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:30.4282009Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:30.4282185Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:30.4282371Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:30.4282534Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:30.4282737Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:30.4282930Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:30.4283126Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:30.4283317Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:30.4283535Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:30.4283770Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:30.4283997Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:30.4284183Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:30.4284402Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:30.4284627Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:30.4284830Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:30.4285036Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:30.4285115Z 
2026-11-17T17:34:30.4285444Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[nce: 100 registros] -- Time elapsed: 0.042 s <<< ERROR!
2026-11-17T17:34:30.4285779Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:34:30.4286016Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:34:30.4286237Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:34:30.4286469Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:34:30.4286692Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:34:30.4286919Z 	at net.sf.jasperreports.engine.fill.JRFillTextField.prepare(JRFillTextField.java:554)
2026-11-17T17:34:30.4287120Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:34:30.4287340Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:34:30.4287544Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:34:30.4287753Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:34:30.4287992Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReportStart(JRVerticalFiller.java:262)
2026-11-17T17:34:30.4288214Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:128)
2026-11-17T17:34:30.4288494Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:34:30.4288697Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:34:30.4288870Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:34:30.4289133Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:34:30.4289377Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:34:30.4289609Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:30.4289818Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:30.4290082Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:30.4290301Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:30.4290503Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:30.4290723Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:30.4290909Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:30.4291193Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:30.4291399Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:30.4291617Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:30.4291830Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:30.4292059Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:30.4292253Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:30.4292447Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:30.4292639Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:30.4292803Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:30.4292994Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:30.4293175Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:30.4293355Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:30.4293548Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:30.4293754Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:30.4293950Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:30.4294112Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:30.4294310Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:30.4294502Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:30.4294702Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:30.4294922Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:30.4295149Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:30.4295375Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:30.4295607Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:30.4295787Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:30.4295995Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:30.4296198Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:30.4296348Z 
2026-11-17T17:34:30.4296623Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[rural: 0 registros] -- Time elapsed: 0.024 s <<< ERROR!
2026-11-17T17:34:30.4296966Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:34:30.4297233Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:34:30.4297450Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:34:30.4297670Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:34:30.4297911Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:34:30.4298144Z 	at net.sf.jasperreports.engine.fill.JRFillStaticText.prepare(JRFillStaticText.java:183)
2026-11-17T17:34:30.4298381Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:34:30.4298603Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:34:30.4298816Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:34:30.4298999Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:34:30.4299236Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReportStart(JRVerticalFiller.java:262)
2026-11-17T17:34:30.4299455Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:128)
2026-11-17T17:34:30.4299667Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:34:30.4299887Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:34:30.4300088Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:34:30.4300301Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:34:30.4300542Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:34:30.4300742Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:30.4300964Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:30.4301272Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:30.4301487Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:30.4301690Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:30.4301926Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:30.4302140Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:30.4302351Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:30.4302552Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:30.4302725Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:30.4302949Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:30.4303148Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:30.4303340Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:30.4303533Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:30.4303740Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:30.4303932Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:30.4304160Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:30.4304311Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:30.4304506Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:30.4304696Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:30.4304920Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:30.4305207Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:30.4305486Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:30.4305767Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:30.4305973Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:30.4306183Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:30.4306415Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:30.4306664Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:30.4306882Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:30.4307102Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:30.4307322Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:30.4307583Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:30.4307802Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:30.4307883Z 
2026-11-17T17:34:30.4308214Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[rural: 1 registros] -- Time elapsed: 0.025 s <<< ERROR!
2026-11-17T17:34:30.4308554Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:34:30.4308779Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:34:30.4308966Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:34:30.4309189Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:34:30.4309421Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:34:30.4309650Z 	at net.sf.jasperreports.engine.fill.JRFillStaticText.prepare(JRFillStaticText.java:183)
2026-11-17T17:34:30.4309881Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:34:30.4310117Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:34:30.4310331Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:34:30.4310542Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:34:30.4310763Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReportStart(JRVerticalFiller.java:262)
2026-11-17T17:34:30.4310956Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:128)
2026-11-17T17:34:30.4311239Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:34:30.4311445Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:34:30.4311647Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:34:30.4311859Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:34:30.4312130Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:34:30.4312360Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:30.4312624Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:30.4312862Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:30.4313044Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:30.4313967Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:30.4314220Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:30.4314439Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:30.4314669Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:30.4314907Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:30.4315135Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:30.4315355Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:30.4315557Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:30.4315721Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:30.4315919Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:30.4316112Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:30.4316319Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:30.4316509Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:30.4316711Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:30.4316886Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:30.4317039Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:30.4317233Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:30.4317436Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:30.4317635Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:30.4317832Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:30.4318041Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:30.4318241Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:30.4318476Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:30.4318669Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:30.4318892Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:30.4319112Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:30.4319328Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:30.4319533Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:30.4319745Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:30.4319827Z 
2026-11-17T17:34:30.4320145Z [ERROR] br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao[rural: 100 registros] -- Time elapsed: 0.280 s <<< ERROR!
2026-11-17T17:34:30.4320483Z net.sf.jasperreports.engine.util.JRFontNotFoundException: Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:34:30.4320723Z 	at net.sf.jasperreports.engine.util.JRFontUtil.checkAwtFont(JRFontUtil.java:358)
2026-11-17T17:34:30.4320944Z 	at net.sf.jasperreports.engine.util.JRStyledText.getAwtAttributedString(JRStyledText.java:226)
2026-11-17T17:34:30.4321229Z 	at net.sf.jasperreports.engine.fill.TextMeasurer.measure(TextMeasurer.java:362)
2026-11-17T17:34:30.4321507Z 	at net.sf.jasperreports.engine.fill.JRFillTextElement.chopTextElement(JRFillTextElement.java:1129)
2026-11-17T17:34:30.4321705Z 	at net.sf.jasperreports.engine.fill.JRFillStaticText.prepare(JRFillStaticText.java:183)
2026-11-17T17:34:30.4321951Z 	at net.sf.jasperreports.engine.fill.JRFillElementContainer.prepareElements(JRFillElementContainer.java:329)
2026-11-17T17:34:30.4322201Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:419)
2026-11-17T17:34:30.4322405Z 	at net.sf.jasperreports.engine.fill.JRFillBand.fill(JRFillBand.java:378)
2026-11-17T17:34:30.4322619Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillTitle(JRVerticalFiller.java:328)
2026-11-17T17:34:30.4322889Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReportStart(JRVerticalFiller.java:262)
2026-11-17T17:34:30.4323114Z 	at net.sf.jasperreports.engine.fill.JRVerticalFiller.fillReport(JRVerticalFiller.java:128)
2026-11-17T17:34:30.4323331Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:946)
2026-11-17T17:34:30.4323545Z 	at net.sf.jasperreports.engine.fill.JRBaseFiller.fill(JRBaseFiller.java:864)
2026-11-17T17:34:30.4323713Z 	at net.sf.jasperreports.engine.fill.JRFiller.fillReport(JRFiller.java:84)
2026-11-17T17:34:30.4323925Z 	at net.sf.jasperreports.engine.JasperFillManager.fillReport(JasperFillManager.java:624)
2026-11-17T17:34:30.4324167Z 	at br.gov.caixa.siemp.relatorios.ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao(ExportacaoPdfTest.java:104)
2026-11-17T17:34:30.4324397Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
2026-11-17T17:34:30.4324609Z 	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
2026-11-17T17:34:30.4324863Z 	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
2026-11-17T17:34:30.4325181Z 	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
2026-11-17T17:34:30.4325386Z 	at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:47)
2026-11-17T17:34:30.4325604Z 	at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
2026-11-17T17:34:30.4325786Z 	at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:44)
2026-11-17T17:34:30.4326000Z 	at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
2026-11-17T17:34:30.4326203Z 	at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:271)
2026-11-17T17:34:30.4326406Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70)
2026-11-17T17:34:30.4326620Z 	at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:50)
2026-11-17T17:34:30.4326845Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:30.4327036Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:30.4327232Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:30.4327395Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:30.4327589Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:30.4327777Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:30.4327962Z 	at org.junit.runners.Suite.runChild(Suite.java:127)
2026-11-17T17:34:30.4328140Z 	at org.junit.runners.Suite.runChild(Suite.java:26)
2026-11-17T17:34:30.4328341Z 	at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238)
2026-11-17T17:34:30.4328542Z 	at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63)
2026-11-17T17:34:30.4328706Z 	at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236)
2026-11-17T17:34:30.4328899Z 	at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53)
2026-11-17T17:34:30.4329096Z 	at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229)
2026-11-17T17:34:30.4329312Z 	at org.junit.runners.ParentRunner.run(ParentRunner.java:309)
2026-11-17T17:34:30.4329510Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.execute(JUnit4Provider.java:316)
2026-11-17T17:34:30.4329727Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeWithRerun(JUnit4Provider.java:240)
2026-11-17T17:34:30.4330004Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.executeTestSet(JUnit4Provider.java:214)
2026-11-17T17:34:30.4330220Z 	at org.apache.maven.surefire.junit4.JUnit4Provider.invoke(JUnit4Provider.java:155)
2026-11-17T17:34:30.4330453Z 	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:385)
2026-11-17T17:34:30.4330635Z 	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:162)
2026-11-17T17:34:30.4330844Z 	at org.apache.maven.surefire.booter.ForkedBooter.run(ForkedBooter.java:507)
2026-11-17T17:34:30.4331104Z 	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:495)
2026-11-17T17:34:30.4331221Z 
2026-11-17T17:34:30.4331367Z [INFO] Running br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.manterpercentualdetaxasdejuros.ReceberVigenciaFormTest
2026-11-17T17:34:30.4332113Z [INFO] Tests run: 10, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.006 s -- in br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.manterpercentualdetaxasdejuros.ReceberVigenciaFormTest
2026-11-17T17:34:30.4333568Z [INFO] Running br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.manterpercentualdetaxasdejuros.CopiarEstruturaDeTabelaDeTaxasFormTest
2026-11-17T17:34:30.4350434Z [INFO] Tests run: 8, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0 s -- in br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.manterpercentualdetaxasdejuros.CopiarEstruturaDeTabelaDeTaxasFormTest
2026-11-17T17:34:30.4350782Z [INFO] Running br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.atualizarvaloresnamatrizdeexcepcionacao.AtualizarValoresNaMatrizDeExcepcionacaoFormTest
2026-11-17T17:34:30.4416017Z [INFO] Tests run: 13, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.005 s -- in br.gov.caixa.siemp.apoio.apresentacao.mantertabelas.atualizarvaloresnamatrizdeexcepcionacao.AtualizarValoresNaMatrizDeExcepcionacaoFormTest
2026-11-17T17:34:30.4973690Z [INFO] 
2026-11-17T17:34:30.4973895Z [INFO] Results:
2026-11-17T17:34:30.4974056Z [INFO] 
2026-11-17T17:34:30.4974594Z [ERROR] Errors: 
2026-11-17T17:34:30.4975371Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:34:30.4975811Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:34:30.4976395Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:34:30.4976825Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:34:30.4977246Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:34:30.4977654Z [ERROR]   ExportacaoPdfTest.deveGerarPdfLegivelComCabecalhoDetalhesEPaginacao:104 » JRFontNotFound Font 'Arial Black' is not available to the JVM. See the Javadoc for more details.
2026-11-17T17:34:30.4978532Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarParametrosDoConvenio_1794936868163_643305.java 
2026-11-17T17:34:30.4979063Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarParametrosDoConvenioReport_1794936868270_191526.java 
2026-11-17T17:34:30.4979788Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarTabelaDeTACDoConvenio_1794936868377_930329.java 
2026-11-17T17:34:30.4980344Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarTabelaDeTACDoConvenioNovo_1794936868449_607773.java 
2026-11-17T17:34:30.4980919Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarTabelaDeTACDoConvenioSubReport_1794936868518_229155.java 
2026-11-17T17:34:30.4981539Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarTabelaDeTaxasDoConvenio_1794936868566_790441.java 
2026-11-17T17:34:30.4981998Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarTabelaDeTaxasDoConvenioNovo_1794936868604_68899.java 
2026-11-17T17:34:30.4982564Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/consultarTabelaDeTaxasDoConvenioSubReport_1794936868627_803957.java 
2026-11-17T17:34:30.4983359Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/relatorioExtratoCreditoRural_1794936868665_322636.java 
2026-11-17T17:34:30.4983962Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioExtrato_1794936868679_474975.java 
2026-11-17T17:34:30.4984512Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioLiberacoes_1794936868690_265321.java 
2026-11-17T17:34:30.4985001Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioOcorrencias_1794936868699_229619.java 
2026-11-17T17:34:30.4985568Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioPosicaoDivida_1794936868711_813344.java 
2026-11-17T17:34:30.4986020Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioProAgro_1794936868724_87303.java 
2026-11-17T17:34:30.4986448Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioReembolsos_1794936868733_789753.java 
2026-11-17T17:34:30.4986885Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioReembolsosVencidos_1794936868746_947092.java 
2026-11-17T17:34:30.4987324Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/relatorioEvolucaoDivida_1794936868811_995881.java 
2026-11-17T17:34:30.4987757Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioEvolucaoDivida_1794936868835_316059.java 
2026-11-17T17:34:30.4988222Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioEvolucaoDivida_1794936868858_501042.java 
2026-11-17T17:34:30.4988733Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioEvolucaoDivida_1794936868885_573554.java 
2026-11-17T17:34:30.4989177Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/relatorioEvolucaoDividaSeguradora_1794936868928_392269.java 
2026-11-17T17:34:30.4989666Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/subRelatorioEvolucaoDividaSeguradora_1794936868940_666494.java 
2026-11-17T17:34:30.4990099Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDivida_1794936868976_238824.java 
2026-11-17T17:34:30.4990569Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/relatorioPosicaoDividaSeguradora_1794936869001_898561.java 
2026-11-17T17:34:30.4991000Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/relatorioEvolucaoDividaNCE_1794936869026_651265.java 
2026-11-17T17:34:30.4991525Z [ERROR]   ModelosJasperTest.fonteJrxmlDeveCompilarComBibliotecaAtual:67 » JR Error compiling report java source files : /opt/ads-agent/_work/36/s/siemp-web/simularPrestacoes_1794936869051_108161.java 
2026-11-17T17:34:30.4991738Z [INFO] 
2026-11-17T17:34:30.4991856Z [ERROR] Tests run: 403, Failures: 0, Errors: 32, Skipped: 13
2026-11-17T17:34:30.4992024Z [INFO] 
2026-11-17T17:34:30.5004281Z [INFO] ------------------------------------------------------------------------
2026-11-17T17:34:30.5004489Z [INFO] Reactor Summary for siemp application 14.37.0.6:
2026-11-17T17:34:30.5004643Z [INFO] 
2026-11-17T17:34:30.5006713Z [INFO] siemp application .................................. SUCCESS [  0.193 s]
2026-11-17T17:34:30.5007323Z [INFO] SIEMP Web module ................................... FAILURE [ 14.673 s]
2026-11-17T17:34:30.5007937Z [INFO] SIEMP EAR module ................................... SKIPPED
2026-11-17T17:34:30.5008494Z [INFO] ------------------------------------------------------------------------
2026-11-17T17:34:30.5008676Z [INFO] BUILD FAILURE
2026-11-17T17:34:30.5008904Z [INFO] ------------------------------------------------------------------------
2026-11-17T17:34:30.5009041Z [INFO] Total time:  14.995 s
2026-11-17T17:34:30.5010514Z [INFO] Finished at: 2026-11-17T14:34:30-03:00
2026-11-17T17:34:30.5010812Z [INFO] ------------------------------------------------------------------------
2026-11-17T17:34:30.5019932Z [ERROR] Failed to execute goal org.apache.maven.plugins:maven-surefire-plugin:3.2.5:test (default-test) on project siemp-web: 
2026-11-17T17:34:30.5020530Z [ERROR] 
2026-11-17T17:34:30.5020938Z [ERROR] Please refer to /opt/ads-agent/_work/36/s/siemp-web/target/surefire-reports for the individual test results.
2026-11-17T17:34:30.5021443Z [ERROR] Please refer to dump files (if any exist) [date].dump, [date]-jvmRun[N].dump and [date].dumpstream.
2026-11-17T17:34:30.5021668Z [ERROR] -> [Help 1]
2026-11-17T17:34:30.5021798Z [ERROR] 
2026-11-17T17:34:30.5021988Z [ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
2026-11-17T17:34:30.5022254Z [ERROR] Re-run Maven using the -X switch to enable full debug logging.
2026-11-17T17:34:30.5022410Z [ERROR] 
2026-11-17T17:34:30.5022597Z [ERROR] For more information about the errors and possible solutions, please read the following articles:
2026-11-17T17:34:30.5022797Z [ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoFailureException
2026-11-17T17:34:30.5022952Z [ERROR] 
2026-11-17T17:34:30.5023125Z [ERROR] After correcting the problems, you can resume the build with the command
2026-11-17T17:34:30.5023504Z [ERROR]   mvn <args> -rf :siemp-web
2026-11-17T17:34:30.5761259Z The process '/opt/apache-maven/apache-maven-3.8.5/bin/mvn' failed with exit code 1
2026-11-17T17:34:30.5761651Z Could not retrieve code analysis results - Maven run failed.
2026-11-17T17:34:30.5764493Z ##[error]Build failed.
2026-11-17T17:34:30.5831903Z ##[section]Finishing: Maven
