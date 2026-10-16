Bom dia, Roberto e Ivan!

Analisando o histórico da release, encontramos a causa: às 11:45 a variável UNICO_BIOMETRIC_SDK_KEY foi removida do stage TQS e recriada às 14:35. No intervalo, o build rodou sem a chave, por isso o valor chegou vazio.

Esclarecendo: a injeção da chave pela esteira é exatamente essa variável cadastrada na release. Não há outra origem automática. Ela deve permanecer lá para o app receber o valor no build.

Do jeito que está agora (variável recriada pelo Ivan), está correto e funcionando.

Para HMP/PILOTO/PRD será necessário cadastrar a variável também nesses stages, com a chave correspondente a cada ambiente, se a XID fornecer chaves diferentes.


Sobre proteger a chave como secret: hoje ela está em texto aberto, e é por isso que o System.getenv funciona. Variável secret no Azure DevOps Classic não vira variável de ambiente. Para marcar como secret, antes o Ivan precisa ajustar o build.gradle para ler também via project.findProperty("unicoSdkKey"). Depois testamos em TQS e só então ativamos o secret. Podemos fazer isso juntos quando vocês quiserem.
