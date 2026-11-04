/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)

ssh p585600@10.116.97.79
sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -iE --line-buffered "emp-|WFLYSRV0010|WFLYSRV0021|JMSException|faltam|Registered web context|WELD-001408|Caused by"

Com o log aberto, rode o deploy no 471:

deploy --name=SIFEC-EMP --server-groups=sifec-intranet
✅ Subiu se aparecer Registered web context: '/emp-web' e WFLYSRV0010: "SIFEC-EMP" foi implantado.
❌ Se aparecer WFLYSRV0021, me cola as linhas.
