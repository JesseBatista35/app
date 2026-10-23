Publish Quality Gate Result

View raw log

Starting: Publish Quality Gate Result
==============================================================================
Task         : Bash
Description  : Run a Bash script on macOS, Linux, or Windows
Version      : 3.227.0
Author       : Microsoft Corporation
Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
==============================================================================
Generating script.
========================== Starting Command Output ===========================
/usr/bin/bash /opt/ads-agent/_work/_temp/f3a954a9-3be4-4448-9991-731a410533eb.sh
QG Script --> Using SonarQube instance http://sonar-esteira.apps.produtos4.caixa
QG Script --> Using SonarQube access login ads-sa
QG Script --> Using task id of AaFpmUikPmqzl3Vc6nJS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is SUCCESS
QG Script --> Using analysis id of AaFpmVZHFkwt0Lh6sS0x
QG Script --> Quality Gate status is ERROR
##[error]QG Script --> Ocorrência prevista na TE102 - Não atendimento aos critérios de qualidade
##[error]Bash exited with code '1'.
Finishing: Publish Quality Gate Result


2026-10-23 12:35:03,208 INFO  [javax.enterprise.resource.webcontainer.jsf.application] (ServerService Thread Pool -- 80) JSF1048: PostConstruct/PreDestroy annotations present.  ManagedBeans methods marked with these annotations will have said annotations processed.
2026-10-23 12:35:03,432 ERROR [stderr] (ServerService Thread Pool -- 80) log4j:ERROR Could not parse file [/log_jboss/config-log4j/sigsj_intranet.xml].
2026-10-23 12:35:03,433 ERROR [stderr] (ServerService Thread Pool -- 80) java.io.FileNotFoundException: /log_jboss/config-log4j/sigsj_intranet.xml (Arquivo ou diretório inexistente)
2026-10-23 12:35:03,433 ERROR [stderr] (ServerService Thread Pool -- 80)        at java.io.FileInputStream.open0(Native Method)
2026-10-23 12:35:03,433 ERROR [stderr] (ServerService Thread Pool -- 80)        at java.io.FileInputStream.open(FileInputStream.java:195)
2026-10-23 12:35:03,433 ERROR [stderr] (ServerService Thread Pool -- 80)        at java.io.FileInputStream.<init>(FileInputStream.java:138)
2026-10-23 12:35:03,433 ERROR [stderr] (ServerService Thread Pool -- 80)        at java.io.FileInputStream.<init>(FileInputStream.java:93)
2026-10-23 12:35:03,434 ERROR [stderr] (ServerService Thread Pool -- 80)        at sun.net.www.protocol.file.FileURLConnection.connect(FileURLConnection.java:90)
2026-10-23 12:35:03,434 ERROR [stderr] (ServerService Thread Pool -- 80)        at sun.net.www.protocol.file.FileURLConnection.getInputStream(FileURLConnection.java:188)
2026-10-23 12:35:03,434 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.apache.xerces.impl.XMLEntityManager.setupCurrentEntity(Unknown Source)
2026-10-23 12:35:03,434 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.apache.xerces.impl.XMLVersionDetector.determineDocVersion(Unknown Source)
2026-10-23 12:35:03,434 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.apache.xerces.parsers.XML11Configuration.parse(Unknown Source)
2026-10-23 12:35:03,434 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.apache.xerces.parsers.XML11Configuration.parse(Unknown Source)
2026-10-23 12:35:03,434 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.apache.xerces.parsers.XMLParser.parse(Unknown Source)
2026-10-23 12:35:03,434 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.apache.xerces.parsers.DOMParser.parse(Unknown Source)
2026-10-23 12:35:03,434 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.apache.xerces.jaxp.DocumentBuilderImpl.parse(Unknown Source)
2026-10-23 12:35:03,434 ERROR [stderr] (ServerService Thread Pool -- 80)        at javax.xml.parsers.DocumentBuilder.parse(DocumentBuilder.java:205)
2026-10-23 12:35:03,434 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.apache.log4j.xml.DOMConfigurator$1.parse(DOMConfigurator.java:730)
2026-10-23 12:35:03,434 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.apache.log4j.xml.DOMConfigurator.doConfigure(DOMConfigurator.java:854)
2026-10-23 12:35:03,434 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.apache.log4j.xml.DOMConfigurator.doConfigure(DOMConfigurator.java:737)
2026-10-23 12:35:03,434 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.apache.log4j.xml.DOMConfigurator.configure(DOMConfigurator.java:879)
2026-10-23 12:35:03,434 ERROR [stderr] (ServerService Thread Pool -- 80)        at br.gov.caixa.sigsj.intranet.servlet.CaixaConfigServlet.init(CaixaConfigServlet.java:32)
2026-10-23 12:35:03,438 ERROR [stderr] (ServerService Thread Pool -- 80)        at io.undertow.servlet.core.LifecyleInterceptorInvocation.proceed(LifecyleInterceptorInvocation.java:117)
2026-10-23 12:35:03,439 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.wildfly.elytron.web.undertow.server.servlet.RunAsLifecycleInterceptor.doIt(RunAsLifecycleInterceptor.java:70)
2026-10-23 12:35:03,439 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.wildfly.elytron.web.undertow.server.servlet.RunAsLifecycleInterceptor.init(RunAsLifecycleInterceptor.java:76)
2026-10-23 12:35:03,439 ERROR [stderr] (ServerService Thread Pool -- 80)        at io.undertow.servlet.core.LifecyleInterceptorInvocation.proceed(LifecyleInterceptorInvocation.java:103)
2026-10-23 12:35:03,439 ERROR [stderr] (ServerService Thread Pool -- 80)        at io.undertow.servlet.core.ManagedServlet$DefaultInstanceStrategy.start(ManagedServlet.java:309)
2026-10-23 12:35:03,439 ERROR [stderr] (ServerService Thread Pool -- 80)        at io.undertow.servlet.core.ManagedServlet.createServlet(ManagedServlet.java:145)
2026-10-23 12:35:03,439 ERROR [stderr] (ServerService Thread Pool -- 80)        at io.undertow.servlet.core.DeploymentManagerImpl$2.call(DeploymentManagerImpl.java:589)
2026-10-23 12:35:03,439 ERROR [stderr] (ServerService Thread Pool -- 80)        at io.undertow.servlet.core.DeploymentManagerImpl$2.call(DeploymentManagerImpl.java:559)
2026-10-23 12:35:03,440 ERROR [stderr] (ServerService Thread Pool -- 80)        at io.undertow.servlet.core.ServletRequestContextThreadSetupAction$1.call(ServletRequestContextThreadSetupAction.java:42)
2026-10-23 12:35:03,440 ERROR [stderr] (ServerService Thread Pool -- 80)        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
2026-10-23 12:35:03,440 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.wildfly.extension.undertow.deployment.UndertowDeploymentInfoService$UndertowThreadSetupAction.lambda$create$0(UndertowDeploymentInfoService.java:1555)
2026-10-23 12:35:03,440 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.wildfly.extension.undertow.deployment.UndertowDeploymentInfoService$UndertowThreadSetupAction.lambda$create$0(UndertowDeploymentInfoService.java:1555)
2026-10-23 12:35:03,441 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.wildfly.extension.undertow.deployment.UndertowDeploymentInfoService$UndertowThreadSetupAction.lambda$create$0(UndertowDeploymentInfoService.java:1555)
2026-10-23 12:35:03,441 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.wildfly.extension.undertow.deployment.UndertowDeploymentInfoService$UndertowThreadSetupAction.lambda$create$0(UndertowDeploymentInfoService.java:1555)
2026-10-23 12:35:03,441 ERROR [stderr] (ServerService Thread Pool -- 80)        at io.undertow.servlet.core.DeploymentManagerImpl.start(DeploymentManagerImpl.java:605)
2026-10-23 12:35:03,441 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.wildfly.extension.undertow.deployment.UndertowDeploymentService.startContext(UndertowDeploymentService.java:97)
2026-10-23 12:35:03,441 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.wildfly.extension.undertow.deployment.UndertowDeploymentService$1.run(UndertowDeploymentService.java:78)
2026-10-23 12:35:03,441 ERROR [stderr] (ServerService Thread Pool -- 80)        at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
2026-10-23 12:35:03,441 ERROR [stderr] (ServerService Thread Pool -- 80)        at java.util.concurrent.FutureTask.run(FutureTask.java:266)
2026-10-23 12:35:03,441 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.jboss.threads.ContextClassLoaderSavingRunnable.run(ContextClassLoaderSavingRunnable.java:35)
2026-10-23 12:35:03,441 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.jboss.threads.EnhancedQueueExecutor.safeRun(EnhancedQueueExecutor.java:1990)
2026-10-23 12:35:03,441 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.doRunTask(EnhancedQueueExecutor.java:1486)
2026-10-23 12:35:03,441 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.run(EnhancedQueueExecutor.java:1377)
2026-10-23 12:35:03,442 ERROR [stderr] (ServerService Thread Pool -- 80)        at java.lang.Thread.run(Thread.java:750)
2026-10-23 12:35:03,442 ERROR [stderr] (ServerService Thread Pool -- 80)        at org.jboss.threads.JBossThread.run(JBossThread.java:513)
2026-10-23 12:35:03,480 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 80) WFLYUT0021: Contexto web registrado: '/sigsj_intranet' para servidor 'default-server'
2026-10-23 12:35:03,580 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 43) WFLYSRV0010: "sirotcon-ejb.jar" foi implantado (runtime-name: "sirotcon-ejb.jar")
2026-10-23 12:35:03,580 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 43) WFLYSRV0010: "sigsj_intranet-ear.ear" foi implantado (runtime-name: "sigsj_intranet-ear.ear")
2026-10-23 12:35:03,632 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0212: Retomando servidor
2026-10-23 12:35:03,644 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0025: JBoss EAP 7.4.18.GA (WildFly Core 15.0.37.Final-redhat-00001) iniciado em 9683ms - Iniciado(s) 2578 de serviços 2780 (os serviços 371 estão lentos, passivos ou sob demanda)
2026-10-23 12:35:03,646 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0060: A interface de gerenciamento http escutando em http://0.0.0.0:9990/management
2026-10-23 12:35:03,646 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0051: O console de administração escutando em http://0.0.0.0:9990
2026-10-23 12:35:06,520 ERROR [org.jboss.modcluster] (UndertowEventHandlerAdapterService - 1) MODCLUSTER000043: Failed to send INFO command to localhost/127.0.0.1:6666: Conexão recusada (Connection refused)


 [root@caddeapllx955 novo_sigsj]# ls -ld /log_jboss
