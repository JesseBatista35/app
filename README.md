netstat -ltn | grep 8443


sudo iptables -L INPUT -n -v --line-numbers

sudo tcpdump -ni any host 10.116.220.37 and port 8443

oc exec -n simpf-des simpf-backend-des-447-gzfdw -- \
  timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/8443' && echo OK || echo FALHA
