
grep: server.log: No such file or directory
-sh-4.1$ find / -path "*servers/sipen*" -name "server.log*" 2>/dev/null
/logs/jboss-eap/hc/servers/sipen_node3_lx0006/server.log
/logs/jboss-eap/hc/servers/sipen_node3_lx0006/server.log.1
^C
-sh-4.1$
-sh-4.1$
-sh-4.1$ find /opt /app /jboss /usr/local -name "server.log*" 2>/dev/null | grep -i sipen
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$ cd /opt/jboss-eap/domain/servers/sipen_node3_lx0006/log
-sh: cd: /opt/jboss-eap/domain/servers/sipen_node3_lx0006/log: No such file or directory
-sh-4.1$ grep -n -B5 -A30 "LoginException\|consultaDadosLogin\|ECI\|CTG\|ERR_" server.log | less
grep: server.log: No such file or directory
-sh-4.1$ grep -l "LoginException" server.log*
grep: server.log*: No such file or directory
-sh-4.1$
