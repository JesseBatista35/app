O Apache aqui é o JBCS httpd em /opt/jbcs-httpd24-2.4/httpd, não o do sistema. Por isso o /etc/httpd veio vazio. Detalhe: o processo foi iniciado com dois -f, e o que vale é o último, httpd_eap_71_esteiraagil.conf. Rode:

bash
H=/opt/jbcs-httpd24-2.4/httpd

# timeouts globais e por vhost
grep -RniE '^\s*(Timeout|ProxyTimeout)\b|timeout=' $H/conf $H/conf.d 2>/dev/null

# arquivo do vhost do sigec-csc
grep -Rln 'sigec-csc' $H/conf $H/conf.d 2>/dev/null

Com o arquivo do vhost (troque o caminho):

bash
VH=caminho-que-apareceu
grep -niE 'ServerName|ProxyPass|BalancerMember|timeout|ErrorLog|CustomLog' $VH

E o log de erro procurando o estouro de timeout do proxy:

bash
ls -lt $H/logs | grep -i sigec | head
grep -hE 'AH01102|timeout specified has expired|AH00898' $H/logs/*sigec*error* 2>/dev/null | tail -20

Se nenhum Timeout aparecer no grep, o Apache usa o padrão de 60 s. Aí o corte em 120 s não viria daqui. Por isso o log de erro é a prova mais importante.
