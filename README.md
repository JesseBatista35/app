<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>
    <groupId>br.gov.caixa.siavo</groupId>
    <artifactId>siavo-ms-core</artifactId>
    <version>1.0.0</version>
    <name>siavo-ms-core</name>
    <description>Microsservico core do SIAVO - Plataforma Corporativa do Ativo do FGTS</description>

    <properties>
        <compiler-plugin.version>3.13.0</compiler-plugin.version>
        <maven.compiler.release>21</maven.compiler.release>
        <maven.compiler.source>21</maven.compiler.source>
        <maven.compiler.target>21</maven.compiler.target>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
        <project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>
        <quarkus.platform.artifact-id>quarkus-bom</quarkus.platform.artifact-id>
        <quarkus.platform.group-id>com.redhat.quarkus.platform</quarkus.platform.group-id>
        <quarkus.platform.version>3.15.3.redhat-00002</quarkus.platform.version>
        <skipITs>true</skipITs>
        <surefire-plugin.version>3.3.1</surefire-plugin.version>
        <jacoco.version>0.8.11</jacoco.version>
        <enforcer-plugin.version>3.4.1</enforcer-plugin.version>
        <mapstruct.version>1.6.3</mapstruct.version>
        <mockito.version>5.17.0</mockito.version>
        <archunit.version>1.3.0</archunit.version>
        <sonar.sources>src/main/java,src/main/resources</sonar.sources>
        <sonar.tests>src/test/java</sonar.tests>
        <sonar.test.inclusions>src/test/java/**/*.java</sonar.test.inclusions>
        <sonar.java.coveragePlugin>jacoco</sonar.java.coveragePlugin>
        <sonar.dynamicAnalysis>reuseReports</sonar.dynamicAnalysis>
        <sonar.language>java</sonar.language>
    </properties>

    <dependencyManagement>
        <dependencies>
            <dependency>
                <groupId>${quarkus.platform.group-id}</groupId>
                <artifactId>${quarkus.platform.artifact-id}</artifactId>
                <version>${quarkus.platform.version}</version>
                <type>pom</type>
                <scope>import</scope>
            </dependency>
        </dependencies>
    </dependencyManagement>

    <dependencies>
        <!-- ============================================================ -->
        <!-- Banco de Dados                                               -->
        <!-- ============================================================ -->
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-hibernate-orm</artifactId>
        </dependency>
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-agroal</artifactId>
        </dependency>
        <!-- SQL Server (mssavo) - datasource default em prod -->
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-jdbc-mssql</artifactId>
        </dependency>
        <!-- DB2 (db2avo) - datasource nomeado -->
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-jdbc-db2</artifactId>
        </dependency>
        <!-- H2 in-memory - datasource default no perfil %dev (mockado) -->
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-jdbc-h2</artifactId>
        </dependency>
        <!-- Driver IDMS (idmsavo) - disponivel no Nexus da Caixa -->
        <dependency>
            <groupId>com.ca.idms</groupId>
            <artifactId>jdbc</artifactId>
            <version>1.0</version>
        </dependency>

        <!-- ============================================================ -->
        <!-- Validacao                                                    -->
        <!-- ============================================================ -->
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-hibernate-validator</artifactId>
        </dependency>

        <!-- ============================================================ -->
        <!-- REST (server + client)                                       -->
        <!-- ============================================================ -->
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-rest</artifactId>
        </dependency>
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-rest-jackson</artifactId>
        </dependency>
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-rest-client</artifactId>
        </dependency>
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-rest-client-jackson</artifactId>
        </dependency>

        <!-- ============================================================ -->
        <!-- Mail (substitui Push/Email legado)                           -->
        <!-- ============================================================ -->
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-mailer</artifactId>
        </dependency>

        <!-- ============================================================ -->
        <!-- Observabilidade, cache e resiliencia                         -->
        <!-- ============================================================ -->
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-smallrye-health</artifactId>
        </dependency>
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-cache</artifactId>
        </dependency>
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-smallrye-metrics</artifactId>
        </dependency>
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-smallrye-fault-tolerance</artifactId>
        </dependency>
        <dependency>
            <groupId>io.smallrye.common</groupId>
            <artifactId>smallrye-common-vertx-context</artifactId>
        </dependency>

        <!-- ============================================================ -->
        <!-- Seguranca (OIDC / Keycloak SSO Caixa)                        -->
        <!-- ============================================================ -->
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-oidc</artifactId>
        </dependency>

        <!-- ============================================================ -->
        <!-- CDI                                                          -->
        <!-- ============================================================ -->
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-arc</artifactId>
        </dependency>

        <!-- ============================================================ -->
        <!-- OpenAPI / Swagger UI                                         -->
        <!-- ============================================================ -->
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-smallrye-openapi</artifactId>
        </dependency>

        <!-- ============================================================ -->
        <!-- Mapeamento de objetos (MapStruct)                            -->
        <!-- ============================================================ -->
        <dependency>
            <groupId>org.mapstruct</groupId>
            <artifactId>mapstruct</artifactId>
            <version>${mapstruct.version}</version>
        </dependency>
        <dependency>
            <groupId>org.mapstruct</groupId>
            <artifactId>mapstruct-processor</artifactId>
            <version>${mapstruct.version}</version>
            <scope>provided</scope>
        </dependency>

        <!-- ============================================================ -->
        <!-- Testes                                                       -->
        <!-- ============================================================ -->
        <dependency>
            <groupId>io.quarkus</groupId>
            <artifactId>quarkus-junit5</artifactId>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>io.rest-assured</groupId>
            <artifactId>rest-assured</artifactId>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>org.mockito</groupId>
            <artifactId>mockito-core</artifactId>
            <version>${mockito.version}</version>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>com.tngtech.archunit</groupId>
            <artifactId>archunit-junit5</artifactId>
            <version>${archunit.version}</version>
            <scope>test</scope>
        </dependency>
    </dependencies>

    <repositories>
        <repository>
            <id>caixa-nexus</id>
            <url>http://binario.caixa:8081/repository/maven-public/</url>
            <releases>
                <enabled>true</enabled>
            </releases>
            <snapshots>
                <enabled>true</enabled>
            </snapshots>
        </repository>
    </repositories>

    <pluginRepositories>
        <pluginRepository>
            <id>caixa-nexus</id>
            <url>http://binario.caixa:8081/repository/maven-public/</url>
            <releases>
                <enabled>true</enabled>
            </releases>
            <snapshots>
                <enabled>true</enabled>
            </snapshots>
        </pluginRepository>
    </pluginRepositories>

    <build>
        <plugins>
            <plugin>
                <groupId>${quarkus.platform.group-id}</groupId>
                <artifactId>quarkus-maven-plugin</artifactId>
                <version>${quarkus.platform.version}</version>
                <extensions>true</extensions>
                <executions>
                    <execution>
                        <goals>
                            <goal>build</goal>
                            <goal>generate-code</goal>
                            <goal>generate-code-tests</goal>
                        </goals>
                    </execution>
                </executions>
            </plugin>

            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-enforcer-plugin</artifactId>
                <version>${enforcer-plugin.version}</version>
                <executions>
                    <execution>
                        <id>enforce-regras-pom</id>
                        <goals>
                            <goal>enforce</goal>
                        </goals>
                        <phase>validate</phase>
                        <configuration>
                            <rules>
                                <!-- ============================================================
                                 AMBIENTE DE BUILD
                                 ============================================================ -->
                                <requireMavenVersion>
                                    <version>[3.8.0,)</version>
                                    <message>Maven 3.8 ou superior e obrigatorio para este projeto.</message>
                                </requireMavenVersion>

                                <requireJavaVersion>
                                    <version>[21,)</version>
                                    <message>Java 21 (LTS) ou superior e obrigatorio.</message>
                                </requireJavaVersion>

                                <!-- ============================================================
                                 QUALIDADE DO POM
                                 ============================================================ -->
                                <banDuplicatePomDependencyVersions/>
                                <requireReleaseDeps>
                                    <onlyWhenRelease>true</onlyWhenRelease>
                                    <message>Dependencias SNAPSHOT nao sao permitidas em versao de release.</message>
                                </requireReleaseDeps>

                                <!-- ============================================================
                                 SEGURANCA — CVEs conhecidos (searchTransitive=true)
                                 ============================================================ -->
                                <bannedDependencies>
                                    <searchTransitive>true</searchTransitive>
                                    <excludes>
                                        <exclude>log4j:log4j</exclude>
                                        <exclude>commons-collections:commons-collections:(,3.2.2)</exclude>
                                        <exclude>org.apache.struts:struts2-core</exclude>
                                        <exclude>org.springframework:spring-core:(,5.3.39)</exclude>
                                    </excludes>
                                    <message>Dependencia banida por CVE conhecido. Consulte o time de seguranca.</message>
                                </bannedDependencies>

                                <!-- MAPEAMENTO DE OBJETOS: padrao = MapStruct -->
                                <bannedDependencies>
                                    <searchTransitive>false</searchTransitive>
                                    <excludes>
                                        <exclude>org.modelmapper:modelmapper</exclude>
                                        <exclude>net.sf.dozer:dozer</exclude>
                                        <exclude>ma.glasnost.orika:orika-core</exclude>
                                        <exclude>com.googlecode.jmapper-framework:jmapper-core</exclude>
                                    </excludes>
                                    <message>MAPEAMENTO: este projeto usa MapStruct. Nao adicione ModelMapper, Dozer nem Orika.</message>
                                </bannedDependencies>

                                <!-- SERIALIZACAO JSON: padrao = Jackson -->
                                <bannedDependencies>
                                    <searchTransitive>false</searchTransitive>
                                    <excludes>
                                        <exclude>com.google.code.gson:gson</exclude>
                                        <exclude>com.alibaba:fastjson</exclude>
                                        <exclude>com.alibaba.fastjson2:fastjson2</exclude>
                                        <exclude>com.squareup.moshi:moshi</exclude>
                                        <exclude>org.json:json</exclude>
                                    </excludes>
                                    <message>JSON: este projeto usa Jackson. Nao adicione Gson, Fastjson, Moshi nem org.json.</message>
                                </bannedDependencies>

                                <!-- INJECAO DE DEPENDENCIA: padrao = Quarkus ARC (CDI) -->
                                <bannedDependencies>
                                    <searchTransitive>false</searchTransitive>
                                    <excludes>
                                        <exclude>org.springframework:spring-context</exclude>
                                        <exclude>org.springframework.boot:spring-boot</exclude>
                                        <exclude>com.google.inject:guice</exclude>
                                        <exclude>org.jboss.weld:weld-core</exclude>
                                    </excludes>
                                    <message>CDI: este projeto usa Quarkus ARC. Nao adicione Spring DI, Spring Boot nem Guice.</message>
                                </bannedDependencies>

                                <!-- ORM / PERSISTENCIA: padrao = Hibernate ORM -->
                                <bannedDependencies>
                                    <searchTransitive>false</searchTransitive>
                                    <excludes>
                                        <exclude>org.eclipse.persistence:eclipselink</exclude>
                                        <exclude>org.apache.openjpa:openjpa</exclude>
                                        <exclude>org.mybatis:mybatis</exclude>
                                        <exclude>com.querydsl:querydsl-jpa</exclude>
                                    </excludes>
                                    <message>ORM: este projeto usa Hibernate ORM. Nao adicione EclipseLink, OpenJPA nem MyBatis.</message>
                                </bannedDependencies>

                                <!-- MOCK EM TESTES: padrao = Mockito -->
                                <bannedDependencies>
                                    <searchTransitive>false</searchTransitive>
                                    <excludes>
                                        <exclude>org.powermock:powermock-module-junit4</exclude>
                                        <exclude>org.powermock:powermock-api-mockito2</exclude>
                                        <exclude>org.easymock:easymock</exclude>
                                        <exclude>org.jmock:jmock</exclude>
                                    </excludes>
                                    <message>MOCK: este projeto usa Mockito. Nao adicione PowerMock, EasyMock nem JMock.</message>
                                </bannedDependencies>

                                <!-- TOLERANCIA A FALHAS: padrao = SmallRye Fault Tolerance -->
                                <bannedDependencies>
                                    <searchTransitive>false</searchTransitive>
                                    <excludes>
                                        <exclude>io.github.resilience4j:resilience4j-core</exclude>
                                        <exclude>com.netflix.hystrix:hystrix-core</exclude>
                                        <exclude>io.github.resilience4j:resilience4j-circuitbreaker</exclude>
                                    </excludes>
                                    <message>FAULT TOLERANCE: este projeto usa SmallRye Fault Tolerance. Nao adicione Resilience4j nem Hystrix.</message>
                                </bannedDependencies>

                                <!-- CACHE: padrao = Quarkus Cache (Caffeine) -->
                                <bannedDependencies>
                                    <searchTransitive>false</searchTransitive>
                                    <excludes>
                                        <exclude>net.sf.ehcache:ehcache</exclude>
                                        <exclude>org.ehcache:ehcache</exclude>
                                        <exclude>com.hazelcast:hazelcast</exclude>
                                        <exclude>com.google.guava:guava</exclude>
                                        <exclude>org.infinispan:infinispan-core</exclude>
                                    </excludes>
                                    <message>CACHE: este projeto usa Quarkus Cache com Caffeine. Nao adicione Ehcache, Hazelcast nem Guava.</message>
                                </bannedDependencies>

                                <!-- HTTP CLIENT: padrao = Quarkus REST Client (MicroProfile) -->
                                <bannedDependencies>
                                    <searchTransitive>false</searchTransitive>
                                    <excludes>
                                        <exclude>org.apache.httpcomponents:httpclient</exclude>
                                        <exclude>org.apache.httpcomponents.client5:httpclient5</exclude>
                                        <exclude>com.squareup.okhttp3:okhttp</exclude>
                                        <exclude>io.github.openfeign:feign-core</exclude>
                                        <exclude>org.springframework:spring-web</exclude>
                                    </excludes>
                                    <message>HTTP CLIENT: este projeto usa Quarkus REST Client. Nao adicione Apache HttpClient, OkHttp nem Feign.</message>
                                </bannedDependencies>

                                <!-- VALIDACAO DE BEANS: padrao = Hibernate Validator -->
                                <bannedDependencies>
                                    <searchTransitive>false</searchTransitive>
                                    <excludes>
                                        <exclude>org.apache.bval:bval-jsr</exclude>
                                        <exclude>org.apache.bval:org.apache.bval.bundle</exclude>
                                    </excludes>
                                    <message>VALIDACAO: este projeto usa Hibernate Validator. Nao adicione Apache BVal.</message>
                                </bannedDependencies>

                                <!-- BOILERPLATE: Lombok e proibido -->
                                <bannedDependencies>
                                    <searchTransitive>true</searchTransitive>
                                    <excludes>
                                        <exclude>org.projectlombok:lombok</exclude>
                                    </excludes>
                                    <message>BOILERPLATE: Lombok e proibido neste projeto. Use Java 21 com getters/setters explicitos e MapStruct para mapeamento.</message>
                                </bannedDependencies>
                            </rules>
                            <fail>true</fail>
                        </configuration>
                    </execution>
                </executions>
            </plugin>

            <plugin>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>${compiler-plugin.version}</version>
                <configuration>
                    <encoding>UTF-8</encoding>
                    <parameters>true</parameters>
                </configuration>
            </plugin>
            <plugin>
                <artifactId>maven-surefire-plugin</artifactId>
                <version>${surefire-plugin.version}</version>
                <configuration>
                    <systemPropertyVariables>
                        <java.util.logging.manager>org.jboss.logmanager.LogManager</java.util.logging.manager>
                        <maven.home>${maven.home}</maven.home>
                    </systemPropertyVariables>
                </configuration>
            </plugin>
            <plugin>
                <artifactId>maven-failsafe-plugin</artifactId>
                <version>${surefire-plugin.version}</version>
                <executions>
                    <execution>
                        <goals>
                            <goal>integration-test</goal>
                            <goal>verify</goal>
                        </goals>
                    </execution>
                </executions>
                <configuration>
                    <systemPropertyVariables>
                        <native.image.path>${project.build.directory}/${project.build.finalName}-runner</native.image.path>
                        <java.util.logging.manager>org.jboss.logmanager.LogManager</java.util.logging.manager>
                        <maven.home>${maven.home}</maven.home>
                    </systemPropertyVariables>
                </configuration>
            </plugin>
            <plugin>
                <groupId>org.jacoco</groupId>
                <artifactId>jacoco-maven-plugin</artifactId>
                <version>${jacoco.version}</version>
                <executions>
                    <execution>
                        <goals>
                            <goal>prepare-agent</goal>
                        </goals>
                    </execution>
                    <execution>
                        <id>report</id>
                        <phase>test</phase>
                        <goals>
                            <goal>report</goal>
                        </goals>
                    </execution>
                </executions>
            </plugin>
        </plugins>
    </build>
