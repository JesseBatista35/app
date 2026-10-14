IMG=$(oc get dc siifx-api-aplicacao-des -o jsonpath='{.spec.template.spec.initContainers[?(@.name=="secrets-agent-sidecar")].image}')
S=bt-client-secret-siifx-api-aplicacao-des
CID=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_ID}' | base64 -d)
CSEC=$(oc get secret $S -o jsonpath='{.data.BT_CLIENT_SECRET}' | base64 -d)
oc run bt-test --rm -it --restart=Never --image="$IMG" --env="CID=$CID" --env="CSEC=$CSEC" --command -- sh

exit

unset CID CSEC
