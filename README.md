O 404 nas releases 1.0.17.9 e 1.0.18.9 acontece porque as tags foram geradas sem o ajuste do arquivo jboss-modules feito na branch Cesti-teste. O redeploy funcionou porque reaproveitou a imagem gerada a partir dessa branch.

O script de build da imagem (S2I) descarta as duas primeiras linhas do jboss-modules. Com uma única linha do módulo, o br.gov.caixa.siusr não é instalado, o deploy do sicow-penhor-okd.war falha e o acesso ao /sicowpenhor/login retorna 404.

Ajuste necessário: fazer o merge da Cesti-teste (PR) na branch de vocês, ou ajustar o jboss-modules para o mesmo formato do SICOW-portal-okd:

group_id:artifact_id:version:extension
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar

Depois, gerar uma nova tag e executar a release.

Ac Jessé Batista
