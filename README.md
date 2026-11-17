
16:05:52,968 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-4) WFLYSRV0027: Iniciando a implantação do "SIAPX_JavaWeb" (runtime-name: "sifec-apx-1.7.9.4-b40.ear")
16:05:54,331 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "apx-web.war")
16:05:54,331 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-4) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "apx-ejb.jar")
16:05:54,348 INFO  [org.jboss.as.jpa] (MSC service thread 1-4) WFLYJPA0002: Ler persistence.xml para fecDS
16:05:54,409 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-apx-1.7.9.4-b40.ear#fecDS
16:05:54,410 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 293) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'sifec-apx-1.7.9.4-b40.ear#fecDS'
16:05:54,410 INFO  [org.jboss.weld.deployer] (MSC service thread 1-3) WFLYWELD0003: Processando da implantação weld sifec-apx-1.7.9.4-b40.ear
16:05:54,443 WARN  [org.hibernate.validator.internal.engine.ValidatorFactoryImpl] (MSC service thread 1-3) HV000258: Expression Language interpolation features are not explicitly enabled/disabled. Use 'ORG_HIBERNATE_VALIDATOR_EXPRESSION_LANGUAGE_ENABLED' environment variable, or 'org.hibernate.validator.expressionLanguageEnabled' system property to define the behavior. Defaulting to expression language features being disabled.
16:05:54,446 INFO  [org.jboss.keycloak] (MSC service thread 1-4) Keycloak subsystem override for deployment apx-web.war
16:05:54,447 INFO  [org.jboss.weld.deployer] (MSC service thread 1-4) WFLYWELD0003: Processando da implantação weld apx-web.war
16:05:54,461 INFO  [org.jboss.weld.deployer] (MSC service thread 1-7) WFLYWELD0003: Processando da implantação weld apx-ejb.jar
16:05:54,462 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DAOBarramentoFactory' na unidade de implementação 'subdeployment "apx-ejb.jar" of deployment "sifec-apx-1.7.9.4-b40.ear"' são como segue:

        java:global/sifec-apx-1.7.9.4-b40/apx-ejb/DAOBarramentoFactory!br.gov.caixa.emprestimo.barramento.dao.DAOBarramentoFactory
        java:app/apx-ejb/DAOBarramentoFactory!br.gov.caixa.emprestimo.barramento.dao.DAOBarramentoFactory
        java:module/DAOBarramentoFactory!br.gov.caixa.emprestimo.barramento.dao.DAOBarramentoFactory
        java:global/sifec-apx-1.7.9.4-b40/apx-ejb/DAOBarramentoFactory
        java:app/apx-ejb/DAOBarramentoFactory
        java:module/DAOBarramentoFactory

16:05:54,462 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ConvenioLocator' na unidade de implementação 'subdeployment "apx-ejb.jar" of deployment "sifec-apx-1.7.9.4-b40.ear"' são como segue:

        java:global/sifec-apx-1.7.9.4-b40/apx-ejb/ConvenioLocator!br.gov.caixa.apx.negocio.convenio.ConvenioLocator
        java:app/apx-ejb/ConvenioLocator!br.gov.caixa.apx.negocio.convenio.ConvenioLocator
        java:module/ConvenioLocator!br.gov.caixa.apx.negocio.convenio.ConvenioLocator
        java:global/sifec-apx-1.7.9.4-b40/apx-ejb/ConvenioLocator
        java:app/apx-ejb/ConvenioLocator
        java:module/ConvenioLocator

16:05:54,462 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'MargemConsignavelBean' na unidade de implementação 'subdeployment "apx-ejb.jar" of deployment "sifec-apx-1.7.9.4-b40.ear"' são como segue:

        java:global/sifec-apx-1.7.9.4-b40/apx-ejb/MargemConsignavelBean!br.gov.caixa.apx.negocio.MargemConsignavelBean
        java:app/apx-ejb/MargemConsignavelBean!br.gov.caixa.apx.negocio.MargemConsignavelBean
        java:module/MargemConsignavelBean!br.gov.caixa.apx.negocio.MargemConsignavelBean
        java:global/sifec-apx-1.7.9.4-b40/apx-ejb/MargemConsignavelBean
        java:app/apx-ejb/MargemConsignavelBean
        java:module/MargemConsignavelBean

