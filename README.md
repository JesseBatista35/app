Reunião em Migração JBoss 7.4 - SIFEC, SICCR, SIEMP, SIPEN-20261109_153329-Transcrição da Reunião
9 de novembro de 2026, 06:33PM
31m 48s

Jesse Mouta Pereira Batista começou a transcrição

Jesse Mouta Pereira Batista   0:33
Ele é do MPE do empresas, né Paulo?

Paulo Henrique Barros Santos   0:38
O.
Porque tudo pacote MPE, né?

Jefferson Vieira Alves   0:39
Good, both that.

Jesse Mouta Pereira Batista   0:41
Beleza.

Paulo Henrique Barros Santos   0:43
Well
Gerson entrou aí?

Jefferson Vieira Alves   0:46
Oi, boa tarde, estou aqui, beleza.

Paulo Henrique Barros Santos   0:47
Beleza? Boa tarde.
Meu caro é referente ao CIP, aquele trabalho do ADDR.

Jefferson Vieira Alves   0:58
Mhm.

Paulo Henrique Barros Santos   0:58
Beleza, o pessoal aqui fez lá, né?

Jesse Mouta Pereira Batista   1:05
Isso.

Paulo Henrique Barros Santos   1:06
Rodrigo e Thiago, eles estão trabalhando aqui nos deploys e aí para esses 3 módulos aqui, Sifec rural, Sifec e Silva empresas.
A gente está com um probleminha aqui na build
tu consegue dar uma olhada para gente aí para dar uma mexida

Jefferson Vieira Alves   1:27
Mhm.

Paulo Henrique Barros Santos   1:27
Como é que está a tua, o teu trabalho aí, tua atuação?

Jefferson Vieira Alves   1:30
É, eu estou numa demanda aqui prioritária, mas consigo, eu consigo uns minutos para a gente verificar.

Jesse Mouta Pereira Batista   1:37
Mm.

Jefferson Vieira Alves   1:37
Esse ciente empresas a gente não utiliza aqui.

Paulo Henrique Barros Santos   1:42
Não mexe, né?

Jefferson Vieira Alves   1:43
No.
Não, eu desconheço ele.

Paulo Henrique Barros Santos   1:45
I.
Sim, até uma informação importante, porque assim eu imagino que esse tipo de pacote é um pacote bem antigo.

Jesse Mouta Pereira Batista   1:55
Antigo, não é?

Paulo Henrique Barros Santos   1:57
Tanto é aqui, olha só, não sei se vocês estão vendo a planilha que eu estou aqui.

Jesse Mouta Pereira Batista   2:00
Sim.

Jefferson Vieira Alves   2:01
Yeah.

Paulo Henrique Barros Santos   2:01
Essa planilha aqui eu peguei com o pessoal da Produção do Sifec, aqui são os pacotes de Produção, vou até passar para vocês também aqui, para a gente fazer um controlezinho do que a gente já fez, do que enfim. Mas aí olhando aqui a questão do.

Jesse Mouta Pereira Batista   2:05
Mm-hmm.
That.
Beleza.
Time.

Paulo Henrique Barros Santos   2:18
Empresa.
Aqui no profile do da intranet.
E só.

Jesse Mouta Pereira Batista   2:29
Ele tem um AMP aí, é o AMP 345 aí.

Paulo Henrique Barros Santos   2:29
Tu tem?
É esse aqui é um pacote de internet.

Jefferson Vieira Alves   2:35
É.

Jesse Mouta Pereira Batista   2:39
Miney.

Paulo Henrique Barros Santos   2:39
Isso aqui tem um profile de internet. Esse aqui é só internet. Esse aqui eu acho que é uma tentativa de fazer uma migração por internet usando SSO.

Jesse Mouta Pereira Batista   2:43
Mhm.
SSO Singh.

Paulo Henrique Barros Santos   2:51
Que Eu Acredito que, como eu comparando os pacotes, não tem todos. E esse aqui, se eu não me engano, é ainda no formato de acesso antigo. Esse aqui deve ser o que o pessoal está usando ainda usa. Quer dizer, ainda não usa hoje na prática.
Eu acho que isso aqui é um projeto de migração que ainda não deve ter finalizado.
Agora, o que a gente talvez seja o nosso foco maior, de fato, é o spec intranet.
Principalmente.
E nele aqui a gente tem esse empresas que está aqui com a TASS.
Enfim, esse aqui já deve estar muito tempo que está de Rezende lá.
Ninguém mais está mexendo nele.
Não tem nem esse projeto né Jefferson aí?

Jefferson Vieira Alves   3:39
Não tenho ele aqui, não, só o MPE e o comercial dessa parte aí.

Paulo Henrique Barros Santos   3:39
5 empresas.
So.
É que seria esse, esse aqui seria o, acredito eu, o comercial e esse aqui o rural.

Jesse Mouta Pereira Batista   3:47
Okay.

Jefferson Vieira Alves   3:52
Isso, isso, exatamente.

