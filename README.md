O SIPEN roda no cbrdeapllx409, no servidor sipen_node1_DES_llx409.

1. Ver se o servidor está no ar (CLI do 471):

/host=hc_cbrdeapllx409/server=sipen_node1_DES_llx409:read-attribute(name=server-state)

Tem que vir running.

2. Descobrir o IP do 409 (sai do CLI com quit ou abre outra aba no 471):

bash
getent hosts cbrdeapllx409

3. Log no 409 (com o IP do passo 2):

bash
ssh p585600@<IP que apareceu>
sudo su
LOG=/opt/jboss/jboss-eap/hc/servers/sipen_node1_DES_llx409/log/server.log; ls -l $LOG
tail -f $LOG | grep -aiE "pen-ear|SIPEN|WFLYSRV00(10|21)|WFLYCTL0013|WFLYCTL0412|WELD-001408|ERROR|Contexto web registrado"

Se o ls -l der erro, rode ls -d /opt/jboss/jboss-eap/hc/servers/*/ e me mande a saída.

4. Com o log aberto, faça o deploy no CLI do 471:

deploy /tmp/pen-ear-2.32.0.2.ear --name=SIPEN --runtime-name=pen-ear-2.32.0.2.ear --force

Me mande as saídas do CLI e do log.



ain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] /host=hc_cbrdeapllx409/server=sipen_node1_DES_llx409:read-attribute(name=server-state)
{
    "outcome" => "success",
    "result" => "running"
}

[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /]
[domain@localhost:9999 /] quit
[root@cbrdeapllx471 tmp]#
[root@cbrdeapllx471 tmp]#
[root@cbrdeapllx471 tmp]# getent hosts cbrdeapllx409
[root@cbrdeapllx471 tmp]#
[root@cbrdeapllx471 tmp]#
[root@cbrdeapllx471 tmp]# ^C
[root@cbrdeapllx471 tmp]#



networks
hosts
      networks VLANs lines AS CM import/export manage help
search result

GestióIP
#interno.todos



IP	hostname	description-SD	site	type	AI	comment	reservado	vendor	hostname_Manual	OS	CM	model	Localização	network			

    	10.116.97.41	 CBRDEAPLLX409	REQ000145389635 - WO0000081423922 - SIPEN	CTC											

 


  editdelete   descriptionsitetypecommentAIUTreservadovendorhostname_ManualOSCMmodelLocalização

          GestióIP v3.1


















          
[domain@localhost:9999 /]
[domain@localhost:9999 /] deploy /tmp/pen-ear-2.32.0.2.ear --name=SIPEN --runtime-name=pen-ear-2.32.0.2.ear --force
{"WFLYDC0074: Operation failed or was rolled back on all servers. Server failures:" => {"server-group" => {"sipen" => {"host" => {"hc_cbrdeapllx409" => {"sipen_node1_DES_llx409" => {"WFLYC
TL0080: Falha de serviços" => {"jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".\"pen-web-2.32.0.2.war\".INSTALL" => "WFLYSRV0153: Falha ao processar a fase INSTALL de subdeployment \"pen-web-2.32.
0.2.war\" of deployment \"pen-ear-2.32.0.2.ear\"
    Caused by: org.jboss.msc.service.DuplicateServiceException: WFLYUT0105: Host e caminho de contexto estão ocupados, service jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".\"pen-web-2.32.0.2.war
\".undertow-deployment.UndertowDeploymentInfoService não podem ser registrados. A mensagem foi: Service jboss.undertow.deployment.default-server.default-host./sipen.UndertowDeploymentInfoService is a
lready registered"},"WFLYCTL0412: Serviços necessários que não estão instalados:" => ["jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".\"pen-web-2.32.0.2.war\".deploymentCompleteService"],"WFLYCTL0
180: Os serviços com falta/indisponibilidade de dependências " => ["jboss.deployment.unit.\"pen-ear-2.32.0.2.ear\".deploymentCompleteService faltam [jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".
\"pen-web-2.32.0.2.war\".deploymentCompleteService]"]}}}}}}}

[domain@localhost:9999 /]



[sudo] password for p585600:
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]# LOG=/opt/jboss/jboss-eap/hc/servers/sipen_node1_DES_llx409/log/server.log; ls -l $LOG
-rw-r--r-- 1 jboss jboss 6141864 Nov 19 14:25 /opt/jboss/jboss-eap/hc/servers/sipen_node1_DES_llx409/log/server.log
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]#
[root@cbrdeapllx409 p585600]# tail -f $LOG | grep -aiE "pen-ear|SIPEN|WFLYSRV00(10|21)|WFLYCTL0013|WFLYCTL0412|WELD-001408|ERROR|Contexto web registrado"
2026-11-19 14:13:27,320 WARN  [org.jgroups.protocols.UDP] (mcast-receiver-4,ejb,hc_cbrdeapllx409:sipen_node1_DES_llx409) JGRP000010: packet from 10.116.96.151:45688 has different version (3.2.18) than ours (4.2.23); packet is discarded (received 4 identical messages from 10.116.96.151:45688 in the last 64317 ms)
2026-11-19 14:15:25,439 WARN  [org.jgroups.protocols.UDP] (mcast-receiver-4,ejb,hc_cbrdeapllx409:sipen_node1_DES_llx409) JGRP000010: packet from 10.116.96.151:45688 has different version (3.2.18) than ours (4.2.23); packet is discarded (received 8 identical messages from 10.116.96.151:45688 in the last 118119 ms)
2026-11-19 14:16:39,425 WARN  [org.jgroups.protocols.UDP] (mcast-receiver-4,ejb,hc_cbrdeapllx409:sipen_node1_DES_llx409) JGRP000010: packet from 10.116.96.151:45688 has different version (3.2.18) than ours (4.2.23); packet is discarded (received 4 identical messages from 10.116.96.151:45688 in the last 73986 ms)
2026-11-19 14:17:51,005 WARN  [org.jgroups.protocols.UDP] (mcast-receiver-4,ejb,hc_cbrdeapllx409:sipen_node1_DES_llx409) JGRP000010: packet from 10.116.96.151:45688 has different version (3.2.18) than ours (4.2.23); packet is discarded (received 3 identical messages from 10.116.96.151:45688 in the last 71580 ms)
2026-11-19 14:19:30,332 WARN  [org.jgroups.protocols.UDP] (mcast-receiver-4,ejb,hc_cbrdeapllx409:sipen_node1_DES_llx409) JGRP000010: packet from 10.116.96.151:45688 has different version (3.2.18) than ours (4.2.23); packet is discarded (received 4 identical messages from 10.116.96.151:45688 in the last 99327 ms)
2026-11-19 14:20:30,669 WARN  [org.jgroups.protocols.UDP] (mcast-receiver-4,ejb,hc_cbrdeapllx409:sipen_node1_DES_llx409) JGRP000010: packet from 10.116.96.151:45688 has different version (3.2.18) than ours (4.2.23); packet is discarded (received 4 identical messages from 10.116.96.151:45688 in the last 60337 ms)
2026-11-19 14:22:27,801 WARN  [org.jgroups.protocols.UDP] (mcast-receiver-4,ejb,hc_cbrdeapllx409:sipen_node1_DES_llx409) JGRP000010: packet from 10.116.96.151:45688 has different version (3.2.18) than ours (4.2.23); packet is discarded (received 4 identical messages from 10.116.96.151:45688 in the last 117132 ms)
2026-11-19 14:23:41,072 WARN  [org.jgroups.protocols.UDP] (mcast-receiver-4,ejb,hc_cbrdeapllx409:sipen_node1_DES_llx409) JGRP000010: packet from 10.116.96.151:45688 has different version (3.2.18) than ours (4.2.23); packet is discarded (received 5 identical messages from 10.116.96.151:45688 in the last 73271 ms)
2026-11-19 14:24:45,152 WARN  [org.jgroups.protocols.UDP] (mcast-receiver-4,ejb,hc_cbrdeapllx409:sipen_node1_DES_llx409) JGRP000010: packet from 10.116.96.151:45688 has different version (3.2.18) than ours (4.2.23); packet is discarded (received 3 identical messages from 10.116.96.151:45688 in the last 64080 ms)
2026-11-19 14:25:48,022 WARN  [org.jgroups.protocols.UDP] (mcast-receiver-4,ejb,hc_cbrdeapllx409:sipen_node1_DES_llx409) JGRP000010: packet from 10.116.96.151:45688 has different version (3.2.18) than ours (4.2.23); packet is discarded (received 10 identical messages from 10.116.96.151:45688 in the last 62870 ms)
2026-11-19 14:26:38,264 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-8) WFLYSRV0027: Iniciando a implanta▒▒o do "SIPEN" (runtime-name: "pen-ear-2.32.0.2.ear")
2026-11-19 14:26:38,273 INFO  [org.jboss.modcluster] (ServerService Thread Pool -- 610) MODCLUSTER000046: Starting to drain 1 active sessions from default-host:/sipen in 10 seconds.
2026-11-19 14:26:39,779 ERROR [org.wildfly.extension.undertow] (MSC service thread 1-1) WFLYUT0074: N▒o foi poss▒vel encontrar TLD /WEB-INF/tld/c.tld
2026-11-19 14:26:40,131 ERROR [org.jboss.msc.service.fail] (MSC service thread 1-4) MSC000001: Failed to start service jboss.deployment.subunit."pen-ear-2.32.0.2.ear"."pen-web-2.32.0.2.war".INSTALL: org.jboss.msc.service.StartException in service jboss.deployment.subunit."pen-ear-2.32.0.2.ear"."pen-web-2.32.0.2.war".INSTALL: WFLYSRV0153: Falha ao processar a fase INSTALL de subdeployment "pen-web-2.32.0.2.war" of deployment "pen-ear-2.32.0.2.ear"
Caused by: org.jboss.msc.service.DuplicateServiceException: WFLYUT0105: Host e caminho de contexto est▒o ocupados, service jboss.deployment.subunit."pen-ear-2.32.0.2.ear"."pen-web-2.32.0.2.war".undertow-deployment.UndertowDeploymentInfoService n▒o podem ser registrados. A mensagem foi: Service jboss.undertow.deployment.default-server.default-host./sipen.UndertowDeploymentInfoService is already registered
2026-11-19 14:26:48,273 WARN  [org.jboss.modcluster] (ServerService Thread Pool -- 610) MODCLUSTER000025: Failed to drain 1 remaining active sessions from default-host:/sipen within 10,0 seconds
2026-11-19 14:26:48,274 INFO  [org.jboss.modcluster] (ServerService Thread Pool -- 610) MODCLUSTER000021: All pending requests drained from default-host:/sipen in 10,0 seconds
2026-11-19 14:26:48,275 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 610) WFLYUT0022: Contexto web n▒o registrado:'/sipen' do servidor 'default-server'
2026-11-19 14:26:48,517 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-3) WFLYSRV0028: Implanta▒▒o interrompida SIPEN (runtime-name: sipen-2.29.0.1-2.29.0.1-b1893.ear) em 10261ms
2026-11-19 14:26:48,520 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 613) WFLYCTL0013: Falha na opera▒▒o ("full-replace-deployment") - endere▒o ([]) - falha na descri▒▒o: {
    "WFLYCTL0080: Falha de servi▒os" => {"jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".\"pen-web-2.32.0.2.war\".INSTALL" => "WFLYSRV0153: Falha ao processar a fase INSTALL de subdeployment \"pen-web-2.32.0.2.war\" of deployment \"pen-ear-2.32.0.2.ear\"
    Caused by: org.jboss.msc.service.DuplicateServiceException: WFLYUT0105: Host e caminho de contexto est▒o ocupados, service jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".\"pen-web-2.32.0.2.war\".undertow-deployment.UndertowDeploymentInfoService n▒o podem ser registrados. A mensagem foi: Service jboss.undertow.deployment.default-server.default-host./sipen.UndertowDeploymentInfoService is already registered"},
    "WFLYCTL0412: Servi▒os necess▒rios que n▒o est▒o instalados:" => ["jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".\"pen-web-2.32.0.2.war\".deploymentCompleteService"],
    "WFLYCTL0180: Os servi▒os com falta/indisponibilidade de depend▒ncias " => ["jboss.deployment.unit.\"pen-ear-2.32.0.2.ear\".deploymentCompleteService faltam [jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".\"pen-web-2.32.0.2.war\".deploymentCompleteService]"]
2026-11-19 14:26:48,521 ERROR [org.jboss.as.controller.management-operation] (ServerService Thread Pool -- 613) WFLYCTL0013: Falha na opera▒▒o ("full-replace-deployment") - endere▒o ([]) - falha na descri▒▒o: {
    "WFLYCTL0080: Falha de servi▒os" => {"jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".\"pen-web-2.32.0.2.war\".INSTALL" => "WFLYSRV0153: Falha ao processar a fase INSTALL de subdeployment \"pen-web-2.32.0.2.war\" of deployment \"pen-ear-2.32.0.2.ear\"
    Caused by: org.jboss.msc.service.DuplicateServiceException: WFLYUT0105: Host e caminho de contexto est▒o ocupados, service jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".\"pen-web-2.32.0.2.war\".undertow-deployment.UndertowDeploymentInfoService n▒o podem ser registrados. A mensagem foi: Service jboss.undertow.deployment.default-server.default-host./sipen.UndertowDeploymentInfoService is already registered"},
    "WFLYCTL0412: Servi▒os necess▒rios que n▒o est▒o instalados:" => ["jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".\"pen-web-2.32.0.2.war\".deploymentCompleteService"],
    "WFLYCTL0180: Os servi▒os com falta/indisponibilidade de depend▒ncias " => ["jboss.deployment.unit.\"pen-ear-2.32.0.2.ear\".deploymentCompleteService faltam [jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".\"pen-web-2.32.0.2.war\".deploymentCompleteService]"]
2026-11-19 14:26:48,522 ERROR [org.jboss.as.server] (ServerService Thread Pool -- 613) WFLYSRV0014: A reimplanta▒▒o da implanta▒▒o "sipen-2.29.0.1-2.29.0.1-b1893.ear" pela implanta▒▒o "pen-ear-2.32.0.2.ear" foi revertida com a seguinte mensagem de falha:
    "WFLYCTL0080: Falha de servi▒os" => {"jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".\"pen-web-2.32.0.2.war\".INSTALL" => "WFLYSRV0153: Falha ao processar a fase INSTALL de subdeployment \"pen-web-2.32.0.2.war\" of deployment \"pen-ear-2.32.0.2.ear\"
    Caused by: org.jboss.msc.service.DuplicateServiceException: WFLYUT0105: Host e caminho de contexto est▒o ocupados, service jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".\"pen-web-2.32.0.2.war\".undertow-deployment.UndertowDeploymentInfoService n▒o podem ser registrados. A mensagem foi: Service jboss.undertow.deployment.default-server.default-host./sipen.UndertowDeploymentInfoService is already registered"},
    "WFLYCTL0412: Servi▒os necess▒rios que n▒o est▒o instalados:" => ["jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".\"pen-web-2.32.0.2.war\".deploymentCompleteService"],
    "WFLYCTL0180: Os servi▒os com falta/indisponibilidade de depend▒ncias " => ["jboss.deployment.unit.\"pen-ear-2.32.0.2.ear\".deploymentCompleteService faltam [jboss.deployment.subunit.\"pen-ear-2.32.0.2.ear\".\"pen-web-2.32.0.2.war\".deploymentCompleteService]"]
2026-11-19 14:26:48,522 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-8) WFLYSRV0027: Iniciando a implanta▒▒o do "SIPEN" (runtime-name: "sipen-2.29.0.1-2.29.0.1-b1893.ear")
2026-11-19 14:26:48,807 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-7) WFLYSRV0028: Implanta▒▒o interrompida SIPEN (runtime-name: pen-ear-2.32.0.2.ear) em 285ms
2026-11-19 14:26:50,044 ERROR [org.wildfly.extension.undertow] (MSC service thread 1-1) WFLYUT0074: N▒o foi poss▒vel encontrar TLD /WEB-INF/tld/c.tld
2026-11-19 14:26:50,345 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 627) WFLYUT0021: Contexto web registrado: '/sipen' para servidor 'default-server'
2026-11-19 14:26:50,352 INFO  [org.jboss.as.repository] (ServerService Thread Pool -- 613) WFLYDR0002: Conte▒do removido do local /opt/jboss/jboss-eap/hc/servers/sipen_node1_DES_llx409/data/content/b1/48402de8a13ef43cfdb74636a14369595fd384/content
2026-11-19 14:27:13,319 WARN  [org.jgroups.protocols.UDP] (mcast-receiver-4,ejb,hc_cbrdeapllx409:sipen_node1_DES_llx409) JGRP000010: packet from 10.116.96.151:45688 has different version (3.2.18) than ours (4.2.23); packet is discarded (received 3 identical messages from 10.116.96.151:45688 in the last 85297 ms)


