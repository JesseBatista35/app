
sh-5.1$ cd /tmp && python3 - <<'EOF'
import zipfile, io
ear = zipfile.ZipFile('/opt/server/standalone/deployments/sihdg-3.22.0.1.ear')
war = zipfile.ZipFile(io.BytesIO(ear.read('sihdg-api.war')))
for z in (ear, war):
    for n in z.namelist():
        if n.endswith(('pom.properties','MANIFEST.MF')): print('==',n); print(z.read(n).decode(errors='ignore'))
EOF
== META-INF/MANIFEST.MF
Manifest-Version: 1.0
Created-By: Maven EAR Plugin 3.3.0
Build-Jdk-Spec: 21


== META-INF/maven/br.gov.caixa.bsb.sihdg/sihdg/pom.properties
artifactId=sihdg
groupId=br.gov.caixa.bsb.sihdg
version=3.22.0.1

== META-INF/MANIFEST.MF
Manifest-Version: 1.0
Created-By: Maven WAR Plugin 3.4.0
Build-Jdk-Spec: 21


== META-INF/maven/br.gov.caixa.bsb.sihdg/sihdg-api/pom.properties
artifactId=sihdg-api
groupId=br.gov.caixa.bsb.sihdg
version=3.22.0.1

sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$

<img width="1620" height="860" alt="image" src="https://github.com/user-attachments/assets/000152f7-61d2-44ed-9c3b-d4b737995015" />


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

SIHDG-backend-config
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
SIHDG-backend-config

azure-pipelines.yml
sihdg-backend-pv.yaml
sihdg-backend-pvc.yaml
standalone-okd.xml
standalone.conf

master

/
Type to find a file or folder...
Files
failed

Clone

Contents
History

azure-pipelines.yml
14 de mai. de 2024
76008437
Set up CI with Azure Pipelines Marcos Coimbra Osorio
sihdg-backend-pv.yaml
31 de ago. de 2022
9fa9413f
Renamed sihdg-pv.yaml to sihdg-backend-pv.yaml Rafael Augusto Soares
sihdg-backend-pvc.yaml
31 de ago. de 2022
e3810f4f
Renamed sihdg-pvc.yaml to sihdg-backend-pvc.yaml Rafael Augusto Soares
standalone-okd.xml
19 de ago. de 2024
86ea59be
Updated standalone-okd.xml Nelson Silva dos Santos
standalone.conf
7 de jun. de 2024
cb97f159
Updated standalone.conf Roberto de Souza Rodrigues



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

SIHDG-backend
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
SIHDG-backend

api
core
docs
ear
outros
src
main
webapp
WEB-INF

jboss-web.xml
index.jsp
.gitignore
cast-ci-config.json
pom.xml
README.md

master

/
Type to find a file or folder...
Files
failed

Clone

Contents
History

api
12 de nov. de 2024
8267ebb1
ajustes do sonar nelson.santos
core
12 de nov. de 2024
f95fb43b
versionando para 0.0.0.80 nelson.santos
docs
18 de mai. de 2022
3ffb371c
Migrando branch do ALM para o DEVOPS Edilson Batista de Souza Filho
ear
12 de nov. de 2024
f95fb43b
versionando para 0.0.0.80 nelson.santos
outros
26 de fev. de 2024
448c7b5b
Equalização com a sprint 23 do ALM nelson.santos
src
12 de nov. de 2024
8267ebb1
ajustes do sonar nelson.santos
.gitignore
18 de mai. de 2022
3ffb371c
Migrando branch do ALM para o DEVOPS Edilson Batista de Souza Filho
cast-ci-config.json
18 de mai. de 2022
3ffb371c
Migrando branch do ALM para o DEVOPS Edilson Batista de Souza Filho
pom.xml
12 de nov. de 2024
f95fb43b
versionando para 0.0.0.80 nelson.santos
README.md
18 de mai. de 2022
3ffb371c
Migrando branch do ALM para o DEVOPS Edilson Batista de Souza Filho
Adequação de Environments
Foi feita uma adequação para que o front-end não dependa mais de múltiplos environments e builds para diferentes ambientes. Agora os environments estão agrupados da seguinte forma:

