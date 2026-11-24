
[root@caddeapllx137 p585600]#
[root@caddeapllx137 p585600]#
[root@caddeapllx137 p585600]# grep -niE 'mod_cluster|manager_module|CreateBalancers|ProxyTimeout|AdvertiseFrequency' $H/conf/httpd_eap_71_esteiraagil.conf
grep: /conf/httpd_eap_71_esteiraagil.conf: Arquivo ou diretório não encontrado
[root@caddeapllx137 p585600]#
[root@caddeapllx137 p585600]#
[root@caddeapllx137 p585600]#
[root@caddeapllx137 p585600]#



-sh-4.2$
-sh-4.2$ JB=$(ps -ef | grep -o 'jboss.home.dir=[^ ]*' | head -1 | cut -d= -f2); echo $JB
[^
-sh-4.2$
-sh-4.2$
-sh-4.2$ sudo $JB/bin/jboss-cli.sh -c --controller=10.116.193.253:9990 \
>   '/subsystem=modcluster/mod-cluster-config=configuration:read-attribute(name=node-timeout)' \
>   || sudo $JB/bin/jboss-cli.sh -c --controller=10.116.193.253:9990 \
>   '/subsystem=modcluster/proxy=default:read-attribute(name=node-timeout)'

Presumimos que você recebeu as instruções de sempre do administrador
de sistema local. Basicamente, resume-se a estas três coisas:

    #1) Respeite a privacidade dos outros.
    #2) Pense antes de digitar.
    #3) Com grandes poderes vêm grandes responsabilidades.

[sudo] senha para p585600:
Sinto muito, tente novamente.
[sudo] senha para p585600:
sudo: [^/bin/jboss-cli.sh: comando não encontrado
sudo: [^/bin/jboss-cli.sh: comando não encontrado
-sh-4.2$



