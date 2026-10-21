
-sh-4.2$
-sh-4.2$ openssl s_client -connect 10.116.83.19:8443 -servername sctdeapllx0018.df.caixa </dev/null 2>/dev/null | openssl x509 -noout -subject -issuer -dates
subject= /C=DF/ST=Distrito Federal/L=Brasilia/O=Caixa Economica Federal/OU=CEPEM/CN=SIGCT
issuer= /C=DF/ST=Distrito Federal/L=Brasilia/O=Caixa Economica Federal/OU=CEPEM/CN=SIGCT
notBefore=Aug  3 18:12:45 2022 GMT
notAfter=Jun 29 18:12:45 4760 GMT
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs -n simpf-des simpf-backend-des-448-n4gpg | grep -A 40 "avisoGeral: java.lang.NullPointerException" | grep -E "NullPointer|Caused by|br.gov.caixa" | head -20
2026-10-20 15:45:07,806 ERROR [io.und.req.io] (executor-thread-2) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-2 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
        at br.gov.caixa.simpf.exception.NegocioExceptionMapper.toResponse(NegocioExceptionMapper.java:28)
        at br.gov.caixa.simpf.exception.NegocioExceptionMapper.toResponse(NegocioExceptionMapper.java:14)
2026-10-20 15:45:07,806 ERROR [io.und.req.io] (executor-thread-4) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-1 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
        at br.gov.caixa.simpf.exception.NegocioExceptionMapper.toResponse(NegocioExceptionMapper.java:28)
        at br.gov.caixa.simpf.exception.NegocioExceptionMapper.toResponse(NegocioExceptionMapper.java:14)
2026-10-20 15:45:11,478 ERROR [io.und.req.io] (executor-thread-5) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-6 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
        at br.gov.caixa.simpf.exception.NegocioExceptionMapper.toResponse(NegocioExceptionMapper.java:28)
        at br.gov.caixa.simpf.exception.NegocioExceptionMapper.toResponse(NegocioExceptionMapper.java:14)
2026-10-20 15:45:11,494 ERROR [io.und.req.io] (executor-thread-6) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-8 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
        at br.gov.caixa.simpf.exception.NegocioExceptionMapper.toResponse(NegocioExceptionMapper.java:28)
        at br.gov.caixa.simpf.exception.NegocioExceptionMapper.toResponse(NegocioExceptionMapper.java:14)
2026-10-20 15:47:22,245 ERROR [io.und.req.io] (executor-thread-5) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-10 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
        at br.gov.caixa.simpf.exception.NegocioExceptionMapper.toResponse(NegocioExceptionMapper.java:28)
        at br.gov.caixa.simpf.exception.NegocioExceptionMapper.toResponse(NegocioExceptionMapper.java:14)
2026-10-20 15:47:22,259 ERROR [io.und.req.io] (executor-thread-6) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-12 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
        at br.gov.caixa.simpf.exception.NegocioExceptionMapper.toResponse(NegocioExceptionMapper.java:28)
        at br.gov.caixa.simpf.exception.NegocioExceptionMapper.toResponse(NegocioExceptionMapper.java:14)
2026-10-20 16:15:18,937 ERROR [io.und.req.io] (executor-thread-7) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-14 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
        at br.gov.caixa.simpf.exception.NegocioExceptionMapper.toResponse(NegocioExceptionMapper.java:28)
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n simpf-des simpf-backend-des-448-n4gpg -- sh -c 'echo | keytool -list -v -keystore /deployments/caixa-truststore-acteste-nprd.jks 2>/dev/null | grep -i "CN=SIGCT"'
command terminated with exit code 1
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n simpf-tqs simpf-backend-tqs-290-rgftv -- env | grep -i sigct
API_SIGCT_URL=https://sctdeapllx0018.df.caixa:8443
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n simpf-tqs simpf-backend-tqs-290-rgftv -- ps -ef | grep -o "trustStore=[^ ]*"
time="2026-10-21T17:30:45Z" level=error msg="exec failed: unable to start container process: exec: \"ps\": executable file not found in $PATH"
command terminated with exit code 255
-sh-4.2$



beleza mais o cleomar ta questinado isso aqui

SIPDM
 
tem modulo nao né?
 
tem, só confirmando aqui
 
api-estudante


 eu acho que o sipdm nao tem ahver com o que foi feito ele ta dano uma de jao sem bralo e qer que eu resolva o problema dele



