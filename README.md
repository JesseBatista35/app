Pessoal, atualização do SIRUR no JBoss 7.4 (sifec-intranet):

Fizemos duas tentativas de deploy e as duas foram revertidas pelo servidor:

a versão que já estava disponível no 471;
a sifec-sirur-3.54.51.28, a mesma da planilha de PRD, que o Thiago Jeferson localizou na console. Deploy feito às 11:30.

Nas duas, o log mostra as mesmas causas:

1. Aplicação (fábrica): o Hibernate do JBoss 7.4 não aceita o mesmo nome de gerador de ID (“gen”) em mais de uma entidade. Isso trava as unidades de persistência fec.pu e fec.rur.pu do sirur-ejb.jar. Testamos o ajuste pelo servidor e o JBoss não aplica, então a correção precisa ir no persistence.xml do pacote, nas duas unidades:
<property name="hibernate.jpa.compliance.global_id_generators" value="false"/>
Depois disso, precisamos de um build novo para fazer o deploy.

2. Ambiente (DevOps): um dos datasources do SIRUR está recusando o login no banco (ORA-01017). Já estou comparando com a configuração do 6.4 e corrijo do nosso lado.

@Paulo, pode nos indicar o dev responsável pelo SIRUR para encaminharmos o item 1?

Quando o build novo estiver disponível e o datasource estiver corrigido, faço o deploy de novo e valido o log com vocês.
