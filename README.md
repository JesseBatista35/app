ls -la /opt/jboss-eap/standalone/deployments/ | grep -i sirot

  grep -n -i -A3 "sirot" /opt/jboss-eap/standalone/configuration/standalone*.xml
  ls /opt/jboss-eap/standalone/data/content/

  grep -nE "WFLYCTL0412|WFLYCTL0180" /logs/jboss/jboss-eap/standalone/sigsj-boleto/server.log | tail -10

    grep -nE "WFLYCTL0013|ERROR|Caused by" /logs/jboss/jboss-eap/standalone/sigsj-boleto/server.log | tail -40
