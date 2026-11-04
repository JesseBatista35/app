deploy --name=SIFEC-EMP2 --server-groups=sifec-intranet



[domain@localhost:9443 /] deploy --name=SIFEC-EMP2 --server-groups=sifec-intranet
{"WFLYDC0074: Operation failed or was rolled back on all servers. Server failures:" => {"server-group" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx
473" => {"WFLYCTL0062: A operação de composição falhou e foi revertida. Segue abaixo as etapas que falharam:" => {"Operação step-2" => {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\
"emp-3.92.1.1-b1459.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type VeiculosTotalizadorService with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.emprestimo.rest.VeiculosRest.totalizadorService
  at br.gov.caixa.emprestimo.rest.VeiculosRest.totalizadorService(VeiculosRest.java:0)
"}}}}}}}}}}

[domain@localhost:9443 /]


ServerService Thread Pool -- 112) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'emp-3.95.0.1-b1458.ear#fecDS'
16:15:41,733 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 110) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'emp-3.95.0.1-b1458.ear#SIEMP-PU'
16:15:41,737 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 111) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'emp-3.95.0.1-b1458.ear/emp-ejb.jar#Siemp2EjbSybase'
16:15:41,738 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 111) WFLYCLINF0003: Cache emp-3.95.0.1-b1458.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.OrigemLancamento encerrado a partir do recipiente hibernate
16:15:41,738 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 111) WFLYCLINF0003: Cache emp-3.95.0.1-b1458.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.OrigemLancamento-pending-puts encerrado a partir do recipiente hibernate
16:15:41,739 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 112) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'emp-3.95.0.1-b1458.ear#fecDS'
16:15:41,739 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 112) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'emp-3.95.0.1-b1458.ear#SIEMP-PU'
16:15:41,739 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 110) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'emp-3.95.0.1-b1458.ear/emp-ejb.jar#SiempEjbDB2'
16:15:41,740 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 111) WFLYCLINF0003: Cache emp-3.95.0.1-b1458.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.Unidade encerrado a partir do recipiente hibernate
16:15:41,741 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 110) WFLYCLINF0003: Cache emp-3.95.0.1-b1458.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.OrigemLancamento encerrado a partir do recipiente hibernate
16:15:41,741 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 111) WFLYCLINF0003: Cache emp-3.95.0.1-b1458.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.Unidade-pending-puts encerrado a partir do recipiente hibernate
16:15:41,741 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 110) WFLYCLINF0003: Cache emp-3.95.0.1-b1458.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.OrigemLancamento-pending-puts encerrado a partir do recipiente hibernate
16:15:41,742 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 110) WFLYCLINF0003: Cache emp-3.95.0.1-b1458.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.Unidade encerrado a partir do recipiente hibernate
16:15:41,742 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 111) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'emp-3.95.0.1-b1458.ear/emp-ejb.jar#Siemp2EjbSybase'
16:15:41,742 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 110) WFLYCLINF0003: Cache emp-3.95.0.1-b1458.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.Unidade-pending-puts encerrado a partir do recipiente hibernate
16:15:41,743 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 110) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'emp-3.95.0.1-b1458.ear/emp-ejb.jar#SiempEjbDB2'
16:15:41,755 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 108) WFLYCLINF0003: Cache emp-3.95.0.1-b1458.ear.emp-web.war encerrado a partir do recipiente web
16:15:41,768 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: emp-ejb.jar) em 35ms
16:15:41,779 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-8) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: emp-api.war) em 45ms
16:15:41,792 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: emp-web.war) em 58ms
16:15:41,794 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0028: Implantação interrompida SIFEC-EMP4 (runtime-name: emp-3.95.0.1-b1458.ear) em 62ms
16:17:46,877 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-5) WFLYSRV0027: Iniciando a implantação do "SIFEC-EMP2" (runtime-name: "emp-3.92.1.1-b1459.ear")
16:17:47,679 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-6) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "emp-ejb.jar")
16:17:47,679 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-2) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "emp-web.war")
16:17:47,679 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-5) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "emp-api.war")
16:17:48,415 WARN  [org.jboss.as.server.deployment] (MSC service thread 1-4) WFLYSRV0059: A entrada do caminho da classe toolbox.jar em /content/emp-3.92.1.1-b1459.ear/emp-api.war/WEB-INF/lib/itext-2.0.8.jar não direciona a um jar válido para a referência do caminho da classe.
16:17:48,627 INFO  [org.jboss.as.jpa] (MSC service thread 1-2) WFLYJPA0002: Ler persistence.xml para SIEMP-PU
16:17:48,697 INFO  [org.jipijapa] (MSC service thread 1-1) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.92.1.1-b1459.ear#SIEMP-PU
16:17:48,697 INFO  [org.jipijapa] (MSC service thread 1-1) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.92.1.1-b1459.ear#fecDS
16:17:48,697 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 113) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'emp-3.92.1.1-b1459.ear#fecDS'
16:17:48,698 INFO  [org.jipijapa] (MSC service thread 1-1) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.92.1.1-b1459.ear/emp-ejb.jar#Siemp2EjbSybase
16:17:48,698 INFO  [org.jipijapa] (MSC service thread 1-1) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.92.1.1-b1459.ear/emp-ejb.jar#SiempEjbDB2
16:17:48,698 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 117) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'emp-3.92.1.1-b1459.ear/emp-ejb.jar#SiempEjbDB2'
16:17:48,698 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 111) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'emp-3.92.1.1-b1459.ear#SIEMP-PU'
16:17:48,698 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 116) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'emp-3.92.1.1-b1459.ear/emp-ejb.jar#Siemp2EjbSybase'
16:17:48,722 INFO  [org.jboss.weld.deployer] (MSC service thread 1-7) WFLYWELD0003: Processando da implantação weld emp-3.92.1.1-b1459.ear
16:17:48,743 INFO  [org.jboss.keycloak] (MSC service thread 1-1) Keycloak subsystem override for deployment emp-api.war
16:17:48,743 INFO  [org.jboss.weld.deployer] (MSC service thread 1-1) WFLYWELD0003: Processando da implantação weld emp-api.war
16:17:48,759 INFO  [org.jboss.keycloak] (MSC service thread 1-4) Keycloak subsystem override for deployment emp-web.war
16:17:48,760 INFO  [org.jboss.weld.deployer] (MSC service thread 1-4) WFLYWELD0003: Processando da implantação weld emp-web.war
16:17:48,825 INFO  [org.jboss.weld.deployer] (MSC service thread 1-2) WFLYWELD0003: Processando da implantação weld emp-ejb.jar
16:17:48,827 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RelatorioLancamentoContabilBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/RelatorioLancamentoContabilBean!br.gov.caixa.emprestimo.negocio.RelatorioLancamentoContabilBean
        java:app/emp-ejb/RelatorioLancamentoContabilBean!br.gov.caixa.emprestimo.negocio.RelatorioLancamentoContabilBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/RelatorioLancamentoContabilBean!br.gov.caixa.emprestimo.negocio.RelatorioLancamentoContabilService
        java:app/emp-ejb/RelatorioLancamentoContabilBean!br.gov.caixa.emprestimo.negocio.RelatorioLancamentoContabilService
