Pessoal, conforme combinado com Alessandro, Paulo e Gustavo, o ajuste do ccr-api foi aplicado no SIFEC-CCR do 7.4 (DES).

O que foi feito:

Backup do domain.xml e da configuração atual do Keycloak, para rollback se necessário.
Removido o secure-deployment do ccr-api.war. O container deixa de validar o token, igual ao 6.4, e a validação volta a ser feita pela aplicação, aceitando os realms intranet e internet.
Redeploy do SIFEC-CCR concluído às 15:22, sem erros. O ccr-web (tela do CCR) continua protegido normalmente pelo Keycloak.

Próximo passo: @Matheus Rocha Nascimento, pode testar o /v8/contratos/simular com token intranet e com token internet? Se aparecer qualquer erro, me passa o horário que eu verifico no log.




[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]#
[root@cbrdeapllx473 p585600]# tail -f $LOG | grep -aiE "ccr-api|IJ0|ORA-|ERROR"
15:33:08,173 WARN  [org.keycloak.adapters.RefreshableKeycloakSecurityContext] (default task-115) Refresh token failure status: 400 {"error":"invalid_grant","error_description":"Refresh token expired"}
15:33:08,414 WARN  [org.keycloak.adapters.RefreshableKeycloakSecurityContext] (default task-115) Refresh token failure status: 400 {"error":"invalid_grant","error_description":"Refresh token expired"}
15:33:29,790 WARN  [org.keycloak.adapters.RefreshableKeycloakSecurityContext] (default task-115) Refresh token failure status: 400 {"error":"invalid_grant","error_description":"Refresh token expired"}
15:33:29,800 WARN  [org.keycloak.adapters.RefreshableKeycloakSecurityContext] (default task-115) Refresh token failure status: 400 {"error":"invalid_grant","error_description":"Refresh token expired"}
15:33:29,812 WARN  [org.keycloak.adapters.RefreshableKeycloakSecurityContext] (default task-115) Refresh token failure status: 400 {"error":"invalid_grant","error_description":"Refresh token expired"}
15:33:29,822 WARN  [org.keycloak.adapters.RefreshableKeycloakSecurityContext] (default task-115) Refresh token failure status: 400 {"error":"invalid_grant","error_description":"Refresh token expired"}

