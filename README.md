
sh-5.1$
sh-5.1$ cd /tmp && python3 - <<'EOF'
import zipfile, io, re
cnt = {'arq':0, 'cls':0}
def scan(z, path):
    for n in z.namelist():
        d = z.read(n)
        if n.endswith(('.war','.jar')):
            print('abrindo', path+'!/'+n)
            try: scan(zipfile.ZipFile(io.BytesIO(d)), path+'!/'+n)
            except Exception as e: print('  falhou:', e)
            continue
        cnt['arq'] += 1
        if n.endswith('.class'): cnt['cls'] += 1
        hits = set(re.findall(rb'login\.(?:des|tqs)\.caixa[^\x00"\s]*|SIHDG-SEC_\w+|SEC_\w+|urlServidorAutorizacao|configuracao-seguranca', d))
        if hits: print('>>', path+'!/'+n, sorted(h.decode(errors="ignore") for h in hits))
scan(zipfile.ZipFile('/opt/server/standalone/deployments/sihdg-3.22.0.1.ear'), 'ear')
print(cnt)
EOF
abrindo ear!/sihdg-api.war
>> ear!/sihdg-api.war!/WEB-INF/web.xml ['configuracao-seguranca']
>> ear!/sihdg-api.war!/WEB-INF/classes/br/gov/caixa/arquitetura/javaee/api/comum/dto/ConfiguracoesSegurancaDTO.class ['urlServidorAutorizacao']
>> ear!/sihdg-api.war!/WEB-INF/classes/br/gov/caixa/arquitetura/javaee/api/comum/seguranca/keycloak/OidcConfigurationProvider.class ['login.des.caixa/auth']
>> ear!/sihdg-api.war!/WEB-INF/classes/br/gov/caixa/arquitetura/javaee/api/seguranca/ConfiguracaoSegurancaController.class ['configuracao-seguranca']
abrindo ear!/sihdg-api.war!/WEB-INF/lib/sihdg-core-3.22.0.1.jar
>> ear!/sihdg-api.war!/WEB-INF/lib/sihdg-core-3.22.0.1.jar!/br/gov/caixa/arquitetura/javaee/core/comum/config/seguranca/SecuritySettings.class ['SEC_TEMPO_MAX_IDLE', 'SEC_TEMPO_VIDA_TOKEN', 'SEC_URL_SERV_AUTH']
abrindo ear!/sihdg-api.war!/WEB-INF/lib/hazelcast-3.12.12.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/hazelcast-client-3.12.12.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jackson-annotations-2.15.2.redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jasperreports-6.6.0.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/commons-collections-3.2.2.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/commons-digester-2.1.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jcommon-1.0.23.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jfreechart-1.0.19.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/ecj-4.4.2.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/castor-xml-1.3.3.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/castor-core-1.3.3.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/commons-lang-2.6.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/javax.inject-1.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/stax-1.2.0.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/stax-api-1.0.1.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/stax-api-1.0-2.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/icu4j-57.1.jar
>> ear!/sihdg-api.war!/WEB-INF/lib/icu4j-57.1.jar!/com/ibm/icu/impl/coll/Collation.class ['SEC_AND_TER_CE', 'SEC_TER_MASK']
>> ear!/sihdg-api.war!/WEB-INF/lib/icu4j-57.1.jar!/com/ibm/icu/impl/coll/CollationFastLatin.class ['SEC_AFTER', 'SEC_BEFORE', 'SEC_HIGH', 'SEC_INC', 'SEC_OFFSET', 'SEC_OFFSETS', 'SEC_PLUS_OFFSET']
>> ear!/sihdg-api.war!/WEB-INF/lib/icu4j-57.1.jar!/com/ibm/icu/impl/coll/CollationKeys.class ['SEC_COMMON_HIGH', 'SEC_COMMON_LOW', 'SEC_COMMON_MAX_COUNT', 'SEC_COMMON_MIDDLE']
>> ear!/sihdg-api.war!/WEB-INF/lib/icu4j-57.1.jar!/com/ibm/icu/impl/coll/CollationRootElements.class ['SEC_AND_TER_CE', 'SEC_TER_BOUNDARIES', 'SEC_TER_DELTA_FLAG']
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jasperreports-fonts-6.0.0.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/itext-2.1.7.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/bcmail-jdk14-138.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/bcprov-jdk14-138.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/bctsp-jdk14-1.38.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/bcprov-jdk14-1.38.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/bcmail-jdk14-1.38.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/commons-beanutils-1.9.3.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jakarta.mail-2.0.3.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/reflections-0.9.10.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/guava-15.0.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/annotations-2.0.1.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-http-oidc-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-auth-server-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-auth-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-base-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-permission-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-util-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-x500-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-credential-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-asn1-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-keystore-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-provider-util-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-http-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-jose-jwk-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-x500-cert-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-x500-cert-util-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-jose-util-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-elytron-mechanism-2.2.2.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/wildfly-common-1.6.0.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/httpclient-4.5.14.redhat-00002.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/httpcore-4.4.16.redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jose4j-0.9.3.redhat-00002.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/slf4j-api-2.0.7.redhat-00002.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/gson-2.3.1.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/swagger-jaxrs2-jakarta-2.2.22.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/classgraph-4.8.165.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/javassist-3.30.2-GA.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/swagger-models-jakarta-2.2.22.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/swagger-annotations-jakarta-2.2.22.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/swagger-integration-jakarta-2.2.22.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/swagger-core-jakarta-2.2.22.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/commons-lang3-3.14.0.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jackson-dataformat-yaml-2.16.2.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/snakeyaml-2.2.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jackson-databind-2.15.2.redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jackson-jakarta-rs-json-provider-2.15.2.redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jackson-jakarta-rs-base-2.15.2.redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jackson-module-jakarta-xmlbind-annotations-2.15.2.redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jackson-datatype-jsr310-2.17.2.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jackson-core-2.15.2.redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jboss-logging-3.4.3.Final-redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jakarta.xml.bind-api-4.0.0.redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/jakarta.activation-api-2.1.2.redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/angus-activation-2.0.1.redhat-00001.jar
abrindo ear!/sihdg-api.war!/WEB-INF/lib/commons-logging-1.1.1.jar
{'arq': 33743, 'cls': 27575}
sh-5.1$
