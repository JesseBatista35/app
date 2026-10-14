# 1. nomes dos init containers
oc get pod siifx-caixinhas-api-aplicacao-des-70-t2rc5 \
  -o jsonpath='{range .spec.initContainers[*]}{.name}{"\n"}{end}'

# 2. log do agente (troque NOME pelo init do secrets-agent, o que NÃO é secrets-check)
oc logs siifx-caixinhas-api-aplicacao-des-70-t2rc5 -c NOME | grep -E 'secret path|ERROR|UserName'

# 3. variáveis do agente (para ver a credencial e o usuário)
oc get pod siifx-caixinhas-api-aplicacao-des-70-t2rc5 \
  -o jsonpath='{.spec.initContainers[?(@.name=="NOME")].env}' | tr ',' '\n'


  oc debug pod/siifx-caixinhas-api-aplicacao-des-70-t2rc5 -c NOME

  oc get pods -w | grep siifx-api-aplicacao
