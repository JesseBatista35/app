Realizada a análise da falha de comunicação entre o backend do SIMPF em DES (namespace simpf-des) e o serviço SIGCT (sctdeapllx0018.df.caixa – 10.116.83.19:8443).

Causa identificada: ausência de regra no firewall de rede para a origem 10.116.220.37 (egress IP do simpf-des) com destino 10.116.83.19:8443/TCP. O ambiente TQS funciona porque sua origem (10.116.220.90) já possui essa regra.

Evidências:

O teste TCP do pod DES para 10.116.83.19:8443 expira sem resposta. A mesma origem acessa a porta 22 do destino normalmente.
O pod TQS acessa 10.116.83.19:8443 normalmente.
No destino, a porta 8443 está em escuta (JBoss EAP 6.4), sem firewall local (iptables vazio, policy ACCEPT).
O tcpdump no destino mostra pacotes da origem 10.116.220.37 chegando na porta 22 e nenhum chegando na 8443, o que comprova o bloqueio no firewall de rede.

Ação: registrada a solicitação de regra de firewall à CETEL (ID 98314) para liberar 10.116.220.37 → 10.116.83.19:8443/TCP. Após a aplicação da regra, a conectividade será validada a partir do pod simpf-backend-des.

Justificativa do SLA

O prazo de atendimento foi excedido porque a demanda estava originalmente na fila de outro analista e só foi redistribuída a este analista posteriormente. Após o recebimento, a análise foi conduzida e concluída no mesmo dia, com identificação da causa e encaminhamento da solicitação de regra de firewall à CETEL (ID 98314).

Mensagem para o Flávio no Teams

Olá, Flávio, tudo bem?

Registrei a solicitação de regra de firewall ID 98314 e preciso da sua aprovação, por favor.

Regra: 10.116.220.37 → 10.116.83.19 (sctdeapllx0018.df.caixa), TCP 8443.
Motivo: o backend do SIMPF em DES não consegue acessar o SIGCT. O ambiente TQS já tem regra equivalente (origem 10.116.220.90) e funciona. Confirmei via teste de conexão e tcpdump no servidor de destino que o bloqueio está no firewall de rede.

Obrigado!
