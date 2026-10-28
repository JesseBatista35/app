Prezados,

Solicito suporte para falha no deploy do SIGCN MED Worker em DES. O problema ocorreu em três branches diferentes, sempre apresentando falha na sincronização (exit code 1).

Pod: sigcn-med-worker-des-74698b888c-z8xls

O pod está fora de sincronia, com possível problema relacionado ao ConfigMap.

Run com erro no GitHub Actions

Favor apoiar na verificação e regularização da sincronização.

Skip to content
GitHub Enterprise
Users managed by Caixa Economica Federal
caixagithub
sigcn-med-worker
Repository navigation
Code
Issues
Pull requests
1
 (1)
Actions
Projects
Wiki
Security and quality
1
 (1)
Insights
Settings
CI/CD Workflow - DES/TQS
caixagithub/sigcn-med-worker_develop_40540986363.93 #93
All jobs
Run details
Annotations
1 error and 1 warning
CI_CD / ArgoCD_Deploy / ArgoCD_Deploy (DES)
failed yesterday in 8m 21s
Search logs
8s
1s
1s
0s
0s
0s
0s
0s
0s
0s
0s
0s
0s
1m 8s
0s
7s
0s
0s
0s
15s
0s
0s
0s
0s
0s
22s
5s
0s
0s
0s
6m 6s
Run caixagithub/DevSecOps-Actions/.github/integrations/argocd/health@main
  with:
    ARGOCD_SERVER: https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io
    ARGOCD_APP: sigcn-med-worker
    AMBIENTE: DES
    IMAGE_TAG: 40540986363
  env:
    APIM_VERSIONAPI: 
    APIM_displaynameAPI: 
    APIM_PATH: 
    APIM_SWAGGERPATH: 
    APIM_TAGSAPI: 
    APIM_POLICIESALLOPERATIONSPATH: 
    AZ_INSTALL_STATUS: ms_repo_ok
    AZ_VERSION: latest
    INSTALL_PREREQUISITES: true
    AZ_LATEST_VERSION: 2.91.0
    environment: des
    repository_suffix: infranprd
    REPO: sigcn-med-worker
    JOB_ID: 169496
    ARGOCD_AUTH_TOKEN: ***
Logging image tag
0s
Run echo "INPUT_IMAGE_TAG: '40540986363'"
    echo "INPUT_IMAGE_TAG: '40540986363'"
    shell: /usr/bin/bash --noprofile --norc -e -o pipefail {0}
    env:
      APIM_VERSIONAPI: 
      APIM_displaynameAPI: 
      APIM_PATH: 
      APIM_SWAGGERPATH: 
      APIM_TAGSAPI: 
      APIM_POLICIESALLOPERATIONSPATH: 
      AZ_INSTALL_STATUS: ms_repo_ok
      AZ_VERSION: latest
      INSTALL_PREREQUISITES: true
      AZ_LATEST_VERSION: 2.91.0
      environment: des
      repository_suffix: infranprd
      REPO: sigcn-med-worker
      JOB_ID: 169496
      ARGOCD_AUTH_TOKEN: ***
  INPUT_IMAGE_TAG: '40540986363'
Aguardando processo de SYNC finalizar
6m 6s
Run for i in {1..30}; do
    for i in {1..30}; do
      STATUS=$(curl -s -X GET "https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io/api/v1/applications/sigcn-med-worker-des" \
      -H "Authorization: ***")
    
      HEALTH=$(echo "$STATUS" | jq -r '.status.health.status')
      SYNCED=$(echo "$STATUS" | jq -r '.status.sync.status')
      PHASE=$(echo "$STATUS" | jq -r '.status.operationState.phase')
      TAG=$(echo "$STATUS" | jq -r '.status.summary.images[0]' | sed 's/.*://')
    
      echo "Tentativa $i - Phase: $PHASE, Health: $HEALTH, Sync: $SYNCED, Argo_Tag: $TAG, Image_Tag: 40540986363"
    
      if [[ "$PHASE" == "Running" ]]; then
        echo "Sync ainda em execução, aguardando..."
      fi
    
      if [[ "$PHASE" == "Failed" ]]; then
        echo "HEALTH_WAS_SUCCESSFUL=false" >> $GITHUB_OUTPUT
    
        echo "A sincronização falhou"
    
        exit 0
      fi
    
      if [[ "$PHASE" == "Succeeded" && "$HEALTH" == "Healthy" && "$SYNCED" == "Synced" && "$TAG" == "40540986363" ]]; then
        echo "Aplicação UP e Sincronizada."
    
        echo "HEALTH_WAS_SUCCESSFUL=true" >> $GITHUB_OUTPUT
    
        exit 0
      fi
    
      sleep 20
    done
    
    echo "HEALTH_WAS_SUCCESSFUL=false" >> $GITHUB_OUTPUT
    shell: /usr/bin/bash --noprofile --norc -e -o pipefail {0}
    env:
      APIM_VERSIONAPI: 
      APIM_displaynameAPI: 
      APIM_PATH: 
      APIM_SWAGGERPATH: 
      APIM_TAGSAPI: 
      APIM_POLICIESALLOPERATIONSPATH: 
      AZ_INSTALL_STATUS: ms_repo_ok
      AZ_VERSION: latest
      INSTALL_PREREQUISITES: true
      AZ_LATEST_VERSION: 2.91.0
      environment: des
      repository_suffix: infranprd
      REPO: sigcn-med-worker
      JOB_ID: 169496
      ARGOCD_AUTH_TOKEN: ***
