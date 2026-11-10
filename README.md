# no 2863 (intranet TQS, que funciona)
unzip -l /opt/jboss-eap/standalone/deployments/sigsj_intranet-ear.ear | grep -iE 'cef|log4j|sirot'
# no 2854 (internet DES)
unzip -l /opt/jboss-eap/standalone/deployments/sigsj_internet-ear.ear | grep -iE 'cef|log4j|sirot'
