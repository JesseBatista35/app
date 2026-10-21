Reunião de alinhamento ADDR SIGSJ | Pendências JBOSS 
Status Geral 
믆Em andamento
A reunião esclareceu a estratégia de implantação do SIGSJ na esteira DevOps, eliminando 
a necessidade de uma segunda pipeline para o Apache. 
Foram definidos os ajustes necessários no repositório e os próximos passos para 
viabilizar a publicação completa da aplicação. 
믇 Concluído 
Definições Técnicas 
 Confirmado que não será necessária uma segunda pipeline para publicação dos 
conteúdos estáticos. 
 A mesma solução atenderá Apache e JBoss. 脥�
 Esclarecida a arquitetura da esteira, que já contempla Apache e JBoss na 
infraestrutura disponibilizada. 脥�
 Definido que será utilizada inicialmente a URL padrão da esteira, evitando 
tratativas adicionais com certificados e URLs customizadas. 脥�
 Analisados exemplos de implementações de outros sistemas para servirem como 
referência para o SIGSJ. 脥�
믆 Em Andamento 
Adequação da Solução 
 Avaliação de modelos de configuração Apache mais aderentes ao cenário do 
SIGSJ. 
 Estruturação da solução para publicação conjunta dos artefatos da aplicação e 
conteúdos estáticos. 
 Evolução das atividades de migração e adequação do repositório. 
Responsáveis:
 Vitor Mendes Guedes 
 Suporte CESTI 
 
 
믅 Pontos de Atenção 
Estrutura do Repositório 
 O repositório ainda não possui a estrutura necessária para configuração do 
Apache (pasta HTTPD). 
Publicação dos Conteúdos Estáticos 
 A configuração do Apache precisa ser implementada e validada antes da 
execução dos testes completos. 
Validação Final da Migração 
 A equipe ainda não avançou para a etapa de homologação completa do processo 
de Deploy integrado. 
꼝 Pendências 
Pendência Responsável
Disponibilizar modelo de configuração Apache para 
referência Suporte CESTI 
Criar estrutura HTTPD no repositório Suporte CESTI
Implementar configuração Apache no projeto Equipe SIGSJ
Executar testes completos de implantação Equipe SIGSJ / Suporte 
CESTI 
Validar publicação dos conteúdos estáticos Equipe SIGSJ
Próximos Passos 
꼝 Alta Prioridade 
1. Criar a estrutura HTTPD no repositório. 
2. Disponibilizar e adaptar o modelo de configuração Apache. 
3. Concluir os ajustes necessários para a publicação da aplicação. 
믆 Média Prioridade 
4. Executar testes integrados envolvendo JBoss e Apache. 
5. Validar o funcionamento dos conteúdos estáticos após o Deploy. 



O conteúdo gerado por IA pode estar incorreto

Patricia Vourakis Barbosa Braga começou a transcrição

Evandro Alves de Souza
0 minutos 4 segundos0:04
Evandro Alves de Souza 0 minutos 4 segundos
I.
Evandro Alves de Souza 0 minutos 5 segundos
Imigração.
Evandro Alves de Souza 0 minutos 8 segundos
Vocês rodaram essa esse pacote no localmente aí no JBoss 74, né, Victor?
VG

Vitor Mendes Guedes
0 minutos 16 segundos0:16
Vitor Mendes Guedes 0 minutos 16 segundos
Sim, eu, Gisele, mas eu colchou esses 2 aqui, é, você pode responder, Gisele?
GD

Gisele Cristina Dias
0 minutos 22 segundos0:22
Gisele Cristina Dias 0 minutos 22 segundos
Sim, boa tarde.
VG

Vitor Mendes Guedes
0 minutos 22 segundos0:22
Vitor Mendes Guedes 0 minutos 22 segundos
Someone is that?

Marcio Aparecido Sitoni
0 minutos 25 segundos0:25
Marcio Aparecido Sitoni 0 minutos 25 segundos
Boa tarde.
GD

Gisele Cristina Dias
0 minutos 25 segundos0:25
Gisele Cristina Dias 0 minutos 25 segundos
Sim, a gente executou aqui de forma local.
J

