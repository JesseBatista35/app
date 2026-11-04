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



[p585600@cbrdeapllx473 ~]$ ls -l /usr/java/openjdk-1.8.0.482/jre/lib/security/cacerts
-r--r--r-- 1 root root 165797 Jan 18  2026 /usr/java/openjdk-1.8.0.482/jre/lib/security/cacerts
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$






[domain@localhost:9443 /] /server-group=sifec-intranet/system-property=javax.net.ssl.trustStore:read-resource
{
    "outcome" => "success",
    "result" => {
        "boot-time" => true,
        "value" => "C:/Desenvolvimento/JDK/jdk1.8.0_231/jre/lib/security/cacerts"
    }
}

[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /] /server-group=sifec-intranet/jvm=*:read-resource
{
    "outcome" => "success",
    "result" => [{
        "address" => [
            ("server-group" => "sifec-intranet"),
            ("jvm" => "SIFEC-JVM")
        ],
        "outcome" => "success",
        "result" => {
            "agent-lib" => undefined,
            "agent-path" => undefined,
            "env-classpath-ignored" => undefined,
            "environment-variables" => undefined,
            "heap-size" => "8192m",
            "java-agent" => undefined,
            "java-home" => undefined,
            "jvm-options" => [
                "-Djava.awt.headless=true",
                "-Dhttp.proxyHost=proxydes.caixa",
                "-Dhttp.proxyPort=80",
                "-Dhttps.proxyHost=proxydes.caixa",
                "-Dhttps.proxyPort=80",
                "-Dhttps.protocols=TLSv1.2",
                "-Dhttp.nonProxyHosts=10.195.192.1|172.28.10.49|.caixa|*.intra.caixa.gov.br|*.extracaixa|*.siapenet.gov.br|*.caixa.gov.br",
                "-Dhttp.proxySet=true",
                "-Duser.language=pt",
                "-Duser.country=BR",
                "-Duser.timezone=GMT-3"
            ],
            "launch-command" => undefined,
            "max-heap-size" => "8192m",
            "max-permgen-size" => "2048m",
            "module-options" => undefined,
            "permgen-size" => "2048m",
            "stack-size" => undefined,
            "type" => undefined
        }
    }]
}

[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
