Lucas, seguinte — investigando o 401 do AI_IIFX_Job#1 aqui e cheguei num ponto que precisa confirmação do time de segurança (cofre/BeyondTrust).

Resumo rápido: o job gera o token OAuth com sucesso (200) e faz o login (SignAppin) com sucesso (200), mas trava no passo de buscar a credencial no Secrets Safe, com 401 “User not authenticated”. Já descartei bug de parâmetro, de header, de cookie e também TLS/certificado/keystore da máquina — reproduzi o mesmo 401 com o mesmo token fora do Control-M, então não é configuração local do agente.

Como isso começou a falhar depois da manutenção em que a máquina caddeapllx2695 perdeu e recuperou configurações, minha suspeita agora é: o Connection Profile do Control-M (ClientID/Secret usado pra gerar o token) pode ter sido restaurado com uma credencial diferente da que estava de fato autorizada na pasta SIIFX_BATCH_DES do Secrets Safe.

Duvida pro time de segurança: dá pra confirmar se o client_id abaixo (decodificado do token que o job está usando hoje) é exatamente o mesmo client_id/API Registration que está com permissão de leitura (Read) concedida na pasta SIIFX_BATCH_DES?

client_id: 098c4f49-efa5-4042-b19f-8a8b5afc79d2
_clientAccessPolicyId: 332
_clientUserId: 1902

Se não for o mesmo, achamos a causa. Se for o mesmo, voltamos a olhar do lado da sessão/política no BeyondTrust.
