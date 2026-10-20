for r in $(aws ec2 describe-regions --query 'Regions[].RegionName' --output text); do
  c=$(aws eks list-clusters --region $r --query 'clusters' --output text 2>/dev/null)
  [ -n "$c" ] && echo "$r: $c"
done
