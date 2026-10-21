oc get pod sigsj-alvara-des-702-m5bvt -o jsonpath='{.spec.containers[*].image}{"\n"}'
oc get rc | grep sigsj-alvara-des-
oc get rc sigsj-alvara-des-693 -o jsonpath='{.spec.template.spec.containers[*].image}{"\n"}'
oc get rc sigsj-alvara-des-701 -o jsonpath='{.spec.template.spec.containers[*].image}{"\n"}'


oc logs sigsj-alvara-des-702-m5bvt | head -40          # procurar "started in X.XXXs"
oc get dc sigsj-alvara-des -o yaml | grep -B2 -A12 -E 'readinessProbe|livenessProbe|timeoutSeconds'

oc get events --sort-by=.metadata.creationTimestamp | grep -i alvara
