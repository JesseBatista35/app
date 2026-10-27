
-sh-4.2$
-sh-4.2$ oc get template quarkus-caixa-release -n openshift -o yaml | grep -n -i -E 'expose-route|ISTIO|labels:'
3:labels:
15:  labels:
21:      f:labels:
33:        f:labels:
57:    labels:
72:    labels:
88:    labels:
106:    labels:
114:    labels:
134:        labels:
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get dc sispi-med-gestao-des -n sispi-des -o jsonpath='{.spec.triggers}'; echo
[]
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get gateway,virtualservice -n sispi-des 2>/dev/null | head
NAME                                                                              AGE
gateway.networking.istio.io/gt-pix-qrcode-h-des                                   2y40d
gateway.networking.istio.io/gt-sispi-agendar-pix-internos-des                     63d
gateway.networking.istio.io/gt-sispi-agrupador-frontend-des                       2y64d
gateway.networking.istio.io/gt-sispi-agrupador-frontend-des-custom                420d
gateway.networking.istio.io/gt-sispi-agrupador-frontend-des-custom-api            242d
gateway.networking.istio.io/gt-sispi-agrupador-frontend-des-esteiras-custom       241d
gateway.networking.istio.io/gt-sispi-api-consulta-chave-parceiros-des             2y137d
gateway.networking.istio.io/gt-sispi-api-consulta-chave-parceiros-des-custom      412d
gateway.networking.istio.io/gt-sispi-api-consulta-situacao-transacao-des          724d
-sh-4.2$
