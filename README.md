
/usr/java/openjdk-1.8.0.482/sample/jmx/jmx-scandir/truststore
/usr/java/openjdk-17.0.6/lib/security/cacerts
[root@cbrdeapllx473 p585600]# /usr/java/openjdk-1.8.0.482/jre/bin/keytool -list -v -keystore /etc/pki/ca-trust/extracted/java/cacerts -storepass changeit | grep -iE "^(Alias|Owner).*(caixa|icp)"
Alias name: cadsvitrlx271.intra.caixa.gov.br
Owner: CN=cadsvitrlx271.intra.caixa.gov.br, OU=SomeOrgUnit, O=Katello, L=Raleigh, ST=North Carolina, C=US
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#

