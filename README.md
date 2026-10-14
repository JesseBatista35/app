
-sh-4.2$ oc get pod siifx-caixinhas-api-aplicacao-des-70-t2rc5 \
>   -o jsonpath='{range .spec.initContainers[*]}{.name}{"\n"}{end}'
secrets-agent-sidecar
secrets-check
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ c logs siifx-caixinhas-api-aplicacao-des-70-t2rc5 -c NOME | grep -E 'secret path|ERROR|UserName'
-sh: c: comando não encontrado
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs siifx-caixinhas-api-aplicacao-des-70-t2rc5 -c NOME | grep -E 'secret path|ERROR|UserName'
Error from server (BadRequest): container NOME is not valid for pod siifx-caixinhas-api-aplicacao-des-70-t2rc5
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pod siifx-caixinhas-api-aplicacao-des-70-t2rc5 \
>   -o jsonpath='{.spec.initContainers[?(@.name=="NOME")].env}' | tr ',' '\n'
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc debug pod/siifx-caixinhas-api-aplicacao-des-70-t2rc5 -c NOME
error: the container "NOME" is not a valid container name; must be one of [siifx-caixinhas-api-aplicacao-des]
-sh-4.2$
-sh-4.2$
-sh-4.2$   oc get pods -w | grep siifx-api-aplicacao
siifx-api-aplicacao-des-2892-deploy               0/1       Completed               0          17h
siifx-api-aplicacao-des-2893-deploy               0/1       Completed               0          14h
siifx-api-aplicacao-des-2897-9559p                0/1       Init:0/2                0          34s
siifx-api-aplicacao-des-2897-deploy               1/1       Running                 0          1m

