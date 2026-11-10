cd /logs/jboss-eap/hc/servers/sipen_node3_lx0006/
ls -lh


grep -c "LoginException\|Erro na montagem do Menu" server.log server.log.1

grep -n -B10 -A40 "LoginException" server.log | head -200]

grep -n -i "Caused by\|ECI\|CTG\|CICS\|Connection refused\|timed out\|SocketException\|obtenção dos dados de login" server.log | head -100

grep -n "JBAS015874\|WFLYSRV0025\|started in" server.log server.log.1
