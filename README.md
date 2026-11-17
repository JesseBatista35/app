
[root@cbrdeapllx473 p585600]# tail -f $LOG | grep -aE "originacao|WFLYSRV00(10|21)|WFLYCTL0013|WFLYCTL0412|WELD-0014|ERROR|Contexto web registrado"
16:37:40,180 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 115) WFLYUT0021: Contexto web registrado: '/garantias-web' para servidor 'default-server'
16:37:40,858 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 116) WFLYSRV0010: "SIFEC-GARANTIAS4" foi implantado (runtime-name: "garantias-1.8.0.3-b183.ear")
16:40:00,868 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0027: Iniciando a implantação do "SIFEC-ORIGINACAO2" (runtime-name: "sifec-originacao-3.11.1-b344.ear")
16:40:02,976 WARN  [org.jboss.as.server.deployment] (MSC service thread 1-4) WFLYSRV0059: A entrada do caminho da classe log4j.jar em /content/sifec-originacao-3.11.1-b344.ear/lib/commons-logging-1.0.2.jar não direciona a um jar válido para a referência do caminho da classe.
16:40:02,976 WARN  [org.jboss.as.server.deployment] (MSC service thread 1-4) WFLYSRV0059: A entrada do caminho da classe log4j-core.jar em /content/sifec-originacao-3.11.1-b344.ear/lib/commons-logging-1.0.2.jar não direciona a um jar válido para a referência do caminho da classe.
16:40:03,686 WARN  [org.jboss.as.dependency.unsupported] (MSC service thread 1-5) WFLYSRV0019: A implantação "deployment.sifec-originacao-3.11.1-b344.ear.ori-ejb.jar" está usando um módulo não compatível ("org.joda.time") que pode ser alterado ou removido em versões futuras sem nenhum aviso.
16:40:03,686 WARN  [org.jboss.as.dependency.private] (MSC service thread 1-5) WFLYSRV0018: A implantação "deployment.sifec-originacao-3.11.1-b344.ear.ori-ejb.jar" está usando um módulo privado ("org.codehaus.jackson.jackson-mapper-asl") que pode ser alterado ou removido em versões futuras sem nenhum aviso.
16:40:03,687 WARN  [org.jboss.as.dependency.private] (MSC service thread 1-7) WFLYSRV0018: A implantação "deployment.sifec-originacao-3.11.1-b344.ear" está usando um módulo privado ("org.codehaus.jackson.jackson-mapper-asl") que pode ser alterado ou removido em versões futuras sem nenhum aviso.
16:40:03,687 WARN  [org.jboss.as.dependency.unsupported] (MSC service thread 1-7) WFLYSRV0019: A implantação "deployment.sifec-originacao-3.11.1-b344.ear" está usando um módulo não compatível ("org.joda.time") que pode ser alterado ou removido em versões futuras sem nenhum aviso.
16:40:03,687 WARN  [org.jboss.as.dependency.unsupported] (MSC service thread 1-7) WFLYSRV0019: A implantação "deployment.sifec-originacao-3.11.1-b344.ear" está usando um módulo não compatível ("org.joda.time") que pode ser alterado ou removido em versões futuras sem nenhum aviso.
16:40:03,687 WARN  [org.jboss.as.dependency.private] (MSC service thread 1-7) WFLYSRV0018: A implantação "deployment.sifec-originacao-3.11.1-b344.ear" está usando um módulo privado ("org.codehaus.jackson.jackson-mapper-asl") que pode ser alterado ou removido em versões futuras sem nenhum aviso.
16:40:03,743 INFO  [org.jipijapa] (MSC service thread 1-8) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-originacao-3.11.1-b344.ear#Componente-Calculo-PU
16:40:03,744 INFO  [org.jipijapa] (MSC service thread 1-8) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-originacao-3.11.1-b344.ear#SIEMP-PU
16:40:03,745 INFO  [org.jipijapa] (MSC service thread 1-8) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-originacao-3.11.1-b344.ear#fecDS
16:40:03,748 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 110) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'sifec-originacao-3.11.1-b344.ear#Componente-Calculo-PU'
16:40:03,749 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 115) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'sifec-originacao-3.11.1-b344.ear#fecDS'
16:40:03,750 INFO  [org.jipijapa] (MSC service thread 1-8) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-originacao-3.11.1-b344.ear/ori-ejb.jar#default
16:40:03,759 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 120) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'sifec-originacao-3.11.1-b344.ear#SIEMP-PU'
16:40:03,761 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 121) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'sifec-originacao-3.11.1-b344.ear/ori-ejb.jar#default'
16:40:03,788 WARN  [org.jboss.as.dependency.unsupported] (MSC service thread 1-5) WFLYSRV0019: A implantação "deployment.sifec-originacao-3.11.1-b344.ear.ori-web.war" está usando um módulo não compatível ("org.joda.time") que pode ser alterado ou removido em versões futuras sem nenhum aviso.
16:40:03,789 WARN  [org.jboss.as.dependency.private] (MSC service thread 1-5) WFLYSRV0018: A implantação "deployment.sifec-originacao-3.11.1-b344.ear.ori-web.war" está usando um módulo privado ("org.codehaus.jackson.jackson-mapper-asl") que pode ser alterado ou removido em versões futuras sem nenhum aviso.
16:40:03,798 INFO  [org.jboss.weld.deployer] (MSC service thread 1-7) WFLYWELD0003: Processando da implantação weld sifec-originacao-3.11.1-b344.ear
16:40:03,990 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DashboardContratosService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/DashboardContratosService!br.gov.caixa.ori.negocio.DashboardContratosService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/DashboardContratosService
16:40:03,990 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutoAtualizacaoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ProdutoAtualizacaoService!br.gov.caixa.ori.negocio.ProdutoAtualizacaoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ProdutoAtualizacaoService
16:40:03,990 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TipoModeloService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/TipoModeloService!br.gov.caixa.ori.negocio.TipoModeloService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/TipoModeloService
16:40:03,990 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TaxaSeguroPrestamistaService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/TaxaSeguroPrestamistaService!br.gov.caixa.ori.negocio.TaxaSeguroPrestamistaService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/TaxaSeguroPrestamistaService
16:40:03,990 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RetornoPesquisaCadastralService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/RetornoPesquisaCadastralService!br.gov.caixa.ori.negocio.RetornoPesquisaCadastralService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/RetornoPesquisaCadastralService
16:40:03,990 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ControleExecucaoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ControleExecucaoService!br.gov.caixa.ori.negocio.ControleExecucaoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ControleExecucaoService
16:40:03,990 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TaxaIOFService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/TaxaIOFService!br.gov.caixa.ori.negocio.TaxaIOFService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/TaxaIOFService
16:40:03,990 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SaldoOrigemRecursoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/SaldoOrigemRecursoService!br.gov.caixa.ori.negocio.SaldoOrigemRecursoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/SaldoOrigemRecursoService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'OrigemRecursoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/OrigemRecursoService!br.gov.caixa.ori.negocio.OrigemRecursoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/OrigemRecursoService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SituacaoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/SituacaoService!br.gov.caixa.ori.negocio.SituacaoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/SituacaoService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'PerguntaAutorizacaoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/PerguntaAutorizacaoService!br.gov.caixa.ori.negocio.PerguntaAutorizacaoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/PerguntaAutorizacaoService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ProdutoService!br.gov.caixa.ori.negocio.ProdutoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ProdutoService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProcuradorService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ProcuradorService!br.gov.caixa.ori.negocio.ProcuradorService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ProcuradorService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ImpressaoContratoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ImpressaoContratoService!br.gov.caixa.ori.negocio.iface.ImpressaoContratoServiceIface
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ImpressaoContratoService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MunicipioService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/MunicipioService!br.gov.caixa.ori.negocio.MunicipioService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/MunicipioService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ExcepcionacaoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ExcepcionacaoService!br.gov.caixa.ori.negocio.ExcepcionacaoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ExcepcionacaoService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SistemaService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/SistemaService!br.gov.caixa.ori.negocio.SistemaService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/SistemaService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'OrikaProducer' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/OrikaProducer!br.gov.caixa.ori.common.OrikaProducer
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/OrikaProducer
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'NacionalidadeService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/NacionalidadeService!br.gov.caixa.ori.negocio.NacionalidadeService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/NacionalidadeService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ContratoNovadoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ContratoNovadoService!br.gov.caixa.ori.negocio.ContratoNovadoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ContratoNovadoService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ClienteService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ClienteService!br.gov.caixa.ori.negocio.cliente.ClienteService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ClienteService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TestemunhaService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/TestemunhaService!br.gov.caixa.ori.negocio.TestemunhaService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/TestemunhaService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SondaReenvioSiapi' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/SondaReenvioSiapi!br.gov.caixa.ori.negocio.sonda.SondaReenvioSiapi
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/SondaReenvioSiapi
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ImovelService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ImovelService!br.gov.caixa.ori.negocio.ImovelService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ImovelService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'IndicadorPercentualService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/IndicadorPercentualService!br.gov.caixa.ori.negocio.IndicadorPercentualService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/IndicadorPercentualService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ResponsavelCaixaService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ResponsavelCaixaService!br.gov.caixa.ori.negocio.ResponsavelCaixaService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ResponsavelCaixaService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'UnidadeService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/UnidadeService!br.gov.caixa.ori.negocio.UnidadeService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/UnidadeService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SIACGClient' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/SIACGClient!br.gov.caixa.ori.negocio.siacg.SIACGClient
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/SIACGClient
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ServicoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ServicoService!br.gov.caixa.ori.negocio.ServicoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ServicoService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'BDCaixaClient' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/BDCaixaClient!br.gov.caixa.ori.negocio.dbcaixa.BDCaixaClient
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/BDCaixaClient
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'Config' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/Config!br.gov.caixa.ori.common.Config
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/Config
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'VeiculoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/VeiculoService!br.gov.caixa.ori.negocio.VeiculoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/VeiculoService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'StatusGravameService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/StatusGravameService!br.gov.caixa.ori.negocio.StatusGravameService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/StatusGravameService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SimulacaoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/SimulacaoService!br.gov.caixa.ori.negocio.SimulacaoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/SimulacaoService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MaquinaEquipamentoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/MaquinaEquipamentoService!br.gov.caixa.ori.negocio.MaquinaEquipamentoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/MaquinaEquipamentoService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoRiscoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/AvaliacaoRiscoService!br.gov.caixa.ori.negocio.avaliacaorisco.AvaliacaoRiscoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/AvaliacaoRiscoService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'GarantiaService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/GarantiaService!br.gov.caixa.ori.negocio.GarantiaService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/GarantiaService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TipoImovelService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/TipoImovelService!br.gov.caixa.ori.negocio.TipoImovelService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/TipoImovelService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'CanalAtendimentoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/CanalAtendimentoService!br.gov.caixa.ori.negocio.CanalAtendimentoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/CanalAtendimentoService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutoAgricolaService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ProdutoAgricolaService!br.gov.caixa.ori.negocio.ProdutoAgricolaService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ProdutoAgricolaService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'LoggerFactory' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/LoggerFactory!br.gov.caixa.ori.common.LoggerFactory
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/LoggerFactory
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'BandaService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/BandaService!br.gov.caixa.ori.negocio.BandaService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/BandaService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TipoMaquinaEquipamentoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/TipoMaquinaEquipamentoService!br.gov.caixa.ori.negocio.TipoMaquinaEquipamentoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/TipoMaquinaEquipamentoService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EstadoCivilService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/EstadoCivilService!br.gov.caixa.ori.negocio.EstadoCivilService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/EstadoCivilService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ModalidadeService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ModalidadeService!br.gov.caixa.ori.negocio.ModalidadeService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ModalidadeService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'IndicadorService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/IndicadorService!br.gov.caixa.ori.negocio.IndicadorService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/IndicadorService
16:40:03,991 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ContratoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ContratoService!br.gov.caixa.ori.negocio.ContratoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ContratoService
16:40:03,992 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutoIcoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ProdutoIcoService!br.gov.caixa.ori.negocio.ProdutoIcoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ProdutoIcoService
16:40:03,992 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TLPService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/TLPService!br.gov.caixa.ori.negocio.TLPService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/TLPService
16:40:03,992 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProfissaoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ProfissaoService!br.gov.caixa.ori.negocio.ProfissaoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ProfissaoService
16:40:03,992 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'UsuarioService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/UsuarioService!br.gov.caixa.ori.negocio.UsuarioService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/UsuarioService
16:40:03,992 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ParametroProdutoAtualizacaoService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ParametroProdutoAtualizacaoService!br.gov.caixa.ori.negocio.ParametroProdutoAtualizacaoService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/ParametroProdutoAtualizacaoService
16:40:03,992 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvalistaService' na unidade de implementação 'subdeployment "ori-ejb.jar" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/AvalistaService!br.gov.caixa.ori.negocio.AvalistaService
        java:global/sifec-originacao-3.11.1-b344/ori-ejb/AvalistaService
