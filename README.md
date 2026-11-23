Já faz quatro dias. Confira no sistema se foi aprovada e aplicada e rode o teste:

bash
POD=$(oc get pods -n sipgc-des --no-headers | grep informacoes | grep Running | awk '{print $1}' | head -1); oc exec -it $POD -n sipgc-des -- bash -c "timeout 5 bash -c '</dev/tcp/des.sigoc.caixa/443' && echo ABERTA || echo SEM CONEXAO"
Se abrir, a origem estava certa e a de TQS segue o mesmo padrão.
Se continuar sem conexão e o 99038 estiver parado em aprovação, cobre o Flávio e o Rafael antes de abrir a de TQS.

Regra de TQS (pedido novo, só uma linha)

Campo	Valor
Tipo	HOST
Hostname de origem	namespace sipgc-tqs
IP de origem	10.116.222.238
Tipo / hostname de destino	HOST / des.sigoc.caixa
IP de destino	10.116.26.110
Protocolo / porta	TCP / 443
Aprovador	Flávio e Rafael, como na DES

Como o destino é o mesmo de DES, o formulário não deve pedir PTR nem aprovação nacional, que eram do hom.sigoc.caixa (faixa 10.123.0.0/16).

Justificativa

Liberação de comunicação de saída do SIPGC (Api de Informações) em ambiente de testes (TQS) para o SIGOC de DES (des.sigoc.caixa). O tráfego de saída dos pods sai pelo egress IP do namespace sipgc-tqs (OpenShift SDN, confirmado no netnamespace). Teste do pod em 19/11/2026: porta 443 sem conexão. Contato: p585600.

Uma confirmação pendente

Na quinta, o Pablo disse que ia ver a rota de TQS com a Livia e confirmar depois, e a frase "podemos manter o pod de TQS apontando para a rota de DES" veio em seguida. Se ainda não houve confirmação por escrito, mande antes de abrir:

Pablo, confirmando: o TQS segue apontando para des.sigoc.caixa, e vou abrir a regra de firewall de TQS para esse destino. Se for mudar para outro SIGOC depois, avisa antes.

Mensagem para o Flávio e o Rafael (quando salvar)

Bom dia, Flávio e Rafael! Poderiam aprovar a solicitação de firewall ID [novo ID]?

Origem: 10.116.222.238 (egress IP do namespace sipgc-tqs, OKD NPRD)
Destino: des.sigoc.caixa (10.116.26.110), TCP/443
Objetivo: o SIPGC (Api de Informações), em TQS, consumir a API do SIGOC.

É a contrapartida de TQS do pedido 99038 (DES). O pedido anterior de DES (98711) saiu com o IP da rota do cluster, e não o IP de saída dos pods, então não resolveu. Esta usa o egress IP correto.

Me mande o ID quando salvar e o resultado do teste da DES.
