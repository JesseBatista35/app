A build falhava na etapa “Executando Build S2I Binary”. O upload do binário (sisko-backend.ear + jboss-deployments) para o BuildConfig sisko-backend era interrompido com o erro Unable to connect to the server: unexpected EOF na chamada instantiatebinary da API api.produtos4.caixa:6443. As duas tentativas (execução e retry) foram encerradas aos 60 segundos de upload.

Análise:
As etapas de compilação (Maven), publicação no Nexus e login no cluster foram concluídas com sucesso. A falha estava restrita ao envio do artefato para o build S2I no OpenShift. O corte da conexão sempre no mesmo tempo indicava que o upload não concluía dentro do limite da requisição.

Solução:
Foi realizada a limpeza [descrever o que foi limpo, ex.: de builds/imagens antigas do BuildConfig sisko-backend no namespace build-images-ads / do workspace do agente]. Depois disso, a build foi reexecutada e concluída com sucesso, incluindo a geração da imagem.

Status: Resolvido. Build executada com sucesso.