ls -ld /log_jboss/config-log4j
ls: não foi possível acessar '/log_jboss': Arquivo ou diretório inexistente
ls: não foi possível acessar '/log_jboss/config-log4j': Arquivo ou diretório inexistente
[root@caddeapllx955 novo_sigsj]# find / -name "sigsj_intranet.xml" 2>/dev/null
[root@caddeapllx955 novo_sigsj]# mkdir -p /tmp/sigsjlog
cd /tmp/sigsjlog

jar xf /opt/jboss-eap/standalone/deployments/sigsj_intranet-ear.ear
jar xf sigsj_intranet.war
[root@caddeapllx955 sigsjlog]# grep -Rni "config-log4j" .
./WEB-INF/web.xml:152:      <param-value>/log_jboss/config-log4j/sigsj_intranet.xml</param-value>
[root@caddeapllx955 sigsjlog]# grep -Rni "/log_jboss" .
./WEB-INF/web.xml:152:      <param-value>/log_jboss/config-log4j/sigsj_intranet.xml</param-value>
[root@caddeapllx955 sigsjlog]#



 [root@caddeapllx955 sigsjlog]# mkdir -p /log_jboss/config-log4j
[root@caddeapllx955 sigsjlog]# cat > /log_jboss/config-log4j/sigsj_intranet.xml <<EOF
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE log4j:configuration SYSTEM "log4j.dtd">
<log4j:configuration xmlns:log4j="http://jakarta.apache.org/log4j/">

  <appender name="CONSOLE"
            class="org.apache.log4j.ConsoleAppender">
    <layout class="org.apache.log4j.PatternLayout">
      <param name="ConversionPattern"
             value="%d %-5p [%c] %m%n"/>
    </layout>
  </appender>

  <root>
    <level value="INFO"/>
    <appender-ref ref="CONSOLE"/>
  </root>

