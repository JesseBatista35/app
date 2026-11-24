Durante a validação da implantação do módulo SICOW SEG OKD no ambiente OKD, foi identificado um comportamento divergente em relação aos demais sistemas já implantados, como SICOW PORTAL OKD e SICOW LG OKD.

A release está sendo processada sem erros aparentes, porém a aplicação não apresenta o conteúdo esperado após o deploy.

Durante as análises realizadas, foi levantada a possibilidade de ausência dos seguintes artefatos relacionados ao módulo SIUSR:

/opt/jboss/modules/br/gov/caixa/siusr/main/module.xml
/opt/jboss/modules/br/gov/caixa/siusr/main/arquivo-siusr.jar

Entretanto, após diversas verificações e comparações com as configurações dos sistemas SICOW PORTAL OKD e SICOW LG OKD, não foram identificadas diferenças que justifiquem o comportamento observado.

Adicionalmente, quando a configuração abaixo é mantida no ambiente:

<global-modules>
<module name="br.gov.caixa.siusr" slot="main"/>
</global-modules>
 

a aplicação retorna erro HTTP 404. Quando essa configuração é removida, o erro deixa de ocorrer, porém a interface não é carregada, permanecendo apenas uma tela em branco


Sandro Araujo Dantas
REQ000147155016 - SICOW SEG OKD
Bom dia!
 
Daniel Ribeiro da Silva
Paulo Ferreira de Almeida Junior
 
Segue resposta da REQ do SICOW SEG
 
 
23/11/2026 18:58:56 ; (P744064)
Boa noite!

Informamos que o pod subiu com erro, devido a problemas no código da aplicação, não sendo deployado com sucesso o pacote conforme segue:

2026-11-23 14:43:51,031 ERROR [org.jboss.msc.service.fail] (MSC service thread 1-2) MSC000001: Failed to start service jboss.module.service."deployment.sicow-seg-okd.war".main: org.jboss.msc.service.StartException in service jboss.module.service."deployment.sicow-seg-okd.war".main:
 WFLYSRV0179: Failed to load module: deployment.sicow-seg-okd.war
at org.jboss.as.server.moduleservice.ModuleLoadService.start(ModuleLoadService.java:116)
at org.jboss.msc.service.ServiceControllerImpl$StartTask.startService(ServiceControllerImpl.java:1739)
at org.jboss.msc.service.ServiceControllerImpl$StartTask.execute(ServiceControllerImpl.java:1701)
at org.jboss.msc.service.ServiceControllerImpl$ControllerTask.run(ServiceControllerImpl.java:1559)
at org.jboss.threads.ContextClassLoaderSavingRunnable.run(ContextClassLoaderSavingRunnable.java:35)
at org.jboss.threads.EnhancedQueueExecutor.safeRun(EnhancedQueueExecutor.java:1990)
at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.doRunTask(EnhancedQueueExecutor.java:1486)
at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.run(EnhancedQueueExecutor.java:1377)
at java.lang.Thread.run(Thread.java:750)
Caused by: org.jboss.modules.ModuleNotFoundException: br.gov.caixa.siusr
at org.jboss.modules.Module.addPaths(Module.java:1288)
at org.jboss.modules.Module.link(Module.java:1644)
at org.jboss.modules.Module.relinkIfNecessary(Module.java:1672)
at org.jboss.modules.ModuleLoader.loadModule(ModuleLoader.java:303)
at org.jboss.modules.ModuleLoader.loadModule(ModuleLoader.java:287)
at org.jboss.as.server.moduleservice.ModuleLoadService.start(ModuleLoadService.java:93)
... 8 more

