1. Deixe o log aberto no 473 (10.116.97.79):

bash
sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -iE --line-buffered "empresas|rural|WFLYSRV0010|WFLYSRV0021|faltam|WELD-001408|ClassNotFound|Registered web context"

2. SIEMP-EMPRESAS (no jboss-cli do 471, 10.116.97.59):

deploy --name=SIEMP-EMPRESAS --server-groups=sifec-intranet
deployment-info --name=SIEMP-EMPRESAS

3. Depois, o RURAL, assim que confirmarem a versão (a candidata é a SIFEC-RURAL4, 2.115.1.1):

deploy --name=SIFEC-RURAL4 --server-groups=sifec-intranet
deployment-info --name=SIFEC-RURAL4

Em cada um, o esperado é WFLYSRV0010 ... foi implantado e o Registered web context. Se aparecer WFLYSRV0021, o JBoss reverte sozinho. Me cola as linhas que eu classifico como ambiente ou código.

Quando terminar os dois, eu monto o resumo do dia para você mandar ao Paulo e atualizo a planilha.





[domain@localhost:9443 /] deploy --name=SIEMP-EMPRESAS --server-groups=sifec-intranet
{"WFLYDC0074: Operation failed or was rolled back on all servers. Server failures:" => {"server-group" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx
473" => {"WFLYCTL0062: A operação de composição falhou e foi revertida. Segue abaixo as etapas que falharam:" => {"Operação step-2" => {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\
"empresas-1.2.3-b15.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type ParametrizacaoService with qualifiers @Default
  at injection point [BackedAnnotatedField] @Inject private br.gov.caixa.empresa.rest.ParametrizacaoRest.parametrizacaoService
  at br.gov.caixa.empresa.rest.ParametrizacaoRest.parametrizacaoService(ParametrizacaoRest.java:0)
"}}}}}}}}}}

[domain@localhost:9443 /]




[domain@localhost:9443 /]
[domain@localhost:9443 /] deploy --name=SIFEC-RURAL4 --server-groups=sifec-intranet
{"WFLYDC0074: Operation failed or was rolled back on all servers. Server failures:" => {"server-group" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx
473" => {"WFLYCTL0062: A operação de composição falhou e foi revertida. Segue abaixo as etapas que falharam:" => {"Operação step-2" => {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.subuni
t.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".INSTALL" => "WFLYSRV0153: Falha ao processar a fase INSTALL de subdeployment \"rural-ejb.jar\" of deployment \"rural-2.115.1.1-b2421.ear\"
    Caused by: org.jboss.as.server.deployment.DeploymentUnitProcessingException: WFLYEE0024: Não foi possível configurar o componente SirurRestServiceImpl
    Caused by: java.lang.ExceptionInInitializerError
    Caused by: java.lang.IllegalStateException: Erro ao construir SSLContext: Erro ao carregar Trust Store [C:/Desenvolvimento/JDK/jdk1.8.0_231/jre/lib/security/cacerts]: C:/Desenvolvimento/JDK/jdk
1.8.0_231/jre/lib/security/cacerts (No such file or directory)
    Caused by: java.lang.IllegalStateException: Erro ao carregar Trust Store [C:/Desenvolvimento/JDK/jdk1.8.0_231/jre/lib/security/cacerts]: C:/Desenvolvimento/JDK/jdk1.8.0_231/jre/lib/security/cac
erts (No such file or directory)
    Caused by: java.io.FileNotFoundException: C:/Desenvolvimento/JDK/jdk1.8.0_231/jre/lib/security/cacerts (No such file or directory)"},"WFLYCTL0412: Serviços necessários que não estão instalados:
" => ["jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl","jboss.deployment.sub
unit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".jndiDependencyService","jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".beanmanager","jboss.naming.context.java.comp.\"
rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean","jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar
\".deploymentCompleteService","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.Avaliacao
DeRiscoDAO","jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\"","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean"],"WFLYCTL0180:
Os serviços com falta/indisponibilidade de dependências " => ["jboss.deployment.unit.\"rural-2.115.1.1-b2421.ear\".WeldStartService faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-e
jb.jar#Siemp2EjbSybase\", jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".jndiDependencyService, jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2
\"]","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.Avaliaca
oDeRiscoDAO]","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ej
b.SirurRestServiceImpl]","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".ru
ral-ejb.AvaliacaoDeRiscoDAO]","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-e
jb.EmailBean]","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog]",
"jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]",
"jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"br.gov.caixa.arqrefweb.controle.AppServlet\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/ru
ral-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFacto
ry.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServic
eImpl.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl]","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoR
uralBean.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean]","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean.Val
idator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean]","jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"br.gov.caixa.empr
estimo.rest.filtro.FiltroRuralLog\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#
SiempEjbDB2\"]","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.Cred
itoRuralBean]","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLo
g]","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean]","jbo
ss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog]","jboss.deployment.subu
nit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".weld.weldClassIntrospector faltam [jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".beanmanager]","jboss.naming.context.j
ava.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog]","jboss.deployment.subunit.\"ru
ral-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".batch.artifact.factory faltam [jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".beanmanager]","jboss.naming.context.java.comp.\"r
ural-2.115.1.1-b2421\".rural-ejb.EmailBean.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean]","jboss.naming.context.java.comp.\"rural-2.115.
1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO]","jboss.deployment.subunit.\"rural-2.115.1.1-b242
1.ear\".\"rural-web.war\".component.\"javax.servlet.jsp.jstl.tlv.ScriptFreeTLV\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceun
it.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]","jboss.deployment.unit.\"rural-2.115.1.1-b2421.ear\".deploymentCompleteService faltam [jboss.deployment.subunit.\"rural-2.115.1.1-b2421.
ear\".\"rural-ejb.jar\".deploymentCompleteService]","jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"javax.faces.webapp.FacetTag\".START faltam [jboss.persisten
ceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]","jboss.naming.context.java.comp.\"rural-2.115.1.1
-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO]","jboss.deployment.subunit.\"rural-2.115.1.1-b242
1.ear\".\"rural-web.war\".component.\"com.sun.faces.config.ConfigureListener\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit
.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory.ValidatorFactory faltam [jboss.naming.context.jav
a.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl.Validator faltam [jboss.naming.context.jav
a.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl]","jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean.InAppClientContainer faltam [jboss.naming.cont
ext.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean]","jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"javax.servlet.jsp.jstl.tlv.PermittedTaglib
sTLV\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]","jboss.naming
.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl]","jboss.nam
ing.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean]","jboss.naming.context.java.co
mp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]"]}}}}}}}}}

