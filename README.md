# 1. Pod está Ready?  (esperado 1/1; se 0/1, é readiness)
oc get pod -n sispi-des -l name=sispi-med-gestao-des -o wide

# 2. Motivo da readiness falhando
oc describe pod sispi-med-gestao-des-21-k7cws -n sispi-des | grep -iE -A3 'readiness|liveness|warning'

# 3. Service tem endpoint? (vazio = nenhum pod pronto OU selector errado)
oc get endpoints sispi-med-gestao-des -n sispi-des
oc get svc sispi-med-gestao-des -n sispi-des -o yaml | grep -A6 -E 'selector|ports'

# 4. Route aponta pro Service/porta certos?
oc get route -n sispi-des | grep med-gestao
oc get route sispi-med-gestao-des -n sispi-des -o yaml | grep -A4 -E '^  to:|port:|tls:'

# 5. Ver o health por dentro (mostra qual check está DOWN)
oc port-forward pod/sispi-med-gestao-des-21-k7cws 18080:8080 -n sispi-des &
curl -s localhost:18080/q/health/ready | jq .
