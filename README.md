Análise:
A release do SIGSJ-backend-portal-judicial (DES) terminava com timeout na etapa “Verificando Status do Deployment” porque o pod não completava o startup. O log da aplicação mostra que o Quarkus aborta a inicialização com InactiveBeanException. O datasource padrão é desativado automaticamente porque a propriedade quarkus.datasource.jdbc.url não está definida. Com isso, o persistence unit também fica inativo e a injeção do EntityManager/Session no ProcessoRepository falha.

Causa:
É um ambiente novo, no primeiro deploy. O grupo de variáveis SIGSJ-BACKEND-PORTAL-JUDICIAL-DES contém apenas a variável INIT, gerada na criação automática, e não tem nenhuma configuração da aplicação (URL de banco, credenciais e demais parâmetros). Não há falha na esteira.

Ação necessária (fábrica):

Informar as variáveis exigidas pela aplicação, conforme os placeholders do application.properties: no mínimo URL JDBC, usuário/senha (preferencialmente via cofre BeyondTrust) e demais parâmetros de integração. Elas serão cadastradas no grupo de variáveis do ambiente.
Os grupos de TQS e HMP estão na mesma situação. Recomendamos enviar as variáveis dos três ambientes.
Verificar o alerta de que o persistence unit “não inclui nenhuma entidade”. Caso o projeto possua classes @Entity, conferir o uso de jakarta.persistence e a indexação (Jandex) caso as entidades estejam em outro módulo.

Com as variáveis configuradas, basta executar novamente a release. A W.O. será encerrada e, após o envio das variáveis pela fábrica, uma nova solicitação poderá ser aberta caso seja necessário apoio no cadastro.
