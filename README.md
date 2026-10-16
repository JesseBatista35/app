
sihdg-angular18-tqs-27-deploy   0/1       Completed   0          97m
sihdg-angular18-tqs-28-deploy   0/1       Completed   0          81m
sihdg-angular18-tqs-28-xw6jj    2/2       Running     0          81m
sihdg-backend-tqs-142-deploy    0/1       Completed   0          87d
sihdg-backend-tqs-143-deploy    0/1       Completed   0          41d
sihdg-backend-tqs-143-wltb8     1/1       Running     0          41d
sihdg-frontend-tqs-78-deploy    0/1       Completed   0          235d
sihdg-frontend-tqs-79-deploy    0/1       Completed   0          150d
sihdg-frontend-tqs-79-lb6fz     2/2       Running     0          150d
sihdg-jboss8-tqs-46-deploy      0/1       Completed   0          21m
sihdg-jboss8-tqs-47-7rsv2       1/1       Running     0          2m16s
sihdg-jboss8-tqs-47-deploy      0/1       Completed   0          2m19s
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ curl -sk https://sihdg-jboss8-tqs.apps.nprd.caixa/sihdg-api/api/seguranca/configuracao-seguranca; echo
{"realm":"intranet","idCliente":"cli-web-hdg","urlServidorAutorizacao":"https://login.tqs.caixa/auth","tempoVidaToken":300,"tempoMaximoIdle":-1,"versaoApi":"3.22.0.3"}
-sh-4.2$



atualizamos o STANDALONE para pegar os valores da library
 
Entao
 
mais o problema não está no standalone
 
agora o problema e outro
 
mas antes, estava fixo, login.des no standalone
 
eu vi isso mais ele nao pega dai
 
pera ai jaja vou te explicar
 
rsrsrs



 a sandra disse isso 


 entao quandp faz o processo de enstra no link da seguranca em uma abab anonima ele funciona. porem quando entra direto ele ano funica precisasrmo corrgiri isso
 
