Próximo: CONSTRUCARD 1.23.1.2-b64. O pacote já está no 471.

1. No 473, deixe o log aberto:

bash
LOG=/opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log
tail -f $LOG | grep -aE "construcard|WFLYSRV00(10|21)|WFLYCTL0013|WFLYCTL0412|WELD-0014|ERROR|Contexto web registrado"

2. No CLI do 471:

/server-group=sifec-intranet/deployment=SIFEC-CONSTRUCARD:add(enabled=true)

Me mande a saída do CLI e o que aparecer no log. Se der erro, o JBoss desfaz sozinho e o servidor continua de pé.