Paulo Henrique Barros Santos   3:54
Tá esse aqui eu vou te pedir para tu dar uma olhada, porque pelo que eu vi aqui o problema.
É o mesmo desse aqui de baixo e aí depois eu vejo como é que eu vou tratar com quem que eu vou tratar esse aqui.

Jesse Mouta Pereira Batista   4:06
É do eu posso passar aqui, Paulo, rapidinho, é no caso do do empresas aí, mas como vocês comentaram aí, vamos usar só o amp. Então é, ele tá dando esse erro aí. Ele reverte a implementação do pacote com esse.

Paulo Henrique Barros Santos   4:10
Mhm.

Jesse Mouta Pereira Batista   4:23
Com esse erro, o Eld aí 0011 1480 e aí Eu Acredito que esse Weld do EAP 74, ele é mais rígido do que o 6.4, né? Então, pro pro gesto aí, as causas mais comuns desse.

Paulo Henrique Barros Santos   4:36
Mm.

Jesse Mouta Pereira Batista   4:39
Desse tipo de erro aí pode ser porque o BIN lá ele não declara os implementos lá da interface onde ele está sendo injetado, então o EJB lá ele vai dar 11 problema lá da interface ou na assinatura quando ele tenta injetar o módulo lá Por Ela.
Então, onde o módulo está lá no BIM, ele está lá tipo em bins.xml, né? Ou então alguma coisa lá, Discovery Mode. Então ele dá problema, né? E aqui do lado do nosso ambiente, eu e o Jefferson aqui a gente já testou, né? Inclusive a configuração do Weld também não resolveu, né? Então a gente apontou aí que acredito que esse ajuste aí
Seja no código, então quando tiver alguma atualização em alguma coisa, pode mandar pra gente pra gente poder testar. A gente pode fazer esse teste aqui em conjunto, pode entrar em sala, você me chama aqui, ó Jesse, fiz uma atualização aqui no pacote aqui, vamos subir pra gente testar. E aí a gente vai pegando o log ali e vai te mostrando ali pra gente poder ir resolvendo. Eu digo assim porque foi assim.
A gente fez com Pablo, Rodrigo e Paulo, pra gente poder resolver aquele problema lá do cadastro, da consulta do cadastro. Já no rural, ele tá com pacote atual aí do 6.4, onde ele traz o Jackson, os jazz, os jazz, os json provider. Ele tá vindo tudo junto com.

Paulo Henrique Barros Santos   5:39
Mhm.

Jesse Mouta Pereira Batista   5:54
Com o que era? Aí por isso que ele dá esse 001318, que é uma dependência, vamos dizer que ambígua do 7.4. Então é ajustar aí, deixar o Jackson, igual a gente fez, se você quiser conversar com o Pablo lá, ele fez esse ajuste lá, foi um dos primeiros.
erros que deu lá no PJ, tá? Foi essa questão lá do Jackson aí ele fez o ajuste rapidamente lá a gente subiu ele a gente conseguiu implementar o pacote.

Paulo Henrique Barros Santos   6:26
É em Jeferson, me tira uma dúvida aqui, quem é? Quem é que tu conversa? Quem é o coordenador que?
que está relacionado contigo aí só para mim bater um papo e dar uma alinhada lá porque
Como tem impacto aí, pode impactar no que tu tá fazendo.

Jefferson Vieira Alves   6:43
And.

Paulo Henrique Barros Santos   6:46
O Marcelo, Marcelo Mesquita.

Jefferson Vieira Alves   6:48
Isso, isso, what's your mask? Isso, what's your?

Paulo Henrique Barros Santos   6:49
Tá, eu vou bater um papo com o Marcelo.

Jefferson Vieira Alves   6:52
É, eu troquei. Eu troquei uma ideia na sexta-feira com outro colega aqui que a gente desenvolve. Ele tem mais conhecimentos ainda. Ele é mais antigo nesses projetos, principalmente o projeto legado, e esse do do Enp.

Paulo Henrique Barros Santos   6:52
Só para dar uma olhada.
Cert.

Jefferson Vieira Alves   7:09
E eu estava trocando uma ideia com ele sobre é essa questão aí do.
They're not a key.

Paulo Henrique Barros Santos   7:19
Qual dessas aqui que eu vou estar mostrando? Aqui.

Jefferson Vieira Alves   7:20
É sobre essa questão do Jackson, eu tava conversando com ele, é.

Paulo Henrique Barros Santos   7:23
Mm-hmm.
Mas a gente pode, por exemplo, se vocês não conseguiram chegar num ponto aí de solução que nem o Jesse falou aí, a gente pode chamar o Pablo lá do CCR para trocar uma ideia, ver como é que ele resolveu.

Jefferson Vieira Alves   7:39
Mhm.
Entendi.

Paulo Henrique Barros Santos   7:43
A gente usa forças aqui, porque realmente é o CIPHEC completo aí, com todos os módulos, ele é um ambiente bem complexo.

Jefferson Vieira Alves   7:53
Isso, entendi.