0s
0s
0s
0s
0s
0s
0s
0s
1s
0s
1s
0s



I1028 10:29:56.160227       1 version.go:31] "version info" version="" commit="0eef8df" buildDate="2025-05-19T06:17:15Z" component="vaultenv"
I1028 10:29:56.160380       1 main.go:184] "azure key vault env injector initializing"
I1028 10:29:56.160567       1 main.go:253] "found original container command" cmd="/usr/bin/dotnet" args=["dotnet","MedWorker.dll"]
I1028 10:29:56.160634       1 authentication.go:110] "checking if current auth service credentials are stale" url="http://akv2k8s-envinjector.akv2k8s.svc:80/auth/sigcn-med-worker/sigcn-med-worker-des-559fdd88f9-spcqz?secret=akv2k8s-sigcn-med-worker-des"
I1028 10:29:56.238711       1 authentication.go:123] "auth service credentials ok" url="http://akv2k8s-envinjector.akv2k8s.svc:80/auth/sigcn-med-worker/sigcn-med-worker-des-559fdd88f9-spcqz?secret=akv2k8s-sigcn-med-worker-des"
I1028 10:29:56.239040       1 authentication.go:159] "requesting azure key vault oauth token" url="https://akv2k8s-envinjector.akv2k8s.svc:9443/auth/sigcn-med-worker/sigcn-med-worker-des-559fdd88f9-spcqz"
I1028 10:29:56.267556       1 authentication.go:179] "successfully received oauth token"
I1028 10:29:56.407383       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="sigcn-med-worker/akvs-sigcn-med-worker-servicebus-connectionstrings-dev" env="AzureServiceBus__ConnectionString"
I1028 10:29:56.461307       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="sigcn-med-worker/akvs-sigcn-med-worker-redis-connectionstrings-dev" env="Redis__ConnectionString"
I1028 10:29:56.524257       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="sigcn-med-worker/akvs-sigcn-med-worker-cosmosdb-accountkey-dev" env="CosmosDB__AccountKey"
I1028 10:29:56.596017       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="sigcn-med-worker/akvs-sigcn-med-worker-cosmosdb-accountendpoint-dev" env="CosmosDB__AccountEndpoint"
I1028 10:29:56.654003       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="sigcn-med-worker/akvs-sigcn-med-worker-appinsights-connectionstring-dev" env="ApplicationInsights__ConnectionString"
I1028 10:29:56.707610       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="sigcn-med-worker/akvs-sigcn-med-worker-oauth-apikey-dev" env="OAuth__ApiKey"
I1028 10:29:56.762881       1 main.go:338] "secret injected into env var" azurekeyvaultsecret="sigcn-med-worker/akvs-sigcn-med-worker-oauth-clientsecret-dev" env="OAuth__ClientSecret"
I1028 10:29:56.762935       1 main.go:343] "starting process with secrets in env vars" cmd="/usr/bin/dotnet" args=["dotnet","MedWorker.dll"]
warn: Program[0]
      Environment: Development
warn: MedWorker.Workers.RelatoInfracaoProcessamentoWorker[0]
      Iniciando processo de leitura relatos
warn: MedWorker.Workers.RelatoInfracaoProcessamentoWorker[0]
      [RelatoInfracaoProcessamentoWorker.ProcessarMensagemAsync] - verificação se é uma mensagem valida
warn: MedWorker.Workers.RelatoInfracaoProcessamentoWorker[0]
      Model is valid: True
warn: MedWorker.Workers.RelatoInfracaoProcessamentoWorker[0]
      [RelatoInfracaoProcessamentoWorker.ProcessarMensagemAsync] - RELATOINFRACAO inicio do fluxo dos relatos.
warn: MedWorker.Services.RelatosInfracao.RelatoInfracaoServices[0]
      [RelatosInfracaoServices] - inicio do processamento
warn: MedWorker.Services.RelatosInfracao.RelatoInfracaoServices[0]
      [RelatosInfracaoServices] - Fluxo NI - inicio
warn: MedWorker.Services.RelatosInfracao.RelatoInfracaoServices[0]
      Processando...Gerando container para relatos de infração.
warn: MedWorker.Services.RelatosInfracao.RelatoInfracaoServices[0]
      Container Relato de Infracao atualizado
warn: MedWorker.Services.RelatosInfracao.RelatoInfracaoServices[0]
      Payload de envio ao SICLON gerado.
