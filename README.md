oc exec $POD -n sicow-des -- grep -n -A25 "Failed to process phase INSTALL" /opt/jboss/standalone/log/server.log | grep -iE "Caused by|WFLY|missing|jboss.naming|java:" | head -20
oc exec $POD -n sicow-des -- grep -n -A15 "WFLYCTL0013" /opt/jboss/standalone/log/server.log | head -30


<root-logger>
    <level name="INFO"/>
    <handlers>
        <handler name="CONSOLE"/>
        <handler name="FILE"/>
    </handlers>
</root-logger>

