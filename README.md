Solicito apoio da equipe de Infraestrutura para investigar uma falha de comunicação entre o backend do SIMPF no ambiente de Desenvolvimento (DES) e o serviço SIGCT.

Em 23/09/2026, o pod simpf-backend-des-437-bdwf9, no namespace simpf-des, hospedado no nó ceadecldlx058.nprd.caixa, tentou acessar sctdeapllx0018.df.caixa pela porta TCP 8443. O DNS resolveu o destino para 10.116.83.19, porém a tentativa terminou com HttpHostConnectException: Connection timed out, após aproximadamente 2 minutos e 10 segundos.

A mesmo recurso funciona no ambiente de TQS.

Verificações solicitadas:
Validar a conectividade de saída do ambiente DES para 10.116.83.19:8443;

Verificar rota, regras de firewall/políticas de rede e rota de retorno;

Confirmar o endereço de origem efetivamente observado pelo destino, incluindo eventual NAT.

O Graylog registrou o IP do pod como 25.0.44.134; esse endereço é fornecido apenas como referência e deve ser confirmado como origem efetiva antes de ser utilizado em qualquer regra de rede.

A evidência confirma a falha ocorrida em 23/09/2026. Se possível, solicitamos também um teste de conectividade TCP a partir do pod ou de um ambiente com o mesmo contexto de rede, para verificar a situação atual.


pod atual 

simpf-backend-des-447-gzfdw
Running

exec java -Dquarkus.http.host=0.0.0.0 -Dquarkus.http.port=8080 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Djavax.net.ssl.trustStore=/deployments/caixa-truststore-acteste-nprd.jks -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/quarkus-run.jar
LogManager error of type WRITE_FAILURE: The delayed handler's queue was overrun and log record(s) were lost. Did you forget to configure logging?
__  ____  __  _____   ___  __ ____  ______ 
 --/ __ \/ / / / _ | / _ \/ //_/ / / / __/ 
 -/ /_/ / /_/ / __ |/ , _/ ,< / /_/ /\ \   
--\___\_\____/_/ |_/_/|_/_/|_|\____/___/   
2026-10-15 16:34:43,242 DEBUG [org.hib.sta.int.StatisticsInitiator] (main) Statistics initialized [enabled=true]
2026-10-15 16:36:49,054 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-5) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.TipoContratoEntity, time: 9ms, rows: 5
2026-10-15 16:36:49,303 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-5) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.SistemaEntity, time: 2ms, rows: 0
2026-10-15 16:36:49,321 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-8) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.MaquinaEstadoEntity WHERE tipo = ?1 and tipoContrato.nuTipoContrato = ?2, time: 10ms, rows: 8
2026-10-15 16:36:49,754 DEBUG [org.hib.sta.int.StatisticsImpl] (ForkJoinPool.commonPool-worker-59) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL) AND (ae.id.estadoMaquina.nuEstadoMaquina = :nuEstadoMaquina OR :nuEstadoMaquina IS NULL)  AND analise.contrato.tipoContrato.nuTipoContrato like '%'||:nuTipoContrato||'%' , time: 19ms, rows: 1
2026-10-15 16:36:49,755 DEBUG [org.hib.sta.int.StatisticsImpl] (ForkJoinPool.commonPool-worker-37) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL) AND (ae.id.estadoMaquina.nuEstadoMaquina = :nuEstadoMaquina OR :nuEstadoMaquina IS NULL)  AND analise.contrato.tipoContrato.nuTipoContrato like '%'||:nuTipoContrato||'%' , time: 21ms, rows: 1
2026-10-15 16:36:49,757 DEBUG [org.hib.sta.int.StatisticsImpl] (ForkJoinPool.commonPool-worker-51) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL) AND (ae.id.estadoMaquina.nuEstadoMaquina = :nuEstadoMaquina OR :nuEstadoMaquina IS NULL)  AND analise.contrato.tipoContrato.nuTipoContrato like '%'||:nuTipoContrato||'%' , time: 22ms, rows: 1
2026-10-15 16:36:49,763 DEBUG [org.hib.sta.int.StatisticsImpl] (ForkJoinPool.commonPool-worker-23) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL) AND (ae.id.estadoMaquina.nuEstadoMaquina = :nuEstadoMaquina OR :nuEstadoMaquina IS NULL)  AND analise.contrato.tipoContrato.nuTipoContrato like '%'||:nuTipoContrato||'%' , time: 28ms, rows: 1
2026-10-15 16:36:49,773 DEBUG [org.hib.sta.int.StatisticsImpl] (ForkJoinPool.commonPool-worker-9) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL) AND (ae.id.estadoMaquina.nuEstadoMaquina = :nuEstadoMaquina OR :nuEstadoMaquina IS NULL)  AND analise.contrato.tipoContrato.nuTipoContrato like '%'||:nuTipoContrato||'%' , time: 38ms, rows: 1
2026-10-15 16:36:49,782 DEBUG [org.hib.sta.int.StatisticsImpl] (ForkJoinPool.commonPool-worker-45) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL) AND (ae.id.estadoMaquina.nuEstadoMaquina = :nuEstadoMaquina OR :nuEstadoMaquina IS NULL)  AND analise.contrato.tipoContrato.nuTipoContrato like '%'||:nuTipoContrato||'%' , time: 47ms, rows: 1
2026-10-15 16:36:49,929 DEBUG [org.hib.sta.int.StatisticsImpl] (ForkJoinPool.commonPool-worker-45) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL) AND (ae.id.estadoMaquina.nuEstadoMaquina = :nuEstadoMaquina OR :nuEstadoMaquina IS NULL)  AND analise.contrato.tipoContrato.nuTipoContrato like '%'||:nuTipoContrato||'%' , time: 16ms, rows: 1
2026-10-15 16:36:49,963 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  AND analise.contrato.tipoContrato.nuTipoContrato like '%'||:nuTipoContrato||'%' , time: 38ms, rows: 1
2026-10-15 16:36:50,145 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT analise, em FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  AND analise.contrato.tipoContrato.nuTipoContrato like '%'||:nuTipoContrato||'%' ORDER BY analise.dataModificacao ASC, time: 181ms, rows: 30
2026-10-15 16:36:54,486 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ServicoEntity, time: 2ms, rows: 0
2026-10-15 16:36:54,638 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.MaquinaEstadoEntity WHERE tipo = ?1, time: 10ms, rows: 32
2026-10-15 16:36:55,169 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  , time: 331ms, rows: 1
2026-10-15 16:36:55,527 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT analise, em FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  ORDER BY analise.dataModificacao DESC, time: 356ms, rows: 30
2026-10-15 16:36:55,900 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ContagemSNAPEntity WHERE nuContagemDadosSnap IN (:ids_0, :ids_1), time: 1ms, rows: 2
2026-10-15 16:36:55,918 WARNING [br.gov.cai.sim.ser.sip.ItemTrabalhoService] (executor-thread-2) Fluxo Simplifica indispon?vel para o item informado. Aplicando fallback interno.: java.lang.UnsupportedOperationException: Consulta ao Simplifica n?o implementada ainda.
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService.consultarSimplifica(ItemTrabalhoService.java:91)
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService.buscarComFallbackSimplifica(ItemTrabalhoService.java:68)
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService.findHistoriaUsuarioById(ItemTrabalhoService.java:56)
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService_ClientProxy.findHistoriaUsuarioById(ItemTrabalhoService_ClientProxy.zig:157)
	at br.gov.caixa.simpf.service.CalculoContagemService.getListaItemBacklogRTC(CalculoContagemService.java:239)
	at br.gov.caixa.simpf.service.CalculoContagemService.pontuarItensBacklog(CalculoContagemService.java:206)
	at br.gov.caixa.simpf.service.CalculoContagemService_Subclass.pontuarItensBacklog$$superaccessor1(CalculoContagemService_Subclass.zig:211)
	at br.gov.caixa.simpf.service.CalculoContagemService_Subclass$$function$$1.apply(CalculoContagemService_Subclass$$function$$1.zig:33)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.proceed(AroundInvokeInvocationContext.java:54)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.invokeInCallerTx(TransactionalInterceptorBase.java:252)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.doIntercept(TransactionalInterceptorRequired.java:34)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.intercept(TransactionalInterceptorBase.java:53)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.intercept(TransactionalInterceptorRequired.java:26)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired_Bean.intercept(TransactionalInterceptorRequired_Bean.zig:340)
	at io.quarkus.arc.impl.InterceptorInvocation.invoke(InterceptorInvocation.java:41)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.perform(AroundInvokeInvocationContext.java:41)
	at io.quarkus.arc.impl.InvocationContexts.performAroundInvoke(InvocationContexts.java:32)
	at br.gov.caixa.simpf.service.CalculoContagemService_Subclass.pontuarItensBacklog(CalculoContagemService_Subclass.zig:168)
	at br.gov.caixa.simpf.service.CalculoContagemService_ClientProxy.pontuarItensBacklog(CalculoContagemService_ClientProxy.zig:352)
	at br.gov.caixa.simpf.service.ContagemService.pontuarItensBacklog(ContagemService.java:138)
	at br.gov.caixa.simpf.service.ContagemService_Subclass.pontuarItensBacklog$$superaccessor84(ContagemService_Subclass.zig:13665)
	at br.gov.caixa.simpf.service.ContagemService_Subclass$$function$$84.apply(ContagemService_Subclass$$function$$84.zig:33)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.proceed(AroundInvokeInvocationContext.java:54)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.invokeInOurTx(TransactionalInterceptorBase.java:127)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.invokeInOurTx(TransactionalInterceptorBase.java:100)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.doIntercept(TransactionalInterceptorRequired.java:32)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.intercept(TransactionalInterceptorBase.java:53)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.intercept(TransactionalInterceptorRequired.java:26)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired_Bean.intercept(TransactionalInterceptorRequired_Bean.zig:340)
	at io.quarkus.arc.impl.InterceptorInvocation.invoke(InterceptorInvocation.java:41)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.perform(AroundInvokeInvocationContext.java:41)
	at io.quarkus.arc.impl.InvocationContexts.performAroundInvoke(InvocationContexts.java:32)
	at br.gov.caixa.simpf.service.ContagemService_Subclass.pontuarItensBacklog(ContagemService_Subclass.zig:13622)
	at br.gov.caixa.simpf.service.ContagemService_ClientProxy.pontuarItensBacklog(ContagemService_ClientProxy.zig:1005)
	at br.gov.caixa.simpf.controller.ContagemController.getPontuacaoItensBacklog(ContagemController.java:231)
	at br.gov.caixa.simpf.controller.ContagemController_Subclass.getPontuacaoItensBacklog$$superaccessor6(ContagemController_Subclass.zig:1622)
	at br.gov.caixa.simpf.controller.ContagemController_Subclass$$function$$6.apply(ContagemController_Subclass$$function$$6.zig:33)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.proceed(AroundInvokeInvocationContext.java:54)
	at io.quarkus.security.runtime.interceptor.SecurityHandler.handle(SecurityHandler.java:24)
	at io.quarkus.security.runtime.interceptor.RolesAllowedInterceptor.intercept(RolesAllowedInterceptor.java:29)
	at io.quarkus.security.runtime.interceptor.RolesAllowedInterceptor_Bean.intercept(RolesAllowedInterceptor_Bean.zig:386)
	at io.quarkus.arc.impl.InterceptorInvocation.invoke(InterceptorInvocation.java:41)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.perform(AroundInvokeInvocationContext.java:41)
	at io.quarkus.arc.impl.InvocationContexts.performAroundInvoke(InvocationContexts.java:32)
	at br.gov.caixa.simpf.controller.ContagemController_Subclass.getPontuacaoItensBacklog(ContagemController_Subclass.zig:1579)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:566)
	at org.jboss.resteasy.core.MethodInjectorImpl.invoke(MethodInjectorImpl.java:170)
	at org.jboss.resteasy.core.MethodInjectorImpl.invoke(MethodInjectorImpl.java:130)
	at org.jboss.resteasy.core.ResourceMethodInvoker.internalInvokeOnTarget(ResourceMethodInvoker.java:660)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invokeOnTargetAfterFilter(ResourceMethodInvoker.java:524)
	at org.jboss.resteasy.core.ResourceMethodInvoker.lambda$invokeOnTarget$2(ResourceMethodInvoker.java:474)
	at org.jboss.resteasy.core.interception.jaxrs.PreMatchContainerRequestContext.filter(PreMatchContainerRequestContext.java:364)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invokeOnTarget(ResourceMethodInvoker.java:476)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invoke(ResourceMethodInvoker.java:434)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invoke(ResourceMethodInvoker.java:408)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invoke(ResourceMethodInvoker.java:69)
	at org.jboss.resteasy.core.SynchronousDispatcher.invoke(SynchronousDispatcher.java:492)
	at org.jboss.resteasy.core.SynchronousDispatcher.lambda$invoke$4(SynchronousDispatcher.java:261)
	at org.jboss.resteasy.core.SynchronousDispatcher.lambda$preprocess$0(SynchronousDispatcher.java:161)
	at org.jboss.resteasy.core.interception.jaxrs.PreMatchContainerRequestContext.filter(PreMatchContainerRequestContext.java:364)
	at org.jboss.resteasy.core.SynchronousDispatcher.preprocess(SynchronousDispatcher.java:164)
	at org.jboss.resteasy.core.SynchronousDispatcher.invoke(SynchronousDispatcher.java:247)
	at org.jboss.resteasy.plugins.server.servlet.ServletContainerDispatcher.service(ServletContainerDispatcher.java:249)
	at io.quarkus.resteasy.runtime.ResteasyFilter$ResteasyResponseWrapper.service(ResteasyFilter.java:70)
	at io.quarkus.resteasy.runtime.ResteasyFilter$ResteasyResponseWrapper.sendError(ResteasyFilter.java:76)
	at io.undertow.servlet.handlers.DefaultServlet.doGet(DefaultServlet.java:172)
	at javax.servlet.http.HttpServlet.service(HttpServlet.java:503)
	at javax.servlet.http.HttpServlet.service(HttpServlet.java:590)
	at io.undertow.servlet.handlers.ServletHandler.handleRequest(ServletHandler.java:74)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:129)
	at io.quarkus.resteasy.runtime.ResteasyFilter.doFilter(ResteasyFilter.java:31)
	at io.undertow.servlet.core.ManagedFilter.doFilter(ManagedFilter.java:61)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:131)
	at io.undertow.servlet.handlers.FilterHandler.handleRequest(FilterHandler.java:84)
	at io.undertow.servlet.handlers.security.ServletSecurityRoleHandler.handleRequest(ServletSecurityRoleHandler.java:63)
	at io.undertow.servlet.handlers.ServletChain$1.handleRequest(ServletChain.java:68)
	at io.undertow.servlet.handlers.ServletDispatchingHandler.handleRequest(ServletDispatchingHandler.java:36)
	at io.undertow.servlet.handlers.RedirectDirHandler.handleRequest(RedirectDirHandler.java:67)
	at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
	at io.undertow.servlet.handlers.security.ServletAuthenticationCallHandler.handleRequest(ServletAuthenticationCallHandler.java:57)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.security.handlers.AbstractConfidentialityHandler.handleRequest(AbstractConfidentialityHandler.java:46)
	at io.undertow.servlet.handlers.security.ServletConfidentialityConstraintHandler.handleRequest(ServletConfidentialityConstraintHandler.java:65)
	at io.undertow.security.handlers.AuthenticationMechanismsHandler.handleRequest(AuthenticationMechanismsHandler.java:60)
	at io.undertow.servlet.handlers.security.CachedAuthenticatedSessionHandler.handleRequest(CachedAuthenticatedSessionHandler.java:77)
	at io.undertow.security.handlers.NotificationReceiverHandler.handleRequest(NotificationReceiverHandler.java:50)
	at io.undertow.security.handlers.AbstractSecurityContextAssociationHandler.handleRequest(AbstractSecurityContextAssociationHandler.java:43)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.servlet.handlers.ServletInitialHandler.handleFirstRequest(ServletInitialHandler.java:247)
	at io.undertow.servlet.handlers.ServletInitialHandler.access$100(ServletInitialHandler.java:56)
	at io.undertow.servlet.handlers.ServletInitialHandler$2.call(ServletInitialHandler.java:111)
	at io.undertow.servlet.handlers.ServletInitialHandler$2.call(ServletInitialHandler.java:108)
	at io.undertow.servlet.core.ServletRequestContextThreadSetupAction$1.call(ServletRequestContextThreadSetupAction.java:48)
	at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
	at io.quarkus.undertow.runtime.UndertowDeploymentRecorder$9$1.call(UndertowDeploymentRecorder.java:587)
	at io.undertow.servlet.handlers.ServletInitialHandler.dispatchRequest(ServletInitialHandler.java:227)
	at io.undertow.servlet.handlers.ServletInitialHandler.handleRequest(ServletInitialHandler.java:152)
	at io.quarkus.undertow.runtime.UndertowDeploymentRecorder$1.handleRequest(UndertowDeploymentRecorder.java:119)
	at io.undertow.server.Connectors.executeRootHandler(Connectors.java:290)
	at io.undertow.server.DefaultExchangeHandler.handle(DefaultExchangeHandler.java:18)
	at io.quarkus.undertow.runtime.UndertowDeploymentRecorder$5$1.run(UndertowDeploymentRecorder.java:413)
	at java.base/java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:515)
	at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
	at org.jboss.threads.EnhancedQueueExecutor$Task.run(EnhancedQueueExecutor.java:2415)
	at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.run(EnhancedQueueExecutor.java:1452)
	at org.jboss.threads.DelegatingRunnable.run(DelegatingRunnable.java:29)
	at org.jboss.threads.ThreadLocalResettingRunnable.run(ThreadLocalResettingRunnable.java:29)
	at java.base/java.lang.Thread.run(Thread.java:829)
	at org.jboss.threads.JBossThread.run(JBossThread.java:501)

