Analisei a esteira do siarx-backend-autoridade-registro e encontrei uma divergência com o que você comentou sobre o projeto ser AWS.

Hoje a esteira está toda configurada para Azure. O build está identificando o cloud provider como azure e publicando a imagem no ACR (acrcentralcaixanprd), e o config.yaml do ArgoCD aponta para o cluster aks-siarx-nprd, que não existe. Não encontrei nenhuma referência a AWS (EKS/ECR) na configuração atual.

Por isso pode ter havido inconsistência na criação do projeto via Fusion X. Consegue me confirmar alguns pontos?

O projeto deveria mesmo ser AWS? Se sim, sabe qual seria o cluster EKS de destino?
Na criação pela jornada do Fusion X, qual provedor de nuvem foi selecionado?

Se for confirmado que o correto é AWS, o ideal é sanitizar o projeto e executar a jornada novamente com o provedor certo, porque corrigir manualmente cada configuração pode deixar o projeto fora do padrão. Antes disso, recomendo fazer backup das alterações já feitas no repositório.
