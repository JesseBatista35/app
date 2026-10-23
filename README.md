Prezados,

A demanda foi analisada e corrigida, sem necessidade de recriar o repositório.

Causa raiz:
A renomeação do repositório pela jornada FusionX (de siplx-api-plataforma-geracao-relatorios para siplx-plataforma-geracao-relatorios) deixou referências ao nome anterior em dois pontos:

GitOps central. A estrutura ainda correspondia ao nome antigo, o que fazia o cloud_provider chegar vazio ao build e impedia a sincronização no ArgoCD. A estrutura foi ajustada para o nome atual.
Host do Gateway Istio no repositório infranprd (des/values.yaml). O host continuava como siplx-api-plataforma-geracao-relatorios.apl.des.private.azure. Por isso, o external-dns do cluster aks-plx-nprd registrou o DNS com o nome antigo, e a etapa de publicação no APIM falhava por não resolver o novo endereço.

Ações realizadas:

Incluído no des/values.yaml do repositório siplx-plataforma-geracao-relatorios-infranprd o host siplx-plataforma-geracao-relatorios.apl.des.private.azure. O host antigo foi mantido por compatibilidade.
Ajustado o appName do topologySpreadConstraints para o nome atual da aplicação.

Validação:
Pipeline executada com sucesso (run #13 – 39978455325), com todas as etapas concluídas:

Validação e build da imagem, publicada no ACR acrcentralcaixanprd.
Deploy e sincronização via ArgoCD no cluster aks-plx-nprd, namespace siplx-plataforma-geracao-relatorios, com a aplicação saudável.
Publicação da API no APIM.

Observações:

A infraestrutura do projeto está provisionada na Azure (assinatura “Loterias - SIPLX - NPRD”), e o projeto está configurado para esse ambiente. Uma eventual migração para AWS deve ser avaliada pela comunidade responsável e tratada em nova demanda.
O arquivo ci_cd_variables.yaml do repositório da aplicação ainda contém um placeholder do template (“Informe o nome da variavel…”). Recomendamos que a equipe de desenvolvimento faça o ajuste.
Caso o owner do projeto ainda esteja divergente, o ajuste deve ser feito no catálogo do repositório (catalog-info.yaml) ou junto aos administradores da organização no GitHub.

Dessa forma, encerramos a demanda.

Atenciosamente,
Jessé Batista – Esteira DevOps NPRD
