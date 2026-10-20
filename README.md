~ $ aws sts get-caller-identity
{
    "UserId": "AROAQM24VT57IUTFTLUWL:p585600@corp.caixa.gov.br",
    "Account": "027574771582",
    "Arn": "arn:aws:sts::027574771582:assumed-role/AWSReservedSSO_PermissionSetSupportWrite_fbad393e99cf4338/p585600@corp.caixa.gov.br"
}
~ $ aws eks update-kubeconfig --name eks-pix-nprd --region sa-east-1

aws: [ERROR]: An error occurred (ResourceNotFoundException) when calling the DescribeCluster operation: No cluster found for name: eks-pix-nprd.

Additional error details:
clusterName: eks-pix-nprd
~ $ 
~ $ 
~ $ POD=arc-runner-set-default-nprod-nqlwl-runner-4drtx
~ $ NS=<ns>
bash: syntax error near unexpected token `newline'
~ $ 
~ $ 
~ $ kubectl logs -n $NS $POD --all-containers --timestamps > ${POD}.log
error: expected 'logs [-f] [-p] (POD | TYPE/NAME) [-c CONTAINER]'.
POD or TYPE/NAME is a required argument for the logs command
See 'kubectl logs -h' for help and examples
~ $ 
~ $ 
~ $ kubectl describe pod -n $NS $POD > ${POD}-describe.txt
E1020 19:52:59.701642     231 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"http://localhost:8080/api?timeout=32s\": dial tcp 127.0.0.1:8080: connect: connection refused"
E1020 19:52:59.702053     231 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"http://localhost:8080/api?timeout=32s\": dial tcp 127.0.0.1:8080: connect: connection refused"
E1020 19:52:59.703793     231 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"http://localhost:8080/api?timeout=32s\": dial tcp 127.0.0.1:8080: connect: connection refused"
E1020 19:52:59.704219     231 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"http://localhost:8080/api?timeout=32s\": dial tcp 127.0.0.1:8080: connect: connection refused"
E1020 19:52:59.705804     231 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"http://localhost:8080/api?timeout=32s\": dial tcp 127.0.0.1:8080: connect: connection refused"
The connection to the server localhost:8080 was refused - did you specify the right host or port?
~ $ 

