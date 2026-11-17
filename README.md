Reunião em Migração JBoss 7.4 - SIFEC, SICCR, SIEMP, SIPEN-20261117_142159-Transcrição da Reunião
17 de novembro de 2026, 05:22PM
1h 11m 12s

Jesse Mouta Pereira Batista começou a transcrição

Sosthenes Estrela Soares   0:03
das bibliotecas que são legadas inversão de Java ele é a ideia que a gente não fizesse implementação de nada apenas a modernização do sistema é o que faz parte do projeto então se ele não tem

Jesse Mouta Pereira Batista   0:05
Cert.
Mhm.
Uh-huh.

Sosthenes Estrela Soares   0:18
Cobertura desde a sua conceção, ele está está vindo para cá sem essa cobertura também.

Jesse Mouta Pereira Batista   0:25
Entendi.

Sosthenes Estrela Soares   0:25
O time não vai implementar cobertura de teste para esse sistema, sabe?

Jesse Mouta Pereira Batista   0:31
Tá, mas aí eu já não sei, não sei se o Paulo Henrique pode informar, é porque hoje a esteira, ela tem a variável obrigatória de sonar. Aí eu não consigo assim, explicar pra vocês se é realmente obrigatório.

Denilson Socrates de Sousa   0:41
Mhm.

Jesse Mouta Pereira Batista   0:47
Ou não agora, assim, o dentro do.

Sosthenes Estrela Soares   0:49
Head.

Denilson Socrates de Sousa   0:50
De qualquer forma, a gente fez a cobertura com as é não, a gente acabou, a gente fez como a gente viu lá que estava apontando para as coisas que a gente mexeu nas linhas novas que ele aponta, a gente fez até a cobertura, só que aí que quando.

Sosthenes Estrela Soares   0:54
Ah, vocês fizeram?

Jesse Mouta Pereira Batista   0:56
No.
Isso.
O código novo né, Denise? Show!

Denilson Socrates de Sousa   1:05
É no código novo, exatamente, somente nele. Então o restante da aplicação, se for validar, realmente não vai ter. A gente nem responsabiliza por isso, que a gente não foi uma coisa que a gente fez, mas pelo novo a gente até fez, fez a cobertura e estava batendo lá 95%, fazendo local.

Sosthenes Estrela Soares   1:15
É, não pode.

Jesse Mouta Pereira Batista   1:17
Yeah.

Denilson Socrates de Sousa   1:23
Então, tranquilo. Então, se for validar somente nessa cobertura, show de bola. Se for validar aí na aplicação toda, aí é um problema.

Jesse Mouta Pereira Batista   1:23
Uh-huh.
É, não verdade, deixa, é, deixa, eu.

Denilson Socrates de Sousa   1:31
Ele não tem para onde correr, entendeu? Exato. É isso que tem que ser avaliado. Aí tem que ver aí essa questão do sonar para ele passar, aí ver se com cobertura pode ser com cobertura mesmo, sem problema, mas baseando somente no que é novo. Aí tudo bem, a gente entende.

Jesse Mouta Pereira Batista   1:43
Mm-hmm.

Denilson Socrates de Sousa   1:47
Mas no que é que é velho, aí não vai rolar, não tem como.

Jesse Mouta Pereira Batista   1:48
Sim, que é velho, não tem como. É, eu tenho até um cenário que é um de um outro ADDR que eu estou também, que é o do CIJEC. É o mesmo caso aí, mais ou menos do SIEMP, está vindo aqui para a esteira. E aí realmente a gente fez os ajustes lá.

Sosthenes Estrela Soares   1:51
Não vai ter como, mano.

Denilson Socrates de Sousa   1:58
Mm-hmm.

Jesse Mouta Pereira Batista   2:03
do da variável, ele tava tendo a cobertura, só que realmente tava quebrando aí, mas no código novo, realmente tem uns bugs lá de 8, 12 anos atrás, entendeu? Só que aí a gente conseguiu fazer as correções todas lá e a e a build dele passou.

Denilson Socrates de Sousa   2:12
Mm-hmm. Sim.
Mm-hmm.

Jesse Mouta Pereira Batista   2:18
Pode ser que seja o mesmo caso aqui, vamos dar uma avaliada, deixa eu só dar uma olhada aqui rapidinho.

Denilson Socrates de Sousa   2:24
Nesse caso é porque não tenho cobertura nenhuma. Primeiro tem que fazer até a cobertura. Na hora que fizer a cobertura, aí é assim a avaliação.

Jesse Mouta Pereira Batista   2:27
Isso é eu.
Isso, exato. Só que, por exemplo, no caso, nesse momento agora o sonar está fora, a gente não consegue nem ver. Mas eu estou vendo que o problema de vocês não é por causa que o sonar está fora, tá? É realmente a questão da cobertura, beleza?

Denilson Socrates de Sousa   2:35
A four, é?
Yeah, sim.
então se ajustando essa parte aí avisando avisando para a gente show de bola que é o tempo da gente poder analisar aqui e ver se vai dar certo ou não

Helber Fernandes Rodrigues   2:45
Eu consegui abrir.

Jesse Mouta Pereira Batista   2:48
Tá.

Helber Fernandes Rodrigues   2:50
No.

Jesse Mouta Pereira Batista   2:52
Tá, pode falar.

Helber Fernandes Rodrigues   2:53
Eu consegui abrir o sonora aqui.

Jesse Mouta Pereira Batista   2:55
Abriu? Deixa eu ver aqui.

Helber Fernandes Rodrigues   2:57
Okay.
Deixa eu posso apresentar?

Jesse Mouta Pereira Batista   2:59
Okay.
Pode mostrar, pode abrir.
Pode pegar até ali.

Helber Fernandes Rodrigues   3:07
Apareceu aí pra vocês?

Denilson Socrates de Sousa   3:09
Mm-hmm.

Jesse Mouta Pereira Batista   3:10
Apareceu.