Local: para desenvolvimento local com o front-end rodando em http://localhost:4200  e o back-end em http[s]😕/localhost:8080/sihdg-api/ . Nesse caso, como não há uma correspondência relativa entre as duas URL's, são utilizadas as seguintes configurações:

backendUrlFromFrontend: false
backendHttps: [true/false] => preencher conforme o uso do JBoss
backendPort: [8443/8080] => preencher conforme o uso do JBoss
Servidor: para implantação em ambientes centralizados de testes, homologação, produção, seja na Cast ou no cliente. Nesse caso, o front-end estará rodando em alguma URL http[s]😕/.../sihdg/ e o front-end na URL http[s]😕/.../sihdg-api/ . Nesse caso, como existe uma correspondência das URL's dos dois módulos do sistema (o prefixo é exatamente o mesmo), são utilizadas as seguintes configurações:

backendUrlFromFrontend: true
backendHttps: [...] => essa configuração é ignorada
backendPort: [...] => essa configuração é ignorada
Os comandos de geração de build continuaram os mesmos.

Arquitetura - Versão 1.3
Adequação da Autenticação / Autorização do projeto para utilizar o AIM Keycloak. A versão utilizada do Keycloak é a 2.5.4, que corresponde ao Red Hat SSO 7.1 . Comparando com a arquitetura anterior, uma diferença fundamental é que a arquitetura anterior gerava, validava e renovava o token de acesso JWT internamente, mas agora essas operações são todas realizadas pelo Keycloak. Além disso, o Keycloak trabalha com fluxos de autenticação e pode fazer uso de outros tokens, como de refresh ou identificação, para complementar a lógica de interação adotada. Uma observação importante é que a lógica de interação com o LDAP foi inteiramente removida do projeto, pois, o único responsável por interagir com o LDAP de agora em diante é o Keycloak.

Para manter facilidade de uso e um padrão em comparação com os outros serviços, foi montado um Keycloak embedded, que pode ser facilmente configurado via um arquivo de configurações. No entanto, como o Keycloak é uma aplicação pronta, ou seja, possui uma arquitetura para rodar como uma aplicação independente, ele não pode ser incluído como parte do código fonte de outro projeto. Portanto, foi criado um projeto a parte, que está no repositório "aim-keycloak", branch master, do Gitlab da Cast. Esse projeto deverá ser baixado e importado ao Eclipse, sendo que consiste dos seguintes arquivos principais:

\Implementação\src\main\resources\settings.yml: arquivo de configurações que define todos os realms, clientes, perfis e usuários que existirão no domínio do Keycloak

\Implementação\src\main\java\br\gov\caixa\arquitetura\comum\seguranca\keycloak\KeycloakBoot.java: classe de inicialização que executa o Keycloak (possui um método main( ) para execução direta, não precisa de JBoss)

O fluxo de autenticação do Keycloak adotado é o Authorization Code, descrito a seguir:

A aplicação percebe que o usuário não está logado e o redireciona ao Keycloak;
O usuário entra com as credenciais e loga no Keycloak, sendo redirecionado de volta à aplicação com um authorization code passado como parâmetro;
A aplicação envia esse authorization code de volta ao Keycloak e recebe o access token e o refresh token;
A cada chamada a aplicação:
Valida o access token no backend para executar qualquer funcionalidade
Obs.: na Caixa, o access token tem duração padrão de 5 minutos;
Quando o access token expira, o frontend envia um pedido ao Keycloak para geração de novo access token, passando como parâmetro o refresh token;
E assim continua o fluxo da autenticação / autorização até o fim da sessão.
Para instalar o Adapter do Keycloak no JBoss, deverá ser seguido os passos descritos no projeto "aim-keycloak", arquivo \Implementação\adapter\Instalação.txt .

