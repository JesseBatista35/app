tendimento referente à falha de deploy da aplicação SIPGC-api-seguranca no ambiente TQS, com pod preso em Init:CrashLoopBackOff e, anteriormente, falha de criação do DeploymentConfig.

Causa raiz 1 — DeploymentConfig inválido (mountPath duplicado):
Identificado erro spec.template.spec.containers[0].volumeMounts[1].mountPath: Invalid value: must be unique na task de criação de volumes. Causa: coexistência de duas variáveis de senha de banco no grupo de variáveis SIPGC-API-SEGURANCA-TQS — a variável legada _SECRET.DB_PASSWORD_001 (padrão antigo de token) e a variável atual _SECRET.DB_PASSWORD_0010 (padrão vigente, igual ao ambiente DES). Cada variável com prefixo _SECRET. gera um volume/mount automático, e a duplicidade de senha de banco gerava conflito de path.

Ação 1: Removida a variável legada _SECRET.DB_PASSWORD_001 da library SIPGC-API-SEGURANCA-TQS, mantendo apenas _SECRET.DB_PASSWORD_0010. Resolveu o erro de criação do DeploymentConfig.

Causa raiz 2 — Falha de autenticação no BeyondTrust:
Após a correção do mount, o pod passou a ser criado, porém ficava preso em Init:CrashLoopBackOff devido à falha do init container secrets-agent-sidecar em autenticar no BeyondTrust (Failed to authenticate due to one or more authentication rules), impedindo o download dos secrets. Identificado que a regra de autenticação do client BeyondTrust (97f8f98c-9ce6-4a2f-bdf0-be70af3218ee, app TQS) não reconhecia o IP de origem real das chamadas partindo do cluster (10.116.222.238).

Ação 2: Escalado para o time de Segurança (BeyondTrust/vault). Lucas Vinicius de Almeida Santos ajustou a regra de IP de origem no cofre, liberando o IP correto.

Resultado: Novo deploy disparado em TQS, pod íntegro/saudável, aplicação funcionando normalmente.

Atendimento encerrado com sucesso.
