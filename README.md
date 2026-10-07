Chamada com Elza e 6 outras pessoas-20261007_154830-Transcrição da Reunião
7 de outubro de 2026, 06:48PM

Jesse Mouta Pereira Batista começou a transcrição

Jailson Martins Alves   0:03
Para que as pessoas migrem para o Terraform, para acabar com esse negócio de esse bom antigo.
Ah tá é Inclusive eu tô aguardando Robson retornar para a gente conversar com o Reinaldo a respeito disso porque assim a gente não dá mais suporte para ciência bom antigo cara porque se a gente continuar dando suporte por esse antigo
Não vai morrer nunca isso. Isso nunca vai ser migrado para o terra forma, entendeu? O que a gente está orientando? Pô, desabilitem a pesca de monitoração, então.
Sacou? Agora, como a gente não falou com o Reinaldo, mas tá aí o Marinho e o Flávio, é, a gente precisava ver com vocês qual vai ser a ação que a gente vai tomar. Vai dar suporte a isso ou não? Porque esse esse.
Tem que morrer, cara. Uma forma que a gente tem que de achar para o povo migrar para o Terraforme é essa, não dando mais suporte, porque um tempo atrás o Reinaldo falou para a gente não dar mais suporte para a ciência.

Flavio de Almeida Gagliardi   1:07
Fala aí Jailson, beleza?

Jailson Martins Alves   1:08
And yeah, they lay the flag.

Flavio de Almeida Gagliardi   1:10
Ó, já compartilho com a sua revolta aí também acho que o pessoal não tem que usar, tem que migrar, mas é na prática não é muito bem assim, tá? E assim a gente já tentou aqui com alguns times, por exemplo, a fizemos até a migração para o pessoal validar lá e a coisa não foi para frente, né?
Estou atendendo demanda de negócio, não posso mexer nisso agora, não sei o que. Isso que você falou agora do Reinaldo, falar para parar de dar suporte. Eu não tenho essa informação não, tá Jailson? É precisar ver ele mesmo, se a gente vai.

Jailson Martins Alves   1:43
Mhm.

Flavio de Almeida Gagliardi   1:47
fazer isso porque normalmente quando a gente toma uma assim mais drástica, a coisa acaba se voltando contra a gente, tá? O pessoal começa a reclamar, mas assim, eu concordo que tem que tem que migrar, tem que ter um movimento aí para fazer essa migração.

Jailson Martins Alves   1:55
Sim.
Mhm.

Flavio de Almeida Gagliardi   2:04
É, enquanto isso não acontece, tá? Que eu sei que não é rápido, a gente precisava meio que assim, deixar funcional, sabe? Porque eu entendo que isso daí não é uma coisa que parou de, nunca funcionou, né? Isso daí.
Estava funcionando aí, um Monte de gente usa.

Jailson Martins Alves   2:22
Não, sim, deixa eu te falar, deixa eu te falar esse negócio que o Reinaldo falou, cara, tem uns 4 anos atrás, tá?

Flavio de Almeida Gagliardi   2:29
I see.

Jailson Martins Alves   2:30
Eu garanto para você que ele não vai lembrar mais, como aconteceu do SIGCX, que ele autorizou a gente usar o cluster do Pix e depois falou que não era para usar, e depois a gente cassou a documentação e ele tinha autorizado.

Flavio de Almeida Gagliardi   2:36
Sim, sim.

Jailson Martins Alves   2:45
sacou então assim o que que acontece é

Flavio de Almeida Gagliardi   2:45
Excel.

Jailson Martins Alves   2:51
Houve uns ajustes que foram feitos no Terraform devido a algumas mudanças realizadas pela Microsoft tá que antigamente a gente tinha um IP fixo e a Microsoft mudou lá na Azure mudou não é mais IP fixo agora a gente usa a FQDN
A cada momento muda o IP do Zabbix, sacou? Então a gente passou a utilizar a FQDN, então a gente fez vários ajustes no código para o Terraform, enquanto essa teste ficou desativada.
Tá, foi ativada novamente, voltou a funcionar, só que a gente não teve problema na no ensio antigo.
O que tem que ser feito agora? Eu tinha comentado isso com Arnaldo ontem e o código é muito parecido por Terraform enquanto por esse, só que há alguma divergência entre um e o outro. Se vai reativar isso, beleza, não tem problema, a gente vai pedir.

