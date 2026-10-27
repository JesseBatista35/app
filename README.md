# Log da última execução que morreu
oc logs sispi-qrcode-api-validador-des-297-fs9kn -n sispi-des \
  -c sispi-qrcode-api-validador-des --previous | tail -300

# Motivo da última morte: exit code 137/OOMKilled ou kill por liveness
oc get pod sispi-qrcode-api-validador-des-297-fs9kn -n sispi-des \
  -o jsonpath='{.status.containerStatuses[?(@.name=="sispi-qrcode-api-validador-des")].lastState}{"\n"}'

# Health por dentro do pod. O istio-proxy compartilha a rede e costuma ter curl
oc exec sispi-qrcode-api-validador-des-297-fs9kn -n sispi-des -c istio-proxy -- \
  curl -s -w '\n%{http_code}\n' localhost:8080/q/health

# Diferenças entre o que funcionava e o que a pipeline está aplicando
oc rollout history dc/sispi-qrcode-api-validador-des -n sispi-des --revision=309
