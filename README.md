oc get pods -n sihdg-des
oc rsh -n sihdg-des -c <container> <pod-des> curl -s -o /dev/null -w "%{http_code}\n" http://localhost:8080/sihdg-api/health/ready