Dyego dos Santos Barros   3:41
Yeah.
Brazil.

Jailson Martins Alves   3:47
para desativar testes de monitoração e a gente vai pedir para o Arnaldo avaliar.

Dyego dos Santos Barros   3:48
Não sei, acho que sim.

Jailson Martins Alves   3:55
Para que seja adequado com esse bom antigo.
Entender?

Flavio de Almeida Gagliardi   4:01
No, entendi, entendi.
É, mas é que assim, eu não sei quanto tempo vai levar isso daí, tá Jailson? E o que está acontecendo é que estão quebrando aqui. O pessoal está abrindo um Monte de chamado porque está quebrando as releistas por conta disso.

Jailson Martins Alves   4:04
No.

Flavio de Almeida Gagliardi   4:19
Será que tem como é colocar alguém para avaliar isso de maneira mais imediata?

Jailson Martins Alves   4:25
Olha só, Flávio, a gente pode conversar com o Arnaldo, tá? Só que a gente tem um problema que Sério, porque isso não é feito na no.
no git tá esse ajuste tem que ser feito manualmente em todos os agentes não é igual Terraforma você faz lá no nosso repositório no git ele replica para todo mundo não conhece o antigo você vai ter que fazer
Servidor por servidor, ou seja, nós temos, acho que são 12 servidores, tem que ajustar o código nos 12 servidores.

Flavio de Almeida Gagliardi   5:03
Tá, e esse eu já entendi, já que é uma coisa bem trabalhosa, mas esse ajuste que tem que ser feito, a gente já sabe o que é, tipo, é só começar ou ainda vai ter que ter algum?

Jailson Martins Alves   5:08
Thing.
Sim, boa parte, não, boa parte dá para fazer. Só que a gente tem umas particularidades, não é esse o antigo que eu não sei se vai funcionar, que eu tenho que conversar com Arnaldo, porque ele tem um usuário lá e uma senha que no Terraform a gente não tem isso.

Flavio de Almeida Gagliardi   5:17
So.
Ta.

Jailson Martins Alves   5:31
Entendeu? Então eu comecei a dar uma olhada no código, fiz alguns ajustes, mas não surtiu efeito. Eu falei, cara, não é só isso não, velho.
Esse que você estava vendo, Jorge?
Houve umas alterações nos agentes aqui? Sim, eu comecei a mexer, só que não surtiu efeito.

Jorge Milis de Almeida Junior   5:44
Sim.
Mm-hmm.

Jesse Mouta Pereira Batista   5:48
É, a gente olhou 67, Jailson, a gente até setou ele lá dentro no e aí testou e não deu certo.

Jailson Martins Alves   5:52
Sim, não, eu fiz. Sim, eu fiz no 67, eu fiz no 771 e 72.
foi um sistema que eu peguei que tava dando problema eu acho que era o Software não sei o que aqui o

Jesse Mouta Pereira Batista   6:05
Backend, CGPD backend.

Jailson Martins Alves   6:07
Isso é esse cara mesmo, sacou? Aí não, bicho, desativa isso aí, desativa isso aí que eu tenho que ver, tenho que ver aqui com Arnaldo. Aí eu falei com o Arnaldo, o Arnaldo falou, cara, é pra funcionar. Eu falei, mas não tá funcionando.

Jesse Mouta Pereira Batista   6:19
And.

