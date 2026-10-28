
[p585600@caddeapllx2651 ~]$ ^C
[p585600@caddeapllx2651 ~]$ mount | grep siccp
hypernprd12.ad.caixa:/fs_siccp on /siccp type nfs4 (rw,relatime,sync,vers=4.2,rsize=262144,wsize=262144,namlen=255,hard,proto=tcp,timeo=600,retrans=2,sec=sys,clientaddr=10.188.6.241,local_lock=none,addr=10.188.0.12)
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ timeout 5 stat /siccp; echo "rc=$?"
    Arquivo: /siccp
    Tamanho: 4096       Blocos: 8          bloco de E/S: 262144 diretório
Dispositivo: 2dh/45d    Inode: 65          Links: 11
     Acesso: (0777/drwxrwxrwx)  Uid: (20006048/sccpdr01)   Gid: (30000018/controlm)
     Acesso: 2026-10-16 11:16:48.420148080 -0300
Modificação: 2026-10-20 08:42:20.926461990 -0300
  Alteração: 2026-10-23 11:13:00.995316090 -0300
    Criação: -
rc=0
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ imeout 5 df -h /siccp; echo "rc=$?"
-sh: imeout: comando não encontrado
rc=127
[p585600@caddeapllx2651 ~]$ timeout 5 df -h /siccp; echo "rc=$?"
Sist. Arq.                      Tam. Usado Disp. Uso% Montado em
hypernprd12.ad.caixa:/fs_siccp   50G  3,3M   50G   1% /siccp
rc=0
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ ps -eo pid,stat,cmd | awk '$2 ~ /D/'
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$
[p585600@caddeapllx2651 ~]$ rpcinfo -t hypernprd12.ad.caixa nfs
program 100003 version 3 ready and waiting
program 100003 version 4 ready and waiting
[p585600@caddeapllx2651 ~]$ showmount -e hypernprd12.ad.caixa | grep siccp
/fs_siccp                          10.188.6.241,10.188.6.230
[p585600@caddeapllx2651 ~]$
