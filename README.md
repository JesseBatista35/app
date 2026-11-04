1. Servidor no ar (no jboss-cli do 471):

/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)

O resultado esperado é running.

2. SIFEC subiu sem erro (no 473):

bash
sudo grep -E "WFLYSRV0010|WFLYSRV0021|WFLYSRV0025" /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | tail -10

Deve aparecer "SIFEC" foi implantado, junto com SIFEC-CCR, BDCAIXA, HUB-FRONTEND e MINUTAS-FRONT, e no final o WFLYSRV0025. Se aparecer WFLYSRV0021 em algum deles, pare e me mande.

Peça também para alguém da sala testar o login e a Consulta de Contratos.

3. Se o SIFEC estiver ok, o EMPRESAS. Com o tail aberto no 473:

bash
sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -iE --line-buffered "empresas|WFLYSRV0010|WFLYSRV0021|WELD-001408|faltam|Registered web context"

E no 471:

deploy --name=SIEMP-EMPRESAS --server-groups=sifec-intranet

Rollback, se o SIFEC tiver qualquer problema:

/profile=full-ha-sifec-intranet/subsystem=weld:write-attribute(name=require-bean-descriptor,value=false)
/server-group=sifec-intranet:reload-servers(blocking=true)



[domain@localhost:9999 /]
[domain@localhost:9999 /] deploy --name=SIEMP-EMPRESAS --server-groups=sifec-intranet
{"WFLYDC0074: Operation failed or was rolled back on all servers. Server failures:" => {"server-group" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx
473" => {"WFLYCTL0062: A operação de composição falhou e foi revertida. Segue abaixo as etapas que falharam:" => {"Operação step-2" => {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\
"empresas-1.2.3-b15.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type ParametrizacaoService with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.empresa.rest.ParametrizacaoRest.parametrizacaoService
  at br.gov.caixa.empresa.rest.ParametrizacaoRest.parametrizacaoService(ParametrizacaoRest.java:0)
"}}}}}}}}}}

[domain@localhost:9999 /]




[sudo] password for p585600:
16:59:08,826 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "ojdbc6.jar" foi implantado (runtime-name: "ojdbc6.jar")
16:59:08,826 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "ojdbc7-12.1.0.2.jar" foi implantado (runtime-name: "ojdbc7-12.1.0.2.jar")
16:59:08,826 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "ojdbc8-19.19.0.0.jar" foi implantado (runtime-name: "ojdbc8-19.19.0.0.jar")
16:59:08,827 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "wmq.jmsra.rar" foi implantado (runtime-name: "wmq.jmsra.rar")
16:59:08,827 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "SICCR-BDCAIXA" foi implantado (runtime-name: "sifec-bdcaixa-2.0.1-b39.ear")
16:59:08,827 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "SICCR-HUB-FRONTEND" foi implantado (runtime-name: "hub-web-1.4.0-b378.ear")
16:59:08,827 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "SIFEC-MINUTAS-FRONT" foi implantado (runtime-name: "gerenciador-minutas-web-1.0.0-b14.ear")
16:59:08,827 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "SQLSERVER-sqljdbc4.jar" foi implantado (runtime-name: "SQLSERVER-sqljdbc4.jar")
16:59:08,827 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "SIFEC-CCR" foi implantado (runtime-name: "SIFEC-CCR-6.3.0-b4587.ear")
16:59:08,847 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0025: JBoss EAP 7.4.23.GA (WildFly Core 15.0.43.Final-redhat-00001) iniciado em 15307ms - Iniciado(s) 9212 de serviços 9481 (os serviços 574 estão lentos, passivos ou sob demanda)
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$ sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -iE --line-buffered "empresas|WFLYSRV0010|WFLYSRV0021|WELD-001408|faltam|Registered web context"
16:59:08,826 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "ojdbc7-12.1.0.2.jar" foi implantado (runtime-name: "ojdbc7-12.1.0.2.jar")
16:59:08,826 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "ojdbc8-19.19.0.0.jar" foi implantado (runtime-name: "ojdbc8-19.19.0.0.jar")
16:59:08,827 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "wmq.jmsra.rar" foi implantado (runtime-name: "wmq.jmsra.rar")
16:59:08,827 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "SICCR-BDCAIXA" foi implantado (runtime-name: "sifec-bdcaixa-2.0.1-b39.ear")
16:59:08,827 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "SICCR-HUB-FRONTEND" foi implantado (runtime-name: "hub-web-1.4.0-b378.ear")
16:59:08,827 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "SIFEC-MINUTAS-FRONT" foi implantado (runtime-name: "gerenciador-minutas-web-1.0.0-b14.ear")
16:59:08,827 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "SQLSERVER-sqljdbc4.jar" foi implantado (runtime-name: "SQLSERVER-sqljdbc4.jar")
16:59:08,827 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: "SIFEC-CCR" foi implantado (runtime-name: "SIFEC-CCR-6.3.0-b4587.ear")
17:04:44,656 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-4) WFLYSRV0027: Iniciando a implantação do "SIEMP-EMPRESAS" (runtime-name: "empresas-1.2.3-b15.ear")
17:04:45,121 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "empresas-web.war")
17:04:45,121 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-6) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "empresas-ejb.jar")
17:04:45,610 WARN  [org.jboss.as.server.deployment] (MSC service thread 1-5) WFLYSRV0059: A entrada do caminho da classe toolbox.jar em /content/empresas-1.2.3-b15.ear/empresas-web.war/WEB-INF/lib/itext-2.0.8.jar não direciona a um jar válido para a referência do caminho da classe.
17:04:45,724 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para empresas-1.2.3-b15.ear#fecDS
17:04:45,725 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 21) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'empresas-1.2.3-b15.ear#fecDS'
17:04:45,725 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para empresas-1.2.3-b15.ear/empresas-ejb.jar#Siemp2EjbSybase
17:04:45,725 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para empresas-1.2.3-b15.ear/empresas-ejb.jar#fecDS
17:04:45,726 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 20) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'empresas-1.2.3-b15.ear/empresas-ejb.jar#fecDS'
17:04:45,726 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 88) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'empresas-1.2.3-b15.ear/empresas-ejb.jar#Siemp2EjbSybase'
17:04:45,764 INFO  [org.jboss.weld.deployer] (MSC service thread 1-2) WFLYWELD0003: Processando da implantação weld empresas-1.2.3-b15.ear
17:04:45,778 INFO  [org.jboss.keycloak] (MSC service thread 1-1) Keycloak subsystem override for deployment empresas-web.war
17:04:45,778 INFO  [org.jboss.weld.deployer] (MSC service thread 1-1) WFLYWELD0003: Processando da implantação weld empresas-web.war
17:04:45,798 INFO  [org.jboss.weld.deployer] (MSC service thread 1-4) WFLYWELD0003: Processando da implantação weld empresas-ejb.jar
17:04:45,800 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-4) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EnvioEmailBean' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/EnvioEmailBean!br.gov.caixa.empresa.negocio.EnvioEmailService
        java:app/empresas-ejb/EnvioEmailBean!br.gov.caixa.empresa.negocio.EnvioEmailService
        java:global/empresas-1.2.3-b15/empresas-ejb/EnvioEmailBean!br.gov.caixa.empresa.negocio.EnvioEmailBean
        java:app/empresas-ejb/EnvioEmailBean!br.gov.caixa.empresa.negocio.EnvioEmailBean
