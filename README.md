
-sh-4.2$ oc exec -n simpf-des simpf-backend-des-447-gzfdw -- \
  timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/8443' && echo OK || echo FALHA
command terminated with exit code 124
FALHA
-sh-4.2$ oc get egressip
error: the server doesn't have a resource type "egressip"
-sh-4.2$ oc get pod -n simpf-des -o wide
NAME                            READY     STATUS      RESTARTS   AGE       IP            NODE                       NOMINATED NODE   READINESS GATES
simpf-backend-des-446-deploy    0/1       Completed   0          25h       25.1.21.157   ceadecldlx046.nprd.caixa   <none>           <none>
simpf-backend-des-447-deploy    0/1       Completed   0          20h       25.1.19.31    ceadecldlx041.nprd.caixa   <none>           <none>
simpf-backend-des-447-gzfdw     1/1       Running     0          20h       25.1.35.204   ceadecldlx071.nprd.caixa   <none>           <none>
simpf-frontend-des-330-deploy   0/1       Completed   0          7d18h     25.2.6.156    ceadecldlx020.nprd.caixa   <none>           <none>
simpf-frontend-des-331-5d6ss    2/2       Running     0          7d1h      25.0.43.211   ceadecldlx080.nprd.caixa   <none>           <none>
simpf-frontend-des-331-deploy   0/1       Completed   0          7d1h      25.0.16.225   ceadecldlx036.nprd.caixa   <none>           <none>
-sh-4.2$
