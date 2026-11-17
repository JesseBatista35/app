
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# LOG=/opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log
tail -f $LOG | grep -aE "construcard|WFLYSRV00(10|21)|WFLYCTL0013|WFLYCTL0412|WELD-0014|ERROR|Contexto web registrado"
16:28:06,575 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 116) WFLYUT0021: Contexto web registrado: '/apx-web' para servidor 'default-server'
16:28:06,609 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 110) WFLYSRV0010: "SIAPX_JavaWeb" foi implantado (runtime-name: "sifec-apx-1.7.9.4-b40.ear")
16:33:31,522 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-5) WFLYSRV0027: Iniciando a implantação do "SIFEC-CONSTRUCARD" (runtime-name: "construcard-1.23.1.2-b64.ear")
16:33:31,780 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-5) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "construcard-web.war")
16:33:31,780 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-6) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "construcard-ejb.jar")
16:33:32,235 WARN  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0059: A entrada do caminho da classe toolbox.jar em /content/construcard-1.23.1.2-b64.ear/construcard-web.war/WEB-INF/lib/itext-2.0.8.jar não direciona a um jar válido para a referência do caminho da classe.
16:33:32,454 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para construcard-1.23.1.2-b64.ear#fecDS
16:33:32,455 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para construcard-1.23.1.2-b64.ear#SIEMP-PU
16:33:32,455 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para construcard-1.23.1.2-b64.ear/construcard-ejb.jar#Siemp2EjbSybase
16:33:32,456 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para construcard-1.23.1.2-b64.ear/construcard-ejb.jar#fecDS
16:33:32,456 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 110) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'construcard-1.23.1.2-b64.ear#SIEMP-PU'
16:33:32,458 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 115) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'construcard-1.23.1.2-b64.ear#fecDS'
16:33:32,469 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 117) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'construcard-1.23.1.2-b64.ear/construcard-ejb.jar#fecDS'
16:33:32,481 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 118) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'construcard-1.23.1.2-b64.ear/construcard-ejb.jar#Siemp2EjbSybase'
16:33:32,506 INFO  [org.jboss.weld.deployer] (MSC service thread 1-6) WFLYWELD0003: Processando da implantação weld construcard-1.23.1.2-b64.ear
16:33:32,560 INFO  [org.jboss.keycloak] (MSC service thread 1-6) Keycloak subsystem override for deployment construcard-web.war
16:33:32,560 INFO  [org.jboss.weld.deployer] (MSC service thread 1-6) WFLYWELD0003: Processando da implantação weld construcard-web.war
16:33:32,594 INFO  [org.jboss.weld.deployer] (MSC service thread 1-7) WFLYWELD0003: Processando da implantação weld construcard-ejb.jar
16:33:32,596 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'CnaeConstrucardBean' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/CnaeConstrucardBean!br.gov.caixa.construcard.negocio.CnaeConstrucardBean
        java:app/construcard-ejb/CnaeConstrucardBean!br.gov.caixa.construcard.negocio.CnaeConstrucardBean
        java:module/CnaeConstrucardBean!br.gov.caixa.construcard.negocio.CnaeConstrucardBean
        java:global/construcard-1.23.1.2-b64/construcard-ejb/CnaeConstrucardBean!br.gov.caixa.construcard.negocio.CnaeConstrucardService
        java:app/construcard-ejb/CnaeConstrucardBean!br.gov.caixa.construcard.negocio.CnaeConstrucardService
        java:module/CnaeConstrucardBean!br.gov.caixa.construcard.negocio.CnaeConstrucardService
16:33:32,596 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'CnaeConstrucardNegocioImpl' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/CnaeConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.CnaeConstrucardNegocioImpl
        java:app/construcard-ejb/CnaeConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.CnaeConstrucardNegocioImpl
        java:module/CnaeConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.CnaeConstrucardNegocioImpl
        java:global/construcard-1.23.1.2-b64/construcard-ejb/CnaeConstrucardNegocioImpl
        java:app/construcard-ejb/CnaeConstrucardNegocioImpl
