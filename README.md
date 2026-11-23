Boa tarde, Todos! Analisei o ambiente e encontrei os pontos abaixo.
 
1. Script configurado no job


O job CRIACAO_OS_SIGDU está apontando para /producao/simil-precificacao-rotinas-batch.sh, mas esse arquivo não existe no servidor. O script publicado pela release é o /producao/script_simil_rotinas.sh. É ele que executa o simil-precificacao-rotinas-batch.jar em /opt/batch/deploy.

Ajustes necessários na definição do job no Control-M:
 
File Name: script_simil_rotinas.sh

Variável JOB_NAME: informar o nome do job Spring Batch a ser executado. O script recebe esse valor do Control-M.
 
2. Comunicação Control-M -> agente


A comunicação do agente com o servidor está ok, mas até o momento nenhuma execução chegou ao caddeapllx2501. podemos solicitar a liberação da regra de firewall:
 
Origem: cxextrlx038 (10.192.224.54)

Destino: caddeapllx2501 (10.116.200.250)

Porta: TCP 7016
 
Observações para o time de desenvolvimento:
 
No script_simil_rotinas.sh, os parâmetros -Xms/-Xmx estão depois do -jar e por isso não são aplicados à JVM. O correto é java -Xms512m -Xmx1024m -jar "$JAR_FILE" ......
 
fico no aguardo. 
 
Jesse Mouta Pereira Batista adicionou Patricia Vourakis Barbosa Braga ao chat e compartilhou todo o histórico de chats.

 
Jesse Mouta Pereira Batista
Boa tarde, Todos! Analisei o ambiente e encontrei os pontos abaixo.   1. Script configurado no job  O job CRIACAO_OS_SIGDU está apontando para /producao/simil-precificacao-rotinas-batch.sh, mas esse…
Bom dia, então seria o nome do .sh que está errado ? 
 
vou realizar o ajuste para simil-precificacao-rotinas-batch.sh 
 
Jesse Mouta Pereira Batista
Boa tarde, Todos! Analisei o ambiente e encontrei os pontos abaixo.   1. Script configurado no job  O job CRIACAO_OS_SIGDU está apontando para /producao/simil-precificacao-rotinas-batch.sh, mas esse…
Vou solicitor a regra para garantir
 
fiz os ajustes, mas estou com esse problema 
 
Vinicius Tavares Lobato Gama adicionou Eduardo Rosa Calais ao chat e compartilhou o histórico de chats do dia anterior.

 
Jesse, meu amigo, bom dia! Tudo bem?
 
Quem seria o colega CAIXA responsável pelo seu processo para que possamos pedir a ele uma agenda em que possamos, em conjunto, tentar resolver essa comunicação?
 
Nosso projeto é priorizado e em relação a parte "burocrática" acredito que conseguimos formalmente pedir essa agenda



 <img width="800" height="443" alt="image" src="https://github.com/user-attachments/assets/581d108c-36fe-4eee-bcc5-7c0392c301ea" />
