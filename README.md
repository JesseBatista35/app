Outro ponto, independente do 401:
@Alessandro Ricardo Lima, durante a análise encontramos também um erro de banco no CCR no 7.4, na consulta de contrato (ContratacaoRest.consultaListaAutorizacao → ContratoAPXBean.consultarContratoPorId):

ORA-25156: a junção externa de estilo antigo (+) não pode ser usada com junções ANSI

O SQL gerado mistura cross join (padrão ANSI, gerado pelo Hibernate 5 do JBoss 7.4) com (+) (outer join no estilo antigo do Oracle), e o Oracle não aceita os dois na mesma consulta. No 6.4, com o Hibernate 4, isso não acontecia. Normalmente a causa é a unidade de persistência usar um dialeto Oracle antigo. O ajuste sugerido é definir hibernate.dialect como org.hibernate.dialect.Oracle10gDialect (ou Oracle12cDialect) no persistence.xml do CCR, ou revisar essa consulta. É correção no pacote e gera erro 500 nessa funcionalidade. Se precisar, passo o trecho do log.

Para os próximos ambientes: em DES o container não valida mais o token do ccr-api. Nos ambientes seguintes e em produção, precisamos prever a segregação intranet/internet, como já existe hoje em produção.
