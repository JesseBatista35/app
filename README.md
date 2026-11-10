
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$ sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -E "WFLYSRV0010|WFLYSRV0027|WFLYCTL0013|WFLYSRV0021|WFLYUT0021|ERROR|Caused by|Duplicate generator|WELD-001408|WELD-001318|RESTEASY003940|PBOX|sirur|SIRUR"

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for p585600:
11:24:34,814 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 147) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'sifec-sirur-2.9.3-b928.ear/sirur-ejb.jar#fec.rur.pu'
11:24:34,826 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 151) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'sifec-sirur-2.9.3-b928.ear#SIEMP-PU'
11:24:34,827 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 148) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'sifec-sirur-2.9.3-b928.ear#fecDS'
11:24:34,852 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 148) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'sifec-sirur-2.9.3-b928.ear#SIEMP-PU'
11:24:34,852 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 151) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'sifec-sirur-2.9.3-b928.ear#fecDS'
11:24:34,873 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-5) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: sirur-ejb.jar) em 79ms
11:24:34,904 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-2) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: sirur-web.war) em 110ms
11:24:34,918 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-2) WFLYSRV0028: Implantação interrompida SIRUR (runtime-name: sifec-sirur-2.9.3-b928.ear) em 124ms
11:30:12,629 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-5) WFLYSRV0027: Iniciando a implantação do "SIRUR" (runtime-name: "sifec-sirur-3.54.51.28.ear")
11:30:15,906 WARN  [org.jboss.as.server.deployment] (MSC service thread 1-6) WFLYSRV0059: A entrada do caminho da classe jaxb-api.jar em /content/sifec-sirur-3.54.51.28.ear/lib/jaxb-impl-2.2.3-1.jar não direciona a um jar válido para a referência do caminho da classe.
11:30:15,906 WARN  [org.jboss.as.server.deployment] (MSC service thread 1-6) WFLYSRV0059: A entrada do caminho da classe activation.jar em /content/sifec-sirur-3.54.51.28.ear/lib/jaxb-impl-2.2.3-1.jar não direciona a um jar válido para a referência do caminho da classe.
11:30:15,906 WARN  [org.jboss.as.server.deployment] (MSC service thread 1-6) WFLYSRV0059: A entrada do caminho da classe jsr173_1.0_api.jar em /content/sifec-sirur-3.54.51.28.ear/lib/jaxb-impl-2.2.3-1.jar não direciona a um jar válido para a referência do caminho da classe.
11:30:15,906 WARN  [org.jboss.as.server.deployment] (MSC service thread 1-6) WFLYSRV0059: A entrada do caminho da classe jaxb1-impl.jar em /content/sifec-sirur-3.54.51.28.ear/lib/jaxb-impl-2.2.3-1.jar não direciona a um jar válido para a referência do caminho da classe.
11:30:15,922 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-6) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "sirur-ejb.jar")
11:30:15,922 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-8) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "sirur-web.war")
11:30:16,497 INFO  [org.jipijapa] (MSC service thread 1-5) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-sirur-3.54.51.28.ear#SIEMP-PU
11:30:16,497 INFO  [org.jipijapa] (MSC service thread 1-5) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-sirur-3.54.51.28.ear#fecDS
11:30:16,498 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 158) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'sifec-sirur-3.54.51.28.ear#fecDS'
11:30:16,498 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 91) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'sifec-sirur-3.54.51.28.ear#SIEMP-PU'
11:30:16,499 INFO  [org.jipijapa] (MSC service thread 1-1) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.pu
11:30:16,502 INFO  [org.jipijapa] (MSC service thread 1-1) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.rur.pu
11:30:16,515 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 159) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.pu'
11:30:16,516 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 160) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.rur.pu'
11:30:16,557 INFO  [org.jboss.weld.deployer] (MSC service thread 1-3) WFLYWELD0003: Processando da implantação weld sifec-sirur-3.54.51.28.ear
11:30:16,666 INFO  [org.jboss.keycloak] (MSC service thread 1-3) Keycloak subsystem override for deployment sirur-web.war
11:30:16,666 INFO  [org.jboss.weld.deployer] (MSC service thread 1-3) WFLYWELD0003: Processando da implantação weld sirur-web.war
11:30:16,673 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-3) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'seguranca-sso-SecurityKeycloakUtils' na unidade de implementação 'subdeployment "sirur-web.war" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-web/seguranca-sso-SecurityKeycloakUtils!br.gov.caixa.sifec.componentes.seguranca.sso.utils.SecurityKeycloakUtils
        java:app/sirur-web/seguranca-sso-SecurityKeycloakUtils!br.gov.caixa.sifec.componentes.seguranca.sso.utils.SecurityKeycloakUtils
        java:global/sifec-sirur-3.54.51.28/sirur-web/seguranca-sso-SecurityKeycloakUtils
        java:app/sirur-web/seguranca-sso-SecurityKeycloakUtils
11:30:16,843 INFO  [org.jboss.weld.deployer] (MSC service thread 1-6) WFLYWELD0003: Processando da implantação weld sirur-ejb.jar
11:30:16,848 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ExportacaoCadastroAterBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ExportacaoCadastroAterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.ExportacaoCadastroAterBean
        java:app/sirur-ejb/ExportacaoCadastroAterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.ExportacaoCadastroAterBean
        java:module/ExportacaoCadastroAterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.ExportacaoCadastroAterBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ExportacaoCadastroAterBean
        java:app/sirur-ejb/ExportacaoCadastroAterBean
11:30:16,848 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DocumentoInformativoBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DocumentoInformativoBeanImpl!br.gov.caixa.sirur.bean.DocumentoInformativoBean
        java:app/sirur-ejb/DocumentoInformativoBeanImpl!br.gov.caixa.sirur.bean.DocumentoInformativoBean
        java:module/DocumentoInformativoBeanImpl!br.gov.caixa.sirur.bean.DocumentoInformativoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DocumentoInformativoBeanImpl
        java:app/sirur-ejb/DocumentoInformativoBeanImpl
11:30:16,848 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MatriculaServiceV2Impl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/MatriculaServiceV2Impl!br.gov.caixa.sirur.service.MatriculaServiceV2
        java:app/sirur-ejb/MatriculaServiceV2Impl!br.gov.caixa.sirur.service.MatriculaServiceV2
        java:module/MatriculaServiceV2Impl!br.gov.caixa.sirur.service.MatriculaServiceV2
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/MatriculaServiceV2Impl
        java:app/sirur-ejb/MatriculaServiceV2Impl
11:30:16,848 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ViabilidadeEmpreendimentoBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ViabilidadeEmpreendimentoBean!br.gov.caixa.sirur.bean.impl.orcamento.ViabilidadeEmpreendimentoBean
        java:app/sirur-ejb/ViabilidadeEmpreendimentoBean!br.gov.caixa.sirur.bean.impl.orcamento.ViabilidadeEmpreendimentoBean
        java:module/ViabilidadeEmpreendimentoBean!br.gov.caixa.sirur.bean.impl.orcamento.ViabilidadeEmpreendimentoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ViabilidadeEmpreendimentoBean
        java:app/sirur-ejb/ViabilidadeEmpreendimentoBean
11:30:16,848 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DomainServiceV2Impl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DomainServiceV2Impl!br.gov.caixa.sirur.service.DomainServiceV2
        java:app/sirur-ejb/DomainServiceV2Impl!br.gov.caixa.sirur.service.DomainServiceV2
        java:module/DomainServiceV2Impl!br.gov.caixa.sirur.service.DomainServiceV2
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DomainServiceV2Impl
        java:app/sirur-ejb/DomainServiceV2Impl
