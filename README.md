
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# ls -l $DOM/config/ | egrep -i 'lock|pid'
-rw-r--r--   1 sjsas8   sunjava    33251 abr 20  2026 hs_err_pid1703.log
-rw-r--r--   1 sjsas8   sunjava    25991 mar  3  2026 hs_err_pid28142.log
-rw-r--r--   1 sjsas8   sunjava    25461 abr 17  2026 hs_err_pid6525.log
root@sspdeaplux0100:/# egrep -n 'admin-listener' $DOM/config/domain.xml
388:        <http-listener acceptor-threads="1" address="0.0.0.0" blocking-enabled="false" default-virtual-server="__asadmin" enabled="true" family="inet" id="admin-listener" port="14848" security-enabled="true" server-name="" xpowered-by="true"/>
394:        <virtual-server default-web-module="admingui" hosts="${com.sun.aas.hostName}" http-listeners="admin-listener" id="__asadmin" log-file="${com.sun.aas.instanceRoot}/logs/server.log" state="on">
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# sudo -u sjsas8 kill 7248
Sinto muito, usu▒rio root n▒o tem permiss▒o para executar "/bin/kill 7248" como sjsas8 em sspdeaplux0100.
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# sudo -u sjsas8 kill -9 7248
Sinto muito, usu▒rio root n▒o tem permiss▒o para executar "/bin/kill -9 7248" como sjsas8 em sspdeaplux0100.
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# sudo -sjsas8
sudo: illegal option -- j
usage: sudo -h | -K | -k | -V
usage: sudo -v [-ABknS] [-g group] [-h host] [-p prompt] [-u user]
usage: sudo -l [-ABknS] [-g group] [-h host] [-p prompt] [-U user] [-u user] [command]
usage: sudo [-ABbEHknPS] [-C num] [-D directory] [-g group] [-h host] [-p prompt] [-R directory] [-T timeout] [-u user] [VAR=value] [-i|-s] [<command>]
usage: sudo -e [-ABknS] [-C num] [-D directory] [-g group] [-h host] [-p prompt] [-R directory] [-T timeout] [-u user] file ...
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# sudo -u sjsas8 kill 7248
Sinto muito, usu▒rio root n▒o tem permiss▒o para executar "/bin/kill 7248" como sjsas8 em sspdeaplux0100.
root@sspdeaplux0100:/# sudo -u sjsas8 kill -9 7248
Sinto muito, usu▒rio root n▒o tem permiss▒o para executar "/bin/kill -9 7248" como sjsas8 em sspdeaplux0100.
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# kill -9 7248
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# ^C
root@sspdeaplux0100:/# DOM=/opt/SUNWas8/domains/das01
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# ps -ef | grep das01 | grep -v grep | grep -v imq
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# netstat -an -f inet | grep 14848
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# find $DOM ! -user sjsas8 -ls
2146896  259 -rw-------   1 root     root       241041 May 31  2023 /opt/SUNWas8/domains/das01/config/backup/domain.xml.20230531_Daniella
root@sspdeaplux0100:/# grep -c AS_ADMIN_MASTERPASSWORD /opt/SUNWas8/config/passwordfile.conf
0
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# ls -l $DOM/master-password 2>/dev/null
-rw-------   1 sjsas8   sunjava      500 dez  7  2015 /opt/SUNWas8/domains/das01/master-password
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# ls -l $DOM/config/*.db
-rw-------   1 sjsas8   sunjava   131072 set  5  2024 /opt/SUNWas8/domains/das01/config/cert8.db
-rw-------   1 sjsas8   sunjava   131072 set  5  2024 /opt/SUNWas8/domains/das01/config/key3.db
-rw-------   1 sjsas8   sunjava   131072 fev  8  2021 /opt/SUNWas8/domains/das01/config/secmod.db
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#  su - sjsas8 -c "/opt/SUNWas8/bin/asadmin start-domain --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf das01"
Starting Domain das01, please wait.
Default Log location is /opt/SUNWas8/domains/das01/logs/server.log.
The domain (das01) is already running.
CLI156 Could not start the domain das01.
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#  su - sjsas8 -c "/opt/SUNWas8/bin/asadmin start-domain --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf das01"
Starting Domain das01, please wait.
Default Log location is /opt/SUNWas8/domains/das01/logs/server.log.
The domain (das01) is already running.
CLI156 Could not start the domain das01.
root@sspdeaplux0100:/#
root@sspdeaplux0100:/#
root@sspdeaplux0100:/# su - sjsas8
-bash-5.1$
-bash-5.1$
-bash-5.1$ /opt/SUNWas8/bin/asadmin start-domain --user ASadmin das01
Starting Domain das01, please wait.
Default Log location is /opt/SUNWas8/domains/das01/logs/server.log.
The domain (das01) is already running.
CLI156 Could not start the domain das01.
-bash-5.1$
-bash-5.1$
-bash-5.1$
-bash-5.1$
-bash-5.1$  netstat -an -f inet | grep 14848
      *.14848              *.*                  0      0  256000      0 LISTEN
-bash-5.1$
-bash-5.1$
-bash-5.1$ tail -30 $DOM/logs/server.log
tail: cannot open input
-bash-5.1$
-bash-5.1$
-bash-5.1$ tail -30 $DOM/logs/server.log
tail: cannot open input
-bash-5.1$
-bash-5.1$
-bash-5.1$
