Prezados,

Foram realizados os ajustes para injeção da chave do SDK Unico (câmera XID) na esteira do App Habitação (release SIAME-Android-Nativo):

Criada a variável UNICO_BIOMETRIC_SDK_KEY nas variáveis da release.
Ajustado o comando de build (variável BuildGradle) para repassar a chave ao Gradle via parâmetro -PunicoSdkKey.
O app/build.gradle passou a ler a chave via project.findProperty("unicoSdkKey"), com fallback para a variável de ambiente, e a disponibiliza em BuildConfig.XID_UNICO_BIOMETRIC_SDK_KEY em todos os buildTypes.

Ação necessária da equipe: gerar uma nova release para TQS (releases antigas não recebem a alteração) e validar o funcionamento da câmera no fluxo XID.

Pontos de atenção:

A chave está configurada com escopo de Release, ou seja, o mesmo valor vale para TQS, HMP, PILOTO e PRD. Questionamos via Teams se os demais ambientes usam chave diferente e não houve retorno. Caso a equipe XID forneça chaves específicas por ambiente, favor abrir nova solicitação informando os valores.
Recomendação: marcar a variável UNICO_BIOMETRIC_SDK_KEY como secreta no Azure DevOps. Hoje ela está visível em texto aberto. O build já está preparado para isso.

Em caso de falha no teste, favor reabrir a demanda anexando o log da task “Build Gradle” e o comportamento observado no app.

Demanda encerrada.
