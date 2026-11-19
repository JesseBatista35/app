A release
https://devops.caixa/projetos/Caixa/_releaseProgress?_a=release-environment-logs&releaseId=558746&environmentId=2598004 está terminando com timeout na etapa "Verificando Status do Deployment"


2026-11-19T15:13:57.9723214Z ##[section]Starting: Verificando Status do Deployment
2026-11-19T15:13:57.9726501Z ==============================================================================
2026-11-19T15:13:57.9726610Z Task         : Bash
2026-11-19T15:13:57.9726652Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-11-19T15:13:57.9726714Z Version      : 3.227.0
2026-11-19T15:13:57.9726794Z Author       : Microsoft Corporation
2026-11-19T15:13:57.9726843Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-11-19T15:13:57.9726915Z ==============================================================================
2026-11-19T15:13:58.1130049Z Generating script.
2026-11-19T15:13:58.1139372Z ========================== Starting Command Output ===========================
2026-11-19T15:13:58.1146767Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/5399c350-f88c-43b3-81ef-3453f5eb6451.sh
2026-11-19T15:13:58.2005189Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-11-19T15:13:59.1208989Z Waiting for rollout to finish: 0 out of 1 new replicas have been updated...
2026-11-19T15:13:59.1949892Z Waiting for rollout to finish: 0 of 1 updated replicas are available...
2026-11-19T15:20:05.4834152Z ##[error]The task has timed out.
2026-11-19T15:20:05.4835150Z ##[section]Finishing: Verificando Status do Deployment


