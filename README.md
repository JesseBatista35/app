
# pod mais recente do SIIFX-api-aplicacao
POD=$(oc get pod -l name=siifx-api-aplicacao-des --sort-by=.metadata.creationTimestamp -o name | tail -1); echo $POD

# log do agente BeyondTrust nesse pod
oc logs $POD -c secrets-agent-sidecar | grep -E 'secret path|ERROR|UserName|sign_app'

# variáveis do agente, lidas do DC (não depende de pod)
oc get dc siifx-api-aplicacao-des -o jsonpath='{range .spec.template.spec.initContainers[?(@.name=="secrets-agent-sidecar")].env[*]}{.name}={.value}{.valueFrom}{"\n"}{end}'

# mesma coisa do caixinhas, para comparar usuário e lista de segredos
oc get dc siifx-caixinhas-api-aplicacao-des -o jsonpath='{range .spec.template.spec.initContainers[?(@.name=="secrets-agent-sidecar")].env[*]}{.name}={.value}{.valueFrom}{"\n"}{end}'


oc logs $POD -c secrets-agent-sidecar --previous | grep -E 'secret path|ERROR|UserName|sign_app'
