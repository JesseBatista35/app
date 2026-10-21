
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods -n sidcx-des -l name=sidcx-host-des
NAME                     READY     STATUS             RESTARTS      AGE
sidcx-host-des-4-cvfgj   1/2       CrashLoopBackOff   5 (33s ago)   4m33s
-sh-4.2$
-sh-4.2$
-sh-4.2$ ^C
-sh-4.2$
-sh-4.2$ oc exec -n sidcx-des sidcx-host-des-4-cvfgj -c sidcx-host-des -- ls -la /opt/app-root/src/
error: unable to upgrade connection: container not found ("sidcx-host-des")
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n sidcx-des sidcx-host-des-4-cvfgj -c sidcx-host-des -- find /opt/app-root/src -maxdepth 3 -name index.html
error: unable to upgrade connection: container not found ("sidcx-host-des")
-sh-4.2$
-sh-4.2$
-sh-4.2$

