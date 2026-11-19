Vamos confirmar o 500 do intranet. Na 955:

bash
tail -40 /log_jboss/sigsj_intranet/sigsj_intranet.log

E, se precisar, o trecho do erro:

bash
grep -n "ERROR\|SIROT\|SIPER\|getResponse\|Connection\|SenhasSIIBC" /log_jboss/sigsj_intranet/sigsj_intranet.log | tail -20

Se vier SIROTTrans.getResponse nulo / connection timed out → é o firewall pendente, e resolve quando a 99052 subir (mesma coisa do internet). Se for outra exceção, a gente vê.

Mensagem pra sala:
