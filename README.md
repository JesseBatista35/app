CMD=$(aws ssm send-command --region sa-east-1 \
  --instance-ids i-039ba2dcec5242374 i-0774bdd776f027699 \
  --document-name AWS-RunShellScript \
  --parameters 'commands=["ls -d /var/log/pods/*4drtx* 2>/dev/null || echo NAO_ENCONTRADO"]' \
  --query 'Command.CommandId' --output text)
sleep 5
for i in i-039ba2dcec5242374 i-0774bdd776f027699; do
  echo "== $i"
  aws ssm get-command-invocation --region sa-east-1 --command-id "$CMD" --instance-id $i \
    --query 'StandardOutputContent' --output text
done



aws ssm start-session --region sa-east-1 --target i-XXXXXXXXXXXXX