16:33:32,596 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ConstrucardBean' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/ConstrucardBean!br.gov.caixa.construcard.negocio.ConstrucardService
        java:app/construcard-ejb/ConstrucardBean!br.gov.caixa.construcard.negocio.ConstrucardService
        java:module/ConstrucardBean!br.gov.caixa.construcard.negocio.ConstrucardService
        java:global/construcard-1.23.1.2-b64/construcard-ejb/ConstrucardBean!br.gov.caixa.construcard.negocio.ConstrucardBean
        java:app/construcard-ejb/ConstrucardBean!br.gov.caixa.construcard.negocio.ConstrucardBean
        java:module/ConstrucardBean!br.gov.caixa.construcard.negocio.ConstrucardBean
16:33:32,596 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EstabelecimentoConstrucardNegocioImpl' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/EstabelecimentoConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.EstabelecimentoConstrucardNegocioImpl
        java:app/construcard-ejb/EstabelecimentoConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.EstabelecimentoConstrucardNegocioImpl
        java:module/EstabelecimentoConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.EstabelecimentoConstrucardNegocioImpl
        java:global/construcard-1.23.1.2-b64/construcard-ejb/EstabelecimentoConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.EstabelecimentoConstrucardNegocio
        java:app/construcard-ejb/EstabelecimentoConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.EstabelecimentoConstrucardNegocio
        java:module/EstabelecimentoConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.EstabelecimentoConstrucardNegocio
16:33:32,596 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DAOBarramentoFactory' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/DAOBarramentoFactory!br.gov.caixa.construcard.barramento.dao.DAOBarramentoFactory
        java:app/construcard-ejb/DAOBarramentoFactory!br.gov.caixa.construcard.barramento.dao.DAOBarramentoFactory
        java:module/DAOBarramentoFactory!br.gov.caixa.construcard.barramento.dao.DAOBarramentoFactory
        java:global/construcard-1.23.1.2-b64/construcard-ejb/DAOBarramentoFactory
        java:app/construcard-ejb/DAOBarramentoFactory
16:33:32,596 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutorLog' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/ProdutorLog!br.gov.caixa.construcard.log.ProdutorLog
        java:app/construcard-ejb/ProdutorLog!br.gov.caixa.construcard.log.ProdutorLog
        java:module/ProdutorLog!br.gov.caixa.construcard.log.ProdutorLog
        java:global/construcard-1.23.1.2-b64/construcard-ejb/ProdutorLog
        java:app/construcard-ejb/ProdutorLog
16:33:32,596 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MaoDeObraConstrucardNegocioImpl' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/MaoDeObraConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.MaoDeObraConstrucardNegocioImpl
        java:app/construcard-ejb/MaoDeObraConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.MaoDeObraConstrucardNegocioImpl
        java:module/MaoDeObraConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.MaoDeObraConstrucardNegocioImpl
        java:global/construcard-1.23.1.2-b64/construcard-ejb/MaoDeObraConstrucardNegocioImpl
        java:app/construcard-ejb/MaoDeObraConstrucardNegocioImpl
16:33:32,596 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'CompraConstrucardNegocioImpl' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/CompraConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.CompraConstrucardNegocio
        java:app/construcard-ejb/CompraConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.CompraConstrucardNegocio
        java:module/CompraConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.CompraConstrucardNegocio
        java:global/construcard-1.23.1.2-b64/construcard-ejb/CompraConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.CompraConstrucardNegocioImpl
        java:app/construcard-ejb/CompraConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.CompraConstrucardNegocioImpl
        java:module/CompraConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.CompraConstrucardNegocioImpl
