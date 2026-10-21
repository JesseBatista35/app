Run caixagithub/DevSecOps-Actions/.github/integrations/argocd/health@main
  with:
    ARGOCD_SERVER: https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io
    ARGOCD_APP: silce-gestao-operacional
    AMBIENTE: DES
    IMAGE_TAG: 39603505605
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
    REPO: silce-gestao-operacional
    JOB_ID: 166063
    ARGOCD_AUTH_TOKEN: ***
Logging image tag
0s
Run echo "INPUT_IMAGE_TAG: '39603505605'"
    echo "INPUT_IMAGE_TAG: '39603505605'"
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
      REPO: silce-gestao-operacional
      JOB_ID: 166063
      ARGOCD_AUTH_TOKEN: ***
  INPUT_IMAGE_TAG: '39603505605'
Aguardando processo de SYNC finalizar
10m 8s
Run for i in {1..30}; do
    for i in {1..30}; do
      STATUS=$(curl -s -X GET "https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io/api/v1/applications/silce-gestao-operacional-des" \
      -H "Authorization: ***")
    
      HEALTH=$(echo "$STATUS" | jq -r '.status.health.status')
      SYNCED=$(echo "$STATUS" | jq -r '.status.sync.status')
      PHASE=$(echo "$STATUS" | jq -r '.status.operationState.phase')
      TAG=$(echo "$STATUS" | jq -r '.status.summary.images[0]' | sed 's/.*://')
    
      echo "Tentativa $i - Phase: $PHASE, Health: $HEALTH, Sync: $SYNCED, Argo_Tag: $TAG, Image_Tag: 39603505605"
    
      if [[ "$PHASE" == "Running" ]]; then
        echo "Sync ainda em execução, aguardando..."
      fi
    
      if [[ "$PHASE" == "Failed" ]]; then
        echo "HEALTH_WAS_SUCCESSFUL=false" >> $GITHUB_OUTPUT
    
        echo "A sincronização falhou"
    
        exit 0
      fi
    
      if [[ "$PHASE" == "Succeeded" && "$HEALTH" == "Healthy" && "$SYNCED" == "Synced" && "$TAG" == "39603505605" ]]; then
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
      REPO: silce-gestao-operacional
      JOB_ID: 166063
      ARGOCD_AUTH_TOKEN: ***
  Tentativa 1 - Phase: null, Health: Healthy, Sync: Synced, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Tentativa 2 - Phase: null, Health: Healthy, Sync: Synced, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Tentativa 3 - Phase: null, Health: Healthy, Sync: Synced, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Tentativa 4 - Phase: Running, Health: Healthy, Sync: Synced, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Sync ainda em execução, aguardando...
  Tentativa 5 - Phase: Running, Health: Healthy, Sync: Synced, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Sync ainda em execução, aguardando...
  Tentativa 6 - Phase: Running, Health: Healthy, Sync: Synced, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Sync ainda em execução, aguardando...
  Tentativa 7 - Phase: Running, Health: Healthy, Sync: Synced, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Sync ainda em execução, aguardando...
  Tentativa 8 - Phase: Running, Health: Healthy, Sync: Synced, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Sync ainda em execução, aguardando...
  Tentativa 9 - Phase: Running, Health: Healthy, Sync: Synced, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Sync ainda em execução, aguardando...
  Tentativa 10 - Phase: Running, Health: Healthy, Sync: Synced, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Sync ainda em execução, aguardando...
  Tentativa 11 - Phase: Running, Health: Healthy, Sync: Synced, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Sync ainda em execução, aguardando...
  Tentativa 12 - Phase: Running, Health: Healthy, Sync: OutOfSync, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Sync ainda em execução, aguardando...
  Tentativa 13 - Phase: Running, Health: Healthy, Sync: OutOfSync, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Sync ainda em execução, aguardando...
  Tentativa 14 - Phase: Running, Health: Healthy, Sync: OutOfSync, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Sync ainda em execução, aguardando...
  Tentativa 15 - Phase: Succeeded, Health: Healthy, Sync: OutOfSync, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Tentativa 16 - Phase: Succeeded, Health: Progressing, Sync: Synced, Argo_Tag: 39463354047, Image_Tag: 39603505605
  Tentativa 17 - Phase: Succeeded, Health: Healthy, Sync: Synced, Argo_Tag: 39603505365, Image_Tag: 39603505605
  Tentativa 18 - Phase: Succeeded, Health: Healthy, Sync: Synced, Argo_Tag: 39603505365, Image_Tag: 39603505605
  Tentativa 19 - Phase: Succeeded, Health: Healthy, Sync: Synced, Argo_Tag: 39603505365, Image_Tag: 39603505605
  Tentativa 20 - Phase: Succeeded, Health: Healthy, Sync: Synced, Argo_Tag: 39603505365, Image_Tag: 39603505605
  Tentativa 21 - Phase: Succeeded, Health: Healthy, Sync: Synced, Argo_Tag: 39603505365, Image_Tag: 39603505605
  Tentativa 22 - Phase: Succeeded, Health: Healthy, Sync: Synced, Argo_Tag: 39603505365, Image_Tag: 39603505605
  Tentativa 23 - Phase: Succeeded, Health: Healthy, Sync: Synced, Argo_Tag: 39603505365, Image_Tag: 39603505605
  Tentativa 24 - Phase: Succeeded, Health: Healthy, Sync: Synced, Argo_Tag: 39603505365, Image_Tag: 39603505605
  Tentativa 25 - Phase: Succeeded, Health: Healthy, Sync: Synced, Argo_Tag: 39603505365, Image_Tag: 39603505605
  Tentativa 26 - Phase: Succeeded, Health: Healthy, Sync: Synced, Argo_Tag: 39603505365, Image_Tag: 39603505605
  Tentativa 27 - Phase: Succeeded, Health: Healthy, Sync: Synced, Argo_Tag: 39603505365, Image_Tag: 39603505605
  Tentativa 28 - Phase: Succeeded, Health: Healthy, Sync: Synced, Argo_Tag: 39603505365, Image_Tag: 39603505605
  Tentativa 29 - Phase: Succeeded, Health: Healthy, Sync: Synced, Argo_Tag: 39603505365, Image_Tag: 39603505605
  Tentativa 30 - Phase: Succeeded, Health: Healthy, Sync: Synced, Argo_Tag: 39603505365, Image_Tag: 39603505605


  <img width="1615" height="903" alt="image" src="https://github.com/user-attachments/assets/461756ed-0123-4560-8fee-0d1a7b77aa2f" />
