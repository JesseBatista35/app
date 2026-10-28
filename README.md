Boa tarde,
Eu faço parte do time do SIPGC na esteira devops em .net 8 C#.
Configuramos o VAULT em DES/TQS e para funcionar corretamente, você nos auxiliou na configuração de uma variável na esteira referente ao proxy.
 
Iremos fazer um teste de deploy em PRD e precisamos saber se na Mudança já passamos o valor dessa variável ou só solicitamos que seja configurado por eles o valor em PRD.
Módulo: SIPGC-API-DES/TQS
Jesse Mouta Pereira Batista
03/09/2026 15:34
_ENV.HTTP_PROXY
http://proxydes.caixa:80
 
_ENV.HTTPS_PROXY
http://proxydes.caixa:80
 
_ENV.NO_PROXY
.caixa,localhost,127.0.0.1,10.116.92.247,.svc,.svc.cluster.local,10.0.0.0/8


