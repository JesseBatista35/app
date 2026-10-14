Prezados,

Concluímos a análise e o ajuste do ambiente do SIMCN em DES (JBoss EAP domain, Domain Controller 10.116.89.0, server-group simcn).

Causa raiz:
O deploy via Jenkins (step_deploy_git.sh) falhava sem substituir o pacote. O undeploy da versão anterior era recusado pelo domain com WFLYCTL0063 (rollback) e, em seguida, o deploy da nova versão era rejeitado porque o conteúdo SIMCN já existia no repositório. Com isso, a versão antiga (b2260) permanecia ativa e as alterações não eram refletidas, o que exigia remoção manual do .ear e limpeza de cache.

O rollback era causado pelo host sbrdeapllx112, que fazia parte do domain com server-configs padrão de instalação (server-one e server-two) apontando para server-groups inexistentes (main-server-group e other-server-group). Isso tornava o modelo do host inválido (WFLYCTL0369) e bloqueava qualquer operação de deploy/undeploy no domain.

Ações realizadas:

Removidos os server-configs padrão server-one e server-two do host sbrdeapllx112. Ambos estavam parados e não eram utilizados.
Removido o deployment antigo SIMCN do server-group e do repositório de conteúdo.
Implantado o pacote enviado pela equipe: simcn-ear-2.26.3.4.0-20261013.113320-7.ear (name SIMCN, enabled).

Situação atual:

Deployment SIMCN ativo no server-group simcn (servidor simcn_node1_lx103), com o runtime-name acima.
Aplicação respondendo em https://conciliacao.des.caixa/simcn-web/, com redirecionamento para o login DES – INTRANET.
