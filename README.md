
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$ grep -nE "WFLYCTL0412|WFLYCTL0180|sirotcon|SIROTCon" /logs/jboss/jboss-eap/standalone/sigsj-intranet/server.log | tail -20
1005:    "WFLYCTL0412: Serviços necessários que não estão instalados:" => ["jboss.naming.context.java.global.\"sirotcon-ejb-2.3.0.1-farm\".\"SIROTConBean!br.gov.caixa.sirot.e                      jb.SIROTCon\""],
1006:    "WFLYCTL0180: Os serviços com falta/indisponibilidade de dependências " => ["jboss.naming.context.java.module.sigsj_intranet-ear.sigsj_intranet.env.ejb.\"caixa.sirot                      con.SIROTConEJB\" faltam [jboss.naming.context.java.global.\"sirotcon-ejb-2.3.0.1-farm\".\"SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon\"]"]
1008:2026-10-20 16:41:58,773 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 43) WFLYSRV0010: "sirotcon-ejb.jar" foi implantado (runtime-name: "sirotcon-ejb.jar")
1012:service jboss.naming.context.java.global."sirotcon-ejb-2.3.0.1-farm"."SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon" (faltam) dependentes: [service jboss.naming.context.j                      ava.module.sigsj_intranet-ear.sigsj_intranet.env.ejb."caixa.sirotcon.SIROTConEJB"]
1030:2026-10-20 16:47:32,070 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-2) WFLYSRV0028: Implantação interrompida sirotcon-ejb.jar (runtime-name: sirotcon-ej                      b.jar) em 321ms
1190:2026-10-20 16:47:42,798 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0027: Iniciando a implantação do "sirotcon-ejb.jar" (runtime-name: "sirotc                      on-ejb.jar")
1198:2026-10-20 16:47:43,753 INFO  [org.jboss.weld.deployer] (MSC service thread 1-4) WFLYWELD0003: Processando da implantação weld sirotcon-ejb.jar
1211:2026-10-20 16:47:44,253 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-4) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SIROTConBean' na un                      idade de implementação 'deployment "sirotcon-ejb.jar"' são como segue:
1213:   java:global/sirotcon-ejb/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
1214:   java:app/sirotcon-ejb/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
1215:   java:module/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
1216:   java:jboss/exported/sirotcon-ejb/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
1217:   ejb:/sirotcon-ejb/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
1218:   java:global/sirotcon-ejb/SIROTConBean
1219:   java:app/sirotcon-ejb/SIROTConBean
1220:   java:module/SIROTConBean
1242:    "WFLYCTL0412: Serviços necessários que não estão instalados:" => ["jboss.naming.context.java.global.\"sirotcon-ejb-2.3.0.1-farm\".\"SIROTConBean!br.gov.caixa.sirot.e                      jb.SIROTCon\""],
1243:    "WFLYCTL0180: Os serviços com falta/indisponibilidade de dependências " => ["jboss.naming.context.java.module.sigsj_intranet-ear.sigsj_intranet.env.ejb.\"caixa.sirot                      con.SIROTConEJB\" faltam [jboss.naming.context.java.global.\"sirotcon-ejb-2.3.0.1-farm\".\"SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon\"]"]
1245:2026-10-20 16:47:48,649 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 43) WFLYSRV0010: "sirotcon-ejb.jar" foi implantado (runtime-name: "sirotcon-ejb.jar")
1249:service jboss.naming.context.java.global."sirotcon-ejb-2.3.0.1-farm"."SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon" (faltam) dependentes: [service jboss.naming.context.j                      ava.module.sigsj_intranet-ear.sigsj_intranet.env.ejb."caixa.sirotcon.SIROTConEJB"]
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$ grep -n "java:global/sirotcon" /logs/jboss/jboss-eap/standalone/sigsj-intranet/server.log | tail -5
739:    java:global/sirotcon-ejb/SIROTConBean
971:    java:global/sirotcon-ejb/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
976:    java:global/sirotcon-ejb/SIROTConBean
1213:   java:global/sirotcon-ejb/SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon
1218:   java:global/sirotcon-ejb/SIROTConBean
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$ cd /tmp && rm -rf sirotchk && mkdir sirotchk && cd sirotchk
[p585600@caddeapllx955 sirotchk]$
[p585600@caddeapllx955 sirotchk]$
[p585600@caddeapllx955 sirotchk]$
[p585600@caddeapllx955 sirotchk]$ unzip -o -q /opt/jboss-eap/standalone/deployments/sirotcon-ejb.jar 'META-INF/*'
[p585600@caddeapllx955 sirotchk]$
[p585600@caddeapllx955 sirotchk]$
[p585600@caddeapllx955 sirotchk]$
[p585600@caddeapllx955 sirotchk]$
[p585600@caddeapllx955 sirotchk]$ grep -i "module-name" META-INF/ejb-jar.xml 2>/dev/null
cat META-INF/maven/*/*/pom.properties 2>/dev/null
ls -l /opt/jboss-eap/standalone/deployments/
total 47140
-rwxrwxr-x 1 jboss jboss     8888 jun 23  2021 README.txt
-rwxrw-rw- 1 jboss jboss 47365809 out 20 11:26 sigsj_intranet-ear.ear
-rw-r--r-- 1 jboss jboss      535 out 20 16:47 sigsj_intranet-ear.ear.failed
-rw-r--r-- 1 jboss jboss   884041 out 20 16:30 sirotcon-ejb.jar
-rw-r--r-- 1 jboss jboss       16 out 20 16:30 sirotcon-ejb.jar.deployed
[p585600@caddeapllx955 sirotchk]$
[p585600@caddeapllx955 sirotchk]$
[p585600@caddeapllx955 sirotchk]$
[p585600@caddeapllx955 sirotchk]$ exit
sair
Connection to 10.116.194.179 closed.
[p585600@cadsvitrlx100 ~]$ ssh 10.116.194.179
p585600@10.116.194.179's password:
Permission denied, please try again.
p585600@10.116.194.179's password:
^C
[p585600@cadsvitrlx100 ~]$
[p585600@cadsvitrlx100 ~]$
[p585600@cadsvitrlx100 ~]$ ssh 10.116.194.179
p585600@10.116.194.179's password:
Last failed login: Tue Oct 20 17:23:13 -03 2026 from 10.122.150.31 on ssh:notty
There was 1 failed login attempt since the last successful login.
Last login: Tue Oct 20 17:22:13 2026 from 10.122.150.31
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$ cd /opt/jboss-eap/standalone/deployments
mv sirotcon-ejb.jar sirotcon-ejb-2.3.0.1-farm.jar
rm -f sirotcon-ejb.jar.*
touch sigsj_intranet-ear.ear.dodeploy
sleep 40; ls -l | grep -E "deployed|failed"
mv: não foi possível mover 'sirotcon-ejb.jar' para 'sirotcon-ejb-2.3.0.1-farm.jar': Permissão negada
rm: não foi possível remover 'sirotcon-ejb.jar.deployed': Permissão negada
touch: não foi possível tocar 'sigsj_intranet-ear.ear.dodeploy': Permissão negada



