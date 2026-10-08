Obrigado pelo retorno. O nmap confirma que o destino escuta em 31153, mas foi feito do cadsvgerlx035-0, e o nosso teste de fora do OKD também conecta. A falha é só a partir do pod, com egress 10.116.221.46.

Pelo packet-tracer da CRQ, a simulação entrou pela interface AUTO_DES_APRES. Pode confirmar se é por essa interface que o tráfego real do OKD NPRD entra no firewall?

Pedimos duas buscas nos logs do CNPRDFW001-1:

Conexão que funciona: 10.116.29.23:1433 em 08/10 às 10:53 (13:53 UTC). Qual IP de origem e qual interface de entrada aparecem?
Conexão que falha: 10.116.29.201:31153 em 08/10 às 10:44 e 10:53. Há algum registro, seja allow ou deny?

Com isso conseguimos saber se o egress IP está sendo usado e se o fluxo novo casa com a regra.
