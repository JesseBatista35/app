JB=/opt/jboss/jboss-eap
ls $JB/bin/jboss-cli.sh
grep -n -A12 'urn:jboss:domain:modcluster' $JB/standalone/configuration/standalone-full-ha.xml | grep -iE 'modcluster|proxy|node-timeout|balancer|advertise'