2026-11-19T15:20:05.4858437Z ##[section]Starting: Logs da Aplicação
2026-11-19T15:20:05.4862308Z ==============================================================================
2026-11-19T15:20:05.4862461Z Task         : Bash
2026-11-19T15:20:05.4862502Z Description  : Run a Bash script on macOS, Linux, or Windows
2026-11-19T15:20:05.4862561Z Version      : 3.227.0
2026-11-19T15:20:05.4862833Z Author       : Microsoft Corporation
2026-11-19T15:20:05.4862887Z Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
2026-11-19T15:20:05.4862959Z ==============================================================================
2026-11-19T15:20:05.6376766Z Generating script.
2026-11-19T15:20:05.6378193Z ========================== Starting Command Output ===========================
2026-11-19T15:20:05.6388517Z [command]/usr/bin/bash /opt/ads-agent/_work/_temp/6beaaecb-2dd3-4e0a-925c-b90935893390.sh
2026-11-19T15:20:05.6437438Z + shopt -s expand_aliases
2026-11-19T15:20:05.6437613Z + [[ -n okd4_nprd ]]
2026-11-19T15:20:05.6437843Z + [[ okd4_nprd =~ ocp ]]
2026-11-19T15:20:05.6437972Z + [[ -n okd4_nprd ]]
2026-11-19T15:20:05.6438107Z + [[ okd4_nprd =~ (okd4|openshift) ]]
2026-11-19T15:20:05.6438298Z + app=sigsj-backend-portal-judicial-des
2026-11-19T15:20:05.6438442Z + oc version
2026-11-19T15:20:05.7076573Z Client Version: v4.2.0-alpha.0-1394-g45460a5
2026-11-19T15:20:05.7076898Z Server Version: 4.12.0-0.okd-2023-04-16-041331
2026-11-19T15:20:05.7077117Z Kubernetes Version: v1.25.0-2824+27e744f55d2e99-dirty
2026-11-19T15:20:05.7105390Z ++ oc get pod -l name=sigsj-backend-portal-judicial-des -n sigsj-des -o 'jsonpath={range .items[*]}{.metadata.name}{"\n"}' --sort-by=.metadata.creationTimestamp
2026-11-19T15:20:05.7106465Z ++ tac
2026-11-19T15:20:05.7106595Z ++ grep -v '^$'
2026-11-19T15:20:05.7108171Z ++ head -n1
2026-11-19T15:20:05.7920026Z + last_pod=sigsj-backend-portal-judicial-des-1-gfjm6
2026-11-19T15:20:05.7920343Z + echo 'Logs do POD: sigsj-backend-portal-judicial-des-1-gfjm6'
2026-11-19T15:20:05.7920897Z + oc logs sigsj-backend-portal-judicial-des-1-gfjm6 -c sigsj-backend-portal-judicial-des -n sigsj-des
2026-11-19T15:20:05.7921109Z Logs do POD: sigsj-backend-portal-judicial-des-1-gfjm6
2026-11-19T15:20:05.8823762Z exec java -Dquarkus.http.host=0.0.0.0 -Dquarkus.http.port=8080 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -XX:+ExitOnOutOfMemoryError -cp . -jar /deployments/quarkus-run.jar
2026-11-19T15:20:05.8824225Z __  ____  __  _____   ___  __ ____  ______ 
2026-11-19T15:20:05.8824426Z  --/ __ \/ / / / _ | / _ \/ //_/ / / / __/ 
2026-11-19T15:20:05.8824608Z  -/ /_/ / /_/ / __ |/ , _/ ,< / /_/ /\ \   
2026-11-19T15:20:05.8824755Z --\___\_\____/_/ |_/_/|_/_/|_|\____/___/   
2026-11-19T15:20:05.8825263Z [38;5;251m2026-11-19 12:17:31,544[39m[38;5;251m [39m[38;5;222mWARN [39m[38;5;251m [[39m[38;5;153mio.quarkus.config[39m[38;5;251m] ([39m[38;5;250mmain[39m[38;5;251m) [39m[38;5;251m[38;5;231mThe "[38;5;253mquarkus.hibernate-orm.database.generation[38;5;231m" config property is deprecated and should not be used anymore.[39m[39m[38;5;203m[39m[38;5;229m
2026-11-19T15:20:05.8825993Z [39m[38;5;251m2026-11-19 12:17:31,584[39m[38;5;251m [39m[38;5;222mWARN [39m[38;5;251m [[39m[38;5;153mio.quarkus.config[39m[38;5;251m] ([39m[38;5;250mmain[39m[38;5;251m) [39m[38;5;251m[38;5;231mThe "[38;5;253mquarkus.swagger-ui.enable[38;5;231m" config property is deprecated and should not be used anymore.[39m[39m[38;5;203m[39m[38;5;229m
2026-11-19T15:20:05.8826588Z [39m[38;5;251m2026-11-19 12:17:31,713[39m[38;5;251m [39m[38;5;210mERROR[39m[38;5;251m [[39m[38;5;153mio.quarkus.runtime.Application[39m[38;5;251m] ([39m[38;5;250mmain[39m[38;5;251m) [39m[38;5;251mFailed to start application[39m[38;5;203m: java.lang.RuntimeException: Failed to start quarkus
2026-11-19T15:20:05.8826888Z 	at io.quarkus.runner.ApplicationImpl.doStart(Unknown Source)
2026-11-19T15:20:05.8827129Z 	at io.quarkus.runtime.Application.start(Application.java:112)
2026-11-19T15:20:05.8827363Z 	at io.quarkus.runtime.ApplicationLifecycleManager.run(ApplicationLifecycleManager.java:129)
2026-11-19T15:20:05.8827929Z 	at io.quarkus.runtime.Quarkus.run(Quarkus.java:79)
2026-11-19T15:20:05.8828073Z 	at io.quarkus.runtime.Quarkus.run(Quarkus.java:50)
2026-11-19T15:20:05.8828248Z 	at io.quarkus.runtime.Quarkus.run(Quarkus.java:143)
2026-11-19T15:20:05.8828414Z 	at io.quarkus.runner.GeneratedMain.main(Unknown Source)
2026-11-19T15:20:05.8828599Z 	at io.quarkus.bootstrap.runner.QuarkusEntryPoint.doRun(QuarkusEntryPoint.java:70)
2026-11-19T15:20:05.8828776Z 	at io.quarkus.bootstrap.runner.QuarkusEntryPoint.main(QuarkusEntryPoint.java:36)
2026-11-19T15:20:05.8829011Z Caused by: io.quarkus.arc.InactiveBeanException: Bean is not active: SYNTHETIC bean [class=org.hibernate.Session, id=x03UFp930IxQOyJJLmtWw2baujI]
2026-11-19T15:20:05.8829374Z Reason: Persistence unit '<default>' was deactivated automatically because it doesn't include any entity type and its datasource '<default>' was deactivated.
2026-11-19T15:20:05.8829795Z Cause: Datasource '<default>' was deactivated automatically because its URL is not set. To activate the datasource, set configuration property 'quarkus.datasource.jdbc.url'. Refer to https://quarkus.io/guides/datasource for guidance.
2026-11-19T15:20:05.8830045Z To avoid this exception while keeping the bean inactive:
2026-11-19T15:20:05.8830321Z 	- Configure all extensions consuming this bean as inactive as well, if they allow it, e.g. 'quarkus.someextension.active=false'
2026-11-19T15:20:05.8830546Z 	- Make sure that custom code only accesses this bean if it is active
2026-11-19T15:20:05.8830798Z 	- Inject the bean with 'Instance<org.hibernate.Session>' instead of 'org.hibernate.Session'
2026-11-19T15:20:05.8830964Z This bean is injected into:
2026-11-19T15:20:05.8831203Z 	- parameter 'em' of br.gov.caixa.sigsj.portaljudicial.repository.ProcessoRepository constructor
2026-11-19T15:20:05.8831369Z 	at org.hibernate.Session_x03UFp930IxQOyJJLmtWw2baujI_Synthetic_Bean.create(Unknown Source)
2026-11-19T15:20:05.8831632Z 	at org.hibernate.Session_x03UFp930IxQOyJJLmtWw2baujI_Synthetic_Bean.create(Unknown Source)
2026-11-19T15:20:05.8831845Z 	at io.quarkus.arc.impl.AbstractSharedContext.createInstanceHandle(AbstractSharedContext.java:119)
2026-11-19T15:20:05.8832067Z 	at io.quarkus.arc.impl.AbstractSharedContext$1.get(AbstractSharedContext.java:38)
2026-11-19T15:20:05.8832275Z 	at io.quarkus.arc.impl.AbstractSharedContext$1.get(AbstractSharedContext.java:35)
2026-11-19T15:20:05.8832456Z 	at io.quarkus.arc.generator.Default_jakarta_enterprise_context_ApplicationScoped_ContextInstances.ch41(Unknown Source)
2026-11-19T15:20:05.8832756Z 	at io.quarkus.arc.generator.Default_jakarta_enterprise_context_ApplicationScoped_ContextInstances.computeIfAbsent(Unknown Source)
2026-11-19T15:20:05.8832985Z 	at io.quarkus.arc.impl.AbstractSharedContext.get(AbstractSharedContext.java:35)
2026-11-19T15:20:05.8833199Z 	at io.quarkus.arc.impl.ClientProxies.getApplicationScopedDelegate(ClientProxies.java:23)
2026-11-19T15:20:05.8833420Z 	at org.hibernate.Session_x03UFp930IxQOyJJLmtWw2baujI_Synthetic_ClientProxy.arc$delegate(Unknown Source)
2026-11-19T15:20:05.8833602Z 	at org.hibernate.Session_x03UFp930IxQOyJJLmtWw2baujI_Synthetic_ClientProxy.arc_contextualInstance(Unknown Source)
2026-11-19T15:20:05.8833886Z 	at org.hibernate.Session_Observer_Synthetic_4tol_k5Rt0NCI8VXX7R-QHpbagc.notify(Unknown Source)
2026-11-19T15:20:05.8834086Z 	at io.quarkus.arc.impl.EventImpl$Notifier.notifyObservers(EventImpl.java:366)
2026-11-19T15:20:05.8834283Z 	at io.quarkus.arc.impl.EventImpl$Notifier.notify(EventImpl.java:348)
2026-11-19T15:20:05.8834463Z 	at io.quarkus.arc.impl.EventImpl.fire(EventImpl.java:81)
2026-11-19T15:20:05.8834621Z 	at io.quarkus.arc.runtime.ArcRecorder.fireLifecycleEvent(ArcRecorder.java:165)
2026-11-19T15:20:05.8834825Z 	at io.quarkus.arc.runtime.ArcRecorder.handleLifecycleEvents(ArcRecorder.java:115)
2026-11-19T15:20:05.8835031Z 	at io.quarkus.runner.recorded.LifecycleEventsBuildStep$startupEvent1144526294.deploy_0(Unknown Source)
2026-11-19T15:20:05.8835308Z 	at io.quarkus.runner.recorded.LifecycleEventsBuildStep$startupEvent1144526294.deploy(Unknown Source)
2026-11-19T15:20:05.8835462Z 	... 9 more
2026-11-19T15:20:05.8835586Z [39m[38;5;229m
2026-11-19T15:20:05.8907859Z ##[section]Finishing: Logs da Aplicação
