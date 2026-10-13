
-sh-4.2$
-sh-4.2$ oc get pod sinfs-des-80-zlj8m -n sinfs-des -o jsonpath='{.spec.initContainers[*].name}{"\n"}'
secrets-agent-sidecar secrets-check
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc logs sinfs-des-80-zlj8m -n sinfs-des -c <init-do-agent> | grep -E "secret path|UserName|number of files|ERROR"
-sh: erro de sintaxe próximo do `token' não esperado `|'
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ for ns in sinfs-des sinfs-tqs; do
>   echo "== $ns"
>   oc get dc/${ns} -n $ns -o jsonpath='{range .spec.template.spec.initContainers[*]}{.name}{"\n"}{range .env[*]}{"  "}{.name}={.value}{"\n"}{end}{end}' \
>     | grep -viE 'senha|password|key'
> done
== sinfs-des
secrets-agent-sidecar
  SECRETS_PATH=/usr/src/app/secrets_files
  BT_API_URL=https://sicsn.caixa/BeyondTrust/api/public/v3
  CLIENT_ID=
  CLIENT_SECRET=
  BT_API_VERSION=3.1
  BT_VERIFY_CA=False
secrets-check
  SECRETS_PATH=/usr/src/app/secrets_files
== sinfs-tqs
secrets-agent-sidecar
  SECRETS_PATH=/usr/src/app/secrets_files
  BT_API_URL=https://sicsn.caixa/BeyondTrust/api/public/v3
  CLIENT_ID=
  CLIENT_SECRET=
  BT_API_VERSION=3.1
  BT_VERIFY_CA=False
secrets-check
  SECRETS_PATH=/usr/src/app/secrets_files
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
