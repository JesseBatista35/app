
<img width="1881" height="892" alt="image" src="https://github.com/user-attachments/assets/e8f00481-bedf-494b-bde9-141abc639792" />

tem um rodando e travado nesse extao momento

[p585600@caddeapllx2651 ~]$
^C
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ ps -ef --forest | grep -B2 -A8 -i ansible
p585600   150921  150920  0 12:06 pts/1    00:00:00          \_ -sh
p585600   151002  150921  0 12:11 pts/1    00:00:00              \_ ps -ef --forest
p585600   151003  150921  0 12:11 pts/1    00:00:00              \_ grep --color=auto -B2 -A8 -i ansible
root        5338       1  0 out19 ?        00:00:00 /usr/sbin/oddjobd -n -p /run/oddjobd.pid -t 300
root        5382       1  0 out19 ?        00:00:00 /usr/sbin/sssd -i --logger=files
root        5383    5382  0 out19 ?        00:05:27  \_ /usr/libexec/sssd/sssd_be --domain LDAP --uid 0 --gid 0 --logger=files
root        5384    5382  0 out19 ?        00:01:28  \_ /usr/libexec/sssd/sssd_nss --uid 0 --gid 0 --logger=files
root        5385    5382  0 out19 ?        00:00:03  \_ /usr/libexec/sssd/sssd_pam --uid 0 --gid 0 --logger=files
root        5386    5382  0 out19 ?        00:00:04  \_ /usr/libexec/sssd/sssd_sudo --uid 0 --gid 0 --logger=files
sansbp01    5421       1  0 out19 ?        00:00:00 /usr/lib/systemd/systemd --user
sansbp01    5423    5421  0 out19 ?        00:00:00  \_ (sd-pam)
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
