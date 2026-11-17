Correção do Denilson (recomendada). Criar o arquivo siemp-web/src/test/resources/jasperreports.properties com:
net.sf.jasperreports.awt.ignore.missing.font=true

Ele vale só para os testes e não muda o relatório gerado em produção.

Paliativo para chegar ao Sonar hoje. No MVN_GOAL:
clean verify -Dversion.app=$(version.app) -Dmaven.test.failure.ignore=true -U

O build segue até o fim, o JaCoCo gera o relatório e o Quality Gate é avaliado com a cobertura real. Tire esse parâmetro assim que o dev subir o ajuste das fontes.

Não recomendo instalar as fontes da Microsoft no agente. O agente é compartilhado, e esse problema é do teste, não da esteira.

Ainda pendentes, sem relação com os testes:

Corrigir a crítica nova no Sonar. Sem isso, a condição 16.702 > 16.701 continua reprovando.
O -Dversion.app= segue vazio.
Como o Claude está se saindo nesta sessão?
