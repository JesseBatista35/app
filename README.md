
-sh-4.2$ oc logs -n sipdm-des sipdm-api-estudante-des-265-xnh9d --since=10m | grep -vE '^\s+at ' | grep -iE "exception|error|caused|timed out|login failed|connection" | tail -40
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n sipdm-des sipdm-api-estudante-des-265-xnh9d -- sh -c 'env | grep -iE "jdbc|datasource|db_"; ls /usr/src/app/secrets_files/SIPDM_DES'
QUARKUS_DATASOURCE_USERNAME=SPDMDS01
QUARKUS_DATASOURCE_JDBC_URL=jdbc:sqlserver://10.116.100.127:1433;databaseName=PDMDB001;encrypt=false;
NSS_SDB_USE_CACHE=no
QUARKUS_DATASOURCE_PASSWORD=${SPDMDS01_MSSQL}
CLISERPDM_SSO_DES2
CLISERPDM_SSO_DES2_Metadata
CLISERPDM_SSO_INTER
CLISERPDM_SSO_INTER_Metadata
CLISERPDM_SSO_INTRA
CLISERPDM_SSO_INTRA_Metadata
SIPDM_APIKEY_INTRA
SIPDM_APIKEY_INTRA_Metadata
SPDMDS01_MSSQL
SPDMDS01_MSSQL_Metadata
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc exec -n sipdm-des sipdm-api-estudante-des-265-xnh9d -- timeout 10 bash -c 'cat < /dev/null > /dev/tcp/<host-sqlserver>/1433' && echo OK || echo FALHA
bash: /dev/tcp/: Is a directory
command terminated with exit code 1
FALHA
-sh-4.2$
