oc project sisei-des
oc get secret sisei-nprd -o yaml > backup-sisei-nprd-16102026.yaml        # backup
oc extract secret/sisei-nprd-082026 --to=. --confirm                        # baixa o bundle novo (22)
grep -c "BEGIN CERTIFICATE" sisei_nprd_082026.crt                          # 22
oc create secret generic sisei-nprd --from-file=sisei_nprd.crt=sisei_nprd_082026.crt --dry-run -o yaml | oc replace -f -

oc get dc -o name | xargs -I{} sh -c 'oc set volume {} | grep -q "secret/sisei-nprd " && echo {}'



oc rollout latest dc/sisei-mgi-des
oc rollout latest dc/sisei-mgi-sip-des

oc get pods | grep -E "sisei-mgi(-sip)?-des-[0-9]+-[a-z0-9]{5}"
oc exec <pod-mgi> -c sisei-mgi-des -- sh -c 'grep -c "BEGIN CERTIFICATE" /opt/app-root/src/sisei_nprd.crt'          # 22
oc exec <pod-sip> -c sisei-mgi-sip-des -- sh -c 'grep -c "BEGIN CERTIFICATE" /opt/app-root/src/sisei_nprd.crt'       # 22

oc exec <pod-mgi> -c sisei-mgi-des -- sh -c 'echo | /opt/openssl-3.6.0/bin/openssl s_client -connect <host>:443 -servername <host> -CAfile /opt/app-root/src/sisei_nprd.crt 2>/dev/null | grep "Verify return code"'

