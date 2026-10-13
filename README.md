Você está na lista de variáveis da release. Falta adicionar as duas novas.

No canto superior direito, clique em Edit. Se já estiver no modo de edição, pule este passo.
Abra a aba Variables → Pipeline variables.
No final da lista, clique em + Add e preencha:
Name: TERRAFORM_ESX_NETWORK_BCK
Value: tn-BACKUP|BACKUP-NPRD-ap|BACKUP-NPRD-ep
Scope (combo à direita da linha): EC TQS
Clique em + Add de novo:
Name: TERRAFORM_VM_IPNETMASK_BCK
Value: 16
Scope: EC TQS
Clique em Save (canto superior direito), com um comentário, por exemplo: WO0000081801601 - rede backup BACKUP-NPRD p/ hypernprd12.

A variável vm_destroy_before_create aparece vazia na lista. Deixe assim, porque é isso que garante que a VM não seja recriada.

Depois de salvar, siga para o vCenter: Network adapter 2 → tn-BACKUP|BACKUP-NPRD-ap|BACKUP-NPRD-ep.
