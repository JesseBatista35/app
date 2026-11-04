Pablo, boa tarde!

Atualização do deploy do SICCR-PJ 8.40.1 (workflow-credito-pj-ear-8.40.1-20261104.180249-4.ear) no JBoss 7.4 (DES, server-group sifec-intranet).

✅ O que já foi ajustado e validado:

Queries HQL: a sua correção funcionou. A persistence unit fec.wpj.pu sobe sem erro no Hibernate 5.3.
Security domain jaas-sifec: criado no profile do sifec-intranet. Atende o workflow-credito-pj-web.war.
Security domain java:/jaas/jaas-sifec: criado também, porque o EJB SecurityKeycloakUtils referencia o domínio com o prefixo antigo do EAP 6.
Mail session java:jboss/mail/FECMail: criada, apontando para smtp.correio.caixa:25.
Reload do sifec-intranet: feito para ativar as configurações. O SIFEC voltou normalmente (2.160.3.0).

❌ O que falta (código):

O deploy agora falha no CDI/Weld:

WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto
at injection point: @Inject @UsuarioContexto
br.gov.caixa.intgr.comum.operacao.OperacaoIntegracaoMQAbstrata.usuario

O Weld do EAP 7.4 não encontra o produtor @Produces @UsuarioContexto Usuario. Encontra só o Usuario padrão, sem o qualifier.

Sugestão de verificação:

Confirmar se o jar que contém o produtor tem META-INF/beans.xml com bean-discovery-mode="all".
Confirmar se o produtor está visível para o jar intgr-comum. Dentro do ear/lib, os jars não enxergam classes do .war.

No 6.4 isso funcionava porque o CDI era mais permissivo na descoberta de beans.

Sugestão para o próximo build: trocar a referência java:/jaas/jaas-sifec por jaas-sifec (padrão do EAP 7). Com isso o domínio com prefixo deixa de ser necessário.

Assim que o novo pacote estiver no Nexus, me avisa que eu faço o deploy. Do lado do ambiente, está tudo pronto.
