Pessoal, atualização do SIGSJ-intranet (DES):

✅ Release SIGSJ-intranet-21 concluída, com a aplicação implantada e o Check Deployments OK na caddeapllx955.

Ajustes realizados até aqui:

AlocaIP / Infrafácil: correção do cadastro do servidor, ajuste no size e correção da API do Infrafácil.
Library:
inclusão e correção das variáveis de JVM (heap/metaspace); havia um espaço no valor do Xmx que impedia o JBoss de iniciar;
inclusão das variáveis do Apache (URL_CUSTOMIZADA, URL_ALIAS, URL_REWRITE, URL_REDIRECT), seguindo o modelo do SIICO-unidades-jboss.
standalone-full-ha.xml:
inclusão da extensão e do socket-binding do modcluster, que impediam o JBoss de subir;
inclusão dos logs sirot/ceflib, conforme o ambiente legado;
inclusão de um alias JNDI para o EJB do SIROTCon: a aplicação procura o EJB em java:global/sirotcon-ejb-2.3.0.1-farm/... e a esteira o registra como java:global/sirotcon-ejb/.... Não houve alteração no código.
jboss-deployments: implantação do sirotcon-ejb.jar pela própria esteira, junto com a aplicação.
httpd (vhost.conf): estrutura do Apache criada no repositório de config, usando a URL padrão da esteira.

Ponto de atenção (sem impacto na aplicação): a etapa “Configurando Stack de Monitoração” continua com erro 404 na API do Zabbix (monitoracao.az.cloud.caixa). Ela não bloqueia a release e será tratada com a equipe da esteira/CEMOT.

@Vitor @Lederman, o ambiente já está disponível para os testes de vocês. Se encontrarem algum comportamento estranho, é só avisar aqui.

Próximo passo: vamos seguir agora com o SIGSJ-boleto e trazemos o retorno aqui na sala.
