Ação: [INVESTIGAR JOB] Solicita-se análise de falha na execução do JOB CX_101-abertura-movimento-aporte no ambiente DES, devido a erro de autenticação na integração com o Application Integration. A execução no servidor informado está retornando HTTP 401 (Unauthorized), indicando que o usuário/credencial utilizada pela integração não está sendo autenticada.


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
 26 Oct 2026 23:00:08 GMT]; Referrer-Policy:[strict-origin-when-cross-origin, strict-origin-when-cross-origin]; X-Frame-Options:[SA\
MEORIGIN, deny]; Strict-Transport-Security:[max-age=31536000; includeSubDomains, max-age=31536000; includeSubDomains]; x-xss-protec\
tion:[0]; Cache-Control:[no-store, no-cache, max-age=0]; Content-Security-Policy:[default-src 'unsafe-inline' 'unsafe-eval' *; fram\
e-src 'self' blob: https data: https; img-src 'self' data: https:; font-src 'self' data:; connect-src 'self' data: https:; worker-s\
rc blob:; child-src blob:, default-src 'unsafe-inline' 'unsafe-eval' *;]; Set-Cookie:[]; Cross-Origin-Resource-Policy:[same-origin,\
 same-origin]; Cross-Origin-Embedder-Policy:[require-corp, require-corp]; Content-Type:[application/json; charset=UTF-8]; ]


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
; X-Permitted-Cross-Domain-Policies:[none]; Pragma:[no-cache]; Date:[Mon, 26 Oct 2026 23:00:08 GMT]; Referrer-Policy:[strict-origin\
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
; X-Permitted-Cross-Domain-Policies:[none]; Pragma:[no-cache]; Date:[Mon, 26 Oct 2026 23:00:08 GMT]; Referrer-Policy:[strict-origin\
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
ted-Cross-Domain-Policies:[none]; Pragma:[no-cache]; Date:[Mon, 26 Oct 2026 23:00:08 GMT]; Referrer-Policy:[strict-origin-when-cros\
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

/producao/executa-job.sh

Output:
-------

/producao/executa-job.sh: linha 1: ï»¿#!/usr/bin/bash: Arquivo ou diretÃ³rio inexistente
/producao/env_config.sh: linha 47: export: `=': nÃ£o Ã© um identificador vÃ¡lido
Variaveis nao adquiridas: DB_PASS SIIFX_DATAGRID_PASS



Exit code is: 16


Job failure message:
-------------------
Application Integrator plugin: UCM0001 = Application Integrator plugin: UCM0001 = REST request failed. status code: 400 response is\
: Bad Request message: {"error": "invalid_client"}



Job statistics:
+-------------------------+-------------------------+
|Start Time               |20261026200000           |
+-------------------------+-------------------------+
|End Time                 |20261026200002           |
+-------------------------+-------------------------+
|Elapsed Time             |233                      |
+-------------------------+-------------------------+
Exit Code    = 1
Exit Message = Application Integrator plugin: UCM0001 = Application Integrator plugin: UCM0001 = REST request failed. status code: \
400 response is: Bad Request message: { error :  invalid_client }




nao entendi esse chamado do Ailton para o robson.

sendo que ele ficou de mudar no control-M

