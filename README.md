À CEPRO20 – Gestão de Identidade e Acesso

Prezados,

Encaminhamos esta demanda para orientação e atuação de vocês, como continuidade da WO0000081808304, na qual a CEPRO20 orientou a abertura de Solicitação FICUS.

Contexto:
Desde 05/10/2026, todas as releases que usam a esteira-jboss-vm (aplicações em VM, DES e TQS) falham no passo "Configurando Stack de Monitoração", com o erro:
FATAL: password authentication failed for user "monitdbadm"

A falha afeta qualquer sistema. Confirmamos em SIRTA e SIGPD-backend, e as demandas da PI3 já estão represadas por esse motivo.

Dados do acesso:

HOST: 10.244.74.86 (PostgreSQL no Azure)
PORTA: 5432
DATABASE: monitordb001 (esquema mon)
USUÁRIO: monitdbadm

Validações já realizadas:

A conectividade dos agentes ao banco na porta 5432 está liberada (confirmada pelo DBA na WO0000081808304).
A conexão com SSL é aceita pelo pg_hba.conf e rejeitada apenas na senha.
A senha configurada na esteira não muda desde 2024. A credencial foi alterada ou expirou do lado do banco.

Por que não abrimos a FICUS:
O monitdbadm é uma conta de serviço usada pela automação da esteira, e não um usuário pessoal. O formulário de Solicitação FICUS disponível é de cadastramento ou remoção de acesso para uma pessoa ("Solicitado Para", gestor imediato e perfil a ser concedido), e não atende à verificação ou redefinição de senha de conta de serviço.

Solicitação:

Verificar a situação do usuário monitdbadm no monitordb001 (senha alterada, expirada ou bloqueada / VALID UNTIL).
Redefinir ou informar a credencial vigente, por canal seguro, para atualização na esteira.
Caso não seja escopo da CEPRO20, informar qual oferta ou equipe trata credenciais de conta de serviço, para encaminharmos corretamente.

Atenciosamente,
Jessé Batista – CTIS/CESTI Esteira DevOps DES/TQS NPRD

