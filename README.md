A regra 10.116.221.183 -> 10.116.100.127:1433/TCP (CRQ000001516018) foi validada no CNPRDFW001-1, porém o tráfego real da origem continua sem resposta. 
 
Realizado o teste TCP a partir do pod sipdm-api-estudante-des (namespace sipdm-des, egress IP 10.116.221.183 confirmado via netnamespace) para 10.116.100.127:1433 expira sem resposta (timeout). 
 
O serviço está disponível no destino: o teste a partir do pod sipdm-api-estudante-tqs (egress IP [IP do TQS]) para 10.116.100.127:1433 retorna sucesso. 
 
Solicitamos verificar o caminho efetivo da origem 10.116.221.183 até o destino, incluindo outros firewalls no trajeto, e, caso a rede esteja liberada, indicar se há filtro de origem no servidor de destino.



1 nova atividade
9 novas notificações
Há menu de contexto
Chat




Não lido
Canais
Chats
Chats de reunião
Mensagem não lidaÚltima mensagemChats em grupoChat de reuniãoChatFuncionários mencionadosMencionar todosImportanteUrgenteRascunhoRascunhoMudo ativadoReunião em andamentoReunião agora em andamentoVocê não pode enviar mensagens porque não é membro do chat.Não é possível enviar mensagens a este botPrivadoCompartilhadoTem um menu de contextoCanal mencionadoEquipe mencionadaFuncionários mencionadosNão lidoNão lidoReunião em andamentoNão lidoCanalEquipeTem mensagens fixadasVer maisComunidadeMostrar temporariamenteTem um menu de contextoChat com emblemaChats com emblema
Tem um menu de contexto

Equipes e canais

SIPDM-api-estudante- REGRA DE FW


Chat

Compartilhado

Notas

Recapitular

Há menu de contexto

Reunir agora


6



Lista de Mensagens
imagem por Bruno Kingma Clemente
Bruno Kingma Clemente
quinta-feira 15:54

imagem

Bruno Kingma Clemente adicionou Cleomar Barros de Oliveira Junior ao chat.
Jesse , pode entra aqui por favor, o Adrian... por Cleomar Barros de Oliveira Junior
Cleomar Barros de Oliveira Junior
quinta-feira 16:02

Jesse, pode entra aqui por favor, o Adriano da CETEL identificou alguns problemas de configuração na esteira.

Bruno Kingma Clemente   e   Cleomar Barros ... por Jesse Mouta Pereira Batista
quinta-feira 16:06
Jesse Mouta Pereira Batista

Bruno Kingma Clemente  e  Cleomar Barros de Oliveira Junior me desculpem eu estou em uma sala de ADDR no momento não consigo entrar, se o Adriano da Silva Fernandes puder identificar aqui os problemas na esteira. eu faço o ajuste. Agradeço

então, Jesse, o Adriano identificou possíve... por Cleomar Barros de Oliveira Junior
Cleomar Barros de Oliveira Junior
quinta-feira 16:08

então, Jesse, o Adriano identificou possíveis problemas, mas precisamos conversar com vc junto para ver se esse é o diagnostico mesmo.

que horas vc pode hoje ainda por favor? por Cleomar Barros de Oliveira Junior
Cleomar Barros de Oliveira Junior
quinta-feira 16:08

que horas vc pode hoje ainda por favor?

Chamada encerrada às quinta-feira 16:09 após 45 minutos 50 segundos
Cleomar Barros de Oliveira Junior por Jesse Mouta Pereira Batista
quinta-feira 16:55
Jesse Mouta Pereira Batista

Cleomar Barros de Oliveira Junior

boa tarde por Jesse Mouta Pereira Batista
quinta-feira 16:55
Jesse Mouta Pereira Batista

boa tarde

surgiu uma janela agora por Jesse Mouta Pereira Batista
quinta-feira 16:55
Jesse Mouta Pereira Batista

surgiu uma janela agora

opa, então bora por Cleomar Barros de Oliveira Junior
Cleomar Barros de Oliveira Junior
quinta-feira 16:55

opa, então bora

Reunião encerrada quinta-feira 17:12 após 16 minutos 35 segundos, SIPDM-api-estudante- REGRA DE FW, quinta-feira, 22 de outubro de 2026 17:08 - 17:12, link para exibir a recapitulação, 1 arquivo, Pressione Enter para exibir mais
Notas foram criadas nesse chat.
Notas
Jesse Mouta Pereira Batista alterou o nome do grupo para SIPDM-api-estudante- REGRA DE FW.
Adriano da Silva Fernandes , só para confi... por Jesse Mouta Pereira Batista
quinta-feira 17:17
Jesse Mouta Pereira Batista

Adriano da Silva Fernandes, só para confirmar: o teste que falha é do pod (origem 10.116.221.183) para 10.116.100.127:1433, sem VPN de usuário no meio. A nova regra é no túnel/firewall entre CTC e o site do Rio, para essa mesma origem e destino?”

Adriano da Silva Fernandes por Jesse Mouta Pereira Batista
quinta-feira 17:29
Jesse Mouta Pereira Batista

Adriano da Silva Fernandes

Todos , bom dia por Jesse Mouta Pereira Batista
09:21
Jesse Mouta Pereira Batista

Todos, bom dia

Jesse Mouta Pereira Batista adicionou Thiago Rafael Cavalcante Pereira ao chat e compartilhou todo o histórico de chats.
Jesse Mouta Pereira Batista adicionou Flavio de Almeida Gagliardi ao chat e compartilhou todo o histórico de chats.
Cleomar Barros de Oliveira Junior , estou n... por Jesse Mouta Pereira Batista
09:22
Jesse Mouta Pereira Batista

