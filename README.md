DOM=/opt/SUNWas8/domains/das01
ps -ef | grep das01 | grep -v grep | grep -v imq
netstat -an -f inet | grep 14848

find $DOM ! -user sjsas8 -ls

chown -R sjsas8:sunjava $DOM

chown -R sjsas8:sunjava $DOM

grep -c AS_ADMIN_MASTERPASSWORD /opt/SUNWas8/config/passwordfile.conf
ls -l $DOM/master-password 2>/dev/null

  su - sjsas8 -c "/opt/SUNWas8/bin/asadmin start-domain --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf das01"

    su - sjsas8
  /opt/SUNWas8/bin/asadmin start-domain --user ASadmin das01



  netstat -an -f inet | grep 14848
tail -30 $DOM/logs/server.log

su - sjsas8 -c "/opt/SUNWas8/bin/asadmin list-components --target dsv01 --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf"
su - sjsas8 -c "/opt/SUNWas8/bin/asadmin undeploy --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf --target dsv01 sidmf"





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
root@sspdeaplux0100:/#