</log4j:configuration>
EOF
[root@caddeapllx955 sigsjlog]# chown -R jboss:jboss /log_jboss
chmod -R 755 /log_jboss
[root@caddeapllx955 sigsjlog]# systemctl restart jboss-eap-standalone
[root@caddeapllx955 sigsjlog]# tail -100f /logs/jboss/jboss-eap/standalone/sigsj-intranet/server.log
2026-10-23 12:55:36,340 INFO  [org.jboss.as.jsf] (ServerService Thread Pool -- 57) WFLYJSF0007: Ativadas as seguintes implantações do Jakarta Server Faces: [main]
2026-10-23 12:55:36,346 INFO  [org.jboss.as.ejb3] (MSC service thread 1-1) WFLYEJB0482: O pool estrito mdb-strict-max-pool está utilizando um tamanho de instância máximo de 8 (por classe) que é derivado do número de CPUs neste host.
2026-10-23 12:55:36,347 INFO  [org.jboss.as.ejb3] (MSC service thread 1-1) WFLYEJB0481: O pool estrito slsb-strict-max-pool está utilizando um tamanho de instância máximo de 32 (por classe) que é derivado do tamanho de pool do thead de trabalho.
2026-10-23 12:55:36,347 INFO  [org.jboss.as.connector] (MSC service thread 1-1) WFLYJCA0009: Inicialização do Subsistema Jakarta Connectors (WildFly/IronJacamar 1.5.17.Final-redhat-00001)
2026-10-23 12:55:36,419 INFO  [org.wildfly.extension.metrics] (ServerService Thread Pool -- 61) WFLYMETRICS0001: Ativando o subsistema de métricas de base
2026-10-23 12:55:36,430 INFO  [org.jboss.as.naming] (ServerService Thread Pool -- 63) WFLYNAM0001: Ativação do Subsistema de Nomeação
2026-10-23 12:55:36,472 WARN  [org.jboss.as.txn] (ServerService Thread Pool -- 70) WFLYTX0013: O atributo node-identifier em /subsystem=transactions está definido com o valor padrão. Isso é perigoso para ambientes executando vários servidores. Certifique-se de que o valor do atributo é exclusivo.
2026-10-23 12:55:36,492 INFO  [org.jboss.as.webservices] (ServerService Thread Pool -- 72) WFLYWS0002: Ativação da Extensão WebServices
2026-10-23 12:55:36,541 WARN  [org.wildfly.clustering.web.undertow] (ServerService Thread Pool -- 71) WFLYCLWEBUT0007: Nenhum provedor de roteamento encontrado para default-server; usando o provedor herdado baseado na configuração estática
2026-10-23 12:55:36,551 INFO  [org.jboss.as.connector.deployers.jdbc] (MSC service thread 1-1) WFLYJCA0018: Serviço de driver iniciado com nome-do-driver = h2
2026-10-23 12:55:36,579 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-3) WFLYUT0003: Iniciando Undertow 2.2.33.SP1-redhat-00001
2026-10-23 12:55:36,581 INFO  [org.jboss.as.naming] (MSC service thread 1-3) WFLYNAM0003: Iniciando o Serviço de Nomeação
2026-10-23 12:55:36,585 INFO  [org.jboss.as.mail.extension] (MSC service thread 1-1) WFLYMAIL0001: Sessão de e-mail associada [java:jboss/mail/Default]
2026-10-23 12:55:36,607 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 71) WFLYUT0014: Criando identificador de arquivo para caminho de acesso '/opt/jboss-eap/welcome-content' com as opções [directory-listing: 'false', follow-symlink: 'false', case-sensitive: 'true', safe-symlink-paths: '[]']
2026-10-23 12:55:36,615 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-1) WFLYUT0012: Servidor default-server foi iniciado.
2026-10-23 12:55:36,616 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-1) Queuing requests.
2026-10-23 12:55:36,616 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-1) WFLYUT0018: Iniciando host default-host
2026-10-23 12:55:36,689 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-4) WFLYUT0006: UndertowHTTP ouvinte default escutando em 0.0.0.0:8080
2026-10-23 12:55:36,695 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-1) WFLYUT0006: UndertowAJP ouvinte ajp escutando em 0.0.0.0:8009
2026-10-23 12:55:36,710 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-3) WFLYUT0006: UndertowHTTPS ouvinte https escutando em 0.0.0.0:8443
2026-10-23 12:55:36,730 INFO  [org.jboss.modcluster] (ServerService Thread Pool -- 74) MODCLUSTER000001: Initializing mod_cluster version 1.4.5.Final-redhat-00001
2026-10-23 12:55:36,738 INFO  [org.jboss.modcluster] (ServerService Thread Pool -- 74) MODCLUSTER000032: Listening to proxy advertisements on /224.0.1.105:23364
2026-10-23 12:55:36,781 INFO  [org.wildfly.iiop.openjdk] (MSC service thread 1-2) WFLYIIOP0009: Serviço CORBA ORB iniciado
2026-10-23 12:55:36,855 INFO  [org.jboss.as.ejb3] (MSC service thread 1-2) WFLYEJB0493: Suspensão completa do subsistema de Jakarta Enterprise Beans
2026-10-23 12:55:36,899 INFO  [org.jboss.as.connector.subsystems.datasources] (MSC service thread 1-1) WFLYJCA0001: Fonte de dados vinculada[java:jboss/datasources/ExampleDS]
2026-10-23 12:55:36,986 INFO  [org.jboss.as.patching] (MSC service thread 1-3) WFLYPAT0050: A ID de patch cumulativo de JBoss EAP é jboss-eap-7.4.18.CP, os patches únicos incluem: none
2026-10-23 12:55:37,000 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0027: Iniciando a implantação do "sigsj_intranet-ear.ear" (runtime-name: "sigsj_intranet-ear.ear")
2026-10-23 12:55:37,002 INFO  [org.jboss.as.server.deployment.scanner] (MSC service thread 1-1) WFLYDS0013: Foi iniciado FileSystemDeploymentService para o diretório /opt/jboss-eap/standalone/deployments
2026-10-23 12:55:37,004 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0027: Iniciando a implantação do "sirotcon-ejb.jar" (runtime-name: "sirotcon-ejb.jar")
2026-10-23 12:55:37,041 INFO  [org.jboss.ws.common.management] (MSC service thread 1-2) JBWS022052: Starting JBossWS 5.4.9.Final-redhat-00001 (Apache CXF 3.5.8.redhat-00001)
2026-10-23 12:55:37,068 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 74) AMQ221000: live Message Broker is starting with configuration Broker Configuration (clustered=false,journalDirectory=/opt/jboss-eap/standalone/data/activemq/journal,bindingsDirectory=/opt/jboss-eap/standalone/data/activemq/bindings,largeMessagesDirectory=/opt/jboss-eap/standalone/data/activemq/largemessages,pagingDirectory=/opt/jboss-eap/standalone/data/activemq/paging)
2026-10-23 12:55:37,115 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 74) AMQ221012: Using AIO Journal
2026-10-23 12:55:37,235 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 74) AMQ221043: Protocol module found: [artemis-server]. Adding protocol support for: CORE
2026-10-23 12:55:37,235 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 74) AMQ221043: Protocol module found: [artemis-hornetq-protocol]. Adding protocol support for: HORNETQ
2026-10-23 12:55:37,416 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 74) AMQ221034: Waiting indefinitely to obtain live lock
2026-10-23 12:55:37,416 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 74) AMQ221035: Live Server Obtained live lock
2026-10-23 12:55:37,720 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 74) AMQ221003: Deploying ANYCAST queue jms.queue.ExpiryQueue on address jms.queue.ExpiryQueue
2026-10-23 12:55:37,730 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 74) AMQ221003: Deploying ANYCAST queue jms.queue.DLQ on address jms.queue.DLQ
2026-10-23 12:55:37,744 INFO  [org.wildfly.extension.messaging-activemq] (MSC service thread 1-4) WFLYMSGAMQ0016: Atualização HTTP registrada para protocolo activemq-remoting manipulado pelo aceitador http-acceptor-throughput
2026-10-23 12:55:37,745 INFO  [org.wildfly.extension.messaging-activemq] (MSC service thread 1-4) WFLYMSGAMQ0016: Atualização HTTP registrada para protocolo activemq-remoting manipulado pelo aceitador http-acceptor-throughput
2026-10-23 12:55:37,745 INFO  [org.wildfly.extension.messaging-activemq] (MSC service thread 1-4) WFLYMSGAMQ0016: Atualização HTTP registrada para protocolo activemq-remoting manipulado pelo aceitador http-acceptor
2026-10-23 12:55:37,745 INFO  [org.wildfly.extension.messaging-activemq] (MSC service thread 1-2) WFLYMSGAMQ0016: Atualização HTTP registrada para protocolo activemq-remoting manipulado pelo aceitador http-acceptor
2026-10-23 12:55:37,816 INFO  [org.jboss.weld.deployer] (MSC service thread 1-3) WFLYWELD0003: Processando da implantação weld sirotcon-ejb.jar
2026-10-23 12:55:37,913 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 74) AMQ221007: Server is now live
2026-10-23 12:55:37,913 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 74) AMQ221001: Apache ActiveMQ Artemis Message Broker version 2.16.0.redhat-00052 [default, nodeID=8c98d7d4-094e-11ee-abda-00505682f3d2]
2026-10-23 12:55:37,915 WARN  [org.apache.activemq.artemis.jms.server] (ServerService Thread Pool -- 74) AMQ122005: Invalid "host" value "0.0.0.0" detected for "http-connector" connector. Switching to "caddeapllx955.agil.nprd.caixa.gov.br". If this new address is incorrect please manually configure the connector to use the proper one.
2026-10-23 12:55:37,922 INFO  [org.wildfly.extension.messaging-activemq] (ServerService Thread Pool -- 74) WFLYMSGAMQ0002: Objeto de mensagem vinculado ao nome jndi java:jboss/exported/jms/RemoteConnectionFactory
2026-10-23 12:55:37,927 INFO  [org.hibernate.validator.internal.util.Version] (MSC service thread 1-3) HV000001: Hibernate Validator 6.0.23.Final-redhat-00001
2026-10-23 12:55:37,955 INFO  [org.wildfly.extension.messaging-activemq] (ServerService Thread Pool -- 76) WFLYMSGAMQ0002: Objeto de mensagem vinculado ao nome jndi java:/ConnectionFactory
2026-10-23 12:55:38,019 INFO  [org.jboss.as.connector.deployment] (MSC service thread 1-4) WFLYJCA0007: Criação de conexão registrada java:/JmsXA
2026-10-23 12:55:38,108 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-3) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SIROTConBean' na unidade de implementação 'deployment "sirotcon-ejb.jar"' são como segue:

        java:global/sirotcon-ejb/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
        java:app/sirotcon-ejb/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
        java:module/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
        java:jboss/exported/sirotcon-ejb/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
        ejb:/sirotcon-ejb/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
        java:global/sirotcon-ejb/SIROTConBean
        java:app/sirotcon-ejb/SIROTConBean
        java:module/SIROTConBean

