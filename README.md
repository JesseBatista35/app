Resumo – SIGSJ DES (19/11)

Avançamos bastante no diagnóstico dos erros das aplicações em DES após a liberação de acesso pela infra.

✅ Resolvido – biblioteca nativa (internet)
O HTTP 500 no login do SIGSJ-internet era causado pela falta da biblioteca nativa libSenhasSIIBC.so (criptografia da senha enviada ao SIPER/SIROT), que não existia na VM nova. Localizei a lib no servidor legado (sspdeapllx0039), copiei para a VM (caddeapllx2854) e configurei o java.library.path. O erro de criptografia não ocorre mais — o login agora avança até a comunicação com o SIROT.

✅ Causa raiz do login identificada – comunicação com o SIROT
Com a lib ok, o login passou a falhar no envio ao SIROT. Confirmei por teste que as VMs novas não alcançam o farm do SIROT (10.116.89.101:8111 / sspdeaplux0100) — o servidor legado alcança, as VMs novas não. É liberação de firewall. Com o apoio do Jeferson, foram abertas as 3 regras:

Internet (caddeapllx2854) → ID 99053
Intranet (caddeapllx955) → ID 99052
Boleto (caddeapllx2557) → ID 99054

Assim que a Rede aplicar, revalido o login das três.

ℹ️ Intranet não usa a lib
Verifiquei o EAR do intranet: ele usa o SIROT (farm), mas não usa a SenhasSIIBC. Portanto a intranet não precisa da lib — só da liberação de firewall (já aberta).

⏳ Pendências em paralelo (não dependem do firewall)

Banco SIGSJ04 (internet): datasource com ORA-01017. O usuário configurado era uma matrícula pessoal (F731607); o correto, conforme o legado, é o usuário de aplicação SGSJSD01. Vou corrigir o usuário no config e precisamos acionar a Segurança para fornecer/inserir a senha do SGSJSD01 em DES, no mesmo fluxo da REQ000147038150 que usamos em TQS. Afeta as telas internas, não o login.
VIP do intranet: o 503 (caddeapllx135 - eap_71_esteiraagil) é roteamento do VIP, que ainda direciona para a esteira ágil antiga — tratar com a Rede.
Estáticos/encoding do internet: tela sem CSS/imagens e acentuação (ISO-8859-1) — com os devs.
Para validar o login completo do internet, preciso de usuário de teste do portal (Gisele já passou um).

Próximos passos: aguardar a Rede aplicar as 3 regras de firewall e revalidar os logins; e acionar a Segurança para a senha do banco SIGSJ04 (SGSJSD01).
