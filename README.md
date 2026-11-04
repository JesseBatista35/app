/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)

ssh p585600@10.116.97.79
sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -iE --line-buffered "emp-|WFLYSRV0010|WFLYSRV0021|JMSException|faltam|Registered web context|WELD-001408|Caused by"

Com o log aberto, rode o deploy no 471:

deploy --name=SIFEC-EMP --server-groups=sifec-intranet
✅ Subiu se aparecer Registered web context: '/emp-web' e WFLYSRV0010: "SIFEC-EMP" foi implantado.
❌ Se aparecer WFLYSRV0021, me cola as linhas.




[domain@localhost:9443 /] /host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)
{
    "outcome" => "success",
    "result" => "running"
}

[domain@localhost:9443 /]




[domain@localhost:9443 /] deploy --name=SIFEC-EMP --server-groups=sifec-intranet
{"WFLYDC0074: Operation failed or was rolled back on all servers. Server failures:" => {"server-group" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx
473" => {"WFLYCTL0062: A operação de composição falhou e foi revertida. Segue abaixo as etapas que falharam:" => {"Operação step-2" => {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\
"emp-3.95.0.1-b1437.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type VeiculosTotalizadorService with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.emprestimo.rest.VeiculosRest.totalizadorService
  at br.gov.caixa.emprestimo.rest.VeiculosRest.totalizadorService(VeiculosRest.java:0)
"}}}}}}}}}}

[domain@localhost:9443 /]



[p585600@cbrdeapllx473 ~]$ sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -iE --line-buffered "emp-|WFLYSRV0010|WFLYSRV0021|JMSException|faltam|Registered web context|WELD-001408|Caused by"

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for p585600:
16:07:40,146 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 107) WFLYCLINF0003: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.Unidade-pending-puts encerrado a partir do recipiente hibernate
16:07:40,146 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 107) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'emp-3.95.0.1-b1437.ear/emp-ejb.jar#SiempEjbDB2'
16:07:40,146 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 96) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase'
16:07:40,162 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 108) WFLYCLINF0003: Cache emp-3.95.0.1-b1437.ear.emp-web.war encerrado a partir do recipiente web
16:07:40,169 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: emp-ejb.jar) em 37ms
16:07:40,182 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-5) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: emp-api.war) em 50ms
16:07:40,195 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: emp-web.war) em 63ms
16:07:40,200 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0028: Implantação interrompida SIFEC-EMP (runtime-name: emp-3.95.0.1-b1437.ear) em 68ms
16:12:27,422 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0027: Iniciando a implantação do "SIFEC-EMP" (runtime-name: "emp-3.95.0.1-b1437.ear")
16:12:28,426 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-8) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "emp-web.war")
16:12:28,426 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-4) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "emp-ejb.jar")
16:12:28,426 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "emp-api.war")
16:12:29,012 WARN  [org.jboss.as.server.deployment] (MSC service thread 1-2) WFLYSRV0059: A entrada do caminho da classe toolbox.jar em /content/emp-3.95.0.1-b1437.ear/emp-api.war/WEB-INF/lib/itext-2.0.8.jar não direciona a um jar válido para a referência do caminho da classe.
16:12:29,428 INFO  [org.jboss.as.jpa] (MSC service thread 1-2) WFLYJPA0002: Ler persistence.xml para SIEMP-PU
16:12:29,512 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.95.0.1-b1437.ear#SIEMP-PU
16:12:29,513 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.95.0.1-b1437.ear#fecDS
16:12:29,513 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 108) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'emp-3.95.0.1-b1437.ear#SIEMP-PU'
16:12:29,513 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 107) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'emp-3.95.0.1-b1437.ear#fecDS'
16:12:29,517 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase
16:12:29,517 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.95.0.1-b1437.ear/emp-ejb.jar#SiempEjbDB2
16:12:29,517 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 110) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase'
16:12:29,517 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 109) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'emp-3.95.0.1-b1437.ear/emp-ejb.jar#SiempEjbDB2'
16:12:29,541 INFO  [org.jboss.weld.deployer] (MSC service thread 1-3) WFLYWELD0003: Processando da implantação weld emp-3.95.0.1-b1437.ear
16:12:29,572 INFO  [org.jboss.keycloak] (MSC service thread 1-4) Keycloak subsystem override for deployment emp-web.war
16:12:29,572 INFO  [org.jboss.weld.deployer] (MSC service thread 1-4) WFLYWELD0003: Processando da implantação weld emp-web.war
16:12:29,572 INFO  [org.jboss.keycloak] (MSC service thread 1-8) Keycloak subsystem override for deployment emp-api.war
16:12:29,585 INFO  [org.jboss.weld.deployer] (MSC service thread 1-8) WFLYWELD0003: Processando da implantação weld emp-api.war
16:12:29,677 INFO  [org.jboss.weld.deployer] (MSC service thread 1-1) WFLYWELD0003: Processando da implantação weld emp-ejb.jar
16:12:29,679 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RelatorioLancamentoContabilBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/RelatorioLancamentoContabilBean!br.gov.caixa.emprestimo.negocio.RelatorioLancamentoContabilBean
        java:app/emp-ejb/RelatorioLancamentoContabilBean!br.gov.caixa.emprestimo.negocio.RelatorioLancamentoContabilBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/RelatorioLancamentoContabilBean!br.gov.caixa.emprestimo.negocio.RelatorioLancamentoContabilService
        java:app/emp-ejb/RelatorioLancamentoContabilBean!br.gov.caixa.emprestimo.negocio.RelatorioLancamentoContabilService