2026-10-23 12:55:38,143 INFO  [org.apache.activemq.artemis.ra] (MSC service thread 1-4) AMQ151007: Resource adaptor started
2026-10-23 12:55:38,144 INFO  [org.jboss.as.connector.services.resourceadapters.ResourceAdapterActivatorService$ResourceAdapterActivator] (MSC service thread 1-4) IJ020002: Deployed: file://RaActivatoractivemq-ra
2026-10-23 12:55:38,214 INFO  [org.jboss.as.connector.deployment] (MSC service thread 1-3) WFLYJCA0002: Conectores de Jakarta vinculados ConnectionFactory [java:/JmsXA]
2026-10-23 12:55:38,214 INFO  [org.jboss.as.connector.deployment] (MSC service thread 1-3) WFLYJCA0118: Vínculo de criação de conexão chamado java:/JmsXA para o alias java:jboss/DefaultJMSConnectionFactory
2026-10-23 12:55:38,311 INFO  [org.jboss.weld.Version] (MSC service thread 1-2) WELD-000900: 3.1.10 (redhat)
2026-10-23 12:55:38,354 WARN  [org.jboss.as.server.deployment] (MSC service thread 1-3) WFLYSRV0274: A dependência org.slf4j.jcl-over-slf4j excluída do jboss-deployment-structure.xml não existe.
2026-10-23 12:55:38,559 INFO  [org.infinispan.CONTAINER] (ServerService Thread Pool -- 74) ISPN000128: Infinispan version: Infinispan 'Corona Extra' 11.0.19.Final-redhat-00001
2026-10-23 12:55:38,586 INFO  [org.infinispan.CONFIG] (MSC service thread 1-3) ISPN000152: Passivation configured without an eviction policy being selected. Only manually evicted entities will be passivated.
2026-10-23 12:55:38,587 INFO  [org.infinispan.CONFIG] (MSC service thread 1-3) ISPN000152: Passivation configured without an eviction policy being selected. Only manually evicted entities will be passivated.
2026-10-23 12:55:38,649 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-4) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "sigsjintrastatic.war")
2026-10-23 12:55:38,649 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-3) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "sigsj_intranet.war")
2026-10-23 12:55:38,698 INFO  [org.infinispan.PERSISTENCE] (ServerService Thread Pool -- 74) ISPN000556: Starting user marshaller 'org.wildfly.clustering.infinispan.spi.marshalling.InfinispanProtoStreamMarshaller'
2026-10-23 12:55:38,977 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 74) WFLYCLINF0002: Cache http-remoting-connector inicializado a partir do recipiente ejb
2026-10-23 12:55:41,451 INFO  [org.jboss.weld.deployer] (MSC service thread 1-2) WFLYWELD0003: Processando da implantação weld sigsj_intranet-ear.ear
2026-10-23 12:55:41,483 INFO  [org.jboss.weld.deployer] (MSC service thread 1-3) WFLYWELD0003: Processando da implantação weld sigsjintrastatic.war
2026-10-23 12:55:41,838 INFO  [org.jboss.weld.deployer] (MSC service thread 1-4) WFLYWELD0003: Processando da implantação weld sigsj_intranet.war
2026-10-23 12:55:41,862 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-4) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SIROTConBean' na unidade de implementação 'subdeployment "sigsj_intranet.war" of deployment "sigsj_intranet-ear.ear"' são como segue:

        java:global/sigsj_intranet-ear/sigsj_intranet/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
        java:app/sigsj_intranet/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
        java:module/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
        java:jboss/exported/sigsj_intranet-ear/sigsj_intranet/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
        ejb:sigsj_intranet-ear/sigsj_intranet/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
        java:global/sigsj_intranet-ear/sigsj_intranet/SIROTConBean
        java:app/sigsj_intranet/SIROTConBean
        java:module/SIROTConBean

