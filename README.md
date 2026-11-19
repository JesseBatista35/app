Para verificar (é do SIPEN, então no 409, IP 10.116.97.41)

1. O que mais aconteceu às 15:08:52:

bash
LOG=/opt/jboss/jboss-eap/hc/servers/sipen_node1_DES_llx409/log/server.log
grep -a -A15 "15:08:52,769" $LOG | grep -aE "ERROR|WARN|ARJUNA|Exception|MQJCA|JMS" | head -20

2. Comparar o WMQ, como ela pediu (CLI do 471):

/server-group=sipen:read-attribute(name=profile)

Com o profile que aparecer:

/profile=<profile que apareceu>/subsystem=resource-adapters:read-resource(recursive=true)

No 6.4 (10.116.88.20), sem mostrar senha:

bash
grep -n -A40 'wmq.jmsra' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -viE 'password' | head -80

Também vale conferir a versão: no 7.4 está ativo o wmq.jmsra.rar, enquanto no domain existem também o 7.0.1.12 e o 7.5.0.8 sem uso.
