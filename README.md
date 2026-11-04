/deployment=SIEMP:read-children-names(child-type=subdeployment)
/deployment=SIFEC-EMP:read-children-names(child-type=subdeployment)

Abra o log no 473:
bash
   sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -iE --line-buffered "emp-|WFLYSRV0010|WFLYSRV0021|faltam|Registered web context|WELD-|QuerySyntax"
Ative no 471:
   deploy --name=SIFEC-EMP --server-groups=sifec-intranet
   deployment-info --name=SIFEC-EMP

Como ler:

✅ Subiu se aparecer Registered web context: '/emp-web' e WFLYSRV0010: "SIFEC-EMP" foi implantado.
❌ Se aparecer WFLYSRV0021, me cola as linhas e eu classifico como ambiente ou código.

Se a versão de PRD não estiver entre as do domain, peça o link do Nexus e faça o upload pela console, como fizeram com o PJ.




sifec-intranet  not added
sifec-intranet2 not added
sipen           not added

[domain@localhost:9443 /] /deployment=SIEMP:read-children-names(child-type=subdeployment)
{
    "outcome" => "failed",
    "failure-description" => "WFLYCTL0202: No known child type named subdeployment",
    "rolled-back" => true
}

[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /] /deployment=SIFEC-EMP:read-children-names(child-type=subdeployment)
{
    "outcome" => "failed",
    "failure-description" => "WFLYCTL0202: No known child type named subdeployment",
    "rolled-back" => true
}

[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]







[domain@localhost:9443 /]
[domain@localhost:9443 /] deploy --name=SIFEC-EMP --server-groups=sifec-intranet
{"WFLYDC0074: Operation failed or was rolled back on all servers. Server failures:" => {"server-group" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx
473" => {"WFLYCTL0062: A operação de composição falhou e foi revertida. Segue abaixo as etapas que falharam:" => {"Operação step-2" => {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\
"emp-3.95.0.1-b1437.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.WeldException: javax/jms/JMSException
    Caused by: java.lang.NoClassDefFoundError: javax/jms/JMSException
    Caused by: java.lang.ClassNotFoundException: javax.jms.JMSException from [Module \"deployment.emp-3.95.0.1-b1437.ear\" from Service Module Loader]"}}}}}}}}}}

[domain@localhost:9443 /] deployment-info --name=SIFEC-EMP
NAME      RUNTIME-NAME
SIFEC-EMP emp-3.95.0.1-b1437.ear

SERVER-GROUP    STATE
siemp           not added
sifec-intranet  not added
sifec-intranet2 not added
sipen           not added

[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]


[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$ sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -iE --line-buffered "ERROR|Exception|Caused by"

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for p585600:
14:25:29,076 SEVERE [SifbnRestServices] (default task-27) erro: java.lang.NullPointerException
        at io.undertow.servlet.handlers.SendErrorPageHandler.handleRequest(SendErrorPageHandler.java:52) [undertow-servlet-2.2.37.SP2-redhat-00001.jar:2.2.37.SP2-redhat-00001]
15:26:00,988 WARN  [org.jboss.as.connector.deployers.jdbc] (MSC service thread 1-4) WFLYJCA0003: Não foi possível instanciar a classe do driver "org.olap4j.driver.xmla.XmlaOlap4jDriver": java.lang.NoSuchMethodException: org.olap4j.driver.xmla.XmlaOlap4jDriver.<init>()
15:26:05,704 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 167) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SICCR-PJ")]) - falha na descrição: {
15:26:05,707 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 167) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SICCR-PJ")]) - falha na descrição: {
15:26:05,707 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 167) WFLYSRV0021: O procedimento da implantação "sifec-ccr-pj-8.38.0.1-b5720.ear" foi revertido com mensagem de falha:
15:27:05,915 WARN  [org.jboss.as.connector.deployers.jdbc] (MSC service thread 1-8) WFLYJCA0003: Não foi possível instanciar a classe do driver "org.olap4j.driver.xmla.XmlaOlap4jDriver": java.lang.NoSuchMethodException: org.olap4j.driver.xmla.XmlaOlap4jDriver.<init>()
15:27:07,592 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 167) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SICCR-PJ")]) - falha na descrição: {
15:27:07,592 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 167) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SICCR-PJ")]) - falha na descrição: {
15:27:07,592 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 167) WFLYSRV0021: O procedimento da implantação "sifec-ccr-pj-8.38.0.1-b5720.ear" foi revertido com mensagem de falha:
15:31:37,196 ERROR [org.jboss.msc.service.fail] (MSC service thread 1-8) MSC000001: Failed to start service jboss.deployment.unit.SICCR-PJ.STRUCTURE: org.jboss.msc.service.StartException in service jboss.deployment.unit.SICCR-PJ.STRUCTURE: WFLYSRV0153: Falha ao processar a fase STRUCTURE de deployment "SICCR-PJ"
Caused by: org.jboss.as.server.deployment.DeploymentUnitProcessingException: WFLYSRV0160: Falha ao montar o conteúdo de implantação
Caused by: java.io.FileNotFoundException: /opt/jboss/jboss-eap/ear (No such file or directory)
15:31:37,202 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 167) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SICCR-PJ")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.SICCR-PJ.STRUCTURE" => "WFLYSRV0153: Falha ao processar a fase STRUCTURE de deployment \"SICCR-PJ\"
    Caused by: org.jboss.as.server.deployment.DeploymentUnitProcessingException: WFLYSRV0160: Falha ao montar o conteúdo de implantação
    Caused by: java.io.FileNotFoundException: /opt/jboss/jboss-eap/ear (No such file or directory)"}}
