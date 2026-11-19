No 473 (10.116.97.79), sifec-intranet:

bash
grep -a "consultarCorrelationClientePorCPF" /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | tail -3

No 409 (10.116.97.41), SIPEN:

bash
grep -a "consultarCorrelationClientePorCPF" /opt/jboss/jboss-eap/hc/servers/sipen_node1_DES_llx409/log/server.log | tail -3

O servidor que mostrar a linha das 15:08:52 é o certo. Depois, no mesmo log, olhamos o que veio junto:

bash
grep -a -A15 "15:08:52,769" <log onde apareceu> | grep -aE "ERROR|WARN|ARJUNA|Exception|MQJCA|JMS" | head -20

No documento de passagem, eu coloquei a Claudia como contato do SIPEN. Se ela for do CCR, ajusto antes de você mandar. Me confirma.



[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]# grep -a "consultarCorrelationClientePorCPF" /opt/jboss/jboss-eap/hc/servers/sipen_node1_DES_llx409/log/server.log | tail -3
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#






[sudo] password for p585600:
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]# LOG=/opt/jboss/jboss-eap/hc/servers/sipen_node1_DES_llx409/log/server.log
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]# grep -a -A15 "15:08:52,769" $LOG | grep -aE "ERROR|WARN|ARJUNA|Exception|MQJCA|JMS" | head -20
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]# grep -a "consultarCorrelationClientePorCPF" /opt/jboss/jboss-eap/hc/servers/sipen_node1_DES_llx409/log/server.log | tail -3
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]# grep -a -A15 "15:08:52,769" <log onde apareceu> | grep -aE "ERROR|WARN|ARJUNA|Exception|MQJCA|JMS" | head -20
bash: syntax error near unexpected token `|'
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#


Para verificar (é do SIPEN, então no 409, IP 10.116.97.41)

1. O que mais aconteceu às 15:08:52:

bash
LOG=/opt/jboss/jboss-eap/hc/servers/sipen_node1_DES_llx409/log/server.log
grep -a -A15 "15:08:52,769" $LOG | grep -aE "ERROR|WARN|ARJUNA|Exception|MQJCA|JMS" | head -20

2. Comparar o WMQ, como ela pediu (CLI do 471):

/server-group=sipen:read-attribute(name=profile)

Com o profile que aparecer:

/profile=full-ha-sipen/subsystem=resource-adapters:read-resource(recursive=true)

No 6.4 (10.116.88.20), sem mostrar senha:

bash
grep -n -A40 'wmq.jmsra' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -viE 'password' | head -80

Também vale conferir a versão: no 7.4 está ativo o wmq.jmsra.rar, enquanto no domain existem também o 7.0.1.12 e o 7.5.0.8 sem uso.




[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] /server-group=sipen:read-attribute(name=profile)
{
    "outcome" => "success",
    "result" => "full-ha-sipen"
}

[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]


**[domain@localhost:9999 /] /profile=full-ha-sipen/subsystem=resource-adapters:read-resource(recursive=true)
{
    "outcome" => "success",
    "result" => {"resource-adapter" => undefined}
}

[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
**




-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$ grep -n -A40 'wmq.jmsra' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -viE 'password' | head -80
3232:                    <resource-adapter id="wmq.jmsra.rar">
3233-                        <archive>
3234:                            wmq.jmsra.rar
3235-                        </archive>
3236-                        <transaction-support>NoTransaction</transaction-support>
3237-                        <connection-definitions>
3238-                            <connection-definition class-name="com.ibm.mq.connector.outbound.ManagedQueueConnectionFactoryImpl" jndi-name="java:/jms/PMCConnectionFactory" enabled="true" pool-name="java:/jms/PMCConnectionFactory">
3239-                                <config-property name="channel">
3240-                                    ${pmc.ejb.mq.channel}
3241-                                </config-property>
3242-                                <config-property name="hostName">
3243-                                    ${pmc.ejb.mq.hostName}
3244-                                </config-property>
3247-                                </config-property>
3248-                                <config-property name="queueManager">
3249-                                    ${pmc.ejb.mq.queueManager}
3250-                                </config-property>
3251-                                <config-property name="port">
3252-                                    ${pmc.ejb.mq.port}
3253-                                </config-property>
3254-                                <config-property name="username">
3255-                                    ${pmc.ejb.mq.userName}
3256-                                </config-property>
3257-                                <pool>
3258-                                    <max-pool-size>30</max-pool-size>
3259-                                </pool>
3260-                                <security>
3261-                                    <application/>
3262-                                </security>
3263-                                <validation>
3264-                                    <background-validation>false</background-validation>
3265-                                </validation>
3266-                            </connection-definition>
3267-                        </connection-definitions>
3268-                        <admin-objects>
3269-                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.RSP.MANUTENCAO_COBRANCA_BANCARIA" enabled="true" use-java-context="false" pool-name="java:/jms/SIBAR.RSP.MANUTENCAO_COBRANCA_BANCARIA">
3270-                                <config-property name="baseQueueName">
3271-                                    SIBAR.RSP.MANUTENCAO_COBRANCA_BANCARIA
3272-                                </config-property>
3273-                                <config-property name="baseQueueManagerName">
3274-                                    ${pmc.ejb.mq.queueManager}
--
3496:                    <resource-adapter-ref resource-adapter-name="wmq.jmsra.rar"/>
3497-                    <bean-instance-pool-ref pool-name="mdb-strict-max-pool"/>
3498-                </mdb>
3499-                <pools>
3500-                    <bean-instance-pools>
3501-                        <strict-max-pool name="slsb-strict-max-pool" max-pool-size="20" instance-acquisition-timeout="5" instance-acquisition-timeout-unit="MINUTES"/>
3502-                        <strict-max-pool name="mdb-strict-max-pool" max-pool-size="20" instance-acquisition-timeout="5" instance-acquisition-timeout-unit="MINUTES"/>
3503-                    </bean-instance-pools>
3504-                </pools>
3505-                <caches>
3506-                    <cache name="simple" aliases="NoPassivationCache"/>
3507-                    <cache name="passivating" passivation-store-ref="file" aliases="SimpleStatefulCache"/>
3508-                    <cache name="clustered" passivation-store-ref="infinispan" aliases="StatefulTreeCache"/>
3509-                </caches>
3510-                <passivation-stores>
3511-                    <file-passivation-store name="file" idle-timeout="300" idle-timeout-unit="SECONDS" max-size="10000" relative-to="jboss.server.data.dir" groups-path="ejb3/groups" sessions-path="ejb3/sessions" subdirectory-count="100"/>
3512-                    <cluster-passivation-store name="infinispan" idle-timeout="300" idle-timeout-unit="SECONDS" max-size="10000" cache-container="ejb" client-mappings-cache="remote-connector-client-mappings" passivate-events-on-replicate="true"/>
3513-                </passivation-stores>
3514-                <async thread-pool-name="default"/>
3515-                <timer-service thread-pool-name="default" default-data-store="default-file-store">
3516-                    <data-stores>
3517-                        <file-data-store name="default-file-store" path="timer-service-data" relative-to="jboss.server.data.dir"/>
3518-                    </data-stores>
3519-                </timer-service>
3520-                <remote connector-ref="remoting-connector" thread-pool-name="default"/>
3521-                <thread-pools>
3522-                    <thread-pool name="default">
3523-                        <max-threads count="10"/>
3524-                        <keepalive-time time="100" unit="milliseconds"/>
3525-                    </thread-pool>
3526-                </thread-pools>
3527-                <iiop enable-by-default="false" use-qualified-name="false"/>
3528-                <in-vm-remote-interface-invocation pass-by-value="true"/>
3529-            </subsystem>
3530-            <subsystem xmlns="urn:jboss:domain:infinispan:1.5">
3531-                <cache-container name="cluster" aliases="ha-partition" default-cache="default">
3532-                    <transport lock-timeout="60000"/>
3533-                    <replicated-cache name="default" mode="SYNC" batching="true">
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$

