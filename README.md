arc-runners_arc-runner-set-default-aws-nprod-48b8x-runner-mw85k_60157070-c70e-403e-92b1-2267ded8e10d
arc-runners_arc-runner-set-default-aws-nprod-48b8x-runner-qz8zg_88c292ae-6169-444e-bf49-b9177037972b
arc-runners_arc-runner-set-imgcustom-v1-aws-nprod-dqbd6-runner-h92pb_4567cf2f-1dd5-4a31-b568-42b14736299a
arc-systems_arc-runner-set-imgcustom-v1-aws-nprod-754b578d-listener_dfa6e390-e37f-4e6c-a3c1-162cfb71bb56

== i-0774bdd776f027699
arc-runners_arc-runner-set-default-aws-nprod-48b8x-runner-6dtd9_2676c408-8496-4c2b-8809-c57370ad25a3
arc-runners_arc-runner-set-imgcustom-v1-aws-nprod-dqbd6-runner-v5jsd_10306e7d-09dd-40be-9475-8953aee16714
arc-systems_arc-runner-set-default-aws-nprod-754b578d-listener_8326f0e6-7bff-476a-98fe-32ba4fe0f022

~ $ aws rosa list-clusters --region sa-east-1 2>/dev/null
~ $ aws ec2 describe-instances --region sa-east-1 --filters "Name=instance-state-name,Values=running" \
>   --query 'Reservations[].Instances[].Tags[?Key==`Name`].Value[]' --output text | tr '\t' '\n' | sort -u
eks-arc-runners
jumper-devops-instance
~ $ for r in $(aws ec2 describe-regions --query 'Regions[].RegionName' --output text); do
>   c=$(aws eks list-clusters --region $r --query 'clusters' --output text 2>/dev/null)
>   [ -n "$c" ] && echo "$r: $c"
> done

sa-east-1: eks-arc-nprd
~ $ 
~ $ 