16:17:48,827 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MoveBrasilBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/MoveBrasilBean!br.gov.caixa.emprestimo.negocio.MoveBrasilBean
        java:app/emp-ejb/MoveBrasilBean!br.gov.caixa.emprestimo.negocio.MoveBrasilBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/MoveBrasilBean!br.gov.caixa.emprestimo.negocio.MoveBrasilService
        java:app/emp-ejb/MoveBrasilBean!br.gov.caixa.emprestimo.negocio.MoveBrasilService
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RotinaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/RotinaBean!br.gov.caixa.emp.contabil.negocio.RotinaBean
        java:app/emp-ejb/RotinaBean!br.gov.caixa.emp.contabil.negocio.RotinaBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/RotinaBean
        java:app/emp-ejb/RotinaBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DAOBarramentoFactory' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/DAOBarramentoFactory!br.gov.caixa.emprestimo.barramento.dao.DAOBarramentoFactory
        java:app/emp-ejb/DAOBarramentoFactory!br.gov.caixa.emprestimo.barramento.dao.DAOBarramentoFactory
        java:global/emp-3.92.1.1-b1459/emp-ejb/DAOBarramentoFactory
        java:app/emp-ejb/DAOBarramentoFactory
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutorLog' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/ProdutorLog!br.gov.caixa.emprestimo.log.ProdutorLog
        java:app/emp-ejb/ProdutorLog!br.gov.caixa.emprestimo.log.ProdutorLog
        java:global/emp-3.92.1.1-b1459/emp-ejb/ProdutorLog
        java:app/emp-ejb/ProdutorLog
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoRiscoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/AvaliacaoRiscoBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoService
        java:app/emp-ejb/AvaliacaoRiscoBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoService
        java:global/emp-3.92.1.1-b1459/emp-ejb/AvaliacaoRiscoBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoBean
        java:app/emp-ejb/AvaliacaoRiscoBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SistemaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/SistemaBean!br.gov.caixa.emp.contabil.negocio.SistemaBean
        java:app/emp-ejb/SistemaBean!br.gov.caixa.emp.contabil.negocio.SistemaBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/SistemaBean
        java:app/emp-ejb/SistemaBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RelatorioConciliacaoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/RelatorioConciliacaoBean!br.gov.caixa.emp.contabil.negocio.RelatorioConciliacaoBean
        java:app/emp-ejb/RelatorioConciliacaoBean!br.gov.caixa.emp.contabil.negocio.RelatorioConciliacaoBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/RelatorioConciliacaoBean
        java:app/emp-ejb/RelatorioConciliacaoBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'VeiculosFipeBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/VeiculosFipeBean!br.gov.caixa.emprestimo.negocio.VeiculosFipeBean
        java:app/emp-ejb/VeiculosFipeBean!br.gov.caixa.emprestimo.negocio.VeiculosFipeBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/VeiculosFipeBean!br.gov.caixa.emprestimo.negocio.VeiculosFipeService
        java:app/emp-ejb/VeiculosFipeBean!br.gov.caixa.emprestimo.negocio.VeiculosFipeService
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ServicosBndesBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/ServicosBndesBean!br.gov.caixa.emprestimo.negocio.ServicosBndesService
        java:app/emp-ejb/ServicosBndesBean!br.gov.caixa.emprestimo.negocio.ServicosBndesService
        java:global/emp-3.92.1.1-b1459/emp-ejb/ServicosBndesBean!br.gov.caixa.emprestimo.negocio.ServicosBndesBean
        java:app/emp-ejb/ServicosBndesBean!br.gov.caixa.emprestimo.negocio.ServicosBndesBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EntidadeBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/EntidadeBean!br.gov.caixa.emp.contabil.negocio.EntidadeBean
        java:app/emp-ejb/EntidadeBean!br.gov.caixa.emp.contabil.negocio.EntidadeBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/EntidadeBean
        java:app/emp-ejb/EntidadeBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'UnidadeBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/UnidadeBean!br.gov.caixa.emp.contabil.negocio.UnidadeBean
        java:app/emp-ejb/UnidadeBean!br.gov.caixa.emp.contabil.negocio.UnidadeBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/UnidadeBean
        java:app/emp-ejb/UnidadeBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RelatorioSaidaSinafBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/RelatorioSaidaSinafBean!br.gov.caixa.emp.contabil.negocio.RelatorioSaidaSinafBean
        java:app/emp-ejb/RelatorioSaidaSinafBean!br.gov.caixa.emp.contabil.negocio.RelatorioSaidaSinafBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/RelatorioSaidaSinafBean
        java:app/emp-ejb/RelatorioSaidaSinafBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SituacaoMapaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/SituacaoMapaBean!br.gov.caixa.emp.contabil.negocio.SituacaoMapaBean
        java:app/emp-ejb/SituacaoMapaBean!br.gov.caixa.emp.contabil.negocio.SituacaoMapaBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/SituacaoMapaBean
        java:app/emp-ejb/SituacaoMapaBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'GiroCaixaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/GiroCaixaBean!br.gov.caixa.emprestimo.negocio.GiroCaixaService
        java:app/emp-ejb/GiroCaixaBean!br.gov.caixa.emprestimo.negocio.GiroCaixaService
        java:global/emp-3.92.1.1-b1459/emp-ejb/GiroCaixaBean!br.gov.caixa.emprestimo.negocio.GiroCaixaBean
        java:app/emp-ejb/GiroCaixaBean!br.gov.caixa.emprestimo.negocio.GiroCaixaBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EventoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/EventoBean!br.gov.caixa.emp.contabil.negocio.EventoBean
        java:app/emp-ejb/EventoBean!br.gov.caixa.emp.contabil.negocio.EventoBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/EventoBean
        java:app/emp-ejb/EventoBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TimerServiceTestBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/TimerServiceTestBean!br.gov.caixa.emprestimo.negocio.TimerServiceTest
        java:app/emp-ejb/TimerServiceTestBean!br.gov.caixa.emprestimo.negocio.TimerServiceTest
        java:global/emp-3.92.1.1-b1459/emp-ejb/TimerServiceTestBean
        java:app/emp-ejb/TimerServiceTestBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'VeiculosBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/VeiculosBean!br.gov.caixa.emprestimo.negocio.VeiculosService
        java:app/emp-ejb/VeiculosBean!br.gov.caixa.emprestimo.negocio.VeiculosService
        java:global/emp-3.92.1.1-b1459/emp-ejb/VeiculosBean!br.gov.caixa.emprestimo.negocio.VeiculosBean
        java:app/emp-ejb/VeiculosBean!br.gov.caixa.emprestimo.negocio.VeiculosBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'PeriodicidadeBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/PeriodicidadeBean!br.gov.caixa.emp.contabil.negocio.PeriodicidadeBean
        java:app/emp-ejb/PeriodicidadeBean!br.gov.caixa.emp.contabil.negocio.PeriodicidadeBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/PeriodicidadeBean
        java:app/emp-ejb/PeriodicidadeBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'BndesBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/BndesBean!br.gov.caixa.emprestimo.negocio.BndesService
        java:app/emp-ejb/BndesBean!br.gov.caixa.emprestimo.negocio.BndesService
        java:global/emp-3.92.1.1-b1459/emp-ejb/BndesBean!br.gov.caixa.emprestimo.negocio.BndesBean
        java:app/emp-ejb/BndesBean!br.gov.caixa.emprestimo.negocio.BndesBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'OrigemLancamentoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/OrigemLancamentoBean!br.gov.caixa.emp.contabil.negocio.OrigemLancamentoBean
        java:app/emp-ejb/OrigemLancamentoBean!br.gov.caixa.emp.contabil.negocio.OrigemLancamentoBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/OrigemLancamentoBean
        java:app/emp-ejb/OrigemLancamentoBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'VeiculosTabelaAliquotaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/VeiculosTabelaAliquotaBean!br.gov.caixa.emprestimo.negocio.VeiculosTabelaAliquotaService
        java:app/emp-ejb/VeiculosTabelaAliquotaBean!br.gov.caixa.emprestimo.negocio.VeiculosTabelaAliquotaService
        java:global/emp-3.92.1.1-b1459/emp-ejb/VeiculosTabelaAliquotaBean!br.gov.caixa.emprestimo.negocio.VeiculosTabelaAliquotaBean
        java:app/emp-ejb/VeiculosTabelaAliquotaBean!br.gov.caixa.emprestimo.negocio.VeiculosTabelaAliquotaBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/ProdutoBean!br.gov.caixa.emp.contabil.negocio.ProdutoBean
        java:app/emp-ejb/ProdutoBean!br.gov.caixa.emp.contabil.negocio.ProdutoBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/ProdutoBean
        java:app/emp-ejb/ProdutoBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RelatorioEspecificacaoResumidaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/RelatorioEspecificacaoResumidaBean!br.gov.caixa.emp.contabil.negocio.RelatorioEspecificacaoResumidaBean
        java:app/emp-ejb/RelatorioEspecificacaoResumidaBean!br.gov.caixa.emp.contabil.negocio.RelatorioEspecificacaoResumidaBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/RelatorioEspecificacaoResumidaBean
        java:app/emp-ejb/RelatorioEspecificacaoResumidaBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AjusteManualBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/AjusteManualBean!br.gov.caixa.emprestimo.negocio.AjusteManualBean
        java:app/emp-ejb/AjusteManualBean!br.gov.caixa.emprestimo.negocio.AjusteManualBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/AjusteManualBean!br.gov.caixa.emprestimo.negocio.AjusteManualService
        java:app/emp-ejb/AjusteManualBean!br.gov.caixa.emprestimo.negocio.AjusteManualService
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AtualizaTblFIPENegocio' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/AtualizaTblFIPENegocio!br.gov.caixa.emprestimo.negocio.AtualizaTblFIPEService
        java:app/emp-ejb/AtualizaTblFIPENegocio!br.gov.caixa.emprestimo.negocio.AtualizaTblFIPEService
        java:global/emp-3.92.1.1-b1459/emp-ejb/AtualizaTblFIPENegocio
        java:app/emp-ejb/AtualizaTblFIPENegocio
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'FiancaBancariaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/FiancaBancariaBean!br.gov.caixa.emprestimo.negocio.FiancaBancariaBean
        java:app/emp-ejb/FiancaBancariaBean!br.gov.caixa.emprestimo.negocio.FiancaBancariaBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/FiancaBancariaBean!br.gov.caixa.emprestimo.negocio.FiancaBancariaService
        java:app/emp-ejb/FiancaBancariaBean!br.gov.caixa.emprestimo.negocio.FiancaBancariaService
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SubgrupoContabilBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/SubgrupoContabilBean!br.gov.caixa.emp.contabil.negocio.SubgrupoContabilBean
        java:app/emp-ejb/SubgrupoContabilBean!br.gov.caixa.emp.contabil.negocio.SubgrupoContabilBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/SubgrupoContabilBean
        java:app/emp-ejb/SubgrupoContabilBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ConsultaRemessaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/ConsultaRemessaBean!br.gov.caixa.emprestimo.negocio.ConsultaRemessaService
        java:app/emp-ejb/ConsultaRemessaBean!br.gov.caixa.emprestimo.negocio.ConsultaRemessaService
        java:global/emp-3.92.1.1-b1459/emp-ejb/ConsultaRemessaBean!br.gov.caixa.emprestimo.negocio.ConsultaRemessaBean
        java:app/emp-ejb/ConsultaRemessaBean!br.gov.caixa.emprestimo.negocio.ConsultaRemessaBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MomentoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/MomentoBean!br.gov.caixa.emp.contabil.negocio.MomentoBean
        java:app/emp-ejb/MomentoBean!br.gov.caixa.emp.contabil.negocio.MomentoBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/MomentoBean
        java:app/emp-ejb/MomentoBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoRiscoTimerBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/AvaliacaoRiscoTimerBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoTimerService
        java:app/emp-ejb/AvaliacaoRiscoTimerBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoTimerService
        java:global/emp-3.92.1.1-b1459/emp-ejb/AvaliacaoRiscoTimerBean
        java:app/emp-ejb/AvaliacaoRiscoTimerBean
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'PronampeReservaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/PronampeReservaBean!br.gov.caixa.emprestimo.negocio.PronampeReservaBean
        java:app/emp-ejb/PronampeReservaBean!br.gov.caixa.emprestimo.negocio.PronampeReservaBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/PronampeReservaBean!br.gov.caixa.emprestimo.negocio.PronampeReservaService
        java:app/emp-ejb/PronampeReservaBean!br.gov.caixa.emprestimo.negocio.PronampeReservaService
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoDeRiscoDAO' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/AvaliacaoDeRiscoDAO!br.gov.caixa.emprestimo.dao.AvaliacaoDeRiscoDAO
        java:app/emp-ejb/AvaliacaoDeRiscoDAO!br.gov.caixa.emprestimo.dao.AvaliacaoDeRiscoDAO
        java:global/emp-3.92.1.1-b1459/emp-ejb/AvaliacaoDeRiscoDAO
        java:app/emp-ejb/AvaliacaoDeRiscoDAO
