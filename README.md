Operacional sobre isso para a gente não tomar essa decisão por aqui, como se fosse uma coisa só de infra, tudo bem que tem o arquiteto do CCR da fábrica, deu a posição dele, né? Mas era bom um caixa do CCR falar, né? Que às vezes.
Paulo Henrique Barros Santos
15:01
No.
Jesse Mouta Pereira Batista
15:01
Mm.
Paulo Henrique Barros Santos
15:01
Operacional.
Gustavo Duarte Lepesteur da Costa
15:01
Vai se melhor algum cenário aí que não possa e tal.
Paulo Henrique Barros Santos
15:01
É, eu acho que o Rogel, o Rangel teria condições de opinar sobre isso aí, né? Mas deixa, deixa eu entender um
Gustavo Duarte Lepesteur da Costa
15:01
É, o problema é que por ele estar desse jeito, eu não consigo chamar ele, marcar ele no chat e não fazer nada.
Paulo Henrique Barros Santos
15:01
Sim.
Deixa eu entender uma coisa aqui, cara, assim.
É porque eu não entendi bem o problema. Eu tenho dois token.
Eu estou que o que 2?
Gustavo Duarte Lepesteur da Costa
15:02
Não, você tem um pacote do CCR que está precisando para subir. Ele está precisando usar os 2 tokens. Era isso ou JC?
Paulo Henrique Barros Santos
15:02
Um pacote.
Jesse Mouta Pereira Batista
15:02
Isso ele tá é porque na verdade é o que acontece o clickluck ele ele não não atua no CCR API web então na subida lá ele é por causa lá do do web XML né aí ele não declara o login config né
E isso lá no 64, no cifec 5, já no 74, o adapter do clecluck, ele faz essa aplicação de proteção automaticamente por causa do realming lá que tá configurado, né? Então, como o token lá do cleweb PNC é do realmente internet, aí ele.
Ele traz isso, ele dá conexão recusada, né? Então a opção a decisão aqui, Paulo, foi a gente igualar o 64. A gente removia o security deployment do CCR, e aí a aplicação, ela vai voltar a tratar o token conforme tá lá no 64.
Mas aí tem uma questão, o container deixa de validar, né?
Tem essa questão aí a outra opção seria manter a validação e trocar o Realme para internet, mas aí a gente tinha outro problema por quem tem a recusa dos consumidores de quem usa esse token lá do Realme do internet.
Paulo Henrique Barros Santos
15:03
Tá, mas.
Right.
Deixa eu ver se eu se eu captei aqui.
É, a gente tem a questão, a gente tem um CCR API.
Esse CCR API, introdução, ele tá numa instância separada, acredito eu.
Jesse Mouta Pereira Batista
15:03
Isso.
Gustavo Duarte Lepesteur da Costa
15:03
É, em produção, a gente tem um ambiente separado do Santos Santos Santos SRP.
Paulo Henrique Barros Santos
15:03
Hey Gustavo.
Então, esse ambiente.
