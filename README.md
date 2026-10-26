Environment information:

+-------------------------+--------------------------------------------------+

|Connection Profile Name  |IIFX_TESTE                                        |

+-------------------------+--------------------------------------------------+

|Connection Profile Scope |Local                                             |

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

HRwczovL3NpY3NuLmNhaXhhL3BzYXV0aCIsIm5iZiI6MTc5MzAzNDU1MiwiaWF0IjoxNzkzMDM0NTUyLCJleHAiOjE3OTMwMzgxNTIsImF1ZCI6WyJwdWJsaWNhcGkiLCJt\

b2JpbGVhcHAiLCJodHRwczovL3NpY3NuLmNhaXhhL3BzYXV0aC9yZXNvdXJjZXMiXSwic2NvcGUiOlsicHVibGljYXBpIl0sImNsaWVudF9pZCI6IjI4YjVkMjFmLTIyODg\

tNGYwMy04OWNjLWM1OTk5ZmE4NWUyNiIsIl9jbGllbnRBY2Nlc3NQb2xpY3lJZCI6IjMzMiIsIl9jbGllbnRVc2VySWQiOiIxOTgzIiwianRpIjoiMThBN0Q2RTk3QzREMz\

A3RENBN0RCNUU1MkI1QjVDQzYifQ.cChtMtywqWQzp1F-QmyGCLUfkDh3Kx3ijt0rKwkzWQsdOBVTLl6pBQ3ComTC-bHWkf0-sov51Jg9bDugWcXyWy_R_aQ6V7Dk8PXuRk\

k0O3hKc8aYxE5djCH_Hgj3z4Vxjkh2PASgDww-RSFuqFzis7KmhOSW7L_L_-sQS6W2bDzqAJsO4VNUDEeSkAFUQGn44tvL71-dZaKl3LBtg0UVN6nppPSvcll_p-5cYdvvE\

xkroMG73xzZidDJBQZs53Ye7EQPVCIsbi-bCH8CQnGFiM6jJtSl6NsDgcg-fTHP-QhvpdCyfgfTi3_nkAD73WUUmMkTTnYn3CPREK9TLfN3Ww",

    "scope": "publicapi",

    "token_type": "Bearer",

    "expires_in": 3600

}

m_contentType=application/json; charset=UTF-8

, m_headers=Transfer-Encoding:[chunked]; null:[HTTP/1.1 200 OK]; Server:[, ]; X-Content-Type-Options:[nosniff, nosniff]; Cross-Orig\

in-Opener-Policy:[same-origin, same-origin]; X-Permitted-Cross-Domain-Policies:[none, none]; Pragma:[no-cache]; Date:[Mon, 26 Oct 2\

026 17:09:11 GMT]; Referrer-Policy:[strict-origin-when-cross-origin, strict-origin-when-cross-origin]; X-Frame-Options:[SAMEORIGIN,\

deny]; Strict-Transport-Security:[max-age=31536000; includeSubDomains, max-age=31536000; includeSubDomains]; x-xss-protection:[0];\

Cache-Control:[no-store, no-cache, max-age=0]; Content-Security-Policy:[default-src 'unsafe-inline' 'unsafe-eval' *; frame-src 'se\

lf' blob: https data: https; img-src 'self' data: https:; font-src 'self' data:; connect-src 'self' data: https:; worker-src blob:;\

child-src blob:, default-src 'unsafe-inline' 'unsafe-eval' *;]; Set-Cookie:[]; Cross-Origin-Resource-Policy:[same-origin, same-ori\

gin]; Cross-Origin-Embedder-Policy:[require-corp, require-corp]; Content-Type:[application/json; charset=UTF-8]; ]
 
 
Headers list: 

--------

Transfer-Encoding:chunked; null:HTTP/1.1 200 OK; Server:,; X-Content-Type-Options:nosniff,nosniff; Cross-Origin-Opener-Policy:same-\

origin,same-origin; X-Permitted-Cross-Domain-Policies:none,none; Pragma:no-cache; Date:Mon, 26 Oct 2026 17:09:11 GMT; Referrer-Poli\

cy:strict-origin-when-cross-origin,strict-origin-when-cross-origin; X-Frame-Options:SAMEORIGIN,deny; Strict-Transport-Security:max-\

age=31536000; includeSubDomains,max-age=31536000; includeSubDomains; x-xss-protection:0; Cache-Control:no-store, no-cache, max-age=\

