cd /tmp && rm -rf bolchk && mkdir bolchk && cd bolchk
unzip -p /opt/jboss-eap/standalone/deployments/boletoService-ear.ear META-INF/jboss-deployment-structure.xml
unzip -o -q /opt/jboss-eap/standalone/deployments/boletoService-ear.ear 'boletoService-war-*.war'
unzip -o -q boletoService-war-*.war 'WEB-INF/*.xml'
grep -rn "sirotcon" WEB-INF/ 2>/dev/null
