
-sh-4.2$
-sh-4.2$
-sh-4.2$ getent hosts login.tqs.caixa || nslookup login.tqs.caixa
10.116.18.235   login.tqs.caixa
-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -skS --max-time 15 https://login.tqs.caixa/auth/realms/intranet/.well-known/openid-configuration | head -c 300; echo
{"issuer":"https://login.tqs.caixa/auth/realms/intranet","authorization_endpoint":"https://login.tqs.caixa/auth/realms/intranet/protocol/openid-connect/auth","token_endpoint":"https://login.tqs.caixa/auth/realms/intranet/protocol/openid-connect/token","token_introspection_endpoint":"https://login.tq
-sh-4.2$ curl -skS --max-time 15 "https://login.tqs.caixa/auth/realms/intranet/protocol/openid-connect/auth?client_id=cli-web-hdg&response_type=code&scope=openid&redirect_uri=https%3A%2F%2Fsihdg-angular18-tqs.apps.nprd.caixa%2F" \
  -w "\nHTTP %{http_code}\n" | grep -iE "invalid|not found|kc-form-login|HTTP [0-9]+"
        <form id="kc-form-login" class="login100-form validate-form" action="https://login.tqs.caixa/auth/realms/intranet/login-actions/authenticate?session_code=gGfCQmNAZsPZ754lPYwwNdLHapltRkwZtBEiBCFqmvA&amp;execution=88bee3b3-455a-44be-883b-d63efce19f5b&amp;client_id=cli-web-hdg&amp;tab_id=zD5lDc-AzIk" method="post" onsubmit="onSubmit()">
HTTP 200
-sh-4.2$
