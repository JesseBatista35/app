systemctl status sigdb --no-pager


sudo cp /sigdb/run /sigdb/run.bkp
sudo tee /sigdb/run >/dev/null <<'EOF'
#!/bin/bash
#  AgtSigdb -m<alias-desse-host> -h<ip-do-destino> -i<ip-desse-servidor>
LD_LIBRARY_PATH=/usr/lib
export LD_LIBRARY_PATH

umask 000
cd /sigdb
exec ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
EOF
sudo chmod 755 /sigdb/run

sudo pkill -f "./AgtSigdb -mtr7261lx651"
sudo systemctl restart sigdb
systemctl status sigdb --no-pager      # active (running), Main PID = AgtSigdb
ps -ef | grep -i [A]gtSigdb            # 1 instância, PPID 1
