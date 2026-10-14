-sh-4.2$ BT=https://sicsn.caixa/BeyondTrust/api/public/v3
-sh-4.2$ S=bt-client-secret-siifx-api-aplicacao-des
-sh-4.2$ CID=$(oc get secret $S -n siifx-des -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d)
-sh-4.2$ CSEC=$(oc get secret $S -n siifx-des -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d)
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ BT=https://sicsn.caixa/BeyondTrust/api/public/v3
-sh-4.2$ S=bt-client-secret-siifx-api-aplicacao-des
-sh-4.2$ CID=$(oc get secret $S -n siifx-des -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d)
-sh-4.2$ CSEC=$(oc get secret $S -n siifx-des -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d)
-sh-4.2$
-sh-4.2$
-sh-4.2$ TOKEN=$(curl -sk -m 30 -X POST "$BT/Auth/connect/token" \
>   -d "grant_type=client_credentials&client_id=$CID&client_secret=$CSEC" \
>   | sed -E 's/.*"access_token":"([^"]+)".*/\1/'); echo "token: ${TOKEN:0:15}..."
token: eyJhbGciOiJSUzI...
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -sk -m 30 -c /tmp/bt -X POST "$BT/Auth/SignAppIn" -H "Authorization: Bearer $TOKEN"; echo
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN""http://www.w3.org/TR/html4/strict.dtd">
<HTML><HEAD><TITLE>Length Required</TITLE>
<META HTTP-EQUIV="Content-Type" Content="text/html; charset=us-ascii"></HEAD>
<BODY><h2>Length Required</h2>
<hr><p>HTTP Error 411. The request must be chunked or have a content length.</p>
</BODY></HTML>