2026-10-15 16:36:55,925 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogEntity WHERE LOWER(coItemTrabalho) = LOWER(?1), time: 2ms, rows: 1
2026-10-15 16:36:59,349 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  AND (analise.nuVersaoInicial = :nuVersaoInicial)  , time: 71ms, rows: 1
2026-10-15 16:36:59,419 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT analise, em FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  AND (analise.nuVersaoInicial = :nuVersaoInicial)  ORDER BY analise.dataModificacao DESC, time: 70ms, rows: 1
2026-10-15 16:37:01,283 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ServicoEntity, time: 1ms, rows: 0
2026-10-15 16:37:01,289 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuAnaliseImpacto = ?1, time: 5ms, rows: 1
2026-10-15 16:37:01,358 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 2ms, rows: 1
2026-10-15 16:37:01,365 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 2ms, rows: 15
2026-10-15 16:37:01,428 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.StatusServicoEntity, time: 2ms, rows: 7
2026-10-15 16:37:01,678 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.StatusServicoEntity, time: 1ms, rows: 7
2026-10-15 16:37:01,729 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE ativa = 1 and nuVersaoInicial = ?1 ORDER BY nuAnaliseImpacto, time: 5ms, rows: 7
2026-10-15 16:37:01,759 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:01,763 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 2ms, rows: 15
2026-10-15 16:37:01,791 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:01,794 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 15
2026-10-15 16:37:01,817 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:01,820 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 2ms, rows: 15
2026-10-15 16:37:01,843 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:01,847 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 15
2026-10-15 16:37:01,870 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:01,873 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 15
2026-10-15 16:37:01,885 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.DisciplinaArtefatoEntity, time: 11ms, rows: 0
2026-10-15 16:37:01,901 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:01,905 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 2ms, rows: 15
2026-10-15 16:37:01,938 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:01,941 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 2ms, rows: 15
2026-10-15 16:37:02,527 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 6ms, rows: 30
2026-10-15 16:37:02,578 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FuncionalidadeEntity, time: 215ms, rows: 2560
2026-10-15 16:37:02,584 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 2ms, rows: 1
2026-10-15 16:37:02,814 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FluxoEstadoEntity WHERE estadoOrigem.nuEstadoMaquina = ?1, time: 6ms, rows: 1
2026-10-15 16:37:02,966 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 2ms, rows: 2
2026-10-15 16:37:02,969 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1 ORDER BY dataModificacao DESC, time: 4ms, rows: 3
2026-10-15 16:37:02,972 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1, time: 1ms, rows: 1
2026-10-15 16:37:09,318 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 1ms, rows: 2
2026-10-15 16:37:09,696 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 1ms, rows: 2
2026-10-15 16:37:09,893 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuAnaliseImpacto = ?1, time: 4ms, rows: 1
2026-10-15 16:37:09,939 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE itemSistema.nuItemSistema = ?1 and lower(iteracao) = ?2 and lower(siglaSquad) = ?3 and ativa=1, time: 3ms, rows: 8
2026-10-15 16:37:09,943 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 420 ORDER BY id.dataAtualizacao DESC, time: 2ms, rows: 1
2026-10-15 16:37:09,945 INFO  [br.gov.cai.sim.ser.AnaliseImpactoService] (executor-thread-6) Maquina de estado padronizado para Cancelado
2026-10-15 16:37:09,947 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 1ms, rows: 2
2026-10-15 16:37:09,959 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogEntity WHERE nuItemBacklogRequisito = ?1, time: 1ms, rows: 1
WARNING: An illegal reflective access operation has occurred
WARNING: Illegal reflective access by br.gov.caixa.simpf.service.LogService (file:/deployments/app/SIMPF-3.13.0.5.jar) to field java.lang.Long.value
WARNING: Please consider reporting this to the maintainers of br.gov.caixa.simpf.service.LogService
WARNING: Use --illegal-access=warn to enable warnings of further illegal reflective access operations
WARNING: All illegal access operations will be denied in a future release
2026-10-15 16:37:09,973 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogImpactadoEntity WHERE NU_ANALISE_IMPACTO=:idAnaliseImpacto and NU_ITEM_BACKLOG=:idItemBacklog, time: 1ms, rows: 1
2026-10-15 16:37:09,999 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:10,002 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuVersaoInicial = ?1, time: 1ms, rows: 7
2026-10-15 16:37:10,141 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuAnaliseImpacto = ?1, time: 4ms, rows: 1
2026-10-15 16:37:10,178 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:10,181 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 16
2026-10-15 16:37:10,384 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE ativa = 1 and nuVersaoInicial = ?1 ORDER BY nuAnaliseImpacto, time: 5ms, rows: 7
2026-10-15 16:37:10,409 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:10,414 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 16
2026-10-15 16:37:10,440 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:10,442 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 16
2026-10-15 16:37:10,467 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:10,469 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 16
2026-10-15 16:37:10,493 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:10,495 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 16
2026-10-15 16:37:10,518 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:10,523 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 3ms, rows: 16
2026-10-15 16:37:10,544 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:10,547 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 16
2026-10-15 16:37:10,569 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:10,572 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 16
2026-10-15 16:37:11,107 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 5ms, rows: 30
2026-10-15 16:37:11,145 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FuncionalidadeEntity, time: 190ms, rows: 2560
2026-10-15 16:37:11,152 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 1ms, rows: 1
2026-10-15 16:37:11,487 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FluxoEstadoEntity WHERE estadoOrigem.nuEstadoMaquina = ?1, time: 3ms, rows: 1
2026-10-15 16:37:11,624 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1 ORDER BY dataModificacao DESC, time: 3ms, rows: 3
2026-10-15 16:37:11,627 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1, time: 2ms, rows: 1
2026-10-15 16:37:11,631 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 2
2026-10-15 16:37:14,684 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 2
2026-10-15 16:37:15,070 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 1ms, rows: 2
2026-10-15 16:37:15,257 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuAnaliseImpacto = ?1, time: 4ms, rows: 1
2026-10-15 16:37:15,282 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 1ms, rows: 2
2026-10-15 16:37:15,305 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogEntity WHERE nuItemBacklogRequisito = ?1, time: 1ms, rows: 1
2026-10-15 16:37:15,307 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogImpactadoEntity WHERE NU_ANALISE_IMPACTO=:idAnaliseImpacto and NU_ITEM_BACKLOG=:idItemBacklog, time: 0ms, rows: 0
2026-10-15 16:37:15,318 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogEntity WHERE nuItemBacklogRequisito = ?1, time: 1ms, rows: 1
2026-10-15 16:37:15,320 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogImpactadoEntity WHERE NU_ANALISE_IMPACTO=:idAnaliseImpacto and NU_ITEM_BACKLOG=:idItemBacklog, time: 0ms, rows: 1
2026-10-15 16:37:15,361 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogImpactadoEntity WHERE NU_ANALISE_IMPACTO=:idAnaliseImpacto and NU_ITEM_BACKLOG=:idItemBacklog, time: 0ms, rows: 1
2026-10-15 16:37:15,371 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogImpactadoEntity WHERE NU_ANALISE_IMPACTO=:idAnaliseImpacto and NU_ITEM_BACKLOG=:idItemBacklog, time: 0ms, rows: 1
2026-10-15 16:37:15,423 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuAnaliseImpacto = ?1, time: 0ms, rows: 1
2026-10-15 16:37:15,454 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogEntity WHERE nuItemBacklogRequisito = ?1, time: 0ms, rows: 1
2026-10-15 16:37:15,456 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogImpactadoEntity WHERE NU_ANALISE_IMPACTO=:idAnaliseImpacto and NU_ITEM_BACKLOG=:idItemBacklog, time: 0ms, rows: 1
2026-10-15 16:37:15,461 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:15,463 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuVersaoInicial = ?1, time: 1ms, rows: 8
2026-10-15 16:37:15,604 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuAnaliseImpacto = ?1, time: 4ms, rows: 1
2026-10-15 16:37:15,642 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:15,646 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 2ms, rows: 17
2026-10-15 16:37:15,855 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE ativa = 1 and nuVersaoInicial = ?1 ORDER BY nuAnaliseImpacto, time: 4ms, rows: 8
2026-10-15 16:37:15,880 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:15,884 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:37:15,923 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:15,926 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:37:15,948 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:15,950 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:37:15,975 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:15,977 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:37:15,999 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:16,002 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:37:16,025 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:16,028 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 2ms, rows: 17
2026-10-15 16:37:16,049 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:16,051 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:37:16,073 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:37:16,075 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:37:16,589 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 5ms, rows: 30
2026-10-15 16:37:16,613 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FuncionalidadeEntity, time: 164ms, rows: 2560
2026-10-15 16:37:16,628 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 0ms, rows: 1
2026-10-15 16:37:16,905 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FluxoEstadoEntity WHERE estadoOrigem.nuEstadoMaquina = ?1, time: 3ms, rows: 1
2026-10-15 16:37:17,041 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 1ms, rows: 2
2026-10-15 16:37:17,055 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1 ORDER BY dataModificacao DESC, time: 2ms, rows: 3
2026-10-15 16:37:17,056 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1, time: 0ms, rows: 1
2026-10-15 16:38:45,832 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  AND (analise.nuVersaoInicial = :nuVersaoInicial)  , time: 5ms, rows: 1
2026-10-15 16:38:45,839 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT analise, em FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  AND (analise.nuVersaoInicial = :nuVersaoInicial)  ORDER BY analise.dataModificacao DESC, time: 6ms, rows: 1
2026-10-15 16:38:54,334 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ServicoEntity, time: 1ms, rows: 0
2026-10-15 16:38:54,464 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.StatusServicoEntity, time: 1ms, rows: 7
2026-10-15 16:38:54,535 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.StatusServicoEntity, time: 1ms, rows: 7
2026-10-15 16:38:54,723 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.DisciplinaArtefatoEntity, time: 3ms, rows: 0
2026-10-15 16:38:56,842 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL) AND (ae.id.estadoMaquina.nuEstadoMaquina = :nuEstadoMaquina OR :nuEstadoMaquina IS NULL)  AND analise.contrato.tipoContrato.nuTipoContrato like '%'||:nuTipoContrato||'%' , time: 58ms, rows: 1
2026-10-15 16:38:56,925 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT analise, em FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL) AND (ae.id.estadoMaquina.nuEstadoMaquina = :nuEstadoMaquina OR :nuEstadoMaquina IS NULL)  AND analise.contrato.tipoContrato.nuTipoContrato like '%'||:nuTipoContrato||'%' ORDER BY analise.dataModificacao DESC, time: 82ms, rows: 1
2026-10-15 16:38:59,208 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  , time: 315ms, rows: 1
2026-10-15 16:38:59,526 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT analise, em FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  ORDER BY analise.dataModificacao DESC, time: 317ms, rows: 30
2026-10-15 16:38:59,809 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ContagemSNAPEntity WHERE nuContagemDadosSnap IN (:ids_0, :ids_1), time: 0ms, rows: 2
2026-10-15 16:38:59,815 WARNING [br.gov.cai.sim.ser.sip.ItemTrabalhoService] (executor-thread-2) Fluxo Simplifica indispon?vel para o item informado. Aplicando fallback interno.: java.lang.UnsupportedOperationException: Consulta ao Simplifica n?o implementada ainda.
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService.consultarSimplifica(ItemTrabalhoService.java:91)
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService.buscarComFallbackSimplifica(ItemTrabalhoService.java:68)
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService.findHistoriaUsuarioById(ItemTrabalhoService.java:56)
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService_ClientProxy.findHistoriaUsuarioById(ItemTrabalhoService_ClientProxy.zig:157)
	at br.gov.caixa.simpf.service.CalculoContagemService.getListaItemBacklogRTC(CalculoContagemService.java:239)
	at br.gov.caixa.simpf.service.CalculoContagemService.pontuarItensBacklog(CalculoContagemService.java:206)
	at br.gov.caixa.simpf.service.CalculoContagemService_Subclass.pontuarItensBacklog$$superaccessor1(CalculoContagemService_Subclass.zig:211)
	at br.gov.caixa.simpf.service.CalculoContagemService_Subclass$$function$$1.apply(CalculoContagemService_Subclass$$function$$1.zig:33)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.proceed(AroundInvokeInvocationContext.java:54)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.invokeInCallerTx(TransactionalInterceptorBase.java:252)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.doIntercept(TransactionalInterceptorRequired.java:34)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.intercept(TransactionalInterceptorBase.java:53)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.intercept(TransactionalInterceptorRequired.java:26)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired_Bean.intercept(TransactionalInterceptorRequired_Bean.zig:340)
	at io.quarkus.arc.impl.InterceptorInvocation.invoke(InterceptorInvocation.java:41)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.perform(AroundInvokeInvocationContext.java:41)
	at io.quarkus.arc.impl.InvocationContexts.performAroundInvoke(InvocationContexts.java:32)
	at br.gov.caixa.simpf.service.CalculoContagemService_Subclass.pontuarItensBacklog(CalculoContagemService_Subclass.zig:168)
	at br.gov.caixa.simpf.service.CalculoContagemService_ClientProxy.pontuarItensBacklog(CalculoContagemService_ClientProxy.zig:352)
	at br.gov.caixa.simpf.service.ContagemService.pontuarItensBacklog(ContagemService.java:138)
	at br.gov.caixa.simpf.service.ContagemService_Subclass.pontuarItensBacklog$$superaccessor84(ContagemService_Subclass.zig:13665)
	at br.gov.caixa.simpf.service.ContagemService_Subclass$$function$$84.apply(ContagemService_Subclass$$function$$84.zig:33)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.proceed(AroundInvokeInvocationContext.java:54)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.invokeInOurTx(TransactionalInterceptorBase.java:127)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.invokeInOurTx(TransactionalInterceptorBase.java:100)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.doIntercept(TransactionalInterceptorRequired.java:32)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.intercept(TransactionalInterceptorBase.java:53)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.intercept(TransactionalInterceptorRequired.java:26)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired_Bean.intercept(TransactionalInterceptorRequired_Bean.zig:340)
	at io.quarkus.arc.impl.InterceptorInvocation.invoke(InterceptorInvocation.java:41)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.perform(AroundInvokeInvocationContext.java:41)
	at io.quarkus.arc.impl.InvocationContexts.performAroundInvoke(InvocationContexts.java:32)
	at br.gov.caixa.simpf.service.ContagemService_Subclass.pontuarItensBacklog(ContagemService_Subclass.zig:13622)
	at br.gov.caixa.simpf.service.ContagemService_ClientProxy.pontuarItensBacklog(ContagemService_ClientProxy.zig:1005)
	at br.gov.caixa.simpf.controller.ContagemController.getPontuacaoItensBacklog(ContagemController.java:231)
	at br.gov.caixa.simpf.controller.ContagemController_Subclass.getPontuacaoItensBacklog$$superaccessor6(ContagemController_Subclass.zig:1622)
	at br.gov.caixa.simpf.controller.ContagemController_Subclass$$function$$6.apply(ContagemController_Subclass$$function$$6.zig:33)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.proceed(AroundInvokeInvocationContext.java:54)
	at io.quarkus.security.runtime.interceptor.SecurityHandler.handle(SecurityHandler.java:24)
	at io.quarkus.security.runtime.interceptor.RolesAllowedInterceptor.intercept(RolesAllowedInterceptor.java:29)
	at io.quarkus.security.runtime.interceptor.RolesAllowedInterceptor_Bean.intercept(RolesAllowedInterceptor_Bean.zig:386)
	at io.quarkus.arc.impl.InterceptorInvocation.invoke(InterceptorInvocation.java:41)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.perform(AroundInvokeInvocationContext.java:41)
	at io.quarkus.arc.impl.InvocationContexts.performAroundInvoke(InvocationContexts.java:32)
	at br.gov.caixa.simpf.controller.ContagemController_Subclass.getPontuacaoItensBacklog(ContagemController_Subclass.zig:1579)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:566)
	at org.jboss.resteasy.core.MethodInjectorImpl.invoke(MethodInjectorImpl.java:170)
	at org.jboss.resteasy.core.MethodInjectorImpl.invoke(MethodInjectorImpl.java:130)
	at org.jboss.resteasy.core.ResourceMethodInvoker.internalInvokeOnTarget(ResourceMethodInvoker.java:660)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invokeOnTargetAfterFilter(ResourceMethodInvoker.java:524)
	at org.jboss.resteasy.core.ResourceMethodInvoker.lambda$invokeOnTarget$2(ResourceMethodInvoker.java:474)
	at org.jboss.resteasy.core.interception.jaxrs.PreMatchContainerRequestContext.filter(PreMatchContainerRequestContext.java:364)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invokeOnTarget(ResourceMethodInvoker.java:476)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invoke(ResourceMethodInvoker.java:434)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invoke(ResourceMethodInvoker.java:408)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invoke(ResourceMethodInvoker.java:69)
	at org.jboss.resteasy.core.SynchronousDispatcher.invoke(SynchronousDispatcher.java:492)
	at org.jboss.resteasy.core.SynchronousDispatcher.lambda$invoke$4(SynchronousDispatcher.java:261)
	at org.jboss.resteasy.core.SynchronousDispatcher.lambda$preprocess$0(SynchronousDispatcher.java:161)
	at org.jboss.resteasy.core.interception.jaxrs.PreMatchContainerRequestContext.filter(PreMatchContainerRequestContext.java:364)
	at org.jboss.resteasy.core.SynchronousDispatcher.preprocess(SynchronousDispatcher.java:164)
	at org.jboss.resteasy.core.SynchronousDispatcher.invoke(SynchronousDispatcher.java:247)
	at org.jboss.resteasy.plugins.server.servlet.ServletContainerDispatcher.service(ServletContainerDispatcher.java:249)
	at io.quarkus.resteasy.runtime.ResteasyFilter$ResteasyResponseWrapper.service(ResteasyFilter.java:70)
	at io.quarkus.resteasy.runtime.ResteasyFilter$ResteasyResponseWrapper.sendError(ResteasyFilter.java:76)
	at io.undertow.servlet.handlers.DefaultServlet.doGet(DefaultServlet.java:172)
	at javax.servlet.http.HttpServlet.service(HttpServlet.java:503)
	at javax.servlet.http.HttpServlet.service(HttpServlet.java:590)
	at io.undertow.servlet.handlers.ServletHandler.handleRequest(ServletHandler.java:74)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:129)
	at io.quarkus.resteasy.runtime.ResteasyFilter.doFilter(ResteasyFilter.java:31)
	at io.undertow.servlet.core.ManagedFilter.doFilter(ManagedFilter.java:61)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:131)
	at io.undertow.servlet.handlers.FilterHandler.handleRequest(FilterHandler.java:84)
	at io.undertow.servlet.handlers.security.ServletSecurityRoleHandler.handleRequest(ServletSecurityRoleHandler.java:63)
	at io.undertow.servlet.handlers.ServletChain$1.handleRequest(ServletChain.java:68)
	at io.undertow.servlet.handlers.ServletDispatchingHandler.handleRequest(ServletDispatchingHandler.java:36)
	at io.undertow.servlet.handlers.RedirectDirHandler.handleRequest(RedirectDirHandler.java:67)
	at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
	at io.undertow.servlet.handlers.security.ServletAuthenticationCallHandler.handleRequest(ServletAuthenticationCallHandler.java:57)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.security.handlers.AbstractConfidentialityHandler.handleRequest(AbstractConfidentialityHandler.java:46)
	at io.undertow.servlet.handlers.security.ServletConfidentialityConstraintHandler.handleRequest(ServletConfidentialityConstraintHandler.java:65)
	at io.undertow.security.handlers.AuthenticationMechanismsHandler.handleRequest(AuthenticationMechanismsHandler.java:60)
	at io.undertow.servlet.handlers.security.CachedAuthenticatedSessionHandler.handleRequest(CachedAuthenticatedSessionHandler.java:77)
	at io.undertow.security.handlers.NotificationReceiverHandler.handleRequest(NotificationReceiverHandler.java:50)
	at io.undertow.security.handlers.AbstractSecurityContextAssociationHandler.handleRequest(AbstractSecurityContextAssociationHandler.java:43)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.servlet.handlers.ServletInitialHandler.handleFirstRequest(ServletInitialHandler.java:247)
	at io.undertow.servlet.handlers.ServletInitialHandler.access$100(ServletInitialHandler.java:56)
	at io.undertow.servlet.handlers.ServletInitialHandler$2.call(ServletInitialHandler.java:111)
	at io.undertow.servlet.handlers.ServletInitialHandler$2.call(ServletInitialHandler.java:108)
	at io.undertow.servlet.core.ServletRequestContextThreadSetupAction$1.call(ServletRequestContextThreadSetupAction.java:48)
	at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
	at io.quarkus.undertow.runtime.UndertowDeploymentRecorder$9$1.call(UndertowDeploymentRecorder.java:587)
	at io.undertow.servlet.handlers.ServletInitialHandler.dispatchRequest(ServletInitialHandler.java:227)
	at io.undertow.servlet.handlers.ServletInitialHandler.handleRequest(ServletInitialHandler.java:152)
	at io.quarkus.undertow.runtime.UndertowDeploymentRecorder$1.handleRequest(UndertowDeploymentRecorder.java:119)
	at io.undertow.server.Connectors.executeRootHandler(Connectors.java:290)
	at io.undertow.server.DefaultExchangeHandler.handle(DefaultExchangeHandler.java:18)
	at io.quarkus.undertow.runtime.UndertowDeploymentRecorder$5$1.run(UndertowDeploymentRecorder.java:413)
	at java.base/java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:515)
	at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
	at org.jboss.threads.EnhancedQueueExecutor$Task.run(EnhancedQueueExecutor.java:2415)
	at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.run(EnhancedQueueExecutor.java:1452)
	at org.jboss.threads.DelegatingRunnable.run(DelegatingRunnable.java:29)
	at org.jboss.threads.ThreadLocalResettingRunnable.run(ThreadLocalResettingRunnable.java:29)
	at java.base/java.lang.Thread.run(Thread.java:829)
	at org.jboss.threads.JBossThread.run(JBossThread.java:501)

