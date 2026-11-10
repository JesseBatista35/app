1. Na 471: qual versão do LCR está no 7.4
sudo /opt/jboss/jboss-eap/bin/jboss-cli.sh --connect --controller=localhost:9999

Dentro do CLI, liste tudo do server-group e a versão de cada deployment:

/server-group=sifec-intranet:read-children-resources(child-type=deployment)

Procure na saída o que tiver lcr ou silcr. O runtime-name é o arquivo/versão que está implantado.

Para ver também os pacotes enviados ao domain que ainda não foram atribuídos ao grupo:

:read-children-names(child-type=deployment)
2. Na 473: confirmar no log a versão que subiu e os erros do Weld
sudo grep -nE "WFLYSRV0027.*(lcr|LCR)|WFLYSRV0010.*(lcr|LCR)|WFLYSRV0021|WELD-001408|WELD-001409" /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | tail -20
WFLYSRV0027 mostra qual arquivo começou a implantar.
WELD-001408 (dependência não encontrada) e WELD-001409 (mais de uma candidata) são os erros do CDI que o Jeferson descreveu.
3. Na sbrdeapllx0001 (6.4): qual versão roda hoje
sudo grep -niE 'lcr' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -iE 'deployment|runtime-name'
Atenção à versão

O Jeferson citou a silcr-1.19.0-b152.ear, mas a planilha de PRD do Paulo indica sifec_lcr_1.117.1. Os nomes e as numerações são diferentes. Pode ser que tenhamos subido um pacote que não corresponde ao que está em produção. Antes de levar os erros de CDI para o dev, confirme com os comandos acima qual versão está no 7.4 e qual roda no 6.4.

Se a versão do 7.4 não for a da planilha: o próximo passo é localizar e subir a sifec_lcr_1.117.1 e ver se o erro continua.
Se for a mesma: os erros de injeção (DadosSICLIDao, AliquotasIofDao e o Logger em UserProfile) são de código e empacotamento. Vão para o dev, como a análise do Jeferson aponta.

Me manda as saídas que eu fecho a análise e monto a mensagem para a sala.




[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$ sudo grep -nE "WFLYSRV0027.*(lcr|LCR)|WFLYSRV0010.*(lcr|LCR)|WFLYSRV0021|WELD-001408|WELD-001409" /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | tail -20

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for p585600:
18084:11:20:08,980 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 89) WFLYSRV0021: O procedimento da implantação "sifec-sirur-2.9.3-b928.ear" foi revertido com mensagem de falha:
25274:11:24:34,795 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 91) WFLYSRV0021: O procedimento da implantação "sifec-sirur-2.9.3-b928.ear" foi revertido com mensagem de falha:
26341:11:30:41,816 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 148) WFLYSRV0021: O procedimento da implantação "sifec-sirur-3.54.51.28.ear" foi revertido com mensagem de falha:
55788:15:11:44,584 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-5) WFLYSRV0027: Iniciando a implantação do "SILCR" (runtime-name: "silcr-1.19.0-b152.ear")
56623:org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type DadosSICLIDao with qualifiers @Default
56642:org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type AliquotasIofDao with qualifiers @Default
56661:org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Logger with qualifiers @Default
56690:  Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type DadosSICLIDao with qualifiers @Default
56708:  Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type AliquotasIofDao with qualifiers @Default
56726:  Suppressed: org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Logger with qualifiers @Default
56750:org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type DadosSICLIDao with qualifiers @Default
56769:org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type AliquotasIofDao with qualifiers @Default
56788:org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Logger with qualifiers @Default
56812:org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type DadosSICLIDao with qualifiers @Default
56831:org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type AliquotasIofDao with qualifiers @Default
56850:org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Logger with qualifiers @Default
56871:15:11:48,408 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 173) WFLYSRV0021: O procedimento da implantação "silcr-1.19.0-b152.ear" foi revertido com mensagem de falha:
56875:org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type DadosSICLIDao with qualifiers @Default
56894:org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type AliquotasIofDao with qualifiers @Default
56913:org.jboss.weld.exceptions.DeploymentException: WELD-001408: Unsatisfied dependencies for type Logger with qualifiers @Default
[p585600@cbrdeapllx473 ~]$