11:30:16,848 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SituacaoSolicitacaoServiceImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SituacaoSolicitacaoServiceImpl!br.gov.caixa.sirur.service.SituacaoSolicitacaoService
        java:app/sirur-ejb/SituacaoSolicitacaoServiceImpl!br.gov.caixa.sirur.service.SituacaoSolicitacaoService
        java:module/SituacaoSolicitacaoServiceImpl!br.gov.caixa.sirur.service.SituacaoSolicitacaoService
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SituacaoSolicitacaoServiceImpl
        java:app/sirur-ejb/SituacaoSolicitacaoServiceImpl
11:30:16,848 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DocumentacaoBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DocumentacaoBeanImpl!br.gov.caixa.sirur.bean.DocumentacaoBean
        java:app/sirur-ejb/DocumentacaoBeanImpl!br.gov.caixa.sirur.bean.DocumentacaoBean
        java:module/DocumentacaoBeanImpl!br.gov.caixa.sirur.bean.DocumentacaoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DocumentacaoBeanImpl
        java:app/sirur-ejb/DocumentacaoBeanImpl
11:30:16,848 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ConexaoLDAP' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ConexaoLDAP!br.gov.caixa.sirur.ldap.ConexaoLDAP
        java:app/sirur-ejb/ConexaoLDAP!br.gov.caixa.sirur.ldap.ConexaoLDAP
        java:module/ConexaoLDAP!br.gov.caixa.sirur.ldap.ConexaoLDAP
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ConexaoLDAP
        java:app/sirur-ejb/ConexaoLDAP
11:30:16,849 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EtapaCadastroProducaoRuralBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/EtapaCadastroProducaoRuralBeanImpl!br.gov.caixa.sirur.bean.EtapaCadastroProducaoRuralBean
        java:app/sirur-ejb/EtapaCadastroProducaoRuralBeanImpl!br.gov.caixa.sirur.bean.EtapaCadastroProducaoRuralBean
        java:module/EtapaCadastroProducaoRuralBeanImpl!br.gov.caixa.sirur.bean.EtapaCadastroProducaoRuralBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/EtapaCadastroProducaoRuralBeanImpl
        java:app/sirur-ejb/EtapaCadastroProducaoRuralBeanImpl
11:30:16,849 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'OrcamentoAnaliticoBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/OrcamentoAnaliticoBean!br.gov.caixa.sirur.bean.impl.orcamento.OrcamentoAnaliticoBean
        java:app/sirur-ejb/OrcamentoAnaliticoBean!br.gov.caixa.sirur.bean.impl.orcamento.OrcamentoAnaliticoBean
        java:module/OrcamentoAnaliticoBean!br.gov.caixa.sirur.bean.impl.orcamento.OrcamentoAnaliticoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/OrcamentoAnaliticoBean
        java:app/sirur-ejb/OrcamentoAnaliticoBean
11:30:16,849 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DominioBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DominioBean!br.gov.caixa.sirur.bean.impl.oportunidadenegocio.DominioBean
        java:app/sirur-ejb/DominioBean!br.gov.caixa.sirur.bean.impl.oportunidadenegocio.DominioBean
        java:module/DominioBean!br.gov.caixa.sirur.bean.impl.oportunidadenegocio.DominioBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DominioBean
        java:app/sirur-ejb/DominioBean
11:30:16,849 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DadosEmpresaAterBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DadosEmpresaAterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.DadosEmpresaAterBean
        java:app/sirur-ejb/DadosEmpresaAterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.DadosEmpresaAterBean
        java:module/DadosEmpresaAterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.DadosEmpresaAterBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DadosEmpresaAterBean
        java:app/sirur-ejb/DadosEmpresaAterBean
11:30:16,849 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'RelatorioAterBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/RelatorioAterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.RelatorioAterBean
        java:app/sirur-ejb/RelatorioAterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.RelatorioAterBean
        java:module/RelatorioAterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.RelatorioAterBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/RelatorioAterBean
        java:app/sirur-ejb/RelatorioAterBean
11:30:16,849 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TecnicoBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/TecnicoBeanImpl!br.gov.caixa.sirur.bean.TecnicoBean
        java:app/sirur-ejb/TecnicoBeanImpl!br.gov.caixa.sirur.bean.TecnicoBean
        java:module/TecnicoBeanImpl!br.gov.caixa.sirur.bean.TecnicoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/TecnicoBeanImpl
        java:app/sirur-ejb/TecnicoBeanImpl
11:30:16,849 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EmpresaBeanImplV2' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/EmpresaBeanImplV2!br.gov.caixa.sirur.bean.EmpresaBeanV2
        java:app/sirur-ejb/EmpresaBeanImplV2!br.gov.caixa.sirur.bean.EmpresaBeanV2
        java:module/EmpresaBeanImplV2!br.gov.caixa.sirur.bean.EmpresaBeanV2
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/EmpresaBeanImplV2
        java:app/sirur-ejb/EmpresaBeanImplV2
11:30:16,854 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'OrcamentoBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/OrcamentoBeanImpl!br.gov.caixa.sirur.orcamento.OrcamentoBeanRmt
        java:app/sirur-ejb/OrcamentoBeanImpl!br.gov.caixa.sirur.orcamento.OrcamentoBeanRmt
        java:module/OrcamentoBeanImpl!br.gov.caixa.sirur.orcamento.OrcamentoBeanRmt
        java:jboss/exported/sifec-sirur-3.54.51.28/sirur-ejb/OrcamentoBeanImpl!br.gov.caixa.sirur.orcamento.OrcamentoBeanRmt
        ejb:sifec-sirur-3.54.51.28/sirur-ejb/OrcamentoBeanImpl!br.gov.caixa.sirur.orcamento.OrcamentoBeanRmt
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/OrcamentoBeanImpl
        java:app/sirur-ejb/OrcamentoBeanImpl
11:30:16,854 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'BeanProducaoRuralImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/BeanProducaoRuralImpl!br.gov.caixa.sirur.cadastro.BeanProducaoRural
        java:app/sirur-ejb/BeanProducaoRuralImpl!br.gov.caixa.sirur.cadastro.BeanProducaoRural
        java:module/BeanProducaoRuralImpl!br.gov.caixa.sirur.cadastro.BeanProducaoRural
        java:jboss/exported/sifec-sirur-3.54.51.28/sirur-ejb/BeanProducaoRuralImpl!br.gov.caixa.sirur.cadastro.BeanProducaoRural
        ejb:sifec-sirur-3.54.51.28/sirur-ejb/BeanProducaoRuralImpl!br.gov.caixa.sirur.cadastro.BeanProducaoRural
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/BeanProducaoRuralImpl
        java:app/sirur-ejb/BeanProducaoRuralImpl
11:30:16,855 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'BeanClienteImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/BeanClienteImpl!br.gov.caixa.sirur.base.BeanCliente
        java:app/sirur-ejb/BeanClienteImpl!br.gov.caixa.sirur.base.BeanCliente
        java:module/BeanClienteImpl!br.gov.caixa.sirur.base.BeanCliente
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/BeanClienteImpl
        java:app/sirur-ejb/BeanClienteImpl
11:30:16,855 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'FaseOportunidadeBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/FaseOportunidadeBean!br.gov.caixa.sirur.bean.impl.oportunidadenegocio.FaseOportunidadeBean
        java:app/sirur-ejb/FaseOportunidadeBean!br.gov.caixa.sirur.bean.impl.oportunidadenegocio.FaseOportunidadeBean
        java:module/FaseOportunidadeBean!br.gov.caixa.sirur.bean.impl.oportunidadenegocio.FaseOportunidadeBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/FaseOportunidadeBean
        java:app/sirur-ejb/FaseOportunidadeBean
