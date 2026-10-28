[p585600@caddeapllx2651 ~]$ ps -ef --forest | grep -A15 "sshd: sansbp01" | grep -v grep
root      151088    5297  0 12:21 ?        00:00:00  \_ sshd: sansbp01 [priv]
sansbp01  151090  151088  0 12:21 ?        00:00:00      \_ sshd: sansbp01@notty
sansbp01  162524  151090  0 12:24 ?        00:00:00          \_ /bin/sh -c sudo -i  -u root /bin/sh -c 'echo BECOME-SUCCESS-nuqlrtalgdnjzctfdwckppjbnyvmqzvf ; /usr/bin/python' && sleep 0
root      162544  162524  0 12:24 ?        00:00:00              \_ sudo -i -u root /bin/sh -c echo BECOME-SUCCESS-nuqlrtalgdnjzctfdwckppjbnyvmqzvf ; /usr/bin/python
root      162545  162544  0 12:24 ?        00:00:00                  \_ /usr/bin/python
root        5338       1  0 out19 ?        00:00:00 /usr/sbin/oddjobd -n -p /run/oddjobd.pid -t 300
root        5382       1  0 out19 ?        00:00:00 /usr/sbin/sssd -i --logger=files
root        5383    5382  0 out19 ?        00:05:28  \_ /usr/libexec/sssd/sssd_be --domain LDAP --uid 0 --gid 0 --logger=files
root        5384    5382  0 out19 ?        00:01:28  \_ /usr/libexec/sssd/sssd_nss --uid 0 --gid 0 --logger=files
root        5385    5382  0 out19 ?        00:00:03  \_ /usr/libexec/sssd/sssd_pam --uid 0 --gid 0 --logger=files
root        5386    5382  0 out19 ?        00:00:05  \_ /usr/libexec/sssd/sssd_sudo --uid 0 --gid 0 --logger=files
sansbp01    5421       1  0 out19 ?        00:00:00 /usr/lib/systemd/systemd --user
sansbp01    5423    5421  0 out19 ?        00:00:00  \_ (sd-pam)
root        7287       1  0 out19 ?        00:01:31 /usr/bin/python3 -Es /usr/sbin/tuned -l -P
root       11259       1  0 out19 ?        00:06:45 /usr/share/metricbeat/bin/metricbeat --environment systemd -c /etc/metricbeat/metricbeat.yml --path.home /usr/share/metricbeat --path.config /etc/metricbeat --path.data /var/lib/metricbeat --path.logs /var/log/metricbeat
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ tail -50 /logs/jboss/jboss-eap/standalone/siccp-intra/server.log
Description: Invalid config-property-type for ManagedConnectionFactory.
Code: Class: com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl Property: rescanInterval Type: int

