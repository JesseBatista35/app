localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /] /profile=full-ha-sifec-intranet:read-children-names(child-type=subsystem)
{
    "outcome" => "success",
    "result" => [
        "batch-jberet",
        "bean-validation",
        "datasources",
        "discovery",
        "distributable-web",
        "ee",
        "ee-security",
        "ejb3",
        "elytron",
        "infinispan",
        "io",
        "jaxrs",
        "jca",
        "jdr",
        "jgroups",
        "jmx",
        "jpa",
        "jsf",
        "keycloak",
        "logging",
        "mail",
        "modcluster",
        "naming",
        "pojo",
        "remoting",
        "request-controller",
        "resource-adapters",
        "sar",
        "security",
        "security-manager",
        "transactions",
        "undertow",
        "webservices",
        "weld"
    ]
}

[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /] /profile=full-ha-sifec-intranet/subsystem=ee:read-attribute(name=global-modules)
{
    "outcome" => "success",
    "result" => undefined
}

[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /] /profile=full-ha-sifec-intranet/subsystem=ee:list-add(name=global-modules,value={name=javax.jms.api,slot=main})
{
    "outcome" => "success",
    "result" => undefined,
    "server-groups" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx473" => {"response" => {
        "outcome" => "success",
        "result" => undefined
    }}}}}}
}

[domain@localhost:9443 /]



me da p comando para ver o log no 473
