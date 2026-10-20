
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$ LOG=/logs/jboss/jboss-eap/standalone/sigsj-intranet/server.log
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$ ls -la $LOG /opt/jboss-eap/standalone/log/server.log
-rw-r--r-- 1 jboss jboss 41742 out 20 15:48 /logs/jboss/jboss-eap/standalone/sigsj-intranet/server.log
-rw-r--r-- 1 jboss jboss 55743 out 20 15:27 /opt/jboss-eap/standalone/log/server.log
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$
[p585600@caddeapllx955 ~]$ grep -nE "WFLYCTL0013|WFLYCTL0412|WFLYCTL0180|ERROR|Caused by" $LOG | tail -40
36:2026-10-20 15:27:52,215 ERROR [org.jboss.as.controller.management-operation] (Controller Boot Thread) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "sigsj_intranet-ear.ear")]) - falha na descrição: {
37:    "WFLYCTL0412: Serviços necessários que não estão instalados:" => ["jboss.naming.context.java.global.\"sirotcon-ejb-2.3.0.1-farm\".\"SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon\""],
38:    "WFLYCTL0180: Os serviços com falta/indisponibilidade de dependências " => ["jboss.naming.context.java.module.sigsj_intranet-ear.sigsj_intranet.env.ejb.\"caixa.sirotcon.SIROTConEJB\" faltam [jboss.naming.context.java.global.\"sirotcon-ejb-2.3.0.1-farm\".\"SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon\"]"]
46:2026-10-20 15:27:52,354 ERROR [org.jboss.as] (Controller Boot Thread) WFLYSRV0026: JBoss EAP 7.4.18.GA (WildFly Core 15.0.37.Final-redhat-00001) iniciado (com erros) em 8977ms - Iniciado(s) 1568 de serviços 2150 (377 serviços falharam ou tinham dependências ausentes, os serviços 364 estão lentos, passivos ou sob demanda)
49:2026-10-20 15:27:56,264 ERROR [org.jboss.modcluster] (UndertowEventHandlerAdapterService - 1) MODCLUSTER000043: Failed to send INFO command to localhost/127.0.0.1:6666: Conexão recusada (Connection refused)
85:     co.elastic.apm.agent.shaded.slf4j.simpleLogger.log.co.elastic.apm = ERROR
255:2026-10-20 15:33:43,177 ERROR [org.jboss.as.controller.management-operation] (Controller Boot Thread) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "sigsj_intranet-ear.ear")]) - falha na descrição: {
256:    "WFLYCTL0412: Serviços necessários que não estão instalados:" => ["jboss.naming.context.java.global.\"sirotcon-ejb-2.3.0.1-farm\".\"SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon\""],
257:    "WFLYCTL0180: Os serviços com falta/indisponibilidade de dependências " => ["jboss.naming.context.java.module.sigsj_intranet-ear.sigsj_intranet.env.ejb.\"caixa.sirotcon.SIROTConEJB\" faltam [jboss.naming.context.java.global.\"sirotcon-ejb-2.3.0.1-farm\".\"SIROTConBean!br.gov.caixa.sirot.ejb.SIROTCon\"]"]
265:2026-10-20 15:33:43,277 ERROR [org.jboss.as] (Controller Boot Thread) WFLYSRV0026: JBoss EAP 7.4.18.GA (WildFly Core 15.0.37.Final-redhat-00001) iniciado (com erros) em 8719ms - Iniciado(s) 1568 de serviços 2150 (377 serviços falharam ou tinham dependências ausentes, os serviços 364 estão lentos, passivos ou sob demanda)
268:2026-10-20 15:33:47,528 ERROR [org.jboss.modcluster] (UndertowEventHandlerAdapterService - 1) MODCLUSTER000043: Failed to send INFO command to localhost/127.0.0.1:6666: Conexão recusada (Connection refused)
269:2026-10-20 15:48:07,578 ERROR [org.jboss.modcluster] (UndertowEventHandlerAdapterService - 1) MODCLUSTER000040: Failed to parse response header from localhost/127.0.0.1:6666 for INFO command: java.lang.NumberFormatException: For input string: "/"
289:2026-10-20 15:48:07,579 ERROR [org.jboss.modcluster] (UndertowEventHandlerAdapterService - 1) MODCLUSTER000042: Error null sending INFO command to localhost/127.0.0.1:6666, configuration will be reset: null
[p585600@caddeapllx955 ~]$
