O paste embolou (as linhas do prompt entraram como comando). E reparei: via VIP o 135 não apareceu de novo — então talvez o VIP já esteja indo pra VM nova, e o que sobra é a app. Mas falta o dado que importa: o código HTTP via VIP. Roda esse, é uma linha só por vez (sem comentário, à prova de paste):

bash
for i in 1 2 3; do curl -sk -o /tmp/r -w "intranet try$i: %{http_code}\n" https://sigsj-intranet.des.caixa/sigsj_intranet/default.jsp; grep -oE "caddeapllx[0-9]+" /tmp/r; done

Depois:

bash
for i in 1 2 3; do curl -sk -o /tmp/r -w "boleto try$i: %{http_code}\n" "https://sigsj-boleto.des.caixa/boletoService/contaJudicial"; grep -oE "caddeapllx[0-9]+" /tmp/r; done

O que vou comparar com o direto na VM (intranet 500 / boleto 200):

Se via VIP o intranet também der 500 e o boleto 200 (sem 135) → o VIP já está certo, indo pra VM nova! O 135 era estado antigo. Aí não precisa de REQ de VIP; o que sobra é: intranet 500 = SIROT (firewall 99052 pendente), boleto já ok.
Se via VIP aparecer o 135 em alguma tentativa → pool do VIP ainda tem o 135, e aí sim é REQ pra Rede.

Manda os dois resultados. Com o código HTTP via VIP eu fecho se ainda precisa mexer no VIP ou se o problema agora é só o SIROT (firewall) no intranet.
