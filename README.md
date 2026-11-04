batch
/profile=full-ha-sifec-intranet/subsystem=security/security-domain="java:/jaas/jaas-sifec":add(cache-type=default)
/profile=full-ha-sifec-intranet/subsystem=security/security-domain="java:/jaas/jaas-sifec"/authentication=classic:add(login-modules=[{code=Remoting,flag=optional,module-options={password-stacking=useFirstPass}},{code=RealmDirect,flag=required,module-options={password-stacking=useFirstPass}}])
run-batch


/profile=full-ha-sifec-intranet/subsystem=security:read-children-names(child-type=security-domain)

/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)
