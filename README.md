Sim, dá pra testar direto por SSH antes de mexer no Control-M, pra confirmar que funciona:

1. Cria o arquivo no servidor:

vi /tmp/teste_cofre.sh

Cola o conteúdo do script, salva e sai (Esc, :wq).

2. Dá permissão de execução:

chmod +x /tmp/teste_cofre.sh

3. Exporta as credenciais como variável de ambiente (nessa mesma sessão, antes de rodar):

export CLIENT_ID="28b5d21f-2288-4f03-89cc-c5999fa85e26"
export CLIENT_SECRET="hOXSgaD1YECHSRVWAlT/Xt1l25N2HwTWYYMb2M/otHI="

4. Roda:

/tmp/teste_cofre.sh

Se aparecer “Credencial obtida com sucesso.” no final, a prova de conceito funcionou e já dá pra levar essa lógica pro Control-M. Se der erro, me manda a saída completa que eu ajudo a ajustar.



#!/bin/bash
set -euo pipefail

BASE_URL="https://sicsn.caixa/BeyondTrust/api/public/v3"
FOLDER="SIIFX_BATCH_DES"
COOKIE_JAR=$(mktemp)
trap 'rm -f "$COOKIE_JAR"' EXIT

# CLIENT_ID e CLIENT_SECRET devem vir do Connection Profile do Control-M,
# injetados como variável de ambiente (não hardcode no script)
if [ -z "${CLIENT_ID:-}" ] || [ -z "${CLIENT_SECRET:-}" ]; then
    echo "ERRO: CLIENT_ID ou CLIENT_SECRET não definidos" >&2
    exit 1
fi

echo "== 1. Gerando token =="
TOKEN_RESPONSE=$(curl -s -k -X POST "$BASE_URL/auth/connect/token" \
    -H "Content-Type: application/x-www-form-urlencoded" \
    --data "grant_type=client_credentials&client_id=${CLIENT_ID}&client_secret=${CLIENT_SECRET}" \
    -c "$COOKIE_JAR")

ACCESS_TOKEN=$(echo "$TOKEN_RESPONSE" | python3 -c "import sys,json; print(json.load(sys.stdin)['access_token'])")

if [ -z "$ACCESS_TOKEN" ]; then
    echo "ERRO: não foi possível obter o access_token" >&2
    echo "$TOKEN_RESPONSE" >&2
    exit 1
fi

echo "== 2. Login no Beyond Trust (SignAppin) =="
curl -s -k -X POST "$BASE_URL/Auth/SignAppin" \
    -H "Authorization: Bearer ${ACCESS_TOKEN}" \
    -b "$COOKIE_JAR" -c "$COOKIE_JAR" > /dev/null

echo "== 3. Obtendo credencial =="
SECRET_RESPONSE=$(curl -s -k -X GET "$BASE_URL/Secrets-Safe/Secrets?Path=${FOLDER}" \
    -H "Authorization: Bearer ${ACCESS_TOKEN}" \
    -b "$COOKIE_JAR" -c "$COOKIE_JAR")

PASSWORD=$(echo "$SECRET_RESPONSE" | python3 -c "
import sys, json
data = json.load(sys.stdin)
item = data[0] if isinstance(data, list) else data
print(item.get('Password',''))
")

echo "== 4. Logout =="
curl -s -k -X POST "$BASE_URL/Auth/Signout" -b "$COOKIE_JAR" > /dev/null

if [ -z "$PASSWORD" ]; then
    echo "ERRO: não foi possível extrair a credencial" >&2
    exit 1
fi

echo "Credencial obtida com sucesso."
export VARIAVEL_DO_SISTEMA="$(echo "$PASSWORD" | base64 | tr -d '\n')"
