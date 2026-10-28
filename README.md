[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo journalctl -k --since "2026-10-28 11:05" --until "2026-10-28 11:40" | grep -iE "nfs|not responding|hung|blocked"

Presumimos que você recebeu as instruções de sempre do administrador
de sistema local. Basicamente, resume-se a estas três coisas:

    #1) Respeite a privacidade dos outros.
    #2) Pense antes de digitar.
    #3) Com grandes poderes vêm grandes responsabilidades.

[sudo] senha para p585600:
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ journalctl -k --since "2026-10-28 11:05" --until "2026-10-28 11:40" | grep -iE "nfs|not responding|hung|blocked"
Hint: You are currently not seeing messages from other users and the system.
      Users in groups 'adm', 'systemd-journal', 'wheel' can see all messages.
      Pass -q to turn off this notice.
No journal files were opened due to insufficient permissions.
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo grep -iE "not responding|hung_task|blocked for more" /var/log/messages | grep "Oct 28"
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ grep -E "nfs|cifs|fuse" /proc/mounts
fusectl /sys/fs/fuse/connections fusectl rw,nosuid,nodev,noexec,relatime 0 0
sunrpc /var/lib/nfs/rpc_pipefs rpc_pipefs rw,relatime 0 0
hypernprd12.ad.caixa:/fs_siccp /siccp nfs4 rw,sync,relatime,vers=4.2,rsize=262144,wsize=262144,namlen=255,hard,proto=tcp,timeo=600,retrans=2,sec=sys,clientaddr=10.188.6.241,local_lock=none,addr=10.188.0.12 0 0
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ timeout 15 df -hT >/dev/null; echo "df rc=$?"
timeout 15 findmnt >/dev/null; echo "findmnt rc=$?"
timeout 15 lsblk >/dev/null; echo "lsblk rc=$?"
timeout 15 sudo dmidecode -t system >/dev/null; echo "dmidecode rc=$?"
df rc=0
findmnt rc=0
lsblk rc=0
dmidecode rc=0
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ ps -ef --forest | grep -A5 -i ansible
p585600   150999  150921  0 12:10 pts/1    00:00:00              \_ grep --color=auto -A5 -i ansible
root        5338       1  0 out19 ?        00:00:00 /usr/sbin/oddjobd -n -p /run/oddjobd.pid -t 300
root        5382       1  0 out19 ?        00:00:00 /usr/sbin/sssd -i --logger=files
root        5383    5382  0 out19 ?        00:05:27  \_ /usr/libexec/sssd/sssd_be --domain LDAP --uid 0 --gid 0 --logger=files
root        5384    5382  0 out19 ?        00:01:28  \_ /usr/libexec/sssd/sssd_nss --uid 0 --gid 0 --logger=files
root        5385    5382  0 out19 ?        00:00:03  \_ /usr/libexec/sssd/sssd_pam --uid 0 --gid 0 --logger=files
[p585600@caddeapllx2651 ~]$
