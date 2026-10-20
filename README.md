aws ec2 describe-instances --region sa-east-1 \
  --filters "Name=tag:eks:cluster-name,Values=eks-arc-nprd" "Name=instance-state-name,Values=running" \
  --query 'Reservations[].Instances[].[InstanceId,PrivateDnsName]' --output table