Jailson Martins Alves   6:20
Cara, estou numa reunião aqui, estou numa call aqui, depois você me procura, beleza, está bom.
Então, agora sim, se vocês querem que a gente faça isso, pede para desativar a TSK de monitoração, que eu vou repassar isso para o Arnaldo, eu vou trabalhar em conjunto com ele para a gente sanar isso. Mais uma vez, eu peço que tentem migrar isso.
Tudo por Terraform, para acabar com esses problemas.

Flavio de Almeida Gagliardi   6:45
Sim. O Mário, tem algum problema essa desativação aí?
This a task.

Mario Luiz Costa Marinho da Silva   6:50
Não, cara, não vejo problema nenhum. Inclusive, se você acha que está impactando aí, cara, você pode até colocar um condicional, Jailson.

Jailson Martins Alves   7:01
Mm.

Mario Luiz Costa Marinho da Silva   7:02
para verificar se for uma aplicação do molde do Terraform executa se não for esquipa por enquanto entendeu

Jailson Martins Alves   7:09
Thank you.

Flavio de Almeida Gagliardi   7:10
Oh, hein, that's bem legal.

Mario Luiz Costa Marinho da Silva   7:12
Aí, como é que você pode fazer esse condicional? Ou você busca se a pipeline de DevOps, ou você busca o Henrique conhece bastante. Se você quiser, pode ver com ele. Se tiver, por exemplo, aquela library de terraform esteira common, sabe? É uma boa forma de você.

Jailson Martins Alves   7:26
Mm.

Mario Luiz Costa Marinho da Silva   7:27
é determinar que ***** isso aqui é uma Terraform ou então você simplesmente ver se tem a teste do Cria VM Terraform né

Jailson Martins Alves   7:34
Aí, ô Flávio, desculpa, Mário, aí tem um outro problema, sabe o que é? Alguns projetos já não está mais utilizando a library do terraform, sacou? Tá lá no infradevops.

Mario Luiz Costa Marinho da Silva   7:40
Mm.
Não tá usando mais a do do

Jailson Martins Alves   7:49
Não, não, não. Tem outro que já vem lá do infra fácil, já vem lá do infra fácil, sacou?

Dyego dos Santos Barros   7:51
So.

Mario Luiz Costa Marinho da Silva   7:51
Então buscar na festa então.
Entendi, então busca na testa, se ele tiver com a testa, significa que ele está usando a

Flavio de Almeida Gagliardi   7:57
Let's.

Jailson Martins Alves   8:02
Não, mas a TSC tem nos dois, tem tanto no Encebo quanto no Terraform.

Mario Luiz Costa Marinho da Silva   8:08
Não a Tesk D Terraform. Se a pipeline tiver a Tesk que cria VM Terraform, ela não é um modelo, entendeu?

Jailson Martins Alves   8:10
Ah, tá, tá, entendi, entendi, entendi, entendi.
Entendi, entendi.
Beleza, vamos fazer um laboratório aqui.

Flavio de Almeida Gagliardi   8:22
Você dá um toque aí, Jailson, na sala aqui você.

Jailson Martins Alves   8:22
mas viu sim Flávio é você pede para o pessoal desativar cara tá o Flávio a deu problema no sistema XPTO por favor desativem a teste de monitoração que o pessoal de suporte está fazendo os ajustes
para acionar esse problema, beleza?

Flavio de Almeida Gagliardi   8:40
Está uma vez que uma vez que desativa essa task aí a release do cara.

Jailson Martins Alves   8:46
Não desativa aí não. Eu digo desativar na pipeline do projeto. Se você desativar aí, você desativa para todo mundo.

Jesse Mouta Pereira Batista   8:47
Não.

Thiago Jorge Araujo   8:49
Okay.

Jorge Milis de Almeida Junior   8:55
Pois é, é isso que eu queria mostrar. É porque assim, a gente tem outras arquivos que estão junto aqui. Se eu venho aqui e desativo aqui, esses aqui no impacto não.

Jesse Mouta Pereira Batista   8:58
É.

Jailson Martins Alves   9:02
Não é aí, não é aí, não é aí, você vai desativar aquela dali. Volta lá, Jorge, por favor, a de baixo. Isso é essa daí.

