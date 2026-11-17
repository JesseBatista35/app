Para garantir, confira só o override:

bash
grep -a "Keycloak subsystem override" $LOG | tail -3

O horário da última linha tem que ser anterior a 15:21. Se não sair nada, melhor ainda.

Mensagem para a sala:

Ajuste aplicado no SIFEC-CCR (DES 7.4): removida a validação do token pelo container para o ccr-api, igual ao 6.4. O redeploy foi concluído às 15:22. Matheus, pode testar o /v8/contratos/simular com token intranet e com token internet? Se der qualquer erro, me manda o horário que eu olho o log.

Enquanto o Matheus testa, deixe o log aberto no 473:

bash
tail -f $LOG | grep -aiE "ccr-api|keycloak|401|403|ERROR"
