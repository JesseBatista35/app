~ $ 
~ $ aws eks update-kubeconfig --name eks-arc-nprd --region sa-east-1
Added new context arn:aws:eks:sa-east-1:027574771582:cluster/eks-arc-nprd to /home/cloudshell-user/.kube/config
~ $ 
~ $ 
~ $ 
~ $ 
~ $ 
~ $ 
~ $ 
~ $ 
~ $ kubectl get pods -A | grep 4drtx


^C
~ $ POD=arc-runner-set-default-nprod-nqlwl-runner-4drtx
~ $ 
