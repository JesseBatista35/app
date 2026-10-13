A release SINFS-okd4 em TQS (namespace sinfs-tqs) falha no init do BeyondTrust. O client entregue na WO0000081007679 (BT_CLIENT_ID 4c3c08e8-336e-4fa1-9919-e5f9f730f865) autentica normalmente no sicsn.caixa, mas como o usuário SNFSTR02, e as consultas abaixo retornam “Secret was not found”:

SINFS_TQS/JCICSDIRECT
SINFS_TQS/SSO_SENHA
SINFS_TQS/TGNFSNFDV_SENHA

Em DES, o client equivalente (WO0000080991099) autentica como clientid_SNFSDR01 e lê os segredos SINFS_DES/* normalmente.

Solicito verificar se os segredos estão cadastrados na pasta SINFS_TQS e conceder acesso de leitura a esse client, ou fornecer o client correto para TQS no mesmo padrão do DES (clientid_SNFSTR01). Se possível, cadastrar também SINFS_TQS/TGSGRS142_SENHA, TGSGRS143_SENHA e TGSGRS144_SENHA, para igualar ao DES.