</project>


Skip to main content
Azure DevOps
projetos
/
Caixa
/
Pipelines
/
Releases
/
SIAVO-ms-core
Search


Caixa

Overview

Boards

Repos

Pipelines
Pipelines
Environments
Releases
Library
Task groups
Deployment groups
Portal Infra

Test Plans

Artifacts
Project settings
All pipelines

SIAVO

SIAVO-ms-core
Predefined variables
SonarQube Variables (1)
Variáveis com dados do SonarQube
Scopes: Release
Usuario-Azure-DevOps (12)
Scopes: Release
MONITORACAO_LOGS (4)
REQ000143540550 - Conforme autorizado na req por FLAVIO ALMEIDA GAGLIARDI, removido as variáveis JAVA_OPTS_MONITORING e URL_APM_SERVER, por entrar em conflitos com releases que utilizam o Application Insights
Scopes: Release
EGRESS_IP_OKD (81)
WO0000072264656 - Config Portal Infrafácil NO_PROXY
Scopes: Release
OKD-REGISTRY-CENTRALIZADO (7)
Credenciais para o Registry Centralizado - Produtos 4 (OKD)
Scopes: Release
OKD-4-NPRD (12)
Credenciais para o Cluster OKD4 de NPRD (DES/TQS/HMP)
Scopes: EC DES,EC TQS,EC HMP
SIAVO-MS-CORE-DES (22)
Grupo de variáveis de SIAVO-MS-CORE-DES

