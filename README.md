Veja o que são, sem expor senha nenhuma (no 6.4; o comando mascara valores reais e mostra só as referências de vault):

grep -E 'SECRET|API_KEY|PASSWORD' /tmp/props_sirur.cli | sed -E 's/value="([^$][^"]*)"/value="***"/'

E veja se o 7.4 tem vault configurado (CLI do 471):

/host=*/core-service=vault:read-resource
7.4 sem vault (o mais provável): precisamos dos valores reais dessas properties. Quem tem é o dev ou o responsável pelo SIRUR (o resource name normalmente é um cli-ser-... e o secret vem do Keycloak). Não dá para extrair do vault do 6.4.
7.4 com vault FEC-SIRUR: copiamos como está.

2. Datasource: no 7.4 o jdbc/OracleSirurDS aponta para scan-oradesbr01.extra.caixa.gov.br:1521:ORADES01. Me mande:

o resultado do test-connection-in-pool (ficou sem resposta no seu print);
o grep do datasource no 6.4, para conferir se o SIRUR do 6.4 usa esse banco ou o oracle-nprd-1000 ... prim_D01NGSRV:
grep -A4 'OracleSirurDS"' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -E "jndi-name|connection-url|user-name" | sort -u




-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$ grep -E 'SECRET|API_KEY|PASSWORD' /tmp/props_sirur.cli | sed -E 's/value="([^$][^"]*)"/value="***"/'
/server-group=sifec-intranet/system-property=SIRUR_SITAE_PASSWORD:add(value="${VAULT::SIRUR::password::1}")
/server-group=sifec-intranet/system-property=SIRUR_API_MANAGER_API_KEY:add(value="${VAULT::FEC-SIRUR::SirurAPIKey::1}")
/server-group=sifec-intranet/system-property=SIRUR_SSO_INTRANET_SERVICE_SECRET :add(value="${VAULT::FEC-SIRUR::SirurSSOIntraSecret::1}")
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$




