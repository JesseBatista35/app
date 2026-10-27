# Quando a injeção do OTel/Dynatrace mudou
oc get instrumentation -n sispi-des -o yaml | grep -E 'creationTimestamp|resourceVersion|image:|generation'
oc get pod $POD -n sispi-des -o jsonpath='{range .spec.initContainers[*]}{.name}{"  "}{.image}{"\n"}{end}'

# O container está estrangulado de CPU?
oc adm top pod $POD -n sispi-des --containers

# Os outros pods em CrashLoop param no mesmo ponto?
oc logs sispi-dict-batch-polling-des-735-rkrxh -n sispi-des -c sispi-dict-batch-polling-des --previous | tail -20


  oc patch dc/sispi-qrcode-api-validador-des -n sispi-des --type=json \
    -p '[{"op":"remove","path":"/spec/template/metadata/annotations/instrumentation.opentelemetry.io~1inject-java"}]'

      oc set resources dc/sispi-qrcode-api-validador-des -n sispi-des -c sispi-qrcode-api-validador-des --requests=cpu=500m
  oc set probe dc/sispi-qrcode-api-validador-des -n sispi-des -c sispi-qrcode-api-validador-des --liveness --initial-delay-seconds=240
