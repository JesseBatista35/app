Análise – SIBDO-web DES (release 543372)

O deploy do sibdo.war fica em FAILED porque os datasources sibdo-ds e siico-ds não sobem. O standalone-full-ha.xml do repositório SIBDO-web-config declara o driver PostgreSQL como módulo (module="org.postgresql"), mas esse módulo não é entregue ao servidor por nenhuma configuração do repositório. O resultado é a falha WFLYJCA0115 (módulo org.postgresql ausente). Como o default-bindings do subsystem EE aponta para o sibdo-ds, a falha do datasource derruba o deployment inteiro.

A esteira já permite entregar o driver pelo próprio repositório de config, então não há ação de Infra. A correção é feita pelo time de desenvolvimento no SIBDO-web-config:

Arquivo jboss/jboss-deployments: substituir a linha de modelo pela coordenada do driver disponível no Nexus (binario.caixa). Exemplo:
org.postgresql:postgresql:42.7.4:jar
Arquivo jboss/standalone-full-ha.xml:
Remover do bloco <drivers> o driver name="postgresql" module="org.postgresql".
Nos datasources sibdo-ds e siico-ds, alterar o driver para o nome do JAR publicado, com a mesma versão do item 1:
<driver>postgresql-42.7.4.jar</driver>
Pontos para conferir junto:
As variáveis SIBDO_DB_USER, SIBDO_DB_PASSWORD, SIICO_DB_USER e SIICO_DB_PASSWORD precisam estar cadastradas na release ou Library de DES.
A porta do sibdo-ds (51123) precisa estar correta. O siico-ds, no mesmo host, usa 5102.

Após o ajuste, executar nova release em DES. Em caso de falha, encaminhar o log da etapa “Copiando deployments adicionais” e do “Check Deployments”.
