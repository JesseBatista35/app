oc rsh -c sihdg-jboss8-tqs sihdg-jboss8-tqs-28-q6ngx
for i in 1 2 3; do date -u '+%H:%M:%S UTC'; timeout 5 bash -c '</dev/tcp/10.116.29.201/31153'; echo "201:31153 rc=$?"; done
date -u '+%H:%M:%S UTC'; timeout 5 bash -c '</dev/tcp/10.116.29.23/1433'; echo "23:1433 rc=$?"
