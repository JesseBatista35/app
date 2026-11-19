
Warning: Permanently added '10.116.200.45' (ED25519) to the list of known hosts.
p585600@10.116.200.45's password:
Creating home directory for p585600.
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ sudo su

Presumimos que você recebeu as instruções de sempre do administrador
de sistema local. Basicamente, resume-se a estas três coisas:

    #1) Respeite a privacidade dos outros.
    #2) Pense antes de digitar.
    #3) Com grandes poderes vêm grandes responsabilidades.

[sudo] senha para p585600:
[root@caddeapllx2318 p585600]#
[root@caddeapllx2318 p585600]#
[root@caddeapllx2318 p585600]#
[root@caddeapllx2318 p585600]# for h in sigsj-internet.des.caixa sigsj-intranet.des.caixa sigsj-boleto.des.caixa; do
>   echo "=== $h ==="; nslookup $h | grep -iA2 "name\|address"
> done
=== sigsj-internet.des.caixa ===
bash: nslookup: comando não encontrado
=== sigsj-intranet.des.caixa ===
bash: nslookup: comando não encontrado
=== sigsj-boleto.des.caixa ===
bash: nslookup: comando não encontrado
[root@caddeapllx2318 p585600]# echo "--- IP do caddeapllx135 ---"
--- IP do caddeapllx135 ---
[root@caddeapllx2318 p585600]# getent hosts caddeapllx135.agil.nprd.caixa.gov.br || nslookup caddeapllx135
bash: nslookup: comando não encontrado
[root@caddeapllx2318 p585600]#
[root@caddeapllx2318 p585600]# echo "--- app direto nas VMs novas (pra provar que a app está ok) ---"
--- app direto nas VMs novas (pra provar que a app está ok) ---
[root@caddeapllx2318 p585600]# curl -s -o /dev/null -w "boleto VM 2557: %{http_code}\n"  http://10.116.201.25/boletoService/
boleto VM 2557: 404
[root@caddeapllx2318 p585600]# curl -s -o /dev/null -w "intranet VM 955: %{http_code}\n" http://10.116.194.179/sigsj_intranet/
intranet VM 955: 200
[root@caddeapllx2318 p585600]#
[root@caddeapllx2318 p585600]#
[root@caddeapllx2318 p585600]#
[root@caddeapllx2318 p585600]#
[root@caddeapllx2318 p585600]#
