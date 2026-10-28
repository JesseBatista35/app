mount | grep siccp
timeout 5 stat /siccp; echo "rc=$?"        # rc=124 => mount pendurado
timeout 5 df -h /siccp; echo "rc=$?"
ps -eo pid,stat,cmd | awk '$2 ~ /D/'       # processos presos em I/O
rpcinfo -t hypernprd12.ad.caixa nfs
showmount -e hypernprd12.ad.caixa | grep siccp


sudo umount -f -l /siccp
sudo mount -t nfs hypernprd12.ad.caixa:/fs_siccp /siccp
timeout 5 ls /siccp
