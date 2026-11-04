/usr/java/openjdk-1.8.0.482/jre/bin/keytool -list -v -keystore /usr/java/openjdk-1.8.0.482/jre/lib/security/cacerts -storepass changeit | grep -iE "^(Alias|Owner).*(caixa|icp)"

find /opt/jboss /etc/pki /usr/java -iname "*.jks" -o -iname "*truststore*" -o -iname "cacerts*" 2>/dev/null | grep -v "/legal/" | head -20

