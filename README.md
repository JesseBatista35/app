
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
-sh-4.2$ ^C
-sh-4.2$ oc debug dc/sidcx-host-des -c sidcx-host-des -n sidcx-des
Debugging with pod/sidcx-host-des-debug, original command: <image entrypoint>
Waiting for pod to start ...
If you don't see a command prompt, try pressing enter.
sh-5.1$ ls -la /opt/app-root/src; find / -name index.html 2>/dev/null | grep -v /usr/share
total 4
drwxr-xr-x. 1 default root   36 Oct 20 12:32 .
drwxr-xr-x. 1 root    root   17 Mar  1  2026 ..
drwxr-xr-x. 3 default root   19 Feb 17  2026 .pki
drwxr-xr-x. 2 default root    6 Oct 20 12:32 dist
drwxrwxr-x. 2 default root    6 Mar  1  2026 nginx-start
drwxr-xr-x. 2 default root 4096 Oct 20 12:31 sidcx-host
/opt/app-root/src/sidcx-host/index.html
sh-5.1$
