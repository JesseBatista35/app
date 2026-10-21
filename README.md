
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n sipdm-des sipdm-api-estudante-des-265-xnh9d -- \
>   timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.100.127/1433' && echo OK || echo FALHA
command terminated with exit code 124
FALHA
-sh-4.2$ oc get netnamespace sipdm-des
NAME        NETID      EGRESS IPS
sipdm-des   11268449   ["10.116.221.183"]
-sh-4.2$
