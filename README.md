oc get pod -n sipdm-des
oc logs -n sipdm-des <pod-api-estudante> --since=10m | grep -vE '^\s+at ' | grep -iE "exception|error|caused|timed out|login failed|connection" | tail -40

oc exec -n sipdm-des <pod-api-estudante> -- sh -c 'env | grep -iE "jdbc|datasource|db_"; ls /usr/src/app/secrets_files/SIPDM_DES'

oc exec -n sipdm-des <pod-api-estudante> -- timeout 10 bash -c 'cat < /dev/null > /dev/tcp/<host-sqlserver>/1433' && echo OK || echo FALHA
