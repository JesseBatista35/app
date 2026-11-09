Boa tarde, Jesse, tudo bem? Sobre o chamado REQ000146916154, de configuração do agente do Control-M nas esteiras ágeis, poderia me informar como posso solicitar os ajustes que apontou na resolução do chamado?
 
Iury Damasceno Mota, boa tarde, tudo bem e com voce? posso dar uma olhada, e te passar um retorno, porem hoje não consigo, se puder me chamar na segunda feira, pois eu encerrei meu turno mais cedo para ir a uma consulta hoje. obrigado. 
 
Tranquilo! Mandei imaginando que ficaria para esta semana mesmo
 
Obrigado
 
Boa tarde! Para referência, o projeto que estamos com esse problema de conexão é o SIMIL-precificacao-rotinas-batch - Repos, que foi feito baseado no projeto SISME-rotinas - Repos.



 À CAIXA

Prezados,

Conforme solicitado análise Validação do agente Control-M – SIMIL-precificacao-rotinas-batch (DES)

Foi validada a configuração do agente Control-M no servidor caddeapllx2501.agil.nprd.caixa.gov.br (10.116.200.250), aplicada pela release em 15/10/2026.

Resultado: o agente está instalado e em execução, mas não se comunica com o servidor Control-M.

Processos do agente (Listener, Tracker e Tracker-Worker) em execução.
O agente está configurado para o servidor crjdeaprlx038 (autorizados: crjdeaprlx038 e crjdeaprlx039), portas 7015/7016.

O ag_diag_comm retorna Failed no ping ao Control-M/Server.

O nome crjdeaprlx038 não é resolvido. As entradas no /etc/hosts, vindas do arquivo etc/hosts-des do repositório SIMIL-precificacao-rotinas-batch-config, estão comentadas. 

Ele também não está no DNS.
Pelos IPs antigos (10.116.99.99 e 10.116.99.100), a porta 7015 recusa a conexão.

Comparação: um agente de DES que funciona normalmente (caddeapllx2695) aponta para o servidor sspdeaprlx0028 (10.116.84.154), portas 18007/18008, com comunicação OK. A partir do caddeapllx2501, a porta 18007 desse servidor está acessível.

Conclusão: a configuração aplicada aponta para um servidor Control-M que não está acessível. Para o agente funcionar no BR DES - Negocial, é preciso ajustar o servidor e as portas do Control-M, além do arquivo etc/hosts-des, e depois confirmar o cadastro do agente no servidor.


Atenciosamente,

Jessé Mouta Pereira Batista
Analista
CTIS / CESTI Esteira DEVOPS DES TQS NPRD


