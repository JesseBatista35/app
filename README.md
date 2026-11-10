Pessoal, atualização do SILCR:

Ficou definido com o Paulo que a versão a subir no JBoss 7.4 é a sifec_lcr_1.117.1, que está na planilha de PRD.

Hoje essa versão não está disponível para nós. A única que existe na console e no servidor é a silcr-1.19.0-b152.ear, a mesma que roda no 6.4 DES. Tentamos com ela e o deploy foi revertido por erro de CDI (Weld). A análise é do Thiago Jeferson.

O que precisamos da fábrica:

Disponibilizar o pacote da sifec_lcr_1.117.1, com link do binário ou do build, para fazermos o deploy.
Ao gerar esse pacote, conferir os pontos de CDI que quebraram na versão do DES. É provável que eles se repitam no 7.4:
DadosSICLIDao (injetado em DadosSICLIBean) e AliquotasIofDao (injetado em AliquotasIofBean) não foram reconhecidos como beans. O jar que contém as implementações precisa estar no EAR, com META-INF/beans.xml (bean-discovery-mode="all") ou com anotação de bean nas classes.
Logger injetado em UserProfile: o único producer encontrado tem o qualifier @BatchProperty. A classe com o @Produces Logger da aplicação precisa ser visível para o CDI.

Quando o pacote estiver disponível, faço o deploy e acompanho o log. Do nosso lado, já vou deixar pronta a configuração de segurança (Keycloak) do lcr-web.war.

Alguém do LCR pode indicar quem gera esse pacote?
