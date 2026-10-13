oc get pod sihdg-jboss8-tqs-37-6llp9 -n sihdg-tqs
oc get events -n sihdg-tqs --field-selector involvedObject.name=sihdg-jboss8-tqs-37-6llp9 | tail

oc rsh -n sihdg-des -c sihdg-jboss8-des sihdg-jboss8-des-116-mq4ct curl -s -o /dev/null -w "%{http_code}\n" http://localhost:8080/sihdg-api/health/ready
