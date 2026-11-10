find / -path "*servers/sipen*" -name "server.log*" 2>/dev/null

find /opt /app /jboss /usr/local -name "server.log*" 2>/dev/null | grep -i sipen

cd /opt/jboss-eap/domain/servers/sipen_node3_lx0006/log
grep -n -B5 -A30 "LoginException\|consultaDadosLogin\|ECI\|CTG\|ERR_" server.log | less

grep -l "LoginException" server.log*
