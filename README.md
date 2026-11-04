/deployment=SIEMP:read-children-names(child-type=subdeployment)
/deployment=SIFEC-EMP:read-children-names(child-type=subdeployment)

Abra o log no 473:
bash
   sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -iE --line-buffered "emp-|WFLYSRV0010|WFLYSRV0021|faltam|Registered web context|WELD-|QuerySyntax"
Ative no 471:
   deploy --name=SIFEC-EMP --server-groups=sifec-intranet
   deployment-info --name=SIFEC-EMP

Como ler:

✅ Subiu se aparecer Registered web context: '/emp-web' e WFLYSRV0010: "SIFEC-EMP" foi implantado.
❌ Se aparecer WFLYSRV0021, me cola as linhas e eu classifico como ambiente ou código.

Se a versão de PRD não estiver entre as do domain, peça o link do Nexus e faça o upload pela console, como fizeram com o PJ.
