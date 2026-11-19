
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]# for i in 1 2 3; do curl -sk -o /tmp/r -w "intranet try$i: %{http_code}\n" https://sigsj-intranet.des.caixa/sigsj_intranet/default.jsp; grep -oE "caddeapllx[0-9]+" /tmp/r; done
intranet try1: 500
intranet try2: 500
intranet try3: 500
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]# for i in 1 2 3; do curl -sk -o /tmp/r -w "boleto try$i: %{http_code}\n" "https://sigsj-boleto.des.caixa/boletoService/contaJudicial"; grep -oE "caddeapllx[0-9]+" /tmp/r; done
boleto try1: 200
boleto try2: 200
boleto try3: 200
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
