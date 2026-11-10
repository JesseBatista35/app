Marcio, a release do internet em DES está falhando porque o SIROT agora vai embutido no EAR, mas faltam duas bibliotecas que ele usa: ceflog-1.0.0.0-farm.jar e ceflib-2.5.0.1.jar. O erro é ClassNotFoundException: br.gov.caixa.log.Log.

O intranet leva as duas na pasta lib/ do EAR. Consegue incluir as duas no pom do internet, igual está no intranet, e gerar um novo build?

Do nosso lado, já tiramos o SIROT externo do servidor e ajustamos o config para o embutido. Com o build novo, rodamos a release de novo.
