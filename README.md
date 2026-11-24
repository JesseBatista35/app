# no 137 (como root)
grep -niE 'mod_cluster|manager_module|CreateBalancers|ProxyTimeout|AdvertiseFrequency' $H/conf/httpd_eap_71_esteiraagil.conf


Correção recomendada: na 765, só afeta o SIGEC-CSC

Na VM caddeapllx765, primeiro leia o valor atual (o caminho varia conforme a versão do EAP):


JB=$(ps -ef | grep -o 'jboss.home.dir=[^ ]*' | head -1 | cut -d= -f2); echo $JB
sudo $JB/bin/jboss-cli.sh -c --controller=10.116.193.253:9990 \
  '/subsystem=modcluster/mod-cluster-config=configuration:read-attribute(name=node-timeout)' \
  || sudo $JB/bin/jboss-cli.sh -c --controller=10.116.193.253:9990 \
  '/subsystem=modcluster/proxy=default:read-attribute(name=node-timeout)'


  Se voltar undefined ou -1, use o caminho que funcionou e grave o novo valor:

  ...:write-attribute(name=node-timeout,value=600)
:reload
