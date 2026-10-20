aws eks update-kubeconfig --name eks-arc-nprd --region sa-east-1
kubectl get pods -A --request-timeout=15s | grep 4drtx


aws logs describe-log-groups --region sa-east-1 --query 'logGroups[].logGroupName' --output text | tr '\t' '\n' | grep -iE 'arc|containerinsights'



~ $ aws logs describe-log-groups --region sa-east-1 --query 'logGroups[].logGroupName' --output text | tr '\t' '\n' | grep -iE 'arc|containerinsights'
/aws/eks/eks-arc-nprd/cluster
~ $ 


~ $ aws logs describe-log-groups --region sa-east-1 --query 'logGroups[].logGroupName' --output text | tr '\t' '\n' | grep -iE 'arc|containerinsights'
/aws/eks/eks-arc-nprd/cluster
~ $ 


~ $ aws eks update-kubeconfig --name eks-arc-nprd --region sa-east-1
Updated context arn:aws:eks:sa-east-1:027574771582:cluster/eks-arc-nprd in /home/cloudshell-user/.kube/config
~ $ kubectl get pods -A --request-timeout=15s | grep 4drtx
E1020 19:58:58.562686     309 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://A86DA1557BD7D03415CD86B8DABEDAAC.sk1.sa-east-1.eks.amazonaws.com/api?timeout=15s\": context deadline exceeded (Client.Timeout exceeded while awaiting headers)"
E1020 19:59:13.563602     309 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://A86DA1557BD7D03415CD86B8DABEDAAC.sk1.sa-east-1.eks.amazonaws.com/api?timeout=15s\": net/http: request canceled while waiting for connection (Client.Timeout exceeded while awaiting headers)"