A parametrização da aplicação no JBoss mudou. Antes eram utilizados estes parâmetros:

    <property name="SIXXX-SEC_TEMPO_VIDA_SESSAO" value="600"/>
    <property name="SIXXX-SEC_TIMEOUT_SESSAO" value="30"/>
    <property name="SIXXX-SEC_TEMPO_MINIMO_RENOVACAO_TOKEN" value="20"/>
    <property name="SIXXX-SEC_CHAVE_JWT" value="Umgoe-pPyZ93S6SwfgUay_Z_q1lwZsFaQdLJFdca2PI"/>
    <property name="SIXXX-SEC_LDAP_URL" value="ldap://localhost:10389"/>
    <property name="SIXXX-SEC_LDAP_USUARIO" value="interno"/>
    <property name="SIXXX-SEC_LDAP_SENHA" value="!@3%9$0"/>
    <property name="SIXXX-SEC_LDAP_BASE_DN_USUARIOS" value="ou=Users,o=caixa"/>
    <property name="SIXXX-SEC_LDAP_BASE_DN_PESSOAS" value="ou=People,o=caixa"/>
    <property name="SIXXX-SEC_LDAP_BASE_DN_PERFIS" value="cn=SIXXX,ou=Groups,o=caixa"/>
    <property name="SIXXX-SEC_LDAP_INTERNO" value="true"/>
    <property name="SIXXX-DB_INTERNO" value="true"/>
Agora serão necessários apenas estes:

    <property name="SIXXX-SEC_TEMPO_VIDA_TOKEN" value="5"/>
    <property name="SIXXX-DB_INTERNO" value="true"/>
Existem outras seções que devem ser acrescentadas, e estão gravadas no standalone.xml de exemplo que está dentro da pasta do projeto ( \Implementação\outros\jboss\7.0\configuration\standalone.xml ).

Arquitetura - Versão 1.2
Versão 1.2 da arquitetura, com as seguintes inclusões mais significativas:

Migração de Spring para Java EE:
Spring MVC => JAX-RS
Spring Security => Java EE Security
Spring (Core) => CDI / Enterprise JavaBeans
Spring Data => <Nenhum>
Caracterização das diferenças entre os projetos SIGDF e SIHDG: SIGDF | SIHDG ----------------- JBoss EAP: 6.4 | 7.0 JAX-RS: 1.1 | 2.0 CDI: 1.0 | 1.1 EJB: 3.1 | 3.2 JPA: 2.1 | 2.0 Hibernate: 4.3.2 | 5.2.5
Segmentação do código entre arquitetura e funcional
Revisão do processo de geração de builds
Autenticação (e parcialmente Autorização) via LDAP
Para facilitar a montagem do ambiente, a seguir estão algumas instruções importantes:

Link de download do JBoss EAP:

6.4: https://developers.redhat.com/download-manager/file/jboss-eap-6.4.0.GA.zip 
7.0: https://developers.redhat.com/download-manager/file/jboss-eap-7.0.0.zip 
Configurações a fazer no Eclipse: [sigdf/sihdg-core] Project \ Properties \ JPA \ Errors/Warnings \ No persistent.xml file found in project => Ignore [sigdf/sihdg-core] Project \ Properties \ JPA \ Errors/Warnings \ Persistent.xml file does not have supported content for JPA platform => Ignore

A configuração do HTTPS no JBoss pode ser feita de acordo com o standalone.xml localizado na pasta "\Implementação\outros\jboss[9.9]\configuration" do projeto

Chamada no Angular:
ng serve --env=local --ssl 1 --ssl-key "Implementação\outros\cert\cast-jboss.key" --ssl-cert "Implementação\outros\cert\cast-jboss.crt" URL: https://localhost:4200 

