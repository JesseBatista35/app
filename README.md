Executar atividades necessárias para a configuração inicial do BeyondTrust no projeto SIAVO-ms-core. 

OBS: Mais informações detalhadas na REQ.


Histórico de Informações de Trabalho da Ordem de Trabalho
ID da Ordem de Trabalho	 WO0000081940371
Criado em	 15/10/2026 09:46:16
Criado por	 P730708
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Campo "Notas" ajustado pelo Operação Datacenter conforme abaixo:


Executar atividades necessárias para a configuração inicial do BeyondTrust no projeto SIAVO-ms-core.

OBS: Mais informações detalhadas na REQ.
ID da Ordem de Trabalho	 WO0000081940371
Criado em	 15/10/2026 09:46:03
Criado por	 P730708
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Demanda inicial sem viés de falha, erro, degradação ou esgotamento de infraestrutura, serviço, máquina, armazenamento, rotina ou situação que não esteja na iminência de tornar-se incidente. Previsto atendimento em até 24 horas úteis.
[CENTRAL-SID]
ID da Ordem de Trabalho	 WO0000081940371
Criado em	 15/10/2026 09:03:17
Criado por	 P558217
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezado(a),



Informamos que sua solicitação foi recebida.  



Nosso SLA para atendimento é de até 24h úteis, analisaremos a solicitação para nos certificarmos que o atendimento está dentro do escopo de atuação da nossa equipe.



Caso seja identificado que o atendimento não corresponde ao nosso escopo, a solicitação será redirecionada à equipe responsável.



Novas informações e atualizações serão registradas diretamente nesta WO.



Atte.



Esteira Devops DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081940371
Criado em	 15/10/2026 09:02:24
Criado por	 Remedy Application Service
Origem de Comunicação	 E-mail
Exibir Acesso	 Interno
Notas	 Este ticket foi criado a partir do sistema de solicitação de serviço.
Impresso por P585600 em Quinta-feira, 15/10/2026 11:29:05


Prezados,

Solicito a execução das atividades necessárias para a configuração inicial do BeyondTrust no projeto SIAVO-ms-core, conforme descrito abaixo:

Atividades solicitadas
Adicionar a task do BeyondTrust na release pipeline do projeto, posicionando-a após a task Cria_APP_OKD.
Criar a library para o ambiente DES com a seguinte nomenclatura:
SIAVO-ms-core-BT-VAULT-DES

Validação:
Solicito, a confirmação de que o padrão de nomenclatura da library informado acima está de acordo com as diretrizes vigentes.

Documentação de configuração encaminhada à equipe: https://devops.caixa/projetos/Caixa/_wiki/wikis/Caixa.wiki/1935/Configura%C3%A7%C3%A3o-Beyondtrust-Quarkus#

Pipeline do projeto: https://devops.caixa/projetos/Caixa/_build?definitionId=7049

A library deverá conter os seguintes campos:

BT_CLIENT_ID
BT_CLIENT_SECRET
BT_SECRETS_LIST

Agradeço o apoio e fico à disposição para quaisquer esclarecimentos.

Atenciosamente,
Tiago Seibel
Fábrica - Fóton Informática
