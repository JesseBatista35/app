Bruno, bom dia! Investiguei o erro 500 do sipdm-api-estudante em DES.

A aplicação sobe normal, mas não consegue conectar no SQL Server do PDM (10.116.100.127:1433, banco PDMDB001). Toda chamada que consulta o banco cai em timeout de conexão, e o handler devolve 500.

O que verifiquei:
• Do pod para 10.116.100.127:1433 → timeout
• Do bastion para o mesmo destino → conecta OK (o banco está no ar)
• O namespace sipdm-des não tem regra bloqueando no OpenShift
• O namespace sai com egress IP dedicado 10.116.221.183, que não está liberado no firewall para o banco

Para eu conseguir abrir a regra de firewall (10.116.221.183 → 10.116.100.127:1433/TCP), preciso que você abra uma REQ para a nossa equipe pedindo a análise do erro 500 do sipdm-api-estudante em DES. Assim que a REQ chegar, eu registro a regra vinculada a ela e acompanho a validação.

Depois de liberado, não precisa de redeploy: a aplicação volta a conectar sozinha.
