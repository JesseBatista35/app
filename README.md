1. Restart (CLI do 471; aplica a URL nova e carrega as properties do SIRUR):

/server-group=sifec-intranet:restart-servers(blocking=true)
/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473:read-attribute(name=server-state)

Espere ficar running.

2. Teste do banco:

/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473/subsystem=datasources/data-source="jdbc/OracleSirurDS":test-connection-in-pool
[true]: pode seguir.
Falhar (ex.: ORA-01017 invalid username/password): a senha do 7.4 é diferente da do 6.4. Me mande o erro, que buscamos a senha.

3. Log no 473 (abra antes do deploy):

sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -E "WFLYSRV0010|WFLYCTL0013|WFLYUT0021|ERROR|VAULT|PBOX|WELD-00|RESTEASY003940|sirur|SIRUR"

4. Deploy do SIRUR (CLI do 471):

deploy --name=SIRUR --server-groups=sifec-intranet

O esperado é WFLYUT0021 ... /sirur-web e WFLYSRV0010: "SIRUR" foi implantado (sifec-sirur-2.9.3-b928.ear). O pacote também é do 6.4, então pode aparecer o mesmo WELD-001318 do Jackson que o RURAL teve. Se aparecer, me mande que montamos a mensagem para o dev.

Depois do restart, confira se o fec-web abre com estilo. Se não abrir: /server-group=sifec-intranet/deployment=SIFEC:redeploy.
