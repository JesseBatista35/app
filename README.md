Prezados,

A criação de novos projetos e módulos na esteira DevOps é feita pelo próprio solicitante, no InfraFácil. O processo é automatizado e entrega o repositório, a pipeline e a release em devops.caixa.

Para criar o SIGSJ-deposito-retencao:

Acesse Ambientes ➝ Esteiras DevOps ➝ Novo Projeto.
Informe o sistema SIGSJ. Ele precisa estar registrado no SIPGC.
Clique em Incluir Módulo, informe SIGSJ-deposito-retencao e clique em Criar Módulo.
Clique em Configurar Módulo, selecione o tipo (Online/Batch) e a tecnologia (ex.: JBoss 7.4 VM, Quarkus, Spring, Angular) e vincule o módulo.
Selecione o grupo (squad) e a comunidade. Se não encontrar o grupo, procure a CESTI36. Se não encontrar a comunidade, procure a CESTI35.
Confira o resumo e clique em Solicitar.

Depois da criação, a primeira pipeline precisa ser executada. É ela que aloca o IP/hostname e cria a VM ou o container. Só depois disso o módulo aparece no InfraFácil.

O passo a passo completo está na Wiki: https://wikifacil.caixa/article/esteira-devops/criacao-e-consulta-de-modulo

Encerro a demanda. Se ocorrer algum erro durante a criação ou na primeira execução da pipeline, abram um novo chamado.

Atenciosamente,
Jessé Batista – CESTI / Esteiras DevOps
