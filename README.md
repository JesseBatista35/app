systemctl status jboss-eap-standalone --no-pager | head -15
echo "=== erros de boot ==="
grep -nE "ERROR|FATAL|Failed to|Exception" /opt/jboss-eap/standalone/log/server.log | tail -30
echo "=== fim do server.log ==="
tail -40 /opt/jboss-eap/standalone/log/server.log
echo "=== ta rodando agora? ==="
ps -ef | grep -v grep | grep -o "java.library.path=[^ ]*"
curl -s -o /dev/null -w "internet raiz: %{http_code}\n" http://10.116.202.45/sigsj_internet/