11:30:16,855 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AterBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AterBeanImpl!br.gov.caixa.sirur.bean.AterBean
        java:app/sirur-ejb/AterBeanImpl!br.gov.caixa.sirur.bean.AterBean
        java:module/AterBeanImpl!br.gov.caixa.sirur.bean.AterBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AterBeanImpl
        java:app/sirur-ejb/AterBeanImpl
11:30:16,855 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DadosProprietarioProcessorV2' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DadosProprietarioProcessorV2!br.gov.caixa.sirur.processor.imovel.DadosProprietarioProcessorV2
        java:app/sirur-ejb/DadosProprietarioProcessorV2!br.gov.caixa.sirur.processor.imovel.DadosProprietarioProcessorV2
        java:module/DadosProprietarioProcessorV2!br.gov.caixa.sirur.processor.imovel.DadosProprietarioProcessorV2
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DadosProprietarioProcessorV2
        java:app/sirur-ejb/DadosProprietarioProcessorV2
11:30:16,855 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'PropriedadeBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/PropriedadeBeanImpl!br.gov.caixa.sirur.bean.PropriedadeBean
        java:app/sirur-ejb/PropriedadeBeanImpl!br.gov.caixa.sirur.bean.PropriedadeBean
        java:module/PropriedadeBeanImpl!br.gov.caixa.sirur.bean.PropriedadeBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/PropriedadeBeanImpl
        java:app/sirur-ejb/PropriedadeBeanImpl
11:30:16,855 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DadosTecnicosBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DadosTecnicosBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.DadosTecnicosBean
        java:app/sirur-ejb/DadosTecnicosBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.DadosTecnicosBean
        java:module/DadosTecnicosBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.DadosTecnicosBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DadosTecnicosBean
        java:app/sirur-ejb/DadosTecnicosBean
11:30:16,855 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'GedBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/GedBean!br.gov.caixa.sirur.bean.impl.GedBean
        java:app/sirur-ejb/GedBean!br.gov.caixa.sirur.bean.impl.GedBean
        java:module/GedBean!br.gov.caixa.sirur.bean.impl.GedBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/GedBean
        java:app/sirur-ejb/GedBean
11:30:16,855 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EtapaCadastroOrcamentoBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/EtapaCadastroOrcamentoBean!br.gov.caixa.sirur.bean.impl.orcamento.EtapaCadastroOrcamentoBean
        java:app/sirur-ejb/EtapaCadastroOrcamentoBean!br.gov.caixa.sirur.bean.impl.orcamento.EtapaCadastroOrcamentoBean
        java:module/EtapaCadastroOrcamentoBean!br.gov.caixa.sirur.bean.impl.orcamento.EtapaCadastroOrcamentoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/EtapaCadastroOrcamentoBean
        java:app/sirur-ejb/EtapaCadastroOrcamentoBean
11:30:16,855 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'UnidadeBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/UnidadeBeanImpl!br.gov.caixa.sirur.bean.UnidadeBean
        java:app/sirur-ejb/UnidadeBeanImpl!br.gov.caixa.sirur.bean.UnidadeBean
        java:module/UnidadeBeanImpl!br.gov.caixa.sirur.bean.UnidadeBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/UnidadeBeanImpl
        java:app/sirur-ejb/UnidadeBeanImpl
11:30:16,855 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'CadastroProducaoRuralBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/CadastroProducaoRuralBeanImpl!br.gov.caixa.sirur.bean.CadastroProducaoRuralBean
        java:app/sirur-ejb/CadastroProducaoRuralBeanImpl!br.gov.caixa.sirur.bean.CadastroProducaoRuralBean
        java:module/CadastroProducaoRuralBeanImpl!br.gov.caixa.sirur.bean.CadastroProducaoRuralBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/CadastroProducaoRuralBeanImpl
        java:app/sirur-ejb/CadastroProducaoRuralBeanImpl
11:30:16,855 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'GrupoEconomicoBeanV2' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/GrupoEconomicoBeanV2!br.gov.caixa.sirur.bean.impl.GrupoEconomicoBeanV2
        java:app/sirur-ejb/GrupoEconomicoBeanV2!br.gov.caixa.sirur.bean.impl.GrupoEconomicoBeanV2
        java:module/GrupoEconomicoBeanV2!br.gov.caixa.sirur.bean.impl.GrupoEconomicoBeanV2
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/GrupoEconomicoBeanV2
        java:app/sirur-ejb/GrupoEconomicoBeanV2
11:30:16,855 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'BeanAterEmpresaImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/BeanAterEmpresaImpl!br.gov.caixa.sirur.cadastro.BeanAterEmpresa
        java:app/sirur-ejb/BeanAterEmpresaImpl!br.gov.caixa.sirur.cadastro.BeanAterEmpresa
        java:module/BeanAterEmpresaImpl!br.gov.caixa.sirur.cadastro.BeanAterEmpresa
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/BeanAterEmpresaImpl
        java:app/sirur-ejb/BeanAterEmpresaImpl
11:30:16,856 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'HistoricoSituacaoBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/HistoricoSituacaoBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.HistoricoSituacaoBean
        java:app/sirur-ejb/HistoricoSituacaoBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.HistoricoSituacaoBean
        java:module/HistoricoSituacaoBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.HistoricoSituacaoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/HistoricoSituacaoBean
        java:app/sirur-ejb/HistoricoSituacaoBean
11:30:16,856 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AterBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.AterBean
        java:app/sirur-ejb/AterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.AterBean
        java:module/AterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.AterBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AterBean
        java:app/sirur-ejb/AterBean
11:30:16,856 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SicliIntegracaoNegocio' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SicliIntegracaoNegocio!br.gov.caixa.sirur.integracao.rest.sicli.SicliIntegracaoNegocio
        java:app/sirur-ejb/SicliIntegracaoNegocio!br.gov.caixa.sirur.integracao.rest.sicli.SicliIntegracaoNegocio
        java:module/SicliIntegracaoNegocio!br.gov.caixa.sirur.integracao.rest.sicli.SicliIntegracaoNegocio
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SicliIntegracaoNegocio
        java:app/sirur-ejb/SicliIntegracaoNegocio
11:30:16,856 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ImprimirCadatroBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ImprimirCadatroBeanImpl!br.gov.caixa.sirur.bean.ImprimirCadatroBean
        java:app/sirur-ejb/ImprimirCadatroBeanImpl!br.gov.caixa.sirur.bean.ImprimirCadatroBean
        java:module/ImprimirCadatroBeanImpl!br.gov.caixa.sirur.bean.ImprimirCadatroBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ImprimirCadatroBeanImpl
        java:app/sirur-ejb/ImprimirCadatroBeanImpl
11:30:16,856 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'InscricaoEstadualBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/InscricaoEstadualBeanImpl!br.gov.caixa.sirur.bean.InscricaoEstadualBean
        java:app/sirur-ejb/InscricaoEstadualBeanImpl!br.gov.caixa.sirur.bean.InscricaoEstadualBean
        java:module/InscricaoEstadualBeanImpl!br.gov.caixa.sirur.bean.InscricaoEstadualBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/InscricaoEstadualBeanImpl
        java:app/sirur-ejb/InscricaoEstadualBeanImpl
