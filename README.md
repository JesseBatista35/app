P=sisei-mgi-des-175-wmccw; C=sisei-mgi-des
oc exec $P -c $C -- sh -c 'grep -c "BEGIN CERTIFICATE" /opt/app-root/src/sisei_nprd.crt'
oc exec $P -c $C -- sh -c 'cd /opt/app-root/src; for f in sisei_nprd.crt sisei_nprd_082026.crt; do awk "/BEGIN/{c=\"\"} {c=c \$0} /END/{print c}" $f | sort -u > /tmp/$f.lst; done; echo "certs do antigo que NAO estao no novo:"; comm -23 /tmp/sisei_nprd.crt.lst /tmp/sisei_nprd_082026.crt.lst | wc -l'

# o mgi-sip usa o mesmo ini?
oc exec sisei-mgi-sip-des-126-zmqxg -c sisei-mgi-sip-des -- sh -c 'grep -iE "cafile|cainfo" /etc/php.d/*.ini'
oc get configmap | grep -i config-custom
