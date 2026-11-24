No 137 (já como root)
bash
H=/opt/jbcs-httpd24-2.4/httpd
grep -niE 'mod_cluster|manager_module|CreateBalancers|ProxyTimeout|AdvertiseFrequency|EnableMCPMReceive' $H/conf/httpd_eap_71_esteiraagil.conf
Na 765

Entre como root primeiro (sudo su) para não precisar repetir o sudo, e então:

bash
ps -ef | grep '[j]boss-modules' | tr ' ' '\n' | grep -E 'jboss.home.dir|jboss.server.base.dir|server-config|^-c$|\.xml'

Isso mostra o diretório do JBoss e qual XML ele usa. Com o caminho em mãos:

bash
JB=cole-aqui-o-jboss.home.dir
ls $JB/bin/jboss-cli.sh
grep -n -A12 'urn:jboss:domain:modcluster' $JB/standalone/configuration/standalone-full-ha.xml | grep -iE 'modcluster|proxy|node-timeout|balancer|advertise'

Esse grep no XML é só leitura: mostra se o modcluster está configurado e se já existe node-timeout. Me manda as duas saídas antes de alterar qualquer coisa.
