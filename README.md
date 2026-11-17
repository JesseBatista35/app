Na VM, descubra onde o JBoss está e o que ele publicou:

bash
# onde está o JBoss
ps -ef | grep -i [j]boss | grep -o "jboss.home.dir=[^ ]*"
sudo ls /opt

# contextos registrados e erros de deploy (ajuste o caminho com o resultado acima)
JB=<jboss.home.dir>
sudo grep -E "WFLYUT0021|WFLYSRV0010|WFLYSRV0026|WFLYCTL0013|ERROR" $JB/standalone/log/server.log | tail -30
sudo ls -l $JB/standalone/deployments/

O que procurar:

WFLYUT0021: Registered web context: '/xxxx': esse é o contexto real. Se vier algo como /siemp ou /siemp-web, teste esse caminho no curl. Nesse caso, o Apache está redirecionando a raiz para o contexto errado (/siemp_java), e o ajuste fica na variável http_context_default da release ou no context-root do application.xml do EAR.
Arquivo .failed em deployments/, ou ERROR no log: o EAR não subiu. O motivo aparece no log. Pode ser o problema do mod_cluster no standalone-full-ha.xml que você analisou antes, ou falta de datasource ou módulo.
Nenhum .ear em deployments/: a release não copiou o pacote.

Me cola a saída que eu te digo qual é o caso.
