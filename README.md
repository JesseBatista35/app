1. SICDT 3.24.3.003 (o Jeferson está subindo)

O jeito certo é Replace no deployment existente SICDT-FEC (não Upload novo, senão os contextos conflitam).

Log no 473:

sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -E "WFLYSRV0010|WFLYSRV0016|WFLYCTL0013|WFLYUT0021|ERROR|WELD-00|RESTEASY|sicdt|sifec-cdt"

O esperado é:

WFLYUT0021 ... /sifec-cdt-web e /sicdt-orig-api-rest
WFLYSRV0016: Replaced deployment "sifec-cdt-3.24.3.001.ear" with "sifec-cdt-3.24.3.003.ear" (ou WFLYSRV0010 ... sifec-cdt-3.24.3.003.ear)

Confirmação no CLI do 471:

/deployment=SICDT-FEC:read-attribute(name=runtime-name)

O resultado deve ser sifec-cdt-3.24.3.003.ear.

Se o fec-web ficar sem css/js depois da troca (aconteceu com o PJ): /server-group=sifec-intranet/deployment=SIFEC:redeploy.

Mensagem para o Inocêncio quando subir:

Inocêncio, a versão sifec-cdt-3.24.3.003.ear foi republicada no SICDT-FEC (sifec-intranet). Contextos /sifec-cdt-web e /sicdt-orig-api-rest registrados. Pode validar.

2. SIRUR (preparação: rodar enquanto o SICDT sobe)

No 7.4 faltam as properties do SIRUR (a comparação de sexta mostrou: SIRUR_AMBIENTE, SIRUR_API_MANAGER_API_KEY, SIRUR_SITAE_*, SIRUR_SSO_INTRANET_SERVICE_*). O datasource jdbc/OracleSirurDS e o secure-deployment sirur-web.war já existem.

a) Pacote no repositório e versão (CLI do 471):

/deployment=SIRUR:read-attribute(name=runtime-name)

Confirme na planilha do Paulo se é essa versão que deve subir.

b) Gerar as properties do SIRUR no 6.4 (mesmo método do PJ):

sed -n '57701,58040p' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -E '<property name="SIRUR_' | sed -E 's#.*name="([^"]*)" value="([^"]*)".*#/server-group=sifec-intranet/system-property=\1:add(value="\2")#' > /tmp/props_sirur.cli; wc -l /tmp/props_sirur.cli
grep -viE 'SECRET|API_KEY|PASSWORD|SENHA' /tmp/props_sirur.cli

Me mande a saída do grep (sem os segredos) para eu conferir se algum valor aponta para o 6.4.

c) Conferir o datasource do SIRUR no 7.4 (CLI do 471):

/profile=full-ha-sifec-intranet/subsystem=datasources/data-source="jdbc/OracleSirurDS":read-attribute(name=connection-url)
/host=hc_cbrdeapllx473/server=sifec-intranet_node1_lx473/subsystem=datasources/data-source="jdbc/OracleSirurDS":test-connection-in-pool

Depois de aplicar as properties e fazer o restart, subimos o SIRUR com deploy --name=SIRUR --server-groups=sifec-intranet e acompanhamos o log.