[domain@localhost:9443 /]


[p585600@cbrdeapllx473 ~]$ sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -iE --line-buffered "empresas|rural|WFLYSRV0010|WFLYSRV0021|faltam|WELD-001408|ClassNotFound|Registered web context"

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for p585600:
,16:45:11,889 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 124) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'rural-2.115.0.1-b2446.ear/rural-ejb.jar#Siemp2EjbSybase'
16:45:11,889 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 123) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'rural-2.115.0.1-b2446.ear#fecDS'
16:45:11,894 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 123) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'rural-2.115.0.1-b2446.ear#fecDS'
16:45:11,896 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 124) WFLYCLINF0003: Cache rural-2.115.0.1-b2446.ear.rural-web.war encerrado a partir do recipiente web
16:45:11,902 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-2) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: rural-ejb.jar) em 13ms
16:45:11,931 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-5) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: rural-web.war) em 42ms
16:45:11,935 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-5) WFLYSRV0028: Implantação interrompida SIFEC-RURAL (runtime-name: rural-2.115.0.1-b2446.ear) em 46ms
16:48:22,700 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-6) WFLYSRV0027: Iniciando a implantação do "SIEMP-EMPRESAS" (runtime-name: "empresas-1.2.3-b15.ear")
16:48:23,089 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-4) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "empresas-web.war")
16:48:23,089 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-1) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "empresas-ejb.jar")
16:48:23,580 WARN  [org.jboss.as.server.deployment] (MSC service thread 1-5) WFLYSRV0059: A entrada do caminho da classe toolbox.jar em /content/empresas-1.2.3-b15.ear/empresas-web.war/WEB-INF/lib/itext-2.0.8.jar não direciona a um jar válido para a referência do caminho da classe.
16:48:23,718 INFO  [org.jipijapa] (MSC service thread 1-8) JIPIORMV53020253: Cache de segundo nível habilitado para empresas-1.2.3-b15.ear#fecDS
16:48:23,718 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 124) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'empresas-1.2.3-b15.ear#fecDS'
16:48:23,718 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para empresas-1.2.3-b15.ear/empresas-ejb.jar#Siemp2EjbSybase
16:48:23,718 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para empresas-1.2.3-b15.ear/empresas-ejb.jar#fecDS
16:48:23,719 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 125) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'empresas-1.2.3-b15.ear/empresas-ejb.jar#fecDS'
16:48:23,719 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 118) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'empresas-1.2.3-b15.ear/empresas-ejb.jar#Siemp2EjbSybase'
16:48:23,743 INFO  [org.jboss.weld.deployer] (MSC service thread 1-3) WFLYWELD0003: Processando da implantação weld empresas-1.2.3-b15.ear
16:48:23,769 INFO  [org.jboss.keycloak] (MSC service thread 1-2) Keycloak subsystem override for deployment empresas-web.war
16:48:23,770 INFO  [org.jboss.weld.deployer] (MSC service thread 1-2) WFLYWELD0003: Processando da implantação weld empresas-web.war
16:48:23,789 INFO  [org.jboss.weld.deployer] (MSC service thread 1-1) WFLYWELD0003: Processando da implantação weld empresas-ejb.jar
16:48:23,790 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EnvioEmailBean' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/EnvioEmailBean!br.gov.caixa.empresa.negocio.EnvioEmailService
        java:app/empresas-ejb/EnvioEmailBean!br.gov.caixa.empresa.negocio.EnvioEmailService
        java:global/empresas-1.2.3-b15/empresas-ejb/EnvioEmailBean!br.gov.caixa.empresa.negocio.EnvioEmailBean
        java:app/empresas-ejb/EnvioEmailBean!br.gov.caixa.empresa.negocio.EnvioEmailBean
