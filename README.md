<?xml version="1.0" encoding="UTF-8"?>
<persistence version="2.1" xmlns="http://xmlns.jcp.org/xml/ns/persistence" 
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
	xsi:schemaLocation="http://xmlns.jcp.org/xml/ns/persistence http://xmlns.jcp.org/xml/ns/persistence/persistence_2_1.xsd">
	
	<persistence-unit name="SicowConresPersistUnit" transaction-type="JTA">
		<provider>org.hibernate.ejb.HibernatePersistence</provider>
		
		<jta-data-source>java:/jboss/datasources/sicow-ds</jta-data-source>
		
		<class>br.gov.caixa.pr.sicow.conres.entity.Motivo</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.MotivoUnidade</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.SubMotivo</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.SubMotivoUnidade</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.AlertaImportacaoConres</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.TipoExclusaoOcorrencia</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.Log</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.Ocorrencia</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.HistoricoOcorrencia</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.Sistema</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.PassWordSistema</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.Servidor</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.WsServicosSistema</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.WsServico</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.MotivoLegadoConres</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.ArquivoRecebido</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.StatusRecebido</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.ViaRecebimento</class>
		<class>br.gov.caixa.pr.sicow.conres.entity.ImportacaoArquivosConres</class>
		
		<class>br.gov.caixa.pr.sicow.conres.entity.audit.SicowConresAuditEntity</class>
		
		<class>br.gov.caixa.siico.entity.Unidade</class>
		
		<properties>
			<property name="hibernate.dialect" value="org.hibernate.dialect.PostgreSQLDialect" />
			<property name="hibernate.show_sql" value="false" />
			<property name="hibernate.format_sql" value="true" />
			<property name="hibernate.jdbc.batch_size" value="50" />
			<property name="hibernate.cache.use_second_level_cache" value="false" />
			<property name="hibernate.ejb.interceptor" value="br.gov.caixa.pr.sicow.conres.audit.SicowConresAuditInterceptor"/>
		</properties>
	</persistence-unit>
	
</persistence>


