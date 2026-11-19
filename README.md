No 473 (10.116.97.79), sifec-intranet:

bash
grep -a "consultarCorrelationClientePorCPF" /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | tail -3

No 409 (10.116.97.41), SIPEN:

bash
grep -a "consultarCorrelationClientePorCPF" /opt/jboss/jboss-eap/hc/servers/sipen_node1_DES_llx409/log/server.log | tail -3

O servidor que mostrar a linha das 15:08:52 é o certo. Depois, no mesmo log, olhamos o que veio junto:

bash
grep -a -A15 "15:08:52,769" <log onde apareceu> | grep -aE "ERROR|WARN|ARJUNA|Exception|MQJCA|JMS" | head -20

No documento de passagem, eu coloquei a Claudia como contato do SIPEN. Se ela for do CCR, ajusto antes de você mandar. Me confirma.