16:48:23,790 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DAOBarramentoFactory' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/DAOBarramentoFactory!br.gov.caixa.empresa.barramento.dao.DAOBarramentoFactory
        java:app/empresas-ejb/DAOBarramentoFactory!br.gov.caixa.empresa.barramento.dao.DAOBarramentoFactory
        java:global/empresas-1.2.3-b15/empresas-ejb/DAOBarramentoFactory
        java:app/empresas-ejb/DAOBarramentoFactory
16:48:23,790 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutorLog' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/ProdutorLog!br.gov.caixa.empresa.log.ProdutorLog
        java:app/empresas-ejb/ProdutorLog!br.gov.caixa.empresa.log.ProdutorLog
        java:global/empresas-1.2.3-b15/empresas-ejb/ProdutorLog
        java:app/empresas-ejb/ProdutorLog
16:48:23,790 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoRiscoNegocio' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/AvaliacaoRiscoNegocio!br.gov.caixa.empresa.negocio.AvaliacaoRiscoNegocio
        java:app/empresas-ejb/AvaliacaoRiscoNegocio!br.gov.caixa.empresa.negocio.AvaliacaoRiscoNegocio
        java:global/empresas-1.2.3-b15/empresas-ejb/AvaliacaoRiscoNegocio
        java:app/empresas-ejb/AvaliacaoRiscoNegocio
16:48:23,790 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SimulacaoBean' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/SimulacaoBean!br.gov.caixa.empresa.negocio.SimulacaoBean
        java:app/empresas-ejb/SimulacaoBean!br.gov.caixa.empresa.negocio.SimulacaoBean
        java:global/empresas-1.2.3-b15/empresas-ejb/SimulacaoBean!br.gov.caixa.empresa.negocio.SimulacaoService
        java:app/empresas-ejb/SimulacaoBean!br.gov.caixa.empresa.negocio.SimulacaoService
16:48:23,790 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DadosPessoaisSICLIBean' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/DadosPessoaisSICLIBean!br.gov.caixa.empresa.negocio.DadosPessoaisSICLIBean
        java:app/empresas-ejb/DadosPessoaisSICLIBean!br.gov.caixa.empresa.negocio.DadosPessoaisSICLIBean
        java:global/empresas-1.2.3-b15/empresas-ejb/DadosPessoaisSICLIBean!br.gov.caixa.empresa.negocio.DadosPessoaisSICLIService
        java:app/empresas-ejb/DadosPessoaisSICLIBean!br.gov.caixa.empresa.negocio.DadosPessoaisSICLIService
