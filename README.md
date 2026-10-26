cat > /tmp/teste_cofre.sh << 'EOF'
#!/bin/bash
set -euo pipefail

BASE_URL="https://sicsn.caixa/BeyondTrust/api/public/v3"
FOLDER="SIIFX_BATCH_DES"
SECRET_TITLE="SIIFX_BT_APIKEY"
COOKIE_JAR=$(mktemp)
trap 'rm -f "$COOKIE_JAR"' EXIT

if [ -z "${CLIENT_ID:-}" ] || [ -z "${CLIENT_SECRET:-}" ]; then
    echo "ERRO: CLIENT_ID ou CLIENT_SECRET nao definidos" >&2
    exit 1
fi

TOKEN_RESPONSE=$(curl -s -k -X POST "$BASE_URL/auth/connect/token" \
    -H "Content-Type: application/x-www-form-urlencoded" \
    --data "grant_type=client_credentials&client_id=${CLIENT_ID}&client_secret=${CLIENT_SECRET}" \
    -c "$COOKIE_JAR")

ACCESS_TOKEN=$(echo "$TOKEN_RESPONSE" | python3 -c "import sys,json; print(json.load(sys.stdin)['access_token'])")
if [ -z "$ACCESS_TOKEN" ]; then
    echo "ERRO: falha ao gerar token" >&2
    exit 1
fi

curl -s -k -X POST "$BASE_URL/Auth/SignAppin" \
    -H "Authorization: Bearer ${ACCESS_TOKEN}" -d "" \
    -b "$COOKIE_JAR" -c "$COOKIE_JAR" > /dev/null

SECRET_RESPONSE=$(curl -s -k -X GET "$BASE_URL/Secrets-Safe/Secrets?Path=${FOLDER}" \
    -H "Authorization: Bearer ${ACCESS_TOKEN}" \
    -b "$COOKIE_JAR" -c "$COOKIE_JAR")

PASSWORD=$(echo "$SECRET_RESPONSE" | python3 -c "
import sys, json
data = json.load(sys.stdin)
for item in data:
    if item.get('Title') == '$SECRET_TITLE':
        print(item.get('Password',''))
        break
")

curl -s -k -X POST "$BASE_URL/Auth/Signout" -d "" -b "$COOKIE_JAR" > /dev/null

if [ -z "$PASSWORD" ]; then
    echo "ERRO: credencial '$SECRET_TITLE' nao encontrada" >&2
    exit 1
fi

export VARIAVEL_DO_SISTEMA="$(echo "$PASSWORD" | base64 | tr -d '\n')"
echo "Credencial obtida com sucesso."
EOF
chmod +x /tmp/teste_cofre.sh
/tmp/teste_cofre.sh
