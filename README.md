
[root@caddeapllx2854 properties]#
[root@caddeapllx2854 properties]# head -3 /opt/jboss-eap/standalone/configuration/custom.sh
ls -la /log_jboss/config-log4j/ /apl/sigsj/properties/
ls -la /opt/jboss-eap/standalone/configuration/properties/   # tem que estar vazia
curl -s -o /dev/null -w "internet: %{http_code}\n" http://10.116.202.45/sigsj_internet/
# SIGSJ-internet - entrega a config externa que nao vem no EAR
# Os arquivos chegam via esteira em /opt/jboss-eap/standalone/configuration/properties/
# e sao movidos para o destino final na VM.
/apl/sigsj/properties/:
total 12
drwxr-xr-x 2 jboss jboss   79 nov 19 16:09 .
drwxr-xr-x 4 jboss jboss   35 nov 19 15:21 ..
-rw-r--r-- 1 jboss jboss 1351 nov 19 16:09 b2b.properties
-rw-r--r-- 1 jboss jboss  277 nov 19 16:09 config.properties
-rw-r--r-- 1 jboss jboss   22 nov 19 16:09 release.properties

/log_jboss/config-log4j/:
total 4
drwxr-xr-x 2 jboss jboss  32 nov 19 16:09 .
drwxr-xr-x 4 jboss jboss  48 nov 12 16:47 ..
-rw-r--r-- 1 jboss jboss 770 nov 19 16:09 sigsj_internet.xml
total 4
drwxr-xr-x 2 jboss jboss    6 nov 19 16:09 .
drwxrwxr-x 4 jboss jboss 4096 nov 19 16:09 ..
internet: 302
[root@caddeapllx2854 properties]#
[root@caddeapllx2854 properties]#
[root@caddeapllx2854 properties]#
[root@caddeapllx2854 properties]#



acho que da 302 porqeu eu ja troquei o usurio do banco a req para eguranca ja esta aberta



**
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]# head -3 /opt/jboss-eap/standalone/configuration/custom.sh
ls -la /log_jboss/config-log4j/ /apl/sigsj/properties/
curl -s -o /dev/null -w "boleto: %{http_code}\n" http://10.116.201.25/boletoService/contaJudicial
# SIGSJ-boleto - entrega a config externa que nao vem no EAR
# Os arquivos chegam via esteira em /opt/jboss-eap/standalone/configuration/properties/
# e sao movidos para o destino final na VM.
/apl/sigsj/properties/:
total 12
drwxr-xr-x 2 jboss jboss   79 nov 19 16:17 .
drwxr-xr-x 3 jboss jboss   24 nov 19 15:22 ..
-rw-r--r-- 1 jboss jboss 1348 nov 19 16:17 b2b.properties
-rw-r--r-- 1 jboss jboss  277 nov 19 16:17 config.properties
-rw-r--r-- 1 jboss jboss   22 nov 19 16:17 release.properties

/log_jboss/config-log4j/:
total 4
drwxr-xr-x 2 jboss jboss  33 nov 12 16:55 .
drwxr-xr-x 4 jboss jboss  48 nov 12 16:55 ..
-rw-r--r-- 1 jboss jboss 869 nov 12 16:55 sigsj_ws_boleto.xml
boleto: 200
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
[root@caddeapllx2557 properties]#
**
