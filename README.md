mkdir -p /tmp/certs && cd /tmp/certs
echo | openssl s_client -showcerts -connect login.des.caixa:443 2>/dev/null | awk '/BEGIN CERT/,/END CERT/' > login_chain.pem
echo | openssl s_client -showcerts -connect api.des.caixa:8443 2>/dev/null | awk '/BEGIN CERT/,/END CERT/' > api_chain.pem
grep -c "BEGIN CERT" *.pem

