oc get pod siifx-api-aplicacao-des-2896-p97pn -n siifx-des \
  -o jsonpath='{range .spec.initContainers[*]}{.name}{"\n"}{end}'

# ver as variáveis do init do agente (troque <init-agente>)
oc get pod siifx-api-aplicacao-des-2896-p97pn -n siifx-des \
  -o jsonpath='{.spec.initContainers[?(@.name=="<init-agente>")].env}' | tr ',' '\n'


  oc debug pod/siifx-api-aplicacao-des-2896-p97pn -c <init-agente> -n siifx-des

  BT=https://sicsn.caixa/BeyondTrust/api/public/v3
AUTH="PS-Auth key=<APIKEY>; runas=SIFXDS05;"

# login
time curl -sk -c /tmp/c -X POST "$BT/Auth/SignAppin" -H "Authorization: $AUTH"

# o segredo que deu timeout (retorna só metadados, não o valor)
time curl -sk -b /tmp/c -H "Authorization: $AUTH" \
  "$BT/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/&title=apikey_siifx_intranet"

# os outros 4, para ver se é só esse
for t in sifxds01_oracle cli-ser-ifx_sso_intra siifx_api SIFXDS04_DATAGRID; do
  echo "== $t"; time curl -sk -b /tmp/c -m 60 -H "Authorization: $AUTH" \
    "$BT/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/&title=$t"
done

# a pasta inteira, para ver se existe título duplicado
time curl -sk -b /tmp/c -m 60 -H "Authorization: $AUTH" \
  "$BT/Secrets-Safe/Secrets?path=SIIFX_DES&separator=/"

# logout
curl -sk -b /tmp/c -X POST "$BT/Auth/Signout" -H "Authorization: $AUTH"
