# log do agente no caixinhas: qual usuário e qual segredo travou
oc logs siifx-caixinhas-api-aplicacao-des-70-t2rc5 -c secrets-agent-sidecar | grep -E 'secret path|ERROR|UserName'

# variáveis do agente (credencial / usuário / lista de segredos)
oc get pod siifx-caixinhas-api-aplicacao-des-70-t2rc5 \
  -o jsonpath='{.spec.initContainers[?(@.name=="secrets-agent-sidecar")].env}' | tr ',' '\n'


  oc get secret <nome-da-secret> -o jsonpath='{.data.<chave>}' | base64 -d; echo

  
