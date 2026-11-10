Flavio de Almeida Gagliardi, com base em nossa última conversa sobre possível apoio ou redirecionamento por parte da infra, poderia nos indicar alguém para verificar porque no build está tendo problemas em recuperar o jar abaixo, mesmo confirmando a existência deste?
 
 


2026-11-10T16:30:17.2820912Z [INFO] ------------------------------------------------------------------------
2026-11-10T16:30:17.2821284Z [INFO] Reactor Summary for SIGEC-PORTABILIDADE 5.0.0-batch-SNAPSHOT:
2026-11-10T16:30:17.2821450Z [INFO] 
2026-11-10T16:30:17.2821712Z [INFO] SIGEC-PORTABILIDADE ................................ SUCCESS [  0.059 s]
2026-11-10T16:30:17.2821910Z [INFO] GEC XML module ..................................... FAILURE [01:00 min]
2026-11-10T16:30:17.2822119Z [INFO] GEC Azure module ................................... SKIPPED
2026-11-10T16:30:17.2822365Z [INFO] GEC Common module - DTOs e Interfaces Compartilhadas SKIPPED
2026-11-10T16:30:17.2822554Z [INFO] GEC EJB module ..................................... SKIPPED
2026-11-10T16:30:17.2822944Z [INFO] GEC Batch module - Processamento Assíncrono ........ SKIPPED
2026-11-10T16:30:17.2823124Z [INFO] SIGEC PORTABILIDADE ................................ SKIPPED
2026-11-10T16:30:17.2823322Z [INFO] GEC EAR module ..................................... SKIPPED
2026-11-10T16:30:17.2823525Z [INFO] ------------------------------------------------------------------------
2026-11-10T16:30:17.2823696Z [INFO] BUILD FAILURE
2026-11-10T16:30:17.2823938Z [INFO] ------------------------------------------------------------------------
2026-11-10T16:30:17.2824114Z [INFO] Total time:  01:00 min
2026-11-10T16:30:17.2825880Z [INFO] Finished at: 2026-11-10T13:30:17-03:00
2026-11-10T16:30:17.2826139Z [INFO] ------------------------------------------------------------------------
2026-11-10T16:30:17.2836986Z [ERROR] Failed to execute goal on project gec-xml: Could not resolve dependencies for project br.gov.caixa.sigec:gec-xml:jar:5.0.0-batch-SNAPSHOT: Could not transfer artifact br.gov.caixa.arqref:arqref-services:jar:3.6.3.13 from/to Nexus Caixa (http://binario.caixa:8081/repository/caixa-group-br): transfer failed for http://binario.caixa:8081/repository/caixa-group-br/br/gov/caixa/arqref/arqref-services/3.6.3.13/arqref-services-3.6.3.13.jar, status: 500 Server Error -> [Help 1]
2026-11-10T16:30:17.2839646Z [ERROR] 
2026-11-10T16:30:17.2839886Z [ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
2026-11-10T16:30:17.2840160Z [ERROR] Re-run Maven using the -X switch to enable full debug logging.
2026-11-10T16:30:17.2840350Z [ERROR] 
2026-11-10T16:30:17.2840495Z [ERROR] For more information about the errors and possible solutions, please read the following articles:
2026-11-10T16:30:17.2840704Z [ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/DependencyResolutionException
2026-11-10T16:30:17.2840869Z [ERROR] 
2026-11-10T16:30:17.2841030Z [ERROR] After correcting the problems, you can resume the build with the command
2026-11-10T16:30:17.2841284Z [ERROR]   mvn <args> -rf :gec-xml
2026-11-10T16:30:17.3086152Z The process '/opt/apache-maven/apache-maven-3.8.5/bin/mvn' failed with exit code 1
2026-11-10T16:30:17.3086772Z Could not retrieve code analysis results - Maven run failed.
2026-11-10T16:30:17.3117237Z ##[error]Build failed.
2026-11-10T16:30:17.3173889Z ##[section]Finishing: Maven



2026-11-10T16:29:15.2936880Z ##[section]Starting: Maven
2026-11-10T16:29:15.2943725Z ==============================================================================
2026-11-10T16:29:15.2943817Z Task         : Maven
2026-11-10T16:29:15.2943865Z Description  : Build, test, and deploy with Apache Maven
2026-11-10T16:29:15.2943969Z Version      : 4.225.0
2026-11-10T16:29:15.2944013Z Author       : Microsoft Corporation
2026-11-10T16:29:15.2944063Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/build/maven
2026-11-10T16:29:15.2944175Z ==============================================================================
2026-11-10T16:29:15.9574102Z [command]/opt/apache-maven/apache-maven-3.8.5/bin/mvn -version
2026-11-10T16:29:16.0597225Z Apache Maven 3.8.5 (3599d3414f046de2324203b78ddcf9b5e4388aa0)
2026-11-10T16:29:16.0597951Z Maven home: /opt/apache-maven/apache-maven-3.8.5
2026-11-10T16:29:16.0598307Z Java version: 17.0.8, vendor: OpenLogic, runtime: /usr/java/open-jdk-17.0.8
2026-11-10T16:29:16.0598609Z Default locale: pt_BR, platform encoding: UTF-8
2026-11-10T16:29:16.0598933Z OS name: "linux", version: "5.18.5-100.fc35.x86_64", arch: "amd64", family: "unix"
2026-11-10T16:29:16.0775708Z [command]/opt/apache-maven/apache-maven-3.8.5/bin/mvn -f /opt/ads-agent/_work/34/s/pom.xml clean package -Dversion.app= -DskipTests=true -U
2026-11-10T16:29:16.7617103Z [INFO] Scanning for projects...
2026-11-10T16:29:16.8285706Z [WARNING] 
2026-11-10T16:29:16.8286446Z [WARNING] Some problems were encountered while building the effective model for br.gov.caixa.sigec:gec-xml:jar:5.0.0-batch-SNAPSHOT
2026-11-10T16:29:16.8286804Z [WARNING] 'version' contains an expression but should be a constant. @ br.gov.caixa.sigec:gec:${sigec.version}, /opt/ads-agent/_work/34/s/pom.xml, line 8, column 11
2026-11-10T16:29:16.8287019Z [WARNING] 
2026-11-10T16:29:16.8287310Z [WARNING] Some problems were encountered while building the effective model for br.gov.caixa.sigec:gec:pom:5.0.0-batch-SNAPSHOT
2026-11-10T16:29:16.8288002Z [WARNING] 'version' contains an expression but should be a constant. @ br.gov.caixa.sigec:gec:${sigec.version}, /opt/ads-agent/_work/34/s/pom.xml, line 8, column 11
2026-11-10T16:29:16.8288216Z [WARNING] 
2026-11-10T16:29:16.8288533Z [WARNING] It is highly recommended to fix these problems because they threaten the stability of your build.
2026-11-10T16:29:16.8288712Z [WARNING] 
2026-11-10T16:29:16.8288845Z [WARNING] For this reason, future Maven versions might no longer support building such malformed projects.
2026-11-10T16:29:16.8289009Z [WARNING] 
2026-11-10T16:29:16.8319412Z [INFO] ------------------------------------------------------------------------
2026-11-10T16:29:16.8319673Z [INFO] Reactor Build Order:
2026-11-10T16:29:16.8319813Z [INFO] 
2026-11-10T16:29:16.8325976Z [INFO] SIGEC-PORTABILIDADE                                                [pom]
2026-11-10T16:29:16.8326182Z [INFO] GEC XML module                                                     [jar]
2026-11-10T16:29:16.8326425Z [INFO] GEC Azure module                                                   [jar]
2026-11-10T16:29:16.8326628Z [INFO] GEC Common module - DTOs e Interfaces Compartilhadas               [jar]
2026-11-10T16:29:16.8326796Z [INFO] GEC EJB module                                                     [ejb]
2026-11-10T16:29:16.8327029Z [INFO] GEC Batch module - Processamento Assíncrono                        [jar]
2026-11-10T16:29:16.8327202Z [INFO] SIGEC PORTABILIDADE                                                [war]
2026-11-10T16:29:16.8329270Z [INFO] GEC EAR module                                                     [ear]
2026-11-10T16:29:16.8370312Z [INFO] 
2026-11-10T16:29:16.8370686Z [INFO] -----------------------< br.gov.caixa.sigec:gec >-----------------------
2026-11-10T16:29:16.8370924Z [INFO] Building SIGEC-PORTABILIDADE 5.0.0-batch-SNAPSHOT                  [1/8]
2026-11-10T16:29:16.8371296Z [INFO] --------------------------------[ pom ]---------------------------------
2026-11-10T16:29:16.8571247Z [INFO] 
2026-11-10T16:29:16.8571727Z [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ gec ---
2026-11-10T16:29:16.8970396Z [INFO] 
2026-11-10T16:29:16.8971223Z [INFO] ---------------------< br.gov.caixa.sigec:gec-xml >---------------------
2026-11-10T16:29:16.8971688Z [INFO] Building GEC XML module 5.0.0-batch-SNAPSHOT                       [2/8]
2026-11-10T16:29:16.8972129Z [INFO] --------------------------------[ jar ]---------------------------------
2026-11-10T16:29:17.0659729Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/br/gov/caixa/arqref/arqref-core/3.7.2.2/arqref-core-3.7.2.2.pom
2026-11-10T16:29:17.6013005Z Progress (1): 4.1/5.3 kB
2026-11-10T16:29:18.0532077Z Progress (1): 5.3 kB    
2026-11-10T16:29:18.0532419Z                     
2026-11-10T16:29:18.0533213Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/br/gov/caixa/arqref/arqref-core/3.7.2.2/arqref-core-3.7.2.2.pom (5.3 kB at 5.3 kB/s)
2026-11-10T16:29:18.0707434Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/jboss/arquillian/arquillian-bom/1.0.2.Final/arquillian-bom-1.0.2.Final.pom
2026-11-10T16:29:18.0823920Z Progress (1): 4.1/11 kB
2026-11-10T16:29:18.0826445Z Progress (1): 8.2/11 kB
2026-11-10T16:29:18.0899753Z Progress (1): 11 kB    
2026-11-10T16:29:18.0900419Z                    
2026-11-10T16:29:18.0901025Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/jboss/arquillian/arquillian-bom/1.0.2.Final/arquillian-bom-1.0.2.Final.pom (11 kB at 559 kB/s)
2026-11-10T16:29:18.0973814Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/jboss/shrinkwrap/shrinkwrap-bom/1.0.1/shrinkwrap-bom-1.0.1.pom
2026-11-10T16:29:18.1105293Z Progress (1): 3.2 kB
2026-11-10T16:29:18.1106107Z                     
2026-11-10T16:29:18.1106972Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/jboss/shrinkwrap/shrinkwrap-bom/1.0.1/shrinkwrap-bom-1.0.1.pom (3.2 kB at 243 kB/s)
2026-11-10T16:29:18.1223273Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/jboss/shrinkwrap/resolver/shrinkwrap-resolver-bom/1.0.0-beta-7/shrinkwrap-resolver-bom-1.0.0-beta-7.pom
2026-11-10T16:29:18.1386723Z Progress (1): 3.3 kB
2026-11-10T16:29:18.1387250Z                     
2026-11-10T16:29:18.1387803Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/jboss/shrinkwrap/resolver/shrinkwrap-resolver-bom/1.0.0-beta-7/shrinkwrap-resolver-bom-1.0.0-beta-7.pom (3.3 kB at 204 kB/s)
2026-11-10T16:29:18.1459517Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/jboss/shrinkwrap/descriptors/shrinkwrap-descriptors-bom/2.0.0-alpha-3/shrinkwrap-descriptors-bom-2.0.0-alpha-3.pom
2026-11-10T16:29:18.1529510Z Progress (1): 2.3/4.4 kB
2026-11-10T16:29:18.1594730Z Progress (1): 4.4 kB    
2026-11-10T16:29:18.1595480Z                     
2026-11-10T16:29:18.1596117Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/jboss/shrinkwrap/descriptors/shrinkwrap-descriptors-bom/2.0.0-alpha-3/shrinkwrap-descriptors-bom-2.0.0-alpha-3.pom (4.4 kB at 311 kB/s)
2026-11-10T16:29:18.1693272Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/com/google/code/gson/gson/2.2.4/gson-2.2.4.pom
2026-11-10T16:29:18.2694945Z Progress (1): 4.1/8.0 kB
2026-11-10T16:29:18.2695943Z Progress (1): 7.7/8.0 kB
2026-11-10T16:29:18.3165921Z Progress (1): 8.0 kB    
2026-11-10T16:29:18.3166112Z                     
2026-11-10T16:29:18.3166778Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/com/google/code/gson/gson/2.2.4/gson-2.2.4.pom (8.0 kB at 55 kB/s)
2026-11-10T16:29:18.3378699Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/jboss/shrinkwrap/shrinkwrap-api/1.0.1/shrinkwrap-api-1.0.1.pom
2026-11-10T16:29:18.3546482Z Progress (1): 3.1 kB
2026-11-10T16:29:18.3548510Z                     
2026-11-10T16:29:18.3549596Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/jboss/shrinkwrap/shrinkwrap-api/1.0.1/shrinkwrap-api-1.0.1.pom (3.1 kB at 182 kB/s)
2026-11-10T16:29:18.3612342Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/jboss/shrinkwrap/shrinkwrap-parent/1.0.1/shrinkwrap-parent-1.0.1.pom
2026-11-10T16:29:18.4214877Z Progress (1): 4.1/11 kB
2026-11-10T16:29:18.4216525Z Progress (1): 7.7/11 kB
2026-11-10T16:29:18.4907301Z Progress (1): 11 kB    
2026-11-10T16:29:18.4907496Z                    
2026-11-10T16:29:18.4908340Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/jboss/shrinkwrap/shrinkwrap-parent/1.0.1/shrinkwrap-parent-1.0.1.pom (11 kB at 83 kB/s)
2026-11-10T16:29:18.5058730Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/freemarker/freemarker/2.3.23/freemarker-2.3.23.pom
2026-11-10T16:29:18.6430752Z Progress (1): 1.5 kB
2026-11-10T16:29:18.6431130Z                     
2026-11-10T16:29:18.6431849Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/freemarker/freemarker/2.3.23/freemarker-2.3.23.pom (1.5 kB at 11 kB/s)
2026-11-10T16:29:18.6534373Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/javax/mail/mail/1.4.7/mail-1.4.7.pom
2026-11-10T16:29:18.6668468Z Progress (1): 4.1/5.3 kB
2026-11-10T16:29:18.6733382Z Progress (1): 5.3 kB    
2026-11-10T16:29:18.6734293Z                     
2026-11-10T16:29:18.6735224Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/javax/mail/mail/1.4.7/mail-1.4.7.pom (5.3 kB at 266 kB/s)
2026-11-10T16:29:18.6838793Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/com/sun/mail/all/1.4.7/all-1.4.7.pom
2026-11-10T16:29:18.6915065Z Progress (1): 4.1/20 kB
2026-11-10T16:29:18.6917038Z Progress (1): 7.7/20 kB
2026-11-10T16:29:18.6918694Z Progress (1): 12/20 kB 
2026-11-10T16:29:18.6920400Z Progress (1): 16/20 kB
2026-11-10T16:29:18.6921867Z Progress (1): 20/20 kB
2026-11-10T16:29:18.6963917Z Progress (1): 20 kB   
2026-11-10T16:29:18.6964928Z                    
2026-11-10T16:29:18.6966065Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/com/sun/mail/all/1.4.7/all-1.4.7.pom (20 kB at 1.6 MB/s)
2026-11-10T16:29:18.7049894Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/br/gov/caixa/arqref/arqref-services/3.6.3.13/arqref-services-3.6.3.13.pom
2026-11-10T16:29:56.0252481Z Progress (1): 473 B
2026-11-10T16:29:56.0255968Z                    
2026-11-10T16:29:56.0256701Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/br/gov/caixa/arqref/arqref-services/3.6.3.13/arqref-services-3.6.3.13.pom (473 B at 12 B/s)
2026-11-10T16:29:56.0327634Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/br/gov/caixa/arqref/arqref-web/3.1.0.1/arqref-web-3.1.0.1.pom
2026-11-10T16:29:56.3498354Z [WARNING] The POM for br.gov.caixa.arqref:arqref-web:jar:3.1.0.1 is missing, no dependency information available
2026-11-10T16:29:56.3545946Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/br/gov/caixa/arqref/arqref-core/3.7.2.2/arqref-core-3.7.2.2.jar
2026-11-10T16:29:56.3546882Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/com/google/code/gson/gson/2.2.4/gson-2.2.4.jar
2026-11-10T16:29:56.3551327Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/jboss/shrinkwrap/shrinkwrap-api/1.0.1/shrinkwrap-api-1.0.1.jar
2026-11-10T16:29:56.3552469Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/freemarker/freemarker/2.3.23/freemarker-2.3.23.jar
2026-11-10T16:29:56.3553824Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/javax/mail/mail/1.4.7/mail-1.4.7.jar
2026-11-10T16:29:56.3825123Z Progress (1): 4.1/521 kB
2026-11-10T16:29:56.3826011Z Progress (1): 8.2/521 kB
2026-11-10T16:29:56.3829427Z Progress (1): 12/521 kB 
2026-11-10T16:29:56.3831720Z Progress (2): 12/521 kB | 4.1/63 kB
2026-11-10T16:29:56.3834259Z Progress (2): 16/521 kB | 4.1/63 kB
2026-11-10T16:29:56.3836271Z Progress (2): 16/521 kB | 7.7/63 kB
2026-11-10T16:29:56.3838216Z Progress (2): 20/521 kB | 7.7/63 kB
2026-11-10T16:29:56.3840292Z Progress (2): 20/521 kB | 12/63 kB 
2026-11-10T16:29:56.3841997Z Progress (2): 25/521 kB | 12/63 kB
2026-11-10T16:29:56.3844079Z Progress (2): 25/521 kB | 16/63 kB
2026-11-10T16:29:56.3846242Z Progress (2): 29/521 kB | 16/63 kB
2026-11-10T16:29:56.3847486Z Progress (2): 29/521 kB | 20/63 kB
2026-11-10T16:29:56.3850029Z Progress (2): 33/521 kB | 20/63 kB
2026-11-10T16:29:56.3851903Z Progress (2): 33/521 kB | 24/63 kB
2026-11-10T16:29:56.3853891Z Progress (2): 37/521 kB | 24/63 kB
2026-11-10T16:29:56.3855733Z Progress (2): 37/521 kB | 28/63 kB
2026-11-10T16:29:56.3857611Z Progress (2): 41/521 kB | 28/63 kB
2026-11-10T16:29:56.3859570Z Progress (2): 41/521 kB | 32/63 kB
2026-11-10T16:29:56.3861146Z Progress (2): 45/521 kB | 32/63 kB
2026-11-10T16:29:56.3862912Z Progress (2): 45/521 kB | 36/63 kB
2026-11-10T16:29:56.3864812Z Progress (2): 49/521 kB | 36/63 kB
2026-11-10T16:29:56.3866603Z Progress (2): 49/521 kB | 41/63 kB
2026-11-10T16:29:56.3868279Z Progress (2): 53/521 kB | 41/63 kB
2026-11-10T16:29:56.3870665Z Progress (2): 53/521 kB | 45/63 kB
2026-11-10T16:29:56.3872332Z Progress (2): 57/521 kB | 45/63 kB
2026-11-10T16:29:56.3874050Z Progress (2): 57/521 kB | 49/63 kB
2026-11-10T16:29:56.3875739Z Progress (2): 61/521 kB | 49/63 kB
2026-11-10T16:29:56.3877307Z Progress (2): 61/521 kB | 53/63 kB
2026-11-10T16:29:56.3878991Z Progress (2): 66/521 kB | 53/63 kB
2026-11-10T16:29:56.3881164Z Progress (2): 66/521 kB | 57/63 kB
2026-11-10T16:29:56.3882379Z Progress (2): 70/521 kB | 57/63 kB
2026-11-10T16:29:56.3884206Z Progress (2): 70/521 kB | 61/63 kB
2026-11-10T16:29:56.3885995Z Progress (2): 74/521 kB | 61/63 kB
2026-11-10T16:29:56.3887190Z Progress (2): 74/521 kB | 63 kB   
2026-11-10T16:29:56.3890111Z Progress (2): 78/521 kB | 63 kB
2026-11-10T16:29:56.3893916Z Progress (2): 82/521 kB | 63 kB
2026-11-10T16:29:56.3896056Z Progress (2): 86/521 kB | 63 kB
2026-11-10T16:29:56.3897995Z Progress (2): 90/521 kB | 63 kB
2026-11-10T16:29:56.3900213Z Progress (2): 94/521 kB | 63 kB
2026-11-10T16:29:56.3902250Z Progress (2): 98/521 kB | 63 kB
2026-11-10T16:29:56.3904341Z Progress (2): 102/521 kB | 63 kB
2026-11-10T16:29:56.3906685Z Progress (2): 106/521 kB | 63 kB
2026-11-10T16:29:56.3908380Z Progress (2): 111/521 kB | 63 kB
2026-11-10T16:29:56.3910478Z Progress (2): 115/521 kB | 63 kB
2026-11-10T16:29:56.3912805Z Progress (2): 119/521 kB | 63 kB
2026-11-10T16:29:56.3914837Z Progress (2): 123/521 kB | 63 kB
2026-11-10T16:29:56.3926403Z Progress (2): 127/521 kB | 63 kB
2026-11-10T16:29:56.3928610Z Progress (2): 131/521 kB | 63 kB
2026-11-10T16:29:56.3930801Z Progress (2): 135/521 kB | 63 kB
2026-11-10T16:29:56.3932777Z Progress (2): 139/521 kB | 63 kB
2026-11-10T16:29:56.3934443Z Progress (2): 143/521 kB | 63 kB
2026-11-10T16:29:56.3936475Z Progress (2): 147/521 kB | 63 kB
2026-11-10T16:29:56.3938242Z Progress (2): 152/521 kB | 63 kB
2026-11-10T16:29:56.3940288Z Progress (2): 156/521 kB | 63 kB
2026-11-10T16:29:56.3942711Z Progress (2): 160/521 kB | 63 kB
2026-11-10T16:29:56.3944848Z Progress (2): 164/521 kB | 63 kB
2026-11-10T16:29:56.3945639Z Progress (2): 168/521 kB | 63 kB
2026-11-10T16:29:56.3946767Z                                 
2026-11-10T16:29:56.3947821Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/jboss/shrinkwrap/shrinkwrap-api/1.0.1/shrinkwrap-api-1.0.1.jar (63 kB at 1.6 MB/s)
2026-11-10T16:29:56.3948209Z Progress (1): 172/521 kB
2026-11-10T16:29:56.3948349Z                         
2026-11-10T16:29:56.3952207Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/br/gov/caixa/arqref/arqref-services/3.6.3.13/arqref-services-3.6.3.13.jar
2026-11-10T16:29:56.3952481Z Progress (1): 176/521 kB
2026-11-10T16:29:56.3952627Z Progress (1): 180/521 kB
2026-11-10T16:29:56.3954026Z Progress (1): 184/521 kB
2026-11-10T16:29:56.3956346Z Progress (1): 188/521 kB
2026-11-10T16:29:56.3957758Z Progress (1): 193/521 kB
2026-11-10T16:29:56.3959051Z Progress (1): 197/521 kB
2026-11-10T16:29:56.3960689Z Progress (1): 201/521 kB
2026-11-10T16:29:56.3961936Z Progress (1): 205/521 kB
2026-11-10T16:29:56.3963549Z Progress (1): 209/521 kB
2026-11-10T16:29:56.3964941Z Progress (1): 213/521 kB
2026-11-10T16:29:56.3966634Z Progress (1): 217/521 kB
2026-11-10T16:29:56.3967619Z Progress (1): 221/521 kB
2026-11-10T16:29:56.3969017Z Progress (1): 225/521 kB
2026-11-10T16:29:56.3970334Z Progress (1): 229/521 kB
2026-11-10T16:29:56.3971615Z Progress (1): 233/521 kB
2026-11-10T16:29:56.3973217Z Progress (1): 238/521 kB
2026-11-10T16:29:56.3974444Z Progress (1): 242/521 kB
2026-11-10T16:29:56.3976079Z Progress (1): 246/521 kB
2026-11-10T16:29:56.3977416Z Progress (1): 250/521 kB
2026-11-10T16:29:56.3978894Z Progress (1): 254/521 kB
2026-11-10T16:29:56.3980269Z Progress (1): 258/521 kB
2026-11-10T16:29:56.3981705Z Progress (1): 262/521 kB
2026-11-10T16:29:56.3983302Z Progress (1): 266/521 kB
2026-11-10T16:29:56.3984916Z Progress (1): 270/521 kB
2026-11-10T16:29:56.3986060Z Progress (1): 274/521 kB
2026-11-10T16:29:56.3987502Z Progress (1): 279/521 kB
2026-11-10T16:29:56.3988988Z Progress (1): 283/521 kB
2026-11-10T16:29:56.3990261Z Progress (1): 287/521 kB
2026-11-10T16:29:56.3991401Z Progress (1): 291/521 kB
2026-11-10T16:29:56.3992640Z Progress (1): 295/521 kB
2026-11-10T16:29:56.3993840Z Progress (1): 299/521 kB
2026-11-10T16:29:56.3995113Z Progress (1): 303/521 kB
2026-11-10T16:29:56.3996190Z Progress (1): 307/521 kB
2026-11-10T16:29:56.3997576Z Progress (1): 311/521 kB
2026-11-10T16:29:56.3998594Z Progress (1): 315/521 kB
2026-11-10T16:29:56.3999828Z Progress (1): 319/521 kB
2026-11-10T16:29:56.4000953Z Progress (1): 324/521 kB
2026-11-10T16:29:56.4002309Z Progress (1): 328/521 kB
2026-11-10T16:29:56.4003580Z Progress (1): 332/521 kB
2026-11-10T16:29:56.4004696Z Progress (1): 336/521 kB
2026-11-10T16:29:56.4006351Z Progress (1): 340/521 kB
2026-11-10T16:29:56.4007633Z Progress (1): 344/521 kB
2026-11-10T16:29:56.4008680Z Progress (1): 348/521 kB
2026-11-10T16:29:56.4009841Z Progress (1): 352/521 kB
2026-11-10T16:29:56.4011407Z Progress (1): 356/521 kB
2026-11-10T16:29:56.4012102Z Progress (1): 360/521 kB
2026-11-10T16:29:56.4013565Z Progress (1): 365/521 kB
2026-11-10T16:29:56.4014924Z Progress (1): 369/521 kB
2026-11-10T16:29:56.4016110Z Progress (1): 373/521 kB
2026-11-10T16:29:56.4017428Z Progress (1): 377/521 kB
2026-11-10T16:29:56.4018365Z Progress (1): 381/521 kB
2026-11-10T16:29:56.4019619Z Progress (1): 385/521 kB
2026-11-10T16:29:56.4020667Z Progress (1): 389/521 kB
2026-11-10T16:29:56.4022613Z Progress (1): 393/521 kB
2026-11-10T16:29:56.4023914Z Progress (1): 397/521 kB
2026-11-10T16:29:56.4024985Z Progress (1): 401/521 kB
2026-11-10T16:29:56.4026159Z Progress (1): 406/521 kB
2026-11-10T16:29:56.4027218Z Progress (1): 410/521 kB
2026-11-10T16:29:56.4028433Z Progress (1): 414/521 kB
2026-11-10T16:29:56.4029465Z Progress (1): 418/521 kB
2026-11-10T16:29:56.4030505Z Progress (1): 422/521 kB
2026-11-10T16:29:56.4031567Z Progress (1): 426/521 kB
2026-11-10T16:29:56.4032702Z Progress (1): 430/521 kB
2026-11-10T16:29:56.4033779Z Progress (1): 434/521 kB
2026-11-10T16:29:56.4034806Z Progress (1): 438/521 kB
2026-11-10T16:29:56.4035876Z Progress (1): 442/521 kB
2026-11-10T16:29:56.4036894Z Progress (1): 446/521 kB
2026-11-10T16:29:56.4037929Z Progress (1): 451/521 kB
2026-11-10T16:29:56.4038937Z Progress (1): 455/521 kB
2026-11-10T16:29:56.4040484Z Progress (1): 459/521 kB
2026-11-10T16:29:56.4041354Z Progress (1): 463/521 kB
2026-11-10T16:29:56.4042762Z Progress (1): 467/521 kB
2026-11-10T16:29:56.4043838Z Progress (1): 471/521 kB
2026-11-10T16:29:56.4044995Z Progress (1): 475/521 kB
2026-11-10T16:29:56.4046067Z Progress (1): 479/521 kB
2026-11-10T16:29:56.4047107Z Progress (1): 483/521 kB
2026-11-10T16:29:56.4048223Z Progress (1): 487/521 kB
2026-11-10T16:29:56.4049236Z Progress (1): 492/521 kB
2026-11-10T16:29:56.4050234Z Progress (1): 496/521 kB
2026-11-10T16:29:56.4051275Z Progress (1): 500/521 kB
2026-11-10T16:29:56.4052579Z Progress (1): 504/521 kB
2026-11-10T16:29:56.4053673Z Progress (1): 508/521 kB
2026-11-10T16:29:56.4054675Z Progress (1): 512/521 kB
2026-11-10T16:29:56.4055748Z Progress (1): 516/521 kB
2026-11-10T16:29:56.4056926Z Progress (1): 520/521 kB
2026-11-10T16:29:56.4108116Z Progress (1): 521 kB    
2026-11-10T16:29:56.4109222Z                     
2026-11-10T16:29:56.4109812Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/javax/mail/mail/1.4.7/mail-1.4.7.jar (521 kB at 9.5 MB/s)
2026-11-10T16:29:56.4110249Z Downloading from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/br/gov/caixa/arqref/arqref-web/3.1.0.1/arqref-web-3.1.0.1.jar
2026-11-10T16:29:56.4170430Z Progress (1): 4.1/5.1 kB
2026-11-10T16:29:56.4219262Z Progress (1): 5.1 kB    
2026-11-10T16:29:56.4220867Z Progress (2): 5.1 kB | 4.1/190 kB
2026-11-10T16:29:56.4223060Z Progress (2): 5.1 kB | 7.7/190 kB
2026-11-10T16:29:56.4224472Z Progress (2): 5.1 kB | 12/190 kB 
2026-11-10T16:29:56.4225984Z Progress (2): 5.1 kB | 16/190 kB
2026-11-10T16:29:56.4227248Z Progress (2): 5.1 kB | 20/190 kB
2026-11-10T16:29:56.4228919Z Progress (2): 5.1 kB | 24/190 kB
2026-11-10T16:29:56.4229169Z Progress (2): 5.1 kB | 28/190 kB
2026-11-10T16:29:56.4231256Z                                 
2026-11-10T16:29:56.4232371Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/br/gov/caixa/arqref/arqref-web/3.1.0.1/arqref-web-3.1.0.1.jar (5.1 kB at 75 kB/s)
2026-11-10T16:29:56.4233088Z Progress (1): 32/190 kB
2026-11-10T16:29:56.4234339Z Progress (1): 36/190 kB
2026-11-10T16:29:56.4235967Z Progress (1): 40/190 kB
2026-11-10T16:29:56.4237064Z Progress (1): 45/190 kB
2026-11-10T16:29:56.4238063Z Progress (1): 49/190 kB
2026-11-10T16:29:56.4239088Z Progress (1): 53/190 kB
2026-11-10T16:29:56.4240221Z Progress (1): 57/190 kB
2026-11-10T16:29:56.4241482Z Progress (1): 61/190 kB
2026-11-10T16:29:56.4243499Z Progress (1): 65/190 kB
2026-11-10T16:29:56.4244605Z Progress (1): 69/190 kB
2026-11-10T16:29:56.4245772Z Progress (1): 73/190 kB
2026-11-10T16:29:56.4246698Z Progress (1): 77/190 kB
2026-11-10T16:29:56.4247737Z Progress (1): 81/190 kB
2026-11-10T16:29:56.4248818Z Progress (1): 86/190 kB
2026-11-10T16:29:56.4250284Z Progress (1): 90/190 kB
2026-11-10T16:29:56.4251585Z Progress (1): 94/190 kB
2026-11-10T16:29:56.4252945Z Progress (1): 98/190 kB
2026-11-10T16:29:56.4254245Z Progress (1): 102/190 kB
2026-11-10T16:29:56.4255557Z Progress (1): 106/190 kB
2026-11-10T16:29:56.4256998Z Progress (1): 110/190 kB
2026-11-10T16:29:56.4258030Z Progress (1): 114/190 kB
2026-11-10T16:29:56.4259352Z Progress (1): 118/190 kB
2026-11-10T16:29:56.4260829Z Progress (1): 122/190 kB
2026-11-10T16:29:56.4264020Z Progress (1): 127/190 kB
2026-11-10T16:29:56.4266768Z Progress (1): 131/190 kB
2026-11-10T16:29:56.4267837Z Progress (1): 135/190 kB
2026-11-10T16:29:56.4268730Z Progress (1): 139/190 kB
2026-11-10T16:29:56.4269894Z Progress (1): 143/190 kB
2026-11-10T16:29:56.4271040Z Progress (1): 147/190 kB
2026-11-10T16:29:56.4272036Z Progress (1): 151/190 kB
2026-11-10T16:29:56.4273054Z Progress (1): 155/190 kB
2026-11-10T16:29:56.4273904Z Progress (1): 159/190 kB
2026-11-10T16:29:56.4274855Z Progress (1): 163/190 kB
2026-11-10T16:29:56.4275699Z Progress (1): 167/190 kB
2026-11-10T16:29:56.4276606Z Progress (1): 172/190 kB
2026-11-10T16:29:56.4278178Z Progress (1): 176/190 kB
2026-11-10T16:29:56.4279072Z Progress (1): 180/190 kB
2026-11-10T16:29:56.4280358Z Progress (1): 184/190 kB
2026-11-10T16:29:56.4281245Z Progress (1): 188/190 kB
2026-11-10T16:29:56.4790625Z Progress (1): 190 kB    
2026-11-10T16:29:56.4791166Z                     
2026-11-10T16:29:56.4791841Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/com/google/code/gson/gson/2.2.4/gson-2.2.4.jar (190 kB at 1.5 MB/s)
2026-11-10T16:29:56.5704867Z Progress (1): 0/1.4 MB
2026-11-10T16:29:56.5705080Z Progress (1): 0/1.4 MB
2026-11-10T16:29:56.5705577Z Progress (1): 0/1.4 MB
2026-11-10T16:29:56.5705953Z Progress (1): 0/1.4 MB
2026-11-10T16:29:56.5707342Z Progress (1): 0/1.4 MB
2026-11-10T16:29:56.5708698Z Progress (1): 0/1.4 MB
2026-11-10T16:29:56.5709748Z Progress (1): 0.1/1.4 MB
2026-11-10T16:29:56.5710790Z Progress (1): 0.1/1.4 MB
2026-11-10T16:29:56.5711848Z Progress (1): 0.1/1.4 MB
2026-11-10T16:29:56.5712840Z Progress (1): 0.1/1.4 MB
2026-11-10T16:29:56.5714685Z Progress (1): 0.1/1.4 MB
2026-11-10T16:29:56.5715102Z Progress (1): 0.1/1.4 MB
2026-11-10T16:29:56.5716309Z Progress (1): 0.1/1.4 MB
2026-11-10T16:29:56.5717156Z Progress (1): 0.1/1.4 MB
2026-11-10T16:29:56.5718344Z Progress (1): 0.1/1.4 MB
2026-11-10T16:29:56.5736387Z Progress (1): 0.1/1.4 MB
2026-11-10T16:29:56.5738141Z Progress (1): 0.1/1.4 MB
2026-11-10T16:29:56.5738431Z Progress (1): 0.1/1.4 MB
2026-11-10T16:29:56.5739640Z Progress (1): 0.2/1.4 MB
2026-11-10T16:29:56.5740786Z Progress (1): 0.2/1.4 MB
2026-11-10T16:29:56.5741884Z Progress (1): 0.2/1.4 MB
2026-11-10T16:29:56.5743728Z Progress (1): 0.2/1.4 MB
2026-11-10T16:29:56.5746180Z Progress (1): 0.2/1.4 MB
2026-11-10T16:29:56.5746571Z Progress (1): 0.2/1.4 MB
2026-11-10T16:29:56.5746907Z Progress (1): 0.2/1.4 MB
2026-11-10T16:29:56.5748420Z Progress (1): 0.2/1.4 MB
2026-11-10T16:29:56.5749611Z Progress (1): 0.2/1.4 MB
2026-11-10T16:29:56.5750618Z Progress (1): 0.2/1.4 MB
2026-11-10T16:29:56.5751646Z Progress (1): 0.2/1.4 MB
2026-11-10T16:29:56.5752601Z Progress (1): 0.2/1.4 MB
2026-11-10T16:29:56.5753820Z Progress (1): 0.3/1.4 MB
2026-11-10T16:29:56.5754683Z Progress (1): 0.3/1.4 MB
2026-11-10T16:29:56.5756057Z Progress (1): 0.3/1.4 MB
2026-11-10T16:29:56.5756948Z Progress (1): 0.3/1.4 MB
2026-11-10T16:29:56.5758123Z Progress (1): 0.3/1.4 MB
2026-11-10T16:29:56.5759760Z Progress (1): 0.3/1.4 MB
2026-11-10T16:29:56.5760920Z Progress (1): 0.3/1.4 MB
2026-11-10T16:29:56.5762004Z Progress (1): 0.3/1.4 MB
2026-11-10T16:29:56.5763087Z Progress (1): 0.3/1.4 MB
2026-11-10T16:29:56.5764123Z Progress (1): 0.3/1.4 MB
2026-11-10T16:29:56.5765168Z Progress (1): 0.3/1.4 MB
2026-11-10T16:29:56.5766315Z Progress (1): 0.3/1.4 MB
2026-11-10T16:29:56.5767345Z Progress (1): 0.4/1.4 MB
2026-11-10T16:29:56.5768365Z Progress (1): 0.4/1.4 MB
2026-11-10T16:29:56.5769336Z Progress (1): 0.4/1.4 MB
2026-11-10T16:29:56.5770445Z Progress (1): 0.4/1.4 MB
2026-11-10T16:29:56.5771527Z Progress (1): 0.4/1.4 MB
2026-11-10T16:29:56.5773115Z Progress (1): 0.4/1.4 MB
2026-11-10T16:29:56.5774508Z Progress (1): 0.4/1.4 MB
2026-11-10T16:29:56.5775568Z Progress (1): 0.4/1.4 MB
2026-11-10T16:29:56.5776823Z Progress (1): 0.4/1.4 MB
2026-11-10T16:29:56.5777861Z Progress (1): 0.4/1.4 MB
2026-11-10T16:29:56.5778957Z Progress (1): 0.4/1.4 MB
2026-11-10T16:29:56.5780082Z Progress (1): 0.4/1.4 MB
2026-11-10T16:29:56.5781159Z Progress (1): 0.5/1.4 MB
2026-11-10T16:29:56.5782283Z Progress (1): 0.5/1.4 MB
2026-11-10T16:29:56.5783517Z Progress (1): 0.5/1.4 MB
2026-11-10T16:29:56.5784625Z Progress (1): 0.5/1.4 MB
2026-11-10T16:29:56.5785889Z Progress (1): 0.5/1.4 MB
2026-11-10T16:29:56.5786770Z Progress (1): 0.5/1.4 MB
2026-11-10T16:29:56.5787792Z Progress (1): 0.5/1.4 MB
2026-11-10T16:29:56.5788762Z Progress (1): 0.5/1.4 MB
2026-11-10T16:29:56.5789798Z Progress (1): 0.5/1.4 MB
2026-11-10T16:29:56.5790861Z Progress (1): 0.5/1.4 MB
2026-11-10T16:29:56.5791905Z Progress (1): 0.5/1.4 MB
2026-11-10T16:29:56.5793170Z Progress (1): 0.5/1.4 MB
2026-11-10T16:29:56.5794378Z Progress (1): 0.5/1.4 MB
2026-11-10T16:29:56.5795297Z Progress (1): 0.6/1.4 MB
2026-11-10T16:29:56.5796243Z Progress (1): 0.6/1.4 MB
2026-11-10T16:29:56.5797171Z Progress (1): 0.6/1.4 MB
2026-11-10T16:29:56.5798433Z Progress (1): 0.6/1.4 MB
2026-11-10T16:29:56.5799357Z Progress (1): 0.6/1.4 MB
2026-11-10T16:29:56.5800220Z Progress (1): 0.6/1.4 MB
2026-11-10T16:29:56.5801247Z Progress (1): 0.6/1.4 MB
2026-11-10T16:29:56.5802201Z Progress (1): 0.6/1.4 MB
2026-11-10T16:29:56.5803225Z Progress (1): 0.6/1.4 MB
2026-11-10T16:29:56.5804269Z Progress (1): 0.6/1.4 MB
2026-11-10T16:29:56.5805161Z Progress (1): 0.6/1.4 MB
2026-11-10T16:29:56.5806037Z Progress (1): 0.6/1.4 MB
2026-11-10T16:29:56.5806895Z Progress (1): 0.7/1.4 MB
2026-11-10T16:29:56.5807713Z Progress (1): 0.7/1.4 MB
2026-11-10T16:29:56.5808583Z Progress (1): 0.7/1.4 MB
2026-11-10T16:29:56.5809386Z Progress (1): 0.7/1.4 MB
2026-11-10T16:29:56.5810290Z Progress (1): 0.7/1.4 MB
2026-11-10T16:29:56.5811279Z Progress (1): 0.7/1.4 MB
2026-11-10T16:29:56.5812510Z Progress (1): 0.7/1.4 MB
2026-11-10T16:29:56.5813607Z Progress (1): 0.7/1.4 MB
2026-11-10T16:29:56.5814544Z Progress (1): 0.7/1.4 MB
2026-11-10T16:29:56.5815566Z Progress (1): 0.7/1.4 MB
2026-11-10T16:29:56.5816639Z Progress (1): 0.7/1.4 MB
2026-11-10T16:29:56.5817567Z Progress (1): 0.7/1.4 MB
2026-11-10T16:29:56.5818389Z Progress (1): 0.8/1.4 MB
2026-11-10T16:29:56.5819592Z Progress (1): 0.8/1.4 MB
2026-11-10T16:29:56.5820605Z Progress (1): 0.8/1.4 MB
2026-11-10T16:29:56.5821110Z Progress (1): 0.8/1.4 MB
2026-11-10T16:29:56.5822061Z Progress (1): 0.8/1.4 MB
2026-11-10T16:29:56.5822963Z Progress (1): 0.8/1.4 MB
2026-11-10T16:29:56.5823889Z Progress (1): 0.8/1.4 MB
2026-11-10T16:29:56.5824745Z Progress (1): 0.8/1.4 MB
2026-11-10T16:29:56.5825829Z Progress (1): 0.8/1.4 MB
2026-11-10T16:29:56.5826770Z Progress (1): 0.8/1.4 MB
2026-11-10T16:29:56.5827628Z Progress (1): 0.8/1.4 MB
2026-11-10T16:29:56.5828565Z Progress (1): 0.8/1.4 MB
2026-11-10T16:29:56.5829377Z Progress (1): 0.9/1.4 MB
2026-11-10T16:29:56.5830277Z Progress (1): 0.9/1.4 MB
2026-11-10T16:29:56.5831128Z Progress (1): 0.9/1.4 MB
2026-11-10T16:29:56.5831942Z Progress (1): 0.9/1.4 MB
2026-11-10T16:29:56.5832805Z Progress (1): 0.9/1.4 MB
2026-11-10T16:29:56.5833702Z Progress (1): 0.9/1.4 MB
2026-11-10T16:29:56.5835249Z Progress (1): 0.9/1.4 MB
2026-11-10T16:29:56.5836278Z Progress (1): 0.9/1.4 MB
2026-11-10T16:29:56.5837161Z Progress (1): 0.9/1.4 MB
2026-11-10T16:29:56.5838082Z Progress (1): 0.9/1.4 MB
2026-11-10T16:29:56.5839017Z Progress (1): 0.9/1.4 MB
2026-11-10T16:29:56.5839911Z Progress (1): 0.9/1.4 MB
2026-11-10T16:29:56.5840684Z Progress (1): 0.9/1.4 MB
2026-11-10T16:29:56.5841510Z Progress (1): 1.0/1.4 MB
2026-11-10T16:29:56.5842537Z Progress (1): 1.0/1.4 MB
2026-11-10T16:29:56.5843346Z Progress (1): 1.0/1.4 MB
2026-11-10T16:29:56.5844257Z Progress (1): 1.0/1.4 MB
2026-11-10T16:29:56.5845270Z Progress (1): 1.0/1.4 MB
2026-11-10T16:29:56.5846074Z Progress (1): 1.0/1.4 MB
2026-11-10T16:29:56.5846953Z Progress (1): 1.0/1.4 MB
2026-11-10T16:29:56.5847744Z Progress (1): 1.0/1.4 MB
2026-11-10T16:29:56.5849074Z Progress (1): 1.0/1.4 MB
2026-11-10T16:29:56.5849949Z Progress (1): 1.0/1.4 MB
2026-11-10T16:29:56.5850889Z Progress (1): 1.0/1.4 MB
2026-11-10T16:29:56.5851725Z Progress (1): 1.0/1.4 MB
2026-11-10T16:29:56.5852872Z Progress (1): 1.1/1.4 MB
2026-11-10T16:29:56.5853408Z Progress (1): 1.1/1.4 MB
2026-11-10T16:29:56.5854262Z Progress (1): 1.1/1.4 MB
2026-11-10T16:29:56.5855056Z Progress (1): 1.1/1.4 MB
2026-11-10T16:29:56.5856037Z Progress (1): 1.1/1.4 MB
2026-11-10T16:29:56.5856940Z Progress (1): 1.1/1.4 MB
2026-11-10T16:29:56.5857862Z Progress (1): 1.1/1.4 MB
2026-11-10T16:29:56.5858670Z Progress (1): 1.1/1.4 MB
2026-11-10T16:29:56.5859429Z Progress (1): 1.1/1.4 MB
2026-11-10T16:29:56.5860273Z Progress (1): 1.1/1.4 MB
2026-11-10T16:29:56.5861149Z Progress (1): 1.1/1.4 MB
2026-11-10T16:29:56.5862001Z Progress (1): 1.1/1.4 MB
2026-11-10T16:29:56.5862771Z Progress (1): 1.2/1.4 MB
2026-11-10T16:29:56.5863569Z Progress (1): 1.2/1.4 MB
2026-11-10T16:29:56.5864348Z Progress (1): 1.2/1.4 MB
2026-11-10T16:29:56.5865177Z Progress (1): 1.2/1.4 MB
2026-11-10T16:29:56.5866122Z Progress (1): 1.2/1.4 MB
2026-11-10T16:29:56.5866929Z Progress (1): 1.2/1.4 MB
2026-11-10T16:29:56.5867757Z Progress (1): 1.2/1.4 MB
2026-11-10T16:29:56.5868720Z Progress (1): 1.2/1.4 MB
2026-11-10T16:29:56.5869485Z Progress (1): 1.2/1.4 MB
2026-11-10T16:29:56.5870369Z Progress (1): 1.2/1.4 MB
2026-11-10T16:29:56.5871233Z Progress (1): 1.2/1.4 MB
2026-11-10T16:29:56.5872051Z Progress (1): 1.2/1.4 MB
2026-11-10T16:29:56.5872933Z Progress (1): 1.3/1.4 MB
2026-11-10T16:29:56.5873823Z Progress (1): 1.3/1.4 MB
2026-11-10T16:29:56.5874693Z Progress (1): 1.3/1.4 MB
2026-11-10T16:29:56.5875532Z Progress (1): 1.3/1.4 MB
2026-11-10T16:29:56.5876632Z Progress (1): 1.3/1.4 MB
2026-11-10T16:29:56.5877341Z Progress (1): 1.3/1.4 MB
2026-11-10T16:29:56.5878084Z Progress (1): 1.3/1.4 MB
2026-11-10T16:29:56.5878821Z Progress (1): 1.3/1.4 MB
2026-11-10T16:29:56.5879640Z Progress (1): 1.3/1.4 MB
2026-11-10T16:29:56.5880359Z Progress (1): 1.3/1.4 MB
2026-11-10T16:29:56.5881323Z Progress (1): 1.3/1.4 MB
2026-11-10T16:29:56.5882181Z Progress (1): 1.3/1.4 MB
2026-11-10T16:29:56.7475156Z Progress (1): 1.4 MB    
2026-11-10T16:29:56.7475507Z                     
2026-11-10T16:29:56.7476219Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/org/freemarker/freemarker/2.3.23/freemarker-2.3.23.jar (1.4 MB at 3.4 MB/s)
2026-11-10T16:29:56.8934715Z Progress (1): 4.1/236 kB
2026-11-10T16:29:56.8935120Z Progress (1): 7.7/236 kB
2026-11-10T16:29:56.8935456Z Progress (1): 12/236 kB 
2026-11-10T16:29:56.8935625Z Progress (1): 16/236 kB
2026-11-10T16:29:56.8936718Z Progress (1): 20/236 kB
2026-11-10T16:29:56.8937112Z Progress (1): 24/236 kB
2026-11-10T16:29:56.8938037Z Progress (1): 28/236 kB
2026-11-10T16:29:56.8938369Z Progress (1): 32/236 kB
2026-11-10T16:29:56.8939346Z Progress (1): 36/236 kB
2026-11-10T16:29:56.8939831Z Progress (1): 40/236 kB
2026-11-10T16:29:56.8940767Z Progress (1): 45/236 kB
2026-11-10T16:29:56.8941234Z Progress (1): 49/236 kB
2026-11-10T16:29:56.8942302Z Progress (1): 53/236 kB
2026-11-10T16:29:56.8942818Z Progress (1): 57/236 kB
2026-11-10T16:29:56.8942994Z Progress (1): 61/236 kB
2026-11-10T16:29:56.8943787Z Progress (1): 65/236 kB
2026-11-10T16:29:56.8944311Z Progress (1): 69/236 kB
2026-11-10T16:29:56.8944847Z Progress (1): 73/236 kB
2026-11-10T16:29:56.8945527Z Progress (1): 77/236 kB
2026-11-10T16:29:56.8946030Z Progress (1): 81/236 kB
2026-11-10T16:29:56.8946904Z Progress (1): 86/236 kB
2026-11-10T16:29:56.8947068Z Progress (1): 90/236 kB
2026-11-10T16:29:56.8947817Z Progress (1): 94/236 kB
2026-11-10T16:29:56.8948489Z Progress (1): 98/236 kB
2026-11-10T16:29:56.8949094Z Progress (1): 102/236 kB
2026-11-10T16:29:56.8949750Z Progress (1): 106/236 kB
2026-11-10T16:29:56.8950413Z Progress (1): 110/236 kB
2026-11-10T16:29:56.8950943Z Progress (1): 114/236 kB
2026-11-10T16:29:56.8951383Z Progress (1): 118/236 kB
2026-11-10T16:29:56.8951855Z Progress (1): 122/236 kB
2026-11-10T16:29:56.8952369Z Progress (1): 127/236 kB
2026-11-10T16:29:56.8956765Z Progress (1): 131/236 kB
2026-11-10T16:29:56.8957238Z Progress (1): 135/236 kB
2026-11-10T16:29:56.8957870Z Progress (1): 139/236 kB
2026-11-10T16:29:56.8958291Z Progress (1): 143/236 kB
2026-11-10T16:29:56.8958776Z Progress (1): 147/236 kB
2026-11-10T16:29:56.8959264Z Progress (1): 151/236 kB
2026-11-10T16:29:56.8959811Z Progress (1): 155/236 kB
2026-11-10T16:29:56.8960251Z Progress (1): 159/236 kB
2026-11-10T16:29:56.8960963Z Progress (1): 163/236 kB
2026-11-10T16:29:56.8961403Z Progress (1): 167/236 kB
2026-11-10T16:29:56.8961957Z Progress (1): 172/236 kB
2026-11-10T16:29:56.8962431Z Progress (1): 176/236 kB
2026-11-10T16:29:56.8963039Z Progress (1): 180/236 kB
2026-11-10T16:29:56.8963574Z Progress (1): 184/236 kB
2026-11-10T16:29:56.8964045Z Progress (1): 188/236 kB
2026-11-10T16:29:56.8964530Z Progress (1): 192/236 kB
2026-11-10T16:29:56.8964972Z Progress (1): 196/236 kB
2026-11-10T16:29:56.8965469Z Progress (1): 200/236 kB
2026-11-10T16:29:56.8965903Z Progress (1): 204/236 kB
2026-11-10T16:29:56.8966344Z Progress (1): 208/236 kB
2026-11-10T16:29:56.8966842Z Progress (1): 213/236 kB
2026-11-10T16:29:56.8967268Z Progress (1): 217/236 kB
2026-11-10T16:29:56.8967793Z Progress (1): 221/236 kB
2026-11-10T16:29:56.8968357Z Progress (1): 225/236 kB
2026-11-10T16:29:56.8968859Z Progress (1): 229/236 kB
2026-11-10T16:29:56.8969261Z Progress (1): 233/236 kB
2026-11-10T16:29:57.3690298Z Progress (1): 236 kB    
2026-11-10T16:29:57.3690715Z                     
2026-11-10T16:29:57.3691439Z Downloaded from Nexus Caixa: http://binario.caixa:8081/repository/caixa-group-br/br/gov/caixa/arqref/arqref-core/3.7.2.2/arqref-core-3.7.2.2.jar (236 kB at 232 kB/s)
2026-11-10T16:30:17.2820912Z [INFO] ------------------------------------------------------------------------
2026-11-10T16:30:17.2821284Z [INFO] Reactor Summary for SIGEC-PORTABILIDADE 5.0.0-batch-SNAPSHOT:
2026-11-10T16:30:17.2821450Z [INFO] 
2026-11-10T16:30:17.2821712Z [INFO] SIGEC-PORTABILIDADE ................................ SUCCESS [  0.059 s]
2026-11-10T16:30:17.2821910Z [INFO] GEC XML module ..................................... FAILURE [01:00 min]
2026-11-10T16:30:17.2822119Z [INFO] GEC Azure module ................................... SKIPPED
2026-11-10T16:30:17.2822365Z [INFO] GEC Common module - DTOs e Interfaces Compartilhadas SKIPPED
2026-11-10T16:30:17.2822554Z [INFO] GEC EJB module ..................................... SKIPPED
2026-11-10T16:30:17.2822944Z [INFO] GEC Batch module - Processamento Assíncrono ........ SKIPPED
2026-11-10T16:30:17.2823124Z [INFO] SIGEC PORTABILIDADE ................................ SKIPPED
2026-11-10T16:30:17.2823322Z [INFO] GEC EAR module ..................................... SKIPPED
2026-11-10T16:30:17.2823525Z [INFO] ------------------------------------------------------------------------
2026-11-10T16:30:17.2823696Z [INFO] BUILD FAILURE
2026-11-10T16:30:17.2823938Z [INFO] ------------------------------------------------------------------------
2026-11-10T16:30:17.2824114Z [INFO] Total time:  01:00 min
2026-11-10T16:30:17.2825880Z [INFO] Finished at: 2026-11-10T13:30:17-03:00
2026-11-10T16:30:17.2826139Z [INFO] ------------------------------------------------------------------------
2026-11-10T16:30:17.2836986Z [ERROR] Failed to execute goal on project gec-xml: Could not resolve dependencies for project br.gov.caixa.sigec:gec-xml:jar:5.0.0-batch-SNAPSHOT: Could not transfer artifact br.gov.caixa.arqref:arqref-services:jar:3.6.3.13 from/to Nexus Caixa (http://binario.caixa:8081/repository/caixa-group-br): transfer failed for http://binario.caixa:8081/repository/caixa-group-br/br/gov/caixa/arqref/arqref-services/3.6.3.13/arqref-services-3.6.3.13.jar, status: 500 Server Error -> [Help 1]
2026-11-10T16:30:17.2839646Z [ERROR] 
2026-11-10T16:30:17.2839886Z [ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
2026-11-10T16:30:17.2840160Z [ERROR] Re-run Maven using the -X switch to enable full debug logging.
2026-11-10T16:30:17.2840350Z [ERROR] 
2026-11-10T16:30:17.2840495Z [ERROR] For more information about the errors and possible solutions, please read the following articles:
2026-11-10T16:30:17.2840704Z [ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/DependencyResolutionException
2026-11-10T16:30:17.2840869Z [ERROR] 
2026-11-10T16:30:17.2841030Z [ERROR] After correcting the problems, you can resume the build with the command
2026-11-10T16:30:17.2841284Z [ERROR]   mvn <args> -rf :gec-xml
2026-11-10T16:30:17.3086152Z The process '/opt/apache-maven/apache-maven-3.8.5/bin/mvn' failed with exit code 1
2026-11-10T16:30:17.3086772Z Could not retrieve code analysis results - Maven run failed.
2026-11-10T16:30:17.3117237Z ##[error]Build failed.
2026-11-10T16:30:17.3173889Z ##[section]Finishing: Maven




# Variable 'version.app' was defined in the Variables tab
# Variable Group 'BUILD_VARIABLES' was defined in the Variables tab
# Variable Group 'SONAR_VARIABLES - ESTEIRA' was defined in the Variables tab
# Variable Group 'SAST_FORTIFY_COMUNIDADE_CREDITO_COMERCIAL' was defined in the Variables tab
resources:
  repositories:
  - repository: self
    type: git
    ref: null
jobs:
- job: Job_1
  displayName: Agent job 1
  pool:
    name: Build-Linux-OKD4
  steps:
  - checkout: self
  - task: Bash@3
    displayName: Validação da VEC
    enabled: False
    inputs:
      targetType: inline
      script: "echo \"##[section]branch/tag: $BUILD_SOURCEBRANCHNAME\"\n\necho \"##[warning] -------------------- ATENÇÃO --------------------\n##[warning] Foi definido que a partir de 01/2025 apenas compilações oriundas de tag dentro do padrão estabelecido no PPDS poderão ser implantadas em HMP/PRD.\n##[warning] Para mais informações visite https://caixa.sharepoint.com/sites/PPDS/SitePages/GCM_Diretrizes_Padrao_Baseline.aspx ou consulte a GEQTI04\n-------------------------------------------------\"\n\npontos=`echo ${BUILD_SOURCEBRANCHNAME//[^\\.]} | sed 's/\\./\\.\\n/g' | wc -w`\nnumber=`echo $BUILD_SOURCEBRANCHNAME | sed 's/\\.//g'`\n\nif [[ ${pontos} = 3 ]];then\nif [[ ${number} =~ ^([0-9]+)$ ]];then\necho \"VEC $BUILD_SOURCEBRANCHNAME dentro do padrão estabelecido pelo PPDS.\nPacote apto a ser implantado em HMP/PRD.\"\nvec='true'\necho \"##vso[build.updatebuildnumber]\"$BUILD_SOURCEBRANCHNAME\"\"\nelse\necho \"A TAG $BUILD_SOURCEBRANCHNAME utilizada não se encontra dentro do padrão estabelecido pelo PPDS e este pacote não poderá ser implantado nos ambientes HMP/PRD.\"\nvec='false'\nfi\nelse\necho \"Foi selecionada para compilação uma branch ou tag fora do padrão estabelcido no PPDS. Esteja ciente de que este pacote poderá ser implantado somente em ambientes NPRD\"\nvec='false'\nfi\necho \"##[section]Valida VEC: $vec\"\necho \"##vso[task.setvariable variable=valida.vec;]$vec\"\n\necho \"------------------------------------------------- \nps: Essa regra se aplicará somente a projetos que possuem infra HMP/PRD criada na esteira devops.\nAté o presente momento esse passo é meramente INFORMATIVO, a aplicação da trava será realizada somente em janeiro de 2025\""
  - task: Bash@3
    displayName: Localização do Repositório
    inputs:
      targetType: inline
      script: >
        if [[ "$BUILD_REPOSITORY_URI" == *"github.com"* ]]; then

        echo "É um repositório do GitHub"

        REPO_FINAL_NAME=`basename "$BUILD_REPOSITORY_URI" .git`

        echo "##vso[task.setvariable variable=fortify_disable;]gecmi"

        echo "##vso[task.setvariable variable=sonar_disable;]true"

        else

        echo "É um repositório do Devops.Caixa"

        REPO_FINAL_NAME=`echo $(Build.Repository.Name)`

        fi

        echo "Nome do repositório: $REPO_FINAL_NAME"

        echo "##vso[task.setvariable variable=REPO_FINAL_NAME;]$REPO_FINAL_NAME"
  - task: Bash@3
    displayName: Validação da VEC
    inputs:
      targetType: inline
      script: "echo \"##[section]branch/tag: $BUILD_SOURCEBRANCHNAME\"\n\necho \"##[warning] -------------------- ATENÇÃO --------------------\n##[warning] Foi definido conforme CE GEQTI 011/2024 que a partir de 03/2025 apenas compilações oriundas de tag dentro do padrão estabelecido no PPDS poderão ser implantadas em TQS/HMP/PRD.\n##[warning] Para mais informações acesse as urls:\n##[warning] https://devops.caixa/projetos/Caixa/_wiki/wikis/Caixa.wiki/1689/Valida%C3%A7%C3%A3o-da-VEC\n##[warning] https://caixa.sharepoint.com/sites/PPDS/SitePages/GCM_Diretrizes_Padrao_Baseline.aspx ou consulte a GEQTI04\n-------------------------------------------------\"\necho $BUILD_SOURCEBRANCH\nif [[ `echo $BUILD_SOURCEBRANCH | grep -c tags` -gt 0 ]];then\npontos=`echo ${BUILD_SOURCEBRANCHNAME//[^\\.]} | sed 's/\\./\\.\\n/g' | wc -w`\nnumber=`echo $BUILD_SOURCEBRANCHNAME | sed 's/\\\\.//g'`\n\nif [[ ${pontos} = 3 ]];then\nif [[ ${number} =~ ^([0-9]+)$ ]];then\necho \"VEC $BUILD_SOURCEBRANCHNAME dentro do padrão estabelecido pelo PPDS.\nPacote apto a ser implantado em TQS/HMP/PRD.\"\nvec='true'\necho \"##vso[build.updatebuildnumber]\"$BUILD_SOURCEBRANCHNAME\"\"\nelse\necho \"A TAG $BUILD_SOURCEBRANCHNAME não se encontra dentro do padrão estabelecido pelo PPDS e este pacote não poderá ser implantado nos ambientes TQS/HMP/PRD.\"\nvec='false'\nfi\nelse\necho \"A TAG $BUILD_SOURCEBRANCHNAME não se encontra dentro do padrão estabelecido pelo PPDS e este pacote não poderá ser implantado nos ambientes TQS/HMP/PRD.\"\nvec='false'\nfi\nelif [[ `echo $BUILD_SOURCEBRANCH | grep -c heads` -gt 0 ]];then\necho \"##[warning]Foi selecionada para compilação uma branch. Esteja ciente de que este pacote poderá ser implantado somente em ambiente DES.\"\nvec='false'\nelse\necho \"##[warning]Foi selecionada para compilação uma branch. Esteja ciente de que este pacote poderá ser implantado somente em ambiente DES.\"\nvec='false'\nfi\n\necho \"##[section]Valida VEC: $vec\"\necho \"##vso[task.setvariable variable=valida.vec;]$vec\"\n\necho \"------------------------------------------------- \nps: Essa regra se aplica somente a projetos que possuem infra criada na esteira devops.\""
  - task: Bash@3
    displayName: Obtendo branch do Sonar
    enabled: False
    inputs:
      targetType: inline
      script: >-
        if [[ `echo $BUILD_SOURCEBRANCH | grep -c tags` -gt 0 ]];then

        token=$(AZPAT)


        #Apresenta object_id da tag

        object_id_tag=`curl -s -u :$token "https://devops.caixa/projetos/Caixa/_apis/git/repositories/$BUILD_REPOSITORY_NAME/refs?filter=tags/$BUILD_SOURCEBRANCHNAME&api-version=7.0" | jq -r '.value[0].objectId'`


        echo "Commit da TAG: " $object_id_tag


        #Apresenta commit_id branch

        object_id_commit=`curl -s -u :$token "https://devops.caixa/projetos/Caixa/_apis/git/repositories/$BUILD_REPOSITORY_NAME/annotatedtags/$object_id_tag?api-version=7.0" | jq -r '.taggedObject.objectId'`


        echo "Commit da branch que gerou a tag: " $object_id_commit


        #Pasea json localiza branch

        branch_of_tag=`curl -s -u :$token "https://devops.caixa/projetos/Caixa/_apis/git/repositories/$BUILD_REPOSITORY_NAME/refs?filter=heads&api-version=7.0" | jq -c '.value[] | select(.objectId | contains("'$object_id_commit'")).name' | awk 'NR==1'`


        if [ -z $branch_of_tag ];then

        echo "Não foi possível localizar a Branch que originou a TAG."

        sonar_branch=$BUILD_SOURCEBRANCHNAME

        else

        branch_of_tag=`echo $branch_of_tag | sed -e 's/\"//g'`

        echo "Branch que gerou a Tag: " $branch_of_tag

        sonar_branch=`echo $branch_of_tag | awk -F '/' '{print $NF'}`

        fi


        else


        sonar_branch=$BUILD_SOURCEBRANCHNAME


        fi


        echo $sonar_branch


        echo "##vso[task.setvariable variable=sonar_branch;]$sonar_branch"
  - task: Bash@3
    displayName: Obtendo branch do Sonar
    inputs:
      targetType: inline
      script: "#!/usr/bin/env bash\nset -euo pipefail\n\nif [[ `echo $BUILD_SOURCEBRANCH | grep -c tags` -gt 0 ]];then\n\necho \"Build originada de uma TAG.\"\n\n# ====== CONFIGURAÇÃO ======\nTAG=$BUILD_SOURCEBRANCH\nREMOTE=\"origin\"\n\n# ====== RESOLVER COMMIT FINAL DA TAG ======\nif ! COMMIT=`git rev-parse \"$TAG^{commit}\" 2>/dev/null`; then\n  echo \"Erro: a tag '$TAG' não existe ou não é válida.\"\n  exit 1\nfi\n\necho \"Tag        : $TAG\"\necho \"Commit     : $COMMIT\"\necho \"Remote     : $REMOTE\"\necho\necho \"Analisando branches que contêm o commit...\"\necho \"------------------------------------------------------------\"\nprintf \"%-8s %s\\n\" \"DISTÂNCIA\" \"BRANCH\"\necho \"------------------------------------------------------------\"\n\nFOUND=0\n\nwhile read -r BRANCH; do\n  if git merge-base --is-ancestor \"$COMMIT\" \"$BRANCH\"; then\n    DIST=`git rev-list --count \"$COMMIT..$BRANCH\"`\n    \n    # Remove origin/\n    BRANCH_DISPLAY=\"${BRANCH#origin/}\"    \n\n    printf \"%-8s %s\\n\" \"$DIST\" \"$BRANCH_DISPLAY\"\n    FOUND=1\n  fi\ndone < <(\n  git for-each-ref \\\n    --format='%(refname:short)' \\\n    \"refs/remotes/$REMOTE\"\n)\n\nif [[ \"$FOUND\" -eq 0 ]]; then\n  echo \"Nenhuma branch remota contém esse commit.\"\n  exit 1\nfi\n\necho \"------------------------------------------------------------\"\n\n# ====== BRANCH MAIS PROVÁVEL ======\nBEST_BRANCH=$(\n  while read -r BRANCH; do\n    if git merge-base --is-ancestor \"$COMMIT\" \"$BRANCH\"; then\n      # Remove origin/\n      BRANCH_DISPLAY=\"${BRANCH#origin/}\"    \n      echo \"`git rev-list --count \"$COMMIT..$BRANCH\"` $BRANCH_DISPLAY\"\n    fi\n  done < <(\n    git for-each-ref \\\n      --format='%(refname:short)' \\\n      \"refs/remotes/$REMOTE\"\n  ) | sort -n | head -n1\n)\n\nBEST_DISTANCE=`echo \"$BEST_BRANCH\" | awk '{print $1}'`\nBEST_NAME=`echo \"$BEST_BRANCH\" | awk '{print $2}'`\n\necho \"Branch mais provável de origem:\"\necho \"$BEST_NAME (distância: $BEST_DISTANCE commits)\"\n\nelse\n\necho \"Build originada de uma BRANCH.\"\nBEST_NAME=$BUILD_SOURCEBRANCHNAME\n\nfi\n\necho \"Branch que será informada para o SONAR: $BEST_NAME \"\n\necho \"##vso[task.setvariable variable=sonar_branch;]$BEST_NAME\"\n"
  - task: Bash@3
    displayName: Configurando Registry NPM
    inputs:
      targetType: inline
      script: >-
        npm config set email pipeline-agil@mail.caixa

        npm config set registry http://binario.caixa:8081/repository/npm-all/

        npm config set sass_binary_site http://binario.caixa:8081/repository/node-sass/

        npm config set strict-ssl false


        npm config list
  - task: CopyFiles@2
    displayName: 'Copy Files to: $(Agent.BuildDirectory)/fortify'
    condition: ne(variables['fortify_disable'], 'gecmi')
    inputs:
      SourceFolder: $(Build.SourcesDirectory)
      TargetFolder: $(Agent.BuildDirectory)/fortify
      CleanTargetFolder: true
  - task: Maven@4
    displayName: Maven
    inputs:
      goals: clean package -Dversion.app=$(version.app) -DskipTests=true -U
      publishJUnitResults: false
      javaHomeSelection: Path
      jdkUserInputPath: /usr/java/open-jdk-17.0.8
      mavenVersionSelection: Path
      mavenPath: /opt/apache-maven/apache-maven-3.8.5/
      mavenOpts: '-Xms1024m -Xmx6144m '
  - task: Bash@3
    displayName: Recupera versão projeto (groupId:artifactId:type:version)
    inputs:
      targetType: inline
      script: "cd $(Build.SourcesDirectory)\n\nfind . -name maven-wrapper.jar -delete\n\necho \"Entrando no diretório: $(Build.SourcesDirectory)\"\necho \"Arquivos encontrados: `ls -la`\"\n\nif [ -z \"$TARGET_PATH\" ]; then \n	TARGET_PATH=\".\" \nfi\n\nfor extension in ear war jar\ndo\n   file=`find $TARGET_PATH -name \"*.${extension}\"`\n   if [ -n \"${file}\" ]\n   then\n			PROJECT_FILE=\"${file}\"\n			p_extension=\"${extension}\"\n			break\n   fi\ndone\n\necho \"Encontrado o arquivo: $file\\n\"\n\nexport PROJECT_DIR=`dirname ${PROJECT_FILE}`\nexport PROJECT_POM_PROPERTIES_FILE=`find ${PROJECT_DIR} -name pom.properties`\n\necho \"Diretório do projeto: $PROJECT_DIR\"\necho \"Conteúdo do diretório: `ls -la $PROJECT_DIR`\"\necho \"Arquivo POM: $PROJECT_POM_PROPERTIES_FILE\"\n\n#if [ -z $PROJECT_POM_PROPERTIES_FILE ]\n#then\n#      echo \"Arquivo pom.properties não encontrado, favor verificar a versão da TAG <maven-ear-plugin-version> no pom.properties, algumas versões #possuem BUG e não gera o arquivo.\"\n#      exit 1\n#fi\n\n\np_version=`egrep version ${PROJECT_POM_PROPERTIES_FILE} | awk -F = {'print $2'}`		 \np_group=`egrep groupId ${PROJECT_POM_PROPERTIES_FILE} | awk -F = {'print $2'}`\np_artifact=`egrep artifactId ${PROJECT_POM_PROPERTIES_FILE} | awk -F = {'print $2'}`\np_projectKey=`echo $p_artifact | tr -cd '[:alnum:]'` \n\necho \"${p_group}:${p_artifact}:${p_extension}:${p_version}\"\n\necho \"##vso[task.setvariable variable=project.group;]$p_group\"\n\necho \"##vso[task.setvariable variable=project.name;]$p_artifact\"\n\necho \"##vso[task.setvariable variable=project.version;]$p_version\"\n\necho \"##vso[task.setvariable variable=project.extension;]$p_extension\"\n\necho \"##vso[task.setvariable variable=project.key;]$p_projectKey\"\n\necho \"##vso[task.setvariable variable=project.file;]${PROJECT_FILE}\"\n\nif [[ ! -z ${PROJECT_RELEASE} ]] && ([ ${PROJECT_RELEASE} == false ] || [ ${PROJECT_RELEASE} == true ]) ; then\n\necho \"##vso[task.setvariable variable=project.release;]${PROJECT_RELEASE}\"\n\nelse\n\necho \"##vso[task.setvariable variable=project.release;]true\"\n\nif [[ ${p_version} == *\"SNAPSHOT\"* ]]; then\n  echo \"##vso[task.setvariable variable=project.release;]false\"\nfi\n\nfi\n\necho \"##vso[task.setvariable variable=POM_PATH;]pom.xml\"\n\n"
      failOnStderr: true
  - task: Bash@3
    displayName: Recupera repositório nexus
    inputs:
      targetType: inline
      script: >-
        #tudo que não for padrão VEC é snapshot

        if [ $(valida.vec) = true ]; then

        NEXUS_URL=$(NEXUS_URL_MAVEN_RELEASE)

        else

        NEXUS_URL=$(NEXUS_URL_MAVEN_SNAPSHOT)

        fi



        p_repository=`echo ${NEXUS_URL##*/}`

        echo "##vso[task.setvariable variable=project.repository;]$p_repository"
  - task: DownloadSecureFile@1
    displayName: Download secure file
    inputs:
      secureFile: d2041121-de1c-45da-9c21-5e8a73c00647
  - task: Bash@3
    displayName: Definindo Linguagem de Programação
    inputs:
      targetType: inline
      script: >
        #!/bin/bash

        set -o errexit

        set -o nounset

        set -o pipefail


        cd $(Build.SourcesDirectory)

        for file in pom.xml angular.json tsconfig.json package.json project.ini *.csproj *.sln

        do
           f_language=`find . -maxdepth 3 -name "${file}" -exec basename {} \; | head -n 1`
           if [[ "${f_language}" == pom.xml ]]
            then
                p_language=java
                break
           elif [[ "${f_language}" == angular.json ]] || [[ "${f_language}" == tsconfig.json ]]
                 then
                    p_language=angular
                break
           elif [[ "${f_language}" == package.json ]]
             then
                    p_language=nodejs
                break
           elif [[ "${f_language}" == project.ini ]]
             then
                    p_language=php
                break
           elif [[ "${f_language}" == *".csproj" ]] || [[ "${f_language}" == *".sln" ]]
             then
                    p_language=dotnet
                break
             else
                echo "Não foi possivel determinar a linguagem da aplicação do codigo fonte"
                   p_language=null
           fi
        done


        echo "Linguagem de Programação:" $p_language

        echo "##vso[task.setvariable variable=p_language;]$p_language"



        RepositoryName=`(echo "$(REPO_FINAL_NAME)" | tr '[[:upper:]]' '[[:lower:]]')`

        echo "##vso[task.setvariable variable=REPOSITORIO;]$RepositoryName"
  - task: Bash@3
    displayName: Verifica se pacote existe no binario.caixa
    inputs:
      targetType: inline
      script: "if [ $(valida.vec) = true ]; then\n\nreplace=\"\\/\"\n\np_name=\"$(project.name)\"\np_version=\"$(project.version)\"\np_extension=\"$(project.extension)\"\np_group=$(project.group) || true\np_group=`[ -z \"$p_group\" ] && echo \"\"br.gov.caixa.$p_name\"\" || echo \"$p_group\"`\np_group=`echo $p_group | awk -F \":\" '{print $1}' | sed -e \"s/\\./${replace}/g\"`\n\np_group=`[ ! -z \"$p_group\" ] && echo \"/$p_group\"`\n	\np_version=$BUILD_SOURCEBRANCHNAME	\n\n	p_version=`echo \"${p_version}\" | sed -r 's/([A-Z]+)//g'`\n        [[ $p_version = *- ]] && p_version=`echo $p_version | sed 's/.$//'`\n\n	p_file=\"$p_name-$p_version.$p_extension\"\n\n       echo $(NEXUS_URL_MAVEN_RELEASE)/$p_group/$p_name/$p_version/$p_file\n	response=`curl -s --head $(NEXUS_URL_MAVEN_RELEASE)/$p_group/$p_name/$p_version/$p_file | head -n 1 | grep \"HTTP/1.[01] [234]..\"`\n\n	code=`echo $response | awk '{print $2}'` \n\n	if [ ${code} = \"200\" ]; then\n		echo \"Pacote com identificador $BUILD_SOURCEBRANCHNAME já existe no repositório, por favor compile utilizando outra TAG\";\n		exit 1\n	fi\nfi"
  - task: Bash@3
    displayName: Run Code Analisis
    condition: and(ne(variables['sonar_disable'], 'true'), succeeded())
    inputs:
      targetType: inline
      script: >-
        #!/bin/bash


        if [[ "$(p_language)" != "dotnet" ]]

        then


        p_name=$(REPO_FINAL_NAME)

        p_version=$(project.version)

        p_projectKey=$(REPO_FINAL_NAME)


        #p_properties=`echo $(SONAR_PROPERTIES)`

        #echo "SONAR_PROPERTIES" $(SONAR_PROPERTIES)

        #echo "p_properties" $p_properties


        echo sonar-scanner -Dsonar.host.url=$(SONAR_URL) -Dsonar.login=$(SONAR_LOGIN) -Dsonar.password=$(SONAR_PASSWORD) -Dsonar.projectKey=$p_projectKey -Dsonar.projectName=$p_name -Dsonar.projectVersion=$p_version -Dsonar.sources=. $(SONAR_PROPERTIES)


        sonar-scanner -Dsonar.host.url=$(SONAR_URL) -Dsonar.login=$(SONAR_LOGIN) -Dsonar.password=$(SONAR_PASSWORD) -Dsonar.projectKey=$p_projectKey -Dsonar.projectName=$p_name -Dsonar.projectVersion=$p_version -Dsonar.sources=. $(SONAR_PROPERTIES)


        fi
  - task: Bash@3
    displayName: Publish Quality Gate Result
    condition: and(ne(variables['sonar_disable'], 'true'), succeeded())
    timeoutInMinutes: 5
    inputs:
      targetType: inline
      script: >-
        #!/bin/bash


        if [[ "$(p_language)" != "dotnet" ]]

        then


        cd $(Build.SourcesDirectory)


        REPORT_PATH=".scannerwork/report-task.txt"

        CE_TASK_ID_KEY="ceTaskId="


        SONAR_INSTANCE=$(SONAR_URL)

        SONAR_ACCESS_LOGIN=$(SONAR_LOGIN)

        SONAR_ACCESS_PASSWORD=$(SONAR_PASSWORD)

        SLEEP_TIME=5


        echo "QG Script --> Using SonarQube instance ${SONAR_INSTANCE}"

        echo "QG Script --> Using SonarQube access login ${SONAR_ACCESS_LOGIN}"


        # get the compute engine task id

        ce_task_id=`cat $REPORT_PATH | grep $CE_TASK_ID_KEY | cut -d'=' -f2`

        echo "QG Script --> Using task id of ${ce_task_id}"


        if [ -z "$ce_task_id" ]; then
           echo "QG Script --> No task id found"
           exit 1
        fi


        # grab the status of the task

        # if CANCELLED or FAILED, fail the Build

        # if SUCCESS, stop waiting and grab the analysisId

        wait_for_success=true


        while [ "${wait_for_success}" = "true" ]

        do

          ce_status=`curl --connect-timeout 3 --max-time 7 --retry 7 --retry-delay 0 --retry-max-time 50 -s -u ${SONAR_ACCESS_LOGIN}:${SONAR_ACCESS_PASSWORD} "${SONAR_INSTANCE}"/api/ce/task?id=${ce_task_id} | jq -r .task.status`

          echo "QG Script --> Status of SonarQube task is ${ce_status}"

          if [ "${ce_status}" = "CANCELLED" ]; then
            echo "QG Script --> SonarQube Compute job has been cancelled - exiting with error"
            exit 1
          fi

          if [ "${ce_status}" = "FAILED" ]; then
            echo "QG Script --> Ocorrência prevista na TE102 - Não atendimento aos critérios de qualidade"
            exit 1
          fi

          if [ "${ce_status}" = "SUCCESS" ]; then
            wait_for_success=false
          fi

          sleep "${SLEEP_TIME}"

        done


        ce_analysis_id=`curl --connect-timeout 3 --max-time 7 --retry 7 --retry-delay 0 --retry-max-time 50 -s -u ${SONAR_ACCESS_LOGIN}:${SONAR_ACCESS_PASSWORD} $SONAR_INSTANCE/api/ce/task?id=$ce_task_id | jq -r .task.analysisId`

        echo "QG Script --> Using analysis id of ${ce_analysis_id}"


        # get the status of the quality gate for this analysisId

        qg_status=`curl --connect-timeout 3 --max-time 7 --retry 7 --retry-delay 0 --retry-max-time 50 -s -u ${SONAR_ACCESS_LOGIN}:${SONAR_ACCESS_PASSWORD} $SONAR_INSTANCE/api/qualitygates/project_status?analysisId="${ce_analysis_id}" | jq -r .projectStatus.status`

        echo "QG Script --> Quality Gate status is ${qg_status}"


        if [ "${qg_status}" != "OK" ]; then
          echo "##[error]QG Script --> Ocorrência prevista na TE102 - Não atendimento aos critérios de qualidade"
          exit 1
        fi


        fi
      failOnStderr: true
  - task: Bash@3
    displayName: Definindo Version no Fortify
    enabled: False
    inputs:
      targetType: inline
      script: >
        #!/bin/bash


        #set -x


        extrair_versao() {

        echo "$1" | grep -oE '^[0-9]+(\.[0-9]+){0,2}'

        }

        if [[ -n "$(version.app)" && "$(version.app)" =~ ^[0-9] ]] || [[ -n "$(versionApp)" && "$(versionApp)" =~ ^[0-9] ]]

        then

        FORTIFY_VERSION_BUILD=$(extrair_versao "$(version.app)" || extrair_versao "$(versionApp)" )

        if [[ -n "$(Agent.ReleaseDirectory)" && -n "$(Release.PrimaryArtifactSourceAlias)" ]]

        then

        Build_SourcesDirectory="$(Agent.ReleaseDirectory)/$(Release.PrimaryArtifactSourceAlias)"

        echo "##vso[task.setvariable variable=Build.SourcesDirectory;]$Build_SourcesDirectory"

        fi

        else

        FORTIFY_VERSION_BUILD=$(Build.BuildNumber)

        fi

        echo "##vso[task.setvariable variable=FORTIFY_VERSION_BUILD;]$FORTIFY_VERSION_BUILD"

        echo "FORTIFY_VERSION_BUILD=$FORTIFY_VERSION_BUILD"
  - task: Bash@3
    displayName: Checagem de bypass
    condition: and(succeeded(), ne(variables['p_language'], 'dotnet'))
    enabled: False
    inputs:
      targetType: inline
      script: "#!/bin/bash\n\n#set -x\nif [ ! -z \"$(fortify_disable)\" ] && [ $(fortify_disable) = \"true\" ];\nthen\necho - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - \necho Análise do fortify encontra-se desabilitada, procure imediatamente o suporte da CESTI36 para que este passo seja habilitado. \necho Bypass a partir de 2024 somente com autorização da GECMI.\necho - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - \nreturn 1 2>/dev/null\nexit 1\nelif [ $(fortify_disable) = \"gecmi\" ];\nthen\necho Bypass autorizado pela GECMI.\nelse\necho Projeto habilitado para análise do fortify.\nfi"
  - task: Bash@3
    displayName: Definindo variáveis Fortify
    condition: and(succeeded(), ne(variables['fortify_disable'], 'gecmi'))
    enabled: False
    timeoutInMinutes: 2
    inputs:
      targetType: inline
      script: >-
        #!/bin/bash

        set -o errexit

        set -o nounset

        set -o pipefail

        #set -x


        GitRepositoryName=$(Build.Repository.Name)

        DefinitionName=$(Build.DefinitionName)


        RepositoryName=`(echo "$GitRepositoryName" | tr '[[:upper:]]' '[[:lower:]]')`

        echo "##vso[task.setvariable variable=REPOSITORIO;]$RepositoryName"

        ProjectName=`(echo "$GitRepositoryName" | tr '[[:upper:]]' '[[:lower:]]' | cut -f1 -d"-")`

        echo "##vso[task.setvariable variable=PROJETO;]$ProjectName"


        echo "Definindo liguagem de programação"

        cd $(Build.SourcesDirectory)

        for file in pom.xml angular.json tsconfig.json package.json project.ini *.csproj *.sln build.gradle

        do
           f_language=`find . -maxdepth 3 -name "${file}" -exec basename {} \; | head -n 1`
           if [[ "${f_language}" == pom.xml ]]
            then
                p_language=java
                break
           elif [[ "${f_language}" == angular.json ]] || [[ "${f_language}" == tsconfig.json ]]
                 then
                    p_language=angular
                break
           elif [[ "${f_language}" == package.json ]]
             then
                    p_language=nodejs
                break
           elif [[ "${f_language}" == project.ini ]]
             then
                    p_language=php
                break
           elif [[ "${f_language}" == *".csproj" ]] || [[ "${f_language}" == *".sln" ]]
             then
                    p_language=dotnet
                break
        elif [[ "${f_language}" == "build.gradle" ]]

        then

        p_language=android

        break
             else
                echo "Não foi possivel determinar a linguagem da aplicação do codigo fonte"
                   p_language=null
           fi
        done


        echo "Linguagem de Programação:" $p_language


        echo "##vso[task.setvariable variable=p_language;]$p_language"


        p_lang=`echo "${p_language}" | sed 's/[[:punct:]]\+$//'`

        echo "Liguagem de programação: $p_lang"


        if [ $p_language == null ]
         then
           echo "Não foi possivel definir a linguagem de programação deste codigo fonte"
           exit 1
        fi


        echo "Autenticando no Fortify e adquirindo token"
        	get_token=`curl -s --user $(FORTIFY_USER):$(FORTIFY_PASS) -k -X POST -H "Content-Type:application/json" -d '{"type": "UnifiedLoginToken"}' '$(FORTIFY_API)/tokens'`
            token=`echo $get_token | jq -r '.data.token'`
        	token_id=`echo $get_token | jq -r '.data.id'`
        	response=`echo $get_token | jq -r '.responseCode'`
        	    if [[ $response != 201 ]]
                then
                    echo "Ocorreu um erro ao realizar ação no Fortify Status_code: $response"
        			exit 1
                fi

        echo "##vso[task.setvariable variable=token]$token"

        echo "##vso[task.setvariable variable=token_id]$token_id"
  - task: script-retryer@0
    displayName: Criando Application no Fortify
    condition: and(succeeded(), ne(variables['fortify_disable'], 'gecmi'), ne(variables['p_language'], 'dotnet'))
    enabled: False
    timeoutInMinutes: 2
    inputs:
      targetType: inline
      script: "#!/bin/bash\n\necho \"Repo: $(REPOSITORIO)\"\n#Corrigir caracter bizzaro que o ads coloca (java'\\''')\np_lang=`echo '$(p_language)' | sed 's/[[:punct:]]\\+$//'`\necho \"Liguagem de programação: $p_lang\"\n\necho \"Iniciando fluxo de criação de Application no Fortify\"\nlista_projeto=`curl -k -s -X POST \"$(FORTIFY_API)/projects/action/test\" -H \"Authorization:FortifyToken $(token)\" -H \"accept: application/json\" -H \"Content-Type: application/json\" -d \"{ \\\"applicationName\\\": \\\"$(REPOSITORIO)\\\"}\"`\nlprojeto=`echo $lista_projeto | jq -r '.data.found'`\nresponse=`echo $lista_projeto | jq -r '.responseCode'`\n        if [[ $response != 200 ]]\n        then\n            echo \"Ocorreu um erro ao realizar ação no Fortify Status_code: $response\"\n			exit 1\n        fi\necho \"Listando Application ==>\"$lprojeto\necho \"Listando Application response ==> \"$response\nif [ $lprojeto = false ]\nthen \n  echo \"Criando o Application no Fortify\"\n	cria_projeto=`curl -s -k -X POST -H \"Content-Type:application/json\" -H \"Authorization:FortifyToken $(token)\" -d '{\"name\":\"'$(FORTIFY_VERSION_BUILD)'\",\"description\":\"\",\"active\":true,\"project\":{\"name\":\"'$(REPOSITORIO)'\",\"description\":\"\",\"issueTemplateId\":\"Prioritized-HighRisk-Project-Template\"},\"issueTemplateId\":\"Prioritized-HighRisk-Project-Template\",\"committed\":true}' '$(FORTIFY_API)/projectVersions'`\n	idFortify=`echo $cria_projeto | jq -r '.data.id'`\n    response=`echo $cria_projeto | jq -r '.responseCode'`\n	    if [[ $response != 201 ]]\n        then\n            echo \"Ocorreu um erro ao realizar ação no Fortify Status_code: $response\"\n			exit 1\n        fi	\n    echo \"Project Fortify ID ==> \"$idFortify\n    echo \"Project Fortify ID response ==> \"$response\nsleep 10	\n    #id_versao=`curl -k -s \"$(FORTIFY_API)/projectVersions?start=0&limit=2000&fulltextsearch=false\" -H \"Authorization:FortifyToken $(token)\" -H \"accept: application/json\" -H \"Content-Type: application/json\"`\n	#iversao=`echo $id_versao | jq -r '.data[] | select(.name==\"$(FORTIFY_VERSION_BUILD)\" and .project.name==\"$(REPOSITORIO)\") | .id'`\n	#response=`echo $id_versao | jq -r '.responseCode'`\n	#	if [[ $response != 200 ]]\n    #    then\n    #        echo \"Ocorreu um erro ao realizar ação no Fortify Status_code: $response\"\n	#		exit 1\n    #    fi	\n	#echo \"Project Version ID ==> \"$iversao\n	#echo \"Project Version ID response ==> \"$response\n	\n	if [ $p_lang == android ]\n	then\n		cat /opt/ads-agent/javaDefault.json | sed -e 's/idFortify/'$idFortify'/g' | curl -s -k -X POST -H \"Content-Type:application/json\" -H \"Authorization:FortifyToken $(token)\" -d @- '$(FORTIFY_API)/bulk'	\n	elif [ $p_lang == java ]\n	  then\n	     cat /opt/ads-agent/javaDefault.json | sed -e 's/idFortify/'$idFortify'/g' | curl -s -k -X POST -H \"Content-Type:application/json\" -H \"Authorization:FortifyToken $(token)\" -d @- '$(FORTIFY_API)/bulk'\n	elif [ $p_lang == angular ] || [ $p_lang == nodejs ]\n	   then\n	     cat /opt/ads-agent/javascriptDefault.json | sed -e 's/idFortify/'$idFortify'/g' | curl -s -k -X POST -H \"Content-Type:application/json\" -H \"Authorization:FortifyToken $(token)\" -d @- '$(FORTIFY_API)/bulk'\n	elif [ $p_lang == php ]\n	   then\n	     cat /opt/ads-agent/phpDefault.json | sed -e 's/idFortify/'$idFortify'/g' | curl -s -k -X POST -H \"Content-Type:application/json\" -H \"Authorization:FortifyToken $(token)\" -d @- '$(FORTIFY_API)/bulk'\n	fi\nelse \n  echo \"A Application $(REPOSITORIO) já esta criada no Fortify\"	\nfi"
      delay: 10
      retryTimes: 3
  - task: Bash@3
    displayName: Criando Version no Fortify
    condition: and(succeeded(), ne(variables['fortify_disable'], 'gecmi'), ne(variables['p_language'], 'dotnet'))
    enabled: False
    timeoutInMinutes: 2
    inputs:
      targetType: inline
      script: "#!/bin/bash\n\necho \"Repo: $(REPOSITORIO)\"\n#Corrigir caracter bizzaro que o ads coloca (java'\\''')\np_lang=`echo '$(p_language)' | sed 's/[[:punct:]]\\+$//'`\necho \"Liguagem de programação: $p_lang\"\n\necho \"Criando nova Application Version\"\nlista_versao=`curl -k -s -X POST \"$(FORTIFY_API)/projectVersions/action/test\" -H \"Authorization:FortifyToken $(token)\" -H \"accept: application/json\" -H \"Content-Type: application/json\" -d \"{ \\\"projectName\\\": \\\"$(REPOSITORIO)\\\", \\\"projectVersionName\\\": \\\"$(FORTIFY_VERSION_BUILD)\\\"}\"`\nlversao=`echo $lista_versao | jq -r '.data.found'`\nresponse=`echo $lista_versao | jq -r '.responseCode'`\n        if [[ $response != 200 ]]\n        then\n            echo \"Ocorreu um erro ao realizar ação no Fortify Status_code: $response\"\n			exit 1\n        fi\necho \"listar_versão ==>\"$lversao\necho \"listar_versão response ==>\"$response\nif [ $lversao = false ]\nthen \n  echo \"Criando o versão no fortify para o projeto '$(REPOSITORIO)'\"\n  id_project=`curl -k -s \"$(FORTIFY_API)/projects?start=0&limit=2000&fulltextsearch=false\" -H \"Authorization:FortifyToken $(token) \" -H \"accept: application/json\" -H \"Content-Type: application/json\"`\n    iproject=`echo $id_project | jq -r '.data[] | select (.name==\"$(REPOSITORIO)\") | .id'`\n    response=`echo $id_project | jq -r '.responseCode'`\n	    if [[ $response != 200 ]]\n        then\n            echo \"Ocorreu um erro ao realizar ação no Fortify Status_code: $response\"\n			exit 1\n        fi	\n    echo \"Project ID ==> \"$iproject\n    echo \"Project ID response ==> \"$response\nsleep 8	\n  cria_versao=`curl -s -k -X POST -H \"Content-Type:application/json\" -H \"Authorization:FortifyToken $(token)\" -d '{\"name\":\"'$(FORTIFY_VERSION_BUILD)'\",\"description\":\"\",\"active\":true,\"committed\":true,\"project\":{\"name\":\"'$(REPOSITORIO)'\",\"description\":null,\"issueTemplateId\":\"Prioritized-HighRisk-Project-Template\",\"id\":'$iproject'},\"issueTemplateId\":\"Prioritized-HighRisk-Project-Template\"}' '$(FORTIFY_API)/projectVersions'`\n  	cversion=`echo $cria_versao | jq -r '.data.id'`\n    response=`echo $cria_versao | jq -r '.responseCode'`\n	    if [[ $response != 201 ]]\n        then\n            echo \"Ocorreu um erro ao realizar ação no Fortify Status_code: $response\"\n			exit 1\n        fi	\n    echo \"Criando Application Version ==> \"$cversion\n    echo \"Criando  Application Version response ==> \"$response\nsleep 8\necho \"Atribuindo atributos a Application Version\"$cversion\necho \"Linguagem de programacao $p_lang\"\n 	if [ $p_lang == android ]\n	  then\ncat /opt/ads-agent/javaDefault.json | sed -e 's/idFortify/'$cversion'/g' | curl -s -k -X POST -H \"Content-Type:application/json\" -H \"Authorization:FortifyToken $(token)\" -d @- '$(FORTIFY_API)/bulk'\n 	elif [ $p_lang == java ]\n	  then\n	     cat /opt/ads-agent/javaDefault.json | sed -e 's/idFortify/'$cversion'/g' | curl -s -k -X POST -H \"Content-Type:application/json\" -H \"Authorization:FortifyToken $(token)\" -d @- '$(FORTIFY_API)/bulk'\n	elif [ $p_lang == angular ] || [ $p_lang == nodejs ]\n	   then\n	     cat /opt/ads-agent/javascriptDefault.json | sed -e 's/idFortify/'$cversion'/g' | curl -s -k -X POST -H \"Content-Type:application/json\" -H \"Authorization:FortifyToken $(token)\" -d @- '$(FORTIFY_API)/bulk'\n	elif [ $p_lang == php ]\n	   then\n	     cat /opt/ads-agent/phpDefault.json | sed -e 's/idFortify/'$cversion'/g' | curl -s -k -X POST -H \"Content-Type:application/json\" -H \"Authorization:FortifyToken $(token)\" -d @- '$(FORTIFY_API)/bulk'\n	fi\nelse \n  echo \"A Application Version: $(FORTIFY_VERSION_BUILD) já esta criada no Fortify\"	\nfi\necho \"##vso[task.setvariable variable=lista_versao;]$lista_versao\"\necho $lista_versao"
  - task: Bash@3
    displayName: Herdando Atributos
    condition: and(succeeded(), ne(variables['fortify_disable'], 'gecmi'), ne(variables['p_language'], 'dotnet'))
    enabled: False
    inputs:
      targetType: inline
      filePath: /opt/ads-agent/fortify_analisis.sh
      script: >
        #!/bin/bash

        #set -x

        echo "LANGUAGE $(p_language)"


        identificar_projeto=$(curl -s -k --location --request GET "$(FORTIFY_API)/projects?q=name:$(REPOSITORIO)" \

        --header "Accept: application/json" \

        --header "Authorization: FortifyToken $(FORTIFY_APITOKEN)" | jq '.data[].id')


        identificar_versao=`curl -k -s -X GET "$(FORTIFY_API)/projects/$identificar_projeto/versions?orderby=creationDate&limit=0" \

        -H "Authorization: FortifyToken $(FORTIFY_APITOKEN)" \

        -H "accept: application/json"`


        if [[ $(echo "$(lista_versao)" | grep "found":true) ]]

        then

        IdUltimaVersao=`echo "$identificar_versao" | jq -r '.data[-1].id'`

        else

        IdUltimaVersao=`echo "$identificar_versao" | jq -r '.data[-2].id'`

        fi


        IdAtualVersao=`curl -s -k --location --request GET "$(FORTIFY_API)/projects/$identificar_projeto/versions?orderby=creationDate&limit=0" --header "Accept: application/json" --header "Authorization: FortifyToken $(FORTIFY_APITOKEN)" | jq '.data[] | select(.name == "$(FORTIFY_VERSION_BUILD)") | .id'`

        echo "IdUltimaVersao: $IdUltimaVersao"

        echo "IdAtualVersao: $IdAtualVersao"

        version_count=`echo "$identificar_versao" | jq -r '.count'`

        if [[ $version_count -eq 1 ]]

        then
        	echo "Esta e a primeira versao, skip na heranca de atributos"
        	exit 0
        elif [[ "$IdUltimaVersao" == "$IdAtualVersao" ]]

        then
                echo "Esta e a ultima versao, skip na heranca de atributos"
        	exit 0
        else
        	echo "Fazendo a Heranca de Atributo da ultima para a versao atual"
        	refresh_audit=$(curl -o /dev/null -w "%{http_code}" -k -s -L -X POST "$(FORTIFY_API)/projectVersions/action/refresh" \
        	-H "accept: application/json" \
        	-H "Content-Type: application/json" \
        	-H "Authorization: FortifyToken $(token)" \
        	-d '{
        	 "projectVersionIds": [ '$IdUltimaVersao' ]
        	}')
        	if [[ $refresh_audit -ne 200 ]]
        	then
        		echo "Skip refresh"
        	else
        		echo "Refresh da ultima versao realizado com sucesso"
                        sleep 20
        	fi
        	replicar_atributos=$(curl -o /dev/null -w "%{http_code}" -k -s -L -X POST "$(FORTIFY_API)/projectVersions/action/copyCurrentState" \
        	-H "accept: application/json" \
        	-H "Content-Type: application/json" \
        	-H "Authorization: FortifyToken $(token)" \
        	-d '{
        	 "previousProjectVersionId": '$IdUltimaVersao',
        	 "projectVersionId": '$IdAtualVersao'
        	}')
        	if [[ $replicar_atributos -ne 200 ]]
        	then
        		echo "Erro ao copiar application state da ultima para a versao atual"
        		exit 1
        	else
        		echo "Replicado application state da ultima para a versao atual"
        	fi
        	response_acessos=$(curl -k -s -L -X GET "$(FORTIFY_API)/projectVersions/$IdUltimaVersao/authEntities" \
        	-H "accept: application/json" \
        	-H "Authorization: FortifyToken $(token)")
                 response_acessos_code=`echo $response_acessos | jq -r '.responseCode'`
        	if [[ $response_acessos_code -ne 200 ]]
        	then
        		echo "Erro ao capturar response de acessos da ultima versao"
        		exit 1
        	else
        		echo "Identificado o response de acesso da ultima versao"
        	fi
                 response_acessos_data=`echo $response_acessos | jq -r '.data'`
        	replicar_acessos=$(curl -o /dev/null -w "%{http_code}" -k -s -L -X PUT "$(FORTIFY_API)/projectVersions/$IdAtualVersao/authEntities" \
        	-H "accept: application/json" \
        	-H "Content-Type: application/json" \
        	-H "Authorization: FortifyToken $(token)" \
        	-d "$response_acessos_data")
        	if [[ $replicar_acessos -ne 200 ]]
        	then
        		echo "Erro ao atualizar acessos da versao atual"
        		exit 1
        	else
        		echo "Replicado acessos para a versao atual"
        	fi
        fi
  - task: Bash@3
    displayName: Iniciando Análise no Fortify
    condition: and(succeeded(), ne(variables['fortify_disable'], 'gecmi'), ne(variables['p_language'], 'dotnet'))
    enabled: False
    inputs:
      targetType: inline
      filePath: /opt/ads-agent/fortify_analisis.sh
      script: "#!/bin/bash\n\nexport PATH=/opt/apache-maven/apache-maven-3.8.5/bin:$PATH\nmvn -version\n\necho \"Iniciando Fortify Clean, Translate e Analysis\" \n\np_lang=`echo '$(p_language)' | sed 's/[[:punct:]]\\+$//'`\necho \"LANG $p_lang\"\n\nif [ $p_lang == java ]\n  then\n      \n	  DIR=$(Agent.BuildDirectory)/fortify\n     \n	  if [ -d \"$DIR\" ]; then\n		  echo \"Pasta ${DIR} existe...\"\n		  cd ${DIR}\n	  else\n	    DIR=$(Build.SourcesDirectory)\n	  fi\n	  \n	  if [ $POM_PATH ]\n	   then\n	     POM=`dirname $POM_PATH`\n	  cd ${DIR}/$POM\n	   else\n	  cd ${DIR}\n      fi\n\nscancentral -url $(SCANCENTRAL_URL) start -bt mvn -pool $(FORTIFY_POOL_SILVER_NOVO) -application $(REPOSITORIO) -version $(FORTIFY_VERSION_BUILD) -uptoken $(FORTIFY_UPTOKEN) -fprssc $(Build.BuildId).fpr -upload\n\nelif [ $p_lang == android ]\nthen\ncd $(Build.SourcesDirectory)\nchmod +x gradlew\nsed -i  \"s,distributionUrl=.*,distributionUrl=file:///opt/ferramentas/gradle/gradle-$(GradleVersion)-all.zip,\" gradle/wrapper/gradle-wrapper.properties\nscancentral arguments -o -targs \"-exclude './**/build/**/*'\"\nscancentral -url $(SCANCENTRAL_URL) start -bt gradle -bc $(FORTIFY_BUILD) -skipBuild -pool $(FORTIFY_POOL_GOLD_NOVO) -application $(REPOSITORIO) -version $(FORTIFY_VERSION_BUILD) -uptoken $(FORTIFY_UPTOKEN) -fprssc $(Build.BuildId).fpr -upload\n\nelse\n      if [ $PACKAGE_JSON_PATH ]\n	    then\n          cd $PACKAGE_JSON_PATH\n		else\n		  cd $(Build.SourcesDirectory)\n		fi\n	  scancentral arguments -o -targs \"-Dcom.fortify.sca.exclude.unimported.node.modules 'true'\" -targs \"-exclude './**/node_modules/**/*'\" -targs \"-exclude './**/*.min.js'\" -targs \"-exclude './**/dist/**/*'\"\n          scancentral -url $(SCANCENTRAL_URL) start -bt none -pool $(FORTIFY_POOL_GOLD_NOVO) -application $(REPOSITORIO) -version $(FORTIFY_VERSION_BUILD) -uptoken $(FORTIFY_UPTOKEN) -fprssc $(Build.BuildId).fpr -upload\nfi\n"
  - task: Bash@3
    displayName: Revogando Token
    condition: always()
    enabled: False
    inputs:
      targetType: inline
      filePath: /opt/ads-agent/fortify_analisis.sh
      script: >-
        #!/bin/bash

        set -o errexit

        set -o nounset

        set -o pipefail

        #set -x


        echo "Verificando se o token foi criado."

        if [[ -n $(token_id) ]]

        then
            echo "Revogando token"
        	delete_token=`curl -s --user $(FORTIFY_USER):$(FORTIFY_PASS) -k -X DELETE -H "Content-Type:application/json" '$(FORTIFY_API)/tokens/$(token_id)'`
        	response=`echo $delete_token | jq -r '.responseCode'`
        	    if [[ $response != 200 ]]
                    then
                        echo "Ocorreu um erro ao revogar o token no Fortify Status_code: $response"
        		#exit 1
                    fi
        else
          echo "Token não foi criado. Favor verificar se alguma task apresenta erro."
        fi
  - task: CmdLine@2
    displayName: 'SAST: Limpando MVN_GOAL'
    condition: and(eq(variables['valida.vec'], 'true'), succeeded(), ne(variables['fortify_disable'], 'gecmi'), eq(variables['p_language'], 'java'))
    inputs:
      script: "if [[ -n $MVN_GOAL ]]; then\n  FTFY_MVN_GOAL=\"$(\n    printf '%s' \"$MVN_GOAL\" |\n      sed -E '\n        s/(^|[[:space:]])-DskipTests=(true|false)([[:space:]]|$)/ /g;\n        s/(^|[[:space:]])(clean|install)([[:space:]]|$)/ /g;\n        s/[[:space:]]+/ /g;\n        s/^ //; s/ $//\n      '\n  )\"\n\n  # Força -DskipTests=true no final para garantir que testes não sejam executados em análise\n  FTFY_MVN_GOAL=\"${FTFY_MVN_GOAL:+$FTFY_MVN_GOAL }-DskipTests=true\"\n  echo \"##vso[task.setvariable variable=FTFY_MVN_GOAL]$FTFY_MVN_GOAL\"\n  echo MVN_GOAL: $FTFY_MVN_GOAL  \nfi"
  - task: CmdLine@2
    displayName: 'SAST: Define Variáveis'
    condition: and(eq(variables['valida.vec'], 'true'), succeeded(), ne(variables['fortify_disable'], 'gecmi'))
    inputs:
      script: >-
        echo "Verificando a existência das variáveis de comunidade..."

        if [[ -z $FORTIFY_SENSOR_POOL ]]; then
            echo "##vso[task.logissue type=error;]Não foi possível determinar a comunidade responsável por este sistema. Entre em contato com a CESET10 para vincular seu pipeline ao Variable Group correspondente à sua comunidade."
            exit 1
        fi


        if [[ -n $FORTIFY_SOBRESCREVE_POOL ]]; then
          echo "##vso[task.setvariable variable=FORTIFY_SENSOR_POOL;]$FORTIFY_SOBRESCREVE_POOL"
          echo POOL: $FORTIFY_SOBRESCREVE_POOL
        fi


        #######


        JAVA_HOME_17_X64=/usr/java/open-jdk-17.0.8

        echo "##[command]echo \$JAVA_HOME_17_X64"

        echo JAVA_HOME_17_X64: $JAVA_HOME_17_X64


        echo "##vso[task.setvariable variable=JAVA_HOME_17_X64;]$JAVA_HOME_17_X64"


        if [[ -n $MVN_GOAL ]]; then

        echo MVN_GOAL: $FTFY_MVN_GOAL

        fi


        #######


        echo Build.Repository.Name=$(Build.Repository.Name)

        echo Build.DefinitionName=$(Build.DefinitionName)

        echo Build.BuildNumber=$(Build.BuildNumber)

        echo Build.BuildId=$(Build.BuildId)

        echo Build.SourceBranch=$(Build.SourceBranch)

        echo Build.SourceBranchName=$(Build.SourceBranchName)

        echo Build.SourceVersion=$(Build.SourceVersion)


        echo "##[command]echo \$valida.vec"

        echo vec=$(valida.vec)


        echo "##[command]echo \$sonar_branch"

        echo branch=$sonar_branch

        if [[ $sonar_branch =~ ^INC(\d)* ]]; then
            echo "##[warning]Hotfix detectado. Aplicando bypass no Guardrail."
            echo "##vso[task.setvariable variable=guardrail.sec;]false"
        fi


        echo FORTIFY_APPLICATION=$FORTIFY_APPLICATION

        echo FORTIFY_SESSION=$FORTIFY_SESSION

        echo KEYSTORE_SECUREFILEPATH=$(KEYSTORE_SECUREFILEPATH)

        echo NODE_EXTRA_CA_CERTS=$(NODE_EXTRA_CA_CERTS)


        #verificar diretório contendo os certificados necessários para a próxima task

        #ls -lah /etc/pki/ca-trust/source/anchors/


        echo "Versão atual:"

        echo "##[command]git log --pretty=format:"%H %D" | sed -n '1p'"

        git -c safe.directory=* log --pretty=format:"%H %D" | sed -n '1p'

        echo "##[command]git describe --tags $(Build.SourceVersion)"

        git -c safe.directory=* describe --tags $(Build.SourceVersion)


        #######


        echo "Versões anteriores [tag] seguindo a branch atual:"


        FORTIFY_NEW_VERSION=`git -c safe.directory=* log --pretty=format:"%H %D" | grep -oP '(?<=tag: )[^\s]*([0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3})' | sed -n '1p'`

        FORTIFY_LAST_VERSION=`git -c safe.directory=* log --pretty=format:"%H %D" | grep -oP '(?<=tag: )[^\s]*([0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3})' | sed -n '2p'`

        FORTIFY_THIRD_VERSION=`git -c safe.directory=* log --pretty=format:"%H %D" | grep -oP '(?<=tag: )[^\s]*([0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3})' | sed -n '3p'`


        echo Última tag mais recente: $FORTIFY_NEW_VERSION

        echo Penúltima tag mais recente: $FORTIFY_LAST_VERSION

        echo Antepenúltima tag mais recente: $FORTIFY_THIRD_VERSION


        if [[ $FORTIFY_NEW_VERSION == null ]]; then
            echo "##[error]Incapaz de determinar a versão da aplicação."
            exit 1
        fi


        echo Validando VEC e versão...

        # A VEC dá false pois o valor $(Build.SourceBranchName) não passa o valor da tag quando o build é disparado a partir da branch.

        if [[ $(valida.vec) == false ]]; then

        echo "O nome de versão ' $(Build.SourceBranchName) ' NÃO ATENDE aos parâmetros da VEC."

        fi

        if [[ -n $FORTIFY_NEW_VERSION ]]; then
          FORTIFY_NEW_VERSION=`echo $FORTIFY_NEW_VERSION | grep -oP $(FORTIFY_REGEX)`
          FORTIFY_LAST_VERSION=`echo $FORTIFY_LAST_VERSION | grep -oP $(FORTIFY_REGEX)`
        else

        if [[ -n $FORTIFY_LAST_VERSION ]]; then
          FORTIFY_NEW_VERSION="develop"
        else
          FORTIFY_NEW_VERSION=`echo $FORTIFY_LAST_VERSION | grep -oP $(FORTIFY_REGEX)`
          FORTIFY_LAST_VERSION=`echo $FORTIFY_THIRD_VERSION | grep -oP $(FORTIFY_REGEX)`
        fi

        fi


        echo "##[debug]Seu resultado será publicado no Fortify sob a Versão de nome: ' $FORTIFY_APPLICATION:$FORTIFY_NEW_VERSION '"


        #######


        FORTIFY_FPR_NAME=`git -c safe.directory=* describe --tags $(Build.SourceVersion)`


        echo "##vso[task.setvariable variable=FORTIFY_NEW_VERSION]$FORTIFY_NEW_VERSION"

        echo "##vso[task.setvariable variable=FORTIFY_LAST_VERSION]$FORTIFY_LAST_VERSION"

        echo "##vso[task.setvariable variable=FORTIFY_FPR_NAME]$FORTIFY_FPR_NAME"


        #######


        echo "Agent Name: $AGENT_NAME"

        AGENT_SHORT_NAME=$(echo "$AGENT_NAME" | sed -E 's/^([a-zA-Z]+)[0-9]*\..*/\1/')


        echo "Nome curto do agente: $AGENT_SHORT_NAME"


        if [[ "$AGENT_SHORT_NAME" == "cadsvaprlx" && -n $DOTNET_VERSION ]]; then
            echo DOTNET_VERSION: $DOTNET_VERSION
            echo "##[warning]Este Agent não possui os requisitos para executar a ferramenta de SAST ( .NET 8.0 ). O Bypass do SAST será ativado."
            echo "##vso[task.setvariable variable=fortify_disable;]gecmi"
        fi


        if [[ "$AGENT_SHORT_NAME" == "cadsvaprlx" ]]; then
            CONTAINER_ENGINE=docker
            echo "##vso[task.setvariable variable=CONTAINER_ENGINE]docker"
        else
            CONTAINER_ENGINE=podman
            echo "##vso[task.setvariable variable=CONTAINER_ENGINE]podman"
        fi


        echo "##[debug]Container engine selecionado: $CONTAINER_ENGINE"
  - task: CmdLine@2
    displayName: '[MANTER] SAST: Validando a Passagem de Valores'
    enabled: False
    inputs:
      script: >-
        scancentral --version

        /opt/ads-agent/_work/_tool/scancentral/24.4.0/x64/bin/scancentral --version


        echo FORTIFY_SESSION: $FORTIFY_SESSION

        echo FORTIFY_APPLICATION: $FORTIFY_APPLICATION


        echo FORTIFY_NEW_VERSION: $FORTIFY_NEW_VERSION

        echo FORTIFY_LAST_VERSION: $FORTIFY_LAST_VERSION

        echo FORTIFY_APPLICATION-FORTIFY_NEW_VERSION

        echo $FORTIFY_APPLICATION-$FORTIFY_NEW_VERSION

        #echo FORTIFY_APPLICATION-[ dependencies.A.outputs['FORTIFY_NEW_VERSION'] ]

        #echo $FORTIFY_APPLICATION-$[ dependencies.A.outputs['FORTIFY_NEW_VERSION'] ]
  - task: CmdLine@2
    displayName: 'SAST: Cria Aplicação - Backup'
    condition: and(eq(variables['valida.vec'], 'true'), succeeded(), ne(variables['fortify_disable'], 'gecmi'))
    retryCountOnTaskFailure: 5
    enabled: False
    inputs:
      script: "command -v docker && docker --version\ncommand -v podman && podman --version\n\n#sudo usermod -aG docker $USER\n\n#ls -l /var/run/docker.sock\n\n#set -o errexit\n#set -o pipefail\n#echo Engine selecionado: $CONTAINER_ENGINE\n#echo Versão mais recente: $FORTIFY_NEW_VERSION\n#echo Versão anterior: $FORTIFY_LAST_VERSION\n\necho \"$FORTIFY_REGISTRY_PASSWORD\" | $CONTAINER_ENGINE login default-route-openshift-image-registry.apps.produtos4.caixa --username \"$FORTIFY_REGISTRY_USERNAME\" --password-stdin\n \necho FORTIFY_APPLICATION: $FORTIFY_APPLICATION\necho KEYSTORE_SECUREFILEPATH: $(KEYSTORE_SECUREFILEPATH)\nKEYSTORE_SECUREFILEPATH=$(KEYSTORE_SECUREFILEPATH)\ncp $KEYSTORE_SECUREFILEPATH $(System.DefaultWorkingDirectory)/keystore.jks\n#echo \"##vso[task.setvariable variable=KEYSTORE_SECUREFILEPATH]$KEYSTORE_SECUREFILEPATH\"\n\n# Valida Integridade do JKS (parte 1, fora do container)\necho Valida integridade do certificado FORA do container\necho \"##[command]md5sum /etc/pki/ca-trust/source/anchors/keystore-ssc24.jks\"\nmd5sum /etc/pki/ca-trust/source/anchors/keystore-ssc24.jks\necho \"##[command]md5sum $KEYSTORE_SECUREFILEPATH\"\nmd5sum $KEYSTORE_SECUREFILEPATH\necho \"##[command]md5sum $(System.DefaultWorkingDirectory)/keystore.jks\"\nmd5sum $(System.DefaultWorkingDirectory)/keystore.jks\n\n# Executa o container Fortify com as variáveis herdadas do ambiente\necho \"##[command]$CONTAINER_ENGINE --version\"\n$CONTAINER_ENGINE --version\necho \"##[command]$CONTAINER_ENGINE run -v $(System.DefaultWorkingDirectory):/src default-route-openshift-image-registry.apps.produtos4.caixa/fortify/fortify-ci-tools:7.0.0-jdk-17\"\n$CONTAINER_ENGINE run --rm \\\n  --security-opt seccomp=unconfined \\\n  --memory=12g \\\n  --memory-swap=12g \\\n  -v $(System.DefaultWorkingDirectory):/src \\\n  -w /src \\\n  -e FORTIFY_APPLICATION \\\n  -e FORTIFY_APP_VERSION=$FORTIFY_NEW_VERSION \\\n  -e FORTIFY_PREVIOUS_VERSION=$FORTIFY_LAST_VERSION \\\n  -e FORTIFY_SESSION \\\n  -e FORTIFY_URL \\\n  -e FORTIFY_CI_TOKEN \\\n  -e FORTIFY_CLIENT_AUTH_TOKEN \\\n  -e FORTIFY_SENSOR_VERSION \\\n  -e FORTIFY_SIGLA=$(Build.DefinitionName) \\\n  -e FORTIFY_COMUNIDADE \\\n  -e FORTIFY_LDAP_GROUP \\\n  default-route-openshift-image-registry.apps.produtos4.caixa/fortify/fortify-ci-tools:7.0.0-jdk-17 \\\n  bash -c \"\n    \n    echo Valida integridade do certificado DENTRO do container\n    echo md5sum /src/keystore.jks\n    md5sum /src/keystore.jks\n    \n    echo Configurando Key Store\n    fcli config truststore set \\\n      --file=/src/keystore.jks \\\n      --password=$KEYSTORE_PWD \\\n      --type=jks\n \n    echo \\\"Nome do Sistema: \\$FORTIFY_APPLICATION\\\"\n \n    echo \\\"Nome da Versão: \\$FORTIFY_APP_VERSION\\\"\n \n    echo \\\"Nome da Versão Anterior: \\$FORTIFY_PREVIOUS_VERSION\\\"\n \n   #FORTIFY_CI_TOKEN proveniente do Fortify (expira)\n   #FORTIFY_CLIENT_AUTH_TOKEN (não expira)\n    echo Login no Fortify...\n    fcli ssc session login \\\n      --url=\\$FORTIFY_URL \\\n      --token=\\$FORTIFY_CI_TOKEN \\\n      --client-auth-token=\\$FORTIFY_CLIENT_AUTH_TOKEN \\\n      --socket-timeout=10m \\\n      --connect-timeout=5m \\\n      --ssc-session=\\$FORTIFY_SESSION\n    \n \n    echo Criando aplicação no Fortify...\n    fcli ssc action run setup-appversion \\\n      --appversion=\\$FORTIFY_APPLICATION:\\$FORTIFY_APP_VERSION \\\n      --attributes=\\\"Comunidade=\\$FORTIFY_COMUNIDADE,Sigla=\\$FORTIFY_SIGLA\\\" \\\n      --add-users=\\$FORTIFY_LDAP_GROUP \\\n      --copy-from=\\$FORTIFY_APPLICATION:\\$FORTIFY_PREVIOUS_VERSION \\\n      --ssc-session=\\$FORTIFY_SESSION || true\n \n    fcli ssc action run setup-appversion \\\n      --appversion=\\$FORTIFY_APPLICATION:\\$FORTIFY_APP_VERSION \\\n      --attributes=\\\"Comunidade=\\$FORTIFY_COMUNIDADE,Sigla=\\$FORTIFY_SIGLA\\\" \\\n      --add-users=\\$FORTIFY_LDAP_GROUP \\\n      --ssc-session=\\$FORTIFY_SESSION || true\n \n    echo Atribuindo acessos ao Fortify...\n    fcli ssc appversion update \\\n      \\$FORTIFY_APPLICATION:\\$FORTIFY_APP_VERSION \\\n      --add-users=\\$FORTIFY_LDAP_GROUP \\\n      --ssc-session=\\$FORTIFY_SESSION || true\n \n    echo Logout do Fortify...\n    fcli ssc session logout \\\n      --ssc-session=\\$FORTIFY_SESSION \\\n      --no-revoke-token\n  \""
  - task: CmdLine@2
    displayName: 'SAST: Cria Aplicação'
    condition: and(eq(variables['valida.vec'], 'true'), succeeded(), ne(variables['fortify_disable'], 'gecmi'))
    retryCountOnTaskFailure: 5
    inputs:
      script: "command -v docker && docker --version\ncommand -v podman && podman --version\n\n#sudo usermod -aG docker $USER\n\n#ls -l /var/run/docker.sock\n\n#set -o errexit\n#set -o pipefail\n#echo Engine selecionado: $CONTAINER_ENGINE\n#echo Versão mais recente: $FORTIFY_NEW_VERSION\n#echo Versão anterior: $FORTIFY_LAST_VERSION\n\necho \"$FORTIFY_REGISTRY_PASSWORD\" | $CONTAINER_ENGINE login default-route-openshift-image-registry.apps.produtos4.caixa --username \"$FORTIFY_REGISTRY_USERNAME\" --password-stdin\n \necho FORTIFY_APPLICATION: $FORTIFY_APPLICATION\necho KEYSTORE_SECUREFILEPATH: $(KEYSTORE_SECUREFILEPATH)\nKEYSTORE_SECUREFILEPATH=$(KEYSTORE_SECUREFILEPATH)\ncp $KEYSTORE_SECUREFILEPATH $(System.DefaultWorkingDirectory)/keystore.jks\n#echo \"##vso[task.setvariable variable=KEYSTORE_SECUREFILEPATH]$KEYSTORE_SECUREFILEPATH\"\n\n# Valida Integridade do JKS (parte 1, fora do container)\necho Valida integridade do certificado FORA do container\necho \"##[command]md5sum /etc/pki/ca-trust/source/anchors/keystore-ssc24.jks\"\nmd5sum /etc/pki/ca-trust/source/anchors/keystore-ssc24.jks\necho \"##[command]md5sum $KEYSTORE_SECUREFILEPATH\"\nmd5sum $KEYSTORE_SECUREFILEPATH\necho \"##[command]md5sum $(System.DefaultWorkingDirectory)/keystore.jks\"\nmd5sum $(System.DefaultWorkingDirectory)/keystore.jks\n\n# Executa o container Fortify com as variáveis herdadas do ambiente\necho \"##[command]$CONTAINER_ENGINE --version\"\n$CONTAINER_ENGINE --version\necho \"##[command]$CONTAINER_ENGINE run -v $(System.DefaultWorkingDirectory):/src default-route-openshift-image-registry.apps.produtos4.caixa/fortify/fortify-ci-tools:7.0.0-jdk-17\"\n$CONTAINER_ENGINE run --rm \\\n  --security-opt seccomp=unconfined \\\n  --memory=12g \\\n  --memory-swap=12g \\\n  -v $(System.DefaultWorkingDirectory):/src \\\n  -w /src \\\n  -e FORTIFY_APPLICATION \\\n  -e FORTIFY_APP_VERSION=$FORTIFY_NEW_VERSION \\\n  -e FORTIFY_PREVIOUS_VERSION=$FORTIFY_LAST_VERSION \\\n  -e FORTIFY_SESSION \\\n  -e FORTIFY_URL \\\n  -e FORTIFY_CI_TOKEN \\\n  -e FORTIFY_CLIENT_AUTH_TOKEN \\\n  -e FORTIFY_SENSOR_VERSION \\\n  -e FORTIFY_SIGLA=$(Build.DefinitionName) \\\n  -e FORTIFY_COMUNIDADE \\\n  -e FORTIFY_LDAP_GROUP \\\n  default-route-openshift-image-registry.apps.produtos4.caixa/fortify/fortify-ci-tools:7.0.0-jdk-17 \\\n  bash -c \"\n\n    echo Valida integridade do certificado DENTRO do container\n    echo md5sum /src/keystore.jks\n    md5sum /src/keystore.jks\n\n    echo Configurando Key Store\n    fcli config truststore set \\\n      --file=/src/keystore.jks \\\n      --password=$KEYSTORE_PWD \\\n      --type=jks\n\n    echo \\\"Nome do Sistema: \\$FORTIFY_APPLICATION\\\"\n\n    echo \\\"Nome da Versão: \\$FORTIFY_APP_VERSION\\\"\n\n    echo \\\"Nome da Versão Anterior: \\$FORTIFY_PREVIOUS_VERSION\\\"\n\n   #FORTIFY_CI_TOKEN proveniente do Fortify (expira)\n   #FORTIFY_CLIENT_AUTH_TOKEN (não expira)\n    echo Login no Fortify...\n    fcli ssc session login \\\n      --url=\\$FORTIFY_URL \\\n      --token=\\$FORTIFY_CI_TOKEN \\\n      --client-auth-token=\\$FORTIFY_CLIENT_AUTH_TOKEN \\\n      --socket-timeout=10m \\\n      --connect-timeout=5m \\\n      --ssc-session=\\$FORTIFY_SESSION\n\n    echo Criando aplicação no Fortify...\n    fcli ssc action run setup-appversion \\\n      --appversion=\\$FORTIFY_APPLICATION:\\$FORTIFY_APP_VERSION \\\n      --attributes=\\\"Comunidade=\\$FORTIFY_COMUNIDADE,Sigla=\\$FORTIFY_SIGLA\\\" \\\n      --add-users=\\$FORTIFY_LDAP_GROUP \\\n      --copy-from=\\$FORTIFY_APPLICATION:\\$FORTIFY_PREVIOUS_VERSION \\\n      --ssc-session=\\$FORTIFY_SESSION || true\n\n    fcli ssc action run setup-appversion \\\n      --appversion=\\$FORTIFY_APPLICATION:\\$FORTIFY_APP_VERSION \\\n      --attributes=\\\"Comunidade=\\$FORTIFY_COMUNIDADE,Sigla=\\$FORTIFY_SIGLA\\\" \\\n      --add-users=\\$FORTIFY_LDAP_GROUP \\\n      --ssc-session=\\$FORTIFY_SESSION || true\n \n    echo Atribuindo acessos ao Fortify...\n    fcli ssc appversion update \\\n      \\$FORTIFY_APPLICATION:\\$FORTIFY_APP_VERSION \\\n      --add-users=\\$FORTIFY_LDAP_GROUP \\\n      --ssc-session=\\$FORTIFY_SESSION || true\n\n    echo Pegando Rules\n    fcli ssc rest call \\\n      -X GET \\\n      -o json \\\n      --to-file rules.json \\\n      --ssc-session=\\\"\\$FORTIFY_SESSION\\\" \\\n      \\\"/api/v1/projectVersions/10000/resultProcessingRules\\\" || true\n\n    echo Pegando ID app\n    FRTF_ID_VERSION=\\$(\n     fcli ssc appversion get \\\n      --ssc-session=\\\"\\$FORTIFY_SESSION\\\" \\\n      -o expr=\\\"{id}\\\" \\\n      \\\"\\$FORTIFY_APPLICATION:\\$FORTIFY_APP_VERSION\\\"\n    ) || true\n\n    echo Atualizando Rules\n    fcli ssc rest call \\\n      -X PUT \\\n      -d '@@rules.json' \\\n      --ssc-session=\\\"\\$FORTIFY_SESSION\\\" \\\n      \\\"/api/v1/projectVersions/\\$FRTF_ID_VERSION/resultProcessingRules\\\" || true \n    echo \\\"FRTF_ID_VERSION: \\$FRTF_ID_VERSION\\\"\n\n    echo Logout do Fortify...\n    fcli ssc session logout \\\n      --ssc-session=\\$FORTIFY_SESSION \\\n      --no-revoke-token\n  \""
  - task: CmdLine@2
    displayName: '[MANTER] SAST: Disparando SAST no Fortify'
    enabled: False
    inputs:
      script: "echo Sistema: $FORTIFY_APPLICATION\necho Versão mais recente: $FORTIFY_NEW_VERSION\necho Versão anterior: $FORTIFY_LAST_VERSION\n\necho Empacotando aplicação...\n/opt/ads-agent/_work/_tool/scancentral/24.4.0/x64/bin/scancentral package --output package.zip\n\necho Disparando requisição de análise SAST...\n/opt/ads-agent/_work/_tool/scancentral/24.4.0/x64/bin/scancentral \\\n    -url $FORTIFY_URL_CONTROLLER \\\n    start --upload-to-ssc \\\n    -application $FORTIFY_APPLICATION \\\n    -version $FORTIFY_NEW_VERSION \\\n    --package package.zip \\\n    --ssc-upload-token $FORTIFY_CI_TOKEN "
  - task: CmdLine@2
    displayName: 'SAST: Confirmando Variáveis'
    condition: and(eq(variables['valida.vec'], 'true'), succeeded(), ne(variables['fortify_disable'], 'gecmi'))
    inputs:
      script: >-
        echo "Definindo liguagem de programação"

        cd $(Build.SourcesDirectory)

        for file in pom.xml angular.json tsconfig.json package.json project.ini *.csproj *.sln build.gradle

        do
            f_language=`find . -maxdepth 3 -name "${file}" -exec basename {} \; | head -n 1`
            if [[ "${f_language}" == pom.xml ]]; then
                echo MVN_GOAL: $FTFY_MVN_GOAL
                p_language=java
                break
            elif [[ "${f_language}" == angular.json ]] || [[ "${f_language}" == tsconfig.json ]]; then
                p_language=angular
                break
            elif [[ "${f_language}" == package.json ]]; then
                p_language=nodejs
                break
            elif [[ "${f_language}" == project.ini ]]; then
                p_language=php
                break
            elif [[ "${f_language}" == *".csproj" ]] || [[ "${f_language}" == *".sln" ]];then
                p_language=dotnet
                break
            elif [[ "${f_language}" == "build.gradle" ]]; then
                p_language=android
                break
            else
                p_language=null
            fi
        done


        echo "Linguagem de Programação:" $p_language

        echo "##vso[task.setvariable variable=p_language;]$p_language"


        if [ $p_language == null ]; then
            echo "##[warning]Não foi possivel definir a linguagem de programação deste codigo fonte"
        fi


        #######


        JAVA_HOME_17_X64=/usr/java/open-jdk-17.0.8

        echo "##[command]echo \$JAVA_HOME_17_X64"

        echo JAVA_HOME_17_X64: $JAVA_HOME_17_X64


        echo "##vso[task.setvariable variable=JAVA_HOME_17_X64;]$JAVA_HOME_17_X64"


        echo MAVEN_VERSION: $MAVEN_VERSION


        if [[ -n $MAVEN_VERSION ]]; then
            export PATH=/opt/apache-maven/apache-maven-$MAVEN_VERSION/bin:$PATH
            echo "##vso[task.setvariable variable=PATH;]$PATH"
        fi

        echo PATH: $PATH


        #######


        echo Build.Repository.Name=$(Build.Repository.Name)


        echo FORTIFY_APPLICATION=$FORTIFY_APPLICATION

        echo FORTIFY_SESSION=$FORTIFY_SESSION


        echo "##[command]echo NODE_EXTRA_CA_CERTS"

        echo $(NODE_EXTRA_CA_CERTS)

        echo "##[command]md5sum NODE_EXTRA_CA_CERTS"

        md5sum $(NODE_EXTRA_CA_CERTS)


        #verificar diretório contendo os certificados necessários para a próxima task

        #ls -lah /etc/pki/ca-trust/source/anchors/


        echo Build.DefinitionName=$(Build.DefinitionName)

        echo Build.BuildNumber=$(Build.BuildNumber)

        echo Build.BuildId=$(Build.BuildId)

        echo Build.SourceBranch=$(Build.SourceBranch)

        echo Build.SourceBranchName=$(Build.SourceBranchName)

        echo Build.SourceVersion=$(Build.SourceVersion)


        echo "##[command]echo \$valida.vec"

        echo vec=$(valida.vec)


        #######


        echo "Versão atual:"

        echo "##[command]git log --pretty=format:"%H %D" | sed -n '1p'"

        git -c safe.directory=* log --pretty=format:"%H %D" | sed -n '1p'

        echo "##[command]git describe --tags $(Build.SourceVersion)"

        git -c safe.directory=* describe --tags $(Build.SourceVersion)


        #######


        echo "Versões anteriores [tag] seguindo a branch atual:"


        FORTIFY_NEW_VERSION=`git -c safe.directory=* log --pretty=format:"%H %D" | grep -oP '(?<=tag: )[^\s]*([0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3})' | sed -n '1p'`

        FORTIFY_LAST_VERSION=`git -c safe.directory=* log --pretty=format:"%H %D" | grep -oP '(?<=tag: )[^\s]*([0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3})' | sed -n '2p'`

        FORTIFY_THIRD_VERSION=`git -c safe.directory=* log --pretty=format:"%H %D" | grep -oP '(?<=tag: )[^\s]*([0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3})' | sed -n '3p'`


        echo Última tag mais recente: $FORTIFY_NEW_VERSION

        echo Penúltima tag mais recente: $FORTIFY_LAST_VERSION

        echo Antepenúltima tag mais recente: $FORTIFY_THIRD_VERSION


        echo Validando VEC e versão...

        # A VEC dá false pois o valor $(Build.SourceBranchName) não passa o valor da tag quando o build é disparado a partir da branch.

        if [[ $(valida.vec) == false ]]; then

        echo "O nome de versão ' $(Build.SourceBranchName) ' NÃO ATENDE aos parâmetros da VEC."

        fi

        if [[ -n $FORTIFY_NEW_VERSION ]]; then
          FORTIFY_NEW_VERSION=`echo $FORTIFY_NEW_VERSION | grep -oP $(FORTIFY_REGEX)`
          FORTIFY_LAST_VERSION=`echo $FORTIFY_LAST_VERSION | grep -oP $(FORTIFY_REGEX)`
        else

        if [[ -n $FORTIFY_LAST_VERSION ]]; then
          FORTIFY_NEW_VERSION="develop"
        else
          FORTIFY_NEW_VERSION=`echo $FORTIFY_LAST_VERSION | grep -oP $(FORTIFY_REGEX)`
          FORTIFY_LAST_VERSION=`echo $FORTIFY_THIRD_VERSION | grep -oP $(FORTIFY_REGEX)`
        fi

        fi

        #

        #echo FORTIFY_NEW_VERSION=$FORTIFY_NEW_VERSION

        #echo FORTIFY_LAST_VERSION=$FORTIFY_LAST_VERSION

        echo "##[debug]Seu resultado será publicado no Fortify sob a Versão de nome: ' $FORTIFY_APPLICATION:$FORTIFY_NEW_VERSION '"


        echo "##vso[task.setvariable variable=FORTIFY_NEW_VERSION]$FORTIFY_NEW_VERSION"

        echo "##vso[task.setvariable variable=FORTIFY_LAST_VERSION]$FORTIFY_LAST_VERSION"


        ########


        echo "Agent Name: $AGENT_NAME"

        AGENT_SHORT_NAME=$(echo "$AGENT_NAME" | sed -E 's/^([a-zA-Z]+)[0-9]*\..*/\1/')


        echo "Nome curto do agente: $AGENT_SHORT_NAME"


        if [[ "$AGENT_SHORT_NAME" == "cadsvaprlx" ]]; then
            CONTAINER_ENGINE=docker
            echo "##vso[task.setvariable variable=CONTAINER_ENGINE]docker"
        else
            CONTAINER_ENGINE=podman
            echo "##vso[task.setvariable variable=CONTAINER_ENGINE]podman"
        fi


        echo "##[debug]Container engine selecionado: $CONTAINER_ENGINE"
  - task: CmdLine@2
    displayName: '[MANTER] SAST: Validando Passagem de Variáveis'
    enabled: False
    inputs:
      script: >-
        scancentral --version

        /opt/ads-agent/_work/_tool/scancentral/24.4.0/x64/bin/scancentral --version


        echo FORTIFY_SESSION: $FORTIFY_SESSION

        echo FORTIFY_APPLICATION: $FORTIFY_APPLICATION


        echo FORTIFY_NEW_VERSION: $FORTIFY_NEW_VERSION

        echo FORTIFY_LAST_VERSION: $FORTIFY_LAST_VERSION

        echo FORTIFY_APPLICATION-FORTIFY_NEW_VERSION

        echo $FORTIFY_APPLICATION-$FORTIFY_NEW_VERSION

        #echo FORTIFY_APPLICATION-[ dependencies.A.outputs['FORTIFY_NEW_VERSION'] ]

        #echo $FORTIFY_APPLICATION-$[ dependencies.A.outputs['FORTIFY_NEW_VERSION'] ]
  - task: CmdLine@2
    displayName: '[MANTER] SAST: Fortify ScanCentral SAST Assessment v1'
    enabled: False
    inputs:
      script: "echo Sistema: $FORTIFY_APPLICATION\necho Versão mais recente: $FORTIFY_NEW_VERSION\necho Versão anterior: $FORTIFY_LAST_VERSION\n\necho Empacotando aplicação...\n/opt/ads-agent/_work/_tool/scancentral/24.4.0/x64/bin/scancentral package --output package.zip\n\necho Disparando requisição de análise SAST...\n/opt/ads-agent/_work/_tool/scancentral/24.4.0/x64/bin/scancentral \\\n    -url $FORTIFY_URL_CONTROLLER \\\n    start --upload-to-ssc \\\n    -application $FORTIFY_APPLICATION \\\n    -version $FORTIFY_NEW_VERSION \\\n    --fpr-filename-on-ssc $(Build.BuildNumber)\n    --package package.zip \\\n    --ssc-upload-token $FORTIFY_CI_TOKEN "
  - task: FortifyScanCentralSAST@7
    displayName: 'SAST: Análise Java [Assíncrona]'
    condition: and(eq(variables['valida.vec'], 'true'), succeeded(), ne(variables['guardrail.sec'], 'true'), ne(variables['fortify_disable'], 'gecmi'), eq(variables['p_language'], 'java'))
    retryCountOnTaskFailure: 2
    inputs:
      scanCentralCtrlUrl: $(FORTIFY_URL_CONTROLLER)
      scanCentralClientToken: $(FORTIFY_CLIENT_AUTH_TOKEN)
      sscUrl: $(FORTIFY_URL)
      sscCiToken: $(FORTIFY_CI_TOKEN)
      uploadToSSC: true
      applicationName: $(Build.Repository.Name)
      applicationVersion: $(FORTIFY_NEW_VERSION)
      buildTool: mvn
      buildCommand: $(FTFY_MVN_GOAL)
      buildFile: pom.xml
      additionalTranslationArgs: >-
        -Dcom.fortify.sca.NullPtrMaxFunctionTime=30000

        -Dcom.fortify.sca.exclude.unimported.node.modules=true

        -Dcom.fortify.sca.EnableDOMModeling=true

        -Dcom.fortify.sca.fileextensions.inc=PHP

        -Dcom.fortify.sca.rules.password_regex.global=(?i)(s|_)?(user|usr|member|admin|guest|login|default|new|current|old|client|server|proxy|sqlserver|my|mysql|mongo|mongodb|db|database|ldap|smtp|email|email(_)?smtp)?(_|\.)?(pass(wd|word|phrase)|secret|senha)
      excludeArgs: >-
        ./**/node_modules/**/*

        ./**/*.min.js

        ./**/dist/**/*
      skipBuild: false
      excludeDisabledProjects: false
      includeTest: false
      includeNodeModules: false
      additionalScanArgs: >-
        -build-label $(FORTIFY_FPR_NAME)

        -build-version $(FORTIFY_FPR_NAME)-$(Build.BuildNumber)
      sensorPool: $(FORTIFY_SENSOR_POOL)
      overwrite: false
      quiet: false
      downloadDebugLogs: false
      debugLogFileName: $(Build.Repository.Name)-$(FORTIFY_FPR_NAME)-fortify-debug-logs.zip
  - task: FortifyScanCentralSAST@7
    displayName: 'SAST: Análise Default [Assíncrona]'
    condition: and(eq(variables['valida.vec'], 'true'), succeeded(), ne(variables['guardrail.sec'], 'true'), ne(variables['fortify_disable'], 'gecmi'), ne(variables['p_language'], 'java'))
    retryCountOnTaskFailure: 2
    inputs:
      scanCentralCtrlUrl: $(FORTIFY_URL_CONTROLLER)
      scanCentralClientToken: $(FORTIFY_CLIENT_AUTH_TOKEN)
      sscUrl: $(FORTIFY_URL)
      sscCiToken: $(FORTIFY_CI_TOKEN)
      uploadToSSC: true
      applicationName: $(Build.Repository.Name)
      applicationVersion: $(FORTIFY_NEW_VERSION)
      autoDetectBuildTool: true
      additionalTranslationArgs: >-
        -Dcom.fortify.sca.exclude.unimported.node.modules=true

        -Dcom.fortify.sca.EnableDOMModeling=true

        -Dcom.fortify.sca.fileextensions.inc=PHP

        -Dcom.fortify.sca.rules.password_regex.global=(?i)(s|_)?(user|usr|member|admin|guest|login|default|new|current|old|client|server|proxy|sqlserver|my|mysql|mongo|mongodb|db|database|ldap|smtp|email|email(_)?smtp)?(_|\.)?(pass(wd|word|phrase)|secret|senha)
      excludeArgs: >-
        ./**/node_modules/**/*

        ./**/*.min.js

        ./**/dist/**/*
      skipBuild: false
      excludeDisabledProjects: false
      includeTest: false
      includeNodeModules: false
      additionalScanArgs: >-
        -build-label $(FORTIFY_FPR_NAME)

        -build-version $(FORTIFY_FPR_NAME)-$(Build.BuildNumber)
      sensorPool: $(FORTIFY_SENSOR_POOL)
      overwrite: false
      quiet: false
      downloadDebugLogs: false
      debugLogFileName: $(Build.Repository.Name)-$(FORTIFY_FPR_NAME)-fortify-debug-logs.zip
  - task: FortifyScanCentralSAST@7
    displayName: 'SAST: Análise Java [Síncrona]'
    condition: and(eq(variables['valida.vec'], 'true'), succeeded(), eq(variables['guardrail.sec'], 'true'), ne(variables['fortify_disable'], 'gecmi'), eq(variables['p_language'], 'java'))
    retryCountOnTaskFailure: 2
    inputs:
      scanCentralCtrlUrl: $(FORTIFY_URL_CONTROLLER)
      scanCentralClientToken: $(FORTIFY_CLIENT_AUTH_TOKEN)
      sscUrl: $(FORTIFY_URL)
      sscCiToken: $(FORTIFY_CI_TOKEN)
      uploadToSSC: true
      applicationName: $(Build.Repository.Name)
      applicationVersion: $(FORTIFY_NEW_VERSION)
      buildTool: mvn
      buildCommand: $(FTFY_MVN_GOAL)
      buildFile: pom.xml
      additionalTranslationArgs: >-
        -Dcom.fortify.sca.NullPtrMaxFunctionTime=30000

        -Dcom.fortify.sca.exclude.unimported.node.modules=true

        -Dcom.fortify.sca.EnableDOMModeling=true

        -Dcom.fortify.sca.fileextensions.inc=PHP

        -Dcom.fortify.sca.rules.password_regex.global=(?i)(s|_)?(user|usr|member|admin|guest|login|default|new|current|old|client|server|proxy|sqlserver|my|mysql|mongo|mongodb|db|database|ldap|smtp|email|email(_)?smtp)?(_|\.)?(pass(wd|word|phrase)|secret|senha)
      excludeArgs: >-
        ./**/node_modules/**/*

        ./**/*.min.js

        ./**/dist/**/*
      skipBuild: false
      excludeDisabledProjects: false
      includeTest: false
      includeNodeModules: false
      additionalScanArgs: >-
        -build-label $(FORTIFY_FPR_NAME)

        -build-version $(FORTIFY_FPR_NAME)-$(Build.BuildNumber)
      sensorPool: $(FORTIFY_SENSOR_POOL)
      block: true
      logFile: $(Build.Repository.Name)-$(FORTIFY_NEW_VERSION)-$(Build.BuildNumber).log
      overwrite: true
      quiet: false
      downloadDebugLogs: false
      debugLogFileName: $(Build.Repository.Name)-$(FORTIFY_FPR_NAME)-fortify-debug-logs.zip
  - task: FortifyScanCentralSAST@7
    displayName: 'SAST: Análise Default [Síncrona]'
    condition: and(eq(variables['valida.vec'], 'true'), succeeded(), eq(variables['guardrail.sec'], 'true'), ne(variables['fortify_disable'], 'gecmi'), ne(variables['p_language'], 'java'))
    retryCountOnTaskFailure: 2
    inputs:
      scanCentralCtrlUrl: $(FORTIFY_URL_CONTROLLER)
      scanCentralClientToken: $(FORTIFY_CLIENT_AUTH_TOKEN)
      sscUrl: $(FORTIFY_URL)
      sscCiToken: $(FORTIFY_CI_TOKEN)
      uploadToSSC: true
      applicationName: $(Build.Repository.Name)
      applicationVersion: $(FORTIFY_NEW_VERSION)
      autoDetectBuildTool: true
      additionalTranslationArgs: >-
        -Dcom.fortify.sca.exclude.unimported.node.modules=true

        -Dcom.fortify.sca.EnableDOMModeling=true

        -Dcom.fortify.sca.fileextensions.inc=PHP

        -Dcom.fortify.sca.rules.password_regex.global=(?i)(s|_)?(user|usr|member|admin|guest|login|default|new|current|old|client|server|proxy|sqlserver|my|mysql|mongo|mongodb|db|database|ldap|smtp|email|email(_)?smtp)?(_|\.)?(pass(wd|word|phrase)|secret|senha)
      excludeArgs: >-
        ./**/node_modules/**/*

        ./**/*.min.js

        ./**/dist/**/*
      skipBuild: false
      excludeDisabledProjects: false
      includeTest: false
      includeNodeModules: false
      additionalScanArgs: >-
        -build-label $(FORTIFY_FPR_NAME)

        -build-version $(FORTIFY_FPR_NAME)-$(Build.BuildNumber)
      sensorPool: $(FORTIFY_SENSOR_POOL)
      block: true
      logFile: $(Build.Repository.Name)-$(FORTIFY_NEW_VERSION)-$(Build.BuildNumber).log
      overwrite: true
      quiet: false
      downloadDebugLogs: false
      debugLogFileName: $(Build.Repository.Name)-$(FORTIFY_FPR_NAME)-fortify-debug-logs.zip
  - task: CmdLine@2
    displayName: '[MANTER] SAST: Imprime Log da execução -- Futuro Guardrail'
    condition: and(eq(variables['valida.vec'], 'true'), succeeded())
    continueOnError: True
    enabled: False
    inputs:
      script: >-
        echo Imprimindo log da execução...


        echo "##[command]cat $(System.DefaultWorkingDirectory)/$(Build.Repository.Name)-$(FORTIFY_FPR_NAME)-$(Build.BuildNumber).log"


        cat $(System.DefaultWorkingDirectory)/$(Build.Repository.Name)-$(FORTIFY_FPR_NAME)-$(Build.BuildNumber).log
  - task: CmdLine@2
    displayName: 'SAST: Avalia Bypass do Guardrail'
    condition: and(eq(variables['valida.vec'], 'true'), succeeded(), eq(variables['guardrail.sec'], 'true'), ne(variables['fortify_disable'], 'gecmi'))
    inputs:
      script: >-
        #!/usr/bin/env bash

        set -euo pipefail


        REF="${BUILD_SOURCEBRANCH:-}"

        COMMIT="${BUILD_SOURCEVERSION:-}"


        HOTFIX_REF_PREFIX='refs/remotes/origin/hotfix/'

        HOTFIX_BRANCH_REGEX='^origin/hotfix/INC[0-9]+$'

        MAX_DISTANCE=0


        echo "================================================="

        echo "##[section]VALIDAÇÃO DO BYPASS GUARDRAIL DE SEGURANÇA:"

        echo "Esta task verifica se a versão candidata pertence a um fluxo de correção emergencial autorizado."

        echo "- O bypass do guardrail somente será autorizado quando:"

        echo "- A pipeline for disparada por uma tag;"

        echo "- O commit da tag estiver em uma branch hotfix válida;"

        echo "- A branch seguir o padrão hotfix/INC<numero>;"

        echo ""

        echo "##[section]IMPORTANTE:"

        echo "- O bypass se aplica somente ao guardrail de segurança;"

        echo "- O fluxo de exceção deve estar vinculado a um incidente;"

        echo "- A utilização deste fluxo é monitorada."

        echo ""

        echo "##[section]Documentação:"

        echo "##[command]https://caixa.sharepoint.com/sites/PPDS/SitePages/Guardrail-de-Seguran%C3%A7a.aspx"

        echo "================================================="

        echo "BUILD_SOURCEBRANCH=${BUILD_SOURCEBRANCH:-N/A}"

        echo "BUILD_SOURCEBRANCHNAME=${BUILD_SOURCEBRANCHNAME:-N/A}"

        echo "BUILD_REASON=${BUILD_REASON:-N/A}"

        echo "BUILD_SOURCEVERSION=${BUILD_SOURCEVERSION:-N/A}"

        echo "MAX_DISTANCE=${MAX_DISTANCE}"

        echo "================================================="


        skip_guardrail=false

        is_hotfix=false


        if [[ "$REF" =~ ^refs/tags/ ]]; then

            TAG="${REF#refs/tags/}"

            echo "[guardrail-bypass] Build disparada por TAG."
            echo "[guardrail-bypass] Tag: ${TAG}"
            echo "[guardrail-bypass] Commit: ${COMMIT:-N/A}"

            if [[ -n "$COMMIT" ]]; then

                # Cada linha: <nome curto> <ref completa> <hash do HEAD da branch>
                HOTFIX_BRANCHES="$(git -c color.ui=never for-each-ref \
                    --contains "$COMMIT" \
                    --format='%(refname:short) %(refname) %(objectname)' \
                    "$HOTFIX_REF_PREFIX" 2>/dev/null | tr -d '\r' || true)"

                echo "-------------------------------------------------"
                echo "DEBUG - Branches hotfix remotas contendo o commit"
                echo "${HOTFIX_BRANCHES:-<nenhuma>}"

                while read -r branch full_ref branch_head; do

                    [[ -z "${branch:-}" ]] && continue

                    if ! [[ "$branch" =~ $HOTFIX_BRANCH_REGEX ]]; then
                        echo "[guardrail-bypass] Ignorada (fora do padrão INC): $branch"
                        continue
                    fi

                    echo "-------------------------------------------------"
                    echo "[guardrail-bypass] Hotfix candidata: $branch"
                    echo "[guardrail-bypass] HEAD da hotfix: ${branch_head}"

                    if [[ "$branch_head" == "$COMMIT" ]]; then
                        # Commit da tag É o HEAD: distância 0, sem percorrer histórico
                        DISTANCE=0
                    else
                        # Ref completa + "--" evita ambiguidade com tags/arquivos;
                        # stderr é capturado para aparecer no log em caso de falha
                        if ! DISTANCE=`git rev-list --count "${COMMIT}..${full_ref}" -- 2>&1`; then
                            echo "[guardrail-bypass] Falha no git rev-list: ${DISTANCE}"
                            continue
                        fi
                    fi

                    if ! [[ "$DISTANCE" =~ ^[0-9]+$ ]]; then
                        echo "[guardrail-bypass] Distância inválida: $DISTANCE . Ignorando."
                        continue
                    fi

                    echo "[guardrail-bypass] Distância até HEAD da hotfix: ${DISTANCE}"

                    if (( DISTANCE <= MAX_DISTANCE )); then
                        echo "[guardrail-bypass] Commit considerado RECENTE."
                        echo "[guardrail-bypass] Bypass autorizado."
                        skip_guardrail=true
                        is_hotfix=true
                        break
                    else
                        echo "[guardrail-bypass] Commit muito antigo para bypass."
                    fi

                done <<< "$HOTFIX_BRANCHES"

            else
                echo "[guardrail-bypass] BUILD_SOURCEVERSION vazio."
                echo "[guardrail-bypass] Mantendo guardrail."
            fi

        else
            echo "[guardrail-bypass] Build não foi disparada por TAG."
            echo "[guardrail-bypass] Mantendo guardrail."
        fi


        echo "##vso[task.setvariable variable=isHotfix]$is_hotfix"


        echo "[guardrail-bypass] RESULTADO FINAL"

        echo "[guardrail-bypass] isHotfix=${is_hotfix}"


        if [[ "$skip_guardrail" == "true" ]]; then
            echo "##vso[task.setvariable variable=guardrail.sec]false"
            echo "[guardrail-bypass] guardrail.sec=false"
        else
            echo "[guardrail-bypass] guardrail.sec preservado"
        fi
  - task: CmdLine@2
    displayName: 'SAST: Guardrail Segurança Cibernética'
    condition: and(eq(variables['valida.vec'], 'true'), succeeded(), eq(variables['guardrail.sec'], 'true'), ne(variables['fortify_disable'], 'gecmi'))
    inputs:
      script: "command -v docker && docker --version\ncommand -v podman && podman --version\n\necho \"$FORTIFY_REGISTRY_PASSWORD\" | $CONTAINER_ENGINE login default-route-openshift-image-registry.apps.produtos4.caixa \\\n  --username \"$FORTIFY_REGISTRY_USERNAME\" \\\n  --password-stdin\n \necho FORTIFY_APPLICATION: $FORTIFY_APPLICATION\n\necho KEYSTORE_SECUREFILEPATH: $KEYSTORE_SECUREFILEPATH\ncp \"$KEYSTORE_SECUREFILEPATH\" \"$(System.DefaultWorkingDirectory)/keystore.jks\"\n\necho \"##[command]$CONTAINER_ENGINE --version\"\n$CONTAINER_ENGINE --version\n\necho \"##[command]Executando container Fortify...\"\n\n$CONTAINER_ENGINE run --rm \\\n  --security-opt seccomp=unconfined \\\n  --memory=12g \\\n  --memory-swap=12g \\\n  -v $(System.DefaultWorkingDirectory):/src \\\n  -w /src \\\n  -e FORTIFY_APPLICATION \\\n  -e FORTIFY_APP_VERSION=$FORTIFY_NEW_VERSION \\\n  -e FORTIFY_PREVIOUS_VERSION=$FORTIFY_LAST_VERSION \\\n  -e FORTIFY_SESSION \\\n  -e FORTIFY_URL \\\n  -e FORTIFY_CI_TOKEN \\\n  -e FORTIFY_CLIENT_AUTH_TOKEN \\\n  -e FORTIFY_FILTERSET_GUARDRAIL \\\n  -e FORTIFY_SENSOR_VERSION \\\n  -e FORTIFY_SIGLA=$(Build.DefinitionName) \\\n  -e FORTIFY_COMUNIDADE \\\n  -e FORTIFY_LDAP_GROUP \\\n  default-route-openshift-image-registry.apps.produtos4.caixa/fortify/fortify-ci-tools:7.0.0-jdk-17 \\\n  bash -c \"\n    \n    echo Configurando Key Store\n    fcli config truststore set \\\n      --file=/src/keystore.jks \\\n      --password=$KEYSTORE_PWD \\\n      --type=jks\n    \n    echo \\\"Nome do Sistema: \\$FORTIFY_APPLICATION\\\"\n    echo \\\"Nome da Versão: \\$FORTIFY_APP_VERSION\\\"\n    echo \\\"Nome da Versão Anterior: \\$FORTIFY_PREVIOUS_VERSION\\\"\n    \n    echo Login no Fortify...\n    fcli ssc session login \\\n      --ssc-session=\\$FORTIFY_SESSION \\\n      --url=\\$FORTIFY_URL \\\n      --token=\\$FORTIFY_CI_TOKEN \\\n      --client-auth-token=\\$FORTIFY_CLIENT_AUTH_TOKEN \\\n      --socket-timeout=180\n    \n    echo Atualizando aplicação no Fortify...\n    fcli ssc appversion refresh-metrics \\\n      \\$FORTIFY_APPLICATION:\\$FORTIFY_APP_VERSION \\\n      --ssc-session=\\$FORTIFY_SESSION || true\n\n    echo ===== BUSCANDO VULNERABILIDADES CRÍTICAS =====\n    rc=1\n    for tentativa in 1 2 3; do\n    echo \\\"Tentativa \\$tentativa de 3...\\\"\n     timeout -k 30s 2m fcli ssc issue list \\\n        --appversion=\\\"\\$FORTIFY_APPLICATION:\\$FORTIFY_APP_VERSION\\\" \\\n        --filterset=\\\"\\$FORTIFY_FILTERSET_GUARDRAIL\\\" \\\n        --filter='Folder:Critical' \\\n        --output=csv \\\n        --to-file=guardrail-raw.csv \\\n        --ssc-session=\\\"\\$FORTIFY_SESSION\\\" \\\n        --log-level=INFO --log-file=/src/fcli-issue-list.log\n      rc=\\$?\n      [ \\$rc -eq 0 ] && break\n      echo \\\"Tentativa \\$tentativa falhou (rc=\\$rc; 124 = timeout). Aguardando...\\\"\n      sleep 20\n  done\n  if [ \\$rc -ne 0 ]; then \n    echo \\\"ERRO: Falha ao consultar vulnerabilidades no SSC após 3 tentativas.\\\"\n    exit 1\n  fi\n\n    echo\n    echo ===== FILTRANDO ITENS INVÁLIDOS =====\n    \n    grep -v 'Not an Issue' guardrail-raw.csv > guardrail-results.csv || true\n\n    echo Resultado final:\n    cat guardrail-results.csv\n\n    echo\n    echo Logout do Fortify...\n    fcli ssc session logout \\\n      --ssc-session=\\$FORTIFY_SESSION \\\n      --no-revoke-token\n  \" || {\n    echo \"##vso[task.logissue type=error]Falha ao consultar Fortify. Build bloqueado.\"\n    exit 1\n       }\n\necho\necho \"##[debug]Resultado do Guardrail...\"\n\nguardrail_count=$(awk -F',' '\nNR > 1 {\n  for(i=1;i<=NF;i++){\n    if ($i == \"Critical\") {\n      count++\n      break\n    }\n  }\n}\nEND { print count+0 }\n' guardrail-results.csv)\n\nguardrail_count=${guardrail_count:-0}\n\necho \"##[debug]Total de vulnerabilidades críticas válidas: $guardrail_count\"\n\nif [ \"$guardrail_count\" -gt 0 ]; then\n  echo \"##vso[task.logissue type=error]Foram encontradas $guardrail_count vulnerabilidades críticas que violam os padrões de segurança exigidos.\"\n  exit 1\nelse\n  echo \"##[debug]Não foram encontradas vulnerabilidades críticas válidas.\"\nfi\n\necho \"##[debug]Resultado publicado no Fortify: '$FORTIFY_APPLICATION:$FORTIFY_NEW_VERSION'\""
  - task: CmdLine@2
    displayName: 'SAST: Guardrail Segurança Cibernética - Backup'
    condition: and(eq(variables['valida.vec'], 'true'), succeeded(), eq(variables['guardrail.sec'], 'true'), ne(variables['fortify_disable'], 'gecmi'))
    enabled: False
    inputs:
      script: "command -v docker && docker --version\ncommand -v podman && podman --version\n\n#sudo usermod -aG docker $USER\n\n#ls -l /var/run/docker.sock\n\n#set -o errexit\n#set -o pipefail\n#echo Engine selecionado: $CONTAINER_ENGINE\n#echo Versão mais recente: $FORTIFY_NEW_VERSION\n#echo Versão anterior: $FORTIFY_LAST_VERSION\n\necho \"$FORTIFY_REGISTRY_PASSWORD\" | $CONTAINER_ENGINE login default-route-openshift-image-registry.apps.produtos4.caixa --username \"$FORTIFY_REGISTRY_USERNAME\" --password-stdin\n \necho FORTIFY_APPLICATION: $FORTIFY_APPLICATION\necho KEYSTORE_SECUREFILEPATH: $(KEYSTORE_SECUREFILEPATH)\nKEYSTORE_SECUREFILEPATH=$(KEYSTORE_SECUREFILEPATH)\ncp $KEYSTORE_SECUREFILEPATH $(System.DefaultWorkingDirectory)/keystore.jks\n#echo \"##vso[task.setvariable variable=KEYSTORE_SECUREFILEPATH]$KEYSTORE_SECUREFILEPATH\"\n\n# Valida Integridade do JKS (parte 1, fora do container)\n#echo Valida integridade do certificado FORA do container\n#echo \"##[command]md5sum /etc/pki/ca-trust/source/anchors/keystore-ssc24.jks\"\n#md5sum /etc/pki/ca-trust/source/anchors/keystore-ssc24.jks\n#echo \"##[command]md5sum $KEYSTORE_SECUREFILEPATH\"\n#md5sum $KEYSTORE_SECUREFILEPATH\n#echo \"##[command]md5sum $(System.DefaultWorkingDirectory)/keystore.jks\"\n#md5sum $(System.DefaultWorkingDirectory)/keystore.jks\n\n# Executa o container Fortify com as variáveis herdadas do ambiente\necho \"##[command]$CONTAINER_ENGINE --version\"\n$CONTAINER_ENGINE --version\necho \"##[command]$CONTAINER_ENGINE run -v $(System.DefaultWorkingDirectory):/src default-route-openshift-image-registry.apps.produtos4.caixa/fortify/fortify-ci-tools:7.0.0-jdk-17\"\n$CONTAINER_ENGINE run --rm \\\n  --security-opt seccomp=unconfined \\\n  --memory=12g \\\n  --memory-swap=12g \\\n  -v $(System.DefaultWorkingDirectory):/src \\\n  -w /src \\\n  -e FORTIFY_APPLICATION \\\n  -e FORTIFY_APP_VERSION=$FORTIFY_NEW_VERSION \\\n  -e FORTIFY_PREVIOUS_VERSION=$FORTIFY_LAST_VERSION \\\n  -e FORTIFY_SESSION \\\n  -e FORTIFY_URL \\\n  -e FORTIFY_CI_TOKEN \\\n  -e FORTIFY_CLIENT_AUTH_TOKEN \\\n  -e FORTIFY_FILTERSET_GUARDRAIL \\\n  -e FORTIFY_SENSOR_VERSION \\\n  -e FORTIFY_SIGLA=$(Build.DefinitionName) \\\n  -e FORTIFY_COMUNIDADE \\\n  -e FORTIFY_LDAP_GROUP \\\n  default-route-openshift-image-registry.apps.produtos4.caixa/fortify/fortify-ci-tools:7.0.0-jdk-17 \\\n  bash -c \"\n    \n    #echo Valida integridade do certificado DENTRO do container\n    #echo md5sum /src/keystore.jks\n    #md5sum /src/keystore.jks\n    \n    echo Configurando Key Store\n    fcli config truststore set \\\n      --file=/src/keystore.jks \\\n      --password=$KEYSTORE_PWD \\\n      --type=jks\n    \n    echo \\\"Nome do Sistema: \\$FORTIFY_APPLICATION\\\"\n    \n    echo \\\"Nome da Versão: \\$FORTIFY_APP_VERSION\\\"\n    \n    echo \\\"Nome da Versão Anterior: \\$FORTIFY_PREVIOUS_VERSION\\\"\n    \n    echo Login no Fortify...\n    fcli ssc session login \\\n      --ssc-session=\\$FORTIFY_SESSION \\\n      --url=\\$FORTIFY_URL \\\n      --token=\\$FORTIFY_CI_TOKEN \\\n      --client-auth-token=\\$FORTIFY_CLIENT_AUTH_TOKEN \\\n    \n    \n    echo Atualizando aplicação no Fortify...\n    fcli ssc appversion refresh-metrics \\\n      \\$FORTIFY_APPLICATION:\\$FORTIFY_APP_VERSION \\\n      --ssc-session=\\$FORTIFY_SESSION || true\n    \n    echo Consultando número de vulnerabilidades da aplicação...\n    fcli ssc issue count \\\n      --appversion=\\$FORTIFY_APPLICATION:\\$FORTIFY_APP_VERSION \\\n      --by=FOLDER \\\n      --filterset=\\$FORTIFY_FILTERSET_GUARDRAIL \\\n      --filter='Folder:Critical' \\\n      --output=csv \\\n      --to-file=guardrail-results.csv \\\n      --ssc-session=\\$FORTIFY_SESSION || true\n    \n    cat guardrail-results.csv\n    \n    echo\n    echo Logout do Fortify...\n    fcli ssc session logout \\\n      --ssc-session=\\$FORTIFY_SESSION \\\n      --no-revoke-token\n  \"\n\necho \"##[debug]Resultado do Guardrail...\"\nguardrail_results=false\nwhile IFS=',' read -r id cleanName name totalCount auditedCount visibleCount; do\n  if [ \"$cleanName\" == \"Critical\" ] && [ \"$totalCount\" -gt 0 ]; then\n    guardrail_results=true\n    guardrail_count=$totalCount\n  fi\ndone < guardrail-results.csv\nif [ $guardrail_results == \"true\" ]; then\n  echo \"##vso[task.logissue type=error]Foram encontradas $guardrail_count vulnerabilidades que violam os padrões de segurança exigidos.\"\n  exit 1\nelse\n  echo \"##[debug]Não foram encontradas vulnerabilidades que violam os padrões de segurança exigidos.\"\nfi\necho \"##[debug]Seu resultado está publicado no Fortify sob a Versão de nome: ' $FORTIFY_APPLICATION:$FORTIFY_NEW_VERSION '\""
  - task: Bash@3
    displayName: md5
    inputs:
      targetType: inline
      script: >
        pwd

        ls $(project.file)

        HASH=`md5sum -b $(project.file)`

        SHA=`sha1sum -b $(project.file)`

        echo "MD5-BUILD: $HASH"

        echo "SHA1-BUILD: $SHA"
  - task: Bash@3
    displayName: Publica no Nexus
    inputs:
      targetType: inline
      script: >-
        cd $(Build.SourcesDirectory)


        p_group=$(project.group) || true

        p_name=$(project.name)

        p_version=$(project.version)

        p_extension=$(project.extension)


        p_group=`[ -z "$p_group" ] && echo ""br.gov.caixa.$p_name"" || echo "$p_group"`


        echo VEC $(valida.vec)

        if [ $(valida.vec) = true ];then

        p_version=$BUILD_SOURCEBRANCHNAME

        NEXUS_URL=$(NEXUS_URL_MAVEN_RELEASE)

        else

        p_version=${p_version^^}

        p_version=${p_version/-SNAPSHOT/}-SNAPSHOT

        #definido por GECPA em Nov/2025 que todo artefato não release candidate deve conter sufixo -SNAPSHOT

        echo "##vso[build.updatebuildnumber]"$p_version""

        NEXUS_URL=$(NEXUS_URL_MAVEN_SNAPSHOT)

        fi


        echo "##[section]=== Info do pacote ==="

        echo "##[section]groupid= $p_group"

        echo "##[section]artifact= $p_name"

        echo "##[section]version= $p_version"

        echo "========================================================="


        LIB="$(library)"

        # quando for uma pipeline do tipo lib o pom original do projeto precisa subir junto

        if [ "${LIB:-}" = "true" ] || [ "${LIB:-}" = "TRUE" ]; then


        echo -Dversion.app=$(Build.BuildNumber) -Dnexus_interno_user=$(nexus_interno_user) -Dnexus_interno_pass=$(nexus_interno_pass) -DgroupId="${p_group}" -DartifactId="${p_name}" -Dversion="${p_version}" -Dpackaging="${p_extension}" -Dfile="$(project.file)" -DpomFile="$(Build.SourcesDirectory)/pom.xml" -DrepositoryId=$(NEXUS_REPOSITORY_ID) -DgeneratePom=false -Durl=${NEXUS_URL} -Drevision="${p_version}"


        /opt/apache-maven/apache-maven-3.8.5/bin/mvn deploy:deploy-file -Dversion.app=$(Build.BuildNumber) -Dnexus_interno_user=$(nexus_interno_user) -Dnexus_interno_pass=$(nexus_interno_pass) -DgroupId="${p_group}" -DartifactId="${p_name}" -Dversion="${p_version}" -Dpackaging="${p_extension}" -Dfile="$(project.file)" -DpomFile="$(Build.SourcesDirectory)/pom.xml" -DrepositoryId=$(NEXUS_REPOSITORY_ID) -DgeneratePom=false -Durl=${NEXUS_URL} -Drevision="${p_version}"


        else


        echo -Dversion.app=$(Build.BuildNumber) -DgroupId="${p_group}" -DartifactId="${p_name}" -Dversion="${p_version}" -Dpackaging="${p_extension}" -Dfile="$(project.file)" -DrepositoryId=$(NEXUS_REPOSITORY_ID) -DgeneratePom=true -Durl=${NEXUS_URL}


        /opt/apache-maven/apache-maven-3.8.5/bin/mvn deploy:deploy-file -Dversion.app=$(Build.BuildNumber) -Dnexus_interno_user=$(nexus_interno_user) -Dnexus_interno_pass=$(nexus_interno_pass) -DgroupId="${p_group}" -DartifactId="${p_name}" -Dversion="${p_version}" -Dpackaging="${p_extension}" -Dfile="$(project.file)" -DrepositoryId=$(NEXUS_REPOSITORY_ID) -DgeneratePom=true -Durl=${NEXUS_URL} -Drevision="${p_version}"


        fi


        echo "##vso[task.setvariable variable=project.uploaded;]true"
  - task: Bash@3
    displayName: Publica no Nexus old
    enabled: False
    inputs:
      targetType: inline
      script: >-
        cd $(Build.SourcesDirectory)


        p_group=$(project.group) || true

        p_name=$(project.name)

        p_version=$(project.version)

        p_extension=$(project.extension)


        p_group=`[ -z "$p_group" ] && echo ""br.gov.caixa.$p_name"" || echo "$p_group"`



        if [ $(project.release) = true ]; then

        NEXUS_URL=$(NEXUS_URL_MAVEN_RELEASE)

        else

        NEXUS_URL=$(NEXUS_URL_MAVEN_SNAPSHOT)

        p_version=${p_version/-SNAPSHOT/}-SNAPSHOT

        fi


        echo $(valida.vec)

        if [ $(valida.vec) = true ];then

        p_version=$BUILD_SOURCEBRANCHNAME

        NEXUS_URL=$(NEXUS_URL_MAVEN_RELEASE)

        fi


        echo "##[section]info: -Dversion.app=$(Build.BuildNumber) -DgroupId="${p_group}" -DartifactId="${p_name}" -Dversion="${p_version}" -Dpackaging="${p_extension}" -Dfile="$(project.file)" -DrepositoryId=$(NEXUS_REPOSITORY_ID) -DgeneratePom=true -Durl=${NEXUS_URL}"


        /opt/apache-maven/apache-maven-3.8.5/bin/mvn deploy:deploy-file -Dversion.app=$(Build.BuildNumber) -Dnexus_interno_user=$(nexus_interno_user) -Dnexus_interno_pass=$(nexus_interno_pass) -DgroupId="${p_group}" -DartifactId="${p_name}" -Dversion="${p_version}" -Dpackaging="${p_extension}" -Dfile="$(project.file)" -DrepositoryId=$(NEXUS_REPOSITORY_ID) -DgeneratePom=true -Durl=${NEXUS_URL} -Drevision="${p_version}"



        echo "##vso[task.setvariable variable=project.uploaded;]true"
      failOnStderr: true
  - task: Bash@3
    displayName: Bash Script
    enabled: False
    inputs:
      targetType: inline
      script: exit 1
  - task: DeleteFiles@1
    displayName: Delete files from $(Agent.BuildDirectory)/fortify
    condition: always()
    inputs:
      SourceFolder: $(Agent.BuildDirectory)/fortify
      Contents: '*'
      RemoveSourceFolder: true
  - task: PublishTestResults@2
    displayName: Publica o resultado do teste
...

