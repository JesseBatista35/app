
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /] /profile=full-ha-sifec-intranet/subsystem=security:read-children-names(child-type=security-domain)
{
    "outcome" => "success",
    "result" => [
        "jaas-sifec",
        "jaspitest",
        "java:/jaas/jaas-sifec",
        "jboss-ejb-policy",
        "jboss-web-policy",
        "keycloak",
        "other"
    ]
}

[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /] /profile=full-ha-sifec-intranet/subsystem=security/security-domain="java:/jaas/jaas-sifec":read-resource(recursive=true)
{
    "outcome" => "success",
    "result" => {
        "cache-type" => "default",
        "acl" => undefined,
        "audit" => undefined,
        "authentication" => {"classic" => {
            "login-modules" => [
                {
                    "code" => "Remoting",
                    "flag" => "optional",
                    "module" => undefined,
                    "module-options" => {"password-stacking" => "useFirstPass"}
                },
                {
                    "code" => "RealmDirect",
                    "flag" => "required",
                    "module" => undefined,
                    "module-options" => {"password-stacking" => "useFirstPass"}
                }
            ],
            "login-module" => {
                "Remoting" => {
                    "code" => "Remoting",
                    "flag" => "optional",
                    "module" => undefined,
                    "module-options" => {"password-stacking" => "useFirstPass"}
                },
                "RealmDirect" => {
                    "code" => "RealmDirect",
                    "flag" => "required",
                    "module" => undefined,
                    "module-options" => {"password-stacking" => "useFirstPass"}
                }
            }
        }},
        "authorization" => undefined,
        "identity-trust" => undefined,
        "jsse" => undefined,
        "mapping" => undefined
    }
}

[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /] /host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)
{
    "outcome" => "success",
    "result" => "running"
}

[domain@localhost:9443 /]
