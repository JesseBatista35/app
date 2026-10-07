Bom dia, tudo bem?
Estamos com um sucessivo problema na pipeline do módulo de backend do SIPQV. 

Na etapa "Configurando Stack de Monitoração". Poderiam nos ajudar?

https://devops.caixa/projetos/Caixa/_releaseProgress?_a=release-environment-logs&releaseId=536631&environmentId=2493276

Histórico de Informações de Trabalho da Ordem de Trabalho
ID da Ordem de Trabalho	 WO0000081824515
Criado em	 07/10/2026 10:11:03
Criado por	 C159528
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Bom dia, tudo bem?
O problema persiste. Na mensagem de resolução, foi informada a pipeline do SIGPD, mas não foi essa aplicação que foi informada nessa REQ, e sim o SIPQV. Segue a mais recente evidência do problema:

https://devops.caixa/projetos/Caixa/_releaseProgress?_a=release-pipeline-progress&releaseId=537235
ID da Ordem de Trabalho	 WO0000081824515
Criado em	 06/10/2026 18:53:22
Criado por	 P779823
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezados,  

Validado em Sala via teams a normalização.

Todos
Elza Oliveira Leao
Esse erro inicial apresentado na  etapa "Configurando Stack de Monitoração" da esteira esteira-jboss-vm, a consulta à base PostgreSQL falha na autenticação. Ja foi corrigido na esteira

Todos, em validação com solicitante Ronaldo Mota e equipe de esteiras, situação foi solucionada no script novo, a etapa da pipeline 'Configurando Stack de Monitoração' não está mais presente travando a pipeline na esteira TQS SIGPD-backend. Obrigado pelo empenho de todos

https://teams.microsoft.com/l/chat/19:4800dab4f0414d14a3e9f0a953514e2c@thread.v2/conversations?context=%7B%22contextType%22%3A%22chat%22%7D



Atenciosamente,
P779823 -  Plataforma Intermediária
HITSS/CEPRO20 - Gestão de Identidade e acesso
ID da Ordem de Trabalho	 WO0000081824515
Criado em	 06/10/2026 15:54:14
Criado por	 P972797
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 À CESTI

   Conforme respondido na WO0000081808304, fiz a tentativa de conectar via SSH no host e não é possível, ele deve ser um postgres no Azure.

   Refiz o teste de liberação de firewall e o servidor cadsvaprlx072 (10.122.155.67) tem acesso ao IP  10.244.74.86 na porta 5432.

   Não consegui encontrar o nome do host de IP mas ele deve estar no Azure tal como está o servidor apontado pelo FQDN db-monit-prd.postgres.database.azure.com --> c6cdf8f79b7d.privatelink.postgres.database.azure.com (10.244.74.88) (exemplo)

    A mensagem de erro original, conforme observado em nota anterior, indica problemas de "Password".

    Neste caso sugiro encaminhar esta solicitação para a equipe de segurança que administra/armazena normalmente as senhas dos usuários.

Att.
  Jeandre Bernadelli Guerra
  DBA Suporte - CTIS
ID da Ordem de Trabalho	 WO0000081824515
Criado em	 06/10/2026 11:16:18
Criado por	 P981778
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 À EQUIPE DE BANCO DE DADOS

Durante a etapa "Configurando Stack de Monitoração" da esteira esteira-jboss-vm, ocorreu falha na consulta à base PostgreSQL de monitoração.

Origem: cadsvaprlx072 (10.122.155.67) - agente Azure DevOps
Destino: 10.244.74.86:5432
Banco: monitordb001
Usuário: monitdbadm

Validações realizadas:

- Conectividade com o banco validada com sucesso na porta 5432 (nc/telnet).
- Identificada na configuração da esteira a utilização da base monitordb001 no endereço 10.244.74.86, utilizando o usuário monitdbadm.
- Teste de conexão realizado a partir do agente com a credencial configurada na esteira retornou:

FATAL: password authentication failed for user "monitdbadm"

A conectividade entre origem e destino está operacional. A falha observada está relacionada à autenticação do usuário monitdbadm na base monitordb001.

Solicitação:

Validar se a senha do usuário monitdbadm foi alterada, expirada (VALID UNTIL) ou bloqueada, e informar a credencial vigente para atualização da esteira de implantação.




Thiago Silva
Analista
CTIS / CESTI Esteira DEVOPS DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081824515
Criado em	 06/10/2026 11:02:22
Criado por	 P768728
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezado(a),

Informamos que sua solicitação PRIORIZADA foi recebida .

Nosso SLA para atendimento é de até 8h úteis, analisaremos a solicitação para nos certificarmos que o atendimento está dentro do escopo de atuação da nossa equipe.

Caso seja identificado que o atendimento não corresponde ao nosso escopo, a solicitação será redirecionada à equipe responsável.

Novas informações e atualizações serão registradas diretamente nesta WO.

Atte.

Esteira DEVOPS DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081824515
Criado em	 06/10/2026 10:41:15
Criado por	 P768728
Origem de Comunicação	 
Exibir Acesso	 Público
Notas	 Prezado(a),

Informamos que sua solicitação foi recebida.

Nosso SLA para atendimento é de até 24h úteis, analisaremos a solicitação para nos certificarmos que o atendimento está dentro do escopo de atuação da nossa equipe.

Caso seja identificado que o atendimento não corresponde ao nosso escopo, a solicitação será redirecionada à equipe responsável.

Novas informações e atualizações serão registradas diretamente nesta WO.

Atte.

Esteira Devops DES TQS NPRD
ID da Ordem de Trabalho	 WO0000081824515
Criado em	 06/10/2026 10:39:20
Criado por	 Remedy Application Service
Origem de Comunicação	 E-mail
Exibir Acesso	 Interno
Notas	 Este ticket foi criado a partir do sistema de solicitação de serviço.
Impresso por P585600 em Quarta-feira, 07/10/2026 14:35:53
