Antes de alterar, confira onde está a propriedade. No jboss-cli do 471:

/server-group=sifec-intranet/system-property=javax.net.ssl.trustStore:read-resource
/server-group=sifec-intranet/jvm=*:read-resource

No 473, confirme que o arquivo existe:

bash
ls -l /usr/java/openjdk-1.8.0.482/jre/lib/security/cacerts

Me mande as saídas que eu te passo o comando exato. Depende se a propriedade está em system-property ou em jvm-options. A troca exige reload ou restart do sifec-intranet, então combine o horário com a sala.

Há outras variáveis com caminho do Windows também, como SIAPX_WS_MPOG_TRUST_STORE=C:/kit/java/... e DATAPREV_CERTIFICADO_CAIXA_PATH=C:/Users/.... Vale revisar junto com o time, porque outros módulos (SIAPX, integração Dataprev) devem falhar pelo mesmo motivo.

2. SIEMP-EMPRESAS: mesmo padrão do EMP e do PJ (CDI)

WELD-001408: Unsatisfied dependencies for type ParametrizacaoService
  at ParametrizacaoRest.parametrizacaoService

Já são três sistemas com o mesmo tipo de erro: um REST que injeta um service por @Inject e o Weld não encontra a implementação. Em todos eles isso funciona no 6.4. Isso reforça que é a diferença de descoberta de beans do CDI do 7.4. Há duas saídas:

o dev ajustar o código (@Local/implements ou beans.xml);
ou testarmos o require-bean-descriptor=true no subsystem weld, que também exige reload. Dá para aproveitar o mesmo reload da correção da truststore e testar EMP, EMPRESAS e PJ de uma vez.

Frase para a sala:

“O RURAL falhou por configuração de ambiente: o JVM do SIFEC aponta a truststore para um caminho do Windows (C:/Desenvolvimento/...). Vou corrigir para a cacerts do servidor, o que precisa de um reload. O EMPRESAS falhou pelo mesmo padrão de CDI do EMP e do PJ (ParametrizacaoService). No mesmo reload, posso testar uma configuração do Weld compatível com o 6.4, que pode destravar os três. Podemos agendar esse reload?”
