deployment-info --server-group=sifec-intranet

2. Abrir o log no 473, em outra sessão:

bash
sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -iE --line-buffered "WFLYSRV0010|WFLYSRV0021|faltam|QuerySyntax|Registered web context"

3. Ativar, no jboss-cli do 471:

deploy --name=<NOME-DA-PRIMEIRA-COLUNA> --server-groups=sifec-intranet

Ou pela console: Deployments → Server Groups → sifec-intranet → (+) → Deploy Existing Content, e escolha o 8.40.1.

Como ler o resultado:

✅ Funcionou se aparecer Registered web context: '/workflow-credito-pj-web' e WFLYSRV0010 ... foi implantado. Peça para testarem o link do PJ no SIFEC.
❌ Se aparecer WFLYSRV0021 ou faltam [...], me cola as linhas.


[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$
[p585600@cbrdeapllx473 ~]$ sudo tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -iE --line-buffered "WFLYSRV0010|WFLYSRV0021|faltam|QuerySyntax|Registered web context"

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for p585600:



[domain@localhost:9443 /] deployment-info --server-group=sifec-intranet
NAME                               RUNTIME-NAME                                  STATE
SIAEF                              siaef-1.0.188-b223.ear                        not added
SIAFC                              siafc-1.0.123-b7.ear                          not added
SIAOI                              siaoi.ear                                     not added
SIAPC                              siapc-02.00.00.01-b74.ear                     not added
SIAPX_JavaWeb                      sifec-apx-1.7.9.4-b40.ear                     not added
SIARA                              siara-1.2.1.3-b11.ear                         not added
SIARC                              siarc_EAP6.ear                                not added
SIATD-INTERNET                     siatdEAR-3.70.4.0-b195.ear                    not added
SIATD-INTRANET                     siatdEAR-3.71.5.0-b2185.ear                   not added
SIBAN-CONSTRUCARD                  construcard-ma-1.0.0-b5.ear                   not added
SIBAN-MCM                          mcm-1.0.1.23-b47.ear                          not added
SIBAN-MCM2                         mcm-1.0.0.25-b45.ear                          not added
SICCR-BDCAIXA                      sifec-bdcaixa-2.0.1-b39.ear                   enabled
SICCR-DOCUMENTOS                   SIFEC-MANTERDOCUMENTO-2.2.7-b91.ear           not added
SICCR-DOCUMENTOS2                  SIFEC-MANTERDOCUMENTO-2.2.7-b94.ear           not added
SICCR-DOCUMENTOS3                  SIFEC-MANTERDOCUMENTO-2.2.7-b88.ear           not added
SICCR-HUB-BACKEND2                 hub-api-2.2.0-b809.ear                        not added
SICCR-HUB-BACKEND3                 hub-api-1.18.0-b744.ear                       not added
SICCR-HUB-BACKEND4                 hub-api-1.18.0-b745.ear                       not added
SICCR-HUB-BACKEND5                 hub-api-2.2.0-b807.ear                        not added
SICCR-HUB-FRONTEND                 hub-web-1.4.0-b378.ear                        enabled
SICCR-HUB-FRONTEND2                hub-web-1.10.0.1-b418.ear                     not added
SICCR-HUB-FRONTEND3                hub-web-1.7.0-b397.ear                        not added
SICCR-HUB-FRONTEND4                hub-web-1.4.0-b383.ear                        not added
SICCR-HUB-FRONTEND5                hub-web-1.10.0.1-b417.ear                     not added
SICCR-INTEGRACAO                   componente-calculo-web-1.0.0-b74.war          not added
SICCR-MINUTAS                      sifec-minutaGarantias-1.0.0-b36.ear           not added
SICCR-PARAMETROS                   sifec-ccr-parametros-3.2.0.1-b1073.ear        not added
SICCR-PARAMETROS2                  sifec-ccr-parametros-3.3.1.2-b1170.ear        not added
SICCR-PARAMETROS3                  sifec-ccr-parametros-3.3.1.1-b1172.ear        not added
SICCR-PARAMETROS4                  sifec-ccr-parametros-3.3.1.1-b1177.ear        not added
SICCR-PARAMETROS5                  sifec-ccr-parametros-3.3.1.2-b1180.ear        not added
SICCR-PJ                           sifec-ccr-pj.ear                              not added
SICCR-PJ-INTERNET                  sifec-ccr-pj-5.8.0.1-b72.ear                  not added
SICCR-PJ2                          sifec-ccr-pj-8.40.0.3-b5717.ear               not added
SICCR-PJ3                          sifec-ccr-pj-8.40.0.3-b5719.ear               not added
SICCR-PJ4                          sifec-ccr-pj-8.40.0.3-b5718.ear               not added
SICCR-PJ5                          sifec-ccr-pj-8.39.0.1-b5681.ear               not added
SICCR-TRIBUTOS                     sifec-tributos-1.1.0-b7.ear                   not added
SICDT-FEC                          sifec-cdt-3.23.5.4-b2448.ear                  not added
SICDT-FEC2                         sifec-cdt-3.22.1-b2421.ear                    not added
SICDT-FEC3                         sifec-cdt-3.21.0-b2394.ear                    not added
SICDT-FEC4                         sifec-cdt-3.23.5.5-b2449.ear                  not added
SICDT-FEC5                         sifec-cdt-3.23.5.6-b2454.ear                  not added
SICDU-CONVENIADO-INTERNET.ear      SICDU-CONVENIADO-INTERNET.ear                 not added
SICEM                              SicemWEB_6.1.0.13.06.war                      not added
SICLI-APP                          sicli_api-01.114.01-b623.ear                  not added
SICLI-NCC                          sicli.ear                                     not added
SICRS                              sicrs-2.3.134-b40.ear                         not added
SICTD-APDCTD                       sictd-server-intranet_3.31.37.4.ear           not added
SICTD-DIGITALIZAR-INTRANET         sictd-digitalizar-intranet_3.13.49.133.51.ear not added
SICTD-JKLNCTD                      sictd-digitalizar-intranet_3.31.37.4.ear      not added
SICTD-SERVER                       sictd-server-intranet_3.13.49.133.51.ear      not added
SICVE                              sicve-1.0-1.0-b2933.ear                       not added
SICVE-ANEXO                        sicve-anexo-1.0-1.0-b53.ear                   not added
SICVE-API                          sicve-1.0-1.0-b1.ear                          not added
SICVE-TIMER                        sicve-timer-1.0-1.0-b463.ear                  not added
SIECM-PRE-DES                      siecm-preteste.ear                            not added
SIEMP                              siemp-ear-14.37.0.6.ear                       not added
SIEMP-EMPRESAS                     empresas-1.2.3-b15.ear                        not added
SIEVJ                              sievj.ear                                     not added
SIFEC                              sifec-2.160.3.0.ear                           enabled
SIFEC-API                          sifec-2.160.0.0.ear                           not added
SIFEC-BAN                          sifec-ban-1.8.1-b122.ear                      not added
SIFEC-BAN2                         sifec-ban-1.8.1-b120.ear                      not added
SIFEC-BAN3                         sifec-ban-1.7.0-b117.ear                      not added
SIFEC-BAN4                         sifec-ban-1.7.0-b104.ear                      not added
SIFEC-BAN5                         sifec-ban-1.8.1-b119.ear                      not added
SIFEC-BATCH                        fec-2.47.0.0-b2.ear                           not added
SIFEC-BNDES-ONLINE                 sifec-bndes-1.1.0-b8.ear                      not added
SIFEC-CCR                          SIFEC-CCR-6.3.0-b4587.ear                     enabled
SIFEC-CCR-API                      originacao-api-parent-1.0.0-b9.ear            not added
SIFEC-CCR2                         SIFEC-CCR-6.3.0-b4591.ear                     not added
SIFEC-CCR3                         SIFEC-CCR-6.0.0-b4564.ear                     not added
SIFEC-CCR4                         SIFEC-CCR-4.24.1-b4437.ear                    not added
SIFEC-CCR5                         SIFEC-CCR-6.4.0-b4589.ear                     not added
SIFEC-CONSTRUCARD                  construcard-1.23.1.2-b64.ear                  not added
SIFEC-EMP                          emp-3.95.0.1-b1437.ear                        not added
SIFEC-EMP-MGE                      mge-1.0.0-b14.ear                             not added
SIFEC-EMP2                         emp-3.92.1.1-b1459.ear                        not added
SIFEC-EMP3                         emp-3.95.0.1-b1436.ear                        not added
SIFEC-EMP4                         emp-3.95.0.1-b1458.ear                        not added
SIFEC-EMP5                         emp-3.92.1.1-b1408.ear                        not added
SIFEC-FBN4                         sifec-fbn-1.0.1.0-b84.ear                     not added
SIFEC-GARANTIAS                    garantias-1.9.0-b187.ear                      not added
SIFEC-GARANTIAS2                   garantias-1.9.0-b186.ear                      not added
SIFEC-GARANTIAS3                   garantias-1.8.0.2-b178.ear                    not added
SIFEC-GARANTIAS4                   garantias-1.8.0.3-b183.ear                    not added
SIFEC-GARANTIAS5                   garantias-1.8.0.3-b183.ear                    not added
SIFEC-INTEGRACAO                   componente-dataprev-web-1.0.0-b488.war        not added
SIFEC-INTEGRACAO2                  componente-dataprev-web-1.0.0-b491.war        not added
SIFEC-INTEGRACAO3                  componente-srcc-web-1.0.0-b449.war            not added
SIFEC-INTEGRACAO4                  componente-dataprev-web-1.0.0-b385.war        not added
SIFEC-INTEGRACAO5                  componente-dataprev-web-1.0.0-b490.war        not added
SIFEC-INTERNET                     fec-2.2.0.1-b131.ear                          not added
SIFEC-INTERNET-EMP                 emp-3.2.3-b3.ear                              not added
SIFEC-IR                           sifec-ir-1.3.0.1-b36.ear                      not added
SIFEC-MINUTA-API2                  gerenciador-minutas-api-1.0.0-b97.ear         not added
SIFEC-MINUTAS-FRONT                gerenciador-minutas-web-1.0.0-b14.ear         enabled
SIFEC-NOVOEX                       sifec-novoex-0.0.0.1-b32.ear                  not added
SIFEC-ORIGINACAO2                  sifec-originacao-3.11.1-b344.ear              not added
SIFEC-ORIGINACAO3                  sifec-originacao-4.0.0-b377.ear               not added
SIFEC-ORIGINACAO5                  sifec-originacao-4.0.0-b376.ear               not added
SIFEC-PEN                          pen-1.1.0.4-b25.ear                           not added
SIFEC-RURAL                        rural-2.115.0.1-b2446.ear                     not added
SIFEC-RURAL2                       rural-2.114.0.0-b2422.ear                     not added
SIFEC-RURAL3                       rural-2.115.0.1-b2420.ear                     not added
SIFEC-RURAL4                       rural-2.115.1.1-b2421.ear                     not added
SIFEC-RURAL5                       rural-2.112.0.0-b2317.ear                     not added
SIFEC2                             fec-2.160.0.0-b2435.ear                       not added
SIFEC3                             fec-2.160.1.0-b2437.ear                       not added
SIFEC4                             fec-2.160.0.0-b2430.ear                       not added
SIFEC5                             fec-2.160.0.0-b2416.ear                       not added
SIFEC6                             fec-2.143.1.1-b1923.ear                       not added
SIFEC_ADDR                         sifec-2.160.0.0-b-20261022.181925-1.ear       not added
SIFES                              fes-3.110.0.0-b97.ear                         not added
SIFES-INTERNET                     fes-3.109.3.0-b1051.ear                       not added
SIFES2                             fes-3.108.5.0-b69.ear                         not added
SIFES3                             fes-3.108.3.0-b85.ear                         not added
SIFES4                             fes-3.111.0.0-b71.ear                         not added
SIGCH                              SIGCH_V1.0.2.0.21.ear                         not added
SIGCR                              bei010caixa.ear                               not added
SIGCT                              sigct-3.10.0.1-3.10.0.1-b4.ear                not added
SIGDF                              sigdf_02012018_1715.ear                       not added
SIGDP                              sigdp_5.4_270.ear                             not added
SIGDR                              sigdr.ear                                     not added
SIGEC-COMERCIAL                    com-1.0.41.4-b86.ear                          not added
SIGFI_ECR                          sigfi-ecr-1.8.0-1.8.0-b439.ear                not added
SIGRR_vTMP-JBOSS_EAP.9.ear         SIGRR_vTMP-JBOSS_EAP.9.ear                    not added
SIGTC                              gtc-1.0.0.0-b56.ear                           not added
SILCR                              silcr-1.19.0-b152.ear                         not added
SINAD                              sinad-ear-1.7.0.2.ear                         not added
SINAF-VALIDADOR                    sinaf_validador_ds200.ear                     not added
SINAF2-PRD-LEGADO                  sinaf-1.68.044-b31.ear                        not added
SINAFWEB                           sinaf3.ear                                    not added
SIOPI-INTRANET                     SIOPIIntranet-1352-20240808.155611-1.ear      not added
SIOPI-JDBC-SYBASE-jconn3.jar       SIOPI-JDBC-SYBASE-jconn3.jar                  not added
SIOPI-WS                           SIOPIWs-1352-20240808.155618-1.ear            not added
SIOTP                              siotp_1.0.20.ear                              not added
SIOUV                              siouv-5.20.10.01-b249.ear                     not added
SIPEN                              sipen-2.29.0.1-2.29.0.1-b1893.ear             not added
SIPES                              sipes-1.27.1.1-b242.ear                       not added
SIPGE                              SIPGE_ReferencialTecnico_20170314.ear         not added
SIPLD                              sipld-3.75.0.0-b201.ear                       not added
SIPLD-NARQ                         sipld-nvarq-3.42.0.1-b25.ear                  not added
SIPLD-TESTE                        sipld-1.1.0.1.0-b3.ear                        not added
SIPMC-INTERNET                     sipmc_internet_ear_1.001.1.11.029.ear         not added
SIPMC-INTRANET                     sipmc-intranet-1.001.1.10.027-b70.ear         not added
SIPON                              SIPON.ear                                     not added
SIPRC                              SIPRC_Build.ear                               not added
SIRCL                              SIRCL_web.war                                 not added
SIRIC                              ric-web-2.0.3.4-b61.ear                       not added
SIRTA                              sirta-06.47.10-06.47.10-b2902.ear             not added
SIRTA2                             sirta-06.47.10-06.47.10-b2903.ear             not added
SIRUR                              sifec-sirur-2.9.3-b928.ear                    not added
SIRUR-INTERNET                     sifec-sirur-3.5.10.1-b187.ear                 not added
SIRUR2                             sifec-sirur-0.5.0.1-0.5.0.1-b231.ear          not added
SISDU                              sisdu-0.0.0.1-0.0.0.1-b1.ear                  not added
SISRS                              sisrs.ear                                     not added
SITAH-MON                          sitah-mon-V1.0.1.1.76.ear                     not added
SIVEP                              sivep-0.0.1-b20.ear                           not added
SIWIC                              siwic.ear                                     not added
SQLSERVER-sqljdbc4.jar             SQLSERVER-sqljdbc4.jar                        enabled
conppwextratorjb.ear               conppwextratorjb.ear                          not added
conppwservice.ear                  conppwservice.ear                             not added
consoleppware.ear                  consoleppware.ear                             not added
framework-2.0.1-des.jar            framework.jar                                 enabled
framework_sisgd-1.0.0              framework_sisgd.jar                           enabled
guia.ear                           guia.ear                                      not added
idmsjdbc-17.1.4.0.jar              idmsjdbc-17.1.4.0.jar                         enabled
idmsjdbc.jar                       idmsjdbc.jar                                  enabled
jconn4.jar                         jconn4.jar                                    enabled
jconn42.jar                        jconn42.jar                                   enabled
ojdbc6-11.2.0.4.0.jar              ojdbc6-11.2.0.4.0.jar                         not added
ojdbc6.jar                         ojdbc6.jar                                    enabled
ojdbc7-12.1.0.2.jar                ojdbc7-12.1.0.2.jar                           enabled
ojdbc8-19.19.0.0.jar               ojdbc8-19.19.0.0.jar                          enabled
postgresql-42.2.22.jre7.jar        postgresql-42.2.22.jre7.jar                   not added
postgresql-42.2.29.jar             postgresql-42.2.29.jar                        not added
postgresql-42.2.29.jre7.jar        postgresql-42.2.29.jre7.jar                   not added
postgresql-42.6.0.jar              postgresql-42.6.0.jar                         not added
postgresql-9.0-801.jdbc4.jar       postgresql-9.0-801.jdbc4.jar                  not added
postgresql-9.1-901-1.jdbc4.jar     postgresql-9.1-901-1.jdbc4.jar                not added
postgresql-9.4.1212.jre7.jar       postgresql-9.4.1212.jre7.jar                  not added
sicdu-cliente.ear                  sicdu-cliente.ear                             not added
sicdu-conveniado.ear               sicdu-conveniado.ear                          not added
siefi-ear.ear                      siefi-ear.ear                                 not added
siico.ear                          siico.ear                                     not added
sipag_des.ear                      sipag_des.ear                                 not added
sisgdinternet.ear                  sisgdinternet.ear                             not added
sitah_pmcmv_V1.0.8.8.ear           sitah_mcmv.ear                                not added
wmq.jmsra-7.0.1.12-transaction.rar wmq.jmsra-7.0.1.12.rar                        not added
wmq.jmsra-7.5.0.8.rar              wmq.jmsra-7.5.0.8.rar                         not added
wmq.jmsra.rar                      wmq.jmsra.rar                                 enabled

[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
[domain@localhost:9443 /]
