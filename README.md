configuration/properties/connector-log4j.xml

<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE log4j:configuration SYSTEM "log4j.dtd">

<log4j:configuration xmlns:log4j="http://jakarta.apache.org/log4j/" >

        <appender name="connector-LogDefault-Appender" class="org.apache.log4j.RollingFileAppender">
            <param name="File" value="/log_jboss/config-log4j/connector/connector.log" />
            <param name="Append" value="true"></param>
            <param name="MaxFileSize" value="300MB" />
            <param name="MaxBackupIndex" value="99" />
            <layout class="org.apache.log4j.PatternLayout">
                      <param name="ConversionPattern" value="[%d{yyMMdd HH:mm:ss,SSS} %-5p %m%n"/>
            </layout>
        </appender>

        <appender name="connector-LogDefault-Appender-ceflib" class="org.apache.log4j.RollingFileAppender">
            <param name="File" value="/log_jboss/config-log4j/connector/connector-ceflib.log" />
            <param name="Append" value="true"></param>
            <param name="MaxFileSize" value="300MB" />
            <param name="MaxBackupIndex" value="99" />
            <layout class="org.apache.log4j.PatternLayout">
                      <param name="ConversionPattern" value="[%d{yyMMdd HH:mm:ss,SSS} %-5p %m%n"/>
            </layout>
        </appender>

        <appender name="connector-Monitor-appender" class="org.apache.log4j.FileAppender">
            <param name="File" value="/log_jboss/config-log4j/connector/monitor.log" />
            <param name="Append" value="true"></param>
            <layout class="org.apache.log4j.PatternLayout">
                      <param name="ConversionPattern" value="[%d{yyMMdd HH:mm:ss,SSS} %-5p %m%n"/>
            </layout>
        </appender>

        <appender name="connector-LogSrvConnection-appender" class="org.apache.log4j.FileAppender">
            <param name="File" value="/log_jboss/config-log4j/connector/server-connection.log" />
            <param name="Append" value="true"></param>
            <layout class="org.apache.log4j.PatternLayout">
                      <param name="ConversionPattern" value="[%d{yyMMdd HH:mm:ss,SSS} %-5p %m%n"/>
            </layout>
        </appender>

        <appender name="connector-LogCliConnection-appender" class="org.apache.log4j.FileAppender">
            <param name="File" value="/log_jboss/config-log4j/connector/client-connection.log" />
            <param name="Append" value="true"></param>
            <layout class="org.apache.log4j.PatternLayout">
                      <param name="ConversionPattern" value="[%d{yyMMdd HH:mm:ss,SSS} %-5p %m%n"/>
            </layout>
        </appender>

        <appender name="connector-LogAudit-appender" class="org.apache.log4j.FileAppender">
            <param name="File" value="/log_jboss/config-log4j/connector/auditor.log" />
            <param name="Append" value="true"></param>
            <layout class="org.apache.log4j.PatternLayout">
                      <param name="ConversionPattern" value="[%d{yyMMdd HH:mm:ss,SSS} %-5p %m%n"/>
            </layout>
        </appender>

        <appender name="connector-LogDefault-Appender-async" class="org.apache.log4j.AsyncAppender">
            <appender-ref ref="connector-LogDefault-Appender"/>
        </appender>

        <appender name="connector-LogDefault-Appender-async-ceflib" class="org.apache.log4j.AsyncAppender">
            <appender-ref ref="connector-LogDefault-Appender-ceflib"/>
        </appender>

        <appender name="connector-Monitor-appender-async" class="org.apache.log4j.AsyncAppender">
            <appender-ref ref="connector-Monitor-appender"/>
        </appender>

      <category name="br.gov.caixa.util">
            <priority value="INFO"/>
                <appender-ref ref="connector-LogDefault-Appender-async"/>
        </category>

      <category name="br.gov.caixa.iso">
            <priority value="INFO"/>
                <appender-ref ref="connector-LogDefault-Appender-async"/>
        </category>

      <category name="br.gov.caixa.sirot">
            <priority value="INFO"/>
                <appender-ref ref="connector-LogDefault-Appender-async"/>
        </category>

      <category name="br.gov.caixa.libsp">
            <priority value="INFO"/>
                <appender-ref ref="connector-LogDefault-Appender-async-ceflib"/>
        </category>

     <category name="SIROT2_AUDIT_LOG">
            <priority value="INFO"/>
                <appender-ref ref="connector-LogAudit-appender"/>
        </category>

      <category name="CONNECTOR_AUDIT_LOG">
            <priority value="INFO"/>
                <appender-ref ref="connector-LogAudit-appender"/>
        </category>

      <category name="CLI_CONNECTION_LOG">
            <priority value="INFO"/>
                <appender-ref ref="connector-LogCliConnection-appender"/>
        </category>

      <category name="SRV_CONNECTION_LOG">
            <priority value="INFO"/>
                <appender-ref ref="connector-LogSrvConnection-appender"/>
        </category>

        <category name="org.apache.log4j.xml">
              <priority value="INFO" />
        </category>

</log4j:configuration>


configuration/properties/map.properties

9702=cicsplex 9702 #SIWIN
#9602=cicsd2 34100 #SIIBC WO0000030357789
9602=cicsplex 9602  #SIIBC
#9692=cicsplex 9602  #SIIBC

