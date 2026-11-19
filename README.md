[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]# D=/opt/jboss/jboss-eap/dc/configuration/domain.xml
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]# sed -n '19607,20596p' $D | sed -n '/<resource-adapter id="wmq/,/<\/resource-adapter>/p' | grep -A1 -E 'jndi-name=|name="(hostName|port|channel|queueManager)"' | grep -vE '^--$|password'
                            <connection-definition class-name="com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl" jndi-name="java:/jms/UniSibarConnectionFactory" pool-name="UniSibarConnectionFactory">
                                <config-property name="channel">
                                    SIFEC.SVRCONN
                                <config-property name="hostName">
                                    10.192.224.100
                                <config-property name="queueManager">
                                    BRD3
                                <config-property name="port">
                                    1415
                            <connection-definition class-name="com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl" jndi-name="java:/jms/SiarcConnectionFactory" pool-name="SiarcConnectionFactory">
                                <config-property name="hostName">
                                    10.192.228.145
                                <config-property name="queueManager">
                                    BRD1
                                <config-property name="port">
                                    1414
                                <config-property name="channel">
                                    BRSUN033.TO.BRD1
                            <connection-definition class-name="com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl" jndi-name="java:/jms/SiormConnectionFactory" pool-name="SiormConnectionFactory">
                                <config-property name="channel">
                                    SIFEC.SVRCONN
                                <config-property name="hostName">
                                    ibmspdes.caixa
                                <config-property name="queueManager">
                                    QSDA
                                <config-property name="port">
                                    1420
                            <connection-definition class-name="com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl" jndi-name="java:/jms/TrfConnectionFactory" pool-name="java:/jms/TrfConnectionFactory">
                                <config-property name="channel">
                                    SIPGE.SVRCONN
                                <config-property name="hostName">
                                    10.216.80.111
                                <config-property name="queueManager">
                                    RJH1
                                <config-property name="port">
                                    1414
                            <connection-definition class-name="com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl" jndi-name="java:/jms/SiabeConnectionFactory" pool-name="SiabeConnectionFactory">
                                <config-property name="channel">
                                    BRD3.SVRCONN.SIABE
                                <config-property name="hostName">
                                    10.192.224.100
                                <config-property name="queueManager">
                                    BRD3
                                <config-property name="port">
                                    1415
                            <connection-definition class-name="com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl" jndi-name="java:/jms/SICCRConnectionFactory" enabled="true" pool-name="java:/jms/SICCRConnectionFactory">
                                <config-property name="channel">
                                    SICCR.SVRCONN
                                <config-property name="hostName">
                                    10.116.97.49
                                <config-property name="queueManager">
                                    QSD1
                                <config-property name="port">
                                    1420
                            <connection-definition class-name="com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl" jndi-name="java:/jms/SipesConnectionFactory" enabled="true" pool-name="java:/jms/SipesConnectionFactory">
                                <config-property name="channel">
                                    SIFEC.SVRCONN
                                <config-property name="hostName">
                                    10.192.224.100
                                <config-property name="queueManager">
                                    BRD3
                                <config-property name="port">
                                    1415
                            <connection-definition class-name="com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl" jndi-name="java:/jms/SicliConnectionFactory" enabled="true" pool-name="java:/jms/SicliConnectionFactory">
                                <config-property name="channel">
                                    SIFEC.SVRCONN
                                <config-property name="hostName">
                                    10.192.224.100
                                <config-property name="queueManager">
                                    BRD3
                                <config-property name="port">
                                    1415
                            <connection-definition class-name="com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl" jndi-name="java:/jms/SiapxConnectionFactory" enabled="true" pool-name="java:/jms/SiapxConnectionFactory">
                                <config-property name="channel">
                                    SIFEC.SVRCONN
                                <config-property name="hostName">
                                    10.192.224.100
                                <config-property name="queueManager">
                                    BRD3
                                <config-property name="port">
                                    1415
                            <connection-definition class-name="com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl" jndi-name="java:/jms/SiempConnectionFactory" pool-name="SiempConnectionFactory">
                                <config-property name="channel">
                                    SIEMP.SVRCONN
                                <config-property name="hostName">
                                    10.192.224.100
                                <config-property name="queueManager">
                                    BRD3
                                <config-property name="port">
                                    1415
                            <connection-definition class-name="com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl" jndi-name="java:/jms/SiricConnectionFactory" enabled="true" pool-name="java:/jms/SiricConnectionFactory">
                                <config-property name="channel">
                                    SIFEC.SVRCONN
                                <config-property name="hostName">
                                    10.192.224.100
                                <config-property name="queueManager">
                                    BRD3
                                <config-property name="port">
                                    1415
                            <connection-definition class-name="com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl" jndi-name="java:/jms/SiapxConnectionFactoryFCE" enabled="true" pool-name="java:/jms/SiapxConnectionFactoryFCE">
                                <config-property name="channel">
                                    SIFEC.SVRCONN
                                <config-property name="hostName">
                                    10.192.224.100
                                <config-property name="queueManager">
                                    BRD7
                                <config-property name="port">
                                    1416
                            <connection-definition class-name="com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl" jndi-name="java:/jms/SiccrConnectionFactory" pool-name="SiccrConnectionFactory">
                                <config-property name="channel">
                                    SICCR.SVRCONN
                                <config-property name="hostName">
                                    10.192.224.100
                                <config-property name="queueManager">
                                    BRD3
                                <config-property name="port">
                                    1415
                            <connection-definition class-name="com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl" jndi-name="java:/jms/SinceConnectionFactory" pool-name="java:/jms/SinceConnectionFactory">
                                <config-property name="channel">
                                    SINCE.SVRCONN
                                <config-property name="hostName">
                                    10.192.224.66
                                <config-property name="queueManager">
                                    QSDA
                                <config-property name="port">
                                    1420
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.REQ.CONSULTA_CLIENTE" pool-name="SIBAR.REQ.CONSULTA_CLIENTE">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/TRF.RSP.SIPGE" pool-name="TRF.RSP.SIPGE">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.RSP.CONSULTA_BENEFICIARIO_INSS" use-java-context="false" pool-name="java:/jms/SIBAR.RSP.CONSULTA_BENEFICIARIO_INSS">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIFEC.REQ.PORTAL" enabled="true" use-java-context="false" pool-name="java:/jms/SIFEC.REQ.PORTAL">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.REQ.RELATORIO_AVALIACAO_RISCO" pool-name="SIBAR.REQ.RELATORIO_AVALIACAO_RISCO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.REQ.PESQUISA_CADASTRAL" pool-name="SIBAR.REQ.PESQUISA_CADASTRAL">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SICCR.RSP.CREDITO" use-java-context="false" pool-name="java:/jms/SICCR.RSP.CREDITO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.REQ.CANCELAMENTO_AVALIACAO_RISCO" pool-name="SIBAR.REQ.CANCELAMENTO_AVALIACAO_RISCO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.RSP.ORQUESTRACAO_MENSAGEM" pool-name="SIBAR.RSP.ORQUESTRACAO_MENSAGEM">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.REQ.DESBLOQUEIO_ALCADA" enabled="true" use-java-context="false" pool-name="SIBAR.REQ.DESBLOQUEIO_ALCADA">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SINCE.RSP.CONSULTA_CONTRATO" pool-name="SINCE.RSP.CONSULTA_CONTRATO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.RSP.CONSULTA_CLIENTE" pool-name="SIBAR.RSP.CONSULTA_CLIENTE">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SINCE.REQ.CONSULTA_CONTRATO" pool-name="SINCE.REQ.CONSULTA_CONTRATO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/TRF.RSP.ITRF01" pool-name="TRF.RSP.ITRF01">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SICCR.REQ.CREDITO" use-java-context="false" pool-name="java:/jms/SICCR.REQ.CREDITO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIRUR.RSP.AVALIACAO_RISCO_CREDITO" pool-name="SIRUR.RSP.AVALIACAO_RISCO_CREDITO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SICCR.REQ.MCONTAB" pool-name="SICCR.REQ.MCONTAB">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.RSP.DESBLOQUEIO_ALCADA" enabled="true" use-java-context="false" pool-name="SIBAR.RSP.DESBLOQUEIO_ALCADA">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/LQ.RSP.SIRUR.AVALIACAO_RISCO_CREDITO" pool-name="LQ.RSP.SIRUR.AVALIACAO_RISCO_CREDITO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.RSP.MANUTENCAO_CLIENTE" pool-name="SIBAR.RSP.MANUTENCAO_CLIENTE">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIAPX.REQ.CONSIGNACAO" enabled="true" use-java-context="false" pool-name="java:/jms/SIAPX.REQ.CONSIGNACAO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SICCR.RSP.AVALIACAO_RISCO_CREDITO" pool-name="SICCR.RSP.AVALIACAO_RISCO_CREDITO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.RSP.PESQUISA_CADASTRAL" pool-name="SIBAR.RSP.PESQUISA_CADASTRAL">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.REQ.ORQUESTRACAO_MENSAGEM" pool-name="SIBAR.REQ.ORQUESTRACAO_MENSAGEM">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.RSP.CANCELAMENTO_AVALIACAO_RISCO" pool-name="SIBAR.RSP.CANCELAMENTO_AVALIACAO_RISCO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.REQ.MANUTENCAO_CLIENTE" pool-name="SIBAR.REQ.MANUTENCAO_CLIENTE">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.REQ.CONSULTA_BENEFICIARIO_INSS" use-java-context="false" pool-name="java:/jms/SIBAR.REQ.CONSULTA_BENEFICIARIO_INSS">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIFEC.RSP.PORTAL" enabled="true" use-java-context="false" pool-name="java:/jms/SIFEC.RSP.PORTAL">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.RSP.CONSULTA_AVALIACAO_RISCO" enabled="true" use-java-context="false" pool-name="java:/jms/SIBAR.RSP.CONSULTA_AVALIACAO_RISCO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIAPX.RSP.AVALIACAO_RISCO_CREDITO" enabled="true" use-java-context="false" pool-name="SIAPX.RSP.AVALIACAO_RISCO_CREDITO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIEMP.RSP.AVALIACAO_RISCO_CREDITO" pool-name="SIEMP.RSP.AVALIACAO_RISCO_CREDITO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.REQ.AVALIACAO_RISCO_CREDITO" pool-name="SIBAR.REQ.AVALIACAO_RISCO_CREDITO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.RSP.RELATORIO_AVALIACAO_RISCO" pool-name="SIBAR.RSP.RELATORIO_AVALIACAO_RISCO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.REQ.CONSULTA_AVALIACAO_RISCO" enabled="true" use-java-context="false" pool-name="java:/jms/SIBAR.REQ.CONSULTA_AVALIACAO_RISCO">
                                <config-property name="baseQueueName">
                            <admin-object class-name="com.ibm.mq.connector.outbound.MQQueueProxy" jndi-name="java:/jms/SIBAR.RSP.AVALIACAO_RISCO_PROTOCOLO" pool-name="SIBAR.RSP.AVALIACAO_RISCO_PROTOCOLO">
                                <config-property name="baseQueueName">
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
