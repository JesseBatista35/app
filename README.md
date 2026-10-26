Robson, sobre a iteração aparecer 1 na tela mas executar com 0: isso costuma acontecer quando a correção é feita só no Designer/numa instância que já estava ordenada — ela não é aplicada retroativamente. Pode tentar isso:

Confirma se o campo “Iterations Range Attribute” é um valor fixo ou se referencia uma variável/parâmetro. Se for variável, verifica se ela está definida como 0 na aba Variables da pasta (Planning).
Depois de ajustar e salvar no Designer, salva/atualiza a pasta (Folder) na Planning também.
Faz um Order novo da pasta (não um Rerun de uma instância que já existia) — só assim o job pega o valor de iteração atualizado.

Testa assim e manda o log de novo.
