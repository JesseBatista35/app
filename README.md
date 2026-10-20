~ $ 
~ $ 
~ $ 
~ $ aws eks describe-cluster --name eks-arc-nprd --region sa-east-1 \
>   --query 'cluster.resourcesVpcConfig.{publico:endpointPublicAccess,privado:endpointPrivateAccess,cidrs:publicAccessCidrs,vpc:vpcId,subnets:subnetIds,sgs:clusterSecurityGroupId}'
{
    "publico": false,
    "privado": true,
    "cidrs": [
        "0.0.0.0/0"
    ],
    "vpc": "vpc-0b04261c457bfcd0c",
    "subnets": [
        "subnet-014be534b7f3812ae",
        "subnet-0b4b364ddbac61173"
    ],
    "sgs": "sg-0e95bc99eb513af77"
}
~ $ 
~ $ 
~ $ 
~ $ 
~ $ kubectl get ns --request-timeout=10s
E1020 19:56:49.486078     263 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://A86DA1557BD7D03415CD86B8DABEDAAC.sk1.sa-east-1.eks.amazonaws.com/api?timeout=10s\": context deadline exceeded (Client.Timeout exceeded while awaiting headers)"
E1020 19:56:59.488514     263 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://A86DA1557BD7D03415CD86B8DABEDAAC.sk1.sa-east-1.eks.amazonaws.com/api?timeout=10s\": context deadline exceeded (Client.Timeout exceeded while awaiting headers)"
E1020 19:57:09.488936     263 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://A86DA1557BD7D03415CD86B8DABEDAAC.sk1.sa-east-1.eks.amazonaws.com/api?timeout=10s\": net/http: request canceled while waiting for connection (Client.Timeout exceeded while awaiting headers)"
E1020 19:57:19.489664     263 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://A86DA1557BD7D03415CD86B8DABEDAAC.sk1.sa-east-1.eks.amazonaws.com/api?timeout=10s\": context deadline exceeded (Client.Timeout exceeded while awaiting headers)"
E1020 19:57:29.490279     263 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://A86DA1557BD7D03415CD86B8DABEDAAC.sk1.sa-east-1.eks.amazonaws.com/api?timeout=10s\": context deadline exceeded"
Unable to connect to the server: context deadline exceeded
~ $ 
