# conteúdo montado no mgi
oc exec sisei-mgi-des-175-wmccw -c sisei-mgi-des -- sh -c 'ls -la /opt/app-root/src/sisei_nprd_082026.crt; cat /opt/app-root/src/sisei_nprd_082026.crt* 2>/dev/null | grep -c "BEGIN CERTIFICATE"; cat /opt/app-root/src/sisei_nprd_082026.crt* 2>/dev/null | grep -c "MIIDjjCCAnagAwIBAgIQAzrx5qcRqaC7KGSxHQn65T"'

# mesmo teste no mgi-sip (primeiro confirma o caminho)
oc set volume pod/sisei-mgi-sip-des-126-zmqxg | grep -A2 "sisei-nprd"
oc exec sisei-mgi-sip-des-126-zmqxg -c sisei-mgi-sip-des -- sh -c 'cat /opt/app-root/src/sisei_nprd_082026.crt* 2>/dev/null | grep -c "BEGIN CERTIFICATE"'

# qual arquivo o PHP usa de fato
oc exec sisei-mgi-des-175-wmccw -c sisei-mgi-des -- sh -c 'grep -iE "cafile|cainfo|capath" /etc/php.d/*.ini'

# a secret foi atualizada hoje?
oc get secrets | grep sisei-nprd
