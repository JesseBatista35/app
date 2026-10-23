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
m_statusCode=200
m_statusMesg=OK
, m_message=
{
    "access_token": "eyJhbGciOiJSUzI1NiIsImtpZCI6IjkwMTk3RTZCLThEMDEtNDg0Ny1CQThELTNCRDdDRDg4QUUxQSIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJod\
HRwczovL3NpY3NuLmNhaXhhL3BzYXV0aCIsIm5iZiI6MTc5Mjc4MDYzOSwiaWF0IjoxNzkyNzgwNjM5LCJleHAiOjE3OTI3ODQyMzksImF1ZCI6WyJwdWJsaWNhcGkiLCJt\
b2JpbGVhcHAiLCJodHRwczovL3NpY3NuLmNhaXhhL3BzYXV0aC9yZXNvdXJjZXMiXSwic2NvcGUiOlsicHVibGljYXBpIl0sImNsaWVudF9pZCI6IjA5OGM0ZjQ5LWVmYTU\
tNDA0Mi1iMTlmLThhOGI1YWZjNzlkMiIsIl9jbGllbnRBY2Nlc3NQb2xpY3lJZCI6IjMzMiIsIl9jbGllbnRVc2VySWQiOiIxOTAyIiwianRpIjoiMzc3Mzg1Nzc3ODczRD\
RBRkU5MDg5QjYwNzBFNDUwN0IifQ.DiiIfddnnfwlqEAlxS367sAk5cU-Kmg73aGaRJwcN39o37zA-7A_EtPdQGBAKc51I7EPy7ey7v9dpTQddQfeUbiTq8NDzHQHyNqjNr\
SDPrk8BvgNbtxSQsMuBwwvwjBA-IpyADwrxB-D7KDV3IaNMjgio2o3fQnOFVUP_hhNddy7v4xKJc0sAKE-QfY4kPkp2N_Itiz55xlG-kxj5MlUyQM8T1yvNXw9GG5pRrfYh\
uiv-lnzR4rVykSIZf4T55yUYgzTncN6GLkhFJaIZSKmjhYnOJ09zPGOAFH1uq3quJRQk-JgcKBRWaU27FTmwBYWMXqqy1HN5zWqmfoNmeVZIQ",
    "scope": "publicapi",
    "token_type": "Bearer",
    "expires_in": 3600
}
m_contentType=application/json; charset=UTF-8
, m_headers=Transfer-Encoding:[chunked]; null:[HTTP/1.1 200 OK]; Server:[, ]; X-Content-Type-Options:[nosniff, nosniff]; Cross-Orig\
in-Opener-Policy:[same-origin, same-origin]; X-Permitted-Cross-Domain-Policies:[none, none]; Pragma:[no-cache]; Date:[Fri, 23 Oct 2\
026 18:37:19 GMT]; Referrer-Policy:[strict-origin-when-cross-origin, strict-origin-when-cross-origin]; X-Frame-Options:[SAMEORIGIN,\
deny]; Strict-Transport-Security:[max-age=31536000; includeSubDomains, max-age=31536000; includeSubDomains]; x-xss-protection:[0];\
Cache-Control:[no-store, no-cache, max-age=0]; Content-Security-Policy:[default-src 'unsafe-inline' 'unsafe-eval' *; frame-src 'se\
lf' blob: https data: https; img-src 'self' data: https:; font-src 'self' data:; connect-src 'self' data: https:; worker-src blob:;\
child-src blob:, default-src 'unsafe-inline' 'unsafe-eval' *;]; Set-Cookie:[]; Cross-Origin-Resource-Policy:[same-origin, same-ori\
gin]; Cross-Origin-Embedder-Policy:[require-corp, require-corp]; Content-Type:[application/json; charset=UTF-8]; ]
 
 
Headers list: 
--------
Transfer-Encoding:chunked; null:HTTP/1.1 200 OK; Server:,; X-Content-Type-Options:nosniff,nosniff; Cross-Origin-Opener-Policy:same-\
origin,same-origin; X-Permitted-Cross-Domain-Policies:none,none; Pragma:no-cache; Date:Fri, 23 Oct 2026 18:37:19 GMT; Referrer-Poli\
cy:strict-origin-when-cross-origin,strict-origin-when-cross-origin; X-Frame-Options:SAMEORIGIN,deny; Strict-Transport-Security:max-\
age=31536000; includeSubDomains,max-age=31536000; includeSubDomains; x-xss-protection:0; Cache-Control:no-store, no-cache, max-age=\
0; Content-Security-Policy:default-src 'unsafe-inline' 'unsafe-eval' *; frame-src 'self' blob: https data: https; img-src 'self' da\
ta: https:; font-src 'self' data:; connect-src 'self' data: https:; worker-src blob:; child-src blob:,default-src 'unsafe-inline' '\
unsafe-eval' *;; Set-Cookie:; Cross-Origin-Resource-Policy:same-origin,same-origin; Cross-Origin-Embedder-Policy:require-corp,requi\
re-corp; Content-Type:application/json; charset=UTF-8; 
[Extracted runtime parameter: 'SESSIONID' ==> ''] 
[Extracted runtime parameter: 'TOKEN' ==> 'eyJhbGciOiJSUzI1NiIsImtpZCI6IjkwMTk3RTZCLThEMDEtNDg0Ny1CQThELTNCRDdDRDg4QUUxQSIsInR5cCI6\
IkpXVCJ9.eyJpc3MiOiJodHRwczovL3NpY3NuLmNhaXhhL3BzYXV0aCIsIm5iZiI6MTc5Mjc4MDYzOSwiaWF0IjoxNzkyNzgwNjM5LCJleHAiOjE3OTI3ODQyMzksImF1ZC\
I6WyJwdWJsaWNhcGkiLCJtb2JpbGVhcHAiLCJodHRwczovL3NpY3NuLmNhaXhhL3BzYXV0aC9yZXNvdXJjZXMiXSwic2NvcGUiOlsicHVibGljYXBpIl0sImNsaWVudF9pZ\
CI6IjA5OGM0ZjQ5LWVmYTUtNDA0Mi1iMTlmLThhOGI1YWZjNzlkMiIsIl9jbGllbnRBY2Nlc3NQb2xpY3lJZCI6IjMzMiIsIl9jbGllbnRVc2VySWQiOiIxOTAyIiwianRp\
IjoiMzc3Mzg1Nzc3ODczRDRBRkU5MDg5QjYwNzBFNDUwN0IifQ.DiiIfddnnfwlqEAlxS367sAk5cU-Kmg73aGaRJwcN39o37zA-7A_EtPdQGBAKc51I7EPy7ey7v9dpTQd\
dQfeUbiTq8NDzHQHyNqjNrSDPrk8BvgNbtxSQsMuBwwvwjBA-IpyADwrxB-D7KDV3IaNMjgio2o3fQnOFVUP_hhNddy7v4xKJc0sAKE-QfY4kPkp2N_Itiz55xlG-kxj5Ml\
UyQM8T1yvNXw9GG5pRrfYhuiv-lnzR4rVykSIZf4T55yUYgzTncN6GLkhFJaIZSKmjhYnOJ09zPGOAFH1uq3quJRQk-JgcKBRWaU27FTmwBYWMXqqy1HN5zWqmfoNmeVZIQ\
']
 
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
m_statusCode=200
m_statusMesg=OK
, m_message=
{
    "UserName": "SIFXDB01",
    "UserId": 1902,
    "EmailAddress": null,
    "SID": null,
    "Name": "SIFXDB01"
}
m_contentType=application/json; charset=utf-8
, m_headers=null:[HTTP/1.1 200 OK]; Server:[]; X-Content-Type-Options:[nosniff]; Cross-Origin-Opener-Policy:[same-origin]; X-Permit\
ted-Cross-Domain-Policies:[none]; Pragma:[no-cache]; Date:[Fri, 23 Oct 2026 18:37:19 GMT]; Referrer-Policy:[strict-origin-when-cros\
s-origin]; X-Frame-Options:[SAMEORIGIN]; Strict-Transport-Security:[max-age=31536000; includeSubDomains]; x-xss-protection:[0]; Cac\
he-Control:[no-cache]; Content-Security-Policy:[default-src 'unsafe-inline' 'unsafe-eval' *; frame-src 'self' blob: https data: htt\
ps; img-src 'self' data: https:; font-src 'self' data:; connect-src 'self' data: https:; worker-src blob:; child-src blob:]; Set-Co\
okie:[]; Cross-Origin-Resource-Policy:[same-origin]; Cross-Origin-Embedder-Policy:[require-corp]; Expires:[-1]; Content-Length:[86]\
; Content-Type:[application/json; charset=utf-8]; ]
 
 
=============================================
Operation: Execute
Step name: 'Obter credencial'
=============================================
REST service details: 
--------------------
 
