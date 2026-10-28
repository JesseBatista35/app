
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ ls -l /etc/init.d/sigdb; head -3 /sigdb/run
-rwxr-xr-x 1 root root 346 out 28 14:05 /etc/init.d/sigdb
#!/bin/bash
#  AgtSigdb -m<alias-desse-host> -h<ip-do-destino> -i<ip-desse-servidor>
LD_LIBRARY_PATH=/usr/lib
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ systemctl status sigdb --no-pager; ps -ef | grep -i [A]gtSigdb
● sigdb.service - SIGDB Agent
     Loaded: loaded (/etc/systemd/system/sigdb.service; enabled; preset: disabled)
     Active: active (running) since Wed 2026-10-28 14:07:25 -03; 5min ago
   Main PID: 171651 (AgtSigdb)
      Tasks: 3 (limit: 23083)
     Memory: 2.4M
        CPU: 38ms
     CGroup: /system.slice/sigdb.service
             └─171651 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
root      171651       1  0 14:07 ?        00:00:00 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
[p585600@caddeapllx2651 ~]$
