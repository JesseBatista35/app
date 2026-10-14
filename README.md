
[domain@10.116.89.0:9999 /]
[domain@10.116.89.0:9999 /]
[domain@10.116.89.0:9999 /] ls /host=sbrdeapllx105_corporativo/server-config
sicdu-cliente-intranet_node1_lx105   sicdu-convenio-intranet_node1_lx105  sinad_node1_lx105                    siric_node1_lx105                    sisgd-intranet_node1_lx105
sicdu-convenio-internet_node1_lx105  simcn_node1_lx103                    siric-adm_node1_lx105                sisgd-internet_node1_lx105           siwic_node1_lx105

[domain@10.116.89.0:9999 /]
[domain@10.116.89.0:9999 /]
[domain@10.116.89.0:9999 /] /host=sbrdeapllx112:read-attribute(name=host-state)
{
    "outcome" => "success",
    "result" => "running"
}
[domain@10.116.89.0:9999 /]
[domain@10.116.89.0:9999 /]
[domain@10.116.89.0:9999 /] /host=sbrdeapllx105_corporativo/server-config=simcn_node1_lx103:stop(blocking=true)
{
    "outcome" => "success",
    "result" => "STOPPED"
}
[domain@10.116.89.0:9999 /] undeploy SIMCN --server-groups=simcn
Undeploy failed: {"host-failure-descriptions" => {"sbrdeapllx112" => "WFLYCTL0063: Composite operation was rolled back"}}
[domain@10.116.89.0:9999 /] /host=sbrdeapllx105_corporativo/server-config=simcn_node1_lx103:start(blocking=true)
{
    "outcome" => "success",
    "result" => "STARTED"
}
[domain@10.116.89.0:9999 /]