method: 	GET
URL: 	https://sicsn.caixa path: /BeyondTrust/api/public/v3/Secrets-Safe/Secrets?FolderPath=SIIFX_BATCH_DES
 
Response: 
--------
HttpResponseInfo [
m_statusCode=401
m_statusMesg=Unauthorized
, m_message=
"User not authenticated"
m_contentType=application/json
, m_headers=null:[HTTP/1.1 401 Unauthorized]; Server:[]; X-Content-Type-Options:[nosniff]; Cross-Origin-Opener-Policy:[same-origin]\
; X-Permitted-Cross-Domain-Policies:[none]; Pragma:[no-cache]; Date:[Fri, 23 Oct 2026 18:37:19 GMT]; Referrer-Policy:[strict-origin\
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
ted-Cross-Domain-Policies:[none]; Pragma:[no-cache]; Date:[Fri, 23 Oct 2026 18:37:19 GMT]; Referrer-Policy:[strict-origin-when-cros\
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
: Unauthorized message: "User not authenticated"
 
 
Job statistics:
+-------------------------+-------------------------+
|Start Time               |20261023153713           |
+-------------------------+-------------------------+
|End Time                 |20261023153715           |
+-------------------------+-------------------------+
|Elapsed Time             |227                      |
+-------------------------+-------------------------+
Exit Code    = 1
Exit Message = Application Integrator plugin: UCM0001 = Application Integrator plugin: UCM0001 = REST request failed. status code: \
401 response is: Unauthorized message:  User not authenticated
 
