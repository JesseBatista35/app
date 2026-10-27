oc get gateway,virtualservice -n sispi-des | grep -i med
oc get gateway gt-sispi-agendar-pix-internos-des -n sispi-des -o yaml | sed -n '/^spec:/,$p'
oc get virtualservice -n sispi-des | grep agendar-pix-internos
oc get route -A | grep sispi-agendar-pix-internos-des    # descobre em qual ns fica a rota (provavelmente istio-system)