11:30:16,856 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'OportunidadeNegocioBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/OportunidadeNegocioBean!br.gov.caixa.sirur.bean.impl.oportunidadenegocio.OportunidadeNegocioBean
        java:app/sirur-ejb/OportunidadeNegocioBean!br.gov.caixa.sirur.bean.impl.oportunidadenegocio.OportunidadeNegocioBean
        java:module/OportunidadeNegocioBean!br.gov.caixa.sirur.bean.impl.oportunidadenegocio.OportunidadeNegocioBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/OportunidadeNegocioBean
        java:app/sirur-ejb/OportunidadeNegocioBean
11:30:16,857 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EmpresaBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/EmpresaBeanImpl!br.gov.caixa.sirur.bean.EmpresaBean
        java:app/sirur-ejb/EmpresaBeanImpl!br.gov.caixa.sirur.bean.EmpresaBean
        java:module/EmpresaBeanImpl!br.gov.caixa.sirur.bean.EmpresaBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/EmpresaBeanImpl
        java:app/sirur-ejb/EmpresaBeanImpl
11:30:16,857 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SiricBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SiricBeanImpl!br.gov.caixa.sirur.bean.impl.SiricBeanImpl
        java:app/sirur-ejb/SiricBeanImpl!br.gov.caixa.sirur.bean.impl.SiricBeanImpl
        java:module/SiricBeanImpl!br.gov.caixa.sirur.bean.impl.SiricBeanImpl
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SiricBeanImpl
        java:app/sirur-ejb/SiricBeanImpl
11:30:16,857 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutorRuralEmpresaBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ProdutorRuralEmpresaBeanImpl!br.gov.caixa.sirur.bean.ProdutorRuralEmpresaBean
        java:app/sirur-ejb/ProdutorRuralEmpresaBeanImpl!br.gov.caixa.sirur.bean.ProdutorRuralEmpresaBean
        java:module/ProdutorRuralEmpresaBeanImpl!br.gov.caixa.sirur.bean.ProdutorRuralEmpresaBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ProdutorRuralEmpresaBeanImpl
        java:app/sirur-ejb/ProdutorRuralEmpresaBeanImpl
11:30:16,857 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SituacaoCadastroOrcamentoBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SituacaoCadastroOrcamentoBean!br.gov.caixa.sirur.bean.impl.orcamento.SituacaoCadastroOrcamentoBean
        java:app/sirur-ejb/SituacaoCadastroOrcamentoBean!br.gov.caixa.sirur.bean.impl.orcamento.SituacaoCadastroOrcamentoBean
        java:module/SituacaoCadastroOrcamentoBean!br.gov.caixa.sirur.bean.impl.orcamento.SituacaoCadastroOrcamentoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SituacaoCadastroOrcamentoBean
        java:app/sirur-ejb/SituacaoCadastroOrcamentoBean
11:30:16,857 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'LocalidadeIntegracaoNegocio' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/LocalidadeIntegracaoNegocio!br.gov.caixa.sirur.integracao.rest.localidade.LocalidadeIntegracaoNegocio
        java:app/sirur-ejb/LocalidadeIntegracaoNegocio!br.gov.caixa.sirur.integracao.rest.localidade.LocalidadeIntegracaoNegocio
        java:module/LocalidadeIntegracaoNegocio!br.gov.caixa.sirur.integracao.rest.localidade.LocalidadeIntegracaoNegocio
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/LocalidadeIntegracaoNegocio
        java:app/sirur-ejb/LocalidadeIntegracaoNegocio
11:30:16,857 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ParecerTecnicoBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ParecerTecnicoBean!br.gov.caixa.sirur.bean.impl.orcamento.ParecerTecnicoBean
        java:app/sirur-ejb/ParecerTecnicoBean!br.gov.caixa.sirur.bean.impl.orcamento.ParecerTecnicoBean
        java:module/ParecerTecnicoBean!br.gov.caixa.sirur.bean.impl.orcamento.ParecerTecnicoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ParecerTecnicoBean
        java:app/sirur-ejb/ParecerTecnicoBean
11:30:16,857 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SituacaoSolicitacaoBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SituacaoSolicitacaoBeanImpl!br.gov.caixa.sirur.bean.SituacaoSolicitacaoBean
        java:app/sirur-ejb/SituacaoSolicitacaoBeanImpl!br.gov.caixa.sirur.bean.SituacaoSolicitacaoBean
        java:module/SituacaoSolicitacaoBeanImpl!br.gov.caixa.sirur.bean.SituacaoSolicitacaoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SituacaoSolicitacaoBeanImpl
        java:app/sirur-ejb/SituacaoSolicitacaoBeanImpl
11:30:16,857 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'PerfilProdutorBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/PerfilProdutorBeanImpl!br.gov.caixa.sirur.bean.PerfilProdutorBean
        java:app/sirur-ejb/PerfilProdutorBeanImpl!br.gov.caixa.sirur.bean.PerfilProdutorBean
        java:module/PerfilProdutorBeanImpl!br.gov.caixa.sirur.bean.PerfilProdutorBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/PerfilProdutorBeanImpl
        java:app/sirur-ejb/PerfilProdutorBeanImpl
11:30:16,857 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'IntegranteGrupoEconomicoBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/IntegranteGrupoEconomicoBeanImpl!br.gov.caixa.sirur.bean.IntegranteGrupoEconomicoBean
        java:app/sirur-ejb/IntegranteGrupoEconomicoBeanImpl!br.gov.caixa.sirur.bean.IntegranteGrupoEconomicoBean
        java:module/IntegranteGrupoEconomicoBeanImpl!br.gov.caixa.sirur.bean.IntegranteGrupoEconomicoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/IntegranteGrupoEconomicoBeanImpl
        java:app/sirur-ejb/IntegranteGrupoEconomicoBeanImpl
11:30:16,857 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'InformeBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/InformeBeanImpl!br.gov.caixa.sirur.bean.InformeBean
        java:app/sirur-ejb/InformeBeanImpl!br.gov.caixa.sirur.bean.InformeBean
        java:module/InformeBeanImpl!br.gov.caixa.sirur.bean.InformeBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/InformeBeanImpl
        java:app/sirur-ejb/InformeBeanImpl
11:30:16,857 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'OrcamentoBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/OrcamentoBean!br.gov.caixa.sirur.bean.impl.orcamento.OrcamentoBean
        java:app/sirur-ejb/OrcamentoBean!br.gov.caixa.sirur.bean.impl.orcamento.OrcamentoBean
        java:module/OrcamentoBean!br.gov.caixa.sirur.bean.impl.orcamento.OrcamentoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/OrcamentoBean
        java:app/sirur-ejb/OrcamentoBean
11:30:16,857 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EmpreendimentoBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/EmpreendimentoBean!br.gov.caixa.sirur.bean.impl.orcamento.EmpreendimentoBean
        java:app/sirur-ejb/EmpreendimentoBean!br.gov.caixa.sirur.bean.impl.orcamento.EmpreendimentoBean
        java:module/EmpreendimentoBean!br.gov.caixa.sirur.bean.impl.orcamento.EmpreendimentoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/EmpreendimentoBean
        java:app/sirur-ejb/EmpreendimentoBean
11:30:16,858 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ImovelBeanV2Impl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ImovelBeanV2Impl!br.gov.caixa.sirur.bean.impl.ImovelBeanV2Impl
        java:app/sirur-ejb/ImovelBeanV2Impl!br.gov.caixa.sirur.bean.impl.ImovelBeanV2Impl
        java:module/ImovelBeanV2Impl!br.gov.caixa.sirur.bean.impl.ImovelBeanV2Impl
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ImovelBeanV2Impl
        java:app/sirur-ejb/ImovelBeanV2Impl