16:48:23,790 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoDeRiscoDAO' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/AvaliacaoDeRiscoDAO!br.gov.caixa.empresa.barramento.dao.AvaliacaoDeRiscoDAO
        java:app/empresas-ejb/AvaliacaoDeRiscoDAO!br.gov.caixa.empresa.barramento.dao.AvaliacaoDeRiscoDAO
        java:global/empresas-1.2.3-b15/empresas-ejb/AvaliacaoDeRiscoDAO
        java:app/empresas-ejb/AvaliacaoDeRiscoDAO
16:48:23,790 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ParametrizacaoBean' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/ParametrizacaoBean!br.gov.caixa.empresa.negocio.ParametrizacaoBean
        java:app/empresas-ejb/ParametrizacaoBean!br.gov.caixa.empresa.negocio.ParametrizacaoBean
        java:global/empresas-1.2.3-b15/empresas-ejb/ParametrizacaoBean
        java:app/empresas-ejb/ParametrizacaoBean
16:48:23,790 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-1) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ContratacaoBean' na unidade de implementação 'subdeployment "empresas-ejb.jar" of deployment "empresas-1.2.3-b15.ear"' são como segue:
        java:global/empresas-1.2.3-b15/empresas-ejb/ContratacaoBean!br.gov.caixa.empresa.negocio.ContratacaoService
        java:app/empresas-ejb/ContratacaoBean!br.gov.caixa.empresa.negocio.ContratacaoService
        java:global/empresas-1.2.3-b15/empresas-ejb/ContratacaoBean!br.gov.caixa.empresa.negocio.ContratacaoBean
        java:app/empresas-ejb/ContratacaoBean!br.gov.caixa.empresa.negocio.ContratacaoBean
16:48:23,792 INFO  [org.jipijapa] (MSC service thread 1-5) JIPIORMV53020253: Cache de segundo nível habilitado para empresas-1.2.3-b15.ear#fecDS
16:48:23,820 INFO  [org.jipijapa] (MSC service thread 1-7) JIPIORMV53020253: Cache de segundo nível habilitado para empresas-1.2.3-b15.ear/empresas-ejb.jar#Siemp2EjbSybase
16:48:23,821 INFO  [org.jipijapa] (MSC service thread 1-7) JIPIORMV53020253: Cache de segundo nível habilitado para empresas-1.2.3-b15.ear/empresas-ejb.jar#fecDS
16:48:23,821 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 124) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'empresas-1.2.3-b15.ear#fecDS'
16:48:23,827 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 125) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'empresas-1.2.3-b15.ear/empresas-ejb.jar#fecDS'
16:48:23,827 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 118) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'empresas-1.2.3-b15.ear/empresas-ejb.jar#Siemp2EjbSybase'
16:48:24,239 ERROR [org.jboss.msc.service.fail] (MSC service thread 1-4) MSC000001: Failed to start service jboss.deployment.unit."empresas-1.2.3-b15.ear".WeldStartService: org.jboss.msc.service.StartException in service jboss.deployment.unit."empresas-1.2.3-b15.ear".WeldStartService: Failed to start service
Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type ParametrizacaoService with qualifiers @Default
16:48:24,241 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 122) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SIEMP-EMPRESAS")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"empresas-1.2.3-b15.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type ParametrizacaoService with qualifiers @Default
16:48:24,241 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 122) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SIEMP-EMPRESAS")]) - falha na descrição: {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"empresas-1.2.3-b15.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type ParametrizacaoService with qualifiers @Default
16:48:24,241 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 122) WFLYSRV0021: O procedimento da implantação "empresas-1.2.3-b15.ear" foi revertido com mensagem de falha:
{"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\"empresas-1.2.3-b15.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type ParametrizacaoService with qualifiers @Default
16:48:24,242 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 118) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'empresas-1.2.3-b15.ear#fecDS'
16:48:24,242 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 124) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'empresas-1.2.3-b15.ear/empresas-ejb.jar#fecDS'
16:48:24,243 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 125) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'empresas-1.2.3-b15.ear/empresas-ejb.jar#Siemp2EjbSybase'
16:48:24,244 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 125) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'empresas-1.2.3-b15.ear/empresas-ejb.jar#Siemp2EjbSybase'
16:48:24,244 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 124) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'empresas-1.2.3-b15.ear/empresas-ejb.jar#fecDS'
16:48:24,245 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 118) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'empresas-1.2.3-b15.ear#fecDS'
16:48:24,258 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-6) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: empresas-ejb.jar) em 16ms
16:48:24,269 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: empresas-web.war) em 27ms
16:48:24,271 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0028: Implantação interrompida SIEMP-EMPRESAS (runtime-name: empresas-1.2.3-b15.ear) em 29ms
16:48:46,078 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0027: Iniciando a implantação do "SIFEC-RURAL4" (runtime-name: "rural-2.115.1.1-b2421.ear")
16:48:46,926 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-3) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "rural-ejb.jar")
16:48:46,926 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-2) WFLYSRV0207: Iniciando a subimplantação (runtime-name: "rural-web.war")
16:48:47,804 INFO  [org.jipijapa] (MSC service thread 1-3) JIPIORMV53020253: Cache de segundo nível habilitado para rural-2.115.1.1-b2421.ear#fecDS
16:48:47,804 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 124) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'rural-2.115.1.1-b2421.ear#fecDS'
16:48:47,815 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase
16:48:47,815 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2
16:48:47,818 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 118) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase'
16:48:47,819 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 126) WFLYJPA0010: Iniciando unidade de persistência (fase 1 de 2) Serviço'rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2'
16:48:47,848 INFO  [org.jboss.weld.deployer] (MSC service thread 1-8) WFLYWELD0003: Processando da implantação weld rural-2.115.1.1-b2421.ear
16:48:47,878 INFO  [org.jboss.keycloak] (MSC service thread 1-8) Keycloak subsystem override for deployment rural-web.war
16:48:47,878 INFO  [org.jboss.weld.deployer] (MSC service thread 1-8) WFLYWELD0003: Processando da implantação weld rural-web.war
16:48:47,915 INFO  [org.jboss.weld.deployer] (MSC service thread 1-7) WFLYWELD0003: Processando da implantação weld rural-ejb.jar
16:48:47,917 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'EmailBean' na unidade de implementação 'subdeployment "rural-ejb.jar" of deployment "rural-2.115.1.1-b2421.ear"' são como segue:
        java:global/rural-2.115.1.1-b2421/rural-ejb/EmailBean!br.gov.caixa.emprestimo.email.EmailBean
        java:app/rural-ejb/EmailBean!br.gov.caixa.emprestimo.email.EmailBean
        java:global/rural-2.115.1.1-b2421/rural-ejb/EmailBean
        java:app/rural-ejb/EmailBean
