
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$ /opt/server/bin/jboss-cli.sh -c --command='/system-property=SIHDG-SEC_URL_SERV_AUTH:add(value="https://login.tqs.caixa/auth")'
/opt/server/bin/jboss-cli.sh -c --command=':reload'
# aguardar subir e conferir:
curl -sk https://sihdg-jboss8-tqs.apps.nprd.caixa/sihdg-api/api/seguranca/configuracao-seguranca
{"outcome" => "success"}
{
    "outcome" => "success",
    "result" => undefined
}
{"realm":"intranet","idCliente":"cli-web-hdg","urlServidorAutorizacao":"https://login.des.caixa/auth","tempoVidaToken":300,"tempoMaximoIdle":-1,"versaoApi":"3.22.0.1"}sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$ until /opt/server/bin/jboss-cli.sh -c --command=':read-attribute(name=server-state)' 2>/dev/null | grep -q running; do sleep 3; done
sh-5.1$
sh-5.1$
sh-5.1$ /opt/server/bin/jboss-cli.sh -c --command='/deployment=sihdg-3.22.0.1.ear:read-attribute(name=status)'
/opt/server/bin/jboss-cli.sh -c --command='/system-property=SIHDG-SEC_URL_SERV_AUTH:read-resource'
curl -sk https://sihdg-jboss8-tqs.apps.nprd.caixa/sihdg-api/api/seguranca/configuracao-seguranca; echo
{
    "outcome" => "success",
    "result" => "OK"
}
{
    "outcome" => "failed",
    "failure-description" => "WFLYCTL0216: Management resource '[(\"system-property\" => \"SIHDG-SEC_URL_SERV_AUTH\")]' not found",
    "rolled-back" => true
}
{"realm":"intranet","idCliente":"cli-web-hdg","urlServidorAutorizacao":"https://login.des.caixa/auth","tempoVidaToken":300,"tempoMaximoIdle":-1,"versaoApi":"3.22.0.1"}
sh-5.1$
sh-5.1$
sh-5.1$
sh-5.1$ cd /tmp && python3 - <<'EOF'
import zipfile, io, re
ear = zipfile.ZipFile('/opt/server/standalone/deployments/sihdg-3.22.0.1.ear')
war = zipfile.ZipFile(io.BytesIO(ear.read('sihdg-api.war')))
core = zipfile.ZipFile(io.BytesIO(war.read('WEB-INF/lib/sihdg-core-3.22.0.1.jar')))
alvos = [(war, 'WEB-INF/classes/br/gov/caixa/arquitetura/javaee/api/comum/seguranca/keycloak/OidcConfigurationProvider.class'),
         (core, 'br/gov/caixa/arquitetura/javaee/core/comum/config/seguranca/SecuritySettings.class')]
for z, n in alvos:
    print('==', n.split('/')[-1])
    for s in re.findall(rb'[\x20-\x7e]{4,}', z.read(n)):
        s = s.decode()
        if not s.startswith(('(', 'L', 'java/', 'Ljava')) or 'SEC' in s or 'http' in s:
            print('  ', s)
EOF
== OidcConfigurationProvider.class
   <init>
   Vbr/gov/caixa/arquitetura/javaee/api/comum/seguranca/keycloak/OidcConfigurationProvider
   intranet
   cli-web-hdg
   https://login.des.caixa/auth
   valueOf
   2org/wildfly/security/http/oidc/OidcSecurityContext
   getName
   jakarta/servlet/ServletContext
   getAttribute
   &(Ljava/lang/String;)Ljava/lang/Object;
   org/slf4j/LoggerFactory
   getLogger
   %(Ljava/lang/Class;)Lorg/slf4j/Logger;
   REALM
   ConstantValue
   CLIENT_ID
   AUTH_SERVER_URL
   TOKEN_LIFESPAN
   MAX_IDLE_TIME
   Code
   this
   XLbr/gov/caixa/arquitetura/javaee/api/comum/seguranca/keycloak/OidcConfigurationProvider;
   getRealm
   getClientId
   getAuthServerUrl
   getTokenLifespan
   getMaxIdleTime
   obterOidcSecurityContext
   V(Ljakarta/servlet/ServletContext;)Lorg/wildfly/security/http/oidc/OidcSecurityContext;
   servletContext
    Ljakarta/servlet/ServletContext;
   attr
   StackMapTable
   <clinit>
   SourceFile
   OidcConfigurationProvider.java
   RuntimeVisibleAnnotations
   .Ljakarta/enterprise/context/ApplicationScoped;
== SecuritySettings.class
   >br/gov/caixa/arquitetura/javaee/core/comum/config/BaseSettings
   <init>
   SEC_URL_SERV_AUTH
   getSystemProperty
   &(Ljava/lang/String;)Ljava/lang/String;
   urlServAuth
   SEC_TEMPO_VIDA_TOKEN
   parseInt
   valueOf
   tempoVidaToken
   SEC_TEMPO_MAX_IDLE
   tempoMaximoIdle
   Code
   valor
   !Ljava/lang/NumberFormatException;
   this
   NLbr/gov/caixa/arquitetura/javaee/core/comum/config/seguranca/SecuritySettings;
   StackMapTable
   getUrlServAuth
   getTempoVidaToken
   getTempoMaximoIdle
   SourceFile
   SecuritySettings.java
sh-5.1$
sh-5.1$
sh-5.1$











