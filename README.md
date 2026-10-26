
[p585600@caddeapllx2695 ~]$ grep -r -i "trustStorePassword\|keyStorePassword\|storepass" /opt/ctmage/ctm/cm/AI/ 2>/dev/null
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$ cat /opt/ctmage/ctm/cm/AI/exe/cm_container 2>/dev/null
#!/bin/sh

current_dir=`pwd`
utl_path=`which $0`
utl_dir=`dirname $utl_path`
rc=0
JAR_NAME='javapasswordsdk.jar'
AGENT_DIR=/opt/ctmage/ctm
CM_VERSION=921300

CM_NAME=`cat $utl_dir/cm_name.txt`
CM_HOME="$AGENT_DIR/cm/$CM_NAME"
CM_JAR_NAME=cm$CM_NAME-$CM_VERSION.jar

. $utl_dir/set_cm_java.sh
export cm_java

# Handle heap size. Based on sapcmbe
# TODO: add the auto-increase mechanism
XMS=512
XMX_DEFAULT=1024
XMX=$XMX_DEFAULT
TRUSTSTORE="-Djavax.net.ssl.trustStore="$CM_HOME/data/security/apcerts""
KEYSTORE="-Djavax.net.ssl.keyStore="$CM_HOME/data/security/apks""
REMOTE_CONNECT="-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=*:6006"
jvm_mem_args="-Xms${XMS}m -Xmx${XMX}m -XX:-ExitOnOutOfMemoryError -XX:+HeapDumpOnOutOfMemoryError -XX:+UseStringDeduplication"

# SaaS arguments
SAAS_PARAMS=""
IS_SAAS=`$AGENT_DIR/exe/ctmagenv SaaS | grep SaaS | cut -d " " -f2`
if [ "$IS_SAAS" = on ] ; then
   SAAS_PARAMS="-Dsaas.config.file=$CM_HOME/data/saas/config.properties -Dsaas.metrics.file=$CM_HOME/data/saas/metrics.properties"
fi

#JVM_PARAMS="-DappName=$CM_NAME -DcmVer=$CM_VERSION -Dagent.logs="$AGENT_DIR/proclog" -Dcm.home="$CM_HOME" $SAAS_PARAMS --add-opens java.base/java.lang=ALL-UNNAMED"
JVM_PARAMS="-DappName=$CM_NAME -DcmVer=$CM_VERSION -Dagent.logs="$AGENT_DIR/proclog" -Dcm.home="$CM_HOME" $SAAS_PARAMS -Dlog4j2.configurationFile=$CM_HOME/data/log4j2.xml --add-opens java.base/java.lang=ALL-UNNAMED -Dlog4j2.isThreadContextMapInheritable=true"
CLASSPATH="$CM_HOME/exe/jars/*:$CM_HOME/exe/$CM_JAR_NAME"
MAIN_CLASS="com.bmc.cm.ServerActions"
. $utl_dir/setVaultSdkPath.sh
export sdk_path
if [ -n "$sdk_path" ]; then
    CLASSPATH="$sdk_path/$JAR_NAME:$CLASSPATH"
fi

$cm_java $JVM_PARAMS ${jvm_mem_args} $TRUSTSTORE $KEYSTORE -classpath $CLASSPATH $MAIN_CLASS "$@" >&2
rc=$?

cd $current_dir
exit $rc
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$
[p585600@caddeapllx2695 ~]$ find /opt/ctmage/ctm/cm/AI -iname "*.properties" -o -iname "*.conf" -o -iname "*.cfg" 2>/dev/null
/opt/ctmage/ctm/cm/AI/data/saas/metrics.properties
/opt/ctmage/ctm/cm/AI/data/saas/config.properties
/opt/ctmage/ctm/cm/AI/data/vault.properties
/opt/ctmage/ctm/cm/AI/data/one_params.properties
/opt/ctmage/ctm/cm/AI/ipp/data_masters/one_params.properties
[p585600@caddeapllx2695 ~]$
