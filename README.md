Pessoal, atualização da investigação do build do SIGEC-Portabilidade (branch rtc/STRY00052082_migracao_java_17):

Já identificamos e contornamos um dos problemas. O build falhava com erro 500 ao baixar o pacote arqref-services-3.6.3.13 do Nexus. Trocando a versão para a 3.31.0 em uma branch de teste (Cesti-001), o erro 500 deixou de ocorrer e os módulos gec-xml, gec-azure, gec-common e gec-ejb compilaram com sucesso.

Seguimos investigando um segundo ponto: o módulo gec-batch agora falha por não encontrar o artefato caixa-framework-2.0.1 no Nexus. Estamos validando se é uma versão ausente ou algum problema no repositório.

Assim que tivermos novidades, avisamos aqui na sala.
