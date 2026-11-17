
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# ls -d /opt/jboss/jboss-eap/hc/servers/*/
/opt/jboss/jboss-eap/hc/servers/server-one/  /opt/jboss/jboss-eap/hc/servers/sifec-intranet2_node1_llx473/
/opt/jboss/jboss-eap/hc/servers/server-two/  /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# LOG=/opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log; ls -l $LOG
-rw-r--r-- 1 jboss jboss 1359113 Nov 17 15:22 /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log
[root@cbrdeapllx473 p585600]# grep -aE "Keycloak subsystem override|ccr-api|SIFEC-CCR|WFLYSRV0016|WFLYSRV0010" $LOG | tail -20
        java:global/SIFEC-CCR-6.3.0-b4587/ccr-ejb/AuditoriaBean!br.gov.caixa.ccr.negocio.AuditoriaBean
15:21:51,539 INFO  [org.jipijapa] (MSC service thread 1-3) JIPIORMV53020253: Cache de segundo nível habilitado para SIFEC-CCR-6.3.0-b4587.ear#fecDS
15:21:51,541 INFO  [org.jipijapa] (MSC service thread 1-3) JIPIORMV53020253: Cache de segundo nível habilitado para SIFEC-CCR-6.3.0-b4587.ear#CCR-PU
15:21:51,542 INFO  [org.jipijapa] (MSC service thread 1-3) JIPIORMV53020253: Cache de segundo nível habilitado para SIFEC-CCR-6.3.0-b4587.ear#SIEMP-PU
15:21:51,709 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 225) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'SIFEC-CCR-6.3.0-b4587.ear#fecDS'
15:21:51,709 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 241) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'SIFEC-CCR-6.3.0-b4587.ear#CCR-PU'
15:21:51,709 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 222) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'SIFEC-CCR-6.3.0-b4587.ear#SIEMP-PU'
15:21:51,948 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para SIFEC-CCR-6.3.0-b4587.ear/ccr-ejb.jar#dataguard
15:21:51,948 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para SIFEC-CCR-6.3.0-b4587.ear/ccr-ejb.jar#SiapxEjbIDMS
15:21:51,949 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para SIFEC-CCR-6.3.0-b4587.ear/ccr-ejb.jar#SiempEjbDB2
15:21:51,949 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para SIFEC-CCR-6.3.0-b4587.ear/ccr-ejb.jar#CCR-PU
15:21:51,949 INFO  [org.jipijapa] (MSC service thread 1-4) JIPIORMV53020253: Cache de segundo nível habilitado para SIFEC-CCR-6.3.0-b4587.ear/ccr-ejb.jar#SiccrEjbDB2
15:21:52,099 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 222) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'SIFEC-CCR-6.3.0-b4587.ear/ccr-ejb.jar#CCR-PU'
15:21:52,100 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 241) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'SIFEC-CCR-6.3.0-b4587.ear/ccr-ejb.jar#SiapxEjbIDMS'
15:21:52,103 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 236) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'SIFEC-CCR-6.3.0-b4587.ear/ccr-ejb.jar#dataguard'
15:21:52,107 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 217) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'SIFEC-CCR-6.3.0-b4587.ear/ccr-ejb.jar#SiempEjbDB2'
15:21:52,107 INFO  [org.jboss.as.jpa] (ServerService Thread Pool -- 243) WFLYJPA0010: Iniciando unidade de persistência (fase 2 de 2) Serviço'SIFEC-CCR-6.3.0-b4587.ear/ccr-ejb.jar#SiccrEjbDB2'
15:21:53,597 INFO  [org.jboss.weld.Bootstrap] (Weld Thread Pool -- 4) WELD-000119: Not generating any bean definitions from br.gov.caixa.arqrefservices.contrato.siban.SibanEjbServices because of underlying class loading error: Type br.gov.caixa.arqref.business.consultacontratos.services.siban.PlanilhaServiceIface from [Module "deployment.SIFEC-CCR-6.3.0-b4587.ear" from Service Module Loader] not found.  If this is unexpected, enable DEBUG logging to see the full error.
15:22:01,771 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 236) WFLYUT0021: Contexto web registrado: '/ccr-api' para servidor 'default-server'
15:22:01,784 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 216) WFLYSRV0013: "SIFEC-CCR-6.3.0-b4587.ear" reimplantado
[root@cbrdeapllx473 p585600]#
