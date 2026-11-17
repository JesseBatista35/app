[root@cbrdeapllx473 p585600]# tail -f $LOG | grep -aE "ban|WFLYSRV00(10|21)|WFLYCTL0013|WFLYCTL0412|WELD-0014|ERROR|Contexto web registrado"
16:41:30,577 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 143) WFLYUT0021: Contexto web registrado: '/minutaGarantias-web' para servidor 'default-server'
16:41:30,609 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 135) WFLYSRV0010: "SICCR-MINUTAS" foi implantado (runtime-name: "sifec-minutaGarantias-1.0.0-b36.ear")
16:42:53,537 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-4) WFLYSRV0027: Iniciando a implantação do "SIFEC-BAN3" (runtime-name: "sifec-ban-1.7.0-b117.ear")
16:42:54,437 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-3) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "siban-api.war")
16:42:54,437 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "siban-ejb.jar")
16:42:55,398 WARN  [org.jboss.as.server.deployment] (MSC service thread 1-3) WFLYSRV0059: A entrada do caminho da classe toolbox.jar em /content/sifec-ban-1.7.0-b117.ear/siban-api.war/WEB-INF/lib/itext-2.0.8.jar não direciona a um jar válido para a referência do caminho da classe.
16:42:55,437 WARN  [org.jboss.as.ejb3] (MSC service thread 1-1) WFLYEJB0525: O 'mappedName' em anotações de Jacarta Enterprise Beans não é suportado. Valor de 'ClienteSibanService' para Jacarta Enterprise Beans 'ClienteSibanService' será ignorado.
16:42:55,437 WARN  [org.jboss.as.ejb3] (MSC service thread 1-1) WFLYEJB0525: O 'mappedName' em anotações de Jacarta Enterprise Beans não é suportado. Valor de 'ImpostoRendaSibanService' para Jacarta Enterprise Beans 'ImpostoRendaSibanService' será ignorado.
16:42:55,437 WARN  [org.jboss.as.ejb3] (MSC service thread 1-1) WFLYEJB0525: O 'mappedName' em anotações de Jacarta Enterprise Beans não é suportado. Valor de 'ContratoSibanService' para Jacarta Enterprise Beans 'ContratoSibanService' será ignorado.
16:42:55,611 INFO  [org.jipijapa] (MSC service thread 1-5) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-ban-1.7.0-b117.ear#fecDS
16:42:55,611 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 135) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'sifec-ban-1.7.0-b117.ear#fecDS'
16:42:55,612 INFO  [org.jipijapa] (MSC service thread 1-7) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-ban-1.7.0-b117.ear/siban-ejb.jar#DsSybaseSIBAN
16:42:55,616 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 142) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'sifec-ban-1.7.0-b117.ear/siban-ejb.jar#DsSybaseSIBAN'
16:42:55,623 INFO  [org.jboss.weld.deployer] (MSC service thread 1-5) WFLYWELD0003: Processando da implantação weld sifec-ban-1.7.0-b117.ear
16:42:55,663 INFO  [org.jboss.weld.deployer] (MSC service thread 1-7) WFLYWELD0003: Processando da implantação weld siban-ejb.jar
16:42:55,665 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ContratoSibanService' na unidade de implementação 'subdeployment "siban-ejb.jar" of deployment "sifec-ban-1.7.0-b117.ear"' são como segue:
        java:global/sifec-ban-1.7.0-b117/siban-ejb/ContratoSibanService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ContratoSibanServiceIface
        java:app/siban-ejb/ContratoSibanService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ContratoSibanServiceIface
        java:module/ContratoSibanService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ContratoSibanServiceIface
        java:jboss/exported/sifec-ban-1.7.0-b117/siban-ejb/ContratoSibanService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ContratoSibanServiceIface
        ejb:sifec-ban-1.7.0-b117/siban-ejb/ContratoSibanService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ContratoSibanServiceIface
        java:global/sifec-ban-1.7.0-b117/siban-ejb/ContratoSibanService
        java:app/siban-ejb/ContratoSibanService
        java:module/ContratoSibanService