11:30:16,858 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ImovelBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ImovelBeanImpl!br.gov.caixa.sirur.bean.ImovelBean
        java:app/sirur-ejb/ImovelBeanImpl!br.gov.caixa.sirur.bean.ImovelBean
        java:module/ImovelBeanImpl!br.gov.caixa.sirur.bean.ImovelBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ImovelBeanImpl
        java:app/sirur-ejb/ImovelBeanImpl
11:30:16,858 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutorRuralBeanV2' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ProdutorRuralBeanV2!br.gov.caixa.sirur.bean.impl.ProdutorRuralBeanV2
        java:app/sirur-ejb/ProdutorRuralBeanV2!br.gov.caixa.sirur.bean.impl.ProdutorRuralBeanV2
        java:module/ProdutorRuralBeanV2!br.gov.caixa.sirur.bean.impl.ProdutorRuralBeanV2
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ProdutorRuralBeanV2
        java:app/sirur-ejb/ProdutorRuralBeanV2
11:30:16,858 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TipoProdutorBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/TipoProdutorBeanImpl!br.gov.caixa.sirur.bean.TipoProdutorBean
        java:app/sirur-ejb/TipoProdutorBeanImpl!br.gov.caixa.sirur.bean.TipoProdutorBean
        java:module/TipoProdutorBeanImpl!br.gov.caixa.sirur.bean.TipoProdutorBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/TipoProdutorBeanImpl
        java:app/sirur-ejb/TipoProdutorBeanImpl
11:30:16,858 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EnquadramentoDapImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/EnquadramentoDapImpl!br.gov.caixa.sirur.bean.EnquadramentoDap
        java:app/sirur-ejb/EnquadramentoDapImpl!br.gov.caixa.sirur.bean.EnquadramentoDap
        java:module/EnquadramentoDapImpl!br.gov.caixa.sirur.bean.EnquadramentoDap
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/EnquadramentoDapImpl
        java:app/sirur-ejb/EnquadramentoDapImpl
11:30:16,858 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SiricServiceImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SiricServiceImpl!br.gov.caixa.sirur.service.impl.SiricServiceImpl
        java:app/sirur-ejb/SiricServiceImpl!br.gov.caixa.sirur.service.impl.SiricServiceImpl
        java:module/SiricServiceImpl!br.gov.caixa.sirur.service.impl.SiricServiceImpl
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SiricServiceImpl
        java:app/sirur-ejb/SiricServiceImpl
11:30:16,858 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SiricXMLIntegracaoNegocioImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SiricXMLIntegracaoNegocioImpl!br.gov.caixa.sirur.integracao.mq.siric.impl.SiricXMLIntegracaoNegocioImpl
        java:app/sirur-ejb/SiricXMLIntegracaoNegocioImpl!br.gov.caixa.sirur.integracao.mq.siric.impl.SiricXMLIntegracaoNegocioImpl
        java:module/SiricXMLIntegracaoNegocioImpl!br.gov.caixa.sirur.integracao.mq.siric.impl.SiricXMLIntegracaoNegocioImpl
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SiricXMLIntegracaoNegocioImpl
        java:app/sirur-ejb/SiricXMLIntegracaoNegocioImpl
11:30:16,858 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DomainBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DomainBeanImpl!br.gov.caixa.sirur.bean.DomainBean
        java:app/sirur-ejb/DomainBeanImpl!br.gov.caixa.sirur.bean.DomainBean
        java:module/DomainBeanImpl!br.gov.caixa.sirur.bean.DomainBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DomainBeanImpl
        java:app/sirur-ejb/DomainBeanImpl
11:30:16,858 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ImovelBeneficiadoBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ImovelBeneficiadoBean!br.gov.caixa.sirur.bean.impl.orcamento.ImovelBeneficiadoBean
        java:app/sirur-ejb/ImovelBeneficiadoBean!br.gov.caixa.sirur.bean.impl.orcamento.ImovelBeneficiadoBean
        java:module/ImovelBeneficiadoBean!br.gov.caixa.sirur.bean.impl.orcamento.ImovelBeneficiadoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ImovelBeneficiadoBean
        java:app/sirur-ejb/ImovelBeneficiadoBean
11:30:16,858 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DadosMatriculaDtoProcessorV2' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DadosMatriculaDtoProcessorV2!br.gov.caixa.sirur.processor.imovel.DadosMatriculaDtoProcessorV2
        java:app/sirur-ejb/DadosMatriculaDtoProcessorV2!br.gov.caixa.sirur.processor.imovel.DadosMatriculaDtoProcessorV2
        java:module/DadosMatriculaDtoProcessorV2!br.gov.caixa.sirur.processor.imovel.DadosMatriculaDtoProcessorV2
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DadosMatriculaDtoProcessorV2
        java:app/sirur-ejb/DadosMatriculaDtoProcessorV2
11:30:16,858 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AnaliseDocumentacaoBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AnaliseDocumentacaoBean!br.gov.caixa.sirur.bean.impl.orcamento.AnaliseDocumentacaoBean
        java:app/sirur-ejb/AnaliseDocumentacaoBean!br.gov.caixa.sirur.bean.impl.orcamento.AnaliseDocumentacaoBean
        java:module/AnaliseDocumentacaoBean!br.gov.caixa.sirur.bean.impl.orcamento.AnaliseDocumentacaoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AnaliseDocumentacaoBean
        java:app/sirur-ejb/AnaliseDocumentacaoBean
11:30:16,858 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AtividadePecuariaBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AtividadePecuariaBeanImpl!br.gov.caixa.sirur.bean.AtividadePecuariaBean
        java:app/sirur-ejb/AtividadePecuariaBeanImpl!br.gov.caixa.sirur.bean.AtividadePecuariaBean
        java:module/AtividadePecuariaBeanImpl!br.gov.caixa.sirur.bean.AtividadePecuariaBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AtividadePecuariaBeanImpl
        java:app/sirur-ejb/AtividadePecuariaBeanImpl
11:30:16,858 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'GlebasBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/GlebasBean!br.gov.caixa.sirur.bean.impl.orcamento.GlebasBean
        java:app/sirur-ejb/GlebasBean!br.gov.caixa.sirur.bean.impl.orcamento.GlebasBean
        java:module/GlebasBean!br.gov.caixa.sirur.bean.impl.orcamento.GlebasBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/GlebasBean
        java:app/sirur-ejb/GlebasBean
11:30:16,859 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AnaliseDocumentalAterBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AnaliseDocumentalAterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.AnaliseDocumentalAterBean
        java:app/sirur-ejb/AnaliseDocumentalAterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.AnaliseDocumentalAterBean
        java:module/AnaliseDocumentalAterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.AnaliseDocumentalAterBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AnaliseDocumentalAterBean
        java:app/sirur-ejb/AnaliseDocumentalAterBean
11:30:16,859 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoRiscoProdutorNegocio' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AvaliacaoRiscoProdutorNegocio!br.gov.caixa.sirur.bean.impl.AvaliacaoRiscoProdutorNegocio
        java:app/sirur-ejb/AvaliacaoRiscoProdutorNegocio!br.gov.caixa.sirur.bean.impl.AvaliacaoRiscoProdutorNegocio
        java:module/AvaliacaoRiscoProdutorNegocio!br.gov.caixa.sirur.bean.impl.AvaliacaoRiscoProdutorNegocio
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AvaliacaoRiscoProdutorNegocio
        java:app/sirur-ejb/AvaliacaoRiscoProdutorNegocio
