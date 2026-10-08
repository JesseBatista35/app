
sh-5.1$ date; timeout 10 bash -c '</dev/tcp/10.116.29.23/1433'; echo "rc=$?"
Thu Oct  8 13:53:21 America 2026
rc=0
sh-5.1$
