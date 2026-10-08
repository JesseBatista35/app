da Tarefa	 TAS000050480711
Criado em	 15/09/2026 08:44:21
Criado por	 P751081
Origem	 
Exibir Acesso	 Interno
Sumário	 Script planejado
Notas	 À

CETEL/REDES

======================EXECUÇÃO=========================
Prezados,

Regras planejadas a partir do AlgoSec via Fireflow #32553 Pedido: 97802 - CRQ000001499711

Fluxo Origem -> Destino: CNPRDFW001-1

***OBS: Aplicar deploy no firewall***

========================VALIDACÃO========================
>> CNPRDFW001-1
packet-tracer input AUTO_DES_APRES TCP 10.116.221.46 65001 10.116.29.201 31153

ping tcp 10.116.29.201 31153 source 10.116.221.46 65001

Att,
João Victor Sousa Prudencio
Analista de Datacenter - Redes
TELEDATA/CETEL/REDES
Printed by P585600 on Quinta-feira, 08/10/2026 10:38:54



ID da Tarefa	 TAS000050480712
Criado em	 30/09/2026 20:06:35
Criado por	 P687208
Origem	 
Exibir Acesso	 Interno
Sumário	 Script aplicado conforme tarefa de planejamento.
Notas	 À

TELEDATA/CETEL/REDES ]

A regra foi aplicada conforme tarefa de planejamento.

Att,
Igor Alexandro
Preposto - Redes
TELEDATA/CETEL/REDES
Printed by P585600 on Quinta-feira, 08/10/2026 10:39:24

Histórico de Informações de Trabalho
ID da Tarefa	 TAS000050480713
Criado em	 30/09/2026 20:07:01
Criado por	 P687208
Origem	 
Exibir Acesso	 Interno
Sumário	 Script Validado.
Notas	 À

TELEDATA/CETEL/REDES

Foi validado que as regras estão permitindo o fluxo. Seguem as evidências:

CNPRDFW001-1# packet-tracer input AUTO_DES_APRES TCP 10.116.221.46 65001 10.11$
Action: allow
CNPRDFW001-1# ping tcp 10.116.29.201 31153 source 10.116.221.46 65001
Type escape sequence to abort.
Sending 5 TCP SYN requests to 10.116.29.201 port 31153
from 10.116.221.46 starting port 65001, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 1/1/1 ms

Att,
Igor Alexandro
Preposto - Redes
TELEDATA/CETEL/REDES
Printed by P585600 on Quinta-feira, 08/10/2026 10:39:36
