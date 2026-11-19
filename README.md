@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]# timeout 5 bash -c "cat < /dev/null > /dev/tcp/10.116.89.101/8111" && echo "0039 ABRIU 101:8111" || echo "0039 SEM CONEXAO 101:8111"
0039 ABRIU 101:8111
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]# cd /tmp && rm -rf sirotjar && unzip -o $B/deployapp/sirotconEjb_v2.2.7.jar -d /tmp/sirotjar >/dev/null 2>&1
[root@sspdeapllx0039 tmp]# find /tmp/sirotjar -name "*.properties" -exec echo "== {} ==" \; -exec cat {} \;
== /tmp/sirotjar/cefsirot2con.properties ==
PROJECT_NAME=Helperclass CEFSirotCon
PROJECT_VERSION=v2.2.4
LOG_STATISTICS=true
RAJADA_LENIENTE=false
REDE_TRANSMISSORA=7999
DEFAULT_TIMEOUT=30000
RECONECTAR_A_CADA=50
<!--SERVER=10.192.227.38-->
SERVER=localhost
<!--SERVER=10.192.228.120-->
PORT=8111
<!--PORT=8111-->
SO_LINGER=0
MANTEM_CONEXAO=false
<!--LOG4J_CONFIG_FILE=/log_ias/config-log4j/sirot2/sirot2-{IAS.INSTANCE}.xml -->
LOG4J_CONFIG_FILE=/log_jboss/config-log4j/sirot2/sirot2.xml
LOG_LEVEL=1
LOG_CONSOLE=true

== /tmp/sirotjar/ceflog2.properties ==
ARQUIVO_CONFIGURACAO_LOG4J=/log_jboss/config-log4j/sirot2/sirot2.xml[root@sspdeapllx0039 tmp]# grep -rniE "8111|8[0-9]{3}|10\.116\.|host|ip|farm|siper|conector" /tmp/sirotjar 2>/dev/null | grep -viE "class|META-INF|password" | head -20
Binary file /tmp/sirotjar/log4j-1.2.8.jar matches
/tmp/sirotjar/cefsirot2con.properties:9:SERVER=localhost
/tmp/sirotjar/cefsirot2con.properties:11:PORT=8111
/tmp/sirotjar/cefsirot2con.properties:12:<!--PORT=8111-->
Binary file /tmp/sirotjar/ceflib2.0.5.jar matches
[root@sspdeapllx0039 tmp]#
[root@sspdeapllx0039 tmp]#
[root@sspdeapllx0039 tmp]#
[root@sspdeapllx0039 tmp]# find / -iname "*sirot*" 2>/dev/null | grep -viE "/proc/|\.class" | head
/opt/jboss/jboss-5.1.0.GA/server/sigsj_boleto/deployapp/sirotconEjb_v2.2.7.jar
/opt/jboss/jboss-5.1.0.GA/server/sigsj_boleto/tmp/a382g2o-yibr8q-mvscq520-1-mvscqf2n-a2/boletoService-war-2.2.1.war/WEB-INF/classes/br/gov/caixa/sigsj/boletoservice/dao/sirot
/opt/jboss/jboss-5.1.0.GA/server/sigsj_boleto/tmp/a382g2o-yibr8q-mvscq520-1-mvscqf2n-a2/boletoService-war-2.2.1.war/WEB-INF/classes/br/gov/caixa/sigsj/boletoservice/common/sirot
/opt/jboss/jboss-5.1.0.GA/server/sigsj_boleto/tmp/a382g2o-yibr8q-mvscq520-1-mvscqf2n-a2/boletoService-war-2.2.1.war/WEB-INF/classes/br/gov/caixa/sigsj/boletoservice/common/transaction/sirot
/opt/jboss/jboss-5.1.0.GA/server/sigsj_boleto/tmp/a382g2o-yibr8q-mvscq520-1-mvscqf2n-a2/boletoService-war-2.2.1.war/WEB-INF/classes/br/gov/caixa/sigsj/boletoservice/transaction/sirot
/opt/jboss/jboss-5.1.0.GA/server/backup/sigsj_boleto/deployapp/sirotconEjb_v2.2.7.jar
/opt/jboss/jboss-5.1.0.GA/server/backup/sicuc_inter/deployapp/sirotconEjb_v2.2.7.jar
/opt/jboss/jboss-5.1.0.GA/server/backup/sigsj_intranet/deployapp/sirotconEjb_v2.2.7.jar
/opt/jboss/jboss-5.1.0.GA/server/backup/sigsj_internet/deployapp/sirotconEjb_v2.2.7.jar
/opt/jboss/jboss-5.1.0.GA/server/backup/sigsj_inter01_bkp.20180430/deployapp/sirotconEjb_v2.2.7.jar
[root@sspdeapllx0039 tmp]# cat /apl/sigsj/properties/*.properties 2>/dev/null | grep -iE "siper|sirot|farm|conector|8111|10\.116\.89\.101"
[root@sspdeapllx0039 tmp]#
[root@sspdeapllx0039 tmp]#
[root@sspdeapllx0039 tmp]#
[root@sspdeapllx0039 tmp]#