Helber Fernandes Rodrigues   3:12
Você já está na Camp Java Web, na Brand Developer. Então é esse.

Jesse Mouta Pereira Batista   3:15
Aham, develope, desce ali para a gente ver as coberturas ali rapidinho.

Denilson Socrates de Sousa   3:17
Olha só, só já tá na tela, só tem uma condição que falhou, que não tá tendo cobertura nenhuma.

Jesse Mouta Pereira Batista   3:21
É zero, é, é. Clica ali onde está zero ali, por favor.

Helber Fernandes Rodrigues   3:27
Aqui.

Denilson Socrates de Sousa   3:28
Não é embaixo da esquerda, a esquerda no último, overage and new code.

Jesse Mouta Pereira Batista   3:29
E 00 ali lá condition condition.

Helber Fernandes Rodrigues   3:29
New bug.

Jesse Mouta Pereira Batista   3:33
Condition.
Isso em cima, em cima, sobe.

Helber Fernandes Rodrigues   3:35
Aqui.

Denilson Socrates de Sousa   3:36
No, now it's him. Scared, scared, scared.

Helber Fernandes Rodrigues   3:40
Sear them.

Denilson Socrates de Sousa   3:40
No.

Jesse Mouta Pereira Batista   3:41
Volta lá no overview, isso.

Denilson Socrates de Sousa   3:42
aí não não falta de novo agora vai anda com o mouse para a esquerda agora
Pode andar, sobe, sobe, sobe, pode subir agora. E é.

Jesse Mouta Pereira Batista   3:49
Isso, onde está 0.0 aí por cento aí, ó. Isso.

Helber Fernandes Rodrigues   3:53
Okay.

Jesse Mouta Pereira Batista   3:56
Hey, oh, tell you.

Denilson Socrates de Sousa   3:58
Exatamente. Mas esse aí

Jesse Mouta Pereira Batista   3:59
tá as atualizações que você precisa só código novo show

Denilson Socrates de Sousa   4:02
É esse código novo e foi feito. Tem teste para isso aí já, já. Mas é que eu apontei lá o Jacoco. Não está sendo gerado nenhum XML para o Jacoco analisar. Entendeu? Mas é porque também, pelo que eu tenho, pelo que eu vejo.

Jesse Mouta Pereira Batista   4:04
Já foi feito isso aí? Não, então beleza.

Denilson Socrates de Sousa   4:17
Os testes não estão sendo executados, que está dando aquele skip, então não vai executar, né? anão ser que vocês façam de outra forma. Então, ou faz esse, muda o jeito, muda a configuração aí para poder executar e executar os testes. E ele lê esses testes, né?

Jesse Mouta Pereira Batista   4:19
Sim.
É verdade. Deixa eu ver aqui.
Sim, deixa eu ver aqui rapidinho, ele tá como?
Menos o clamp e aqui é porque ele já tá correto aqui, vamos ver
Olha, ele está rodando com true, o disk past é de disk test, está rodando com true, é.

Denilson Socrates de Sousa   4:52
Mm-hmm.

Sosthenes Estrela Soares   4:56
They skip test.

Denilson Socrates de Sousa   4:59
É o skip, né?

Jesse Mouta Pereira Batista   5:00
Is.

Sosthenes Estrela Soares   5:01
Mm.

Denilson Socrates de Sousa   5:01
Exatamente, aí não pode.

Sosthenes Estrela Soares   5:04
E essa configuração está no projeto ou está lá no servidor?

Helber Fernandes Rodrigues   5:05
No.

Denilson Socrates de Sousa   5:07
Servidor.

Jesse Mouta Pereira Batista   5:08
Não, não, ela é no, ela é na esteira mesmo.

Sosthenes Estrela Soares   5:10
Na esteira, está na esteira.

Denilson Socrates de Sousa   5:10
Nice later.

Jesse Mouta Pereira Batista   5:11
É, a gente troca ela aqui, está? Eu vou, deixa eu, vamos dar uma mexida aqui. Eu vou tirar o skip aqui.

Denilson Socrates de Sousa   5:17
Ta.

Paulo Henrique Barros Santos   5:20
voltei aqui pessoal

Jesse Mouta Pereira Batista   5:22
Ah, eu tava beleza.

Sosthenes Estrela Soares   5:22
Opa, beleza.

Helber Fernandes Rodrigues   5:23
What's that?

Jesse Mouta Pereira Batista   5:26
Eu vou tirar, deixa eu só mostrar, só pegar a tela aqui, tá só assim, rapidinho.

Denilson Socrates de Sousa   5:29
Mm.

Sosthenes Estrela Soares   5:30
Because of and made.

Helber Fernandes Rodrigues   5:30
pode pode fica à vontade

Jesse Mouta Pereira Batista   5:31
Só para mim mostrar para vocês o que eu estou trocando aqui, qualquer coisa a gente volta. Oh, eu tirei o the skip, está?

Sosthenes Estrela Soares   5:38
Alexandre.

Jesse Mouta Pereira Batista   5:39
Beleza, eu tirei ele, vamos salvar aqui.
Na develop, né?

Helber Fernandes Rodrigues   5:52
Yeah, develop.

Jesse Mouta Pereira Batista   5:53
Beleza.

Sosthenes Estrela Soares   6:00
PJ 17 Jana.

Jesse Mouta Pereira Batista   6:02
Sim.

Sosthenes Estrela Soares   6:05
Você de Almeida a produção até dia 29.

Jesse Mouta Pereira Batista   6:12
A produção.

Sosthenes Estrela Soares   6:13
Yeah.

Jesse Mouta Pereira Batista   6:16
Would you, I know, and

Sosthenes Estrela Soares   6:16
Não é isso? Esse é o prazo, Paulo.

Jesse Mouta Pereira Batista   6:19
Okay.

Paulo Henrique Barros Santos   6:19
Isso a gente vai subir, vai subir ele com DNS diferente lá em produção, num primeiro momento.

