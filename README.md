
[p585600@caddeapllx2651 ~]$ ls -l /sigdb/run /etc/init.d/sigdb
-rwxr-xr-x 1 root root 346 out 28 14:35 /etc/init.d/sigdb
-rwxr-xr-x 1 root root 656 out 28 14:35 /sigdb/run
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ cat -A /sigdb/run | tail -5
    ;;$
  *)$
    echo "Uso: $0 {start|stop|status|restart}"; exit 1$
    ;;$
esac[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo bash -x /sigdb/run
[sudo] senha para p585600:
+ case "$1" in
+ echo 'Uso: /sigdb/run {start|stop|status|restart}'
Uso: /sigdb/run {start|stop|status|restart}
+ exit 1
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo journalctl -u sigdb --no-pager | tail -20
out 28 14:35:16 caddeapllx2651.agil.nprd.caixa.gov.br run[192737]: Uso: /sigdb/run {start|stop|status|restart}
out 28 14:35:16 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: sigdb.service: Main process exited, code=exited, status=1/FAILURE
out 28 14:35:16 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: sigdb.service: Failed with result 'exit-code'.
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: sigdb.service: Scheduled restart job, restart counter is at 4.
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: Stopped SIGDB Agent.
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: Started SIGDB Agent.
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br run[192738]: Uso: /sigdb/run {start|stop|status|restart}
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: sigdb.service: Main process exited, code=exited, status=1/FAILURE
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: sigdb.service: Failed with result 'exit-code'.
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: sigdb.service: Scheduled restart job, restart counter is at 5.
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: Stopped SIGDB Agent.
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: Started SIGDB Agent.
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br run[192739]: Uso: /sigdb/run {start|stop|status|restart}
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: sigdb.service: Main process exited, code=exited, status=1/FAILURE
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: sigdb.service: Failed with result 'exit-code'.
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: sigdb.service: Scheduled restart job, restart counter is at 6.
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: Stopped SIGDB Agent.
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: sigdb.service: Start request repeated too quickly.
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: sigdb.service: Failed with result 'exit-code'.
out 28 14:35:17 caddeapllx2651.agil.nprd.caixa.gov.br systemd[1]: Failed to start SIGDB Agent.
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo sed -i 's/\r$//' /sigdb/run /etc/init.d/sigdb
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo systemctl restart sigdb
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ systemctl status sigdb --no-pager; ps -ef | grep -i [A]gtSigdb
× sigdb.service - SIGDB Agent
     Loaded: loaded (/etc/systemd/system/sigdb.service; enabled; preset: disabled)
     Active: failed (Result: exit-code) since Wed 2026-10-28 14:37:57 -03; 5s ago
   Duration: 1ms
    Process: 192768 ExecStart=/sigdb/run (code=exited, status=1/FAILURE)
   Main PID: 192768 (code=exited, status=1/FAILURE)
        CPU: 1ms
[p585600@caddeapllx2651 ~]$
