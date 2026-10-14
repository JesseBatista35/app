oc get pod $POD -n simcn-des -o jsonpath='{.metadata.annotations.openshift\.io/scc}{"\n"}{.spec.securityContext}{"\n"}'
oc get ns simcn-des -o yaml | grep -i 'sa.scc'
oc get rc -n simcn-des --sort-by=.metadata.creationTimestamp
# para uma rc antiga, de antes de 10/10:
oc get rc <rc-antiga> -n simcn-des -o jsonpath='{.spec.template.spec.securityContext}{"\n"}'
