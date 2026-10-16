sudo tcpdump -ni any host 10.116.220.37




oc exec -n simpf-des simpf-backend-des-447-gzfdw -- timeout 5 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/22' && echo OK22
oc exec -n simpf-des simpf-backend-des-447-gzfdw -- timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/8443' && echo OK8443 || echo FALHA8443
