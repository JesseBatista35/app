O ambiente DES do SIMKT foi verificado. A infraestrutura está operacional:

O JBoss EAP 7.4 está em execução e o simkt.war está implantado com status OK.
Os datasources simkt-ds (MKTDB001) e siico-mkt-ds (posdes151) estão com conexão OK.
A autenticação via SSO (Keycloak) funciona normalmente.

Causa raiz

A indisponibilidade foi causada por erro na versão da aplicação publicada em 08/10/2026 às 16:03, correspondente ao commit 655b40e0 (branch CD053_2026_PI3_Sprint4, “FEAT: 16439 - Incluir Relatório Gerencial”).

O commit alterou o arquivo src/main/resources/mpas.csv, que passou a ter uma linha em branco após cada registro, a partir da linha 2, logo após o cabeçalho. Na inicialização da aplicação, o PrivilegeRepository falha ao ler esse arquivo:

08/10 16:03:42 CsvRequiredFieldEmptyException: Número de campos de dados incompatível com número de cabeçalhos.
PrivilegeRepository - Erro ao analisar linha: 2. []

A exceção é capturada e registrada apenas em nível INFO, e a lista de privilégios fica nula. Com isso, todas as requisições autenticadas falham com NullPointerException em PrivilegeRepository.findByUriAndHttpMethod (linha 47) e o endpoint /simkt/api/v1/privilege retorna HTTP 500, deixando a tela em branco após o login. O erro afeta todos os usuários desde 09/10, no primeiro acesso após o deploy.

Ações necessárias (equipe de desenvolvimento)

Remover as linhas em branco do mpas.csv, conferir também a entrada PARAEXPO (PARAMETRIZACAO_EXPORTAR), que está com a URI vazia, e publicar nova versão. Alternativa: rollback para o commit 01851153 (05/10).
Recomendado: configurar o leitor CSV para ignorar linhas vazias (withIgnoreEmptyLine(true)), tratar a falha de carga com log de ERRO sem deixar a lista nula, e incluir teste unitário de carga do mpas.csv. A execução de pipeline desse commit consta como failed.
Recomendado: remover o log do access token JWT completo em nível INFO no SSOAuthenticationService.

Encerramento

Não há ação pendente de infraestrutura ou de esteira. A correção é de código e cabe à equipe de desenvolvimento. Após a publicação da versão corrigida pela esteira, a aplicação volta a funcionar sem intervenção no ambiente. WO encerrada.

Evidências anexas: trecho do console-stdout.log (08/10 16:03:42), início do mpas.csv implantado (cat -A) e stack trace do NPE no server.log.