2026-10-23 12:55:42,208 WARN  [org.jboss.as.connector.deployers.jdbc] (MSC service thread 1-3) WFLYJCA0003: Não foi possível instanciar a classe do driver "org.olap4j.driver.xmla.XmlaOlap4jDriver": java.lang.NoSuchMethodException: org.olap4j.driver.xmla.XmlaOlap4jDriver.<init>()
2026-10-23 12:55:42,877 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 77) WFLYUT0021: Contexto web registrado: '/sigsjintrastatic' para servidor 'default-server'
2026-10-23 12:55:42,922 INFO  [javax.enterprise.resource.webcontainer.jsf.config] (ServerService Thread Pool -- 78) Initializing Mojarra (1.2_15-20100816-SNAPSHOT) for context '/sigsj_intranet'
2026-10-23 12:55:43,293 INFO  [javax.enterprise.resource.webcontainer.jsf.application] (ServerService Thread Pool -- 78) JSF1048: PostConstruct/PreDestroy annotations present.  ManagedBeans methods marked with these annotations will have said annotations processed.
2026-10-23 12:55:43,528 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 78) WFLYUT0021: Contexto web registrado: '/sigsj_intranet' para servidor 'default-server'
2026-10-23 12:55:43,611 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 43) WFLYSRV0010: "sirotcon-ejb.jar" foi implantado (runtime-name: "sirotcon-ejb.jar")
2026-10-23 12:55:43,613 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 43) WFLYSRV0010: "sigsj_intranet-ear.ear" foi implantado (runtime-name: "sigsj_intranet-ear.ear")
2026-10-23 12:55:43,642 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0212: Retomando servidor
2026-10-23 12:55:43,645 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0025: JBoss EAP 7.4.18.GA (WildFly Core 15.0.37.Final-redhat-00001) iniciado em 9561ms - Iniciado(s) 2578 de serviços 2780 (os serviços 371 estão lentos, passivos ou sob demanda)
2026-10-23 12:55:43,646 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0060: A interface de gerenciamento http escutando em http://0.0.0.0:9990/management
2026-10-23 12:55:43,647 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0051: O console de administração escutando em http://0.0.0.0:9990
2026-10-23 12:55:46,748 ERROR [org.jboss.modcluster] (UndertowEventHandlerAdapterService - 1) MODCLUSTER000043: Failed to send INFO command to localhost/127.0.0.1:6666: Conexão recusada (Connection refused)



 Skip to main contentSkip to measure filters
