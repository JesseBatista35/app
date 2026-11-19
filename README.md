1. Confirmar no 473 (10.116.97.79):

bash
LOG=/opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log
grep -a "consultarCorrelationClientePorCPF" $LOG | tail -3
grep -a -A15 "15:08:52,769" $LOG | grep -aE "ERROR|WARN|ARJUNA|Exception|MQJCA|JMS" | head -20

2. WMQ no 7.4, profile do SIFEC (CLI do 471):

/profile=full-ha-sifec-intranet/subsystem=resource-adapters:read-resource(recursive=true)

3. WMQ no 6.4, só no profile do SIFEC (10.116.88.20). Primeiro, ver em quais profiles existe WMQ:

bash
D=/opt/jboss/jboss-eap/dc/configuration/domain.xml
grep -n '<profile name=' $D
grep -n 'resource-adapter id="wmq' $D

Me mande as três saídas. Cruzando os números de linha, descubro qual bloco de WMQ é do SIFEC e te passo o grep exato.

Sobre o documento: como não é do SIPEN, a Claudia provavelmente é do CCR. Na tabela de contatos, troque a linha dela de “SIPEN” para “CCR (teste no 7.4)” antes de mandar.


o jefseron disse isso


O fluxo está completamente saudável e não há nenhuma falha. A linha do MQJCA4016 é apenas uma notificação de rotina durante uma consulta bem-sucedida ao barramento/SICLI.
 
Analisando a saída dos comandos, podemos confirmar quatro pontos importantes:
 
A requisição continuou normalmente. Logo após o MQJCA4016 (às 15:08:52,769), a mesma thread avançou para consultarCorrelationIdPF, executou o ValidaDadosSicliProcessor e realizou as consultas no banco de dados via Hibernate sem nenhuma exceção.
Comportamento padrão em todas as chamadas. Às 15:08:55,213, houve uma segunda chamada idêntica (consultarCorrelationClientePorCPF), que gerou exatamente o mesmo log MQJCA4016 e também seguiu o fluxo normalmente.
Ausência de vazamento de conexões. O comando de busca por erros não retornou nenhum alerta IJ000100 (que é o código que o JBoss EAP emite quando o desenvolvedor esquece de fechar uma conexão e ela vaza do pool).
Por que acontece aqui. Como você está rodando em um ambiente gerenciado (JBoss EAP Domain/Host Controller), o contêiner encerra a conexão JMS ao fim da sub-transação do MQ, e logo em seguida o código da aplicação (ou framework de mensageria) chama close() no ConnectionWrapper, gerando o aviso informativo.
 

