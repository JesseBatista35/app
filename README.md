
-sh-4.2$ ssh 10.116.223.233
The authenticity of host '10.116.223.233 (10.116.223.233)' can't be established.
ECDSA key fingerprint is SHA256:pQv6RtXKFT4d4ekRd9WMqBljpwhWnoBgurHJgjiiBY8.
ECDSA key fingerprint is MD5:11:65:5c:2e:ec:e5:d7:55:db:82:91:ac:0d:ef:cc:01.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '10.116.223.233' (ECDSA) to the list of known hosts.
***********************************************************************
(1) - Este e um computador privado de propriedade da Caixa Economica
Federal. Usuarios autorizados e nao autorizados nao possuem direitos de
divulgar as informacoes contidas aqui.
(2) - Ao fazer uso do sistema, o usuario esta ciente que pode estar
sendo monitorado, interceptado e auditado pelo departamento competente
da Caixa Economica Federal.
(3) - O uso nao autorizado ou improprio deste sistema pode resultar em
um processo disciplinar administrativo e/ou punicao atraves de acoes
civis ou criminais. Ao continuar o uso deste sistema, indica que voce
esta ciente e concordando com os termos e condicoes acima descritos.

Pressione <Control+D> IMEDIATAMENTE se voce nao concorda com as
condicoes deste aviso
***********************************************************************
p585600@10.116.223.233's password:
Creating home directory for p585600.
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ ps -ef | grep -E '[h]ttpd|[a]pache' | head -3
prometh+   1519      1  0  2025 ?        00:00:28 /usr/local/bin/apache_exporter --insecure --scrape_uri=http://10.116.223.233/server-status/?auto --telemetry.address=0.0.0.0:9117 --telemetry.endpoint=/metrics
root       3119      1  0  2025 ?        02:07:12 /opt/jbcs-httpd24-2.4/httpd/sbin/httpd -f /opt/jbcs-httpd24-2.4/httpd/conf/httpd.conf -E /opt/jbcs-httpd24-2.4/httpd/logs/httpd.log -d /opt/jbcs-httpd24-2.4/httpd -f /opt/jbcs-httpd24-2.4/httpd/conf/httpd_eap_71_esteiraagil.conf -k start
apache    52440   3119  0 10:18 ?        00:00:00 /opt/jbcs-httpd24-2.4/httpd/sbin/httpd -f /opt/jbcs-httpd24-2.4/httpd/conf/httpd.conf -E /opt/jbcs-httpd24-2.4/httpd/logs/httpd.log -d /opt/jbcs-httpd24-2.4/httpd -f /opt/jbcs-httpd24-2.4/httpd/conf/httpd_eap_71_esteiraagil.conf -k start
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ grep -RniE '^\s*(Timeout|ProxyTimeout)\b|timeout=' /etc/httpd/ 2>/dev/null
-sh-4.2$
-sh-4.2$
-sh-4.2$ grep -Rln 'sigec-csc' /etc/httpd/ 2>/dev/null
-sh-4.2$
-sh-4.2$