16:12:29,679 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MoveBrasilBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/MoveBrasilBean!br.gov.caixa.emprestimo.negocio.MoveBrasilBean
        java:app/emp-ejb/MoveBrasilBean!br.gov.caixa.emprestimo.negocio.MoveBrasilBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/MoveBrasilBean!br.gov.caixa.emprestimo.negocio.MoveBrasilService
        java:app/emp-ejb/MoveBrasilBean!br.gov.caixa.emprestimo.negocio.MoveBrasilService
16:12:29,679 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RotinaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/RotinaBean!br.gov.caixa.emp.contabil.negocio.RotinaBean
        java:app/emp-ejb/RotinaBean!br.gov.caixa.emp.contabil.negocio.RotinaBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/RotinaBean
        java:app/emp-ejb/RotinaBean
16:12:29,680 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DAOBarramentoFactory' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/DAOBarramentoFactory!br.gov.caixa.emprestimo.barramento.dao.DAOBarramentoFactory
        java:app/emp-ejb/DAOBarramentoFactory!br.gov.caixa.emprestimo.barramento.dao.DAOBarramentoFactory
        java:global/emp-3.95.0.1-b1437/emp-ejb/DAOBarramentoFactory
        java:app/emp-ejb/DAOBarramentoFactory
16:12:29,680 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutorLog' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/ProdutorLog!br.gov.caixa.emprestimo.log.ProdutorLog
        java:app/emp-ejb/ProdutorLog!br.gov.caixa.emprestimo.log.ProdutorLog
        java:global/emp-3.95.0.1-b1437/emp-ejb/ProdutorLog
        java:app/emp-ejb/ProdutorLog
16:12:29,680 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoRiscoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/AvaliacaoRiscoBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoService
        java:app/emp-ejb/AvaliacaoRiscoBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoService
        java:global/emp-3.95.0.1-b1437/emp-ejb/AvaliacaoRiscoBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoBean
        java:app/emp-ejb/AvaliacaoRiscoBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoBean
16:12:29,680 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SistemaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/SistemaBean!br.gov.caixa.emp.contabil.negocio.SistemaBean
        java:app/emp-ejb/SistemaBean!br.gov.caixa.emp.contabil.negocio.SistemaBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/SistemaBean
        java:app/emp-ejb/SistemaBean
16:12:29,680 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RelatorioConciliacaoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/RelatorioConciliacaoBean!br.gov.caixa.emp.contabil.negocio.RelatorioConciliacaoBean
        java:app/emp-ejb/RelatorioConciliacaoBean!br.gov.caixa.emp.contabil.negocio.RelatorioConciliacaoBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/RelatorioConciliacaoBean
        java:app/emp-ejb/RelatorioConciliacaoBean