Paulo Henrique Barros Santos   7:53
Então a gente vamos ajudando, vamos lá um ajudando o outro aí nos entendimentos que já passou pra gente tentar sair do outro lado.

Jefferson Vieira Alves   8:00
É porque assim o como ele é no final das contas, o rural e o comercial, ele é, são módulos, são módulos do CIP.

Paulo Henrique Barros Santos   8:08
Okay.
Sim.

Jefferson Vieira Alves   8:11
E aí o a gente pode até ver com no nas outras, nos outros módulos do CIP que precisou tanto fazer de alteração.

Paulo Henrique Barros Santos   8:21
Sim, a ideia é essa que eu não estou te falando assim. Então, assim, se tu de cara já, cara, era legal pra já bater um papo com o Pablo, a gente já viabiliza isso aí. Com relação a essa questão aqui, a gente, enfim, a gente vai tentando.

Jefferson Vieira Alves   8:23
Isso.

Paulo Henrique Barros Santos   8:36
Sai do outro lado, né?

Jefferson Vieira Alves   8:38
Uhum, não é. Eu acredito que é importante.

Paulo Henrique Barros Santos   8:42
Porque aí esses módulos a gente vai meio que deixar eles, cara, meio que aguardando esses ajustes de pacote para fazer de novo. Vamos começar a trabalhar em outros pacotes. Aí tem bastante.

Jefferson Vieira Alves   8:53
Mm-hmm.

Paulo Henrique Barros Santos   8:54
olha aqui ó tem cada de coisa pra gente deployando aí

Jefferson Vieira Alves   8:58
Mhm.

Paulo Henrique Barros Santos   9:00
Beleza, eu vou conversar com Marcelo e aí eu não sei se tu quiser já trocar uma ideia com o Pablo, eu peço para o Pablo ficar à disposição ali.
Ou a gente chama ele pra cá também, enfim.

Jefferson Vieira Alves   9:15
É Pablo Leite Costa.

Paulo Henrique Barros Santos   9:18
Acho que é, né? Acho que ele está no grupo aqui.

Jesse Mouta Pereira Batista   9:19
Isso, isso mesmo.

Jefferson Vieira Alves   9:21
É, acabei de ver que ele está no grupo.

Jesse Mouta Pereira Batista   9:22
Right.

Paulo Henrique Barros Santos   9:23
From A.C.C.

Jefferson Vieira Alves   9:26
Not the Okay for the document there for me.

Paulo Henrique Barros Santos   9:29
Que aí eu marco ele lá, eu até mando a mensagem aqui no privado para ele falando que a gente precisa de uma ajuda aí, beleza?

Jefferson Vieira Alves   9:34
Pronto.
Pronto, perfeito.
E aí a gente vai se falando.

Paulo Henrique Barros Santos   9:40
Beleza, e aí eu vou, vou acertar com Mesquita lá para a gente dividir a prioridade dos trabalhos, tá? Eu vou ver com ele o que que.

Jefferson Vieira Alves   9:44
Yes.
Isso, só ali, só alinha com ele. Isso. Tranquilo então.

Paulo Henrique Barros Santos   9:49
Sim, vou alinhar, pode ir.
Beleza, valeu Jefferson.

Jefferson Vieira Alves   9:54
William William William William.

Jesse Mouta Pereira Batista   9:56
Valeu. Valeu.

Paulo Henrique Barros Santos   9:57
Aí galera!

Jefferson Vieira Alves   9:57
That.

Paulo Henrique Barros Santos   9:59
vou aí o que que eu tô pensando aqui tá
A gente podia focar aqui, está nessa parte de intranet primeiro, depois a gente dá uma olhada no restante, então seria.
O nosso foco de trabalho aqui, o escopo por hora.
colocar em amarelo aqui, eu vou compartilhar essa planilha aqui no grupo.

Jesse Mouta Pereira Batista   10:21
Beleza.

Paulo Henrique Barros Santos   10:22
Beleza e aí a ideia é que nem eu coloquei aqui, pacote em 10, né? Eu não sei qual pacote que a gente colocou, não necessariamente seja o mesmo de produção, né?

Jesse Mouta Pereira Batista   10:30
Mhm.

Paulo Henrique Barros Santos   10:31
Até porque em alguns a gente já está até mexendo no pacote, né? E isso vai ser um pacote novo. Se for o mesmo pacote, beleza. Até fica fácil depois para a gente levar a produção. Aí é só a gente colocar se foi feita essa implantação aqui com sucesso, e não com a pendência. Por exemplo, esse aí já está com.

Jesse Mouta Pereira Batista   10:34
Tá até mais a frente né do que
Mhm.

Paulo Henrique Barros Santos   10:49
a dependência já está aí em análise com o desenvolvedor daqui, ó os 3, né? 5 empresa, essa empresa ainda vou tentar descobrir que com quem que a gente vai tratar.

Jesse Mouta Pereira Batista   10:55
Mm-hmm.
Beleza.

