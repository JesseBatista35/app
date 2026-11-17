
^C
[root@cbrdeapllx473 p585600]# tail -f $LOG | grep -aE "garantias|WFLYSRV00(10|21)|WFLYCTL0013|WFLYCTL0412|WELD-0014|ERROR|Contexto web registrado"
16:37:38,177 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-2) WFLYSRV0027: Iniciando a implantação do "SIFEC-GARANTIAS4" (runtime-name: "garantias-1.8.0.3-b183.ear")
16:37:39,182 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "garantias-web.war")
16:37:39,182 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-2) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "garantias-ejb.jar")
16:37:39,336 WARN  [org.jboss.as.dependency.private] (MSC service thread 1-2) WFLYSRV0018: A implantação "deployment.garantias-1.8.0.3-b183.ear" está usando um módulo privado ("org.codehaus.jackson.jackson-mapper-asl") que pode ser alterado ou removido em versões futuras sem nenhum aviso.
16:37:39,337 WARN  [org.jboss.as.dependency.private] (MSC service thread 1-4) WFLYSRV0018: A implantação "deployment.garantias-1.8.0.3-b183.ear.garantias-ejb.jar" está usando um módulo privado ("org.codehaus.jackson.jackson-mapper-asl") que pode ser alterado ou removido em versões futuras sem nenhum aviso.
16:37:39,338 WARN  [org.jboss.as.dependency.private] (MSC service thread 1-7) WFLYSRV0018: A implantação "deployment.garantias-1.8.0.3-b183.ear.garantias-web.war" está usando um módulo privado ("org.codehaus.jackson.jackson-mapper-asl") que pode ser alterado ou removido em versões futuras sem nenhum aviso.
16:37:39,338 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para garantias-1.8.0.3-b183.ear#fecDS
16:37:39,339 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para garantias-1.8.0.3-b183.ear#SIEMP-PU
16:37:39,339 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 115) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'garantias-1.8.0.3-b183.ear#fecDS'
16:37:39,339 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 110) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'garantias-1.8.0.3-b183.ear#SIEMP-PU'
16:37:39,362 INFO  [org.jboss.weld.deployer] (MSC service thread 1-4) WFLYWELD0003: Processando da implantação weld garantias-1.8.0.3-b183.ear
16:37:39,402 INFO  [org.jboss.keycloak] (MSC service thread 1-3) Keycloak subsystem override for deployment garantias-web.war
16:37:39,402 INFO  [org.jboss.weld.deployer] (MSC service thread 1-3) WFLYWELD0003: Processando da implantação weld garantias-web.war
16:37:39,404 INFO  [org.jboss.weld.deployer] (MSC service thread 1-7) WFLYWELD0003: Processando da implantação weld garantias-ejb.jar
16:37:39,405 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DAOBarramentoFactory' na unidade de implementação 'subdeployment "garantias-ejb.jar" of deployment "garantias-1.8.0.3-b183.ear"' são como segue:
        java:global/garantias-1.8.0.3-b183/garantias-ejb/DAOBarramentoFactory!br.gov.caixa.garantias.barramento.dao.DAOBarramentoFactory
        java:app/garantias-ejb/DAOBarramentoFactory!br.gov.caixa.garantias.barramento.dao.DAOBarramentoFactory
        java:module/DAOBarramentoFactory!br.gov.caixa.garantias.barramento.dao.DAOBarramentoFactory
        java:global/garantias-1.8.0.3-b183/garantias-ejb/DAOBarramentoFactory
        java:app/garantias-ejb/DAOBarramentoFactory
16:37:39,406 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ServentiaService' na unidade de implementação 'subdeployment "garantias-ejb.jar" of deployment "garantias-1.8.0.3-b183.ear"' são como segue:
        java:global/garantias-1.8.0.3-b183/garantias-ejb/ServentiaService!br.gov.caixa.garantias.negocio.impl.ServentiaService
        java:app/garantias-ejb/ServentiaService!br.gov.caixa.garantias.negocio.impl.ServentiaService
        java:module/ServentiaService!br.gov.caixa.garantias.negocio.impl.ServentiaService
        java:global/garantias-1.8.0.3-b183/garantias-ejb/ServentiaService!br.gov.caixa.garantias.negocio.IServentiaService
        java:app/garantias-ejb/ServentiaService!br.gov.caixa.garantias.negocio.IServentiaService
        java:module/ServentiaService!br.gov.caixa.garantias.negocio.IServentiaService
