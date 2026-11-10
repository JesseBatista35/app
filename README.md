Veja o que são, sem expor senha nenhuma (no 6.4; o comando mascara valores reais e mostra só as referências de vault):

grep -E 'SECRET|API_KEY|PASSWORD' /tmp/props_sirur.cli | sed -E 's/value="([^$][^"]*)"/value="***"/'

E veja se o 7.4 tem vault configurado (CLI do 471):

/host=*/core-service=vault:read-resource
7.4 sem vault (o mais provável): precisamos dos valores reais dessas properties. Quem tem é o dev ou o responsável pelo SIRUR (o resource name normalmente é um cli-ser-... e o secret vem do Keycloak). Não dá para extrair do vault do 6.4.
7.4 com vault FEC-SIRUR: copiamos como está.

2. Datasource: no 7.4 o jdbc/OracleSirurDS aponta para scan-oradesbr01.extra.caixa.gov.br:1521:ORADES01. Me mande:

o resultado do test-connection-in-pool (ficou sem resposta no seu print);
o grep do datasource no 6.4, para conferir se o SIRUR do 6.4 usa esse banco ou o oracle-nprd-1000 ... prim_D01NGSRV:
grep -A4 'OracleSirurDS"' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -E "jndi-name|connection-url|user-name" | sort -u
