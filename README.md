deployment-info --server-group=sifec-intranet

2. Abrir o log no 473, em outra sessão:

bash
sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -iE --line-buffered "WFLYSRV0010|WFLYSRV0021|faltam|QuerySyntax|Registered web context"

3. Ativar, no jboss-cli do 471:

deploy --name=<NOME-DA-PRIMEIRA-COLUNA> --server-groups=sifec-intranet

Ou pela console: Deployments → Server Groups → sifec-intranet → (+) → Deploy Existing Content, e escolha o 8.40.1.

Como ler o resultado:

✅ Funcionou se aparecer Registered web context: '/workflow-credito-pj-web' e WFLYSRV0010 ... foi implantado. Peça para testarem o link do PJ no SIFEC.
❌ Se aparecer WFLYSRV0021 ou faltam [...], me cola as linhas.
