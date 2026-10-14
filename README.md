-sh-4.2$
-sh-4.2$ oc project siifx-des
Now using project "siifx-des" on server "https://api.nprd.caixa:6443".
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pod siifx-api-aplicacao-des-2896-p97pn -n siifx-des \
>   -o jsonpath='{range .spec.initContainers[*]}{.name}{"\n"}{end}'
Error from server (NotFound): pods "siifx-api-aplicacao-des-2896-p97pn" not found
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pod siifx-api-aplicacao-des-2896-p97pn -n siifx-des \
>   -o jsonpath='{.spec.initContainers[?(@.name=="<init-agente>")].env}' | tr ',' '\n'
Error from server (NotFound): pods "siifx-api-aplicacao-des-2896-p97pn" not found
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc debug pod/siifx-api-aplicacao-des-2896-p97pn -c <init-agente> -n siifx-des
-sh: init-agente: Arquivo ou diretório não encontrado
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods
NAME                                              READY     STATUS                  RESTARTS       AGE
quarkus-4-deploy                                  0/1       Completed               0              370d
siifx-api-aplicacao-des-2892-deploy               0/1       Completed               0              17h
siifx-api-aplicacao-des-2893-deploy               0/1       Completed               0              14h
siifx-api-aplicacao-des-2893-dmdmb                0/1       Init:0/2                0              4s
siifx-api-aplicacao-des-2893-qcnl4                0/1       Init:0/2                0              4s
siifx-api-aplicacao-des-2896-jc2fl                0/1       Terminating             0              104s
siifx-api-consulta-investi-des-37-deploy          0/1       Completed               0              109d
siifx-api-consulta-investi-des-38-deploy          0/1       Completed               0              105d
siifx-api-consulta-investi-des-38-gh474           1/1       Running                 0              105d
siifx-api-informacoes-financeiras-des-21-deploy   0/1       Completed               0              140d
siifx-api-informacoes-financeiras-des-21-ps7wb    1/1       Running                 0              140d
siifx-api-openfinance-des-16-deploy               0/1       Completed               0              140d
siifx-api-openfinance-des-16-rtwjt                1/1       Running                 0              140d
siifx-caixinhas-api-aplicacao-des-64-deploy       0/1       Completed               0              18h
siifx-caixinhas-api-aplicacao-des-65-d7655        1/1       Running                 0              10h
siifx-caixinhas-api-aplicacao-des-65-deploy       0/1       Completed               0              10h
siifx-caixinhas-api-aplicacao-des-66-deploy       0/1       Error                   0              10h
siifx-caixinhas-api-aplicacao-des-67-deploy       0/1       Error                   0              70m
siifx-caixinhas-api-aplicacao-des-68-deploy       0/1       Error                   0              50m
siifx-caixinhas-api-aplicacao-des-69-deploy       0/1       Error                   0              18m
siifx-caixinhas-api-aplicacao-des-70-deploy       1/1       Running                 0              7m4s
siifx-caixinhas-api-aplicacao-des-70-t2rc5        0/1       Init:CrashLoopBackOff   5 (108s ago)   7m
siifx-web-des-289-deploy                          0/1       Completed               0              6d
siifx-web-des-290-9469x                           2/2       Running                 0              25h
siifx-web-des-290-deploy                          0/1       Completed               0              25h
siifx-web-tgs-des-6-deploy                        0/1       Error                   0              32d
siifx-web-tgs-des-7-deploy                        0/1       Error                   0              18d
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
