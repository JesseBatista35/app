aws eks describe-cluster --name eks-arc-nprd --region sa-east-1 \
  --query 'cluster.resourcesVpcConfig.{publico:endpointPublicAccess,privado:endpointPrivateAccess,cidrs:publicAccessCidrs,vpc:vpcId,subnets:subnetIds,sgs:clusterSecurityGroupId}'

  kubectl get ns --request-timeout=10s
