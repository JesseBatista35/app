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

SICCP-intra-config
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
SICCP-intra-config

etc
hosts-des
hosts-hmp
httpd
00-mpm.conf
httpd.conf
vhost.conf
jboss
configuration
properties
connector-log4j.xml
map-hmp.properties
map-piloto.properties
map-prd.properties
map.properties
siccp_intranet.xml
siranpkg.nbc.properties
sirot2.xml
custom-deploy.sh
custom.sh
java.security
jboss-custom.cli
jboss-deployments
jboss-modules-custom
standalone-full-ha.xml
standalone.conf
sigdb
des
run
hmp
prd
tqs

master

/
sigdb
/
des
/
run
run

Edit

Contents
History
Compare
Blame

12345678910
#  AgtSigdb -m<alias-desse-host> -h<ip-do-destino> -i<ip-desse-servidor>
#  onde:
#    nome-desse-host    -
#    ip-do-destino      -
#    ip-desse-servidor  -
LD_LIBRARY_PATH=/usr/lib
export LD_LIBRARY_PATH

umask 000
nohup ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111 &




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

SICCP-intra
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
SICCP-intra

.gitignore
file_url.txt

develop

/
Type to find a file or folder...
Files
failed

Clone

Contents
History

.gitignore
2 de set.
ba79b976
tratamento caracteres especiais Bruno Ronet Goncalves
file_url.txt
sexta-feira
a9a94b4e
Updated file_url.txt Bruno Ronet Goncalves



podemos criar uma branch de teste e aplicar a correção
