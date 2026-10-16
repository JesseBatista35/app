
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get project sihdg-tqs
NAME        DISPLAY NAME   STATUS
sihdg-tqs                  Active
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods
NAME                                              READY     STATUS      RESTARTS   AGE
quarkus-4-deploy                                  0/1       Completed   0          372d
siifx-api-aplicacao-des-2920-deploy               0/1       Completed   0          16h
siifx-api-aplicacao-des-2921-deploy               0/1       Completed   0          19m
siifx-api-aplicacao-des-2921-wdxpc                1/1       Running     0          19m
siifx-api-consulta-investi-des-37-deploy          0/1       Completed   0          111d
siifx-api-consulta-investi-des-38-deploy          0/1       Completed   0          107d
siifx-api-consulta-investi-des-38-gh474           1/1       Running     0          107d
siifx-api-informacoes-financeiras-des-21-deploy   0/1       Completed   0          142d
siifx-api-informacoes-financeiras-des-21-ps7wb    1/1       Running     0          142d
siifx-api-openfinance-des-16-deploy               0/1       Completed   0          142d
siifx-api-openfinance-des-16-rtwjt                1/1       Running     0          142d
siifx-caixinhas-api-aplicacao-des-84-deploy       0/1       Completed   0          19h
siifx-caixinhas-api-aplicacao-des-85-deploy       0/1       Completed   0          17h
siifx-caixinhas-api-aplicacao-des-85-f9zd7        1/1       Running     0          17h
siifx-web-des-292-deploy                          0/1       Completed   0          21h
siifx-web-des-293-deploy                          0/1       Completed   0          18h
siifx-web-des-293-nqvcr                           2/2       Running     0          18h
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc project sihdg-tqs
Now using project "sihdg-tqs" on server "https://api.nprd.caixa:6443".
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc get pods
NAME                            READY     STATUS      RESTARTS   AGE
sihdg-angular18-tqs-25-deploy   0/1       Completed   0          22h
sihdg-angular18-tqs-26-8zzpb    2/2       Running     0          13h
sihdg-angular18-tqs-26-deploy   0/1       Completed   0          13h
sihdg-backend-tqs-142-deploy    0/1       Completed   0          87d
sihdg-backend-tqs-143-deploy    0/1       Completed   0          41d
sihdg-backend-tqs-143-wltb8     1/1       Running     0          41d
sihdg-frontend-tqs-78-deploy    0/1       Completed   0          234d
sihdg-frontend-tqs-79-deploy    0/1       Completed   0          150d
sihdg-frontend-tqs-79-lb6fz     2/2       Running     0          150d
sihdg-jboss8-tqs-42-deploy      0/1       Completed   0          22h
sihdg-jboss8-tqs-43-deploy      0/1       Completed   0          12h
sihdg-jboss8-tqs-43-rtlxd       1/1       Running     0          12h
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ oc rsh ^C
-sh-4.2$ oc rsh sihdg-angular18-tqs-26-8zzpb
Error from server (NotFound): pods "sihdg-angular18-tqs-26-8zzpb" not found
-sh-4.2$ oc get pods
NAME                            READY     STATUS      RESTARTS   AGE
sihdg-angular18-tqs-26-deploy   0/1       Completed   0          13h
sihdg-angular18-tqs-27-86kt8    2/2       Running     0          84s
sihdg-angular18-tqs-27-deploy   0/1       Completed   0          87s
sihdg-backend-tqs-142-deploy    0/1       Completed   0          87d
sihdg-backend-tqs-143-deploy    0/1       Completed   0          41d
sihdg-backend-tqs-143-wltb8     1/1       Running     0          41d
sihdg-frontend-tqs-78-deploy    0/1       Completed   0          234d
sihdg-frontend-tqs-79-deploy    0/1       Completed   0          150d
sihdg-frontend-tqs-79-lb6fz     2/2       Running     0          150d
sihdg-jboss8-tqs-43-deploy      0/1       Completed   0          12h
sihdg-jboss8-tqs-44-6jtfq       1/1       Running     0          101s
sihdg-jboss8-tqs-44-deploy      0/1       Completed   0          104s
-sh-4.2$ oc rsh sihdg-angular18-tqs-27-86kt8
Defaulting container name to sihdg-angular18-tqs.
Use 'oc describe pod/sihdg-angular18-tqs-27-86kt8 -n sihdg-tqs' to see all of the containers in this pod.
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$ grep -rl "login.des" /opt/app-root/src /usr/share/nginx/html 2>/dev/null
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$ grep -rl "login.tqs" /opt/app-root/src /usr/share/nginx/html 2>/dev/null
sh-5.1$
sh-5.1$
sh-5.1$ cat /etc/nginx/conf.d/*.conf | grep proxy_pass      # valor real do __HTTP_SERVICE_API__
cat: '/etc/nginx/conf.d/*.conf': No such file or directory
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$ oc rsh ^C
sh-5.1$ oc rsh sihdg-backend-tqs-143-wltb8
sh: oc: command not found
sh-5.1$ oc rsh sihdg-backend-tqs-143-wltb8
sh: oc: command not found
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$ exit
exit
command terminated with exit code 127
-sh-4.2$ oc rsh sihdg-backend-tqs-143-wltb8
sh-4.2$
sh-4.2$
sh-4.2$ grep -n -iE "login\.(des|tqs)|auth-server-url|provider-url|realm" $JBOSS_HOME/standalone/configuration/standalone*.xml
/opt/jboss/standalone/configuration/standalone-full-ha.xml:41:        <security-realms>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:42:            <security-realm name="ManagementRealm">
/opt/jboss/standalone/configuration/standalone-full-ha.xml:50:            </security-realm>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:51:            <security-realm name="ApplicationRealm">
/opt/jboss/standalone/configuration/standalone-full-ha.xml:64:            </security-realm>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:65:        </security-realms>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:80:            <http-interface security-realm="ManagementRealm">
/opt/jboss/standalone/configuration/standalone-full-ha.xml:239:                <security-domain name="ApplicationDomain" default-realm="ApplicationRealm" permission-mapper="default-permission-mapper">
/opt/jboss/standalone/configuration/standalone-full-ha.xml:240:                    <realm name="ApplicationRealm" role-decoder="groups-to-roles"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:241:                    <realm name="local"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:243:                <security-domain name="ManagementDomain" default-realm="ManagementRealm" permission-mapper="default-permission-mapper">
/opt/jboss/standalone/configuration/standalone-full-ha.xml:244:                    <realm name="ManagementRealm" role-decoder="groups-to-roles"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:245:                    <realm name="local" role-mapper="super-user-mapper"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:248:            <security-realms>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:249:                <identity-realm name="local" identity="$local"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:250:                <properties-realm name="ApplicationRealm">
/opt/jboss/standalone/configuration/standalone-full-ha.xml:251:                    <users-properties path="application-users.properties" relative-to="jboss.server.config.dir" digest-realm-name="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:253:                </properties-realm>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:254:                <properties-realm name="ManagementRealm">
/opt/jboss/standalone/configuration/standalone-full-ha.xml:255:                    <users-properties path="mgmt-users.properties" relative-to="jboss.server.config.dir" digest-realm-name="ManagementRealm"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:257:                </properties-realm>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:258:            </security-realms>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:274:                <constant-realm-mapper name="local" realm-name="local"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:284:                            <mechanism-realm realm-name="ManagementRealm"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:291:                            <mechanism-realm realm-name="Application Realm"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:301:                        <mechanism mechanism-name="JBOSS-LOCAL-USER" realm-mapper="local"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:303:                            <mechanism-realm realm-name="ManagementRealm"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:309:                        <mechanism mechanism-name="JBOSS-LOCAL-USER" realm-mapper="local"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:311:                            <mechanism-realm realm-name="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:491:            <http-connector name="http-remoting-connector" connector-ref="default" security-realm="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:510:                        <login-module code="RealmDirect" flag="required">
/opt/jboss/standalone/configuration/standalone-full-ha.xml:556:                <https-listener name="https" socket-binding="https" security-realm="ApplicationRealm" enable-http2="true"/>
/opt/jboss/standalone/configuration/standalone-full-ha.xml:561:                    <http-invoker security-realm="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-full.xml:38:        <security-realms>
/opt/jboss/standalone/configuration/standalone-full.xml:39:            <security-realm name="ManagementRealm">
/opt/jboss/standalone/configuration/standalone-full.xml:47:            </security-realm>
/opt/jboss/standalone/configuration/standalone-full.xml:48:            <security-realm name="ApplicationRealm">
/opt/jboss/standalone/configuration/standalone-full.xml:61:            </security-realm>
/opt/jboss/standalone/configuration/standalone-full.xml:62:        </security-realms>
/opt/jboss/standalone/configuration/standalone-full.xml:77:            <http-interface security-realm="ManagementRealm">
/opt/jboss/standalone/configuration/standalone-full.xml:243:                <security-domain name="ApplicationDomain" default-realm="ApplicationRealm" permission-mapper="default-permission-mapper">
/opt/jboss/standalone/configuration/standalone-full.xml:244:                    <realm name="ApplicationRealm" role-decoder="groups-to-roles"/>
/opt/jboss/standalone/configuration/standalone-full.xml:245:                    <realm name="local"/>
/opt/jboss/standalone/configuration/standalone-full.xml:247:                <security-domain name="ManagementDomain" default-realm="ManagementRealm" permission-mapper="default-permission-mapper">
/opt/jboss/standalone/configuration/standalone-full.xml:248:                    <realm name="ManagementRealm" role-decoder="groups-to-roles"/>
/opt/jboss/standalone/configuration/standalone-full.xml:249:                    <realm name="local" role-mapper="super-user-mapper"/>
/opt/jboss/standalone/configuration/standalone-full.xml:252:            <security-realms>
/opt/jboss/standalone/configuration/standalone-full.xml:253:                <identity-realm name="local" identity="$local"/>
/opt/jboss/standalone/configuration/standalone-full.xml:254:                <properties-realm name="ApplicationRealm">
/opt/jboss/standalone/configuration/standalone-full.xml:255:                    <users-properties path="application-users.properties" relative-to="jboss.server.config.dir" digest-realm-name="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-full.xml:257:                </properties-realm>
/opt/jboss/standalone/configuration/standalone-full.xml:258:                <properties-realm name="ManagementRealm">
/opt/jboss/standalone/configuration/standalone-full.xml:259:                    <users-properties path="mgmt-users.properties" relative-to="jboss.server.config.dir" digest-realm-name="ManagementRealm"/>
/opt/jboss/standalone/configuration/standalone-full.xml:261:                </properties-realm>
/opt/jboss/standalone/configuration/standalone-full.xml:262:            </security-realms>
/opt/jboss/standalone/configuration/standalone-full.xml:278:                <constant-realm-mapper name="local" realm-name="local"/>
/opt/jboss/standalone/configuration/standalone-full.xml:288:                            <mechanism-realm realm-name="ManagementRealm"/>
/opt/jboss/standalone/configuration/standalone-full.xml:295:                            <mechanism-realm realm-name="Application Realm"/>
/opt/jboss/standalone/configuration/standalone-full.xml:305:                        <mechanism mechanism-name="JBOSS-LOCAL-USER" realm-mapper="local"/>
/opt/jboss/standalone/configuration/standalone-full.xml:307:                            <mechanism-realm realm-name="ManagementRealm"/>
/opt/jboss/standalone/configuration/standalone-full.xml:313:                        <mechanism mechanism-name="JBOSS-LOCAL-USER" realm-mapper="local"/>
/opt/jboss/standalone/configuration/standalone-full.xml:315:                            <mechanism-realm realm-name="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-full.xml:444:            <http-connector name="http-remoting-connector" connector-ref="default" security-realm="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-full.xml:463:                        <login-module code="RealmDirect" flag="required">
/opt/jboss/standalone/configuration/standalone-full.xml:501:                <https-listener name="https" socket-binding="https" security-realm="ApplicationRealm" enable-http2="true"/>
/opt/jboss/standalone/configuration/standalone-full.xml:506:                    <http-invoker security-realm="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:38:        <security-realms>
/opt/jboss/standalone/configuration/standalone-ha.xml:39:            <security-realm name="ManagementRealm">
/opt/jboss/standalone/configuration/standalone-ha.xml:47:            </security-realm>
/opt/jboss/standalone/configuration/standalone-ha.xml:48:            <security-realm name="ApplicationRealm">
/opt/jboss/standalone/configuration/standalone-ha.xml:61:            </security-realm>
/opt/jboss/standalone/configuration/standalone-ha.xml:62:        </security-realms>
/opt/jboss/standalone/configuration/standalone-ha.xml:77:            <http-interface security-realm="ManagementRealm">
/opt/jboss/standalone/configuration/standalone-ha.xml:238:                <security-domain name="ApplicationDomain" default-realm="ApplicationRealm" permission-mapper="default-permission-mapper">
/opt/jboss/standalone/configuration/standalone-ha.xml:239:                    <realm name="ApplicationRealm" role-decoder="groups-to-roles"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:240:                    <realm name="local"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:242:                <security-domain name="ManagementDomain" default-realm="ManagementRealm" permission-mapper="default-permission-mapper">
/opt/jboss/standalone/configuration/standalone-ha.xml:243:                    <realm name="ManagementRealm" role-decoder="groups-to-roles"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:244:                    <realm name="local" role-mapper="super-user-mapper"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:247:            <security-realms>
/opt/jboss/standalone/configuration/standalone-ha.xml:248:                <identity-realm name="local" identity="$local"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:249:                <properties-realm name="ApplicationRealm">
/opt/jboss/standalone/configuration/standalone-ha.xml:250:                    <users-properties path="application-users.properties" relative-to="jboss.server.config.dir" digest-realm-name="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:252:                </properties-realm>
/opt/jboss/standalone/configuration/standalone-ha.xml:253:                <properties-realm name="ManagementRealm">
/opt/jboss/standalone/configuration/standalone-ha.xml:254:                    <users-properties path="mgmt-users.properties" relative-to="jboss.server.config.dir" digest-realm-name="ManagementRealm"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:256:                </properties-realm>
/opt/jboss/standalone/configuration/standalone-ha.xml:257:            </security-realms>
/opt/jboss/standalone/configuration/standalone-ha.xml:273:                <constant-realm-mapper name="local" realm-name="local"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:283:                            <mechanism-realm realm-name="ManagementRealm"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:290:                            <mechanism-realm realm-name="Application Realm"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:300:                        <mechanism mechanism-name="JBOSS-LOCAL-USER" realm-mapper="local"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:302:                            <mechanism-realm realm-name="ManagementRealm"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:308:                        <mechanism mechanism-name="JBOSS-LOCAL-USER" realm-mapper="local"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:310:                            <mechanism-realm realm-name="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:452:            <http-connector name="http-remoting-connector" connector-ref="default" security-realm="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:471:                        <login-module code="RealmDirect" flag="required">
/opt/jboss/standalone/configuration/standalone-ha.xml:517:                <https-listener name="https" socket-binding="https" security-realm="ApplicationRealm" enable-http2="true"/>
/opt/jboss/standalone/configuration/standalone-ha.xml:522:                    <http-invoker security-realm="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-load-balancer.xml:10:        <security-realms>
/opt/jboss/standalone/configuration/standalone-load-balancer.xml:11:            <security-realm name="ManagementRealm">
/opt/jboss/standalone/configuration/standalone-load-balancer.xml:19:            </security-realm>
/opt/jboss/standalone/configuration/standalone-load-balancer.xml:20:            <security-realm name="ApplicationRealm">
/opt/jboss/standalone/configuration/standalone-load-balancer.xml:33:            </security-realm>
/opt/jboss/standalone/configuration/standalone-load-balancer.xml:34:        </security-realms>
/opt/jboss/standalone/configuration/standalone-load-balancer.xml:49:            <http-interface security-realm="ManagementRealm">
/opt/jboss/standalone/configuration/standalone-okd.xml:67:        <security-realms>
/opt/jboss/standalone/configuration/standalone-okd.xml:68:            <security-realm name="ManagementRealm">
/opt/jboss/standalone/configuration/standalone-okd.xml:76:            </security-realm>
/opt/jboss/standalone/configuration/standalone-okd.xml:77:            <security-realm name="ApplicationRealm">
/opt/jboss/standalone/configuration/standalone-okd.xml:90:            </security-realm>
/opt/jboss/standalone/configuration/standalone-okd.xml:91:        </security-realms>
/opt/jboss/standalone/configuration/standalone-okd.xml:106:            <http-interface security-realm="ManagementRealm">
/opt/jboss/standalone/configuration/standalone-okd.xml:289:                <security-domain name="ApplicationDomain" default-realm="ApplicationRealm" permission-mapper="default-permission-mapper">
/opt/jboss/standalone/configuration/standalone-okd.xml:290:                    <realm name="ApplicationRealm" role-decoder="groups-to-roles"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:291:                    <realm name="local"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:293:                <security-domain name="ManagementDomain" default-realm="ManagementRealm" permission-mapper="default-permission-mapper">
/opt/jboss/standalone/configuration/standalone-okd.xml:294:                    <realm name="ManagementRealm" role-decoder="groups-to-roles"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:295:                    <realm name="local" role-mapper="super-user-mapper"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:298:            <security-realms>
/opt/jboss/standalone/configuration/standalone-okd.xml:299:                <identity-realm name="local" identity="$local"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:300:                <properties-realm name="ApplicationRealm">
/opt/jboss/standalone/configuration/standalone-okd.xml:301:                    <users-properties path="application-users.properties" relative-to="jboss.server.config.dir" digest-realm-name="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:303:                </properties-realm>
/opt/jboss/standalone/configuration/standalone-okd.xml:304:                <properties-realm name="ManagementRealm">
/opt/jboss/standalone/configuration/standalone-okd.xml:305:                    <users-properties path="mgmt-users.properties" relative-to="jboss.server.config.dir" digest-realm-name="ManagementRealm"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:307:                </properties-realm>
/opt/jboss/standalone/configuration/standalone-okd.xml:308:            </security-realms>
/opt/jboss/standalone/configuration/standalone-okd.xml:324:                <constant-realm-mapper name="local" realm-name="local"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:334:                            <mechanism-realm realm-name="ManagementRealm"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:341:                            <mechanism-realm realm-name="Application Realm"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:351:                        <mechanism mechanism-name="JBOSS-LOCAL-USER" realm-mapper="local"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:353:                            <mechanism-realm realm-name="ManagementRealm"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:359:                        <mechanism mechanism-name="JBOSS-LOCAL-USER" realm-mapper="local"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:361:                            <mechanism-realm realm-name="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:456:            <http-connector name="http-remoting-connector" connector-ref="default" security-realm="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:475:                        <login-module code="RealmDirect" flag="required">
/opt/jboss/standalone/configuration/standalone-okd.xml:518:                <https-listener name="https" socket-binding="https" security-realm="ApplicationRealm" enable-http2="true"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:523:                    <http-invoker security-realm="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone-okd.xml:551:                <realm>intranet</realm>
/opt/jboss/standalone/configuration/standalone-okd.xml:553:                <auth-server-url>https://login.tqs.caixa/auth</auth-server-url>
/opt/jboss/standalone/configuration/standalone.xml:36:        <security-realms>
/opt/jboss/standalone/configuration/standalone.xml:37:            <security-realm name="ManagementRealm">
/opt/jboss/standalone/configuration/standalone.xml:45:            </security-realm>
/opt/jboss/standalone/configuration/standalone.xml:46:            <security-realm name="ApplicationRealm">
/opt/jboss/standalone/configuration/standalone.xml:59:            </security-realm>
/opt/jboss/standalone/configuration/standalone.xml:60:        </security-realms>
/opt/jboss/standalone/configuration/standalone.xml:75:            <http-interface security-realm="ManagementRealm">
/opt/jboss/standalone/configuration/standalone.xml:236:                <security-domain name="ApplicationDomain" default-realm="ApplicationRealm" permission-mapper="default-permission-mapper">
/opt/jboss/standalone/configuration/standalone.xml:237:                    <realm name="ApplicationRealm" role-decoder="groups-to-roles"/>
/opt/jboss/standalone/configuration/standalone.xml:238:                    <realm name="local"/>
/opt/jboss/standalone/configuration/standalone.xml:240:                <security-domain name="ManagementDomain" default-realm="ManagementRealm" permission-mapper="default-permission-mapper">
/opt/jboss/standalone/configuration/standalone.xml:241:                    <realm name="ManagementRealm" role-decoder="groups-to-roles"/>
/opt/jboss/standalone/configuration/standalone.xml:242:                    <realm name="local" role-mapper="super-user-mapper"/>
/opt/jboss/standalone/configuration/standalone.xml:245:            <security-realms>
/opt/jboss/standalone/configuration/standalone.xml:246:                <identity-realm name="local" identity="$local"/>
/opt/jboss/standalone/configuration/standalone.xml:247:                <properties-realm name="ApplicationRealm">
/opt/jboss/standalone/configuration/standalone.xml:248:                    <users-properties path="application-users.properties" relative-to="jboss.server.config.dir" digest-realm-name="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone.xml:250:                </properties-realm>
/opt/jboss/standalone/configuration/standalone.xml:251:                <properties-realm name="ManagementRealm">
/opt/jboss/standalone/configuration/standalone.xml:252:                    <users-properties path="mgmt-users.properties" relative-to="jboss.server.config.dir" digest-realm-name="ManagementRealm"/>
/opt/jboss/standalone/configuration/standalone.xml:254:                </properties-realm>
/opt/jboss/standalone/configuration/standalone.xml:255:            </security-realms>
/opt/jboss/standalone/configuration/standalone.xml:271:                <constant-realm-mapper name="local" realm-name="local"/>
/opt/jboss/standalone/configuration/standalone.xml:281:                            <mechanism-realm realm-name="ManagementRealm"/>
/opt/jboss/standalone/configuration/standalone.xml:288:                            <mechanism-realm realm-name="Application Realm"/>
/opt/jboss/standalone/configuration/standalone.xml:298:                        <mechanism mechanism-name="JBOSS-LOCAL-USER" realm-mapper="local"/>
/opt/jboss/standalone/configuration/standalone.xml:300:                            <mechanism-realm realm-name="ManagementRealm"/>
/opt/jboss/standalone/configuration/standalone.xml:306:                        <mechanism mechanism-name="JBOSS-LOCAL-USER" realm-mapper="local"/>
/opt/jboss/standalone/configuration/standalone.xml:308:                            <mechanism-realm realm-name="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone.xml:403:            <http-connector name="http-remoting-connector" connector-ref="default" security-realm="ApplicationRealm"/>
/opt/jboss/standalone/configuration/standalone.xml:422:                        <login-module code="RealmDirect" flag="required">
/opt/jboss/standalone/configuration/standalone.xml:465:                <https-listener name="https" socket-binding="https" security-realm="ApplicationRealm" enable-http2="true"/>
/opt/jboss/standalone/configuration/standalone.xml:470:                    <http-invoker security-realm="ApplicationRealm"/>
sh-4.2$
sh-4.2$
sh-4.2$ nv | grep -iE "sso|keycloak|oidc|login"
sh: nv: command not found
sh-4.2$ env | grep -iE "sso|keycloak|oidc|login"
sh-4.2$





<img width="1899" height="917" alt="image" src="https://github.com/user-attachments/assets/feeb6fc9-6671-4477-a8be-d9262531a4ef" />

