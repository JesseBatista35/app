
[root@caddeapllx2821 p585600]#
[root@caddeapllx2821 p585600]#
[root@caddeapllx2821 p585600]#
[root@caddeapllx2821 p585600]# arping -I ens224 -c 3 10.188.0.11
ARPING 10.188.0.11 de 10.188.6.225 ens224
Enviadas 3 sondas (3 broadcast(s))
Recebida(s) 0 resposta(s)
[root@caddeapllx2821 p585600]# ip -s link show ens224
3: ens224: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP mode DEFAULT group default qlen 1000
    link/ether 00:50:56:82:a5:1d brd ff:ff:ff:ff:ff:ff
    RX:  bytes packets errors dropped  missed   mcast
     299422525 4112627      0    2221       0       3
    TX:  bytes packets errors dropped carrier collsns
         15814     339      0       0       0       0
    altname enp19s0
[root@caddeapllx2821 p585600]#
