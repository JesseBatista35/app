RETIFICAÇÃO – erro monitdbadm no passo "Configurando Stack de Monitoração" (esteira-jboss-vm)

Pessoal, retificando a mensagem anterior: o problema não é da CEPRO20 nem de senha expirada no banco. Desconsiderem a orientação de encaminhar para lá.

Causa real
A Microsoft alterou o ambiente de monitoração no Azure, que deixou de usar IP fixo e passou a usar FQDN. O modelo Terraform já foi ajustado e está funcionando. O modelo antigo, Ansible (esteira-jboss-vm), ainda não foi adequado. Ele tem particularidades, como o usuário monitdbadm, que não existem no Terraform. Além disso, a correção no modelo antigo não é replicada via git: precisa ser feita manualmente em cada agente (são cerca de 12). O Jailson e o Arnaldo estão trabalhando na correção.

Paliativo aplicado (autorizado por Flávio Gagliardi e Mário Marinho)
Foi habilitado o "Continue on error" na task "Configurando Stack de Monitoração" do task group global.

O passo ainda mostra o erro (em vermelho), mas a release segue e conclui como parcialmente concluída.
O deploy da aplicação não é afetado. Já validado com SIRTA e SIGPD-backend.
Releases no modelo Terraform continuam funcionando normalmente.

Para demandas com esse erro

Peçam ao solicitante para reexecutar a release. Agora ela deve concluir.
Expliquem que o erro no passo de monitoração é conhecido e está em manutenção pelo time de suporte da esteira. A aplicação é implantada normalmente.
Não encaminhem para DBA nem para CEPRO.
Referência: WO0000081840070. Ela fica pendente até a correção definitiva (orientação do Flávio). Dúvidas ou insistência, acionem o Flávio Gagliardi.

Para demandas reclamando do status "Partially succeeded"
Esse status é esperado enquanto o paliativo estiver ativo. Ele aparece por causa do erro conhecido no passo de monitoração, e não indica falha no deploy da aplicação. Informem ao solicitante que o time de suporte da esteira já está trabalhando na solução definitiva e que, após a correção, as releases voltarão a concluir com sucesso total, sem ação do lado dele. Referenciem a WO0000081840070.

Recomendação: sempre que possível, orientem a migração das aplicações para o modelo Terraform. O modelo Ansible antigo está sendo descontinuado.
