SIGSJ DES — resumo do dia (19/11)

Avançamos bastante após a liberação de acesso pela infra. Status por módulo:

✅ Intranet — funcionando ponta a ponta. A causa do 500 pós-login era o diretório /apl/sigsj/properties faltando na VM (a esteira não entregava). Login (LDAP + SIROT GJ01) e Avisos (GJ02) OK.

✅ Boleto — respondendo (SOAP com XML válido).

⏳ Internet — a página renderiza e o login já passa da criptografia (instalei na VM a biblioteca nativa libSenhasSIIBC.so, que faltava). O login ainda depende de 2 pendências abaixo.

Resolvido hoje:
• Lib nativa SenhasSIIBC (internet) — instalada e configurado o java.library.path.
• Causa do login do internet — as VMs novas não alcançavam o farm do SIROT (10.116.89.101:8111). Abertas 3 regras de firewall (internet 99053, intranet 99052, boleto 99054) com o Jeferson.
• Erro caddeapllx135 (intranet/boleto) — era roteamento de VIP pro servidor antigo; normalizou, hoje os VIPs entregam nas VMs novas.
• Properties em DES — RESOLVIDO. O diretório /apl/sigsj/properties (que faltava e quebrava a tela pós-login) foi corrigido e agora é entregue automaticamente pela esteira nos 3 módulos. Seguindo o modelo do Rafael (SIGCX-config), log4j + properties ficam no repo de config (pasta configuration/) — não precisa mais aplicar na mão.

Pendências:
• Internet – banco: datasource SIGSJ04 com ORA-01017. Corrigido o usuário para SGSJSD01 (usuário de aplicação, conforme legado); senha a ser incluída pela Segurança via REQ000147111475 / WO0000082363801 (variável SIGSJ04_PASSWORD, library SIGSJ-INTERNET-DES).
• Internet – firewall SIROT: aguardando a Rede aplicar as regras pro login funcionar.
• Internet – estáticos/encoding: tela sem CSS/imagens e acentuação (ISO-8859-1), a tratar com os devs.

Reunião de terça (24/11, 11h): como DES já está resolvido, o áudio com a Gisele e o Marcio passa a ser para validar os valores dos properties e alinhar TQS/PRD (onde os valores mudam em relação a DES), não mais para resolver DES.

Próximos passos:
• Validar o login do internet assim que a senha (REQ000147111475) e o firewall (99053) estiverem aplicados.
• Levar o modelo de properties pra reunião de terça e alinhar TQS/PRD.
