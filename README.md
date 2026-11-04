/usr/java/openjdk-1.8.0.482/jre/bin/keytool -list -keystore /usr/java/openjdk-1.8.0.482/jre/lib/security/cacerts -storepass changeit | grep -iE "caixa|icp"

find /usr/java /usr/lib/jvm -name keytool 2>/dev/null