Jorge Milis de Almeida Junior   9:09
Essa aqui.

Thiago Jorge Araujo   9:09
O.

Jorge Milis de Almeida Junior   9:12
Então, essa aqui é só lembrando, essa aqui é a global que todo mundo utiliza, tá? Então, quando a gente desativar aqui, o pessoal do Terraform também vai parar de utilizar, tá?

Jesse Mouta Pereira Batista   9:12
Yes.

Jailson Martins Alves   9:16
Não, mas é sim isso.
Sim, não, mas é o que eu estou falando é que façam na release.

Jorge Milis de Almeida Junior   9:25
É, tem que ser aqui.

Jailson Martins Alves   9:27
Na não aí não na release do projeto isso abre o CGPD abre ele aí você já está nele, beleza? Então aí você vai editar a release, você está editando a pipeline, edite a release.

Jorge Milis de Almeida Junior   9:27
Porque?
What is it?

Jesse Mouta Pereira Batista   9:31
Mm.
Mm.

Jorge Milis de Almeida Junior   9:34
about is.
Pois é, só que se eu só que se eu editar a release, o que é que acontece? Eu consigo editar a release, o pessoal da fábrica que vai executar, eles não conseguem. Então, quando eles executarem uma próxima release, vai quebrar.

Jesse Mouta Pereira Batista   9:47
No.
Uma nova.

Jailson Martins Alves   9:53
O que a gente estava fazendo no CG? Não, como é que era?
Hello!
Sigs the sheets.
O pessoal eles pegavam, precisava da monitoração, só que a gente não tinha feito as correções ainda. Então o que era feito? Eles criavam release, não rodava release, depois alguém aqui de suporte ia lá e editava release e habilitava.
Só que depois descobriu-se que o povo da produção, eles tinha essa permissão para fazer isso.
Então passou-se a gente não fazer mais, entendeu? O próprio pessoal da produção.

Jorge Milis de Almeida Junior   10:32
Pois é, mas as fábricas não tem, mas a fábrica não tem.

Mario Luiz Costa Marinho da Silva   10:33
No.
É exatamente.

Jorge Milis de Almeida Junior   10:37
A fábrica não tem para poder fazer isso aqui. Ontem eu até fiz isso, ontem tinha uma que estava quebrando aqui, é, eu entrei na release, rodei, desabilitei lá na tesquezinha da release e rodei e funcionou. Só que hoje, quando ele só não rodar, deu o mesmo erro, entendeu? Porque foi só na é.

Jailson Martins Alves   10:51
Same, because I

Jorge Milis de Almeida Junior   10:53
Então, assim, o que teria que desabilitar para enquanto está fazendo essa avaliação, teria que ser desabilitado aqui. Aí é para geral, para todo mundo, até ser feita essa avaliação, aí depois retornaria.

Jailson Martins Alves   10:53
Só naquela rede.
Sim, todo mundo.

Mario Luiz Costa Marinho da Silva   11:08
E convenhamos o Jailson, se desabilitar isso aí agora.
É, não vai ter impacto para quem precisa usar, correto? Porque uma vez que a Esteiras está instalada, anão ser que o cara destrua VM positivo, já está instalada.

Jailson Martins Alves   11:21
não não não não todo momento que ele faz a release ele faz a verificação

Mario Luiz Costa Marinho da Silva   11:27
Ah, entendi, tem que rodar isso aí.

Jailson Martins Alves   11:27
Ele vai fazer a verificação, é, tem que rodar esse cara aí, independente se está instalado ou não, entendeu?

