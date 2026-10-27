Diagnóstico:
Os erros de “503 Service Unavailable” e “CORS” apresentados no SIGCB-frontend (TQS) não tinham origem no frontend nem na configuração de CORS da aplicação.

As requisições de preflight (OPTIONS) do frontend para o sigcb-backend-tqs.apps.nprd.caixa eram respondidas com 503 pelo router do OpenShift, porque não havia nenhuma instância do backend disponível para atender. Como essa resposta não vinha da aplicação, ela não continha os cabeçalhos CORS, e o navegador exibia o erro de CORS como consequência.

Causa:
O pod do backend (sigcb-backend-tqs, namespace sigcb-tqs) ficou travado no status “ContainerCreating” desde 26/10/2026. Com isso, o serviço ficou sem endpoints ativos. Não houve nova implantação da aplicação no período: a versão em execução era a mesma de 116 dias atrás. O travamento ocorreu na recriação do pod pelo cluster.

Ação realizada:
Foi executado um novo rollout do backend em TQS. O novo pod (deploy 183) subiu normalmente, a aplicação Quarkus iniciou com sucesso e o serviço voltou a ter endpoint ativo. A comunicação entre frontend e backend foi restabelecida.

Observação para a equipe de desenvolvimento:
O log do backend em TQS apresenta erro recorrente (a cada segundo) no agendamento ApropriacaoSimulacaoService#apropriarSimulacao:

DB2 SQLCODE=-204: objeto GCB.GCBTB446_APROPRIACAO_SIMULACAO inexistente no banco de TQS

O erro não impede o funcionamento da aplicação, mas indica que a tabela não foi criada no ambiente TQS e gera volume excessivo de log. Recomenda-se que a equipe responsável avalie a criação do objeto junto ao DBA ou ajuste a rotina.
