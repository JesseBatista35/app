
-sh-4.2$
-sh-4.2$
-sh-4.2$ ls -la /opt/jboss/jboss-eap/standalone/deployments/ | grep -i sirot
-rw-r--r-- 1 jboss jboss   450031 Nov 19  2020 sirotcon-ejb.jar
-rw-r--r-- 1 jboss jboss       16 Nov 19  2020 sirotcon-ejb.jar.deployed
-rw-r--r-- 1 jboss jboss   211362 Nov 19  2020 ValidaSirotcon.war
-rw-r--r-- 1 jboss jboss       18 Nov 19  2020 ValidaSirotcon.war.deployed
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ grep -i "sirot" /logs/jboss/jboss-eap/standalone/sigsj-internet/server.log | grep -iE "WFLYSRV0010|implantado" | head -5
2026-10-20 16:07:14,064 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 43) WFLYSRV0010: Implantado "ValidaSirotcon.war" (runtime-name: "ValidaSirotcon.war")
2026-10-20 16:07:14,064 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 43) WFLYSRV0010: Implantado "sirotcon-ejb.jar" (runtime-name: "sirotcon-ejb.jar")
-sh-4.2$
