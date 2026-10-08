Prezados,

Após análise, verificamos que os 3 alertas de Secret Scanning (5, 6 e 8) foram fechados como “revoked” em 17/07, porém os valores continuam presentes na branch develop. Por isso a validação de GHAS da esteira continua reprovando:

Alerta #8: arquivo PostmanCollection/SIOBS-AppPingFederate.postman_environment.json, variável access_token, com o token JWT ainda preenchido. O arquivo não é alterado desde o commit que o adicionou.
Alertas #5 e #6: arquivo SiobsAppPingFederate/Database/DbInitializer.cs, campos hashed_refresh_token do seed. As propriedades foram renomeadas, mas os valores detectados permanecem os mesmos.

Fechar o alerta ou revogar a credencial não remove o valor do código, e a esteira valida a presença do secret na branch. Para seguir com a publicação:

No environment do Postman, deixar o value do access_token vazio, ou remover o arquivo do repositório (e incluí-lo no .gitignore, se for de uso local);
No DbInitializer.cs, substituir os hashed_refresh_token por valores fictícios ou gerados em tempo de execução. Recomendamos também revisar os valores de unique_user_id, que aparentam ser CPFs, e usar dados fictícios;
Fazer merge na develop e executar uma nova pipeline (não usar “Re-run”, que reexecuta o commit antigo).

Caso a reprovação persista após a remoção, favor acionar a GESED05 (gesed05@caixa.gov.br), responsável pela regra de Secret Scanning da esteira.