16:17:48,828 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'CessaoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/CessaoBean!br.gov.caixa.emp.cessao.negocio.CessaoBean
        java:app/emp-ejb/CessaoBean!br.gov.caixa.emp.cessao.negocio.CessaoBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/CessaoBean!br.gov.caixa.emp.cessao.negocio.CessaoService
        java:app/emp-ejb/CessaoBean!br.gov.caixa.emp.cessao.negocio.CessaoService
16:17:48,829 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'VeiculosTotalizadorBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/VeiculosTotalizadorBean!br.gov.caixa.emprestimo.negocio.VeiculosTotalizadorBean
        java:app/emp-ejb/VeiculosTotalizadorBean!br.gov.caixa.emprestimo.negocio.VeiculosTotalizadorBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/VeiculosTotalizadorBean
        java:app/emp-ejb/VeiculosTotalizadorBean
16:17:48,829 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoRiscoVeiculosBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/AvaliacaoRiscoVeiculosBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoVeiculosService
        java:app/emp-ejb/AvaliacaoRiscoVeiculosBean!br.gov.caixa.emprestimo.negocio.AvaliacaoRiscoVeiculosService
        java:global/emp-3.92.1.1-b1459/emp-ejb/AvaliacaoRiscoVeiculosBean
        java:app/emp-ejb/AvaliacaoRiscoVeiculosBean
