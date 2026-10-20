
sair
Connection to 10.116.201.25 closed.
[p585600@cadsvitrlx100 ~]$ ssh 10.116.195.93
p585600@10.116.195.93's password:
Permission denied, please try again.
p585600@10.116.195.93's password:
Last failed login: Tue Oct 20 16:07:51 -03 2026 from 10.122.150.31 on ssh:notty
There was 1 failed login attempt since the last successful login.
Last login: Tue Oct 20 11:38:59 2026 from 10.122.150.31
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ ls -la /opt/jboss-eap/standalone/deployments/ | grep -i sirot
ls: não é possível acessar /opt/jboss-eap/standalone/deployments/: Arquivo ou diretório não encontrado
-sh-4.2$
-sh-4.2$
-sh-4.2$ grep -n -i -A3 "sirot" /opt/jboss-eap/standalone/configuration/standalone*.xml
grep: /opt/jboss-eap/standalone/configuration/standalone*.xml: Arquivo ou diretório não encontrado
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ ls /opt/jboss-eap/standalone/data/content/
ls: não é possível acessar /opt/jboss-eap/standalone/data/content/: Arquivo ou diretório não encontrado
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ grep -nE "WFLYCTL0412|WFLYCTL0180" /logs/jboss/jboss-eap/standalone/sigsj-boleto/server.log | tail -10
grep: /logs/jboss/jboss-eap/standalone/sigsj-boleto/server.log: Arquivo ou diretório não encontrado
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ grep -nE "WFLYCTL0013|ERROR|Caused by" /logs/jboss/jboss-eap/standalone/sigsj-boleto/server.log | tail -40
grep: /logs/jboss/jboss-eap/standalone/sigsj-boleto/server.log: Arquivo ou diretório não encontrado
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ ps -ef | grep java
jboss      1503    937  9 16:04 ?        00:00:26 java -D[Standalone] -verbose:gc -Xloggc:/logs/jboss/jboss-eap/standalone/sigsj-internet/gc.log -XX:+PrintGCDetails -XX:+PrintGCDateStamps -XX:+UseGCLogFileRotation -XX:NumberOfGCLogFiles=5 -XX:GCLogFileSize=3M -XX:-TraceClassUnloading -Xms1024m -Xmx2048m -XX:MetaspaceSize=96M -XX:MaxMetaspaceSize=256m -Djava.net.preferIPv4Stack=true -Djboss.modules.system.pkgs=org.jboss.byteman -Djava.awt.headless=true -Djavax.net.ssl.trustStore=/opt/jboss/jboss-eap/standalone/configuration/certificados_caixa_completo_gsj_inter.jks -Djboss.modules.policy-permissions=true -server -XX:+ExplicitGCInvokesConcurrent -XX:+UseG1GC -XX:MaxGCPauseMillis=500 -Xbootclasspath/p:/opt/jboss/jboss-eap/modules/system/layers/base/org/jboss/logmanager/main/jboss-logmanager-2.0.7.Final-redhat-1.jar -Djboss.modules.system.pkgs=org.jboss.byteman,org.jboss.logmanager -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Dfile.encoding=ISO-8859-1 -javaagent:/opt/jmx_exporter/jmx_prometheus.jar=8778:/opt/jmx_exporter/jmx_prometheus.yaml -javaagent:/opt/apm_agent/elastic-apm-agent-1.15.0.jar -Delastic.apm.config_file=/opt/apm_agent/elasticapm-1.15.0.properties -Delastic.apm.service_name=sigsj-internet -Delastic.apm.environment=DES -Delastic.apm.application_packages=br.gov.caixa -Delastic.apm.server_urls=http://apm-server-devops.produtos.caixa -Delastic.apm.global_labels=deployment=sigsj-internet-backend-des-esteiras -Dorg.jboss.boot.log.file=/logs/jboss/jboss-eap/standalone/sigsj-internet/server.log -Dlogging.configuration=file:/opt/jboss/jboss-eap/standalone/configuration/logging.properties -jar /opt/jboss/jboss-eap/jboss-modules.jar -mp /opt/jboss/jboss-eap/modules org.jboss.as.standalone -Djboss.home.dir=/opt/jboss/jboss-eap -Djboss.server.base.dir=/opt/jboss/jboss-eap/standalone -b 10.116.195.93 -bmanagement 10.116.195.93 -bprivate 10.116.195.93 -Dhttp.modcluster.proxy1=10.116.223.231 -Dhttp.modcluster.proxy2=10.116.223.232 -Djboss_modcluster_proxy_list=caddeapllx135.extra.caixa.gov.br:6666,caddeapllx136.extra.caixa.gov.br:6666 -Djboss_modcluster_balancer=sigsj-internet -Djboss.cluster.tcp.initial_hosts=10.116.195.93[7600] -Djboss.node.name=caddeapllx1121 -Djboss.tx.node.id=caddeapllx1121 -u 230.0.0.4 -Djboss.server.base.dir=/opt/jboss/jboss-eap/standalone -Djboss.server.log.dir=/logs/jboss/jboss-eap/standalone/sigsj-internet -c standalone-full-ha.xml
p585600    5671   5640  0 16:09 pts/0    00:00:00 grep --color=auto java
-sh-4.2$ ps -ef | grep jboss
root        934      1  0 16:04 ?        00:00:00 runuser jboss -c LAUNCH_JBOSS_IN_BACKGROUND=1 JBOSS_PIDFILE=/opt/jboss/jboss-eap/standalone/tmp/jboss-eap-standalone.pid /opt/jboss/jboss-eap/bin/standalone.sh                -b 10.116.195.93                -bmanagement 10.116.195.93                -bprivate 10.116.195.93                                                -Dhttp.modcluster.proxy1=10.116.223.231                                 -Dhttp.modcluster.proxy2=10.116.223.232                                 -Djboss_modcluster_proxy_list="caddeapllx135.extra.caixa.gov.br:6666,caddeapllx136.extra.caixa.gov.br:6666"                -Djboss_modcluster_balancer=sigsj-internet                -Djboss.cluster.tcp.initial_hosts=10.116.195.93[7600]                -Djboss.node.name=caddeapllx1121                -Djboss.tx.node.id=caddeapllx1121                -u 230.0.0.4                                -Djboss.server.base.dir=/opt/jboss/jboss-eap/standalone                -Djboss.server.log.dir=/logs/jboss/jboss-eap/standalone/sigsj-internet -c standalone-full-ha.xml
jboss       937    934  0 16:04 ?        00:00:00 /bin/sh /opt/jboss/jboss-eap/bin/standalone.sh -b 10.116.195.93 -bmanagement 10.116.195.93 -bprivate 10.116.195.93 -Dhttp.modcluster.proxy1=10.116.223.231 -Dhttp.modcluster.proxy2=10.116.223.232 -Djboss_modcluster_proxy_list=caddeapllx135.extra.caixa.gov.br:6666,caddeapllx136.extra.caixa.gov.br:6666 -Djboss_modcluster_balancer=sigsj-internet -Djboss.cluster.tcp.initial_hosts=10.116.195.93[7600] -Djboss.node.name=caddeapllx1121 -Djboss.tx.node.id=caddeapllx1121 -u 230.0.0.4 -Djboss.server.base.dir=/opt/jboss/jboss-eap/standalone -Djboss.server.log.dir=/logs/jboss/jboss-eap/standalone/sigsj-internet -c standalone-full-ha.xml
jboss      1503    937  9 16:04 ?        00:00:26 java -D[Standalone] -verbose:gc -Xloggc:/logs/jboss/jboss-eap/standalone/sigsj-internet/gc.log -XX:+PrintGCDetails -XX:+PrintGCDateStamps -XX:+UseGCLogFileRotation -XX:NumberOfGCLogFiles=5 -XX:GCLogFileSize=3M -XX:-TraceClassUnloading -Xms1024m -Xmx2048m -XX:MetaspaceSize=96M -XX:MaxMetaspaceSize=256m -Djava.net.preferIPv4Stack=true -Djboss.modules.system.pkgs=org.jboss.byteman -Djava.awt.headless=true -Djavax.net.ssl.trustStore=/opt/jboss/jboss-eap/standalone/configuration/certificados_caixa_completo_gsj_inter.jks -Djboss.modules.policy-permissions=true -server -XX:+ExplicitGCInvokesConcurrent -XX:+UseG1GC -XX:MaxGCPauseMillis=500 -Xbootclasspath/p:/opt/jboss/jboss-eap/modules/system/layers/base/org/jboss/logmanager/main/jboss-logmanager-2.0.7.Final-redhat-1.jar -Djboss.modules.system.pkgs=org.jboss.byteman,org.jboss.logmanager -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Dfile.encoding=ISO-8859-1 -javaagent:/opt/jmx_exporter/jmx_prometheus.jar=8778:/opt/jmx_exporter/jmx_prometheus.yaml -javaagent:/opt/apm_agent/elastic-apm-agent-1.15.0.jar -Delastic.apm.config_file=/opt/apm_agent/elasticapm-1.15.0.properties -Delastic.apm.service_name=sigsj-internet -Delastic.apm.environment=DES -Delastic.apm.application_packages=br.gov.caixa -Delastic.apm.server_urls=http://apm-server-devops.produtos.caixa -Delastic.apm.global_labels=deployment=sigsj-internet-backend-des-esteiras -Dorg.jboss.boot.log.file=/logs/jboss/jboss-eap/standalone/sigsj-internet/server.log -Dlogging.configuration=file:/opt/jboss/jboss-eap/standalone/configuration/logging.properties -jar /opt/jboss/jboss-eap/jboss-modules.jar -mp /opt/jboss/jboss-eap/modules org.jboss.as.standalone -Djboss.home.dir=/opt/jboss/jboss-eap -Djboss.server.base.dir=/opt/jboss/jboss-eap/standalone -b 10.116.195.93 -bmanagement 10.116.195.93 -bprivate 10.116.195.93 -Dhttp.modcluster.proxy1=10.116.223.231 -Dhttp.modcluster.proxy2=10.116.223.232 -Djboss_modcluster_proxy_list=caddeapllx135.extra.caixa.gov.br:6666,caddeapllx136.extra.caixa.gov.br:6666 -Djboss_modcluster_balancer=sigsj-internet -Djboss.cluster.tcp.initial_hosts=10.116.195.93[7600] -Djboss.node.name=caddeapllx1121 -Djboss.tx.node.id=caddeapllx1121 -u 230.0.0.4 -Djboss.server.base.dir=/opt/jboss/jboss-eap/standalone -Djboss.server.log.dir=/logs/jboss/jboss-eap/standalone/sigsj-internet -c standalone-full-ha.xml
p585600    5675   5640  0 16:09 pts/0    00:00:00 grep --color=auto jboss
-sh-4.2$
-sh-4.2$
-sh-4.2$