16:33:32,596 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EstabelecimentoConstrucardBean' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/EstabelecimentoConstrucardBean!br.gov.caixa.construcard.negocio.EstabelecimentoConstrucardService
        java:app/construcard-ejb/EstabelecimentoConstrucardBean!br.gov.caixa.construcard.negocio.EstabelecimentoConstrucardService
        java:module/EstabelecimentoConstrucardBean!br.gov.caixa.construcard.negocio.EstabelecimentoConstrucardService
        java:global/construcard-1.23.1.2-b64/construcard-ejb/EstabelecimentoConstrucardBean!br.gov.caixa.construcard.negocio.EstabelecimentoConstrucardBean
        java:app/construcard-ejb/EstabelecimentoConstrucardBean!br.gov.caixa.construcard.negocio.EstabelecimentoConstrucardBean
        java:module/EstabelecimentoConstrucardBean!br.gov.caixa.construcard.negocio.EstabelecimentoConstrucardBean
16:33:32,596 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DocumentoConstrucardBean' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/DocumentoConstrucardBean!br.gov.caixa.construcard.negocio.DocumentoConstrucardService
        java:app/construcard-ejb/DocumentoConstrucardBean!br.gov.caixa.construcard.negocio.DocumentoConstrucardService
        java:module/DocumentoConstrucardBean!br.gov.caixa.construcard.negocio.DocumentoConstrucardService
        java:global/construcard-1.23.1.2-b64/construcard-ejb/DocumentoConstrucardBean!br.gov.caixa.construcard.negocio.DocumentoConstrucardBean
        java:app/construcard-ejb/DocumentoConstrucardBean!br.gov.caixa.construcard.negocio.DocumentoConstrucardBean
        java:module/DocumentoConstrucardBean!br.gov.caixa.construcard.negocio.DocumentoConstrucardBean
16:33:32,596 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DadosPessoaisSICLIBean' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/DadosPessoaisSICLIBean!br.gov.caixa.construcard.negocio.DadosPessoaisSICLIBean
        java:app/construcard-ejb/DadosPessoaisSICLIBean!br.gov.caixa.construcard.negocio.DadosPessoaisSICLIBean
        java:module/DadosPessoaisSICLIBean!br.gov.caixa.construcard.negocio.DadosPessoaisSICLIBean
        java:global/construcard-1.23.1.2-b64/construcard-ejb/DadosPessoaisSICLIBean!br.gov.caixa.construcard.negocio.DadosPessoaisSICLIService
        java:app/construcard-ejb/DadosPessoaisSICLIBean!br.gov.caixa.construcard.negocio.DadosPessoaisSICLIService
        java:module/DadosPessoaisSICLIBean!br.gov.caixa.construcard.negocio.DadosPessoaisSICLIService
16:33:32,596 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SicliConstrucardNegocioImpl' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/SicliConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.SicliConstrucardNegocioImpl
        java:app/construcard-ejb/SicliConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.SicliConstrucardNegocioImpl
        java:module/SicliConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.SicliConstrucardNegocioImpl
        java:global/construcard-1.23.1.2-b64/construcard-ejb/SicliConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.SicliConstrucardNegocio
        java:app/construcard-ejb/SicliConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.SicliConstrucardNegocio
        java:module/SicliConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.SicliConstrucardNegocio
16:33:32,596 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'CompraConstrucardBean' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/CompraConstrucardBean!br.gov.caixa.construcard.negocio.CompraConstrucardBean
        java:app/construcard-ejb/CompraConstrucardBean!br.gov.caixa.construcard.negocio.CompraConstrucardBean
        java:module/CompraConstrucardBean!br.gov.caixa.construcard.negocio.CompraConstrucardBean
        java:global/construcard-1.23.1.2-b64/construcard-ejb/CompraConstrucardBean!br.gov.caixa.construcard.negocio.CompraConstrucardService
        java:app/construcard-ejb/CompraConstrucardBean!br.gov.caixa.construcard.negocio.CompraConstrucardService
        java:module/CompraConstrucardBean!br.gov.caixa.construcard.negocio.CompraConstrucardService
