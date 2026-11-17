ls -d /opt/jboss/jboss-eap/hc/servers/*/
LOG=/opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log; ls -l $LOG
grep -aE "Keycloak subsystem override|ccr-api|SIFEC-CCR|WFLYSRV0016|WFLYSRV0010" $LOG | tail -20
