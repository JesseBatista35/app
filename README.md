/profile=full-ha-sifec-intranet/subsystem=security:read-children-names(child-type=security-domain)

/profile=full-ha-sifec-intranet/subsystem=security/security-domain="java:/jaas/jaas-sifec":read-resource(recursive=true)

/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)
