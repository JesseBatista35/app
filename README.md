
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$ rm /tmp/domain.xml.bkp_ccr_20261117_1516
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$
[p585600@cbrdeapllx471 ~]$ sudo su

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for p585600:
[root@cbrdeapllx471 p585600]#
[root@cbrdeapllx471 p585600]#
[root@cbrdeapllx471 p585600]# /opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=localhost:9999
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] /opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=10.116.97.59:9990
Node path format is wrong around 'opt' (index=1).

[domain@localhost:9999 /] /opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=10.116.97.59:9990
Node path format is wrong around 'opt' (index=1).

[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] /profile=full-ha-sifec-intranet/subsystem=keycloak/secure-deployment=ccr-api.war:read-resource(recursive=true)
{
    "outcome" => "success",
    "result" => {
        "allow-any-hostname" => false,
        "always-refresh-token" => false,
        "auth-server-url" => undefined,
        "auth-server-url-for-backend-requests" => undefined,
        "autodetect-bearer-only" => false,
        "bearer-only" => true,
        "client-key-password" => undefined,
        "client-keystore" => undefined,
        "client-keystore-password" => undefined,
        "connection-pool-size" => undefined,
        "cors-allowed-headers" => undefined,
        "cors-allowed-methods" => undefined,
        "cors-max-age" => undefined,
        "disable-trust-manager" => false,
        "enable-basic-auth" => false,
        "enable-cors" => false,
        "expose-token" => false,
        "min-time-between-jwks-requests" => undefined,
        "principal-attribute" => undefined,
        "public-client" => false,
        "realm" => "internet",
        "realm-public-key" => undefined,
        "register-node-at-startup" => false,
        "register-node-period" => undefined,
        "resource" => "cli-ser-fec_api",
        "ssl-required" => "external",
        "token-minimum-time-to-live" => undefined,
        "token-store" => undefined,
        "truststore" => undefined,
        "truststore-password" => undefined,
        "turn-off-change-session-id-on-login" => false,
        "use-resource-role-mappings" => false,
        "credential" => undefined
    }
}

[domain@localhost:9999 /]