-sh-4.1$
-sh-4.1$
-sh-4.1$ sudo grep -niE 'lcr' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -iE 'deployment|runtime-name'
[sudo] password for p585600:
20507:                <secure-deployment name="lcr-web.war">
22151:                <secure-deployment name="lcr-web.war">
23797:                <secure-deployment name="lcr-web.war">
25447:                <secure-deployment name="lcr-web.war">
27091:                <secure-deployment name="lcr-web.war">
28557:                <secure-deployment name="lcr-web.war">
29932:                <secure-deployment name="lcr-web.war">
56675:        <deployment name="SILCR" runtime-name="silcr-1.19.0-b152.ear">
57741:                <deployment name="SILCR" runtime-name="silcr-1.19.0-b152.ear"/>
-sh-4.1$
-sh-4.1$
-sh-4.1$
-sh-4.1$

[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] /server-group=sifec-intranet:read-children-resources(child-type=deployment)
{
    "outcome" => "success",
    "result" => {
        "SICCR-BDCAIXA" => {
            "enabled" => true,
            "name" => "SICCR-BDCAIXA",
            "runtime-name" => "sifec-bdcaixa-2.0.1-b39.ear"
        },
        "SICCR-HUB-FRONTEND" => {
            "enabled" => true,
            "name" => "SICCR-HUB-FRONTEND",
            "runtime-name" => "hub-web-1.4.0-b378.ear"
        },
        "SICCR-PJ" => {
            "enabled" => true,
            "name" => "SICCR-PJ",
            "runtime-name" => "workflow-credito-pj-ear-8.40.1-20261105.202759-10.ear"
        },
        "SICDT-FEC" => {
            "enabled" => true,
            "name" => "SICDT-FEC",
            "runtime-name" => "sifec-cdt-3.24.3.003.ear"
        },
        "SIFEC" => {
            "enabled" => true,
            "name" => "SIFEC",
            "runtime-name" => "sifec-2.160.4.0.ear"
        },
        "SIFEC-CCR" => {
            "enabled" => true,
            "name" => "SIFEC-CCR",
            "runtime-name" => "SIFEC-CCR-6.3.0-b4587.ear"
        },
        "SIFEC-FBN4" => {
            "enabled" => true,
            "name" => "SIFEC-FBN4",
            "runtime-name" => "sifec-fbn-1.0.1.0-b84.ear"
        },
        "SIFEC-MINUTAS-FRONT" => {
            "enabled" => true,
            "name" => "SIFEC-MINUTAS-FRONT",
            "runtime-name" => "gerenciador-minutas-web-1.0.0-b14.ear"
        },
        "SQLSERVER-sqljdbc4.jar" => {
            "enabled" => true,
            "name" => "SQLSERVER-sqljdbc4.jar",
            "runtime-name" => "SQLSERVER-sqljdbc4.jar"
        },
        "framework-2.0.1-des.jar" => {
            "enabled" => true,
            "name" => "framework-2.0.1-des.jar",
            "runtime-name" => "framework.jar"
        },
        "framework_sisgd-1.0.0" => {
            "enabled" => true,
            "name" => "framework_sisgd-1.0.0",
            "runtime-name" => "framework_sisgd.jar"
        },
        "idmsjdbc-17.1.4.0.jar" => {
            "enabled" => true,
            "name" => "idmsjdbc-17.1.4.0.jar",
            "runtime-name" => "idmsjdbc-17.1.4.0.jar"
        },
        "idmsjdbc.jar" => {
            "enabled" => true,
            "name" => "idmsjdbc.jar",
            "runtime-name" => "idmsjdbc.jar"
        },
        "jconn4.jar" => {
            "enabled" => true,
            "name" => "jconn4.jar",
            "runtime-name" => "jconn4.jar"
        },
        "jconn42.jar" => {
            "enabled" => true,
            "name" => "jconn42.jar",
            "runtime-name" => "jconn42.jar"
        },
        "ojdbc6.jar" => {
            "enabled" => true,
            "name" => "ojdbc6.jar",
            "runtime-name" => "ojdbc6.jar"
        },
        "ojdbc7-12.1.0.2.jar" => {
            "enabled" => true,
            "name" => "ojdbc7-12.1.0.2.jar",
            "runtime-name" => "ojdbc7-12.1.0.2.jar"
        },
        "ojdbc8-19.19.0.0.jar" => {
            "enabled" => true,
            "name" => "ojdbc8-19.19.0.0.jar",
            "runtime-name" => "ojdbc8-19.19.0.0.jar"
        },
        "wmq.jmsra.rar" => {
            "enabled" => true,
            "name" => "wmq.jmsra.rar",
            "runtime-name" => "wmq.jmsra.rar"
        }
    }
}