16:48:47,917 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'DAOBarramentoFactory' na unidade de implementação 'subdeployment "rural-ejb.jar" of deployment "rural-2.115.1.1-b2421.ear"' são como segue:
        java:global/rural-2.115.1.1-b2421/rural-ejb/DAOBarramentoFactory!br.gov.caixa.emprestimo.barramento.dao.DAOBarramentoFactory
        java:app/rural-ejb/DAOBarramentoFactory!br.gov.caixa.emprestimo.barramento.dao.DAOBarramentoFactory
        java:global/rural-2.115.1.1-b2421/rural-ejb/DAOBarramentoFactory
        java:app/rural-ejb/DAOBarramentoFactory
16:48:47,917 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'ProdutorLog' na unidade de implementação 'subdeployment "rural-ejb.jar" of deployment "rural-2.115.1.1-b2421.ear"' são como segue:
        java:global/rural-2.115.1.1-b2421/rural-ejb/ProdutorLog!br.gov.caixa.emprestimo.log.ProdutorLog
        java:app/rural-ejb/ProdutorLog!br.gov.caixa.emprestimo.log.ProdutorLog
        java:global/rural-2.115.1.1-b2421/rural-ejb/ProdutorLog
        java:app/rural-ejb/ProdutorLog
16:48:47,917 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'SirurRestServiceImpl' na unidade de implementação 'subdeployment "rural-ejb.jar" of deployment "rural-2.115.1.1-b2421.ear"' são como segue:
        java:global/rural-2.115.1.1-b2421/rural-ejb/SirurRestServiceImpl!br.gov.caixa.emprestimo.rest.sirur.SirurRestService
        java:app/rural-ejb/SirurRestServiceImpl!br.gov.caixa.emprestimo.rest.sirur.SirurRestService
        java:global/rural-2.115.1.1-b2421/rural-ejb/SirurRestServiceImpl!br.gov.caixa.emprestimo.rest.sirur.SirurRestServiceImpl
        java:app/rural-ejb/SirurRestServiceImpl!br.gov.caixa.emprestimo.rest.sirur.SirurRestServiceImpl
