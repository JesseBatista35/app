
[root@caddeapllx2318 p585600]#
[root@caddeapllx2318 p585600]#
[root@caddeapllx2318 p585600]# exit
exit
-sh-4.2$
-sh-4.2$
-sh-4.2$ ssh 10.116.202.45
The authenticity of host '10.116.202.45 (10.116.202.45)' can't be established.
ECDSA key fingerprint is SHA256:c9B/MMR4TI4/AMHwh+qeJB5ls+8UelMuD9ts69F7jc0.
ECDSA key fingerprint is MD5:5c:25:ab:a6:6c:a2:9f:85:35:27:2d:33:1b:27:e7:c5.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '10.116.202.45' (ECDSA) to the list of known hosts.
p585600@10.116.202.45's password:
Last login: Thu Nov 19 10:48:29 2026 from 10.122.150.31
[p585600@caddeapllx2854 ~]$
[p585600@caddeapllx2854 ~]$
[p585600@caddeapllx2854 ~]$
[p585600@caddeapllx2854 ~]$
[p585600@caddeapllx2854 ~]$ sudo su
[sudo] senha para p585600:
Sinto muito, tente novamente.
[sudo] senha para p585600:
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]# ^C
[root@caddeapllx2854 p585600]# for h in sigsj-internet.des.caixa sigsj-intranet.des.caixa sigsj-boleto.des.caixa caddeapllx135.agil.nprd.caixa.gov.br caddeapllx135; do
  echo "=== $h ==="; getent hosts $h
done

echo "--- quem responde via URL (confirma o 135) ---"
for h in sigsj-intranet.des.caixa sigsj-boleto.des.caixa; do
  echo "== $h =="; curl -sk https://$h/ 2>/dev/null | grep -o "caddeapllx[0-9]*[^< ]*" | head -1
done
=== sigsj-internet.des.caixa ===
10.116.181.214  sigsj-internet.des.caixa
=== sigsj-intranet.des.caixa ===
10.116.180.8    sigsj-intranet.des.caixa
=== sigsj-boleto.des.caixa ===
10.116.181.215  sigsj-boleto.des.caixa
=== caddeapllx135.agil.nprd.caixa.gov.br ===
=== caddeapllx135 ===
--- quem responde via URL (confirma o 135) ---
== sigsj-intranet.des.caixa ==
== sigsj-boleto.des.caixa ==
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
