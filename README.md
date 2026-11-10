1. CLI do 471:

/server-group=sifec-intranet/system-property=hibernate.jpa.compliance.global_id_generators:add(value="false")
/server-group=sifec-intranet:restart-servers(blocking=true)
/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)

2. Log no 473 (abra antes):

sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -E "WFLYSRV0010|WFLYCTL0013|WFLYUT0021|ERROR|Duplicate generator|sirur|SIRUR"

3. Deploy de novo:

deploy --name=SIRUR --server-groups=sifec-intranet
