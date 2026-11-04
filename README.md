
[domain@localhost:9443 /]
[domain@localhost:9443 /] /profile=full-ha-sifec-intranet/subsystem=weld:write-attribute(name=require-bean-descriptor,value=true)
{
    "outcome" => "success",
    "result" => undefined,
    "server-groups" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx473" => {"response" => {
        "outcome" => "success",
        "result" => undefined,
        "response-headers" => {
            "operation-requires-reload" => true,
            "process-state" => "reload-required"
        }
    }}}}}}
}

[domain@localhost:9443 /] /server-group=sifec-intranet:reload-servers(blocking=true)
{
    "outcome" => "success",
    "result" => undefined,
    "server-groups" => undefined
}

[domain@localhost:9443 /]
