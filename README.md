Quando o Gustavo liberar, começamos pelo APX

No CLI do 471:

/server-group=sifec-intranet/deployment=SIAPX_JavaWeb:add(enabled=true)

Ao mesmo tempo, no 473:

bash
tail -f /opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log | grep -aE "WFLYSRV|WELD-|ERROR|apx"

Se o deploy falhar, o JBoss desfaz sozinho e o servidor continua de pé. Aí trazemos o erro e vemos se é de ambiente ou de código.