16:37:39,417 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para garantias-1.8.0.3-b183.ear#fecDS
16:37:39,418 INFO  [org.jipijapa] (MSC service thread 1-2) JIPIORMV53020253: Cache de segundo nível habilitado para garantias-1.8.0.3-b183.ear#SIEMP-PU
16:37:39,443 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 110) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'garantias-1.8.0.3-b183.ear#SIEMP-PU'
16:37:39,567 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 115) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'garantias-1.8.0.3-b183.ear#fecDS'
16:37:39,671 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 6) WELD-000119: Not generating any bean definitions from br.gov.caixa.siacg.swagger.api.client.invoker.ApiClient because of underlying class loading error: Type com.squareup.okhttp.logging.HttpLoggingInterceptor from [Module "deployment.garantias-1.8.0.3-b183.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:37:39,695 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 6) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.siemp.sisgd.api.impl.UpLoadDownloadImpl because of underlying class loading error: Type br.gov.caixa.bsb.sisgd.framework.cm.ConectorException from [Module "deployment.garantias-1.8.0.3-b183.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:37:39,718 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 2) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.rest.InformacoesCorporativasPublicasRest because of underlying class loading error: Type com.sun.jersey.api.client.config.ClientConfig from [Module "deployment.garantias-1.8.0.3-b183.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:37:39,763 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 2) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.rest.InformacoesCorporativasPrivadasRest because of underlying class loading error: Type com.sun.jersey.api.client.config.ClientConfig from [Module "deployment.garantias-1.8.0.3-b183.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:37:39,779 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 6) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.rest.CadastroRest because of underlying class loading error: Type com.sun.jersey.api.client.config.ClientConfig from [Module "deployment.garantias-1.8.0.3-b183.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:37:39,794 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 4) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.contrato.sifbn.SifbnEjbServices because of underlying class loading error: Type br.gov.caixa.arqref.business.consultacontratos.services.sifbn.ContratoSifbnServiceIface from [Module "deployment.garantias-1.8.0.3-b183.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:37:39,798 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 3) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.rest.InformacoesCompartilhadasPrivadasRest because of underlying class loading error: Type com.sun.jersey.api.client.config.ClientConfig from [Module "deployment.garantias-1.8.0.3-b183.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:37:39,808 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 5) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.contrato.siban.SibanEjbServices because of underlying class loading error: Type br.gov.caixa.arqref.business.consultacontratos.services.siban.ContratoSibanServiceIface from [Module "deployment.garantias-1.8.0.3-b183.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:37:40,017 WARN  [org.jboss.weld.Validator] (MSC service thread 1-2) WELD-001471: Interceptor method serventias defined on class br.gov.caixa.garantias.negocio.impl.ServentiaService is not defined according to the specification. It should not throw java.io.IOException, which is a checked exception.
        at br.gov.caixa.garantias.negocio.impl.ServentiaService.serventias(ServentiaService.java:0)
16:37:40,136 INFO  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 115) RESTEASY002225: Deploying javax.ws.rs.core.Application: class br.gov.caixa.garantias.rest.JaxRsActivator$Proxy$_$$_WeldClientProxy
16:37:40,180 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 115) WFLYUT0021: Contexto web registrado: '/garantias-web' para servidor 'default-server'
16:37:40,858 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 116) WFLYSRV0010: "SIFEC-GARANTIAS4" foi implantado (runtime-name: "garantias-1.8.0.3-b183.ear")




[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] /server-group=sifec-intranet/deployment=SIFEC-GARANTIAS4:add(enabled=true)
{
    "outcome" => "success",
    "result" => undefined,
    "server-groups" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx473" => {"response" => {
        "outcome" => "success",
        "result" => undefined
    }}}}}}
}

[domain@localhost:9999 /]


