Realizada a análise da falha de comunicação entre o backend do SIMPF em DES (namespace simpf-des) e o serviço SIGCT (sctdeapllx0018.df.caixa – 10.116.83.19:8443).

Causa identificada: ausência de regra no firewall de rede para a origem 10.116.220.37 (egress IP do namespace simpf-des) com destino 10.116.83.19:8443/TCP. O ambiente TQS funciona porque sua origem (10.116.220.90) já possui regra equivalente.

Evidências:

O teste TCP do pod simpf-backend-des para 10.116.83.19:8443 expira sem resposta. A mesma origem acessa a porta 22 do destino normalmente.
O pod simpf-backend-tqs acessa 10.116.83.19:8443 normalmente.
De dentro do pod DES, o DNS resolve sctdeapllx0018.df.caixa corretamente para 10.116.83.19.
No servidor de destino, a porta 8443 está em escuta (JBoss EAP 6.4) e não há firewall local (iptables sem regras, policy ACCEPT).
A captura de pacotes (tcpdump) no destino mostra as conexões da origem 10.116.220.37 chegando na porta 22 e nenhum pacote chegando na 8443, o que comprova o bloqueio no firewall de rede.

Ação: registrada a solicitação de regra de firewall à CETEL (ID 98314) para liberar 10.116.220.37 → 10.116.83.19:8443/TCP, espelhando a regra existente para o ambiente TQS. Após a aplicação, a conectividade será validada a partir do pod simpf-backend-des.

Justificativa do prazo: o prazo de atendimento foi excedido devido à complexidade da análise, que exigiu investigação em múltiplas camadas (aplicação, cluster de contêineres, rede e servidor de destino) para isolar a causa. Foram necessários testes comparativos entre os ambientes DES e TQS, a identificação do IP de saída do namespace e a captura de pacotes no servidor de destino até confirmar o bloqueio no firewall de rede. A resolução definitiva depende da aplicação da regra pela CETEL (ID 98314), equipe externa ao escopo deste atendimento.
