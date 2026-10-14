POD=simcn-backend-des-277-fh2hg

# Onde o volume está montado no container
oc get dc simcn-backend-des -n simcn-des -o jsonpath='{range .spec.template.spec.containers[*].volumeMounts[*]}{.name}{" -> "}{.mountPath}{"\n"}{end}'

oc exec -n simcn-des $POD -- df -h | grep -i ifs
oc exec -n simcn-des $POD -- ls -la /simcn
oc exec -n simcn-des $POD -- ls -la /simcn/upload/des/simcn
oc exec -n simcn-des $POD -- sh -c 'touch /simcn/upload/des/simcn/.teste_cesti && rm /simcn/upload/des/simcn/.teste_cesti && echo ESCRITA_OK'

# IP do nó (é este que o export do Isilon enxerga na montagem)
oc get node ceadecldlx071.nprd.caixa -o wide
