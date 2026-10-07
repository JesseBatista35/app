
[p585600@cadsvitrlx100 ~]$ ssh 10.116.202.23
p585600@10.116.202.23's password:
Last login: Tue Oct  6 16:09:54 2026 from 10.122.150.31
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ getent hosts hypernprd12.ad.caixa
10.188.0.16     hypernprd12.ad.caixa
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$
[p585600@caddeapllx2821 ~]$ ping -c3 hypernprd12.ad.caixa
PING hypernprd12.ad.caixa (10.188.0.11) 56(84) bytes de dados.
De caddeapllx2821.agil.nprd.caixa.gov.br (10.188.6.225) icmp_seq=1 Host de destino inalcançável
De caddeapllx2821.agil.nprd.caixa.gov.br (10.188.6.225) icmp_seq=2 Host de destino inalcançável
De caddeapllx2821.agil.nprd.caixa.gov.br (10.188.6.225) icmp_seq=3 Host de destino inalcançável

--- hypernprd12.ad.caixa estatísticas de ping ---
3 pacotes transmitidos, 0 recebidos, +3 erros, 100% packet loss, time 2062ms
pipe 3
[p585600@caddeapllx2821 ~]$ nc -zv hypernprd12.ad.caixa 2049
-sh: nc: comando não encontrado
[p585600@caddeapllx2821 ~]$ nc -zv hypernprd12.ad.caixa 111
-sh: nc: comando não encontrado
[p585600@caddeapllx2821 ~]$ showmount -e hypernprd12.ad.caixa
clnt_create: RPC: Unable to receive
[p585600@caddeapllx2821 ~]$
