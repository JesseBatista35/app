Dá pra confirmar rápido em cada VM (955 e 2557):

bash
grep -c "SIGSJ04" /opt/jboss-eap/standalone/configuration/standalone-full-ha.xml
0 → limpo, nada a fazer.
1+ → tem datasource sobrando; passa pros devs removerem do SIGSJ-INTRANET-config / SIGSJ-BOLETO-config.

Resposta pro Vitor/Gagliardi:

Isso mesmo, Vitor — confirmado que só o SIGSJ-INTERNET usa o Oracle, então a REQ000147111475 é a única de senha necessária. Boleto e intranet não precisam de ajuste de banco. Só vou verificar se sobrou algum datasource SIGSJ04 no config desses dois (herança do template) pra pedir aos devs removerem e não ficar erro no log. Valeu!

Fora isso, o status do dia segue o mesmo: aguardando a Rede aplicar as 3 regras de firewall do SIROT pra revalidar os logins.
