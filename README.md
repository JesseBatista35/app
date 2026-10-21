Prezados,

Retomamos a análise considerando o pedido original: entender por que a versão mais recente (SIGSJ-alvara-20261020.1646-3.0.12.1-SNAPSHOT, release 543669) não sobe no OKD. Pedimos desculpas pela reexecução anterior com a versão antiga (3.0.2.1-SNAPSHOT), que de fato não respondia ao que foi solicitado.

1. Por que a versão 3.0.12.1 não sobe

Reimplantamos a versão 3.0.12.1 (pod sigsj-alvara-des-703) e acompanhamos o rollout. A aplicação inicia normalmente, mas o endpoint de readiness retorna DOWN, então o OKD nunca considera o pod pronto e mantém a versão anterior em execução:

GET /q/health/ready  ->  "status": "DOWN"
  - Database connections health check ......... UP
  - CNJ indisponível .......................... DOWN
  - SmallRye Reactive Messaging - readiness ... UP

GET /q/health/live   ->  "status": "UP"

O único check com falha é o health check customizado do CNJ.

2. Comparação com a versão que sobe

A versão 3.0.9.101-SNAPSHOT (build 20261021.1323), que está em execução no momento, usa a mesma DeploymentConfig, as mesmas variáveis de ambiente, o mesmo banco e as mesmas credenciais. Nela o mesmo check retorna “CNJ disponível”: UP.

O log dessa versão mostra que a chamada ao endpoint https://apim-parceiros-sandbox.azure-api.net/deposito-judicial/cnj/api/v1/usuarios/healthcheck/perfis já retorna HTTP 400 no ambiente DES. Mesmo assim, a versão 3.0.9.101 considera o CNJ disponível. Na 3.0.12.1 o mesmo cenário resulta em DOWN.

Como o ambiente é idêntico nas duas execuções, a diferença está no código da versão 3.0.12.1, na lógica do health check do CNJ.

3. Por que o motivo não aparecia nas etapas da release

A task “Verificando Status do Deployment” aguarda o pod ficar Ready. Como o readiness permanece DOWN, ela encerra por timeout sem detalhar a causa, que está no conteúdo do /q/health/ready.
Na task “Logs da Aplicação”, a versão 3.0.12.1 não registrou no console nenhuma linha além do comando de inicialização da JVM. Na versão 3.0.9.101 as chamadas de healthcheck ao CNJ aparecem no log, mas na 3.0.12.1 não encontramos nenhum registro relacionado.

4. O que precisa ser corrigido pela equipe da aplicação

Health check do CNJ (causa da falha): revisar a alteração feita entre as versões 3.0.9.101 e 3.0.12.1 no check de readiness do CNJ. Hoje o endpoint .../usuarios/healthcheck/perfis do APIM sandbox responde 400 em DES. É preciso:
verificar com o CNJ/APIM o motivo do 400 (parâmetros, header ou API key esperada pela chamada); ou
reavaliar se a indisponibilidade de um serviço externo deve tirar o pod de serviço (readiness). Uma alternativa comum é não acoplar o readiness a dependências externas, ou tratá-las de forma degradada.
Configuração de logging: o log da aplicação mostra LogManager error of type GENERIC_FAILURE: Unable to find named filter 'controle-logging' e The delayed handler's queue was overrun and log record(s) were lost. Recomendamos revisar a configuração de log. Na versão 3.0.12.1 os registros da aplicação não chegaram ao console, o que impediu o diagnóstico pelos logs da esteira.
Recomendação adicional: há credenciais definidas em texto puro nas variáveis de ambiente da DeploymentConfig (API keys, client secrets OIDC e token FWC). Sugerimos migrá-las para o cofre (BeyondTrust) ou para secrets.

A mensagem do init container secrets-check (“Script nao serah executado, pois nenhuma das seguintes variaveis de ambiente estah definida: ‘SECRETS_LIST’, ‘MANAGED_ACCOUNTS_LIST’”) é apenas informativa e não tem relação com a falha. Os init containers concluem com sucesso, a conexão com o banco está UP e a mesma configuração funciona na versão 3.0.9.101.

Estado atual: o ambiente DES segue com a versão 3.0.9.101-SNAPSHOT em execução. Após a correção do health check, basta gerar novo build e executar a release normalmente.

Como a causa está no código da aplicação, sem ajuste necessário na esteira, encerramos esta WO. Permanecemos à disposição.

Atenciosamente,
Esteira DevOps NPRD
