
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pod -n simpf-tqs
NAME                            READY     STATUS      RESTARTS   AGE
simpf-backend-tqs-289-deploy    0/1       Completed   0          10d
simpf-backend-tqs-290-deploy    0/1       Completed   0          9d
simpf-backend-tqs-290-rgftv     1/1       Running     0          9d
simpf-frontend-tqs-210-deploy   0/1       Completed   0          10d
simpf-frontend-tqs-211-deploy   0/1       Completed   0          9d
simpf-frontend-tqs-211-zd6zg    2/2       Running     0          9d
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n simpf-tqs <pod-backend-tqs> -- \
  timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/8443' && echo OK || echo FALHA
-sh: pod-backend-tqs: Arquivo ou diretório não encontrado
FALHA
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$  oc exec -n simpf-des simpf-backend-des-447-gzfdw -- \
  timeout 5 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/22' && echo OK || echo FALHA
OK
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$  timeout 5 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/8443' && echo OK || echo FALHA
OK
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ sudo tcpdump -ni any host 10.116.220.37 and port 8443
[sudo] senha para p585600:
tcpdump: verbose output suppressed, use -v or -vv for full protocol decode
listening on any, link-type LINUX_SLL (Linux cooked), capture size 262144 bytes
^C
0 packets captured
0 packets received by filter
0 packets dropped by kernel
-sh-4.2$
