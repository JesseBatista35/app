Então o mv funcionou. Confirma o destino:

bash
ls -la /log_jboss/config-log4j/

Se o sigsj_ws_boleto.xml estiver com data de hoje (~16:38) → sucesso, foi entregue pela esteira.

Depois limpa o órfão (é só esse arquivo velho, não afeta nada):

bash
rm -f /opt/jboss-eap/standalone/configuration/properties/sigsj_boleto.xml

E valida o boleto:

bash
curl -s -o /dev/null -w "boleto: %{http_code}\n" http://10.116.201.25/boletoService/contaJudicial

Me manda o ls do /log_jboss/config-log4j/. Se o sigsj_ws_boleto.xml estiver com data de hoje, o boleto fechou 100% pela esteira — sem precisar destruir nada.
