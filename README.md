Prezados,

Após análise das evidências encaminhadas, verificamos que o retorno apresentado (HTTP 500 com mensagem de negócio “Erro ao registrar”) é gerado pela própria aplicação. Isso indica que a requisição passa pelo API Gateway (api.des.caixa:8443), é autenticada e chega ao backend, que falha ao processar o registro. Portanto, não há indício de bloqueio de proxy nem de permissão de acesso, cenários que retornariam erro de conexão ou HTTP 401/403.

Observamos também que as evidências comparam operações diferentes: a requisição de sucesso é uma consulta (GET /push/v3/Registros/{id}), e a de falha corresponde a uma operação de registro.

Por não se tratar de assunto do escopo da equipe de Esteiras DevOps (DES/TQS), estamos encaminhando a demanda à Infraestrutura. Sugerimos verificar no API Gateway e nos logs do backend da API de Notificações Digitais (Push v3) a chamada no horário da falha, pelo horário ou pelo correlation-id da resposta. Para agilizar, o solicitante deve anexar a requisição completa (método, URL, headers sem credenciais e body).

Atenciosamente,
Jessé Batista – CTIS/CESTI – Esteiras DevOps DES/TQS
