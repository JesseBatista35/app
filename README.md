show conn. Ele mostra que as conexões para o 10.116.29.23:1433 saem com origem 10.116.208.104, que é o IP do nó ceadecldlx084, e não com o egress IP 10.116.221.46. Isso confirma o que vimos: a regra da CRQ está correta e a falha está do lado do OKD, que não está aplicando o egress IP ao tráfego do namespace sihdg-tqs. Vamos tratar com a plataforma OKD. Por ora não há ação necessária da Redes; peço apenas que mantenham as capturas JV/JV1 ativas para repetirmos o teste após o ajuste. Obrigado!


Resumo
O tráfego do namespace sihdg-tqs (cluster NPRD, egress IP 10.116.221.46) sai do cluster com o IP do nó de egress ceadecldlx084 (10.116.208.104) e não com o egress IP configurado. Por isso a conexão da aplicação SIHDG-JBOSS8 (TQS) com o banco 10.116.29.201:31153 dá timeout, já que a regra de firewall da CRQ000001499711 libera apenas o 10.116.221.46.

Impacto
O deploy do SIHDG-JBOSS8-TQS está bloqueado (releases 29 a 34 em Error). Apenas o pod antigo (revisão 28, banco anterior) continua no ar.

Evidências

No firewall CNPRDFW001-1 (Redes), show conn | i 10.116.29.23.*1433 mostra conexões com origem 10.116.208.104 (IP do nó 084), e nenhuma com origem 10.116.221.46.
Testes TCP a partir de pods do sihdg-tqs em dois nós diferentes dão timeout em 10.116.29.201:31153:
Nó ceadecldlx081: 14:23:47, 14:23:52 e 14:23:57 (-03)
Nó ceadecldlx077: 14:34:51, 14:34:56 e 14:35:01 (-03)
Esses testes não aparecem nas capturas do firewall com origem 10.116.221.46.
Teste feito a partir do próprio nó 084 com nc -s 10.116.221.46 para 10.116.29.201:31153, às 14:20:00 (-03), conectou normalmente e aparece completo na captura (SYN, SYN-ACK, ACK, FIN, RST). Ou seja, a regra de firewall e a rede externa estão corretas.

O que já foi verificado e está correto

NetNamespace sihdg-tqs (netid 12401478): egressIPs: [10.116.221.46], e o IP não está atribuído a nenhum outro namespace.
HostSubnet ceadecldlx084.nprd.caixa: 10.116.221.46 presente em egressIPs, dentro do egressCIDRs 10.116.192.0/19.
Interface do nó 084: 10.116.221.46 ativo como IP secundário em ens192:eip.
iptables do nó 084: regra SNAT --to-source 10.116.221.46 na chain OPENSHIFT-MASQUERADE com mark 0xbd3b46 (equivalente ao netid 12401478).
Logs do pod SDN sdn-rprgw (nó 084) e sdn-4g965 (nó 081): sem menção ao 10.116.221.46 ou a erros de egress.

Pedido

Analisar por que a regra SNAT do 10.116.221.46 não é aplicada ao tráfego dos pods do sihdg-tqs quando ele chega ao nó 084.
Verificar o caminho entre os nós de origem dos pods (081, 077) e o nó de egress 084 (encaminhamento do tráfego do namespace e marcação do pacote).
Se necessário, recriar o egress do namespace (por exemplo, reaplicar a atribuição do IP ou reiniciar o pod SDN do nó 084), em janela combinada, já que o nó é compartilhado com outros namespaces.

Validação após o ajuste
Repetiremos o teste a partir de um pod do sihdg-tqs para 10.116.29.201:31153, com as capturas JV e JV1 do firewall ativas, e esperamos ver pacotes com origem 10.116.221.46.

Referências: CRQ000001499711, WO/REQ do SIHDG-JBOSS8-TQS.
