600@caddeapllx2651 ~]$ systemctl status sigdb --no-pager

× sigdb.service - SIGDB Agent
     Loaded: loaded (/etc/systemd/system/sigdb.service; enabled; preset: disabled)
     Active: failed (Result: exit-code) since Wed 2026-10-28 14:05:27 -03; 1min 15s ago
   Duration: 1ms
    Process: 170736 ExecStart=/sigdb/run (code=exited, status=203/EXEC)
   Main PID: 170736 (code=exited, status=203/EXEC)
        CPU: 710us
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo cp /sigdb/run /sigdb/run.bkp
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo tee /sigdb/run >/dev/null <<'EOF'
#!/bin/bash
#  AgtSigdb -m<alias-desse-host> -h<ip-do-destino> -i<ip-desse-servidor>
LD_LIBRARY_PATH=/usr/lib
export LD_LIBRARY_PATH

umask 000
cd /sigdb
exec ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
EOF
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo chmod 755 /sigdb/run
[p585600@caddeapllx2651 ~]$ sudo pkill -f "./AgtSigdb -mtr7261lx651"
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo systemctl restart sigdb
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ systemctl status sigdb --no-pager
● sigdb.service - SIGDB Agent
     Loaded: loaded (/etc/systemd/system/sigdb.service; enabled; preset: disabled)
     Active: active (running) since Wed 2026-10-28 14:07:25 -03; 5s ago
   Main PID: 171651 (AgtSigdb)
      Tasks: 3 (limit: 23083)
     Memory: 2.4M
        CPU: 4ms
     CGroup: /system.slice/sigdb.service
             └─171651 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ ps -ef | grep -i [A]gtSigdb
root      171651       1  0 14:07 ?        00:00:00 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
[p585600@caddeapllx2651 ~]$
