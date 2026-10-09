
sh-4.4$ oc get pods -A | grep sipdm-api-estudante-des-264-s2lvb
sh: oc: command not found
sh-4.4$ exit
exit
command terminated with exit code 1
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get networkpolicy -n sipdm-des
No resources found.
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get egressfirewall -n sipdm-des 2>/dev/null
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get egressnetworkpolicy -n sipdm-des 2>/dev/null
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get netnamespace sipdm-des 2>/dev/null
NAME        NETID      EGRESS IPS
sipdm-des   11268449   ["10.116.221.183"]
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get egressip 2>/dev/null
-sh-4.2$ oc get pod sipdm-api-estudante-des-264-s2lvb -n sipdm-des -o wide
NAME                                READY     STATUS    RESTARTS   AGE       IP           NODE                       NOMINATED NODE   READINESS GATES
sipdm-api-estudante-des-264-s2lvb   1/1       Running   0          18h       25.1.3.233   ceadecldlx026.nprd.caixa   <none>           <none>
-sh-4.2$
