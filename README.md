600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ cat /etc/init.d/sigdb
### BEGIN INIT INFO
# Provides: Sigdb Agent
# Required-Start: $local_fs $network $syslog
# Required-Stop: $local_fs $syslog
# Should-Start: $syslog
# Should-Stop: $network $syslog
# Default-Start: 2 3 4 5
# Default-Stop: 0 1 6
# Short-Description: Start Sigdb Agent
# Description: Start Start Sigdb Agent
### END INIT INFO
cd /sigdb;nohup ./run &[p585600@caddeapllx2651 ~]$ ps -ef | grep -i [A]gtSigdb
root       33919       1  0 out19 ?        00:00:50 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
root       65691       1  0 out23 ?        00:00:23 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
root       77263       1  0 out23 ?        00:00:23 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
spcsnpb1   97404       1  0 out27 ?        00:00:07 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
root      109593       1  0 out27 ?        00:00:04 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
root      126369       1  0 10:43 ?        00:00:00 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
root      138099       1  0 11:10 ?        00:00:00 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
root      150245       1  0 11:40 ?        00:00:00 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
root      162582       1  0 12:24 ?        00:00:00 ./AgtSigdb -mtr7261lx651 -h10.192.224.66 -i10.116.201.111
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ sudo kill 162569
[p585600@caddeapllx2651 ~]$