16:48:47,917 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'AvaliacaoDeRiscoDAO' na unidade de implementação 'subdeployment "rural-ejb.jar" of deployment "rural-2.115.1.1-b2421.ear"' são como segue:
        java:global/rural-2.115.1.1-b2421/rural-ejb/AvaliacaoDeRiscoDAO!br.gov.caixa.emprestimo.dao.AvaliacaoDeRiscoDAO
        java:app/rural-ejb/AvaliacaoDeRiscoDAO!br.gov.caixa.emprestimo.dao.AvaliacaoDeRiscoDAO
        java:global/rural-2.115.1.1-b2421/rural-ejb/AvaliacaoDeRiscoDAO
        java:app/rural-ejb/AvaliacaoDeRiscoDAO
16:48:47,917 INFO  [org.jboss.as.ejb3.deployment] (MSC service thread 1-7) WFLYEJB0473: As associações JNDI para o bean de sessão chamado 'CreditoRuralBean' na unidade de implementação 'subdeployment "rural-ejb.jar" of deployment "rural-2.115.1.1-b2421.ear"' são como segue:
        java:global/rural-2.115.1.1-b2421/rural-ejb/CreditoRuralBean!br.gov.caixa.emprestimo.negocio.CreditoRuralBean
        java:app/rural-ejb/CreditoRuralBean!br.gov.caixa.emprestimo.negocio.CreditoRuralBean
        java:module/CreditoRuralBean!br.gov.caixa.emprestimo.negocio.CreditoRuralBean
        java:global/rural-2.115.1.1-b2421/rural-ejb/CreditoRuralBean!br.gov.caixa.emprestimo.negocio.CreditoRuralService
        java:app/rural-ejb/CreditoRuralBean!br.gov.caixa.emprestimo.negocio.CreditoRuralService
        java:module/CreditoRuralBean!br.gov.caixa.emprestimo.negocio.CreditoRuralService
16:48:47,919 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para rural-2.115.1.1-b2421.ear#fecDS
16:48:48,003 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 127) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'rural-2.115.1.1-b2421.ear#fecDS'
16:48:48,006 ERROR [org.jboss.msc.service.fail] (MSC service thread 1-8) MSC000001: Failed to start service jboss.deployment.subunit."rural-2.115.1.1-b2421.ear"."rural-ejb.jar".INSTALL: org.jboss.msc.service.StartException in service jboss.deployment.subunit."rural-2.115.1.1-b2421.ear"."rural-ejb.jar".INSTALL: WFLYSRV0153: Falha ao processar a fase INSTALL de subdeployment "rural-ejb.jar" of deployment "rural-2.115.1.1-b2421.ear"
16:48:48,022 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 124) WFLYCLINF0002: Cache rural-2.115.1.1-b2421.ear.rural-web.war inicializado a partir do recipiente web
16:48:48,092 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 122) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SIFEC-RURAL4")]) - falha na descrição: {
    "WFLYCTL0080: Falha de serviços" => {"jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".INSTALL" => "WFLYSRV0153: Falha ao processar a fase INSTALL de subdeployment \"rural-ejb.jar\" of deployment \"rural-2.115.1.1-b2421.ear\"
        "jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".jndiDependencyService",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".beanmanager",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".deploymentCompleteService",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO",
        "jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\"",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean"
        "jboss.deployment.unit.\"rural-2.115.1.1-b2421.ear\".WeldStartService faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".jndiDependencyService, jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"br.gov.caixa.arqrefweb.controle.AppServlet\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"br.gov.caixa.emprestimo.rest.filtro.FiltroRuralLog\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".weld.weldClassIntrospector faltam [jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".beanmanager]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".batch.artifact.factory faltam [jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".beanmanager]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"javax.servlet.jsp.jstl.tlv.ScriptFreeTLV\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.deployment.unit.\"rural-2.115.1.1-b2421.ear\".deploymentCompleteService faltam [jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".deploymentCompleteService]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"javax.faces.webapp.FacetTag\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"com.sun.faces.config.ConfigureListener\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"javax.servlet.jsp.jstl.tlv.PermittedTaglibsTLV\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]"
