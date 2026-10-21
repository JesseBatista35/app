oc exec -n sipdm-des sipdm-api-estudante-des-265-xnh9d -- \
  timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.100.127/1433' && echo OK || echo FALHA
oc get netnamespace sipdm-des