16:42:55,665 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'PlanilhaService' na unidade de implementação 'subdeployment "siban-ejb.jar" of deployment "sifec-ban-1.7.0-b117.ear"' são como segue:
        java:global/sifec-ban-1.7.0-b117/siban-ejb/PlanilhaService!br.gov.caixa.arqref.business.consultacontratos.services.siban.PlanilhaServiceIface
        java:app/siban-ejb/PlanilhaService!br.gov.caixa.arqref.business.consultacontratos.services.siban.PlanilhaServiceIface
        java:module/PlanilhaService!br.gov.caixa.arqref.business.consultacontratos.services.siban.PlanilhaServiceIface
        java:jboss/exported/sifec-ban-1.7.0-b117/siban-ejb/PlanilhaService!br.gov.caixa.arqref.business.consultacontratos.services.siban.PlanilhaServiceIface
        ejb:sifec-ban-1.7.0-b117/siban-ejb/PlanilhaService!br.gov.caixa.arqref.business.consultacontratos.services.siban.PlanilhaServiceIface
        java:global/sifec-ban-1.7.0-b117/siban-ejb/PlanilhaService
        java:app/siban-ejb/PlanilhaService
16:42:55,665 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutorLog' na unidade de implementação 'subdeployment "siban-ejb.jar" of deployment "sifec-ban-1.7.0-b117.ear"' são como segue:
        java:global/sifec-ban-1.7.0-b117/siban-ejb/ProdutorLog!br.gov.caixa.siban.log.ProdutorLog
        java:app/siban-ejb/ProdutorLog!br.gov.caixa.siban.log.ProdutorLog
        java:module/ProdutorLog!br.gov.caixa.siban.log.ProdutorLog
        java:global/sifec-ban-1.7.0-b117/siban-ejb/ProdutorLog
        java:app/siban-ejb/ProdutorLog
16:42:55,665 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ResolucaoPrejuizoService' na unidade de implementação 'subdeployment "siban-ejb.jar" of deployment "sifec-ban-1.7.0-b117.ear"' são como segue:
        java:global/sifec-ban-1.7.0-b117/siban-ejb/ResolucaoPrejuizoService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ResolucaoPrejuizoServiceIface
        java:app/siban-ejb/ResolucaoPrejuizoService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ResolucaoPrejuizoServiceIface
        java:module/ResolucaoPrejuizoService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ResolucaoPrejuizoServiceIface
        java:jboss/exported/sifec-ban-1.7.0-b117/siban-ejb/ResolucaoPrejuizoService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ResolucaoPrejuizoServiceIface
        ejb:sifec-ban-1.7.0-b117/siban-ejb/ResolucaoPrejuizoService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ResolucaoPrejuizoServiceIface
        java:global/sifec-ban-1.7.0-b117/siban-ejb/ResolucaoPrejuizoService
        java:app/siban-ejb/ResolucaoPrejuizoService
16:42:55,666 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ClienteSibanService' na unidade de implementação 'subdeployment "siban-ejb.jar" of deployment "sifec-ban-1.7.0-b117.ear"' são como segue:
        java:global/sifec-ban-1.7.0-b117/siban-ejb/ClienteSibanService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ClienteSibanServiceIface
        java:app/siban-ejb/ClienteSibanService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ClienteSibanServiceIface
        java:module/ClienteSibanService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ClienteSibanServiceIface
        java:jboss/exported/sifec-ban-1.7.0-b117/siban-ejb/ClienteSibanService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ClienteSibanServiceIface
        ejb:sifec-ban-1.7.0-b117/siban-ejb/ClienteSibanService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ClienteSibanServiceIface
        java:global/sifec-ban-1.7.0-b117/siban-ejb/ClienteSibanService
        java:app/siban-ejb/ClienteSibanService
        java:module/ClienteSibanService
16:42:55,666 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ImpostoRendaSibanService' na unidade de implementação 'subdeployment "siban-ejb.jar" of deployment "sifec-ban-1.7.0-b117.ear"' são como segue:
        java:global/sifec-ban-1.7.0-b117/siban-ejb/ImpostoRendaSibanService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ImpostoRendaSibanServiceIface
        java:app/siban-ejb/ImpostoRendaSibanService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ImpostoRendaSibanServiceIface
        java:module/ImpostoRendaSibanService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ImpostoRendaSibanServiceIface
        java:jboss/exported/sifec-ban-1.7.0-b117/siban-ejb/ImpostoRendaSibanService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ImpostoRendaSibanServiceIface
        ejb:sifec-ban-1.7.0-b117/siban-ejb/ImpostoRendaSibanService!br.gov.caixa.arqref.business.consultacontratos.services.siban.ImpostoRendaSibanServiceIface
        java:global/sifec-ban-1.7.0-b117/siban-ejb/ImpostoRendaSibanService
        java:app/siban-ejb/ImpostoRendaSibanService
        java:module/ImpostoRendaSibanService
