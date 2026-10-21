
-sh-4.2$
-sh-4.2$ oc logs -n simpf-des simpf-backend-des-448-n4gpg  | grep -iE "sctdeapllx0018|sigct|pkix|ssl|handshake|timed out" | tail -30
        at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
        at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
        at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs -n simpf-des simpf-backend-des-448-n4gpg | grep -vE '^\s+at ' \
>   | grep -iE "exception|error|sctdeapllx0018|sigct|pkix|handshake|timed out|refused" | tail -40
2026-10-21 13:08:56,488 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-6) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:08:56,488 ERROR [io.und.req.io] (executor-thread-6) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-99 to /ParametrosGerais/indsSistema: java.lang.NullPointerException
2026-10-21 13:08:56,496 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-6) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:08:56,496 ERROR [io.und.req.io] (executor-thread-6) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-100 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
2026-10-21 13:08:56,505 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-7) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:08:56,505 ERROR [io.und.req.io] (executor-thread-7) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-101 to /ParametrosGerais/indsSistema: java.lang.NullPointerException
2026-10-21 13:08:56,509 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-7) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:08:56,509 ERROR [io.und.req.io] (executor-thread-7) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-102 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
2026-10-21 13:31:55,070 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-5) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:31:55,070 ERROR [io.und.req.io] (executor-thread-5) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-103 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
2026-10-21 13:31:55,070 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-6) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:31:55,070 ERROR [io.und.req.io] (executor-thread-6) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-104 to /ParametrosGerais/indsSistema: java.lang.NullPointerException
2026-10-21 13:31:55,082 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-6) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:31:55,082 ERROR [io.und.req.io] (executor-thread-6) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-105 to /ParametrosGerais/indsSistema: java.lang.NullPointerException
2026-10-21 13:31:55,082 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-7) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:31:55,082 ERROR [io.und.req.io] (executor-thread-7) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-106 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
2026-10-21 13:32:33,325 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-6) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:32:33,325 ERROR [io.und.req.io] (executor-thread-6) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-107 to /ParametrosGerais/indsSistema: java.lang.NullPointerException
2026-10-21 13:32:33,375 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-6) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:32:33,375 ERROR [io.und.req.io] (executor-thread-6) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-108 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
2026-10-21 13:32:33,377 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-7) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:32:33,377 ERROR [io.und.req.io] (executor-thread-7) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-109 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
2026-10-21 13:32:33,381 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-7) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:32:33,381 ERROR [io.und.req.io] (executor-thread-7) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-110 to /ParametrosGerais/indsSistema: java.lang.NullPointerException
2026-10-21 13:39:55,552 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-6) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:39:55,552 ERROR [io.und.req.io] (executor-thread-6) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-111 to /ParametrosGerais/indsSistema: java.lang.NullPointerException
2026-10-21 13:39:55,652 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-6) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:39:55,652 ERROR [io.und.req.io] (executor-thread-6) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-112 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
2026-10-21 13:39:55,660 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-6) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:39:55,660 ERROR [io.und.req.io] (executor-thread-6) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-113 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
2026-10-21 13:39:55,670 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-6) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:39:55,670 ERROR [io.und.req.io] (executor-thread-6) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-114 to /ParametrosGerais/indsSistema: java.lang.NullPointerException
2026-10-21 13:40:31,448 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-7) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:40:31,448 ERROR [io.und.req.io] (executor-thread-7) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-115 to /ParametrosGerais/indsSistema: java.lang.NullPointerException
2026-10-21 13:40:31,516 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-7) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:40:31,516 ERROR [io.und.req.io] (executor-thread-7) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-116 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
2026-10-21 13:40:31,526 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-7) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:40:31,526 ERROR [io.und.req.io] (executor-thread-7) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-117 to /ParametrosGerais/avisoGeral: java.lang.NullPointerException
2026-10-21 13:40:31,529 ERROR [br.gov.cai.sim.exc.NegocioExceptionMapper] (executor-thread-6) ------> erro: br.gov.caixa.simpf.exception.NegocioException
2026-10-21 13:40:31,529 ERROR [io.und.req.io] (executor-thread-6) Exception handling request 64c029e8-b0e2-466e-adc2-df3cbae46d06-118 to /ParametrosGerais/indsSistema: java.lang.NullPointerException
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n simpf-des simpf-backend-des-448-n4gpg -- env | grep -iE "sigct|sctde|8443|url"
API_SIPGC_URL=http://sctdeapllx0020.df.caixa:8181
SIMPF_DATABASE_DATASOURCE_JDBC_URL=jdbc:oracle:thin:@cnpexdadvm01clu04.extra.caixa.gov.br:1521/cdbd08ngpdb003
API_SIICO_PUB_URL=https://api.des.caixa:8443/informacoes-corporativas-publicas
API_SIGCT_URL=https://sctdeapllx0018.df.caixa:8443
API_SIICO_URL=https://api.des.caixa:8443/informacoes-corporativas-privadas
API_SIPGC_SIAPP_URL=http://sctdeapllx0020.df.caixa:8184
QUARKUS_OIDC_INTRANET_AUTH_SERVER_URL=https://login.des.caixa/auth/realms/intranet
SIICO_DATABASE_DATASOURCE_JDBC_URL=jdbc:postgresql://10.116.101.101:5172/icodb001
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ openssl s_client -connect 10.116.83.19:8443 -servername sctdeapllx0018.df.caixa </dev/null 2>/dev/null | openssl x509 -noout -subject -issuer -dates
subject= /C=DF/ST=Distrito Federal/L=Brasilia/O=Caixa Economica Federal/OU=CEPEM/CN=SIGCT
issuer= /C=DF/ST=Distrito Federal/L=Brasilia/O=Caixa Economica Federal/OU=CEPEM/CN=SIGCT
notBefore=Aug  3 18:12:45 2022 GMT
notAfter=Jun 29 18:12:45 4760 GMT
-sh-4.2$
-sh-4.2$
-sh-4.2$
