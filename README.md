
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ ps -ef | grep -i [j]boss | grep -o "jboss.home.dir=[^ ]*"
jboss.home.dir=/opt/jboss-eap
jboss.home.dir=[^
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ sudo ls /opt
[sudo] senha para p585600:
apm_agent  httpd  jboss-eap  jmx_exporter  node_exporter
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ JB=<jboss.home.dir>
-sh: erro de sintaxe próximo ao token inesperado `newline'
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ sudo grep -E "WFLYUT0021|WFLYSRV0010|WFLYSRV0026|WFLYCTL0013|ERROR" $JB/standalone/log/server.log | tail -30
grep: /standalone/log/server.log: Arquivo ou diretório inexistente
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$
[p585600@caddeapllx2864 ~]$ sudo ls -l $JB/standalone/deployments/
ls: não foi possível acessar '/standalone/deployments/': Arquivo ou diretório inexistente
[p585600@caddeapllx2864 ~]$



<img width="1764" height="876" alt="image" src="https://github.com/user-attachments/assets/d719d792-1e6f-4b39-b06a-50d5b8ebb6ac" />


a aplicação esta fncionado voce esta louco
