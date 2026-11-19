# o EAR do intranet referencia a SenhasSIIBC?
find /opt/jboss-eap/standalone/deployments -name "*.ear" -o -name "*.war" 2>/dev/null
grep -rl "SenhasSIIBC" /opt/jboss-eap/standalone/deployments/ 2>/dev/null
# a lib já existe lá?
ls -la /apl/sigsj/lib/ 2>/dev/null
grep -n "library.path" /opt/jboss-eap/bin/standalone.conf