^C
[p585600@caddeapllx955 deployments]$
[p585600@caddeapllx955 deployments]$
[p585600@caddeapllx955 deployments]$ cd /tmp && rm -rf sirotchk && mkdir sirotchk && cd sirotchk
[p585600@caddeapllx955 sirotchk]$
[p585600@caddeapllx955 sirotchk]$
[p585600@caddeapllx955 sirotchk]$
[p585600@caddeapllx955 sirotchk]$
[p585600@caddeapllx955 sirotchk]$ cd /opt/jboss-eap/standalone/deployments
mv sirotcon-ejb.jar sirotcon-ejb-2.3.0.1-farm.jar
rm -f sirotcon-ejb.jar.*
touch sigsj_intranet-ear.ear.dodeploy
sleep 40; ls -l | grep -E "deployed|failed"
mv: não foi possível mover 'sirotcon-ejb.jar' para 'sirotcon-ejb-2.3.0.1-farm.jar': Permissão negada
rm: não foi possível remover 'sirotcon-ejb.jar.deployed': Permissão negada
touch: não foi possível tocar 'sigsj_intranet-ear.ear.dodeploy': Permissão negada
^C
[p585600@caddeapllx955 deployments]$
[p585600@caddeapllx955 deployments]$
[p585600@caddeapllx955 deployments]$
[p585600@caddeapllx955 deployments]$
