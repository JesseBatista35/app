curl -s -o /dev/null -w "%{http_code}\n" http://localhost:8080/sihdg-api/
curl -s -o /dev/null -w "%{http_code}\n" http://localhost:9990/health/ready
