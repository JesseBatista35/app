Bom dia, 

Estamos tentando subir uma nova release para a aplicação em TQS (https://devops.caixa/projetos/Caixa/_release?_a=releases&view=mine&definitionId=6335 e https://devops.caixa/projetos/Caixa/_release?_a=releases&view=mine&definitionId=6334), mas ocorre o erro em anexo ao abrir a aplicação em https://sihdg-angular18-tqs.apps.nprd.caixa/.
Além disso, a url está apontando para https://login.des.caixa/ ao invés de https://login.tqs.caixa/, na hora da autentição via SSO.
Foram feitas algumas mudanças recentemente para resolver um outro problema relacionado a banco de dados, talvez tenha algo a ver: REQ000146641425

Att, 

Anderson Nascimento.


tiveram essas analisess

Histórico de Informações de Trabalho da Ordem de Trabalho
ID da Ordem de Trabalho	 WO0000081943454
Criado em	 15/10/2026 16:51:43
Criado por	 P537007
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 O valid redirect esta corretamente inserido no SSO TQS Intranet.

Atenciosamente,
Eduardo Silva - Analista de Segurança P537007
Plataforma Intermediária
HITSS/CEPRO20 - Identidade e acesso
ID da Ordem de Trabalho	 WO0000081943454
Criado em	 15/10/2026 12:12:35
Criado por	 P730708
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Demanda inicial com viés de falha, erro, degradação ou esgotamento de infraestrutura, serviço, máquina, armazenamento, rotina ou situação que esteja na iminência de tornar-se incidente. Previsto atendimento no prazo indicado pelo demandante.
[CENTRAL-SID]
ID da Ordem de Trabalho	 WO0000081943454
Criado em	 15/10/2026 11:31:36
Criado por	 P564449
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Bom dia, Anderson.

Conforme verificamos, o erro apresentado é de "redirect_uri" onde a comunidade solicita o cadastramento da url junto ao SSO de TQS com o time de Segurança.

Sendo assim, encaminho a WO para o time de Segurança para verificação do erro em questão.

Qualquer dúvida estou à disposição.

At.te,
Kallebe M. Vieira
Analista
CTIS / CESTI Esteira DEVOPS DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081943454
Criado em	 15/10/2026 11:12:57
Criado por	 P558217
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezado(a),



Informamos que sua solicitação foi recebida.  



Nosso SLA para atendimento é de até 24h úteis, analisaremos a solicitação para nos certificarmos que o atendimento está dentro do escopo de atuação da nossa equipe.



Caso seja identificado que o atendimento não corresponde ao nosso escopo, a solicitação será redirecionada à equipe responsável.



Novas informações e atualizações serão registradas diretamente nesta WO.



Atte.



Esteira Devops DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081943454
Criado em	 15/10/2026 11:08:44
Criado por	 C161491
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Anexo do Registro de Solicitação.
Impresso por P585600 em Sexta-feira, 16/10/2026 09:42:47



<img width="1889" height="981" alt="image" src="https://github.com/user-attachments/assets/f829e4fa-a812-4bf5-b940-cc8c32bc3d93" />



a sandra disse isso



Oi Jesse Mouta Pereira Batista! Tudo joia?
 
Muito ocupado?
 
Sandra de Sousa Santos. bom dia tudo bem e com a senhora? estou em uma sala aqui rsrs
 
mais mandar aqui
 
		Ao acessar o frontend Angular 18 TQS, a autenticação retorna o erro "Parâmetro inválido: redirect_uri". 

		Já validamos que a URL do Angular 18 está cadastrada nos Valid Redirect URIs do cliente no SSO. 

		Poderiam, por favor, verificar qual valor de redirect_uri está sendo enviado na requisição e de onde a aplicação está carregando a configuração do domínio de autenticação? 

		Aparentemente, o problema não está no cadastro do cliente no SSO, mas na configuração utilizada pela aplicação durante o login.
 
certo, vou dar uma olhada
 
manda pra mim o projeto
 
https://sihdg-angular18-tqs.apps.nprd.caixa/
 
Estou indo em uma consulta agora assim que retornar verifico. 
 
Sandra de Sousa Santos
https://sihdg-angular18-tqs.apps.nprd.caixa/
o problema é: uso essa url de TQS e a aplicação está  autenticando em DES (login.des)
frontend -> TQS
SSO -> DES
 
não achamos como isso está acontecendo
 
 
Oie
 
Acho que conseguimos desvendar o mistério --> o problema está no arquivo de configurações STANDALONE
 
olá Sandra bom dia, desculpa ontem acabou enrolando no exame ontem e só cheguei depois do horario
 
vou dar uma olhada aqui para ver se consigo ajudar voces



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

SIHDG-angular18-config
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
SIHDG-angular18-config

sihdg-nginx.conf

master

/
sihdg-nginx.conf
sihdg-nginx.conf

Edit

Contents
History
Compare
Blame

123456789
location /api/ {
    client_max_body_size 10M;
    proxy_set_header X-Forwarded-Host $host;
    proxy_set_header X-Forwarded-Server $host;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_pass __HTTP_SERVICE_API__; 
    proxy_redirect off;
    server_tokens off;
}





 
location /api/ {
    client_max_body_size 10M;
    proxy_set_header X-Forwarded-Host $host;
    proxy_set_header X-Forwarded-Server $host;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_pass __HTTP_SERVICE_API__; 
    proxy_redirect off;
    server_tokens off;
}


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

SIHDG-angular18
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
SIHDG-angular18

src
app
assets
environments
environment.cast.ts
environment.des.ts
environment.srv.ts
environment.ts
tests
favicon.ico
index.html
main.ts
polyfills.ts
typings.d.ts
.editorconfig
.gitignore
.npmrc
angular.json
debug.log
gulpfile.ts
jest.config.ts
package-lock.json
package.json
protractor.conf.js
README copy.md
README.md
relatorio-curvas.component.css
setup-jest.ts
sonar-project.properties
tsconfig.app.json
tsconfig.json
tsconfig.spec.json
tslint.json

3.22.0.0

/
Type to find a file or folder...
Files

Clone

Contents
History

.s2i
18 de jun.
8baddeb6
initial commit Anderson Nascimento
.vscode
18 de jun.
8baddeb6
initial commit Anderson Nascimento
e2e
18 de jun.
8baddeb6
initial commit Anderson Nascimento
reports
8 de out.
249407eb
Fix: identação dos campos de data Anderson Nascimento
src
Yesterday
fc529993
ajuste no painel efetividade Nelson Silva dos Santos
.editorconfig
18 de jun.
8baddeb6
initial commit Anderson Nascimento
.gitignore
18 de jun.
8baddeb6
initial commit Anderson Nascimento
.npmrc
30 de jul.
2a96bff5
Update versões para suportar angular 19 Anderson Nascimento
angular.json
10 de ago.
157f03d1
Configs de environment Anderson Nascimento
debug.log
18 de jun.
8baddeb6
initial commit Anderson Nascimento
gulpfile.ts
18 de jun.
8baddeb6
initial commit Anderson Nascimento
jest.config.ts
10 de ago.
7f8f2320
Fix cobertura do setup.component Anderson Nascimento
package-lock.json
11 de ago.
88adc765
feature: Conteudo da aplicação se adapta quando o Menu Lateral é aberto + mel... Anderson Nascimento
package.json
11 de ago.
88adc765
feature: Conteudo da aplicação se adapta quando o Menu Lateral é aberto + mel... Anderson Nascimento
protractor.conf.js
18 de jun.
8baddeb6
initial commit Anderson Nascimento
README copy.md
18 de jun.
8baddeb6
initial commit Anderson Nascimento
README.md
19 de mar. de 2024
45559b40
Added README.md Rafael Augusto Soares
relatorio-curvas.component.css
18 de jun.
8baddeb6
initial commit Anderson Nascimento
setup-jest.ts
5 de ago.
17098948
checkpoint: configuração dos mocks e specs Anderson Nascimento
sonar-project.properties
10 de ago.
7f8f2320
Fix cobertura do setup.component Anderson Nascimento
tsconfig.app.json
6 de ago.
e02eb8e1
fix configs Anderson Nascimento
tsconfig.json
6 de ago.
758fe578
Configuração completa: testes unitários Anderson Nascimento
tsconfig.spec.json
5 de ago.
b12beef7
checkpoint: testes configurados para o jest Anderson Nascimento
tslint.json
18 de jun.
8baddeb6
initial commit Anderson Nascimento
Introduction
TODO: Give a short introduction of your project. Let this section explain the objectives or the motivation behind this project.

Getting Started
TODO: Guide users through getting your code up and running on their own system. In this section you can talk about:

Installation process
Software dependencies
Latest releases
API references
Build and Test
TODO: Describe and show how to build your code and run the tests.

Contribute
TODO: Explain how other users and developers can contribute to make your code better.

If you want to learn more about creating good readme files then refer the following guidelines . You can also seek inspiration from the below readme files:

ASP.NET Core 
Visual Studio Code 
Chakra Core 
Showing 2 items.

Showing 1 filtered items.

Showing 1 filtered items.

Showing 1 filtered items.

Showing 1 filtered items.

Showing 1 filtered items.

Showing 1 filtered items.

Showing 1 filtered items.

Showing 1 filtered items.

Showing 2 filtered items.

Collapsed
