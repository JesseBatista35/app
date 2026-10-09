oc debug node/ceadecldlx026.nprd.caixa
chroot /host
timeout 5 bash -c '</dev/tcp/10.116.100.127/1433' && echo OK || echo FALHOU
