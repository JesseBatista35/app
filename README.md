netstat -an -f inet | grep 14848

sudo -u sjsas8 /opt/SUNWas8/bin/asadmin list-domains

grep -n 'admin-listener' <dir_dominio>/config/domain.xml

sudo -u sjsas8 /opt/SUNWas8/bin/asadmin start-domain --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf <nome_dominio>
tail -200 <dir_dominio>/logs/server.log

sudo -u sjsas8 /opt/SUNWas8/bin/asadmin list-instances --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf
sudo -u sjsas8 /opt/SUNWas8/bin/asadmin list-clusters   --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf
sudo -u sjsas8 /opt/SUNWas8/bin/asadmin list-components --target dsv01 --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf

