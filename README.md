Agora, o datasource.

1. No 6.4, usuário e senha do OracleSirurDS (senha mascarada se for texto):

grep -A12 'jndi-name="java:/jdbc/OracleSirurDS"' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -E "user-name|password" | sed -E 's#<password>([^$][^<]*)</password>#<password>***</password>#' | sort -u

2. No 471 (CLI), aponte para o banco do 6.4 e veja o usuário atual:

/profile=full-ha-sifec-intranet/subsystem=datasources/data-source="jdbc/OracleSirurDS":write-attribute(name=connection-url,value="jdbc:oracle:thin:@oracle-nprd-1000.caixa:1521/prim_D01NGSRV")
/profile=full-ha-sifec-intranet/subsystem=datasources/data-source="jdbc/OracleSirurDS":read-attribute(name=user-name)

Me mande as duas saídas. Se o usuário do 7.4 bater com o do 6.4, já vamos para o restart, o teste de conexão e o deploy do SIRUR.
