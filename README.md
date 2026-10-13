oc logs sinfs-des-80-zlj8m -n sinfs-des -c secrets-agent-sidecar | grep -E "secret path|UserName|number of files|ERROR"

oc get dc/sinfs-des -n sinfs-des -o jsonpath='{range .spec.template.spec.initContainers[0].env[*]}{.name}{" -> "}{.valueFrom}{"\n"}{end}'
oc get dc/sinfs-des -n sinfs-des -o jsonpath='{.spec.template.spec.initContainers[0].envFrom}{"\n"}'
