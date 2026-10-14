# 1. OpenShift SDN (mais comum no OKD da Caixa)
oc get netnamespace siifx-des -o jsonpath='{.egressIPs}{"\n"}'

# 2. OVN-Kubernetes
oc get egressip -o wide 2>/dev/null | grep -i siifx

# 3. Se os dois vierem vazios: não há egress IP fixo, e o pod sai pelo IP do nó onde está rodando
POD=$(oc get pod -l name=siifx-api-aplicacao-des --sort-by=.metadata.creationTimestamp -o name | tail -1)
oc get $POD -o jsonpath='{.spec.nodeName}{"  "}{.status.hostIP}{"\n"}'
