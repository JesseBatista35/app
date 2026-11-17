
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# tail -f $LOG | grep -aE "minutasgarantias|WFLYSRV00(10|21)|WFLYCTL0013|WFLYCTL0412|WELD-0014|ERROR|Contexto web registrado"
16:40:05,449 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 135) WFLYUT0021: Contexto web registrado: '/ori-web' para servidor 'default-server'
16:40:05,477 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 119) WFLYSRV0010: "SIFEC-ORIGINACAO2" foi implantado (runtime-name: "sifec-originacao-3.11.1-b344.ear")
16:41:30,577 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 143) WFLYUT0021: Contexto web registrado: '/minutaGarantias-web' para servidor 'default-server'
16:41:30,609 INFO  [org.jboss.as.server] (ServerService Thread Pool -- 135) WFLYSRV0010: "SICCR-MINUTAS" foi implantado (runtime-name: "sifec-minutaGarantias-1.0.0-b36.ear")




