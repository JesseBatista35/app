
[domain@localhost:9443 /] batch
[domain@localhost:9443 / #] /profile=full-ha-sifec-intranet/subsystem=security/security-domain="java:/jaas/jaas-sifec":add(cache-type=default)
[domain@localhost:9443 / #] /profile=full-ha-sifec-intranet/subsystem=security/security-domain="java:/jaas/jaas-sifec"/authentication=classic:add(login-modules=[{code=Remoting,flag=optional,module-options={password-stacking=useFirstPass}},{code=RealmDirect,flag=required,module-options={password-stacking=useFirstPass}}])
[domain@localhost:9443 / #] run-batch
The batch failed with the following error (you are remaining in the batch editing mode to have a chance to correct the error): {"WFLYCTL0062: Composite operation failed and was rolled ba
ck. Steps that failed:" => {"Operation step-1" => "WFLYCTL0212: Duplicate resource [
    (\"profile\" => \"full-ha-sifec-intranet\"),
    (\"subsystem\" => \"security\"),
    (\"security-domain\" => \"java:/jaas/jaas-sifec\")
]"}}

[domain@localhost:9443 / #]
[domain@localhost:9443 / #]
[domain@localhost:9443 / #]
[domain@localhost:9443 / #]
[domain@localhost:9443 / #]
[domain@localhost:9443 / #]
[domain@localhost:9443 / #] /profile=full-ha-sifec-intranet/subsystem=security:read-children-names(child-type=security-domain)
[domain@localhost:9443 / #]
[domain@localhost:9443 / #]
[domain@localhost:9443 / #] /host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)
[domain@localhost:9443 / #]
