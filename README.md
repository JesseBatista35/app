
-sh-4.2$
-sh-4.2$ oc get pv | grep -i simcn
simcn-backend-data-des                                  50Gi       RWX            Retain           Bound         simcn-des/simcn-backend-data-des                                                                                        4d10h
simcn-backend-data-hmp                                  50Gi       RWX            Retain           Bound         simcn-hmp/simcn-backend-data-hmp                                                                                        85d
simcn-backend-data-tqs                                  50Gi       RWX            Retain           Bound         simcn-tqs/simcn-backend-data-tqs                                                                                        97d
-sh-4.2$ oc get pod -n simcn-tqs -o wide
NAME                          READY     STATUS    RESTARTS       AGE       IP            NODE                       NOMINATED NODE   READINESS GATES
simcn-backend-tqs-41-chn75    1/1       Running   36 (69d ago)   69d       25.3.35.216   ceadecldlx074.nprd.caixa   <none>           <none>
simcn-frontend-tqs-13-zc4fs   2/2       Running   0              96d       25.3.12.157   ceadecldlx032.nprd.caixa   <none>           <none>
-sh-4.2$ oc get ns simcn-tqs -o yaml | grep 'sa.scc.uid-range'
    openshift.io/sa.scc.uid-range: 1009630000/10000
          f:openshift.io/sa.scc.uid-range: {}
-sh-4.2$ POD_TQS=$(oc get pod -n simcn-tqs -l app=simcn-backend-tqs -o jsonpath='{.items[0].metadata.name}')
-sh-4.2$ oc exec -n simcn-tqs $POD_TQS -- id
uid=185 gid=0(root) groups=0(root)
-sh-4.2$ oc exec -n simcn-tqs $POD_TQS -- df -h | grep -i ifs
nfsctcnprd.ctc.caixa:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/UP_SIMCN   20G  3.0M   20G   1% /simcn
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
