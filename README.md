O que fazer aqui

Library SIAVO-MS-CORE-BT-VAULT-DES (sistema + módulo), contendo:
BT_SECRETS_LIST
Library SIAVO-BT-VAULT-SECRET-DES (por sistema, sem o módulo), contendo:
BT_CLIENT_ID
BT_CLIENT_SECRET
Antes de criar, procure na Library por “SIAVO-BT-VAULT-SECRET”. Como ela é por sistema, pode já existir se outro módulo do SIAVO usa BeyondTrust. Se existir, é só vincular.
Vincular as duas na release SIAVO-ms-core com escopo EC DES.
Incluir a task do BeyondTrust logo após o Cria_APP_OKD no stage DES.
