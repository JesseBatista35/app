h-5.1$
sh-5.1$
sh-5.1$ grep -n -iE "connection-url|jndi-name" /opt/server/standalone/configuration/standalone.xml
133:                <datasource jta="true" jndi-name="java:jboss/jdbc/sihdgDS" pool-name="sihdgDS" enabled="true" use-ccm="true">
134:                    <connection-url>jdbc:sqlserver://10.116.29.201:31153;DatabaseName=HDGDB001;encrypt=true;trustServerCertificate=true</connection-url>
160:                    <context-service name="default" jndi-name="java:jboss/ee/concurrency/context/default"/>
163:                    <managed-thread-factory name="default" jndi-name="java:jboss/ee/concurrency/factory/default" context-service="default"/>
166:                    <managed-executor-service name="default" jndi-name="java:jboss/ee/concurrency/executor/default" context-service="default" hung-task-termination-period="0" hung-task-threshold="60000" keepalive-time="5000"/>
169:                    <managed-scheduled-executor-service name="default" jndi-name="java:jboss/ee/concurrency/scheduler/default" context-service="default" hung-task-termination-period="0" hung-task-threshold="60000" keepalive-time="3000"/>
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$ tr '\0' '\n' < /proc/1/cmdline | grep -iE "^-D|login|sso"
sh-5.1$
sh-5.1$
sh-5.1$ grep -n "<property name" /opt/server/standalone/configuration/standalone.xml
28:        <property name="org.apache.catalina.connector.URI_ENCODING" value="UTF-8"/>
29:        <property name="org.jboss.as.web.default-encoding" value="UTF-8"/>
30:        <property name="SIHDG-classificacao.informacao" value="#INTERNO.CONFIDENCIAL"/>
31:        <property name="SIHDG-mail.avaliacao.derivativo" value="GEOMI@MAIL.CAIXA"/>
32:        <property name="SIHDG-mail.registro.efetividade" value="GEANF@MAIL.CAIXA,GEMOC@MAIL.CAIXA"/>
33:        <property name="SIHDG-mail.ordem.invalidacao" value="GEANF@MAIL.CAIXA"/>
34:        <property name="SIHDG-mail.ordem.cancelamento" value="GEOMI@MAIL.CAIXA"/>
35:        <property name="SIHDG-mail.ordem.execucao" value="GEANF@MAIL.CAIXA"/>
36:        <property name="SIHDG-mail.ordem.alteracao" value="GEOMI@MAIL.CAIXA"/>
37:        <property name="SIHDG-mail.ordem.insercao" value="GEOMI@MAIL.CAIXA"/>
38:        <property name="SIHDG-mail.endereco" value="gitecbr05@caixa.gov.br"/>
39:        <property name="SIHDG-ordem.alteracao.remetente" value="GEGAP"/>
40:        <property name="SIHDG-ordem.cancelamento.remetente" value="GEGAP"/>
41:        <property name="SIHDG-ordem.execucao.remetente" value="GETES"/>
42:        <property name="SIHDG-ordem.insercao.remetente" value="GEGAP"/>
43:        <property name="SIHDG-ordem.invalidacao.remetente" value="GESEN"/>
44:        <property name="SIHDG-derivativo.avaliacao.remetente" value="GEGAP"/>
45:        <property name="SIHDG-SEC_TEMPO_VIDA_TOKEN" value="5"/>
46:        <property name="SIHDG-DB_INTERNO" value="true"/>
47:        <property name="SIHDG-mail.smtp.host" value="smtptest.correiolivre.caixa"/>
48:        <property name="SIHDG-mail.smtp.port" value="25"/>
49:        <property name="SIHDG-MAIL_ENDERECO" value="gitecbr05@caixa.gov.br"/>
50:        <property name="SIHDG-MAIL_ORDEM_INSERCAO" value="GEOMI@MAIL.CAIXA"/>
51:        <property name="SIHDG-MAIL_ORDEM_ALTERACAO" value="GEOMI@MAIL.CAIXA"/>
52:        <property name="SIHDG-MAIL_ORDEM_CANCELAMENTO" value="GEOMI@MAIL.CAIXA"/>
53:        <property name="SIHDG-MAIL_ORDEM_EXECUCAO" value="GEANF@MAIL.CAIXA"/>
54:        <property name="SIHDG-MAIL_ORDEM_INVALIDACAO" value="GEANF@MAIL.CAIXA"/>
55:        <property name="SIHDG-MAIL_REGISTRO_EFETIVIDADE" value="GEANF@MAIL.CAIXA,GEMOC@MAIL.CAIXA"/>
56:        <property name="SIHDG-path.arquivo.sinaf" value="/sihdg_tqs/Arquivos_SINAF/"/>
124:                        <property name="@version" value="1"/>
304:                        <property name="wildfly.sasl.local-user.default-user" value="$local"/>
305:                        <property name="wildfly.sasl.local-user.challenge-path" value="${jboss.server.temp.dir}/auth"/>
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$ ls -la /opt/server/standalone/deployments/
total 50336
drwxrwxr-x. 1 jboss root       41 Oct 16 12:53 .
drwxrwxr-x. 1 jboss root       80 Oct 16 12:53 ..
-rw-rw-r--. 1 jboss root     8888 Oct 16 12:37 README.txt
-rw-rw-r--. 1 jboss root 51525334 Oct 16 12:37 sihdg-3.22.0.1.ear
-rw-r--r--. 1 jboss root       18 Oct 16 12:37 sihdg-3.22.0.1.ear.deployed
sh-5.1$
sh-5.1$
sh-5.1$ cd /tmp && python3 - <<'EOF'
> import zipfile, glob, re
for f in glob.glob('/opt/server/standalone/deployments/*.[wej]ar'):
    z = zipfile.ZipFile(f)
    for n in z.namelist():
        if n.endswith(('.properties','.yml','.yaml','.json','.xml','.class')):
            d = z.read(n)
            if b'login.des' in d or b'login.tqs' in d or b'urlServidorAutorizacao' in d:
                print(f, n)
EOF
sh-5.1$
sh-5.1$
sh-5.1$
