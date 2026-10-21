
[root@caddeapllx2557 bolchk]#
[root@caddeapllx2557 bolchk]#
[root@caddeapllx2557 bolchk]# ^C
[root@caddeapllx2557 bolchk]# journalctl -u jboss* --since "16:25" --no-pager | tail -40
out 21 16:35:09 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[170579]: /opt/jboss-eap/bin/init.d/jboss-eap-standalone.sh: linha 4: /etc/init.d/functions: Arquivo ou diretório inexistente
out 21 16:35:09 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[170579]: Stopping JBoss EAP:
out 21 16:35:09 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[170581]: /opt/jboss-eap/bin/common_start.sh: linha 85: success: comando não encontrado
out 21 16:35:09 caddeapllx2557.agil.nprd.caixa.gov.br systemd[1]: jboss-eap-standalone.service: Deactivated successfully.
out 21 16:35:09 caddeapllx2557.agil.nprd.caixa.gov.br systemd[1]: Started JBoss EAP Systemctl - STANDALONE.
out 21 16:35:09 caddeapllx2557.agil.nprd.caixa.gov.br systemd[1]: jboss-eap-standalone.service: Consumed 1.698s CPU time.
out 21 16:35:19 caddeapllx2557.agil.nprd.caixa.gov.br systemd[1]: Starting JBoss EAP Systemctl - STANDALONE...
out 21 16:35:19 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[171285]: /opt/jboss-eap/bin/init.d/jboss-eap-standalone.sh: linha 4: /etc/init.d/functions: Arquivo ou diretório inexistente
out 21 16:35:19 caddeapllx2557.agil.nprd.caixa.gov.br runuser[171287]: pam_unix(runuser:session): session opened for user jboss(uid=30000115) by (uid=0)
out 21 16:35:19 caddeapllx2557.agil.nprd.caixa.gov.br runuser[171287]: pam_unix(runuser:session): session closed for user jboss
out 21 16:35:19 caddeapllx2557.agil.nprd.caixa.gov.br runuser[171291]: pam_unix(runuser:session): session opened for user jboss(uid=30000115) by (uid=0)
out 21 16:35:19 caddeapllx2557.agil.nprd.caixa.gov.br runuser[171291]: pam_unix(runuser:session): session closed for user jboss
out 21 16:35:19 caddeapllx2557.agil.nprd.caixa.gov.br runuser[171295]: pam_unix(runuser:session): session opened for user jboss(uid=30000115) by (uid=0)
out 21 16:35:21 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[171285]: Starting JBoss EAP:
out 21 16:35:21 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[171496]: Erro: Não foi possível localizar nem carregar a classe principal http:..localhost:8200
out 21 16:35:21 caddeapllx2557.agil.nprd.caixa.gov.br runuser[171295]: pam_unix(runuser:session): session closed for user jboss
out 21 16:35:25 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[171542]: /opt/jboss-eap/bin/common_start.sh: linha 58: success: comando não encontrado
out 21 16:35:25 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[171543]: /opt/jboss-eap/bin/init.d/jboss-eap-standalone.sh: linha 4: /etc/init.d/functions: Arquivo ou diretório inexistente
out 21 16:35:25 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[171543]: Stopping JBoss EAP:
out 21 16:35:25 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[171545]: /opt/jboss-eap/bin/common_start.sh: linha 85: success: comando não encontrado
out 21 16:35:25 caddeapllx2557.agil.nprd.caixa.gov.br systemd[1]: jboss-eap-standalone.service: Deactivated successfully.
out 21 16:35:25 caddeapllx2557.agil.nprd.caixa.gov.br systemd[1]: Started JBoss EAP Systemctl - STANDALONE.
out 21 16:35:25 caddeapllx2557.agil.nprd.caixa.gov.br systemd[1]: jboss-eap-standalone.service: Consumed 1.677s CPU time.
out 21 16:38:50 caddeapllx2557.agil.nprd.caixa.gov.br systemd[1]: Starting JBoss EAP Systemctl - STANDALONE...
out 21 16:38:50 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[171726]: /opt/jboss-eap/bin/init.d/jboss-eap-standalone.sh: linha 4: /etc/init.d/functions: Arquivo ou diretório inexistente
out 21 16:38:50 caddeapllx2557.agil.nprd.caixa.gov.br runuser[171728]: pam_unix(runuser:session): session opened for user jboss(uid=30000115) by (uid=0)
out 21 16:38:50 caddeapllx2557.agil.nprd.caixa.gov.br runuser[171728]: pam_unix(runuser:session): session closed for user jboss
out 21 16:38:50 caddeapllx2557.agil.nprd.caixa.gov.br runuser[171732]: pam_unix(runuser:session): session opened for user jboss(uid=30000115) by (uid=0)
out 21 16:38:50 caddeapllx2557.agil.nprd.caixa.gov.br runuser[171732]: pam_unix(runuser:session): session closed for user jboss
out 21 16:38:50 caddeapllx2557.agil.nprd.caixa.gov.br runuser[171736]: pam_unix(runuser:session): session opened for user jboss(uid=30000115) by (uid=0)
out 21 16:38:51 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[171726]: Starting JBoss EAP:
out 21 16:38:51 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[171937]: Erro: Não foi possível localizar nem carregar a classe principal http:..localhost:8200
out 21 16:38:52 caddeapllx2557.agil.nprd.caixa.gov.br runuser[171736]: pam_unix(runuser:session): session closed for user jboss
out 21 16:38:56 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[171983]: /opt/jboss-eap/bin/common_start.sh: linha 58: success: comando não encontrado
out 21 16:38:56 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[171984]: /opt/jboss-eap/bin/init.d/jboss-eap-standalone.sh: linha 4: /etc/init.d/functions: Arquivo ou diretório inexistente
out 21 16:38:56 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[171984]: Stopping JBoss EAP:
out 21 16:38:56 caddeapllx2557.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[171986]: /opt/jboss-eap/bin/common_start.sh: linha 85: success: comando não encontrado
out 21 16:38:56 caddeapllx2557.agil.nprd.caixa.gov.br systemd[1]: jboss-eap-standalone.service: Deactivated successfully.
out 21 16:38:56 caddeapllx2557.agil.nprd.caixa.gov.br systemd[1]: Started JBoss EAP Systemctl - STANDALONE.
out 21 16:38:56 caddeapllx2557.agil.nprd.caixa.gov.br systemd[1]: jboss-eap-standalone.service: Consumed 1.693s CPU time.
[root@caddeapllx2557 bolchk]#
[root@caddeapllx2557 bolchk]#
[root@caddeapllx2557 bolchk]# grep -nE "ERROR|WFLYCTL|WFLYSRV0056|Exception" /opt/jboss-eap/standalone/log/server.log | tail -30
11:     co.elastic.apm.agent.shaded.slf4j.simpleLogger.log.co.elastic.apm = ERROR
106:2026-10-20 09:40:26,795 ERROR [org.jboss.as.controller] (Controller Boot Thread) WFLYCTL0362: As funcionalidades exigidas pelo recurso '/subsystem=modcluster/proxy=default' não estão disponíveis:
109:2026-10-20 09:40:26,800 FATAL [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0056: A inicialização do servidor falhou numa maneira irrecuperável: encerrando. Consulte mensagens anteriores para maiores detalhes.
121:    co.elastic.apm.agent.shaded.slf4j.simpleLogger.log.co.elastic.apm = ERROR
215:2026-10-20 09:45:25,665 INFO  [org.jboss.as.controller.management-deprecated] (ServerService Thread Pool -- 14) WFLYCTL0033: A extensão 'security' é obsoleta e talvez não seja suportada em versões futuras
216:2026-10-20 09:45:25,996 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: O atributo 'security-realm' no recurso, no endereço '/core-service=management/management-interface=http-interface', é obsoleto e pode ser removido em uma versão futura. Veja a descrição do atributo no resultado da operação read-resource-description para saber mais sobre a substituição.
218:2026-10-20 09:45:26,134 INFO  [org.jboss.as.controller.management-deprecated] (ServerService Thread Pool -- 40) WFLYCTL0028: O atributo 'security-realm' no recurso, no endereço '/subsystem=undertow/server=default-server/https-listener=https', é obsoleto e pode ser removido em uma versão futura. Veja a descrição do atributo no resultado da operação read-resource-description para saber mais sobre a substituição.
[root@caddeapllx2557 bolchk]#
