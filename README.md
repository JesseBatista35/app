
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]# JB=/opt/jboss/jboss-eap
[root@caddeapllx765 p585600]# ls $JB/bin/jboss-cli.sh
/opt/jboss/jboss-eap/bin/jboss-cli.sh
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]# grep -n -A12 'urn:jboss:domain:modcluster' $JB/standalone/configuration/standalone-full-ha.xml | grep -iE 'modcluster|proxy|node-timeout|balancer|advertise'
512:        <subsystem xmlns="urn:jboss:domain:modcluster:3.0">
513-            <mod-cluster-config advertise-socket="modcluster" proxies="proxy1 proxy2" balancer="${jboss_modcluster_balancer:mybalancer}" load-balancing-group="${jboss_modcluster_balancer:mybalancer}" connector="ajp">
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]#
