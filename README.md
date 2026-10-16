
p585600@10.116.83.19's password:
Last login: Mon Jun  8 14:58:51 2026 from 10.122.150.31
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$ hostname -i
10.116.83.19
-sh-4.1$ hostname -f
sctdeapllx0018.df.caixa
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$ ps -ef | grep sigct
p585600  31417 31383  0 13:08 pts/1    00:00:00 grep sigct
-sh-4.1$ ps -ef | grep jboss
root      8020     1  0 Aug07 ?        00:00:00 su - jboss -c LAUNCH_JBOSS_IN_BACKGROUND=1 JBOSS_PIDFILE=/opt/EAP-6.4.0/lock/lock.file /opt/EAP-6.4.0/bin/standalone.sh -Djboss.bind.address.management=0.0.0.0 -Djboss.bind.address=0.0.0.0
jboss     8023  8020  0 Aug07 ?        00:00:00 /bin/sh /opt/EAP-6.4.0/bin/standalone.sh -Djboss.bind.address.management=0.0.0.0 -Djboss.bind.address=0.0.0.0
jboss    21461  8023  0 Oct15 ?        00:05:33 /usr/lib/jvm/openjdk-8/bin/java -D[Standalone] -server -XX:+UseCompressedOops -verbose:gc -Xloggc:/opt/EAP-6.4.0/standalone/log/gc.log -XX:+PrintGCDetails -XX:+PrintGCDateStamps -XX:+UseGCLogFileRotation -XX:NumberOfGCLogFiles=5 -XX:GCLogFileSize=3M -XX:-TraceClassUnloading -Xms2048m -Xmx2048m -XX:MaxPermSize=512m -Djava.net.preferIPv4Stack=false -Djava.net.preferIPv6Addresses=true -Djboss.modules.system.pkgs=org.jboss.byteman -Djava.awt.headless=true -Djboss.modules.policy-permissions=true -Dorg.jboss.boot.log.file=/opt/EAP-6.4.0/standalone/log/server.log -Dlogging.configuration=file:/opt/EAP-6.4.0/standalone/configuration/logging.properties -jar /opt/EAP-6.4.0/jboss-modules.jar -mp /opt/EAP-6.4.0/modules -jaxpmodule javax.xml.jaxp-provider org.jboss.as.standalone -Djboss.home.dir=/opt/EAP-6.4.0 -Djboss.server.base.dir=/opt/EAP-6.4.0/standalone -Djboss.bind.address.management=0.0.0.0 -Djboss.bind.address=0.0.0.0
p585600  31420 31383  0 13:09 pts/1    00:00:00 grep jboss
-sh-4.1$ ps -ef | grep java
jboss    21461  8023  0 Oct15 ?        00:05:33 /usr/lib/jvm/openjdk-8/bin/java -D[Standalone] -server -XX:+UseCompressedOops -verbose:gc -Xloggc:/opt/EAP-6.4.0/standalone/log/gc.log -XX:+PrintGCDetails -XX:+PrintGCDateStamps -XX:+UseGCLogFileRotation -XX:NumberOfGCLogFiles=5 -XX:GCLogFileSize=3M -XX:-TraceClassUnloading -Xms2048m -Xmx2048m -XX:MaxPermSize=512m -Djava.net.preferIPv4Stack=false -Djava.net.preferIPv6Addresses=true -Djboss.modules.system.pkgs=org.jboss.byteman -Djava.awt.headless=true -Djboss.modules.policy-permissions=true -Dorg.jboss.boot.log.file=/opt/EAP-6.4.0/standalone/log/server.log -Dlogging.configuration=file:/opt/EAP-6.4.0/standalone/configuration/logging.properties -jar /opt/EAP-6.4.0/jboss-modules.jar -mp /opt/EAP-6.4.0/modules -jaxpmodule javax.xml.jaxp-provider org.jboss.as.standalone -Djboss.home.dir=/opt/EAP-6.4.0 -Djboss.server.base.dir=/opt/EAP-6.4.0/standalone -Djboss.bind.address.management=0.0.0.0 -Djboss.bind.address=0.0.0.0
p585600  31422 31383  0 13:09 pts/1    00:00:00 grep java
-sh-4.1$
