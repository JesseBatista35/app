oc project sihdg-des
oc get dc sihdg-jboss8-des -o jsonpath='{range .spec.template.spec.containers[0].volumeMounts[*]}{.name}{"\t"}{.mountPath}{"\n"}{end}'


oc get pods
oc rsh <pod-novo>
df -h | grep sihdg
