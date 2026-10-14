oc exec -n simcn-des $POD -- id
oc exec -n simcn-des $POD -- sh -c 'touch /simcn/conciliacao/.teste_cesti && ls -l /simcn/conciliacao/.teste_cesti && rm /simcn/conciliacao/.teste_cesti && echo ESCRITA_OK'
oc exec -n simcn-des $POD -- env | grep -iE 'path|storage|nfs|simcn'
oc exec -n simcn-des $POD -- ls -la /upload/des/simcn 2>&1
oc exec -n simcn-des $POD -- ls -lt /simcn/conciliacao | head
