# 1) log externo da aplicação (onde o SIGSJ escreve)
ls -la /log_jboss/sigsj_internet/
tail -80 /log_jboss/sigsj_internet/sigsj_internet.log

# 2) qual server.log está ativo de verdade e o que tem de hoje
ls -la /opt/jboss-eap/standalone/log/
grep -n "2026-11-19 11:3" /opt/jboss-eap/standalone/log/server.log | tail -5
