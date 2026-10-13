p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ getent hosts hypernprd12.ad.caixa
10.188.0.16     hypernprd12.ad.caixa
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ ip -br link
lo               UNKNOWN        00:00:00:00:00:00 <LOOPBACK,UP,LOWER_UP>
ens192           UP             00:50:56:82:3b:cf <BROADCAST,MULTICAST,UP,LOWER_UP>
ens224           UP             00:50:56:82:a5:1d <BROADCAST,MULTICAST,UP,LOWER_UP>
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ ip -br addr
lo               UNKNOWN        127.0.0.1/8 ::1/128
ens192           UP             10.116.202.23/19 fe80::250:56ff:fe82:3bcf/64
ens224           UP             10.188.6.225/19 fe80::250:56ff:fe82:a51d/64
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ nmcli -f NAME,DEVICE,TYPE con show
NAME                         DEVICE  TYPE
VMware customization ens192  ens192  ethernet
lo                           lo      loopback
VMware customization ens224  ens224  ethernet
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ sudo tcpdump -i ens256 -n -c 20 arp
[sudo] senha para p585600:
tcpdump: ens256: No such device exists
(SIOCGIFHWADDR: No such device)
[p585600@caddeapllx2821 ~]$ sudo su
[root@caddeapllx2821 p585600]#
[root@caddeapllx2821 p585600]#
[root@caddeapllx2821 p585600]#
[root@caddeapllx2821 p585600]# tcpdump -i ens256 -n -c 20 arp
tcpdump: ens256: No such device exists
(SIOCGIFHWADDR: No such device)
[root@caddeapllx2821 p585600]#