0; Content-Security-Policy:default-src 'unsafe-inline' 'unsafe-eval' *; frame-src 'self' blob: https data: https; img-src 'self' da\

ta: https:; font-src 'self' data:; connect-src 'self' data: https:; worker-src blob:; child-src blob:,default-src 'unsafe-inline' '\

unsafe-eval' *;; Set-Cookie:; Cross-Origin-Resource-Policy:same-origin,same-origin; Cross-Origin-Embedder-Policy:require-corp,requi\

re-corp; Content-Type:application/json; charset=UTF-8; 

[Extracted runtime parameter: 'SESSIONID' ==> ''] 

[Extracted runtime parameter: 'TOKEN' ==> 'eyJhbGciOiJSUzI1NiIsImtpZCI6IjkwMTk3RTZCLThEMDEtNDg0Ny1CQThELTNCRDdDRDg4QUUxQSIsInR5cCI6\

IkpXVCJ9.eyJpc3MiOiJodHRwczovL3NpY3NuLmNhaXhhL3BzYXV0aCIsIm5iZiI6MTc5MzAzNDU1MiwiaWF0IjoxNzkzMDM0NTUyLCJleHAiOjE3OTMwMzgxNTIsImF1ZC\

I6WyJwdWJsaWNhcGkiLCJtb2JpbGVhcHAiLCJodHRwczovL3NpY3NuLmNhaXhhL3BzYXV0aC9yZXNvdXJjZXMiXSwic2NvcGUiOlsicHVibGljYXBpIl0sImNsaWVudF9pZ\

CI6IjI4YjVkMjFmLTIyODgtNGYwMy04OWNjLWM1OTk5ZmE4NWUyNiIsIl9jbGllbnRBY2Nlc3NQb2xpY3lJZCI6IjMzMiIsIl9jbGllbnRVc2VySWQiOiIxOTgzIiwianRp\

IjoiMThBN0Q2RTk3QzREMzA3RENBN0RCNUU1MkI1QjVDQzYifQ.cChtMtywqWQzp1F-QmyGCLUfkDh3Kx3ijt0rKwkzWQsdOBVTLl6pBQ3ComTC-bHWkf0-sov51Jg9bDug\

WcXyWy_R_aQ6V7Dk8PXuRkk0O3hKc8aYxE5djCH_Hgj3z4Vxjkh2PASgDww-RSFuqFzis7KmhOSW7L_L_-sQS6W2bDzqAJsO4VNUDEeSkAFUQGn44tvL71-dZaKl3LBtg0U\

VN6nppPSvcll_p-5cYdvvExkroMG73xzZidDJBQZs53Ye7EQPVCIsbi-bCH8CQnGFiM6jJtSl6NsDgcg-fTHP-QhvpdCyfgfTi3_nkAD73WUUmMkTTnYn3CPREK9TLfN3Ww\

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

    "UserName": "SIFXDB02",

    "UserId": 1983,

    "EmailAddress": null,

    "SID": null,

    "Name": "SIFXDB02"

}

m_contentType=application/json; charset=utf-8

, m_headers=null:[HTTP/1.1 200 OK]; Server:[]; X-Content-Type-Options:[nosniff]; Cross-Origin-Opener-Policy:[same-origin]; X-Permit\

