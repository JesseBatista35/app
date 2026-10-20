
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$ sed -n '945,965p' /logs/jboss/jboss-eap/standalone/sigsj-boleto/server.log
2026-10-20 11:31:47,512 INFO  [org.apache.activemq.artemis.ra] (MSC service thread 1-2) AMQ151007: Resource adaptor started
2026-10-20 11:31:47,512 INFO  [org.jboss.as.connector.services.resourceadapters.ResourceAdapterActivatorService$ResourceAdapterActivator] (MSC service thread 1-2) IJ020002: Deployed: file://RaActivatoractivemq-ra
2026-10-20 11:31:47,513 INFO  [org.jboss.as.connector.deployment] (MSC service thread 1-2) WFLYJCA0002: Conectores de Jakarta vinculados ConnectionFactory [java:/JmsXA]
2026-10-20 11:31:47,513 INFO  [org.jboss.as.connector.deployment] (MSC service thread 1-2) WFLYJCA0118: Vínculo de criação de conexão chamado java:/JmsXA para o alias java:jboss/DefaultJMSConnectionFactory
2026-10-20 11:31:49,060 ERROR [org.jboss.as.controller.management-operation] (Controller Boot Thread) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "boletoService-ear.ear")]) - falha na descrição: {
    "WFLYCTL0412: Serviços necessários que não estão instalados:" => [
        "module.resolved.service.\"deployment.boletoService-ear.ear\".main",
        "jboss.module.spec.service.\"deployment.sirotcon-ejb-2.3.0.1-farm.jar\".main",
        "module.resolved.service.\"deployment.boletoService-ear.ear.boletoService-war-2.0.2.8.war\".main"
    ],
    "WFLYCTL0180: Os serviços com falta/indisponibilidade de dependências " => [
        "jboss.module.resolve.phase.\"deployment.boletoService-ear.ear.boletoService-war-2.0.2.8.war\".main.2 faltam [jboss.module.spec.service.\"deployment.sirotcon-ejb-2.3.0.1-farm.jar\".main]",
        "jboss.module.service.\"deployment.boletoService-ear.ear.boletoService-war-2.0.2.8.war\".main faltam [module.resolved.service.\"deployment.boletoService-ear.ear.boletoService-war-2.0.2.8.war\".main]",
        "jboss.module.service.\"deployment.boletoService-ear.ear\".main faltam [module.resolved.service.\"deployment.boletoService-ear.ear\".main]",
        "jboss.module.resolve.phase.\"deployment.boletoService-ear.ear\".main.1 faltam [jboss.module.spec.service.\"deployment.sirotcon-ejb-2.3.0.1-farm.jar\".main]"
    ]
}
2026-10-20 11:31:49,074 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 43) WFLYSRV0010: "boletoService-ear.ear" foi implantado (runtime-name: "boletoService-ear.ear")
2026-10-20 11:31:49,074 INFO  [org.jboss.as.controller] (Controller Boot Thread) WFLYCTL0183: Relatório
 de status de serviçoWFLYCTL0184: Não falta/insatisfaz nenhuma das dependências:
service jboss.module.spec.service."deployment.sirotcon-ejb-2.3.0.1-farm.jar".main (faltam) dependentes: [service jboss.module.resolve.phase."deployment.boletoService-ear.ear.boletoService-war-2.0.2.8.war".main.2, service jboss.module.resolve.phase."deployment.boletoService-ear.ear".main.1]
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$ ls -la /opt/jboss/jboss-eap/standalone/deployments/ | grep -i sirot
ls: não foi possível acessar '/opt/jboss/jboss-eap/standalone/deployments/': Arquivo ou diretório inexistente
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$ grep -n -i -B2 -A3 "sirot" /opt/jboss/jboss-eap/standalone/configuration/standalone-full-ha.xml
grep: /opt/jboss/jboss-eap/standalone/configuration/standalone-full-ha.xml: Arquivo ou diretório inexistente
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$ grep -i "sirot" /logs/jboss/jboss-eap/standalone/sigsj-internet/server.log | grep -iE "deploy|WFLYSRV0010|jndi" | head -10
grep: /logs/jboss/jboss-eap/standalone/sigsj-internet/server.log: Arquivo ou diretório inexistente
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
