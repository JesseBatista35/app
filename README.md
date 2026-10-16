oc exec -n simpf-des simpf-backend-des-447-gzfdw -- \
  timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/8443' && echo OK || echo FALHA


  oc get egressip
oc get pod -n simpf-des -o wide
