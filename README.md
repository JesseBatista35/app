Próximo: GARANTIAS 1.8.0.3-b183

No 473, mantenha o tail -f, trocando construcard por garantias no grep. No CLI do 471:

/server-group=sifec-intranet/deployment=SIFEC-GARANTIAS4:add(enabled=true)

para pegar o log do garantias

Log do GARANTIAS. No 473 (10.116.97.79):

Ao vivo, deixe rodando antes de fazer o deploy:

bash
LOG=/opt/jboss/jboss-eap/hc/servers/sifec-intranet_node1_lx473/log/server.log
tail -f $LOG | grep -aE "garantias|WFLYSRV00(10|21)|WFLYCTL0013|WFLYCTL0412|WELD-001408|at injection point|ERROR|Contexto web registrado"

Ou, se o deploy já foi feito:

bash
grep -aE "garantias|WFLYSRV00(10|21)|WFLYCTL0013|WFLYCTL0412|WELD-001408|at injection point|ERROR|Contexto web registrado" $LOG | tail -40

Para saber o resultado:

WFLYSRV0010 ... "SIFEC-GARANTIAS4" foi implantado quer dizer que subiu. Nesse caso, pegue também o contexto web.
WFLYSRV0021 ... revertido quer dizer que falhou. Cole o bloco do erro aqui.