Sosthenes Estrela Soares   6:28
Here they go.

Paulo Henrique Barros Santos   6:29
Beleza, vai estar que nem a gente colocou aqui, a gente colocou migração CIP.10 lá vai ser ponto PRD, o que a gente combinou com a produção.

Sosthenes Estrela Soares   6:37
Tá bom, aí já consegue dar como entregue, depois só muda o DNS, né?

Jesse Mouta Pereira Batista   6:38
And.

Paulo Henrique Barros Santos   6:40
Isso e é o tempo dos gestores testar, né? Ver se não teve nenhum tipo de.

Sosthenes Estrela Soares   6:42
Oh.
There go.

Paulo Henrique Barros Santos   6:47
Efeito colateral.

Jesse Mouta Pereira Batista   6:55
Tá ele, o Maven precisa o dele, senão ele quebra. Deixa eu ver aqui. OPA.
I'll show you a good kick.
É na developer mesmo né que eu rodei? Deixa eu ver aqui se eu fiz alguma coisa errada. Não tá certo, tá certo.

Denilson Socrates de Sousa   7:10
No, for sir, for sir.

Helber Fernandes Rodrigues   7:11
With develop.

Jesse Mouta Pereira Batista   7:13
Estou certo, deixa eu ver aqui rapidinho.
Hankey.
Good morning, morning, okay.
É, ele não consegue sem o da skip lá, ele não consegue exportar, tá vendo? Exportação, PDF, teste, tá, deixa eu ver uma outra.
Um outro exemplo aqui pra ver se a gente consegue
É interessante, acho que foi o Sosiness que conseguiu acessar. Acho que ele tá oscilando aí o sonar, mas isso não acho que não atrapalha a API chegar lá até no.
Funcionar e fazer isso e fazer o teste.

Denilson Socrates de Sousa   8:11
After work.

Sosthenes Estrela Soares   8:19
William back assist so.

Jesse Mouta Pereira Batista   8:21
For web ads.

Helber Fernandes Rodrigues   8:21
Tem algum teste que eu consigo rodar manual aqui ou

Jesse Mouta Pereira Batista   8:27
Pro.

Helber Fernandes Rodrigues   8:28
No, no, no Connor.

Sosthenes Estrela Soares   8:28
É, mas não vai adiantar, porque o mesmo que tem que chamar aqui.

Jesse Mouta Pereira Batista   8:30
É, é o Amazing.

Helber Fernandes Rodrigues   8:32
Pereira.

Jesse Mouta Pereira Batista   8:33
Yeah.

Sosthenes Estrela Soares   8:45
Oh, well, BE.

Jesse Mouta Pereira Batista   8:45
É o já coco.
Data phone.

Helber Fernandes Rodrigues   8:48
Wait, wait.

Sosthenes Estrela Soares   8:48
É, eu estou rapidinho, gente, é, você continua aqui só enquanto eu vou ali no IDP fechar com eles as demanda rapidão.

Helber Fernandes Rodrigues   8:54
Data Data Data Data.

Sosthenes Estrela Soares   8:55
OK, go to Michael.

Helber Fernandes Rodrigues   8:58
Ser

Sosthenes Estrela Soares   8:58
Valeu, já volto gente, rapidão.
Mas pode tocar aí que o Helber vai comandando aí o resto aí o que precisar.

Jesse Mouta Pereira Batista   9:08
Beleza.
Deixa eu ver aqui, eu Apaguei, será? Não, tá aqui
Eu não estou falando de Faria de Oliveira.
Deixa eu dar uma olhada no ponto aqui rapidinho, gente.

Paulo Henrique Barros Santos   9:36
Beleza.

Denilson Socrates de Sousa   10:03
Com certeza, se eu não me engano, não está. O Jacoco não foi cadastrado aí não. Não.

Jesse Mouta Pereira Batista   10:09
gente, a gente tem que cadastrar o Jacoco Mage plugin, entendeu?

Denilson Socrates de Sousa   10:11
Yeah.
Entendi, eu posso fazer isso aqui e mandar ele subir já. Inclusive, eu tenho até uma band que eu vou fazer o pull request aqui, se for o caso, pra fazer o teste, vou fazer o teste, porque também tem essa configuração e você também pode configurar aí no coisa também, como aí vai ter.

Jesse Mouta Pereira Batista   10:17
Pode.
Ah não, beleza, então pode rodar, pode, pode fazer.
É.

Denilson Socrates de Sousa   10:29
Vai de acordo com a necessidade, no caso.

Jesse Mouta Pereira Batista   10:31
Com a necessidade, eu vou trocar lá o

Denilson Socrates de Sousa   10:34
Eu vou fazer aqui, então agora o pull request e já te aviso aí.

Jesse Mouta Pereira Batista   10:38
Beleza, fechou.

Denilson Socrates de Sousa   10:39
Betty.

Jesse Mouta Pereira Batista   10:45
Deixa eu trocar aqui por uma versão mais enxuta
Só pra gente ver se é a questão do Jacoco mesmo.

Denilson Socrates de Sousa   10:54
Come here, safety, my.

Jesse Mouta Pereira Batista   10:57
É, é não, mas pode ir subindo enquanto você eu vou só trocar aqui pra pra ele rodar.

Denilson Socrates de Sousa   11:00
Mhm.

Jesse Mouta Pereira Batista   11:04
Pereira de ti.
trocar a versão dele aqui
Op.
só para ele ignorar enquanto a gente

Denilson Socrates de Sousa   11:19
Eu acabei de subir já o request, já está na develop, tá? É porque eu já adiantei alguma coisa, porque como existe 2 tipos de configurações, né? Você pode usar ir direto no já coloco aí direto, mandando a URL, ou você pode botar no pool também, né? Aí a gente já deixou aqui uma pronta aqui, caso precisasse.

