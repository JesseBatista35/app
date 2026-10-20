~ $ 
~ $ 
~ $ 
~ $ 
~ $ aws ec2 describe-instances --region sa-east-1 \
>   --filters "Name=tag:eks:cluster-name,Values=eks-arc-nprd" "Name=instance-state-name,Values=running" \
>   --query 'Reservations[].Instances[].[InstanceId,PrivateDnsName]' --output table
------------------------------------------------------------------------
|                           DescribeInstances                          |
+----------------------+-----------------------------------------------+
|  i-039ba2dcec5242374 |  ip-10-249-30-191.sa-east-1.compute.internal  |
|  i-0774bdd776f027699 |  ip-10-249-28-123.sa-east-1.compute.internal  |
+----------------------+-----------------------------------------------+
~ $ 
