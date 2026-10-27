oc get pods -n sigcb-tqs | grep backend          # novo pod 1/1 Running, READY
oc get endpoints sigcb-backend-tqs -n sigcb-tqs  # tem que listar IP:8080

oc get events -n sigcb-tqs --sort-by=.lastTimestamp | grep -iE "182|FailedMount|FailedCreatePodSandBox|FailedAttach"
oc describe pod <pod-182> -n sigcb-tqs   # se ainda existir
