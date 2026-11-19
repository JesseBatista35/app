B=/opt/jboss/jboss-5.1.0.GA/server/sigsj_internet

# datasource: url, jndi e qual security-domain usa
grep -n -iE "jndi-name|connection-url|user-name|security-domain|application-policy" $B/deployapp/sigsj-oracle-ds.xml

# security-domain: usuário (senha mascarada)
grep -n -i -A12 "SIGSJ04" $B/conf/login-config.xml | sed -E 's#(name="password">)[^<]*#\1***#I' | grep -iE "application-policy|login-module|username|password|managedConnectionFactoryName"