2026-10-15 16:38:59,817 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogEntity WHERE LOWER(coItemTrabalho) = LOWER(?1), time: 1ms, rows: 1
2026-10-15 16:39:02,168 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ServicoEntity, time: 1ms, rows: 0
2026-10-15 16:39:02,171 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuAnaliseImpacto = ?1, time: 4ms, rows: 1
2026-10-15 16:39:02,214 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 977 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:02,217 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 977 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 3
2026-10-15 16:39:02,306 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.StatusServicoEntity, time: 1ms, rows: 7
2026-10-15 16:39:02,368 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE ativa = 1 and nuVersaoInicial = ?1 ORDER BY nuAnaliseImpacto, time: 4ms, rows: 2
2026-10-15 16:39:02,372 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.StatusServicoEntity, time: 1ms, rows: 7
2026-10-15 16:39:02,401 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 977 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:02,403 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 977 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 3
2026-10-15 16:39:02,432 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 977 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:02,434 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 977 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 3
2026-10-15 16:39:02,555 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.DisciplinaArtefatoEntity, time: 1ms, rows: 0
2026-10-15 16:39:02,803 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 5ms, rows: 30
2026-10-15 16:39:02,836 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 0ms, rows: 1
2026-10-15 16:39:02,877 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FuncionalidadeEntity, time: 193ms, rows: 2560
2026-10-15 16:39:03,080 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FluxoEstadoEntity WHERE estadoOrigem.nuEstadoMaquina = ?1, time: 4ms, rows: 2
2026-10-15 16:39:03,214 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 2ms, rows: 3
2026-10-15 16:39:03,222 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1 ORDER BY dataModificacao DESC, time: 3ms, rows: 3
2026-10-15 16:39:03,222 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1 ORDER BY dataModificacao DESC, time: 3ms, rows: 3
2026-10-15 16:39:03,223 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1, time: 0ms, rows: 1
2026-10-15 16:39:03,223 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1, time: 0ms, rows: 1
2026-10-15 16:39:03,474 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 1ms, rows: 1
2026-10-15 16:39:05,397 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  , time: 327ms, rows: 1
2026-10-15 16:39:05,761 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT analise, em FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  ORDER BY analise.dataModificacao DESC, time: 363ms, rows: 30
2026-10-15 16:39:06,029 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ContagemSNAPEntity WHERE nuContagemDadosSnap IN (:ids_0, :ids_1), time: 0ms, rows: 2
2026-10-15 16:39:06,033 WARNING [br.gov.cai.sim.ser.sip.ItemTrabalhoService] (executor-thread-2) Fluxo Simplifica indispon?vel para o item informado. Aplicando fallback interno.: java.lang.UnsupportedOperationException: Consulta ao Simplifica n?o implementada ainda.
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService.consultarSimplifica(ItemTrabalhoService.java:91)
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService.buscarComFallbackSimplifica(ItemTrabalhoService.java:68)
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService.findHistoriaUsuarioById(ItemTrabalhoService.java:56)
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService_ClientProxy.findHistoriaUsuarioById(ItemTrabalhoService_ClientProxy.zig:157)
	at br.gov.caixa.simpf.service.CalculoContagemService.getListaItemBacklogRTC(CalculoContagemService.java:239)
	at br.gov.caixa.simpf.service.CalculoContagemService.pontuarItensBacklog(CalculoContagemService.java:206)
	at br.gov.caixa.simpf.service.CalculoContagemService_Subclass.pontuarItensBacklog$$superaccessor1(CalculoContagemService_Subclass.zig:211)
	at br.gov.caixa.simpf.service.CalculoContagemService_Subclass$$function$$1.apply(CalculoContagemService_Subclass$$function$$1.zig:33)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.proceed(AroundInvokeInvocationContext.java:54)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.invokeInCallerTx(TransactionalInterceptorBase.java:252)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.doIntercept(TransactionalInterceptorRequired.java:34)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.intercept(TransactionalInterceptorBase.java:53)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.intercept(TransactionalInterceptorRequired.java:26)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired_Bean.intercept(TransactionalInterceptorRequired_Bean.zig:340)
	at io.quarkus.arc.impl.InterceptorInvocation.invoke(InterceptorInvocation.java:41)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.perform(AroundInvokeInvocationContext.java:41)
	at io.quarkus.arc.impl.InvocationContexts.performAroundInvoke(InvocationContexts.java:32)
	at br.gov.caixa.simpf.service.CalculoContagemService_Subclass.pontuarItensBacklog(CalculoContagemService_Subclass.zig:168)
	at br.gov.caixa.simpf.service.CalculoContagemService_ClientProxy.pontuarItensBacklog(CalculoContagemService_ClientProxy.zig:352)
	at br.gov.caixa.simpf.service.ContagemService.pontuarItensBacklog(ContagemService.java:138)
	at br.gov.caixa.simpf.service.ContagemService_Subclass.pontuarItensBacklog$$superaccessor84(ContagemService_Subclass.zig:13665)
	at br.gov.caixa.simpf.service.ContagemService_Subclass$$function$$84.apply(ContagemService_Subclass$$function$$84.zig:33)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.proceed(AroundInvokeInvocationContext.java:54)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.invokeInOurTx(TransactionalInterceptorBase.java:127)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.invokeInOurTx(TransactionalInterceptorBase.java:100)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.doIntercept(TransactionalInterceptorRequired.java:32)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.intercept(TransactionalInterceptorBase.java:53)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.intercept(TransactionalInterceptorRequired.java:26)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired_Bean.intercept(TransactionalInterceptorRequired_Bean.zig:340)
	at io.quarkus.arc.impl.InterceptorInvocation.invoke(InterceptorInvocation.java:41)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.perform(AroundInvokeInvocationContext.java:41)
	at io.quarkus.arc.impl.InvocationContexts.performAroundInvoke(InvocationContexts.java:32)
	at br.gov.caixa.simpf.service.ContagemService_Subclass.pontuarItensBacklog(ContagemService_Subclass.zig:13622)
	at br.gov.caixa.simpf.service.ContagemService_ClientProxy.pontuarItensBacklog(ContagemService_ClientProxy.zig:1005)
	at br.gov.caixa.simpf.controller.ContagemController.getPontuacaoItensBacklog(ContagemController.java:231)
	at br.gov.caixa.simpf.controller.ContagemController_Subclass.getPontuacaoItensBacklog$$superaccessor6(ContagemController_Subclass.zig:1622)
	at br.gov.caixa.simpf.controller.ContagemController_Subclass$$function$$6.apply(ContagemController_Subclass$$function$$6.zig:33)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.proceed(AroundInvokeInvocationContext.java:54)
	at io.quarkus.security.runtime.interceptor.SecurityHandler.handle(SecurityHandler.java:24)
	at io.quarkus.security.runtime.interceptor.RolesAllowedInterceptor.intercept(RolesAllowedInterceptor.java:29)
	at io.quarkus.security.runtime.interceptor.RolesAllowedInterceptor_Bean.intercept(RolesAllowedInterceptor_Bean.zig:386)
	at io.quarkus.arc.impl.InterceptorInvocation.invoke(InterceptorInvocation.java:41)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.perform(AroundInvokeInvocationContext.java:41)
	at io.quarkus.arc.impl.InvocationContexts.performAroundInvoke(InvocationContexts.java:32)
	at br.gov.caixa.simpf.controller.ContagemController_Subclass.getPontuacaoItensBacklog(ContagemController_Subclass.zig:1579)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:566)
	at org.jboss.resteasy.core.MethodInjectorImpl.invoke(MethodInjectorImpl.java:170)
	at org.jboss.resteasy.core.MethodInjectorImpl.invoke(MethodInjectorImpl.java:130)
	at org.jboss.resteasy.core.ResourceMethodInvoker.internalInvokeOnTarget(ResourceMethodInvoker.java:660)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invokeOnTargetAfterFilter(ResourceMethodInvoker.java:524)
	at org.jboss.resteasy.core.ResourceMethodInvoker.lambda$invokeOnTarget$2(ResourceMethodInvoker.java:474)
	at org.jboss.resteasy.core.interception.jaxrs.PreMatchContainerRequestContext.filter(PreMatchContainerRequestContext.java:364)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invokeOnTarget(ResourceMethodInvoker.java:476)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invoke(ResourceMethodInvoker.java:434)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invoke(ResourceMethodInvoker.java:408)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invoke(ResourceMethodInvoker.java:69)
	at org.jboss.resteasy.core.SynchronousDispatcher.invoke(SynchronousDispatcher.java:492)
	at org.jboss.resteasy.core.SynchronousDispatcher.lambda$invoke$4(SynchronousDispatcher.java:261)
	at org.jboss.resteasy.core.SynchronousDispatcher.lambda$preprocess$0(SynchronousDispatcher.java:161)
	at org.jboss.resteasy.core.interception.jaxrs.PreMatchContainerRequestContext.filter(PreMatchContainerRequestContext.java:364)
	at org.jboss.resteasy.core.SynchronousDispatcher.preprocess(SynchronousDispatcher.java:164)
	at org.jboss.resteasy.core.SynchronousDispatcher.invoke(SynchronousDispatcher.java:247)
	at org.jboss.resteasy.plugins.server.servlet.ServletContainerDispatcher.service(ServletContainerDispatcher.java:249)
	at io.quarkus.resteasy.runtime.ResteasyFilter$ResteasyResponseWrapper.service(ResteasyFilter.java:70)
	at io.quarkus.resteasy.runtime.ResteasyFilter$ResteasyResponseWrapper.sendError(ResteasyFilter.java:76)
	at io.undertow.servlet.handlers.DefaultServlet.doGet(DefaultServlet.java:172)
	at javax.servlet.http.HttpServlet.service(HttpServlet.java:503)
	at javax.servlet.http.HttpServlet.service(HttpServlet.java:590)
	at io.undertow.servlet.handlers.ServletHandler.handleRequest(ServletHandler.java:74)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:129)
	at io.quarkus.resteasy.runtime.ResteasyFilter.doFilter(ResteasyFilter.java:31)
	at io.undertow.servlet.core.ManagedFilter.doFilter(ManagedFilter.java:61)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:131)
	at io.undertow.servlet.handlers.FilterHandler.handleRequest(FilterHandler.java:84)
	at io.undertow.servlet.handlers.security.ServletSecurityRoleHandler.handleRequest(ServletSecurityRoleHandler.java:63)
	at io.undertow.servlet.handlers.ServletChain$1.handleRequest(ServletChain.java:68)
	at io.undertow.servlet.handlers.ServletDispatchingHandler.handleRequest(ServletDispatchingHandler.java:36)
	at io.undertow.servlet.handlers.RedirectDirHandler.handleRequest(RedirectDirHandler.java:67)
	at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
	at io.undertow.servlet.handlers.security.ServletAuthenticationCallHandler.handleRequest(ServletAuthenticationCallHandler.java:57)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.security.handlers.AbstractConfidentialityHandler.handleRequest(AbstractConfidentialityHandler.java:46)
	at io.undertow.servlet.handlers.security.ServletConfidentialityConstraintHandler.handleRequest(ServletConfidentialityConstraintHandler.java:65)
	at io.undertow.security.handlers.AuthenticationMechanismsHandler.handleRequest(AuthenticationMechanismsHandler.java:60)
	at io.undertow.servlet.handlers.security.CachedAuthenticatedSessionHandler.handleRequest(CachedAuthenticatedSessionHandler.java:77)
	at io.undertow.security.handlers.NotificationReceiverHandler.handleRequest(NotificationReceiverHandler.java:50)
	at io.undertow.security.handlers.AbstractSecurityContextAssociationHandler.handleRequest(AbstractSecurityContextAssociationHandler.java:43)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.servlet.handlers.ServletInitialHandler.handleFirstRequest(ServletInitialHandler.java:247)
	at io.undertow.servlet.handlers.ServletInitialHandler.access$100(ServletInitialHandler.java:56)
	at io.undertow.servlet.handlers.ServletInitialHandler$2.call(ServletInitialHandler.java:111)
	at io.undertow.servlet.handlers.ServletInitialHandler$2.call(ServletInitialHandler.java:108)
	at io.undertow.servlet.core.ServletRequestContextThreadSetupAction$1.call(ServletRequestContextThreadSetupAction.java:48)
	at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
	at io.quarkus.undertow.runtime.UndertowDeploymentRecorder$9$1.call(UndertowDeploymentRecorder.java:587)
	at io.undertow.servlet.handlers.ServletInitialHandler.dispatchRequest(ServletInitialHandler.java:227)
	at io.undertow.servlet.handlers.ServletInitialHandler.handleRequest(ServletInitialHandler.java:152)
	at io.quarkus.undertow.runtime.UndertowDeploymentRecorder$1.handleRequest(UndertowDeploymentRecorder.java:119)
	at io.undertow.server.Connectors.executeRootHandler(Connectors.java:290)
	at io.undertow.server.DefaultExchangeHandler.handle(DefaultExchangeHandler.java:18)
	at io.quarkus.undertow.runtime.UndertowDeploymentRecorder$5$1.run(UndertowDeploymentRecorder.java:413)
	at java.base/java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:515)
	at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
	at org.jboss.threads.EnhancedQueueExecutor$Task.run(EnhancedQueueExecutor.java:2415)
	at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.run(EnhancedQueueExecutor.java:1452)
	at org.jboss.threads.DelegatingRunnable.run(DelegatingRunnable.java:29)
	at org.jboss.threads.ThreadLocalResettingRunnable.run(ThreadLocalResettingRunnable.java:29)
	at java.base/java.lang.Thread.run(Thread.java:829)
	at org.jboss.threads.JBossThread.run(JBossThread.java:501)

2026-10-15 16:39:06,035 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogEntity WHERE LOWER(coItemTrabalho) = LOWER(?1), time: 0ms, rows: 1
2026-10-15 16:39:07,492 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ServicoEntity, time: 1ms, rows: 0
2026-10-15 16:39:07,495 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuAnaliseImpacto = ?1, time: 3ms, rows: 1
2026-10-15 16:39:07,534 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 3ms, rows: 1
2026-10-15 16:39:07,538 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:39:07,624 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.StatusServicoEntity, time: 1ms, rows: 7
2026-10-15 16:39:07,694 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.StatusServicoEntity, time: 1ms, rows: 7
2026-10-15 16:39:07,748 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE ativa = 1 and nuVersaoInicial = ?1 ORDER BY nuAnaliseImpacto, time: 3ms, rows: 8
2026-10-15 16:39:07,770 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:07,773 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:39:07,800 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:07,802 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:39:07,822 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 0ms, rows: 1
2026-10-15 16:39:07,824 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:39:07,845 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:07,847 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:39:07,869 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:07,871 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:39:07,885 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.DisciplinaArtefatoEntity, time: 1ms, rows: 0
2026-10-15 16:39:07,894 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:07,897 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:39:07,924 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:07,926 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:39:07,950 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:07,953 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 935 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 17
2026-10-15 16:39:08,414 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 5ms, rows: 30
2026-10-15 16:39:08,449 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 0ms, rows: 1
2026-10-15 16:39:08,593 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FuncionalidadeEntity, time: 163ms, rows: 2560
2026-10-15 16:39:08,946 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FluxoEstadoEntity WHERE estadoOrigem.nuEstadoMaquina = ?1, time: 2ms, rows: 1
2026-10-15 16:39:09,082 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 1ms, rows: 2
2026-10-15 16:39:09,084 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1 ORDER BY dataModificacao DESC, time: 2ms, rows: 3
2026-10-15 16:39:09,085 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1, time: 0ms, rows: 1
2026-10-15 16:39:13,672 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  , time: 328ms, rows: 1
2026-10-15 16:39:14,005 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT analise, em FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  ORDER BY analise.dataModificacao DESC, time: 332ms, rows: 30
2026-10-15 16:39:14,421 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ContagemSNAPEntity WHERE nuContagemDadosSnap IN (:ids_0, :ids_1), time: 0ms, rows: 2
2026-10-15 16:39:14,425 WARNING [br.gov.cai.sim.ser.sip.ItemTrabalhoService] (executor-thread-2) Fluxo Simplifica indispon?vel para o item informado. Aplicando fallback interno.: java.lang.UnsupportedOperationException: Consulta ao Simplifica n?o implementada ainda.
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService.consultarSimplifica(ItemTrabalhoService.java:91)
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService.buscarComFallbackSimplifica(ItemTrabalhoService.java:68)
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService.findHistoriaUsuarioById(ItemTrabalhoService.java:56)
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService_ClientProxy.findHistoriaUsuarioById(ItemTrabalhoService_ClientProxy.zig:157)
	at br.gov.caixa.simpf.service.CalculoContagemService.getListaItemBacklogRTC(CalculoContagemService.java:239)
	at br.gov.caixa.simpf.service.CalculoContagemService.pontuarItensBacklog(CalculoContagemService.java:206)
	at br.gov.caixa.simpf.service.CalculoContagemService_Subclass.pontuarItensBacklog$$superaccessor1(CalculoContagemService_Subclass.zig:211)
	at br.gov.caixa.simpf.service.CalculoContagemService_Subclass$$function$$1.apply(CalculoContagemService_Subclass$$function$$1.zig:33)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.proceed(AroundInvokeInvocationContext.java:54)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.invokeInCallerTx(TransactionalInterceptorBase.java:252)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.doIntercept(TransactionalInterceptorRequired.java:34)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.intercept(TransactionalInterceptorBase.java:53)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.intercept(TransactionalInterceptorRequired.java:26)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired_Bean.intercept(TransactionalInterceptorRequired_Bean.zig:340)
	at io.quarkus.arc.impl.InterceptorInvocation.invoke(InterceptorInvocation.java:41)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.perform(AroundInvokeInvocationContext.java:41)
	at io.quarkus.arc.impl.InvocationContexts.performAroundInvoke(InvocationContexts.java:32)
	at br.gov.caixa.simpf.service.CalculoContagemService_Subclass.pontuarItensBacklog(CalculoContagemService_Subclass.zig:168)
	at br.gov.caixa.simpf.service.CalculoContagemService_ClientProxy.pontuarItensBacklog(CalculoContagemService_ClientProxy.zig:352)
	at br.gov.caixa.simpf.service.ContagemService.pontuarItensBacklog(ContagemService.java:138)
	at br.gov.caixa.simpf.service.ContagemService_Subclass.pontuarItensBacklog$$superaccessor84(ContagemService_Subclass.zig:13665)
	at br.gov.caixa.simpf.service.ContagemService_Subclass$$function$$84.apply(ContagemService_Subclass$$function$$84.zig:33)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.proceed(AroundInvokeInvocationContext.java:54)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.invokeInOurTx(TransactionalInterceptorBase.java:127)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.invokeInOurTx(TransactionalInterceptorBase.java:100)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.doIntercept(TransactionalInterceptorRequired.java:32)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.intercept(TransactionalInterceptorBase.java:53)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.intercept(TransactionalInterceptorRequired.java:26)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired_Bean.intercept(TransactionalInterceptorRequired_Bean.zig:340)
	at io.quarkus.arc.impl.InterceptorInvocation.invoke(InterceptorInvocation.java:41)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.perform(AroundInvokeInvocationContext.java:41)
	at io.quarkus.arc.impl.InvocationContexts.performAroundInvoke(InvocationContexts.java:32)
	at br.gov.caixa.simpf.service.ContagemService_Subclass.pontuarItensBacklog(ContagemService_Subclass.zig:13622)
	at br.gov.caixa.simpf.service.ContagemService_ClientProxy.pontuarItensBacklog(ContagemService_ClientProxy.zig:1005)
	at br.gov.caixa.simpf.controller.ContagemController.getPontuacaoItensBacklog(ContagemController.java:231)
	at br.gov.caixa.simpf.controller.ContagemController_Subclass.getPontuacaoItensBacklog$$superaccessor6(ContagemController_Subclass.zig:1622)
	at br.gov.caixa.simpf.controller.ContagemController_Subclass$$function$$6.apply(ContagemController_Subclass$$function$$6.zig:33)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.proceed(AroundInvokeInvocationContext.java:54)
	at io.quarkus.security.runtime.interceptor.SecurityHandler.handle(SecurityHandler.java:24)
	at io.quarkus.security.runtime.interceptor.RolesAllowedInterceptor.intercept(RolesAllowedInterceptor.java:29)
	at io.quarkus.security.runtime.interceptor.RolesAllowedInterceptor_Bean.intercept(RolesAllowedInterceptor_Bean.zig:386)
	at io.quarkus.arc.impl.InterceptorInvocation.invoke(InterceptorInvocation.java:41)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.perform(AroundInvokeInvocationContext.java:41)
	at io.quarkus.arc.impl.InvocationContexts.performAroundInvoke(InvocationContexts.java:32)
	at br.gov.caixa.simpf.controller.ContagemController_Subclass.getPontuacaoItensBacklog(ContagemController_Subclass.zig:1579)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:566)
	at org.jboss.resteasy.core.MethodInjectorImpl.invoke(MethodInjectorImpl.java:170)
	at org.jboss.resteasy.core.MethodInjectorImpl.invoke(MethodInjectorImpl.java:130)
	at org.jboss.resteasy.core.ResourceMethodInvoker.internalInvokeOnTarget(ResourceMethodInvoker.java:660)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invokeOnTargetAfterFilter(ResourceMethodInvoker.java:524)
	at org.jboss.resteasy.core.ResourceMethodInvoker.lambda$invokeOnTarget$2(ResourceMethodInvoker.java:474)
	at org.jboss.resteasy.core.interception.jaxrs.PreMatchContainerRequestContext.filter(PreMatchContainerRequestContext.java:364)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invokeOnTarget(ResourceMethodInvoker.java:476)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invoke(ResourceMethodInvoker.java:434)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invoke(ResourceMethodInvoker.java:408)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invoke(ResourceMethodInvoker.java:69)
	at org.jboss.resteasy.core.SynchronousDispatcher.invoke(SynchronousDispatcher.java:492)
	at org.jboss.resteasy.core.SynchronousDispatcher.lambda$invoke$4(SynchronousDispatcher.java:261)
	at org.jboss.resteasy.core.SynchronousDispatcher.lambda$preprocess$0(SynchronousDispatcher.java:161)
	at org.jboss.resteasy.core.interception.jaxrs.PreMatchContainerRequestContext.filter(PreMatchContainerRequestContext.java:364)
	at org.jboss.resteasy.core.SynchronousDispatcher.preprocess(SynchronousDispatcher.java:164)
	at org.jboss.resteasy.core.SynchronousDispatcher.invoke(SynchronousDispatcher.java:247)
	at org.jboss.resteasy.plugins.server.servlet.ServletContainerDispatcher.service(ServletContainerDispatcher.java:249)
	at io.quarkus.resteasy.runtime.ResteasyFilter$ResteasyResponseWrapper.service(ResteasyFilter.java:70)
	at io.quarkus.resteasy.runtime.ResteasyFilter$ResteasyResponseWrapper.sendError(ResteasyFilter.java:76)
	at io.undertow.servlet.handlers.DefaultServlet.doGet(DefaultServlet.java:172)
	at javax.servlet.http.HttpServlet.service(HttpServlet.java:503)
	at javax.servlet.http.HttpServlet.service(HttpServlet.java:590)
	at io.undertow.servlet.handlers.ServletHandler.handleRequest(ServletHandler.java:74)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:129)
	at io.quarkus.resteasy.runtime.ResteasyFilter.doFilter(ResteasyFilter.java:31)
	at io.undertow.servlet.core.ManagedFilter.doFilter(ManagedFilter.java:61)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:131)
	at io.undertow.servlet.handlers.FilterHandler.handleRequest(FilterHandler.java:84)
	at io.undertow.servlet.handlers.security.ServletSecurityRoleHandler.handleRequest(ServletSecurityRoleHandler.java:63)
	at io.undertow.servlet.handlers.ServletChain$1.handleRequest(ServletChain.java:68)
	at io.undertow.servlet.handlers.ServletDispatchingHandler.handleRequest(ServletDispatchingHandler.java:36)
	at io.undertow.servlet.handlers.RedirectDirHandler.handleRequest(RedirectDirHandler.java:67)
	at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
	at io.undertow.servlet.handlers.security.ServletAuthenticationCallHandler.handleRequest(ServletAuthenticationCallHandler.java:57)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.security.handlers.AbstractConfidentialityHandler.handleRequest(AbstractConfidentialityHandler.java:46)
	at io.undertow.servlet.handlers.security.ServletConfidentialityConstraintHandler.handleRequest(ServletConfidentialityConstraintHandler.java:65)
	at io.undertow.security.handlers.AuthenticationMechanismsHandler.handleRequest(AuthenticationMechanismsHandler.java:60)
	at io.undertow.servlet.handlers.security.CachedAuthenticatedSessionHandler.handleRequest(CachedAuthenticatedSessionHandler.java:77)
	at io.undertow.security.handlers.NotificationReceiverHandler.handleRequest(NotificationReceiverHandler.java:50)
	at io.undertow.security.handlers.AbstractSecurityContextAssociationHandler.handleRequest(AbstractSecurityContextAssociationHandler.java:43)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.servlet.handlers.ServletInitialHandler.handleFirstRequest(ServletInitialHandler.java:247)
	at io.undertow.servlet.handlers.ServletInitialHandler.access$100(ServletInitialHandler.java:56)
	at io.undertow.servlet.handlers.ServletInitialHandler$2.call(ServletInitialHandler.java:111)
	at io.undertow.servlet.handlers.ServletInitialHandler$2.call(ServletInitialHandler.java:108)
	at io.undertow.servlet.core.ServletRequestContextThreadSetupAction$1.call(ServletRequestContextThreadSetupAction.java:48)
	at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
	at io.quarkus.undertow.runtime.UndertowDeploymentRecorder$9$1.call(UndertowDeploymentRecorder.java:587)
	at io.undertow.servlet.handlers.ServletInitialHandler.dispatchRequest(ServletInitialHandler.java:227)
	at io.undertow.servlet.handlers.ServletInitialHandler.handleRequest(ServletInitialHandler.java:152)
	at io.quarkus.undertow.runtime.UndertowDeploymentRecorder$1.handleRequest(UndertowDeploymentRecorder.java:119)
	at io.undertow.server.Connectors.executeRootHandler(Connectors.java:290)
	at io.undertow.server.DefaultExchangeHandler.handle(DefaultExchangeHandler.java:18)
	at io.quarkus.undertow.runtime.UndertowDeploymentRecorder$5$1.run(UndertowDeploymentRecorder.java:413)
	at java.base/java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:515)
	at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
	at org.jboss.threads.EnhancedQueueExecutor$Task.run(EnhancedQueueExecutor.java:2415)
	at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.run(EnhancedQueueExecutor.java:1452)
	at org.jboss.threads.DelegatingRunnable.run(DelegatingRunnable.java:29)
	at org.jboss.threads.ThreadLocalResettingRunnable.run(ThreadLocalResettingRunnable.java:29)
	at java.base/java.lang.Thread.run(Thread.java:829)
	at org.jboss.threads.JBossThread.run(JBossThread.java:501)

2026-10-15 16:39:14,427 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogEntity WHERE LOWER(coItemTrabalho) = LOWER(?1), time: 1ms, rows: 1
2026-10-15 16:39:16,310 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ServicoEntity, time: 1ms, rows: 0
2026-10-15 16:39:16,310 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuAnaliseImpacto = ?1, time: 4ms, rows: 1
2026-10-15 16:39:16,349 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1090 ORDER BY id.dataAtualizacao DESC, time: 7ms, rows: 1
2026-10-15 16:39:16,355 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1090 ORDER BY id.dataAtualizacao DESC, time: 4ms, rows: 1
2026-10-15 16:39:16,437 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.StatusServicoEntity, time: 1ms, rows: 7
2026-10-15 16:39:16,495 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE ativa = 1 and nuVersaoInicial = ?1 ORDER BY nuAnaliseImpacto, time: 3ms, rows: 1
2026-10-15 16:39:16,502 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.StatusServicoEntity, time: 1ms, rows: 7
2026-10-15 16:39:16,508 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1090 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:16,510 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1090 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:16,693 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.DisciplinaArtefatoEntity, time: 1ms, rows: 0
2026-10-15 16:39:16,836 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 4ms, rows: 30
2026-10-15 16:39:16,867 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 0ms, rows: 1
2026-10-15 16:39:16,894 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FuncionalidadeEntity, time: 177ms, rows: 2560
2026-10-15 16:39:17,110 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FluxoEstadoEntity WHERE estadoOrigem.nuEstadoMaquina = ?1, time: 5ms, rows: 4
2026-10-15 16:39:17,243 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 1
2026-10-15 16:39:17,373 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 3
2026-10-15 16:39:17,500 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 1
2026-10-15 16:39:17,630 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 1
2026-10-15 16:39:29,588 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: SELECT COUNT(DISTINCT analise.nuAnaliseImpacto) FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  , time: 302ms, rows: 1
2026-10-15 16:39:29,903 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: SELECT analise, em FROM AnaliseImpactoEntity analise LEFT JOIN AnaliseImpactoEstadoEntity ae ON ae.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial LEFT JOIN MaquinaEstadoEntity em ON em.nuEstadoMaquina = ae.id.estadoMaquina.nuEstadoMaquina WHERE analise.ativa = 1 AND NOT EXISTS (    SELECT 1 FROM AnaliseImpactoEntity a     WHERE analise.nuVersaoInicial = a.nuVersaoInicial     AND a.nuAnaliseImpacto > analise.nuAnaliseImpacto     AND a.ativa = 1 ) AND (    ae.id.dataAtualizacao = (        SELECT MAX(ae2.id.dataAtualizacao)         FROM AnaliseImpactoEstadoEntity ae2         WHERE ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuVersaoInicial         OR ae2.id.analiseImpacto.nuAnaliseImpacto = analise.nuAnaliseImpacto    )     OR ae.id.analiseImpacto.nuAnaliseImpacto IS NULL)  ORDER BY analise.dataModificacao DESC, time: 314ms, rows: 30
2026-10-15 16:39:30,182 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ContagemSNAPEntity WHERE nuContagemDadosSnap IN (:ids_0, :ids_1), time: 0ms, rows: 2
2026-10-15 16:39:30,185 WARNING [br.gov.cai.sim.ser.sip.ItemTrabalhoService] (executor-thread-4) Fluxo Simplifica indispon?vel para o item informado. Aplicando fallback interno.: java.lang.UnsupportedOperationException: Consulta ao Simplifica n?o implementada ainda.
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService.consultarSimplifica(ItemTrabalhoService.java:91)
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService.buscarComFallbackSimplifica(ItemTrabalhoService.java:68)
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService.findHistoriaUsuarioById(ItemTrabalhoService.java:56)
	at br.gov.caixa.simpf.service.sipgc.ItemTrabalhoService_ClientProxy.findHistoriaUsuarioById(ItemTrabalhoService_ClientProxy.zig:157)
	at br.gov.caixa.simpf.service.CalculoContagemService.getListaItemBacklogRTC(CalculoContagemService.java:239)
	at br.gov.caixa.simpf.service.CalculoContagemService.pontuarItensBacklog(CalculoContagemService.java:206)
	at br.gov.caixa.simpf.service.CalculoContagemService_Subclass.pontuarItensBacklog$$superaccessor1(CalculoContagemService_Subclass.zig:211)
	at br.gov.caixa.simpf.service.CalculoContagemService_Subclass$$function$$1.apply(CalculoContagemService_Subclass$$function$$1.zig:33)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.proceed(AroundInvokeInvocationContext.java:54)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.invokeInCallerTx(TransactionalInterceptorBase.java:252)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.doIntercept(TransactionalInterceptorRequired.java:34)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.intercept(TransactionalInterceptorBase.java:53)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.intercept(TransactionalInterceptorRequired.java:26)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired_Bean.intercept(TransactionalInterceptorRequired_Bean.zig:340)
	at io.quarkus.arc.impl.InterceptorInvocation.invoke(InterceptorInvocation.java:41)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.perform(AroundInvokeInvocationContext.java:41)
	at io.quarkus.arc.impl.InvocationContexts.performAroundInvoke(InvocationContexts.java:32)
	at br.gov.caixa.simpf.service.CalculoContagemService_Subclass.pontuarItensBacklog(CalculoContagemService_Subclass.zig:168)
	at br.gov.caixa.simpf.service.CalculoContagemService_ClientProxy.pontuarItensBacklog(CalculoContagemService_ClientProxy.zig:352)
	at br.gov.caixa.simpf.service.ContagemService.pontuarItensBacklog(ContagemService.java:138)
	at br.gov.caixa.simpf.service.ContagemService_Subclass.pontuarItensBacklog$$superaccessor84(ContagemService_Subclass.zig:13665)
	at br.gov.caixa.simpf.service.ContagemService_Subclass$$function$$84.apply(ContagemService_Subclass$$function$$84.zig:33)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.proceed(AroundInvokeInvocationContext.java:54)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.invokeInOurTx(TransactionalInterceptorBase.java:127)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.invokeInOurTx(TransactionalInterceptorBase.java:100)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.doIntercept(TransactionalInterceptorRequired.java:32)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorBase.intercept(TransactionalInterceptorBase.java:53)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired.intercept(TransactionalInterceptorRequired.java:26)
	at io.quarkus.narayana.jta.runtime.interceptor.TransactionalInterceptorRequired_Bean.intercept(TransactionalInterceptorRequired_Bean.zig:340)
	at io.quarkus.arc.impl.InterceptorInvocation.invoke(InterceptorInvocation.java:41)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.perform(AroundInvokeInvocationContext.java:41)
	at io.quarkus.arc.impl.InvocationContexts.performAroundInvoke(InvocationContexts.java:32)
	at br.gov.caixa.simpf.service.ContagemService_Subclass.pontuarItensBacklog(ContagemService_Subclass.zig:13622)
	at br.gov.caixa.simpf.service.ContagemService_ClientProxy.pontuarItensBacklog(ContagemService_ClientProxy.zig:1005)
	at br.gov.caixa.simpf.controller.ContagemController.getPontuacaoItensBacklog(ContagemController.java:231)
	at br.gov.caixa.simpf.controller.ContagemController_Subclass.getPontuacaoItensBacklog$$superaccessor6(ContagemController_Subclass.zig:1622)
	at br.gov.caixa.simpf.controller.ContagemController_Subclass$$function$$6.apply(ContagemController_Subclass$$function$$6.zig:33)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.proceed(AroundInvokeInvocationContext.java:54)
	at io.quarkus.security.runtime.interceptor.SecurityHandler.handle(SecurityHandler.java:24)
	at io.quarkus.security.runtime.interceptor.RolesAllowedInterceptor.intercept(RolesAllowedInterceptor.java:29)
	at io.quarkus.security.runtime.interceptor.RolesAllowedInterceptor_Bean.intercept(RolesAllowedInterceptor_Bean.zig:386)
	at io.quarkus.arc.impl.InterceptorInvocation.invoke(InterceptorInvocation.java:41)
	at io.quarkus.arc.impl.AroundInvokeInvocationContext.perform(AroundInvokeInvocationContext.java:41)
	at io.quarkus.arc.impl.InvocationContexts.performAroundInvoke(InvocationContexts.java:32)
	at br.gov.caixa.simpf.controller.ContagemController_Subclass.getPontuacaoItensBacklog(ContagemController_Subclass.zig:1579)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:566)
	at org.jboss.resteasy.core.MethodInjectorImpl.invoke(MethodInjectorImpl.java:170)
	at org.jboss.resteasy.core.MethodInjectorImpl.invoke(MethodInjectorImpl.java:130)
	at org.jboss.resteasy.core.ResourceMethodInvoker.internalInvokeOnTarget(ResourceMethodInvoker.java:660)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invokeOnTargetAfterFilter(ResourceMethodInvoker.java:524)
	at org.jboss.resteasy.core.ResourceMethodInvoker.lambda$invokeOnTarget$2(ResourceMethodInvoker.java:474)
	at org.jboss.resteasy.core.interception.jaxrs.PreMatchContainerRequestContext.filter(PreMatchContainerRequestContext.java:364)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invokeOnTarget(ResourceMethodInvoker.java:476)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invoke(ResourceMethodInvoker.java:434)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invoke(ResourceMethodInvoker.java:408)
	at org.jboss.resteasy.core.ResourceMethodInvoker.invoke(ResourceMethodInvoker.java:69)
	at org.jboss.resteasy.core.SynchronousDispatcher.invoke(SynchronousDispatcher.java:492)
	at org.jboss.resteasy.core.SynchronousDispatcher.lambda$invoke$4(SynchronousDispatcher.java:261)
	at org.jboss.resteasy.core.SynchronousDispatcher.lambda$preprocess$0(SynchronousDispatcher.java:161)
	at org.jboss.resteasy.core.interception.jaxrs.PreMatchContainerRequestContext.filter(PreMatchContainerRequestContext.java:364)
	at org.jboss.resteasy.core.SynchronousDispatcher.preprocess(SynchronousDispatcher.java:164)
	at org.jboss.resteasy.core.SynchronousDispatcher.invoke(SynchronousDispatcher.java:247)
	at org.jboss.resteasy.plugins.server.servlet.ServletContainerDispatcher.service(ServletContainerDispatcher.java:249)
	at io.quarkus.resteasy.runtime.ResteasyFilter$ResteasyResponseWrapper.service(ResteasyFilter.java:70)
	at io.quarkus.resteasy.runtime.ResteasyFilter$ResteasyResponseWrapper.sendError(ResteasyFilter.java:76)
	at io.undertow.servlet.handlers.DefaultServlet.doGet(DefaultServlet.java:172)
	at javax.servlet.http.HttpServlet.service(HttpServlet.java:503)
	at javax.servlet.http.HttpServlet.service(HttpServlet.java:590)
	at io.undertow.servlet.handlers.ServletHandler.handleRequest(ServletHandler.java:74)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:129)
	at io.quarkus.resteasy.runtime.ResteasyFilter.doFilter(ResteasyFilter.java:31)
	at io.undertow.servlet.core.ManagedFilter.doFilter(ManagedFilter.java:61)
	at io.undertow.servlet.handlers.FilterHandler$FilterChainImpl.doFilter(FilterHandler.java:131)
	at io.undertow.servlet.handlers.FilterHandler.handleRequest(FilterHandler.java:84)
	at io.undertow.servlet.handlers.security.ServletSecurityRoleHandler.handleRequest(ServletSecurityRoleHandler.java:63)
	at io.undertow.servlet.handlers.ServletChain$1.handleRequest(ServletChain.java:68)
	at io.undertow.servlet.handlers.ServletDispatchingHandler.handleRequest(ServletDispatchingHandler.java:36)
	at io.undertow.servlet.handlers.RedirectDirHandler.handleRequest(RedirectDirHandler.java:67)
	at io.undertow.servlet.handlers.security.SSLInformationAssociationHandler.handleRequest(SSLInformationAssociationHandler.java:133)
	at io.undertow.servlet.handlers.security.ServletAuthenticationCallHandler.handleRequest(ServletAuthenticationCallHandler.java:57)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.security.handlers.AbstractConfidentialityHandler.handleRequest(AbstractConfidentialityHandler.java:46)
	at io.undertow.servlet.handlers.security.ServletConfidentialityConstraintHandler.handleRequest(ServletConfidentialityConstraintHandler.java:65)
	at io.undertow.security.handlers.AuthenticationMechanismsHandler.handleRequest(AuthenticationMechanismsHandler.java:60)
	at io.undertow.servlet.handlers.security.CachedAuthenticatedSessionHandler.handleRequest(CachedAuthenticatedSessionHandler.java:77)
	at io.undertow.security.handlers.NotificationReceiverHandler.handleRequest(NotificationReceiverHandler.java:50)
	at io.undertow.security.handlers.AbstractSecurityContextAssociationHandler.handleRequest(AbstractSecurityContextAssociationHandler.java:43)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.server.handlers.PredicateHandler.handleRequest(PredicateHandler.java:43)
	at io.undertow.servlet.handlers.ServletInitialHandler.handleFirstRequest(ServletInitialHandler.java:247)
	at io.undertow.servlet.handlers.ServletInitialHandler.access$100(ServletInitialHandler.java:56)
	at io.undertow.servlet.handlers.ServletInitialHandler$2.call(ServletInitialHandler.java:111)
	at io.undertow.servlet.handlers.ServletInitialHandler$2.call(ServletInitialHandler.java:108)
	at io.undertow.servlet.core.ServletRequestContextThreadSetupAction$1.call(ServletRequestContextThreadSetupAction.java:48)
	at io.undertow.servlet.core.ContextClassLoaderSetupAction$1.call(ContextClassLoaderSetupAction.java:43)
	at io.quarkus.undertow.runtime.UndertowDeploymentRecorder$9$1.call(UndertowDeploymentRecorder.java:587)
	at io.undertow.servlet.handlers.ServletInitialHandler.dispatchRequest(ServletInitialHandler.java:227)
	at io.undertow.servlet.handlers.ServletInitialHandler.handleRequest(ServletInitialHandler.java:152)
	at io.quarkus.undertow.runtime.UndertowDeploymentRecorder$1.handleRequest(UndertowDeploymentRecorder.java:119)
	at io.undertow.server.Connectors.executeRootHandler(Connectors.java:290)
	at io.undertow.server.DefaultExchangeHandler.handle(DefaultExchangeHandler.java:18)
	at io.quarkus.undertow.runtime.UndertowDeploymentRecorder$5$1.run(UndertowDeploymentRecorder.java:413)
	at java.base/java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:515)
	at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
	at org.jboss.threads.EnhancedQueueExecutor$Task.run(EnhancedQueueExecutor.java:2415)
	at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.run(EnhancedQueueExecutor.java:1452)
	at org.jboss.threads.DelegatingRunnable.run(DelegatingRunnable.java:29)
	at org.jboss.threads.ThreadLocalResettingRunnable.run(ThreadLocalResettingRunnable.java:29)
	at java.base/java.lang.Thread.run(Thread.java:829)
	at org.jboss.threads.JBossThread.run(JBossThread.java:501)

