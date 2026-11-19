1. Confirmar no 473 (10.116.97.79):

bash
LOG=/opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log
grep -a "consultarCorrelationClientePorCPF" $LOG | tail -3
grep -a -A15 "15:08:52,769" $LOG | grep -aE "ERROR|WARN|ARJUNA|Exception|MQJCA|JMS" | head -20

2. WMQ no 7.4, profile do SIFEC (CLI do 471):

/profile=full-ha-sifec-intranet/subsystem=resource-adapters:read-resource(recursive=true)

3. WMQ no 6.4, só no profile do SIFEC (10.116.88.20). Primeiro, ver em quais profiles existe WMQ:

bash
D=/opt/jboss/jboss-eap/dc/configuration/domain.xml
grep -n '<profile name=' $D
grep -n 'resource-adapter id="wmq' $D

Me mande as três saídas. Cruzando os números de linha, descubro qual bloco de WMQ é do SIFEC e te passo o grep exato.

Sobre o documento: como não é do SIPEN, a Claudia provavelmente é do CCR. Na tabela de contatos, troque a linha dela de “SIPEN” para “CCR (teste no 7.4)” antes de mandar.