16:33:32,596 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoDeRiscoDAO' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/AvaliacaoDeRiscoDAO!br.gov.caixa.construcard.dao.AvaliacaoDeRiscoDAO
        java:app/construcard-ejb/AvaliacaoDeRiscoDAO!br.gov.caixa.construcard.dao.AvaliacaoDeRiscoDAO
        java:module/AvaliacaoDeRiscoDAO!br.gov.caixa.construcard.dao.AvaliacaoDeRiscoDAO
        java:global/construcard-1.23.1.2-b64/construcard-ejb/AvaliacaoDeRiscoDAO
        java:app/construcard-ejb/AvaliacaoDeRiscoDAO
16:33:32,597 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ConvenenteConstrucardBean' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/ConvenenteConstrucardBean!br.gov.caixa.construcard.negocio.ConvenenteConstrucardService
        java:app/construcard-ejb/ConvenenteConstrucardBean!br.gov.caixa.construcard.negocio.ConvenenteConstrucardService
        java:module/ConvenenteConstrucardBean!br.gov.caixa.construcard.negocio.ConvenenteConstrucardService
        java:global/construcard-1.23.1.2-b64/construcard-ejb/ConvenenteConstrucardBean!br.gov.caixa.construcard.negocio.ConvenenteConstrucardBean
        java:app/construcard-ejb/ConvenenteConstrucardBean!br.gov.caixa.construcard.negocio.ConvenenteConstrucardBean
        java:module/ConvenenteConstrucardBean!br.gov.caixa.construcard.negocio.ConvenenteConstrucardBean
16:33:32,597 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ConvenenteConstrucardNegocioImpl' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/ConvenenteConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.ConvenenteConstrucardNegocioImpl
        java:app/construcard-ejb/ConvenenteConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.ConvenenteConstrucardNegocioImpl
        java:module/ConvenenteConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.ConvenenteConstrucardNegocioImpl
        java:global/construcard-1.23.1.2-b64/construcard-ejb/ConvenenteConstrucardNegocioImpl
        java:app/construcard-ejb/ConvenenteConstrucardNegocioImpl
16:33:32,597 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TabelaAliquotaConstrucardBean' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/TabelaAliquotaConstrucardBean!br.gov.caixa.construcard.negocio.TabelaAliquotaConstrucardBean
        java:app/construcard-ejb/TabelaAliquotaConstrucardBean!br.gov.caixa.construcard.negocio.TabelaAliquotaConstrucardBean
        java:module/TabelaAliquotaConstrucardBean!br.gov.caixa.construcard.negocio.TabelaAliquotaConstrucardBean
        java:global/construcard-1.23.1.2-b64/construcard-ejb/TabelaAliquotaConstrucardBean!br.gov.caixa.construcard.negocio.TabelaAliquotaConstrucardService
        java:app/construcard-ejb/TabelaAliquotaConstrucardBean!br.gov.caixa.construcard.negocio.TabelaAliquotaConstrucardService
        java:module/TabelaAliquotaConstrucardBean!br.gov.caixa.construcard.negocio.TabelaAliquotaConstrucardService
16:33:32,597 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'CorrespondenteConstrucardBean' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/CorrespondenteConstrucardBean!br.gov.caixa.construcard.negocio.CorrespondenteConstrucardService
        java:app/construcard-ejb/CorrespondenteConstrucardBean!br.gov.caixa.construcard.negocio.CorrespondenteConstrucardService
        java:module/CorrespondenteConstrucardBean!br.gov.caixa.construcard.negocio.CorrespondenteConstrucardService
        java:global/construcard-1.23.1.2-b64/construcard-ejb/CorrespondenteConstrucardBean!br.gov.caixa.construcard.negocio.CorrespondenteConstrucardBean
        java:app/construcard-ejb/CorrespondenteConstrucardBean!br.gov.caixa.construcard.negocio.CorrespondenteConstrucardBean
        java:module/CorrespondenteConstrucardBean!br.gov.caixa.construcard.negocio.CorrespondenteConstrucardBean
