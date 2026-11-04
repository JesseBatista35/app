
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /] /profile=full-ha-sifec-intranet/subsystem=modcluster/proxy=default:read-attribute(name=balancer)
{
    "outcome" => "success",
    "result" => "mod_cluster_sifec"
}

[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /] /profile=full-ha-siemp/subsystem=modcluster/proxy=default:read-attribute(name=balancer)
{
    "outcome" => "success",
    "result" => "mod_cluster_siemp"
}

[domain@localhost:9443 /]