Mario Luiz Costa Marinho da Silva   11:29
Cara, o assim.
Esse condicional aí que eu te falei, você pode levar algumas horinhas, não é difícil tá, que ele devolve ser bem tranquilo que mexer. Agora, o que você pode fazer por enquanto Jorge é habita habita habita habita habita habita aa a aa afd
A nível de interface do usuário é meio ruim, vai ter gente abrindo um hack porque vai ter coisinha vermelha na pipeline, mas o devox vai executar e vai ficar verdinho no final, pelo menos, vai dar como concluído. Mas no desespero tem essa opção também, entendeu Flávio?
Existe essa opção? Não, lá é dentro da Tesk mesmo, lá na no script isso aí, control options ali, ó.
A lá você bota continue em um erro, entendeu? E aí quem vai executar vai tomar erro?
Mas o DepoLer vai seguir, vai concluir e a galera do Terraform vai executar, vai funcionar porque o Terraform funciona, então vai dar de boa, entendeu? É um paliativo.

Jailson Martins Alves   12:30
Yes.

Flavio de Almeida Gagliardi   12:32
É, eu acho que entre mortes e feridos, aí essa é a paliativo menos impactante, né?

Mario Luiz Costa Marinho da Silva   12:36
Yep.

Jorge Milis de Almeida Junior   12:37
A.

Mario Luiz Costa Marinho da Silva   12:38
E como a gente tem poucas pipelines do modelo antigo do Ansible, acho que vai ser o impacto mínimo, cara. Eu sou a favor de fazer isso aí, entendeu?

Flavio de Almeida Gagliardi   12:44
Ah tá bom beleza não vamos seguir por esse caminho então aí Elza demais aí CESTI né que suporte Pode ser que vocês comecem a receber esse tipo de hack mesmo tá
E aí tem que explicar lá que isso tá em avaliação pode até fechar a REC tá a nossa teve que a gente desabilitou porque a gente tá passando por manutenção E aí a gente vai avaliando caso a caso aqui né
Você que me procurem aqui, eu vou falando com os coordenadores também. Normalmente o pessoal me aciona aqui e aí se eu precisar de ajuda, eu procuro vocês, mas vamos por esse caminho por enquanto. Acho que é o que impacta menos. E aí, Jailson, quando você tiver uma notícia boa aí.

Jailson Martins Alves   13:28
Beleza, eu vou.

Flavio de Almeida Gagliardi   13:32
Você pode chamar a gente aqui.

Jailson Martins Alves   13:34
There is all this, all this.
E se eu me reúno agora com Arnaldo para a gente trabalhar em cima disso?

Flavio de Almeida Gagliardi   13:42
A.

Jailson Martins Alves   13:43
Beleza?

Flavio de Almeida Gagliardi   13:44
Beleza.

Jorge Milis de Almeida Junior   13:44
Fabio, você abre uma rec pra gente, pra gente ir autorizando?

Flavio de Almeida Gagliardi   13:48
Ó, tem tem alguma já rolando aí? Não, né?

Jorge Milis de Almeida Junior   13:49
Okay.

Jesse Mouta Pereira Batista   13:52
Tem, tem 3, tem 2, na verdade são 3. Na verdade, fiz até um relatóriozinho que a principia mandar lá para Serv por lá, mas aí já tinha um tratado. Aí é, tem uma demanda assim já. Se você quiser, quer usar ela?

Jorge Milis de Almeida Junior   13:53
Okay.

Flavio de Almeida Gagliardi   14:08
What's it?

Jesse Mouta Pereira Batista   14:08
Aqui a gente coloca, coloca o contexto aqui.
Vou te mandar aqui, Jorge.

Jorge Milis de Almeida Junior   14:16
Esse aqui eu coloco aqui autorizado Pedro Flávio

Jesse Mouta Pereira Batista   14:18
Isso aí, aqui a gente coloca aí, oh, pronto.

Jailson Martins Alves   14:21
Mm.

Flavio de Almeida Gagliardi   14:21
Autorizado pelo Flávio Marinho.

Jesse Mouta Pereira Batista   14:24
É essa daí?
Essa WO aí que eu mandei, é essa WO que eu mandei ali, ela é exclusiva do cirta, porém nessa WO eu coloquei uma nota citando o SIPG back-end, o SIPQVL back-end, até agora foram os 3 que a gente tinha olhado que estava dando esse problema, tá?

Jorge Milis de Almeida Junior   14:27
já coloca todo mundo envolvido

Dyego dos Santos Barros   14:44
e eu tô com uma do Seara também que tá dando mesmo problema aí Seara

Flavio de Almeida Gagliardi   14:45
Eu vou.

Jesse Mouta Pereira Batista   14:47
se alvo né aí se aa

Flavio de Almeida Gagliardi   14:53
Eu estou entrando nela aqui, já vou colocar a nota lá, tá? Deixa eu acessar aqui.

Jesse Mouta Pereira Batista   14:56
Tá, beleza, tem uma nota minha aí da que a gente tava encaminhando pra Serv, mas eu vou retificar e vou vou fazer outra, tá?
a gente finalizar aqui nossa aula, beleza?

Jailson Martins Alves   15:10
Beleza, então a gente tá tá acordado aqui, então dessa forma, né? Vou trabalhar aqui com o Arnaldo, beleza?

Jesse Mouta Pereira Batista   15:10
Salvou.
Beleza.

Jorge Milis de Almeida Junior   15:17
Desde meu Nobre.

Flavio de Almeida Gagliardi   15:17
Beleza, cara.

Jesse Mouta Pereira Batista   15:18
Thank you.

Jailson Martins Alves   15:22
O.

Jorge Milis de Almeida Junior   15:22
Vou rodar uma nova do GPD aqui, tá? O Jesse é para a gente testar.

Jesse Mouta Pereira Batista   15:28
Beleza, beleza, até isso aí eu estou rodando aqui do cirta.

Jailson Martins Alves   15:32
Então beleza, falou pessoal.

Jorge Milis de Almeida Junior   15:34
Valeu, Mendes, brigadão.

Jesse Mouta Pereira Batista   15:34
Valeu Jailson, obrigado.

Jailson Martins Alves   15:35
Ah, até mais.

Dyego dos Santos Barros   15:36
Will you pass on?

Flavio de Almeida Gagliardi   15:36
pessoal o Jesse eu acho que tá presa contigo aí essa aí eu não consigo editar tá uma

Jesse Mouta Pereira Batista   15:38
Oi.

Mario Luiz Costa Marinho da Silva   15:38
Hello, hello.

Jesse Mouta Pereira Batista   15:39
TSing.
Pronto, pode ir.
Okay.
064902.
No.

Flavio de Almeida Gagliardi   16:58
Como que é o nome da task aí para eu deixar bonitinho aqui que eu não tô olhando a tela tá

Jesse Mouta Pereira Batista   17:05
Okay.

Jorge Milis de Almeida Junior   17:06
Configurando stack de monitoração.

Flavio de Almeida Gagliardi   17:10
Ah, é, na verdade, o que vai setar aí é o continue on error, né?

Jorge Milis de Almeida Junior   17:14
Isso, habilitar continue um erro na TSK.

Flavio de Almeida Gagliardi   17:15
Beleza, Joe.

Jesse Mouta Pereira Batista   17:15
So.
Mas a até essa até a Tesk Group, a Tesk é a configura de e-boi instala monitoração.

Flavio de Almeida Gagliardi   17:25
No.

Jorge Milis de Almeida Junior   17:38
Vamos ver que já tá batendo ela aqui, vamos ver se ele vai dar erro e vai passar.

Flavio de Almeida Gagliardi   17:44
Como que é o nome da funçãozinha aí? Eu acabei de falar, mas esqueci, tá? Continue on error. Ah tá, essa mesmo.

Jorge Milis de Almeida Junior   17:49
Contínua um erro.
É, beleza, funcionou aqui ó, ele deu o erro.

Jesse Mouta Pereira Batista   18:03
Ele continua.

Jorge Milis de Almeida Junior   18:03
Ficou isso, mas continuou.
Show de bola, então assim, momentaneamente estamos resolvidos.

