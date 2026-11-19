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
