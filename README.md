oc get pod -n simpf-des
oc get netnamespace simpf-des
oc exec -n simpf-des <pod-backend-atual> -- \
  timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/8443' && echo OK || echo FALHA


  oc logs -n simpf-des <pod-backend-atual> | grep -iE "sctdeapllx0018|sigct|pkix|ssl|handshake|timed out" | tail -30


  sudo tcpdump -ni any host 10.116.220.37 and port 8443
