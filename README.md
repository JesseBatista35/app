
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# /usr/java/openjdk-1.8.0.482/jre/bin/keytool -list -v -keystore /usr/java/openjdk-1.8.0.482/jre/lib/security/cacerts -storepass changeit | grep -iE "^(Alias|Owner).*(caixa|icp)"
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# find /opt/jboss /etc/pki /usr/java -iname "*.jks" -o -iname "*truststore*" -o -iname "cacerts*" 2>/dev/null | grep -v "/legal/" | head -20
/etc/pki/ca-trust/extracted/edk2/cacerts.bin
/etc/pki/ca-trust/extracted/java/cacerts
/etc/pki/java/cacerts
/usr/java/openjdk-1.8.0.482/jre/lib/security/cacerts
/usr/java/openjdk-1.8.0.482/sample/jmx/jmx-scandir/truststore
/usr/java/openjdk-17.0.6/lib/security/cacerts
[root@cbrdeapllx473 p585600]#