16:48:48,093 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 122) WFLYCTL0013: Falha na operação ("deploy") - endereço ([("deployment" => "SIFEC-RURAL4")]) - falha na descrição: {
    "WFLYCTL0080: Falha de serviços" => {"jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".INSTALL" => "WFLYSRV0153: Falha ao processar a fase INSTALL de subdeployment \"rural-ejb.jar\" of deployment \"rural-2.115.1.1-b2421.ear\"
        "jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".jndiDependencyService",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".beanmanager",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".deploymentCompleteService",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO",
        "jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\"",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean"
        "jboss.deployment.unit.\"rural-2.115.1.1-b2421.ear\".WeldStartService faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".jndiDependencyService, jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"br.gov.caixa.arqrefweb.controle.AppServlet\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"br.gov.caixa.emprestimo.rest.filtro.FiltroRuralLog\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".weld.weldClassIntrospector faltam [jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".beanmanager]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".batch.artifact.factory faltam [jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".beanmanager]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"javax.servlet.jsp.jstl.tlv.ScriptFreeTLV\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.deployment.unit.\"rural-2.115.1.1-b2421.ear\".deploymentCompleteService faltam [jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".deploymentCompleteService]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"javax.faces.webapp.FacetTag\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"com.sun.faces.config.ConfigureListener\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"javax.servlet.jsp.jstl.tlv.PermittedTaglibsTLV\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]"
16:48:48,093 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 122) WFLYSRV0021: O procedimento da implantação "rural-2.115.1.1-b2421.ear" foi revertido com mensagem de falha:
    "WFLYCTL0080: Falha de serviços" => {"jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".INSTALL" => "WFLYSRV0153: Falha ao processar a fase INSTALL de subdeployment \"rural-ejb.jar\" of deployment \"rural-2.115.1.1-b2421.ear\"
        "jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".jndiDependencyService",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".beanmanager",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".deploymentCompleteService",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO",
        "jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\"",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean"
        "jboss.deployment.unit.\"rural-2.115.1.1-b2421.ear\".WeldStartService faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".jndiDependencyService, jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"br.gov.caixa.arqrefweb.controle.AppServlet\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"br.gov.caixa.emprestimo.rest.filtro.FiltroRuralLog\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".weld.weldClassIntrospector faltam [jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".beanmanager]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.ProdutorLog]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".batch.artifact.factory faltam [jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".beanmanager]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"javax.servlet.jsp.jstl.tlv.ScriptFreeTLV\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.deployment.unit.\"rural-2.115.1.1-b2421.ear\".deploymentCompleteService faltam [jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-ejb.jar\".deploymentCompleteService]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"javax.faces.webapp.FacetTag\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.AvaliacaoDeRiscoDAO]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"com.sun.faces.config.ConfigureListener\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory.ValidatorFactory faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl.Validator faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.CreditoRuralBean]",
        "jboss.deployment.subunit.\"rural-2.115.1.1-b2421.ear\".\"rural-web.war\".component.\"javax.servlet.jsp.jstl.tlv.PermittedTaglibsTLV\".START faltam [jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase\", jboss.persistenceunit.\"rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2\"]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.SirurRestServiceImpl]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean.InstanceName faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.EmailBean]",
        "jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory.InAppClientContainer faltam [jboss.naming.context.java.comp.\"rural-2.115.1.1-b2421\".rural-ejb.DAOBarramentoFactory]"
16:48:48,094 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 126) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'rural-2.115.1.1-b2421.ear/rural-ejb.jar#SiempEjbDB2'
16:48:48,094 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 118) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'rural-2.115.1.1-b2421.ear/rural-ejb.jar#Siemp2EjbSybase'
16:48:48,094 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 127) WFLYJPA0011: Interrompendo unidade de persistência (fase 2 de 2) Serviço 'rural-2.115.1.1-b2421.ear#fecDS'
16:48:48,095 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 126) WFLYJPA0011: Interrompendo unidade de persistência (fase 1 de 2) Serviço 'rural-2.115.1.1-b2421.ear#fecDS'
16:48:48,100 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 127) WFLYCLINF0003: Cache rural-2.115.1.1-b2421.ear.rural-web.war encerrado a partir do recipiente web
16:48:48,107 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-5) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: rural-ejb.jar) em 13ms
16:48:48,138 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-8) WFLYSRV0208: Interrompendo a subimplantação (runtime-name: rural-web.war) em 44ms
16:48:48,142 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-8) WFLYSRV0028: Implantação interrompida SIFEC-RURAL4 (runtime-name: rural-2.115.1.1-b2421.ear) em 48ms


