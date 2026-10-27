# 1. Backup das rotas manuais
oc get route sispi-med-gestao-des -n sispi-des -o yaml > route-med-gestao-sispi-des.bkp.yaml
oc get route sispi-med-auditoria-des -n sispi-des -o yaml > route-med-auditoria-sispi-des.bkp.yaml

# 2. Remover as rotas manuais (só as Routes; o Service fica, o VirtualService usa ele)
oc delete route sispi-med-gestao-des -n sispi-des
oc delete route sispi-med-auditoria-des -n sispi-des

# 3. Conferir se as rotas do istio-system foram admitidas
oc get route sispi-med-gestao-des -n istio-system -o jsonpath='{.status.ingress[*].conditions}'; echo
oc get route sispi-med-auditoria-des -n istio-system -o jsonpath='{.status.ingress[*].conditions}'; echo


curl -skI https://sispi-med-gestao-des.apps.pixnprd4.caixa/q/health/ready
curl -skI https://sispi-med-auditoria-des.apps.pixnprd4.caixa/q/health/ready

