[domain@localhost:9999 /]
[domain@localhost:9999 /] /profile=full-ha-sifec-intranet/subsystem=mail:read-resource(recursive=true)
{
    "outcome" => "success",
    "result" => {"mail-session" => {
        "default" => {
            "debug" => false,
            "from" => undefined,
            "jndi-name" => "java:jboss/mail/Default",
            "custom" => undefined,
            "server" => {"smtp" => {
                "credential-reference" => undefined,
                "outbound-socket-binding-ref" => "mail-smtp",
                "password" => undefined,
                "ssl" => false,
                "tls" => false,
                "username" => undefined
            }}
        },
        "FECMail" => {
            "debug" => false,
            "from" => undefined,
            "jndi-name" => "java:jboss/mail/FECMail",
            "custom" => undefined,
            "server" => {"smtp" => {
                "credential-reference" => undefined,
                "outbound-socket-binding-ref" => "mail-smtp",
                "password" => undefined,
                "ssl" => false,
                "tls" => false,
                "username" => undefined
            }}
        },
        "APXMail" => {
            "debug" => false,
            "from" => undefined,
            "jndi-name" => "java:jboss/mail/APXMail",
            "custom" => undefined,
            "server" => {"smtp" => {
                "credential-reference" => undefined,
                "outbound-socket-binding-ref" => "mail-smtp",
                "password" => undefined,
                "ssl" => false,
                "tls" => false,
                "username" => undefined
            }}
        }
    }}
}

[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] /server-group=sifec-intranet:read-attribute(name=socket-binding-group)
{
    "outcome" => "success",
    "result" => "caixa-full-ha-sockets"
}

[domain@localhost:9999 /]



-sh-4.1$
-sh-4.1$
-sh-4.1$ sudo su
[sudo] password for p585600:
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]# D64=$(ps -ef | grep -o 'jboss.domain.base.dir=[^ ]*' | head -1 | cut -d= -f2)/configuration/domain.xml; echo $D64
[^/configuration/domain.xml
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]# grep -n -B2 -A8 "APXMail" $D64 | head -40
grep: [^/configuration/domain.xml: No such file or directory
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#


