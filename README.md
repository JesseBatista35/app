
sh-5.1$
sh-5.1$ /opt/server/bin/jboss-cli.sh -c --command='/system-property=SIHDG-SEC_URL_SERV_AUTH:add(value="https://login.tqs.caixa/auth")'
/opt/server/bin/jboss-cli.sh -c --command=':reload'
# aguardar subir e conferir:
curl -sk https://sihdg-jboss8-tqs.apps.nprd.caixa/sihdg-api/api/seguranca/configuracao-seguranca
{"outcome" => "success"}
{
    "outcome" => "success",
    "result" => undefined
}
{"realm":"intranet","idCliente":"cli-web-hdg","urlServidorAutorizacao":"https://login.des.caixa/auth","tempoVidaToken":300,"tempoMaximoIdle":-1,"versaoApi":"3.22.0.1"}sh-5.1$
sh-5.1$
sh-5.1$
