-sh-4.2$ for t in apikey_siifx_intranet sifxds01_oracle cli-ser-ifx_sso_intra siifx_api SIFXDS04_DATAGRID; do
>   echo "== $t"
>   curl -sk -m 60 -b /tmp/bt -H "Authorization: Bearer $TOKEN" \
>     -o /dev/null -w "HTTP %{http_code} em %{time_total}s\n" \
>     "$BT/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/&title=$t"
> done
== apikey_siifx_intranet
HTTP 401 em 0,158s
== sifxds01_oracle
HTTP 401 em 0,116s
== cli-ser-ifx_sso_intra
HTTP 401 em 0,110s
== siifx_api
HTTP 401 em 0,110s
== SIFXDS04_DATAGRID
HTTP 401 em 0,109s
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -sk -m 60 -b /tmp/bt -H "Authorization: Bearer $TOKEN" \
>   -w "\nHTTP %{http_code} em %{time_total}s\n" \
>   "$BT/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/"
"User not authenticated"
HTTP 401 em 0,166s
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -sk -b /tmp/bt -X POST "$BT/Auth/Signout" -H "Authorization: Bearer $TOKEN"; rm -f /tmp/bt; unset CID CSEC TOKEN
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN""http://www.w3.org/TR/html4/strict.dtd">
<HTML><HEAD><TITLE>Length Required</TITLE>
<META HTTP-EQUIV="Content-Type" Content="text/html; charset=us-ascii"></HEAD>
<BODY><h2>Length Required</h2>
<hr><p>HTTP Error 411. The request must be chunked or have a content length.</p>
</BODY></HTML>
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ ^C
-sh-4.2$ TTP-EQUIV="Content-Type" Content="text/html; charset=us-ascii"></HEAD>
-sh: erro de sintaxe próximo do `token' não esperado `<'
-sh-4.2$ <BODY><h2>Length Required</h2>
-sh: erro de sintaxe próximo do `token' não esperado `<'
-sh-4.2$ <hr><p>HTTP Error 411. The request must be chunked or have a content length.</p>
-sh: erro de sintaxe próximo do `token' não esperado `<'
-sh-4.2$ </BODY></HTML>
-sh: erro de sintaxe próximo do `token' não esperado `<'
-sh-4.2$
-sh-4.2$ -sh-4.2$ for t in apikey_siifx_intranet sifxds01_oracle cli-ser-ifx_sso_intra siifx_api SIFXDS04_DATAGRID; do
-sh: erro de sintaxe próximo do `token' não esperado `do'
-sh-4.2$ >   echo "== $t"
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -sk -m 60 -b /tmp/bt -H "Authorization: Bearer $TOKEN" \
>   -w "\nHTTP %{http_code} em %{time_total}s\n" \
>   "$BT/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/"
"User not authenticated"
HTTP 401 em 0,166s
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -sk -b /tmp/bt -X POST "$BT/Auth/Signout" -H "Authorization: Bearer $TOKEN"; rm -f /tmp/bt; unset CID CSEC TOKEN
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN""http://www.w3.org/TR/html4/strict.dtd">
<HTML><HEAD><TITLE>Length Required</TITLE>
<META HTTP-EQUIV="Content-Type" Content="text/html; charset=us-ascii"></HEAD>
<BODY><h2>Length Required</h2>
<hr><p>HTTP Error 411. The request must be chunked or have a content length.</p>
</BODY></HTML>
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh: == SIFXDS04_DATAGRID: comando não encontrado
-sh-4.2$ >   curl -sk -m 60 -b /tmp/bt -H "Authorization: Bearer $TOKEN" \
> >     -o /dev/null -w "HTTP %{http_code} em %{time_total}s\n" \
> >     "$BT/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/&title=$t"
-sh: https://sicsn.caixa/BeyondTrust/api/public/v3/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/&title=SIFXDS04_DATAGRID: Arquivo ou diretório não encontrado
-sh-4.2$ > done
-sh-4.2$ == apikey_siifx_intranet
-sh: ==: comando não encontrado
-sh-4.2$ HTTP 401 em 0,158s
-sh: HTTP: comando não encontrado
-sh-4.2$ == sifxds01_oracle
-sh: ==: comando não encontrado
-sh-4.2$ HTTP 401 em 0,116s
-sh: HTTP: comando não encontrado
-sh-4.2$ == cli-ser-ifx_sso_intra
-sh: ==: comando não encontrado
-sh-4.2$ HTTP 401 em 0,110s
-sh: HTTP: comando não encontrado
-sh-4.2$ == siifx_api
-sh: ==: comando não encontrado
-sh-4.2$ HTTP 401 em 0,110s
-sh: HTTP: comando não encontrado
-sh-4.2$ == SIFXDS04_DATAGRID
-sh: ==: comando não encontrado
-sh-4.2$ HTTP 401 em 0,109s
-sh: HTTP: comando não encontrado
-sh-4.2$ -sh-4.2$
-sh: -sh-4.2$: comando não encontrado
-sh-4.2$ -sh-4.2$
-sh: -sh-4.2$: comando não encontrado
-sh-4.2$ -sh-4.2$
-sh: -sh-4.2$: comando não encontrado
-sh-4.2$ -sh-4.2$
-sh: -sh-4.2$: comando não encontrado
-sh-4.2$ -sh-4.2$ curl -sk -m 60 -b /tmp/bt -H "Authorization: Bearer $TOKEN" \
> >   -w "\nHTTP %{http_code} em %{time_total}s\n" \
> >   "$BT/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/"
-sh: https://sicsn.caixa/BeyondTrust/api/public/v3/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/: Arquivo ou diretório não encontrado
-sh-4.2$ "User not authenticated"
-sh: User not authenticated: comando não encontrado
-sh-4.2$ HTTP 401 em 0,166s
-sh: HTTP: comando não encontrado
-sh-4.2$ -sh-4.2$
-sh: -sh-4.2$: comando não encontrado
-sh-4.2$ -sh-4.2$
-sh: -sh-4.2$: comando não encontrado
-sh-4.2$ -sh-4.2$
-sh: -sh-4.2$: comando não encontrado
-sh-4.2$ -sh-4.2$ curl -sk -b /tmp/bt -X POST "$BT/Auth/Signout" -H "Authorization: Bearer $TOKEN"; rm -f /tmp/bt; unset CID CSEC TOKEN
-sh: -sh-4.2$: comando não encontrado
-sh-4.2$ <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN""http://www.w3.org/TR/html4/strict.dtd">
-sh: !DOCTYPE: event not found
-sh-4.2$ <HTML><HEAD><TITLE>Length Required</TITLE>
-sh: erro de sintaxe próximo do `token' não esperado `<'
-sh-4.2$ <META HTTP-EQUIV="Content-Type" Content="text/html; charset=us-ascii"></HEAD>
-sh: erro de sintaxe próximo do `token' não esperado `<'
-sh-4.2$ <BODY><h2>Length Required</h2>
-sh: erro de sintaxe próximo do `token' não esperado `<'
-sh-4.2$ <hr><p>HTTP Error 411. The request must be chunked or have a content length.</p>
-sh: erro de sintaxe próximo do `token' não esperado `<'
-sh-4.2$ </BODY></HTML>
-sh: erro de sintaxe próximo do `token' não esperado `<'
-sh-4.2$ -sh-4.2$
-sh: -sh-4.2$: comando não encontrado
-sh-4.2$ -sh-4.2$
-sh: -sh-4.2$: comando não encontrado
-sh-4.2$ -sh-4.2$
-sh: -sh-4.2$: comando não encontrado
-sh-4.2$ -sh-4.2$
-sh: -sh-4.2$: comando não encontrado
-sh-4.2$ curl -sk -b /tmp/bt -X POST "$BT/Auth/Signout" -H "Authorization: Bearer $TOKEN"; rm -f /tmp/bt; unset CID CSEC TOKEN
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN""http://www.w3.org/TR/html4/strict.dtd">
<HTML><HEAD><TITLE>Length Required</TITLE>
<META HTTP-EQUIV="Content-Type" Content="text/html; charset=us-ascii"></HEAD>
<BODY><h2>Length Required</h2>
<hr><p>HTTP Error 411. The request must be chunked or have a content length.</p>
</BODY></HTML>
-sh-4.2$
