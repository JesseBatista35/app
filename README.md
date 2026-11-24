**
[root@caddeapllx137 p585600]#
[root@caddeapllx137 p585600]#
[root@caddeapllx137 p585600]# H=/opt/jbcs-httpd24-2.4/httpd
[root@caddeapllx137 p585600]# grep -niE 'mod_cluster|manager_module|CreateBalancers|ProxyTimeout|AdvertiseFrequency|EnableMCPMReceive' $H/conf/httpd_eap_71_esteiraagil.conf
63:# mod_proxy_balancer should be disabled when mod_cluster is used
65:LoadModule cluster_slotmem_module modules/mod_cluster_slotmem.so
66:LoadModule manager_module modules/mod_manager.so
69:MemManagerFile /opt/jbcs-httpd24-2.4/httpd/cache/mod_cluster_httpd_eap_71_esteiraagil
71:<IfModule manager_module>
77:    EnableMCPMReceive
78:    <Location /mod_cluster-manager>
79:      SetHandler mod_cluster-manager
[root@caddeapllx137 p585600]#
[root@caddeapllx137 p585600]#
[root@caddeapllx137 p585600]#



-sh-4.2$
-sh-4.2$ sudo su
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]# ps -ef | grep '[j]boss-modules' | tr ' ' '\n' | grep -E 'jboss.home.dir|jboss.server.base.dir|server-config|^-c$|\.xml'
-Djboss.home.dir=/opt/jboss/jboss-eap
-Djboss.server.base.dir=/opt/jboss/jboss-eap/standalone
-Djboss.server.base.dir=/opt/jboss/jboss-eap/standalone
-c
standalone-full-ha.xml
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]# JB=cole-aqui-o-jboss.home.dir
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]# ls $JB/bin/jboss-cli.sh
ls: não é possível acessar cole-aqui-o-jboss.home.dir/bin/jboss-cli.sh: Arquivo ou diretório não encontrado
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]# grep -n -A12 'urn:jboss:domain:modcluster' $JB/standalone/configuration/standalone-full-ha.xml | grep -iE 'modcluster|proxy|node-timeout|balancer|advertise'
grep: cole-aqui-o-jboss.home.dir/standalone/configuration/standalone-full-ha.xml: Arquivo ou diretório não encontrado
[root@caddeapllx765 p585600]#
