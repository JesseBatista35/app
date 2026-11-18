A
Caixa

Informamos que, em análise da build do SICLG-V2-FRONTEND, identificamos que a configuração do SonarQube na pipeline estava com parâmetros voltados para projetos Java. Com isso, o relatório de cobertura gerado pelo Jest (coverage/lcov.info) não era importado, e apenas os arquivos de configuração (jest.config.js e jest.config.spec.js) eram contabilizados na cobertura.

Ajuste realizado pela equipe da Esteira DevOps:
- Configurada na pipeline a importação do relatório de cobertura do Jest (lcov);
- Removidos da análise os arquivos de configuração, os arquivos de teste (*.spec.ts / *.spec.js) e os diretórios gerados na build (dist/ e coverage/).

Após o ajuste, o SonarQube passou a medir corretamente o código da aplicação (src/), e a cobertura no código novo passou de 0,0% para 68,6%. O arquivo jest.config.spec.js deixou de ser necessário e pode ser removido do repositório.

Conforme a TE102, o Quality Gate ainda reprova pelos critérios abaixo, que dependem de ajuste no código da aplicação pela equipe de desenvolvimento:

1. Cobertura de testes no código novo: 68,6%, abaixo do mínimo de 80%.
   Os arquivos com maior volume de linhas e condições sem cobertura são:
   - src/app/feature/termo-recebimento-formulario/termo-recebimento-formulario.component.ts
   - src/app/feature/inicio/inicio.component.ts
   - src/app/app.component.ts (0%)
   - src/app/feature/termo-recebimento-listagem/termo-recebimento-listagem.component.ts
   - Componentes de src/app/feature/ com cobertura entre 18% e 40% (gestao-formal-*, documentacao-*, relatorio-*, administracao-instrumentos-contratuais, legado-placeholder).
   A lista completa está no SonarQube em Measures > Coverage on New Code.

2. Issues críticas: 10 issues de severidade Critical e 11 bugs no código da aplicação.
   A lista está no SonarQube em Issues, filtrando Severity = Critical na branch master.

A parte relacionada à Esteira DevOps foi concluída, e por isso a demanda está sendo encerrada. Após as correções, basta executar uma nova build. Caso ocorra algum erro relacionado à esteira, pedimos que seja aberta uma nova demanda.

Link do projeto no SonarQube:
https://sonar-esteira.apps.produtos4.caixa/dashboard?id=SICLG-V2-FRONTEND&branch=master

Atenciosamente,

CTIS / CESTI Esteira DEVOPS DES TQS NPRD
