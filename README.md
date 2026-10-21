Pessoal, atualização do SIGSJ-boleto (DES):

Situação atual (caddeapllx2557):

JBoss no ar.
sirotcon-ejb.jar implantado pela esteira com status OK.
boletoService-ear.ear com status FAILED.

Causa:
O EAR declara no META-INF/jboss-deployment-structure.xml uma dependência explícita com o nome versionado do SIROTCon:

xml
<module name="deployment.sirotcon-ejb-2.3.0.1-farm.jar" export="true"/>

A esteira publica o EJB como sirotcon-ejb.jar, então o JBoss não encontra o módulo com esse nome e o deploy falha. O jar é o mesmo; só o nome não bate.

Ajuste necessário na aplicação:
@Vitor, consegue alterar essa linha no jboss-deployment-structure.xml do EAR do boleto para:

xml
<module name="deployment.sirotcon-ejb.jar" export="true"/>

e gerar uma nova build? Assim a dependência deixa de depender da versão do SIROTCon no nome do arquivo.
