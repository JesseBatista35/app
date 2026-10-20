aws eks update-kubeconfig --name eks-arc-nprd --region sa-east-1
kubectl get pods -A | grep 4drtx

POD=arc-runner-set-default-nprod-nqlwl-runner-4drtx
NS=nome-do-namespace-aqui
kubectl logs -n "$NS" "$POD" --all-containers --timestamps > "$POD.log"
kubectl describe pod -n "$NS" "$POD" > "$POD-describe.txt"


kubectl get pods -A | grep arc-runner
