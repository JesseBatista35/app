
Last login: Tue Nov 24 11:11:07 2026 from 10.122.150.31
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$ sudo su
[sudo] senha para p585600:
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]# cat /apl/sigsj/properties/config.properties
sigsj.release = 1.13.0
sigsj.convivencia.url = https://sigsj-convivencia-des.apps.nprd.caixa/convivencia/v1
sigsj.ambiente = DES
simtr.url = http://simtr-api-intranet-des.apps.nprd.caixa/
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]# curl -s -o /dev/null -w "intranet: %{http_code}\n" http://10.116.194.179/sigsj_intranet/default.jsp
intranet: 200
[root@caddeapllx955 p585600]#



deu certo estou com duvida sobre sse release 1.13.0 ela vem de onde se apagar em agu lugar via dar ruim se rodar com uma tag nova dar ruim?
