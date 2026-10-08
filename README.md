Confirmado pelo histórico: o custom.sh estava sem alterações desde 08/02/2025 (última execução com sucesso, commit ec5d9232) e recebeu três commits do Dyego dos Santos Barros na segunda (05/10). A release passou a falhar a partir deles. A falha está no comando final de montagem do Azure Blob (stgsiopivendasonline), cujo endpoint não é acessível pela rede NPRD.

Sugestões:

Alinhar com o Dyego o objetivo da alteração. Se o mount do Blob não for necessário em DES, restaurar o conteúdo do commit ec5d9232.
Para restabelecer o serviço de imediato, ajustar o bloco de montagem para não interromper o deploy em caso de falha (segue trecho sugerido).

Se a montagem do Blob for necessária em DES, nos avisem para encaminharmos a liberação de rede ao time de Nuvem.
