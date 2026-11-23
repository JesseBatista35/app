
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# ps -ef | grep -v grep | grep -o "java.library.path=[^ ]*"
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# cp -p /opt/jboss-eap/bin/standalone.conf /opt/jboss-eap/bin/standalone.conf.bkp_20261123
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# echo '' >> /opt/jboss-eap/bin/standalone.conf
echo '# SIGSJ - lib nativa SenhasSIIBC (criptografia SIPER/SIROT)' >> /opt/jboss-eap/bin/standalone.conf
echo 'JAVA_OPTS="$JAVA_OPTS -Djava.library.path=/apl/sigsj/lib"' >> /opt/jboss-eap/bin/standalone.conf
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# systemctl restart jboss-eap-standalone
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# ps -ef | grep -v grep | grep -o "java.library.path=[^ ]*"   # tem que mostrar /apl/sigsj/lib
java.library.path=/apl/sigsj/lib
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]# grep -nE "ERROR|SenhasSIIBC|ORA-|SIROT|getResponse|Connection" /log_jboss/sigsj_internet/sigsj_internet.log | tail -20
grep: /log_jboss/sigsj_internet/sigsj_internet.log: arquivo binário coincide com o padrão
17:[ INFO] 2026/11/23 03:37:38 connector.deployment[MSC service thread 1-3] - WFLYJCA0011: Sem limite de conectores de Jakarta ConnectionFactory [java:/JmsXA]
57:[ERROR] 2026/11/23 03:41:45 undertow.request[default task-3] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
58:java.lang.UnsatisfiedLinkError: no SenhasSIIBC in java.library.path
62:     at br.gov.caixa.util.SenhasSIIBC.<clinit>(Unknown Source)
110:[ERROR] 2026/11/23 03:41:51 undertow.request[default task-3] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
111:java.lang.NoClassDefFoundError: Could not initialize class br.gov.caixa.util.SenhasSIIBC
161:[ERROR] 2026/11/23 08:45:43 undertow.request[default task-3] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
162:java.lang.NoClassDefFoundError: Could not initialize class br.gov.caixa.util.SenhasSIIBC
210:[ERROR] 2026/11/23 08:45:49 undertow.request[default task-5] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
211:java.lang.NoClassDefFoundError: Could not initialize class br.gov.caixa.util.SenhasSIIBC
259:[ERROR] 2026/11/23 08:45:57 undertow.request[default task-5] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
260:java.lang.NoClassDefFoundError: Could not initialize class br.gov.caixa.util.SenhasSIIBC
308:[ERROR] 2026/11/23 08:46:13 undertow.request[default task-5] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
309:java.lang.NoClassDefFoundError: Could not initialize class br.gov.caixa.util.SenhasSIIBC
357:[ERROR] 2026/11/23 08:48:58 undertow.request[default task-5] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
358:java.lang.NoClassDefFoundError: Could not initialize class br.gov.caixa.util.SenhasSIIBC
406:[ERROR] 2026/11/23 09:46:57 undertow.request[default task-5] - UT005023: Exception handling request to /sigsj_internet/Autenticacao
407:java.lang.NoClassDefFoundError: Could not initialize class br.gov.caixa.util.SenhasSIIBC
466:[ INFO] 2026/11/23 10:35:07 connector.deployment[MSC service thread 1-4] - WFLYJCA0011: Sem limite de conectores de Jakarta ConnectionFactory [java:/JmsXA]
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
[root@caddeapllx2854 ~]#
