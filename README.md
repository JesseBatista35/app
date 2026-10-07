[sudo] senha para p585600:
sudo: tcpdump: comando não encontrado
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ sudo su
[root@caddeapllx2821 p585600]# tcpdump -i ens224 -nn arp -c 5
bash: tcpdump: comando não encontrado
[root@caddeapllx2821 p585600]#
[root@caddeapllx2821 p585600]#
[root@caddeapllx2821 p585600]# ping -c1 10.188.0.11
PING 10.188.0.11 (10.188.0.11) 56(84) bytes de dados.
De 10.188.6.225 icmp_seq=1 Host de destino inalcançável

--- 10.188.0.11 estatísticas de ping ---
1 pacotes transmitidos, 0 recebidos, +1 erros, 100% packet loss, time 0ms

[root@caddeapllx2821 p585600]#
