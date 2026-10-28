systemctl status sigdb --no-pager; ps -ef | grep -i [A]gtSigdb


Sandro, boa tarde!

São três etapas, com responsáveis diferentes:

1. Senha atual do usuário scowdb01 → DBA. Confirmar com a equipe de banco de dados, responsável pelo PostgreSQL cowdb001 (10.116.92.41:5116), se a senha foi alterada ou, se for o caso, redefini-la.

2. Geração do novo VAULT.dat → Segurança. Com a senha confirmada, abrir REQ para a Segurança gerar um novo VAULT.dat para o SICOW DES com a senha atualizada do scowdb01 (bloco SICOW, atributo SCOWDB01), usando o mesmo keystore vault-sicow-des.keystore.

3. Atualização nos repositórios → time do SICOW. Substituir o arquivo configuration/vault-des/VAULT.dat no repositório de config de todos os módulos (SICOW-*-okd-config) e executar novamente as releases. A task VAULT_OKD publica esse arquivo no pod automaticamente.

Observação: a variável SCOWDB01 do grupo SICOW-BT-VAULT-SECRET-DES não é usada nesse processo. Alterá-la não corrige o problema.

Ac Jessé Batista
 
Sandro Araujo Dantas
Jesse Mouta Pereira Batista, boa tarde!   Eu estive lendo as suas mensagens e vi que um dos grandes problemas está relacionada ao vault   O usuário scowdb01 continua apresentando falha de autenticaçã…
Ambiente DES
 
