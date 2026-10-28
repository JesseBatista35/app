Skip to main content
Azure DevOps
projetos
/
Caixa
/
Pipelines
/
Releases
/
SICCP-intra
/
SICCP-intra-67
Search


Caixa

Overview

Boards

Repos

Pipelines
Pipelines
Environments
Releases
Library
Task groups
Deployment groups
Portal Infra

Test Plans

Artifacts
Project settings
SICCP-intra

SICCP-intra-67


EC DES

Partially succeeded


Pipeline

Tasks

Variables

Logs

Tests
Agent job
Started: 28/10/2026, 12:20:22
Pool:
Release-Linux
·
Agent: cadsvaprlx067.intra.caixa.gov.br

1h 45m 15s

Initialize job
·
succeeded
<1s

Pre-job: Download secure file
·
succeeded
<1s

Pre-job: Download secure file
·
succeeded
<1s

Pre-job: Download secure file
·
succeeded
<1s

Pre-job: Download secure file
·
succeeded
<1s

Pre-job: Download secure file
·
succeeded
<1s

Download Artifacts
·
succeeded
1 warning
1s

Exportando as variáveis do arquivo Trust Store
·
succeeded

<1s

Recupera VEC
·
succeeded
<1s

VEC - Aferição
·
succeeded
<1s

Exportar variáveis NFS
·
succeeded
<1s

Exportar variáveis Infrafácil
·
succeeded
<1s

Alocando o IP (AlocaIP e Infradevops)
·
succeeded
42s

Exporta as variáveis para o Terraform
·
succeeded
<1s

Replace tokens in **/*.tfvars.json **/*.tf
·
succeeded
<1s

Remove caracteres
·
succeeded
<1s

Install Terraform 1.3.5
·
succeeded
<1s

Terraform init
·
succeeded
6s

Terraform validate
·
succeeded
1s

Terraform workspace
·
succeeded
<1s

Terraform destroy
·
succeeded
<1s

Terraform apply
·
succeeded
16s

Definir size como executado
·
succeeded
13s

Cadastrar Servidor no Satellite
·
succeeded
9s

Valida Variáveis Obrigatórias
·
succeeded
<1s

Recuperando URL Pacote Nexus
·
succeeded
<1s

Recupera Pacote
·
succeeded
<1s

Recuperando nome do repositório
·
succeeded
<1s

Convertendo Minúsculo e Definindo nome do Projeto/Repositório
·
succeeded
<1s

Corrigindo Codificação Arquivos dos2unix
·
succeeded
<1s

Alterando Valores placeholders nos arquivos de config
·
succeeded
<1s

Valida XML JBOSS
·
succeeded
<1s

Git clone https://devops.caixa/projetos/Infraestrutura/_git/esteira-logs
·
succeeded
<1s

Cria Streams Graylog
·
succeeded
1s

Permissionamento LDAP
·
succeeded
18s

Configurando JBoss
·
succeeded
4s

Configurando Stack de Monitoração
·
1 error
33s
Bash exited with code '2'.

Configurando Logrotate
·
succeeded
9s

Configurando o Apache
·
succeeded
25s

Deploy Secure Files [JBOSS]
·
succeeded
8s

Deploy Config no JBOSS
·
succeeded
1h 40m 24s

Deploy Pacote no JBOSS
·
succeeded
18s

Check Deployments [JBOSS]
·
succeeded
6s

Atualizando versão no PortalIF
·
succeeded
<1s

Resumo da release
·
succeeded
49s

Instalar SIGDB
·
succeeded
14s

Finalize Job
·
succeeded
<1s
Showing 26 deployments

Row 13

Row 2

Row 2

Row 13

Row 2

Row 2

Row 3

Row 3

Expanded

Collapsed





o deploy passou nesse caso com ope no repo, temos que pdir ao time de desenvolvimento para analisr e fazer, me ajda co m anota para encaminhar na w.o
