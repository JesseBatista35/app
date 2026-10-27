oc rollout history dc/sispi-qrcode-api-validador-des -n sispi-des --revision=312 | grep -E 'Image|inject|cpu|Liveness|JAVA_'


POD=sispi-qrcode-api-validador-des-312-mthvm

# 1. Onde a main está presa
oc exec $POD -n sispi-des -c sispi-qrcode-api-validador-des -- jcmd 1 Thread.print > /tmp/td-312.txt 2>&1
head -5 /tmp/td-312.txt; grep -A 30 '"main"' /tmp/td-312.txt

# 2. O Dynatrace está injetado?
oc exec $POD -n sispi-des -c sispi-qrcode-api-validador-des -- env | grep -E 'LD_PRELOAD|DT_'
oc get pod $POD -n sispi-des -o jsonpath='{.metadata.annotations}' | tr ',' '\n' | grep -i dynatrace

# 3. O Dynatrace já existia num pod antigo que está saudável?
oc get pod sispi-api-fabrica-ids-des-37-cv5d8 -n sispi-des -o jsonpath='{range .spec.initContainers[*]}{.name}{"\n"}{end}'

# A) sem Dynatrace
oc patch dc/sispi-qrcode-api-validador-des -n sispi-des --type=merge \
  -p '{"spec":{"template":{"metadata":{"annotations":{"oneagent.dynatrace.com/inject":"false"}}}}}'

# B) sem Elastic APM (só se o A não resolver)
oc set env dc/sispi-qrcode-api-validador-des -n sispi-des -c sispi-qrcode-api-validador-des JAVA_OPTS_MONITORING-


