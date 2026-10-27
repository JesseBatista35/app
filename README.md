
-sh-4.2$ oc get route --all-namespaces | grep -E 'med-gestao|med-auditoria|agendar-pix-internos'
istio-system                         sispi-agendar-pix-internos-des                                              sispi-agendar-pix-internos-des.apps.pixnprd4.caixa                                    istio-ingressgateway                              http2             edge/Allow             None
istio-system                         sispi-med-auditoria-des                                                     HostAlreadyClaimed                                                                    istio-ingressgateway                              http2             edge/Allow             None
istio-system                         sispi-med-gestao-des                                                        HostAlreadyClaimed                                                                    istio-ingressgateway                              http2             edge/Allow             None
sispi-des                            sispi-med-auditoria-des                                                     sispi-med-auditoria-des.apps.pixnprd4.caixa                                           sispi-med-auditoria-des                           web               edge/Redirect          None
sispi-des                            sispi-med-gestao-des                                                        sispi-med-gestao-des.apps.pixnprd4.caixa                                              sispi-med-gestao-des                              web               edge/Redirect          None
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get route -n sispi-des | grep agendar-pix-internos
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get route <nome> -n istio-system -o jsonpath='{.status.ingress[*].conditions}'; echo
-sh: nome: Arquivo ou diretório não encontrado

-sh-4.2$