warn: MedWorker.Services.RelatosInfracao.RelatoInfracaoServices[0]
      [RelatosInfracaoServices] - Fluxo NI - fim
warn: MedWorker.Services.RelatosInfracao.RelatoInfracaoServices[0]
      [RelatosInfracaoServices] - Fluxo Bloqueio - inicio
warn: MedWorker.Services.RelatosInfracao.RelatoInfracaoServices[0]
      [RelatosInfracaoServices] - DesbloquearValores - inicio.
warn: MedWorker.Services.DesbloquearValores.DesbloqueioValoresServices[0]
      [DesbloqueioValoresServices] - DesbloquearValores - Obtendo dados do container meddevolucao pelo IdFimAFim - inicio.
warn: MedWorker.Services.DesbloquearValores.DesbloqueioValoresServices[0]
      [DesbloqueioValoresServices] - DesbloquearValores - Obtendo dados do container meddevolucao pelo IdFimAFim - fim.
warn: MedWorker.Services.DesbloquearValores.DesbloqueioValoresServices[0]
      [DesbloqueioValoresServices] - solitando Desbloqueio de Valores - inicio
warn: MedWorker.Services.DesbloquearValores.DesbloqueioValoresServices[0]
      [DesbloqueioValoresServices] - recebeu medRelatoInfracao.bloqueioValor.Bloqueio
warn: MedWorker.Services.DesbloquearValores.DesbloqueioValoresServices[0]
      [DesbloqueioValoresServices] - GerarPayloadDesbloqueioValores - gerou payload com sucesso
warn: MedWorker.Services.ContaDepositoBloqueioDesbloqueioValores.BloqueioDesbloqueioValoresServices[0]
      [BloqueioDesbloqueioValoresServices] - ConverterRequest - inicio.
warn: MedWorker.Services.ContaDepositoBloqueioDesbloqueioValores.BloqueioDesbloqueioValoresServices[0]
      [BloqueioDesbloqueioValoresServices] - ConverterRequest - fim.
warn: MedWorker.Services.ContaDepositoBloqueioDesbloqueioValores.ContaDepositoLancamentoApiClientKiota[0]
      [BloquearDesbloquearValoresAsync][PostAsync] post executado
warn: MedWorker.Services.ContaDepositoBloqueioDesbloqueioValores.ContaDepositoLancamentoApiClientKiota[0]
      [BloquearDesbloquearValoresAsync][PostAsync] IsSuccessStatusCode = false
fail: MedWorker.Services.DesbloquearValores.DesbloqueioValoresServices[0]
      [DesbloqueioValoresServices] - DesbloquearValores - Erro ao processar o desbloqueio de valores.
      MedWorker.Clients.ContaDepositoLancamentoEndpoints.Models.D01LancamentoOperationResponseRoot: Exception of type 'MedWorker.Clients.ContaDepositoLancamentoEndpoints.Models.D01LancamentoOperationResponseRoot' was thrown.
         at MedWorker.Services.ContaDepositoBloqueioDesbloqueioValores.ContaDepositoLancamentoApiClientKiota.BloquearDesbloquearValoresAsync(D01LancamentoRequest request, CancellationToken cancellationToken) in /app/MedWorker/Services/ContaDepositoBloqueioDesbloqueioValores/ContaDepositoLancamentoApiClientKiota.cs:line 62
         at MedWorker.Services.DesbloquearValores.DesbloqueioValoresServices.DesbloquearValores(String idFimaFim, CancellationToken cancellationToken, String eTag) in /app/MedWorker/Services/DesbloquearValores/DesbloqueioValoresServices.cs:line 92
warn: MedWorker.Services.RelatosInfracao.RelatoInfracaoServices[0]
      [RelatosInfracaoServices] - DesbloquearValores - fim.
warn: MedWorker.Services.RelatosInfracao.RelatoInfracaoServices[0]
      [RelatosInfracaoServices] - Fluxo Bloqueio - fim
warn: MedWorker.Workers.RelatoInfracaoProcessamentoWorker[0]
      [RelatoInfracaoProcessamentoWorker.ProcessarMensagemAsync] - RELATOINFRACAO houve retorno - fim do fluxo dos relato.
warn: MedWorker.Workers.RelatoInfracaoProcessamentoWorker[0]
      [RelatoInfracaoProcessamentoWorker.ProcessarMensagemAsync] - RELATOINFRACAO - sucesso - enviado para fila SICLON.
warn: MedWorker.Workers.RelatoInfracaoProcessamentoWorker[0]
      [RelatoInfracaoProcessamentoWorker.ProcessarMensagemAsync] - BLOQUEIOVALORES processado.
warn: MedWorker.Workers.RelatoInfracaoProcessamentoWorker[0]
      [RelatoInfracaoProcessamentoWorker.ProcessarMensagemAsync] - BLOQUEIOVALORES falha enviado para fila SICLON.


<img width="1663" height="939" alt="image" src="https://github.com/user-attachments/assets/a8a31932-31a4-4bb1-ac1b-c469a46f342b" />





	
