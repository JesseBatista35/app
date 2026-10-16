package br.gov.caixa.arquitetura.javaee.api.comum.seguranca.keycloak;

import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.wildfly.security.http.oidc.OidcSecurityContext;

import jakarta.enterprise.context.ApplicationScoped;
import jakarta.servlet.ServletContext;

/**
 * Provider para obter configurações OIDC do WildFly
 *
 * Centraliza a lógica de leitura de configurações Keycloak.
 * A URL do servidor de autorização é lida por ambiente via system property
 * (standalone.xml) ou variável de ambiente, mantendo o valor de DES apenas
 * como fallback.
 */
@ApplicationScoped
public class OidcConfigurationProvider {

    private static final Logger LOG = LoggerFactory.getLogger(OidcConfigurationProvider.class);

    private static final String REALM = "intranet";
    private static final String CLIENT_ID = "cli-web-hdg";
    private static final int TOKEN_LIFESPAN = 300;      // 5 min
    private static final int MAX_IDLE_TIME = -1;         // Sem limite

    private static final String PROP_AUTH_SERVER_URL = "SIHDG-SEC_URL_SERV_AUTH";
    private static final String ENV_AUTH_SERVER_URL = "SEC_URL_SERV_AUTH";
    private static final String AUTH_SERVER_URL_PADRAO = "https://login.des.caixa/auth";

    public String getRealm() {
        return REALM;
    }

    public String getClientId() {
        return CLIENT_ID;
    }

    public String getAuthServerUrl() {
        String url = System.getProperty(PROP_AUTH_SERVER_URL);
        if (url == null || url.isBlank()) {
            url = System.getenv(ENV_AUTH_SERVER_URL);
        }
        if (url == null || url.isBlank()) {
            LOG.warn("Propriedade {} não definida; usando padrão {}", PROP_AUTH_SERVER_URL, AUTH_SERVER_URL_PADRAO);
            return AUTH_SERVER_URL_PADRAO;
        }
        return url.trim();
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