Jesse Mouta Pereira Batista   18:13
Resolvidos. Show.
Beleza.

Jorge Milis de Almeida Junior   18:21
Aí a gente coloca lá no grupo, está o Jesse uma nota.

Jesse Mouta Pereira Batista   18:24
É, eu vou, é, eu vou, vou botar uma nota em cima daquela lá, ajustando aquela lá, pode, pode deixar isso.

Jorge Milis de Almeida Junior   18:28
É falando para todo mundo que já está e pode que ele vai ficar como é como é parcial aqui, mas.

Jesse Mouta Pereira Batista   18:35
facial, né?
Mhm.

Jorge Milis de Almeida Junior   18:39
Está em análise.

Jesse Mouta Pereira Batista   18:42
Yes.

Flavio de Almeida Gagliardi   18:45
O eu coloquei a nota lá, é por enquanto estamos nessa, tá? Vamos esperar o Jailson se manifestar aí, espero que seja breve. É, eu estou voltando lá para outra sala, tá, pessoal?

Jorge Milis de Almeida Junior   18:59
Tranquilo, valeu.

Jesse Mouta Pereira Batista   18:59
Beleza, Gagliardi, eu posso fechar essa WO.

Flavio de Almeida Gagliardi   19:00
Valeu, pessoal.
Giga.
Então ela tá deixa ela deixa ela deixa ela pendente por enquanto se alguém te encher o saco você pede para falar comigo daí beleza valeu até mais

Jesse Mouta Pereira Batista   19:06
Ela é do cirta. Tá, vamos deixar ela pendente.
Beleza, não, tranquilo, fechou. Valeu, valeu.

Elza Oliveira Leao   19:16
Obrigada, Flavio.

Flavio de Almeida Gagliardi   19:18
I little else to jump.

Jesse Mouta Pereira Batista   19:18
Valeu, valeu, obrigado por te falei Elza que era bomba. Antes eu estava chamando ela Jorge Milis, era era 2 e 50. Ó, quando você logar nem respira, só já me chama aqui.

Elza Oliveira Leao   19:22
Pois é, que isso?
So faltou chamar o Reinaldo.
E uma bomba.
Great.

Jorge Milis de Almeida Junior   19:38
É isso aí. Ele estava desde ontem que ele estava dando esse problema, só que aquele que ele está falando a gente a gente consegue editar no na teste aqui do da release, mas o pessoal não consegue.

Jesse Mouta Pereira Batista   19:42
Mm.
pra pra poder parar a transcrição aqui Elza é só sair né? É só quando eu sair né? Da sala né?

Elza Oliveira Leao   19:56
Quem começou? Não tem. Todo mundo tem que sair. Deixa eu derrubar o.

Jesse Mouta Pereira Batista   19:57
Foi eu.
The Roberto Isaiasing.

Elza Oliveira Leao   20:02
Is a Ieda a Ieda a Ieda?
So hard.
Yes.

Jesse Mouta Pereira Batista   20:11
See.

Elza Oliveira Leao   20:13
Yeah.
Aê, obrigado, gente. Vocês vão fazer a notinha para a gente passar para os demais analistas.

Jesse Mouta Pereira Batista   20:20
É isso, vou, é, eu vou, eu vou. Eu vou pegar aquela minha nota lá e vou retificar ela e explicar lá para o pessoal lá do MV, está?

Elza Oliveira Leao   20:29
Beleza, precisa de alguma coisa?

Jesse Mouta Pereira Batista   20:30
Pode ficar tranquilo. Valeu Elza, valeu Jorge.

Jorge Milis de Almeida Junior   20:33
Will this auto age?

Elza Oliveira Leao   20:34
Hello, TS.

Jesse Mouta Pereira Batista   20:34
Aqui o cirta passou, Deus deu bom. Valeu. Valeu.

Jorge Milis de Almeida Junior   20:36
Então beleza.

Jesse Mouta Pereira Batista parou a transcrição
