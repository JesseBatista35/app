
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

# evita instancias duplicadas (init.d / service --status-all / systemd)
if pgrep -f "AgtSigdb -mtr7261lx651" >/dev/null 2>&1; then
  exit 0
fi

# foreground (compativel com systemd) e sem herdar stdout/stderr de quem chamou
exec ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111 >>/sigdb/AgtSigdb.out 2>&1
EOF
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo tee /etc/init.d/sigdb >/dev/null <<'EOF'
#!/bin/bash
### BEGIN INIT INFO
# Provides: sigdb
# Required-Start: $local_fs $network $syslog
# Required-Stop: $local_fs $syslog
# Default-Start: 2 3 4 5
# Default-Stop: 0 1 6
# Short-Description: Sigdb Agent
# Description: Sigdb Agent
### END INIT INFO

case "$1" in
  start)
    cd /sigdb && nohup ./run >/dev/null 2>&1 &
    ;;
  stop)
    pkill -f "./AgtSigdb -m"
    ;;
  status)
    if pgrep -f "./AgtSigdb -m" >/dev/null 2>&1; then
      echo "sigdb em execucao"; exit 0
    else
      echo "sigdb parado"; exit 3
    fi
    ;;
  restart)
    $0 stop; sleep 2; $0 start
    ;;
  *)
    echo "Uso: $0 {start|stop|status|restart}"; exit 1
    ;;
esac
EOF
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo chmod 755 /sigdb/run /etc/init.d/sigdb
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo systemctl reset-failed sigdb
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo systemctl restart sigdb
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ systemctl status sigdb --no-pager; ps -ef | grep -i [A]gtSigdb
● sigdb.service - SIGDB Agent
     Loaded: loaded (/etc/systemd/system/sigdb.service; enabled; preset: disabled)
     Active: active (running) since Wed 2026-10-28 14:40:09 -03; 8s ago
   Main PID: 192790 (AgtSigdb)
      Tasks: 3 (limit: 23083)
     Memory: 2.5M
        CPU: 11ms
     CGroup: /system.slice/sigdb.service
             └─192790 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
root      192790       1  0 14:40 ?        00:00:00 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ time sudo service --status-all | grep sigdb
/etc/init.d/filebeat: line 40: /etc/rc.d/init.d/functions: No such file or directory
/etc/init.d/filebeat: line 44: status: command not found
/etc/init.d/filebeat: line 90: status: command not found
/etc/init.d/metricbeat: line 40: /etc/rc.d/init.d/functions: No such file or directory
/etc/init.d/metricbeat: line 44: status: command not found
/etc/init.d/metricbeat: line 90: status: command not found
sigdb em execucao

real    0m0,065s
user    0m0,015s
sys     0m0,017s
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ ps -ef | grep -i [A]gtSigdb
root      192790       1  0 14:40 ?        00:00:00 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ time sudo service --status-all | grep sigdb
/etc/init.d/filebeat: line 40: /etc/rc.d/init.d/functions: No such file or directory
/etc/init.d/filebeat: line 44: status: command not found
/etc/init.d/filebeat: line 90: status: command not found
/etc/init.d/metricbeat: line 40: /etc/rc.d/init.d/functions: No such file or directory
/etc/init.d/metricbeat: line 44: status: command not found
/etc/init.d/metricbeat: line 90: status: command not found
sigdb em execucao

real    0m0,058s
user    0m0,014s
sys     0m0,014s
[p585600@caddeapllx2651 ~]$
