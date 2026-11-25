Prezados,

Informamos que o erro HTTP 504 Gateway Timeout na funcionalidade de Exportação de Base do SIGEC-CSC foi corrigido.

Causa raiz:
O backend do SIGEC-CSC é publicado através do Apache (caddeapllx137/138) com balanceamento via mod_cluster para o JBoss (caddeapllx765). O JBoss não possuía o parâmetro node-timeout configurado no subsystem modcluster. Com isso, o Apache aplicava o timeout padrão global de 120 segundos e encerrava a espera pela resposta do JBoss enquanto a aplicação ainda processava a exportação. As evidências constam nos logs do Apache (erro AH00878 – read response failed / timeout specified has expired), nas ocorrências de 09, 10, 17, 18 e 23/11/2026, todas com duração de aproximadamente 120 segundos.

Correção aplicada:
Configurado o parâmetro node-timeout=600 (10 minutos) no subsystem modcluster do JBoss, alinhado aos timeouts já existentes na Route OpenShift e no frontend (nginx). O ajuste é específico do SIGEC-CSC e não altera a configuração compartilhada do Apache.

Validação:
Testes realizados nos ambientes DES e TQS com sucesso, incluindo downloads de arquivos grandes com tempo de processamento superior a 2 minutos.

Recomendação:
O ajuste amplia o tempo de espera, mas não reduz o tempo de processamento. Recomendamos que a equipe de desenvolvimento avalie a performance das consultas envolvidas na exportação (conforme análise iniciada em sala) e, se possível, adote exportação assíncrona, evitando que requisições muito longas voltem a atingir limites de timeout.

Diante do exposto, a demanda está sendo encerrada.

Atenciosamente,
Jessé Batista
Analista CTIS / CESTI – Esteira DevOps DES TQS NPRD
