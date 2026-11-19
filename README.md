
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]# grep -rl "SIGSJ04" / --include=*-ds.xml --include=login-config.xml --include=*.xml 2>/dev/null | grep -v "/proc/" | head
/opt/jboss/jboss-5.1.0.GA/server/backup/sigsj_internet/conf/login-config.xml
/opt/jboss/jboss-5.1.0.GA/server/backup/sigsj_internet/deployapp/sigsj-oracle-ds.xml
/opt/jboss/jboss-5.1.0.GA/server/backup/sigsj_inter01_bkp.20180430/conf/login-config.xml
/opt/jboss/jboss-5.1.0.GA/server/backup/sigsj_inter01_bkp.20180430/deployapp/sigsj-oracle-ds.xml
/opt/jboss/jboss-5.1.0.GA/server/backup/sigsj_inter02_bkp.20180428/deployapp/sigsj-oracle-ds.xml
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/conf/login-config.xml
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/deployapp/sigsj-oracle-ds.xml
/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet/tmp/a382g2o-c29mdx-mwb397on-1-mwb39p2q-9w/sigsj_internet-war-2.73.0.10.war/WEB-INF/classes/META-INF/persistence.xml
/caixa/usr/c105762/sigsj-oracle-ds.xml
/caixa/usr/p984222/sigsj-oracle-ds.xml
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]# grep -n -i -B2 -A8 "SIGSJ04" <arquivo> | grep -iE "user|security-domain|application-policy|jndi|connection-url"
bash: syntax error near unexpected token `|'
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
