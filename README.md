grep -c AS_ADMIN_MASTERPASSWORD /opt/SUNWas8/config/passwordfile.conf
ls -l $DOM/master-password 2>/dev/null
ls -l $DOM/config/*.db

  su - sjsas8 -c "/opt/SUNWas8/bin/asadmin start-domain --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf das01"

    su - sjsas8
  /opt/SUNWas8/bin/asadmin start-domain --user ASadmin das01

  netstat -an -f inet | grep 14848
tail -30 $DOM/logs/server.log
