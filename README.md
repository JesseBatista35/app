
Boa tarde, estamos com problema no servidor do SIDMF após tentar fazer o undeploy da Aplicação recebemos o erro:

sudo -u sjsas8 /opt/SUNWas8/bin/asadmin undeploy --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf --target dsv01 sidmf


Aug 28, 2026 4:05:20 PM com.sun.appserv.management.client.ProxyFactory getInstance
SEVERE: ProxyFactory.getInstance: Failure trying to create a new ProxyFactory: java.io.IOException: Unable to connect to admin-server.  Please check if the server is up and running and that the host and port provided are correct.
CLI175 The target dsv01 is invalid. Valid target types are cluster, domain, unclustered server instance, domain administration server.
CLI137 Command undeploy failed.


sudo -u sjsas8 /opt/SUNWas8/bin/asadmin undeploy --host localhost --port 14848 --user ASadmin --passwordfile /opt/SUNWas8/config/passwordfile.conf --target dsv01 sidmf

Aug 28, 2026 4:05:20 PM com.sun.appserv.management.client.ProxyFactory getInstance
SEVERE: ProxyFactory.getInstance: Failure trying to create a new ProxyFactory: java.io.IOException: Unable to connect to admin-server.  Please check if the server is up and running and that the host and port provided are correct.
CLI175 The target dsv01 is invalid. Valid target types are cluster, domain, unclustered server instance, domain administration server.
CLI137 Command undeploy failed.




**
[p585600@cadsvitrlx100 ~]$ ssh 10.116.89.101
#########################################################################
#          Ambiente administrado e monitorado por Brasilia
#########################################################################
#
# Site: CTC
# Hostname: sspdeaplux0100.caixa
# SO Release: Solaris 11.4.53.132.2
# Serial Number: AK00289677
# Memoria Total: 32.00 GB
# VCPUs: 16 Modelo: SPARC M6-32
# Control domain: cadcogerux031
# Ambiente:
# Descricao: SIGOV Aplicacao SJSAS8
(p585600@10.116.89.101) Password: #######################################
Last login: Tue Oct 27 16:17:04 2026 from 10.122.150.31
Could not chdir to home directory /caixa/usr/p585600: No such file or directory
-bash-5.1$
-bash-5.1$
-bash-5.1$
-bash-5.1$ hostname -i
usage: hostname [[-t] system_name]
       hostname [-D]
-bash-5.1$
-bash-5.1$
-bash-5.1$
-bash-5.1$
-bash-5.1$
**
