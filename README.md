POST https://sicsn.caixa/BeyondTrust/api/public/v3/auth/connect/token → gera o token OAuth
POST https://sicsn.caixa/BeyondTrust/api/public/v3/Auth/SignAppin → login (retorna 200, usuário SIFXDB01 confirmado)
GET https://sicsn.caixa/BeyondTrust/api/public/v3/Secrets-Safe/Secrets?FolderPath=SIIFX_BATCH_DES → aqui que dá 401
