
-sh-4.2$
-sh-4.2$
-sh-4.2$ grep -n -B2 -A12 'name="sirot"' /opt/jboss/jboss-eap/standalone/configuration/standalone-full-ha.xml
108-    <profile>
109-        <subsystem xmlns="urn:jboss:domain:logging:3.0">
110:                    <periodic-rotating-file-handler name="sirot" autoflush="true">
111-                            <formatter>
112-                                     <named-formatter name="PATTERN"/>
113-                            </formatter>
114-                            <file relative-to="jboss.server.log.dir" path="sirot.log"/>
115-                            <suffix value=".yyyy-MM-dd"/>
116-                            <append value="true"/>
117-                    </periodic-rotating-file-handler>
118-                    <periodic-rotating-file-handler name="ceflib" autoflush="true">
119-                            <formatter>
120-                                    <named-formatter name="PATTERN"/>
121-                            </formatter>
122-                            <file relative-to="jboss.server.log.dir" path="sirot.log"/>
--
150-                             <level name="DEBUG"/>
151-                            <handlers>
152:                                    <handler name="sirot"/>
153-                            </handlers>
154-                    </logger>
155-                    <logger category="br.gov.caixa.libsp" use-parent-handlers="false">
156-                             <level name="DEBUG"/>
157-                            <handlers>
158-                                    <handler name="ceflib"/>
159-                            </handlers>
160-                    </logger>
161-
162-            <logger category="com.arjuna">
163-                <level name="WARN"/>
164-            </logger>
-sh-4.2$
