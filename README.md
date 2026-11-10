1. No 6.4, veja usuário e senha do datasource do SIRUR (a senha sai mascarada se for texto e aparece se for vault):

grep -A12 'jndi-name="java:/jdbc/OracleSirurDS"' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -E "user-name|password" | sed -E 's#<password>([^$][^<]*)</password>#<password>***</password>#' | sort -u

2. No 6.4, corrija o nome com espaço no arquivo das properties e confira:

sed -i 's/SIRUR_SSO_INTRANET_SERVICE_SECRET :add/SIRUR_SSO_INTRANET_SERVICE_SECRET:add/' /tmp/props_sirur.cli
cut -d= -f3 /tmp/props_sirur.cli | cut -d: -f1

Devem aparecer os 6 nomes, sem espaço.

3. No 471 (CLI), cole as 6 linhas do cat /tmp/props_sirur.cli. Depois apague o arquivo no 6.4 (rm -f /tmp/props_sirur.cli).

4. No 471 (CLI), aponte o datasource para o banco do 6.4 e veja o usuário atual:

/profile=full-ha-sifec-intranet/subsystem=datasources/data-source="jdbc/OracleSirurDS":write-attribute(name=connection-url,value="jdbc:oracle:thin:@oracle-nprd-1000.caixa:1521/prim_D01NGSRV")
/profile=full-ha-sifec-intranet/subsystem=datasources/data-source="jdbc/OracleSirurDS":read-attribute(name=user-name)

Me mande o user-name do 7.4 e o resultado do passo 1. Se o usuário ou a senha forem diferentes, te passo o ajuste antes do restart.

5. Depois disso: restart, teste da conexão e deploy:

/server-group=sifec-intranet:restart-servers(blocking=true)
/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473/subsystem=datasources/data-source="jdbc/OracleSirurDS":test-connection-in-pool
deploy --name=SIRUR --server-groups=sifec-intranet

E o log no 473 (inclui erros de vault):

sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -E "WFLYSRV0010|WFLYCTL0013|ERROR|VAULT|vault|PBOX|sirur|SIRUR"
