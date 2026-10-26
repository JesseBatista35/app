entrei em uma sala agora pouco que esta com pedro, ele cnfimou ´pe esse emso que ta la ele acabou de criar um novo para testes para poder descartar

a a hipotes do problema ser no beyoundtrus

28b5d21f-2288-4f03-89cc-c5999fa85e26
 
hOXSgaD1YECHSRVWAlT/Xt1l25N2HwTWYYMb2M/otHI=


 o robsno madou isso mais nao sei pra que pe com entrei na sala gora estou perdido


Environment information:
+-------------------------+--------------------------------------------------+
|Connection Profile Name  |IIFX                                              |
+-------------------------+--------------------------------------------------+
|Connection Profile Scope |Centralized                                       |
+-------------------------+--------------------------------------------------+


=============================================
Operation: Execute
Step name: 'Proxy'
=============================================

Command line: 
-------------
export no_proxy="$no_proxy,sicsn.caixa,sicsn.gerencia.caixa"
echo $no_proxy



Exit code is: 0
Parameter 'Iterations Range Attribute' is empty or too big (greater than 9999)
=============================================
Operation: Execute
Step name: 'Gerar token'
=============================================
Skipping step due to 0 iterations.

=============================================
Operation: Execute
Step name: 'Login no Beyond Trust'
=============================================
REST service details: 
--------------------

method: 	POST
URL: 	https://sicsn.caixa path: /BeyondTrust/api/public/v3/Auth/SignAppin

Response: 
--------
HttpResponseInfo [
m_statusCode=401
m_statusMesg=Unauthorized
, m_message=
"Failed to authenticate due to one or more authentication rules."
 m_contentType=application/json
, m_headers=null:[HTTP/1.1 401 Unauthorized]; Server:[]; X-Content-Type-Options:[nosniff]; Cross-Origin-Opener-Policy:[same-origin]\
; X-Permitted-Cross-Domain-Policies:[none]; Pragma:[no-cache]; Date:[Mon, 26 Oct 2026 14:57:51 GMT]; Referrer-Policy:[strict-origin\
-when-cross-origin]; X-Frame-Options:[SAMEORIGIN]; Strict-Transport-Security:[max-age=31536000; includeSubDomains]; x-xss-protectio\
n:[0]; Cache-Control:[no-cache]; Content-Security-Policy:[default-src 'unsafe-inline' 'unsafe-eval' *; frame-src 'self' blob: https\
 data: https; img-src 'self' data: https:; font-src 'self' data:; connect-src 'self' data: https:; worker-src blob:; child-src blob\
:]; Set-Cookie:[]; Cross-Origin-Resource-Policy:[same-origin]; Cross-Origin-Embedder-Policy:[require-corp]; Expires:[-1]; Content-L\
ength:[65]; Content-Type:[application/json]; ]


=============================================
Operation: Execute
Step name: 'Obter credencial'
=============================================
REST service details: 
--------------------

method: 	GET
URL: 	https://sicsn.caixa path: /BeyondTrust/api/public/v3/Secrets-Safe/Secrets?Folder=SIIFX_BATCH_DES

Response: 
--------
HttpResponseInfo [
m_statusCode=401
m_statusMesg=Unauthorized
, m_message=
"User not authenticated"
 m_contentType=application/json
, m_headers=null:[HTTP/1.1 401 Unauthorized]; Server:[]; X-Content-Type-Options:[nosniff]; Cross-Origin-Opener-Policy:[same-origin]\
; X-Permitted-Cross-Domain-Policies:[none]; Pragma:[no-cache]; Date:[Mon, 26 Oct 2026 14:57:51 GMT]; Referrer-Policy:[strict-origin\
-when-cross-origin]; X-Frame-Options:[SAMEORIGIN]; Strict-Transport-Security:[max-age=31536000; includeSubDomains]; x-xss-protectio\
n:[0]; Cache-Control:[no-cache]; Content-Security-Policy:[default-src 'unsafe-inline' 'unsafe-eval' *; frame-src 'self' blob: https\
 data: https; img-src 'self' data: https:; font-src 'self' data:; connect-src 'self' data: https:; worker-src blob:; child-src blob\
:]; Set-Cookie:[]; Cross-Origin-Resource-Policy:[same-origin]; Cross-Origin-Embedder-Policy:[require-corp]; Expires:[-1]; Content-L\
ength:[24]; Content-Type:[application/json]; ]


=============================================
Operation: Execute
Step name: 'Logout no Beyond Trust'
=============================================
REST service details: 
--------------------

method: 	POST
URL: 	https://sicsn.caixa path: /BeyondTrust/api/public/v3/Auth/Signout

Response: 
--------
HttpResponseInfo [
m_statusCode=200
m_statusMesg=OK
, m_message=

 m_contentType=
, m_headers=null:[HTTP/1.1 200 OK]; Server:[]; X-Content-Type-Options:[nosniff]; Cross-Origin-Opener-Policy:[same-origin]; X-Permit\
ted-Cross-Domain-Policies:[none]; Pragma:[no-cache]; Date:[Mon, 26 Oct 2026 14:57:51 GMT]; Referrer-Policy:[strict-origin-when-cros\
s-origin]; X-Frame-Options:[SAMEORIGIN]; Strict-Transport-Security:[max-age=31536000; includeSubDomains]; x-xss-protection:[0]; Cac\
he-Control:[no-cache]; Content-Security-Policy:[default-src 'unsafe-inline' 'unsafe-eval' *; frame-src 'self' blob: https data: htt\
ps; img-src 'self' data: https:; font-src 'self' data:; connect-src 'self' data: https:; worker-src blob:; child-src blob:]; Cross-\
Origin-Resource-Policy:[same-origin]; Cross-Origin-Embedder-Policy:[require-corp]; Expires:[-1]; Content-Length:[0]; ]


=============================================
Operation: Execute
Step name: 'Executar job'
=============================================

Command line: 
-------------
#!/bin/bash -x

# Gera um id aleatorio para compor o filename no output do script
export ID=$(mktemp -u XXXXX)
#export ARQ_OUTPUT=/tmp/IIFX_${ID}.txt

export VARIAVEL_DO_SISTEMA="$(echo '' | base64 | tr -d '\n')"

/tmp/teste.sh

Output:
-------




Exit code is: 0


Job failure message:
-------------------
Application Integrator plugin: UCM0001 = Application Integrator plugin: UCM0001 = REST request failed. status code: 401 response is\
: Unauthorized message: "Failed to authenticate due to one or more authentication rules."



Job statistics:
+-------------------------+-------------------------+
|Start Time               |20261026115743           |
+-------------------------+-------------------------+
|End Time                 |20261026115745           |
+-------------------------+-------------------------+
|Elapsed Time             |195                      |
+-------------------------+-------------------------+
Exit Code    = 1
Exit Message = Application Integrator plugin: UCM0001 = Application Integrator plugin: UCM0001 = REST request failed. status code: \
401 response is: Unauthorized message:  Failed to authenticate due to one or more authentication rules. 


