
-sh-4.2$ oc get pvc -n simcn-des
NAME                     STATUS    VOLUME                   CAPACITY   ACCESS MODES   STORAGECLASS   AGE
simcn-backend-data-des   Bound     simcn-backend-data-des   50Gi       RWX                           4d10h
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pv simcn-backend-data-des -o jsonpath='{.spec.nfs}{"\n"}'
map[server:nfsctcnprd.ctc.caixa path:/ifs/CADSVISISD4/SERVIDORES/CEPTIBR/UP_SIMCN/]
-sh-4.2$
-sh-4.2$
-sh-4.2$ POD=$(oc get pod -n simcn-des -l app=simcn-backend-des -o name | head -1)
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n simcn-des $POD -- df -h | grep -i ifs
error: invalid resource name "pod/simcn-backend-des-277-fh2hg": [may not contain '/']
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n simcn-des $POD -- ls -la /simcn/upload/des/simcn
error: invalid resource name "pod/simcn-backend-des-277-fh2hg": [may not contain '/']
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n simcn-des $POD -- sh -c 'touch /simcn/upload/des/simcn/.teste_cesti && rm /simcn/upload/des/simcn/.teste_cesti && echo ESCRITA_OK'
error: invalid resource name "pod/simcn-backend-des-277-fh2hg": [may not contain '/']
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc project simcn-des
Now using project "simcn-des" on server "https://api.nprd.caixa:6443".
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods
NAME                           READY     STATUS      RESTARTS   AGE
simcn-backend-des-276-deploy   0/1       Completed   0          18h
simcn-backend-des-277-deploy   0/1       Completed   0          16h
simcn-backend-des-277-fh2hg    1/1       Running     0          16h
simcn-frontend-des-68-pscq2    2/2       Running     0          19h
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get $POD -n simcn-des -o wide
NAME                          READY     STATUS    RESTARTS   AGE       IP           NODE                       NOMINATED NODE   READINESS GATES
simcn-backend-des-277-fh2hg   1/1       Running   0          16h       25.1.35.28   ceadecldlx071.nprd.caixa   <none>           <none>
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get egressip 2>/dev/null || oc get netnamespace simcn-des -o yaml
apiVersion: network.openshift.io/v1
egressIPs:
- 10.116.209.118
kind: NetNamespace
metadata:
  creationTimestamp: 2026-04-20T16:37:52Z
  generation: 2
  labels:
    projeto: simcn-des
  managedFields:
  - apiVersion: network.openshift.io/v1
    fieldsType: FieldsV1
    fieldsV1:
      f:netid: {}
      f:netname: {}
    manager: openshift-sdn-controller
    operation: Update
    time: 2026-04-20T16:37:52Z
  - apiVersion: network.openshift.io/v1
    fieldsType: FieldsV1
    fieldsV1:
      f:metadata:
        f:labels:
          .: {}
          f:projeto: {}
    manager: kubectl-label
    operation: Update
    time: 2026-04-20T16:37:53Z
  - apiVersion: network.openshift.io/v1
    fieldsType: FieldsV1
    fieldsV1:
      f:egressIPs: {}
    manager: kubectl-patch
    operation: Update
    time: 2026-04-20T17:02:38Z
  name: simcn-des
  resourceVersion: "1902974367"
  uid: 48e49baa-bb43-4569-b09d-abcdb528c53f
netid: 3367146
netname: simcn-des
-sh-4.2$
