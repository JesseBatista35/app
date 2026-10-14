oc get pv | grep -i simcn
oc get pod -n simcn-tqs -o wide
oc get ns simcn-tqs -o yaml | grep 'sa.scc.uid-range'
POD_TQS=$(oc get pod -n simcn-tqs -l app=simcn-backend-tqs -o jsonpath='{.items[0].metadata.name}')
oc exec -n simcn-tqs $POD_TQS -- id
oc exec -n simcn-tqs $POD_TQS -- df -h | grep -i ifs
