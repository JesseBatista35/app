O Apache é a única camada ainda não verificada e o suspeito principal. Entre no 137 (e depois repita no 138) e rode:

bash
# onde está a config do Apache (pode não ser /etc/httpd)
ps -ef | grep -E '[h]ttpd|[a]pache' | head -3

# timeouts globais e no vhost do sigec-csc
grep -RniE '^\s*(Timeout|ProxyTimeout)\b|timeout=' /etc/httpd/ 2>/dev/null
grep -Rln 'sigec-csc' /etc/httpd/ 2>/dev/null

Com o arquivo do vhost em mãos:

bash
VH=caminho-do-arquivo-que-apareceu
grep -niE 'ServerName|ProxyPass|timeout|BalancerMember' $VH

E a prova no log de erro. Quando o mod_proxy estoura o timeout, ele grava AH01102 / timeout specified has expired e devolve exatamente um 504:

bash
grep -RlE 'sigec-csc' /var/log/httpd/ 2>/dev/null | head
grep -hE 'AH01102|timeout specified has expired|AH00898' /var/log/httpd/*sigec*error* 2>/dev/null | tail -20

Se os caminhos /etc/httpd e /var/log/httpd vierem vazios, use o caminho que o ps -ef mostrar (parâmetro -f ou -d) e me manda que eu ajusto os comandos