[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]# D=/opt/jboss/jboss-eap/dc/configuration/domain.xml
[root@sbrdeapllx0001 p585600]# grep -n '<profile name=' $D
84:        <profile name="default">
302:        <profile name="ha">
598:        <profile name="full">
923:        <profile name="full-ha">
1348:        <profile name="full-ha-siefi">
1758:        <profile name="full-ha-simph">
2129:        <profile name="full-ha-sigch">
2512:        <profile name="full-ha-sitah-mcmv">
2886:        <profile name="full-ha-sipmc-internet">
3363:        <profile name="full-ha-sipmc-intranet">
3841:        <profile name="full-ha-sisdu">
4220:        <profile name="full-ha-siwic">
4571:        <profile name="full-ha-siotp">
5019:        <profile name="full-ha-sisrs">
5427:        <profile name="full-ha-sifes-intranet">
5960:        <profile name="full-ha-sifes-intranet2">
6519:        <profile name="full-ha-sifes-intranet3">
7068:        <profile name="full-ha-sifes-intranet4">
7617:        <profile name="full-ha-sipge">
7963:        <profile name="full-ha-sifes-internet">
8503:        <profile name="full-ha-siric">
8945:        <profile name="full-ha-siatd">
9359:        <profile name="full-ha-sipes">
9780:        <profile name="full-ha-siopi-batch">
10939:        <profile name="full-ha-sigrr">
11383:        <profile name="full-ha-sipen">
11765:        <profile name="full-ha-sigdr">
12250:        <profile name="full-ha-sicve">
12698:        <profile name="full-ha-sicve-internet">
13129:        <profile name="full-ha-siouv">
13597:        <profile name="full-ha-sicdu-cliente-intranet">
14057:        <profile name="full-ha-sicdu-convenio-internet">
14443:        <profile name="full-ha-sirta">
14980:        <profile name="full-ha-sirta2">
15517:        <profile name="full-ha-sirta3">
16054:        <profile name="full-ha-sirta4">
16599:        <profile name="full-ha-sirta5">
17136:        <profile name="full-ha-sievj">
17560:        <profile name="full-ha-siexc">
18058:        <profile name="full-ha-sisfw">
18437:        <profile name="full-ha-siprc">
18837:        <profile name="full-ha-sifec-intranet">
20596:        <profile name="full-ha-sifec-intranet2">
22240:        <profile name="full-ha-sifec-intranet3">
23886:        <profile name="full-ha-sifec-intranet4">
25536:        <profile name="full-ha-sifec-intranet5">
27180:        <profile name="full-ha-sifec-batch">
28628:        <profile name="full-ha-sifec-internet">
29967:        <profile name="full-ha-siico">
30346:        <profile name="full-ha-sipag">
30685:        <profile name="full-ha-sipon">
31023:        <profile name="full-ha-sicli">
31556:        <profile name="full-ha-sisgd-intranet">
31934:        <profile name="full-ha-simcd">
32878:        <profile name="full-ha-sisgd-internet">
33251:        <profile name="full-ha-sictd-digitalizar-intranet">
33756:        <profile name="full-ha-sictd-intranet">
34278:        <profile name="full-ha-sinaf2-prd-legado">
34655:        <profile name="full-ha-sinafweb3-git">
35032:        <profile name="full-ha-sinaf-validador">
35390:        <profile name="full-ha-sigdp">
35819:        <profile name="full-ha-sicrs">
36171:        <profile name="full-ha-siaoi">
36890:        <profile name="full-ha-siarc">
37276:        <profile name="full-ha-siemp">
37717:        <profile name="full-ha-sipld">
38107:        <profile name="full-ha-sinch">
38540:        <profile name="full-ha-sigcr">
38934:        <profile name="full-ha-siaef">
39259:        <profile name="full-ha-siafc">
39596:        <profile name="full-ha-sigfi-ecr">
40037:        <profile name="full-ha-sigfi">
40375:        <profile name="full-ha-sigtc">
40957:        <profile name="full-ha-siccr">
41546:        <profile name="full-ha-sitah-mon">
41937:        <profile name="full-ha-siavl">
42348:        <profile name="full-ha-sisrh">
42670:        <profile name="full-ha-siapc">
43063:        <profile name="full-ha-siara">
43508:        <profile name="full-ha-sicdu-convenio-intranet">
43904:        <profile name="full-ha-sineb">
44471:        <profile name="full-ha-sinad">
44910:        <profile name="full-ha-sigct">
45278:        <profile name="full-ha-siopi-apps">
46461:        <profile name="full-ha-siecm-pre-des">
46816:        <profile name="full-ha-sicve-msw">
47247:        <profile name="full-ha-sigdf">
47612:        <profile name="full-ha-sicli-app">
48077:        <profile name="full-ha-siatd-analise-pauta">
48491:        <profile name="full-ha-sispe">
48873:        <profile name="full-ha-siatd-intranet">
49390:        <profile name="full-ha-siatd-internet">
49871:        <profile name="full-ha-siatd-pauta-intranet">
50280:        <profile name="full-ha-siatd-pauta-internet">
50688:        <profile name="full-ha-sicve-anexo">
51077:        <profile name="full-ha-sivep">
51482:        <profile name="full-ha-sifec-api">
52769:        <profile name="full-ha-sipld-teste">
53135:        <profile name="full-ha-sigec-comercial">
53640:        <profile name="full-ha-jklnctd-sictd-digitalizar-intranet">
54148:        <profile name="full-ha-apdctd-sictd-intranet">
54677:        <profile name="full-ha-sircl">
55111:        <profile name="full-ha-sictd-internet">
55499:        <profile name="full-ha-sicve-api">
55891:        <profile name="full-ha-sicem">
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]#
[root@sbrdeapllx0001 p585600]# grep -n 'resource-adapter id="wmq' $D
3232:                    <resource-adapter id="wmq.jmsra.rar">
3711:                    <resource-adapter id="wmq.jmsra.rar">
4891:                    <resource-adapter id="wmq.jmsra.rar">
5769:                    <resource-adapter id="wmq.jmsra.rar">
6328:                    <resource-adapter id="wmq.jmsra.rar">
6887:                    <resource-adapter id="wmq.jmsra.rar">
7436:                    <resource-adapter id="wmq.jmsra.rar">
8322:                    <resource-adapter id="wmq.jmsra.rar">
8817:                    <resource-adapter id="wmq.jmsra.rar">
10179:                    <resource-adapter id="wmq.jmsra-7.0.1.12-XATransaction">
10375:                    <resource-adapter id="wmq.jmsra-7.0.1.12-NoTransaction">
12133:                    <resource-adapter id="wmq.jmsra.rar">
12568:                    <resource-adapter id="wmq.jmsra.rar">
13012:                    <resource-adapter id="wmq.jmsra.rar">
13453:                    <resource-adapter id="wmq.jmsra.rar">
13914:                    <resource-adapter id="wmq.jmsra.rar">
14790:                    <resource-adapter id="wmq.jmsra.rar">
15327:                    <resource-adapter id="wmq.jmsra.rar">
15864:                    <resource-adapter id="wmq.jmsra.rar">
16409:                    <resource-adapter id="wmq.jmsra.rar">
16946:                    <resource-adapter id="wmq.jmsra.rar">
17945:                    <resource-adapter id="wmq.jmsra.rar">
19607:                    <resource-adapter id="wmq.jmsra.rar">
21342:                    <resource-adapter id="wmq.jmsra.rar">
22988:                    <resource-adapter id="wmq.jmsra.rar">
24638:                    <resource-adapter id="wmq.jmsra.rar">
26282:                    <resource-adapter id="wmq.jmsra.rar">
27876:                    <resource-adapter id="wmq.jmsra.rar">
29276:                    <resource-adapter id="wmq.jmsra.rar">
31344:                    <resource-adapter id="wmq.jmsra.rar">
32356:                    <resource-adapter id="wmq.jmsra.rar">
33555:                    <resource-adapter id="wmq.jmsra.rar">
34077:                    <resource-adapter id="wmq.jmsra.rar">
36502:                    <resource-adapter id="wmq.jmsra-7.5.0.8_NOTX.rar">
36626:                    <resource-adapter id="wmq.jmsra-7.5.0.8_XATX.rar">
36750:                    <resource-adapter id="wmq.jmsra-7.5.0.8_XATX2.rar">
37607:                    <resource-adapter id="wmq.jmsra.rar">
38418:                    <resource-adapter id="wmq.jmsra.rar">
39896:                    <resource-adapter id="wmq.jmsra.rar">
40742:                    <resource-adapter id="wmq.jmsra.rar">
41329:                    <resource-adapter id="wmq.jmsra.rar">
43380:                    <resource-adapter id="wmq.jmsra.rar">
44235:                    <resource-adapter id="wmq.jmsra.rar">
44790:                    <resource-adapter id="wmq.jmsra.rar">
45679:                    <resource-adapter id="wmq.jmsra-7.0.1.12-XATransaction">
45897:                    <resource-adapter id="wmq.jmsra-7.0.1.12-NoTransaction">
47130:                    <resource-adapter id="wmq.jmsra.rar">
47930:                    <resource-adapter id="wmq.jmsra.rar">
49232:                    <resource-adapter id="wmq.jmsra.rar">
49733:                    <resource-adapter id="wmq.jmsra.rar">
52160:                    <resource-adapter id="wmq.jmsra.rar">
53481:                    <resource-adapter id="wmq.jmsra.rar">
53945:                    <resource-adapter id="wmq.jmsra.rar">
54469:                    <resource-adapter id="wmq.jmsra.rar">
56201:                    <resource-adapter id="wmq.jmsra.rar">
[root@sbrdeapllx0001 p585600]#



