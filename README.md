ps -ef | grep das01 | grep -v grep | grep -v imq
tail -40 /opt/SUNWas8/domains/das01/logs/server.log

/opt/SUNWas8/bin/asadmin list-instances --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf
/opt/SUNWas8/bin/asadmin list-components --target dsv01 --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf
/opt/SUNWas8/bin/asadmin undeploy --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf --target dsv01 sidmf
