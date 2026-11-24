Agora, já logado na VM 765
bash
ip -4 a | grep -E '10.116.(180.23|193.253)'
ss -ltnp 2>/dev/null | grep -E ':(80|443|8080|8443) '
systemctl is-active httpd 2>/dev/null
grep -RniE '^\s*(Timeout|ProxyTimeout)\b|timeout=' /etc/httpd/conf /etc/httpd/conf.d 2>/dev/null
Se o 10.116.180.23 não aparecer na VM, é VIP mesmo.
Se o httpd estiver ativo aqui, o último grep já mostra o timeout dele.
Se o Apache não estiver na 765

No Azure DevOps, abra o log da task "Configurando o Apache" dessa mesma release (SIGEC-CSC-1012, EC TQS). Na linha ok:/changed: do PLAY [apache_tqs] aparece o host do Apache. Entre nele e rode:

bash
grep -RniE '^\s*(Timeout|ProxyTimeout)\b|timeout=' /etc/httpd/conf /etc/httpd/conf.d 2>/dev/null
grep -Rln 'sigec-csc' /etc/httpd/conf.d 2>/dev/null

Me manda as saídas. Se aparecer Timeout 120 ou ProxyTimeout 120, achamos a causa.

Como o Claude está se saindo nesta sessão?
