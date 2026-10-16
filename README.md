Oi Sandra! Resolvemos o SIHDG Angular 18 em TQS. Segue o resumo:

Causa raiz
O front pega a URL do SSO no endpoint do backend /sihdg-api/api/seguranca/configuracao-seguranca. Esse endpoint devolvia login.des.caixa porque a URL estava fixa no código, na classe OidcConfigurationProvider (repositório SIHDG-jboss8). Por isso o front TQS ia para o SSO de DES, onde a URL de TQS não está cadastrada, e dava o erro de redirect_uri. O cadastro no SSO TQS estava correto.

O que fizemos

Ajustamos o OidcConfigurationProvider para ler a URL por ambiente (system property SIHDG-SEC_URL_SERV_AUTH ou variável de ambiente SEC_URL_SERV_AUTH). Se nenhuma estiver definida, usa DES como padrão. A alteração está na branch Cesti-teste001, tag 3.22.0.3.
Incluímos nos grupos da Library:
SIHDG-JBOSS8-TQS: SIHDG-SEC_URL_SERV_AUTH e _ENV.SEC_URL_SERV_AUTH = https://login.tqs.caixa/auth
SIHDG-JBOSS8-DES: as mesmas variáveis com https://login.des.caixa/auth
Fizemos a release em TQS. O endpoint agora retorna login.tqs.caixa e o login funciona.
A sua alteração no standalone (OIDC lendo da Library) deve ser mantida, porque é ela que valida o token TQS no backend.

Sobre a tela em branco na janela normal
Era a estação sem a cadeia da AC Icptestes (Raiz e Sub), que emite o certificado das rotas *.apps.nprd.caixa. Sem ela, o navegador bloqueia a chamada ao backend. Quem for testar precisa instalar a Raiz em “Autoridades Raiz Confiáveis” e a Sub em “Intermediárias”, e reabrir o navegador. O patch de truststore no pod do angular18 não é necessário: o pod é nginx e não usa .jks.

Pendências para o time (Anderson)

Levar a alteração do OidcConfigurationProvider para a linha oficial, conferindo se nada da 3.22.0.2 ficou de fora, já que a 3.22.0.3 foi gerada para o teste.
Criar a SIHDG-SEC_URL_SERV_AUTH nos grupos de HMP e PRD antes de promover, senão esses ambientes caem no padrão de DES.
Se o secret caixa-truststore-acteste-nprd foi criado no sihdg-tqs só para o teste do patch, pode ser removido.
Melhoria opcional: fazer o front chamar o backend pelo proxy /api/ do nginx em vez de ir direto ao host do jboss8.

Qualquer dúvida, estou à disposição!
