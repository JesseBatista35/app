standalone.conf  SICOW-conres-okd-config


## -*- shell-script -*- ######################################################
##                                                                          ##
##  JBoss EAP Bootstrap Script Configuration                                ##
##                                                                          ##
##############################################################################
#
# This file is optional; it may be removed if not needed.
#

#
# Specify the maximum file descriptor limit, use "max" or "maximum" to use
# the default, as queried by the system.
#
# Defaults to "maximum"
#
#MAX_FD="maximum"

#
# Specify the profiler configuration file to load.
#
# Default is to not load profiler configuration file.
#
#PROFILER=""

#
# Specify the location of the Java home directory.  If set then $JAVA will
# be defined to $JAVA_HOME/bin/java, else $JAVA will be "java".
#
#JAVA_HOME="/opt/java/jdk"

#
# Specify the exact Java VM executable to use.
#
#JAVA=""

if [ "x$JBOSS_MODULES_SYSTEM_PKGS" = "x" ]; then
  $JBOSS_MODULES_SYSTEM_PKGS="org.jboss.byteman"
fi

# Uncomment the following line to prevent manipulation of JVM options
# by shell scripts.
#
#PRESERVE_JAVA_OPTS=true

#
# Specify options to pass to the Java VM.
#
if [ "x$JAVA_OPTS" = "x" ]; then
   JAVA_OPTS="-Xms__JVM_HEAP_MIN__ -Xmx__JVM_HEAP_MAX__ -XX:MetaspaceSize=__JVM_METASPACE_MIN__ -XX:MaxMetaspaceSize=__JVM_METASPACE_MAX__ -Djava.net.preferIPv4Stack=true"
   JAVA_OPTS="$JAVA_OPTS -Djboss.modules.system.pkgs=$JBOSS_MODULES_SYSTEM_PKGS -Djava.awt.headless=true"
   JAVA_OPTS="$JAVA_OPTS -Djavax.net.ssl.trustStore=$JBOSS_HOME/standalone/configuration/__JKS_FILE__ -Djavax.net.ssl.trustStorePassword=__PASSWORD_TRUSTSTORE__"
   JAVA_OPTS="$JAVA_OPTS -Dhttps.proxyHost=__JVM_PROXY_HOST__ -Dhttps.proxyPort=__JVM_PROXY_PORT__ -Dhttp.proxyHost=__JVM_PROXY_HOST__ -Dhttp.proxyPort=__JVM_PROXY_PORT__ -Dhttp.nonProxyHosts=*.caixa"
   JAVA_OPTS="$JAVA_OPTS -Djboss.modules.policy-permissions=true"
   JAVA_OPTS="$JAVA_OPTS -server -XX:+ExplicitGCInvokesConcurrent -XX:+UseG1GC -XX:MaxGCPauseMillis=500"
   JAVA_OPTS="$JAVA_OPTS -Xbootclasspath/p:$JBOSS_HOME/modules/system/layers/base/org/wildfly/common/main/wildfly-common-1.5.4.Final-redhat-00001.jar"
   JAVA_OPTS="$JAVA_OPTS -Xbootclasspath/p:$JBOSS_HOME/modules/system/layers/base/org/jboss/logmanager/main/jboss-logmanager-2.1.18.Final-redhat-00001.jar"   
   JAVA_OPTS="$JAVA_OPTS -Djboss.modules.system.pkgs=org.jboss.byteman,org.jboss.logmanager"
   JAVA_OPTS="$JAVA_OPTS -Djava.util.logging.manager=org.jboss.logmanager.LogManager"   
   JAVA_OPTS="$JAVA_OPTS -javaagent:/opt/jmx_exporter/jmx_prometheus.jar=8778:/opt/jmx_exporter/jmx_prometheus.yaml"
#  JAVA_OPTS="$JAVA_OPTS -javaagent:/opt/apm_agent/elastic-apm-agent.jar -Delastic.apm.config_file=/opt/apm_agent/elasticapm.properties -Delastic.apm.service_name=__SistemaNome__ -Delastic.apm.environment=__SistemaAmbiente__ -Delastic.apm.application_packages=br.gov.caixa -Delastic.apm.server_urls=__URL_APM_SERVER__ -Delastic.apm.global_labels=deployment=__DEPLOYMENT__"
   JAVA_OPTS="$JAVA_OPTS -javaagent:$JBOSS_HOME/standalone/deployments/applicationinsights-agent-3.7.1.jar"
#  JAVA_OPTS="$JAVA_OPTS -javaagent:$JBOSS_HOME/standalone/deployments/applicationinsights-agent.jar"
else
   echo "JAVA_OPTS already set in environment; overriding default settings with values: $JAVA_OPTS"