16:33:32,597 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'TotalizadorConstrucardBean' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/TotalizadorConstrucardBean!br.gov.caixa.construcard.negocio.TotalizadorConstrucardBean
        java:app/construcard-ejb/TotalizadorConstrucardBean!br.gov.caixa.construcard.negocio.TotalizadorConstrucardBean
        java:module/TotalizadorConstrucardBean!br.gov.caixa.construcard.negocio.TotalizadorConstrucardBean
        java:global/construcard-1.23.1.2-b64/construcard-ejb/TotalizadorConstrucardBean
        java:app/construcard-ejb/TotalizadorConstrucardBean
16:33:32,597 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MaoDeObraConstrucardBean' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/MaoDeObraConstrucardBean!br.gov.caixa.construcard.negocio.MaoDeObraConstrucardService
        java:app/construcard-ejb/MaoDeObraConstrucardBean!br.gov.caixa.construcard.negocio.MaoDeObraConstrucardService
        java:module/MaoDeObraConstrucardBean!br.gov.caixa.construcard.negocio.MaoDeObraConstrucardService
        java:global/construcard-1.23.1.2-b64/construcard-ejb/MaoDeObraConstrucardBean!br.gov.caixa.construcard.negocio.MaoDeObraConstrucardBean
        java:app/construcard-ejb/MaoDeObraConstrucardBean!br.gov.caixa.construcard.negocio.MaoDeObraConstrucardBean
        java:module/MaoDeObraConstrucardBean!br.gov.caixa.construcard.negocio.MaoDeObraConstrucardBean
16:33:32,597 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'CorrespondenteConstrucardNegocioImpl' na unidade de implementação 'subdeployment "construcard-ejb.jar" of deployment "construcard-1.23.1.2-b64.ear"' são como segue:
        java:global/construcard-1.23.1.2-b64/construcard-ejb/CorrespondenteConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.CorrespondenteConstrucardNegocioImpl
        java:app/construcard-ejb/CorrespondenteConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.CorrespondenteConstrucardNegocioImpl
        java:module/CorrespondenteConstrucardNegocioImpl!br.gov.caixa.construcard.negocio.CorrespondenteConstrucardNegocioImpl
        java:global/construcard-1.23.1.2-b64/construcard-ejb/CorrespondenteConstrucardNegocioImpl
        java:app/construcard-ejb/CorrespondenteConstrucardNegocioImpl
