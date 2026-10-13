Prezados,

Demanda atendida. A aplicação SINAF-acoes-em-lote-mensageria (DES, namespace sinaf-des) está em execução, com conexão ao banco DB2 e aos tópicos Kafka estabelecidas com sucesso.

Diagnóstico:

O cofre BeyondTrust estava entregando corretamente o secret SINAF_DES/DATASOURCE_PASSWORD_SNAFPB01. O sidecar recuperou o valor sem erros e gravou o arquivo em /usr/src/app/secrets_files/SINAF_DES/, e a validação do secrets-check foi concluída com sucesso.
A falha estava na aplicação. Ela é Spring Boot 3.4.5, mas estava configurada para ler os secrets via SmallRye Config (SMALLRYE_CONFIG_SOURCE_FILE_LOCATIONS), mecanismo voltado a Quarkus que o Spring não utiliza nativamente. Além disso, a classe DatasourcePropertiesLogger (um BeanFactoryPostProcessor) lê a senha numa fase muito inicial do boot, o que causava o erro Could not resolve placeholder 'DATASOURCE_PASSWORD_SNAFPB01'. As demais variáveis do cofre (Kafka) só são resolvidas mais tarde, por isso o erro aparecia apenas nessa variável.

Ação realizada:

Incluída na biblioteca SINAF-ACOES-EM-LOTE-MENSAGERIA-DES a variável _ENV.SPRING_CONFIG_IMPORT = optional:configtree:/usr/src/app/secrets_files/SINAF_DES/, que faz o Spring carregar nativamente os arquivos do cofre no início do boot.
Novo deploy realizado com sucesso (release SINAF-acoes-em-lote-mensageria-20261009.1436-1.2.03-SNAPSHOT(2), EC DES).
