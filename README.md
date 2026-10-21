85600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$
[p585600@caddeapllx2557 ~]$ cd /tmp && rm -rf bolchk && mkdir bolchk && cd bolchk
[p585600@caddeapllx2557 bolchk]$
[p585600@caddeapllx2557 bolchk]$
[p585600@caddeapllx2557 bolchk]$ unzip -p /opt/jboss-eap/standalone/deployments/boletoService-ear.ear META-INF/jboss-deployment-structure.xml
<?xml version="1.0" encoding="UTF-8"?>
<jboss-deployment-structure xmlns="urn:jboss:deployment-structure:1.2">

    <ear-subdeployments-isolated>false</ear-subdeployments-isolated>

    <deployment>
        <dependencies>
            <module name="deployment.sirotcon-ejb-2.3.0.1-farm.jar" export="true"/>
        </dependencies>
    </deployment>

</jboss-deployment-structure>
[p585600@caddeapllx2557 bolchk]$
[p585600@caddeapllx2557 bolchk]$
[p585600@caddeapllx2557 bolchk]$ unzip -o -q /opt/jboss-eap/standalone/deployments/boletoService-ear.ear 'boletoService-war-*.war'
[p585600@caddeapllx2557 bolchk]$
[p585600@caddeapllx2557 bolchk]$
[p585600@caddeapllx2557 bolchk]$ unzip -o -q boletoService-war-*.war 'WEB-INF/*.xml'
[p585600@caddeapllx2557 bolchk]$ grep -rn "sirotcon" WEB-INF/ 2>/dev/null
[p585600@caddeapllx2557 bolchk]$

