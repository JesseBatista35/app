
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec sisei-mgi-des-175-wmccw -c sisei-mgi-des -- sh -c 'ls -la /opt/app-root/src/sisei_nprd_082026.crt; cat /opt/app-root/src/sisei_nprd_082026.crt* 2>/dev/null | grep -c "BEGIN CERTIFICATE"; cat /opt/app-root/src/sisei_nprd_082026.crt* 2>/dev/null | grep -c "MIIDjjCCAnagAwIBAgIQAzrx5qcRqaC7KGSxHQn65T"'
-rw-r--r--. 1 root root 41868 out 16 16:34 /opt/app-root/src/sisei_nprd_082026.crt
22
1
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc set volume pod/sisei-mgi-sip-des-126-zmqxg | grep -A2 "sisei-nprd"
  secret/sisei-nprd as sisei-nprd
    mounted at /opt/app-root/src/sisei_nprd.crt in container sisei-mgi-sip-des
    mounted at /opt/app-root/src/sisei_nprd.crt in container sisei-mgi-sip-des-exporter
--
  secret/sisei-nprd-082026 as sisei-nprd-082026
    mounted at /opt/app-root/src/sisei_nprd_082026.crt in container sisei-mgi-sip-des
    mounted at /opt/app-root/src/sisei_nprd_082026.crt in container sisei-mgi-sip-des-exporter
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec sisei-mgi-sip-des-126-zmqxg -c sisei-mgi-sip-des -- sh -c 'cat /opt/app-root/src/sisei_nprd_082026.crt* 2>/dev/null | grep -c "BEGIN CERTIFICATE"'
22
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec sisei-mgi-des-175-wmccw -c sisei-mgi-des -- sh -c 'grep -iE "cafile|cainfo|capath" /etc/php.d/*.ini'
]/etc/php.d/99-custom.ini:curl.cainfo="/opt/app-root/src/sisei_nprd.crt"
/etc/php.d/99-custom.ini:openssl.cafile="/opt/app-root/src/sisei_nprd.crt"
-sh-4.2$ ]
-sh: ]: comando não encontrado
-sh-4.2$
-sh-4.2$ oc get secrets | grep sisei-nprd
sisei-nprd                            Opaque                                1         67d
sisei-nprd-082026                     Opaque                                1         6m
-sh-4.2$



pronto fopi né


ja atualize o dolwosd secure file de tqs nao vou rodar a relase de tqs
