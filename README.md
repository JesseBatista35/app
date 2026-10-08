Igor, João Victor, a regra da CRQ000001499711 está correta e a validação do firewall passou, mas o acesso real do OKD ao banco novo continua falhando.

Testes feitos de dentro do mesmo pod (sihdg-jboss8-tqs-28-q6ngx, namespace sihdg-tqs, egress 10.116.221.46, nó ceadecldlx084), em 08/10/2026:

10:44 (-03) / 13:44 UTC: 10.116.29.201:31153 → timeout
10:53 (-03) / 13:53 UTC: 10.116.29.23:1433 (banco antigo, release de 01/10 bem-sucedida) → conecta

De um host fora do OKD, o 10.116.29.201:31153 também responde. Ou seja, a origem 10.116.221.46 é aceita para o banco antigo e falha só para esse destino novo.

O ping tcp do firewall parte do próprio equipamento e não cobre o fluxo real. Pedimos:

Verificar no CNPRDFW001-1 (logs ou captura) se o SYN de 10.116.221.46 para 10.116.29.201:31153 chega, e se o SYN-ACK volta, nas janelas acima.
Confirmar se há outro firewall, ACL ou balanceador entre o OKD e 10.116.29.201, e se existe rota de retorno para 10.116.221.x.
Confirmar com o DBA se o servidor aceita a origem 10.116.221.46 e se o SQL Server escuta em 31153.