Jesse Mouta Pereira Batista
0 minutos 26 segundos0:26
Jesse Mouta Pereira Batista 0 minutos 26 segundos
Good I do.
GD

Gisele Cristina Dias
0 minutos 32 segundos0:32
Gisele Cristina Dias 0 minutos 32 segundos
Aí a gente precisou, durante a migração, a gente precisou fazer algumas configurações ali no.
VG
Vitor Mendes Guedes
1 hora 4 minutos 34 segundos1:04:34
Vitor Mendes Guedes 1 hora 4 minutos 34 segundos
Isso é Gisele e Marcio, números para só isso?
Vitor Mendes Guedes 1 hora 4 minutos 43 segundos
a gente vai lá mais para frente que vai ter essa bula
GD
Gisele Cristina Dias
1 hora 4 minutos 52 segundos1:04:52
Gisele Cristina Dias 1 hora 4 minutos 52 segundos
Por enquanto não. Tô tranquilo.

Evandro Alves de Souza
1 hora 4 minutos 52 segundos1:04:52
Evandro Alves de Souza 1 hora 4 minutos 52 segundos
Acho.
VG
Vitor Mendes Guedes
1 hora 4 minutos 54 segundos1:04:54
Vitor Mendes Guedes 1 hora 4 minutos 54 segundos
No.

Claudio Monteiro Lima
1 hora 4 minutos 54 segundos1:04:54
Claudio Monteiro Lima 1 hora 4 minutos 54 segundos
Essa parte tá tranquila, Gisele, para poder transformá-la no Projeto WR.
GD
Gisele Cristina Dias
1 hora 4 minutos 59 segundos1:04:59
Gisele Cristina Dias 1 hora 4 minutos 59 segundos
Sim, sim.

Claudio Monteiro Lima
1 hora 5 minutos 1 segundo1:05:01
Claudio Monteiro Lima 1 hora 5 minutos 1 segundo
Então tranquilo, aí é só fazer esse teste, transforma esse projeto aí num WR, coloca o contexto dele para o JBoss poder identificar e aí coloca tudo junto, que aí quem vai passar a atender as requisições http no stat que vai ser o JBoss e não Apache.
Claudio Monteiro Lima 1 hora 5 minutos 17 segundos
A parte vai ser só uma camada de apresentação.
VG
Vitor Mendes Guedes
1 hora 5 minutos 22 segundos1:05:22
Vitor Mendes Guedes 1 hora 5 minutos 22 segundos
Não entendido, mas beleza, a gente vai testar aqui no local e aí se tiver alguma novidade ou impedimento, aí a gente avisa vocês.
GD
Gisele Cristina Dias
1 hora 5 minutos 23 segundos1:05:23
Gisele Cristina Dias 1 hora 5 minutos 23 segundos
Believe.

Claudio Monteiro Lima
1 hora 5 minutos 27 segundos1:05:27
Claudio Monteiro Lima 1 hora 5 minutos 27 segundos
Oh.
Claudio Monteiro Lima 1 hora 5 minutos 30 segundos
Tranquilo.
Claudio Monteiro Lima 1 hora 5 minutos 32 segundos
Precisa de ajuda para mais uma coisa pessoal?

Evandro Alves de Souza
1 hora 5 minutos 35 segundos1:05:35
Evandro Alves de Souza 1 hora 5 minutos 35 segundos
Não, Claudio, obrigado. Já esclareceu bastante. Aí devia ter colocado você na primeira reunião, porque eu não soube explicar isso para eles aí. Aí quando veio para cá, acho que deu problema.

Claudio Monteiro Lima
1 hora 5 minutos 38 segundos1:05:38
Claudio Monteiro Lima 1 hora 5 minutos 38 segundos
Okay.
Claudio Monteiro Lima 1 hora 5 minutos 42 segundos
I'm most fight so do I do.
Claudio Monteiro Lima 1 hora 5 minutos 45 segundos
Não faz isso não que eu estou com tanta coisa.
Claudio Monteiro Lima 1 hora 5 minutos 48 segundos
Eu vou começar a botar, vou começar a colocar coisa de outro projeto aqui sem querer, confundindo as coisas. Então tá bom gente, até mais, viu?