16:12:29,680 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'VeiculosFipeBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/VeiculosFipeBean!br.gov.caixa.emprestimo.negocio.VeiculosFipeBean
        java:app/emp-ejb/VeiculosFipeBean!br.gov.caixa.emprestimo.negocio.VeiculosFipeBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/VeiculosFipeBean!br.gov.caixa.emprestimo.negocio.VeiculosFipeService
        java:app/emp-ejb/VeiculosFipeBean!br.gov.caixa.emprestimo.negocio.VeiculosFipeService
16:12:29,680 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ServicosBndesBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/ServicosBndesBean!br.gov.caixa.emprestimo.negocio.ServicosBndesService
        java:app/emp-ejb/ServicosBndesBean!br.gov.caixa.emprestimo.negocio.ServicosBndesService
        java:global/emp-3.95.0.1-b1437/emp-ejb/ServicosBndesBean!br.gov.caixa.emprestimo.negocio.ServicosBndesBean
        java:app/emp-ejb/ServicosBndesBean!br.gov.caixa.emprestimo.negocio.ServicosBndesBean
16:12:29,680 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EntidadeBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/EntidadeBean!br.gov.caixa.emp.contabil.negocio.EntidadeBean
        java:app/emp-ejb/EntidadeBean!br.gov.caixa.emp.contabil.negocio.EntidadeBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/EntidadeBean
        java:app/emp-ejb/EntidadeBean
16:12:29,680 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'UnidadeBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/UnidadeBean!br.gov.caixa.emp.contabil.negocio.UnidadeBean
        java:app/emp-ejb/UnidadeBean!br.gov.caixa.emp.contabil.negocio.UnidadeBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/UnidadeBean
        java:app/emp-ejb/UnidadeBean
16:12:29,680 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RelatorioSaidaSinafBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/RelatorioSaidaSinafBean!br.gov.caixa.emp.contabil.negocio.RelatorioSaidaSinafBean
        java:app/emp-ejb/RelatorioSaidaSinafBean!br.gov.caixa.emp.contabil.negocio.RelatorioSaidaSinafBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/RelatorioSaidaSinafBean
        java:app/emp-ejb/RelatorioSaidaSinafBean
16:12:29,680 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SituacaoMapaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/SituacaoMapaBean!br.gov.caixa.emp.contabil.negocio.SituacaoMapaBean
        java:app/emp-ejb/SituacaoMapaBean!br.gov.caixa.emp.contabil.negocio.SituacaoMapaBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/SituacaoMapaBean
        java:app/emp-ejb/SituacaoMapaBean
16:12:29,681 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'GiroCaixaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/GiroCaixaBean!br.gov.caixa.emprestimo.negocio.GiroCaixaService
        java:app/emp-ejb/GiroCaixaBean!br.gov.caixa.emprestimo.negocio.GiroCaixaService
        java:global/emp-3.95.0.1-b1437/emp-ejb/GiroCaixaBean!br.gov.caixa.emprestimo.negocio.GiroCaixaBean
        java:app/emp-ejb/GiroCaixaBean!br.gov.caixa.emprestimo.negocio.GiroCaixaBean
16:12:29,681 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EventoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/EventoBean!br.gov.caixa.emp.contabil.negocio.EventoBean
        java:app/emp-ejb/EventoBean!br.gov.caixa.emp.contabil.negocio.EventoBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/EventoBean
        java:app/emp-ejb/EventoBean
16:12:29,681 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TimerServiceTestBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/TimerServiceTestBean!br.gov.caixa.emprestimo.negocio.TimerServiceTest
        java:app/emp-ejb/TimerServiceTestBean!br.gov.caixa.emprestimo.negocio.TimerServiceTest
        java:global/emp-3.95.0.1-b1437/emp-ejb/TimerServiceTestBean
        java:app/emp-ejb/TimerServiceTestBean
16:12:29,681 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'VeiculosBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/VeiculosBean!br.gov.caixa.emprestimo.negocio.VeiculosService
        java:app/emp-ejb/VeiculosBean!br.gov.caixa.emprestimo.negocio.VeiculosService
        java:global/emp-3.95.0.1-b1437/emp-ejb/VeiculosBean!br.gov.caixa.emprestimo.negocio.VeiculosBean
        java:app/emp-ejb/VeiculosBean!br.gov.caixa.emprestimo.negocio.VeiculosBean
