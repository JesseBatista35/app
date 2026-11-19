1. Descobrir em qual host/servidor o sipen roda, para olharmos o log. No CLI:

/host=*/server-config=*:read-attribute(name=group)

Procure na saída o servidor que tem "result" => "sipen". Vai aparecer o nome do host (ex.: hc_cbrdeapllx4xx) e do servidor.

2. Deploy (no CLI, depois de abrir o log do servidor do sipen):

deploy /tmp/pen-ear-2.32.0.2.ear --name=SIPEN --runtime-name=pen-ear-2.32.0.2.ear --force

O --force troca a 2.29.0.1 pela 2.32.0.2 no server-group sipen.

Atenção: depois do deploy, a 2.29.0.1 sai do domain. Se precisar voltar, dá para baixá-la de novo do binario.

Me mande primeiro a saída do passo 1. Com ela te digo o IP e o caminho do log antes do deploy.
