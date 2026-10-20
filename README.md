cd /opt/jboss/jboss-eap/standalone/deployments/
unzip -p sirotcon-ejb.jar META-INF/MANIFEST.MF | grep -iE "version|build"
unzip -l sirotcon-ejb.jar | grep -i pom.properties
unzip -p sirotcon-ejb.jar 'META-INF/maven/*/pom.properties' 2>/dev/null


<img width="1867" height="911" alt="image" src="https://github.com/user-attachments/assets/23802da8-bced-4dbe-b376-fbbca17387c0" />


achamos esse exemplo aqui.. 

