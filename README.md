aws sts get-caller-identity          # confirma que está na conta 027574771582
aws eks update-kubeconfig --name eks-pix-nprd --region sa-east-1
kubectl get pods -A | grep 4drtx      # descobre o namespace (normalmente arc-runners ou parecido)

POD=arc-runner-set-default-nprod-nqlwl-runner-4drtx
NS=<ns>

kubectl logs -n $NS $POD --all-containers --timestamps > ${POD}.log
kubectl describe pod -n $NS $POD > ${POD}-describe.txt

