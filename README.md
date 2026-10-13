
Recebida(s) 0 resposta(s)
[root@caddeapllx2821 p585600]# ip neigh show dev ens224
[root@caddeapllx2821 p585600]# arping -c3 -I ens224 10.188.0.16
ARPING 10.188.0.16 de 10.188.6.225 ens224
Unicast resposta de 10.188.0.16 [B0:4F:A6:68:E8:0B]  0.682ms
Unicast resposta de 10.188.0.16 [B0:4F:A6:68:E8:0B]  0.626ms
Unicast resposta de 10.188.0.16 [B0:4F:A6:68:E8:0B]  0.642ms
Enviadas 3 sondas (1 broadcast(s))
Recebida(s) 3 resposta(s)
[root@caddeapllx2821 p585600]#