2026-10-28 12:04:16,759 INFO  [org.jboss.as.connector.deployers.RaXmlDeployer] (MSC service thread 1-2) IJ020002: Deployed: file:/opt/jboss-eap/standalone/tmp/vfs/temp/tempbb0a732f57680f28/content-1e33b87aeca9e6dc/contents/
2026-10-28 12:04:16,760 INFO  [org.jboss.as.connector.deployment] (MSC service thread 1-2) WFLYJCA0002: Conectores de Jakarta vinculados ConnectionFactory [java:jboss/jms/SiccpQueueConnectionFactory]
2026-10-28 12:04:16,760 INFO  [org.jboss.as.connector.deployment] (MSC service thread 1-2) WFLYJCA0002: Conectores de Jakarta vinculados AdminObject [java:jboss/jms/rsp_consulta_imagem_cheque]
2026-10-28 12:04:16,760 INFO  [org.jboss.as.connector.deployment] (MSC service thread 1-2) WFLYJCA0002: Conectores de Jakarta vinculados AdminObject [java:jboss/jms/req_consulta_imagem_cheque]
2026-10-28 12:04:16,765 INFO  [org.infinispan.CONFIG] (MSC service thread 1-1) ISPN000152: Passivation configured without an eviction policy being selected. Only manually evicted entities will be passivated.
2026-10-28 12:04:16,765 INFO  [org.infinispan.CONFIG] (MSC service thread 1-1) ISPN000152: Passivation configured without an eviction policy being selected. Only manually evicted entities will be passivated.
2026-10-28 12:04:16,858 INFO  [org.infinispan.PERSISTENCE] (ServerService Thread Pool -- 73) ISPN000556: Starting user marshaller 'org.wildfly.clustering.infinispan.spi.marshalling.InfinispanProtoStreamMarshaller'
2026-10-28 12:04:17,065 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 73) WFLYCLINF0002: Cache http-remoting-connector inicializado a partir do recipiente ejb
2026-10-28 12:04:18,477 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 72) AMQ221003: Deploying ANYCAST queue jms.queue.ExpiryQueue on address jms.queue.ExpiryQueue
2026-10-28 12:04:18,484 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 72) AMQ221003: Deploying ANYCAST queue jms.queue.DLQ on address jms.queue.DLQ
2026-10-28 12:04:18,493 INFO  [org.wildfly.extension.messaging-activemq] (MSC service thread 1-4) WFLYMSGAMQ0016: Atualização HTTP registrada para protocolo activemq-remoting manipulado pelo aceitador http-acceptor
2026-10-28 12:04:18,493 INFO  [org.wildfly.extension.messaging-activemq] (MSC service thread 1-2) WFLYMSGAMQ0016: Atualização HTTP registrada para protocolo activemq-remoting manipulado pelo aceitador http-acceptor-throughput
2026-10-28 12:04:18,494 INFO  [org.wildfly.extension.messaging-activemq] (MSC service thread 1-1) WFLYMSGAMQ0016: Atualização HTTP registrada para protocolo activemq-remoting manipulado pelo aceitador http-acceptor-throughput
2026-10-28 12:04:18,494 INFO  [org.wildfly.extension.messaging-activemq] (MSC service thread 1-4) WFLYMSGAMQ0016: Atualização HTTP registrada para protocolo activemq-remoting manipulado pelo aceitador http-acceptor
2026-10-28 12:04:18,628 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 72) AMQ221007: Server is now live
2026-10-28 12:04:18,628 INFO  [org.apache.activemq.artemis.core.server] (ServerService Thread Pool -- 72) AMQ221001: Apache ActiveMQ Artemis Message Broker version 2.16.0.redhat-00052 [default, nodeID=8c98d7d4-094e-11ee-abda-00505682f3d2]
2026-10-28 12:04:18,631 WARN  [org.apache.activemq.artemis.jms.server] (ServerService Thread Pool -- 73) AMQ122005: Invalid "host" value "0.0.0.0" detected for "http-connector" connector. Switching to "caddeapllx2651.agil.nprd.caixa.gov.br". If this new address is incorrect please manually configure the connector to use the proper one.
2026-10-28 12:04:18,642 INFO  [org.wildfly.extension.messaging-activemq] (ServerService Thread Pool -- 73) WFLYMSGAMQ0002: Objeto de mensagem vinculado ao nome jndi java:jboss/exported/jms/RemoteConnectionFactory
2026-10-28 12:04:18,652 INFO  [org.wildfly.extension.messaging-activemq] (ServerService Thread Pool -- 72) WFLYMSGAMQ0002: Objeto de mensagem vinculado ao nome jndi java:/ConnectionFactory
2026-10-28 12:04:18,661 INFO  [org.jboss.as.connector.deployment] (MSC service thread 1-2) WFLYJCA0007: Criação de conexão registrada java:/JmsXA
2026-10-28 12:04:18,670 INFO  [org.jboss.weld.deployer] (MSC service thread 1-3) WFLYWELD0003: Processando da implantação weld siccp-intra.war
2026-10-28 12:04:18,743 INFO  [org.apache.activemq.artemis.ra] (MSC service thread 1-2) AMQ151007: Resource adaptor started
2026-10-28 12:04:18,743 INFO  [org.jboss.as.connector.services.resourceadapters.ResourceAdapterActivatorService$ResourceAdapterActivator] (MSC service thread 1-2) IJ020002: Deployed: file://RaActivatoractivemq-ra
2026-10-28 12:04:18,743 INFO  [org.jboss.as.connector.deployment] (MSC service thread 1-1) WFLYJCA0002: Conectores de Jakarta vinculados ConnectionFactory [java:/JmsXA]
2026-10-28 12:04:18,743 INFO  [org.jboss.as.connector.deployment] (MSC service thread 1-1) WFLYJCA0118: Vínculo de criação de conexão chamado java:/JmsXA para o alias java:jboss/DefaultJMSConnectionFactory
2026-10-28 12:04:19,218 INFO  [org.jboss.weld.Event] (MSC service thread 1-2) WELD-000411: Observer method [BackedAnnotatedMethod] org.apache.myfaces.config.annotation.CdiAnnotationProviderExtension.processAnnotatedType(@Observes ProcessAnnotatedType<T>) receives events for all annotated types. Consider restricting events using @WithAnnotations or a generic type with bounds.
2026-10-28 12:04:19,227 INFO  [org.jboss.weld.Event] (MSC service thread 1-2) WELD-000411: Observer method [BackedAnnotatedMethod] org.apache.myfaces.cdi.JsfArtifactProducerExtension.processAnnotatedType(@Observes ProcessAnnotatedType<T>, BeanManager) receives events for all annotated types. Consider restricting events using @WithAnnotations or a generic type with bounds.
2026-10-28 12:04:19,780 INFO  [org.apache.myfaces.ee.MyFacesContainerInitializer] (ServerService Thread Pool -- 72) Using org.apache.myfaces.ee.MyFacesContainerInitializer
2026-10-28 12:04:19,844 INFO  [org.apache.myfaces.config.DefaultFacesConfigurationProvider] (ServerService Thread Pool -- 72) Reading standard config META-INF/standard-faces-config.xml
2026-10-28 12:04:19,959 INFO  [org.apache.myfaces.config.DefaultFacesConfigurationProvider] (ServerService Thread Pool -- 72) Reading config /WEB-INF/faces-config.xml
2026-10-28 12:04:20,109 INFO  [org.apache.myfaces.config.DefaultFacesConfigurationProvider] (ServerService Thread Pool -- 72) Reading config : vfs:/content/siccp-intra.war/WEB-INF/lib/tomahawk20-1.1.14.jar/META-INF/faces-config.xml
2026-10-28 12:04:20,209 INFO  [org.apache.myfaces.util.ExternalSpecifications] (ServerService Thread Pool -- 72) MyFaces Core CDI support enabled
2026-10-28 12:04:20,210 INFO  [org.apache.myfaces.spi.impl.DefaultInjectionProviderFactory] (ServerService Thread Pool -- 72) Using InjectionProvider org.apache.myfaces.spi.impl.CDIAnnotationDelegateInjectionProvider
2026-10-28 12:04:20,241 INFO  [org.apache.myfaces.util.ExternalSpecifications] (ServerService Thread Pool -- 72) MyFaces Core Bean Validation support enabled
2026-10-28 12:04:20,266 INFO  [org.apache.myfaces.config.FacesConfigurator] (ServerService Thread Pool -- 72) Serialization provider : class org.apache.myfaces.shared_impl.util.serial.DefaultSerialFactory
2026-10-28 12:04:20,275 INFO  [org.apache.myfaces.config.annotation.DefaultLifecycleProviderFactory] (ServerService Thread Pool -- 72) Using LifecycleProvider org.apache.myfaces.config.annotation.Tomcat7AnnotationLifecycleProvider
2026-10-28 12:04:20,301 INFO  [org.apache.myfaces.webapp.AbstractFacesInitializer] (ServerService Thread Pool -- 72) ServletContext initialized.
2026-10-28 12:04:20,311 INFO  [org.apache.myfaces.webapp.StartupServletContextListener] (ServerService Thread Pool -- 72) MyFaces Core has started, it took [520] ms.
2026-10-28 12:04:20,341 INFO  [org.apache.myfaces.webapp.MyFacesServlet] (ServerService Thread Pool -- 72) MyFacesServlet for context '/opt/jboss-eap/standalone/tmp/vfs/temp/tempbb0a732f57680f28/content-48db082ec165d920' initialized.
2026-10-28 12:04:20,342 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 72) WFLYUT0021: Contexto web registrado: '/' para servidor 'default-server'
2026-10-28 12:04:20,421 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 42) WFLYSRV0010: "siccp-intra.war" foi implantado (runtime-name: "siccp-intra.war")
2026-10-28 12:04:20,421 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 42) WFLYSRV0010: "sirotcon-ejb.jar" foi implantado (runtime-name: "sirotcon-ejb.jar")
2026-10-28 12:04:20,422 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 42) WFLYSRV0010: "wmq.jmsra.rar" foi implantado (runtime-name: "wmq.jmsra.rar")
2026-10-28 12:04:20,453 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0212: Retomando servidor
2026-10-28 12:04:20,456 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0025: JBoss EAP 7.4.18.GA (WildFly Core 15.0.37.Final-redhat-00001) iniciado em 9595ms - Iniciado(s) 1881 de serviços 2083 (os serviços 371 estão lentos, passivos ou sob demanda)
2026-10-28 12:04:20,458 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0060: A interface de gerenciamento http escutando em http://0.0.0.0:9990/management
2026-10-28 12:04:20,458 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0051: O console de administração escutando em http://0.0.0.0:9990
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ ss -ltnp | grep -E "8080|8443|9990"
LISTEN 0      50           0.0.0.0:9990       0.0.0.0:*
LISTEN 0      10000        0.0.0.0:8080       0.0.0.0:*
LISTEN 0      10000        0.0.0.0:8443       0.0.0.0:*
[p585600@caddeapllx2651 ~]$