11:30:16,859 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MatriculaPrincipalMunicipioProcessorV2' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/MatriculaPrincipalMunicipioProcessorV2!br.gov.caixa.sirur.processor.imovel.MatriculaPrincipalMunicipioProcessorV2
        java:app/sirur-ejb/MatriculaPrincipalMunicipioProcessorV2!br.gov.caixa.sirur.processor.imovel.MatriculaPrincipalMunicipioProcessorV2
        java:module/MatriculaPrincipalMunicipioProcessorV2!br.gov.caixa.sirur.processor.imovel.MatriculaPrincipalMunicipioProcessorV2
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/MatriculaPrincipalMunicipioProcessorV2
        java:app/sirur-ejb/MatriculaPrincipalMunicipioProcessorV2
11:30:16,859 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SicliXmlIntegracaoNegocio' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SicliXmlIntegracaoNegocio!br.gov.caixa.sirur.integracao.mq.sicli.SicliXmlIntegracaoNegocio
        java:app/sirur-ejb/SicliXmlIntegracaoNegocio!br.gov.caixa.sirur.integracao.mq.sicli.SicliXmlIntegracaoNegocio
        java:module/SicliXmlIntegracaoNegocio!br.gov.caixa.sirur.integracao.mq.sicli.SicliXmlIntegracaoNegocio
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SicliXmlIntegracaoNegocio
        java:app/sirur-ejb/SicliXmlIntegracaoNegocio
11:30:16,859 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DocumentacaoAterBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DocumentacaoAterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.DocumentacaoAterBean
        java:app/sirur-ejb/DocumentacaoAterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.DocumentacaoAterBean
        java:module/DocumentacaoAterBean!br.gov.caixa.sirur.bean.impl.unificacaocadastroater.DocumentacaoAterBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DocumentacaoAterBean
        java:app/sirur-ejb/DocumentacaoAterBean
11:30:16,859 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ConsultaAvaliacaoRiscoOperacao' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ConsultaAvaliacaoRiscoOperacao!br.gov.caixa.sirur.integracao.mq.siric.operacao.ConsultaAvaliacaoRiscoOperacao
        java:app/sirur-ejb/ConsultaAvaliacaoRiscoOperacao!br.gov.caixa.sirur.integracao.mq.siric.operacao.ConsultaAvaliacaoRiscoOperacao
        java:module/ConsultaAvaliacaoRiscoOperacao!br.gov.caixa.sirur.integracao.mq.siric.operacao.ConsultaAvaliacaoRiscoOperacao
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ConsultaAvaliacaoRiscoOperacao
        java:app/sirur-ejb/ConsultaAvaliacaoRiscoOperacao
11:30:16,859 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MtrIntegracaoNegocio' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/MtrIntegracaoNegocio!br.gov.caixa.sirur.integracao.rest.mtr.MtrIntegracaoNegocio
        java:app/sirur-ejb/MtrIntegracaoNegocio!br.gov.caixa.sirur.integracao.rest.mtr.MtrIntegracaoNegocio
        java:module/MtrIntegracaoNegocio!br.gov.caixa.sirur.integracao.rest.mtr.MtrIntegracaoNegocio
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/MtrIntegracaoNegocio
        java:app/sirur-ejb/MtrIntegracaoNegocio
11:30:16,859 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'UfSimulacaoBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/UfSimulacaoBean!br.gov.caixa.sirur.bean.impl.UfSimulacaoBean
        java:app/sirur-ejb/UfSimulacaoBean!br.gov.caixa.sirur.bean.impl.UfSimulacaoBean
        java:module/UfSimulacaoBean!br.gov.caixa.sirur.bean.impl.UfSimulacaoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/UfSimulacaoBean
        java:app/sirur-ejb/UfSimulacaoBean
11:30:16,859 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DomainBeanV2' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DomainBeanV2!br.gov.caixa.sirur.bean.impl.DomainBeanV2
        java:app/sirur-ejb/DomainBeanV2!br.gov.caixa.sirur.bean.impl.DomainBeanV2
        java:module/DomainBeanV2!br.gov.caixa.sirur.bean.impl.DomainBeanV2
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DomainBeanV2
        java:app/sirur-ejb/DomainBeanV2
11:30:16,859 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SiicoIntegracaoNegocio' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SiicoIntegracaoNegocio!br.gov.caixa.sirur.integracao.rest.siico.SiicoIntegracaoNegocio
        java:app/sirur-ejb/SiicoIntegracaoNegocio!br.gov.caixa.sirur.integracao.rest.siico.SiicoIntegracaoNegocio
        java:module/SiicoIntegracaoNegocio!br.gov.caixa.sirur.integracao.rest.siico.SiicoIntegracaoNegocio
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SiicoIntegracaoNegocio
        java:app/sirur-ejb/SiicoIntegracaoNegocio
11:30:16,859 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'UnidadeServiceV2Impl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/UnidadeServiceV2Impl!br.gov.caixa.sirur.service.UnidadeServiceV2
        java:app/sirur-ejb/UnidadeServiceV2Impl!br.gov.caixa.sirur.service.UnidadeServiceV2
        java:module/UnidadeServiceV2Impl!br.gov.caixa.sirur.service.UnidadeServiceV2
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/UnidadeServiceV2Impl
        java:app/sirur-ejb/UnidadeServiceV2Impl
11:30:16,860 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DocumentoBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DocumentoBeanImpl!br.gov.caixa.sirur.bean.DocumentoBean
        java:app/sirur-ejb/DocumentoBeanImpl!br.gov.caixa.sirur.bean.DocumentoBean
        java:module/DocumentoBeanImpl!br.gov.caixa.sirur.bean.DocumentoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DocumentoBeanImpl
        java:app/sirur-ejb/DocumentoBeanImpl
11:30:16,860 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'GrupoEconomicoBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/GrupoEconomicoBeanImpl!br.gov.caixa.sirur.bean.GrupoEconomicoBean
        java:app/sirur-ejb/GrupoEconomicoBeanImpl!br.gov.caixa.sirur.bean.GrupoEconomicoBean
        java:module/GrupoEconomicoBeanImpl!br.gov.caixa.sirur.bean.GrupoEconomicoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/GrupoEconomicoBeanImpl
        java:app/sirur-ejb/GrupoEconomicoBeanImpl
11:30:16,860 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DossieOrcamentoBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DossieOrcamentoBean!br.gov.caixa.sirur.integracao.rest.mtr.bean.DossieOrcamentoBean
        java:app/sirur-ejb/DossieOrcamentoBean!br.gov.caixa.sirur.integracao.rest.mtr.bean.DossieOrcamentoBean
        java:module/DossieOrcamentoBean!br.gov.caixa.sirur.integracao.rest.mtr.bean.DossieOrcamentoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DossieOrcamentoBean
        java:app/sirur-ejb/DossieOrcamentoBean
11:30:16,860 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DocumentoProdutoBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DocumentoProdutoBean!br.gov.caixa.sirur.integracao.rest.mtr.bean.DocumentoProdutoBean
        java:app/sirur-ejb/DocumentoProdutoBean!br.gov.caixa.sirur.integracao.rest.mtr.bean.DocumentoProdutoBean
        java:module/DocumentoProdutoBean!br.gov.caixa.sirur.integracao.rest.mtr.bean.DocumentoProdutoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DocumentoProdutoBean
        java:app/sirur-ejb/DocumentoProdutoBean
11:30:16,860 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SituacaoOrcamentoBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SituacaoOrcamentoBean!br.gov.caixa.sirur.bean.impl.orcamento.SituacaoOrcamentoBean
        java:app/sirur-ejb/SituacaoOrcamentoBean!br.gov.caixa.sirur.bean.impl.orcamento.SituacaoOrcamentoBean
        java:module/SituacaoOrcamentoBean!br.gov.caixa.sirur.bean.impl.orcamento.SituacaoOrcamentoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SituacaoOrcamentoBean
        java:app/sirur-ejb/SituacaoOrcamentoBean
