ls -la /opt/jboss/jboss-eap/standalone/deployments/ | grep -i sirot
grep -n -i -B2 -A3 "sirot" /opt/jboss/jboss-eap/standalone/configuration/standalone-full-ha.xml
grep -i "sirot" /logs/jboss/jboss-eap/standalone/sigsj-internet/server.log | grep -iE "deploy|WFLYSRV0010|jndi" | head -10


ssh 10.116.201.25
grep -nE "WFLYCTL0412|WFLYCTL0180" /logs/jboss/jboss-eap/standalone/sigsj-boleto/server.log | tail -10
