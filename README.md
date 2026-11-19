
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# grep -n "Autenticacao\|SenhasSIIBC\|SIROT\|SIPER\|ERROR" /opt/jboss-eap/standalone/log/server.log | tail -40
11:     co.elastic.apm.agent.shaded.slf4j.simpleLogger.log.co.elastic.apm = ERROR
105:2026-10-22 12:01:04,967 ERROR [org.jboss.as.controller] (Controller Boot Thread)
125:2026-10-22 12:01:04,967 ERROR [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0055: Foi vista uma exceção durante a inicialização: org.jboss.as.controller.persistence.ConfigurationPersistenceException: WFLYCTL0085: Falha ao pesquisar a configuração
143:    co.elastic.apm.agent.shaded.slf4j.simpleLogger.log.co.elastic.apm = ERROR
237:2026-10-22 12:01:21,820 ERROR [org.jboss.as.controller] (Controller Boot Thread)
257:2026-10-22 12:01:21,820 ERROR [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0055: Foi vista uma exceção durante a inicialização: org.jboss.as.controller.persistence.ConfigurationPersistenceException: WFLYCTL0085: Falha ao pesquisar a configuração
275:    co.elastic.apm.agent.shaded.slf4j.simpleLogger.log.co.elastic.apm = ERROR
369:2026-10-22 12:04:53,149 ERROR [org.jboss.as.controller] (Controller Boot Thread)
389:2026-10-22 12:04:53,149 ERROR [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0055: Foi vista uma exceção durante a inicialização: org.jboss.as.controller.persistence.ConfigurationPersistenceException: WFLYCTL0085: Falha ao pesquisar a configuração
407:    co.elastic.apm.agent.shaded.slf4j.simpleLogger.log.co.elastic.apm = ERROR
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# sed -n '/2026-11-19 11:3/,$p' /opt/jboss-eap/standalone/log/server.log | grep -A30 "Autenticacao" | head -60
[root@caddeapllx2854 ~]#
