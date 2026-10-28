Prezado Welinton,

Analisamos a falha na release do SIACG-gde (TQS, namespace siacg-tqs).

Causa: a aplicação Quarkus não subia porque duas variáveis de ambiente referenciadas no application.properties não estavam disponíveis no momento do deploy:

JANELA_ENVIO_HORA_INICIAL (propriedade gde.janela.envio.hora-inicio)
JANELA_ENVIO_HORA_FINAL (propriedade gde.janela.envio.hora-fim)

Sem essas variáveis, a validação de configuração do SmallRye falhava (SRCFG00011: Could not expand value) e o pod siacg-gde-tqs-60 encerrava na inicialização. Por isso o rollout não concluía e a task “Verificando Status do Deployment” era cancelada.

Situação atual: na execução seguinte, as variáveis foram resolvidas. O deployment siacg-gde-tqs-61 foi concluído com sucesso e a aplicação iniciou normalmente (Quarkus 3.2.0, profile prod, porta 8080).

Recomendação: sempre que novas propriedades com placeholder ${...} forem incluídas no código, é preciso cadastrar as variáveis correspondentes na Library/variáveis da release de cada ambiente (DES/TQS) antes do deploy.

Observação: no log de inicialização em TQS, a MAP de permissões está sendo carregada do caminho /SIACG/login-module/DES. Sugerimos que a equipe confirme se esse é mesmo o caminho esperado para o ambiente TQS.

Diante do exposto, encerramos a demanda.

Atenciosamente,
Jessé Batista – CESTI
