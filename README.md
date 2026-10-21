
[root@caddeapllx2557 bolchk]# grep -nE "log4j|FileNotFound|Exception:|log_jboss|Caused by" /logs/jboss/jboss-eap/standalone/sigsj-boleto/server.log | tail -15
1088:Caused by: org.jboss.msc.service.DuplicateServiceException: Service jboss.naming.context.java.global."sirotcon-ejb-2.3.0.1-farm"."SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon" is already registered
1101:2026-10-21 16:07:53,576 ERROR [stderr] (ServerService Thread Pool -- 81) log4j:ERROR Could not parse file [/log_jboss/config-log4j/sigsj_ws_boleto.xml].
1102:2026-10-21 16:07:53,576 ERROR [stderr] (ServerService Thread Pool -- 81) java.io.FileNotFoundException: /log_jboss/config-log4j/sigsj_ws_boleto.xml (Arquivo ou diretório inexistente)
1117:2026-10-21 16:07:53,582 ERROR [stderr] (ServerService Thread Pool -- 81)   at org.apache.log4j.xml.DOMConfigurator$1.parse(DOMConfigurator.java:730)
1118:2026-10-21 16:07:53,582 ERROR [stderr] (ServerService Thread Pool -- 81)   at org.apache.log4j.xml.DOMConfigurator.doConfigure(DOMConfigurator.java:854)
1119:2026-10-21 16:07:53,583 ERROR [stderr] (ServerService Thread Pool -- 81)   at org.apache.log4j.xml.DOMConfigurator.doConfigure(DOMConfigurator.java:737)
1120:2026-10-21 16:07:53,583 ERROR [stderr] (ServerService Thread Pool -- 81)   at org.apache.log4j.xml.DOMConfigurator.configure(DOMConfigurator.java:879)
1152:    Caused by: org.jboss.as.server.deployment.DeploymentUnitProcessingException: WFLYEE0052: Falha ao instalar o componente SIROTConBean
1153:    Caused by: org.jboss.msc.service.DuplicateServiceException: Service jboss.naming.context.java.global.\"sirotcon-ejb-2.3.0.1-farm\".\"SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon\" is already registered"},
1403:2026-10-21 16:53:18,732 ERROR [stderr] (ServerService Thread Pool -- 74) log4j:ERROR Could not parse file [/log_jboss/config-log4j/sigsj_ws_boleto.xml].
1404:2026-10-21 16:53:18,732 ERROR [stderr] (ServerService Thread Pool -- 74) java.io.FileNotFoundException: /log_jboss/config-log4j/sigsj_ws_boleto.xml (Arquivo ou diretório inexistente)
1419:2026-10-21 16:53:18,733 ERROR [stderr] (ServerService Thread Pool -- 74)   at org.apache.log4j.xml.DOMConfigurator$1.parse(DOMConfigurator.java:730)
1420:2026-10-21 16:53:18,733 ERROR [stderr] (ServerService Thread Pool -- 74)   at org.apache.log4j.xml.DOMConfigurator.doConfigure(DOMConfigurator.java:854)
1421:2026-10-21 16:53:18,733 ERROR [stderr] (ServerService Thread Pool -- 74)   at org.apache.log4j.xml.DOMConfigurator.doConfigure(DOMConfigurator.java:737)
1422:2026-10-21 16:53:18,733 ERROR [stderr] (ServerService Thread Pool -- 74)   at org.apache.log4j.xml.DOMConfigurator.configure(DOMConfigurator.java:879)
[root@caddeapllx2557 bolchk]#
