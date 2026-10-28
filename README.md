
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ cat /sigdb/run
#  AgtSigdb -m<alias-desse-host> -h<ip-do-destino> -i<ip-desse-servidor>
#  onde:
#    nome-desse-host    -
#    ip-do-destino      -
#    ip-desse-servidor  -
LD_LIBRARY_PATH=/usr/lib
export LD_LIBRARY_PATH

umask 000
nohup ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111 &[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo mv /etc/init.d/sigdb /root/sigdb.initd.bkp
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo tee /etc/systemd/system/sigdb.service >/dev/null <<'EOF'
[Unit]
Description=SIGDB Agent
After=network-online.target
Wants=network-online.target

[Service]
Type=simple
WorkingDirectory=/sigdb
ExecStart=/sigdb/run
Restart=on-failure
StandardOutput=journal
StandardError=journal

[Install]
WantedBy=multi-user.target
EOF
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo systemctl daemon-reload
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo pkill -f "./AgtSigdb -mtr7261lx651"
[p585600@caddeapllx2651 ~]$ sudo systemctl enable --now sigdb
Created symlink /etc/systemd/system/multi-user.target.wants/sigdb.service → /etc/systemd/system/sigdb.service.
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ ps -ef | grep -i [A]gtSigdb
[p585600@caddeapllx2651 ~]$ ps -ef | grep -i [A]gtSigdb
root      171628       1  0 14:05 ?        00:00:00 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
[p585600@caddeapllx2651 ~]$
