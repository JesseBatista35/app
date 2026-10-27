Análise:
A falha ocorreu porque a release foi executada no pipeline SISKO-backend, que é a esteira antiga, ainda configurada para o cluster OKD3. Ela usa os grupos de variáveis legados (OKD-NPRD / cloudnprd2.caixa). Durante o oc start-build com upload binário do sisko-backend.ear, a conexão com a API foi encerrada (Unable to connect to the server: unexpected EOF) e a task terminou com código 255.

O SISKO-backend já possui um pipeline de release próprio para o OKD4: SISKO-backend-okd4. É nele que as releases de DES/TQS devem ser geradas.

Solução / Orientação:

Gerar a release pelo pipeline Releases > SISKO-backend-okd4, selecionando o artefato de build desejado.
Não usar mais o pipeline SISKO-backend (OKD3), que está descontinuado para esse sistema.

Encerrando o chamado. Caso a execução no SISKO-backend-okd4 apresente qualquer falha, favor abrir nova solicitação com o link da release.