16:33:32,601 INFO  [org.jipijapa] (MSC service thread 1-5) JIPIORMV53020253: Cache de segundo nível habilitado para construcard-1.23.1.2-b64.ear#fecDS
16:33:32,601 INFO  [org.jipijapa] (MSC service thread 1-5) JIPIORMV53020253: Cache de segundo nível habilitado para construcard-1.23.1.2-b64.ear#SIEMP-PU
16:33:32,621 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 115) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'construcard-1.23.1.2-b64.ear#fecDS'
16:33:32,621 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 118) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'construcard-1.23.1.2-b64.ear#SIEMP-PU'
16:33:32,706 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para construcard-1.23.1.2-b64.ear/construcard-ejb.jar#Siemp2EjbSybase
16:33:32,706 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para construcard-1.23.1.2-b64.ear/construcard-ejb.jar#fecDS
16:33:32,727 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 115) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'construcard-1.23.1.2-b64.ear/construcard-ejb.jar#fecDS'
16:33:32,728 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 118) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'construcard-1.23.1.2-b64.ear/construcard-ejb.jar#Siemp2EjbSybase'
16:33:32,861 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 7) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.util.ArquillianHelper because of underlying class loading error: Type org.jboss.shrinkwrap.api.asset.Asset from [Module "deployment.construcard-1.23.1.2-b64.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:33:32,872 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 7) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.email.api.operacao.SendMail because of underlying class loading error: Type freemarker.template.TemplateException from [Module "deployment.construcard-1.23.1.2-b64.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:33:33,073 ERROR [org.jboss.msc.service.fail] (MSC service thread 1-2) MSC000001: Failed to start service jboss.deployment.unit."construcard-1.23.1.2-b64.ear".WeldStartService: org.jboss.msc.service.StartException in service jboss.deployment.unit."construcard-1.23.1.2-b64.ear".WeldStartService: Failed to start service
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type MaoDeObraConstrucardNegocio with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.MaoDeObraConstrucardRest.negocio
  at br.gov.caixa.construcard.rest.MaoDeObraConstrucardRest.negocio(MaoDeObraConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type TotalizadorConstrucardService with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.TotalizadorConstrucardRest.service
  at br.gov.caixa.construcard.rest.TotalizadorConstrucardRest.service(TotalizadorConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type ConvenenteConstrucardNegocio with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.ConvenenteConstrucardRest.negocio
  at br.gov.caixa.construcard.rest.ConvenenteConstrucardRest.negocio(ConvenenteConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type CorrespondenteConstrucardNegocio with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.CorrespondenteConstrucardRest.negocio
  at br.gov.caixa.construcard.rest.CorrespondenteConstrucardRest.negocio(CorrespondenteConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type CnaeConstrucardNegocio with qualifiers @Default
  at injection point [UnbackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.CnaeRest.cnaeConstrucardNegocio
  at br.gov.caixa.construcard.rest.CnaeRest.cnaeConstrucardNegocio(CnaeRest.java:0)
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type MaoDeObraConstrucardNegocio with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.MaoDeObraConstrucardRest.negocio
  at br.gov.caixa.construcard.rest.MaoDeObraConstrucardRest.negocio(MaoDeObraConstrucardRest.java:0)
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type TotalizadorConstrucardService with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.TotalizadorConstrucardRest.service
  at br.gov.caixa.construcard.rest.TotalizadorConstrucardRest.service(TotalizadorConstrucardRest.java:0)
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type ConvenenteConstrucardNegocio with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.ConvenenteConstrucardRest.negocio
  at br.gov.caixa.construcard.rest.ConvenenteConstrucardRest.negocio(ConvenenteConstrucardRest.java:0)
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type CorrespondenteConstrucardNegocio with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.CorrespondenteConstrucardRest.negocio
  at br.gov.caixa.construcard.rest.CorrespondenteConstrucardRest.negocio(CorrespondenteConstrucardRest.java:0)
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type CnaeConstrucardNegocio with qualifiers @Default
  at injection point [UnbackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.CnaeRest.cnaeConstrucardNegocio
  at br.gov.caixa.construcard.rest.CnaeRest.cnaeConstrucardNegocio(CnaeRest.java:0)
16:33:33,082 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 116) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SIFEC-CONSTRUCARD")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"construcard-1.23.1.2-b64.ear\".WeldStartService" => "Failed to start service
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type MaoDeObraConstrucardNegocio with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.MaoDeObraConstrucardRest.negocio
  at br.gov.caixa.construcard.rest.MaoDeObraConstrucardRest.negocio(MaoDeObraConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type TotalizadorConstrucardService with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.TotalizadorConstrucardRest.service
  at br.gov.caixa.construcard.rest.TotalizadorConstrucardRest.service(TotalizadorConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type ConvenenteConstrucardNegocio with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.ConvenenteConstrucardRest.negocio
  at br.gov.caixa.construcard.rest.ConvenenteConstrucardRest.negocio(ConvenenteConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type CorrespondenteConstrucardNegocio with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.CorrespondenteConstrucardRest.negocio
  at br.gov.caixa.construcard.rest.CorrespondenteConstrucardRest.negocio(CorrespondenteConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type CnaeConstrucardNegocio with qualifiers @Default
  at injection point [UnbackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.CnaeRest.cnaeConstrucardNegocio
  at br.gov.caixa.construcard.rest.CnaeRest.cnaeConstrucardNegocio(CnaeRest.java:0)
16:33:33,084 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 116) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SIFEC-CONSTRUCARD")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"construcard-1.23.1.2-b64.ear\".WeldStartService" => "Failed to start service
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type MaoDeObraConstrucardNegocio with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.MaoDeObraConstrucardRest.negocio
  at br.gov.caixa.construcard.rest.MaoDeObraConstrucardRest.negocio(MaoDeObraConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type TotalizadorConstrucardService with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.TotalizadorConstrucardRest.service
  at br.gov.caixa.construcard.rest.TotalizadorConstrucardRest.service(TotalizadorConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type ConvenenteConstrucardNegocio with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.ConvenenteConstrucardRest.negocio
  at br.gov.caixa.construcard.rest.ConvenenteConstrucardRest.negocio(ConvenenteConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type CorrespondenteConstrucardNegocio with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.CorrespondenteConstrucardRest.negocio
  at br.gov.caixa.construcard.rest.CorrespondenteConstrucardRest.negocio(CorrespondenteConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type CnaeConstrucardNegocio with qualifiers @Default
  at injection point [UnbackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.CnaeRest.cnaeConstrucardNegocio
  at br.gov.caixa.construcard.rest.CnaeRest.cnaeConstrucardNegocio(CnaeRest.java:0)
16:33:33,086 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 116) WFLYSRV0021: O procedimento da implantação "construcard-1.23.1.2-b64.ear" foi revertido com mensagem de falha:
{"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"construcard-1.23.1.2-b64.ear\".WeldStartService" => "Failed to start service
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type MaoDeObraConstrucardNegocio with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.MaoDeObraConstrucardRest.negocio
  at br.gov.caixa.construcard.rest.MaoDeObraConstrucardRest.negocio(MaoDeObraConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type TotalizadorConstrucardService with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.TotalizadorConstrucardRest.service
  at br.gov.caixa.construcard.rest.TotalizadorConstrucardRest.service(TotalizadorConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type ConvenenteConstrucardNegocio with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.ConvenenteConstrucardRest.negocio
  at br.gov.caixa.construcard.rest.ConvenenteConstrucardRest.negocio(ConvenenteConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type CorrespondenteConstrucardNegocio with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.CorrespondenteConstrucardRest.negocio
  at br.gov.caixa.construcard.rest.CorrespondenteConstrucardRest.negocio(CorrespondenteConstrucardRest.java:0)
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type CnaeConstrucardNegocio with qualifiers @Default
  at injection point [UnbackedAnnotatedField] @Inject private br.gov.caixa.construcard.rest.CnaeRest.cnaeConstrucardNegocio
  at br.gov.caixa.construcard.rest.CnaeRest.cnaeConstrucardNegocio(CnaeRest.java:0)
16:33:33,099 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 115) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'construcard-1.23.1.2-b64.ear/construcard-ejb.jar#fecDS'
16:33:33,099 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 117) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'construcard-1.23.1.2-b64.ear/construcard-ejb.jar#Siemp2EjbSybase'
16:33:33,099 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 110) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'construcard-1.23.1.2-b64.ear#fecDS'
16:33:33,099 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 118) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'construcard-1.23.1.2-b64.ear#SIEMP-PU'
16:33:33,109 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 118) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'construcard-1.23.1.2-b64.ear/construcard-ejb.jar#Siemp2EjbSybase'
16:33:33,109 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 117) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'construcard-1.23.1.2-b64.ear#SIEMP-PU'
16:33:33,109 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 110) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'construcard-1.23.1.2-b64.ear/construcard-ejb.jar#fecDS'
16:33:33,111 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 115) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'construcard-1.23.1.2-b64.ear#fecDS'
16:33:33,139 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: construcard-ejb.jar) em 50ms
16:33:33,167 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-8) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: construcard-web.war) em 79ms
16:33:33,169 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-8) WFLYSRV0028: Implantação interrompida SIFEC-CONSTRUCARD (runtime-name: construcard-1.23.1.2-b64.ear) em 83ms

