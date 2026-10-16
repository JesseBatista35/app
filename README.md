
oc get pod -n simpf-tqs
oc exec -n simpf-tqs <pod-backend-tqs> -- \
  timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/8443' && echo OK || echo FALHA


  oc exec -n simpf-des simpf-backend-des-447-gzfdw -- \
  timeout 5 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/22' && echo OK || echo FALHA


  timeout 5 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/8443' && echo OK || echo FALHA

  sudo tcpdump -ni any host 10.116.220.37 and port 8443

  
