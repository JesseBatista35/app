POD=sicow-conres-okd-des-27-jftds
oc exec $POD -n sicow-des -- ls -la /opt/jboss/standalone/log/
oc exec $POD -n sicow-des -- grep -E "ModuleNotFound|WFLYUT0021|WFLYSRV0010|WFLYSRV0025|WFLYSRV0026|veio sem valor|Login failed|scowdb01|ERROR" /opt/jboss/standalone/log/server.log | head -40


oc exec $POD -n sicow-des -- grep -n -A8 "<root-logger>" /opt/jboss/standalone/configuration/standalone-okd.xml

