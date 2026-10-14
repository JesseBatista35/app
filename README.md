
[domain@10.116.89.0:9999 /]
[domain@10.116.89.0:9999 /]
[domain@10.116.89.0:9999 /]
[domain@10.116.89.0:9999 /] ls /host
DC_LX069                   sbrdeapllx103_financeiro   sbrdeapllx105_corporativo  sbrdeapllx111_orcamento    sbrdeapllx114_risco
sbrdeapllx099_habitacao    sbrdeapllx104_credito      sbrdeapllx110_servico      sbrdeapllx112

[domain@10.116.89.0:9999 /]
[domain@10.116.89.0:9999 /]
[domain@10.116.89.0:9999 /] /host=<nome-do-host-105>/server-config=simcn_node1_lx103:stop(blocking=true)
Failed to get the list of the operation properties: "WFLYCTL0030: No resource definition is registered for address [
    ("host" => "<nome-do-host-105>"),
    ("server-config" => "simcn_node1_lx103")
]"
[domain@10.116.89.0:9999 /]
[domain@10.116.89.0:9999 /]
[domain@10.116.89.0:9999 /]
