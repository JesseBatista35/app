
[domain@10.116.89.0:9999 /] ls /host=sbrdeapllx112/server-config
[domain@10.116.89.0:9999 /] /server-group=simcn/deployment=SIMCN:read-resource(include-runtime=true)
{
    "outcome" => "failed",
    "failure-description" => "WFLYCTL0216: Management resource '[
    (\"server-group\" => \"simcn\"),
    (\"deployment\" => \"SIMCN\")
]' not found",
    "rolled-back" => true
}
[domain@10.116.89.0:9999 /]
