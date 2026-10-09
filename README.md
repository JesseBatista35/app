
-sh-4.2$ oc debug node/ceadecldlx026.nprd.caixa
error: cannot debug ceadecldlx026.nprd.caixa: unable to extract pod template from type *v1.Node
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ chroot /host
chroot: não foi possível mudar o diretório raiz para /host: Arquivo ou diretório não encontrado
-sh-4.2$
-sh-4.2$
-sh-4.2$
-sh-4.2$ timeout 5 bash -c '</dev/tcp/10.116.100.127/1433' && echo OK || echo FALHOU
OK
-sh-4.2$
