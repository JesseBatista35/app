Paulo, resumo de hoje no JBoss 7.4 (DES, sifec-intranet):

✅ No ar: SIFEC 2.160.3.0 (Jackson corrigido), SIFEC-CCR, SICCR-BDCAIXA, HUB-FRONTEND e MINUTAS-FRONT. O SIEMP 14.37.0.6 também está no ar, no grupo siemp.

🔧 Ambiente ajustado: security domains jaas-sifec e java:/jaas/jaas-sifec, mail session FECMail (smtp.correio.caixa:25) e API JMS liberada no profile.

⏳ Pendências de código (com os devs):
• SICCR-PJ 8.40.1: CDI, @UsuarioContexto sem produtor (OperacaoIntegracaoMQAbstrata).
• SIFEC-EMP (3.95 e 3.92): VeiculosTotalizadorBean não expõe a interface VeiculosTotalizadorService.
• SIEMP-EMPRESAS 1.2.3-b15: ParametrizacaoBean não expõe a interface ParametrizacaoService.
Nos três casos, a classe precisa declarar implements ou @Local da interface. Testamos no ambiente o modo de CDI compatível com o 6.4, sem efeito.

⏳ Pendência de ambiente (comigo):
• SIFEC-RURAL 2.115.1.1: o JVM do SIFEC aponta a truststore para um caminho do Windows (C:/Desenvolvimento/...). A correção é criar uma truststore com as ACs da Caixa e aplicar com restart do sifec-intranet. O SIFEC fica fora do ar por alguns minutos. Aguardando a confirmação de vocês sobre o melhor horário para esse restart. Com o OK, eu aplico e faço o deploy do RURAL em seguida.
