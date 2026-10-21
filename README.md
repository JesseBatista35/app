Pessoal, atualização do SIGSJ-boleto (DES):

✅ Release concluída, com o boletoService-ear.ear implantado e o Check Deployments OK na caddeapllx2557. Contexto publicado: /boletoService.

Ajustes realizados até aqui:

Aplicação: o EAR declarava no jboss-deployment-structure.xml uma dependência com o nome versionado do SIROTCon (deployment.sirotcon-ejb-2.3.0.1-farm.jar), mas a esteira publica o EJB como sirotcon-ejb.jar. Para destravar o deploy, ajustamos essa linha diretamente na master do SIGSJ-boleto para deployment.sirotcon-ejb.jar, alterando apenas a dependência.
standalone-full-ha.xml: inclusão da extensão e do socket-binding do modcluster e dos logs sirot/ceflib, conforme o legado.
jboss-deployments: implantação do sirotcon-ejb.jar pela própria esteira, junto com a aplicação.
Library:
variáveis de URL trocadas para a padrão da esteira (sigsj-boleto.esteiras.des.caixa);
http_context_default definido como boletoService;
correção de um espaço no valor de uma variável que impedia o JBoss de iniciar.

Pontos de atenção:

A aplicação procura um arquivo de log4j externo em /log_jboss/config-log4j/sigsj_ws_boleto.xml, que não existe no servidor novo. Não impede o deploy, mas a aplicação fica sem essa configuração de log. Vamos levantar o modelo do legado e incluir na esteira.
@Vitor, como o ajuste foi feito na master, consegue validar o commit e sincronizar com alguma branch de desenvolvimento em andamento, para ele não se perder? Confirme também se a dependência do sirotcon-ejb no pom.xml do EAR está com <scope>provided</scope>.

@Vitor @Lederman, o ambiente já está disponível para os testes de vocês. Se encontrarem algum comportamento estranho, é só avisar aqui.
