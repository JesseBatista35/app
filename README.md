Verificado o deploy do SIGCN MED Worker em DES (GitHub Actions + ArgoCD, app sigcn-med-worker-des).

A falha das execuções anteriores (ex.: run #93, branch develop) acontecia no step de health do ArgoCD_Deploy. Naquele momento o ArgoCD registrou a operação de sincronização como Failed, e por isso a esteira terminava com exit code 1. Como o pipeline foi disparado em três branches diferentes, as atualizações de tag de imagem no repositório de infra (infranprd) podem ter se sobreposto, gerando sincronizações concorrentes.

Foi realizada nova execução única do pipeline (run #94, branch Sprint_18, tag 40696031627), concluída com sucesso. No ArgoCD, a aplicação está Healthy e Synced (sync OK em 28/10/2026 às 10:29). O novo pod (ReplicaSet 559fdd88f9) está em execução, e os ConfigMaps cm-sigcn-med-worker e cm-sigcn-med-worker-appsettings estão sincronizados. O pod citado na abertura (sigcn-med-worker-des-74698b888c-z8xls) foi substituído.

Observação: o erro presente no log da aplicação, em DesbloquearValores (retorno sem sucesso da API de conta-depósito/lançamento D01), é de integração/negócio da aplicação e não tem relação com o deploy. Caso persista, deve ser tratado com o time responsável pela API.

Recomenda-se executar o pipeline em uma branch por vez para o mesmo ambiente, evitando sincronizações concorrentes no ArgoCD.

Demanda resolvida.