Paulo Henrique Barros Santos   11:01
Acho que vai ter que ser com a equipe lá mesmo. Eu sei que eles não têm nem conhecimento.
Eu não vou colocar como implantado porque não está implantado. A gente tentou implantar e deu pau.
É isso?

Jesse Mouta Pereira Batista   11:13
Isso, exatamente.
Precisava do ajuste. A princípio é o ajuste simples, o mesmo ajuste inicial lá que o Pablo fez. Realmente é o caso de saber quem é a fábrica dele mesmo.

Paulo Henrique Barros Santos   11:31
Sim.
Aqui tá no grupo aqui, não tá não? Jeferson Vieira.
Jesus.
É, a gente pode fazer isso aqui, Oh, se fax ciru.
Pode fazer começar por esses 3 últimos aqui.
What say?
Começar a fazer tipo agora a tarde, mas é como é que está?

Jesse Mouta Pereira Batista   14:01
De desculpa, Paulo, eu tava eu tava falando mudo, é ciru LCR e o cred.

Paulo Henrique Barros Santos   14:05
Okay.
Por que foi o Crédito PJ?

Jesse Mouta Pereira Batista   14:09
Esse Crédito PJ é o do Pablo que a gente já subiu ou não?

Paulo Henrique Barros Santos   14:12
Ele é com esse nome aqui, então ele já está OK, então esse cara já está OK.

Jesse Mouta Pereira Batista   14:14
E Workflow Crédito PJ.

Thiago Jeferson de Sousa Silva   14:15
Venho com esse nome aí.

Jesse Mouta Pereira Batista   14:19
Isso.

Paulo Henrique Barros Santos   14:20
de Contratos de Contratos.

Jesse Mouta Pereira Batista   14:22
Yes.
Let's see, Jata.

Paulo Henrique Barros Santos   14:26
As well.

Jesse Mouta Pereira Batista   14:27
Tá certo, beleza.

Paulo Henrique Barros Santos   14:28
Então, CIP, O LCR.

Jesse Mouta Pereira Batista   14:31
Mhm. Beleza.

Paulo Henrique Barros Santos   14:31
E agora que na prática, cara, vamos começar a fazer todos aí na sequência, acho que CCR também já foi, que era aquele que o procote estava atuando.

Jesse Mouta Pereira Batista   14:40
Isso.
Então, espera aí, vamos lá, é o que acontece? Foi essa. Acho que foi até essa questão que a gente confundiu, né? Jefferson, o CCR, ele é o mesmo workflow ou isso aí já é outra coisa? Porque a princípio a gente estava tratando ele a princípio, a gente estava tratando ele como CCR. Então acredito que esse CCR não foi ainda não, viu Paulo?

Paulo Henrique Barros Santos   14:54
Então tem outras coisas.

Jesse Mouta Pereira Batista   15:02
Esse workflow aí, beleza, que a gente chama ele de PJ, é isso, né?

Paulo Henrique Barros Santos   15:05
Isso, eu acredito que seja porque não tem outro PJ aqui, eu dei uma olhadinha rápida.

Jesse Mouta Pereira Batista   15:09
Mm-hmm.

Thiago Jeferson de Sousa Silva   15:10
A gente implantou o workflow como CISCCR PJ.

Paulo Henrique Barros Santos   15:10
Thing I.

Jesse Mouta Pereira Batista   15:14
Isso, ele está com esse nome, CISCCR PJ.

Paulo Henrique Barros Santos   15:19
Será que tem diferença aí nesse caso a gente precisaria tirar essa dúvida com o Pablo então

Jesse Mouta Pereira Batista   15:23
É.
Tem que ver com ele. É, acho que ele já resolve.

Paulo Henrique Barros Santos   15:26
Deixa eu chamar logo ele aqui que a gente já mata esse essa dúvida aqui.

Jesse Mouta Pereira Batista   15:30
Okay.

Paulo Henrique Barros Santos   15:33
Essa planilha fica mais ajustada
Bob blue.

Jesse Mouta Pereira Batista   15:44
Late.

Paulo Henrique Barros Santos   15:46
H.

Jesse Mouta Pereira Batista   15:47
Yeah.

Paulo Henrique Barros Santos   15:50
Okay.

Jesse Mouta Pereira Batista   15:51
Isso.

Paulo Henrique Barros Santos   15:52
Deixa eu ver se ele consegue entrar aqui.
O pablo, beleza?

Pablo Leite Costa   16:12
Oi pessoal, boa tarde! Joia?

Paulo Henrique Barros Santos   16:14
What the?

Jesse Mouta Pereira Batista   16:15
Boa tarde. Beleza.

Paulo Henrique Barros Santos   16:16
o cara tá podendo falar cara

Rodrigo Abreu Costa   16:17
That's right.

Pablo Leite Costa   16:19
O outro, sim, eu estava na ligação ali, mas vou dar prioridade aqui.

Paulo Henrique Barros Santos   16:24
Agradeço cara, agradeço bastante. A gente está fazendo aqui um.
Para aqui do que a gente já fez aqui no ambiente do Cifec, né? Que tu tem acompanhado aí.
E aí, como tu está com CCR PJ, pelo que eu entendi.
A gente ficou um pouco na dúvida aqui se esses pacotes que você deve estar vendo aí são pacotes da produção, tá? Então a gente estava.

Pablo Leite Costa   16:43
A.
Pera aí, eu não tô vendo ainda não.

Paulo Henrique Barros Santos   16:51
Ainda não? Então, pera aí.

Pablo Leite Costa   16:52
No, no, be sure.
Quem tiver compartilhar com você Paulo, se puder compartilhar de novo.

Paulo Henrique Barros Santos   16:57
So, so, so.
It is.

Pablo Leite Costa   17:05
agora está carregando o conteúdo e vai aparecer

Paulo Henrique Barros Santos   17:07
Believe.

Pablo Leite Costa   17:11
Fine.
So.
Estou na sala, deixa eu sair, entrar de novo aqui na sala, pera aí.

Paulo Henrique Barros Santos   17:21
Bill is.

Jesse Mouta Pereira Batista   17:21
É, a gente está conseguindo ver normal.

Pablo Leite Costa   17:23
É, acho que é minha máquina aqui, deixa eu sair e entrar de novo.

Paulo Henrique Barros Santos   17:27
It is.

Pablo Leite Costa   17:45
É cara, é minha máquina, pessoal, não consigo ver, mas se vocês puderem falar, eu vou tentar entender o que é.

Paulo Henrique Barros Santos   17:53
Então, mas eu vou tirar um print da tela aqui.

Pablo Leite Costa   17:57
Uh-huh.

Paulo Henrique Barros Santos   17:58
colocar no grupo
Mais.
Fácil.
Dá uma olhadinha aí, tem um, tem um ser, a parte tá ali servidor em amarelo, sifec intranet.
carregou para ti a imagem

Pablo Leite Costa   18:20
Arregou.

Paulo Henrique Barros Santos   18:22
Lá no finalzinho do da parte amarela, a última linha tem assim, workflow, Crédito PJAR 8 ponto 40.

Pablo Leite Costa   18:29
Then.

Paulo Henrique Barros Santos   18:30
Esse cara aí é o pacote PJ?

Pablo Leite Costa   18:34
É o pacote PJ.

Paulo Henrique Barros Santos   18:37
É porque o pessoal falou que está com outro nome, né? Ele está com se CIPEC ou é CCR, PJ, alguma coisa assim. Mas o pacote é o mesmo.

Pablo Leite Costa   18:37
He's so where I am.
Okay.
Isso, o pacote é o mesmo, tá? É porque esse cara é o WAR do projeto, entendeu?
Yeah.
E o nome que é o nome que ele é compilado e deployado no J Boss.
Até onde eu sei, é o cifec mesmo.
mas o nome do projeto é o Workflow Crédito PJEAL. Esse é o nome que ele é persistido lá no Nexus. Se a gente for lá no Nexus lá, deixa eu até pegar aqui.

Paulo Henrique Barros Santos   19:20
No.

Pablo Leite Costa   19:26
e mandar para vocês
Thanks.
I show.
Como eu não estou vendo a tela de vocês, eu vou nem tentar compartilhar aqui não, mas eu vou mandar o link.

Paulo Henrique Barros Santos   19:52
Tranquilly.

Pablo Leite Costa   19:57
e vocês vão entender o que que

Paulo Henrique Barros Santos   19:59
Deixa eu tirar uma outra dúvida aqui, é esse pacote, ele é o mesmo que vai para internet?

Pablo Leite Costa   20:01
Mm-hmm.
Ele é o mesmo que vai para internet, tá? Porque o que que acontece? Esse cara aqui, ó.

Paulo Henrique Barros Santos   20:13
Do do.

Pablo Leite Costa   20:15
fez aqui, vê se vocês conseguem abrir ali o link.
Então esse cara aqui é um nome
Do meu pacote, tá? Só que o EAR gerado.
Se você for clicar dentro aí de cada pacote desse daí
Then, I have a swen one for Pedrops discussed.
It tá gerando this day.

Paulo Henrique Barros Santos   20:51
L geral workflow ponto EAR.

Pablo Leite Costa   20:54
Isso, ele gera uma ponta a R lá dentro do Nexus.

Paulo Henrique Barros Santos   21:01
Sim.
O.
A gente só estranhou aqui mesmo a questão pela nomenclatura, tá?

Pablo Leite Costa   21:11
And should aqui no que eu mandei para vocês?

Paulo Henrique Barros Santos   21:12
Thank you.

Pablo Leite Costa   21:17
Mas esse é o pacote gerado dentro do Pon, tá? É o nome dele lá dentro do Pon, é o Word PJ Crédito.

Paulo Henrique Barros Santos   21:25
Search.

Pablo Leite Costa   21:26
Quando a gente gera?
Quando a gente gera, faz o download dele, deixa eu pegar aqui, esse é o 8 ponto 40, não é?
Wait, they should be imagine.

