Segue o pedido de TQS, separado do de DES.

Campo	Valor
Origem	HOST namespace sipgc-tqs, 10.116.222.238
Destino	HOST des.sigoc.caixa, 10.116.26.110
Protocolo / porta	TCP / 443

Justificativa

Liberação de comunicação de saída do sistema SIPGC (serviço Api de Informações), em ambiente de testes (TQS), para o serviço SIGOC de desenvolvimento (des.sigoc.caixa), porta 443/TCP, para consulta de dados de colaboradores via API REST. O SIPGC em TQS está configurado para consumir esse endereço.

O tráfego de saída dos pods sai pelo endereço de saída (egress IP) do namespace sipgc-tqs, 10.116.222.238, no cluster OpenShift NPRD, confirmado no netnamespace. Teste do pod em 19/11/2026: porta 443 sem conexão.

Contato para esclarecimentos: Jesse Mouta Pereira Batista (P585600), telefone [seu telefone], via Teams.

Troque o [seu telefone] pelo seu número. Os aprovadores são os mesmos de DES, e o destino é o mesmo, então o formulário não deve exigir PTR nem aprovação nacional.

Antes de salvar, confira só uma coisa: na quinta, o Pablo disse que ia ver a rota de TQS com a Livia. Se ele ainda não confirmou por escrito que o TQS fica em des.sigoc.caixa, mande a confirmação antes de abrir, para você não precisar cancelar depois.

Me mande o ID quando salvar.
