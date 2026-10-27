   oc logs sispi-qrcode-api-validador-des-297-fs9kn -n sispi-des --previous

      curl -s -w '\n%{http_code}\n' localhost:8080/q/health
   curl -s -w '\n%{http_code}\n' localhost:8080/q/health/live
   curl -s -w '\n%{http_code}\n' localhost:8080/q/health/ready

      oc rollout history dc/sispi-qrcode-api-validador-des -n sispi-des
   oc rollout history dc/sispi-qrcode-api-validador-des -n sispi-des --revision=297

   
