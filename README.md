oc exec sicow-penhor-okd-des-68-qnfbk -n sicow-des -- ls -la /opt/jboss/standalone/configuration/ | grep -iE "vault|keystore|\.dat|jks"
oc get dc sicow-penhor-okd-des -n sicow-des -o yaml | grep -iE -B2 -A6 "vault|keystore"
