Pablo, o deploy do sifec-ccr-pj passou dos problemas de ambiente (jaas-sifec, FECMail e as queries estão ok). Agora falha no CDI/Weld:

WELD-001408: Unsatisfied dependencies for type Usuario with qualifiers @UsuarioContexto no ponto de injeção OperacaoIntegracaoMQAbstrata.usuario (pacote br.gov.caixa.intgr.comum).

O Weld do EAP 7.4 não encontra o produtor @Produces @UsuarioContexto Usuario. Verifique se o jar onde está esse produtor tem META-INF/beans.xml com bean-discovery-mode="all" e se ele é visível para o jar intgr-comum (no ear/lib, o jar não enxerga classes do .war). No 6.4 isso passava porque o CDI era mais permissivo. Assim que gerar o novo build, eu implanto.
