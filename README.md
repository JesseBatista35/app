df -h -T | grep nfs
df -h -T | grep -c nfs
mount | grep -E ' /SIEXC_SWIFT | /producao/SWIFT | /opt/sigdb ' | awk '{print $3}'
