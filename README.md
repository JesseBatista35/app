
-bash-5.1$ tail -40 /opt/SUNWas8/domains/das01/logs/server.log
[#|2026-10-27T16:34:50.995-0300|INFO|sun-appserver-ee8.2|javax.enterprise.system.tools.admin|_ThreadID=10;|ADM1506: Status of Standard JMX Connector: Active = [true]|#]

[#|2026-10-27T16:34:51.019-0300|INFO|sun-appserver-ee8.2|javax.enterprise.resource.jms|_ThreadID=10;|JMS5023: JMS service successfully started. Instance Name = imqbroker, Home = [/opt/SUNWas8/imq/bin].|#]

[#|2026-10-27T16:34:51.060-0300|WARNING|sun-appserver-ee8.2|javax.ee.enterprise.system.tools.admin|_ThreadID=10;|EEADM0302:Connection exception while connecting to server dsv01, MBeans from server instance dsv01 cannot be cascaded|#]

[#|2026-10-27T16:34:51.085-0300|WARNING|sun-appserver-ee8.2|javax.ee.enterprise.system.tools.admin|_ThreadID=10;|EEADM0302:Connection exception while connecting to server dsv02, MBeans from server instance dsv02 cannot be cascaded|#]

[#|2026-10-27T16:34:51.112-0300|WARNING|sun-appserver-ee8.2|javax.ee.enterprise.system.tools.admin|_ThreadID=10;|EEADM0302:Connection exception while connecting to server dsv03, MBeans from server instance dsv03 cannot be cascaded|#]

[#|2026-10-27T16:34:51.128-0300|WARNING|sun-appserver-ee8.2|javax.ee.enterprise.system.tools.admin|_ThreadID=10;|EEADM0302:Connection exception while connecting to server dsv04, MBeans from server instance dsv04 cannot be cascaded|#]

[#|2026-10-27T16:34:51.139-0300|WARNING|sun-appserver-ee8.2|javax.ee.enterprise.system.tools.admin|_ThreadID=10;|EEADM0302:Connection exception while connecting to server dsv05, MBeans from server instance dsv05 cannot be cascaded|#]

[#|2026-10-27T16:34:51.148-0300|WARNING|sun-appserver-ee8.2|javax.ee.enterprise.system.tools.admin|_ThreadID=10;|EEADM0302:Connection exception while connecting to server dsv06, MBeans from server instance dsv06 cannot be cascaded|#]

[#|2026-10-27T16:34:51.157-0300|WARNING|sun-appserver-ee8.2|javax.ee.enterprise.system.tools.admin|_ThreadID=10;|EEADM0302:Connection exception while connecting to server dsv07, MBeans from server instance dsv07 cannot be cascaded|#]

[#|2026-10-27T16:34:51.172-0300|WARNING|sun-appserver-ee8.2|javax.ee.enterprise.system.tools.admin|_ThreadID=10;|EEADM0302:Connection exception while connecting to server dsv08, MBeans from server instance dsv08 cannot be cascaded|#]

[#|2026-10-27T16:34:51.185-0300|WARNING|sun-appserver-ee8.2|javax.ee.enterprise.system.tools.admin|_ThreadID=10;|EEADM0302:Connection exception while connecting to server dsv09, MBeans from server instance dsv09 cannot be cascaded|#]

[#|2026-10-27T16:34:51.198-0300|WARNING|sun-appserver-ee8.2|javax.ee.enterprise.system.tools.admin|_ThreadID=10;|EEADM0302:Connection exception while connecting to server dsv10, MBeans from server instance dsv10 cannot be cascaded|#]

[#|2026-10-27T16:34:51.210-0300|WARNING|sun-appserver-ee8.2|javax.ee.enterprise.system.tools.admin|_ThreadID=10;|EEADM0302:Connection exception while connecting to server dsv11, MBeans from server instance dsv11 cannot be cascaded|#]

[#|2026-10-27T16:34:51.257-0300|INFO|sun-appserver-ee8.2|javax.enterprise.system.core|_ThreadID=10;|Application server startup complete.|#]

[#|2026-10-27T16:37:57.566-0300|SEVERE|sun-appserver-ee8.2|javax.enterprise.system.container.web|_ThreadID=12;|failure (23294): HTTP3068: Error receiving request from 10.116.89.101 (SSL_ERROR_CERTIFICATE_UNKNOWN_ALERT: SSL peer had some unspecified issue with the certificate it received)
|#]

[#|2026-10-27T16:37:57.570-0300|SEVERE|sun-appserver-ee8.2|javax.enterprise.system.container.web|_ThreadID=13;|failure (23294): HTTP3068: Error receiving request from 10.116.89.101 (SSL_ERROR_CERTIFICATE_UNKNOWN_ALERT: SSL peer had some unspecified issue with the certificate it received)
|#]

[#|2026-10-27T16:38:02.613-0300|SEVERE|sun-appserver-ee8.2|javax.enterprise.system.container.web|_ThreadID=13;|failure (23294): HTTP3068: Error receiving request from 127.0.0.1 (SSL_ERROR_CERTIFICATE_UNKNOWN_ALERT: SSL peer had some unspecified issue with the certificate it received)
|#]

[#|2026-10-27T16:38:02.617-0300|SEVERE|sun-appserver-ee8.2|javax.enterprise.system.container.web|_ThreadID=13;|failure (23294): HTTP3068: Error receiving request from 127.0.0.1 (SSL_ERROR_CERTIFICATE_UNKNOWN_ALERT: SSL peer had some unspecified issue with the certificate it received)
|#]

-bash-5.1$
-bash-5.1$
-bash-5.1$ /opt/SUNWas8/bin/asadmin list-instances --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf
java.security.cert.CertificateExpiredException: NotAfter: Sun Dec 07 17:46:23 BRT 2025
CLI137 Command list-instances failed.
-bash-5.1$
-bash-5.1$
-bash-5.1$ /opt/SUNWas8/bin/asadmin list-components --target dsv01 --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf
Usage: list-components [--terse=false] [--echo=false] [--interactive=true] [--host localhost] [--port 4848|4849] [--secure | -s] --user admin_user [--passwordfile filename] [--type application|ejb|web|connector] [target (Default server)]
CLI013 Option target does not apply to list-components.
-bash-5.1$
-bash-5.1$
-bash-5.1$ /opt/SUNWas8/bin/asadmin undeploy --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf --target dsv01 sidmf
27/10/2026 16:39:34 com.sun.appserv.management.client.ProxyFactory getInstance
SEVERE: ProxyFactory.getInstance: Failure trying to create a new ProxyFactory: java.io.IOException: java.security.cert.CertificateExpiredException: NotAfter: Sun Dec 07 17:46:23 BRT 2025
CLI175 The target dsv01 is invalid. Valid target types are cluster, domain, unclustered server instance, domain administration server.
CLI137 Command undeploy failed.
-bash-5.1$
-bash-5.1$
-bash-5.1$
