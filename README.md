systemctl status sigdb --no-pager; ps -ef | grep -i [A]gtSigdb



Salve Sandro Araujo Dantas
feito correções referente ao vault em sicow-seg-okd-config standalone-okd.xml
continua erro time out na última release
 
Paulo Ferreira de Almeida Junior
Salve Sandro Araujo Dantas feito correções referente ao vault em sicow-seg-okd-config standalone-okd.xml continua erro time out na última release 📷
Salve Paulo Ferreira de Almeida Junior
 
O Jesse Mouta Pereira Batista indicou a seguinte situação. Já fez isto?
 
1. Correções de Desenvolvimento (Penhor e CONRES)
Realizar merge/PR da branch Cesti-teste para a branch oficial.
Aplicar os ajustes dos arquivos:
jboss-modules
cli-offline.sh
OcorrenciaConresWS.java
Gerar nova tag após a aplicação das correções.
Executar nova release/deploy.
Validar o funcionamento e confirmar no grupo.
 
Jesse Mouta Pereira Batista
Paulo Ferreira de Almeida Junior, bom dia   Analise Realizada no SICOW-penhor   O 404 nas releases 1.0.17.9 e 1.0.18.9 acontece porque as tags foram geradas sem o ajuste do arquivo jboss-modules fei…
Funcionou
Código de erro: 500 Internal Server Error
Precisamos confirmar se a senha do usuário de banco e/ou descriptografia da senha pelo vault 
Sandro Araujo Dantas & Daniel Ribeiro da Silva segue .
 
Paulo Ferreira de Almeida Junior
Funcionou 📷 📷 📷 Código de erro: 500 Internal Server Error Precisamos confirmar se a senha do usuário de banco e/ou descriptografia da senha pelo vault Sandro Araujo Dantas & Daniel Ribeiro da Sil…
Pessoal!
 
Quem pode nos ajudar para saber se a senha do Vault está atualizada, por gentileza?
 
Jesse Mouta Pereira Batista
Todos   A esteira do SICOW-penhor-okd (DES) foi regularizada. O módulo Penhor está disponível pelo portal: o login é feito no SICOW-portal-okd e o acesso ao módulo carrega normalmente a tela “SICOW M…
aqui
 
Jesse Mouta Pereira Batista
Paulo Ferreira de Almeida Junior, bom dia   Analise Realizada no SICOW-penhor   O 404 nas releases 1.0.17.9 e 1.0.18.9 acontece porque as tags foram geradas sem o ajuste do arquivo jboss-modules fei…
 
Paulo Ferreira de Almeida Junior
Daniel Ribeiro da Silva
 
Já concluímos esta atividade para todos os módulos?
 
Jesse Mouta Pereira Batista
Paulo Ferreira de Almeida Junior, bom dia   Analise Realizada no SICOW-penhor   O 404 nas releases 1.0.17.9 e 1.0.18.9 acontece porque as tags foram geradas sem o ajuste do arquivo jboss-modules fei…
Situação sobre jboss-modules
 
Módulo	
Adicionar as informações abaixo no arquivo
jboss-modules
	Situação
SICOW_PORTAL_OKD	group_id:artifact_id:version:extension
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar	
Feito


SICOW_PENHOR_OKD
	group_id:artifact_id:version:extension
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar	
Feito

SICOW_NIA_OKD	group_id:artifact_id:version:extension
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar	 
SICOW_SEG_OKD	group_id:artifact_id:version:extension
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar	 

SICOW_IMP_OKD
	group_id:artifact_id:version:extension
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar	 
SICOW_LG_OKD	group_id:artifact_id:version:extension
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar	 
SICOW_MTE_OKD	group_id:artifact_id:version:extension
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar	 
SICOW_CONRES_OKD	group_id:artifact_id:version:extension
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar	 
 
 
 
Jesse Mouta Pereira Batista, boa tarde!
 
Eu estive lendo as suas mensagens e vi que um dos grandes problemas está relacionada ao vault
 
O usuário scowdb01 continua apresentando falha de autenticação na base cowdb001 (10.116.92.41:5116). O mesmo comportamento ocorre no Portal SICOW e no módulo PENHOR.
Enquanto a credencial armazenada no Vault (VAULT::SICOW::SCOWDB01::1) não for corrigida, as funcionalidades que dependem de acesso ao banco de dados poderão retornar erro ou exibir dados incompletos/vazios.
 
Gentileza, saberia me indicar com quem eu devo falar?
 
Sandro Araujo Dantas
Jesse Mouta Pereira Batista, boa tarde!   Eu estive lendo as suas mensagens e vi que um dos grandes problemas está relacionada ao vault   O usuário scowdb01 continua apresentando falha de autenticaçã…
Se mais alguém souber indicar, gentileza, avise-nos 
 
Sandro Araujo Dantas
Jesse Mouta Pereira Batista, boa tarde!   Eu estive lendo as suas mensagens e vi que um dos grandes problemas está relacionada ao vault   O usuário scowdb01 continua apresentando falha de autenticaçã…
Ambiente DES
 
