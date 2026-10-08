oc get pod sihdg-jboss8-tqs-28-q6ngx -n sihdg-tqs -o wide
oc get hostsubnet ceadecldlx084.nprd.caixa -o yaml | grep -i -A3 egress
oc debug node/ceadecldlx084.nprd.caixa -- chroot /host ip -4 addr show | grep 10.116.221.46