2026-11-23 14:43:51,035 ERROR [org.jboss.as.controller.management-operation] (Controller Boot Thread) WFLYCTL0013: Operation ("deploy") failed - address: ([("deployment" => "sicow-seg-okd.war")]) - failure description: {"WFLYCTL0080: Failed services" => {"jboss.module.service.\"deployment.sicow-seg-okd.war\".main"
 => "WFLYSRV0179: Failed to load module: deployment.sicow-seg-okd.war
Caused by: org.jboss.modules.ModuleNotFoundException: br.gov.caixa.siusr"}}

Obs, Por este motivo que ocorre erro 404 por não encontrar o contexto da aplicação que não foi feito deploy.

At.te,

Wellington Silva
 
 
Sandro Araujo Dantas
Bom dia!   Daniel Ribeiro da Silva Paulo Ferreira de Almeida Junior   Segue resposta da REQ do SICOW SEG        23/11/2026 18:58:56 ; (P744064)   Boa noite!  Informamos que o pod subiu com erro, dev…
REQ000147155016 - REABERTO
 
MOTIVO: 
 
24/11/2026 09:12:50 ; (F730914)
Já tínhamos conhecimento do erro, porém não sabemos como solucioná-lo, poderia nos ajudar? Podemos entrar em reunião caso seja necessário ação de ambas as equipes.
 
23/11/2026 18:58:56 ; (P744064)
Boa noite!

Informamos que o pod subiu com erro, devido a problemas no código da aplicação, não sendo deployado com sucesso o pacote conforme segue:

2026-11-23 14:43:51,031 ERROR [org.jboss.msc.service.fail] (MSC service thread 1-2) MSC000001: Failed to start service jboss.module.service."deployment.sicow-seg-okd.war".main: org.jboss.msc.service.StartException in service jboss.module.service."deployment.sicow-seg-okd.war".main:
 WFLYSRV0179: Failed to load module: deployment.sicow-seg-okd.war
at org.jboss.as.server.moduleservice.ModuleLoadService.start(ModuleLoadService.java:116)
at org.jboss.msc.service.ServiceControllerImpl$StartTask.startService(ServiceControllerImpl.java:1739)
at org.jboss.msc.service.ServiceControllerImpl$StartTask.execute(ServiceControllerImpl.java:1701)
at org.jboss.msc.service.ServiceControllerImpl$ControllerTask.run(ServiceControllerImpl.java:1559)
at org.jboss.threads.ContextClassLoaderSavingRunnable.run(ContextClassLoaderSavingRunnable.java:35)
at org.jboss.threads.EnhancedQueueExecutor.safeRun(EnhancedQueueExecutor.java:1990)
at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.doRunTask(EnhancedQueueExecutor.java:1486)
at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.run(EnhancedQueueExecutor.java:1377)
at java.lang.Thread.run(Thread.java:750)
Caused by: org.jboss.modules.ModuleNotFoundException: br.gov.caixa.siusr
at org.jboss.modules.Module.addPaths(Module.java:1288)
at org.jboss.modules.Module.link(Module.java:1644)
at org.jboss.modules.Module.relinkIfNecessary(Module.java:1672)
at org.jboss.modules.ModuleLoader.loadModule(ModuleLoader.java:303)
at org.jboss.modules.ModuleLoader.loadModule(ModuleLoader.java:287)
at org.jboss.as.server.moduleservice.ModuleLoadService.start(ModuleLoadService.java:93)
... 8 more

2026-11-23 14:43:51,035 ERROR [org.jboss.as.controller.management-operation] (Controller Boot Thread) WFLYCTL0013: Operation ("deploy") failed - address: ([("deployment" => "sicow-seg-okd.war")]) - failure description: {"WFLYCTL0080: Failed services" => {"jboss.module.service.\"deployment.sicow-seg-okd.war\".main"
 => "WFLYSRV0179: Failed to load module: deployment.sicow-seg-okd.war
Caused by: org.jboss.modules.ModuleNotFoundException: br.gov.caixa.siusr"}}

Obs, Por este motivo que ocorre erro 404 por não encontrar o contexto da aplicação que não foi feito deploy.

At.te,

Wellington Silva
 
23/11/2026 17:21:24 ; (P779123)
Demanda inicial com viés de falha, erro, degradação ou esgotamento de infraestrutura, serviço, máquina, armazenamento, rotina ou situação que esteja na iminência de tornar-se incidente. Previsto atendimento em até 8 horas. [CENTRAL-SID]
 
23/11/2026 15:53:41 ; (P768728)
Prezado(a),

Informamos que sua solicitação PRIORIZADA foi recebida .

Conforme definição da Coordenação NPRD (CESTI36) e em conformidade com o fluxo de atendimento estabelecido para a Esteira DevOps NPRD, os atendimentos realizados por esta equipe seguem SLAs específicos, distintos dos praticados pelas demais macrocélulas.

Dessa forma, o SLA desta solicitação foi ajustado para até 8 horas úteis, prazo aplicável à sua classificação.

Nesse período, a demanda será analisada para validação do escopo de atuação da equipe e definição do tratamento adequado.

Caso seja identificado que a solicitação não pertence ao escopo de atendimento da Esteira DevOps NPRD, a demanda será direcionada à equipe responsável, observando os fluxos e processos vigentes.

Novas informações e atualizações serão registradas diretamente nesta WO.

Atenciosamente,

Esteira DevOps NPRD
 
 
 
