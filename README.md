
-sh-4.2$
-sh-4.2$ for i in 1 2 3; do date -u '+%H:%M:%S UTC'; timeout 5 bash -c '</dev/tcp/10.116.29.201/31153'; echo "201:31153 rc=$?"; done
14:27:27 UTC
201:31153 rc=0
14:27:27 UTC
201:31153 rc=0
14:27:27 UTC
201:31153 rc=0
-sh-4.2$
-sh-4.2$
-sh-4.2$ date -u '+%H:%M:%S UTC'; timeout 5 bash -c '</dev/tcp/10.116.29.23/1433'; echo "23:1433 rc=$?"

14:27:37 UTC
23:1433 rc=0
-sh-4.2$
-sh-4.2$
-sh-4.2$
