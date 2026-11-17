
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# grep -a "Keycloak subsystem override" $LOG | tail -3
15:21:50,770 INFO  [org.jboss.keycloak] (MSC service thread 1-5) Keycloak subsystem override for deployment ccr-web.war
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# tail -f $LOG | grep -aiE "ccr-api|keycloak|401|403|ERROR"
15:29:47,536 WARN  [com.arjuna.ats.arjuna] (default task-110) ARJUNA012091: Top-level abort of action 0:ffff0a74614f:717b6493:6af5c389:906a received TwoPhaseOutcome.FINISH_ERROR from com.arjuna.ats.internal.arjuna.abstractrecords.LastResourceRecord
15:29:47,536 WARN  [com.arjuna.ats.arjuna] (default task-107) ARJUNA012091: Top-level abort of action 0:ffff0a74614f:717b6493:6af5c389:907f received TwoPhaseOutcome.FINISH_ERROR from com.arjuna.ats.internal.arjuna.abstractrecords.LastResourceRecord
15:29:48,966 WARN  [org.keycloak.adapters.RefreshableKeycloakSecurityContext] (default task-110) Refresh token failure status: 400 {"error":"invalid_grant","error_description":"Refresh token expired"}
15:29:49,021 INFO  [org.jboss.as.connector.deployers.RaXmlDeployer] (default task-110) wmq.jmsra.rar: MQJCA4016:Identificador de conexões não registrado sendo fechado: 'com.ibm.mq.connector.outbound.ConnectionWrapper@582f30fb'.
15:29:49,254 WARN  [org.keycloak.adapters.RefreshableKeycloakSecurityContext] (default task-110) Refresh token failure status: 400 {"error":"invalid_grant","error_description":"Refresh token expired"}
15:29:50,812 WARN  [org.keycloak.adapters.RefreshableKeycloakSecurityContext] (default task-110) Refresh token failure status: 400 {"error":"invalid_grant","error_description":"Refresh token expired"}
15:29:50,867 INFO  [org.jboss.as.connector.deployers.RaXmlDeployer] (default task-110) wmq.jmsra.rar: MQJCA4016:Identificador de conexões não registrado sendo fechado: 'com.ibm.mq.connector.outbound.ConnectionWrapper@430c144e'.
15:29:51,067 WARN  [org.keycloak.adapters.RefreshableKeycloakSecurityContext] (default task-110) Refresh token failure status: 400 {"error":"invalid_grant","error_description":"Refresh token expired"}
15:29:52,508 WARN  [org.keycloak.adapters.RefreshableKeycloakSecurityContext] (default task-110) Refresh token failure status: 400 {"error":"invalid_grant","error_description":"Refresh token expired"}
15:29:52,563 INFO  [org.jboss.as.connector.deployers.RaXmlDeployer] (default task-110) wmq.jmsra.rar: MQJCA4016:Identificador de conexões não registrado sendo fechado: 'com.ibm.mq.connector.outbound.ConnectionWrapper@5bc72b91'.
15:29:53,080 WARN  [org.keycloak.adapters.RefreshableKeycloakSecurityContext] (default task-110) Refresh token failure status: 400 {"error":"invalid_grant","error_description":"Refresh token expired"}
         parameter=_=1794940196342
       queryString=_=1794940196342
         parameter=_=1794940196343
       queryString=_=1794940196343
         parameter=_=1794940196344
       queryString=_=1794940196344
         parameter=_=1794940196345
       queryString=_=1794940196345
         parameter=_=1794940196346
       queryString=_=1794940196346
15:30:03,401 WARN  [org.jboss.jca.core.connectionmanager.pool.strategy.OnePool] (default task-108) IJ000604: Throwable while attempting to get a new connection: null: javax.resource.ResourceException: IJ031084: Unable to create connection
        at org.keycloak.adapters.undertow.UndertowAuthenticatedActionsHandler.handleRequest(UndertowAuthenticatedActionsHandler.java:66)
        at org.keycloak.adapters.undertow.ServletPreAuthActionsHandler.handleRequest(ServletPreAuthActionsHandler.java:69)
        at io.undertow.servlet.handlers.SendErrorPageHandler.handleRequest(SendErrorPageHandler.java:52)
15:30:03,435 WARN  [org.hibernate.engine.jdbc.spi.SqlExceptionHelper] (default task-108) SQL Error: 0, SQLState: null
15:30:03,435 ERROR [org.hibernate.engine.jdbc.spi.SqlExceptionHelper] (default task-108) javax.resource.ResourceException: IJ000453: Unable to get managed connection for java:/jdbc/OracleSiccrDS



