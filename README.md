
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
[root@caddeapllx765 p585600]# JB=/opt/jboss/jboss-eap
[root@caddeapllx765 p585600]# CFG=$JB/standalone/configuration/standalone-full-ha.xml
[root@caddeapllx765 p585600]# cp -p $CFG $CFG.bkp.$(date +%Y%m%d%H%M)
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]# $JB/bin/jboss-cli.sh -c '/subsystem=modcluster/mod-cluster-config=configuration:read-attribute(name=node-timeout)'
Failed to connect to the controller: The controller is not available at localhost:9990: java.net.ConnectException: WFLYPRT0053: Não foi possível conectar-se oa remote+http://localhost:9990. A conexão falhou: WFLYPRT0053: Não foi possível conectar-se oa remote+http://localhost:9990. A conexão falhou: Conexão recusada
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]# $JB/bin/jboss-cli.sh -c --controller=10.116.193.253:9990 '/subsystem=modcluster/mod-cluster-config=configuration:read-attribute(name=node-timeout)'
{
    "outcome" => "success",
    "result" => -1
}
[root@caddeapllx765 p585600]# $JB/bin/jboss-cli.sh -c '/subsystem=modcluster/mod-cluster-config=configuration:write-attribute(name=node-timeout,value=600)'
Failed to connect to the controller: The controller is not available at localhost:9990: java.net.ConnectException: WFLYPRT0053: Não foi possível conectar-se oa remote+http://localhost:9990. A conexão falhou: WFLYPRT0053: Não foi possível conectar-se oa remote+http://localhost:9990. A conexão falhou: Conexão recusada
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]# $JB/bin/jboss-cli.sh -c ':reload'
Failed to connect to the controller: The controller is not available at localhost:9990: java.net.ConnectException: WFLYPRT0053: Não foi possível conectar-se oa remote+http://localhost:9990. A conexão falhou: WFLYPRT0053: Não foi possível conectar-se oa remote+http://localhost:9990. A conexão falhou: Conexão recusada
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]#
[root@caddeapllx765 p585600]# $JB/bin/jboss-cli.sh -c ':reload'
Failed to connect to the controller: The controller is not available at localhost:9990: java.net.ConnectException: WFLYPRT0053: Não foi possível conectar-se oa remote+http://localhost:9990. A conexão falhou: WFLYPRT0053: Não foi possível conectar-se oa remote+http://localhost:9990. A conexão falhou: Conexão recusada
[root@caddeapllx765 p585600]#