Jesse Mouta Pereira Batista   11:20
Enquanto você subiu.
Ah, já foi?
Uh-huh.
Mm-hmm.
I know, beleza, facial.
Deixa eu tirar esse cara aqui então.
Tá na develop já né?

Denilson Socrates de Sousa   11:52
Tá.

Jesse Mouta Pereira Batista   11:54
Beleza vou rodar aqui vamos rodar aqui para ver
Wow.

Denilson Socrates de Sousa   12:37
Deus eu erro mais.

Jesse Mouta Pereira Batista   12:39
No.
Sure King.
Modelos já é, mas ele já apareceu o outro.
Vamos ver aqui rapidinho.
O Jacoco veio, Jacoco veio plugin, está aqui, beleza. Agora ele já está reclamando de outro problema aqui, deixa eu.
subir aqui para ver se a gente consegue identificar
log for J log for J log
Ó, já coloco já tá ativo, beleza.
Parece que está faltando no binário aqui o Java C.
Erro.
Deixa eu ver aqui.
só botar um best aqui rapidinho

Denilson Socrates de Sousa   14:05
Yeah.

Jesse Mouta Pereira Batista   14:07
Como que ele tá se comportando aqui?
Michael.
Sir.
Java.
deixa eu cobrir ele aqui Open JDK
Daqui, é esse cara aqui que ele tá perto com o Bafa do Log
Deixa eu pedir aqui pra ele.
Cuspe uma mensagem aqui pra gente?
Vamos rodar ele aqui de novo.

Denilson Socrates de Sousa   15:44
Yes.

Jesse Mouta Pereira Batista   16:30
Eu tô falando que acho que tem um tempão que eu tô falando no mundo aqui ou não foi agora.

Denilson Socrates de Sousa   16:33
Mm.
Four.

Jesse Mouta Pereira Batista   16:37
Cristina Soares. Ah.

Helber Fernandes Rodrigues   16:37
Santos.

Jesse Mouta Pereira Batista   16:43
tava avisando o pessoal aqui que eu tava em outra sala
Deixa eu rodar aqui de novo. Achei estranho porque ele não cuspiu nada lá, falou que o diretório não foi encontrado.
Vamos ver aqui.
Operacional.
É que quebrou aqui, hein?
and deixa passar
Deus and tax cara.

Denilson Socrates de Sousa   17:24
Okay.

Jesse Mouta Pereira Batista   17:25
ele tá com ele sim tá é o bestzinho que eu tô fazendo aqui só para ver se o se o já você tá funcionando só para a gente ver de onde que ele tá vindo que agora o agora o erro não é mais o jacoco já é outra coisa

Denilson Socrates de Sousa   17:27
Ah, tá, beleza, show, entendi.

Jesse Mouta Pereira Batista   18:06
Eu acho.
The Hudson and King.
Acho que esse editor aqui do Azure, ele não aceita.
Deixa eu trocar só o caminhão aqui.
vamos ver se assim aceita
Beleza, o que ele passou? Ele achou esse cara aqui.
Pedro no Mario de novo, vamos ver aqui
Oh.
Modelos Jasper Test
Martin
Consignação consta parâmetros do convênio.
Isso aqui no no caso Denilson já é tipo o teste já trazendo trazendo para a gente os os problemas né os erros

Denilson Socrates de Sousa   20:01
Mm-hmm.
O.
Mhm.

Jesse Mouta Pereira Batista   20:14
26.
Isso.
modelo já pestation
É, mas eu acho que aqui ele não aplicou o Java C ainda.
Agora.
Essa outra versão.
No, I'm a barrel and throw.

Denilson Socrates de Sousa   23:17
S.

Jesse Mouta Pereira Batista   23:42
Ele está faltando aqui.

Helber Fernandes Rodrigues   23:47
Pontes, né?

Jesse Mouta Pereira Batista   23:48
É fonte, tá vendo? É 6 erros aqui de exportação, PDF, teste. Ele tá falando da fonte da Arial da Arial Arial Black é fonte mesmo. Se a gente criar um arquivo lá do Jasper Resport properties.

Helber Fernandes Rodrigues   23:52
O.

Jesse Mouta Pereira Batista   24:03
Pra ele aceitar a fonte, será se?
Kill.
Não sei se já viu isso Denise aqui rapidinho, OPA.
So, we'll talk you.
Deixa eu testar aqui pra gente ver se vai dar certo.
Esquentar seu teste aqui ainda, mas vamos ver aqui
Vou criar aqui só pra gente fazer um teste, tá? Qualquer coisa depois você tira lá, tá, Denise?

Denilson Socrates de Sousa   25:06
Mm-hmm.

Jesse Mouta Pereira Batista   25:07
And.
Só com essa linha aqui, ó.
que é o mesmo que ele tá
Heckleman La.
Deixa um.
Beleza.
deixa eu trocar esse cara aqui também deixa
Off.
Aí deu certo. Vamos ver agora se ele vai passar a cobertura. É, realmente era só as fontes mesmo lá, tá?

Denilson Socrates de Sousa   27:10
Mm-hmm.

Jesse Mouta Pereira Batista   27:11
Aí eu fiz uma develop e depois você quiser dar uma olhada lá avaliado.

Denilson Socrates de Sousa   27:12
E?

Jesse Mouta Pereira Batista   27:18
Eu só adicionar essa linha aqui.

Denilson Socrates de Sousa   27:19
Tem como botar ele no marven também, tá?

Jesse Mouta Pereira Batista   27:21
Tem do lado direto, né?
Você fala?

Denilson Socrates de Sousa   27:24
Eu tenho na no chat aí, é?

Jesse Mouta Pereira Batista   27:26
Deixa eu ver aqui.

Denilson Socrates de Sousa   27:27
Não, mas pode deixar aí se você quiser, já tá funcionando, tá cheio por enquanto. Só pra você ter o conhecimento mesmo, é?

Jesse Mouta Pereira Batista   27:31
Tá, é não, depois troca tranquilo, beleza.
Okay.
Sonar está abrindo para vocês ir.

