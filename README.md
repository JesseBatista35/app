aws eks update-kubeconfig --name eks-arc-nprd --region sa-east-1
kubectl get pods -A --request-timeout=15s | grep 4drtx


aws logs describe-log-groups --region sa-east-1 --query 'logGroups[].logGroupName' --output text | tr '\t' '\n' | grep -iE 'arc|containerinsights'
