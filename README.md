# policies da malha no namespace
oc get networkpolicy -n sispi-des
oc get networkpolicy -n sispi-des -o yaml | grep -B2 -A8 expose-route

# comparar labels com um irmão que funciona
oc get pod -n sispi-des -l name=sispi-med-auditoria-des --show-labels
oc get pod sispi-med-gestao-des-22-ckdkt -n sispi-des --show-labels


curl -skI https://sispi-med-auditoria-des.apps.pixnprd4.caixa/q/health/ready

oc label pod sispi-med-gestao-des-22-ckdkt -n sispi-des maistra.io/expose-route=true
curl -skI https://sispi-med-gestao-des.apps.pixnprd4.caixa/q/health/ready   # do Windows

oc patch dc sispi-med-gestao-des -n sispi-des --type merge \
  -p '{"spec":{"template":{"metadata":{"labels":{"maistra.io/expose-route":"true"}}}}}'
