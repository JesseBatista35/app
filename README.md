cp -p /opt/jboss-eap/bin/standalone.conf /opt/jboss-eap/bin/standalone.conf.bkp_20261123
echo '' >> /opt/jboss-eap/bin/standalone.conf
echo '# SIGSJ - lib nativa SenhasSIIBC (criptografia SIPER/SIROT)' >> /opt/jboss-eap/bin/standalone.conf
echo 'JAVA_OPTS="$JAVA_OPTS -Djava.library.path=/apl/sigsj/lib"' >> /opt/jboss-eap/bin/standalone.conf

systemctl restart jboss-eap-standalone
sleep 60
ps -ef | grep -v grep | grep -o "java.library.path=[^ ]*"   # tem que mostrar /apl/sigsj/lib

grep -nE "ERROR|SenhasSIIBC|ORA-|SIROT|getResponse|Connection" /log_jboss/sigsj_internet/sigsj_internet.log | tail -20