#**** Estatistica *****************
# CICS????
0001=cicsplex 9702
0003=cicsplex 9602
#0002=cicsd2 34100 # WO0000030357789
#0004=cicsplex 9602


configuration/properties/siranpkg.nbc.properties


#############################################
#     SIRANPKG - Configuracoes SINBC        #
#############################################
nbc.ks=/apl/sinbc/keystore/.jx44699
nbc.pf=/apl/sinbc/pf/.xs35987
nbc.ks.type=JCEKS
nbc.xf=F8B95E98B00EEA151A0DC2BC8383EF409129319E6BD58375

#Versao antiga
#Configuracao SENHA_NUMERICA
nbc.1.lb=ibc.ran.sk.001
nbc.1.sk=1
#Configuracao SENHA_NAO_CORRENTISTA
nbc.2.lb=ibc.ran.sk.001
nbc.2.sk=1
#Configuracao HASH_MAC3DES
nbc.11.sk=0
nbc.11.lb=ibc.ran.sk.001
#Configuracao ASSINATURA ELETRONICA SIMPLES
nbc.3.sk=1
nbc.3.lb=ibc.ran.sk.001
#Configuracao ASSINATURA ELETRONICA MULTIPLA
nbc.13.sk=1
nbc.13.lb=ibc.ran.sk.001

#Configuracao B2B
nbc.16.sk=0
nbc.16.lb=ibc.sk.001


configuration/properties/sirot2.xml


<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE log4j:configuration SYSTEM "log4j.dtd">
<log4j:configuration xmlns:log4j='http://jakarta.apache.org/log4j/'>

    <appender name="SIROT2_AUDIT_LOG" class="org.apache.log4j.DailyRollingFileAppender">
        <param name="File" value="/log_jboss/sirot2/sirot2-${jboss.server.name}.log" />
        <param name="Append" value="true" />
        <param name="DatePattern" value="'.'dd" />
        <layout class="org.apache.log4j.PatternLayout">
                <param name="ConversionPattern" value="%d{HH:mm:ss} %5p [%t] (%F:%L) - %m%n"/>
        </layout>
    </appender>

    <category name="org.apache.log4j.xml">
        <priority value="debug" />
    </category>

    <category name="br.gov.caixa.sirot">
        <priority value="debug" />
        <appender-ref ref="SIROT2_AUDIT_LOG"/>
    </category>

</log4j:configuration>


configuration/custom-deploy.sh


#deploy modules
cd /opt/jboss-eap/standalone/deployments/
chown -R jboss:jboss /opt/jboss-eap/standalone/deployments/
unzip sigcx-parent.zip
chown -R jboss:jboss /opt/jboss-eap/standalone/deployments/
cd modules

mkdir /opt/jboss-eap/modules-caixa

unzip modules-local.zip -d /opt/jboss-eap/modules-caixa
chown -R jboss:jboss /opt/jboss-eap/modules-caixa
rm -Rf modules-local.zip

#deploy application
cd /opt/jboss-eap/standalone/deployments/deploy
unzip deploy-local.zip -d /opt/jboss-eap/standalone/deployments/
chown -R jboss:jboss /opt/jboss-eap/standalone/deployments/
rm -Rf deploy-local.zip

#deploy apache
cd /opt/jboss-eap/standalone/deployments/static

mkdir /opt/httpd/htdocs/sigcx-static
chown -R apache:apache /opt/httpd/htdocs/sigcx-static/
chomod 775 /opt/httpd/htdocs/sigcx-static
unzip static-local.zip -d /opt/httpd/htdocs/sigcx-static
rm -Rf static-local.zip
rm -Rf /opt/jboss-eap/standalone/deployments/sigcx-parent.zip
rm -Rf /opt/jboss-eap/standalone/deployments/deploy
rm -Rf /opt/jboss-eap/standalone/deployments/modules
rm -Rf /opt/jboss-eap/standalone/deployments/static

echo "job done"


configuration/custom.sh

# Caminho do arquivo de configuração
ARQUIVO="/opt/httpd/conf.modules.d/01-ldap.conf"

# Comenta todas as linhas que não estão comentadas
sed -i '/^[[:space:]]*[^#[:space:]]/s/^/#/' "$ARQUIVO"

echo "Criação de arquivo do sirot"

mkdir -p /log_jboss/connector

mkdir -p /log_jboss/config-log4j/sirot2/
mv /opt/jboss-eap/standalone/configuration/properties/sirot2.xml /log_jboss/config-log4j/sirot2/.
mkdir -p /log_jboss/config-log4j/connector/
mv /opt/jboss-eap/standalone/configuration/properties/connector-log4j.xml /log_jboss/config-log4j/connector/.
chown -R jboss:jboss /log_jboss

cd /
mkdir connector 
chown -R jboss:jboss /connector
cd /connector
wget https://binario.caixa/repository/thirdparty/br/gov/br/sigcx/sirot-gcx/2.0/sirot-gcx-2.0.zip
unzip sirot-gcx-2.0.zip

mv /opt/jboss-eap/standalone/configuration/properties/map.properties /connector/config/.
chown -R jboss:jboss .
pgrep -f start-connector.sh | xargs kill -9
run.sh start
rm sirot-gcx-2.0.zip

echo "Processo concluído."


