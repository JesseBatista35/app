exit                     # sai da 2557 e volta para a 1121
hostname                 # confirme: caddeapllx1121
ls -la /opt/jboss/jboss-eap/standalone/deployments/ | grep -i sirot
grep -i "sirot" /logs/jboss/jboss-eap/standalone/sigsj-internet/server.log | grep -iE "WFLYSRV0010|implantado" | head -5
