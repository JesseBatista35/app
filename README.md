1. Servidor no ar (no jboss-cli do 471):

/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)

O resultado esperado é running.

2. SIFEC subiu sem erro (no 473):

bash
sudo grep -E "WFLYSRV0010|WFLYSRV0021|WFLYSRV0025" /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | tail -10

Deve aparecer "SIFEC" foi implantado, junto com SIFEC-CCR, BDCAIXA, HUB-FRONTEND e MINUTAS-FRONT, e no final o WFLYSRV0025. Se aparecer WFLYSRV0021 em algum deles, pare e me mande.

Peça também para alguém da sala testar o login e a Consulta de Contratos.

3. Se o SIFEC estiver ok, o EMPRESAS. Com o tail aberto no 473:

bash
sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -iE --line-buffered "empresas|WFLYSRV0010|WFLYSRV0021|WELD-001408|faltam|Registered web context"

E no 471:

deploy --name=SIEMP-EMPRESAS --server-groups=sifec-intranet

Rollback, se o SIFEC tiver qualquer problema:

/profile=full-ha-sifec-intranet/subsystem=weld:write-attribute(name=require-bean-descriptor,value=false)
/server-group=sifec-intranet:reload-servers(blocking=true)
