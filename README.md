oc get template quarkus-caixa-release -n openshift -o yaml | grep -n -i -E 'expose-route|ISTIO|labels:' 
oc get dc sispi-med-gestao-des -n sispi-des -o jsonpath='{.spec.triggers}'; echo

oc get gateway,virtualservice -n sispi-des 2>/dev/null | head
