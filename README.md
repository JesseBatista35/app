# resolve o nome?
getent hosts login.tqs.caixa || nslookup login.tqs.caixa

# teste 1 mostrando erros
curl -skS --max-time 15 https://login.tqs.caixa/auth/realms/intranet/.well-known/openid-configuration | head -c 300; echo

# teste 2 mostrando o código HTTP e a mensagem de erro (se houver)
curl -skS --max-time 15 "https://login.tqs.caixa/auth/realms/intranet/protocol/openid-connect/auth?client_id=cli-web-hdg&response_type=code&scope=openid&redirect_uri=https%3A%2F%2Fsihdg-angular18-tqs.apps.nprd.caixa%2F" \
  -w "\nHTTP %{http_code}\n" | grep -iE "invalid|not found|kc-form-login|HTTP [0-9]+"