Logo, link to homepage
Projects
Issues
Rules
Quality Profiles
Quality Gates

Search for projects...
JM
SIGSJ-intranet


merge-develop
Last analysis of this Branch had 3 warnings
October 23, 2026 at 1:28 PM
Version 10.0.1.1

Overview
Issues
Security Hotspots
Measures
Code
Activity
Project Information

Project Overview
Reliability
Security
Security Review
Maintainability
Coverage
Coverage on New Code

Overview
On new code

Coverage
70.0%

Lines to Cover
10

Uncovered Lines
3

Line Coverage
70.0%

Conditions to Cover
0

Uncovered Conditions
0
Overall

Coverage
70.4%

Lines to Cover
25

Uncovered Lines
7

Line Coverage
72.0%

Conditions to Cover
2

Uncovered Conditions
1

Condition Coverage
50.0%
Tests

Errors
0

Failures
0

Skipped
0

Success
100%
Duplications
Size
Complexity
Issues
SIGSJ-intranetsigsj_intranet-warsrcmainjava/br/gov/caixa/sigsjintranetservletCaixaConfigServlet.java
Coverage on New Code
70.0%
 SIGSJ-intranet sigsj_intranet-war/.../br/gov/caixa/sigsj/intranet/servlet/CaixaConfigServlet.java

