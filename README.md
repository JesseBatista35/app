
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc project sisei-des
Already on project "sisei-des" on server "https://api.nprd.caixa:6443".
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get secret sisei-nprd -o yaml > backup-sisei-nprd-16102026.yaml
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc extract secret/sisei-nprd-082026 --to=. --confirm
sisei_nprd_082026.crt
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ grep -c "BEGIN CERTIFICATE" sisei_nprd_082026.crt
22
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc create secret generic sisei-nprd --from-file=sisei_nprd.crt=sisei_nprd_082026.crt --dry-run -o yaml | oc replace -f -
secret/sisei-nprd replaced
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get dc -o name | xargs -I{} sh -c 'oc set volume {} | grep -q "secret/sisei-nprd " && echo {}'
deploymentconfig.apps.openshift.io/sisei-mencache-des
deploymentconfig.apps.openshift.io/sisei-mgi-des
deploymentconfig.apps.openshift.io/sisei-mgi-mencache-des
deploymentconfig.apps.openshift.io/sisei-mgi-sip-des
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc rollout latest dc/sisei-mgi-des
deploymentconfig.apps.openshift.io/sisei-mgi-des rolled out
-sh-4.2$ oc rollout latest dc/sisei-mgi-sip-des
deploymentconfig.apps.openshift.io/sisei-mgi-sip-des rolled out
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods | grep -E "sisei-mgi(-sip)?-des-[0-9]+-[a-z0-9]{5}"
sisei-mgi-des-174-deploy           0/1       Completed           0          28h
sisei-mgi-des-175-deploy           0/1       Completed           0          15m
sisei-mgi-des-175-wmccw            2/2       Running             0          15m
sisei-mgi-des-176-4gqt4            1/2       Running             0          14s
sisei-mgi-des-176-deploy           1/1       Running             0          17s
sisei-mgi-sip-des-125-deploy       0/1       Completed           0          28h
sisei-mgi-sip-des-126-deploy       0/1       Completed           0          15m
sisei-mgi-sip-des-126-zmqxg        2/2       Running             0          14m
sisei-mgi-sip-des-127-deploy       1/1       Running             0          11s
sisei-mgi-sip-des-127-xvcns        0/2       ContainerCreating   0          8s
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ ^C
-sh-4.2$ oc exec sisei-mgi-des-176-4gqt4  -c sisei-mgi-des -- sh -c 'grep -c "BEGIN CERTIFICATE" /opt/app-root/src/sisei_nprd.crt'
22
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec sisei-mgi-sip-des-127-xvcns -c sisei-mgi-sip-des -- sh -c 'grep -c "BEGIN CERTIFICATE" /opt/app-root/src/sisei_nprd.crt'
22
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec sisei-mgi-des-176-4gqt4 -c sisei-mgi-des -- sh -c 'echo | /opt/openssl-3.6.0/bin/openssl s_client -connect <host>:443 -servername <host> -CAfile /opt/app-root/src/sisei_nprd.crt 2>/dev/null | grep "Verify return code"'
sh: host: No such file or directory
command terminated with exit code 1
-sh-4.2$
-sh-4.2$
-sh-4.2$
