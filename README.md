
[root@caddeapllx2854 deployments]#
[root@caddeapllx2854 deployments]# ls /opt/jboss-eap/standalone/deployments/
ojdbc8.jar  ojdbc8.jar.deployed  README.txt  sigsj_internet-ear.ear  sigsj_internet-ear.ear.failed
[root@caddeapllx2854 deployments]#
[root@caddeapllx2854 deployments]#
[root@caddeapllx2854 deployments]#



[root@caddeapllx2854 deployments]# grep -E 'WFLYUT0021|WFLYSRV0010|WFLYEE0047|NumberFormatException|ClassNotFound' /logs/jboss/jboss-eap/standalone/sigsj-internet/server.log | tail -10
Caused by: java.lang.ClassNotFoundException: br.gov.caixa.log.Log from [Module "deployment.sigsj_internet-ear.ear.br.gov.caixa.farm-sirotcon-ejb-2.3.0.2-farm.jar" from Service Module Loader]
    Caused by: java.lang.ClassNotFoundException: br.gov.caixa.log.Log from [Module \"deployment.sigsj_internet-ear.ear.br.gov.caixa.farm-sirotcon-ejb-2.3.0.2-farm.jar\" from Service Module Loader]"},
Caused by: java.lang.ClassNotFoundException: br.gov.caixa.log.Log from [Module "deployment.sigsj_internet-ear.ear.br.gov.caixa.farm-sirotcon-ejb-2.3.0.2-farm.jar" from Service Module Loader]
    Caused by: java.lang.ClassNotFoundException: br.gov.caixa.log.Log from [Module \"deployment.sigsj_internet-ear.ear.br.gov.caixa.farm-sirotcon-ejb-2.3.0.2-farm.jar\" from Service Module Loader]"},
2026-11-10 14:58:42,313 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 43) WFLYSRV0010: "ojdbc8.jar" foi implantado (runtime-name: "ojdbc8.jar")
2026-11-10 14:58:42,313 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 43) WFLYSRV0010: "sigsj_internet-ear.ear" foi implantado (runtime-name: "sigsj_internet-ear.ear")
Caused by: java.lang.ClassNotFoundException: br.gov.caixa.log.Log from [Module "deployment.sigsj_internet-ear.ear.br.gov.caixa.farm-sirotcon-ejb-2.3.0.2-farm.jar" from Service Module Loader]
    Caused by: java.lang.ClassNotFoundException: br.gov.caixa.log.Log from [Module \"deployment.sigsj_internet-ear.ear.br.gov.caixa.farm-sirotcon-ejb-2.3.0.2-farm.jar\" from Service Module Loader]"},
2026-11-10 15:04:33,722 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 43) WFLYSRV0010: "ojdbc8.jar" foi implantado (runtime-name: "ojdbc8.jar")
2026-11-10 15:04:33,722 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 43) WFLYSRV0010: "sigsj_internet-ear.ear" foi implantado (runtime-name: "sigsj_internet-ear.ear")
[root@caddeapllx2854 deployments]#
