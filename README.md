Oi Iury, boa tarde! Tudo bem?

Para o ajuste, pode abrir uma nova REQ do mesmo tipo da anterior (“Ajustar ambiente ou parametrização de software”, ambiente DES) para o SIMIL-precificacao-rotinas-batch, citando a REQ000146916154 como referência. Na descrição, pode colocar:

Ajuste da configuração do agente Control-M no servidor caddeapllx2501 para apontar ao servidor do BR DES - Negocial (hoje está apontando para o crjdeaprlx038, que não está mais acessível).
Ajuste do arquivo etc/hosts-des do repositório SIMIL-precificacao-rotinas-batch-config. Hoje ele tem as entradas comentadas e aponta para o servidor antigo.
Validação da comunicação do agente e do cadastro dele no servidor Control-M.

Obrigado pela referência do SISME-rotinas. Como o SIMIL foi criado a partir dele, a configuração antiga provavelmente veio junto, e vou levar isso em conta no ajuste.