16:42:55,666 INFO  [org.jboss.weld.deployer] (MSC service thread 1-5) WFLYWELD0003: Processando da implantação weld siban-api.war
16:42:55,677 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-5) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'seguranca-sso-SecurityKeycloakUtils' na unidade de implementação 'subdeployment "siban-api.war" of deployment "sifec-ban-1.7.0-b117.ear"' são como segue:
        java:global/sifec-ban-1.7.0-b117/siban-api/seguranca-sso-SecurityKeycloakUtils!br.gov.caixa.sifec.componentes.seguranca.sso.utils.SecurityKeycloakUtils
        java:app/siban-api/seguranca-sso-SecurityKeycloakUtils!br.gov.caixa.sifec.componentes.seguranca.sso.utils.SecurityKeycloakUtils
        java:global/sifec-ban-1.7.0-b117/siban-api/seguranca-sso-SecurityKeycloakUtils
        java:app/siban-api/seguranca-sso-SecurityKeycloakUtils
16:42:55,693 INFO  [org.jipijapa] (MSC service thread 1-5) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-ban-1.7.0-b117.ear#fecDS
16:42:55,737 INFO  [org.jipijapa] (MSC service thread 1-6) JIPIORMV53020253: Cache de segundo nível habilitado para sifec-ban-1.7.0-b117.ear/siban-ejb.jar#DsSybaseSIBAN
16:42:55,756 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 142) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'sifec-ban-1.7.0-b117.ear/siban-ejb.jar#DsSybaseSIBAN'
16:42:55,813 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 135) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'sifec-ban-1.7.0-b117.ear#fecDS'
16:42:56,000 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 5) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.util.ArquillianHelper because of underlying class loading error: Type org.jboss.shrinkwrap.api.asset.Asset from [Module "deployment.sifec-ban-1.7.0-b117.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:42:56,270 WARN  [io.undertow.servlet] (ServerService Thread Pool -- 146) UT015020: Path /siban/swagger.json is secured for some HTTP methods, however it is not secured for [TRACE, HEAD, DELETE, CONNECT, OPTIONS, PUT]
16:42:56,271 WARN  [io.undertow.servlet] (ServerService Thread Pool -- 146) UT015020: Path /siban/* is secured for some HTTP methods, however it is not secured for [TRACE, HEAD, CONNECT, OPTIONS]
16:42:56,423 INFO  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 146) RESTEASY002225: Deploying javax.ws.rs.core.Application: class br.gov.caixa.siban.api.config.JaxRsActivator$Proxy$_$$_WeldClientProxy
16:42:56,432 INFO  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 146) RESTEASY002200: Adding class resource br.gov.caixa.siban.api.PlanilhaEvolucaoDividaPortabilidadeRest from Application class br.gov.caixa.siban.api.config.JaxRsActivator$Proxy$_$$_WeldClientProxy
16:42:56,432 INFO  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 146) RESTEASY002200: Adding class resource br.gov.caixa.siban.api.ClienteRest from Application class br.gov.caixa.siban.api.config.JaxRsActivator$Proxy$_$$_WeldClientProxy
16:42:56,432 INFO  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 146) RESTEASY002200: Adding class resource br.gov.caixa.siban.api.ImpostoRendaRest from Application class br.gov.caixa.siban.api.config.JaxRsActivator$Proxy$_$$_WeldClientProxy
16:42:56,432 INFO  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 146) RESTEASY002200: Adding class resource io.swagger.jaxrs.listing.ApiListingResource from Application class br.gov.caixa.siban.api.config.JaxRsActivator$Proxy$_$$_WeldClientProxy
16:42:56,432 INFO  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 146) RESTEASY002205: Adding provider class io.swagger.jaxrs.listing.SwaggerSerializers from Application class br.gov.caixa.siban.api.config.JaxRsActivator$Proxy$_$$_WeldClientProxy
16:42:56,432 INFO  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 146) RESTEASY002200: Adding class resource br.gov.caixa.siban.api.ContratosRest from Application class br.gov.caixa.siban.api.config.JaxRsActivator$Proxy$_$$_WeldClientProxy
16:42:56,439 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 146) WFLYUT0021: Contexto web registrado: '/siban-api' para servidor 'default-server'
16:42:56,468 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 143) WFLYSRV0010: "SIFEC-BAN3" foi implantado (runtime-name: "sifec-ban-1.7.0-b117.ear")



