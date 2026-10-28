2. Testar o export direto num nó antes de criar o PV

bash
# pega um nó worker qualquer
oc get nodes -l node-role.kubernetes.io/worker

oc debug node/<nome-do-no>
# dentro do debug:
chroot /host
showmount -e nprdnfs01.ad.caixa        # /fs_sisib deve aparecer
mkdir -p /tmp/teste-sisib
mount -t nfs -o vers=3 nprdnfs01.ad.caixa:/fs_sisib /tmp/teste-sisib
touch /tmp/teste-sisib/teste_jesse && ls -l /tmp/teste-sisib
rm /tmp/teste-sisib/teste_jesse
umount /tmp/teste-sisib
exit; exit


<img width="1381" height="791" alt="image" src="https://github.com/user-attachments/assets/559b7bdb-3425-4f32-8a90-9a2007dee876" />
