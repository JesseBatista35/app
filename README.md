Claudia, boa tarde! Verificamos o log do sifec-intranet no 7.4 e a consulta consultarCorrelationClientePorCPF está funcionando normalmente. Às 15:08:52, 15:08:55 e 15:08:56 houve três chamadas, e todas seguiram o fluxo (consulta ao SICLI e acesso ao banco) sem nenhum erro ou exceção.

A linha MQJCA4016 é de nível INFO, não de erro: o adaptador do IBM MQ apenas registra que fechou um identificador de conexão já liberado pelo container ao fim da transação. É comportamento de rotina e não afeta o resultado. A configuração do WMQ (connection factories e filas) está presente no 7.4 no mesmo padrão do 6.4.

Se vocês estiverem vendo algum erro na tela ou um retorno incorreto nessa consulta, nos passem o horário e o cenário de teste para investigarmos.
