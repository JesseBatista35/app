Conforme alinhado com o Rainier em sala, estamos abrindo essa solicitação novamente para tratamento de performance. Por gentileza, direcionador ao mesmo a pedido.

Estamos identificando problemas recorrentes de processamento e performance no ambiente TQS durante a execução da funcionalidade de atualização de contratos no SIGAF. O comportamento ocorre quando o sistema executa consultas sequenciais em grande volume junto ao serviço externo APF/APFAP327, realizando uma chamada por contrato para obtenção e atualização das informações. Conforme análise realizada com a equipe técnica, a funcionalidade já se encontra otimizada do ponto de vista de aplicação e persistência em banco (DB2), porém os erros persistem durante as chamadas externas e processamento concorrente.

Cenário 1 - Timeout Completo

Durante a execução da atualização em massa, a aplicação permanece processando por longo período e posteriormente retorna falha geral da aplicação com:

HTTP Failure Response
502 Proxy Error
Interrupção total do processamento
Não apresentação da lista de contratos processados ou com erro

Mensagem apresentada:

Ocorreu uma falha geral na aplicação.

Http failure response for:

/sigaf/services/inadimplencia/contrato/atualizar

502 Proxy Error

Cenário 2 - Processamento parcial com falha de integração

Em algumas execuções a requisição permanece ativa dentro do tempo limite configurado, porém durante as consultas ao APF são retornadas indisponibilidades temporárias, resultando na não atualização de diversos contratos.

Mensagens apresentadas:

Não foi possível atualizar o contrato XXXXX.

Motivo: Não foi possível consultar os dados da APFAP327 devido a uma indisponibilidade temporária.

Por favor, tente novamente mais tarde.

Ao final do processamento é retornado:

Http failure response for:

/sigaf/services/inadimplencia/contrato/atualizar

500 Internal Server Error



não encontrar coisas relacionadas entendeu mas a construção é essa o usuário vai chegar na tela vai apertar atualizar a gente vai fazer essa chamada item a item porque a gente só tem AP então é um item por vez a gente tem que atualizar

Rainier Barbosa dos Santos Viana  0:07
Right.

Cauan Henrique Cunha Mendonca  0:19
um algo mesmo e quando a carga é muito grande a gente tem esse probleminha de Tread há um tempo atrás a gente fez um pedido para aumentar um pouco de recurso de TQS uns dois anos por aí porque em desenvolvimento tinha muito mais recurso do que TQS
E a gente conseguia executar normalmente uma entrega de uma demanda muito antiga nossa, em desenvolvimento para TQS o gestor não conseguia. Foi feito um aumento de recurso para TQS, só que agora a gente tem o mesmo problema.

Karina Aparecida dos Santos  0:42
Yes.

Cauan Henrique Cunha Mendonca  0:54
Ele precisa de um recurso a mais para esse nível grande de processamento. O gestor já está ciente da situação de que via código que a gente não pode fazer muita coisa, que depende dessa informação externa, tá? Mas.
O recurso é insuficiente. Em questão de Souza, ela está otimizada para poder salvar aqui na base, porque a gente usa o DB2, mas na hora que vai fazer acesso a conexão externa do APF, nessa funcionalidade devido à carga, ocorre essas quedas, entendeu?

Rainier Barbosa dos Santos Viana  1:27
Então, basicamente, é falta de recurso que está acontecendo aí com a aplicação de vocês, né?

Cauan Henrique Cunha Mendonca  1:28
Okay.
Exatamente, volume muito grande e recurso pequeno pra essa situação.

Rainier Barbosa dos Santos Viana  1:35
Yeah.
Mhm.

Rita de Cassia Capello  1:37
Olha is aí, Karina.

Karina Aparecida dos Santos  1:40
Aí aqui é essa tela aqui, aí são todos esses essas operações que a gente precisa ir lá consultar uma a uma no APF.
Um.

Cauan Henrique Cunha Mendonca  1:54
Consegue, mas é muito raro. Vamos ficar na sorte de parar, mas sim, é recurso constante, tá o Rainier?

Rainier Barbosa dos Santos Viana  2:03
Okay.

Cauan Henrique Cunha Mendonca  2:08
eu deixo a tela travada aí esperando o final do pensamento que eu já estou querendo aqui eu quero que continue mesmo que fale atualiza o que der e o que não der você passa para a gente uma listagem só que como você vê aí dá um timeout até gigante nesse caso não trouxe o
O resultado, que é o que aparece ali em cima. Isso é do sistema mesmo, tá? Essa mensagenzinha. Mas quando a gente consegue fazer todas as chamadas e mudar um recurso pela parte do Java também, eu trago a lista de todos os contatos, todos os contatos, desculpa.
Que falharam na atualização é uma lista inteira de todos que falharam somente o número, né? Mas quando, mas e a gente tem esse problema de recurso também do Java, pela questão que você viu agora, deu um erro geral, fiz uma chamada, ficou em que e da.

Rainier Barbosa dos Santos Viana  2:51
Mhm.

