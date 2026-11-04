[domain@localhost:9443 /] deploy --name=SICCR-PJ --server-groups=sifec-intranet
{"WFLYDC0074: Operation failed or was rolled back on all servers. Server failures:" => {"server-group" => {"sifec-intranet" => {"host" => {"hc_cbrdeapllx473" => {"sifec-intranet_node1_lx
473" => {"WFLYCTL0062: A operação de composição falhou e foi revertida. Segue abaixo as etapas que falharam:" => {"Operação step-2" => {"WFLYCTL0080: Falha de serviços" => {"jboss.deployment.unit.\
"sifec-ccr-pj.ear\".WeldStartService" => "Failed to start service
    Caused by: org.jboss.weld.exceptions.DeploymentException: Exception List with 2 exceptions:
Exception 0 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
  at injection point [BackedAnnotatedField] @Inject @UsuarioContexto protected br.gov.caixa.intgr.comum.operacao.OperacaoIntegracaoMQAbstrata.usuario
  at br.gov.caixa.intgr.comum.operacao.OperacaoIntegracaoMQAbstrata.usuario(OperacaoIntegracaoMQAbstrata.java:0)
WELD-001475: The following beans match by type, but none have matching qualifiers:
  - Managed Bean [class br.gov.caixa.intgr.comum.bean.Usuario] with qualifiers [@Any @Default]

        at org.jboss.weld.bootstrap.Validator.validateInjectionPointForDeploymentProblems(Validator.java:378)
        at org.jboss.weld.bootstrap.Validator.validateInjectionPoint(Validator.java:290)
        at org.jboss.weld.bootstrap.Validator.validateGeneralBean(Validator.java:143)
        at org.jboss.weld.bootstrap.Validator.validateRIBean(Validator.java:164)
        at org.jboss.weld.bootstrap.Validator.validateBean(Validator.java:526)
        at org.jboss.weld.bootstrap.ConcurrentValidator$1.doWork(ConcurrentValidator.java:64)
        at org.jboss.weld.bootstrap.ConcurrentValidator$1.doWork(ConcurrentValidator.java:62)
        at org.jboss.weld.executor.IterativeWorkerTaskFactory$1.call(IterativeWorkerTaskFactory.java:62)
        at org.jboss.weld.executor.IterativeWorkerTaskFactory$1.call(IterativeWorkerTaskFactory.java:55)
        at java.util.concurrent.FutureTask.run(FutureTask.java:266)
        at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
        at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
        at java.lang.Thread.run(Thread.java:750)
        at org.jboss.threads.JBossThread.run(JBossThread.java:513)
Exception 1 :
org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
  at injection point [BackedAnnotatedField] @Inject @UsuarioContexto protected br.gov.caixa.intgr.comum.operacao.OperacaoIntegracaoMQAbstrata.usuario
  at br.gov.caixa.intgr.comum.operacao.OperacaoIntegracaoMQAbstrata.usuario(OperacaoIntegracaoMQAbstrata.java:0)
WELD-001475: The following beans match by type, but none have matching qualifiers:
  - Managed Bean [class br.gov.caixa.intgr.comum.bean.Usuario] with qualifiers [@Any @Default]

        at org.jboss.weld.bootstrap.Validator.validateInjectionPointForDeploymentProblems(Validator.java:378)
        at org.jboss.weld.bootstrap.Validator.validateInjectionPoint(Validator.java:290)
        at org.jboss.weld.bootstrap.Validator.validateGeneralBean(Validator.java:143)
        at org.jboss.weld.bootstrap.Validator.validateRIBean(Validator.java:164)
        at org.jboss.weld.bootstrap.Validator.validateBean(Validator.java:526)
        at org.jboss.weld.bootstrap.ConcurrentValidator$1.doWork(ConcurrentValidator.java:64)
        at org.jboss.weld.bootstrap.ConcurrentValidator$1.doWork(ConcurrentValidator.java:62)
        at org.jboss.weld.executor.IterativeWorkerTaskFactory$1.call(IterativeWorkerTaskFactory.java:62)
        at org.jboss.weld.executor.IterativeWorkerTaskFactory$1.call(IterativeWorkerTaskFactory.java:55)
        at java.util.concurrent.FutureTask.run(FutureTask.java:266)
        at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
        at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
        at java.lang.Thread.run(Thread.java:750)
        at org.jboss.threads.JBossThread.run(JBossThread.java:513)
"}}}}}}}}}}

[domain@localhost:9443 /] deployment-info --name=SICCR-PJ
NAME     RUNTIME-NAME
SICCR-PJ sifec-ccr-pj.ear

SERVER-GROUP    STATE
siemp           not added
sifec-intranet  not added
sifec-intranet2 not added
sipen           not added

[domain@localhost:9443 /]




[sudo] password for p585600:
15:51:11,899 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 32) WFLYSRV0021: O procedimento da implantação "sifec-ccr-pj.ear" foi revertido com mensagem de falha:
15:53:10,455 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 32) WFLYSRV0021: O procedimento da implantação "sifec-ccr-pj.ear" foi revertido com mensagem de falha:



o thiago jeferson fez o deploy pela consoele ele fez errado?
