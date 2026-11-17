
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# LOG=$(ps -ef | grep -o 'jboss.server.log.dir=[^ ]*' | grep sifec-intranet | head -1 | cut -d= -f2)/server.log; echo $LOG
grep -aE "Keycloak subsystem override|ccr-api|SIFEC-CCR|WFLYSRV0016|WFLYSRV0010" $LOG | tail -20
/opt/jboss/jboss-eap/hc/servers/sifec-intranet2_node1_llx473/log/server.log
16:59:42,539 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "framework_sisgd-1.0.0" (runtime-name : "framework_sisgd.jar")
16:59:42,539 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "SIFEC2" (runtime-name : "fec-2.160.0.0-b2435.ear")
17:31:51,700 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "framework-2.0.1-des.jar" (runtime-name : "framework.jar")
17:31:51,701 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "framework_sisgd-1.0.0" (runtime-name : "framework_sisgd.jar")
17:31:51,701 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "SIFEC2" (runtime-name : "fec-2.160.0.0-b2435.ear")
17:55:56,380 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "framework-2.0.1-des.jar" (runtime-name : "framework.jar")
17:55:56,381 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "framework_sisgd-1.0.0" (runtime-name : "framework_sisgd.jar")
17:55:56,381 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "SIFEC2" (runtime-name : "fec-2.160.0.0-b2435.ear")
18:05:47,665 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "framework-2.0.1-des.jar" (runtime-name : "framework.jar")
18:05:47,665 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "framework_sisgd-1.0.0" (runtime-name : "framework_sisgd.jar")
18:05:47,665 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "SIFEC2" (runtime-name : "fec-2.160.0.0-b2435.ear")
16:39:26,783 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "framework-2.0.1-des.jar" (runtime-name : "framework.jar")
16:39:26,783 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "framework_sisgd-1.0.0" (runtime-name : "framework_sisgd.jar")
16:39:26,783 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "SIFEC2" (runtime-name : "fec-2.160.0.0-b2435.ear")
11:08:27,240 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "framework-2.0.1-des.jar" (runtime-name : "framework.jar")
11:08:27,241 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "framework_sisgd-1.0.0" (runtime-name : "framework_sisgd.jar")
11:08:27,241 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "SIFEC2" (runtime-name : "fec-2.160.0.0-b2435.ear")
11:08:56,130 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "framework-2.0.1-des.jar" (runtime-name : "framework.jar")
11:08:56,130 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "framework_sisgd-1.0.0" (runtime-name : "framework_sisgd.jar")
11:08:56,130 INFO  [org.jboss.as.server] (Controller Boot Thread) WFLYSRV0010: Deployed "SIFEC2" (runtime-name : "fec-2.160.0.0-b2435.ear")
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
