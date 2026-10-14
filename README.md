
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pod $POD -n simcn-des -o jsonpath='{.metadata.annotations.openshift\.io/scc}{"\n"}{.spec.securityContext}{"\n"}'
anyuid
map[seLinuxOptions:map[level:s0:c94,c79]]
-sh-4.2$ oc get ns simcn-des -o yaml | grep -i 'sa.scc'
    openshift.io/sa.scc.mcs: s0:c94,c79
    openshift.io/sa.scc.supplemental-groups: 1008900000/10000
    openshift.io/sa.scc.uid-range: 1008900000/10000
          f:openshift.io/sa.scc.mcs: {}
          f:openshift.io/sa.scc.supplemental-groups: {}
          f:openshift.io/sa.scc.uid-range: {}
-sh-4.2$ oc get rc -n simcn-des --sort-by=.metadata.creationTimestamp
NAME                    DESIRED   CURRENT   READY     AGE
simcn-frontend-des-67   0         0         0         5d
simcn-frontend-des-68   1         1         1         5d
simcn-backend-des-276   0         0         0         18h
simcn-backend-des-277   1         1         1         16h
-sh-4.2$ # para uma rc antiga, de antes de 10/10:
-sh-4.2$ oc get rc <rc-antiga> -n simcn-des -o jsonpath='{.spec.template.spec.securityContext}{"\n"}'
-sh: rc-antiga: Arquivo ou diretório não encontrado
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