15:31:37,202 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 167) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SICCR-PJ")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.SICCR-PJ.STRUCTURE" => "WFLYSRV0153: Falha ao processar a fase STRUCTURE de deployment \"SICCR-PJ\"
    Caused by: org.jboss.as.server.deployment.DeploymentUnitProcessingException: WFLYSRV0160: Falha ao montar o conteúdo de implantação
    Caused by: java.io.FileNotFoundException: /opt/jboss/jboss-eap/ear (No such file or directory)"}}
15:31:37,202 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 167) WFLYSRV0021: O procedimento da implantação "SICCR-PJ" foi revertido com mensagem de falha:
    Caused by: org.jboss.as.server.deployment.DeploymentUnitProcessingException: WFLYSRV0160: Falha ao montar o conteúdo de implantação
    Caused by: java.io.FileNotFoundException: /opt/jboss/jboss-eap/ear (No such file or directory)"}}
15:34:11,426 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 3) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.negocio.mq.ConexaoSIRICMQ because of underlying class loading error: Type javax.jms.JMSException from [Module "deployment.sifec-bdcaixa-2.0.1-b39.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:34:11,433 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 6) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.negocio.mq.ConexaoSIEMPMQ because of underlying class loading error: Type javax.jms.JMSException from [Module "deployment.sifec-bdcaixa-2.0.1-b39.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:34:11,440 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 3) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.negocio.mq.ConexaoSIFECMQ because of underlying class loading error: Type javax.jms.JMSException from [Module "deployment.sifec-bdcaixa-2.0.1-b39.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:34:11,448 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 5) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.dao.barramento.ConexaoSIRICMQ because of underlying class loading error: Type javax.jms.JMSException from [Module "deployment.sifec-bdcaixa-2.0.1-b39.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:34:11,458 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 1) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.negocio.mq.ConexaoSICLIMQ because of underlying class loading error: Type javax.jms.JMSException from [Module "deployment.sifec-bdcaixa-2.0.1-b39.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:34:11,459 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 1) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.dao.barramento.SiempDaoBarramento because of underlying class loading error: Type javax.jms.JMSException from [Module "deployment.sifec-bdcaixa-2.0.1-b39.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:34:11,622 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 6) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.excecao.mensagem.mensagemadaptador.JMSExceptionAdapter because of underlying class loading error: Type javax.jms.JMSException from [Module "deployment.sifec-bdcaixa-2.0.1-b39.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:34:11,625 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 6) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.jms.JMSServiceImpl because of underlying class loading error: Type javax.jms.Destination from [Module "deployment.sifec-bdcaixa-2.0.1-b39.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:34:11,631 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 4) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.jms.JMSServiceImplEx because of underlying class loading error: Type javax.jms.Destination from [Module "deployment.sifec-bdcaixa-2.0.1-b39.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:34:13,906 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 6) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.siemp.sisgd.api.impl.UpLoadDownloadImpl because of underlying class loading error: Type br.gov.caixa.bsb.sisgd.framework.cm.ConectorException from [Module "deployment.sifec-2.160.3.0.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:34:14,475 WARN  [io.undertow.servlet] (ServerService Thread Pool -- 76) UT015020: Path /error/* is secured for some HTTP methods, however it is not secured for [TRACE, HEAD, DELETE, CONNECT, OPTIONS, PUT]
15:34:14,498 WARN  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 83) RESTEASY002155: Provider class br.gov.caixa.emprestimo.rest.excecao.BusinessExceptionMapper is already registered.  2nd registration is being ignored.
15:34:14,536 INFO  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 76) RESTEASY002210: Adding provider singleton br.gov.caixa.api.comum.SystemExceptionMapper from Application class br.gov.caixa.api.JaxRsActivator$Proxy$_$$_WeldClientProxy
15:34:14,536 INFO  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 76) RESTEASY002210: Adding provider singleton br.gov.caixa.api.comum.BarramentoExceptionMapper from Application class br.gov.caixa.api.JaxRsActivator$Proxy$_$$_WeldClientProxy
15:34:14,536 INFO  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 76) RESTEASY002210: Adding provider singleton br.gov.caixa.api.comum.SegurancaExceptionMapper from Application class br.gov.caixa.api.JaxRsActivator$Proxy$_$$_WeldClientProxy
15:34:16,400 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 6) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.contrato.siban.SibanEjbServices because of underlying class loading error: Type br.gov.caixa.arqref.business.consultacontratos.services.siban.PlanilhaServiceIface from [Module "deployment.SIFEC-CCR-6.3.0-b4587.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:34:16,991 WARN  [io.undertow.servlet] (ServerService Thread Pool -- 77) UT015020: Path /errorExpirado.html is secured for some HTTP methods, however it is not secured for [TRACE, HEAD, DELETE, CONNECT, OPTIONS, PUT]
15:34:17,037 WARN  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 77) RESTEASY002155: Provider class br.gov.caixa.arqrefcore.excecao.rs.DefaultExceptionMapper is already registered.  2nd registration is being ignored.
15:34:18,292 INFO  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 75) RESTEASY002215: Adding singleton provider br.gov.caixa.api.ccr.util.SegurancaExceptionMapper from Application class br.gov.caixa.api.JaxRsActivator$Proxy$_$$_WeldClientProxy
15:34:18,292 WARN  [org.jboss.resteasy.resteasy_jaxrs.i18n] (ServerService Thread Pool -- 75) RESTEASY002160: Provider instance br.gov.caixa.api.ccr.util.SegurancaExceptionMapper is already registered.  2nd registration is being ignored.
15:42:21,833 WARN  [org.jboss.as.connector.deployers.jdbc] (MSC service thread 1-3) WFLYJCA0003: Não foi possível instanciar a classe do driver "org.olap4j.driver.xmla.XmlaOlap4jDriver": java.lang.NoSuchMethodException: org.olap4j.driver.xmla.XmlaOlap4jDriver.<init>()
15:42:23,144 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 32) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SICCR-PJ")]) - falha na descrição: {
15:42:23,145 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 32) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SICCR-PJ")]) - falha na descrição: {
15:42:23,147 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 32) WFLYSRV0021: O procedimento da implantação "sifec-ccr-pj.ear" foi revertido com mensagem de falha:
15:51:09,104 WARN  [org.jboss.as.connector.deployers.jdbc] (MSC service thread 1-5) WFLYJCA0003: Não foi possível instanciar a classe do driver "org.olap4j.driver.xmla.XmlaOlap4jDriver": java.lang.NoSuchMethodException: org.olap4j.driver.xmla.XmlaOlap4jDriver.<init>()
15:51:10,689 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 7) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.contrato.sifbn.SifbnEjbServices because of underlying class loading error: Type br.gov.caixa.arqref.business.consultacontratos.services.sifbn.ContratoSifbnServiceIface from [Module "deployment.sifec-ccr-pj.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:51:10,705 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 3) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.contrato.siban.SibanEjbServices because of underlying class loading error: Type br.gov.caixa.arqref.business.consultacontratos.services.siban.ContratoSibanServiceIface from [Module "deployment.sifec-ccr-pj.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:51:11,008 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 5) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.util.ArquillianHelper because of underlying class loading error: Type org.jboss.shrinkwrap.api.asset.Asset from [Module "deployment.sifec-ccr-pj.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:51:11,012 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 1) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.email.api.operacao.SendMail because of underlying class loading error: Type freemarker.template.TemplateException from [Module "deployment.sifec-ccr-pj.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:51:11,881 ERROR [org.jboss.msc.service.fail] (MSC service thread 1-6) MSC000001: Failed to start service jboss.deployment.unit."sifec-ccr-pj.ear".WeldStartService: org.jboss.msc.service.StartException in service jboss.deployment.unit."sifec-ccr-pj.ear".WeldStartService: Failed to start service
Caused by: org.jboss.weld.exceptions.DeploymentException: Exception List with 19 exceptions:
Exception 0 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 1 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 2 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 3 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 4 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 5 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 6 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 7 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 8 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 9 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 10 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 11 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 12 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 13 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 14 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 15 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 16 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 17 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 18 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
15:51:11,896 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 32) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SICCR-PJ")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"sifec-ccr-pj.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: Exception List with 19 exceptions:
Exception 0 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 1 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 2 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 3 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 4 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 5 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 6 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 7 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 8 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 9 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 10 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 11 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 12 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 13 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 14 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 15 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 16 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 17 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 18 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
15:51:11,897 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 32) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SICCR-PJ")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"sifec-ccr-pj.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: Exception List with 19 exceptions:
Exception 0 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 1 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 2 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 3 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 4 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 5 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 6 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 7 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 8 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 9 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 10 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 11 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 12 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 13 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 14 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 15 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 16 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 17 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 18 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
15:51:11,899 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 32) WFLYSRV0021: O procedimento da implantação "sifec-ccr-pj.ear" foi revertido com mensagem de falha:
    Caused by: org.jboss.weld.exceptions.DeploymentException: Exception List with 19 exceptions:
Exception 0 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 1 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 2 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 3 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 4 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 5 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 6 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 7 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 8 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 9 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 10 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 11 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 12 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 13 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 14 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 15 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 16 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 17 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 18 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
15:53:07,655 WARN  [org.jboss.as.connector.deployers.jdbc] (MSC service thread 1-2) WFLYJCA0003: Não foi possível instanciar a classe do driver "org.olap4j.driver.xmla.XmlaOlap4jDriver": java.lang.NoSuchMethodException: org.olap4j.driver.xmla.XmlaOlap4jDriver.<init>()
15:53:09,274 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 2) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.util.ArquillianHelper because of underlying class loading error: Type org.jboss.shrinkwrap.api.asset.Asset from [Module "deployment.sifec-ccr-pj.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:53:09,280 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 5) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.email.api.operacao.SendMail because of underlying class loading error: Type freemarker.template.TemplateException from [Module "deployment.sifec-ccr-pj.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:53:09,474 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 4) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.contrato.sifbn.SifbnEjbServices because of underlying class loading error: Type br.gov.caixa.arqref.business.consultacontratos.services.sifbn.ContratoSifbnServiceIface from [Module "deployment.sifec-ccr-pj.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:53:09,482 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 5) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.contrato.siban.SibanEjbServices because of underlying class loading error: Type br.gov.caixa.arqref.business.consultacontratos.services.siban.ContratoSibanServiceIface from [Module "deployment.sifec-ccr-pj.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:53:10,448 ERROR [org.jboss.msc.service.fail] (MSC service thread 1-8) MSC000001: Failed to start service jboss.deployment.unit."sifec-ccr-pj.ear".WeldStartService: org.jboss.msc.service.StartException in service jboss.deployment.unit."sifec-ccr-pj.ear".WeldStartService: Failed to start service
Caused by: org.jboss.weld.exceptions.DeploymentException: Exception List with 2 exceptions:
Exception 0 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 1 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
15:53:10,455 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 32) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SICCR-PJ")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"sifec-ccr-pj.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: Exception List with 2 exceptions:
Exception 0 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 1 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
15:53:10,455 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 32) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SICCR-PJ")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"sifec-ccr-pj.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: Exception List with 2 exceptions:
Exception 0 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 1 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
15:53:10,455 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 32) WFLYSRV0021: O procedimento da implantação "sifec-ccr-pj.ear" foi revertido com mensagem de falha:
    Caused by: org.jboss.weld.exceptions.DeploymentException: Exception List with 2 exceptions:
Exception 0 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 1 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
16:07:09,626 WARN  [org.jboss.as.connector.deployers.jdbc] (MSC service thread 1-8) WFLYJCA0003: Não foi possível instanciar a classe do driver "org.olap4j.driver.xmla.XmlaOlap4jDriver": java.lang.NoSuchMethodException: org.olap4j.driver.xmla.XmlaOlap4jDriver.<init>()
16:07:15,780 WARN  [org.jboss.jca.core.connectionmanager.listener.TxConnectionListener] (ServerService Thread Pool -- 107) IJ000305: Connection error occured: org.jboss.jca.core.connectionmanager.listener.TxConnectionListener@a7aa35b[state=NORMAL managed connection=org.jboss.jca.adapters.jdbc.local.LocalManagedConnection@2f57588a connection handles=1 lastReturned=1793819230131 lastValidated=1793817251244 lastCheckedOut=1793819230773 trackByTx=false pool=org.jboss.jca.core.connectionmanager.pool.strategy.OnePool@1435abfb mcp=SemaphoreConcurrentLinkedDequeManagedConnectionPool@4fb4b9b9[pool=jdbc/OracleSiccrDS] xaResource=LocalXAResourceImpl@78107e4c[connectionListener=a7aa35b connectionManager=6c3f38e1 warned=false currentXid=null productName=Oracle productVersion=Oracle Database 19c Enterprise Edition Release 19.0.0.0.0 - Production
Version 19.29.0.0.0 jndiName=java:/jdbc/OracleSiccrDS] txSync=null]: java.sql.SQLRecoverableException: Erro de ES: Socket read timed out
Caused by: oracle.net.nt.TimeoutInterruptHandler$IOReadTimeoutException: Socket read timed out
16:07:15,786 ERROR [org.hibernate.hql.spi.id.IdTableHelper] (ServerService Thread Pool -- 107) Unable to use JDBC Connection to create Statement: java.sql.SQLRecoverableException: Conexão Fechada
16:07:16,438 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 4) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.contrato.sifbn.SifbnEjbServices because of underlying class loading error: Type br.gov.caixa.arqref.business.consultacontratos.services.sifbn.ContratoSifbnServiceIface from [Module "deployment.workflow-credito-pj-ear-8.40.1-20261104.180249-4.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:07:16,445 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 2) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.contrato.siban.SibanEjbServices because of underlying class loading error: Type br.gov.caixa.arqref.business.consultacontratos.services.siban.ContratoSibanServiceIface from [Module "deployment.workflow-credito-pj-ear-8.40.1-20261104.180249-4.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:07:16,519 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 1) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.util.ArquillianHelper because of underlying class loading error: Type org.jboss.shrinkwrap.api.asset.Asset from [Module "deployment.workflow-credito-pj-ear-8.40.1-20261104.180249-4.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:07:16,525 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 2) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefcore.email.api.operacao.SendMail because of underlying class loading error: Type freemarker.template.TemplateException from [Module "deployment.workflow-credito-pj-ear-8.40.1-20261104.180249-4.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:07:17,331 ERROR [org.jboss.msc.service.fail] (MSC service thread 1-6) MSC000001: Failed to start service jboss.deployment.unit."workflow-credito-pj-ear-8.40.1-20261104.180249-4.ear".WeldStartService: org.jboss.msc.service.StartException in service jboss.deployment.unit."workflow-credito-pj-ear-8.40.1-20261104.180249-4.ear".WeldStartService: Failed to start service
Caused by: org.jboss.weld.exceptions.DeploymentException: Exception List with 170 exceptions:
Exception 0 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 1 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 2 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 3 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 4 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 5 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 6 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 7 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 8 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 9 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 10 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 11 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 12 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 13 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 14 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 15 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 16 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 17 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 18 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 19 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 20 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 21 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 22 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 23 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 24 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 25 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 26 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 27 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 28 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 29 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 30 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 31 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 32 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 33 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 34 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 35 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 36 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 37 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 38 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 39 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 40 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 41 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 42 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 43 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 44 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 45 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 46 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 47 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 48 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 49 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 50 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 51 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 52 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 53 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 54 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 55 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 56 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 57 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 58 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 59 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 60 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 61 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 62 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 63 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 64 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 65 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 66 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 67 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 68 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 69 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 70 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 71 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 72 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 73 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 74 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 75 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 76 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 77 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 78 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 79 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 80 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 81 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 82 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 83 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 84 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 85 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 86 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 87 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 88 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 89 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 90 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 91 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 92 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 93 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 94 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 95 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 96 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 97 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 98 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 99 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 100 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 101 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 102 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 103 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 104 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 105 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 106 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 107 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 108 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 109 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 110 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 111 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 112 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 113 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 114 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 115 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 116 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 117 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 118 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 119 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 120 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 121 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 122 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 123 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 124 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 125 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 126 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 127 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 128 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 129 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 130 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 131 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 132 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 133 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 134 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 135 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 136 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 137 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 138 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 139 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 140 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 141 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 142 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 143 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 144 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 145 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 146 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 147 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 148 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 149 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 150 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 151 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 152 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 153 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 154 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 155 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 156 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 157 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 158 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 159 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 160 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 161 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 162 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 163 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 164 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 165 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 166 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 167 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 168 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 169 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
        Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
16:07:17,375 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 103) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SICCR-PJ")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"workflow-credito-pj-ear-8.40.1-20261104.180249-4.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: Exception List with 170 exceptions:
Exception 0 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 1 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 2 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 3 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 4 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 5 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 6 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 7 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 8 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 9 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 10 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 11 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 12 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 13 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 14 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 15 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 16 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 17 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 18 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 19 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 20 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 21 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 22 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 23 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 24 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 25 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 26 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 27 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 28 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 29 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 30 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 31 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 32 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 33 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 34 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 35 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 36 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 37 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 38 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 39 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 40 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 41 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 42 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 43 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 44 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 45 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 46 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 47 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 48 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 49 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 50 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 51 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 52 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 53 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 54 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 55 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 56 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 57 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 58 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 59 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 60 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 61 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 62 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 63 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 64 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 65 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 66 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 67 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 68 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 69 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 70 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 71 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 72 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 73 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 74 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 75 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 76 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 77 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 78 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 79 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 80 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 81 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 82 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 83 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 84 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 85 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 86 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 87 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 88 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 89 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 90 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 91 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 92 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 93 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 94 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 95 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 96 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 97 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 98 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 99 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 100 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 101 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 102 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 103 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 104 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 105 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 106 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 107 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 108 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 109 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 110 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 111 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 112 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 113 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 114 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 115 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 116 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 117 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 118 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 119 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 120 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 121 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 122 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 123 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 124 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 125 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 126 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 127 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 128 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 129 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 130 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 131 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 132 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 133 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 134 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 135 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 136 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 137 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 138 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 139 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 140 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 141 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 142 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 143 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 144 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 145 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 146 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 147 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 148 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 149 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 150 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 151 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 152 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 153 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 154 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 155 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 156 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 157 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 158 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 159 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 160 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 161 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 162 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 163 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 164 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 165 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 166 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 167 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 168 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 169 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
16:07:17,388 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 103) WFLYCTL0013: Falha na operação ("add") - endereço ([("deployment" => "SICCR-PJ")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"workflow-credito-pj-ear-8.40.1-20261104.180249-4.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: Exception List with 170 exceptions:
Exception 0 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 1 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 2 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 3 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 4 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 5 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 6 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 7 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 8 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 9 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 10 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 11 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 12 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 13 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 14 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 15 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 16 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 17 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 18 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 19 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 20 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 21 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 22 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 23 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 24 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 25 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 26 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 27 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 28 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 29 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 30 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 31 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 32 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 33 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 34 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 35 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 36 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 37 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 38 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 39 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 40 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 41 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 42 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 43 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 44 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 45 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 46 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 47 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 48 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 49 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 50 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 51 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 52 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 53 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 54 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 55 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 56 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 57 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 58 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 59 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 60 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 61 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 62 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 63 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 64 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 65 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 66 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 67 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 68 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 69 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 70 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 71 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 72 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 73 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 74 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 75 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 76 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 77 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 78 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 79 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 80 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 81 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 82 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 83 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 84 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 85 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 86 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 87 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 88 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 89 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 90 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 91 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 92 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 93 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 94 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 95 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 96 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 97 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 98 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 99 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 100 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 101 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 102 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 103 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 104 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 105 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 106 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 107 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 108 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 109 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 110 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 111 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 112 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 113 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 114 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 115 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 116 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 117 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 118 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 119 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 120 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 121 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 122 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 123 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 124 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 125 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 126 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 127 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 128 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 129 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 130 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 131 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 132 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 133 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 134 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 135 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 136 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 137 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 138 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 139 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 140 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 141 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 142 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 143 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 144 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 145 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 146 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 147 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 148 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 149 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 150 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 151 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 152 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 153 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 154 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 155 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 156 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 157 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 158 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 159 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 160 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 161 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 162 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 163 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 164 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 165 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 166 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 167 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 168 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 169 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
16:07:17,409 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 103) WFLYSRV0021: O procedimento da implantação "workflow-credito-pj-ear-8.40.1-20261104.180249-4.ear" foi revertido com mensagem de falha:
    Caused by: org.jboss.weld.exceptions.DeploymentException: Exception List with 170 exceptions:
Exception 0 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 1 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 2 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 3 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 4 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 5 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 6 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 7 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 8 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 9 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 10 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 11 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 12 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 13 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 14 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 15 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 16 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 17 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 18 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 19 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 20 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 21 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 22 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 23 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 24 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 25 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 26 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 27 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 28 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 29 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 30 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 31 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 32 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 33 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 34 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 35 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 36 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 37 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 38 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 39 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 40 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 41 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 42 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 43 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 44 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 45 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 46 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 47 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 48 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 49 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 50 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 51 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 52 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 53 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 54 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 55 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 56 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 57 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 58 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 59 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 60 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 61 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 62 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 63 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 64 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 65 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 66 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 67 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 68 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 69 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 70 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 71 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 72 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 73 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 74 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 75 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 76 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 77 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 78 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 79 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 80 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 81 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 82 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 83 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 84 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 85 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 86 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 87 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 88 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 89 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 90 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 91 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 92 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 93 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 94 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 95 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 96 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 97 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 98 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 99 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 100 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 101 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 102 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 103 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 104 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 105 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 106 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 107 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 108 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 109 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 110 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 111 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 112 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 113 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 114 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 115 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 116 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 117 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 118 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 119 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 120 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 121 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 122 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 123 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 124 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 125 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 126 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 127 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 128 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 129 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 130 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 131 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 132 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 133 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 134 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 135 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 136 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 137 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 138 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 139 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 140 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 141 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 142 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 143 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 144 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 145 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 146 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 147 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 148 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 149 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 150 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 151 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 152 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 153 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 154 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 155 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 156 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 157 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 158 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 159 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 160 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 161 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 162 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 163 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 164 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 165 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 166 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 167 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 168 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
Exception 169 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
16:07:29,409 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 2) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.negocio.mq.ConexaoSIFECContratoMQ because of underlying class loading error: Type javax.jms.JMSException from [Module "deployment.emp-3.95.0.1-b1437.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:07:29,416 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 4) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.negocio.mq.ConexaoSIRICMQ because of underlying class loading error: Type javax.jms.JMSException from [Module "deployment.emp-3.95.0.1-b1437.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:07:29,429 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 1) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.negocio.mq.ConexaoSIEMPMQ because of underlying class loading error: Type javax.jms.JMSException from [Module "deployment.emp-3.95.0.1-b1437.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:07:29,436 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 4) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.negocio.mq.ConexaoSIFECMQ because of underlying class loading error: Type javax.jms.JMSException from [Module "deployment.emp-3.95.0.1-b1437.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:07:29,450 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 6) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.dao.barramento.ConexaoSIRICMQ because of underlying class loading error: Type javax.jms.JMSException from [Module "deployment.emp-3.95.0.1-b1437.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:07:29,458 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 4) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.negocio.mq.ConexaoSICLIMQ because of underlying class loading error: Type javax.jms.JMSException from [Module "deployment.emp-3.95.0.1-b1437.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:07:29,459 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 7) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.dao.barramento.SiempDaoBarramento because of underlying class loading error: Type javax.jms.JMSException from [Module "deployment.emp-3.95.0.1-b1437.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:07:29,493 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 1) WELD-000119: Not generating any bean definitions from br.gov.caixa.sifec.componentes.integracoes.fgi.bndes.rest.client.envioanexo.EnviarAnexoV1Service because of underlying class loading error: Type com.sun.jersey.multipart.BodyPart from [Module "deployment.emp-3.95.0.1-b1437.ear.emp-web.war" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:07:29,497 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 4) WELD-000119: Not generating any bean definitions from br.gov.caixa.sifec.componentes.integracoes.fgi.bndes.rest.catalogo.invoker.ApiClient because of underlying class loading error: Type com.sun.jersey.multipart.BodyPart from [Module "deployment.emp-3.95.0.1-b1437.ear.emp-web.war" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:07:29,504 WARN  [org.jboss.modules.define] (Weld Thread Pool -- 7) Failed to define class br.gov.caixa.sifec.componentes.integracoes.fgi.bndes.rest.client.envioanexo.CustomMultiPartWriter in Module "deployment.emp-3.95.0.1-b1437.ear.emp-web.war" from Service Module Loader: java.lang.NoClassDefFoundError: Failed to link br/gov/caixa/sifec/componentes/integracoes/fgi/bndes/rest/client/envioanexo/CustomMultiPartWriter (Module "deployment.emp-3.95.0.1-b1437.ear.emp-web.war" from Service Module Loader): com/sun/jersey/multipart/impl/MultiPartWriter
Caused by: java.lang.ClassNotFoundException: com.sun.jersey.multipart.impl.MultiPartWriter from [Module "deployment.emp-3.95.0.1-b1437.ear.emp-web.war" from Service Module Loader]
16:07:29,507 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 7) WELD-000119: Not generating any bean definitions from br.gov.caixa.sifec.componentes.integracoes.fgi.bndes.rest.client.envioanexo.CustomMultiPartWriter because of underlying class loading error: Type com.sun.jersey.multipart.impl.MultiPartWriter from [Module "deployment.emp-3.95.0.1-b1437.ear.emp-web.war" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
16:07:40,126 ERROR [org.jboss.msc.service.fail] (MSC service thread 1-4) MSC000001: Failed to start service jboss.deployment.unit."emp-3.95.0.1-b1437.ear".WeldStartService: org.jboss.msc.service.StartException in service jboss.deployment.unit."emp-3.95.0.1-b1437.ear".WeldStartService: Failed to start service
Caused by: org.jboss.weld.exceptions.WeldException: javax/jms/JMSException
        at org.jboss.weld.executor.AbstractExecutorServices.checkForExceptions(AbstractExecutorServices.java:82) [weld-core-impl-3.1.11.Final-redhat-00001.jar:3.1.11.Final-redhat-00001]
        at org.jboss.weld.executor.AbstractExecutorServices.invokeAllAndCheckForExceptions(AbstractExecutorServices.java:59) [weld-core-impl-3.1.11.Final-redhat-00001.jar:3.1.11.Final-redhat-00001]
        at org.jboss.weld.executor.AbstractExecutorServices.invokeAllAndCheckForExceptions(AbstractExecutorServices.java:67) [weld-core-impl-3.1.11.Final-redhat-00001.jar:3.1.11.Final-redhat-00001]
Caused by: java.lang.NoClassDefFoundError: javax/jms/JMSException
Caused by: java.lang.ClassNotFoundException: javax.jms.JMSException from [Module "deployment.emp-3.95.0.1-b1437.ear" from Service Module Loader]
16:07:40,131 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 103) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SIFEC-EMP")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"emp-3.95.0.1-b1437.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.WeldException: javax/jms/JMSException
    Caused by: java.lang.NoClassDefFoundError: javax/jms/JMSException
    Caused by: java.lang.ClassNotFoundException: javax.jms.JMSException from [Module \"deployment.emp-3.95.0.1-b1437.ear\" from Service Module Loader]"}}
16:07:40,131 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 103) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SIFEC-EMP")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"emp-3.95.0.1-b1437.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.WeldException: javax/jms/JMSException
    Caused by: java.lang.NoClassDefFoundError: javax/jms/JMSException
    Caused by: java.lang.ClassNotFoundException: javax.jms.JMSException from [Module \"deployment.emp-3.95.0.1-b1437.ear\" from Service Module Loader]"}}
16:07:40,131 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 103) WFLYSRV0021: O procedimento da implantação "emp-3.95.0.1-b1437.ear" foi revertido com mensagem de falha:
    Caused by: org.jboss.weld.exceptions.WeldException: javax/jms/JMSException
    Caused by: java.lang.NoClassDefFoundError: javax/jms/JMSException
    Caused by: java.lang.ClassNotFoundException: javax.jms.JMSException from [Module \"deployment.emp-3.95.0.1-b1437.ear\" from Service Module Loader]"}}


