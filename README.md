Jesse Mouta Pereira Batista
Todos   Resumo do dia 18/11: Migração JBoss 7.4 (SIFEC/SICCR), DES   Ajustes de ambiente   Datasource IDMS (jdbc/IdmsSiapxDS, SIAPX): no 7.4, o datasource estava sem validação de conexão e sem idle-t…
Claudia Florisbela Freitas boa noite! Consegue fazer este teste para gente no ambiente 7.4: Pendente: reteste do /v8/contratos/simular com token intranet e internet. 
 
Alessandro Ricardo Lima
Claudia Florisbela Freitas boa noite! Consegue fazer este teste para gente no ambiente 7.4: Pendente: reteste do /v8/contratos/simular com token intranet e internet.
Matheus Gabriel de Oliveira Rodrigues já fez. Está funcionando!
 
Gustavo Duarte Lepesteur da Costa adicionou Igor Dreher Sparrenberger ao chat e compartilhou todo o histórico de chats.

 
Prezados, boa tarde!
 
Poderiam, por gentileza, atualizar o pacote do SIFEC-CCR conforme o arquivo anexo?
A atualização corrige a configuração do hibernate.dialect, alterando-a para Oracle12cDialect, pois o dialect anterior gerava SQL incompatível com o Oracle.
 
Desde já, agradeço.
 
Jesse Mouta Pereira Batista
SIFEC-CCR 1.ear
 
Jesse Mouta Pereira Batista
*Pode, por favor, retirar esse "1" do nome do arquivo que o teams adicionou.
 
Thiago Jeferson de Sousa Silva
Michael Lourant de Oliveira Ferreira   SIRUR (sifec-sirur-3.55.51.05.ear)   Durante a implantação do pacote sifec-sirur-3.55.51.05.ear foi identificada falha na fase inicial de validação estrutural…
Prezados,
 
Versão 3.55.51.06 disponível: http://binario.caixa:8081/repository/releases/br/gov/caixa/sirur/sifec-sirur/3.55.51.06/sifec-sirur-3.55.51.06.ear
 
Thiago Jeferson de Sousa Silva, consegue fazer esses Deploys? Acho que o Jesse está fora no momento.
 
Boa tarde, Jesse Mouta Pereira Batista! Por gentileza, poderia fazer um deploy do SIPEN?
 
Link do ear: http://binario.caixa:8081/repository/releases/br/gov/caixa/sipen/pen-ear/2.32.0.2/pen-ear-2.32.0.2.ear
 
Michael Lourant de Oliveira Ferreira Gustavo Duarte Lepesteur da Costa Claudia Florisbela Freitas
 
SIRUR - sifec-sirur-3.55.51.06.ear
 
Foi realizada análise diretamente no conteúdo armazenado no repositório do Domain Controller.

O artefato sifec-sirur-3.55.51.06.ear encontra-se íntegro (unzip -t sem erros), descartando corrupção na transferência ou armazenamento.

Contudo, no arquivo META-INF/MANIFEST.MF foi identificado problema de formatação no atributo Dependencies.

Trecho encontrado:

Dependencies: deployment.framework.jar, deployment.wmq.jmsra.rar,

[TAB][TAB][TAB][TAB]

[TAB][TAB][TAB][TAB]deployment.framework_sisgd.jar


A análise hexadecimal do manifesto confirma a existência de uma linha contendo apenas caracteres TAB:

0d 0a 09 09 09 09 0d 0a

Durante o deployment o WildFly/JDK falha na leitura do manifesto com:

java.io.IOException: invalid header field
 
 
SIFEC-CCR - SIFEC-CCR.ear

Deploy do pacote concluído com sucesso às 13:27:28. O log do JBoss confirma a implantação da aplicação SIFEC-CCR:
 
13:27:28,071 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 140) WFLYSRV0010: "SIFEC-CCR" foi implantado (runtime-name: "SIFEC-CCR.ear")

 
Patricia Vourakis Barbosa Braga Flavio de Almeida Gagliardi Jesse Mouta Pereira Batista PC 
 
Thiago Jeferson de Sousa Silva
Michael Lourant de Oliveira Ferreira Gustavo Duarte Lepesteur da Costa Claudia Florisbela Freitas   SIRUR - sifec-sirur-3.55.51.06.ear   Foi realizada análise diretamente no conteúdo armazenado no re…

Obrigada 🙏🏼
 
