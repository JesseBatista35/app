Limpe a pasta temporária:

bash
cd /tmp && rm -rf /tmp/intra

O que a fábrica ajusta no SIGSJ-intranet-config (master):

jboss/standalone-full-ha.xml: remover o bloco <datasource jndi-name="java:jboss/datasources/SIGSJ04" ...> até o </datasource>. O ExampleDS e o <drivers> do h2 ficam.
jboss/jboss-deployments: remover a linha com.oracle.database.jdbc:ojdbc8:23.26.0.0.0:jar. Pode deixar o arquivo só com o cabeçalho ou apagá-lo.

Depois disso, o intranet TQS roda sem nenhuma variável de banco, e o Vitor não precisa cadastrar o SIGSJ04 no grupo de TQS do intranet. O DES do intranet também passa a usar esse arquivo na próxima release. As variáveis do SIGSJ04 que estão lá no grupo de DES podem ficar ou ser removidas, porque passam a não ser usadas.

Sugestão de resposta para o Marcio:

Marcio, confirmei no pacote do intranet (EAR, WARs e libs) e realmente não há nenhuma referência a datasource ou Oracle. Então, no SIGSJ-intranet-config, podem remover:
• do jboss/standalone-full-ha.xml, o bloco do datasource SIGSJ04;
• do jboss/jboss-deployments, a linha do ojdbc8.

Com isso o intranet não depende mais das variáveis de banco e a release do TQS pode rodar direto. Sobre o proxy, pode manter o proxydes.caixa, não existe proxytqs.caixa.
