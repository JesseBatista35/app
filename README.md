Prezado Ilson Fogaça de Souza,

Conforme combinado, foi agendada reunião via Teams para hoje, 24/11/2026, às 15h30, para validarmos em conjunto o teste da funcionalidade de Exportação de Base. Como não houve participação na sala, não foi possível realizar a validação.

Resumo da análise:
- O erro HTTP 504 Gateway Timeout ocorria sempre em aproximadamente 120 segundos, conforme registrado nos logs do Apache (caddeapllx137/138), nas ocorrências de 09, 10, 17, 18 e 23/11/2026, no endpoint /csc-api/cessaocarteiras/v1/baseelegiveis/exportarbase/108/arquivo/excel/etapa/0.
- O timeout era aplicado pelo Apache/mod_cluster, que encerrava a espera pela resposta do JBoss (caddeapllx765) após 120 segundos, enquanto a aplicação ainda processava a requisição.
- Foi aplicado ajuste no JBoss do ambiente TQS (caddeapllx765), definindo o node-timeout do mod_cluster para 600 segundos (10 minutos), alinhado aos timeouts já configurados na Route OpenShift e no frontend.

Solicitamos que seja realizado novo teste da Exportação de Base no ambiente TQS (https://sigec-csc-frontend-tqs.apps.nprd.caixa) e que o resultado seja registrado nesta requisição, informando o horário do teste e se a exportação foi concluída com sucesso.

Observação: o ajuste amplia o tempo de espera, mas não reduz o tempo de processamento da exportação. Recomendamos que a equipe de desenvolvimento avalie a performance das consultas envolvidas (conforme análise iniciada em sala) e, se possível, a adoção de exportação assíncrona.

A requisição permanecerá pendente aguardando o retorno do teste.

Atenciosamente,
Jessé Batista
Analista CTIS / CESTI – Esteira DevOps DES TQS NPRD
