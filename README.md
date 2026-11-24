NS=sigec-tqs
POD=sigec-csc-frontend-tqs-83-rvzvp

# 1. qual é o 2º container do pod (está 2/2)
oc get pod $POD -n $NS -o jsonpath='{.spec.containers[*].name}'; echo

# 2. 504 e erros de upstream no log do nginx
oc logs -n $NS $POD -c sigec-csc-frontend-tqs --since=168h | grep -E '" 504 |upstream' | tail -20

# 3. para onde resolve o backend e quem responde (header Server/Via)
oc rsh -n $NS -c sigec-csc-frontend-tqs $POD sh -c 'getent hosts sigec-csc.esteiras.tqs.caixa; curl -skI https://sigec-csc.esteiras.tqs.caixa/csc-api/ | head -15'
