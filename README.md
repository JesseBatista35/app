# onde a secret do certificado está montada
oc set volume pod/sisei-mgi-des-175-wmccw | grep -i -B2 -A2 crt

# contar os certificados (troque o caminho pelo que aparecer acima)
oc exec sisei-mgi-des-175-wmccw -- sh -c 'grep -c "BEGIN CERTIFICATE" /caminho/*.crt'
oc exec sisei-mgi-sip-des-126-zmqxg -- sh -c 'grep -c "BEGIN CERTIFICATE" /caminho/*.crt'

oc exec sisei-mgi-des-175-wmccw -- sh -c 'grep -c "MIIDjjCCAnagAwIBAgIQAzrx5qcRqaC7KGSxHQn65T" /caminho/*.crt'

