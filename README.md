$
-sh-4.2$
-sh-4.2$ oc rsh -c sihdg-jboss8-tqs sihdg-jboss8-tqs-28-q6ngx
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$ for i in 1 2 3; do date -u '+%H:%M:%S UTC'; timeout 5 bash -c '</dev/tcp/10.116.29.201/31153'; echo "201:31153 rc=$?"; done
14:28:45 UTC
201:31153 rc=124
14:28:50 UTC
201:31153 rc=124
14:28:55 UTC
201:31153 rc=124
sh-5.1$ date -u '+%H:%M:%S UTC'; timeout 5 bash -c '</dev/tcp/10.116.29.23/1433'; echo "23:1433 rc=$?"
14:29:11 UTC
23:1433 rc=0
sh-5.1$
