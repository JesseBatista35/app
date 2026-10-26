Pessoal, bom dia!

Complementando a análise sobre a falha de autenticação do usuário scowdb01 no banco cowdb001, que afeta todos os módulos:

Origem da senha: a senha do datasource vem do vault do JBoss, a partir do arquivo configuration/vault-des/VAULT.dat de cada repositório de config, criptografado com o vault-sicow-des.keystore. A task VAULT_OKD apenas publica esse arquivo no pod, sem usar nenhuma variável da Library.

Correção necessária: regenerar o VAULT.dat com a senha atual do scowdb01 (validada com o DBA) e atualizá-lo em configuration/vault-des/ nos repositórios de config de todos os módulos. Depois, basta executar novamente as releases.

Library SICOW-BT-VAULT-SECRET-DES: o grupo e a variável SCOWDB01 não são utilizados por nenhuma task, e o SICOW não usa BeyondTrust hoje. O grupo também está fora do padrão, que prevê:

SISTEMA-MODULO-BT-VAULT-AMBIENTE, com a variável BT_SECRETS_LIST;
SISTEMA-BT-VAULT-SECRET-AMBIENTE, com as variáveis BT_CLIENT_ID e BT_CLIENT_SECRET.

Recomendamos a remoção da variável SCOWDB01. Caso o SICOW opte por BeyondTrust, a configuração deve seguir o padrão completo, em demanda específica.

Ac Jessé Batista
