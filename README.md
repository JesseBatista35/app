Skip to main content
Azure DevOps
projetos
/
Caixa
/
Repos
/
Files
/

SIGSJ-boleto-config
Search


Caixa

Overview

Boards

Repos
Files
Commits
Pushes
Branches
Tags
Pull requests

Pipelines

Test Plans

Artifacts
Project settings
SIGSJ-boleto-config

configuration
properties
b2b.properties
config.properties
release.properties
sigsj_ws_boleto.xml
custom.sh
httpd
httpd.conf
vhost.conf
jboss
jboss-custom.cli
jboss-modules-custom
standalone-full-ha.xml
standalone.conf
README.md

master

/
Type to find a file or folder...
Files
succeeded

Clone

Contents
History

configuration
7m ago
25b377e5
Renamed sigsj_boleto.xml to sigsj_ws_boleto.xml Thiago Jeferson de Sousa Silva

httpd
21 de out.
a4c5c553
Added vhost.conf Thiago Jeferson de Sousa Silva
jboss
23m ago
6597f15d
Deleted custom.sh Thiago Jeferson de Sousa Silva
README.md
10 de nov. de 2023
1d39e649
Primeiro commit Rafael Augusto Soares
Exemplo de Repositório de Configuração para JBOSS (VM)
Esse repositório está organizado por pastas

Pastas Disponíveis
ansible
httpd
jboss
so
Para novos sistemas utilizar essa estrutura de pastas. Obs: A antiga estrutura ainda irá funcionar, mas futuramente será descontinuada

Template JBOSS EAP
Template de config utilizado com as aplicações Jboss em VM

Arquivos
/jboss/standalone-full-ha.xml (Obrigatório)
/jboss/standalone.conf (Obrigatório)
/jboss/jboss-deployments (Opcional)
/jboss/jboss-custom.cli (Opcional)
/jboss/jboss-modules-custom (Opcional)
/jboss/configuration/custom.sh (Opcional)
/httpd/httpd.conf (Opcional)
/httpd/vhost.conf (Opcional)
/httpd/00-mpm.conf (Opcional)
/httpd/00-proxy.conf (Opcional)
/so/etc/host-{{ ambiente }} (Opcional)
/ansible/groups_var/{{ grupo_variavel }} (Opcional)
/ansible/inventory/{{ grupo_inventário }} (Opcional)
/jboss/standalone-full-ha.xml
Arquivo responsável pelas configurações básicas do sistema com datasource, logs, system-properties, filas MQ, entre outros.

/jboss/standalone.conf
Arquivo responsável pelas configurações iniciais do JBOSS como memoria a ser utilizada, inicialização de bibliotecas, jks, configurações de proxy entre outras.

/jboss/jboss-deployments
Arquivo responsável por adicionar Deployments adicionais que não estão disponíveis por padrão nas imagens das VMs. Conforme descrito na WIKI

/jboss/jboss-custom.cli
Arquivo responsável por executar alguma configuração adcional via jboss-cli.

/jboss/jboss-modules-custom
Arquivo responsável por adicionar Módulos adicionais que não estão disponíveis por padrão nas imagens das VMs.

/jboss/configuration/custom.sh
Arquivo responsável por executar um script customizado em bash.

/httpd/httpd.conf
O arquivo "httpd.conf" é usado para definir as diretrizes que o Apache segue ao iniciar e executar, e também fornece aos administradores de sistemas a capacidade de personalizar o comportamento do Apache para atender às suas necessidades específicas. Algumas das configurações comuns incluem a porta que o Apache escuta, o local dos arquivos de log, a configuração de virtual hosts, entre outros.

/httpd/vhost.conf
O arquivo "vhost.conf" é responsável para customizar as configurações do apache.

/httpd/00-mpm.conf
O arquivo 00-mpm.conf é usado para configurar o MPM (Mod_Process_Management) do Apache. O MPM é responsável por gerenciar as solicitações HTTP para o servidor Apache e determinar como os processos serão gerenciados e escalados para atender a essas solicitações. O arquivo 00-mpm.conf permite que você configure o MPM do Apache para suas necessidades específicas.

/httpd/00-proxy.conf
Arquivo responsável para habilitar e desabilitar módulos especificos do proxy.

/so/etc/host-{{ ambiente }}
Arquivo responsável para acrescentar/modificar o arquivo de hosts do sistema operacional de acordo com o ambiente (des,tqs,hmp,prd).

/ansible/groups_var/{{ grupo_variavel }}
Arquivo responsável por alterar os grupos de variáveis para grupos específicos que contém variáveis que não se aplicam ao padrão da esteira.

/ansible/inventory/{{ grupo_inventário }}
Arquivo responsável por alterar os grupos de inventário para grupos específicos que contém invetários que não se aplicam ao padrão da esteira.





fizemos a correçao novo deploy masi nao pegou

Skip to main content
Azure DevOps
projetos
/
Caixa
/
Repos
/
Files
/

SIGSJ-boleto-config
Search


Caixa

Overview

Boards

Repos
Files
Commits
Pushes
Branches
Tags
Pull requests

Pipelines

Test Plans

Artifacts
Project settings
SIGSJ-boleto-config