17:04:45,800 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-4) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DAOBarramentoFactory' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/DAOBarramentoFactory!br.gov.caixa.empresa.barramento.dao.DAOBarramentoFactory
        java:app/empresas-ejb/DAOBarramentoFactory!br.gov.caixa.empresa.barramento.dao.DAOBarramentoFactory
        java:global/empresas-1.2.3-b15/empresas-ejb/DAOBarramentoFactory
        java:app/empresas-ejb/DAOBarramentoFactory
17:04:45,800 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-4) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutorLog' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/ProdutorLog!br.gov.caixa.empresa.log.ProdutorLog
        java:app/empresas-ejb/ProdutorLog!br.gov.caixa.empresa.log.ProdutorLog
        java:global/empresas-1.2.3-b15/empresas-ejb/ProdutorLog
        java:app/empresas-ejb/ProdutorLog
17:04:45,800 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-4) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoRiscoNegocio' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/AvaliacaoRiscoNegocio!br.gov.caixa.empresa.negocio.AvaliacaoRiscoNegocio
        java:app/empresas-ejb/AvaliacaoRiscoNegocio!br.gov.caixa.empresa.negocio.AvaliacaoRiscoNegocio
        java:global/empresas-1.2.3-b15/empresas-ejb/AvaliacaoRiscoNegocio
        java:app/empresas-ejb/AvaliacaoRiscoNegocio
17:04:45,800 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-4) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SimulacaoBean' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/SimulacaoBean!br.gov.caixa.empresa.negocio.SimulacaoBean
        java:app/empresas-ejb/SimulacaoBean!br.gov.caixa.empresa.negocio.SimulacaoBean
        java:global/empresas-1.2.3-b15/empresas-ejb/SimulacaoBean!br.gov.caixa.empresa.negocio.SimulacaoService
        java:app/empresas-ejb/SimulacaoBean!br.gov.caixa.empresa.negocio.SimulacaoService
