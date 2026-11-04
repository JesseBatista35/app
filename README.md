
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# mkdir -p /tmp/certs && cd /tmp/certs
[root@cbrdeapllx473 certs]#
[root@cbrdeapllx473 certs]#
[root@cbrdeapllx473 certs]# echo | openssl s_client -showcerts -connect login.des.caixa:443 2>/dev/null | awk '/BEGIN CERT/,/END CERT/' > login_chain.pem
[root@cbrdeapllx473 certs]#
[root@cbrdeapllx473 certs]#
[root@cbrdeapllx473 certs]# echo | openssl s_client -showcerts -connect api.des.caixa:8443 2>/dev/null | awk '/BEGIN CERT/,/END CERT/' > api_chain.pem
[root@cbrdeapllx473 certs]#
[root@cbrdeapllx473 certs]#
[root@cbrdeapllx473 certs]# grep -c "BEGIN CERT" *.pem
api_chain.pem:3
login_chain.pem:3
[root@cbrdeapllx473 certs]#


entao mais e desenvolvimento como esta em migraçao podemos resetar
