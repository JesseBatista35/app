**# 1) O servidor e o realm "intranet" existem? (deve retornar JSON com "issuer")
curl -sk https://login.tqs.caixa/auth/realms/intranet/.well-known/openid-configuration | head -c 300; echo

# 2) O client cli-web-hdg aceita a redirect_uri do front TQS?
curl -sk -o /dev/null -w "%{http_code}\n" \
 "https://login.tqs.caixa/auth/realms/intranet/protocol/openid-connect/auth?client_id=cli-web-hdg&response_type=code&scope=openid&redirect_uri=https%3A%2F%2Fsihdg-angular18-tqs.apps.nprd.caixa%2F"
**
