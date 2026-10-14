
}
[domain@10.116.89.0:9999 /] /host=sbrdeapllx112/server-config=server-one:remove
{
    "outcome" => "failed",
    "result" => undefined,
    "failure-description" => {"host-failure-descriptions" => [("sbrdeapllx112" => "WFLYCTL0369: Required capabilities are not available:
    org.wildfly.domain.server-group.other-server-group in context 'server-config'; Possible registration points for this capability:
                /host=sbrdeapllx112/server-config=*")]},
    "rolled-back" => true
}
[domain@10.116.89.0:9999 /] /host=sbrdeapllx112/server-config=server-two:remove
{
    "outcome" => "failed",
    "result" => undefined,
    "failure-description" => {"host-failure-descriptions" => [("sbrdeapllx112" => "WFLYCTL0369: Required capabilities are not available:
    org.wildfly.domain.server-group.main-server-group in context 'server-config'; Possible registration points for this capability:
                /host=sbrdeapllx112/server-config=*")]},
    "rolled-back" => true
}
[domain@10.116.89.0:9999 /]
[domain@10.116.89.0:9999 /]
[domain@10.116.89.0:9999 /]
