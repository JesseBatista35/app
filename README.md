# 1) Erro atual do EAR (deve ser o WFLYCTL0412 com sirotcon-ejb-2.3.0.1-farm)
grep -nE "WFLYCTL0412|WFLYCTL0180|sirotcon|SIROTCon" /logs/jboss/jboss-eap/standalone/sigsj-intranet/server.log | tail -20

# 2) JNDI em que o EJB foi registrado
grep -n "java:global/sirotcon" /logs/jboss/jboss-eap/standalone/sigsj-intranet/server.log | tail -5

# 3) Se o jar define module-name e qual versão ele é
cd /tmp && rm -rf sirotchk && mkdir sirotchk && cd sirotchk
unzip -o -q /opt/jboss-eap/standalone/deployments/sirotcon-ejb.jar 'META-INF/*'
grep -i "module-name" META-INF/ejb-jar.xml 2>/dev/null
cat META-INF/maven/*/*/pom.properties 2>/dev/null
ls -l /opt/jboss-eap/standalone/deployments/


cd /opt/jboss-eap/standalone/deployments
mv sirotcon-ejb.jar sirotcon-ejb-2.3.0.1-farm.jar
rm -f sirotcon-ejb.jar.* 
touch sigsj_intranet-ear.ear.dodeploy
sleep 40; ls -l | grep -E "deployed|failed"
