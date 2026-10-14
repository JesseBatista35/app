ls /host=sbrdeapllx105_corporativo/server-config
/host=sbrdeapllx112:read-attribute(name=host-state)
/host=sbrdeapllx105_corporativo/server-config=simcn_node1_lx103:stop(blocking=true)
undeploy SIMCN --server-groups=simcn
/host=sbrdeapllx105_corporativo/server-config=simcn_node1_lx103:start(blocking=true)

/opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=10.116.89.0:9999 --command='ls /host=sbrdeapllx105_corporativo/server-config'
/opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=10.116.89.0:9999 --command='/host=sbrdeapllx112:read-attribute(name=host-state)'
/opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=10.116.89.0:9999 --command='/host=sbrdeapllx105_corporativo/server-config=simcn_node1_lx103:stop(blocking=true)'
/opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=10.116.89.0:9999 --command='undeploy SIMCN --server-groups=simcn'
/opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=10.116.89.0:9999 --command='/host=sbrdeapllx105_corporativo/server-config=simcn_node1_lx103:start(blocking=true)'