Cauan Henrique Cunha Mendonca  3:00
Da thread e ela deu timeout. Quando ela não dá timeout a gente tenta, passa pelo tempo de timeout, vamos dizer assim, fica OK. Só que vai fazendo aquelas inúmeras chamadas do APF, top procedure, APF top procedure também dá limite de thread.
Pelo J-Boss, entendeu? Então cai aí.

Rita de Cassia Capello  3:19
O que a gente fez nessa funcionalidade, Rainier, para poder mostrar para o gestor? A gente capou uma quantidade boa de linhas que teria nessa tabela para a gente pelo menos conseguir executar para o gestor ver, entendeu?
Porque se a gente deixa todas as operações que de fato deveriam ter nessa lista, aí ele não vai mesmo.

Rainier Barbosa dos Santos Viana  3:46
Thank you.

Cauan Henrique Cunha Mendonca  3:46
Pereira, uma hora a gente chega naquele caso aí e mostra pra ele, ele está, se possível.

Karina Aparecida dos Santos  3:51
É, não, ele não está trazendo aquela, os erros que retorna do.

Cauan Henrique Cunha Mendonca  3:57
Isso, lembra que a gente fez um, ficou fazendo isso e Do Nada funcionou, passou pelo primeiro timeout? Vai que a gente consiga mostrar para ele, mas seria isso. Se tiver alguma dúvida de como é que está o código, o que é feito, fica à vontade aí para a gente encontrar a melhor solução.

Karina Aparecida dos Santos  4:02
a-ha, a-ha.

Rainier Barbosa dos Santos Viana  4:08
Mhm.
Okay.
Uhum, não é. Eu IA recomendar assim que geralmente isso daí o pessoal pede pela direct e tal, é.
Sim, se vocês puderem, abram uma com essa tela. Depois de dar esse evento de erro como evidência, o detalhe é tudo bonitinho que eu peço para direcionar para mim e a gente consegue tratar aqui.
Agora, vou ser sincero, agora, por enquanto, não consigo ter mais ou menos uma ideia do que pode ser, mas pela Hacker a gente consegue, aí vocês colocam todos os dados de acesso e tal, ou entende no servidor.

Cauan Henrique Cunha Mendonca  4:53
Sim, lá no XML do domain, da configuração do JBoss, teria que aumentar o rap size e o mat size, obviamente, para poder ter uma quantidade maior de memória. Eu não sei qual é a quantidade de memória liberada pelo JBoss lá em TQS.

Rainier Barbosa dos Santos Viana  4:58
Mhm.

Cauan Henrique Cunha Mendonca  5:08
e colocar algum JV em Optimus também para poder fazer uma otimização, coisas de Threads e também aumentar a pool para pelo menos 512 ou 1 GB se a gente conseguir.

Rainier Barbosa dos Santos Viana  5:22
Mhm. Thank you.
É, vocês podem abrir a hack que eu direciono quando quando ela chegar aqui na nossa fila que eu que eu trato dela.

Everton Freitas Oliveira  5:37
Maravilha então, mais a.

Rainier Barbosa dos Santos Viana  5:37
Agora, desculpa, Everton.

Everton Freitas Oliveira  5:40
Não, não pode falar ainda.

Rainier Barbosa dos Santos Viana  5:42
É que agora, sinceramente, eu não tenho muita ideia também do que pode estar acontecendo. Também sou um pouco novo.
Mas de repente, quando o pessoal aqui da equipe não é com mais um, mais um analista aqui me ajudando, a gente consegue ver.

Everton Freitas Oliveira  5:59
Maravilha! Aqui do nosso lado então a gente vai abrir novamente essa hack aí. Vou pegar o Cauan e a Karina aí a gente vai abrir, te mandar as informações aí e vai trabalhando em cima dessa solicitação, tudo bem?

Rainier Barbosa dos Santos Viana  6:11
Não, sem problema.

Everton Freitas Oliveira  6:14
Maravilha, dito isso, Karina e Pamela, acabou mais algum ponto aqui pra gente tratar com o Rainier?

Cauan Henrique Cunha Mendonca  6:23
Pamela.

Everton Freitas Oliveira  6:25
Maravilha, eu acho.

Karina Aparecida dos Santos  6:26
No, Everton.

Everton Freitas Oliveira  6:28
Acho que é isso, então vamos abrir essa tarefa aí. Tarefa não essa hack e a gente vai tratando aí então em paralelo com as atividades. Cara, muito obrigado aí pela sua disponibilidade, viu Rainier? Qualquer coisa vamos conversando aí. Obrigadão mesmo, viu?

Rainier Barbosa dos Santos Viana  6:34
So hacking Martins.
Okay is.
There's nothing that must be some.

Everton Freitas Oliveira  6:45
uma ótima tarde pessoal valeu obrigado aí time até breve tchau tchau

Karina Aparecida dos Santos  6:47
Obrigada, pessoal! Tchau, tchau!

Rainier Barbosa dos Santos Viana  6:48
Boa tarde, pessoal.

Pamela Silva Filomeno  6:49
Tchau.


