oc get pods -n sidcx-des -l name=sidcx-host-des
oc exec -n sidcx-des <pod> -c sidcx-host-des -- ls -la /opt/app-root/src/
oc exec -n sidcx-des <pod> -c sidcx-host-des -- find /opt/app-root/src -maxdepth 3 -name index.html
