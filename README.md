Pessoal, atualização do SILCR:

Conferimos as versões. A silcr-1.19.0-b152.ear que tentamos subir no JBoss 7.4 é a mesma versão que roda hoje no 6.4 (DES), então não é problema de pacote trocado. O deploy foi revertido pelo CDI (Weld) durante a validação das injeções. Não há erro de datasource nem de JNDI. A análise é do Thiago Jeferson, a quem agradeço.

Erros encontrados (WELD-001408 – dependência não satisfeita):

DadosSICLIDao injetado em DadosSICLIBean
AliquotasIofDao injetado em AliquotasIofBean
Logger injetado em UserProfile. O único producer de Logger que o servidor encontrou tem o qualifier @BatchProperty, que não é compatível com um @Inject Logger sem qualifier.

Por que funciona no 6.4 e não no 7.4: o CDI do 7.4 (Weld 3) é mais rígido na descoberta de beans. Classes que antes eram reconhecidas automaticamente agora precisam estar num módulo com beans.xml válido ou ter anotação de escopo.

Ajustes necessários no código/empacotamento (fábrica):

Garantir que o jar onde ficam as implementações de DadosSICLIDao e AliquotasIofDao esteja dentro do EAR e tenha META-INF/beans.xml com bean-discovery-mode="all", ou que as classes tenham anotação de bean (@Stateless, @ApplicationScoped, @Dependent etc.).
Fazer o mesmo com a classe que produz o Logger (o método @Produces). Ela precisa estar num módulo que o CDI enxergue.
Gerar uma nova versão do EAR para fazermos o deploy.

Dúvida de versão: a planilha de PRD indica sifec_lcr_1.117.1, com numeração diferente da silcr-1.19.0-b152 do DES. Alguém do LCR pode confirmar se é a mesma aplicação e qual versão deve ser usada na migração? Assim a correção já sai na versão certa.

Quando o pacote novo estiver pronto, faço o deploy e valido o log. Do nosso lado, já vou conferir a configuração de segurança (Keycloak) do lcr-web.war, que existe no 6.4.

Enquanto a fábrica ajusta: o Keycloak do lcr-web.war

No 6.4 (10.116.88.20), veja como está a configuração do lcr-web.war dentro do bloco do sifec-intranet:

sudo sed -n '57701,58040p' /opt/jboss/jboss-eap/dc/configuration/domain.xml | grep -n 'lcr'

Se aparecer algo, me mande. Repare que os 7 secure-deployment que achamos antes (linhas 20507 a 29932) ficam fora do range do server-group. Eles estão nos profiles, então também quero saber qual profile o sifec-intranet usa no 6.4:

sudo sed -n '57701,57710p' /opt/jboss/jboss-eap/dc/configuration/domain.xml

No 7.4 (471, no CLI), veja se o lcr-web.war já está configurado:

/profile=full-ha-sifec-intranet/subsystem=keycloak:read-children-names(child-type=secure-deployment)

Se o lcr-web.war não aparecer na lista do 7.4, a gente cria igual ao do 6.4 antes do próximo deploy. Assim, quando o código passar do Weld, não trava na autenticação.
