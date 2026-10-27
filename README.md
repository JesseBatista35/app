curl -skI https://sispi-med-gestao-des.apps.pixnprd4.caixa/q/health/ready
curl -skI http://sispi-med-gestao-des.apps.pixnprd4.caixa/q/health/ready   # esperado 302 -> https


oc get route sispi-med-gestao-des -n sispi-des -o jsonpath='{.status.ingress[*].conditions}'; echo
oc get peerauthentication -n sispi-des
oc get route sispi-med-auditoria-des -n sispi-des -o yaml | grep -A4 -E '^  to:|port:|tls:'   # comparar com um irmão que funciona
