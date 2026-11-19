Prezados, boa tarde!
Identificamos a falha abaixo nos logs do ambiente do JBoss 7.4. Poderiam, por gentileza, comparar as configurações do WMQ entre os ambientes para verificar se existe alguma divergência?
 
15:08:52,682 INFO  [ClienteRest] (default task-8) ClienteRest.consultarCorrelationClientePorCPF

15:08:52,769 INFO  [org.jboss.as.connector.deployers.RaXmlDeployer] (default task-8) wmq.jmsra.rar: MQJCA4016:Identificador de conexões não registrado sendo fechado: 'com.ibm.mq.connector.outbound.ConnectionWrapper@5589a774'.
 
Claudia Florisbela Freitas
Prezados, boa tarde! Identificamos a falha abaixo nos logs do ambiente do JBoss 7.4. Poderiam, por gentileza, comparar as configurações do WMQ entre os ambientes para verificar se existe alguma diver…
Jesse Mouta Pereira Batista, Thiago Jeferson de Sousa Silva, conseguem nos apoiar?



 Não, isso não é um erro. Trata-se apenas de um registro informativo (INFO) gerado pelo servidor de aplicação (JBoss/WildFly) em conjunto com o adaptador de recursos do IBM MQ (wmq.jmsra.rar).
 
Esse comportamento ocorre durante o gerenciamento normal do ciclo de vida das conexões JMS. Abaixo estão os detalhes do que cada parte significa:
 
Nível de severidade (INFO). O log indica apenas uma operação de rotina da aplicação, sem qualquer impacto funcional ou falha na execução do método consultarCorrelationClientePorCPF.
O código MQJCA4016. Essa mensagem significa que o adaptador de recursos do IBM MQ fechou um manipulador de conexão (connection handle) que não estava mais associado a uma conexão gerenciada ativa no pool.
Causa comum no código. Geralmente acontece quando a aplicação chama connection.close() mais de uma vez no mesmo objeto, ou quando o contêiner JBoss já encerrou e recolheu a conexão ao final de uma transação JTA antes de o bloco finally (ou try-with-resources) da aplicação tentar fechá-la novamente.
