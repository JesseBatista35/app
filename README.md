D=/opt/jboss/jboss-eap/dc/configuration/domain.xml
sed -n '19607,20596p' $D | sed -n '/<resource-adapter id="wmq/,/<\/resource-adapter>/p' | grep -A1 -E 'jndi-name=|name="(hostName|port|channel|queueManager)"' | grep -vE '^--$|password'