2026-10-15 16:39:30,187 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogEntity WHERE LOWER(coItemTrabalho) = LOWER(?1), time: 0ms, rows: 1
2026-10-15 16:39:33,634 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ServicoEntity, time: 1ms, rows: 0
2026-10-15 16:39:33,637 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuAnaliseImpacto = ?1, time: 4ms, rows: 1
2026-10-15 16:39:33,681 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 8ms, rows: 1
2026-10-15 16:39:33,688 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 4ms, rows: 1
2026-10-15 16:39:33,762 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.StatusServicoEntity, time: 1ms, rows: 7
2026-10-15 16:39:33,828 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE ativa = 1 and nuVersaoInicial = ?1 ORDER BY nuAnaliseImpacto, time: 3ms, rows: 1
2026-10-15 16:39:33,828 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.StatusServicoEntity, time: 1ms, rows: 7
2026-10-15 16:39:33,845 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:33,847 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:34,042 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.DisciplinaArtefatoEntity, time: 1ms, rows: 0
2026-10-15 16:39:34,189 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 4ms, rows: 30
2026-10-15 16:39:34,224 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 0ms, rows: 1
2026-10-15 16:39:34,226 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FuncionalidadeEntity, time: 179ms, rows: 2560
2026-10-15 16:39:34,460 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FluxoEstadoEntity WHERE estadoOrigem.nuEstadoMaquina = ?1, time: 5ms, rows: 4
2026-10-15 16:39:34,591 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1 ORDER BY dataModificacao DESC, time: 2ms, rows: 3
2026-10-15 16:39:34,591 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 1
2026-10-15 16:39:34,592 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1, time: 1ms, rows: 1
2026-10-15 16:39:34,717 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 3
2026-10-15 16:39:34,848 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 1
2026-10-15 16:39:34,973 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 1
2026-10-15 16:39:48,413 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogEntity WHERE nuItemBacklogRequisito = ?1, time: 1ms, rows: 1
2026-10-15 16:39:48,414 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogImpactadoEntity WHERE NU_ANALISE_IMPACTO=:idAnaliseImpacto and NU_ITEM_BACKLOG=:idItemBacklog, time: 0ms, rows: 1
2026-10-15 16:39:51,963 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 1ms, rows: 3
2026-10-15 16:39:52,100 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 1ms, rows: 3
2026-10-15 16:39:52,232 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuAnaliseImpacto = ?1, time: 4ms, rows: 1
2026-10-15 16:39:52,257 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE itemSistema.nuItemSistema = ?1 and lower(iteracao) = ?2 and lower(siglaSquad) = ?3 and ativa=1, time: 1ms, rows: 1
2026-10-15 16:39:52,258 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 3
2026-10-15 16:39:52,262 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogEntity WHERE nuItemBacklogRequisito = ?1, time: 0ms, rows: 1
2026-10-15 16:39:52,263 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogImpactadoEntity WHERE NU_ANALISE_IMPACTO=:idAnaliseImpacto and NU_ITEM_BACKLOG=:idItemBacklog, time: 0ms, rows: 1
2026-10-15 16:39:52,274 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:52,275 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuVersaoInicial = ?1, time: 0ms, rows: 1
2026-10-15 16:39:52,408 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuAnaliseImpacto = ?1, time: 3ms, rows: 1
2026-10-15 16:39:52,439 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:52,442 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 2
2026-10-15 16:39:52,582 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE ativa = 1 and nuVersaoInicial = ?1 ORDER BY nuAnaliseImpacto, time: 4ms, rows: 1
2026-10-15 16:39:52,599 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:39:52,601 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 0ms, rows: 2
2026-10-15 16:39:52,943 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 6ms, rows: 30
2026-10-15 16:39:52,965 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-2) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FuncionalidadeEntity, time: 160ms, rows: 2560
2026-10-15 16:39:52,978 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 0ms, rows: 1
2026-10-15 16:39:53,267 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FluxoEstadoEntity WHERE estadoOrigem.nuEstadoMaquina = ?1, time: 5ms, rows: 5
2026-10-15 16:39:53,397 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1 ORDER BY dataModificacao DESC, time: 2ms, rows: 3
2026-10-15 16:39:53,398 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1, time: 0ms, rows: 1
2026-10-15 16:39:53,413 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 1
2026-10-15 16:39:53,549 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 1
2026-10-15 16:39:53,836 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 1
2026-10-15 16:39:53,968 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 2
2026-10-15 16:39:54,208 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 1
2026-10-15 16:40:02,771 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 1
2026-10-15 16:40:02,908 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 1
2026-10-15 16:40:03,039 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuAnaliseImpacto = ?1, time: 3ms, rows: 1
2026-10-15 16:40:03,061 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 1
2026-10-15 16:40:03,075 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogEntity WHERE nuItemBacklogRequisito = ?1, time: 0ms, rows: 1
2026-10-15 16:40:03,076 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogImpactadoEntity WHERE NU_ANALISE_IMPACTO=:idAnaliseImpacto and NU_ITEM_BACKLOG=:idItemBacklog, time: 0ms, rows: 0
2026-10-15 16:40:03,088 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogEntity WHERE nuItemBacklogRequisito = ?1, time: 0ms, rows: 1
2026-10-15 16:40:03,089 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogImpactadoEntity WHERE NU_ANALISE_IMPACTO=:idAnaliseImpacto and NU_ITEM_BACKLOG=:idItemBacklog, time: 0ms, rows: 1
2026-10-15 16:40:03,116 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogImpactadoEntity WHERE NU_ANALISE_IMPACTO=:idAnaliseImpacto and NU_ITEM_BACKLOG=:idItemBacklog, time: 0ms, rows: 1
2026-10-15 16:40:03,127 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogImpactadoEntity WHERE NU_ANALISE_IMPACTO=:idAnaliseImpacto and NU_ITEM_BACKLOG=:idItemBacklog, time: 0ms, rows: 1
2026-10-15 16:40:03,132 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuAnaliseImpacto = ?1, time: 0ms, rows: 1
2026-10-15 16:40:03,152 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogEntity WHERE nuItemBacklogRequisito = ?1, time: 0ms, rows: 1
2026-10-15 16:40:03,153 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ItemBacklogImpactadoEntity WHERE NU_ANALISE_IMPACTO=:idAnaliseImpacto and NU_ITEM_BACKLOG=:idItemBacklog, time: 0ms, rows: 1
2026-10-15 16:40:03,158 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:40:03,160 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuVersaoInicial = ?1, time: 0ms, rows: 2
2026-10-15 16:40:03,294 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE nuAnaliseImpacto = ?1, time: 3ms, rows: 1
2026-10-15 16:40:03,319 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:40:03,322 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 3
2026-10-15 16:40:03,461 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEntity WHERE ativa = 1 and nuVersaoInicial = ?1 ORDER BY nuAnaliseImpacto, time: 3ms, rows: 2
2026-10-15 16:40:03,477 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 1
2026-10-15 16:40:03,479 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 3
2026-10-15 16:40:03,502 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 0ms, rows: 1
2026-10-15 16:40:03,504 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.AnaliseImpactoEstadoEntity WHERE id.analiseImpacto.nuVersaoInicial = 1086 ORDER BY id.dataAtualizacao DESC, time: 1ms, rows: 3
2026-10-15 16:40:03,940 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FuncionalidadeEntity, time: 172ms, rows: 2560
2026-10-15 16:40:04,060 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 4ms, rows: 30
2026-10-15 16:40:04,092 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ContratoEntity WHERE 1=1, time: 0ms, rows: 1
2026-10-15 16:40:04,175 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.FluxoEstadoEntity WHERE estadoOrigem.nuEstadoMaquina = ?1, time: 3ms, rows: 2
2026-10-15 16:40:04,307 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1 ORDER BY dataModificacao DESC, time: 2ms, rows: 3
2026-10-15 16:40:04,308 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-4) HHH000117: HQL: SELECT COUNT(*) FROM br.gov.caixa.simpf.entity.ParametroRepositorioEntity WHERE 1=1 and itemSistema.coItemPortifolio =:coItemPortifolio and ( lower(itemSistema.deItemPortifolio) like '%'||:deItemPortifolio||'%' OR itemSistema.coItemPortifolio like '%'||:deItemPortifolio||'%') and ativo = 1, time: 0ms, rows: 1
2026-10-15 16:40:04,311 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 0ms, rows: 3
2026-10-15 16:40:04,446 DEBUG [org.hib.sta.int.StatisticsImpl] (executor-thread-6) HHH000117: HQL: FROM br.gov.caixa.simpf.entity.PermissaoEntity WHERE maquinaEstado.nuEstadoMaquina = ?1, time: 1ms, rows: 1