16:05:54,474 INFO  [org.jipijapa] (MSC service thread 1-3) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-apx-1.7.9.4-b40.ear#fecDS
16:05:54,476 WARN  [org.jboss.as.connector.deployers.jdbc] (MSC service thread 1-3) WFLYJCA0003: Não foi possível instanciar a classe do driver "org.olap4j.driver.xmla.XmlaOlap4jDriver": java.lang.NoSuchMethodException: org.olap4j.driver.xmla.XmlaOlap4jDriver.<init>()
16:05:54,524 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 293) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'sifec-apx-1.7.9.4-b40.ear#fecDS'
16:05:54,525 INFO  [org.hibernate.dialect.Dialect] (ServerService Thread Pool -- 293) HHH000400: Using dialect: org.hibernate.dialect.DB2Dialect
16:05:54,534 INFO  [org.hibernate.envers.boot.internal.EnversServiceImpl] (ServerService Thread Pool -- 293) Envers integration enabled? : true
16:05:54,559 WARN  [org.hibernate.validator.internal.engine.ValidatorFactoryImpl] (ServerService Thread Pool -- 293) HV000258: Expression Language interpolation features are not explicitly enabled/disabled. Use 'ORG_HIBERNATE_VALIDATOR_EXPRESSION_LANGUAGE_ENABLED' environment variable, or 'org.hibernate.validator.expressionLanguageEnabled' system property to define the behavior. Defaulting to expression language features being disabled.
16:05:54,585 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 262) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SIAPX_JavaWeb")]) - falha na descrição: {
    "WFLYCTL0412: Serviços necessários que não estão instalados:" => ["jboss.naming.context.java.jboss.mail.APXMail"],
    "WFLYCTL0180: Os serviços com falta/indisponibilidade de dependências " => ["jboss.deployment.unit.\"sifec-apx-1.7.9.4-b40.ear\".WeldStartService faltam [jboss.naming.context.java.jboss.mail.APXMail]"]
}
16:05:54,589 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 262) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SIAPX_JavaWeb")]) - falha na descrição: {
    "WFLYCTL0412: Serviços necessários que não estão instalados:" => ["jboss.naming.context.java.jboss.mail.APXMail"],
    "WFLYCTL0180: Os serviços com falta/indisponibilidade de dependências " => ["jboss.deployment.unit.\"sifec-apx-1.7.9.4-b40.ear\".WeldStartService faltam [jboss.naming.context.java.jboss.mail.APXMail]"]
}
16:05:54,590 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 262) WFLYSRV0021: O procedimento da implantação "sifec-apx-1.7.9.4-b40.ear" foi revertido com mensagem de falha:
{
    "WFLYCTL0412: Serviços necessários que não estão instalados:" => ["jboss.naming.context.java.jboss.mail.APXMail"],
    "WFLYCTL0180: Os serviços com falta/indisponibilidade de dependências " => ["jboss.deployment.unit.\"sifec-apx-1.7.9.4-b40.ear\".WeldStartService faltam [jboss.naming.context.java.jboss.mail.APXMail]"]
}
16:05:54,590 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 285) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'sifec-apx-1.7.9.4-b40.ear#fecDS'
16:05:54,598 INFO  [org.hibernate.orm.beans] (ServerService Thread Pool -- 285) HHH10005004: Stopping BeanContainer : org.hibernate.resource.beans.container.internal.CdiBeanContainerExtendedAccessImpl@51b13536
16:05:54,599 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 285) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'sifec-apx-1.7.9.4-b40.ear#fecDS'
16:05:54,607 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-6) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: apx-ejb.jar) em 17ms
16:05:54,615 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-8) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: apx-web.war) em 24ms
16:05:54,620 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-8) WFLYSRV0028: Implantação interrompida SIAPX_JavaWeb (runtime-name: sifec-apx-1.7.9.4-b40.ear) em 30ms

 