16:12:29,681 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'PeriodicidadeBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/PeriodicidadeBean!br.gov.caixa.emp.contabil.negocio.PeriodicidadeBean
        java:app/emp-ejb/PeriodicidadeBean!br.gov.caixa.emp.contabil.negocio.PeriodicidadeBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/PeriodicidadeBean
        java:app/emp-ejb/PeriodicidadeBean
16:12:29,681 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'BndesBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/BndesBean!br.gov.caixa.emprestimo.negocio.BndesService
        java:app/emp-ejb/BndesBean!br.gov.caixa.emprestimo.negocio.BndesService
        java:global/emp-3.95.0.1-b1437/emp-ejb/BndesBean!br.gov.caixa.emprestimo.negocio.BndesBean
        java:app/emp-ejb/BndesBean!br.gov.caixa.emprestimo.negocio.BndesBean
16:12:29,681 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'OrigemLancamentoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/OrigemLancamentoBean!br.gov.caixa.emp.contabil.negocio.OrigemLancamentoBean
        java:app/emp-ejb/OrigemLancamentoBean!br.gov.caixa.emp.contabil.negocio.OrigemLancamentoBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/OrigemLancamentoBean
        java:app/emp-ejb/OrigemLancamentoBean
16:12:29,681 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'VeiculosTabelaAliquotaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/VeiculosTabelaAliquotaBean!br.gov.caixa.emprestimo.negocio.VeiculosTabelaAliquotaService
        java:app/emp-ejb/VeiculosTabelaAliquotaBean!br.gov.caixa.emprestimo.negocio.VeiculosTabelaAliquotaService
        java:global/emp-3.95.0.1-b1437/emp-ejb/VeiculosTabelaAliquotaBean!br.gov.caixa.emprestimo.negocio.VeiculosTabelaAliquotaBean
        java:app/emp-ejb/VeiculosTabelaAliquotaBean!br.gov.caixa.emprestimo.negocio.VeiculosTabelaAliquotaBean
16:12:29,681 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/ProdutoBean!br.gov.caixa.emp.contabil.negocio.ProdutoBean
        java:app/emp-ejb/ProdutoBean!br.gov.caixa.emp.contabil.negocio.ProdutoBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/ProdutoBean
        java:app/emp-ejb/ProdutoBean
16:12:29,681 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RelatorioEspecificacaoResumidaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/RelatorioEspecificacaoResumidaBean!br.gov.caixa.emp.contabil.negocio.RelatorioEspecificacaoResumidaBean
        java:app/emp-ejb/RelatorioEspecificacaoResumidaBean!br.gov.caixa.emp.contabil.negocio.RelatorioEspecificacaoResumidaBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/RelatorioEspecificacaoResumidaBean
        java:app/emp-ejb/RelatorioEspecificacaoResumidaBean
16:12:29,681 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AjusteManualBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/AjusteManualBean!br.gov.caixa.emprestimo.negocio.AjusteManualBean
        java:app/emp-ejb/AjusteManualBean!br.gov.caixa.emprestimo.negocio.AjusteManualBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/AjusteManualBean!br.gov.caixa.emprestimo.negocio.AjusteManualService
        java:app/emp-ejb/AjusteManualBean!br.gov.caixa.emprestimo.negocio.AjusteManualService
16:12:29,682 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AtualizaTblFIPENegocio' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/AtualizaTblFIPENegocio!br.gov.caixa.emprestimo.negocio.AtualizaTblFIPEService
        java:app/emp-ejb/AtualizaTblFIPENegocio!br.gov.caixa.emprestimo.negocio.AtualizaTblFIPEService
        java:global/emp-3.95.0.1-b1437/emp-ejb/AtualizaTblFIPENegocio
        java:app/emp-ejb/AtualizaTblFIPENegocio
16:12:29,682 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'FiancaBancariaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/FiancaBancariaBean!br.gov.caixa.emprestimo.negocio.FiancaBancariaBean
        java:app/emp-ejb/FiancaBancariaBean!br.gov.caixa.emprestimo.negocio.FiancaBancariaBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/FiancaBancariaBean!br.gov.caixa.emprestimo.negocio.FiancaBancariaService
        java:app/emp-ejb/FiancaBancariaBean!br.gov.caixa.emprestimo.negocio.FiancaBancariaService
