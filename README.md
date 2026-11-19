
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]# grep -n -i -B2 -A8 "SIGSJ04" <arquivo> | grep -iE "user|security-domain|application-policy|jndi|connection-url"
bash: syntax error near unexpected token `|'
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]# B=/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]# grep -n -iE "jndi-name|connection-url|user-name|security-domain|application-policy" $B/deployapp/sigsj-oracle-ds.xml
4:    <jndi-name>jdbc/SIGSJ04</jndi-name>
5:    <connection-url>jdbc:oracle:thin:@cnpexdadvm01-scan8.extra.caixa.gov.br:1521/orad01bc</connection-url>
7:    <user-name>SGSJSD01</user-name>
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]# grep -n -i -A12 "SIGSJ04" $B/conf/login-config.xml | sed -E 's#(name="password">)[^<]*#\1***#I' | grep -iE "application-policy|login-module|username|password|managedConnectionFactoryName"
137:           <module-option name="managedConnectionFactoryName">jboss.jca:name=jdbc/SIGSJ04,service=LocalTxCM</module-option>
138-        </login-module>
140-  </application-policy>
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
