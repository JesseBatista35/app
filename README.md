POD=sispi-qrcode-api-validador-des-297-6jjtp

# Log da execução que acabou de morrer
oc logs $POD -n sispi-des -c sispi-qrcode-api-validador-des --previous | tail -300

# Motivo da morte (OOMKilled / exit code / killed by liveness)
oc get pod $POD -n sispi-des -o jsonpath='{.status.containerStatuses[?(@.name=="sispi-qrcode-api-validador-des")].lastState}{"\n"}'

# O truststore do JAVA_OPTIONS_APPEND existe na imagem?
oc exec $POD -n sispi-des -c sispi-qrcode-api-validador-des -- ls -l /deployments/

# Health por dentro do pod (rode quando o container estiver de pé há mais de ~90s)
oc exec $POD -n sispi-des -c istio-proxy -- curl -s -w '\n%{http_code}\n' localhost:8080/q/health

# Por que o deployer da 309 terminou em Error
oc logs sispi-qrcode-api-validador-des-309-deploy -n sispi-des
