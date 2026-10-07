À CEPRO20 – Gestão de Identidade e Acesso

Prezados,

Encaminhamos esta demanda como continuidade das WO0000081808304 e WO0000081824515, que tratam do mesmo problema e foram encerradas sem a regularização da causa.

Contexto:
Desde 05/10/2026, as releases que usam a esteira-jboss-vm (aplicações em VM, DES e TQS) falham no passo "Configurando Stack de Monitoração", com o erro:
FATAL: password authentication failed for user "monitdbadm"

O problema segue ativo hoje (07/10) e afeta vários sistemas. Por exemplo: SIRTA (esta demanda, releaseId 537141), SIPQV (10h02) e SIGPD-backend (14h23).

Dados do acesso:

HOST: 10.244.74.86 (PostgreSQL no Azure)
PORTA: 5432
DATABASE: monitordb001 (esquema mon)
USUÁRIO: monitdbadm

Validações já realizadas:

A conectividade dos agentes ao banco na porta 5432 está liberada (confirmada pelo DBA).
A conexão com SSL é aceita pelo pg_hba.conf e rejeitada apenas na senha.
A senha configurada na esteira não muda desde 2024. A credencial foi alterada ou expirou do lado do banco.

Sobre a FICUS:
O monitdbadm é uma conta de serviço usada pela automação da esteira, e não um usuário pessoal. O formulário de Solicitação FICUS é de cadastramento ou remoção de acesso para uma pessoa (com gestor imediato e perfil) e não atende à verificação ou redefinição de senha de conta de serviço.

Solicitação:

Verificar a situação do usuário monitdbadm (senha alterada, expirada ou bloqueada / VALID UNTIL).
Redefinir ou informar a credencial vigente, por canal seguro, para atualização na esteira.
Caso não seja escopo da CEPRO20, indicar a equipe ou oferta responsável por credenciais de conta de serviço.

Atenciosamente,
Jessé Batista – CTIS/CESTI Esteira DevOps DES/TQS NPRD
