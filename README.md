ps -ef --forest | grep -A15 "sshd: sansbp01" | grep -v grep

tail -50 /logs/jboss/jboss-eap/standalone/siccp-intra/server.log
ss -ltnp | grep -E "8080|8443|9990"
