<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<groupId>br.gov.caixa.sigec</groupId>
	<artifactId>gec</artifactId>
	<version>${sigec.version}</version>
	<packaging>pom</packaging>
	<name>SIGEC-PORTABILIDADE</name>

	<!-- Módulos definidos nos profiles batch/online -->

	<properties>
		<sigec.version>5.0.0</sigec.version>
		<!-- Explicitly declaring the source encoding eliminates the following 
			message: -->
		<project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>

		<!-- Cache busting: timestamp opaco gerado no build, sem expor versao ou artefato -->
		<maven.build.timestamp.format>yyyyMMddHHmmss</maven.build.timestamp.format>
		<build.timestamp>${maven.build.timestamp}</build.timestamp>

		<!-- JBoss dependency versions -->
		<jboss.as.plugin.version>7.3.Final</jboss.as.plugin.version>

		<!-- Define the version of JBoss' Java EE 6 APIs and Tools we want to
		import. -->
		<jboss.bom.version>1.0.4.Final</jboss.bom.version>
		<!-- Alternatively, comment out the above line, and un-comment the line 
			below to use version 1.0.2.Final-redhat-1 which is a release certified to 
			work with JBoss EAP 6. It requires you have access to the JBoss EAP 6 maven 
			repository. -->
		<!-- <jboss.bom.version>1.0.2.Final-redhat-1</jboss.bom.version>> -->
		<!-- other plugin versions -->
		<compiler.plugin.version>3.13.0</compiler.plugin.version>
		<war.plugin.version>3.4.0</war.plugin.version>
		<ear.plugin.version>3.3.0</ear.plugin.version>
		<ejb.plugin.version>3.0.1</ejb.plugin.version>
		<surefire.plugin.version>3.2.5</surefire.plugin.version>

		<!-- maven-compiler-plugin -->
		<maven.compiler.release>17</maven.compiler.release>
		<maven.compiler.target>17</maven.compiler.target>
		<maven.compiler.source>17</maven.compiler.source>

		<arqref-core.version>3.7.1</arqref-core.version>
		<arqref-services.version>3.6.3.13</arqref-services.version>
		<arqref-web.version>3.1.0.1</arqref-web.version>


		<servlet.version>4.0.1</servlet.version>
		<apache.poi.version>5.2.5</apache.poi.version>
		<sifec-security-sso.version>0.0.5</sifec-security-sso.version>
		<xhtml.core.render.version>R8</xhtml.core.render.version>
		<swagger-version>1.6.14</swagger-version>
		<swagger-ui-version>2.1.4</swagger-ui-version>
		<jackson.version>2.15.4</jackson.version>
		<!-- Apache -->
		<org.apache.commons.version>3.14.0</org.apache.commons.version>
		<org.mockito>5.11.0</org.mockito>
		<guava.version>33.2.1-jre</guava.version>
		<commons.codec.version>1.17.1</commons.codec.version>
		<lombok.version>1.18.36</lombok.version>
		<!-- RESTEasy: 3.1.3.Final disponivel no cache local; escopo provided (JBoss EAP 7.4 fornece em runtime) -->
		<resteasy.version>3.1.3.Final</resteasy.version>
	</properties>

	<dependencyManagement>
		<dependencies>

			<!-- Define the version of the EJB jar so that we don't need to
			repeat 
				ourselves in every module -->
			<dependency>
				<groupId>br.gov.caixa.sigec</groupId>
				<artifactId>gec-ejb</artifactId>
				<version>${project.version}</version>
				<type>ejb</type>
			</dependency>

			<!-- Define the version of the WAR so that we don't need to repeat
			ourselves 
				in every module -->
			<dependency>
				<groupId>br.gov.caixa.sigec</groupId>
				<artifactId>gec-web</artifactId>
				<version>${project.version}</version>
				<type>war</type>
				<scope>compile</scope>
			</dependency>

			<!-- Define the version of the JAR so that we don't need to repeat
			ourselves 
				in every module -->
			<dependency>
				<groupId>br.gov.caixa.sigec</groupId>
				<artifactId>gec-xml</artifactId>
				<version>${project.version}</version>
				<type>jar</type>
				<scope>compile</scope>
			</dependency>

			<dependency>
				<groupId>br.gov.caixa.sigec</groupId>
				<artifactId>gec-api</artifactId>
				<version>${project.version}</version>
				<type>war</type>
				<scope>compile</scope>
			</dependency>

			<dependency>
				<groupId>br.gov.caixa.sigec</groupId>
				<artifactId>gec-azure</artifactId>
				<version>${project.version}</version>
				<type>jar</type>
				<scope>compile</scope>
			</dependency>

			<dependency>
				<groupId>br.gov.caixa.sigec</groupId>
				<artifactId>gec-common</artifactId>
				<version>${project.version}</version>
				<type>jar</type>
				<scope>compile</scope>
			</dependency>

			<dependency>
				<groupId>br.gov.caixa.sigec</groupId>
				<artifactId>gec-batch</artifactId>
				<version>${project.version}</version>
				<type>ejb</type>
				<scope>compile</scope>
			</dependency>

			<dependency>
				<groupId>javax</groupId>
				<artifactId>javaee-api</artifactId>
				<version>7.0</version>
				<scope>provided</scope>
			</dependency>
			<dependency>
				<groupId>br.gov.caixa.arqref</groupId>
				<artifactId>arqref-core</artifactId>
				<version>${arqref-core.version}</version>
				<scope>provided</scope>
				<exclusions>
					<exclusion>
						<groupId>org.hibernate</groupId>
						<artifactId>hibernate</artifactId>
					</exclusion>
				</exclusions>
			</dependency>

			<dependency>
				<groupId>br.gov.caixa.arqref</groupId>
				<artifactId>arqref-web</artifactId>
				<version>${arqref-web.version}</version>
				<scope>provided</scope>
			</dependency>

			<dependency>
				<groupId>br.gov.caixa.arqref</groupId>
				<artifactId>arqref-services</artifactId>
				<version>${arqref-services.version}</version>
				<scope>provided</scope>
			</dependency>

			<dependency>
				<groupId>org.apache.poi</groupId>
				<artifactId>poi</artifactId>
				<version>${apache.poi.version}</version>
				<scope>provided</scope>
			</dependency>

			<dependency>
				<groupId>org.apache.poi</groupId>
				<artifactId>poi-ooxml</artifactId>
				<version>${apache.poi.version}</version>
				<scope>provided</scope>
			</dependency>

			<dependency>
				<groupId>net.sf.jasperreports</groupId>
				<artifactId>jasperreports</artifactId>
				<version>6.6.0</version>
				<scope>provided</scope>
				<exclusions>
					<!-- itext 2.1.7.js6 so existe nos repos HTTP do Jaspersoft (bloqueados pelo Maven 3.8+);
					     substituido por OpenPDF na compilacao e runtime -->
					<exclusion>
						<groupId>com.lowagie</groupId>
						<artifactId>itext</artifactId>
					</exclusion>
				</exclusions>
			</dependency>
			<!-- iText substituído por OpenPDF (fork LGPL, API compatível, suporte Java 17) -->
			<dependency>
				<groupId>com.github.librepdf</groupId>
				<artifactId>openpdf</artifactId>
				<version>1.3.43</version>
			</dependency>

			<!-- https://mvnrepository.com/artifact/org.mockito/mockito-core -->
			<dependency>
				<groupId>org.mockito</groupId>
				<artifactId>mockito-core</artifactId>
				<version>${org.mockito}</version>
				<scope>test</scope>
			</dependency>

			<dependency>
				<groupId>commons-codec</groupId>
				<artifactId>commons-codec</artifactId>
				<version>${commons.codec.version}</version>
				<scope>provided</scope>
			</dependency>

			<dependency>
				<groupId>org.olap4j</groupId>
				<artifactId>olap4j</artifactId>
				<version>0.9.8.343</version>
				<scope>provided</scope>
			</dependency>

			<dependency>
				<groupId>br.gov.caixa</groupId>
				<artifactId>framework</artifactId>
				<version>2.0.1</version>
				<scope>provided</scope>
			</dependency>

			<dependency>
				<groupId>com.ibm.mq</groupId>
				<artifactId>jmqi</artifactId>
				<version>1.0</version>
				<scope>provided</scope>
			</dependency>

			<dependency>
				<groupId>io.swagger</groupId>
				<artifactId>swagger-jaxrs</artifactId>
				<version>${swagger-version}</version>
				<scope>provided</scope>
			</dependency>
			<dependency>
				<groupId>io.swagger</groupId>
				<artifactId>swagger-models</artifactId>
				<version>${swagger-version}</version>
				<scope>provided</scope>
			</dependency>
			<dependency>
				<groupId>io.swagger</groupId>
				<artifactId>swagger-core</artifactId>
				<version>${swagger-version}</version>
				<scope>provided</scope>
			</dependency>
			<dependency>
				<groupId>io.swagger</groupId>
				<artifactId>swagger-annotations</artifactId>
				<version>${swagger-version}</version>
				<scope>provided</scope>
			</dependency>
			<dependency>
				<groupId>org.reflections</groupId>
				<artifactId>reflections</artifactId>
				<version>0.10.2</version>
				<scope>provided</scope>
			</dependency>
			<dependency>
				<groupId>com.google.guava</groupId>
				<artifactId>guava</artifactId>
				<version>${guava.version}</version>
				<scope>provided</scope>
			</dependency>
			<dependency>
				<groupId>org.apache.commons</groupId>
				<artifactId>commons-lang3</artifactId>
				<version>${org.apache.commons.version}</version>
				<scope>provided</scope>
			</dependency>
			<dependency>
				<groupId>commons-collections</groupId>
				<artifactId>commons-collections</artifactId>
				<version>3.2.2</version>
				<scope>provided</scope>
			</dependency>

			<dependency>
				<groupId>org.projectlombok</groupId>
				<artifactId>lombok</artifactId>
				<version>${lombok.version}</version>
				<scope>provided</scope>
			</dependency>

			<dependency>
				<groupId>org.hibernate</groupId>
				<artifactId>hibernate-core</artifactId>
				<version>5.6.9.Final</version>
			</dependency>

			<dependency>
				<groupId>org.hibernate.javax.persistence</groupId>
				<artifactId>hibernate-jpa-2.1-api</artifactId>
				<version>1.0.2.Final</version>
			</dependency>

			<dependency>
				<groupId>com.squareup.okhttp3</groupId>
				<artifactId>okhttp</artifactId>
				<version>4.10.0</version>
			</dependency>

			<dependency>
				<groupId>com.auth0</groupId>
				<artifactId>java-jwt</artifactId>
				<version>4.4.0</version>
			</dependency>
			
			<dependency>
				<groupId>com.fasterxml.jackson.jaxrs</groupId>
				<artifactId>jackson-jaxrs-json-provider</artifactId>
				<version>${jackson.version}</version>
			</dependency>

						<!-- Centralize core Jackson artifacts to avoid version skew -->
			<dependency>
				<groupId>com.fasterxml.jackson.core</groupId>
				<artifactId>jackson-annotations</artifactId>
				<version>${jackson.version}</version>
			</dependency>
			<dependency>
				<groupId>com.fasterxml.jackson.core</groupId>
				<artifactId>jackson-core</artifactId>
				<version>${jackson.version}</version>
			</dependency>
			<dependency>
				<groupId>com.fasterxml.jackson.core</groupId>
				<artifactId>jackson-databind</artifactId>
				<version>${jackson.version}</version>
			</dependency>
			<dependency>
				<groupId>com.fasterxml.jackson.dataformat</groupId>
				<artifactId>jackson-dataformat-xml</artifactId>
				<version>${jackson.version}</version>
			</dependency>
			<dependency>
				<groupId>com.fasterxml.jackson.dataformat</groupId>
				<artifactId>jackson-dataformat-yaml</artifactId>
				<version>${jackson.version}</version>
			</dependency>
			<dependency>
				<groupId>com.fasterxml.jackson.datatype</groupId>
				<artifactId>jackson-datatype-jsr310</artifactId>
				<version>${jackson.version}</version>
			</dependency>

			<!-- JAXB: removido do JDK 9+; EAP 7.4 provê em runtime, declarar como provided -->
			<dependency>
				<groupId>javax.xml.bind</groupId>
				<artifactId>jaxb-api</artifactId>
				<version>2.3.1</version>
				<scope>provided</scope>
			</dependency>

			<!-- JAXB runtime para testes locais sem servidor -->
			<dependency>
				<groupId>org.glassfish.jaxb</groupId>
				<artifactId>jaxb-runtime</artifactId>
				<version>2.3.9</version>
				<scope>test</scope>
			</dependency>

			<!-- RESTEasy 3.15.x — compatível com Java 17 e EAP 7.4 -->
			<dependency>
				<groupId>org.jboss.resteasy</groupId>
				<artifactId>resteasy-jaxrs</artifactId>
				<version>${resteasy.version}</version>
				<scope>provided</scope>
			</dependency>
			<dependency>
				<groupId>org.jboss.resteasy</groupId>
				<artifactId>resteasy-client</artifactId>
				<version>${resteasy.version}</version>
				<scope>provided</scope>
			</dependency>
			<dependency>
				<groupId>org.jboss.resteasy</groupId>
				<artifactId>resteasy-jackson2-provider</artifactId>
				<version>${resteasy.version}</version>
				<scope>provided</scope>
			</dependency>
			<dependency>
				<groupId>org.jboss.resteasy</groupId>
				<artifactId>resteasy-multipart-provider</artifactId>
				<version>${resteasy.version}</version>
				<scope>provided</scope>
			</dependency>
			<dependency>
				<groupId>org.jboss.resteasy</groupId>
				<artifactId>resteasy-jaxb-provider</artifactId>
				<version>${resteasy.version}</version>
				<scope>provided</scope>
			</dependency>


		</dependencies>
	</dependencyManagement>

	<profiles>
		<!-- Profile BATCH: Default profile incluindo componentes batch para processamento assíncrono -->
		<profile>
			<id>batch</id>
			<activation>
				<activeByDefault>true</activeByDefault>
			</activation>
			<properties>
				<sigec.version>5.0.0-batch-SNAPSHOT</sigec.version>
			</properties>
			<modules>
				<module>gec-xml</module>
				<module>gec-azure</module>
				<module>gec-common</module>
				<module>gec-ejb</module>
				<module>gec-batch</module>
				<!-- gec-web excluído do profile batch -->
				<module>gec-api</module>
				<module>gec-ear</module>
			</modules>
		</profile>

		<!-- Profile ONLINE: Profile para ambiente online/web excluindo componentes batch -->
		<profile>
			<id>online</id>
			<activation>
				<activeByDefault>false</activeByDefault>
			</activation>
			<properties>
				<sigec.version>5.0.0-online-SNAPSHOT</sigec.version>
			</properties>
			<modules>
				<module>gec-xml</module>
				<module>gec-azure</module>
				<module>gec-common</module>
				<module>gec-ejb</module>
				<!-- gec-batch excluído do profile online -->
				<module>gec-web</module>
				<module>gec-api</module>
				<module>gec-ear</module>
			</modules>
		</profile>
	</profiles>

	<build>
		<pluginManagement>
			<plugins>
				<plugin>
					<groupId>org.apache.maven.plugins</groupId>
					<artifactId>maven-compiler-plugin</artifactId>
					<version>${compiler.plugin.version}</version>
					<configuration>
					<release>${maven.compiler.release}</release>
					<parameters>true</parameters>
				</configuration>
			</plugin>

			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-surefire-plugin</artifactId>
				<version>${surefire.plugin.version}</version>
				<configuration>
					<!-- Garante que o Surefire use o mesmo JVM que o Maven (JDK 17+).
					     Sem isso, o fork pode pegar o JRE 8 do PATH do SO, que nao
					     suporta as flags add-opens (disponiveis apenas no Java 9+). -->
					<jvm>${java.home}/bin/java</jvm>
					<argLine>
						--add-opens java.base/java.lang=ALL-UNNAMED
						--add-opens java.base/java.io=ALL-UNNAMED
						--add-opens java.base/java.lang.reflect=ALL-UNNAMED
						--add-opens java.base/java.util=ALL-UNNAMED
						--add-opens java.base/java.util.concurrent=ALL-UNNAMED
					</argLine>
				</configuration>
			</plugin>

			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-resources-plugin</artifactId>
				<version>3.3.1</version>
				</plugin>
			</plugins>
		</pluginManagement>
	</build>
</project>
