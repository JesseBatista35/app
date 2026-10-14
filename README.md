
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs siifx-caixinhas-api-aplicacao-des-70-t2rc5 -c secrets-agent-sidecar | grep -E 'secret path|ERROR|UserName'
Error from server (NotFound): pods "siifx-caixinhas-api-aplicacao-des-70-t2rc5" not found
-sh-4.2$ oc get pod siifx-caixinhas-api-aplicacao-des-70-t2rc5 \
>   -o jsonpath='{.spec.initContainers[?(@.name=="secrets-agent-sidecar")].env}' | tr ',' '\n'
Error from server (NotFound): pods "siifx-caixinhas-api-aplicacao-des-70-t2rc5" not found
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get secret <nome-da-secret> -o jsonpath='{.data.<chave>}' | base64 -d; echo
-sh: nome-da-secret: Arquivo ou diretório não encontrado

-sh-4.2$
