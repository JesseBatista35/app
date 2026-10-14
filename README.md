umount /SIEXC_SWIFT
umount /opt/sigdb
mount | grep -E ' /SIEXC_SWIFT | /opt/sigdb | /producao/SWIFT ' | awk '{print $3}'


df -h -T | grep -c nfs

findmnt -t nfs4 -o TARGET,SOURCE | sort
findmnt -t nfs4 | grep -c nfs4
