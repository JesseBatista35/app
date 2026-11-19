[root@sspdeapllx0039 lib]# B=/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]# grep -rniE "siper|sirot|farm|connector|host|porta|8111|conexao" $B/deployapp $B/conf 2>/dev/null | grep -viE "password|senha" | head -30
Binary file /opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/deployapp/sirotconEjb_v2.2.7.jar matches
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/jboss-service.xml:107:      | events you can have a quick view of important system faults.
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/jboss-service.xml:159:      <!--  The address to use for the host portion of the RMI codebase URL -->
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/jboss-service.xml:160:      <attribute name="Host">${java.rmi.server.hostname}</attribute>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/jbossts-properties.xml:174:        IMPORTANT: make sure the directory is lockable, e.g., /tmp on Unix
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/jbossts-properties.xml:315:        The default behaviour is to use the loopback address (ie localhost).
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/jboss-log4j.xml_bkp:98:     <param name="To" value="admin@myhost.domain.com"/>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/jboss-log4j.xml_bkp:99:     <param name="From" value="nobody@myhost.domain.com"/>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/jboss-log4j.xml_bkp:101:     <param name="SMTPHost" value="localhost"/>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/jboss-log4j.xml_bkp:114:     <param name="SyslogHost" value="localhost"/>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/jboss-log4j.xml_bkp:134:     <param name="ManagementHost" value="127.0.0.1"/>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/jboss-log4j.xml_bkp:135:     <param name="ManagementHostTrapListenPort" value="162"/>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:48:         <!-- Default host name -->
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:62:         <!-- Default host name -->
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:76:         <!-- Default host name -->
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:90:         <!-- Default host name -->
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:128:            <!-- Remoting Connector -->
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:130:               <property name="serviceName">UnifiedInvokerConnector</property>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:132:               <property name="description">Socket for JBoss Remoting Connector used by UnifiedInvoker</property>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:138:               <property name="serviceName">UnifiedInvokerConnector:bindingHome1</property>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:141:               <property name="description">Socket for JBoss Remoting Connector used by UnifiedInvoker on a multihome server</property>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:147:               <property name="serviceName">UnifiedInvokerConnector:bindingHome2</property>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:150:               <property name="description">Socket for JBoss Remoting Connector used by UnifiedInvoker on a multihome server</property>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:188:               <property name="hostName">${jboss.partition.udpGroup:230.0.0.4}</property>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:194:               <property name="fixedHostName">true</property>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:203:               <property name="hostName">${jboss.bind.address}</property>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:250:               <property name="serviceName">jboss.remoting:service=JMXConnectorServer,protocol=rmi</property>
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:255:            <!-- ********************* deploy/ejb3-connectors-service.xml **************** -->
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:258:                 dynamically.  See the value-factory usage in deploy/ejb3-connectors-service.xml -->
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/bindingservice.beans/META-INF/bindings-jboss-beans.xml:268:                anything else that needs to point to the JBoss Web HTTP connector
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]# find /apl/sigsj $B -name "*.properties" 2>/dev/null | xargs grep -liE "siper|sirot|farm|host" 2>/dev/null
[root@sspdeapllx0039 lib]#




[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
^C
[root@caddeapllx2854 ~]#
^C
[root@caddeapllx2854 ~]# grep -n "CONNECTOR-FARM" /opt/jboss-eap/standalone/configuration/standalone-full-ha.xml
43:        <property name="CONNECTOR-FARM-HOST" value="10.116.89.101"/>
44:        <property name="CONNECTOR-FARM-PORT" value="8111"/>
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# timeout 5 bash -c "cat < /dev/null > /dev/tcp/$HOST/$PORT" && echo "ABRIU $HOST:$PORT" || echo "SEM CONEXAO $HOST:$PORT"
bash: linha 1: : Nome ou serviço desconhecido
bash: linha 1: /dev/tcp//: Argumento inválido
SEM CONEXAO :
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#

