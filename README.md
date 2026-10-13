
-sh-4.2$ oc rsh -c sihdg-jboss8-tqs sihdg-jboss8-tqs-37-6llp9
error: Internal error occurred: error executing command in container: container is not created or running
-sh-4.2$ oc rsh -c sihdg-jboss8-tqs sihdg-jboss8-tqs-37-6llp9
sh-5.1$
sh-5.1$
sh-5.1$ curl -s -o /dev/null -w "%{http_code}\n" http://localhost:8080/sihdg-api/health/ready
404
sh-5.1$

