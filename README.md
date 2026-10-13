# 1. A rede continua de pé? (descarta reversão da placa)
arping -c3 -I ens224 10.188.0.16
ip route get 10.188.0.16

# 2. As portas respondem?
rpcinfo -p 10.188.0.16 | grep -E "nfs|mountd"
timeout 5 bash -c '</dev/tcp/10.188.0.16/2049' && echo "2049 OK" || echo "2049 FALHOU"

# 3. Montagem manual com detalhe, testando versões
mount -v -t nfs -o vers=3 hypernprd12.ad.caixa:/fs_siccv /mnt; umount /mnt 2>/dev/null
mount -v -t nfs -o vers=4.1 hypernprd12.ad.caixa:/fs_siccv /mnt; umount /mnt 2>/dev/null
