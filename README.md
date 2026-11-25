caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]# systemctl status jboss-eap-standalone --no-pager | head -15
○ jboss-eap-standalone.service - JBoss EAP Systemctl - STANDALONE
     Loaded: loaded (/etc/systemd/system/jboss-eap-standalone.service; enabled; preset: disabled)
     Active: inactive (dead) since Wed 2026-11-25 10:47:01 -03; 24min ago
   Duration: 1h 16min 5.324s
    Process: 2376952 ExecStart=/opt/jboss-eap/bin/init.d/jboss-eap-standalone.sh start (code=exited, status=0/SUCCESS)
    Process: 2377214 ExecStop=/opt/jboss-eap/bin/init.d/jboss-eap-standalone.sh stop (code=exited, status=0/SUCCESS)
        CPU: 1.815s

nov 25 10:46:57 caddeapllx2854.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[2376952]: Starting JBoss EAP:
nov 25 10:46:57 caddeapllx2854.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[2377167]: Erro: Não foi possível localizar nem carregar a classe principal http:..apm-server-devops.apps.produtos4.caixa
nov 25 10:46:57 caddeapllx2854.agil.nprd.caixa.gov.br runuser[2376962]: pam_unix(runuser:session): session closed for user jboss
nov 25 10:47:01 caddeapllx2854.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[2377213]: /opt/jboss-eap/bin/common_start.sh: linha 58: success: comando não encontrado
nov 25 10:47:01 caddeapllx2854.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[2377214]: /opt/jboss-eap/bin/init.d/jboss-eap-standalone.sh: linha 4: /etc/init.d/functions: Arquivo ou diretório inexistente
nov 25 10:47:01 caddeapllx2854.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[2377214]: Stopping JBoss EAP:
nov 25 10:47:01 caddeapllx2854.agil.nprd.caixa.gov.br jboss-eap-standalone.sh[2377216]: /opt/jboss-eap/bin/common_start.sh: linha 85: success: comando não encontrado
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]# grep -nE "ERROR|FATAL|Failed to|Exception" /opt/jboss-eap/standalone/log/server.log | tail -30
11:     co.elastic.apm.agent.shaded.slf4j.simpleLogger.log.co.elastic.apm = ERROR
105:2026-10-22 12:01:04,967 ERROR [org.jboss.as.controller] (Controller Boot Thread)
125:2026-10-22 12:01:04,967 ERROR [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0055: Foi vista uma exceção durante a inicialização: org.jboss.as.controller.persistence.ConfigurationPersistenceException: WFLYCTL0085: Falha ao pesquisar a configuração
131:2026-10-22 12:01:04,969 FATAL [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0056: A inicialização do servidor falhou numa maneira irrecuperável: encerrando. Consulte mensagens anteriores para maiores detalhes.
143:    co.elastic.apm.agent.shaded.slf4j.simpleLogger.log.co.elastic.apm = ERROR
237:2026-10-22 12:01:21,820 ERROR [org.jboss.as.controller] (Controller Boot Thread)
257:2026-10-22 12:01:21,820 ERROR [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0055: Foi vista uma exceção durante a inicialização: org.jboss.as.controller.persistence.ConfigurationPersistenceException: WFLYCTL0085: Falha ao pesquisar a configuração
263:2026-10-22 12:01:21,821 FATAL [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0056: A inicialização do servidor falhou numa maneira irrecuperável: encerrando. Consulte mensagens anteriores para maiores detalhes.
275:    co.elastic.apm.agent.shaded.slf4j.simpleLogger.log.co.elastic.apm = ERROR
369:2026-10-22 12:04:53,149 ERROR [org.jboss.as.controller] (Controller Boot Thread)
389:2026-10-22 12:04:53,149 ERROR [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0055: Foi vista uma exceção durante a inicialização: org.jboss.as.controller.persistence.ConfigurationPersistenceException: WFLYCTL0085: Falha ao pesquisar a configuração
395:2026-10-22 12:04:53,150 FATAL [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0056: A inicialização do servidor falhou numa maneira irrecuperável: encerrando. Consulte mensagens anteriores para maiores detalhes.
407:    co.elastic.apm.agent.shaded.slf4j.simpleLogger.log.co.elastic.apm = ERROR
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]# echo "=== fim do server.log ==="
=== fim do server.log ===
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]# tail -40 /opt/jboss-eap/standalone/log/server.log
2026-10-22 12:31:37,643 INFO  [org.xnio] (MSC service thread 1-2) XNIO version 3.8.16.Final-redhat-00001
2026-10-22 12:31:37,653 INFO  [org.xnio.nio] (MSC service thread 1-2) XNIO NIO Implementation Version 3.8.16.Final-redhat-00001
2026-10-22 12:31:37,732 INFO  [org.wildfly.extension.health] (ServerService Thread Pool -- 48) WFLYHEALTH0001: Ativando o Subsistema Básico de integridade
2026-10-22 12:31:37,744 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 50) WFLYCLINF0001: Ativação do subsistema Infinispan.
2026-10-22 12:31:37,775 INFO  [org.jboss.as.connector.subsystems.datasources] (ServerService Thread Pool -- 42) WFLYJCA0004: Implantação do driver compatível-JDBC class org.h2.Driver (versão 1.4)
2026-10-22 12:31:37,777 INFO  [org.wildfly.extension.io] (ServerService Thread Pool -- 51) WFLYIO001: O operador 'default' configurou automaticamente para as threads de E/S 4 com o máximo de 32 threads de tarefas com base em seus 2 processadores disponíveis.
2026-10-22 12:31:37,800 INFO  [org.jboss.as.jsf] (ServerService Thread Pool -- 57) WFLYJSF0007: Ativadas as seguintes implantações do Jakarta Server Faces: [main]
2026-10-22 12:31:37,813 INFO  [org.jboss.as.connector] (MSC service thread 1-4) WFLYJCA0009: Inicialização do Subsistema Jakarta Connectors (WildFly/IronJacamar 1.5.17.Final-redhat-00001)
2026-10-22 12:31:37,838 INFO  [org.wildfly.iiop.openjdk] (ServerService Thread Pool -- 49) WFLYIIOP0001: Ativação de subsistema IIOP
2026-10-22 12:31:37,848 INFO  [org.jboss.as.jaxrs] (ServerService Thread Pool -- 52) WFLYRS0016: RESTEasy versão 3.15.9.Final-redhat-00001
2026-10-22 12:31:37,863 INFO  [org.wildfly.extension.metrics] (ServerService Thread Pool -- 61) WFLYMETRICS0001: Ativando o subsistema de métricas de base
2026-10-22 12:31:37,877 INFO  [org.jboss.as.naming] (ServerService Thread Pool -- 63) WFLYNAM0001: Ativação do Subsistema de Nomeação
2026-10-22 12:31:37,901 WARN  [org.jboss.as.txn] (ServerService Thread Pool -- 70) WFLYTX0013: O atributo node-identifier em /subsystem=transactions está definido com o valor padrão. Isso é perigoso para ambientes executando vários servidores. Certifique-se de que o valor do atributo é exclusivo.
2026-10-22 12:31:37,938 INFO  [org.jboss.as.webservices] (ServerService Thread Pool -- 72) WFLYWS0002: Ativação da Extensão WebServices
2026-10-22 12:31:37,954 INFO  [org.jboss.as.connector.deployers.jdbc] (MSC service thread 1-3) WFLYJCA0018: Serviço de driver iniciado com nome-do-driver = h2
2026-10-22 12:31:37,963 INFO  [org.jboss.as.naming] (MSC service thread 1-3) WFLYNAM0003: Iniciando o Serviço de Nomeação
2026-10-22 12:31:37,964 INFO  [org.jboss.as.mail.extension] (MSC service thread 1-3) WFLYMAIL0001: Sessão de e-mail associada [java:jboss/mail/Default]
2026-10-22 12:31:38,039 WARN  [org.wildfly.clustering.web.undertow] (ServerService Thread Pool -- 71) WFLYCLWEBUT0007: Nenhum provedor de roteamento encontrado para default-server; usando o provedor herdado baseado na configuração estática
2026-10-22 12:31:38,063 WARN  [org.wildfly.extension.elytron] (MSC service thread 1-4) WFLYELY00023: O arquivo '/opt/jboss-eap/standalone/configuration/application.keystore' da KeyStore não existe. Usado em branco.
2026-10-22 12:31:38,095 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-1) WFLYUT0003: Iniciando Undertow 2.2.33.SP1-redhat-00001
2026-10-22 12:31:38,127 INFO  [org.jboss.as.ejb3] (MSC service thread 1-1) WFLYEJB0481: O pool estrito slsb-strict-max-pool está utilizando um tamanho de instância máximo de 32 (por classe) que é derivado do tamanho de pool do thead de trabalho.
2026-10-22 12:31:38,131 INFO  [org.jboss.as.ejb3] (MSC service thread 1-2) WFLYEJB0482: O pool estrito mdb-strict-max-pool está utilizando um tamanho de instância máximo de 8 (por classe) que é derivado do número de CPUs neste host.
2026-10-22 12:31:38,137 INFO  [org.jboss.remoting] (MSC service thread 1-1) JBoss Remoting version 5.0.29.Final-redhat-00001
2026-10-22 12:31:38,157 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 71) WFLYUT0014: Criando identificador de arquivo para caminho de acesso '/opt/jboss-eap/welcome-content' com as opções [directory-listing: 'false', follow-symlink: 'false', case-sensitive: 'true', safe-symlink-paths: '[]']
2026-10-22 12:31:38,175 WARN  [org.wildfly.extension.elytron] (MSC service thread 1-2) WFLYELY01084: KeyStore /opt/jboss-eap/standalone/configuration/application.keystore não encontrado; ele será gerado automaticamente na primeira utilização com um certificado autoassinado para o host localhost
2026-10-22 12:31:38,335 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-4) WFLYUT0012: Servidor default-server foi iniciado.
2026-10-22 12:31:38,357 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-4) Queuing requests.
2026-10-22 12:31:38,357 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-4) WFLYUT0018: Iniciando host default-host
2026-10-22 12:31:38,391 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-4) WFLYUT0006: UndertowAJP ouvinte ajp escutando em 0.0.0.0:8009
2026-10-22 12:31:38,394 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-4) WFLYUT0006: UndertowHTTP ouvinte default escutando em 0.0.0.0:8080
2026-10-22 12:31:38,412 INFO  [org.wildfly.iiop.openjdk] (MSC service thread 1-3) WFLYIIOP0009: Serviço CORBA ORB iniciado
2026-10-22 12:31:38,426 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-4) WFLYUT0006: UndertowHTTPS ouvinte https escutando em 0.0.0.0:8443
2026-10-22 12:31:38,429 INFO  [org.jboss.modcluster] (ServerService Thread Pool -- 74) MODCLUSTER000001: Initializing mod_cluster version 1.4.5.Final-redhat-00001
2026-10-22 12:31:38,437 INFO  [org.jboss.as.ejb3] (MSC service thread 1-4) WFLYEJB0493: Suspensão completa do subsistema de Jakarta Enterprise Beans
2026-10-22 12:31:38,444 INFO  [org.jboss.modcluster] (ServerService Thread Pool -- 74) MODCLUSTER000032: Listening to proxy advertisements on /224.0.1.105:23364
2026-10-22 12:31:38,555 INFO  [org.jboss.as.connector.subsystems.datasources] (MSC service thread 1-3) WFLYJCA0001: Fonte de dados vinculada[java:jboss/datasources/ExampleDS]
2026-10-22 12:31:38,869 INFO  [org.jboss.as.patching] (MSC service thread 1-1) WFLYPAT0050: A ID de patch cumulativo de JBoss EAP é jboss-eap-7.4.18.CP, os patches únicos incluem: none
2026-10-22 12:31:38,913 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-2) WFLYSRV0027: Iniciando a implantação do "sirotcon-ejb.jar" (runtime-name: "sirotcon-ejb.jar")
2026-10-22 12:31:38,914 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-2) WFLYSRV0027: Iniciando a implantação do "sigsj_internet-ear.ear" (runtime-name: "sigsj_internet-ear.ear")
2026-10-22 12:31:38,915 INFO  [org.jboss.as.server.deployment.scanner] (MSC service thread 1-2) WFLYDS0013: Foi iniciado FileSystemDeploymentService para o diretório /opt/jboss-eap/standalone/deployments
[root@caddeapllx2854 p585600]# echo "=== ta rodando agora? ==="
ps -ef | grep -v grep | grep -o "java.library.path=[^ ]*"
=== ta rodando agora? ===
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]# ps -ef | grep -v grep | grep -o "java.library.path=[^ ]*"
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]#
[root@caddeapllx2854 p585600]# curl -s -o /dev/null -w "internet raiz: %{http_code}\n" http://10.116.202.45/sigsj_internet/
internet raiz: 000
[root@caddeapllx2854 p585600]#
