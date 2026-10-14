Suporte para disponibilização do ambiente de DES do projeto SIARX Frontend Autoridade de Registro (siarx-frontend-autoridade-registro-x).
Atualmente, a esteira está apresentando erro durante a execução do build, especificamente na etapa “Docker Container Build”, conforme evidenciado na imagem anexa.
Apoio na análise e identificação da causa do erro, bem como nas orientações necessárias para possibilitar a conclusão do build e a disponibilização do ambiente de DES.

OBS: As informações passadas não foram suficientes para identificação do IC. A equipe técnica responsável deverá sanar esta pendência.



Skip to content
GitHub Enterprise
Users managed by Caixa Economica Federal
caixagithub
siarx-frontend-autoridade-registro-x
Repository navigation
Code
Issues
Pull requests
Actions
Projects
Wiki
Security and quality
63
 (63)
Insights
Settings
CI/CD Workflow Generic
caixagithub/siarx-frontend-autoridade-registro-x_main_37774800875.5 #5
All jobs
Run details
Annotations
1 error and 1 warning
CI_DES / ArgoCD_Deploy / ArgoCD_Deploy (DES)
failed last week in 1m 17s
Search logs
10s
0s
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
56s
0s
1s
Run caixagithub/DevSecOps-Actions/.github/integrations/argocd/pr@main
  with:
    ambiente: DES
    TOKEN_GITHUB: ***
    acr_name: acrcentralcaixanprd
    sigla: siarx
    modulo: frontend-autoridade-registro-x
    registry_url: acrcentralcaixanprd.azurecr.io
    image_dir: siarx/frontend-autoridade-registro-x/siarx-frontend-autoridade-registro-x
    image_tag: 37774800875
    github_org: caixagithub
    repository: siarx-frontend-autoridade-registro-x
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
Lower environment input
0s
Run environment=$(echo "$NON_PARSED_ENVIRONMENT" | tr '[:upper:]' '[:lower:]')
Verify Environment to set repo
0s
Run repository_suffix="infranprd"
  des
  repository_suffix=infranprd
Checkout Infra Repository
1s
Run actions/checkout@v5
  Syncing repository: caixagithub/siarx-frontend-autoridade-registro-x-infranprd
Getting Git version info
  Temporarily overriding HOME='/home/runner/_work/_temp/9ced492e-758e-4227-a372-6afc8d19e0f2' before making global git config changes
  Adding repository directory to the temporary git global config as a safe directory
  /usr/bin/git config --global --add safe.directory /home/runner/_work/siarx-frontend-autoridade-registro-x/siarx-frontend-autoridade-registro-x
  Deleting the contents of '/home/runner/_work/siarx-frontend-autoridade-registro-x/siarx-frontend-autoridade-registro-x'
Initializing the repository
Disabling automatic garbage collection
Setting up auth
Fetching the repository
Determining the checkout info
  /usr/bin/git sparse-checkout disable
  /usr/bin/git config --local --unset-all extensions.worktreeConfig
Checking out the ref
  /usr/bin/git log -1 --format=%H
  14bbaaaf9538b9f606475a03a5a503bcacbf55f4
Verify YAML File Exists
0s
Run echo `find . -name 'values.yaml'`
  
  Error: File des/values.yaml does not exist.
  Error: Process completed with exit code 1.
Check PR Creation Success
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
0s
0s
0s
0s
0s
0s
1s
0s
