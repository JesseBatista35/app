Skip to main content
Azure DevOps
projetos
/
Caixa
/
Repos
/
Files
/

SIHDG-jboss8
Search


Caixa

Overview

Boards

Repos
Files
Commits
Pushes
Branches
Tags
Pull requests

Pipelines

Test Plans

Artifacts
Project settings
SIHDG-jboss8

api
src
main
java
br
gov
caixa
arquitetura
javaee
api
cadastrobasico
comum
config
dto
seguranca
keycloak
KeycloakHelper.java
KeycloakPrincipalHelper.java
OidcConfigurationProvider.java
OidcPrincipalHelper.java
AuditoriaWebHelper.java
UsuarioAutenticadoHelper.java
web
mapper
seguranca
sobre
javaee7
bsb
META-INF
resources
webapp
test
WebContent
nb-configuration.xml
pom.xml
core

3.22.0.2


/
javaee
/
api
/
comum
/
seguranca
/
keycloak
/
OidcConfigurationProvider.java
OidcConfigurationProvider.java

Edit

Contents
History
Compare
Blame

1234567891011121314151617181920212223242526272829303132333435363738394041424344
package br.gov.caixa.arquitetura.javaee.api.comum.seguranca.keycloak;

import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.wildfly.security.http.oidc.OidcSecurityContext;

import jakarta.enterprise.context.ApplicationScoped;
import jakarta.servlet.ServletContext;

/**
…        Object attr = servletContext.getAttribute(OidcSecurityContext.class.getName());

        if (attr instanceof OidcSecurityContext) {
            return (OidcSecurityContext) attr;
        }

        return null;
    }
}
Expanded

Collapsed




package br.gov.caixa.arquitetura.javaee.api.comum.seguranca.keycloak;

import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.wildfly.security.http.oidc.OidcSecurityContext;

import jakarta.enterprise.context.ApplicationScoped;
import jakarta.servlet.ServletContext;

/**
 * Provider para obter configurações OIDC do WildFly
 * 
 * Centraliza a lógica de leitura de configurações Keycloak
 */
@ApplicationScoped
public class OidcConfigurationProvider {

    private static final Logger LOG = LoggerFactory.getLogger(OidcConfigurationProvider.class);

    private static final String REALM = "intranet";
    private static final String CLIENT_ID = "cli-web-hdg";
    private static final String AUTH_SERVER_URL = "https://login.des.caixa/auth";
    private static final int TOKEN_LIFESPAN = 300;      // 5 min
    private static final int MAX_IDLE_TIME = -1;         // Sem limite

    public String getRealm() {
        return REALM;
    }

    public String getClientId() {
        return CLIENT_ID;
    }

    public String getAuthServerUrl() {
        return AUTH_SERVER_URL;
    }

    public Integer getTokenLifespan() {
        return TOKEN_LIFESPAN;
    }

    public Integer getMaxIdleTime() {
        return MAX_IDLE_TIME;
    }

    public OidcSecurityContext obterOidcSecurityContext(ServletContext servletContext) {
        if (servletContext == null) {
            return null;
        }

        Object attr = servletContext.getAttribute(OidcSecurityContext.class.getName());

        if (attr instanceof OidcSecurityContext) {
            return (OidcSecurityContext) attr;
        }

        return null;
    }
}
