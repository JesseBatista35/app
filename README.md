
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ ps -o pid,ppid,user,lstart,cmd -p 162567,162569
    PID    PPID USER                      STARTED CMD
 162567  162545 root     Wed Oct 28 12:24:08 2026 /bin/sh -c /sbin/service --status-all 2>&1 | grep -E "\[ (\+|\-) \]"
 162569  162567 root     Wed Oct 28 12:24:08 2026 grep -E \[ (\+|\-) \]
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ ps -ef --forest | grep -B3 -A3 -E "16256[79]" | grep -v grep
sansbp01  162524  151090  0 12:24 ?        00:00:00          \_ /bin/sh -c sudo -i  -u root /bin/sh -c 'echo BECOME-SUCCESS-nuqlrtalgdnjzctfdwckppjbnyvmqzvf ; /usr/bin/python' && sleep 0
root      162544  162524  0 12:24 ?        00:00:00              \_ sudo -i -u root /bin/sh -c echo BECOME-SUCCESS-nuqlrtalgdnjzctfdwckppjbnyvmqzvf ; /usr/bin/python
root      162545  162544  0 12:24 ?        00:00:00                  \_ /usr/bin/python
root        5338       1  0 out19 ?        00:00:00 /usr/sbin/oddjobd -n -p /run/oddjobd.pid -t 300
root        5382       1  0 out19 ?        00:00:00 /usr/sbin/sssd -i --logger=files
root        5383    5382  0 out19 ?        00:05:28  \_ /usr/libexec/sssd/sssd_be --domain LDAP --uid 0 --gid 0 --logger=files
[p585600@caddeapllx2651 ~]$