package br.gov.caixa.sigsj.intranet.servlet;
import java.io.IOException;
import java.util.Locale;
import javax.servlet.ServletConfig;
import javax.servlet.ServletException;
import javax.servlet.http.HttpServlet;
import org.apache.log4j.Logger;
import org.apache.log4j.xml.DOMConfigurator;
import br.gov.caixa.sigsj.common.dao.infra.IsoXmlMapeamento;
import br.gov.caixa.sigsj.common.exception.SystemException;
public class CaixaConfigServlet extends HttpServlet {
	private static final long serialVersionUID = 3035100159720835011L;
	private static final Logger LOG = Logger.getLogger(CaixaConfigServlet.class);
	@Override
	public void init(final ServletConfig config) throws ServletException {
		super.init(config);
		Locale.setDefault(new Locale("pt", "BR"));
		final String sistema = config.getInitParameter("nome_sistema");
		final String file;
		file = config.getInitParameter("log4j-Caixa");
		if (file != null) {
			DOMConfigurator.configure(file);
		}
		carregarListaXml();
		populaXmlProcessamento();
		LOG.debug(sistema + " INTRANET SUBIU COM SUCESSO!");
	}
	private void carregarListaXml() throws ServletException {
		try {
			IsoXmlMapeamento.getInstance().carregaListaXmls();
		} catch (final IOException e) {
			LOG.error("Erro ao realizar o parser da lista dos XMLs:", e);
			throw new ServletException("Não foi possível efetuar leitura da lista de arquivos XML!", e);
		}
	}
	private void populaXmlProcessamento() throws ServletException {
		try {
			final String[] transacoesIniciais = {"GJ92", "GJ97", "GJ93", "GJ98", "GJ95", "GJ96", "GJ99", "GJ90", "GJ91", "GJ94", "GJ8S", "GJ66",
					"GJ0O", "GJAI", "GJ4D", "GJ01", "GJ02", "GJ0P", "GJ0Q"};
			IsoXmlMapeamento.getInstance().efetuarLeituraXML(transacoesIniciais);
		} catch (final SystemException e) {
			LOG.error("Erro ao realizar o parser nos XMLs:", e);
			throw new ServletException("Não foi possível efetuar leitura dos arquivos XML!", e);
		}
	}
}
SonarQube™ technology is powered by SonarSource SA
Community Editionv9.9.5 (build 90363)NO LONGER ACTIVELGPL v3CommunityDocumentationPluginsWeb API


