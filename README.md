oc get pods -n sispi-des -l deploymentconfig=sispi-qrcode-api-validador-des -o wide
oc get rc -n sispi-des | grep sispi-qrcode-api-validador

POD=<nome-do-pod>

oc logs $POD -n sispi-des -c sispi-qrcode-api-validador-des --previous | tail -300
# se der "previous terminated container not found", tire o --previous

oc get pod $POD -n sispi-des -o jsonpath='{.status.containerStatuses[?(@.name=="sispi-qrcode-api-validador-des")].lastState}{"\n"}'

oc exec $POD -n sispi-des -c sispi-qrcode-api-validador-des -- ls -l /deployments/