Evandro Alves de Souza
1 hora 5 minutos 54 segundos1:05:54
Evandro Alves de Souza 1 hora 5 minutos 54 segundos
Alves.
Evandro Alves de Souza 1 hora 5 minutos 56 segundos
Brigado Programas.
VG
Vitor Mendes Guedes
1 hora 5 minutos 57 segundos1:05:57
Vitor Mendes Guedes 1 hora 5 minutos 57 segundos
Claudio, obrigado, agradeço aí pelo SW. Obrigadão, viu?

Claudio Monteiro Lima
1 hora 6 minutos1:06:00
Claudio Monteiro Lima 1 hora 6 minutos
até mais
J
Jesse Mouta Pereira Batista
1 hora 6 minutos1:06:00
Jesse Mouta Pereira Batista 1 hora 6 minutos
Bingado.

Evandro Alves de Souza
1 hora 6 minutos 3 segundos1:06:03
Evandro Alves de Souza 1 hora 6 minutos 3 segundos
É, então, pessoal, eu vou colocar na sala lá que vocês vão fazer ajustes no código e depois fazer uma nova pipeline release e deploy, é isso?
VG
Vitor Mendes Guedes
1 hora 6 minutos 3 segundos1:06:03
Vitor Mendes Guedes 1 hora 6 minutos 3 segundos
That.
Vitor Mendes Guedes 1 hora 6 minutos 14 segundos
Isso, a gente vai fazer o ajuste aqui, testar localmente para ver se não teve nenhum tipo de mudança do que se espera da aplicação. E aí, se der certo, a gente vai fazer uma nova.
Vitor Mendes Guedes 1 hora 6 minutos 29 segundos
Logo de Pessoas e uma nova Rezende para ver como é que vai se comportar a Esteiras, tá?

Evandro Alves de Souza
1 hora 6 minutos 32 segundos1:06:32
Evandro Alves de Souza 1 hora 6 minutos 32 segundos
So.
Evandro Alves de Souza 1 hora 6 minutos 34 segundos
Tá bom, é quando vocês forem fazer, pode marcar lá na sala que a gente vai acompanhando aqui.
J
Jesse Mouta Pereira Batista
1 hora 6 minutos 39 segundos1:06:39
Jesse Mouta Pereira Batista 1 hora 6 minutos 39 segundos
Open the top.
VG
Vitor Mendes Guedes
1 hora 6 minutos 41 segundos1:06:41
Vitor Mendes Guedes 1 hora 6 minutos 41 segundos
Okay, no, that is.

Evandro Alves de Souza
1 hora 6 minutos 44 segundos1:06:44
Evandro Alves de Souza 1 hora 6 minutos 44 segundos
Pode falar, Jose.
J
Jesse Mouta Pereira Batista
1 hora 6 minutos 45 segundos1:06:45
Jesse Mouta Pereira Batista 1 hora 6 minutos 45 segundos
Não, desculpa, estava falando com minha esposa aqui, perdão.

Evandro Alves de Souza
1 hora 6 minutos 48 segundos1:06:48
Evandro Alves de Souza 1 hora 6 minutos 48 segundos
Ah, imagina.
Evandro Alves de Souza 1 hora 6 minutos 50 segundos
Então tá pessoal, acho que a gente pode encerrar aqui então.
VG
Vitor Mendes Guedes
1 hora 6 minutos 53 segundos1:06:53
Vitor Mendes Guedes 1 hora 6 minutos 53 segundos
isso pessoal obrigadão tá agradeço aí auxílio tá E aí qualquer coisa a gente avisa vocês tá boa tarde bom trabalho viu

Evandro Alves de Souza
1 hora 6 minutos 59 segundos1:06:59
Evandro Alves de Souza 1 hora 6 minutos 59 segundos
Tá bom, Vitor. Obrigado, pessoal.
J
Jesse Mouta Pereira Batista
1 hora 7 minutos1:07:00
Jesse Mouta Pereira Batista 1 hora 7 minutos
Obrigado, Vitor. Obrigado. Obrigado, Alexandre.

Evandro Alves de Souza
1 hora 7 minutos 3 segundos1:07:03
Evandro Alves de Souza 1 hora 7 minutos 3 segundos
Valeu, Jose, até mais.

Patricia Vourakis Barbosa Braga parou a transcrição