16:12:29,682 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SubgrupoContabilBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/SubgrupoContabilBean!br.gov.caixa.emp.contabil.negocio.SubgrupoContabilBean
        java:app/emp-ejb/SubgrupoContabilBean!br.gov.caixa.emp.contabil.negocio.SubgrupoContabilBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/SubgrupoContabilBean
        java:app/emp-ejb/SubgrupoContabilBean
16:12:29,682 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ConsultaRemessaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/ConsultaRemessaBean!br.gov.caixa.emprestimo.negocio.ConsultaRemessaService
        java:app/emp-ejb/ConsultaRemessaBean!br.gov.caixa.emprestimo.negocio.ConsultaRemessaService
        java:global/emp-3.95.0.1-b1437/emp-ejb/ConsultaRemessaBean!br.gov.caixa.emprestimo.negocio.ConsultaRemessaBean
        java:app/emp-ejb/ConsultaRemessaBean!br.gov.caixa.emprestimo.negocio.ConsultaRemessaBean
16:12:29,682 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MomentoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/MomentoBean!br.gov.caixa.emp.contabil.negocio.MomentoBean
        java:app/emp-ejb/MomentoBean!br.gov.caixa.emp.contabil.negocio.MomentoBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/MomentoBean
        java:app/emp-ejb/MomentoBean
16:12:29,682 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoRiscoTimerBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/AvaliacaoRiscoTimerBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoTimerService
        java:app/emp-ejb/AvaliacaoRiscoTimerBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoTimerService
        java:global/emp-3.95.0.1-b1437/emp-ejb/AvaliacaoRiscoTimerBean
        java:app/emp-ejb/AvaliacaoRiscoTimerBean
16:12:29,682 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'PronampeReservaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/PronampeReservaBean!br.gov.caixa.emprestimo.negocio.PronampeReservaBean
        java:app/emp-ejb/PronampeReservaBean!br.gov.caixa.emprestimo.negocio.PronampeReservaBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/PronampeReservaBean!br.gov.caixa.emprestimo.negocio.PronampeReservaService
        java:app/emp-ejb/PronampeReservaBean!br.gov.caixa.emprestimo.negocio.PronampeReservaService
16:12:29,682 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoDeRiscoDAO' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/AvaliacaoDeRiscoDAO!br.gov.caixa.emprestimo.dao.AvaliacaoDeRiscoDAO
        java:app/emp-ejb/AvaliacaoDeRiscoDAO!br.gov.caixa.emprestimo.dao.AvaliacaoDeRiscoDAO
        java:global/emp-3.95.0.1-b1437/emp-ejb/AvaliacaoDeRiscoDAO
        java:app/emp-ejb/AvaliacaoDeRiscoDAO
16:12:29,682 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'CessaoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/CessaoBean!br.gov.caixa.emp.cessao.negocio.CessaoBean
        java:app/emp-ejb/CessaoBean!br.gov.caixa.emp.cessao.negocio.CessaoBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/CessaoBean!br.gov.caixa.emp.cessao.negocio.CessaoService
        java:app/emp-ejb/CessaoBean!br.gov.caixa.emp.cessao.negocio.CessaoService
16:12:29,682 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'VeiculosTotalizadorBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/VeiculosTotalizadorBean!br.gov.caixa.emprestimo.negocio.VeiculosTotalizadorBean
        java:app/emp-ejb/VeiculosTotalizadorBean!br.gov.caixa.emprestimo.negocio.VeiculosTotalizadorBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/VeiculosTotalizadorBean
        java:app/emp-ejb/VeiculosTotalizadorBean
16:12:29,682 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoRiscoVeiculosBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/AvaliacaoRiscoVeiculosBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoVeiculosService
        java:app/emp-ejb/AvaliacaoRiscoVeiculosBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoVeiculosService
        java:global/emp-3.95.0.1-b1437/emp-ejb/AvaliacaoRiscoVeiculosBean
        java:app/emp-ejb/AvaliacaoRiscoVeiculosBean
