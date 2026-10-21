oc logs -n simpf-des simpf-backend-des-448-n4gpg | grep -vE '^\s+at ' \
  | grep -iE "exception|error|sctdeapllx0018|sigct|pkix|handshake|timed out|refused" | tail -40

  oc exec -n simpf-des simpf-backend-des-448-n4gpg -- env | grep -iE "sigct|sctde|8443|url"

  openssl s_client -connect 10.116.83.19:8443 -servername sctdeapllx0018.df.caixa </dev/null 2>/dev/null | openssl x509 -noout -subject -issuer -dates
