Acredito que alguém cliclou em Iterations acidentalmente, nenhum outro step utiliza esse atributo
 
removi ele e passou
 
=============================================

Operation: Execute

Step name: 'Gerar token'

=============================================

REST service details: 

--------------------
 
method: 	POST

URL: 	https://sicsn.caixa path: /BeyondTrust/api/public/v3/auth/connect/token
 
Response: 

--------

HttpResponseInfo [

m_statusCode=400

m_statusMesg=Bad Request

, m_message=

{"error": "invalid_client"}

m_contentType=application/json; charset=UTF-8

, m_headers=Transfer-Encoding:[chunked]; null:[HTTP/1.1 400 Bad Request]; Server:[, ]; X-Content-Type-Options:[nosniff, nosniff]; C\

ross-Origin-Opener-Policy:[same-origin, same-origin]; X-Permitted-Cross-Domain-Policies:[none, none]; Pragma:[no-cache]; Date:[Mon,\

26 Oct 2026 15:33:41 GMT]; Referrer-Policy:[strict-origin-when-cross-origin, strict-origin-when-cross-origin]; X-Frame-Options:[SA\

MEORIGIN, deny]; Strict-Transport-Security:[max-age=31536000; includeSubDomains, max-age=31536000; includeSubDomains]; x-xss-protec\

tion:[0]; Cache-Control:[no-store, no-cache, max-age=0]; Content-Security-Policy:[default-src 'unsafe-inline' 'unsafe-eval' *; fram\

e-src 'self' blob: https data: https; img-src 'self' data: https:; font-src 'self' data:; connect-src 'self' data: https:; worker-s\

rc blob:; child-src blob:, default-src 'unsafe-inline' 'unsafe-eval' *;]; Set-Cookie:[]; Cross-Origin-Resource-Policy:[same-origin,\

same-origin]; Cross-Origin-Embedder-Policy:[require-corp, require-corp]; Content-Type:[application/json; charset=UTF-8]; ]
 
 
Com esse novo client_id não vai
 
Pedro Henrique Paiva de Souza
 
Foi utilizado o cliente de teste?
 
ClientID: 28b5d21f-2288-4f03-89cc-c5999fa85e26

Secret: hOXSgaD1YECHSRVWAlT/Xt1l25N2HwTWYYMb2M/otHI=
 
Ailton Antonio de Araujo, atualiza a senha
hOXSgaD1YECHSRVWAlT%2FXt1l25N2HwTWYYMb2M%2FotHI%3D
 
Fiz a troca dos caracteres especiais
 
Pra ver se continua o mesmo problema
 
Mesmo problema
 
