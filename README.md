$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ for p in 3516221 3516222; do sudo find /proc/[0-9]*/fd -lname "pipe:\[$p\]" 2>/dev/null; done
/proc/162545/fd/4
/proc/162567/fd/1
/proc/162569/fd/1
/proc/162545/fd/6
/proc/162567/fd/2
/proc/162569/fd/2
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ for p in 3516221 3516222; do sudo find /proc/[0-9]*/fd -lname "pipe:\[$p\]" 2>/dev/null; do^C
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
