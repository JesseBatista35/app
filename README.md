findmnt -t nfs4 -o TARGET,SOURCE | sort
findmnt -t nfs4 -o TARGET | sort -u | wc -l