configuration
properties
b2b.properties
config.properties
release.properties
sigsj_ws_boleto.xml
custom.sh
httpd
httpd.conf
vhost.conf
jboss
jboss-custom.cli
jboss-modules-custom
standalone-full-ha.xml
standalone.conf
README.md

master

/
Type to find a file or folder...
Files
succeeded

Clone

Contents
History


Renamed sigsj_boleto.xml to sigsj_ws_boleto.xml
25b377e5
Thiago Jeferson de Sousa Silva
Today at 16:22
succeeded
Added release.properties
3582c3b6
Thiago Jeferson de Sousa Silva
Today at 16:09
succeeded
Added b2b.properties
faa3115b
Thiago Jeferson de Sousa Silva
Today at 16:08
Added config.properties
6107f061
Thiago Jeferson de Sousa Silva
Today at 16:08
Added sigsj_boleto.xml
afc28ab9
Thiago Jeferson de Sousa Silva
Today at 16:07
Added custom.sh
fe8fb57a
Thiago Jeferson de Sousa Silva
Today at 16:06
Deleted custom.sh
6597f15d
Thiago Jeferson de Sousa Silva
Today at 16:06
Added custom.sh
3ec60420
Jesse Mouta Pereira Batista
12 de nov. at 16:54
Atualiza configuracao do standalone-full-ha
75a6be4d
f658838
3 de nov. at 12:34
succeeded
Updated standalone-full-ha.xml
96180f78
Jesse Mouta Pereira Batista
22 de out. at 14:59
failed
Deleted jboss-deployments
d65ddcfb
Jesse Mouta Pereira Batista
22 de out. at 14:56
Updated standalone-full-ha.xml
9a403534
Thiago Jeferson de Sousa Silva
21 de out. at 15:35
failed
Updated standalone-full-ha.xml
871e8f76
Thiago Jeferson de Sousa Silva
21 de out. at 15:19
failed

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
SIGSJ-boleto
/
SIGSJ-boleto-25
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
SIGSJ-boleto

SIGSJ-boleto-25


EC DES

Succeeded


Pipeline

Tasks

Variables

Logs

Tests
Agent job
Started: 19/11/2026, 16:22:31
Pool:
Release-Linux
·
Agent: cadsvaprlx070.intra.caixa.gov.br

4m 26s

Initialize job
·
succeeded
1s

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
1s

Recupera VEC
·
succeeded
1s

VEC - Aferição
·
succeeded
1 warning
<1s

Exportar variáveis NFS
·
succeeded
<1s

Exportar variáveis Infrafácil
·
succeeded
1s

Alocando o IP (AlocaIP e Infradevops)
·
succeeded
13s

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
1s

Terraform init
·
succeeded
7s

Terraform validate
·
succeeded
1s

Terraform workspace
·
succeeded
1s

Terraform destroy
·
succeeded
<1s

Terraform apply
·
succeeded
17s

Definir size como executado
·
succeeded
23s

Cadastrar Servidor no Satellite
·
succeeded
10s

Valida Variáveis Obrigatórias
·
succeeded
<1s

Recuperando URL Pacote Nexus
·
succeeded
1s

Recupera Pacote
·
succeeded
1s

Recuperando nome do repositório
·
succeeded
1s

Convertendo Minúsculo e Definindo nome do Projeto/Repositório
·
succeeded
<1s

Corrigindo Codificação Arquivos dos2unix
·
succeeded
1s

Alterando Valores placeholders nos arquivos de config
·
succeeded
<1s

Valida XML JBOSS
·
succeeded
1s

Git clone https://devops.caixa/projetos/Infraestrutura/_git/esteira-logs
·
succeeded
1s

Cria Streams Graylog
·
succeeded
3s

Permissionamento LDAP
·
succeeded
19s

Configurando JBoss
·
succeeded
5s

Configurando Stack de Monitoração
·
succeeded
43s

Configurando Logrotate
·
succeeded
9s

Configurando o Apache
·
succeeded
21s

Deploy Secure Files [JBOSS]
·
succeeded
6s

Deploy Config no JBOSS
·
succeeded
39s

Deploy Pacote no JBOSS
·
succeeded
8s

Check Deployments [JBOSS]
·
succeeded
7s

Atualizando versão no PortalIF
·
succeeded
<1s

Resumo da release
·
succeeded
<1s

Finalize Job
·
succeeded
<1s
Expanded

Collapsed

Row 2


[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]# ls -la /opt/jboss-eap/standalone/configuration/properties/
total 8
drwxr-xr-x 2 jboss jboss   30 nov 19 16:26 .
drwxrwxr-x 4 jboss jboss 4096 nov 19 16:17 ..
-rwxr-xr-x 1 jboss jboss  776 nov 19 16:17 sigsj_boleto.xml
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]# ls -la /opt/jboss-eap/standalone/configuration/properties/
total 8
drwxr-xr-x 2 jboss jboss   30 nov 19 16:26 .
drwxrwxr-x 4 jboss jboss 4096 nov 19 16:17 ..
-rwxr-xr-x 1 jboss jboss  776 nov 19 16:17 sigsj_boleto.xml
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