16:40:03,992 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TipoMaquinaEquipamentoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/TipoMaquinaEquipamentoResource!br.gov.caixa.ori.rest.resource.TipoMaquinaEquipamentoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/TipoMaquinaEquipamentoResource
16:40:03,992 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TipoImovelResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/TipoImovelResource!br.gov.caixa.ori.rest.resource.TipoImovelResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/TipoImovelResource
16:40:03,992 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DashboardContratosResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/DashboardContratosResource!br.gov.caixa.ori.rest.resource.DashboardContratosResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/DashboardContratosResource
16:40:03,992 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ContratoFecResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/ContratoFecResource!br.gov.caixa.ori.rest.resource.ContratoFecResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/ContratoFecResource
16:40:03,992 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SituacaoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/SituacaoResource!br.gov.caixa.ori.rest.resource.SituacaoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/SituacaoResource
16:40:03,992 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TestemunhaResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/TestemunhaResource!br.gov.caixa.ori.rest.resource.TestemunhaResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/TestemunhaResource
16:40:03,992 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ServicoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/ServicoResource!br.gov.caixa.ori.rest.resource.ServicoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/ServicoResource
16:40:03,992 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'OrigemRecursoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/OrigemRecursoResource!br.gov.caixa.ori.rest.resource.OrigemRecursoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/OrigemRecursoResource
16:40:03,993 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'FontePagadoraResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/FontePagadoraResource!br.gov.caixa.ori.rest.resource.FontePagadoraResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/FontePagadoraResource
16:40:03,993 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ControleExecucaoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/ControleExecucaoResource!br.gov.caixa.ori.rest.resource.ControleExecucaoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/ControleExecucaoResource
16:40:03,993 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'StatusGravameResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/StatusGravameResource!br.gov.caixa.ori.rest.resource.StatusGravameResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/StatusGravameResource
16:40:03,993 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/ProdutoResource!br.gov.caixa.ori.rest.resource.ProdutoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/ProdutoResource
16:40:03,993 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ContratoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/ContratoResource!br.gov.caixa.ori.rest.resource.ContratoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/ContratoResource
16:40:03,993 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EstadoCivilResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/EstadoCivilResource!br.gov.caixa.ori.rest.resource.EstadoCivilResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/EstadoCivilResource
16:40:03,993 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ContratoRenegociadoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/ContratoRenegociadoResource!br.gov.caixa.ori.rest.resource.ContratoRenegociadoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/ContratoRenegociadoResource
16:40:03,993 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProfissaoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/ProfissaoResource!br.gov.caixa.ori.rest.resource.ProfissaoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/ProfissaoResource
16:40:03,993 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TipoModeloResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/TipoModeloResource!br.gov.caixa.ori.rest.resource.TipoModeloResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/TipoModeloResource
16:40:03,993 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SistemaResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/SistemaResource!br.gov.caixa.ori.rest.resource.SistemaResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/SistemaResource
16:40:03,993 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'OcupacaoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/OcupacaoResource!br.gov.caixa.ori.rest.resource.OcupacaoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/OcupacaoResource
16:40:03,993 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'BandaResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/BandaResource!br.gov.caixa.ori.rest.resource.BandaResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/BandaResource
16:40:03,993 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'IndicadoresResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/IndicadoresResource!br.gov.caixa.ori.rest.resource.IndicadoresResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/IndicadoresResource
16:40:03,993 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'UnidadeResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/UnidadeResource!br.gov.caixa.ori.rest.resource.UnidadeResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/UnidadeResource
16:40:03,993 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ResponsavelCaixaResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/ResponsavelCaixaResource!br.gov.caixa.ori.rest.resource.ResponsavelCaixaResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/ResponsavelCaixaResource
16:40:03,994 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'CanalAtendimentoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/CanalAtendimentoResource!br.gov.caixa.ori.rest.resource.CanalAtendimentoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/CanalAtendimentoResource
16:40:03,994 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'NacionalidadeResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/NacionalidadeResource!br.gov.caixa.ori.rest.resource.NacionalidadeResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/NacionalidadeResource
16:40:03,994 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ModalidadeResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/ModalidadeResource!br.gov.caixa.ori.rest.resource.ModalidadeResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/ModalidadeResource
16:40:03,994 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ExcepcionacaoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/ExcepcionacaoResource!br.gov.caixa.ori.rest.resource.ExcepcionacaoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/ExcepcionacaoResource
16:40:03,994 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'PerguntaAutorizacaoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/PerguntaAutorizacaoResource!br.gov.caixa.ori.rest.resource.PerguntaAutorizacaoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/PerguntaAutorizacaoResource
16:40:03,994 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SaldoOrigemRecursoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/SaldoOrigemRecursoResource!br.gov.caixa.ori.rest.resource.SaldoOrigemRecursoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/SaldoOrigemRecursoResource
16:40:03,994 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutoIcoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/ProdutoIcoResource!br.gov.caixa.ori.rest.resource.ProdutoIcoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/ProdutoIcoResource
16:40:03,994 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ClienteResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/ClienteResource!br.gov.caixa.ori.rest.resource.ClienteResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/ClienteResource
16:40:03,994 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'GarantiasResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/GarantiasResource!br.gov.caixa.ori.rest.resource.GarantiasResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/GarantiasResource
16:40:03,994 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ContratoNovadoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/ContratoNovadoResource!br.gov.caixa.ori.rest.resource.ContratoNovadoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/ContratoNovadoResource
16:40:03,994 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SimulacaoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/SimulacaoResource!br.gov.caixa.ori.rest.resource.SimulacaoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/SimulacaoResource
16:40:03,994 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'HistoricoProdutoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/HistoricoProdutoResource!br.gov.caixa.ori.rest.resource.HistoricoProdutoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/HistoricoProdutoResource
16:40:03,994 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'IndicadorPercentualResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/IndicadorPercentualResource!br.gov.caixa.ori.rest.resource.IndicadorPercentualResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/IndicadorPercentualResource
16:40:03,994 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-8) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'VigenciaParametrizacoesProdutoResource' na unidade de implementação 'subdeployment "ori-web.war" of deployment "sifec-originacao-3.11.1-b344.ear"' são como segue:
        java:global/sifec-originacao-3.11.1-b344/ori-web/VigenciaParametrizacoesProdutoResource!br.gov.caixa.ori.rest.resource.VigenciaParametrizacoesProdutoResource
        java:global/sifec-originacao-3.11.1-b344/ori-web/VigenciaParametrizacoesProdutoResource
