Pessoal, bom dia! Atualização do SIGSJ (configuração dos properties pela esteira):

Orientação do Rafael: seguir o padrão Replace Tokens + Library — os arquivos de properties ficam com placeholders (tokens) e os valores de cada ambiente ficam na Library por stage (EC DES/TQS/HMP/PRD), igual já é feito no standalone. O passo de Replace Tokens da esteira processa os arquivos de configuration/properties/.

O que já fizemos, testamos e validamos: tokenizei os properties (config.properties, b2b.properties, release.properties), configurei as variáveis na Library de DES e rodei a release do intranet. Validado: a esteira substituiu os tokens pelos valores corretos na VM e a aplicação continuou OK. Ou seja, o modelo funciona ponta a ponta.

Próximos passos — precisamos dos valores dos outros ambientes. Pra alimentar as Libraries de TQS, HMP e PRD, preciso dos valores destas variáveis em cada ambiente (o DES eu já tenho):

sigsj.convivencia.url (serviço de convivência)
simtr.url (API do SIMTR)
base do B2B/clote (http://host:porta)
base do B2B internet (equivalente ao sigsj.b2b.des... de cada ambiente)
sigsj.release (versão)

Ponto pro time da aplicação (Gisele/Marcio): sobre o sigsj.release — cada ambiente tem uma versão diferente ou é sempre a mesma? Se for diferente por ambiente, mantemos ela na Library por stage; se for sempre a mesma, fica fixa. Isso ajuda a definir como tratar essa variável.

Assim que o Vitor trouxer os valores de TQS/HMP/PRD, eu replico nos 3 módulos (intranet, internet e boleto) e deixo tudo pronto pra qualquer ambiente, sem ajuste manual.

Quer que eu deixe mais enxuta ou está boa nesse nível pra postar?
