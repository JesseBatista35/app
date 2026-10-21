Análise da falha no ArgoCD_Deploy (DES) – silce-gestao-operacional

Diagnóstico:
O push do commit 0e29072 na branch develop disparou dois workflows distintos ao mesmo tempo:
- "CI/CD Workflow" (run 39603505365 #44)
- "CI/CD Workflow (develop)" (run 39603505605 #38)

As duas execuções atualizaram a tag de imagem no repositório infranprd. Prevaleceu a tag 39603505365 (PR #300). O health check da run #38 esperava a tag 39603505605 e falhou por divergência de tag após 30 tentativas, embora a aplicação estivesse Synced e Healthy.

Situação atual:
A aplicação silce-gestao-operacional-des está Synced/Healthy no ArgoCD, rodando a imagem do mesmo commit (0e29072). O Quarkus subiu normalmente. Não houve impacto funcional em DES.

Ações necessárias (responsabilidade do time de desenvolvimento):
1. Manter apenas um workflow disparando em push na branch develop. Remover o trigger duplicado ou desabilitar um dos arquivos em .github/workflows.
2. Incluir o tópico "backend" no repositório (About > Topics). Sem ele, o deploy em TQS da run #44 falhou com "Nenhum tópico válido encontrado".
3. Não aprovar o deploy em PLT pendente na run #44 enquanto não for definido qual é o workflow oficial.

Após os ajustes, executar novo push ou re-run no workflow mantido.
