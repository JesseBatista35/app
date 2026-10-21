
-sh-4.2$
-sh-4.2$ oc project simpf-des
Now using project "simpf-des" on server "https://api.nprd.caixa:6443".
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get netnamespace simpf-des
NAME        NETID      EGRESS IPS
simpf-des   12461632   ["10.116.220.37"]
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n simpf-des <pod-backend-atual> -- \
>   timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/8443' && echo OK || echo FALHA
-sh: pod-backend-atual: Arquivo ou diretório não encontrado
FALHA
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs -n simpf-des <pod-backend-atual> | grep -iE "sctdeapllx0018|sigct|pkix|ssl|handshake|timed out" | tail -30
-sh: erro de sintaxe próximo do `token' não esperado `|'
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods
NAME                            READY     STATUS      RESTARTS   AGE
simpf-backend-des-447-deploy    0/1       Completed   0          5d21h
simpf-backend-des-448-deploy    0/1       Completed   0          22h
simpf-backend-des-448-n4gpg     1/1       Running     0          22h
simpf-frontend-des-331-deploy   0/1       Completed   0          12d
simpf-frontend-des-332-deploy   0/1       Completed   0          34m
simpf-frontend-des-332-t4fqx    2/2       Running     0          34m
-sh-4.2$ oc exec -n simpf-des simpf-backend-des-448-n4gpg  -- \
>   timeout 10 bash -c 'cat < /dev/null > /dev/tcp/10.116.83.19/8443' && echo OK || echo FALHA
OK
-sh-4.2$
-sh-4.2$
-sh-4.2$
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
-sh-4.2$
