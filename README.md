-sh-4.2$
-sh-4.2$
-sh-4.2$ POD=$(oc get pods -n sipgc-des --no-headers | grep informacoes | grep Running | awk '{print $1}' | head -1); oc exec -it $POD -n sipgc-des -- bash -c "timeout 5 bash -c '</dev/tcp/des.sigoc.caixa/443' && echo ABERTA || echo SEM CONEXAO"
SEM CONEXAO
-sh-4.2$



eu nao enteid porque esse teste na ofoi pedido regra nehum a que estava entes fizeram errada eu nao solicitei uma nova, vou fazer isso agora
