oão Victor, a regra da CRQ000001499711 está correta e a validação do firewall passou, mas o acesso real a partir do OKD continua falhando.

Teste de dentro do pod sihdg-jboss8-tqs-28-q6ngx (namespace sihdg-tqs, cluster OKD4 NPRD), em 08/10/2026 às 10:44:05 (-03) / 13:44:05 UTC:
/dev/tcp/10.116.29.201/31153 retorna timeout (rc=124).
IP de egress do namespace: 10.116.221.46 (atribuído ao nó ceadecldlx084.nprd.caixa).

Contraste: de um host de operação fora do OKD, a mesma porta conecta (rc=0). O banco está escutando, e o problema está no caminho ou na aceitação da origem 10.116.221.46.

O ping tcp do firewall parte do próprio equipamento e não cobre o fluxo real. Pedimos:

Verificar no CNPRDFW001-1 (logs, show conn ou captura) se o SYN de 10.116.221.46 para 10.116.29.201:31153 chega e se o SYN-ACK volta, na janela do teste acima.
Confirmar se há rota de retorno para a rede 10.116.221.x e se existe outro firewall, ACL ou balanceador entre o OKD e o destino, além do CNPRDFW001-1.
Confirmar se o servidor do banco (ou um firewall dele) aceita a origem 10.116.221.46.
