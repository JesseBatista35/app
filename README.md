# lista de segredos de cada app
for d in siifx-api-aplicacao-des siifx-caixinhas-api-aplicacao-des; do
  echo "== $d"; oc get dc $d -o jsonpath='{.spec.template.spec.initContainers[?(@.name=="secrets-agent-sidecar")].env[?(@.name=="SECRETS_LIST")].value}'; echo
done

# o que o agente do caixinhas fez no pod que subiu (tempo de cada segredo)
oc logs siifx-caixinhas-api-aplicacao-des-72-rkr7s -c secrets-agent-sidecar | grep -E 'secret path|ERROR|number of files'