o jeferson fez essas alteraçoes para poder resolver o problema mais ta quebrando a build agora me ajdua a desfazer o que ele fez pois fx na branch principal




Skip to main content
Azure DevOps
projetos
/
Caixa
/
Repos
/
Commits
/

SIGSJ-intranet
Search


Caixa

Overview

Boards

Repos
Files
Commits
Pushes
Branches
Tags
Pull requests

Pipelines

Test Plans

Artifacts
Project settings
Updated CaixaConfigServlet.java
Browse Files

0109de56

Thiago Jeferson de Sousa Silva
committed
33m ago
merge-develop
failed
Files
Details
Parent 1 → This commit

Filter
1 changed file

Inline



SIGSJ-intranet


CaixaConfigServlet.java
-34+9
/sigsj_intranet-war/src/main/java/br/gov/caixa/sigsj/intranet/servlet/CaixaConfigServlet.java
View
package br.gov.caixa.sigsj.intranet.servlet;
import java.io.File;
import java.io.IOException;
import java.util.Locale;
public class CaixaConfigServlet extends HttpServlet {
	private static final long serialVersionUID = 3035100159720835011L;
	private static final Logger LOG = Logger.getLogger(CaixaConfigServlet.class);
	@Override
	public void init(final ServletConfig config) throws ServletException {
		super.init(config);
		Locale.setDefault(new Locale("pt", "BR"));
		final String sistema = config.getInitParameter("nome_sistema");
        final String file = config.getInitParameter("log4j-Caixa");
		final String file;
        if (file != null) {
		file = config.getInitParameter("log4j-Caixa");
            if (new File(file).exists()) {
		if (file != null) {
			DOMConfigurator.configure(file);
            } else {
                LOG.warn("Arquivo de configuração Log4j não encontrado: " + file);
		}
        }
		carregarListaXml();
		populaXmlProcessamento();
	private void carregarListaXml() throws ServletException {
		try {
			IsoXmlMapeamento.getInstance().carregaListaXmls();
		} catch (final IOException e) {
			LOG.error("Erro ao realizar o parser da lista dos XMLs:", e);
            throw new ServletException(
                "Não foi possível efetuar leitura da lista de arquivos XML!",
                e);
			throw new ServletException("Não foi possível efetuar leitura da lista de arquivos XML!", e);
		}
	}
		try {
            final String[] transacoesIniciais = {
                "GJ92", "GJ97", "GJ93", "GJ98", "GJ95",
                "GJ96", "GJ99", "GJ90", "GJ91", "GJ94",
                "GJ8S", "GJ66", "GJ0O", "GJAI", "GJ4D",
                "GJ01", "GJ02", "GJ0P", "GJ0Q"
            };
			final String[] transacoesIniciais = {"GJ92", "GJ97", "GJ93", "GJ98", "GJ95", "GJ96", "GJ99", "GJ90", "GJ91", "GJ94", "GJ8S", "GJ66",
					"GJ0O", "GJAI", "GJ4D", "GJ01", "GJ02", "GJ0P", "GJ0Q"};
            IsoXmlMapeamento.getInstance()
                .efetuarLeituraXML(transacoesIniciais);
			IsoXmlMapeamento.getInstance().efetuarLeituraXML(transacoesIniciais);
		} catch (final SystemException e) {
			LOG.error("Erro ao realizar o parser nos XMLs:", e);
            throw new ServletException(
                "Não foi possível efetuar leitura dos arquivos XML!",
                e);
			throw new ServletException("Não foi possível efetuar leitura dos arquivos XML!", e);
		}
	}
}
Row 2

4 pipelines found

Row 2

Showing 16 deployments

Row 2

Expanded

Collapsed

Row 5. Clickable

Showing 25 filtered items.

Get started and run this pipeline for the first time!

Showing 31 filtered items.

Showing 25 filtered items.

Row 2. Clickable

Row 2. Clickable

Showing 25 filtered items.

Get started and run this pipeline for the first time!

Showing 31 filtered items.

Showing 25 filtered items.

Row 2. Clickable

Row 2. Clickable

