<img width="1835" height="590" alt="image" src="https://github.com/user-attachments/assets/226a901b-5960-4492-8ba4-c4f9acc4fe78" />



Histórico de Informações de Trabalho
ID da Tarefa	 TAS000050679845
Criado em	 15/10/2026 21:54:29
Criado por	 P787922
Origem	 
Exibir Acesso	 Interno
Sumário	 Script Validado.
Notas	 À

TELEDATA/CETEL/REDES

Foi validado que o fluxo está permitido. Segue evidência:

CNPRDFW001-1# packet-tracer input AUTO_DES_APRES TCP 10.116.221.183 65001 10.1$
Action: allow
CNPRDFW001-1# ping tcp 10.116.100.127 1433 source 10.116.221.183 65001
Type escape sequence to abort.
Sending 5 TCP SYN requests to 10.116.100.127 port 1433
from 10.116.221.183 starting port 65001, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 1/1/1 ms

Att,
Felipe de Jesus Araujo
Analista de Infraestrutura - Redes
TELEDATA/CETEL/REDES
Printed by P585600 on Quarta-feira, 21/10/2026 15:07:21



Histórico de Informações de Trabalho
ID da Tarefa	 TAS000050679844
Criado em	 15/10/2026 21:54:13
Criado por	 P787922
Origem	 
Exibir Acesso	 Interno
Sumário	 Script aplicado conforme tarefa de planejamento.
Notas	 À

TELEDATA/CETEL/REDES

A regra foi aplicada conforme tarefa de planejamento.

Att,
Felipe de Jesus Araujo
Analista de Infraestrutura - Redes
TELEDATA/CETEL/REDES
Printed by P585600 on Quarta-feira, 21/10/2026 15:07:34



ID da Tarefa	 TAS000050679843
Criado em	 15/10/2026 10:36:33
Criado por	 P929918
Origem	 
Exibir Acesso	 Interno
Sumário	 script planejado
Notas	 À

TELEDATA/CETEL/REDES

############ PLANO DE EXECUÇÃO ############
Prezados,
Regras planejadas a partir do AlgoSec via Fireflow #33603 CRQ000001516018.
Acessar o Algosec (10.122.156.210) para implementar as mudanças.
Fluxo Origem -> Destino:  -> CNPRDFW001-1

############ PLANO DE VALIDAÇÃO ############
CNPRDFW001-1
packet-tracer input AUTO_DES_APRES TCP 10.116.221.183 65001 10.116.100.127 1433

ping tcp 10.116.100.127 1433 source 10.116.221.183 65001

Att,
Adriano da Silva Fernandes
Analista de Datacenter - Redes
TELEDATA/CETEL/REDES
Printed by P585600 on Quarta-feira, 21/10/2026 15:07:46
