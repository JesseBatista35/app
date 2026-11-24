Solicitamos suporte em sala TEAMS com nossa equipe Dev Java. Visando obtermos auxílio em tela que está dando TIMEOUT quando realizamos UPLOAD de arquivo em DES.


Histórico de Informações de Trabalho da Ordem de Trabalho
ID da Ordem de Trabalho	 WO0000082251789
Criado em	 24/11/2026 09:26:28
Criado por	 P776093
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Demanda inicial sem viés de falha, erro, degradação ou esgotamento de infraestrutura, serviço, máquina, armazenamento, rotina ou situação que não esteja na iminência de tornar-se incidente. Previsto atendimento em até 72 horas.

[CENTRAL-SID]
ID da Ordem de Trabalho	 WO0000082251789
Criado em	 24/11/2026 09:23:24
Criado por	 P935210
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 À CESTI,

Conforme parecer técnico em nota anterior, segue para avaliação.

Atenciosamente,
Clara Dias.
Preposta de Redes Datacenter
ID da Ordem de Trabalho	 WO0000082251789
Criado em	 24/11/2026 08:49:38
Criado por	 P929918
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 À

TELEDATA/CETEL/REDES

Prezados,
Informo que as regras de firewall foram validadas e a conectividade entre as redes encontra-se operacional.

Att,
Adriano da Silva Fernandes
Analista de Datacenter - Redes
TELEDATA/CETEL/REDES
ID da Ordem de Trabalho	 WO0000082251789
Criado em	 17/11/2026 08:57:02
Criado por	 P564449
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Bom dia, Valdir.

Seguem as informações disponíveis para análise:

FQDN: sigec-csc-frontn-des.apps.nprd.caixa
Servidor backend: CADDEAPLLX765
IP backend: 10.116.193.253
Porta da aplicação: HTTPS (443)
Funcionalidade afetada: Exportação de Base (download de arquivo)
Erro apresentado: HTTP 504 Gateway Timeout
Tempo para ocorrência do erro: aproximadamente 120 segundos

Durante as validações realizadas na aplicação, não foram identificadas configurações locais com timeout de 2 minutos. A Route OpenShift encontra-se configurada com timeout de 10 minutos através da annotation haproxy.router.openshift.io/timeout: 10m.

Solicitamos apoio na verificação da existência de algum equipamento ou camada intermediária de rede (F5, Proxy, WAF, Gateway ou balanceador) que possa estar encerrando a conexão após aproximadamente 120 segundos.

Caso necessário, podemos solicitar ao usuário a realização de um novo teste para levantamento do IP de origem e horário exato da ocorrência.

Atenciosamente,

Kallebe M. Vieira
Analista CTIS / CESTI – Esteira DevOps DES TQS NPRD
ID da Ordem de Trabalho	 WO0000082251789
Criado em	 17/11/2026 08:06:48
Criado por	 P558217
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezado(a),

 

Informamos que sua solicitação foi recebida.

 

Conforme definição da Coordenação NPRD (CESTI36) e em conformidade com o fluxo de atendimento estabelecido para a Esteira DevOps NPRD, os atendimentos realizados por esta equipe seguem SLAs específicos, distintos dos praticados pelas demais macrocélulas.  

 

Dessa forma, o SLA desta solicitação foi ajustado para até 24 horas úteis, prazo aplicável à sua classificação.

 

Nesse período, a demanda será analisada para validação do escopo de atuação da equipe e definição do tratamento adequado.

 

Caso seja identificado que a solicitação não pertence ao escopo de atendimento da Esteira DevOps NPRD, a demanda será direcionada à equipe responsável, observando os fluxos e processos vigentes.

 

Novas informações e atualizações serão registradas diretamente nesta WO.

 

Atenciosamente,

 

Esteira DevOps NPRD

ID da Ordem de Trabalho	 WO0000082251789
Criado em	 12/11/2026 21:24:05
Criado por	 P695452
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Para análise da equipe de rede, será necessário informar os IP's de origem/destino porta e fqdn.


Atenciosamente,
Valdir Soares
TELEDATA\CETEL\REDE
ID da Ordem de Trabalho	 WO0000082251789
Criado em	 11/11/2026 09:52:42
Criado por	 P564449
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Bom dia

Durante a análise foram realizadas as seguintes validações:

A Route OpenShift da aplicação encontra-se configurada com timeout de 10 minutos através da annotation:

haproxy.router.openshift.io/timeout: 10m
 
Não foi identificada configuração de timeout de 2 minutos no arquivo standalone-full-ha.xml do JBoss.
O parâmetro max-post-size está configurado para 200 MB, não havendo indícios de limitação relacionada ao tamanho do upload.
O serviço JBoss encontra-se ativo nas portas 8080 e 8443.
Não foram identificados proxies locais (Apache, Nginx ou HAProxy) na VM da aplicação.
Os logs da aplicação não apresentam evidências de timeout relacionado ao processamento da requisição de upload.

