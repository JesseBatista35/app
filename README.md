for h in sihdg-jboss8-tqs.apps.nprd.caixa sihdg-angular18-tqs.apps.nprd.caixa; do
  echo "== $h"
  echo | openssl s_client -connect $h:443 -servername $h 2>/dev/null | openssl x509 -noout -subject -issuer -dates
done

