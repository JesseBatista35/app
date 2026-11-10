Comandos do SIRUR, em ordem:

1. CLI do 471 (10.116.97.59): qual pacote está no repositório

/opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=localhost:9999
/deployment=SIRUR:read-attribute(name=runtime-name)
/profile=full-ha-sifec-intranet/subsystem=datasources/data-source="jdbc/OracleSirurDS":read-attribute(name=connection-url)
/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473/subsystem=datasources/data-source="jdbc/OracleSirurDS":test-connection-in-pool
/profile=full-ha-sifec-intranet/subsystem=keycloak/secure-deployment=sirur-web.war:read-attribute(name=resource)

2. No 6.4 (sbrdeapllx0001): properties do SIRUR

sed -n '57701,58040p' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -E '<property name="SIRUR_' | sed -E 's#.*name="([^"]*)" value="([^"]*)".*#/server-group=sifec-intranet/system-property=\1:add(value="\2")#' > /tmp/props_sirur.cli; wc -l /tmp/props_sirur.cli
grep -viE 'SECRET|API_KEY|PASSWORD|SENHA' /tmp/props_sirur.cli

E o datasource do SIRUR no 6.4, para comparar (sem senha):

grep -A4 'OracleSirurDS"' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -E "jndi-name|connection-url|user-name" | sort -u

Me mande as saídas dos dois blocos. Com elas eu confiro os valores, te passo os comandos de aplicar as properties e o restart, e depois o deploy:

deploy --name=SIRUR --server-groups=sifec-intranet

(Esse último ainda não: só depois das properties e do restart.)
