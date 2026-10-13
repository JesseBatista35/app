[root@caddeapllx2821 p585600]# arping -c3 -I ens224 10.188.0.16
ARPING 10.188.0.16 de 10.188.6.225 ens224
Enviadas 3 sondas (3 broadcast(s))
Recebida(s) 0 resposta(s)
[root@caddeapllx2821 p585600]# ip route get 10.188.0.16
10.188.0.16 dev ens224 src 10.188.6.225 uid 0
    cache
[root@caddeapllx2821 p585600]#
[root@caddeapllx2821 p585600]#
[root@caddeapllx2821 p585600]# rpcinfo -p 10.188.0.16 | grep -E "nfs|mountd"
10.188.0.16: RPC: Remote system error - No route to host
[root@caddeapllx2821 p585600]#
[root@caddeapllx2821 p585600]#
[root@caddeapllx2821 p585600]# timeout 5 bash -c '</dev/tcp/10.188.0.16/2049' && echo "2049 OK" || echo "2049 FALHOU"
bash: connect: Não há rota para o host
bash: linha 1: /dev/tcp/10.188.0.16/2049: Não há rota para o host
2049 FALHOU
[root@caddeapllx2821 p585600]#
[root@caddeapllx2821 p585600]#
[root@caddeapllx2821 p585600]#
[root@caddeapllx2821 p585600]# mount -v -t nfs -o vers=3 hypernprd12.ad.caixa:/fs_siccv /mnt; umount /mnt 2>/dev/null
mount.nfs: timeout set for Tue Oct 13 16:16:49 2026
Created symlink /run/systemd/system/remote-fs.target.wants/rpc-statd.service → /usr/lib/systemd/system/rpc-statd.service.
mount.nfs: trying text-based options 'vers=3,addr=10.188.0.16'
mount.nfs: prog 100003, trying vers=3, prot=6
mount.nfs: portmap query failed: RPC: Remote system error - No route to host
mount.nfs: trying text-based options 'vers=3,addr=10.188.0.16'
mount.nfs: prog 100003, trying vers=3, prot=6
mount.nfs: portmap query failed: RPC: Remote system error - No route to host
mount.nfs: trying text-based options 'vers=3,addr=10.188.0.16'
mount.nfs: prog 100003, trying vers=3, prot=6
mount.nfs: portmap query failed: RPC: Remote system error - No route to host
mount.nfs: trying text-based options 'vers=3,addr=10.188.0.16'
mount.nfs: prog 100003, trying vers=3, prot=6
mount.nfs: portmap query failed: RPC: Remote system error - No route to host
mount.nfs: trying text-based options 'vers=3,addr=10.188.0.16'
mount.nfs: prog 100003, trying vers=3, prot=6
mount.nfs: portmap query failed: RPC: Remote system error - No route to host
mount.nfs: trying text-based options 'vers=3,addr=10.188.0.16'
mount.nfs: prog 100003, trying vers=3, prot=6
mount.nfs: portmap query failed: RPC: Remote system error - No route to host
mount.nfs: trying text-based options 'vers=3,addr=10.188.0.16'
mount.nfs: prog 100003, trying vers=3, prot=6
mount.nfs: portmap query failed: RPC: Remote system error - No route to host
^C
[root@caddeapllx2821 p585600]# mount -v -t nfs -o vers=4.1 hypernprd12.ad.caixa:/fs_siccv /mnt; umount /mnt 2>/dev/null
mount.nfs: timeout set for Tue Oct 13 16:17:53 2026
mount.nfs: trying text-based options 'vers=4.1,addr=10.188.0.14,clientaddr=10.188.6.225'
mount.nfs: mount(2): No route to host
mount.nfs: trying text-based options 'vers=4.1,addr=10.188.0.14,clientaddr=10.188.6.225'
mount.nfs: mount(2): No route to host
mount.nfs: trying text-based options 'vers=4.1,addr=10.188.0.14,clientaddr=10.188.6.225'
mount.nfs: mount(2): No route to host
mount.nfs: trying text-based options 'vers=4.1,addr=10.188.0.14,clientaddr=10.188.6.225'
mount.nfs: mount(2): No route to host

