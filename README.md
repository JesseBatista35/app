
sh-5.1$ curl -s -o /dev/null -w "%{http_code}\n" http://localhost:8080/sihdg-api/
503
sh-5.1$ curl -s -o /dev/null -w "%{http_code}\n" http://localhost:9990/health/ready
503
sh-5.1$



oc rsh -n sihdg-des <pod-des> curl -s -o /dev/null -w "%{http_code}\n" http://localhost:8080/sihdg-api/health/ready
