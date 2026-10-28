
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ P=$(sudo readlink /proc/162569/fd/0 | tr -dc 0-9); echo "pipe=$P"
pipe=3517727
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo find /proc/[0-9]*/fd -lname "pipe:\[$P\]" 2>/dev/null
/proc/162569/fd/0
/proc/162582/fd/1
/proc/162582/fd/2
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ ps -o pid,ppid,user,lstart,cmd -p <PIDs que aparecerem, exceto 162569>
-sh: erro de sintaxe próximo ao token inesperado `newline'
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ ls -l /etc/init.d/
total 12
-rwxr-xr-x 1 root root 2602 jul 18  2023 filebeat
-rwxr-xr-x 1 root root 2624 mai 25  2022 metricbeat
-rwxr-xr-x 1 root root  346 out 19 16:25 sigdb
[p585600@caddeapllx2651 ~]$ ps -o pid,ppid,user,lstart,cmd -p 162582
    PID    PPID USER                      STARTED CMD
 162582       1 root     Wed Oct 28 12:24:08 2026 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
[p585600@caddeapllx2651 ~]$