[domain@localhost:9999 /] :read-children-names(child-type=deployment)
{
    "outcome" => "success",
    "result" => [
        "SIAEF",
        "SIAFC",
        "SIAOI",
        "SIAPC",
        "SIAPX_JavaWeb",
        "SIARA",
        "SIARC",
        "SIATD-INTERNET",
        "SIATD-INTRANET",
        "SIBAN-CONSTRUCARD",
        "SIBAN-MCM",
        "SIBAN-MCM2",
        "SICCR-BDCAIXA",
        "SICCR-DOCUMENTOS",
        "SICCR-DOCUMENTOS2",
        "SICCR-DOCUMENTOS3",
        "SICCR-HUB-BACKEND2",
        "SICCR-HUB-BACKEND3",
        "SICCR-HUB-BACKEND4",
        "SICCR-HUB-BACKEND5",
        "SICCR-HUB-FRONTEND",
        "SICCR-HUB-FRONTEND2",
        "SICCR-HUB-FRONTEND3",
        "SICCR-HUB-FRONTEND4",
        "SICCR-HUB-FRONTEND5",
        "SICCR-INTEGRACAO",
        "SICCR-MINUTAS",
        "SICCR-PARAMETROS",
        "SICCR-PARAMETROS2",
        "SICCR-PARAMETROS3",
        "SICCR-PARAMETROS4",
        "SICCR-PARAMETROS5",
        "SICCR-PJ",
        "SICCR-PJ-INTERNET",
        "SICCR-PJ2",
        "SICCR-PJ3",
        "SICCR-PJ4",
        "SICCR-PJ5",
        "SICCR-TRIBUTOS",
        "SICDT-FEC",
        "SICDT-FEC2",
        "SICDT-FEC3",
        "SICDT-FEC4",
        "SICDT-FEC5",
        "SICDU-CONVENIADO-INTERNET.ear",
        "SICEM",
        "SICLI-APP",
        "SICLI-NCC",
        "SICRS",
        "SICTD-APDCTD",
        "SICTD-DIGITALIZAR-INTRANET",
        "SICTD-JKLNCTD",
        "SICTD-SERVER",
        "SICVE",
        "SICVE-ANEXO",
        "SICVE-API",
        "SICVE-TIMER",
        "SIECM-PRE-DES",
        "SIEMP",
        "SIEMP-EMPRESAS",
        "SIEVJ",
        "SIFEC",
        "SIFEC-API",
        "SIFEC-BAN",
        "SIFEC-BAN2",
        "SIFEC-BAN3",
        "SIFEC-BAN4",
        "SIFEC-BAN5",
        "SIFEC-BATCH",
        "SIFEC-BNDES-ONLINE",
        "SIFEC-CCR",
        "SIFEC-CCR-API",
        "SIFEC-CCR2",
        "SIFEC-CCR3",
        "SIFEC-CCR4",
        "SIFEC-CCR5",
        "SIFEC-CONSTRUCARD",
        "SIFEC-EMP",
        "SIFEC-EMP-MGE",
        "SIFEC-EMP2",
        "SIFEC-EMP3",
        "SIFEC-EMP4",
        "SIFEC-EMP5",
        "SIFEC-FBN4",
        "SIFEC-GARANTIAS",
        "SIFEC-GARANTIAS2",
        "SIFEC-GARANTIAS3",
        "SIFEC-GARANTIAS4",
        "SIFEC-GARANTIAS5",
        "SIFEC-INTEGRACAO",
        "SIFEC-INTEGRACAO2",
        "SIFEC-INTEGRACAO3",
        "SIFEC-INTEGRACAO4",
        "SIFEC-INTEGRACAO5",
        "SIFEC-INTERNET",
        "SIFEC-INTERNET-EMP",
        "SIFEC-IR",
        "SIFEC-MINUTA-API2",
        "SIFEC-MINUTAS-FRONT",
        "SIFEC-NOVOEX",
        "SIFEC-ORIGINACAO2",
        "SIFEC-ORIGINACAO3",
        "SIFEC-ORIGINACAO5",
        "SIFEC-PEN",
        "SIFEC-RURAL",
        "SIFEC-RURAL2",
        "SIFEC-RURAL3",
        "SIFEC-RURAL4",
        "SIFEC-RURAL5",
        "SIFEC2",
        "SIFEC3",
        "SIFEC4",
        "SIFEC5",
        "SIFEC6",
        "SIFEC_ADDR",
        "SIFES",
        "SIFES-INTERNET",
        "SIFES2",
        "SIFES3",
        "SIFES4",
        "SIGCH",
        "SIGCR",
        "SIGCT",
        "SIGDF",
        "SIGDP",
        "SIGDR",
        "SIGEC-COMERCIAL",
        "SIGFI_ECR",
        "SIGRR_vTMP-JBOSS_EAP.9.ear",
        "SIGTC",
        "SILCR",
        "SINAD",
        "SINAF-VALIDADOR",
        "SINAF2-PRD-LEGADO",
        "SINAFWEB",
        "SIOPI-INTRANET",
        "SIOPI-JDBC-SYBASE-jconn3.jar",
        "SIOPI-WS",
        "SIOTP",
        "SIOUV",
        "SIPEN",
        "SIPES",
        "SIPGE",
        "SIPLD",
        "SIPLD-NARQ",
        "SIPLD-TESTE",
        "SIPMC-INTERNET",
        "SIPMC-INTRANET",
        "SIPON",
        "SIPRC",
        "SIRCL",
        "SIRIC",
        "SIRTA",
        "SIRTA2",
        "SIRUR",
        "SIRUR-INTERNET",
        "SIRUR2",
        "SISDU",
        "SISRS",
        "SITAH-MON",
        "SIVEP",
        "SIWIC",
        "SQLSERVER-sqljdbc4.jar",
        "conppwextratorjb.ear",
        "conppwservice.ear",
        "consoleppware.ear",
        "framework-2.0.1-des.jar",
        "framework_sisgd-1.0.0",
        "guia.ear",
        "idmsjdbc-17.1.4.0.jar",
        "idmsjdbc.jar",
        "jconn4.jar",
        "jconn42.jar",
        "ojdbc6-11.2.0.4.0.jar",
        "ojdbc6.jar",
        "ojdbc7-12.1.0.2.jar",
        "ojdbc8-19.19.0.0.jar",
        "postgresql-42.2.22.jre7.jar",
        "postgresql-42.2.29.jar",
        "postgresql-42.2.29.jre7.jar",
        "postgresql-42.6.0.jar",
        "postgresql-9.0-801.jdbc4.jar",
        "postgresql-9.1-901-1.jdbc4.jar",
        "postgresql-9.4.1212.jre7.jar",
        "sicdu-cliente.ear",
        "sicdu-conveniado.ear",
        "siefi-ear.ear",
        "siico.ear",
        "sipag_des.ear",
        "sisgdinternet.ear",
        "sitah_pmcmv_V1.0.8.8.ear",
        "wmq.jmsra-7.0.1.12-transaction.rar",
        "wmq.jmsra-7.5.0.8.rar",
        "wmq.jmsra.rar"
    ]
}

[domain@localhost:9999 /]





