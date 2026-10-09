exit

oc get networkpolicy -n sipdm-des
oc get egressfirewall -n sipdm-des 2>/dev/null
oc get egressnetworkpolicy -n sipdm-des 2>/dev/null
oc get netnamespace sipdm-des 2>/dev/null
oc get egressip 2>/dev/null
oc get pod sipdm-api-estudante-des-264-s2lvb -n sipdm-des -o wide
