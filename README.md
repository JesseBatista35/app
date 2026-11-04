1. Deixe o log aberto no 473 (10.116.97.79):

bash
sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -iE --line-buffered "empresas|rural|WFLYSRV0010|WFLYSRV0021|faltam|WELD-001408|ClassNotFound|Registered web context"

2. SIEMP-EMPRESAS (no jboss-cli do 471, 10.116.97.59):

deploy --name=SIEMP-EMPRESAS --server-groups=sifec-intranet
deployment-info --name=SIEMP-EMPRESAS

3. Depois, o RURAL, assim que confirmarem a versão (a candidata é a SIFEC-RURAL4, 2.115.1.1):

deploy --name=SIFEC-RURAL4 --server-groups=sifec-intranet
deployment-info --name=SIFEC-RURAL4

Em cada um, o esperado é WFLYSRV0010 ... foi implantado e o Registered web context. Se aparecer WFLYSRV0021, o JBoss reverte sozinho. Me cola as linhas que eu classifico como ambiente ou código.

Quando terminar os dois, eu monto o resumo do dia para você mandar ao Paulo e atualizo a planilha.
