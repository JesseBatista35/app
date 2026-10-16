
-sh-4.2$
-sh-4.2$ for h in sihdg-jboss8-tqs.apps.nprd.caixa sihdg-angular18-tqs.apps.nprd.caixa; do
  echo "== $h"
  echo | openssl s_client -connect $h:443 -servername $h 2>/dev/null | openssl x509 -noout -subject -issuer -dates
done
== sihdg-jboss8-tqs.apps.nprd.caixa
subject= /C=BR/O=Caixa Economica Federal/CN=*.apps.nprd.caixa
issuer= /C=BR/O=Caixa Economica Federal/CN=AC Icptestes Sub
notBefore=Jul 18 15:07:38 2024 GMT
notAfter=Jul 18 15:17:38 2029 GMT
== sihdg-angular18-tqs.apps.nprd.caixa
subject= /C=BR/O=Caixa Economica Federal/CN=*.apps.nprd.caixa
issuer= /C=BR/O=Caixa Economica Federal/CN=AC Icptestes Sub
notBefore=Jul 18 15:07:38 2024 GMT
notAfter=Jul 18 15:17:38 2029 GMT
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
