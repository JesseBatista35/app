
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]# mount -t nfs 192.168.227.59:/export/sicql_bovespa /opt/sigdb
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]# echo $?
0
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]# ls -ld /producao/SWIFT
drwxrwxrwx 4 jboss jboss 32 out 13 19:30 /producao/SWIFT
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]# mount -t nfs 192.168.227.59:/export/sicql_bovespa /producao/SWIFT
[root@caddeapllx2193 p585600]# echo $?
0
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]# mkdir /producao/SWIFT
mkdir: não foi possível criar o diretório “/producao/SWIFT”: Arquivo existe
[root@caddeapllx2193 p585600]# mount -t nfs 192.168.227.59:/export/sicql_bovespa /producao/SWIFT
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
[root@caddeapllx2193 p585600]#