16:17:48,829 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MomentoRoteiroBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/MomentoRoteiroBean!br.gov.caixa.emp.contabil.negocio.MomentoRoteiroBean
        java:app/emp-ejb/MomentoRoteiroBean!br.gov.caixa.emp.contabil.negocio.MomentoRoteiroBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/MomentoRoteiroBean
        java:app/emp-ejb/MomentoRoteiroBean
16:17:48,829 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'GrupoContabilBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/GrupoContabilBean!br.gov.caixa.emp.contabil.negocio.GrupoContabilBean
        java:app/emp-ejb/GrupoContabilBean!br.gov.caixa.emp.contabil.negocio.GrupoContabilBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/GrupoContabilBean
        java:app/emp-ejb/GrupoContabilBean
16:17:48,829 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RelatorioBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/RelatorioBean!br.gov.caixa.emprestimo.negocio.RelatorioService
        java:app/emp-ejb/RelatorioBean!br.gov.caixa.emprestimo.negocio.RelatorioService
        java:global/emp-3.92.1.1-b1459/emp-ejb/RelatorioBean!br.gov.caixa.emprestimo.negocio.RelatorioBean
        java:app/emp-ejb/RelatorioBean!br.gov.caixa.emprestimo.negocio.RelatorioBean
16:17:48,829 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'VeiculosMatrizTaxasBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/VeiculosMatrizTaxasBean!br.gov.caixa.emprestimo.negocio.VeiculosMatrizTaxasService
        java:app/emp-ejb/VeiculosMatrizTaxasBean!br.gov.caixa.emprestimo.negocio.VeiculosMatrizTaxasService
        java:global/emp-3.92.1.1-b1459/emp-ejb/VeiculosMatrizTaxasBean!br.gov.caixa.emprestimo.negocio.VeiculosMatrizTaxasBean
        java:app/emp-ejb/VeiculosMatrizTaxasBean!br.gov.caixa.emprestimo.negocio.VeiculosMatrizTaxasBean
