
-sh-4.2$ oc get pod -n sipdm-tqs
NAME                                 READY     STATUS      RESTARTS   AGE
sipdm-api-estudante-tqs-154-deploy   0/1       Completed   0          12d
sipdm-api-estudante-tqs-155-deploy   0/1       Completed   0          6d20h
sipdm-api-estudante-tqs-155-qjsks    1/1       Running     0          6d20h
sipdm-backend-tqs-39-lhvzn           1/1       Running     0          381d
sipdm-frontend-tqs-3-cmn7k           2/2       Running     2          396d
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n sipdm-tqs sipdm-api-estudante-tqs-155-qjsks -- timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.100.127/1433' && echo OK || echo FALHA
OK
-sh-4.2$
-sh-4.2$
-sh-4.2$

C:\Users\p585600>timeout 5 bash -c 'cat < /dev/null > /dev/tcp/10.116.100.127/1433' && echo OK || echo FALHA
O sistema não pode encontrar o caminho especificado.
FALHA

C:\Users\p585600>
C:\Users\p585600>
C:\Users\p585600>



