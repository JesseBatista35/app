Rafael Augusto Soares, boa tarde tudo bem?
 
Estou com o SIGSJ (intranet, internet e boleto) na esteira-jboss-vm-v2 e fiquei com uma dúvida sobre o custom.sh.
 
As aplicações precisam de um XML de log4j externo em /log_jboss/config-log4j/ (igual ao legado). A ideia era entregar isso via custom.sh no repositório de config, mas olhando a esteira vi que:


O stack_custom.yml só executa o {{ jboss_home }}/standalone/configuration/custom.sh se ele já existir na VM;

Na task "Deploy Config no JBOSS" são copiados do repo de config o standalone-full-ha.xml, o standalone.conf, o jboss-custom.cli, o jboss-deployments e o jboss-modules-custom, mas não encontrei cópia do custom.sh.
 
Coloquei o custom.sh na pasta jboss/ do repo de config e, na release, a task "Verifica se o arquivo .../custom.sh existe" passa, mas a execução é pulada porque o arquivo não chega na VM.
 
Dúvidas:


1. Existe uma forma suportada de entregar o custom.sh pelo repo de config para VMs com JBoss? Se sim, em qual pasta ele deve ficar?

2. Se hoje ele for só manual na VM, faz sentido a esteira copiar o jboss/custom.sh do repo de config (como faz com o standalone.conf), com permissão de execução, antes de executar?
 
Por enquanto apliquei a configuração manualmente nas VMs de DES para destravar, Valeu!
 
Boa tarde!
 
tudo bem e vc?
 
a esteira já faz a copia desse arquivo do repositorio de config
 
basta estar no lugar correto
 
copia a estrutura desse aqui;
https://devops.caixa/projetos/Caixa/_git/SIGCX-config
 
Rafael Augusto Soares
tudo bem e vc?
tudo bem graças a Deus. muito obrigado. vou conferir lá.
 
de nada!




 sobre isso vamos la 

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

SIGCX-config
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
SIGCX-config

ansible
configuration
etc
httpd
jboss-custom.cli
jboss-deployments
jboss-modules-custom
standalone-full-ha.xml
standalone.conf

master

/
Type to find a file or folder...
Files
failed

Clone

Contents
History

ansible
11 de mar.
d1393d11
Updated ctc_prod1 Thiago Jorge Araujo
configuration
19 de fev.
27972a93
Updated custom.sh Claudio Monteiro Lima
etc
9 de fev.
7d191b20
Added hosts-des Claudio Monteiro Lima
httpd
6 de fev.
cae711ba
Added vhost.conf Claudio Monteiro Lima
jboss-custom.cli
6 de fev.
3715942f
Updated jboss-custom.cli Claudio Monteiro Lima
jboss-deployments
5 de fev.
c1676a2a
Updated jboss-deployments Claudio Monteiro Lima
jboss-modules-custom
6 de fev.
3101152b
Updated jboss-modules-custom Claudio Monteiro Lima
standalone-full-ha.xml
10 de fev.
c4e9af51
Correções standalone-full-ha.xml Claudio Monteiro Lima
standalone.conf
13 de fev.
57d9d711
Updated standalone.conf Claudio Monteiro Lima



com oque agente descobre como ele fucniona

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
SIGCX
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
All pipelines

SIGCX

SIGCX
Predefined variables
Filter by keywords
Scope


AMBIENTE
DES
AMBIENTE
DES
AMBIENTE
DES
AMBIENTE
DES
AMBIENTE
DES
AMBIENTE
DES
AMBIENTE
DES
AMBIENTE
DES
AMBIENTE
DES
AMBIENTE
DES
AMBIENTE
DES
AMBIENTE
DES
AMBIENTE
DES
AMBIENTE
DES
AMBIENTE
DES
AMBIENTE
TQS
AMBIENTE
TQS
AMBIENTE
PRD
CGC_UNIDADE_DES
7390
CGC_UNIDADE_OPS
7259
http_context_additional
http_context_default
sigcx
http_sso
no
produto_nome_vm
Jboss
produto_versao_vm
7.4
sistema_ambiente
des
sistema_ambiente
des
sistema_ambiente
des
sistema_ambiente
des
sistema_ambiente
des
sistema_ambiente
des
sistema_ambiente
des
sistema_ambiente
des
sistema_ambiente
des
sistema_ambiente
des
sistema_ambiente
des
sistema_ambiente
des
sistema_ambiente
des
sistema_ambiente
des
sistema_ambiente
des
sistema_ambiente
tqs
sistema_ambiente
tqs
sistema_ambiente
hmp
sistema_ambiente
prd
sistema_ambiente
prd
sistema_ambiente
prd
sistema_ambiente
prd
sistema_ambiente
prd
sistema_ambiente
prd
sistema_ambiente
prd
sistema_ambiente
prd
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm-piloto
sistema_nome
sigcx-farm-piloto
sistema_nome
sigcx-farm-piloto
sistema_nome
sigcx-farm-piloto
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
sistema_nome
sigcx-farm
SISTEMAAMBIENTE
DES
SISTEMAAMBIENTE
DES
SISTEMAAMBIENTE
DES
SISTEMAAMBIENTE
DES
Expanded

Expanded

Collapsed

Collapsed

Collapsed

Expanded

375 pipelines found

Select a release pipeline to view its releases

12 pipelines found

Row 2

Showing filters 1 through 2