ted-Cross-Domain-Policies:[none]; Pragma:[no-cache]; Date:[Mon, 26 Oct 2026 17:09:11 GMT]; Referrer-Policy:[strict-origin-when-cros\

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

; X-Permitted-Cross-Domain-Policies:[none]; Pragma:[no-cache]; Date:[Mon, 26 Oct 2026 17:09:11 GMT]; Referrer-Policy:[strict-origin\

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

ted-Cross-Domain-Policies:[none]; Pragma:[no-cache]; Date:[Mon, 26 Oct 2026 17:09:11 GMT]; Referrer-Policy:[strict-origin-when-cros\

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

#export ARQ_OUTPUT=/tmp/SIIFX_${ID}.txt
 
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

|Start Time               |20261026140904           |

+-------------------------+-------------------------+

|End Time                 |20261026140905           |

+-------------------------+-------------------------+

|Elapsed Time             |132                      |

+-------------------------+-------------------------+

Exit Code    = 1

Exit Message = Application Integrator plugin: UCM0001 = Application Integrator plugin: UCM0001 = REST request failed. status code: \

401 response is: Unauthorized message:  User not authenticated
 
 
 
Environment information:

+-------------------------+--------------------------------------------------+

|Connection Profile Name  |IIFX_TESTE                                        |

+-------------------------+--------------------------------------------------+

|Connection Profile Scope |Local                                             |

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

HRwczovL3NpY3NuLmNhaXhhL3BzYXV0aCIsIm5iZiI6MTc5MzAzNTc2OSwiaWF0IjoxNzkzMDM1NzY5LCJleHAiOjE3OTMwMzkzNjksImF1ZCI6WyJwdWJsaWNhcGkiLCJt\

b2JpbGVhcHAiLCJodHRwczovL3NpY3NuLmNhaXhhL3BzYXV0aC9yZXNvdXJjZXMiXSwic2NvcGUiOlsicHVibGljYXBpIl0sImNsaWVudF9pZCI6IjI4YjVkMjFmLTIyODg\

tNGYwMy04OWNjLWM1OTk5ZmE4NWUyNiIsIl9jbGllbnRBY2Nlc3NQb2xpY3lJZCI6IjMzMiIsIl9jbGllbnRVc2VySWQiOiIxOTgzIiwianRpIjoiRTBBMTVDQkYxODIyRk\

ZGNEYyODBGQzc4OTIwRDREQzUifQ.GL_Pj9zO7Irn0yY3yexSsnqYuGFUQnYc7r0PerqNqWYWqtdFgBVhCDVLMnzk0TScK9hAddyWzv2-FXCfCaYgTdUNLLkh9JG6tsxyJr\

Bk-xQtcUt1v0ooYvIJ4M2reNHElIqIU9SqGD6yGj3AplCbJjXlAXqTzPhWY7IAXIvcYrYErscMv-DRHMIfcdF7VmXJRUqOz0-uXdCHnRLZSQhHSZ2PG8UqoCvBZK6H9im0b\

gkJtulDgnDLoSqiwZ1iNtyeGdDunADwVUuZK6FmoOlp4gXpXAMrC2NXS2XEWvBMS-ZGPDTEJr0zinywvww9hGV0g9O5oRU4yOBcd-lb9e1OPQ",

    "scope": "publicapi",

    "token_type": "Bearer",

    "expires_in": 3600

}

m_contentType=application/json; charset=UTF-8

, m_headers=Transfer-Encoding:[chunked]; null:[HTTP/1.1 200 OK]; Server:[, ]; X-Content-Type-Options:[nosniff, nosniff]; Cross-Orig\

in-Opener-Policy:[same-origin, same-origin]; X-Permitted-Cross-Domain-Policies:[none, none]; Pragma:[no-cache]; Date:[Mon, 26 Oct 2\

026 17:29:29 GMT]; Referrer-Policy:[strict-origin-when-cross-origin, strict-origin-when-cross-origin]; X-Frame-Options:[SAMEORIGIN,\

deny]; Strict-Transport-Security:[max-age=31536000; includeSubDomains, max-age=31536000; includeSubDomains]; x-xss-protection:[0];\

Cache-Control:[no-store, no-cache, max-age=0]; Content-Security-Policy:[default-src 'unsafe-inline' 'unsafe-eval' *; frame-src 'se\

lf' blob: https data: https; img-src 'self' data: https:; font-src 'self' data:; connect-src 'self' data: https:; worker-src blob:;\

child-src blob:, default-src 'unsafe-inline' 'unsafe-eval' *;]; Set-Cookie:[]; Cross-Origin-Resource-Policy:[same-origin, same-ori\

gin]; Cross-Origin-Embedder-Policy:[require-corp, require-corp]; Content-Type:[application/json; charset=UTF-8]; ]
 
 
Headers list: 

--------

Transfer-Encoding:chunked; null:HTTP/1.1 200 OK; Server:,; X-Content-Type-Options:nosniff,nosniff; Cross-Origin-Opener-Policy:same-\

origin,same-origin; X-Permitted-Cross-Domain-Policies:none,none; Pragma:no-cache; Date:Mon, 26 Oct 2026 17:29:29 GMT; Referrer-Poli\

cy:strict-origin-when-cross-origin,strict-origin-when-cross-origin; X-Frame-Options:SAMEORIGIN,deny; Strict-Transport-Security:max-\

age=31536000; includeSubDomains,max-age=31536000; includeSubDomains; x-xss-protection:0; Cache-Control:no-store, no-cache, max-age=\

0; Content-Security-Policy:default-src 'unsafe-inline' 'unsafe-eval' *; frame-src 'self' blob: https data: https; img-src 'self' da\

ta: https:; font-src 'self' data:; connect-src 'self' data: https:; worker-src blob:; child-src blob:,default-src 'unsafe-inline' '\

unsafe-eval' *;; Set-Cookie:; Cross-Origin-Resource-Policy:same-origin,same-origin; Cross-Origin-Embedder-Policy:require-corp,requi\

re-corp; Content-Type:application/json; charset=UTF-8; 

[Extracted runtime parameter: 'SESSIONID' ==> ''] 

[Extracted runtime parameter: 'TOKEN' ==> 'eyJhbGciOiJSUzI1NiIsImtpZCI6IjkwMTk3RTZCLThEMDEtNDg0Ny1CQThELTNCRDdDRDg4QUUxQSIsInR5cCI6\

IkpXVCJ9.eyJpc3MiOiJodHRwczovL3NpY3NuLmNhaXhhL3BzYXV0aCIsIm5iZiI6MTc5MzAzNTc2OSwiaWF0IjoxNzkzMDM1NzY5LCJleHAiOjE3OTMwMzkzNjksImF1ZC\

I6WyJwdWJsaWNhcGkiLCJtb2JpbGVhcHAiLCJodHRwczovL3NpY3NuLmNhaXhhL3BzYXV0aC9yZXNvdXJjZXMiXSwic2NvcGUiOlsicHVibGljYXBpIl0sImNsaWVudF9pZ\

CI6IjI4YjVkMjFmLTIyODgtNGYwMy04OWNjLWM1OTk5ZmE4NWUyNiIsIl9jbGllbnRBY2Nlc3NQb2xpY3lJZCI6IjMzMiIsIl9jbGllbnRVc2VySWQiOiIxOTgzIiwianRp\

IjoiRTBBMTVDQkYxODIyRkZGNEYyODBGQzc4OTIwRDREQzUifQ.GL_Pj9zO7Irn0yY3yexSsnqYuGFUQnYc7r0PerqNqWYWqtdFgBVhCDVLMnzk0TScK9hAddyWzv2-FXCf\

CaYgTdUNLLkh9JG6tsxyJrBk-xQtcUt1v0ooYvIJ4M2reNHElIqIU9SqGD6yGj3AplCbJjXlAXqTzPhWY7IAXIvcYrYErscMv-DRHMIfcdF7VmXJRUqOz0-uXdCHnRLZSQh\

HSZ2PG8UqoCvBZK6H9im0bgkJtulDgnDLoSqiwZ1iNtyeGdDunADwVUuZK6FmoOlp4gXpXAMrC2NXS2XEWvBMS-ZGPDTEJr0zinywvww9hGV0g9O5oRU4yOBcd-lb9e1OPQ\

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

    "UserName": "SIFXDB02",

    "UserId": 1983,

    "EmailAddress": null,

    "SID": null,

    "Name": "SIFXDB02"

}

m_contentType=application/json; charset=utf-8

, m_headers=null:[HTTP/1.1 200 OK]; Server:[]; X-Content-Type-Options:[nosniff]; Cross-Origin-Opener-Policy:[same-origin]; X-Permit\

ted-Cross-Domain-Policies:[none]; Pragma:[no-cache]; Date:[Mon, 26 Oct 2026 17:29:29 GMT]; Referrer-Policy:[strict-origin-when-cros\

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

; X-Permitted-Cross-Domain-Policies:[none]; Pragma:[no-cache]; Date:[Mon, 26 Oct 2026 17:29:29 GMT]; Referrer-Policy:[strict-origin\

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

ted-Cross-Domain-Policies:[none]; Pragma:[no-cache]; Date:[Mon, 26 Oct 2026 17:29:29 GMT]; Referrer-Policy:[strict-origin-when-cros\

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

#export ARQ_OUTPUT=/tmp/SIIFX_${ID}.txt
 
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

|Start Time               |20261026142922           |

+-------------------------+-------------------------+

|End Time                 |20261026142923           |

+-------------------------+-------------------------+

|Elapsed Time             |133                      |

+-------------------------+-------------------------+

Exit Code    = 1

Exit Message = Application Integrator plugin: UCM0001 = Application Integrator plugin: UCM0001 = REST request failed. status code: \

401 response is: Unauthorized message:  User not authenticated
 
 
 
