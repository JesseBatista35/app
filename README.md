/usr/java/openjdk-1.8.0.482/jre/bin/keytool -list -v -keystore /etc/pki/ca-trust/extracted/java/cacerts -storepass changeit | grep -iE "^(Alias|Owner).*(caixa|icp)"

