# a release não recriou a Route manual?  (esperado: só a linha do istio-system, com host)
oc get route --all-namespaces | grep med-gestao


curl -skI https://sispi-med-gestao-des.apps.pixnprd4.caixa/q/health/ready
curl -sk  https://sispi-med-gestao-des.apps.pixnprd4.caixa/