11:30:16,860 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MatriculaBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/MatriculaBeanImpl!br.gov.caixa.sirur.bean.MatriculaBean
        java:app/sirur-ejb/MatriculaBeanImpl!br.gov.caixa.sirur.bean.MatriculaBean
        java:module/MatriculaBeanImpl!br.gov.caixa.sirur.bean.MatriculaBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/MatriculaBeanImpl
        java:app/sirur-ejb/MatriculaBeanImpl
11:30:16,860 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'CadastroProducaoRuralBeanImplV2' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/CadastroProducaoRuralBeanImplV2!br.gov.caixa.sirur.bean.impl.CadastroProducaoRuralBeanImplV2
        java:app/sirur-ejb/CadastroProducaoRuralBeanImplV2!br.gov.caixa.sirur.bean.impl.CadastroProducaoRuralBeanImplV2
        java:module/CadastroProducaoRuralBeanImplV2!br.gov.caixa.sirur.bean.impl.CadastroProducaoRuralBeanImplV2
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/CadastroProducaoRuralBeanImplV2
        java:app/sirur-ejb/CadastroProducaoRuralBeanImplV2
11:30:16,860 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'BeanAterTecnicoImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/BeanAterTecnicoImpl!br.gov.caixa.sirur.cadastro.BeanAterTecnico
        java:app/sirur-ejb/BeanAterTecnicoImpl!br.gov.caixa.sirur.cadastro.BeanAterTecnico
        java:module/BeanAterTecnicoImpl!br.gov.caixa.sirur.cadastro.BeanAterTecnico
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/BeanAterTecnicoImpl
        java:app/sirur-ejb/BeanAterTecnicoImpl
11:30:16,860 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SiempIntegracaoNegocio' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SiempIntegracaoNegocio!br.gov.caixa.sirur.integracao.bd.siemp.SiempIntegracaoNegocio
        java:app/sirur-ejb/SiempIntegracaoNegocio!br.gov.caixa.sirur.integracao.bd.siemp.SiempIntegracaoNegocio
        java:module/SiempIntegracaoNegocio!br.gov.caixa.sirur.integracao.bd.siemp.SiempIntegracaoNegocio
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/SiempIntegracaoNegocio
        java:app/sirur-ejb/SiempIntegracaoNegocio
11:30:16,860 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MatriculaPrincipalMunicipioServiceImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/MatriculaPrincipalMunicipioServiceImpl!br.gov.caixa.sirur.service.MatriculaPrincipalMunicipioService
        java:app/sirur-ejb/MatriculaPrincipalMunicipioServiceImpl!br.gov.caixa.sirur.service.MatriculaPrincipalMunicipioService
        java:module/MatriculaPrincipalMunicipioServiceImpl!br.gov.caixa.sirur.service.MatriculaPrincipalMunicipioService
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/MatriculaPrincipalMunicipioServiceImpl
        java:app/sirur-ejb/MatriculaPrincipalMunicipioServiceImpl
11:30:16,860 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TecnicoBeanV2' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/TecnicoBeanV2!br.gov.caixa.sirur.bean.impl.TecnicoBeanV2
        java:app/sirur-ejb/TecnicoBeanV2!br.gov.caixa.sirur.bean.impl.TecnicoBeanV2
        java:module/TecnicoBeanV2!br.gov.caixa.sirur.bean.impl.TecnicoBeanV2
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/TecnicoBeanV2
        java:app/sirur-ejb/TecnicoBeanV2
11:30:16,860 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AtividadeBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AtividadeBeanImpl!br.gov.caixa.sirur.bean.AtividadeBean
        java:app/sirur-ejb/AtividadeBeanImpl!br.gov.caixa.sirur.bean.AtividadeBean
        java:module/AtividadeBeanImpl!br.gov.caixa.sirur.bean.AtividadeBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AtividadeBeanImpl
        java:app/sirur-ejb/AtividadeBeanImpl
11:30:16,861 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ExcluirDadosStepsPosImovelBeneficiadoBean' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ExcluirDadosStepsPosImovelBeneficiadoBean!br.gov.caixa.sirur.bean.impl.orcamento.ExcluirDadosStepsPosImovelBeneficiadoBean
        java:app/sirur-ejb/ExcluirDadosStepsPosImovelBeneficiadoBean!br.gov.caixa.sirur.bean.impl.orcamento.ExcluirDadosStepsPosImovelBeneficiadoBean
        java:module/ExcluirDadosStepsPosImovelBeneficiadoBean!br.gov.caixa.sirur.bean.impl.orcamento.ExcluirDadosStepsPosImovelBeneficiadoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ExcluirDadosStepsPosImovelBeneficiadoBean
        java:app/sirur-ejb/ExcluirDadosStepsPosImovelBeneficiadoBean
11:30:16,861 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TecnicoConveniadoBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/TecnicoConveniadoBeanImpl!br.gov.caixa.sirur.bean.TecnicoConveniadoBean
        java:app/sirur-ejb/TecnicoConveniadoBeanImpl!br.gov.caixa.sirur.bean.TecnicoConveniadoBean
        java:module/TecnicoConveniadoBeanImpl!br.gov.caixa.sirur.bean.TecnicoConveniadoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/TecnicoConveniadoBeanImpl
        java:app/sirur-ejb/TecnicoConveniadoBeanImpl
11:30:16,861 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AtividadePecuariaV2ServiceImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AtividadePecuariaV2ServiceImpl!br.gov.caixa.sirur.service.AtividadePecuriariaV2Service
        java:app/sirur-ejb/AtividadePecuariaV2ServiceImpl!br.gov.caixa.sirur.service.AtividadePecuriariaV2Service
        java:module/AtividadePecuariaV2ServiceImpl!br.gov.caixa.sirur.service.AtividadePecuriariaV2Service
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AtividadePecuariaV2ServiceImpl
        java:app/sirur-ejb/AtividadePecuariaV2ServiceImpl
11:30:16,861 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutorRuralBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ProdutorRuralBeanImpl!br.gov.caixa.sirur.bean.ProdutorRuralBean
        java:app/sirur-ejb/ProdutorRuralBeanImpl!br.gov.caixa.sirur.bean.ProdutorRuralBean
        java:module/ProdutorRuralBeanImpl!br.gov.caixa.sirur.bean.ProdutorRuralBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ProdutorRuralBeanImpl
        java:app/sirur-ejb/ProdutorRuralBeanImpl
11:30:16,861 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AtividadeAgricolaServiceV2Impl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AtividadeAgricolaServiceV2Impl!br.gov.caixa.sirur.service.AtividadeAgricolaServiceV2
        java:app/sirur-ejb/AtividadeAgricolaServiceV2Impl!br.gov.caixa.sirur.service.AtividadeAgricolaServiceV2
        java:module/AtividadeAgricolaServiceV2Impl!br.gov.caixa.sirur.service.AtividadeAgricolaServiceV2
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AtividadeAgricolaServiceV2Impl
        java:app/sirur-ejb/AtividadeAgricolaServiceV2Impl
11:30:16,861 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DocumentoAterBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DocumentoAterBeanImpl!br.gov.caixa.sirur.bean.DocumentoAterBean
        java:app/sirur-ejb/DocumentoAterBeanImpl!br.gov.caixa.sirur.bean.DocumentoAterBean
        java:module/DocumentoAterBeanImpl!br.gov.caixa.sirur.bean.DocumentoAterBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/DocumentoAterBeanImpl
        java:app/sirur-ejb/DocumentoAterBeanImpl
