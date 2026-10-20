aws rosa list-clusters --region sa-east-1 2>/dev/null
aws ec2 describe-instances --region sa-east-1 --filters "Name=instance-state-name,Values=running" \
  --query 'Reservations[].Instances[].Tags[?Key==`Name`].Value[]' --output text | tr '\t' '\n' | sort -u