[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# LOG=/opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# grep -a "consultarCorrelationClientePorCPF" $LOG | tail -3
15:08:52,682 INFO  [ClienteRest] (default task-8) ClienteRest.consultarCorrelationClientePorCPF
15:08:55,213 INFO  [ClienteRest] (default task-8) ClienteRest.consultarCorrelationClientePorCPF
15:08:56,977 INFO  [ClienteRest] (default task-8) ClienteRest.consultarCorrelationClientePorCPF
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# grep -a -A15 "15:08:52,769" $LOG | grep -aE "ERROR|WARN|ARJUNA|Exception|MQJCA|JMS" | head -20
15:08:52,769 INFO  [org.jboss.as.connector.deployers.RaXmlDeployer] (default task-8) wmq.jmsra.rar: MQJCA4016:Identificador de conexões não registrado sendo fechado: 'com.ibm.mq.connector.outbound.ConnectionWrapper@5589a774'.
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#





[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] /server-group=sipen:read-attribute(name=profile)
{
    "outcome" => "success",
    "result" => "full-ha-sipen"
}

[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] /profile=full-ha-sipen/subsystem=resource-adapters:read-resource(recursive=true)
{
    "outcome" => "success",
    "result" => {"resource-adapter" => undefined}
}

[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] /profile=full-ha-sifec-intranet/subsystem=resource-adapters:read-resource(recursive=true)
{
    "outcome" => "success",
    "result" => {"resource-adapter" => {"wmq.jmsra.rar" => {
        "archive" => "wmq.jmsra.rar",
        "beanvalidationgroups" => undefined,
        "bootstrap-context" => undefined,
        "module" => undefined,
        "statistics-enabled" => false,
        "transaction-support" => "NoTransaction",
        "wm-elytron-security-domain" => undefined,
        "wm-security" => false,
        "wm-security-default-groups" => undefined,
        "wm-security-default-principal" => undefined,
        "wm-security-domain" => "other",
        "wm-security-mapping-groups" => undefined,
        "wm-security-mapping-required" => false,
        "wm-security-mapping-users" => undefined,
        "admin-objects" => {
            "SIBAR.REQ.CONSULTA_CLIENTE" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIBAR.REQ.CONSULTA_CLIENTE",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIBAR.REQ.CONSULTA_CLIENTE"},
                    "CCSID" => {"value" => "500"}
                }
            },
            "TRF.RSP.SIPGE" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/TRF.RSP.SIPGE",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "LQ.RSP.SIPGE"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "java:/jms/LQ.RSP.SICLI_SIPLAN" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/LQ.RSP.SICLI_SIPLAN",
                "use-java-context" => false,
                "config-properties" => {
                    "baseQueueName" => {"value" => "LQ.RSP.SICLI_SIPLAN"},
                    "CCSID" => {"value" => "500"}
                }
            },
            "java:/jms/SIFEC.REQ.PORTAL" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIFEC.REQ.PORTAL",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIFEC.REQ.PORTAL"},
                    "CCSID" => {"value" => "1208"}
                }
            },
            "SIBAR.REQ.RELATORIO_AVALIACAO_RISCO" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIBAR.REQ.RELATORIO_AVALIACAO_RISCO",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIBAR.REQ.RELATORIO_AVALIACAO_RISCO"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "SIBAR.REQ.CANCELAMENTO_AVALIACAO_RISCO" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIBAR.REQ.CANCELAMENTO_AVALIACAO_RISCO",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIBAR.REQ.CANCELAMENTO_AVALIACAO_RISCO"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "SIFEC.REQ.RECUPERAR_DADOS_MINUTA" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIFEC.REQ.RECUPERAR_DADOS_MINUTA",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIFEC.REQ.RECUPERAR_DADOS_MINUTA"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "SIBAR.REQ.CONSULTA_AVALIACAO_RISCO" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIBAR.REQ.CONSULTA_AVALIACAO_RISCO",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIBAR.REQ.CONSULTA_AVALIACAO_RISCO"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "java:/jms/SIAPX.RSP.CONSIGNACAO" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIAPX.RSP.CONSIGNACAO",
                "use-java-context" => false,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIAPX.RSP.CONSIGNACAO"},
                    "CCSID" => {"value" => "500"}
                }
            },
            "SINCE.RSP.CONSULTA_CONTRATO" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SINCE.RSP.CONSULTA_CONTRATO",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SINCE.RSP.CONSULTA_CONTRATO"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "SIBAR.RSP.CONSULTA_CLIENTE" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIBAR.RSP.CONSULTA_CLIENTE",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIBAR.RSP.CONSULTA_CLIENTE"},
                    "CCSID" => {"value" => "500"}
                }
            },
            "SINCE.REQ.CONSULTA_CONTRATO" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SINCE.REQ.CONSULTA_CONTRATO",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SINCE.REQ.CONSULTA_CONTRATO"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "TRF.RSP.ITRF01" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/TRF.RSP.ITRF01",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "LQ.RSP.SITRF01"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "SIFEC.RSP.GERAR_MINUTA" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIFEC.RSP.GERAR_MINUTA",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIFEC.RSP.GERAR_MINUTA"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "SIFEC.RSP.RECUPERAR_DADOS_MINUTA" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIFEC.RSP.RECUPERAR_DADOS_MINUTA",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIFEC.RSP.RECUPERAR_DADOS_MINUTA"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "SIBAR.RSP.MANUTENCAO_CLIENTE" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIBAR.RSP.MANUTENCAO_CLIENTE",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIBAR.RSP.MANUTENCAO_CLIENTE"},
                    "CCSID" => {"value" => "500"}
                }
            },
            "java:/jms/SIAPX.REQ.CONSIGNACAO" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIAPX.REQ.CONSIGNACAO",
                "use-java-context" => false,
                "config-properties" => {
                    "baseQueueName" => {"value" => "LQ.RSP.SIARC.BACEN_PESQUISA"},
                    "CCSID" => {"value" => "500"}
                }
            },
            "SICCR.RSP.AVALIACAO_RISCO_CREDITO" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SICCR.RSP.AVALIACAO_RISCO_CREDITO",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SICCR.RSP.AVALIACAO_RISCO_CREDITO"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "SIFEC.REQ.GERAR_MINUTA" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIFEC.REQ.GERAR_MINUTA",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIFEC.REQ.GERAR_MINUTA"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "SIBAR.RSP.CANCELAMENTO_AVALIACAO_RISCO" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIBAR.RSP.CANCELAMENTO_AVALIACAO_RISCO",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIBAR.RSP.CANCELAMENTO_AVALIACAO_RISCO"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "SIBAR.REQ.MANUTENCAO_CLIENTE" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIBAR.REQ.MANUTENCAO_CLIENTE",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIBAR.REQ.MANUTENCAO_CLIENTE"},
                    "CCSID" => {"value" => "500"}
                }
            },
            "java:/jms/SIFEC.RSP.PORTAL" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIFEC.RSP.PORTAL",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIFEC.RSP.PORTAL"},
                    "CCSID" => {"value" => "1208"}
                }
            },
            "java:/jms/LQ.REQ.SICLI_SIPLAN" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/LQ.REQ.SICLI_SIPLAN",
                "use-java-context" => false,
                "config-properties" => {
                    "baseQueueName" => {"value" => "LQ.REQ.SICLI_SIPLAN"},
                    "CCSID" => {"value" => "500"}
                }
            },
            "SIAPX.RSP.AVALIACAO_RISCO_CREDITO" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIAPX.RSP.AVALIACAO_RISCO_CREDITO",
                "use-java-context" => false,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIAPX.RSP.AVALIACAO_RISCO_CREDITO"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "SIEMP.RSP.AVALIACAO_RISCO_CREDITO" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIEMP.RSP.AVALIACAO_RISCO_CREDITO",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIEMP.RSP.AVALIACAO_RISCO_CREDITO"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "SIBAR.REQ.AVALIACAO_RISCO_CREDITO" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIBAR.REQ.AVALIACAO_RISCO_CREDITO",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIBAR.REQ.AVALIACAO_RISCO_CREDITO"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "SIBAR.RSP.RELATORIO_AVALIACAO_RISCO" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIBAR.RSP.RELATORIO_AVALIACAO_RISCO",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIBAR.RSP.RELATORIO_AVALIACAO_RISCO"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            },
            "SIBAR.RSP.AVALIACAO_RISCO_PROTOCOLO" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIBAR.RSP.AVALIACAO_RISCO_PROTOCOLO",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIBAR.RSP.AVALIACAO_RISCO_PROTOCOLO"},
                    "CCSID" => {"value" => "500"}
                }
            },
            "SIBAR.RSP.CONSULTA_AVALIACAO_RISCO" => {
                "class-name" => "com.ibm.mq.connector.outbound.MQQueueProxy",
                "enabled" => true,
                "jndi-name" => "java:/jms/SIBAR.RSP.CONSULTA_AVALIACAO_RISCO",
                "use-java-context" => true,
                "config-properties" => {
                    "baseQueueName" => {"value" => "SIBAR.RSP.CONSULTA_AVALIACAO_RISCO"},
                    "CCSID" => {"value" => "500"},
                    "targetClient" => {"value" => "MQ"}
                }
            }
        },
        "config-properties" => undefined,
        "connection-definitions" => {
            "java:/jms/SicliConnectionFactory2" => {
                "allocation-retry" => undefined,
                "allocation-retry-wait-millis" => undefined,
                "authentication-context" => undefined,
                "authentication-context-and-application" => undefined,
                "background-validation" => false,
                "background-validation-millis" => undefined,
                "blocking-timeout-wait-millis" => undefined,
                "capacity-decrementer-class" => undefined,
                "capacity-decrementer-properties" => undefined,
                "capacity-incrementer-class" => undefined,
                "capacity-incrementer-properties" => undefined,
                "class-name" => "com.ibm.mq.connector.outbound.ManagedQueueConnectionFactoryImpl",
                "connectable" => false,
                "elytron-enabled" => false,
                "enabled" => true,
                "enlistment" => true,
                "enlistment-trace" => false,
                "flush-strategy" => "FailingConnectionOnly",
                "idle-timeout-minutes" => undefined,
                "initial-pool-size" => undefined,
                "interleaving" => false,
                "jndi-name" => "java:/jms/SicliConnectionFactory2",
                "max-pool-size" => 20,
                "mcp" => undefined,
                "min-pool-size" => 0,
                "no-recovery" => false,
                "no-tx-separate-pool" => false,
                "pad-xid" => false,
                "pool-fair" => true,
                "pool-prefill" => false,
                "pool-use-strict-min" => false,
                "recovery-authentication-context" => undefined,
                "recovery-credential-reference" => undefined,
                "recovery-elytron-enabled" => false,
                "recovery-password" => undefined,
                "recovery-plugin-class-name" => undefined,
                "recovery-plugin-properties" => undefined,
                "recovery-security-domain" => undefined,
                "recovery-username" => undefined,
                "same-rm-override" => undefined,
                "security-application" => true,
                "security-domain" => undefined,
                "security-domain-and-application" => undefined,
                "sharable" => true,
                "tracking" => undefined,
                "use-ccm" => true,
                "use-fast-fail" => false,
                "use-java-context" => true,
                "validate-on-match" => undefined,
                "wrap-xa-resource" => true,
                "xa-resource-timeout" => undefined,
                "config-properties" => {
                    "channel" => {"value" => "SYSTEM.DEF.SVRCONN"},
                    "hostName" => {"value" => "10.192.228.145"},
                    "password" => {"value" => "undefined"},
                    "queueManager" => {"value" => "BRD1"},
                    "port" => {"value" => "1414"},
                    "username" => {"value" => "SCLIBD01"}
                }
            },
            "SicliConnectionFactory" => {
                "allocation-retry" => undefined,
                "allocation-retry-wait-millis" => undefined,
                "authentication-context" => undefined,
                "authentication-context-and-application" => undefined,
                "background-validation" => undefined,
                "background-validation-millis" => undefined,
                "blocking-timeout-wait-millis" => undefined,
                "capacity-decrementer-class" => undefined,
                "capacity-decrementer-properties" => undefined,
                "capacity-incrementer-class" => undefined,
                "capacity-incrementer-properties" => undefined,
                "class-name" => "com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl",
                "connectable" => false,
                "elytron-enabled" => false,
                "enabled" => true,
                "enlistment" => true,
                "enlistment-trace" => false,
                "flush-strategy" => "FailingConnectionOnly",
                "idle-timeout-minutes" => undefined,
                "initial-pool-size" => undefined,
                "interleaving" => false,
                "jndi-name" => "java:/jms/SicliConnectionFactory",
                "max-pool-size" => 20,
                "mcp" => undefined,
                "min-pool-size" => 0,
                "no-recovery" => false,
                "no-tx-separate-pool" => false,
                "pad-xid" => false,
                "pool-fair" => true,
                "pool-prefill" => false,
                "pool-use-strict-min" => false,
                "recovery-authentication-context" => undefined,
                "recovery-credential-reference" => undefined,
                "recovery-elytron-enabled" => false,
                "recovery-password" => undefined,
                "recovery-plugin-class-name" => undefined,
                "recovery-plugin-properties" => undefined,
                "recovery-security-domain" => undefined,
                "recovery-username" => undefined,
                "same-rm-override" => undefined,
                "security-application" => false,
                "security-domain" => undefined,
                "security-domain-and-application" => undefined,
                "sharable" => true,
                "tracking" => undefined,
                "use-ccm" => true,
                "use-fast-fail" => false,
                "use-java-context" => true,
                "validate-on-match" => undefined,
                "wrap-xa-resource" => true,
                "xa-resource-timeout" => undefined,
                "config-properties" => {
                    "channel" => {"value" => "SIFEC.SVRCONN"},
                    "hostName" => {"value" => "10.192.224.100"},
                    "password" => {"value" => "SCNLFECD"},
                    "queueManager" => {"value" => "BRD3"},
                    "port" => {"value" => "1415"},
                    "username" => {"value" => "SCNLFECD"}
                }
            },
            "MinutaConnectionFactory" => {
                "allocation-retry" => undefined,
                "allocation-retry-wait-millis" => undefined,
                "authentication-context" => undefined,
                "authentication-context-and-application" => undefined,
                "background-validation" => undefined,
                "background-validation-millis" => undefined,
                "blocking-timeout-wait-millis" => undefined,
                "capacity-decrementer-class" => undefined,
                "capacity-decrementer-properties" => undefined,
                "capacity-incrementer-class" => undefined,
                "capacity-incrementer-properties" => undefined,
                "class-name" => "com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl",
                "connectable" => false,
                "elytron-enabled" => false,
                "enabled" => true,
                "enlistment" => true,
                "enlistment-trace" => false,
                "flush-strategy" => "FailingConnectionOnly",
                "idle-timeout-minutes" => undefined,
                "initial-pool-size" => undefined,
                "interleaving" => false,
                "jndi-name" => "java:/jms/MinutaConnectionFactory",
                "max-pool-size" => 20,
                "mcp" => undefined,
                "min-pool-size" => 0,
                "no-recovery" => false,
                "no-tx-separate-pool" => false,
                "pad-xid" => false,
                "pool-fair" => true,
                "pool-prefill" => false,
                "pool-use-strict-min" => false,
                "recovery-authentication-context" => undefined,
                "recovery-credential-reference" => undefined,
                "recovery-elytron-enabled" => false,
                "recovery-password" => undefined,
                "recovery-plugin-class-name" => undefined,
                "recovery-plugin-properties" => undefined,
                "recovery-security-domain" => undefined,
                "recovery-username" => undefined,
                "same-rm-override" => undefined,
                "security-application" => false,
                "security-domain" => undefined,
                "security-domain-and-application" => undefined,
                "sharable" => true,
                "tracking" => undefined,
                "use-ccm" => true,
                "use-fast-fail" => false,
                "use-java-context" => true,
                "validate-on-match" => undefined,
                "wrap-xa-resource" => true,
                "xa-resource-timeout" => undefined,
                "config-properties" => {
                    "channel" => {"value" => "CHANNEL.SIFEC"},
                    "hostName" => {"value" => "10.192.224.94"},
                    "password" => {"value" => "SCNLFECD"},
                    "queueManager" => {"value" => "QM_broker01_DES"},
                    "port" => {"value" => "1414"},
                    "username" => {"value" => "SCNLFECD"}
                }
            },
            "SiricConnectionFactory" => {
                "allocation-retry" => undefined,
                "allocation-retry-wait-millis" => undefined,
                "authentication-context" => undefined,
                "authentication-context-and-application" => undefined,
                "background-validation" => undefined,
                "background-validation-millis" => undefined,
                "blocking-timeout-wait-millis" => undefined,
                "capacity-decrementer-class" => undefined,
                "capacity-decrementer-properties" => undefined,
                "capacity-incrementer-class" => undefined,
                "capacity-incrementer-properties" => undefined,
                "class-name" => "com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl",
                "connectable" => false,
                "elytron-enabled" => false,
                "enabled" => true,
                "enlistment" => true,
                "enlistment-trace" => false,
                "flush-strategy" => "FailingConnectionOnly",
                "idle-timeout-minutes" => undefined,
                "initial-pool-size" => undefined,
                "interleaving" => false,
                "jndi-name" => "java:/jms/SiricConnectionFactory",
                "max-pool-size" => 20,
                "mcp" => undefined,
                "min-pool-size" => 0,
                "no-recovery" => false,
                "no-tx-separate-pool" => false,
                "pad-xid" => false,
                "pool-fair" => true,
                "pool-prefill" => false,
                "pool-use-strict-min" => false,
                "recovery-authentication-context" => undefined,
                "recovery-credential-reference" => undefined,
                "recovery-elytron-enabled" => false,
                "recovery-password" => undefined,
                "recovery-plugin-class-name" => undefined,
                "recovery-plugin-properties" => undefined,
                "recovery-security-domain" => undefined,
                "recovery-username" => undefined,
                "same-rm-override" => undefined,
                "security-application" => false,
                "security-domain" => undefined,
                "security-domain-and-application" => undefined,
                "sharable" => true,
                "tracking" => undefined,
                "use-ccm" => true,
                "use-fast-fail" => false,
                "use-java-context" => true,
                "validate-on-match" => undefined,
                "wrap-xa-resource" => true,
                "xa-resource-timeout" => undefined,
                "config-properties" => {
                    "channel" => {"value" => "SIFEC.SVRCONN"},
                    "hostName" => {"value" => "10.192.224.100"},
                    "password" => {"value" => "SCNLFECD"},
                    "queueManager" => {"value" => "BRD3"},
                    "port" => {"value" => "1415"},
                    "username" => {"value" => "SCNLFECD"}
                }
            },
            "SiempConnectionFactory_PRD" => {
                "allocation-retry" => undefined,
                "allocation-retry-wait-millis" => undefined,
                "authentication-context" => undefined,
                "authentication-context-and-application" => undefined,
                "background-validation" => undefined,
                "background-validation-millis" => undefined,
                "blocking-timeout-wait-millis" => undefined,
                "capacity-decrementer-class" => undefined,
                "capacity-decrementer-properties" => undefined,
                "capacity-incrementer-class" => undefined,
                "capacity-incrementer-properties" => undefined,
                "class-name" => "com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl",
                "connectable" => false,
                "elytron-enabled" => false,
                "enabled" => true,
                "enlistment" => true,
                "enlistment-trace" => false,
                "flush-strategy" => "FailingConnectionOnly",
                "idle-timeout-minutes" => undefined,
                "initial-pool-size" => undefined,
                "interleaving" => false,
                "jndi-name" => "java:/jms/SiempConnectionFactory_PRD",
                "max-pool-size" => 20,
                "mcp" => undefined,
                "min-pool-size" => 0,
                "no-recovery" => false,
                "no-tx-separate-pool" => false,
                "pad-xid" => false,
                "pool-fair" => true,
                "pool-prefill" => false,
                "pool-use-strict-min" => false,
                "recovery-authentication-context" => undefined,
                "recovery-credential-reference" => undefined,
                "recovery-elytron-enabled" => false,
                "recovery-password" => undefined,
                "recovery-plugin-class-name" => undefined,
                "recovery-plugin-properties" => undefined,
                "recovery-security-domain" => undefined,
                "recovery-username" => undefined,
                "same-rm-override" => undefined,
                "security-application" => false,
                "security-domain" => undefined,
                "security-domain-and-application" => undefined,
                "sharable" => true,
                "tracking" => undefined,
                "use-ccm" => true,
                "use-fast-fail" => false,
                "use-java-context" => true,
                "validate-on-match" => undefined,
                "wrap-xa-resource" => true,
                "xa-resource-timeout" => undefined,
                "config-properties" => {
                    "channel" => {"value" => "SIEMP.SVRCONN"},
                    "hostName" => {"value" => "10.252.176.47"},
                    "password" => {"value" => "SFECEMPP"},
                    "queueManager" => {"value" => "BRPC"},
                    "port" => {"value" => "1418"},
                    "username" => {"value" => "SFECEMPP"}
                }
            },
            "SicliQueueConnectionFactory" => {
                "allocation-retry" => undefined,
                "allocation-retry-wait-millis" => undefined,
                "authentication-context" => undefined,
                "authentication-context-and-application" => undefined,
                "background-validation" => undefined,
                "background-validation-millis" => undefined,
                "blocking-timeout-wait-millis" => undefined,
                "capacity-decrementer-class" => undefined,
                "capacity-decrementer-properties" => undefined,
                "capacity-incrementer-class" => undefined,
                "capacity-incrementer-properties" => undefined,
                "class-name" => "com.ibm.mq.connector.outbound.ManagedQueueConnectionFactoryImpl",
                "connectable" => false,
                "elytron-enabled" => false,
                "enabled" => true,
                "enlistment" => true,
                "enlistment-trace" => false,
                "flush-strategy" => "FailingConnectionOnly",
                "idle-timeout-minutes" => undefined,
                "initial-pool-size" => undefined,
                "interleaving" => false,
                "jndi-name" => "java:/jms/SicliQueueConnectionFactory",
                "max-pool-size" => 20,
                "mcp" => undefined,
                "min-pool-size" => 0,
                "no-recovery" => false,
                "no-tx-separate-pool" => false,
                "pad-xid" => false,
                "pool-fair" => true,
                "pool-prefill" => false,
                "pool-use-strict-min" => false,
                "recovery-authentication-context" => undefined,
                "recovery-credential-reference" => undefined,
                "recovery-elytron-enabled" => false,
                "recovery-password" => undefined,
                "recovery-plugin-class-name" => undefined,
                "recovery-plugin-properties" => undefined,
                "recovery-security-domain" => undefined,
                "recovery-username" => undefined,
                "same-rm-override" => undefined,
                "security-application" => false,
                "security-domain" => undefined,
                "security-domain-and-application" => undefined,
                "sharable" => true,
                "tracking" => undefined,
                "use-ccm" => true,
                "use-fast-fail" => false,
                "use-java-context" => true,
                "validate-on-match" => undefined,
                "wrap-xa-resource" => true,
                "xa-resource-timeout" => undefined,
                "config-properties" => {
                    "channel" => {"value" => "SIEMP.SVRCONN"},
                    "hostName" => {"value" => "brd5brk.desenvolvimento.extracaixa"},
                    "password" => {"value" => "SFECEMPD"},
                    "queueManager" => {"value" => "BRD3"},
                    "port" => {"value" => "1418"},
                    "username" => {"value" => "SFECEMPD"}
                }
            },
            "SiarcConnectionFactory" => {
                "allocation-retry" => undefined,
                "allocation-retry-wait-millis" => undefined,
                "authentication-context" => undefined,
                "authentication-context-and-application" => undefined,
                "background-validation" => undefined,
                "background-validation-millis" => undefined,
                "blocking-timeout-wait-millis" => undefined,
                "capacity-decrementer-class" => undefined,
                "capacity-decrementer-properties" => undefined,
                "capacity-incrementer-class" => undefined,
                "capacity-incrementer-properties" => undefined,
                "class-name" => "com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl",
                "connectable" => false,
                "elytron-enabled" => false,
                "enabled" => true,
                "enlistment" => true,
                "enlistment-trace" => false,
                "flush-strategy" => "FailingConnectionOnly",
                "idle-timeout-minutes" => undefined,
                "initial-pool-size" => undefined,
                "interleaving" => false,
                "jndi-name" => "java:/jms/SiarcConnectionFactory",
                "max-pool-size" => 20,
                "mcp" => undefined,
                "min-pool-size" => 0,
                "no-recovery" => false,
                "no-tx-separate-pool" => false,
                "pad-xid" => false,
                "pool-fair" => true,
                "pool-prefill" => false,
                "pool-use-strict-min" => false,
                "recovery-authentication-context" => undefined,
                "recovery-credential-reference" => undefined,
                "recovery-elytron-enabled" => false,
                "recovery-password" => undefined,
                "recovery-plugin-class-name" => undefined,
                "recovery-plugin-properties" => undefined,
                "recovery-security-domain" => undefined,
                "recovery-username" => undefined,
                "same-rm-override" => undefined,
                "security-application" => false,
                "security-domain" => undefined,
                "security-domain-and-application" => undefined,
                "sharable" => true,
                "tracking" => undefined,
                "use-ccm" => true,
                "use-fast-fail" => false,
                "use-java-context" => true,
                "validate-on-match" => undefined,
                "wrap-xa-resource" => true,
                "xa-resource-timeout" => undefined,
                "config-properties" => {
                    "hostName" => {"value" => "10.192.228.145"},
                    "password" => {"value" => "SRVARCD1"},
                    "queueManager" => {"value" => "BRD1"},
                    "port" => {"value" => "1414"},
                    "channel" => {"value" => "BRSUN033.TO.BRD1"},
                    "transportType" => {"value" => "CLIENT"},
                    "username" => {"value" => "SRVARCD1"}
                }
            },
            "java:/jms/SiapxConnectionFactory" => {
                "allocation-retry" => undefined,
                "allocation-retry-wait-millis" => undefined,
                "authentication-context" => undefined,
                "authentication-context-and-application" => undefined,
                "background-validation" => false,
                "background-validation-millis" => undefined,
                "blocking-timeout-wait-millis" => undefined,
                "capacity-decrementer-class" => undefined,
                "capacity-decrementer-properties" => undefined,
                "capacity-incrementer-class" => undefined,
                "capacity-incrementer-properties" => undefined,
                "class-name" => "com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl",
                "connectable" => false,
                "elytron-enabled" => false,
                "enabled" => true,
                "enlistment" => true,
                "enlistment-trace" => false,
                "flush-strategy" => "FailingConnectionOnly",
                "idle-timeout-minutes" => undefined,
                "initial-pool-size" => undefined,
                "interleaving" => false,
                "jndi-name" => "java:/jms/SiapxConnectionFactory",
                "max-pool-size" => 20,
                "mcp" => undefined,
                "min-pool-size" => 0,
                "no-recovery" => false,
                "no-tx-separate-pool" => false,
                "pad-xid" => false,
                "pool-fair" => true,
                "pool-prefill" => false,
                "pool-use-strict-min" => false,
                "recovery-authentication-context" => undefined,
                "recovery-credential-reference" => undefined,
                "recovery-elytron-enabled" => false,
                "recovery-password" => undefined,
                "recovery-plugin-class-name" => undefined,
                "recovery-plugin-properties" => undefined,
                "recovery-security-domain" => undefined,
                "recovery-username" => undefined,
                "same-rm-override" => undefined,
                "security-application" => false,
                "security-domain" => undefined,
                "security-domain-and-application" => undefined,
                "sharable" => true,
                "tracking" => undefined,
                "use-ccm" => true,
                "use-fast-fail" => false,
                "use-java-context" => true,
                "validate-on-match" => undefined,
                "wrap-xa-resource" => true,
                "xa-resource-timeout" => undefined,
                "config-properties" => {
                    "channel" => {"value" => "SIFEC.SVRCONN"},
                    "hostName" => {"value" => "10.192.224.100"},
                    "password" => {"value" => "undefined"},
                    "queueManager" => {"value" => "BRD3"},
                    "port" => {"value" => "1415"},
                    "username" => {"value" => "SCNLAPXD"}
                }
            },
            "SiempConnectionFactory" => {
                "allocation-retry" => undefined,
                "allocation-retry-wait-millis" => undefined,
                "authentication-context" => undefined,
                "authentication-context-and-application" => undefined,
                "background-validation" => undefined,
                "background-validation-millis" => undefined,
                "blocking-timeout-wait-millis" => undefined,
                "capacity-decrementer-class" => undefined,
                "capacity-decrementer-properties" => undefined,
                "capacity-incrementer-class" => undefined,
                "capacity-incrementer-properties" => undefined,
                "class-name" => "com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl",
                "connectable" => false,
                "elytron-enabled" => false,
                "enabled" => true,
                "enlistment" => true,
                "enlistment-trace" => false,
                "flush-strategy" => "FailingConnectionOnly",
                "idle-timeout-minutes" => undefined,
                "initial-pool-size" => undefined,
                "interleaving" => false,
                "jndi-name" => "java:/jms/SiempConnectionFactory",
                "max-pool-size" => 20,
                "mcp" => undefined,
                "min-pool-size" => 0,
                "no-recovery" => false,
                "no-tx-separate-pool" => false,
                "pad-xid" => false,
                "pool-fair" => true,
                "pool-prefill" => false,
                "pool-use-strict-min" => false,
                "recovery-authentication-context" => undefined,
                "recovery-credential-reference" => undefined,
                "recovery-elytron-enabled" => false,
                "recovery-password" => undefined,
                "recovery-plugin-class-name" => undefined,
                "recovery-plugin-properties" => undefined,
                "recovery-security-domain" => undefined,
                "recovery-username" => undefined,
                "same-rm-override" => undefined,
                "security-application" => false,
                "security-domain" => undefined,
                "security-domain-and-application" => undefined,
                "sharable" => true,
                "tracking" => undefined,
                "use-ccm" => true,
                "use-fast-fail" => false,
                "use-java-context" => true,
                "validate-on-match" => undefined,
                "wrap-xa-resource" => true,
                "xa-resource-timeout" => undefined,
                "config-properties" => {
                    "channel" => {"value" => "SIEMP.SVRCONN"},
                    "hostName" => {"value" => "10.1.14.40"},
                    "password" => {"value" => "SFECEMPD"},
                    "queueManager" => {"value" => "BRD3"},
                    "port" => {"value" => "1415"},
                    "username" => {"value" => "SFECEMPD"}
                }
            },
            "java:/jms/SiapxConnectionFactoryFCE" => {
                "allocation-retry" => undefined,
                "allocation-retry-wait-millis" => undefined,
                "authentication-context" => undefined,
                "authentication-context-and-application" => undefined,
                "background-validation" => false,
                "background-validation-millis" => undefined,
                "blocking-timeout-wait-millis" => undefined,
                "capacity-decrementer-class" => undefined,
                "capacity-decrementer-properties" => undefined,
                "capacity-incrementer-class" => undefined,
                "capacity-incrementer-properties" => undefined,
                "class-name" => "com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl",
                "connectable" => false,
                "elytron-enabled" => false,
                "enabled" => true,
                "enlistment" => true,
                "enlistment-trace" => false,
                "flush-strategy" => "FailingConnectionOnly",
                "idle-timeout-minutes" => undefined,
                "initial-pool-size" => undefined,
                "interleaving" => false,
                "jndi-name" => "java:/jms/SiapxConnectionFactoryFCE",
                "max-pool-size" => 20,
                "mcp" => undefined,
                "min-pool-size" => 0,
                "no-recovery" => false,
                "no-tx-separate-pool" => false,
                "pad-xid" => false,
                "pool-fair" => true,
                "pool-prefill" => false,
                "pool-use-strict-min" => false,
                "recovery-authentication-context" => undefined,
                "recovery-credential-reference" => undefined,
                "recovery-elytron-enabled" => false,
                "recovery-password" => undefined,
                "recovery-plugin-class-name" => undefined,
                "recovery-plugin-properties" => undefined,
                "recovery-security-domain" => undefined,
                "recovery-username" => undefined,
                "same-rm-override" => undefined,
                "security-application" => false,
                "security-domain" => undefined,
                "security-domain-and-application" => undefined,
                "sharable" => true,
                "tracking" => undefined,
                "use-ccm" => true,
                "use-fast-fail" => false,
                "use-java-context" => true,
                "validate-on-match" => undefined,
                "wrap-xa-resource" => true,
                "xa-resource-timeout" => undefined,
                "config-properties" => {
                    "channel" => {"value" => "SIFEC.SVRCONN"},
                    "hostName" => {"value" => "10.192.224.100"},
                    "password" => {"value" => "undefined"},
                    "queueManager" => {"value" => "BRD7"},
                    "port" => {"value" => "1416"},
                    "username" => {"value" => "SCNLFECD"}
                }
            },
            "java:/jms/TrfConnectionFactory" => {
                "allocation-retry" => undefined,
                "allocation-retry-wait-millis" => undefined,
                "authentication-context" => undefined,
                "authentication-context-and-application" => undefined,
                "background-validation" => undefined,
                "background-validation-millis" => undefined,
                "blocking-timeout-wait-millis" => undefined,
                "capacity-decrementer-class" => undefined,
                "capacity-decrementer-properties" => undefined,
                "capacity-incrementer-class" => undefined,
                "capacity-incrementer-properties" => undefined,
                "class-name" => "com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl",
                "connectable" => false,
                "elytron-enabled" => false,
                "enabled" => true,
                "enlistment" => true,
                "enlistment-trace" => false,
                "flush-strategy" => "FailingConnectionOnly",
                "idle-timeout-minutes" => undefined,
                "initial-pool-size" => undefined,
                "interleaving" => false,
                "jndi-name" => "java:/jms/TrfConnectionFactory",
                "max-pool-size" => 20,
                "mcp" => undefined,
                "min-pool-size" => 0,
                "no-recovery" => false,
                "no-tx-separate-pool" => false,
                "pad-xid" => false,
                "pool-fair" => true,
                "pool-prefill" => false,
                "pool-use-strict-min" => false,
                "recovery-authentication-context" => undefined,
                "recovery-credential-reference" => undefined,
                "recovery-elytron-enabled" => false,
                "recovery-password" => undefined,
                "recovery-plugin-class-name" => undefined,
                "recovery-plugin-properties" => undefined,
                "recovery-security-domain" => undefined,
                "recovery-username" => undefined,
                "same-rm-override" => undefined,
                "security-application" => false,
                "security-domain" => undefined,
                "security-domain-and-application" => undefined,
                "sharable" => true,
                "tracking" => undefined,
                "use-ccm" => true,
                "use-fast-fail" => false,
                "use-java-context" => true,
                "validate-on-match" => undefined,
                "wrap-xa-resource" => true,
                "xa-resource-timeout" => undefined,
                "config-properties" => {
                    "channel" => {"value" => "SIPGE.SVRCONN"},
                    "hostName" => {"value" => "10.216.80.111"},
                    "queueManager" => {"value" => "RJH1"},
                    "port" => {"value" => "1414"},
                    "username" => {"value" => "SPGETRFT"}
                }
            },
            "java:/jms/SinceConnectionFactory" => {
                "allocation-retry" => undefined,
                "allocation-retry-wait-millis" => undefined,
                "authentication-context" => undefined,
                "authentication-context-and-application" => undefined,
                "background-validation" => undefined,
                "background-validation-millis" => undefined,
                "blocking-timeout-wait-millis" => undefined,
                "capacity-decrementer-class" => undefined,
                "capacity-decrementer-properties" => undefined,
                "capacity-incrementer-class" => undefined,
                "capacity-incrementer-properties" => undefined,
                "class-name" => "com.ibm.mq.connector.outbound.ManagedConnectionFactoryImpl",
                "connectable" => false,
                "elytron-enabled" => false,
                "enabled" => true,
                "enlistment" => true,
                "enlistment-trace" => false,
                "flush-strategy" => "FailingConnectionOnly",
                "idle-timeout-minutes" => undefined,
                "initial-pool-size" => undefined,
                "interleaving" => false,
                "jndi-name" => "java:/jms/SinceConnectionFactory",
                "max-pool-size" => 20,
                "mcp" => undefined,
                "min-pool-size" => 0,
                "no-recovery" => false,
                "no-tx-separate-pool" => false,
                "pad-xid" => false,
                "pool-fair" => true,
                "pool-prefill" => false,
                "pool-use-strict-min" => false,
                "recovery-authentication-context" => undefined,
                "recovery-credential-reference" => undefined,
                "recovery-elytron-enabled" => false,
                "recovery-password" => undefined,
                "recovery-plugin-class-name" => undefined,
                "recovery-plugin-properties" => undefined,
                "recovery-security-domain" => undefined,
                "recovery-username" => undefined,
                "same-rm-override" => undefined,
                "security-application" => false,
                "security-domain" => undefined,
                "security-domain-and-application" => undefined,
                "sharable" => true,
                "tracking" => undefined,
                "use-ccm" => true,
                "use-fast-fail" => false,
                "use-java-context" => true,
                "validate-on-match" => undefined,
                "wrap-xa-resource" => true,
                "xa-resource-timeout" => undefined,
                "config-properties" => {
                    "channel" => {"value" => "SINCE.SVRCONN"},
                    "hostName" => {"value" => "10.192.224.66"},
                    "queueManager" => {"value" => "QSDA"},
                    "port" => {"value" => "1420"},
                    "username" => {"value" => "SNCEMQD1"}
                }
            }
        }
    }}}
}

[domain@localhost:9999 /]
