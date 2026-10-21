# 1. Da sua máquina (outra origem): o SQL Server responde?
timeout 5 bash -c 'cat < /dev/null > /dev/tcp/10.116.100.127/1433' && echo OK || echo FALHA

# 2. Do TQS do SIPDM
oc get pod -n sipdm-tqs
oc exec -n sipdm-tqs <pod-api-estudante-tqs> -- timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.100.127/1433' && echo OK || echo FALHA
