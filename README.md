oc get route --all-namespaces | grep -E 'med-gestao|med-auditoria|agendar-pix-internos'
oc get route -n sispi-des | grep agendar-pix-internos     # esperado: nada (irmão sem Route direta)

  oc get route <nome> -n istio-system -o jsonpath='{.status.ingress[*].conditions}'; echo

  