Considerando que o erro reportado é um HTTP 504 Gateway Timeout, ocorrendo após aproximadamente 2 minutos, solicitamos apoio do time de Redes para verificar a existência de alguma camada intermediária de infraestrutura (F5, Proxy, Gateway, WAF ou equipamento de balanceamento) que possa estar aplicando timeout de 120 segundos entre o cliente e a aplicação.

Atenciosamente,

Kallebe M. Vieira
Analista CTIS / CESTI – Esteira DevOps DES TQS NPRD
ID da Ordem de Trabalho	 WO0000082251789
Criado em	 11/11/2026 07:11:53
Criado por	 P558217
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezado(a),


Informamos que por ter reaberto sua solicitação hoje o atendimento será retomado nesta data.  

Iremos realizar uma nova análise conforme as informações adicionais registradas na sua última nota.

Ressaltamos que um novo SLA de 24h úteis passa a vigorar a partir de agora.

Todas as atualizações e evoluções do atendimento serão registradas diretamente nesta WO.


Atte.  

CTIS / CESTI Esteira DEVOPS DES TQS NPRD
ID da Ordem de Trabalho	 WO0000082251789
Criado em	 10/11/2026 14:38:18
Criado por	 P730708
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Campo "Notas" ajustado pelo Operação Datacenter conforme abaixo:

Avaliar e corrigir erro de timeout na realização de download de arquivo. Conforme detalhamento em REQ.

Obs: Data final mantida para o dia 11/11/2026 11:50:32, conforme ajuste realizado pela equipe técnica.

OBS: As informações passadas não foram suficientes para identificação do IC. A equipe técnica responsável deverá sanar esta pendência.

OBS: Não é possível relacionar a respectiva demanda, pois não há item de configuração aplicável para este caso.
[Sem Item de Configuração a Relacionar]
ID da Ordem de Trabalho	 WO0000082251789
Criado em	 10/11/2026 14:37:10
Criado por	 P730708
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Demanda inicial com viés de falha, erro, degradação ou esgotamento de infraestrutura, serviço, máquina, armazenamento, rotina ou situação que esteja na iminência de tornar-se incidente. Previsto atendimento no prazo indicado pelo demandante.

[CENTRAL-SID]
ID da Ordem de Trabalho	 WO0000082251789
Criado em	 10/11/2026 14:34:39
Criado por	 C074256
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Erro persiste. Favor interagirmos pelo TEAMS. Por favor!
ID da Ordem de Trabalho	 WO0000082251789
Criado em	 10/11/2026 12:47:49
Criado por	 P564449
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Boa tarde, Roberto.

Foi realizado o ajuste de timeout do upload da aplicação para 10m conforme o solicitado.

oc get route sigec-csc-frontend-tqs -o yaml | grep -i timeout
   haproxy.router.openshift.io/timeout: 10m
         f:haproxy.router.openshift.io/timeout: {}

Qualquer dúvida estou à disposição.

Atenciosamente,
Kallebe M. Vieira
Analista
CTIS / CESTI – Esteira DevOps DES TQS NPRD
ID da Ordem de Trabalho	 WO0000082251789
Criado em	 10/11/2026 12:16:38
Criado por	 C074256
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Solicitamos aumentar o parâmetro de 'Tempos' de 2 para 10 minutos. Conforme consta na Evidência2 que segue anexo.
ID da Ordem de Trabalho	 WO0000082251789
Criado em	 10/11/2026 12:05:22
Criado por	 C074256
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 RETIFICAMOS o erro está ocorrendo no ambiente de TQS, conforme evidência que segue anexo.
ID da Ordem de Trabalho	 WO0000082251789
Criado em	 10/11/2026 11:52:25
Criado por	 P558217
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezado(a),

 

Informamos que sua solicitação foi recebida.

 

Conforme definição da Coordenação NPRD (CESTI36) e em conformidade com o fluxo de atendimento estabelecido para a Esteira DevOps NPRD, os atendimentos realizados por esta equipe seguem SLAs específicos, distintos dos praticados pelas demais macrocélulas.  

 

Dessa forma, o SLA desta solicitação foi ajustado para até 24 horas úteis, prazo aplicável à sua classificação.

 

Nesse período, a demanda será analisada para validação do escopo de atuação da equipe e definição do tratamento adequado.

 

Caso seja identificado que a solicitação não pertence ao escopo de atendimento da Esteira DevOps NPRD, a demanda será direcionada à equipe responsável, observando os fluxos e processos vigentes.

 

Novas informações e atualizações serão registradas diretamente nesta WO.

 

Atenciosamente,

 

Esteira DevOps NPRD
ID da Ordem de Trabalho	 WO0000082251789
Criado em	 10/11/2026 11:50:31
Criado por	 Remedy Application Service
Origem de Comunicação	 E-mail
Exibir Acesso	 Interno
Notas	 Este ticket foi criado a partir do sistema de solicitação de serviço.
Impresso por P585600 em Terça-feira, 24/11/2026 10:18:12


me ajdua a resolver isso