fi

# Sample JPDA settings for remote socket debugging
#JAVA_OPTS="$JAVA_OPTS -agentlib:jdwp=transport=dt_socket,address=8787,server=y,suspend=n"

# Sample JPDA settings for shared memory debugging
#JAVA_OPTS="$JAVA_OPTS -agentlib:jdwp=transport=dt_shmem,server=y,suspend=n,address=jboss"

# Uncomment to not use JBoss Modules lockless mode
#JAVA_OPTS="$JAVA_OPTS -Djboss.modules.lockless=false"

# Uncomment to gather JBoss Modules metrics
#JAVA_OPTS="$JAVA_OPTS -Djboss.modules.metrics=true"

# Uncomment this to run with a security manager enabled
# SECMGR="true"

# Uncomment this in order to be able to run WildFly on FreeBSD
# when you get "epoll_create function not implemented" message in dmesg output
#JAVA_OPTS="$JAVA_OPTS -Djava.nio.channels.spi.SelectorProvider=sun.nio.ch.PollSelectorProvider"

# Use system or custom proxies, but not BOTH.
JAVA_OPTS="$JAVA_OPTS -Djava.net.useSystemProxies=false"

# CUSTOM Proxies.
JAVA_OPTS="$JAVA_OPTS -Dhttp.proxyHost=__JVM_PROXY_HOST__"
JAVA_OPTS="$JAVA_OPTS -Dhttp.proxyPort=__JVM_PROXY_PORT__"
JAVA_OPTS="$JAVA_OPTS -Dhttps.proxyHost=__JVM_PROXY_HOST__"
JAVA_OPTS="$JAVA_OPTS -Dhttps.proxyPort=__JVM_PROXY_PORT__"
JAVA_OPTS="$JAVA_OPTS -Dhttp.nonProxyHosts=localhost\|127.0.0.1\|*.caixa"

export https_proxy=__JVM_PROXY_HOST__:__JVM_PROXY_PORT__
export http_proxy=__JVM_PROXY_HOST__:__JVM_PROXY_PORT__

# proxydes.caixa = ip 10.252.32.65

# enable garbage collection logging if not set in environment differently
if [ "x$GC_LOG" = "x" ]; then
   GC_LOG="true"
else
   echo "GC_LOG set in environment to $GC_LOG"
fi



standalone.conf   SICOW-penhor-okd-config

## -*- shell-script -*- ######################################################
##                                                                          ##
##  JBoss EAP Bootstrap Script Configuration                                ##
##                                                                          ##
##############################################################################
#
# This file is optional; it may be removed if not needed.
#

#
# Specify the maximum file descriptor limit, use "max" or "maximum" to use
# the default, as queried by the system.
#
# Defaults to "maximum"
#
#MAX_FD="maximum"

#
# Specify the profiler configuration file to load.
#
# Default is to not load profiler configuration file.
#
#PROFILER=""

#
# Specify the location of the Java home directory.  If set then $JAVA will
# be defined to $JAVA_HOME/bin/java, else $JAVA will be "java".
#
#JAVA_HOME="/opt/java/jdk"

#
# Specify the exact Java VM executable to use.
#
#JAVA=""

if [ "x$JBOSS_MODULES_SYSTEM_PKGS" = "x" ]; then
   JBOSS_MODULES_SYSTEM_PKGS="org.jboss.byteman"
fi

# Uncomment the following line to prevent manipulation of JVM options
# by shell scripts.
#
#PRESERVE_JAVA_OPTS=true

