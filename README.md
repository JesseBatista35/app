Como confirmar (2 minutos)

Abra direto os dois arquivos na develop:
https://github.com/caixagithub/siobs-intra-administracaopingfederate/blob/develop/PostmanCollection/SIOBS-AppPingFederate.postman_environment.json
https://github.com/caixagithub/siobs-intra-administracaopingfederate/blob/develop/SiobsAppPingFederate/Database/DbInitializer.cs
No primeiro arquivo, dê Ctrl+F por access_token e veja se o campo value ainda tem o JWT. Esse é o alerta #8.
No segundo, dê Ctrl+F por HashedRefreshToken e veja se os valores dos cli-ser-oba e TaobfOykDNc7... ainda estão lá. Esses são os alertas #6 e #5.
Alternativa: na barra de busca do topo do GitHub, use repo:caixagithub/siobs-intra-administracaopingfederate HashedRefreshToken. Essa busca procura conteúdo, mas só na branch padrão.
