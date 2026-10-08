Obrigado pelo retorno e pela captura, pessoal. Esclarecendo um ponto: o 10.116.221.46 não é um servidor, é o IP de egress do namespace sihdg-tqs no OKD. Ele fica atribuído ao nó ceadecldlx084 (IP 10.116.208.104), e o pod do teste roda no nó ceadecldlx081 (IP 10.116.208.101). O tráfego do pod passa por VXLAN do 081 para o 084 e só então sai com o egress IP. Do nosso lado, conferi no cluster que o 10.116.221.46 está atribuído ao nó 084.

A captura filtrou só host 10.116.221.46 host 10.116.29.201. Se o tráfego estiver saindo com outra origem (por exemplo o IP de um dos nós), ele não aparece nesse filtro. Isso é compatível com o que vimos: do mesmo pod, o banco antigo 10.116.29.23:1433 conecta, e o 10.116.29.201:31153 dá timeout.

Podem refazer a captura em AUTO_DES_APRES só por destino: host 10.116.29.201 e host 10.116.29.23? Assim vemos qual IP de origem chega ao firewall: 10.116.221.46, 10.116.208.101 ou 10.116.208.104.

Me avisem quando a captura estiver ativa que eu disparo o teste do pod na hora e passo o horário exato (3 tentativas para o .201:31153 e 1 para o .23:1433).