Denilson Socrates de Sousa   31:35
It.

Helber Fernandes Rodrigues   31:37
Akita.

Denilson Socrates de Sousa   31:39
Yeah.

Helber Fernandes Rodrigues   31:39
Pode apresentar?

Jesse Mouta Pereira Batista   31:40
Pode, vamos dar uma olhada aí.

Denilson Socrates de Sousa   31:40
William William Will

Helber Fernandes Rodrigues   31:47
Develop.

Jesse Mouta Pereira Batista   31:47
Okay.

Helber Fernandes Rodrigues   31:52
Well, eu vou aqui no.

Jesse Mouta Pereira Batista   31:52
Oh.

Helber Fernandes Rodrigues   31:54
Next boogie film.

Jesse Mouta Pereira Batista   31:56
Ó, ele já apresentou cobertura, agora tava zero, já tá 95%. Cli isso, clica nesses 13 aí.

Helber Fernandes Rodrigues   32:01
Okay.

Jesse Mouta Pereira Batista   32:06
Esses foram três que ele pulou agora
Vai ali em suíço ali rapidinho para a gente ver.
Buggy.
Oh, 15 dias, um dia, 22 horas.

Helber Fernandes Rodrigues   32:33
Call Congresso.

Jesse Mouta Pereira Batista   32:35
Sim, Elita.
Okay.
Lock Critical.
É, tem que fazer esses ajustes aí, Oh, está vendo? É um dia 22 horas.
Click on a save presume plan.
Aí ó, estou pedindo para remover o comentário, nada a ver.

Denilson Socrates de Sousa   33:03
Ship.

Jesse Mouta Pereira Batista   33:04
remove lá o comentário Uai que estranho isso aí

Helber Fernandes Rodrigues   33:09
Deixa eu ver aqui no overview.

Jesse Mouta Pereira Batista   33:11
é tem uma condição né que falhou né clica lá naquela ali em cima aí ó uma condição falhou

Helber Fernandes Rodrigues   33:13
Direct me.

Denilson Socrates de Sousa   33:18
Que é exatamente essa de baixa do skipping.

Jesse Mouta Pereira Batista   33:20
É essa daí é os é os 13 né? Isso aí ó.

Denilson Socrates de Sousa   33:23
E os três que eu falho, a gente vai ter que clicar nela.
Mhm.

Jesse Mouta Pereira Batista   33:30
Clica lá, Consulta Contrato Java Test No de cima aí Aí, isso, isso, aí, clica aí, é

Denilson Socrates de Sousa   33:31
Yeah.
Right, we kind of a

Helber Fernandes Rodrigues   33:35
Hello.

Denilson Socrates de Sousa   33:36
I.

Helber Fernandes Rodrigues   33:36
Aqui.

Denilson Socrates de Sousa   33:38
Uh-huh.

Jesse Mouta Pereira Batista   33:41
aí ele vai apontar aí os

Denilson Socrates de Sousa   33:43
Over me.

Jesse Mouta Pereira Batista   33:44
Vermelho, cadê?

Denilson Socrates de Sousa   33:46
Não tem nenhum. E aí, o que é que faz?

Jesse Mouta Pereira Batista   33:47
Não tem nenhum, muito bom, muito bom.

Denilson Socrates de Sousa   33:54
Much more.
Eu achei, é os 3, é como é um arquivo só com 13 itens que foi que deu skipping.
Para que tem que saber o que vai fazer, né?

Helber Fernandes Rodrigues   34:06
Have means Sarakh no HC, HC, but.

Denilson Socrates de Sousa   34:09
Não é o que ele só sempre sobre a condição que ele aponta lá, a condição. É o que se for, entendeu? Se for para o outro lado lá, vai ter 17000 o registro para gente trabalhar aí às vezes.

Jesse Mouta Pereira Batista   34:11
É sobre a condição que ele aponta ali.

Helber Fernandes Rodrigues   34:13
Tá, entendi.
Entendi, entendi.

Jesse Mouta Pereira Batista   34:22
Mas pelo menos a cobertura tá chegando agora, então.

Denilson Socrates de Sousa   34:24
Uhum, tá, agora tem que saber o que tem que fazer naquele arquivo lá.

Jesse Mouta Pereira Batista   34:29
Siemp Java aqui para mim abriu deixa eu ver se eu consigo

Denilson Socrates de Sousa   34:32
Like I'm a

Jesse Mouta Pereira Batista   34:36
develop

Denilson Socrates de Sousa   34:36
Eu vou tentar abrir aqui também.

Jesse Mouta Pereira Batista   34:39
É.

Denilson Socrates de Sousa   34:39
Okay.
Vê se tem o manda pesquisar, pesquisar, ignore aí, só por curiosidade.

Helber Fernandes Rodrigues   35:07
Online.

Denilson Socrates de Sousa   35:08
Aí, manda pesquisar, ignore.

Jesse Mouta Pereira Batista   35:10
Ignore it.

Denilson Socrates de Sousa   35:11
Yeah.

Jesse Mouta Pereira Batista   35:11
Você acha que foi por causa que eu coloquei lá o ignore?

Denilson Socrates de Sousa   35:15
Não, mas eu quero ver se tem, pode ser também, mas eu estou querendo esse arquivo se tem.

Jesse Mouta Pereira Batista   35:16
Nice.
Massing.

Denilson Socrates de Sousa   35:24
Cont

Helber Fernandes Rodrigues   35:28
O termo ignore.

Denilson Socrates de Sousa   35:29
No, I don't think.

Jesse Mouta Pereira Batista   35:31
Não tem.

Denilson Socrates de Sousa   35:33
And don't ask good.

Helber Fernandes Rodrigues   35:33
Aqui não tem não.

Jesse Mouta Pereira Batista   35:34
Estranho que ele não aponta. Quem é o quem é o defeituoso? Quem é o cara que está?