16:12:29,682 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MomentoRoteiroBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/MomentoRoteiroBean!br.gov.caixa.emp.contabil.negocio.MomentoRoteiroBean
        java:app/emp-ejb/MomentoRoteiroBean!br.gov.caixa.emp.contabil.negocio.MomentoRoteiroBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/MomentoRoteiroBean
        java:app/emp-ejb/MomentoRoteiroBean
16:12:29,683 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'GrupoContabilBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/GrupoContabilBean!br.gov.caixa.emp.contabil.negocio.GrupoContabilBean
        java:app/emp-ejb/GrupoContabilBean!br.gov.caixa.emp.contabil.negocio.GrupoContabilBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/GrupoContabilBean
        java:app/emp-ejb/GrupoContabilBean
16:12:29,683 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RelatorioBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/RelatorioBean!br.gov.caixa.emprestimo.negocio.RelatorioService
        java:app/emp-ejb/RelatorioBean!br.gov.caixa.emprestimo.negocio.RelatorioService
        java:global/emp-3.95.0.1-b1437/emp-ejb/RelatorioBean!br.gov.caixa.emprestimo.negocio.RelatorioBean
        java:app/emp-ejb/RelatorioBean!br.gov.caixa.emprestimo.negocio.RelatorioBean
16:12:29,683 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'VeiculosMatrizTaxasBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/VeiculosMatrizTaxasBean!br.gov.caixa.emprestimo.negocio.VeiculosMatrizTaxasService
        java:app/emp-ejb/VeiculosMatrizTaxasBean!br.gov.caixa.emprestimo.negocio.VeiculosMatrizTaxasService
        java:global/emp-3.95.0.1-b1437/emp-ejb/VeiculosMatrizTaxasBean!br.gov.caixa.emprestimo.negocio.VeiculosMatrizTaxasBean
        java:app/emp-ejb/VeiculosMatrizTaxasBean!br.gov.caixa.emprestimo.negocio.VeiculosMatrizTaxasBean
16:12:29,683 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RelatorioProrrogacaoPrazoContratoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/RelatorioProrrogacaoPrazoContratoBean!br.gov.caixa.emprestimo.negocio.RelatorioProrrogacaoPrazoContratoService
        java:app/emp-ejb/RelatorioProrrogacaoPrazoContratoBean!br.gov.caixa.emprestimo.negocio.RelatorioProrrogacaoPrazoContratoService
        java:global/emp-3.95.0.1-b1437/emp-ejb/RelatorioProrrogacaoPrazoContratoBean!br.gov.caixa.emprestimo.negocio.RelatorioProrrogacaoPrazoContratoBean
        java:app/emp-ejb/RelatorioProrrogacaoPrazoContratoBean!br.gov.caixa.emprestimo.negocio.RelatorioProrrogacaoPrazoContratoBean
16:12:29,683 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RenegociacaoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/RenegociacaoBean!br.gov.caixa.emprestimo.negocio.RenegociacaoBean
        java:app/emp-ejb/RenegociacaoBean!br.gov.caixa.emprestimo.negocio.RenegociacaoBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/RenegociacaoBean!br.gov.caixa.emprestimo.negocio.RenegociacaoService
        java:app/emp-ejb/RenegociacaoBean!br.gov.caixa.emprestimo.negocio.RenegociacaoService
16:12:29,683 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MapaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/MapaBean!br.gov.caixa.emp.contabil.negocio.MapaBean
        java:app/emp-ejb/MapaBean!br.gov.caixa.emp.contabil.negocio.MapaBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/MapaBean
        java:app/emp-ejb/MapaBean
16:12:29,683 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TabelaFipeBeanTimeService' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/TabelaFipeBeanTimeService!br.gov.caixa.emprestimo.negocio.TabelaFipeTimeService
        java:app/emp-ejb/TabelaFipeBeanTimeService!br.gov.caixa.emprestimo.negocio.TabelaFipeTimeService
        java:global/emp-3.95.0.1-b1437/emp-ejb/TabelaFipeBeanTimeService
        java:app/emp-ejb/TabelaFipeBeanTimeService
