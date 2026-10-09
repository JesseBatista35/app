
oc get networkpolicy -n <namespace>
oc get egressfirewall -n <namespace> 2>/dev/null
oc get egressnetworkpolicy -n <namespace> 2>/dev/null


oc get pod sipdm-api-estudante-des-264-s2lvb -o wide      # pega o NODE
oc debug node/<node>
chroot /host
timeout 5 bash -c '</dev/tcp/10.116.100.127/1433' && echo OK || echo FALHOU


cat /var/run/secrets/kubernetes.io/serviceaccount/namespace

oc get pods -A | grep sipdm-api-estudante-des-264-s2lvb