16:17:48,829 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RelatorioProrrogacaoPrazoContratoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/RelatorioProrrogacaoPrazoContratoBean!br.gov.caixa.emprestimo.negocio.RelatorioProrrogacaoPrazoContratoService
        java:app/emp-ejb/RelatorioProrrogacaoPrazoContratoBean!br.gov.caixa.emprestimo.negocio.RelatorioProrrogacaoPrazoContratoService
        java:global/emp-3.92.1.1-b1459/emp-ejb/RelatorioProrrogacaoPrazoContratoBean!br.gov.caixa.emprestimo.negocio.RelatorioProrrogacaoPrazoContratoBean
        java:app/emp-ejb/RelatorioProrrogacaoPrazoContratoBean!br.gov.caixa.emprestimo.negocio.RelatorioProrrogacaoPrazoContratoBean
16:17:48,829 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RenegociacaoBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/RenegociacaoBean!br.gov.caixa.emprestimo.negocio.RenegociacaoBean
        java:app/emp-ejb/RenegociacaoBean!br.gov.caixa.emprestimo.negocio.RenegociacaoBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/RenegociacaoBean!br.gov.caixa.emprestimo.negocio.RenegociacaoService
        java:app/emp-ejb/RenegociacaoBean!br.gov.caixa.emprestimo.negocio.RenegociacaoService
