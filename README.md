Análise: a aplicação sipdm-api-estudante (DES, namespace sipdm-des) retorna HTTP 500 por não conseguir conectar ao SQL Server do PDM (CRJDEDADNT009 – 10.116.100.127:1433, banco PDMDB001).

A regra anterior, ID 98173 (CRQ000001516018), com origem 10.116.221.183 (egress IP do namespace sipdm-des) e destino 10.116.100.127:1433/TCP, foi aplicada no CNPRDFW001-1. Mesmo assim, o tráfego do pod continuou sem resposta. Os testes mostraram:

do pod sipdm-api-estudante-des → timeout;
do bastion e do ambiente TQS → sucesso (banco ativo).

Conforme análise da CETEL (Adriano da Silva Fernandes), falta liberar o mesmo par origem/destino no túnel/firewall entre o CTC e o site do Rio de Janeiro.

Ação: registrada nova solicitação de regra de firewall ID 98502 (origem 10.116.221.183 → destino 10.116.100.127, TCP/1433), em processo de aprovação (Flávio Gagliardi / Reinaldo Barboza).

Após a execução, valide de dentro do pod com timeout 5 bash -c '</dev/tcp/10.116.100.127/1433'. Nenhuma alteração ou redeploy da aplicação é necessária.

Caso a conectividade não seja restabelecida após a execução da regra ID 98502, abrir nova REQ referenciando a REQ000146876335 e as regras 98173 e 98502, anexando o resultado do teste a partir do pod.