Paulo Henrique Barros Santos   21:41
É ponto 40.1.

Pablo Leite Costa   21:43
8.40.1.

Paulo Henrique Barros Santos   21:46
Esse aqui é uma lista que eu peguei semana passada com o pessoal da Produção. Se não subiu nada, deve ser esse o.
Pacote que está em vigente, não é?

Pablo Leite Costa   22:02
And it seems.
Bone.

Paulo Henrique Barros Santos   22:05
que também é o mesmo que está na internet, no ambiente de internet.

Pablo Leite Costa   22:09
Please.
Então o deixa eu pegar aqui agora, esse é o releases, deixa eu pegar aqui o William Mack.
Let's next Jorge.
Deixa eu compartilhar minha tela aqui, vamos ver se vocês conseguem ver.

Paulo Henrique Barros Santos   22:45
A.

Pablo Leite Costa   22:55
Quando aparecer mais vocês me avisa, tá?

Paulo Henrique Barros Santos   22:58
And.

Jesse Mouta Pereira Batista   23:02
Para mim já está aparecendo.

Pablo Leite Costa   23:06
Então vamos lá dentro do Nexus, ele gera esse nome certinho aqui, workflow crédito PJ, que é 8 40.0.1. Quando a gente gera ele o compilador, aí é o próprio.

Paulo Henrique Barros Santos   23:06
So I see.
Mhm.

Pablo Leite Costa   23:22
É o próprio Shell na hora de gerar o pacote que eu mandei para vocês foi Skype.
This is fine.
Ele gera.
através do deploy dentro do
Do da ferramenta de Jesse, ele gera esse cara aqui.
Esse cara, ele tem um nome diferente.
Ele tem um nome diferente.
Do pacote gerado dentro do Nexus, tá? Aí o motivo Eu Acredito que é o sh que faz deploy, tá? Mas se você for ver o diretório dele aqui, ele está certo, tá vendo? O workflow crédito PJE.

Paulo Henrique Barros Santos   24:11
Mm-hmm.

Pablo Leite Costa   24:13
E aí ele traz a versão snapshot.
E aí ele traz um cara, tá certo, tá? O Controle Crédito.
That's it.

Paulo Henrique Barros Santos   24:24
Mm.
Não, beleza, assim, já até aqui.

Pablo Leite Costa   24:27
So to search you.

Paulo Henrique Barros Santos   24:29
Aqui já está até está, ficou até esclarecido já.

Pablo Leite Costa   24:29
Yes.
É porque o que você deve ter recebido deve ter sido isso daqui, nesse pé que.

Paulo Henrique Barros Santos   24:38
CCR PJ até apareceu aí, ó, ó lá ó.

Pablo Leite Costa   24:41
Thanks, this same big, it's a kind of key.
É porque esse cara aqui, quando a gente a gente gera um build local.

Paulo Henrique Barros Santos   24:51
Já era desse jeito.

Pablo Leite Costa   24:53
E era desse jeito. Então acredito que foi pego esse cara aqui e colocado lá, tá? Aí depois a gente começou a mandar para você dentro do Nexus. Aí pegava o link e mandava para você. Então acho que essa que foi a divergência.

Paulo Henrique Barros Santos   25:01
Entendi, entendi.

Pablo Leite Costa   25:07
A divergência foi a quem gerou o local e mandou para vocês em vez de pegar dentro do binário.

Paulo Henrique Barros Santos   25:08
Então beleza, tá bom.

Pablo Leite Costa   25:15
aqui é o nome correto dele

Paulo Henrique Barros Santos   25:19
Não beleza aí deixa eu te perguntar então assim a gente pode entender então que esse pacote ele tá ele tá no ar aí no novo ambiente tá ok né

Pablo Leite Costa   25:27
No novo ambiente está OK, já pode dar OK. Eu entrei lá, fiz os testes, é editei operação, fiz uma inserção.
In Tel
Ele não tem nada ainda que não precisa de evoluir mais nada dele nele, não pode dar como fechado.

Paulo Henrique Barros Santos   25:45
Não show.
Show de bola!
Tem, tem mais alguma coisa do CCR aí, o do que tu atua, cara? Que o CCR é bem picado, né?

Pablo Leite Costa   25:54
Got it.
É bem picado, é. Se eu não estou muito enganado, o procote, ele atuou direto no tributário. Eu acho que o tributário é um dos mais críticos.
And.

Paulo Henrique Barros Santos   26:06
Sim.

Pablo Leite Costa   26:08
É aí teria que ver com o pacote, está porque eu só peguei aqui do PJ.

Paulo Henrique Barros Santos   26:11
Não vejo, vejo com ele, vejo com ele.

Pablo Leite Costa   26:15
Só vi realmente eu só vi do PJ, eu não vi os demais não.

Paulo Henrique Barros Santos   26:20
não beleza a mim fechou aqui quando chega aqui cara brigadão na verdade eu deixa eu aproveitar uma oportunidade aqui que é o seguinte o pessoal comentou que tu passou por um algumas questões aqui que o

