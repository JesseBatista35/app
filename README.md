# PV/PVC efetivos
oc get pvc -n simcn-des
oc get pv simcn-backend-data-des -o jsonpath='{.spec.nfs}{"\n"}'

# Montagem dentro do pod
POD=$(oc get pod -n simcn-des -l app=simcn-backend-des -o name | head -1)
oc exec -n simcn-des $POD -- df -h | grep -i ifs
oc exec -n simcn-des $POD -- ls -la /simcn/upload/des/simcn
oc exec -n simcn-des $POD -- sh -c 'touch /simcn/upload/des/simcn/.teste_cesti && rm /simcn/upload/des/simcn/.teste_cesti && echo ESCRITA_OK'

# Nó onde o pod roda (IP que precisa estar liberado no export)
oc get $POD -n simcn-des -o wide
oc get node <NODE> -o wide

# Egress IP do namespace (para confirmar o que é o 25.128.181.35)
oc get egressip 2>/dev/null || oc get netnamespace simcn-des -o yaml
