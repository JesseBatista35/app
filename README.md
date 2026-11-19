
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]# echo "== intranet via VIP =="; curl -sk https://sigsj-intranet.des.caixa/sigsj_intranet/default.jsp | grep -oE "caddeapllx[0-9]+|eap_71_esteiraagil"
echo "== boleto via VIP ==";  curl -sk "https://sigsj-boleto.des.caixa/boletoService/contaJudicial" | grep -oE "caddeapllx[0-9]+|eap_71_esteiraagil"
echo "== direto nas VMs novas (mesmo path) =="
curl -s -o /dev/null -w "intranet 955: %{http_code}\n" http://10.116.194.179/sigsj_intranet/default.jsp
curl -s -o /dev/null -w "boleto 2557: %{http_code}\n"  http://10.116.201.25/boletoService/contaJudicial
== intranet via VIP ==
== boleto via VIP ==
== direto nas VMs novas (mesmo path) ==
intranet 955: 500
boleto 2557: 200
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