Pablo Leite Costa   26:22
Andre data.
He is a money.

Paulo Henrique Barros Santos   26:35
O dev lá do siempe.
É, tá passando parecido, tá? Que é o Jefferson, Jefferson Alves.

Pablo Leite Costa   26:43
Mm-hmm.

Paulo Henrique Barros Santos   26:44
Aí, cara, tu consegue depois dar um apoio para ele só para tu meio que dar uma direcionada. O que tu fez para resolver teu pacote?

Pablo Leite Costa   26:51
Você ligo o Jefferson o quê?

Paulo Henrique Barros Santos   26:53
Jefferson Alves.
Não Vieira Alves.

Pablo Leite Costa   26:58
Little song.

Jesse Mouta Pereira Batista   26:58
É a questão lá, Pablo, desculpa interromper, Paulo, é a questão lá do Jackson, tá, Pablo? Que foi o primeiro errinho lá que a gente pegou. Lembra do do do workflow aí do PJ?

Paulo Henrique Barros Santos   27:02
For phone.

Pablo Leite Costa   27:11
Lembro, lembro sim. Ele está tendo esse mesmo problema.

Jesse Mouta Pereira Batista   27:13
All right.
É só o mesmo problema, exatamente, é o mesmo problema.

Pablo Leite Costa   27:20
Está, eu estou mandando mensagem aqui para ele.

Jesse Mouta Pereira Batista   27:23
Tá.

Pablo Leite Costa   27:25
Boa tarde.
Tá, vou falar que.
Eu vou falar que vocês mandaram mensagem para mim sobre o problema lá do Jackson, e aí, se ele tiver dúvida, ele me chama aqui.

Jesse Mouta Pereira Batista   27:37
Mhm.

Paulo Henrique Barros Santos   27:37
Isso.

Jesse Mouta Pereira Batista   27:39
Yes.

Paulo Henrique Barros Santos   27:39
Beleza, bacana cara!

Pablo Leite Costa   27:42
Beleza, pessoal? Valeu! Já tem data programada já?

Paulo Henrique Barros Santos   27:42
We got that.

Jesse Mouta Pereira Batista   27:44
Beleza.

Paulo Henrique Barros Santos   27:47
A gente está montando, a gente também está subindo um ambiente de produção ainda, o pessoal está criando máquina, está nesse processo.

Pablo Leite Costa   27:52
Mhm.

Paulo Henrique Barros Santos   27:56
A ideia é que a gente suba um ambiente paralelo, então deve ter um ambiente que nem a gente está criando aqui com o pessoal aqui em desenvolvimento, migração. A ideia é a gente ter outra outra vertical lá também de produção.

Pablo Leite Costa   27:59
Sim.
Mhm.
Mhm.

Paulo Henrique Barros Santos   28:09
até pra gente fazer um teste, um piloto controlado ali e aí a gente vai informando.
Mas, cara, todo o trabalho está focado para isso acontecer até o final desse mês, tá? Então, com relação a data mesmo, seria algo assim.

Pablo Leite Costa   28:16
Oh, believe.
Querendo ou não vai subir, né?

Paulo Henrique Barros Santos   28:25
Pô cara, vai ter que acontecer velho.

Pablo Leite Costa   28:28
Vai, vai ter que acontecer de um jeito ou outro. Não, beleza. Eu mandei mensagem aqui para ele, está se vocês precisar de qualquer coisa de ajuda minha e eu e eu conseguir resolver alguma coisa para vocês, me falam, beleza?

Paulo Henrique Barros Santos   28:30
See.
Brigadão, viu?
A.
Pô, show de bola, cara! Obrigadão mesmo!

Pablo Leite Costa   28:42
Beleza, valeu, Jesse, valeu Paulo. Valeu, galera.

Jesse Mouta Pereira Batista   28:45
Valeu, Pablo. Valeu.

Paulo Henrique Barros Santos   28:48
Falou, valeu.

Pablo Leite Costa   28:48
Valeu, tchau.

Jesse Mouta Pereira Batista   28:49
No.

Rodrigo Abreu Costa   28:49
William William.

Paulo Henrique Barros Santos   28:50
Tchau.
Vou pegar o compartilhamento de novo aqui, pessoal.

Jesse Mouta Pereira Batista   28:54
Tá, beleza.

Paulo Henrique Barros Santos   28:59
é o que que a gente já pode fazer no caso do workflow
ele falou que tá ok né ele já fez os testes então assim
Eu vou dar OK aqui pra esse workflow, mesmo que a versão está diferente, porque o profile de SSO que nem eu falei, eu vou confirmar lá com Luiz depois, mas eu acho que isso aqui é um ambiente que ainda não está funcional. Assim, quando eu falo não está funcional, não está aberto.
para uso na internet pessoal deve estar fazendo uma preparação aqui mas só para para fingir

Jesse Mouta Pereira Batista   29:28
There.

