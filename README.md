Há três conexões persistentes da sansbp01, e não só a das 11:08. Duas delas são de 23/10, sobras de deploys de cinco dias atrás que nunca foram fechadas. Isso explica a release “travada desde ontem”: o agente fica reaproveitando conexões mestre velhas do ControlPersist, e alguma delas está num estado inconsistente.

Para limpar:

Cancele a release 66 primeiro, para não matar a conexão no meio de um passo.
Derrube as três sessões matando o [priv] de cada uma (os filhos caem junto):
bash
sudo kill 54198 65770 126599
ps -ef --forest | grep -E "sshd: sansbp01" | grep -v grep   # deve vir vazio
Faça o redeploy do EC DES e confira se o agente abriu uma conexão nova:
bash
sudo grep "Accepted" /var/log/secure | grep sansbp01 | tail -3

Do lado do agente (10.122.155.64), o socket de controle morre junto com a conexão. O Ansible vai abrir uma nova na próxima task.

Se passar, vale avisar os responsáveis pelo pool de agentes. Há conexões ControlPersist sobrevivendo por dias, provavelmente pelo ControlPersist muito alto no ansible.cfg ou por ssh órfão de execuções canceladas. Isso deve estar afetando outras VMs da esteira-jboss-vm-v2 também.
