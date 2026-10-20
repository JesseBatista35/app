cd /opt/jboss/jboss-eap/standalone/deployments/
unzip -p sirotcon-ejb.jar META-INF/MANIFEST.MF | grep -iE "version|build"
unzip -l sirotcon-ejb.jar | grep -i pom.properties
unzip -p sirotcon-ejb.jar 'META-INF/maven/*/pom.properties' 2>/dev/null