Denilson Socrates de Sousa   35:42
Eu vou olhar aqui também, deixa eu pesquisar aqui que eu fico pensando e vou pesquisar.
A tela aberta aqui também.

Jesse Mouta Pereira Batista   35:53
Será se não é por causa desse da quantidade de critical em sues aqui?
Deixa eu ver, porque assim a cobertura tá 95% num, porque ela precisa de estar acima de 80 pra poder passar.

Denilson Socrates de Sousa   36:06
É, por isso que eu te falei que a gente conseguiu ainda botar ela altona.

Jesse Mouta Pereira Batista   36:10
É, já chegou já no topo.

Denilson Socrates de Sousa   36:12
É, e agora? Esse ignora aí que me quebrou agora, deixa eu pensar aqui.

Jesse Mouta Pereira Batista   36:15
Who is that?
Porque tem.
Tem muita coisa aqui.
15 dias atrás, né?

Denilson Socrates de Sousa   36:34
Eu acho que eu já sei quem que é.

Jesse Mouta Pereira Batista   36:41
Swiss.

Denilson Socrates de Sousa   36:43
Nossa, nossa, assume false.
Acho que esse cara eu vou ter que fazer. Eu vou pedir aqui para fazer uma alteração e subir de novo se ele for só esse caso.

Jesse Mouta Pereira Batista   36:52
Beleza.

Denilson Socrates de Sousa   36:55
Aí a gente descobre.

Jesse Mouta Pereira Batista   36:58
Beleza, beleza, beleza.

Denilson Socrates de Sousa   37:00
beleza Valeu aí eu vejo aí eu falo para eu aviso para vocês eu vou falar aqui beleza mas eu acho eu acho que é isso

Jesse Mouta Pereira Batista   37:04
Está tranquilo, só avisa a gente aqui na sala.

Helber Fernandes Rodrigues   37:06
O pilar precisa fazer alguma alteração ou ele pode subir lá o pull request e tem que fazer alguma alteração depois.

Denilson Socrates de Sousa   37:16
Eu acho que como ele já fez as alterações, é só subir o pull request, fazer o pull request e fazer o deploy de novo.

Jesse Mouta Pereira Batista   37:16
Eu só criei.
You said.
É só subir para o request, é porque eu fiz lá na developer, beleza?

Denilson Socrates de Sousa   37:24
Fernando deve, aí eu faço, eu vou fazer aqui a alteração, vê se é isso mesmo que eu estou pensando aqui mesmo, que não ficou muito claro. E aí eu subo. Se der certo, eu aviso para vocês, beleza?

Helber Fernandes Rodrigues   37:26
William.

Jesse Mouta Pereira Batista   37:36
Fechou então, valeu Denise Valeu

Denilson Socrates de Sousa   37:37
Alô, abraço.

Helber Fernandes Rodrigues   37:39
Beleza, valeu pessoal, muito obrigado aí pelo apoio.

Gustavo Duarte Lepesteur da Costa   37:41
Oh.

Jesse Mouta Pereira Batista   37:41
Valeu, Weber. Obrigado.

Gustavo Duarte Lepesteur da Costa   37:42
Boa tarde. Yes, sir.

Helber Fernandes Rodrigues   37:43
Um abraço, bom trabalho.

Jesse Mouta Pereira Batista   37:44
Está oi, oh Gustavo.

Gustavo Duarte Lepesteur da Costa   37:45
A gente consegue continuar aqui para a gente falar do faq.

Jesse Mouta Pereira Batista   37:49
Bora, vamos sim.

Gustavo Duarte Lepesteur da Costa   37:51
A laser.

Jesse Mouta Pereira Batista   37:53
Deixe your soccer a mall.

Gustavo Duarte Lepesteur da Costa   37:53
Pega a Tania ainda aí.

Paulo Henrique Barros Santos   37:56
Tossing.

Gustavo Duarte Lepesteur da Costa   37:57
Tá, deixa eu te falar, cara. Teve uma discussão técnica sobre o token lá do SSO, do CCR. E aí, cara, o Jesse expôs o cenário um pouco mais assim, mais acima aí no chat, umas 1038.

Jesse Mouta Pereira Batista   37:59
Sim.

Gustavo Duarte Lepesteur da Costa   38:13
e o Alessandro que está como arquiteto, só que ele da fábrica, foi direcionando. Tentei falar com o Toninho e o Rangel e não consegui de manhã, agora que eu consegui falar com o Rangel, só que eu toquei o Ele está como Pra você também, ele está bugado como usuário desconhecido?

Paulo Henrique Barros Santos   38:17
Mm-hmm.
O Tune parece estar fora, né? Eu vi que ele tá com
Tá, ele tá como se estivesse ausente, né?

Gustavo Duarte Lepesteur da Costa   38:34
De férias, né?

Paulo Henrique Barros Santos   38:36
Yeah, ou licença, enfim.

Gustavo Duarte Lepesteur da Costa   38:37
É, então, mas aí ele está verdinho, velho. Então eu achei que era só para mim que estava dando esse pau, que o minei disse que viu ele aí, pode ter sido só para mim. Então beleza, enfim, aí o que o Alessandro como eu não consegui falar com eles, cara, eu pedi para o Alessandro fazer um backup do domain e a gente fazer o que ele estava pedindo.

Paulo Henrique Barros Santos   38:44
No.
Mhm.

Gustavo Duarte Lepesteur da Costa   38:55
É porque qualquer coisa a gente volta, mas eu acho que o ideal era a gente ter uma apreciação da galera lá do CCR, mesmo se isso viola algum tipo de regra, de enfim, ou de segurança ou alguma normativa da vida nosso aí que não possa.
Usar é o mesmo pacote usando os 2 tokens, não é isso? Hoje essa?

Jesse Mouta Pereira Batista   39:14
Isso, isso, exato. O mesmo pacote está usando os dois toques.

