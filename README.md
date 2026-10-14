
[domain@10.116.89.0:9999 /] /server-group=simcn/deployment=SIMCN:read-resource(include-runtime=true)
{
    "outcome" => "failed",
    "failure-description" => "WFLYCTL0216: Management resource '[
    (\"server-group\" => \"simcn\"),
    (\"deployment\" => \"SIMCN\")
]' not found",
    "rolled-back" => true
}
[domain@10.116.89.0:9999 /] ls /host=sbrdeapllx112/server-config
server-one  server-two

[domain@10.116.89.0:9999 /] /host=sbrdeapllx112/server-config=*:read-attribute(name=group)
{
    "outcome" => "success",
    "result" => [
        {
            "address" => [
                ("host" => "sbrdeapllx112"),
                ("server-config" => "server-one")
            ],
            "outcome" => "success",
            "result" => "main-server-group"
        },
        {
            "address" => [
                ("host" => "sbrdeapllx112"),
                ("server-config" => "server-two")
            ],
            "outcome" => "success",
            "result" => "other-server-group"
        }
    ]
}
[domain@10.116.89.0:9999 /] /host=sbrdeapllx112/server=*:read-attribute(name=server-state)
{
    "outcome" => "success",
    "result" => [
        {
            "address" => [
                ("host" => "sbrdeapllx112"),
                ("server" => "server-one")
            ],
            "outcome" => "success",
            "result" => "STOPPED"
        },
        {
            "address" => [
                ("host" => "sbrdeapllx112"),
                ("server" => "server-two")
            ],
            "outcome" => "success",
            "result" => "STOPPED"
        }
    ]
}
[domain@10.116.89.0:9999 /]
