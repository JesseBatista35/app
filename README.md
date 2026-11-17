
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# grep -a "IJ031084\|IJ000453" $LOG | awk '{print $1}' | tail -20
15:30:03,401
15:30:03,435
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# tail -f $LOG | grep -aiE "ccr-api|IJ0|ORA-|ERROR"
15:33:08,173 WARN  [org.keycloak.adapters.RefreshableKeycloakSecurityContext] (default task-115) Refresh token failure status: 400 {"error":"invalid_grant","error_description":"Refresh token expired"}
15:33:08,414 WARN  [org.keycloak.adapters.RefreshableKeycloakSecurityContext] (default task-115) Refresh token failure status: 400 {"error":"invalid_grant","error_description":"Refresh token expired"}