16:12:29,683 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'PortabilidadeBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.95.0.1-b1437.ear"' são como segue:
        java:global/emp-3.95.0.1-b1437/emp-ejb/PortabilidadeBean!br.gov.caixa.emprestimo.negocio.PortabilidadeBean
        java:app/emp-ejb/PortabilidadeBean!br.gov.caixa.emprestimo.negocio.PortabilidadeBean
        java:global/emp-3.95.0.1-b1437/emp-ejb/PortabilidadeBean!br.gov.caixa.emprestimo.negocio.PortabilidadeService
        java:app/emp-ejb/PortabilidadeBean!br.gov.caixa.emprestimo.negocio.PortabilidadeService
16:12:29,688 INFO  [org.jipijapa] (MSC service thread 1-8) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.95.0.1-b1437.ear#SIEMP-PU
16:12:29,688 INFO  [org.jipijapa] (MSC service thread 1-8) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.95.0.1-b1437.ear#fecDS
16:12:29,729 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 107) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'emp-3.95.0.1-b1437.ear#SIEMP-PU'
16:12:29,731 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 108) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'emp-3.95.0.1-b1437.ear#fecDS'
16:12:29,793 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 107) WFLYCLINF0002: Cache emp-3.95.0.1-b1437.ear.emp-web.war inicializado a partir do recipiente web
16:12:29,910 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase
16:12:29,911 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.95.0.1-b1437.ear/emp-ejb.jar#SiempEjbDB2
16:12:29,958 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 108) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase'
16:12:29,959 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 107) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'emp-3.95.0.1-b1437.ear/emp-ejb.jar#SiempEjbDB2'
16:12:30,204 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 108) WFLYCLINF0002: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.Unidade inicializado a partir do recipiente hibernate
16:12:30,204 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 107) WFLYCLINF0002: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.Unidade inicializado a partir do recipiente hibernate
16:12:30,206 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 108) WFLYCLINF0002: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.Unidade-pending-puts inicializado a partir do recipiente hibernate
16:12:30,206 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 107) WFLYCLINF0002: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.Unidade-pending-puts inicializado a partir do recipiente hibernate
16:12:30,208 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 107) WFLYCLINF0002: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.OrigemLancamento inicializado a partir do recipiente hibernate
16:12:30,208 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 108) WFLYCLINF0002: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.OrigemLancamento inicializado a partir do recipiente hibernate
16:12:30,210 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 108) WFLYCLINF0002: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.OrigemLancamento-pending-puts inicializado a partir do recipiente hibernate
16:12:30,210 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 107) WFLYCLINF0002: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.OrigemLancamento-pending-puts inicializado a partir do recipiente hibernate
16:12:30,316 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 4) WELD-000119: Not generating any bean definitions from br.gov.caixa.sifec.componentes.integracoes.fgi.bndes.rest.catalogo.invoker.ApiClient because of underlying class loading error: Type com.sun.jersey.multipart.BodyPart from [Module "deployment.emp-3.95.0.1-b1437.ear.emp-web.war" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:12:30,316 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 1) WELD-000119: Not generating any bean definitions from br.gov.caixa.sifec.componentes.integracoes.fgi.bndes.rest.client.envioanexo.EnviarAnexoV1Service because of underlying class loading error: Type com.sun.jersey.multipart.BodyPart from [Module "deployment.emp-3.95.0.1-b1437.ear.emp-web.war" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:12:30,318 WARN  [org.jboss.modules.define] (Weld Thread Pool -- 7) Failed to define class br.gov.caixa.sifec.componentes.integracoes.fgi.bndes.rest.client.envioanexo.CustomMultiPartWriter in Module "deployment.emp-3.95.0.1-b1437.ear.emp-web.war" from Service Module Loader: java.lang.NoClassDefFoundError: Failed to link br/gov/caixa/sifec/componentes/integracoes/fgi/bndes/rest/client/envioanexo/CustomMultiPartWriter (Module "deployment.emp-3.95.0.1-b1437.ear.emp-web.war" from Service Module Loader): com/sun/jersey/multipart/impl/MultiPartWriter
Caused by: java.lang.ClassNotFoundException: com.sun.jersey.multipart.impl.MultiPartWriter from [Module "deployment.emp-3.95.0.1-b1437.ear.emp-web.war" from Service Module Loader]
16:12:30,321 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 7) WELD-000119: Not generating any bean definitions from br.gov.caixa.sifec.componentes.integracoes.fgi.bndes.rest.client.envioanexo.CustomMultiPartWriter because of underlying class loading error: Type com.sun.jersey.multipart.impl.MultiPartWriter from [Module "deployment.emp-3.95.0.1-b1437.ear.emp-web.war" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:12:30,332 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 7) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.util.ArquillianHelper because of underlying class loading error: Type org.jboss.shrinkwrap.api.asset.Asset from [Module "deployment.emp-3.95.0.1-b1437.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:12:30,343 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 6) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.email.api.operacao.SendMail because of underlying class loading error: Type freemarker.template.TemplateException from [Module "deployment.emp-3.95.0.1-b1437.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:12:30,882 ERROR [org.jboss.msc.service.fail] (MSC service thread 1-4) MSC000001: Failed to start service jboss.deployment.unit."emp-3.95.0.1-b1437.ear".WeldStartService: org.jboss.msc.service.StartException in service jboss.deployment.unit."emp-3.95.0.1-b1437.ear".WeldStartService: Failed to start service
Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type VeiculosTotalizadorService with qualifiers @Default
16:12:30,886 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 103) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SIFEC-EMP")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"emp-3.95.0.1-b1437.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type VeiculosTotalizadorService with qualifiers @Default
16:12:30,886 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 103) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SIFEC-EMP")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"emp-3.95.0.1-b1437.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type VeiculosTotalizadorService with qualifiers @Default
16:12:30,887 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 103) WFLYSRV0021: O procedimento da implantação "emp-3.95.0.1-b1437.ear" foi revertido com mensagem de falha:
{"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"emp-3.95.0.1-b1437.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type VeiculosTotalizadorService with qualifiers @Default
16:12:30,888 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 107) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'emp-3.95.0.1-b1437.ear#SIEMP-PU'
16:12:30,888 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 108) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'emp-3.95.0.1-b1437.ear#fecDS'
16:12:30,891 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 110) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase'
16:12:30,892 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 107) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'emp-3.95.0.1-b1437.ear#fecDS'
16:12:30,892 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 108) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'emp-3.95.0.1-b1437.ear#SIEMP-PU'
16:12:30,894 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 110) WFLYCLINF0003: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.OrigemLancamento encerrado a partir do recipiente hibernate
16:12:30,895 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 110) WFLYCLINF0003: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.OrigemLancamento-pending-puts encerrado a partir do recipiente hibernate
16:12:30,896 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 108) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'emp-3.95.0.1-b1437.ear/emp-ejb.jar#SiempEjbDB2'
16:12:30,896 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 109) WFLYCLINF0003: Cache emp-3.95.0.1-b1437.ear.emp-web.war encerrado a partir do recipiente web
16:12:30,896 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 110) WFLYCLINF0003: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.Unidade encerrado a partir do recipiente hibernate
16:12:30,899 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 108) WFLYCLINF0003: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.OrigemLancamento encerrado a partir do recipiente hibernate
16:12:30,900 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 110) WFLYCLINF0003: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.Unidade-pending-puts encerrado a partir do recipiente hibernate
16:12:30,901 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 108) WFLYCLINF0003: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.OrigemLancamento-pending-puts encerrado a partir do recipiente hibernate
16:12:30,904 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 110) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'emp-3.95.0.1-b1437.ear/emp-ejb.jar#Siemp2EjbSybase'
16:12:30,904 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 108) WFLYCLINF0003: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.Unidade encerrado a partir do recipiente hibernate
16:12:30,904 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 108) WFLYCLINF0003: Cache emp-3.95.0.1-b1437.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.Unidade-pending-puts encerrado a partir do recipiente hibernate
16:12:30,905 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 108) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'emp-3.95.0.1-b1437.ear/emp-ejb.jar#SiempEjbDB2'
16:12:30,926 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-3) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: emp-ejb.jar) em 39ms
16:12:30,941 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: emp-api.war) em 54ms
16:12:30,952 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: emp-web.war) em 65ms
16:12:30,959 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0028: Implantação interrompida SIFEC-EMP (runtime-name: emp-3.95.0.1-b1437.ear) em 72ms

