1. Desfazer o ajuste do Weld, já que não ajudou (no jboss-cli do 471):

/profile=full-ha-sifec-intranet/subsystem=weld:write-attribute(name=require-bean-descriptor,value=false)

Isso marca o servidor como reload-required, mas o SIFEC continua funcionando. O reload pode ficar para amanhã, junto com o restart da truststore do RURAL, numa parada só.

2. Confirmar que o SIFEC subiu no reload das 16:59. A linha dele não apareceu no trecho que você colou:

bash
sudo grep -E "WFLYSRV0010: \"SIFEC\"" /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | tail -1

O esperado é 16:59:xx ... "SIFEC" foi implantado (runtime-name: "sifec-2.160.3.0.ear").

[domain@localhost:9999 /] /profile=full-ha-sifec-intranet/subsystem=weld:write-attribute(name=require-bean-descriptor,value=false)
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

[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]


[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$ sudo grep -E "WFLYSRV0010: \"SIFEC\"" /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | tail -1
16:59:08,826 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "SIFEC" foi implantado (runtime-name: "sifec-2.160.3.0.ear")
[p585600@cbrdeapllx473 ~]$