Paulo Henrique Barros Santos   29:32
de associar né uma coisa com a outra aqui eu vou colocar aqui tá ok mesmo que tá com a versão antiga
And.
A internet também, que é o que o pessoal deve estar em uso mesmo efetivo, que é esse aqui é o mesmo pacote da intranet.
Então vou aqui só para ver esse Controle também eu vou dar ok aqui também
A ideia é mais ou menos fazer isso, porque vocês vão ver que tem pacote repetido nos profiles.

Jesse Mouta Pereira Batista   30:00
É, lá tem uns pacotes repetidos mesmo.

Paulo Henrique Barros Santos   30:01
So.
Que aí é só para a gente não, então aí.

Jesse Mouta Pereira Batista   30:05
Yeah.
For quotes.
Exactly.

Paulo Henrique Barros Santos   30:19
Ok, mas esse aqui, até porque eu acho que realmente não está em uso, não está antigo ou o pessoal ainda não está dando andamento nesse trabalho aqui. Aqui é só mesmo só para a gente não perder de vista.

Jesse Mouta Pereira Batista   30:31
Beleza.

Paulo Henrique Barros Santos   30:32
Beleza.

Jesse Mouta Pereira Batista   30:32
Beleza.

Paulo Henrique Barros Santos   30:37
é CCR se eu não me engano esse aqui foi aquele que o procote atuou né é esse do CCR tem mais um outro aí que é o de tributo que eu confesso que eu nem sei qual seria

Jesse Mouta Pereira Batista   30:47
Mhm.

Paulo Henrique Barros Santos   30:49
So.
Pode tentar chamar o procote aqui também.
BE C.
Pessoal, acho que vamos fazer assim, eu vou compartilhar esse aqui com vocês Bora focar nesses dois aqui pra gente tentar

Jesse Mouta Pereira Batista   31:06
Isso no s no ciru e a LCR, tá?

Paulo Henrique Barros Santos   31:09
Isso para a gente que aí o ciru eu tenho condição de colocar a galera para fazer teste depois que terminar.

Jesse Mouta Pereira Batista   31:15
Best.

Paulo Henrique Barros Santos   31:16
No.
E aí eu vou colocar a gente, eu vou atualizando, vou deixando vocês poderem também. Se vocês querem escrever aqui, vai ser um negócio meio para a gente trabalhar mesmo, tá?

Jesse Mouta Pereira Batista   31:25
Tá fechando.

Paulo Henrique Barros Santos   31:27
Beleza?

Jesse Mouta Pereira Batista   31:28
Beleza.

Paulo Henrique Barros Santos   31:28
Ei senhores, qualquer coisa me chama e marca aqui.

Jesse Mouta Pereira Batista   31:30
From.
Beleza então, obrigado Paulo.

Thiago Jeferson de Sousa Silva   31:33
That's it.

Paulo Henrique Barros Santos   31:33
Nada. Valeu, galera. Até mais.

Jesse Mouta Pereira Batista   31:34
Obrigado, Rodrigo. Oi, Jefferson, falou, valeu. Não, achei que você tinha falado alguma coisa.

Rodrigo Abreu Costa   31:35
Beleza, valeu, valeu.

Thiago Jeferson de Sousa Silva   31:37
O Oper.
No, no, só agradecer.

Jesse Mouta Pereira Batista   31:43
Beleza. Obrigado Rodrigo. Valeu.

Rodrigo Abreu Costa   31:45
Valeu, valeu, senhor. Contratos.

Jesse Mouta Pereira Batista   31:47
Thanks.

Jesse Mouta Pereira Batista parou a transcrição



Boa tarde,
 
REQ000146999232 - Certificado SIEMP esteira em DES, solicitamos a gentileza de priorizar o atendimento desta requisição.
 
Patricia do Prado Albuquerque
 
Elisabeth da Silva Ana Paula Pazitto da Costa
 
Jesse Mouta, boa tarde.
 
Fiz um novo build de artefato do SICDT com as alterações de algumas dependências, se puder republicar, agradeço. Segue o link:
http://binario.caixa:8081/repository/releases/br/gov/caixa/sicdt/sifec-cdt/3.24.3.003/sifec-cdt-3.24.3.003.ear
 
Flavio de Almeida Gagliardi adicionou Marcela Gomes da Silva ao chat e compartilhou o histórico de chats dos últimos 83 dias.

 
Paulo Henrique Barros Santos
Criação ambiente SIPEN (PRODUÇÃO)      WO0000082203406 Criação de servidores do SIPEN - Aguardando atendimento   WO0000082163841 Emissão do certificado para o ambiente de transmissão: migracaos…
Boa tarde Marcela Gomes da Silva
PC
SIPEN apto para criação do ambiente PRD
 
Flavio de Almeida Gagliardi
Boa tarde Marcela Gomes da Silva PC SIPEN apto para criação do ambiente PRD

Boa noite! Quem da CEPIP é responsável do SIPEN em ambiente PRD? Já está na sala?
 
