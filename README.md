
Verificar Problema no ArgoCD deploy em DES Conforme Solicitado na REQ

https://github.com/caixagithub/sipgs-backend-bff-simulacao/actions/runs/38421067850/job/115379852691Criação solicitada por:REQ000095661629 Qual o tipo de serviço?: Ajustar ambiente ou parametrização de software

Skip to content
GitHub Enterprise
Users managed by Caixa Economica Federal
caixagithub
sipgs-backend-bff-simulacao
Repository navigation
Code
Issues
Pull requests
Actions
Projects
Wiki
Security and quality
2
 (2)
Insights
Settings
CI/CD Workflow Generic
caixagithub/sipgs-backend-bff-simulacao_develop_38421067850.7 #7
All jobs
Run details
Annotations
1 error and 1 warning
CI_DES / ArgoCD_Deploy / ArgoCD_Deploy (DES)
failed 20 hours ago in 11m 53s. View latest attempt.
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
49s
0s
7s
0s
0s
0s
4s
0s
0s
0s
0s
0s
21s
5s
0s
0s
1s
10m 4s
1s
Run caixagithub/DevSecOps-Actions/.github/integrations/argocd/logs@main
  with:
    ARGOCD_SERVER: https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io
    ARGOCD_APP: caixagithub/sipgs-backend-bff-simulacao
    AMBIENTE: DES
    IMAGE_TAG: 38421067850
    HEALTH_CHECK_WAS_SUCCESSFUL: false
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
    REPO: sipgs-backend-bff-simulacao
    JOB_ID: 161420
    ARGOCD_AUTH_TOKEN: ***
Formate ARGO REPOSITORY
0s
Run echo "REPO_NAME=$(echo 'caixagithub/sipgs-backend-bff-simulacao' | cut -d'/' -f2)" >> $GITHUB_ENV
  INPUT_IMAGE_TAG: '38421067850'
Coletando logs dos pods
0s
Run RESOURCE_TREE_URL="https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io/api/v1/applications/sipgs-backend-bff-simulacao-des/resource-tree?appNamespace=openshift-gitops"
  Fazendo requisição para: https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io/api/v1/applications/sipgs-backend-bff-simulacao-des/resource-tree?appNamespace=openshift-gitops
  Resource-tree obtido com sucesso
  Filtrando pods e encontrando o mais recente...
  Pod mais recente encontrado: sipgs-backend-bff-simulacao-des-844cbb5c66-mdjgw
  URL dos logs: https://openshift-gitops-server-openshift-gitops.apps.aroidpprd.brazilsouth.aroapp.io/api/v1/applications/sipgs-backend-bff-simulacao-des/logs?appNamespace=openshift-gitops&container=sipgs-backend-bff-simulacao-des&namespace=sipgs-backend-bff-simulacao&follow=false&podName=sipgs-backend-bff-simulacao-des-844cbb5c66-mdjgw&tailLines=1000&sinceSeconds=0
  Logs obtidos com sucesso
  Logs do pod sipgs-backend-bff-simulacao-des-844cbb5c66-mdjgw:
  ================================================
  Exibindo os Logs:
  container "sipgs-backend-bff-simulacao-des" in pod "sipgs-backend-bff-simulacao-des-844cbb5c66-mdjgw" is waiting to start: trying and failing to pull image
  
  ================================================
  Script executado com sucesso!
  Pod utilizado: sipgs-backend-bff-simulacao-des-844cbb5c66-mdjgw
  Falha na sincronização
  Error: Process completed with exit code 1.
0s
0s
0s
0s
0s
0s
0s
0s
0s
6s
0s
