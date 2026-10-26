cat > /tmp/teste_cofre.sh << 'EOF'
#!/bin/bash
set -euo pipefail

BASE_URL="https://sicsn.caixa/BeyondTrust/api/public/v3"
FOLDER="SIIFX_BATCH_DES"
COOKIE_JAR=$(mktemp)
trap 'rm -f "$COOKIE_JAR"' EXIT

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

echo "DEBUG - cookie jar apos passo 1:"
cat "$COOKIE_JAR"

echo "== 2. Login no Beyond Trust (SignAppin) =="
LOGIN_RESPONSE=$(curl -s -k -X POST "$BASE_URL/Auth/SignAppin" \
    -H "Authorization: Bearer ${ACCESS_TOKEN}" \
    -b "$COOKIE_JAR" -c "$COOKIE_JAR")

echo "DEBUG - resposta do login:"
echo "$LOGIN_RESPONSE"
echo "DEBUG - cookie jar apos passo 2:"
cat "$COOKIE_JAR"

echo "== 3. Obtendo credencial =="
SECRET_RESPONSE=$(curl -s -k -X GET "$BASE_URL/Secrets-Safe/Secrets?Path=${FOLDER}" \
    -H "Authorization: Bearer ${ACCESS_TOKEN}" \
    -b "$COOKIE_JAR" -c "$COOKIE_JAR")

echo "DEBUG - resposta crua:"
echo "$SECRET_RESPONSE"

echo "== 4. Logout =="
curl -s -k -X POST "$BASE_URL/Auth/Signout" -b "$COOKIE_JAR" > /dev/null
EOF
chmod +x /tmp/teste_cofre.sh
/tmp/teste_cofre.sh
