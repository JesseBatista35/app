# nomes dos init containers
oc get pod sinfs-des-80-zlj8m -n sinfs-des -o jsonpath='{.spec.initContainers[*].name}{"\n"}'

# log do agent (troque pelo nome que aparecer, provavelmente o que vem antes do secrets-check)
oc logs sinfs-des-80-zlj8m -n sinfs-des -c <init-do-agent> | grep -E "secret path|UserName|number of files|ERROR"

for ns in sinfs-des sinfs-tqs; do
  echo "== $ns"
  oc get dc/${ns} -n $ns -o jsonpath='{range .spec.template.spec.initContainers[*]}{.name}{"\n"}{range .env[*]}{"  "}{.name}={.value}{"\n"}{end}{end}' \
    | grep -viE 'senha|password|key'
done