16:17:48,829 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MapaBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/MapaBean!br.gov.caixa.emp.contabil.negocio.MapaBean
        java:app/emp-ejb/MapaBean!br.gov.caixa.emp.contabil.negocio.MapaBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/MapaBean
        java:app/emp-ejb/MapaBean
16:17:48,829 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TabelaFipeBeanTimeService' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/TabelaFipeBeanTimeService!br.gov.caixa.emprestimo.negocio.TabelaFipeTimeService
        java:app/emp-ejb/TabelaFipeBeanTimeService!br.gov.caixa.emprestimo.negocio.TabelaFipeTimeService
        java:global/emp-3.92.1.1-b1459/emp-ejb/TabelaFipeBeanTimeService
        java:app/emp-ejb/TabelaFipeBeanTimeService
16:17:48,829 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-2) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'PortabilidadeBean' na unidade de implementação 'subdeployment "emp-ejb.jar" of deployment "emp-3.92.1.1-b1459.ear"' são como segue:
        java:global/emp-3.92.1.1-b1459/emp-ejb/PortabilidadeBean!br.gov.caixa.emprestimo.negocio.PortabilidadeBean
        java:app/emp-ejb/PortabilidadeBean!br.gov.caixa.emprestimo.negocio.PortabilidadeBean
        java:global/emp-3.92.1.1-b1459/emp-ejb/PortabilidadeBean!br.gov.caixa.emprestimo.negocio.PortabilidadeService
        java:app/emp-ejb/PortabilidadeBean!br.gov.caixa.emprestimo.negocio.PortabilidadeService
