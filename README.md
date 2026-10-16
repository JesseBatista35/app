
-sh-4.2$
-sh-4.2$ oc set volume pod/sisei-mgi-des-175-wmccw | grep -i -B2 -A2 crt
    mounted at /etc/secrets in container sisei-mgi-des
  secret/icptest as icptest
    mounted at /opt/app-root/src/icptest.sisei.crt in container sisei-mgi-des
    mounted at /opt/app-root/src/icptest.sisei.crt in container sisei-mgi-des-exporter
  secret/sisei-nprd as sisei-nprd
    mounted at /opt/app-root/src/sisei_nprd.crt in container sisei-mgi-des
    mounted at /opt/app-root/src/sisei_nprd.crt in container sisei-mgi-des-exporter
  pvc/sisei-mgi-data-des (allocated 50GiB) as sisei-mgi-data-des
    mounted at /sisei in container sisei-mgi-des
    mounted at /sisei in container sisei-mgi-des-exporter
  secret/sisei-nprd-082026 as sisei-nprd-082026
    mounted at /opt/app-root/src/sisei_nprd_082026.crt in container sisei-mgi-des
    mounted at /opt/app-root/src/sisei_nprd_082026.crt in container sisei-mgi-des-exporter
  configMap/config-custom-sisei-mgi as php-config-custom-sisei-mgi
    mounted at /etc/php.d/99-custom.ini in container sisei-mgi-des
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec sisei-mgi-des-175-wmccw -- sh -c 'grep -c "BEGIN CERTIFICATE" /caminho/*.crt'
Defaulting container name to sisei-mgi-des.
Use 'oc describe pod/sisei-mgi-des-175-wmccw -n sisei-des' to see all of the containers in this pod.
grep: /caminho/*.crt: No such file or directory
command terminated with exit code 2
-sh-4.2$ oc exec sisei-mgi-sip-des-126-zmqxg -- sh -c 'grep -c "BEGIN CERTIFICATE" /caminho/*.crt'
Defaulting container name to sisei-mgi-sip-des.
Use 'oc describe pod/sisei-mgi-sip-des-126-zmqxg -n sisei-des' to see all of the containers in this pod.
grep: /caminho/*.crt: No such file or directory
command terminated with exit code 2
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec sisei-mgi-des-175-wmccw -- sh -c 'grep -c "MIIDjjCCAnagAwIBAgIQAzrx5qcRqaC7KGSxHQn65T" /caminho/*.crt'
Defaulting container name to sisei-mgi-des.
Use 'oc describe pod/sisei-mgi-des-175-wmccw -n sisei-des' to see all of the containers in this pod.
grep: /caminho/*.crt: No such file or directory
command terminated with exit code 2
-sh-4.2$