Gustavo Duarte Lepesteur da Costa   39:17
So.
E aí eu e eu acho que era interessante eles opinarem o.
Operacional sobre isso para a gente não tomar essa decisão por aqui, como se fosse uma coisa só de infra, tudo bem que tem o arquiteto do CCR da fábrica, deu a posição dele, né? Mas era bom um caixa do CCR falar, né? Que às vezes.

Paulo Henrique Barros Santos   39:28
No.

Jesse Mouta Pereira Batista   39:29
Mm.

Paulo Henrique Barros Santos   39:38
Operacional.

Gustavo Duarte Lepesteur da Costa   39:39
Vai se melhor algum cenário aí que não possa e tal.

Paulo Henrique Barros Santos   39:43
É, eu acho que o Rogel, o Rangel teria condições de opinar sobre isso aí, né? Mas deixa, deixa eu entender um

Gustavo Duarte Lepesteur da Costa   39:47
É, o problema é que por ele estar desse jeito, eu não consigo chamar ele, marcar ele no chat e não fazer nada.

Paulo Henrique Barros Santos   39:52
Sim.
Deixa eu entender uma coisa aqui, cara, assim.
É porque eu não entendi bem o problema. Eu tenho dois token.
Eu estou que o que 2?

Gustavo Duarte Lepesteur da Costa   40:06
Não, você tem um pacote do CCR que está precisando para subir. Ele está precisando usar os 2 tokens. Era isso ou JC?

Paulo Henrique Barros Santos   40:08
Um pacote.

Jesse Mouta Pereira Batista   40:13
Isso ele tá é porque na verdade é o que acontece o clickluck ele ele não não atua no CCR API web então na subida lá ele é por causa lá do do web XML né aí ele não declara o login config né
E isso lá no 64, no cifec 5, já no 74, o adapter do clecluck, ele faz essa aplicação de proteção automaticamente por causa do realming lá que tá configurado, né? Então, como o token lá do cleweb PNC é do realmente internet, aí ele.
Ele traz isso, ele dá conexão recusada, né? Então a opção a decisão aqui, Paulo, foi a gente igualar o 64. A gente removia o security deployment do CCR, e aí a aplicação, ela vai voltar a tratar o token conforme tá lá no 64.
Mas aí tem uma questão, o container deixa de validar, né?
Tem essa questão aí a outra opção seria manter a validação e trocar o Realme para internet, mas aí a gente tinha outro problema por quem tem a recusa dos consumidores de quem usa esse token lá do Realme do internet.

Paulo Henrique Barros Santos   41:11
Tá, mas.
Right.
Deixa eu ver se eu se eu captei aqui.
É, a gente tem a questão, a gente tem um CCR API.
Esse CCR API, introdução, ele tá numa instância separada, acredito eu.

Jesse Mouta Pereira Batista   41:35
Isso.

Gustavo Duarte Lepesteur da Costa   41:43
É, em produção, a gente tem um ambiente separado do Santos Santos Santos SRP.

Paulo Henrique Barros Santos   41:44
Hey Gustavo.
Então, esse ambiente.
Então, esse ambiente aqui bem provável, essa configuração do JBoss e eu acredito que seja JBoss diferente do que a gente tem da intranet.
Ele deve estar com esse apontamento de configuração aí para aceitar esse toque de internet, imagino eu.

Gustavo Duarte Lepesteur da Costa   42:06
Você acha que é porque, porque aqui é um ambiente só, é um ambiente só, tipo.

Paulo Henrique Barros Santos   42:06
Como aqui é um ambiente diferente, isso como a gente está num ambiente só.

Jesse Mouta Pereira Batista   42:07
É.

Paulo Henrique Barros Santos   42:12
Talvez a gente tivesse que ter um outro ambiente só de internet para testar os pacotes de internet nesse sentido.
Entendeu ou não?

Gustavo Duarte Lepesteur da Costa   42:25
Mm-hmm.

Jesse Mouta Pereira Batista   42:25
Entendi, é?

Paulo Henrique Barros Santos   42:25
Porque eu acho que a gente vai ter dificuldade com outros pacotes do do CIPEC também que tratam internet, porque deveriam estar usando tokens de internet.

Jesse Mouta Pereira Batista   42:37
F.
É uma, é uma boa questão, não é?

Paulo Henrique Barros Santos   42:42
Eu acho que a gente poderia então.
Solicitar um novo?

Jesse Mouta Pereira Batista   42:48
Okay.
Pode ser, é porque assim a aplicação ela recebe o token, hoje ela trata sozinha o web XML, então lá o login config ele não declara lá no 74, esse subsistema do clay clock.

Paulo Henrique Barros Santos   42:57
Mm-hmm.

Jesse Mouta Pereira Batista   43:05
Ele tem um, ele tem esse essa, o security deployment para o CCR e ele é. Ele aponta para esse home. Então, com isso, o adapter passa a proteger a aplicação automaticamente. Eu Acredito que um outro é, pode ser um outro pacote.

Paulo Henrique Barros Santos   43:20
Entendi. Então assim, então a gente poderia pensar aqui e manter, tirando essa verificação para ele poder aceitar qualquer um dos token e quando for para a produção já ter essa segregação aí.

Jesse Mouta Pereira Batista   43:21
I.
Isso.
Pode ser.

Paulo Henrique Barros Santos   43:36
Gustom.

Jesse Mouta Pereira Batista   43:39
No more.

Gustavo Duarte Lepesteur da Costa   43:39
Cara, confesso que nesse assunto de token, eu não sei ajudar muito não, cara. Tem que tomar.

Paulo Henrique Barros Santos   43:44
Não, não, mas tu entendeu o ponto que eu coloquei aqui, que a gente tem uma proteção do ambiente.

Jesse Mouta Pereira Batista   43:47
Go.

Gustavo Duarte Lepesteur da Costa   43:48
Sim, um ambiente diferente, sim.