[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$ grep -A4 'OracleSirurDS"' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -E "jndi-name|connection-url|user-name" | sort -u
grep: /opt/jboss/jboss-eap/dc/configuration/domain.xml: Permission denied
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$ sudo su

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for p585600:
[root@cbrdeapllx473 p585600]# grep -A4 'OracleSirurDS"' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -E "jndi-name|connection-url|user-name" | sort -u
grep: /opt/jboss/jboss-eap/dc/configuration/domain.xml: No such file or directory
[root@cbrdeapllx473 p585600]#





[root@cbrdeapllx471 p585600]# tail -900f /opt/jboss/jboss-eap/dc/log/host-controller.log
2026-11-05 16:37:57,671 INFO  [org.jboss.modules] (main) JBoss Modules version 1.12.3.Final-redhat-00001
2026-11-05 16:37:57,845 INFO  [org.jboss.msc] (main) JBoss MSC version 1.4.13.Final-redhat-00001
2026-11-05 16:37:57,853 INFO  [org.jboss.threads] (main) JBoss Threads version 2.4.0.Final-redhat-00001
2026-11-05 16:37:57,889 INFO  [org.jboss.as] (MSC service thread 1-2) WFLYSRV0049: JBoss EAP 7.4.23.GA (WildFly Core 15.0.43.Final-redhat-00001) starting
2026-11-05 16:37:58,188 INFO  [org.wildfly.security] (Host Controller Service Threads - 4) ELY00001: WildFly Elytron version 1.15.26.Final-redhat-00001
2026-11-05 16:37:58,419 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/host=DC_LX471/core-service=management/management-interface=native-interface' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:58,421 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/host=DC_LX471/core-service=management/management-interface=http-interface' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:58,482 INFO  [org.jboss.as.host.controller] (Controller Boot Thread) WFLYHC0003: Creating http management service using network interface (management) port (9990) securePort (9443)
2026-11-05 16:37:58,486 INFO  [org.xnio] (MSC service thread 1-1) XNIO version 3.8.16.Final-redhat-00001
2026-11-05 16:37:58,491 INFO  [org.xnio.nio] (MSC service thread 1-1) XNIO NIO Implementation Version 3.8.16.Final-redhat-00001
2026-11-05 16:37:58,524 INFO  [org.jboss.remoting] (MSC service thread 1-6) JBoss Remoting version 5.0.31.Final-redhat-00001
2026-11-05 16:37:58,536 INFO  [org.jboss.as.patching] (MSC service thread 1-1) WFLYPAT0050: JBoss EAP cumulative patch ID is: jboss-eap-7.4.23.CP, one-off patches include: none
2026-11-05 16:37:58,550 WARN  [org.jboss.as.domain.management.security] (MSC service thread 1-1) WFLYDM0111: Keystore /opt/jboss/jboss-eap/dc/configuration/application.keystore not found, it will be auto generated on first use with a self signed certificate for host localhost
2026-11-05 16:37:58,638 INFO  [org.jboss.as.remoting] (MSC service thread 1-1) WFLYRMT0001: Listening on 0.0.0.0:9999
2026-11-05 16:37:59,117 INFO  [org.jboss.as.controller.management-deprecated] (Host Controller Service Threads - 8) WFLYCTL0033: Extension 'security' is deprecated and may not be supported in future versions
2026-11-05 16:37:59,320 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'realm' in the resource at address '/core-service=management/access=authorization/role-mapping=SuperUser/include=group-EAPSEG@ldap_security_realm' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,320 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'realm' in the resource at address '/core-service=management/access=authorization/role-mapping=Administrator/include=group-EAPAUD@ldap_security_realm' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,321 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'realm' in the resource at address '/core-service=management/access=authorization/role-mapping=Administrator/include=group-EAPADM@ldap_security_realm' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,321 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'realm' in the resource at address '/core-service=management/access=authorization/role-mapping=Administrator/include=user-admin@ManagementRealm' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,321 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'realm' in the resource at address '/core-service=management/access=authorization/role-mapping=Administrator/include=user-rhqadmin@ManagementRealm' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,322 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'realm' in the resource at address '/core-service=management/access=authorization/role-mapping=Administrator/include=user-builduser@ManagementRealm' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,322 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'realm' in the resource at address '/core-service=management/access=authorization/role-mapping=Monitor/include=group-EAPMON@ldap_security_realm' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,322 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'realm' in the resource at address '/core-service=management/access=authorization/role-mapping=Auditor/include=group-EAPAUD@ldap_security_realm' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,360 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/profile=full-ha-sipen/subsystem=undertow/server=default-server/https-listener=https' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,386 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/profile=full-ha-sifec-intranet/subsystem=undertow/server=default-server/https-listener=https' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,421 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'security-realm' in the resource at address '/profile=full-ha-siemp/subsystem=undertow/server=default-server/https-listener=https' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,432 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'permgen-size' in the resource at address '/server-group=sifec-intranet/jvm=SIFEC-JVM' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,433 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'max-permgen-size' in the resource at address '/server-group=sifec-intranet/jvm=SIFEC-JVM' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,436 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'permgen-size' in the resource at address '/server-group=sipen/jvm=SIPEN-JVM' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,437 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'max-permgen-size' in the resource at address '/server-group=sipen/jvm=SIPEN-JVM' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,437 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'permgen-size' in the resource at address '/server-group=siemp/jvm=SIEMP-JVM' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,437 INFO  [org.jboss.as.controller.management-deprecated] (Controller Boot Thread) WFLYCTL0028: Attribute 'max-permgen-size' in the resource at address '/server-group=siemp/jvm=SIEMP-JVM' is deprecated, and may be removed in a future version. See the attribute description in the output of the read-resource-description operation to learn more about the deprecation.
2026-11-05 16:37:59,621 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0062: Http management interface listening on http://0.0.0.0:9990/management and https://0.0.0.0:9443/management
2026-11-05 16:37:59,622 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0053: Admin console listening on http://0.0.0.0:9990 and https://0.0.0.0:9443
2026-11-05 16:37:59,648 INFO  [org.jboss.as] (Controller Boot Thread) WFLYSRV0025: JBoss EAP 7.4.23.GA (WildFly Core 15.0.43.Final-redhat-00001) (Host Controller) started in 2234ms - Started 93 of 95 services (29 services are lazy, passive or on-demand)
2026-11-05 16:38:02,093 INFO  [org.jboss.as.domain.controller] (Host Controller Service Threads - 31) WFLYHC0019: Registered remote slave host "hc_cbrdeapllx409", JBoss JBoss EAP 7.4.23.GA (WildFly 15.0.43.Final-redhat-00001)
2026-11-05 16:38:02,151 INFO  [org.jboss.as.domain.controller] (Host Controller Service Threads - 13) WFLYHC0019: Registered remote slave host "hc_cbrdeapllx465", JBoss JBoss EAP 7.4.23.GA (WildFly 15.0.43.Final-redhat-00001)
2026-11-05 16:38:02,155 INFO  [org.jboss.as.domain.controller] (Host Controller Service Threads - 32) WFLYHC0019: Registered remote slave host "hc_cbrdeapllx472", JBoss JBoss EAP 7.4.23.GA (WildFly 15.0.43.Final-redhat-00001)
2026-11-05 16:38:02,357 INFO  [org.jboss.as.domain.controller] (Host Controller Service Threads - 16) WFLYHC0019: Registered remote slave host "hc_cbrdeapllx473", JBoss JBoss EAP 7.4.23.GA (WildFly 15.0.43.Final-redhat-00001)
2026-11-05 16:38:49,957 INFO  [org.jboss.as.domain.controller] (management task-1) WFLYHC0026: Unregistered remote slave host "hc_cbrdeapllx473"
2026-11-05 16:39:15,141 INFO  [org.jboss.as.domain.controller] (Host Controller Service Threads - 16) WFLYHC0019: Registered remote slave host "hc_cbrdeapllx473", JBoss JBoss EAP 7.4.23.GA (WildFly 15.0.43.Final-redhat-00001)
2026-11-05 16:47:58,063 INFO  [org.jboss.as.repository] (Host Controller Service Threads - 37) WFLYDR0009: Content /opt/jboss/jboss-eap/dc/data/content/29/9b09b502346548571cc855c752f855e3346ddc is obsolete and will be removed
2026-11-05 16:47:58,070 INFO  [org.jboss.as.repository] (Host Controller Service Threads - 37) WFLYDR0002: Content removed from location /opt/jboss/jboss-eap/dc/data/content/29/9b09b502346548571cc855c752f855e3346ddc/content
2026-11-06 09:45:55,512 INFO  [org.jboss.as.repository] (External Management Request Threads -- 5) WFLYDR0002: Content removed from location /opt/jboss/jboss-eap/dc/data/content/03/b848451079e2156d29d11ec81190040a02902d/content
2026-11-06 09:46:30,202 INFO  [org.jboss.as.repository] (External Management Request Threads -- 5) WFLYDR0001: Content added at location /opt/jboss/jboss-eap/dc/data/content/ea/786c0fdda41cc0ad6fcfbf29c2c623d1a3501e/content
2026-11-06 11:19:30,029 INFO  [org.jboss.as.repository] (External Management Request Threads -- 3) WFLYDR0001: Content added at location /opt/jboss/jboss-eap/dc/data/content/ce/315876195f5569b4389b610f7fe8b688279646/content
2026-11-06 11:19:30,303 INFO  [org.jboss.as.repository] (External Management Request Threads -- 3) WFLYDR0002: Content removed from location /opt/jboss/jboss-eap/dc/data/content/0f/71c92bc97f4eec8de36cb8e5c666b5ae743c48/content
2026-11-06 11:19:42,927 INFO  [org.jboss.as.repository] (External Management Request Threads -- 3) WFLYDR0002: Content removed from location /opt/jboss/jboss-eap/dc/data/content/ce/315876195f5569b4389b610f7fe8b688279646/content
2026-11-06 11:20:00,369 INFO  [org.jboss.as.repository] (External Management Request Threads -- 3) WFLYDR0001: Content added at location /opt/jboss/jboss-eap/dc/data/content/ce/315876195f5569b4389b610f7fe8b688279646/content
2026-11-06 14:25:59,857 INFO  [org.jboss.as.repository] (External Management Request Threads -- 3) WFLYDR0002: Content removed from location /opt/jboss/jboss-eap/dc/data/content/4b/d4e4cedd61737a5eee0cef13c73eb659879706/content
2026-11-06 14:26:12,724 INFO  [org.jboss.as.repository] (External Management Request Threads -- 3) WFLYDR0001: Content added at location /opt/jboss/jboss-eap/dc/data/content/4b/d4e4cedd61737a5eee0cef13c73eb659879706/content
2026-11-10 10:47:59,728 INFO  [org.jboss.as.repository] (External Management Request Threads -- 1) WFLYDR0002: Content removed from location /opt/jboss/jboss-eap/dc/data/content/53/4b22f779eab741838a0bd48c8bc42f3b82c3d4/content
2026-11-10 10:48:30,403 INFO  [org.jboss.as.repository] (External Management Request Threads -- 1) WFLYDR0001: Content added at location /opt/jboss/jboss-eap/dc/data/content/20/accb6adc13cf43dc9fd3971a3ee7cad4195a97/content
^C
[root@cbrdeapllx471 p585600]# /opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=localhost:9999
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] /host=*/core-service=vault:read-resource
{
    "outcome" => "success",
    "result" => [
        {
            "address" => [
                ("host" => "hc_cbrdeapllx473"),
                ("core-service" => "vault")
            ],
            "outcome" => "success",
            "result" => undefined
        },
        {
            "address" => [
                ("host" => "hc_cbrdeapllx472"),
                ("core-service" => "vault")
            ],
            "outcome" => "success",
            "result" => {
                "code" => undefined,
                "module" => undefined,
                "vault-options" => {
                    "KEYSTORE_URL" => "/opt/jboss/jboss-eap/modules/security/vaultcaixa_sirur.keystore",
                    "KEYSTORE_PASSWORD" => "MASK-lHQotGsUSmQ5YQRzdtNLD361rwn0c0oJ",
                    "KEYSTORE_ALIAS" => "SecurityK",
                    "SALT" => "87654321",
                    "ITERATION_COUNT" => "44",
                    "ENC_FILE_DIR" => "/opt/jboss/jboss-eap/modules/security/"
                }
            }
        },
        {
            "address" => [
                ("host" => "hc_cbrdeapllx465"),
                ("core-service" => "vault")
            ],
            "outcome" => "success",
            "result" => undefined
        },
        {
            "address" => [
                ("host" => "hc_cbrdeapllx409"),
                ("core-service" => "vault")
            ],
            "outcome" => "success",
            "result" => undefined
        }
    ]
}

[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] grep -A4 'OracleSirurDS"' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -E "jndi-name|connection-url|user-name" | sort -u
The closing '"' is missing.

[domain@localhost:9999 /]

