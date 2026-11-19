<img width="1694" height="989" alt="image" src="https://github.com/user-attachments/assets/9d09acc4-2774-4837-8b8c-71a9d165c84d" />



[root@caddeapllx955 apl]# cd
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]# echo "== custom.sh chegou? =="
head -3 /opt/jboss-eap/standalone/configuration/custom.sh
== custom.sh chegou? ==
# SIGSJ-intranet - entrega a config externa que nao vem no EAR
# Os arquivos chegam via esteira em /opt/jboss-eap/standalone/configuration/properties/
# e sao movidos para o destino final na VM.
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]# echo "== arquivos nos destinos =="
ls -la /log_jboss/config-log4j/
ls -la /apl/sigsj/properties/
== arquivos nos destinos ==
total 4
drwxr-xr-x 2 jboss jboss  32 nov 19 15:56 .
drwxr-xr-x 4 jboss jboss  48 nov 12 17:00 ..
-rw-r--r-- 1 jboss jboss 878 nov 19 15:56 sigsj_intranet.xml
total 12
drwxr-xr-x 2 jboss jboss   79 nov 19 15:56 .
drwxr-xr-x 3 jboss jboss   24 nov 19 15:17 ..
-rw-r--r-- 1 jboss jboss 1348 nov 19 15:56 b2b.properties
-rw-r--r-- 1 jboss jboss  277 nov 19 15:56 config.properties
-rw-r--r-- 1 jboss jboss   22 nov 19 15:56 release.properties
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]# echo "== a pasta de origem foi esvaziada pelo mv? =="
ls -la /opt/jboss-eap/standalone/configuration/properties/ 2>/dev/null
== a pasta de origem foi esvaziada pelo mv? ==
total 4
drwxr-xr-x 2 jboss jboss    6 nov 19 15:56 .
drwxrwxr-x 4 jboss jboss 4096 nov 19 15:56 ..
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]# echo "== app respondendo =="
curl -s -o /dev/null -w "intranet default.jsp: %{http_code}\n" http://10.116.194.179/sigsj_intranet/default.jsp
== app respondendo ==
intranet default.jsp: 200
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]#
[root@caddeapllx955 ~]#
