
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ grep -Rn --exclude-dir=logs 'balancer://sigec-csc' $H | grep -v ProxyPass
grep: /opt/jbcs-httpd24-2.4/httpd/run/cgisock.109161: Permissão negada
grep: /opt/jbcs-httpd24-2.4/httpd/run/cgisock.74424: Permissão negada
grep: /opt/jbcs-httpd24-2.4/httpd/run/cgisock.3119: Permissão negada
grep: /opt/jbcs-httpd24-2.4/httpd/conf/openssl/pki/tls/certs/localhost.crt: Permissão negada
grep: /opt/jbcs-httpd24-2.4/httpd/conf/openssl/pki/tls/private/localhost.key: Permissão negada
grep: /opt/jbcs-httpd24-2.4/httpd/cache/mod_cluster_httpd_eap_71_esteiraagil: Permissão negada
^C
-sh-4.2$
-sh-4.2$
-sh-4.2$ sudo su

Presumimos que você recebeu as instruções de sempre do administrador
de sistema local. Basicamente, resume-se a estas três coisas:

    #1) Respeite a privacidade dos outros.
    #2) Pense antes de digitar.
    #3) Com grandes poderes vêm grandes responsabilidades.

[sudo] senha para p585600:
[root@caddeapllx137 p585600]#
[root@caddeapllx137 p585600]#
[root@caddeapllx137 p585600]#
[root@caddeapllx137 p585600]# grep -Rn --exclude-dir=logs 'balancer://sigec-csc' $H | grep -v ProxyPass
[root@caddeapllx137 p585600]#
[root@caddeapllx137 p585600]# grep -hE 'AH01102|timeout specified has expired' /logs/apache2/sigec-csc/sigec-csc.esteiras.tqs.caixa-error.log* 2>/dev/null | tail -10
[Fri Aug 07 16:46:06.042737 2026] [proxy_ajp:error] [pid 28871:tid 139753932416768] (70007)The timeout specified has expired: [client 10.116.4.158:11364] AH00878: read response failed from 10.116.193.253:8009 (10.116.193.253), referer: https://sigec-csc-frontend-tqs.apps.nprd.caixa/
[Fri Aug 07 16:52:56.908521 2026] [proxy_ajp:error] [pid 28841:tid 139754106607360] (70007)The timeout specified has expired: [client 10.116.4.145:43075] AH00878: read response failed from 10.116.193.253:8009 (10.116.193.253), referer: https://sigec-csc-frontend-tqs.apps.nprd.caixa/
[Thu Aug 13 11:03:01.839082 2026] [proxy_ajp:error] [pid 55975:tid 139753865275136] (70007)The timeout specified has expired: [client 10.116.4.151:61539] AH00878: read response failed from 10.116.193.253:8009 (10.116.193.253), referer: https://sigec-csc-frontend-tqs.apps.nprd.caixa/
[Mon Nov 09 20:13:54.273487 2026] [proxy_ajp:error] [pid 42776:tid 139753924024064] (70007)The timeout specified has expired: [client 10.116.4.156:23944] AH00878: read response failed from 10.116.193.253:8009 (10.116.193.253), referer: https://sigec-csc-frontend-tqs.apps.nprd.caixa/
[Tue Nov 10 02:54:45.674287 2026] [proxy_ajp:error] [pid 42776:tid 139754123392768] (70007)The timeout specified has expired: [client 10.116.4.147:34256] AH00878: read response failed from 10.116.193.253:8009 (10.116.193.253), referer: https://sigec-csc-frontend-tqs.apps.nprd.caixa/
[Tue Nov 10 09:17:57.664209 2026] [proxy_ajp:error] [pid 83463:tid 139753873667840] (70007)The timeout specified has expired: [client 10.116.4.147:29239] AH00878: read response failed from 10.116.193.253:8009 (10.116.193.253), referer: https://sigec-csc-frontend-tqs.apps.nprd.caixa/
[Tue Nov 10 15:43:32.189356 2026] [proxy_ajp:error] [pid 4507:tid 139753915631360] (70007)The timeout specified has expired: [client 10.116.4.156:31788] AH00878: read response failed from 10.116.193.253:8009 (10.116.193.253), referer: https://sigec-csc-frontend-tqs.apps.nprd.caixa/
[Tue Nov 17 11:08:19.570708 2026] [proxy_ajp:error] [pid 27646:tid 139753957594880] (70007)The timeout specified has expired: [client 10.116.4.145:25306] AH00878: read response failed from 10.116.193.253:8009 (10.116.193.253), referer: https://sigec-csc-frontend-tqs.apps.nprd.caixa/
[Wed Nov 18 10:45:30.122354 2026] [proxy_ajp:error] [pid 56879:tid 139753982772992] (70007)The timeout specified has expired: [client 10.116.4.155:24706] AH00878: read response failed from 10.116.193.253:8009 (10.116.193.253), referer: https://sigec-csc-frontend-tqs.apps.nprd.caixa/
[Mon Nov 23 15:19:42.527122 2026] [proxy_ajp:error] [pid 91090:tid 139754106607360] (70007)The timeout specified has expired: [client 10.116.4.151:2006] AH00878: read response failed from 10.116.193.253:8009 (10.116.193.253), referer: https://sigec-csc-frontend-tqs.apps.nprd.caixa/
[root@caddeapllx137 p585600]#
[root@caddeapllx137 p585600]#
[root@caddeapllx137 p585600]# grep -E '" 504 ' /logs/apache2/sigec-csc/sigec-csc.esteiras.tqs.caixa-access.log | tail -10
10.116.4.158 - - [07/Aug/2026:16:44:05 -0300] "GET /csc-api/cessaocarteiras/v1/baseelegiveis?filters=%7B%22criterio%22:%22todos%22,%22etapa%22:%22%22,%22sistema%22:%22%22,%22base%22:null,%22dataInicial%22:%222026-07-08T19:44:05.512Z%22,%22dataFinal%22:%222026-08-07T19:44:05.512Z%22,%22situacao%22:null%7D&sortBy=identificacaoNumeroBe&sortOrder=asc&pageNumber=0&pageSize=10 HTTP/1.1" 504 342 "https://sigec-csc-frontend-tqs.apps.nprd.caixa/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:140.0) Gecko/20100101 Firefox/140.0" text/html 504 342 529 120096379
10.116.4.145 - - [07/Aug/2026:16:50:56 -0300] "GET /csc-api/cessaocarteiras/v1/baseelegiveis?filters=%7B%22criterio%22:%22todos%22,%22etapa%22:%22%22,%22sistema%22:%22%22,%22base%22:null,%22dataInicial%22:%222026-07-08T19:42:00.211Z%22,%22dataFinal%22:%222026-08-07T19:42:00.211Z%22,%22situacao%22:null%7D&sortBy=identificacaoNumeroBe&sortOrder=desc&pageNumber=0&pageSize=10 HTTP/1.1" 504 342 "https://sigec-csc-frontend-tqs.apps.nprd.caixa/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:140.0) Gecko/20100101 Firefox/140.0" text/html 504 342 529 120081843
10.116.4.151 - - [13/Aug/2026:11:01:01 -0300] "GET /csc-api/cessaocarteiras/v1/baseelegiveis?filters=%7B%22criterio%22:%22todos%22,%22etapa%22:%22%22,%22sistema%22:%22%22,%22base%22:null,%22dataInicial%22:%222026-07-14T14:01:01.557Z%22,%22dataFinal%22:%222026-08-13T14:01:01.557Z%22,%22situacao%22:null%7D&sortBy=identificacaoNumeroBe&sortOrder=asc&pageNumber=0&pageSize=10 HTTP/1.1" 504 342 "https://sigec-csc-frontend-tqs.apps.nprd.caixa/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:140.0) Gecko/20100101 Firefox/140.0" text/html 504 342 529 120139864
10.116.4.156 - - [09/Nov/2026:20:11:54 -0300] "GET /csc-api/cessaocarteiras/v1/baseelegiveis/exportarbase/108/arquivo/excel/etapa/0?z=1794265913750 HTTP/1.1" 504 342 "https://sigec-csc-frontend-tqs.apps.nprd.caixa/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:140.0) Gecko/20100101 Firefox/140.0" text/html 504 342 529 120115818
10.116.4.147 - - [10/Nov/2026:02:52:45 -0300] "GET /csc-api/cessaocarteiras/v1/baseelegiveis/exportarbase/108/arquivo/excel/etapa/0?z=1794289965203 HTTP/1.1" 504 342 "https://sigec-csc-frontend-tqs.apps.nprd.caixa/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:140.0) Gecko/20100101 Firefox/140.0" text/html 504 342 529 120089872
10.116.4.147 - - [10/Nov/2026:09:15:57 -0300] "GET /csc-api/cessaocarteiras/v1/baseelegiveis/exportarbase/108/arquivo/excel/etapa/0?z=1794312957244 HTTP/1.1" 504 342 "https://sigec-csc-frontend-tqs.apps.nprd.caixa/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:140.0) Gecko/20100101 Firefox/140.0" text/html 504 342 529 120096634
10.116.4.156 - - [10/Nov/2026:15:41:32 -0300] "GET /csc-api/cessaocarteiras/v1/baseelegiveis/exportarbase/108/arquivo/excel/etapa/0?z=1794336091711 HTTP/1.1" 504 342 "https://sigec-csc-frontend-tqs.apps.nprd.caixa/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:140.0) Gecko/20100101 Firefox/140.0" text/html 504 342 529 120102648
10.116.4.145 - - [17/Nov/2026:11:06:19 -0300] "GET /csc-api/cessaocarteiras/v1/baseelegiveis/exportarbase/108/arquivo/excel/etapa/0?z=1794924378833 HTTP/1.1" 504 342 "https://sigec-csc-frontend-tqs.apps.nprd.caixa/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:140.0) Gecko/20100101 Firefox/140.0" text/html 504 342 529 120083990
10.116.4.155 - - [18/Nov/2026:10:43:30 -0300] "GET /csc-api/cessaocarteiras/v1/baseelegiveis/exportarbase/108/arquivo/excel/etapa/0?z=1795009409930 HTTP/1.1" 504 342 "https://sigec-csc-frontend-tqs.apps.nprd.caixa/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:140.0) Gecko/20100101 Firefox/140.0" text/html 504 342 529 120101463
10.116.4.151 - - [23/Nov/2026:15:17:42 -0300] "GET /csc-api/cessaocarteiras/v1/baseelegiveis/exportarbase/108/arquivo/excel/etapa/0?z=1795457862073 HTTP/1.1" 504 342 "https://sigec-csc-frontend-tqs.apps.nprd.caixa/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:140.0) Gecko/20100101 Firefox/140.0" text/html 504 342 529 120102150
[root@caddeapllx137 p585600]#
