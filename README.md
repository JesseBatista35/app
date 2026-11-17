LOG=$(ps -ef | grep -o 'jboss.server.log.dir=[^ ]*' | grep sifec-intranet | head -1 | cut -d= -f2)/server.log; echo $LOG
grep -aE "Keycloak subsystem override|ccr-api|SIFEC-CCR|WFLYSRV0016|WFLYSRV0010" $LOG | tail -20