Paulo Henrique Barros Santos   43:51
E aí é aquela questão, hoje a gente monta um ambiente diferente de internet só pra gente ter.
mais perto do que se espera quando for para a produção ou para a gente ganhar tempo aqui a gente tira esse cheque do ambiente.

Gustavo Duarte Lepesteur da Costa   44:04
A miss.
É porque, assim, sempre vai ser diferente o ambiente de Deus e produção. A gente não vai ter um ambiente só de Serviços e do FCVS igual a gente tem. A gente tem que fazer funcionar aqui e isso aí vai ser uma das coisas que vai divergir em produção.

Paulo Henrique Barros Santos   44:20
Is, is, is, is.

Gustavo Duarte Lepesteur da Costa   44:27
Eu acho que vale a pena deixar ele como exato, como se fosse assim, cara, se fosse uma produção, como é que ele funcionaria? É que a gente tira o que não precisa, entendeu?

Paulo Henrique Barros Santos   44:30
Funcionar com os dois.
É porque, por exemplo, pelo que eu entendi, a gente tem uma configuração aqui que a gente pode tirar e ele vai setar os 2. Não sei se é o deployment que vocês falaram aí.

Gustavo Duarte Lepesteur da Costa   44:39
And CI.

Jesse Mouta Pereira Batista   44:39
Mm.

Paulo Henrique Barros Santos   44:50
74.

Gustavo Duarte Lepesteur da Costa   44:50
No.

Jesse Mouta Pereira Batista   44:52
Então a gente tira a verificação do container pro CCR, removendo o security deployment. Aí eu acredito que ele vai aceitar os 2 tokens, igual hoje está no 64.

Paulo Henrique Barros Santos   44:58
Yes.

Jesse Mouta Pereira Batista   45:07
164.

Paulo Henrique Barros Santos   45:09
Que é o ideal, porque realmente em ambientes de desenvolvimento a gente não tem essa segregação.

Jesse Mouta Pereira Batista   45:14
Sim, aí ela fica como requisito para ambientes seguintes, né?

Paulo Henrique Barros Santos   45:15
E aí, em produção?

Gustavo Duarte Lepesteur da Costa   45:15
Raiza.

Paulo Henrique Barros Santos   45:17
Isso.

Gustavo Duarte Lepesteur da Costa   45:18
É, improdução não pode ser desse jeito, né? Vai ter que ser certinho.

Jesse Mouta Pereira Batista   45:21
Mhm.

Paulo Henrique Barros Santos   45:21
Não, não pode. Aí não pode. Ele nem vai funcionar, né? No final das contas, que tu vai configurar um, vai deixar de funcionar outro.

Gustavo Duarte Lepesteur da Costa   45:25
Right.
Nice.
Beleza.

Jesse Mouta Pereira Batista   45:32
É aí só fica combinado aqui pra vocês combinarem isso, por exemplo, em TQS quando for subir, porque com a verificação, quando a gente remover a verificação aqui em 10, os testes, eles não vão é, eles não vão pegar.

Paulo Henrique Barros Santos   45:32
Beleza.

Jesse Mouta Pereira Batista   45:47
problema de Helm né então por exemplo se algum pacote chamar o token errado isso vai só vai aparecer quando o ambiente segregado existir entendeu a gente tem essa assim tem essa questão é mas hoje hoje

Paulo Henrique Barros Santos   45:48
Mm-hmm.

Gustavo Duarte Lepesteur da Costa   45:59
Mas hoje não é assim, em tese.

Jesse Mouta Pereira Batista   46:02
Isso, hoje, isso, hoje tá assim, né? Exatamente, entendeu?
Mm.

Paulo Henrique Barros Santos   46:09
Vamos seguir nesse caminho.

Jesse Mouta Pereira Batista   46:10
Beleza, combinado.

Paulo Henrique Barros Santos   46:11
Que aí eu não vou nem aguardar o pessoal do CCR ver isso não.

Jesse Mouta Pereira Batista   46:14
Tá, é porque também eu posso fazer um backup aqui, PH, igual eu combinei com o Gustavo aqui, e aí se o pessoal, não, não era pra a gente vem aqui, faz o rollback, tá resolvido.

Paulo Henrique Barros Santos   46:19
Mm-hmm.
Não, cara, é porque assim é porque realmente algumas com algumas definições, algumas coisas aí a gente vamos ter que deixar para um segundo momento, por questão de tempo mesmo. A gente tem que avançar nos pacotes, enfim.

Jesse Mouta Pereira Batista   46:31
Isso, pro segundo momento, é. Não, beleza, como
é como a gente tá em 10 aí para teste e tudo fazemos aqui né E aí se futuramente alguém falar não e tal tem uma outra solução tem algo para fazer a gente aplica aqui então fechado então eu vou eu não tinha executado ainda tá Gustavo vou executar aqui eu mando lá na sala lá para vocês tá

Paulo Henrique Barros Santos   46:41
Is.

Gustavo Duarte Lepesteur da Costa   46:53
Mm-hmm.
Tá aí quando você terminar isso, então me chama aqui na sala de novo pra gente tocar os pacotes, os pacotes que ainda estão lá no.

Jesse Mouta Pereira Batista   46:57
Beleza.
Chamo pra gente, chamo sim.
Ainda os pendentes, né? Tá fechado Beleza, de lá, valeu, valeu Gustavo, valeu Pegar, até mais, valeu, até mais, tchau tchau.

Gustavo Duarte Lepesteur da Costa   47:03
Precisando a gente tentar, é exato.
Shut.

Paulo Henrique Barros Santos   47:08
Valeu, senhores. Até mais. Tchau, tchau.

Gustavo Duarte Lepesteur da Costa   47:09
Beleza, valeu, valeu.

Jesse Mouta Pereira Batista parou a transcrição






PRIOCMIO PASSO AGORA E VER O QUE O GUSTOVA QUER, CONTINUAR SUBINDO OS DO INTRANET, QUAIS SÃO OS PROXIMOS
