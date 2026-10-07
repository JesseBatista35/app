
[p585600@caddeapllx2821 ~]$ ping -c2 10.188.0.16
PING 10.188.0.16 (10.188.0.16) 56(84) bytes de dados.
De 10.188.6.225 icmp_seq=1 Host de destino inalcançável
De 10.188.6.225 icmp_seq=2 Host de destino inalcançável

--- 10.188.0.16 estatísticas de ping ---
2 pacotes transmitidos, 0 recebidos, +2 erros, 100% packet loss, time 1047ms
pipe 2
[p585600@caddeapllx2821 ~]$ ping -c2 10.188.0.11
PING 10.188.0.11 (10.188.0.11) 56(84) bytes de dados.
De 10.188.6.225 icmp_seq=1 Host de destino inalcançável
De 10.188.6.225 icmp_seq=2 Host de destino inalcançável

--- 10.188.0.11 estatísticas de ping ---
2 pacotes transmitidos, 0 recebidos, +2 erros, 100% packet loss, time 1031ms
pipe 2
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ ip -4 -br addr
lo               UNKNOWN        127.0.0.1/8
ens192           UP             10.116.202.23/19
ens224           UP             10.188.6.225/19
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ ip -4 addr show ens224
ip link show ens224
ip neigh show | grep 10.188
bash -c 'timeout 3 bash -c "</dev/tcp/10.188.0.11/2049" && echo 2049 ok || echo 2049 falhou'
3: ens224: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP group default qlen 1000
    altname enp19s0
    inet 10.188.6.225/19 brd 10.188.31.255 scope global noprefixroute ens224
       valid_lft forever preferred_lft forever
3: ens224: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP mode DEFAULT group default qlen 1000
    link/ether 00:50:56:82:a5:1d brd ff:ff:ff:ff:ff:ff
    altname enp19s0
10.188.0.14 dev ens224 FAILED
10.188.0.18 dev ens224 FAILED
10.188.0.16 dev ens224 FAILED
10.188.0.13 dev ens224 FAILED
10.188.0.11 dev ens224 FAILED
10.188.0.17 dev ens224 FAILED
2049 falhou
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