Cleomar Barros de Oliveira Junior, estou no aguardo da confirmação acima para podermos prosseguir com a solicitação da regra. 

Bom dia pessoal,  Adriano , pode ajudar a g... por Cleomar Barros de Oliveira Junior
Cleomar Barros de Oliveira Junior
09:23

Bom dia pessoal, Adriano, pode ajudar a gente com essa informação, estamos bem atrasado pessoal, peço o apoio e cerelidade de vcs.

BOM DIA !!! por Adriano da Silva Fernandes
Adriano da Silva Fernandes
09:31

BOM DIA !!!

podemos testa se esta funcionando?? por Adriano da Silva Fernandes
Adriano da Silva Fernandes
09:38

podemos testa se esta funcionando??

Adriano da Silva Fernandes , bom dia tudo b... por Jesse Mouta Pereira Batista
09:40
Jesse Mouta Pereira Batista

Adriano da Silva Fernandes, bom dia tudo bem? ainda não foi solicitada a regra de FW, precisamos da confirmação:

 

o teste que falha é do pod (origem 10.116.221.183) para 10.116.100.127:1433, sem VPN de usuário no meio. A nova regra é no túnel/firewall entre CTC e o site do Rio, para essa mesma origem e destino?”

sim  por Adriano da Silva Fernandes
Adriano da Silva Fernandes
09:42

sim 

vc lembra o ID dessa regra ??? por Adriano da Silva Fernandes
Adriano da Silva Fernandes
09:43

vc lembra o ID dessa regra ???

imagem por Jesse Mouta Pereira Batista
09:51
Jesse Mouta Pereira Batista

imagem

da primeira que foi solicitada é essa acima por Jesse Mouta Pereira Batista
09:51
Jesse Mouta Pereira Batista

da primeira que foi solicitada é essa acima.

Adriano , conseguiu avaliar? por Cleomar Barros de Oliveira Junior
Cleomar Barros de Oliveira Junior
11:25

Adriano, conseguiu avaliar?

na verdade não entendi o que vc está avalia... por Cleomar Barros de Oliveira Junior
Cleomar Barros de Oliveira Junior
11:27

na verdade não entendi o que vc está avaliando da solicitação anterior, nós já não identificamos que a regra estava errada? Entendi que só precisava dessa confirmação de origem e destino para o Jesse criar outra solicitação

Início da citação, Jesse Mouta Pereira Bati... por Adriano da Silva Fernandes
Adriano da Silva Fernandes
11:40

Jesse Mouta Pereira Batista
27/10/2026 09:40
Adriano da Silva Fernandes, bom dia tudo bem? ainda não foi solicitada a regra de FW, precisamos da confirmação: o teste que falha é do pod (origem 10.116.221.183) para 10.116.100.127:1433, sem VPN…
isso aqui mesmo 

Jesse , pode dar prosseguimento na abertura... por Cleomar Barros de Oliveira Junior
Cleomar Barros de Oliveira Junior
11:46

Jesse, pode dar prosseguimento na abertura do novo item por favor?


👍
1 Curtir reação.

quem seria o responsável pela aprovação e a... por Cleomar Barros de Oliveira Junior
Cleomar Barros de Oliveira Junior
11:46

quem seria o responsável pela aprovação e autorização da CRQ?

Cleomar Barros de Oliveira Junior , posso s... por Jesse Mouta Pereira Batista
12:19
Jesse Mouta Pereira Batista

Cleomar Barros de Oliveira Junior, posso sim. preciso que seja aberto uma nova REQ para que seja atrelado ao nova solicitação de regra de fw. pode colocar no campo da nota que é aos meus cuidados, que jÁ vou providenciar a solicitação; 

Início da citação, Cleomar Barros de Olivei... por Jesse Mouta Pereira Batista
12:19
Jesse Mouta Pereira Batista

Cleomar Barros de Oliveira Junior
27/10/2026 11:46
quem seria o responsável pela aprovação e autorização da CRQ?
quando eu abro coloco o Flavio Gagliardi e o Reinaldo Barboza

Início da citação, Jesse Mouta Pereira Bati... por Flavio de Almeida Gagliardi
Flavio de Almeida Gagliardi
12:20

Jesse Mouta Pereira Batista
27/10/2026 12:19
quando eu abro coloco o Flavio Gagliardi e o Reinaldo Barboza
pode nos colocar Jesse Mouta Pereira Batista, eu peço aqui pro Reinaldo aprovar e gero a mudança na sequencia


👍
1 Curtir reação.

Início da citação, Flavio de Almeida Gaglia... por Cleomar Barros de Oliveira Junior
Cleomar Barros de Oliveira Junior
12:52

Flavio de Almeida Gagliardi
27/10/2026 12:20
pode nos colocar Jesse Mouta Pereira Batista, eu peço aqui pro Reinaldo aprovar e gero a mudança na sequencia
obrigado Flavio


👍
1 Curtir reação.

Bruno , pode abrir uma nova REQ por favor? por Cleomar Barros de Oliveira Junior
Cleomar Barros de Oliveira Junior
12:53

Bruno, pode abrir uma nova REQ por favor?

Última lida
REQ000146876335 por Bruno Kingma Clemente
Bruno Kingma Clemente
13:04

REQ000146876335

Início da citação, Bruno Kingma Clemente, 2... por Thiago Rafael Cavalcante Pereira
Thiago Rafael Cavalcante Pereira
13:22

Bruno Kingma Clemente
27/10/2026 13:04
REQ000146876335
Jesse Mouta Pereira Batista já coloquei a demanda na sua fila, obg

tem menu de contexto



👍

❤️

😆

😮





entao o correto é abrimos uma nova regra de firal npe o adriano confimou me ajuda a abrir a regra
