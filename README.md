oc rsh -c sihdg-jboss8-tqs sihdg-jboss8-tqs-37-6llp9
curl -s -o /dev/null -w "%{http_code}\n" http://localhost:8080/sihdg-api/health/ready