11:30:16,861 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ComunicadoBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ComunicadoBeanImpl!br.gov.caixa.sirur.bean.ComunicadoBean
        java:app/sirur-ejb/ComunicadoBeanImpl!br.gov.caixa.sirur.bean.ComunicadoBean
        java:module/ComunicadoBeanImpl!br.gov.caixa.sirur.bean.ComunicadoBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/ComunicadoBeanImpl
        java:app/sirur-ejb/ComunicadoBeanImpl
11:30:16,861 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'BeanRiscoCreditoImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/BeanRiscoCreditoImpl!br.gov.caixa.sirur.base.BeanRiscoCredito
        java:app/sirur-ejb/BeanRiscoCreditoImpl!br.gov.caixa.sirur.base.BeanRiscoCredito
        java:module/BeanRiscoCreditoImpl!br.gov.caixa.sirur.base.BeanRiscoCredito
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/BeanRiscoCreditoImpl
        java:app/sirur-ejb/BeanRiscoCreditoImpl
11:30:16,861 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'UnidadeIntegracaoNegocio' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/UnidadeIntegracaoNegocio!br.gov.caixa.sirur.integracao.rest.unidade.UnidadeIntegracaoNegocio
        java:app/sirur-ejb/UnidadeIntegracaoNegocio!br.gov.caixa.sirur.integracao.rest.unidade.UnidadeIntegracaoNegocio
        java:module/UnidadeIntegracaoNegocio!br.gov.caixa.sirur.integracao.rest.unidade.UnidadeIntegracaoNegocio
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/UnidadeIntegracaoNegocio
        java:app/sirur-ejb/UnidadeIntegracaoNegocio
11:30:16,861 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AtividadeAgricolaBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AtividadeAgricolaBeanImpl!br.gov.caixa.sirur.bean.AtividadeAgricolaBean
        java:app/sirur-ejb/AtividadeAgricolaBeanImpl!br.gov.caixa.sirur.bean.AtividadeAgricolaBean
        java:module/AtividadeAgricolaBeanImpl!br.gov.caixa.sirur.bean.AtividadeAgricolaBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/AtividadeAgricolaBeanImpl
        java:app/sirur-ejb/AtividadeAgricolaBeanImpl
11:30:16,861 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TecnicoConveniadoAssistenciaBeanImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/TecnicoConveniadoAssistenciaBeanImpl!br.gov.caixa.sirur.bean.TecnicoConveniadoAssistenciaBean
        java:app/sirur-ejb/TecnicoConveniadoAssistenciaBeanImpl!br.gov.caixa.sirur.bean.TecnicoConveniadoAssistenciaBean
        java:module/TecnicoConveniadoAssistenciaBeanImpl!br.gov.caixa.sirur.bean.TecnicoConveniadoAssistenciaBean
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/TecnicoConveniadoAssistenciaBeanImpl
        java:app/sirur-ejb/TecnicoConveniadoAssistenciaBeanImpl
11:30:16,861 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-6) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'BeanSirurImpl' na unidade de implementação 'subdeployment "sirur-ejb.jar" of deployment "sifec-sirur-3.54.51.28.ear"' são como segue:
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/BeanSirurImpl!br.gov.caixa.sirur.base.BeanSirur
        java:app/sirur-ejb/BeanSirurImpl!br.gov.caixa.sirur.base.BeanSirur
        java:module/BeanSirurImpl!br.gov.caixa.sirur.base.BeanSirur
        java:global/sifec-sirur-3.54.51.28/sirur-ejb/BeanSirurImpl
        java:app/sirur-ejb/BeanSirurImpl
11:30:16,871 INFO  [org.jipijapa] (MSC service thread 1-7) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-sirur-3.54.51.28.ear#SIEMP-PU
11:30:16,872 INFO  [org.jipijapa] (MSC service thread 1-7) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-sirur-3.54.51.28.ear#fecDS
11:30:16,901 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 160) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'sifec-sirur-3.54.51.28.ear#fecDS'
11:30:16,902 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 159) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'sifec-sirur-3.54.51.28.ear#SIEMP-PU'
11:30:16,905 WARN  [org.jboss.as.ejb3] (MSC service thread 1-4) WFLYEJB0131: Jakarta Enterprise Beans br.gov.caixa.sirur.ldap.ConexaoLDAP não devem ter um método final ou estático (getAtributosUsuarioInternoPorLogin)
11:30:16,906 WARN  [org.jboss.as.ejb3] (MSC service thread 1-4) WFLYEJB0131: Jakarta Enterprise Beans br.gov.caixa.sirur.ldap.ConexaoLDAP não devem ter um método final ou estático (getAtributosUsuarioExternoPorLogin)
11:30:16,906 WARN  [org.jboss.as.ejb3] (MSC service thread 1-4) WFLYEJB0131: Jakarta Enterprise Beans br.gov.caixa.sirur.ldap.ConexaoLDAP não devem ter um método final ou estático (getAtributosUsuarioPorLogin)
11:30:17,143 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.pu
11:30:17,144 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.rur.pu
11:30:17,211 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 158) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.pu'
11:30:17,211 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 91) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.rur.pu'
Caused by: java.sql.SQLException: ORA-01017: invalid username/password; logon denied
11:30:18,330 ERROR [org.jboss.msc.service.fail] (ServerService Thread Pool -- 91) MSC000001: Failed to start service jboss.persistenceunit."sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.rur.pu": org.jboss.msc.service.StartException in service jboss.persistenceunit."sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.rur.pu": java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false
Caused by: java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false
11:30:41,810 ERROR [org.jboss.msc.service.fail] (ServerService Thread Pool -- 158) MSC000001: Failed to start service jboss.persistenceunit."sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.pu": org.jboss.msc.service.StartException in service jboss.persistenceunit."sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.pu": java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false
Caused by: java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false
11:30:41,816 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 148) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SIRUR")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {
    "jboss.persistenceunit.\"sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.rur.pu\"" => "java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false
    Caused by: java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false ",
    "jboss.persistenceunit.\"sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.pu\"" => "java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false
    Caused by: java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false "
11:30:41,816 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 148) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SIRUR")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {
    "jboss.persistenceunit.\"sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.rur.pu\"" => "java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false
    Caused by: java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false ",
    "jboss.persistenceunit.\"sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.pu\"" => "java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false
    Caused by: java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false "
11:30:41,816 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 148) WFLYSRV0021: O procedimento da implantação "sifec-sirur-3.54.51.28.ear" foi revertido com mensagem de falha:
    "jboss.persistenceunit.\"sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.rur.pu\"" => "java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false
    Caused by: java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false ",
    "jboss.persistenceunit.\"sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.pu\"" => "java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false
    Caused by: java.lang.IllegalArgumentException: Duplicate generator name gen you will likely want to set the property hibernate.jpa.compliance.global_id_generators to false "
11:30:41,817 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 159) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'sifec-sirur-3.54.51.28.ear#SIEMP-PU'
11:30:41,818 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 160) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'sifec-sirur-3.54.51.28.ear#fecDS'
11:30:41,822 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 91) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.rur.pu'
11:30:41,822 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 161) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'sifec-sirur-3.54.51.28.ear/sirur-ejb.jar#fec.pu'
11:30:41,832 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 159) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'sifec-sirur-3.54.51.28.ear#SIEMP-PU'
11:30:41,835 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 160) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'sifec-sirur-3.54.51.28.ear#fecDS'
11:30:41,855 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-6) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: sirur-ejb.jar) em 38ms
11:30:41,876 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-5) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: sirur-web.war) em 60ms
11:30:41,888 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-5) WFLYSRV0028: Implantação interrompida SIRUR (runtime-name: sifec-sirur-3.54.51.28.ear) em 72ms