17:04:45,800 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-4) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DadosPessoaisSICLIBean' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/DadosPessoaisSICLIBean!br.gov.caixa.empresa.negocio.DadosPessoaisSICLIBean
        java:app/empresas-ejb/DadosPessoaisSICLIBean!br.gov.caixa.empresa.negocio.DadosPessoaisSICLIBean
        java:global/empresas-1.2.3-b15/empresas-ejb/DadosPessoaisSICLIBean!br.gov.caixa.empresa.negocio.DadosPessoaisSICLIService
        java:app/empresas-ejb/DadosPessoaisSICLIBean!br.gov.caixa.empresa.negocio.DadosPessoaisSICLIService
17:04:45,800 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-4) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoDeRiscoDAO' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/AvaliacaoDeRiscoDAO!br.gov.caixa.empresa.barramento.dao.AvaliacaoDeRiscoDAO
        java:app/empresas-ejb/AvaliacaoDeRiscoDAO!br.gov.caixa.empresa.barramento.dao.AvaliacaoDeRiscoDAO
        java:global/empresas-1.2.3-b15/empresas-ejb/AvaliacaoDeRiscoDAO
        java:app/empresas-ejb/AvaliacaoDeRiscoDAO
17:04:45,800 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-4) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ParametrizacaoBean' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/ParametrizacaoBean!br.gov.caixa.empresa.negocio.ParametrizacaoBean
        java:app/empresas-ejb/ParametrizacaoBean!br.gov.caixa.empresa.negocio.ParametrizacaoBean
        java:global/empresas-1.2.3-b15/empresas-ejb/ParametrizacaoBean
        java:app/empresas-ejb/ParametrizacaoBean
17:04:45,800 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-4) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ContratacaoBean' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/ContratacaoBean!br.gov.caixa.empresa.negocio.ContratacaoService
        java:app/empresas-ejb/ContratacaoBean!br.gov.caixa.empresa.negocio.ContratacaoService
        java:global/empresas-1.2.3-b15/empresas-ejb/ContratacaoBean!br.gov.caixa.empresa.negocio.ContratacaoBean
        java:app/empresas-ejb/ContratacaoBean!br.gov.caixa.empresa.negocio.ContratacaoBean
17:04:45,802 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para empresas-1.2.3-b15.ear#fecDS
17:04:45,836 INFO  [org.jipijapa] (MSC service thread 1-5) JIPIORMV53020253: Cache de segundo nível habilitado para empresas-1.2.3-b15.ear/empresas-ejb.jar#Siemp2EjbSybase
17:04:45,836 INFO  [org.jipijapa] (MSC service thread 1-5) JIPIORMV53020253: Cache de segundo nível habilitado para empresas-1.2.3-b15.ear/empresas-ejb.jar#fecDS
17:04:45,837 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 88) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'empresas-1.2.3-b15.ear#fecDS'
17:04:45,844 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 20) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'empresas-1.2.3-b15.ear/empresas-ejb.jar#fecDS'
17:04:45,845 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 21) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'empresas-1.2.3-b15.ear/empresas-ejb.jar#Siemp2EjbSybase'
17:04:46,168 ERROR [org.jboss.msc.service.fail] (MSC service thread 1-5) MSC000001: Failed to start service jboss.deployment.unit."empresas-1.2.3-b15.ear".WeldStartService: org.jboss.msc.service.StartException in service jboss.deployment.unit."empresas-1.2.3-b15.ear".WeldStartService: Failed to start service
Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type ParametrizacaoService with qualifiers @Default
17:04:46,170 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 85) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SIEMP-EMPRESAS")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"empresas-1.2.3-b15.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type ParametrizacaoService with qualifiers @Default
17:04:46,170 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 85) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SIEMP-EMPRESAS")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"empresas-1.2.3-b15.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type ParametrizacaoService with qualifiers @Default
17:04:46,171 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 85) WFLYSRV0021: O procedimento da implantação "empresas-1.2.3-b15.ear" foi revertido com mensagem de falha:
{"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"empresas-1.2.3-b15.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type ParametrizacaoService with qualifiers @Default
17:04:46,171 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 21) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'empresas-1.2.3-b15.ear/empresas-ejb.jar#fecDS'
17:04:46,171 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 20) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'empresas-1.2.3-b15.ear#fecDS'
17:04:46,173 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 89) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'empresas-1.2.3-b15.ear/empresas-ejb.jar#Siemp2EjbSybase'
17:04:46,173 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 20) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'empresas-1.2.3-b15.ear#fecDS'
17:04:46,174 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 21) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'empresas-1.2.3-b15.ear/empresas-ejb.jar#fecDS'
17:04:46,174 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 20) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'empresas-1.2.3-b15.ear/empresas-ejb.jar#Siemp2EjbSybase'
17:04:46,182 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-3) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: empresas-ejb.jar) em 11ms
17:04:46,192 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-2) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: empresas-web.war) em 20ms
17:04:46,194 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-2) WFLYSRV0028: Implantação interrompida SIEMP-EMPRESAS (runtime-name: empresas-1.2.3-b15.ear) em 23ms

