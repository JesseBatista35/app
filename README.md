sh-4.2$ find / -xdev \( -iname "sirot2.xml" -o -iname "map.properties" -o -iname "connector-log4j.xml" \) 2>/dev/null
-sh-4.2$ ls -la /log_jboss/sirot2/ 2>/dev/null
-sh-4.2$ grep -i "sirot" /opt/jboss/jboss-eap/standalone/configuration/standalone-full-ha.xml
                        <periodic-rotating-file-handler name="sirot" autoflush="true">
                                <file relative-to="jboss.server.log.dir" path="sirot.log"/>
                                <file relative-to="jboss.server.log.dir" path="sirot.log"/>
                        <logger category="br.gov.caixa.sirot" use-parent-handlers="false">
                                        <handler name="sirot"/>
-sh-4.2$
-sh-4.2$



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