16:40:04,013 INFO  [org.jipijapa] (MSC service thread 1-1) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-originacao-3.11.1-b344.ear#Componente-Calculo-PU
16:40:04,013 INFO  [org.jipijapa] (MSC service thread 1-1) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-originacao-3.11.1-b344.ear#SIEMP-PU
16:40:04,014 INFO  [org.jipijapa] (MSC service thread 1-1) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-originacao-3.11.1-b344.ear#fecDS
16:40:04,043 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 115) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'sifec-originacao-3.11.1-b344.ear#Componente-Calculo-PU'
16:40:04,043 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 110) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'sifec-originacao-3.11.1-b344.ear#fecDS'
16:40:04,043 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 121) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'sifec-originacao-3.11.1-b344.ear#SIEMP-PU'
16:40:04,134 INFO  [org.jipijapa] (MSC service thread 1-6) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-originacao-3.11.1-b344.ear/ori-ejb.jar#default
16:40:04,198 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 110) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'sifec-originacao-3.11.1-b344.ear/ori-ejb.jar#default'
16:40:04,887 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 6) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.contrato.sifbn.SifbnEjbServices because of underlying class loading error: Type br.gov.caixa.arqref.business.consultacontratos.services.sifbn.ContratoSifbnServiceIface from [Module "deployment.sifec-originacao-3.11.1-b344.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:40:04,903 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 6) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.contrato.siban.SibanEjbServices because of underlying class loading error: Type br.gov.caixa.arqref.business.consultacontratos.services.siban.ContratoSibanServiceIface from [Module "deployment.sifec-originacao-3.11.1-b344.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:40:05,449 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 135) WFLYUT0021: Contexto web registrado: '/ori-web' para servidor 'default-server'
16:40:05,477 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 119) WFLYSRV0010: "SIFEC-ORIGINACAO2" foi implantado (runtime-name: "sifec-originacao-3.11.1-b344.ear")






