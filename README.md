Prezados,

Encaminhamos demanda referente ao projeto SIARX (projeto novo, GitHub Actions + ArgoCD/AKS).

A aplicação siarx-backend-autoridade-registro teve o build DES concluído com sucesso (CI/CD Workflow Generic, branch Cesti-test001, run #3), porém o deploy não ocorreu.

Evidências:

O job ArgoCD_Deploy consultou a aplicação no ArgoCD (aroidpprd) e recebeu status nulo em todas as 30 tentativas. A aplicação não é criada no ArgoCD.
O repositório central gitops/apps possui as aplicações SIARX registradas (siarx-backend-autoridade-registro, siarx-backend-certificados, siarx-backend-certificados-digitais, siarx-backend-api-gestao-certificados, siarx-frontend-autoridade-registro-x), todas com destino cluster.destination.name: aks-siarx-nprd.
O cluster aks-siarx-nprd não foi localizado no portal Azure, e nenhuma aplicação SIARX aparece no ArgoCD.
O demandante confirmou que nenhuma aplicação do SIARX está funcionando em nenhum ambiente.

Solicitamos:

Verificar o provisionamento do AKS NPRD do SIARX (aks-siarx-nprd) e seu registro no ArgoCD; ou
Informar o cluster correto a ser utilizado pelo projeto.

Observação adicional: os arquivos de DES gerados pela jornada Fusion X vieram com valores de HMP (ex.: gitops/apps/siarx-backend-certificados/des/config.yaml com project: hmp / path: hmp, e host hmp-nprd no des/values.yaml da autoridade-registro). O config.yaml da autoridade-registro já foi corrigido pela CESTI. Os demais precisarão de revisão pelo demandante.
