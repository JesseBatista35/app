
[sudo] senha para p585600:
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]# find /opt/jboss-eap/standalone/deployments -name "*.ear" -o -name "*.war" 2>/dev/null
/opt/jboss-eap/standalone/deployments/sigsj_intranet-ear.ear
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]# grep -rl "SenhasSIIBC" /opt/jboss-eap/standalone/deployments/ 2>/dev/null
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]# ls -la /apl/sigsj/lib/ 2>/dev/null
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]# grep -n "library.path" /opt/jboss-eap/bin/standalone.conf
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]#
[root@caddeapllx955 p585600]# cd /tmp && rm -rf earx && mkdir earx && cd earx
[root@caddeapllx955 earx]#
[root@caddeapllx955 earx]#
[root@caddeapllx955 earx]#
[root@caddeapllx955 earx]# unzip -o /opt/jboss-eap/standalone/deployments/sigsj_intranet-ear.ear >/dev/null 2>&1
[root@caddeapllx955 earx]#
[root@caddeapllx955 earx]#
[root@caddeapllx955 earx]#
[root@caddeapllx955 earx]# for f in $(find . -name "*.war" -o -name "*.jar"); do d="${f}.d"; mkdir -p "$d"; unzip -o "$f" -d "$d" >/dev/null 2>&1; done
[root@caddeapllx955 earx]#
[root@caddeapllx955 earx]#
[root@caddeapllx955 earx]# grep -rl "SenhasSIIBC" . 2>/dev/null
[root@caddeapllx955 earx]# echo "--- SIROT/SIPER? ---"
--- SIROT/SIPER? ---
[root@caddeapllx955 earx]# echo "--- SIROT/SIPER? ---"
grep -rliE "sirot|siper|CONNECTOR-FARM|sendRajada" . 2>/dev/null | head
echo "--- classe da lib? ---"
--- SIROT/SIPER? ---
./META-INF/maven/br.gov.caixa/sigsj_intranet-ear/pom.xml
./META-INF/application.xml
./lib/sirotcon-ejb-lib-2.3.0.2-farm.jar
./lib/ceflib-2.5.0.1.jar
./lib/sirotcon-ejb-lib-2.3.0.2-farm.jar.d/META-INF/maven/br.gov.caixa.farm/sirotcon-ejb-lib/pom.xml
./lib/sirotcon-ejb-lib-2.3.0.2-farm.jar.d/META-INF/maven/br.gov.caixa.farm/sirotcon-ejb-lib/pom.properties
./lib/sirotcon-ejb-lib-2.3.0.2-farm.jar.d/br/gov/caixa/iso/SIROT1Message.class
./lib/sirotcon-ejb-lib-2.3.0.2-farm.jar.d/br/gov/caixa/iso/SIROTMessage.class
./lib/sirotcon-ejb-lib-2.3.0.2-farm.jar.d/br/gov/caixa/sirot/ejb/SIROTCon.class
./lib/sirotcon-ejb-lib-2.3.0.2-farm.jar.d/br/gov/caixa/sirot/transacoes/SIROTTrans.class
--- classe da lib? ---
[root@caddeapllx955 earx]#
[root@caddeapllx955 earx]#
[root@caddeapllx955 earx]#
[root@caddeapllx955 earx]# find . -iname "*SenhasSIIBC*" 2>/dev/null
[root@caddeapllx955 earx]#
