oc exec -n simpf-tqs simpf-backend-tqs-290-rgftv -- \
  timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/8443' && echo OK || echo FALHA