As seguintes configurações influenciam os perfis e permissões do sistema: [sigdf/sihdg-core] /resources/ldap-embedded.ldif => Configurações básicas do LDAP [sigdf/sihdg-core] br.gov.caixa.arquitetura.javaee.core.comum.config.seguranca.SecurityConfig => Configurações específicas de teste: Usuários: ADM/adm e USU/usu [sigdf/sihdg-api] web.xml => Configurações gerais de permissões de chamadas REST [sigdf/sihdg-api] Rest Controller => anotação @RolesAllowed controla quais recursos existentes no perfil permitem chamar o método REST Exemplos: ExemploController => diferentes métodos com diferentes permissões UsuarioController => como recuperar o usuário logado a partir do token de acesso

Acesso à documentação dos REST via Swagger: https://localhost:8443/sihdg-api/swagger/index.html 

Ações realizadas:

Adequação para o JBoss EAP 7
Remover o Spring e adequar ao JavaEE
Fazer controle de acesso via perfis:
É prudente usar o próprio JWT pra carregar o perfil do usuário? R: Não => Recupera na hora via método de backend
Criar dois usuários fictícios com diferentes permissões
Controlar no backend: autorização nos métodos WS da API
Colocar o Swagger
Fazer o /swagger buscar de /dist do build do swagger-ui
URL: https://localhost:8443/sigdf-api/swagger/index.html 
URL: http://localhost:8080/sigdf-api/swagger/index.html 
Inserir https
Frontend:
ng serve --env=local --ssl 1 --ssl-key "Implementação\outros\cert\cast-jboss.key" --ssl-cert "Implementação\outros\cert\cast-jboss.crt" URL: https://localhost:4200 

Backend:
Mudanças no standalone.xml exemplificadas no arquivo \Implementação\outros\jboss\standalone.xml
O arquivo server.keystore precisa ser colocado na pasta \standalone\configuration do JBoss
Gerar o DAS
Ações pendentes:

Transformar o comando do serviço que apaga em background em JPQL
Refactoring do BaseJwtFilter, JBossWeb, Undertow (e Spring?)
Controlar o total de renovações que o token sofreu, ou o tempo total de vida do token
Controlar a versão do sistema
Incluir a versão do sistema (buscar pelo META-INF) dinamicamente em SwaggerDocConfig?
Revisar o framework de testes unitários para o Java EE
Fazer uma tela de cadastro/consulta básica
Fazer um merge do CSS
Fazer controle de acesso via perfis:
Controlar no frontend: menus e rotas
Inserir comentários faltando
Fazer testes automatizados de autenticação e autorização
Melhorar os logs de tudo
Definir como vão ficar os logs do frontend
Arquitetura - Versão 1.1
Versão 1.1 da arquitetura, com as seguintes inclusões mais significativas:

Controle de sessão Front/Backend
Renovação de token
Revisão do processo de geração de builds
Autenticação (e parcialmente Autorização) via LDAP
O documento SIHDG_Espec_Deploy.doc também foi atualizado para essa nova versão.

Comandos previstos para geração de build:

Backend: ao executar o Maven no sihdg-bom, diferenciar da seguinte forma:
Apenas na produção: utilizar o parâmetro 'prod': "clean install -Dprod"
Para os outros ambientes: "clean install"
Para analisar a árvore de dependência: "dependency:tree"
Frontend:
Publicar para desenvolvimento local: "ng serve --env=local"
Análise de código: "ng lint --fix --type-check"
Build para a produção: "ng build --env=prd --prod --base-href ./"
Build para os outros ambientes: "ng build --env=local --base-href ./"
Ações realizadas:

Fazer com que as janelas de confirmação ou aviso recebam o focus
Controlar a sessão no Angular / depois de X minutos, volta pro login (ou pergunta se renova)
Novas configurações:
Duração do token e tempo de sessão do Angular (mesma configuração)
Tempo mínimo para renovar o token
Implementar a renovação de token
Testar a renovação do token
Colocar configuração de tempo mínimo para renovar e anexar no token
Usar no backend:
Renovar o token na resposta
Usar no frontend:
Colocar num serviço periódico o ping de um método neutro
Confirmar que não há problema renovar o token enquanto estiver idle
Controlar quando fazê-lo a partir do tempo mínimo configurado
Em cada requisição (Angular), validar se o token mudou e atualizá-lo
Ler os dados do token no Angular
Definir a ordem mais adequada de inicialização:
Autenticar
Gravar o token separadamente
Definir o timeout da sessão
Puxar os dados do usuário
Gravar os dados do usuário
Renovar o token
Mesmo fluxo da autenticação
Trocar #loginBean.loginDTO.usuario => pelo login do usuário
Revisão do processo de geração de builds, para que seja possível integrar num build só (.ear) o sistema inteiro
Revisar parâmetros de geração para a produção, incluindo remoção de comentários do frontend, minificação, etc.
Inserir autenticação via LDAP
Implementar o mock desse login através de um servidor LDAP embedded
Fazer com que esse servidor embedded não suba no pacote de produção
Controlar abertura de sessão (via o storage) caso o usuário recarregue o sistema via F5
Fazer controle de acesso via perfis:
Criar dois usuários fictícios com diferentes permissões
Ações pendentes:

Fazer uma tela de cadastro básica
Fazer um merge do CSS
Adequar pro JBoss EAP 7
Perguntar qual versão do spring existe, se é particular da Caixa ou não
Colocar o Swagger
Fazer controle de acesso via perfis:
Controlar no backend: autorização nos métodos WS da API
Controlar no frontend: menus e rotas
E o serviço que apaga em background? => Transformar em JPQL
Inserir https
Melhorar os logs de tudo
Definir como vão ficar os logs do frontend
Fazer testes automatizados de autenticação
Documentar tudo
Arquitetura - Versão 1.0
Versão 1.0 completa da arquitetura, consistindo dos seguintes frameworks, padrões e linguagens:

Camada de Apresentação:

Frontend
Angular 4.4.6
Bootstrap 3.3.7
jQuery 3.2.1
Backend
Spring MVC 4.2.5
Spring Security 4.0.3
Java JWT 0.9.0
Camada de Negócio:

Spring 4.2.5
Camada de Dados:

Spring Data 1.9.4
JPA 2.0
Hibernate 4.2.27
Camada de Testes:

Spring Test 4.2.5
A arquitetura usa o conceito de WS RESTful, na qual são usados os métodos GET, POST, PUT e DELETE para requisições de CRUD, resumidamente, e autenticação via o conceito de JSON Web Tokens ( https://jwt.io/  ).

As seguintes ferramentas adicionais foram utilizadas:

Node.js ( https://nodejs.org/en/  ): 8.9.3 LTS
Visual Studio Code ( https://code.visualstudio.com/  ): 1.18.1
O documento SIHDG_Espec_Deploy.doc também foi atualizado para essa nova versão.

Ações realizadas:

Analisar diferentes arquiteturas e implementações anteriores de frontend Angular
Implementar uma versão básica do frontend em Angular 2+
Importar o layout atual do sistema
Refatorar o projeto para passar de JSF para WS REST usando Spring MVC
Nova subdivisão do projeto de core/web para core/api/web
Revisar todo o código do frontend Angular: componentes, serviços, organização, etc.
Implementar a comunicação http entre o frontend e o backend, fazendo uso de JSON
Revisar a organização do boot do spring na aplicação e das configurações envolvidas
Incluir a implementação do JWT e integrá-lo com o Spring Security
Analisar diferentes arquiteturas e implementações anteriores do JWT
Incluir o Spring Security
Implementar o logout
Limpar o keycloak do projeto Angular
Ações pendentes:

Inserir https
Implementar a renovação de token
Inserir autenticação via LDAP
Implementar o mock desse login
Melhorar os logs de tudo
Fazer um merge do CSS
Fazer testes automatizados de autenticação
Colocar o Swagger
Documentar tudo
Implementar a troca de senha??