#
# Specify options to pass to the Java VM.
#
if [ "x$JAVA_OPTS" = "x" ]; then
   JAVA_OPTS="-Xms__JVM_HEAP_MIN__ -Xmx__JVM_HEAP_MAX__ -XX:MetaspaceSize=__JVM_METASPACE_MIN__ -XX:MaxMetaspaceSize=__JVM_METASPACE_MAX__ -Djava.net.preferIPv4Stack=true"
   JAVA_OPTS="$JAVA_OPTS -Djboss.modules.system.pkgs=$JBOSS_MODULES_SYSTEM_PKGS -Djava.awt.headless=true"
   JAVA_OPTS="$JAVA_OPTS -Djavax.net.ssl.trustStore=$JBOSS_HOME/standalone/configuration/__JKS_FILE__ -Djavax.net.ssl.trustStorePassword=__PASSWORD_TRUSTSTORE__"
   JAVA_OPTS="$JAVA_OPTS -Dhttps.proxyHost=__JVM_PROXY_HOST__ -Dhttps.proxyPort=__JVM_PROXY_PORT__ -Dhttp.proxyHost=__JVM_PROXY_HOST__ -Dhttp.proxyPort=__JVM_PROXY_PORT__ -Dhttp.nonProxyHosts=*.caixa"
   JAVA_OPTS="$JAVA_OPTS -Djboss.modules.policy-permissions=true"
   JAVA_OPTS="$JAVA_OPTS -server -XX:+ExplicitGCInvokesConcurrent -XX:+UseG1GC -XX:MaxGCPauseMillis=500"
   JAVA_OPTS="$JAVA_OPTS -Xbootclasspath/p:$JBOSS_HOME/modules/system/layers/base/org/wildfly/common/main/wildfly-common-1.5.4.Final-redhat-00001.jar"
   JAVA_OPTS="$JAVA_OPTS -Xbootclasspath/p:$JBOSS_HOME/modules/system/layers/base/org/jboss/logmanager/main/jboss-logmanager-2.1.18.Final-redhat-00001.jar"   
   JAVA_OPTS="$JAVA_OPTS -Djboss.modules.system.pkgs=org.jboss.byteman,org.jboss.logmanager"
   JAVA_OPTS="$JAVA_OPTS -Djava.util.logging.manager=org.jboss.logmanager.LogManager"   
   JAVA_OPTS="$JAVA_OPTS -javaagent:/opt/jmx_exporter/jmx_prometheus.jar=8778:/opt/jmx_exporter/jmx_prometheus.yaml"
#  JAVA_OPTS="$JAVA_OPTS -javaagent:/opt/apm_agent/elastic-apm-agent.jar -Delastic.apm.config_file=/opt/apm_agent/elasticapm.properties -Delastic.apm.service_name=__SistemaNome__ -Delastic.apm.environment=__SistemaAmbiente__ -Delastic.apm.application_packages=br.gov.caixa -Delastic.apm.server_urls=__URL_APM_SERVER__ -Delastic.apm.global_labels=deployment=__DEPLOYMENT__"
   JAVA_OPTS="$JAVA_OPTS -javaagent:$JBOSS_HOME/standalone/deployments/applicationinsights-agent-3.7.1.jar"
#  JAVA_OPTS="$JAVA_OPTS -javaagent:$JBOSS_HOME/standalone/deployments/applicationinsights-agent.jar"
else
   echo "JAVA_OPTS already set in environment; overriding default settings with values: $JAVA_OPTS"
fi

# Sample JPDA settings for remote socket debugging
#JAVA_OPTS="$JAVA_OPTS -agentlib:jdwp=transport=dt_socket,address=8787,server=y,suspend=n"

# Sample JPDA settings for shared memory debugging
#JAVA_OPTS="$JAVA_OPTS -agentlib:jdwp=transport=dt_shmem,server=y,suspend=n,address=jboss"

# Uncomment to not use JBoss Modules lockless mode
#JAVA_OPTS="$JAVA_OPTS -Djboss.modules.lockless=false"

# Uncomment to gather JBoss Modules metrics
#JAVA_OPTS="$JAVA_OPTS -Djboss.modules.metrics=true"

# Uncomment this to run with a security manager enabled
# SECMGR="true"

# Uncomment this in order to be able to run WildFly on FreeBSD
# when you get "epoll_create function not implemented" message in dmesg output
#JAVA_OPTS="$JAVA_OPTS -Djava.nio.channels.spi.SelectorProvider=sun.nio.ch.PollSelectorProvider"

# Use system or custom proxies, but not BOTH.
JAVA_OPTS="$JAVA_OPTS -Djava.net.useSystemProxies=false"

# CUSTOM Proxies.
JAVA_OPTS="$JAVA_OPTS -Dhttp.proxyHost=__JVM_PROXY_HOST__"
JAVA_OPTS="$JAVA_OPTS -Dhttp.proxyPort=__JVM_PROXY_PORT__"
JAVA_OPTS="$JAVA_OPTS -Dhttps.proxyHost=__JVM_PROXY_HOST__"
JAVA_OPTS="$JAVA_OPTS -Dhttps.proxyPort=__JVM_PROXY_PORT__"
JAVA_OPTS="$JAVA_OPTS -Dhttp.nonProxyHosts=localhost\|127.0.0.1\|*.caixa"

export https_proxy=__JVM_PROXY_HOST__:__JVM_PROXY_PORT__
export http_proxy=__JVM_PROXY_HOST__:__JVM_PROXY_PORT__

# proxydes.caixa = ip 10.252.32.65

# enable garbage collection logging if not set in environment differently
if [ "x$GC_LOG" = "x" ]; then
   GC_LOG="true"
else
   echo "GC_LOG set in environment to $GC_LOG"
fi
