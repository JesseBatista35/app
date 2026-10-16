-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec $P -c $C -- sh -c 'grep -c "BEGIN CERTIFICATE" /opt/app-root/src/sisei_nprd.crt'
error: expected 'exec POD_NAME COMMAND [ARG1] [ARG2] ... [ARGN]'.
POD_NAME and COMMAND are required arguments for the exec command
See 'oc exec -h' for help and examples.
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec $P -c $C -- sh -c 'cd /opt/app-root/src; for f in sisei_nprd.crt sisei_nprd_082026.crt; do awk "/BEGIN/{c=\"\"} {c=c \$0} /END/{print c}" $f | sort -u > /tmp/$f.lst; done; echo "certs do antigo que NAO estao no novo:"; comm -23 /tmp/sisei_nprd.crt.lst
> /tmp/sisei_nprd_082026.crt.lst | wc -l'
error: expected 'exec POD_NAME COMMAND [ARG1] [ARG2] ... [ARGN]'.
POD_NAME and COMMAND are required arguments for the exec command
See 'oc exec -h' for help and examples.
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec sisei-mgi-sip-des-126-zmqxg -c sisei-mgi-sip-des -- sh -c 'grep -iE "cafile|cainfo" /etc/php.d/*.ini'
/etc/php.d/99-custom.ini:curl.cainfo="/opt/app-root/src/sisei_nprd.crt"
/etc/php.d/99-custom.ini:openssl.cafile="/opt/app-root/src/sisei_nprd.crt"
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get configmap | grep -i config-custom
config-custom-sisei           3         253d
config-custom-sisei-mgi       3         8m38s
config-custom-sisei-mgi-sip   3         8m7s
config-custom-sisei-sip       3         253d
-sh-4.2$
