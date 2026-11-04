/profile=full-ha-sifec-intranet:read-children-names(child-type=subsystem)
/profile=full-ha-sifec-intranet/subsystem=ee:read-attribute(name=global-modules)

  /profile=full-ha-sifec-intranet/subsystem=ee:list-add(name=global-modules,value={name=javax.jms.api,slot=main})

  /server-group=sifec-intranet:reload-servers(blocking=true)

  deploy --name=SIFEC-EMP --server-groups=sifec-intranet