Scopes: EC DES
DATASOURCE_PASSWORD
********
DATASOURCE_PASSWORD_DB2
********
DATASOURCE_PASSWORD_IDMS
********
OIDC_CREDENTIALS_SECRET
********
_ENV.CRF_URL
https://tqs.inter.corerj.caixa:8617
_ENV.CRP_URL
https://cadprev.previdencia.gov.br
_ENV.ICO_API_URL
https://api.des.caixa:8443/informacoes-corporativas-publicas
_ENV.ISO_API_URL
https://api.des.caixa:8443/cadastro-receita
_ENV.JAVA_OPTIONS_APPEND
"-Djavax.net.ssl.trustStore=/deployments/caixa-truststore-acteste-nprd.jks"
_ENV.MAIL_HOST
smtptest.correiolivre.caixa
_ENV.QUARKUS_DATASOURCE_DB2_JDBC_URL
jdbc:db2://10.216.80.110:448/RJKDB2DSD0
_ENV.QUARKUS_DATASOURCE_DB2_USERNAME
SAVORD01
_ENV.QUARKUS_DATASOURCE_IDMS_JDBC_URL
jdbc:idms://10.216.80.110:3721/DICTATV
_ENV.QUARKUS_DATASOURCE_IDMS_USERNAME
SAVORD01
_ENV.QUARKUS_DATASOURCE_JDBC_URL
"jdbc:sqlserver://AGSQLDES100.extra.caixa.gov.br:22100;databaseName=AVODB001;trustServerCertificate=true"
_ENV.QUARKUS_DATASOURCE_USERNAME
SAVORD04
_ENV.QUARKUS_OIDC_AUTH_SERVER_URL
https://login.des.caixa/auth/realms/intranet
_ENV.QUARKUS_OIDC_CLIENT_ID
cli-web-avo
_SECRET.QUARKUS_DATASOURCE_DB2_PASSWORD
#{DATASOURCE_PASSWORD_DB2}#
_SECRET.QUARKUS_DATASOURCE_IDMS_PASSWORD
#{DATASOURCE_PASSWORD_IDMS}#
_SECRET.QUARKUS_DATASOURCE_PASSWORD
#{DATASOURCE_PASSWORD}#
_SECRET.QUARKUS_OIDC_CREDENTIALS_SECRET
#{OIDC_CREDENTIALS_SECRET}#
SIAVO-MS-CORE-TQS (1)
Grupo de variáveis de SIAVO-MS-CORE-TQS
Scopes: EC TQS
SIAVO-MS-CORE-HMP (1)
Grupo de variáveis de SIAVO-MS-CORE-HMP
Scopes: EC HMP
OKD-4-APL (12)
Scopes: EC PRD
SIAVO-MS-CORE-PRD (1)
Grupo de variáveis de SIAVO-MS-CORE-PRD
Scopes: EC PRD
|Manage variable groups
Select a release pipeline to view its releases

17 pipelines found

Select a release pipeline to view its releases

8 pipelines found

Select a release pipeline to view its releases

2 pipelines found

Select a release pipeline to view its releases

1 pipelines found

Row 2

Showing 21 deployments

Row 2

Row 2

Showing filters 1 through 2
