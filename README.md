oc logs -n simpf-des simpf-backend-des-448-n4gpg | grep -A 40 "avisoGeral: java.lang.NullPointerException" | grep -E "NullPointer|Caused by|br.gov.caixa" | head -20

oc exec -n simpf-des simpf-backend-des-448-n4gpg -- sh -c 'echo | keytool -list -v -keystore /deployments/caixa-truststore-acteste-nprd.jks 2>/dev/null | grep -i "CN=SIGCT"'

oc exec -n simpf-tqs simpf-backend-tqs-290-rgftv -- env | grep -i sigct
oc exec -n simpf-tqs simpf-backend-tqs-290-rgftv -- ps -ef | grep -o "trustStore=[^ ]*"
