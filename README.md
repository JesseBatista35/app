-sh-4.2$
-sh-4.2$ oc get pod sihdg-jboss8-tqs-28-q6ngx -n sihdg-tqs -o wide
NAME                        READY     STATUS    RESTARTS   AGE       IP           NODE                       NOMINATED NODE   READINESS GATES
sihdg-jboss8-tqs-28-q6ngx   1/1       Running   0          6d21h     25.1.38.77   ceadecldlx081.nprd.caixa   <none>           <none>
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get hostsubnet ceadecldlx084.nprd.caixa -o yaml | grep -i -A3 egress
egressCIDRs:
- 10.116.192.0/19
egressIPs:
- 10.116.209.59
- 10.116.222.206
- 10.116.222.190
--
      f:egressCIDRs: {}
    manager: kubectl-patch
    operation: Update
    time: 2025-09-22T20:07:07Z
--
      f:egressIPs: {}
    manager: openshift-sdn-controller
    operation: Update
    time: 2026-08-30T05:39:44Z
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc debug node/ceadecldlx084.nprd.caixa -- chroot /host ip -4 addr show | grep 10.116.221.46

error: cannot debug ceadecldlx084.nprd.caixa: unable to extract pod template from type *v1.Node
-sh-4.2$
