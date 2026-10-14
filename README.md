À CAIXA

Prezados,

Conforme solicitado em demanda, foi realizada a análise da falha na esteira do projeto siarx-frontend-autoridade-registro-x.

O build e a publicação da imagem foram concluídos com sucesso.

A falha ocorre na etapa de deploy via ArgoCD (DES), pois o repositório de infraestrutura siarx-frontend-autoridade-registro-x-infranprd contém apenas o README.md. A estrutura de deploy (des/values.yaml), que deveria ter sido gerada pela jornada de criação de aplicação no Fusion X, não está presente.

Identificamos que a jornada não foi executada corretamente, uma vez que o merge da branch de inclusão de arquivos não trouxe os artefatos esperados.

Para regularização, orientamos os seguintes passos:

A equipe de desenvolvimento deve realizar o backup de eventuais alterações já feitas no repositório da aplicação.
Após o backup, deve ser aberta uma nova requisição solicitando a sanitização do projeto siarx-frontend-autoridade-registro-x, incluindo os repositórios gerados pela jornada.
Concluído o atendimento dessa requisição, a equipe poderá executar novamente a jornada de criação do projeto via Fusion X.

Atenciosamente,
