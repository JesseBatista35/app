Prezados,

Após análise das evidências encaminhadas, verificamos que o retorno apresentado (HTTP 500 com mensagem de negócio “Erro ao registrar”) é gerado pela própria aplicação. Isso indica que a requisição passa pelo API Gateway (api.des.caixa:8443), é autenticada e chega ao backend, que falha ao processar o registro. Portanto, não se trata de bloqueio de proxy nem de permissão de acesso, cenários que retornariam erro de conexão ou HTTP 401/403.

Observamos também que as evidências comparam operações diferentes: a requisição de sucesso é uma consulta (GET /push/v3/Registros/{id}), e a de falha corresponde a uma operação de registro.

Orientamos que a demanda seja direcionada ao time responsável pela API de Notificações Digitais (Push v3), para análise do log da aplicação no horário da falha. Para isso, encaminhar a requisição completa (método, URL, headers sem credenciais e body). Caso seja necessário rastrear a chamada no gateway, o time responsável pelo API Gateway pode localizá-la pelo horário ou pelo correlation-id da resposta.

Por não se tratar de assunto do escopo da equipe de Esteiras DevOps (DES/TQS), estamos encerrando esta solicitação.

Atenciosamente,
Jessé Batista – CTIS/CESTI – Esteiras DevOps DES/TQS