16:17:48,833 INFO  [org.jipijapa] (MSC service thread 1-7) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.92.1.1-b1459.ear#SIEMP-PU
16:17:48,833 INFO  [org.jipijapa] (MSC service thread 1-7) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.92.1.1-b1459.ear#fecDS
16:17:48,906 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 111) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'emp-3.92.1.1-b1459.ear#SIEMP-PU'
16:17:48,914 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 113) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'emp-3.92.1.1-b1459.ear#fecDS'
16:17:48,926 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 118) WFLYCLINF0002: Cache emp-3.92.1.1-b1459.ear.emp-web.war inicializado a partir do recipiente web
16:17:49,071 INFO  [org.jipijapa] (MSC service thread 1-6) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.92.1.1-b1459.ear/emp-ejb.jar#Siemp2EjbSybase
16:17:49,071 INFO  [org.jipijapa] (MSC service thread 1-6) JIPIORMV53020253: Cache de segundo nível habilitado para emp-3.92.1.1-b1459.ear/emp-ejb.jar#SiempEjbDB2
16:17:49,120 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 117) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'emp-3.92.1.1-b1459.ear/emp-ejb.jar#SiempEjbDB2'
16:17:49,122 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 116) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'emp-3.92.1.1-b1459.ear/emp-ejb.jar#Siemp2EjbSybase'
16:17:49,335 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 117) WFLYCLINF0002: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.OrigemLancamento inicializado a partir do recipiente hibernate
16:17:49,337 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 117) WFLYCLINF0002: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.OrigemLancamento-pending-puts inicializado a partir do recipiente hibernate
16:17:49,338 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 117) WFLYCLINF0002: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.Unidade inicializado a partir do recipiente hibernate
16:17:49,339 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 117) WFLYCLINF0002: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.Unidade-pending-puts inicializado a partir do recipiente hibernate
16:17:49,345 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 116) WFLYCLINF0002: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.Unidade inicializado a partir do recipiente hibernate
16:17:49,347 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 116) WFLYCLINF0002: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.Unidade-pending-puts inicializado a partir do recipiente hibernate
16:17:49,349 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 116) WFLYCLINF0002: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.OrigemLancamento inicializado a partir do recipiente hibernate
16:17:49,350 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 116) WFLYCLINF0002: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.OrigemLancamento-pending-puts inicializado a partir do recipiente hibernate
16:17:49,529 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 2) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.util.ArquillianHelper because of underlying class loading error: Type org.jboss.shrinkwrap.api.asset.Asset from [Module "deployment.emp-3.92.1.1-b1459.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:17:49,537 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 2) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.email.api.operacao.SendMail because of underlying class loading error: Type freemarker.template.TemplateException from [Module "deployment.emp-3.92.1.1-b1459.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:17:49,586 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 5) WELD-000119: Not generating any bean definitions from br.gov.caixa.sifec.componentes.integracoes.fgi.bndes.rest.client.envioanexo.EnviarAnexoV1Service because of underlying class loading error: Type com.sun.jersey.multipart.BodyPart from [Module "deployment.emp-3.92.1.1-b1459.ear.emp-web.war" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:17:49,587 WARN  [org.jboss.modules.define] (Weld Thread Pool -- 3) Failed to define class br.gov.caixa.sifec.componentes.integracoes.fgi.bndes.rest.client.envioanexo.CustomMultiPartWriter in Module "deployment.emp-3.92.1.1-b1459.ear.emp-web.war" from Service Module Loader: java.lang.NoClassDefFoundError: Failed to link br/gov/caixa/sifec/componentes/integracoes/fgi/bndes/rest/client/envioanexo/CustomMultiPartWriter (Module "deployment.emp-3.92.1.1-b1459.ear.emp-web.war" from Service Module Loader): com/sun/jersey/multipart/impl/MultiPartWriter
Caused by: java.lang.ClassNotFoundException: com.sun.jersey.multipart.impl.MultiPartWriter from [Module "deployment.emp-3.92.1.1-b1459.ear.emp-web.war" from Service Module Loader]
16:17:49,589 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 7) WELD-000119: Not generating any bean definitions from br.gov.caixa.sifec.componentes.integracoes.fgi.bndes.rest.catalogo.invoker.ApiClient because of underlying class loading error: Type com.sun.jersey.multipart.BodyPart from [Module "deployment.emp-3.92.1.1-b1459.ear.emp-web.war" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:17:49,591 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 3) WELD-000119: Not generating any bean definitions from br.gov.caixa.sifec.componentes.integracoes.fgi.bndes.rest.client.envioanexo.CustomMultiPartWriter because of underlying class loading error: Type com.sun.jersey.multipart.impl.MultiPartWriter from [Module "deployment.emp-3.92.1.1-b1459.ear.emp-web.war" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:17:50,124 ERROR [org.jboss.msc.service.fail] (MSC service thread 1-1) MSC000001: Failed to start service jboss.deployment.unit."emp-3.92.1.1-b1459.ear".WeldStartService: org.jboss.msc.service.StartException in service jboss.deployment.unit."emp-3.92.1.1-b1459.ear".WeldStartService: Failed to start service
Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type VeiculosTotalizadorService with qualifiers @Default
16:17:50,128 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 103) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SIFEC-EMP2")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"emp-3.92.1.1-b1459.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type VeiculosTotalizadorService with qualifiers @Default
16:17:50,128 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 103) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SIFEC-EMP2")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"emp-3.92.1.1-b1459.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type VeiculosTotalizadorService with qualifiers @Default
16:17:50,128 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 103) WFLYSRV0021: O procedimento da implantação "emp-3.92.1.1-b1459.ear" foi revertido com mensagem de falha:
{"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"emp-3.92.1.1-b1459.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type VeiculosTotalizadorService with qualifiers @Default
16:17:50,130 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 116) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'emp-3.92.1.1-b1459.ear#fecDS'
16:17:50,130 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 117) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'emp-3.92.1.1-b1459.ear#SIEMP-PU'
16:17:50,132 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 118) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'emp-3.92.1.1-b1459.ear/emp-ejb.jar#SiempEjbDB2'
16:17:50,134 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 113) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'emp-3.92.1.1-b1459.ear/emp-ejb.jar#Siemp2EjbSybase'
16:17:50,135 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 118) WFLYCLINF0003: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.OrigemLancamento encerrado a partir do recipiente hibernate
16:17:50,135 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 113) WFLYCLINF0003: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.OrigemLancamento encerrado a partir do recipiente hibernate
16:17:50,136 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 116) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'emp-3.92.1.1-b1459.ear#fecDS'
16:17:50,136 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 116) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'emp-3.92.1.1-b1459.ear#SIEMP-PU'
16:17:50,136 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 118) WFLYCLINF0003: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.OrigemLancamento-pending-puts encerrado a partir do recipiente hibernate
16:17:50,136 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 113) WFLYCLINF0003: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.OrigemLancamento-pending-puts encerrado a partir do recipiente hibernate
16:17:50,137 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 118) WFLYCLINF0003: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.Unidade encerrado a partir do recipiente hibernate
16:17:50,137 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 113) WFLYCLINF0003: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.Unidade encerrado a partir do recipiente hibernate
16:17:50,137 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 118) WFLYCLINF0003: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#SiempEjbDB2.br.gov.caixa.emp.contabil.dominio.Unidade-pending-puts encerrado a partir do recipiente hibernate
16:17:50,137 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 113) WFLYCLINF0003: Cache emp-3.92.1.1-b1459.ear/emp-ejb.jar#Siemp2EjbSybase.br.gov.caixa.emp.contabil.dominio.Unidade-pending-puts encerrado a partir do recipiente hibernate
16:17:50,138 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 118) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'emp-3.92.1.1-b1459.ear/emp-ejb.jar#Siemp2EjbSybase'
16:17:50,138 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 113) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'emp-3.92.1.1-b1459.ear/emp-ejb.jar#SiempEjbDB2'
16:17:50,144 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 111) WFLYCLINF0003: Cache emp-3.92.1.1-b1459.ear.emp-web.war encerrado a partir do recipiente web
16:17:50,162 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: emp-ejb.jar) em 33ms
16:17:50,170 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-6) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: emp-api.war) em 41ms
16:17:50,189 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-8) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: emp-web.war) em 61ms
16:17:50,195 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-8) WFLYSRV0028: Implantação interrompida SIFEC-EMP2 (runtime-name: emp-3.92.1.1-b1459.ear) em 66ms

