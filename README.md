/opt/server/bin/jboss-cli.sh -c --command='/system-property=SIHDG-SEC_URL_SERV_AUTH:add(value="https://login.tqs.caixa/auth")'
/opt/server/bin/jboss-cli.sh -c --command=':reload'
# aguardar subir e conferir:
curl -sk https://sihdg-jboss8-tqs.apps.nprd.caixa/sihdg-api/api/seguranca/configuracao-seguranca
